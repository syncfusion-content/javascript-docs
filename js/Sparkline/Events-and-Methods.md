---
layout: post
title: Events and Methods
description: Learn how to add Events and Methods in Sparkline.
platform: js
control: Sparkline
documentation: ug
api: /api/js/ejsparkline
---

# Methods and Events

## Methods

### redraw()

This methods redraws the entire sparkline. You can call [`redraw()`](../api/ejsparkline#methods:redraw) whenever you update, add or remove points from the data source or whenever you want to refresh the UI.

{% highlight js %}

// redraw method for sparkline
$("#container").ejSparkline("redraw");

{% endhighlight %}

## Events

### load

The [`load`](../api/ejsparkline#events:load) event is fired before loading the sparkline.

{% highlight js %}

$("#container").ejSparkline({

 //load event for sparkline
    load: function (args) {
             //Do something
    }
    
});

{% endhighlight %}

### loaded

The [`loaded`](../api/ejsparkline#events:loaded) event is fired after loaded the sparkline.

{% highlight js %}

$("#container").ejSparkline({

//loaded event for sparkline
    loaded: function (args) {
             //Do something
    }
    
});

{% endhighlight %}

### tooltipInitialize

Fires before rendering trackball tooltip. You can use [`tooltipInitialize`](../api/ejsparkline#events:tooltipinitialize) event to customize the text displayed in trackball tooltip.

{% highlight js %}

$("#container").ejSparkline({

//ToolTip event for sparkline
    tooltipInitialize: function (args) {
              //Do something
    }
   
});

{% endhighlight %}

### seriesRendering

Fires before rendering a series. The [`seriesRendering`](../api/ejsparkline#events:seriesrendering) event is fired for each series in Sparkline.

{% highlight js %}

$("#container").ejSparkline({

//seriesRendering event for sparkline
    seriesRendering: function (args) {
              //Do something
    }
    
});

{% endhighlight %}

### pointRegionMouseMove

The [`pointRegionMouseMove`](../api/ejsparkline#events:pointregionmousemove) event is fired when mouse is moved over a point.

{% highlight js %}

$("#container").ejSparkline({

//pointRegionMouseMove event for sparkline
    pointRegionMouseMove: function (args) {
                  //Do something
    }
   
});

{% endhighlight %}

### pointRegionMouseClick

The [`pointRegionMouseClick`](../api/ejsparkline#events:pointregionmouseclick) event is fired on clicking a point in sparkline. You can use this event to handle clicks made on points.

{% highlight js %}

$("#container").ejSparkline({

//pointRegionClick event for sparkline
    pointRegionMouseClick: function (args) {
             //Do something
    }
    
});

{% endhighlight %}

### sparklineMouseMove

The [`sparklineMouseMove`](../api/ejsparkline#events:sparklinemousemove) is fired on moving mouse over the sparkline.

{% highlight js %}

$("#container").ejSparkline({

//sparklineMouseMove event for sparkline
    sparklineMouseMove: function (args) {
              //Do something
    }
   
});

{% endhighlight %}

### sparklineMouseLeave

The [`sparklineMouseLeave`](../api/ejsparkline#events:sparklinemouseleave) event is fired on moving mouse outside the sparkline.

{% highlight js %}

$("#container").ejSparkline({

//sparklineMouseLeave event for sparkline
    sparklineMouseLeave: function (args) {
              //Do something
    }
   
});

{% endhighlight %}

### Click

The [`click`](../api/ejsparkline#events:click) event is fired on clicking the sparkline.


{% highlight js %}
 
//Click event for sparkline

 $("#container").ejSparkline({


    click: function (args) {
              //Do something
    }
   
});

{% endhighlight %}


### doubleClick

The [`doubleClick`](../api/ejsparkline#events:doubleclick) event is fired on double clicking the sparkline.


{% highlight js %}
 
//DoubleClick event for sparkline

 $("#container").ejSparkline({


    doubleClick: function (args) {
              //Do something
    }
   
});

{% endhighlight %}



### rightClick

The [`rightClick`](../api/ejsparkline#events:rightclick) event is fired on right clicking the sparkline.


{% highlight js %}
 
//RightClick event for sparkline

 $("#container").ejSparkline({

    rightClick: function (args) {
              //Do something
    }
   
});

{% endhighlight %}