---
layout: post
title: Public Methos and Events
description: Learn how to add public methos and events to Sunburstchart .
platform: js
control: Sunburst Chart
documentation: ug
api: /api/js/ejsunburstchart
---

## Methods


### redraw()

[`redraw`](../api/ejsunburstchart#methods:redraw) the entire sunburst. You can call this method whenever you update, add or remove points from the data source or whenever you want to refresh the UI.


#### Example

{% highlight js %}
// Redraw Sunburst
var sunburstObj = $("#container").data("ejSunburstChart");
sunburstObj.redraw();
{% endhighlight %}


{% highlight js %}
 
$("#container").ejSparkline("redraw");      
{% endhighlight %}


### destroy ()

[`destroy`](../api/ejsunburstchart#methods:destroy) the sunburst


#### Example


{% highlight js %}

// Destroy sunburst
var sunburstObj = $("#container").data("ejSunburstChart");
sunburstObj.destroy(); 

{% endhighlight %}


{% highlight js %}

$("#container").ejSunburstChart("destroy"); 
   
{% endhighlight %}



## Events

### load

Fires before loading, you can use [`load`](../api/ejsunburstchart#events:load) event.

#### Example

{% highlight js %}
 
//load event for sunburst

$("#container").ejSunburstChart({

    load: function (args) {
             //Do something
    }
    
});

{% endhighlight %}



### preRender

Fires before rendering sunburst, you can use [`preRender`](../api/ejsunburstchart#events:prerender) event. 


#### Example


{% highlight js %}
 
//preRender event for sunburst

$("#container").ejSunburstChart({

    preRender: function (args) {
              //Do something
    }
   
});

{% endhighlight %}



### loaded

Fires after rendering sunburst, you can use [`loaded`](../api/ejsunburstchart#events:loaded) event.  


#### Example


{% highlight js %}
 
//loaded event for sunburst

$("#container").ejSunburstChart({

    loaded: function (args) {
              //Do something
    }
   
});

{% endhighlight %}


### dataLabelRendering

Fires before rendering the datalabel, you can use [`dataLabelRendering`](../api/ejsunburstchart#events:datalabelrendering) event. 


#### Example


{% highlight js %}
 
//data label rendering event for sunburst

$("#container").ejSunburstChart({

    dataLabelRendering: function (args) {
              //Do something
    }
   
});

{% endhighlight %}


### segmentRendering

Fires before rendering each segment, you can use [`segmentRendering`](../api/ejsunburstchart#events:segmentrendering) event. 


#### Example


{% highlight js %}
 
//segment rendering event for sunburst

$("#container").ejSunburstChart({

    segmentRendering: function (args) {
              //Do something
    }
   
});

{% endhighlight %}



### titleRendering

Fires before rendering sunburst title, you can use [`titleRendering`](../api/ejsunburstchart#events:titlerendering) event.  


#### Example


{% highlight js %}
 
//title rendering event for sunburst

$("#container").ejSunburstChart({

    titleRendering: function (args) {
              //Do something
    }
   
});

{% endhighlight %}



### tooltipInitialize
{:#events:tooltipinitialize}




Fires during initialization of tooltip, you can use [`tooltipInitialize`](../api/ejsunburstchart#events:tooltipinitialize) event.  


#### Example


{% highlight js %}
 
//tooltip initialize event for sunburst

$("#container").ejSunburstChart({

    tooltipInitialize: function (args) {
              //Do something
    }
   
});

{% endhighlight %}



### pointRegionClick

Fires after clicking the point in sunburst, you can use [`pointRegionClick`](../api/ejsunburstchart#events:pointregionclick) event. 


#### Example


{% highlight js %}
 
//point region click event for sunburst

$("#container").ejSunburstChart({

    pointRegionClick: function (args) {
              //Do something
    }
   
});

{% endhighlight %}


### pointRegionMouseMove

Fires while moving the mouse over sunburst points, you can use [`pointRegionMouseMove`](../api/ejsunburstchart#events:pointregionmousemove) event. 

#### Example


{% highlight js %}
 
//point region mouse move event for sunburst

$("#container").ejSunburstChart({

    pointRegionMouseMove: function (args) {
              //Do something
    }
   
});

{% endhighlight %}


### drillDownClick

Fires when clicking the point to perform drilldown, you can use [`drillDownClick`](../api/ejsunburstchart#events:drilldownclick) event.  


#### Example


{% highlight js %}
 
//drill down click event for sunburst

$("#container").ejSunburstChart({

    drillDownClick: function (args) {
              //Do something
    }
   
});

{% endhighlight %}


### drillDownBack

Fires when resetting drilldown points, you can use [`drillDownBack`](../api/ejsunburstchart#events:drilldownback) event.  


#### Example


{% highlight js %}
 
//drill down back event for sunburst

$("#container").ejSunburstChart({

    drillDownBack: function (args) {
              //Do something
    }
   
});

{% endhighlight %}



### drillDownReset


Fires after resetting the sunburst points, you can use [`drillDownReset`](../api/ejsunburstchart#events:drilldownreset) event.  


#### Example


{% highlight js %}
 
//drill down reset event for sunburst

$("#container").ejSunburstChart({

    drillDownReset: function (args) {
              //Do something
    }
   
});

{% endhighlight %}

### legendItemRendering


Fires before rendering the legend item, you can use [`legendItemRendering`](../api/ejsunburstchart#events:legenditemrendering) event. 


#### Example


{% highlight js %}
 
//legend item rendering event for sunburst

$("#container").ejSunburstChart({

    legendItemRendering: function (args) {
              //Do something
    }
   
});

{% endhighlight %}


### legendItemClick


Fires when clicking the legend item, you can use [`legendItemClick`](../api/ejsunburstchart#events:legenditemclick) event.


#### Example


{% highlight js %}
 
//legend item click event for sunburst

$("#container").ejSunburstChart({

    legendItemClick: function (args) {
              //Do something
    }
   
});

{% endhighlight %}


### Click

Fires when clicking the sunburst points, you can use [`click`](../api/ejsunburstchart#events:click) event.



{% highlight js %}
 
//Click event for sunburst chart

 $("#container").ejSunburstChart({


    click: function (args) {
              //Do something
    }
   
});

{% endhighlight %}


### doubleClick

Fires when double clicking the sunburst points, you can use [`doubleClick`](../api/ejsunburstchart#events:doubleclick) event.



{% highlight js %}
 
//DoubleClick event for sunburst chart

 $("#container").ejSunburstChart({


    doubleClick: function (args) {
              //Do something
    }
   
});

{% endhighlight %}



### rightClick


Fires when right clicking the sunburst points, you can use [`rightClick`](../api/ejsunburstchart#events:rightclick) event.


{% highlight js %}
 
//RightClick event for sunburst chart

 $("#container").ejSunburstChart({

    rightClick: function (args) {
              //Do something
    }
   
});

{% endhighlight %}

