---
layout: post
title:  Drill Through
description:  drill through
platform: js
control: PivotGrid
documentation: ug
api: /api/js/ejpivotgrid
---

# Drill Through

Drill-through retrieves the raw items that are used to create a specific cell. To enable drill-through support, set [`enableDrillThrough`](/api/js/ejpivotgrid#members:enableDrillThrough) property to true. Raw items are obtained through the [`drillThrough`](/api/js/ejpivotgrid#events:drillthrough) event, using which user can bind them to an external widget for precise view. 

## OLAP

N> Drill-through is supported in PivotGrid only when we configure and enable drill-through action at the Cube. 

![](DrillThrough_images/pivotgrid.png)

On clicking any value cell, the "Drill Through Information" dialog will be opened.  It consists of a Grid with data which are associated with the measure values of clicked value cell. In this example, the measure behind the respective cell is “Sales Amount” and the values of the dimensions which are associated with this measure are alone displayed in the Grid. 

![](DrillThrough_images/DrillThroughData.png)

On clicking the "Hierarchy Selector" button which is displayed below the Grid, the "Hierarchy Selector" dialog will be opened. It consists of the dimensions which are associated with the measure of the clicked value cell. In this example, the measure behind the respective cell is “Sales Amount” and the dimensions associated with this measure are alone displayed in the dialog.   

![](DrillThrough_images/hierarchy_selector.png)

By dragging and dropping the respective hierarchies and finally clicking “OK” button, drill through MDX query will be framed and executed internally and provides back the raw items through "drillThrough" event. In this example, we have bound the raw items obtained to our ejGrid widget. Please refer the code sample and screen-shot below.

## Client Mode

{% highlight html %}

<!--Create a tag which acts as a container for PivotGrid-->
<div id="PivotGrid1"></div>

<script type="text/javascript">
    $(function() {
        $("#PivotGrid1").ejPivotGrid({
            //...
            enableDrillThrough : true, drillThrough: "drilledData"
        });
    });

    function drilledData(args) {
        $(".e-dialog, .clientDialog, .tableDlg").remove();
        gridData = JSON.parse(args.data);
        var dialogContent = ej.buildTag("div#" + this._id + "_tableDlg.tableDlg", $("<div id=\"Grid1\"></div>"))[0].outerHTML;
        var dialogFooter = ej.buildTag("div", ej.buildTag("button#btnOK.dialogBtnOK", "Hierarchy Selector")[0].outerHTML, { "float": "right", "margin": "-5px 0 6px" })[0].outerHTML
        ejDialog = ej.buildTag("div#clientDialog.clientDialog", dialogContent + dialogFooter, { "opacity": "1" }).attr("title", "Drill Through Information")[0].outerHTML;
        $(ejDialog).appendTo("#" + this._id);
        $("#btnOK").ejButton().css({ margin: "30px 0 20px 0" });
        $("#Grid1").ejGrid({
            dataSource: gridData,
            allowPaging: true,
            allowTextWrap: true,
            pageSettings: { pageSize: 8 }
        });
        this.element.find(".clientDialog").ejDialog({ width: "70%", content: "#" + this._id, enableResize: false, close: ej.proxy(ej.Pivot.closePreventPanel, this) });
        var pivotGrid = $("#" + this._id).data("ejPivotGrid");
        $("#btnOK").click(function () {
            ej.Pivot.openHierarchySelector(pivotGrid);
        });
    }
</script>

{% endhighlight %}

## Server Mode

{% highlight html %}

<!--Create a tag which acts as a container for PivotGrid-->
<div id="PivotGrid1"></div>

<script type="text/javascript">
    $(function() {
        $("#PivotGrid1").ejPivotGrid({
            //...
            enableDrillThrough : true, drillThrough: "drilledData"
        });
    });

    function drilledData(args) {
        $(".e-dialog, .clientDialog, .tableDlg").remove();
		gridData = ej.isNullOrUndefined(args.data.d) ? JSON.parse(args.data.DrillDataTable) : JSON.parse(args.data.d[1].Value);
        var dialogContent = ej.buildTag("div#" + this._id + "_tableDlg.tableDlg", $("<div id=\"Grid1\"></div>"))[0].outerHTML;
        var dialogFooter = ej.buildTag("div", ej.buildTag("button#btnOK.dialogBtnOK", "Hierarchy Selector")[0].outerHTML, { "float": "right", "margin": "-5px 0 6px" })[0].outerHTML
        ejDialog = ej.buildTag("div#clientDialog.clientDialog", dialogContent + dialogFooter, { "opacity": "1" }).attr("title", "Drill Through Information")[0].outerHTML;
        $(ejDialog).appendTo("#" + this._id);
        $("#btnOK").ejButton().css({ margin: "30px 0 20px 0" });
        $("#Grid1").ejGrid({
            dataSource: gridData,
            allowPaging: true,
            allowTextWrap: true,
            pageSettings: { pageSize: 8 }
        });
        this.element.find(".clientDialog").ejDialog({ width: "70%", content: "#" + this._id, enableResize: false, close: ej.proxy(ej.Pivot.closePreventPanel, this) });
        var pivotGrid = this;
        $("#btnOK").click(function () {
            $(".e-dialog, .clientDialog, .tableDlg").remove();
            if (pivotGrid.model.operationalMode == ej.PivotGrid.OperationalMode.ServerMode) {
                pivotGrid._waitingPopup.show()
                pivotGrid.doAjaxPost("POST", pivotGrid.model.url + "/" + pivotGrid.model.serviceMethodSettings.drillThroughHierarchies, JSON.stringify({ "currentReport": JSON.parse(pivotGrid.getOlapReport()).Report, "layout": pivotGrid.model.layout, "cellPos": "", "customObject": JSON.stringify(pivotGrid.model.customObject) }), function (args) {
                    ej.Pivot.openHierarchySelector(pivotGrid, args);
                })
            }
        });
    }
</script>

{% endhighlight %}

When PivotGrid is rendered in server mode, below service methods need to be added in WCF/WebAPI for drill through operation.

For WebAPI controller, the below methods need to be added.

{% highlight c# %}

[System.Web.Http.ActionName("DrillThroughHierarchies")]
[System.Web.Http.HttpPost]
public string DrillThroughHierarchies(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);              
    DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
    return htmlHelper.DrillthroughHierarchies(DataManager, jsonResult["layout"].ToString(), jsonResult["cellPos"].ToString());
}

[System.Web.Http.ActionName("DrillThroughDataTable")]
[System.Web.Http.HttpPost]
public Dictionary<string, object> DrillThroughDataTable(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
    return htmlHelper.DrillthroughDataTable(DataManager, jsonResult["layout"].ToString(), jsonResult["cellPos"].ToString(), jsonResult["selector"].ToString());
}  

{% endhighlight %}

For WCF service, the below methods need to be added. 

{% highlight c# %}

public string DrillThroughHierarchies(string currentReport, string layout, string cellPos)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(currentReport));
    return htmlHelper.DrillthroughHierarchies(DataManager, layout, cellPos);
}

