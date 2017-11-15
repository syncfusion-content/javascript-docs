---
layout: post
title: Public Methos and Events
description: Learn how to add public methos and events to Sunburstchart .
platform: ts
control: Sunburst Chart
documentation: ug
api: /api/js/ejsunburstchart
---

## Methods


### redraw()

[`redraw`](../api/js/ejsunburstchart#methods:redraw) the entire sunburst. You can call this method whenever you update, add or remove points from the data source or whenever you want to refresh the UI.


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

[`destroy`](../api/js/ejsunburstchart#methods:destroy) the sunburst


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

Fires before loading, you can use [`load`](../api/js/ejsunburstchart#events:load) event.

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

Fires before rendering sunburst, you can use [`preRender`](../api/js/ejsunburstchart#events:prerender) event. 


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

Fires after rendering sunburst, you can use [`loaded`](../api/js/ejsunburstchart#events:loaded) event.  


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

Fires before rendering the datalabel, you can use [`dataLabelRendering`](../api/js/ejsunburstchart#events:datalabelrendering) event. 


#### Example


{% highlight js %}
 
//datalabelrendering event for sunburst

$("#container").ejSunburstChart({

    dataLabelRendering: function (args) {
              //Do something
    }
   
});

{% endhighlight %}


### segmentRendering

Fires before rendering each segment, you can use [`segmentRendering`](../api/js/ejsunburstchart#events:segmentrendering) event. 


#### Example


{% highlight js %}
 
//segmentrendering event for sunburst

$("#container").ejSunburstChart({

    segmentRendering: function (args) {
              //Do something
    }
   
});

{% endhighlight %}



### titleRendering

Fires before rendering sunburst title, you can use [`titleRendering`](../api/js/ejsunburstchart#events:titlerendering) event.  


#### Example


{% highlight js %}
 
//titlerendering event for sunburst

$("#container").ejSunburstChart({

    titleRendering: function (args) {
              //Do something
    }
   
});

{% endhighlight %}



### tooltipInitialize
{:#events:tooltipinitialize}




Fires during initialization of tooltip, you can use [`tooltipInitialize`](../api/js/ejsunburstchart#events:tooltipinitialize) event.  


#### Example


{% highlight js %}
 
//tooltipinitialize event for sunburst

$("#container").ejSunburstChart({

    tooltipInitialize: function (args) {
              //Do something
    }
   
});

{% endhighlight %}



### pointRegionClick

Fires after clicking the point in sunburst, you can use [`pointRegionClick`](../api/js/ejsunburstchart#events:pointregionclick) event. 


#### Example


{% highlight js %}
 
//pointregionclick event for sunburst

$("#container").ejSunburstChart({

    pointRegionClick: function (args) {
              //Do something
    }
   
});

{% endhighlight %}


### pointRegionMouseMove

Fires while moving the mouse over sunburst points, you can use [`pointRegionMouseMove`](../api/js/ejsunburstchart#events:pointregionmousemove) event. 

#### Example


{% highlight js %}
 
//pointregionmousemove event for sunburst

$("#container").ejSunburstChart({

    pointRegionMouseMove: function (args) {
              //Do something
    }
   
});

{% endhighlight %}


### drillDownClick

Fires when clicking the point to perform drilldown, you can use [`drillDownClick`](../api/js/ejsunburstchart#events:drilldownclick) event.  


#### Example


{% highlight js %}
 
//drilldownclick event for sunburst

$("#container").ejSunburstChart({

    drillDownClick: function (args) {
              //Do something
    }
   
});

{% endhighlight %}


### drillDownBack

Fires when resetting drilldown points, you can use [`drillDownBack`](../api/js/ejsunburstchart#events:drilldownback) event.  


#### Example


{% highlight js %}
 
//drilldownback event for sunburst

$("#container").ejSunburstChart({

    drillDownBack: function (args) {
              //Do something
    }
   
});

{% endhighlight %}



### drillDownReset


Fires after resetting the sunburst points, you can use [`drillDownReset`](../api/js/ejsunburstchart#events:drilldownreset) event.  


#### Example


{% highlight js %}
 
//drilldownreset event for sunburst

$("#container").ejSunburstChart({

    drillDownReset: function (args) {
              //Do something
    }
   
});

{% endhighlight %}

### legendItemRendering


Fires before rendering the legend item, you can use [`legendItemRendering`](../api/js/ejsunburstchart#events:legenditemrendering) event. 


#### Example


{% highlight js %}
 
//drilldownreset event for sunburst

$("#container").ejSunburstChart({

    legendItemRendering: function (args) {
              //Do something
    }
   
});

{% endhighlight %}


### legendItemClick


Fires when clicking the legend item, you can use [`legendItemClick`](../api/js/ejsunburstchart#events:legenditemclick) event.


#### Example


{% highlight js %}
 
//drilldownreset event for sunburst

$("#container").ejSunburstChart({

    legendItemClick: function (args) {
              //Do something
    }
   
});

{% endhighlight %}

