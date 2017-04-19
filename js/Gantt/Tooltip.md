---
layout: post
title: Tooltip
description: Tooltip
platform: Js
control: Gantt
documentation: Ug
api: /api/js/ejgantt
---
# Tooltip

Gantt has support to display tooltip for both taskbars and for column cells.

## Taskbar Tooltip

In Gantt, you can enable or disable taskbar mouse hover tooltip by using the [enableTaskbarTooltip](/api/js/ejgantt#members:enabletaskbartooltip) property. By default, this property is set to true. The following code example shows, how to enable the taskbar tooltip in Gantt.

{% highlight javascript %}
$("#GanttContainer").ejGantt({

    //...

    enableTaskbarTooltip: true,

});
{% endhighlight %}

This tooltip can be customized further by using [taskbarTooltipTemplate](/api/js/ejgantt#members:taskbartooltiptemplate) this property, which is described briefly in the [customization](/js/gantt/customizations) section.

## Taskbar drag tooltip

It is possible to enable or disable the tooltip while performing editing actions on taskbar (left resizing, right resizing, dragging and progress resizing) by using the [enableTaskbarDragTooltip](/api/js/ejgantt#members:enabletaskbardragtooltip)  this property. By default, this property is set to true. The following code example explains this behavior.

{% highlight javascript %}
$("#GanttContainer").ejGantt({
    //...
    enableTaskbarDragTooltip: true,
});
{% endhighlight %}

## Cell tooltip

It is possible to enable or disable the TreeGrid cell tooltip in mouse hover by using [showGridCellTooltip](/api/js/ejgantt#members:showgridcelltooltip) property. By default, this property is set to true. The following code example explains, how to enable disable this property,

{% highlight javascript %}
$("#GanttContainer").ejGantt({

    //...

    showGridCellTooltip: true,

});
{% endhighlight %}

This tooltip can be customizable using the [cellTooltipTemplate](/api/js/ejgantt#members:celltooltiptemplate) property, which is described briefly in the [customization](/js/gantt/customizations) section.

![](/js/Gantt/Tooltip_images/Tooltip_img1.png)

## Tree column (Expander column) tooltip 

It is also possible to display tooltip only for expander column by setting [showExpandGridCellTooltip](/api/js/ejgantt#members:showgridexpandcelltooltip) property. The following code example shows you to enable expander column tooltip in Gantt.

{% highlight javascript %}
$("#GanttContainer").ejGantt({

    //...

    showExpandGridCellTooltip: true,

});
{% endhighlight %}

![](/js/Gantt/Tooltip_images/Tooltip_img2.png)

