---
layout: post
title: Field-List with PivotGrid widget for Syncfusion Essential JS
description: field list
platform: js
control: PivotGrid
documentation: ug
api: /api/js/ejpivotgrid
---

# PivotTable field list

## Initialization
The field list, also known as Pivot Schema Designer, allows you to add, rearrange, filter, and remove fields to show the data in the pivot grid as exactly you want.

Based on the data source and OLAP bound to the pivot grid control, the PivotTable field list will be automatically populated with cube information or field names. The PivotTable field list provides an Excel like appearance and behavior.

To initialize the PivotTable field list, first you should define a “div” tag with an appropriate “id” attribute which acts as a container for the widget. Then, you should initialize the PivotTable field list by using the **“ejPivotSchemaDesigner”** method.

### Client mode

{% highlight html %}

<html>
//...

<body>

<!--Create a tag which acts as a container for PivotGrid-->
    <div id="PivotGrid1" style="width: 55%; height: 670px; overflow: scroll; float: left;"></div>

<!--Create a tag which acts as a container for PivotTable Field List-->
    <div id="PivotSchemaDesigner1" style="height:650px;width:40%;">
    </div>

    <script type="text/javascript">
        $(function() {
            $("#PivotGrid1").ejPivotGrid({
                dataSource: {
                    data: "https://bi.syncfusion.com/olap/msmdpump.dll", //data
                    catalog: "Adventure Works DW 2008 SE",
                    cube: "Adventure Works",
                    rows: [{
                        fieldName: "[Customer].[Customer Geography]"
                    }],
                    columns: [{
                        fieldName: "[Date].[Fiscal]"
                    }],
                    values: [{
                        measures: [{
                            fieldName: "[Measures].[Internet Sales Amount]",
                        }],
                        axis: "columns"
                    }]
                },
                renderSuccess: "RenderFieldList"
            });
        });

        function RenderFieldList(args) {
            $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({
                pivotControl: args,
                layout: ej.PivotSchemaDesigner.Layouts.Excel,
                OLAP: {
                    showKpi: false,
                    showNamedSets: true
                }
            });
        }
    </script>

</body>

</html>

{% endhighlight %}


![Field list in JavaScript pivot grid OLAP client mode](PivotTable-Field-List_images/olapclientfieldlsit.png)


### Server mode

{% highlight html %}

<html>
//...

<body>

<!--Create a tag which acts as a container for PivotGrid-->
    <div id="PivotGrid1" style="width: 55%; height: 670px; overflow: scroll; float: left;"></div>

<!--Create a tag which acts as a container for PivotTable Field List-->
    <div id="PivotSchemaDesigner1" style="height:650px;width:40%;"></div>

    <script type="text/javascript">
        $(function() {
            $("#PivotGrid1").ejPivotGrid({
                url: "/OLAPService",
                afterServiceInvoke: "onServiceInvokes"
            });
        });

        function onServiceInvokes(args) {
            if (args.action == "initialize")
                $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({
                    pivotControl: this,
                    layout: ej.PivotSchemaDesigner.Layouts.Excel
                });
        }
    </script>
</body>

</html>

{% endhighlight %}

![Excel structure of field list in JavaScript pivot grid control](PivotTable-Field-List_images/schema1.png)

