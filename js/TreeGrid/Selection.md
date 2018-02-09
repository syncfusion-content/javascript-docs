---
layout: post
title: Selection
description: selection
platform: js
control: TreeGrid
documentation: ug
api: /api/js/ejtreegrid
---

# Selection

The TreeGrid control provides support for row and cell selections using [`selectionSettings`](/api/js/ejtreegrid#members:selectionsettings) property. 

## Row selection

You can enable or disable the row selection in TreeGrid, using the [`allowSelection`](/api/js/ejtreegrid#members:allowselection) property. By default row selection is enabled in TreeGrid.
The following code example shows, how to disable the row selection in TreeGrid.


{% highlight js %}

   $("#TreeGridContainer").ejTreeGrid({
        //...
         allowSelection: false,
   });

{% endhighlight %}

The output of the TreeGrid with row selection is as follows.

![](/js/TreeGrid/Selection_images/Selection_img1.png)

### Selecting a row at initial load

You can select a row at initial load by setting the index of the row to the [`selectedRowIndex`](/api/js/ejtreegrid#members:selectedrowindex) property.

Find the following code for selecting a row at initial load.


{% highlight js %}

   $("#TreeGridContainer").ejTreeGrid({
        //... 
        selectedRowIndex: 3,
   });

{% endhighlight %}

### Multiple row selection

It is also possible to select multiple rows by setting the [`selectionType`](/api/js/ejtreegrid#members:selectionsettings-selectiontype "selectionSettings.selectionType") as `multiple`. You can select more than one row by holding down `CTRL` key and to click on the rows. 
The following code example explains how to enable multiple selection in TreeGrid.

{% highlight js %}

       $("#TreeGridContainer").ejTreeGrid({
              //... 
               selectionSettings: {
                     selectionType: "ej.TreeGrid.SelectionType.Multiple"                                 
               }
        });

{% endhighlight %}

The output of the TreeGrid with multiple row selection is as follows.

![](/js/TreeGrid/Selection_images/Selection_img2.png)

To enable multiple selection, you can set the [`selectionType`](/api/js/ejtreegrid#members:selectionsettings-selectiontype "selectionSettings.selectionType") property either as `multiple` or enumeration value `ej.TreeGrid.SelectionType.Multiple`.

### Selecting a row programmatically 

You can select a row programmatically by setting the row index value to the [`selectedRowIndex`](/api/js/ejtreegrid#members:selectedrowindex) property. 
The following code shows on how to select a row programmatically with button click action.

{% highlight html %}

    <html>
        <body>
        <button id="selectRow">SelectRow</button>
        //...
        </body>
    </html>

{% endhighlight %}

{% highlight js %}

     $("#TreeGridContainer").ejTreeGrid({
        //...
     });
     $("#selectRow").click(function (args) {
         $("#TreeGridContainer").ejTreeGrid("option", "selectedRowIndex", 4);           
     })

{% endhighlight %}

### Customize row selection action

While selecting a row in TreeGrid, [`rowSelecting`](https://help.syncfusion.com/api/js/ejtreegrid#events:rowselecting) and [`rowSelected`](https://help.syncfusion.com/api/js/ejtreegrid#events:rowselected) event will be triggered. Row selecting event will be triggered on initialization of row selection action. In [`rowSelecting`](https://help.syncfusion.com/api/js/ejtreegrid#events:rowselecting) event we can get the previously selected row and current selecting row’s information, using this information we can prevent selection of particular row. The [`rowSelected`](https://help.syncfusion.com/api/js/ejtreegrid#events:rowselected) event will be triggered on completion of row selection action, in this event we can get the current selected row’s information. 

The following code example shows how to prevent the selection of particular row using [`rowSelecting`](https://help.syncfusion.com/api/js/ejtreegrid#events:rowselecting) event.

{% highlight js %}

     $("#TreeGridContainer").ejTreeGrid({
        //...
        allowSelection: true,
        rowSelecting: function(args) {
            if(args.data.taskID == 5) // prevent selection of Task id 5
                args.cancel = true;
        },
        //...

{% endhighlight %}

### Get record details

In TreeGrid, It is possible to get the record detail when `click` and `dblClick` the row using [`recordClick`](https://help.syncfusion.com/api/js/ejtreegrid#events:recordclick) and [`recordDoubleClick`](https://help.syncfusion.com/api/js/ejtreegrid#events:recorddoubleclick) event, using this method we can get the record details even [`allowSelection`](/api/js/ejtreegrid#members:allowselection) is `false`.

The below code example show, how to get record details when `click` the row.

 {% highlight js %}

     $("#TreeGridContainer").ejTreeGrid({
        //...
        allowSelection: false,
        recordClick:function(args)
        {
            var n=0;
        },
        //...

{% endhighlight %}

## Cell selection

You can select cells in TreeGrid by setting the [`selectionMode`](/api/js/ejtreegrid#members:selectionsettings-selectionmode "selectionSettings.selectionMode") property as `cell`. And you can able to get the selected cell information using the [`selectedCellIndexes`](/api/js/ejtreegrid#members:selectedcellindexes) property from the TreeGrid object. The [`selectedCellIndexes`](/api/js/ejtreegrid#members:selectedcellindexes) is an object collection, which has the [`cellIndex`](/api/js/ejtreegrid#members:selectedcellindexes-cellindex "selectedCellIndexes.cellIndex") and [`rowIndex`](/api/js/ejtreegrid#members:selectedcellindexes-rowindex "selectedCellIndexes.rowIndex") information of the selected cells.
Find the code example below to enable the cell selection in TreeGrid.

{% highlight js %}

     $("#TreeGridContainer").ejTreeGrid({
        //...
         selectionSettings:
         {
           selectionMode: ej.TreeGrid.SelectionMode.Cell,                                 
         }
     });

{% endhighlight %}

The output of the TreeGrid with cell selection is as follows.

![](/js/TreeGrid/Selection_images/Selection_img3.png)

It is possible to get the list of HTML elements of the selected cells at run-time using the [`getSelectedCells`](https://help.syncfusion.com/api/js/ejtreegrid#methods:getselectedcells "getSelectedCells") method.

### Select cells dynamically

You can select the cells programmatically using the [`selectCells`](/api/js/ejtreegrid#methods:selectcells "selectCells(indexes,preservePreviousSelectedCell)") public method. Find the code example below for details.

{% highlight html %}

    <html>
        <body>
        <button id="selectCells">Select Cells</button>
        //...
        </body>
    </html>

{% endhighlight %}

{% highlight js %}

     $("#TreeGridContainer").ejTreeGrid({
        //...
        selectionSettings:
        {
            selectionMode: ej.TreeGrid.SelectionMode.Cell,
            selectionType: ej.TreeGrid.SelectionType.Multiple
        },
        //..
     });
     $("#selectCells").click(function (args) {
         var treegridObj = $("#TreeGridContainer").ejTreeGrid("instance");
         var cellIndex = [{
            rowIndex: 2,
            cellIndex: 1
        }, {
            rowIndex: 3,
            cellIndex: 1
        }];       
        treegridObj.selectCells(cellIndex);    
     })

{% endhighlight %}

![](/js/TreeGrid/Selection_images/Selection_img8.png)

### Disabling cell selection for specific column

It is possible to disable cell selection for a specific column by setting [`allowCellSelection`](/api/js/ejtreegrid#members:columns-allowcellselection "columns.allowCellSelection") as `false` in the column definition.

The below code snippet explains how to disable cell selection for specific column in tree grid

{% highlight js %}

    $(function () {
        $("#TreeGridContainer").ejTreeGrid({
            //...
            columns: [
                { field: "taskID", headerText: "Task Id"},
                { field: "taskName", headerText: "Task Name",allowCellSelection: false },
                { field: "startDate", headerText: "Start Date"},
                { field: "endDate", headerText: "End Date" }
            ]
        })
    });

{% endhighlight %}

### Multiple cell selection

You can also select multiple cell by setting the [`selectionType`](/api/js/ejtreegrid#members:selectionsettings-selectiontype "selectionSettings.selectionType") property as `multiple`. 
Multiple selection can be done by holding the `CTRL` key and to click the required cells. 
The following code example shows you to select multiple cells.

{% highlight js %}

      $("#TreeGridContainer").ejTreeGrid({
       //...
       selectionSettings: {
            selectionType: "ej.TreeGrid.SelectionType.Multiple",
            selectionMode: "ej.TreeGrid.SelectionType.Cell",
        }
     });

{% endhighlight %}

The output of the TreeGrid with multiple cell selection is as follows.

![](/js/TreeGrid/Selection_images/Selection_img4.png)

### Selecting cells programmatically 

You can select the cells programmatically using the `selectCells` public method. Find the code example below for selecting TreeGrid cells programmatically.


{% highlight html %}

    <html>
        <body>
         <button id="selectCells">SelectCells</button>
         //...
        </body> 
    </html>

{% endhighlight %}

{% highlight js %}

     $("#TreeGridContainer").ejTreeGrid({
        //...
     });
     
     $("#selectCells").click(function (args) {
            //create TreeGrid object
            var TreeGridObj = $("#TreeGridContainer").data("ejTreeGrid");
            cellIndex = [{ rowIndex: 2, cellIndex: 1 }, {rowIndex:3,cellIndex:1}];
            TreeGridObj.selectCells(cellIndex);
     })

{% endhighlight %}

### Customize cell selection action

While selecting a cell in TreeGrid, [`cellSelecting`](https://help.syncfusion.com/api/js/ejtreegrid#events:cellselecting) and [`cellSelected`](https://help.syncfusion.com/api/js/ejtreegrid#events:cellselected) event will be triggered. Cell selecting event will be triggered on initialization of cell selection action. In [`cellSelecting`](https://help.syncfusion.com/api/js/ejtreegrid#events:cellselecting) event we can get the current selecting cell information, using this information we can prevent selection of particular cell in particular row. The[`cellSelected`](https://help.syncfusion.com/api/js/ejtreegrid#events:cellselected) event will be triggered on completion of cell selection action, in this event we can get the current selected cell’s information. 

The following code example shows how to prevent the selection of particular cell using [`cellSelecting`](https://help.syncfusion.com/api/js/ejtreegrid#events:cellselecting) event.

{% highlight js %}

     $("#TreeGridContainer").ejTreeGrid({
        //...
        allowSelection: true,
        selectionSettings:{
            selectionMode:ej.TreeGrid.SelectionMode.Cell,
            selectionType: ej.TreeGrid.SelectionType.Single
        },
        cellSelecting: function(args) {
            if(args.data.taskID == 5 && args.cellIndex == 1) // prevent selection of Task Name cell of Task id 5
                args.cancel = true;
        },
        //...

{% endhighlight %}

## Checkbox selection

TreeGrid supports checkbox selection and to enable the checkbox selection, you need to set the [`selectionType`](/api/js/ejtreegrid#members:selectionsettings-selectiontype "selectionSettings.selectionType") property to `checkbox` and the [`selectionMode`](/api/js/ejtreegrid#members:selectionsettings-selectionmode "selectionSettings.selectionMode") property as `row`. By default, checkbox column will be displayed as the left most column, on enabling the checkbox selection in TreeGrid.

### Column header checkbox

It is possible to select/unselect all the TreeGrid rows using column header checkbox. To enable this you need to set the [`enableSelectAll`](/api/js/ejtreegrid#members:selectionsettings-enableselectall "selectionSettings.enableSelectAll") property as `true`. The following code snippet explains how to enable the column header checkbox.

{% highlight js %}
        $("#TreeGridContainer").ejTreeGrid ({
          selectionSettings: {
                     selectionType: "ej.TreeGrid.SelectionType.Checkbox",
                     selectionMode: "ej.TreeGrid.SelectionType.Row",
                     enableSelectAll: true,                        
                 },
           });
{% endhighlight %}

The output of the TreeGrid with checkbox enabled in column header.

![](/js/TreeGrid/Selection_images/Selection_img5.png)

### Hierarchy selection
It is possible to select the rows hierarchically using checkboxes in TreeGrid by enabling the [`enableHierarchySelection`](/api/js/ejtreegrid#members:selectionsettings-enablehierarchyselection "selectionSettings.enableHierarchySelection") property.
In this selection the hierarchy between the records will be retained, where the child records will get selected on selecting its parent record’s checkbox and parent record checkbox will get selected on checking all of its child items. 

Following code snippet explains on enabling hierarchy selection in TreeGrid.

{% highlight js %}
        $("#TreeGridContainer"). ejTreeGrid ({
            selectionSettings: {
                       selectionType: "ej.TreeGrid.SelectionType.Checkbox",
                       selectionMode: " ej.TreeGrid.SelectionType.Row",
                       enableHierarchySelection: true,                        
                    },
           });
{% endhighlight %}

The output of the TreeGrid with hierarchy selection enabled.

![](/js/TreeGrid/Selection_images/Selection_img6.png)

### Checkbox column

It is possible to change the default index of the checkbox column and we can display the checkboxes in any of the existing column. And to enable the checkbox in any of the column, we need to set [`showCheckbox`](/api/js/ejtreegrid#members:columns-showcheckbox "columns.showCheckbox") property as true in the column object.

{% highlight js %}

            $("#TreeGridContainer"). ejTreeGrid ({
             selectionSettings: {
                    selectionType: "ej.TreeGrid.SelectionType.Checkbox",
                    selectionMode: " ej.TreeGrid.SelectionType.Row",
                    },
             columns: [
                    {field: "taskID", headerText: "Task Id", editType: "numericedit" },
                    {field: "taskName", headerText: "Task Name", editType: "stringedit",                          
                        showCheckbox: true},                                          
                    ]
           });
           
{% endhighlight %}

The output of the TreeGrid with checkbox enabled in task name column.

![](/js/TreeGrid/Selection_images/Selection_img7.png)

## MultiSelection – Touch Option

It is possible to select cells using touch action in TreeGrid. TreeGrid provides support for both single selection and multiple cell selection using touch action. For multiple cell selection, when we tap on a cell a helper icon will be displayed using that we can select multiple cells.

The following code example describes how to enable multiple selection in TreeGrid.

{% highlight js %}

$("#TreeGridContainer"). ejTreeGrid ({
    //..
    selectionSettings: {
        selectionType: "ej.TreeGrid.SelectionType.Multiple"
    },
    //..
});
           
{% endhighlight %}

The following output is displayed the result of multiple selection in touch device environment.

![](/js/TreeGrid/Selection_images/multiselection.png)

## Deselecting records using method

It is possible to clear the selection in TreeGrid at run-time using the [`clearSelection`](/api/js/ejtreegrid#methods:clearselection "clearSelection") method.

The specific row will be deselected when the row index is passed as the method parameter. If the index is not passed, then all the selected rows in tree grid will be deselected.

{% highlight js %}

        var treegridObj = $("#treegrid").data("ejTreeGrid");
        treegridObj.clearSelection(2);
           
{% endhighlight %}
