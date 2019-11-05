---
layout: post
title:  Drill Through with PivotClient widget for Syncfusion Essential JS
description:  This document explains that how to define drill through feature with respective to the modes in JavaScript PivotClient control
platform: js
control: PivotClient
documentation: ug
api: /api/js/ejpivotclient
---

# Drill Through

## OLAP

The drill-through retrieves raw items that are used to create a specified cell of the pivot grid. To enable drill-through support, set [`enableDrillThrough`](/api/js/ejpivotclient#members:enabledrillthrough) property to true. Raw items are obtained through the [`drillThrough`](/api/js/ejpivotclient#events:drillthrough) event, using which user can bind them to an external widget for precise view.

N> The drill-through is supported in the pivot grid only when you configure and enable the drill-through action at the cube.

![DrillThrough support in JavaScript pivot client control](DrillThrough_images/pivotclient.png)

On clicking any value cell, the "Drill Through Information" dialog will be opened. It consists of grid with data which are associated with the measure values of the clicked value cell. In this example, the measure behind the respective cell is “Sales Amount” and the values of the dimensions which are associated with this measure are alone displayed in the grid.

![DrillThrough data in JavaScript pivot client control](DrillThrough_images/DrillThroughData.png)

On clicking the "Hierarchy Selector" button which is displayed below the Grid, the "Hierarchy Selector" dialog will be opened. It consists of dimensions that are associated with the measure of clicked value cell. In this example, the measure behind the respective cell is “Sales Amount” and the dimensions associated with this measure are alone displayed in the dialog.

![Hierarchy selector in JavaScript pivot client control](DrillThrough_images/hierarchy_selector.png)

By dragging and dropping the respective hierarchies and click “OK”, the drill through MDX query will be framed and executed internally, and it provides the raw items back through the "drillThrough" event. In this example, the obtained raw items were bound to the ejGrid widget. Please refer the following code sample and screenshot:

## Client mode

{% highlight html %}

<!--Create a tag which acts as a container for PivotClient-->
<div id="PivotClient1"></div>

<script type="text/javascript">
    $(function() {
        $("#PivotClient1").ejPivotClient({
            //...
            enableDrillThrough : true, drillThrough: "drilledData"
        });
    });
    function drilledData(args) {
        $(".e-dialog, .e-clientDialog, .e-tableDlg").remove();
        gridData = JSON.parse(args.data);
        var dialogContent = ej.buildTag("div#" + this._id + "_tableDlg.e-tableDlg", $("<div id=\"Grid1\"></div>"))[0].outerHTML;
        var dialogFooter = ej.buildTag("div", ej.buildTag("button#btnOK.e-dialogBtnOK", "Hierarchy Selector")[0].outerHTML, { "float": "right", "margin": "-5px 0 6px" })[0].outerHTML
        ejDialog = ej.buildTag("div#clientDialog.e-clientDialog", dialogContent + dialogFooter, { "opacity": "1" }).attr("title", "Drill Through Information")[0].outerHTML;
        $(ejDialog).appendTo("#" + this._id);
        $("#btnOK").ejButton().css({ margin: "30px 0 20px 0" });
        $("#Grid1").ejGrid({
            dataSource: gridData,
            allowPaging: true,
            allowTextWrap: true,
            pageSettings: { pageSize: 8 }
        });
        this.element.find(".e-clientDialog").ejDialog({ width: "70%", content: "#" + this._id, enableResize: false, close: ej.proxy(ej.Pivot.closePreventPanel, this) });
        var pivotClient = $("#" + this._id).data("ejPivotClient");
        $("#btnOK").click(function () {
            ej.Pivot.openHierarchySelector(pivotClient);
        });
    }
</script>

{% endhighlight %}

## Server Mode

{% highlight html %}

<!--Create a tag which acts as a container for PivotClient-->
<div id="PivotClient1"></div>

<script type="text/javascript">
    $(function() {
        $("#PivotClient1").ejPivotClient({
            //...
            enableDrillThrough : true, drillThrough: "drilledData"
        });
    });
    function drilledData(args) {
        $(".e-dialog, .e-clientDialog, .e-tableDlg").remove();
        gridData = ej.isNullOrUndefined(args.data.d) ? JSON.parse(args.data.DrillDataTable) : JSON.parse(args.data.d[1].Value);
        var dialogContent = ej.buildTag("div#" + this._id + "_tableDlg.e-tableDlg", $("<div id=\"Grid1\"></div>"))[0].outerHTML;
        var dialogFooter = ej.buildTag("div", ej.buildTag("button#btnOK.e-dialogBtnOK", "Hierarchy Selector")[0].outerHTML, { "float": "right", "margin": "-5px 0 6px" })[0].outerHTML
        ejDialog = ej.buildTag("div#clientDialog.e-clientDialog", dialogContent + dialogFooter, { "opacity": "1" }).attr("title", "Drill Through Information")[0].outerHTML;
        $(ejDialog).appendTo("#" + this._id);
        $("#btnOK").ejButton().css({ margin: "30px 0 20px 0" });
        $("#Grid1").ejGrid({
            dataSource: gridData,
            allowPaging: true,
            allowTextWrap: true,
            pageSettings: { pageSize: 8 }
        });
        this.element.find(".e-clientDialog").ejDialog({ width: "70%", content: "#" + this._id, enableResize: false, close: ej.proxy(ej.Pivot.closePreventPanel, this) });
        var pivotClient = this;
        $("#btnOK").click(function () {
            $(".e-dialog, .e-clientDialog, .e-tableDlg").remove();
            if (pivotClient.model.operationalMode == ej.PivotGrid.OperationalMode.ServerMode) {
                pivotClient._waitingPopup.show()
                pivotClient.doAjaxPost("POST", pivotClient.model.url + "/" + pivotClient.model.serviceMethodSettings.drillThroughHierarchies, JSON.stringify({ "currentReport": pivotClient.currentReport, "layout": pivotClient.model.layout, "cellPos": "", "customObject": JSON.stringify(pivotClient.model.customObject) }), function (args) {
                    ej.Pivot.openHierarchySelector(pivotClient, args);
                })
            }
        });
    }
</script>

{% endhighlight %}

When the pivot client is rendered in the server mode, the following service methods should be added to WCF/WebAPI for the drill through operation.

For WebAPI controller, the following methods should be added.

{% highlight c# %}

[System.Web.Http.ActionName("DrillThroughHierarchies")]
[System.Web.Http.HttpPost]
public string DrillThroughHierarchies(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
    return pivotClientHelper.DrillthroughHierarchies(DataManager, jsonResult["layout"].ToString(), jsonResult["cellPos"].ToString());
}

[System.Web.Http.ActionName("DrillThroughDataTable")]
[System.Web.Http.HttpPost]
public Dictionary<string, object> DrillThroughDataTable(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
    return pivotClientHelper.DrillthroughDataTable(DataManager, jsonResult["layout"].ToString(), jsonResult["cellPos"].ToString(), jsonResult["selector"].ToString());
}

{% endhighlight %}

For WCF service, the following methods should be added.

{% highlight c# %}

public string DrillThroughHierarchies(string currentReport, string layout, string cellPos)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(currentReport));
    return pivotClientHelper.DrillthroughHierarchies(DataManager, layout, cellPos);
}

public Dictionary<string, object> DrillThroughDataTable(string currentReport, string layout, string cellPos, string selector)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(currentReport));
    return pivotClientHelper.DrillthroughDataTable(DataManager, layout, cellPos, selector);
}

