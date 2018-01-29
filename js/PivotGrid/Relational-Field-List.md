---
layout: post
title: Field-List
description: field list
platform: js
control: PivotGrid
documentation: ug
api: /api/js/ejpivotgrid
---

# PivotTable field list

## Initialization
The field list, also known as Pivot Schema Designer, allows you to add, rearrange, filter, and remove fields to show the data in the pivot grid as exactly you want.

Based on the data source and relational bound to the pivot grid control, the PivotTable field list will be automatically populated with the cube information or field names. The PivotTable field list provides an Excel like appearance and behavior.

To initialize the PivotTable field list, first you should define a “div” tag with an appropriate “id” attribute which acts as a container for the widget. Then, you can initialize the PivotTable field list by using the **“ejPivotSchemaDesigner”** method.

### Client mode

{% highlight html %}

<html>
//...

<body>

    <!--Create a tag which acts as a container for PivotGrid-->
    <div id="PivotGrid1" style="width: 55%; height: 670px; overflow: scroll; float: left;"></div>

    <!--Create a tag which acts as a container for PivotTable Field List-->
    <div id="PivotSchemaDesigner1" style="height:650px;width:40%;"></div>

    <script type="text/javascript">

    // Datasource

      $(function() {
        $("#PivotGrid1").ejPivotGrid({
            dataSource: {
                data: pivotData,
                rows: [{
                    fieldName: "Country",
                    fieldCaption: "Country"
                }, {
                    fieldName: "State",
                    fieldCaption: "State"
                }],
                columns: [{
                    fieldName: "Product",
                    fieldCaption: "Product"
                }],
                values: [{
                    fieldName: "Amount",
                    fieldCaption: "Amount"
                }, {
                    fieldName: "Quantity",
                    fieldCaption: "Quantity"
                }],
                filters: [{
                    fieldName: "Date",
                    fieldCaption: "Date"
                }]
            },
            renderSuccess: "RenderFieldList",
        });
    });

    function RenderFieldList(args) {
        $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({
            pivotControl: args,
            layout: ej.PivotSchemaDesigner.Layouts.Excel
        });
    }
    </script>

</body>

</html>

{% endhighlight %}

![](PivotTable-Field-List_images/relationalfieldlist.png)

### Server mode

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
                url: "/RelationalService",
                afterServiceInvoke: "onServiceInvokes"
            });
        });

        function onServiceInvokes(args) {
            //Initialize PivotTable Field List
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

![](PivotTable-Field-List_images/relationalserverfieldlist.png)


## Layout
The top portion of the layout shows field or cube items in a categorized way. They can be dynamically added to the report either by drag and drop option or through the simple check box selection.
 
On item(s) selection, they will be placed in the row section except numeric based item(s) or measures, which will alone be placed in the value section, by default.
 
The bottom portion of the layout is segregated as follows:

* Report filter: Exclusively designed to filter an item(s) placed in the particular position of the layout. 
* Value section: The value label usually displays the numeric value item(s) present in the report.
* Column section: It displays the item(s) as column header and values in the pivot grid control.
* Row section: It displays the item(s) as row header and values in the pivot grid control.

## UI interactions

### By drag and drop

You can alter the report on fly through the drag-and-drop operation. You can drag any item from the field list and drop it into the column, row, value, or filter section available at the bottom of the field list.

![](PivotTable-Field-List_images/ralationaldragndrop.png)

### By drag and drop to grid headers

You can also drag and drop elements from the field list to grid headers.

![](PivotTable-Field-List_images/HeaderDrop.png)

![](PivotTable-Field-List_images/HeaderDrop1.png)

![](PivotTable-Field-List_images/HeaderDrop2.png)

### By tree view selection
 
You can alter the report on fly through the check and uncheck option as an alternate. By default, fields will be added to the row label when checked.

![](PivotTable-Field-List_images/relationalcheckRuncheck.png)

### By context menu

You can also alter the report by using the context menu.

![](PivotTable-Field-List_images/Pivotbutton_Context.png)

![](PivotTable-Field-List_images/Treeview_Context.png)
 
## Searching values
The search option in the field list allows you to search a specific value that needs to be filtered from the list of values in the filter pop-up window.

![](PivotTable-Field-List_images/relationalBfiltering.png)

![](PivotTable-Field-List_images/relationaldialogsearch.png)

## Filtering
Values can be filtered by checking/unchecking the check box besides them, in the filter pop-up window. At least, one value should be present in checked state while filtering. Otherwise “Ok” will be disabled.

![](PivotTable-Field-List_images/relationalBfiltering.png)

![](PivotTable-Field-List_images/relationaldialogfilter.png)

## Defer update
Defer update in the field list allows you to refresh the control on-demand and not during every UI operation. This operation can be enabled/disabled through [`enableDeferUpdate`](/api/js/ejpivotgrid#members:enabledeferupdate) property internally.