public Dictionary<string, object> DrillThroughDataTable(string currentReport, string layout, string cellPos, string selector)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(currentReport));
    return htmlHelper.DrillthroughDataTable(DataManager, layout, cellPos, selector);
}

{% endhighlight %}

![](DrillThrough_images/drill_data.png)

## Relational

To enable drill-through support, set [`enableDrillThrough`](/api/js/ejpivotgrid#members:enableDrillThrough) property to true. Raw items are obtained through the [`drillThrough`](/api/js/ejpivotgrid#events:drillthrough) event.

{% highlight html %}

<script type="text/javascript">
    $(function() {
        $("#PivotGrid1").ejPivotGrid({
            //...
            enableDrillThrough : true, drillThrough: "drillData"
        });
    });

function drillData(args) {
    gridData = args.selectedData;
    var dialogContent = ej.buildTag("div#Grid1", {height:"50px"})[0].outerHTML;
    ejDialog = ej.buildTag("div#clientDialog.clientDialog", dialogContent, { "opacity": "1" }).attr("title", "Drill Through Information")[0].outerHTML;
    $(ejDialog).appendTo("#" + this._id);
    this.element.find(".clientDialog").ejDialog({ width: "70%", height: "100%", content: "#" + this._id, enableResize: false, close: ej.proxy(ej.Pivot.closePreventPanel, this) });
        
    $("#Grid1").ejGrid({
        dataSource: gridData,
    });
}
</script>

{% endhighlight %}

![](DrillThrough_images/DrillThroughRelational.png)