{% endhighlight %}


![DrillThrough data in JavaScript pivot client OLAP server mode](DrillThrough_images/drill_data.png)


## Relational

To enable drill-through support, set the [`enableDrillThrough`](/api/js/ejpivotclient#members:enabledrillthrough) property to true. Raw items are obtained through the [`drillThrough`](/api/js/ejpivotclient#events:drillthrough) event.

{% highlight html %}

<script type="text/javascript">

    $(function() {
        $("#PivotClient1").ejPivotClient({
            //...
            enableDrillThrough : true, drillThrough: "drilledData", load: "onLoad"
        });
    });

    function onLoad(args) {
        this.model.analysisMode = "pivot";
    }

    function drilledData(args) {
        gridData = args.selectedData;
        var dialogContent = ej.buildTag("div#Grid", { })[0].outerHTML;
        ejDialog = ej.buildTag("div#clientDialog.e-clientDialog", dialogContent, { "opacity": "1" }).attr("title", "Drill Through Information")[0].outerHTML;
        $(ejDialog).appendTo("#" + this._id);
        this.element.find(".e-clientDialog").ejDialog({ width: "70%", content: "#" + this._id, enableResize: false, close: ej.proxy(ej.Pivot.closePreventPanel, this) });

        $("#Grid").ejGrid({
            dataSource: gridData,
            allowScrolling: true,
            scrollSettings: { width: "85%" },
            allowPaging: true,
            allowResizing: true,
            allowResizeToFit: true,
            pageSettings: {pageSize: 8}
        });
    }
</script>

{% endhighlight %}

![DrillThrough data in JavaScript pivot client relational](DrillThrough_images/relational_drilledData.png)
