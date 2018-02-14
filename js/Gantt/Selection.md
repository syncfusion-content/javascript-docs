---
layout: post
title: Selection
description: Selection
platform: Js
control: Gantt
documentation: ug
api: /api/js/ejgantt
---
# Selection

## Row selection

The row selection in Gantt can be enabled or disabled, by using the  [`allowSelection`](/api/js/ejgantt#members:allowselection) property. You can able to get the selected row object using the `selectedItem` property from the Gantt model. The following code example shows how to disable the row selection in Gantt.

{% highlight javascript %}
$("#GanttContainer").ejGantt({

    //...

    allowSelection: false,

});
{% endhighlight %}

### Selecting a row on initial load

You can select a row on load time by setting the index of the row to the [`selectedRowIndex`](/api/js/ejgantt#members:selectedrowindex) property. Find the following code example for details.

{% highlight javascript %}
$("#GanttContainer").ejGantt({

    //...

    selectedRowIndex: 3,

});
{% endhighlight %}

![](/js/Gantt/Selection_images/Selection_img1.png)

### Selecting a row programmatically 

You can also select a row programmatically by setting index of the row value to the [`selectedRowIndex`](/api/js/ejgantt#members:selectedrowindex) property. The following code shows to select a row programmatically with a custom button click action.

{% highlight html %}
<body>

    <button id="selectRow">SelectRow</button> //...

</body>
{% endhighlight %}

{% highlight javascript %}
$("#GanttContainer").ejGantt({

    //...

});

$("#selectRow").click(function(args) {

    $("#GanttContainer ").ejGantt("option", "selectedRowIndex", 4);

})
{% endhighlight %}

### Multiple row selection

It is also possible to select multiple rows by setting [`selectionType`](/api/js/ejgantt#members:selectiontype) as `multiple`. You can select more than one row by holding down <kbd>CTRL</kbd> key while selecting multiple rows.
The following code example explains how to enable multiple selection in Gantt.

{% highlight js %}

       $("#GanttContainer").ejGantt({            
                     selectionType: "multiple",
                     selectionMode: "row",					 
        });

{% endhighlight %}

The output of the Gantt with multiple row selection is as follows.

![](/js/Gantt/Selection_images/Selection_img5.png)

To enable multiple selection, you can set the [`selectionType`](/api/js/ejgantt#members:selectiontype) property either as `multiple` or enumeration value `ej.Gantt.SelectionType.Multiple`.

### Selecting multiple rows programmatically 

You can also select multiple rows programmatically  by using the [`selectMultipleRows`](/api/js/ejgantt#methods:selectmultiplerows "selectMultipleRows(rowIndexes)") public method. The following code example explains how to enable multiple selection in Gantt.
{% highlight html %}
<body>

    <button id="selectMultipleRow">SelectMultipleRows</button> //...

</body>
{% endhighlight %}

{% highlight javascript %}
$("#GanttContainer").ejGantt({
        selectionType: "multiple",
        selectionMode: "row",
    //...

});

$("#selectMultipleRow").click(function(args) {

     //create Gantt object

    var ganttObj = $("#GanttContainer").data("ejGantt"),

    multipleRowIndex = [1,0,5,7];     

    ganttObj.selectMultipleRows(multipleRowIndex);

})
{% endhighlight %}

### Customize row selection action

While selecting a row in Gantt, [`rowSelecting`](/api/js/ejgantt#events:rowselecting) and [`rowSelected`](/api/js/ejgantt#events:rowselected) event will be triggered. Row selecting event will be triggered on initialization of row selection action. In [`rowSelecting`](/api/js/ejgantt#events:rowselecting) event we can get the previously selected row and current selecting row's information, using this information we can prevent selection of particular row. The [`rowSelected`](/api/js/ejgantt#events:rowselected) event will be triggered on completion of row selection action, in this event we can get the current selected row's information. The following code example shows how to prevent the selection of particular row using [`rowSelecting`](/api/js/ejgantt#events:rowselecting) event.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        allowSelection: true,
        selectionMode: "row",
        selectionType: "single",
        rowSelecting: function(args) {
            if(args.data.taskId == 5) // prevent selection of Task id 5
                args.cancel = true;
        },
        //...
    });

{% endhighlight %}

You can find the JS playground sample for this [here](http://jsplayground.syncfusion.com/Sync_birtlzhd "Demo Link").

## Cell selection

You can select a cell in Gantt by setting the [`selectionMode`](/api/js/ejgantt#members:selectionmode) property as `cell`. And you can able to get the selected cell information using the [`selectedCellIndexes`](/api/js/ejgantt#members:selectedcellindexes) property from the Gantt object. The [`selectedCellIndexes`](/api/js/ejgantt#members:selectedcellindexes) is an object collection, which has the [`cellIndex`](/api/js/ejgantt#members:selectedcellindexes-cellindex "selectedCellIndexes.cellIndex") and [`rowIndex`](/api/js/ejgantt#members:selectedcellindexes-rowindex "selectedCellIndexes.rowIndex") information of the selected cells.

Find the code example below to enable the cell selection in Gantt. 

{% highlight javascript %}
$("#GanttContainer").ejGantt({

    //...

    selectionMode: "cell",

});
{% endhighlight %}

The following screen shots shows you cell selection.

![](/js/Gantt/Selection_images/Selection_img2.png)

### Selecting multiple cells

You can also select multiple cells by setting the [`selectionType`](/api/js/ejgantt#members:selectiontype) property as `multiple` while the [`selectionMode`](/api/js/ejgantt#members:selectionmode) property is set to `cell`. Multiple cells can be selected by holding the <kbd>ctrl</kbd> key and to click on the cells. The following code example shows you to select multiple cells.

{% highlight javascript %}
$("#GanttContainer").ejGantt({

    //...

    selectionMode: "cell",

    selectionType: "multiple",

});
{% endhighlight %}

![](/js/Gantt/Selection_images/Selection_img3.png)

### Select cells programmatically 

You can select the cells programmatically using the [`selectCells`](/api/js/ejgantt#methods:selectcells "selectCells(Indexes,preservePreviousSelectedCell)") public method. Find the code example below for details.

{% highlight html %}
<body>

    <button id="selectCells">SelectCells</button> //…

</body>
{% endhighlight %}

{% highlight javascript %}
$("#GanttContainer").ejGantt({


    //...

});

$("#selectCells").click(function(args) {

    //create Gantt object

    var ganttObj = $("#GanttContainer").data("ejGantt");

    cellIndex = [{
        rowIndex: 2,
        cellIndex: 1
    }, {
        rowIndex: 3,
        cellIndex: 1
    }];

    ganttObj.selectCells(cellIndex);

})
{% endhighlight %}

![](/js/Gantt/Selection_images/Selection_img4.png)

### Customize cell selection action

While selecting a cell in Gantt, [`cellSelecting`](/api/js/ejgantt#events:cellselecting) and [`cellSelected`](/api/js/ejgantt#events:cellselected) event will be triggered. Cell selecting event will be triggered on initialization of cell selection action. In [`cellSelecting`](/api/js/ejgantt#events:cellselecting) event we can get the current selecting cell information, using this information we can prevent selection of particular cell in particular row. The [`cellSelected`](/api/js/ejgantt#events:cellselected) event will be triggered on completion of cell selection action, in this event we can get the current selected cell's information. The following code example shows how to prevent the selection of particular cell using [`cellSelecting`](/api/js/ejgantt#events:cellselecting) event.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        allowSelection: true,
        selectionMode: "cell",
        selectionType: "single",
        cellSelecting: function(args) {
            if(args.data.taskId == 5 && args.cellIndex == 1) // prevent selection of Task Name cell of Task id 5
                args.cancel = true;
        },
        //...
    });

{% endhighlight %}

You can find the JS playground sample for this [here](http://jsplayground.syncfusion.com/Sync_x3ep3n4r "Demo Link").

## Multiple Selection – Touch Option

It is possible to select rows using touch action in Gantt. Gantt provides support for both single selection and multiple row selection using touch action. For multiple row selection, when we tap on a cell, a helper icon will be displayed using that multiple rows can be selected.

The following code example describes how to enable multiple selection in Gantt.

{% highlight js %}

$("#GanttContainer"). ejGantt ({
      selectionType: "multiple",
      selectionMode: "row",
   //..
});
           
{% endhighlight %}

The following output displays the result of multiple selection in touch device environment.

![](/js/Gantt/Selection_images/Selection_img6.png)
