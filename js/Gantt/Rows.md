---
layout: post
title: Rows
description: Rows
platform: Js
control: Gantt
documentation: ug
api: /api/js/ejgantt
---
# Rows 

Row represents a task information from the data source, and it is possible to perform the following actions in Gantt rows.

## Adding a row

A row can be added in the following ways in Gantt.

* Toolbar 
* Context menu 
* Adding a row programmatically 

### Toolbar adding


Row can be added in Gantt from toolbar while the [`editSettings.allowAdding`](/api/js/ejgantt#members:editsettings-allowadding) property is set to true. On clicking the toolbar add icon, you need to provide the task information in the add dialog. If a row is previously selected, then the new row will be added below and in the same hierarchical level as that of the selected row. If there are no rows selected in Gantt, by default the new row will be added as the top most row in Gantt.

{% highlight javascript %}
$("#GanttContainer").ejGantt({

    //...

    editSettings: {

        //…

        allowAdding: true,

    },

});
{% endhighlight %}

![](/js/Gantt/Rows_images/Rows_img1.png)

### Context menu adding

New rows can either be added above or below the selected rows by using the default context menu, while the [`enableContextMenu`](/api/js/ejgantt#members:enablecontextmenu) is set to `true`. The new row added will have the same task information similar to the selected row.

{% highlight javascript %}
$("#GanttContainer").ejGantt({

    //...

    enableContextMenu: true,

    editSettings: {

        //…

        allowAdding: true,

    },

});
{% endhighlight %}

![](/js/Gantt/Rows_images/Rows_img2.png)

### Adding a row programmatically

You can add rows in the below positions dynamically using [`addRecord`](/api/js/ejgantt#methods:addrecord "addRecord(data, rowPosition)") public method and we can define the default new record add position by using [`rowPosition`](/api/js/ejgantt#members:editsettings-rowposition "editSettings.rowPosition") property.

* Top of all the rows
* Bottom to all the existing rows
* Above the selected row
* Below the selected row
* As child to the selected row

The below code example explains on adding a row using a custom button.

{% highlight html %}
<button id="addRow" style="top:27px;left:50px;position:absolute">AddRow</button>

{% endhighlight %}

{% highlight javascript %}
$("#GanttContainer").ejGantt({

    //...

});

$("#addRow").click(function(args) {

    //Create Gantt object

    var GanttObj = $("#GanttContainer").data("ejGantt");

    // data to be added

    var data = {

        taskID: 5,

        taskName: "New Task",

        startDate: "02/13/2014",

        endDate: "02/14/2014",

        duration: 2

    };

    GanttObj.addRecord(data, ej.Gantt.AddRowPosition.Child);

})
{% endhighlight %}

The following screen shot shows to add new row as child.

![](/js/Gantt/Rows_images/Rows_img3.png)

N> While adding a new record [`actionComplete`](/api/js/ejgantt#events:actioncomplete) event will be triggered with arguments `addedRecord` value as new record and `requestType` value as `save`, using this event we can update new record information in server database.

## Row drag and drop

It is possible to dynamically re-arrange the rows in the Gantt control by using the [`allowDragAndDrop`](/api/js/ejgantt#members:allowdraganddrop "allowDragAndDrop") property. With this property, row drag and drop can be enabled or disabled. Rows can be inserted above, below as a sibling or as a child to the existing row with the help of this feature. A default tooltip is rendered while dragging the Gantt row and this tooltip can be customized by the [`dragTooltip`](/api/js/ejgantt#members:dragtooltip "dragTooltip") property. This property has inner properties such as [`showTooltip`](/api/js/ejgantt#members:dragtooltip-showtooltip "dragTooltip.showTooltip"), [`tooltipItems`](/api/js/ejgantt#members:dragtooltip-tooltipitems "dragTooltip.tooltipItems") and [`tooltipTemplate`](/api/js/ejgantt#members:dragtooltip-tooltiptemplate "dragTooltip.tooltipTemplate").

The [`showTooltip`](/api/js/ejgantt#members:dragtooltip-showtooltip "dragTooltip.showTooltip") property is used to enable or disable the tooltip. By default, this property value is `false`.

The following code explains about enabling the row drag and drop with the default tooltip in the Gantt.

{% highlight javascript %}
$("#GanttContainer").ejGantt({

    //...     

    allowDragAndDrop: true,

    dragTooltip: {

        showTooltip: true

    },

    // ...

});
{% endhighlight %}

The following screenshot depicts a row drag and drop in the Gantt widget.

![](/js/Gantt/Rows_images/Rows_img4.png)

[Click](http://js.syncfusion.com/demos/web/#!/bootstrap/gantt/rowdraganddrop) here to view the online demo sample for row drag and drop in Gantt.

### Customizing drag tooltip

The [`tooltipItems`](/api/js/ejgantt#members:dragtooltip-tooltipitems "dragTooltip.tooltipItems") property is used to customize the tooltip items. By using this property, specific fields can be rendered in the tooltip. By default this property value is `null`, and all the defined field items are rendered in the tooltip.

The following code shows how to render row drag tooltip with the desired field items.

{% highlight javascript %}
$("#GanttContainer").ejGantt({

    //...     

    dragTooltip: {

        showTooltip: true,

        tooltipItems: [

            "taskID",

            "taskName",

            "startDate",

            "endDate"

        ]

    },

    //... 

});
{% endhighlight %}

The [`tooltipTemplate`](/api/js/ejgantt#members:dragtooltip-tooltiptemplate "dragTooltip.tooltipTemplate") property renders the template tooltip for row drag and drop in the Gantt control by using the JsRender template. You can provide either the id value of the script element or the script element to the property.

The following code shows how to render row drag tooltip with tooltip template.

{% highlight javascript %}
<script id="customTooltip" type="text/x-jsrender">

    <tr>

        <td class="border" style='height:30px;'>

            <div>{{"{{"}}:#data['TaskId'] {{}}}}</div>

        </td>

        <td class="border" style='height:30px;'>

            <div>{{"{{"}}:#data['TaskName'] {{}}}}</div>

        </td>

    </tr>

</script>
$("#GanttContainer").ejGantt({
    //...
    dragTooltip: {
        showTooltip: true,
        tooltipTemplate: "#customTooltip"
    },
});
{% endhighlight %}

![](/js/Gantt/Rows_images/Rows_img6.png)

### Customize row drag and drop action

In Gantt, [`rowDragStart`](/api/js/ejgantt#events:rowdragstart), [`rowDrag`](/api/js/ejgantt#events:rowdrag) and [`rowDragStop`](/api/js/ejgantt#events:rowdragstop) events are triggered on row drag and drop action. Using this event we can prevent drag and drop action of particular task and validate the drop position on particular row. The below code example shows how to use this events.

{% highlight javascript %}

$("#GanttContainer").ejGantt({
    //...
    allowDragAndDrop: true,
    rowDragStart: function (args) {
        if (args.draggedRow.taskId == 6) // Task Id 6 can't be dragged
            args.cancel = true;
    },
    rowDrag: function (args) {
        if (args.targetRow.taskId == 5 && args.dropPosition == "insertAsChild") // Can't drop task as child on Task Id 5
            args.canDrop = false;
    },
    rowDragStop: function (args) {
        if (args.targetRow.taskId == 6) // Can't drop any task on Task Id 6
            args.cancel = true;
    },
});

{% endhighlight %}

You can find the JS playground sample for this [here](http://jsplayground.syncfusion.com/Sync_hgbrt1ky "Demo Link").

## Alternate row background

In Gantt, it is possible to enable or disable the alternate row background using the [`enableAltRow`](/api/js/ejgantt#members:enablealtrow) property. The following code example shows you to disable the alternate row color in Gantt.

{% highlight javascript %}
$("#GanttContainer").ejGantt({

    //...     

    enableAltRow: false,

    //...             

});
{% endhighlight %}

![](/js/Gantt/Rows_images/Rows_img7.png)

### Change alternate rows background

The alternate rows background can be changed by setting the background color for the alternate row elements using CSS. The following code example shows you how to change the alternate rows background color in Gantt.

{% highlight html %}
<head>

    <style>
        .e-treegrid .e-alt-row {
            background-color: Bisque;
        }
    </style>

</head>

{% endhighlight %}

{% highlight javascript %}
$("#GanttContainer").ejGantt({

    //...     

    enableAltRow: true,

    //...             

});
{% endhighlight %}
![](/js/Gantt/Rows_images/Rows_img5.png)

## Row height

It is possible to change the height of the row in Gantt by setting row height in pixels to the [`rowHeight`](/api/js/ejtreegrid#members:rowheight) property. The following code example explains how to change the row height in Gantt at load time.

{% highlight javascript %}
$("#GanttContainer").ejGantt({

    //...     

    rowHeight: 60,

    //...             

});
{% endhighlight %}

![](/js/Gantt/Rows_images/Rows_img8.png)

## Expand/Collapse Row

In Gantt parent tasks are expanded/collapsed by using expand/collapse icons, expand all/collapse all toolbar items and by using public methods. By default all tasks in Gantt was rendered in expanded state but we can change this status in Gantt.

### Collapse all tasks at Gantt load

All tasks available in Gantt was rendered in collapsed state by setting [`enableCollapseAll`](/api/js/ejgantt#members:enablecollapseall) property as `true`. The following code example shows how to use this property.

{% highlight javascript %}

$("#GanttContainer").ejGantt({
    //...     
    enableCollapseAll: true,
});

{% endhighlight %}

The below screenshot shows the output of above code example.

![](/js/Gantt/Rows_images/Rows_img9.png)

### Define expand/collapse status of tasks at Gantt load

In Gantt, we can render some tasks in collapsed state and some tasks in expanded state, this can done by defining expand status of the task in data source. This value was mapped to Gantt control by using [`expandStateMapping`](/api/js/ejgantt#members:expandstatemapping) property. The following code example shows how to use this property.

{% highlight javascript %}

 var data = [
    {
        taskID: 1,
        taskName: "Project Schedule",
        expandState: true,
        //...
        subtasks: [
            {
                taskID: 2,
                taskName: "Design",
                expandState: false,
                //...
            }]
    }];

$("#GanttContainer").ejGantt({
    dataSource: data,
    expandStateMapping: "expandState",
    //...
});

{% endhighlight %}

The below screenshot shows the output of above code example.

![](/js/Gantt/Rows_images/Rows_img10.png)


### Expand/Collapse the task dynamically

Gantt tasks can be expanded/collapsed dynamically by using [`expandCollapseRecord`](/api/js/ejgantt#methods:expandcollapserecord "expandCollapseRecord(taskId)") method. The following code example shows how to use this method.

{% highlight javascript %}

$("#GanttContainer").ejGantt({
    //...
});

$("#expandCollapseTask").click(function () {
    var ganttObj = $("#GanttContainer").ejGantt("instance");
        ganttObj.expandCollapseRecord(2);
});

{% endhighlight %}

N> This method was used to toggle the expand status of Gantt task, when we pass the id of task which is in expanded state to this method and this task will be collapsed, similarly collapsed task will be expanded.

### Expand/Collapse all the tasks dynamically

All the tasks in Gantt will be expanded/collapsed by clicking `expandAll` and `collapsedAll` toolbar items or by using [`expandAllItems`](/api/js/ejgantt#methods:expandallitems "expandAllItems()") and [`collapseAllItems`](/api/js/ejgantt#methods:collapseallitems "collapseAllItems()") methods. We can invoke this methods dynamically on any action like external button click. The below code example shows how to use this methods.

{% highlight js %}

$("#GanttContainer").ejGantt({
    //...
    toolbarSettings: {
        showToolbar: true,
        toolbarItems: [
            ej.Gantt.ToolbarItems.Add,
            //..
            ej.Gantt.ToolbarItems.ExpandAll,
		    ej.Gantt.ToolbarItems.CollapseAll
        ]
    },
});

$("#expandAllTasks").click(function () {
    var ganttObj = $("#GanttContainer").ejGantt("instance");
        ganttObj.expandAllItems();
});

$("#collapseAllTasks").click(function () {
    var ganttObj = $("#GanttContainer").ejGantt("instance");
        ganttObj.collapseAllItems();
});

{% endhighlight %}

### Customize expand/collapse action

On expand action [`expanding`](/api/js/ejgantt#events:expanding) and [`expanded`](/api/js/ejgantt#events:expanded) event will be triggered with current expanding row's information. Similarly on collapse action [`collapsing`](/api/js/ejgantt#events:collapsing) and [`collapsed`](/api/js/ejgantt#events:collapsed) event will be triggered. Using this events and it's arguments we can customize the expand/collapse action. The following code example shows how to prevent the particular row from expand/collapse action using [`expanding`](/api/js/ejgantt#events:expanding) and [`collapsing`](/api/js/ejgantt#events:collapsing) event.

{% highlight js %}

$("#GanttContainer").ejGantt({
    //...
    expandStateMapping: "expandState",
    expanding: function (args) {
        if (args.data.taskId == 2) // we can't expand Task Id 2
            args.cancel = true;
    },
    collapsing: function (args) { // we can't collapse Task Id 1
        if (args.data.taskId == 1)
            args.cancel = true;
    },
    
});

{% endhighlight %}

You can find the JS playground sample for this [here](http://jsplayground.syncfusion.com/Sync_wmcj2lbp "Demo Link").