N> The [`url`](/api/js/ejpivotschemadesigner#members:url) property is used to connect the service by using the specified URL for any server updates.


## Service Method Settings
The [`serviceMethods`](/api/js/ejpivotschemadesigner#members:servicemethods) allows the user to set custom name for service methods at service-end.

{% highlight html %}

<script type="text/javascript">

$("#PivotSchemaDesigner1").ejPivotSchemaDesigner({

    serviceMethods: { initialize: "InitializeGrid"}

    });

</script>

{% endhighlight %}

The following table will explain the available service methods in the pivot schema designer:

| Service Methods | Description |
|---|---|
|[fetchMembers](/api/js/ejpivotschemadesigner#members:servicemethod-fetchmembers)|It is responsible for getting the values for the tree view in the filter dialog.|
|[filtering](/api/js/ejpivotschemadesigner#members:servicemethod-filtering)|It is responsible for filtering operation in the field list.|
|[memberExpand](/api/js/ejpivotschemadesigner#members:servicemethod-memberexpand)|It is responsible for the server-side action when expanding members in the field list.|
|[nodeDropped](/api/js/ejpivotschemadesigner#members:servicemethod-nodedropped)|It is responsible for the server-side action when dropping a node into the field list.|
|[nodeStateModified](/api/js/ejpivotschemadesigner#members:servicemethod-nodestatemodified)|It is responsible for the server-side action when changing the checked state of a node in the field list.|
|[removeButton](/api/js/ejpivotschemadesigner#members:servicemethod-removebutton)|It is responsible for button removing operation in field list.|

N> The [`customObject`](/api/js/ejpivotschemadesigner#members:customobject) property in pivot schema designer is used to pass additional information between the client-end and the service-end.


## Layout
The top portion of the layout shows field or cube items in a categorized way. They can be dynamically added to the report either by the drag and drop option or through the simple check box selection.

On item(s) selection, they will be placed in the row section except numeric based item(s) or measures, which alone will be placed in the value section, by default.

The bottom portion of the layout is segregated as below:

* Report filter: Filter the item(s) placed in the particular position of the layout.
* Value section: The value label usually displays the numeric value item(s) present in the report.
* Column section: Displays the item(s) as column header and values in the pivot grid control.
* Row section: Display the item(s) as row header and values in the pivot grid control.

### Height of the pivot schema designer
The [`height`](/api/js/ejpivotschemadesigner#members:height) property is used to set the height of the pivot schema designer.

{% highlight html %}

$("#PivotSchemaDesigner1").ejPivotSchemaDesigner({

     height: "630px"

     });

{% endhighlight %}

### Width of the pivot schema designer
The [`width`](/api/js/ejpivotschemadesigner#members:width) property is used to set the width of the pivot schema designer.

{% highlight html %}

$("#PivotSchemaDesigner1").ejPivotSchemaDesigner({

     width: "415px"

     });

{% endhighlight %}

### Types of layout in pivot schema designer
The [`layout`](/api/js/ejpivotschemadesigner#members:layout) property is used to set the layout for pivot schema designer. The following table will explain the available types in pivot schema designer along with the pivot grid.

| Layout | Description |
|---|---|
|Excel|To set the layout as same in the Excel.|
|Normal|To set normal layout for the field list.|

## UI interactions

### By drag and drop

You can alter the report on fly through the drag-and-drop operation. You can drag any item from the field list and drop it into column, row, value, or filter section available at the bottom of the field list.

![Drag and drop in JavaScript field list](PivotTable-Field-List_images/ui-operartion.png)

N> You can enable/disable the drag and drop operation by the [`enableDragDrop`](/api/js/ejpivotschemadesigner#members:enabledragdrop) property.

### By tree view selection

You can also alter the report on fly through the check and uncheck option as an alternate. By default, fields will be added to the row label when checked.

![Filtering in JavaScript field list](PivotTable-Field-List_images/pivotfield.png)

### By context menu

You can also alter the report by using the context menu.

![Context menu in pivot button of JavaScript field list](PivotTable-Field-List_images/Olap_Pivotbutton_Context.png)

![Context menu in tree view elements of JavaScript field list](PivotTable-Field-List_images/Olap_Treeview_Context.png)

## Searching values
Search option in the field list allows you to search a specific value that needs to be filtered from the list of values in the filter pop-up window.

![Tree drop icon in JavaScript field list](PivotTable-Field-List_images/filterclick.png)

![Searching in member editor dialog of JavaScript field list](PivotTable-Field-List_images/search.png)

## Filtering
Values can be filtered by checking/unchecking the check box besides them, in the filter pop-up window. At least, one value should be present in the checked state while filtering. Otherwise “Ok” will be disabled.

![Tree drop icon click in JavaScript field list](PivotTable-Field-List_images/filterclick.png)

![Filtering in member editor dialog of JavaScript field list](PivotTable-Field-List_images/filter.png)

## Defer update
Defer update in the field list allows you to refresh the control on-demand and not during every UI operation. This operation can be enabled/disabled through the [`enableDeferUpdate`](/api/js/ejpivotgrid#members:enabledeferupdate) property internally.

### Showing KPI
The [`showKpi`](/api/js/ejpivotschemadesigner#members:olap-showkpi) property is used to view the KPI elements in tree view in the pivot table field list. This property should be defined under the [`olap`](/api/js/ejpivotschemadesigner#members:olap) object.

{% highlight js %}

<script type="text/javascript">

    $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({

        olap: { showKpi : true }

        });
</script>

{% endhighlight %}

![Key Performance Indicator, aka KPI support in JavaScript pivot schema designer](PivotTable-Field-List_images/kpi.png)

### Showing NamedSets
The [`showNamedSets `](/api/js/ejpivotschemadesigner#members:olap-shownamedsets) property is used to view the named sets in tree view of the pivot table field list. This property should be defined under [`olap`](/api/js/ejpivotschemadesigner#members:olap) object.

{% highlight js %}

<script type="text/javascript">

    $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({

        olap: { showNamedSets : true }

        });
</script>

{% endhighlight %}

## Setting pivot control to pivot schema designer
The [`pivotControl `](/api/js/ejpivotschemadesigner#members:pivotcontrol) property is used to set the pivot control bound with the pivot schema designer.

{% highlight js %}

<script type="text/javascript">

    $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({

        pivotControl: controlObject

        });
</script>

{% endhighlight %}

