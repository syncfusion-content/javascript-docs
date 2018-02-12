---
layout: post
title: Explore the features of the HeatMap control.
description: Explore the features of the HeatMap control.
platform: js
control: HeatMap
documentation: ug
api: /api/js/ejheatmap
---

# Events

## cellMouseOver

The [cellMouseOver](/api/js/ejheatmap#events:cellmouseover "cellMouseOver") event gets triggered when we mouse over on the cell.

{% highlight js %}

// cellMouseOver event for HeatMap
$("#heatmapcontent").ejHeatMap({
    cellMouseOver: function(args) {}
});
            
{% endhighlight %}

## cellMouseEnter

The [cellMouseEnter](/api/js/ejheatmap#events:cellmouseenter "cellMouseEnter") event gets triggered when mouse enters the cell.

{% highlight js %}

// cellMouseEnter event for HeatMap
$("#heatmapcontent").ejHeatMap({
    cellMouseEnter: function(args) {}
});

{% endhighlight %}

## cellMouseLeave

The [cellMouseLeave](/api/js/ejheatmap#events:cellmouseleave "cellMouseLeave") event gets triggered when mouse leaves the cell.

{% highlight js %}

// cellMouseLeave event for HeatMap
$("#heatmapcontent").ejHeatMap({
    cellMouseLeave: function(args) {}
});

{% endhighlight %}

## cellSelected

The [cellSelected](/api/js/ejheatmap#events:cellselected "cellSelected") event gets triggered when we select the heatmap cell.

{% highlight js %}

// cellSelected event for HeatMap
$("#heatmapcontent").ejHeatMap({
    cellSelected: function(args) {}
});

{% endhighlight %}