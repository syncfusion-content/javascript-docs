---
layout: post
title: Field-List
description: field list
platform: js
control: PivotGrid
documentation: ug
api: /api/js/ejpivotgrid
---

# PivotTable Field List

## Initialization  
Field list, also known as Pivot Schema Designer, allows you to add, rearrange, filter, and remove fields to show the data in PivotGrid as exactly you want.

Based on the datasource and OLAP bound to the PivotGrid control, the PivotTable field list will be automatically populated with cube information or field names. The PivotTable field list provides an Excel like appearance and behavior.

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
                    data: "http://bi.syncfusion.com/olap/msmdpump.dll", //data
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
                    showKPI: false,
                    showNamedSets: true
                }
            });
        }
    </script>

</body>

</html>   

{% endhighlight %}
 

![](PivotTable-Field-List_images/olapclientfieldlsit.png)


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

![](PivotTable-Field-List_images/schema1.png)

## Layout
The top portion of the layout shows field or cube items in a categorized way. They can be dynamically added to the report either by the drag and drop option or through the simple check box selection.
 
On item(s) selection, they will be placed in the row section except numeric based item(s) or measures, which will alone be placed in the value section, by default.
 
The bottom portion of the layout is segregated as below:

* Report filter: Exclusively designed to filter the item(s) placed in the particular position of the layout. 
* Value section: The value label usually displays the numeric value item(s) present in the report.
* Column section: It is used to display the item(s) as column header and values in the PivotGrid control.
* Row section: It is used to display the item(s) as row header and values in the PivotGrid control.

## UI interactions

### By drag and drop

You can alter the report on fly through the drag-and-drop operation. You can drag any item from the field list and drop into column, row, value, or filter section available at the bottom of the field list.

![](PivotTable-Field-List_images/ui-operartion.png)
 
### By Treeview selection
 
You can also alter the report on fly through the check and uncheck option as an alternate. By default, fields will be added to the row label when checked.

![](PivotTable-Field-List_images/pivotfield.png)
 
### By context menu
 
You can also alter the report by using the context menu.

![](PivotTable-Field-List_images/Olap_Pivotbutton_Context.png)

![](PivotTable-Field-List_images/Olap_Treeview_Context.png)

## Searching values
Search option in the field list allows you to search a specific value that needs to be filtered from the list of values in the filter pop-up window.

![](PivotTable-Field-List_images/filterclick.png)

![](PivotTable-Field-List_images/search.png)

## Filtering
Values can be filtered by checking/unchecking the check box besides them, in the filter pop-up window. At least, one value should be present in the checked state while filtering. Otherwise “Ok” will be disabled.

![](PivotTable-Field-List_images/filterclick.png)

![](PivotTable-Field-List_images/filter.png)
