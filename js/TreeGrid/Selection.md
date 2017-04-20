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

The TreeGrid control provides support for row and cell selections. 

## Row selection

You can enable or disable the row selection in TreeGrid, using `allowSelection` property. By default row selection is enabled in TreeGrid.
The following code example shows you to disable the row selection in TreeGrid.


{% highlight js %}

   $("#TreeGridContainer").ejTreeGrid({
        //...
         allowSelection: false,
   });

{% endhighlight %}

The output of the TreeGrid with row selection is as follows.

![](/js/TreeGrid/Selection_images/Selection_img1.png)

### Selecting a row at initial load

You can select a row at initial load by setting the index of the row to the `selectedRowIndex` property.

Find the following code for selecting a row at initial load.


{% highlight js %}

   $("#TreeGridContainer").ejTreeGrid({
        //... 
        selectedRowIndex: 3,
   });

{% endhighlight %}

### Multiple row selection

It is also possible to select multiple rows by setting `selectionSettings.selectionType` as `multiple`. You can select more than one row by holding down `CTRL` key and to click on the rows. 
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

To enable multiple selection, you can set `selectionSettings.selectionType` property either as `multiple` or enumeration value `ej.TreeGrid.SelectionType.Multiple`.

### Selecting a row programmatically 

You can select a row programmatically by setting the row index value to `selectedRowIndex` property. 
The following code shows on how to select a row programmatically with button click action,

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
         $("#TreeGridContainer ").ejTreeGrid("option", "selectedRowIndex", 4);           
     })

{% endhighlight %}

## Cell selection

You can select cells in TreeGrid by setting `selectionSettings.selectionMode` property as `cell`.
Find the code example below to enable the cell selection in TreeGrid.

{% highlight js %}

     $("#TreeGridContainer").ejTreeGrid({
        //...
         selectionSettings:
         {
           selectionMode: "ej.TreeGrid.SelectionType.Cell",                                 
         }
     });

{% endhighlight %}

The output of the TreeGrid with cell selection is as follows.

![](/js/TreeGrid/Selection_images/Selection_img3.png)

### Multiple cell selection

You can also select multiple cell by setting `selectionSettings.selectionType` property as `multiple`. 
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

You can select the cells programmatically using `selectCells` public method. Find the code example below for selecting TreeGrid cells programmatically


{% highlight html %}

    <html>
        <body>
         <button id="selectcells">SelectCells</button>
         //...
        </body> 
    </html>

{% endhighlight %}

{% highlight js %}

     $("#TreeGridContainer").ejTreeGrid({
        //...
     });
     
     $("#selectcells").click(function (args) {
            //create TreeGrid object
            var TreeGridObj = $("#TreeGridContainer").data("ejTreeGrid");
            cellIndex = [{ rowIndex: 2, cellIndex: 1 }, {rowIndex:3,cellIndex:1}];
            TreeGridObj.selectCells(cellIndex);
     })

{% endhighlight %}

## Checkbox selection

TreeGrid supports checkbox selection and to enable the checkbox selection, you need to set `selectionSettings.selectionType` property to `checkbox` and `selectionSettings.selectionMode` property as `row`. By default, checkbox column will be displayed as the left most column, on enabling the checkbox selection in TreeGrid.

### Column header checkbox

It is possible to select/unselect all the TreeGrid rows using column header checkbox. To enable this you need to set, `selectionSettings.enableSelectAll` property as `true`. The following code snippet explains how to enable the column header checkbox,

{% highlight js %}
        $("#TreeGridContainer").ejTreeGrid ({
          selectionSettings: {
                     selectionType: "ej.TreeGrid.SelectionType.Checkbox",
                     selectionMode: "ej.TreeGrid.SelectionType.Row",
                     enableSelectAll: true,                        
                 },
           });
{% endhighlight %}

The output of the TreeGrid with checkbox enabled in column header

![](/js/TreeGrid/Selection_images/Selection_img5.png)

### Hierarchy selection
It is possible to select the rows hierarchically using checkboxes in TreeGrid by enabling the `selectionSettings.enableHierarchySelection` property.
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

The output of the TreeGrid with hierarchy selection enabled

![](/js/TreeGrid/Selection_images/Selection_img6.png)

### Checkbox column

It is possible to change the default index of the checkbox column and we can display the checkboxes in any of the existing column. And to enable the checkbox in any of the column, we need to set `showCheckbox` property as true in the column object.

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