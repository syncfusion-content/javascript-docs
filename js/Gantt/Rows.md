---
layout: post
title: Rows
description: Rows
platform: Js
control: Gantt
documentation: ug
---
# Rows 

Row represents a task information from the datasource, and it is possible to perform the following actions in Gantt rows

## Adding a row

A row can be added in the following ways in Gantt,

* Toolbar 
* Context menu 
* Adding a row programmatically 

### Toolbar Adding


Row can be added in Gantt from toolbar while [editSettings.allowAdding](/api/js/ejgantt#members:editsettings-allowadding) property is set to true. On clicking the toolbar add icon, you need to provide the task information in the add dialog. If a row is previously selected, then the new row will be added below and in the same hierarchical level as that of the selected row. If there are no rows selected in Gantt, by default the new row will be added as the top most row in Gantt.

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

You can able to add new rows either above or below the selected rows by using the default context menu, while [enableContextMenu](/api/js/ejgantt#members:enablecontextmenu) is set to true. The new row added will have the same task information similar to the selected row.

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

You can add rows in the below positions dynamically using [addRecord](/api/js/ejgantt#methods:addrecord) public method,

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

    var GanttObj = $("#gantt").data("ejGantt");

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

## Row drag and drop

It is possible to dynamically re-arrange the rows in the Gantt control by using the [allowDragAndDrop](/api/js/ejgantt#members:allowdraganddrop "allowDragAndDrop") property. With this property, row drag and drop can be enabled or disabled. Rows can be inserted above, below as a sibling or as a child to the existing row with the help of this feature. A default tooltip is rendered while dragging the Gantt row and this tooltip can be customized by the [dragTooltip](/api/js/ejgantt#members:dragtooltip "dragTooltip") property. This property has inner properties such as [showTooltip](/api/js/ejgantt#members:dragtooltip-showtooltip "dragTooltip.showTooltip"), [tooltipItems](/api/js/ejgantt#members:dragtooltip-tooltipitems "dragTooltip.tooltipItems") and [tooltipTemplate](/api/js/ejgantt#members:dragtooltip-tooltiptemplate "dragTooltip.tooltipTemplate").

The `showTooltip` property is used to enable or disable the tooltip. By default, this property value is `false`.

The following code explains about enabling the row drag and drop with the default tooltip in the Gantt.

{% highlight javascript %}
$("#gantt").ejGantt({

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

### Customizing Drag tooltip

The [tooltipItems](/api/js/ejgantt#members:dragtooltip-tooltipitems) property is used to customize the tooltip items. By using this property, specific fields can be rendered in the tooltip. By default this property value is `null`, and all the defined field items are rendered in the tooltip.

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

The [tooltipTemplate](/api/js/ejgantt#members:dragtooltip-tooltiptemplate) property renders the template tooltip for row drag and drop in the Gantt control by using the JsRender template. You can provide either the id value of the script element or the script element to the property.

The following code shows how to render row drag tooltip with tooltip template.

{% highlight javascript %}
<script id="customTooltip" type="text/x-jsrender">

    <tr>

        <td class="border" style='height:30px;'>

            <div>{{“{{“}}:#data['TaskId'] {{}}}}</div>

        </td>

        <td class="border" style='height:30px;'>

            <div>{{“{{“}}:#data['TaskName'] {{}}}}</div>

        </td>

    </tr>

</script>
$("#GanttContainer").ejGantt({
    //...
    dragTooltip: {
        showTooltip: true,
        tooltipTemplate: "#customtooltip"
    },
});
{% endhighlight %}

![](/js/Gantt/Rows_images/Rows_img6.png)

## Alternate row background

In Gantt, it is possible to enable or disable the alternate row background using the [enableAltRow](/api/js/ejgantt#members:enablealtrow) property. The following code example shows you to disable the alternate row color in Gantt.

{% highlight javascript %}
$("#GanttContainer").ejGantt({

    //...     

    enableAltRow: false,

    //...             

});
{% endhighlight %}

![](/js/Gantt/Rows_images/Rows_img7.png)

### Change altRow background

The altRow background can be changed by setting the background color for the altRow using CSS. The following code example shows you how to change the altRow color.

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

# Row height

It is possible to change the height of the row in Gantt by setting row height in pixels to [rowHeight](/api/js/ejtreegrid#members:rowheight) property. The following code example explains how to change the row height in Gantt at load time.

{% highlight javascript %}
$("#GanttContainer").ejGantt({

    //...     

    rowHeight: 60,

    //...             

});
{% endhighlight %}

![](/js/Gantt/Rows_images/Rows_img8.png)

