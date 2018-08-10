---
layout: post
title: Public Methods and Events
description: Public methods and events
platform: js
control: Maps
documentation: ug
api: /api/js/ejmap
---


## Methods

### navigateTo(latitude, longitude, level)

Method for navigating to specific shape based on latitude, longitude and zoom level, you can use [`navigateTo`](../api/ejmap#methods:navigateto) method.


{% highlight js %}
 
//navigateTo method for map
   $("#container").ejMap("navigateTo", latitude, longitude, level);
   
{% endhighlight %}


### pan(direction)

Method to perform map panning, you can use [`pan`](../api/ejmap#methods:pan) method.


{% highlight js %}
 
//pan method for map
   $("#container").ejMap("pan", direction);

{% endhighlight %}


### refresh()

Method to reload the map, you can use [`refresh`](../api/ejmap#methods:refresh) method.


{% highlight js %}
 
//refresh method for map
   $("#container").ejMap("refresh");

{% endhighlight %}


### refreshLayers()

Method to reload the shapeLayers with updated values, you can use [`refreshLayers`](../api/ejmap#methods:refreshlayers) method.


{% highlight js %}
 
//refresh layers method for map
   $("#container").ejMap("refreshLayers");

{% endhighlight %}


### refreshNavigationControl(navigation)

Method to reload the navigation control with updated values, you can use [`refreshNavigationControl`](../api/ejmap#methods:refreshnavigationcontrol) method.


{% highlight js %}
 
//Refresh navigation control method for map
   $("#container").ejMap("refreshNavigationControl",navigation);{% endhighlight %}


### zoom(level, isAnimate)

Method to perform map zooming, you can use [`zoom`](../api/ejmap#methods:zoom) method.


{% highlight js %}
 
//zoom method for map
   $("#container").ejMap("zoom",level,isAnimate);

{% endhighlight %}



## Events

### markerSelected

Triggered on selecting the map markers, you can use [`markerSelected`](../api/ejmap#events:markerselected) event.


{% highlight js %}
 
//markerSelected event for map
  
  $("#container").ejMap({
   markerSelected: function (event) {}
  });

{% endhighlight %}


### mouseleave

Triggers while leaving the hovered map shape, you can use [`mouseleave`](../api/ejmap#events:mouseleave) event.


{% highlight js %}
 
//mouseleave  event for map
  $("#container").ejMap({
   mouseleave : function (event) {}
  });

{% endhighlight %}


### mouseover

Triggers while hovering the map shape, you can use [`mouseover`](../api/ejmap#events:mouseover) event.


{% highlight js %}
 
//mouseover  event for map
  $("#container").ejMap({
   mouseover : function (event) {}
  });

{% endhighlight %}


### onRenderComplete

Triggers once map render completed, you can use [`onRenderComplete`](../api/ejmap#events:onrendercomplete) event.


{% highlight js %}
 
//onRenderComplete event for map
  $("#container").ejMap({
   onRenderComplete: function () {}
  });
  
{% endhighlight %}


### panned

Triggers when map panning ends, you can use [`panned`](../api/ejmap#events:panned) event.


{% highlight js %}
 
//panned event for map
  $("#container").ejMap({
   panned: function (event) {}
  });
{% endhighlight %}


### shapeSelected

Triggered on selecting the map shapes, you can use [`shapeSelected`](../api/ejmap#events:shapeselected) event.


{% highlight js %}
 
//shapeSelected event for map
  $("#container").ejMap({
   shapeSelected: function (event) {}
  });

{% endhighlight %}


### zoomedIn

Triggered when map is zoomed-in, you can use [`zoomedIn`](../api/ejmap#events:zoomedin) event.



{% highlight js %}
 
//zoomedIn event for map
  $("#container").ejMap({
   zoomedIn: function (event) {}
  });

{% endhighlight %}


### zoomedOut

Triggers when map is zoomed out, you can use [`zoomedOut`](../api/ejmap#events:zoomedout) event.



{% highlight js %}
 
//zoomedOut event for map
  $("#container").ejMap({
   zoomedOut: function () {}
  });

{% endhighlight %}

### shapeRendering

The [`shapeRendering`](../api/ejmap#events:shaperendering) event is triggered while rendering each shape in the map.

{% highlight js %}

//shapeRendering event for map
  $("#container").ejMap({
   shapeRendering : function (event) {}
  });

{% endhighlight %}


### bubbleRendering

The [`bubbleRendering`](../api/ejmap#events:bubblerendering) event is triggered while rendering each bubble in the map.

{% highlight js %}

//bubbleRendering event for map
  $("#container").ejMap({
   bubbleRendering : function (event) {}
  });

{% endhighlight %}


### legendItemRendering

The [`legendItemRendering`](../api/ejmap#events:legenditemrendering) event is triggered before rendering each legend in the map.

{% highlight js %}

//legendItemRendering event for map
  $("#container").ejMap({
   legendItemRendering : function (event) {}
  });

{% endhighlight %}


### Click

Triggers while clicking on the layers of the map, you can use [`click`](../api/ejmap#events:click) event.


{% highlight js %}
 
//Click event for map

$("#container").ejMap({

    click: function (args) {
              //Do something
    }
   
});

{% endhighlight %}


### doubleClick

Triggers while double clicking on the layers of the map, you can use [`doubleClick`](../api/ejmap#events:doubleclick) event.


{% highlight js %}
 
//DoubleClick event for map.

$("#container").ejMap({

    doubleClick: function (args) {
              //Do something
    }
   
});

{% endhighlight %}



### rightClick

Triggers while right clicking on the layers of the map, you can use [`rightClick`](../api/ejmap#events:rightclick) event.



{% highlight js %}
 
//RightClick event for map

$("#container").ejMap({
    rightClick: function (args) {
              //Do something
    }
   
});

{% endhighlight %}


### onLoad

Triggers before loading the map, you can use [`onLoad`](../api/ejmap#events:onload) event.



{% highlight js %}
 
//onLoad event for map

$("#container").ejMap({
    onLoad: function (args) {
              //Do something
    }
   
});

{% endhighlight %}


### displayTextRendering

The [`displayTextRendering`](../api/ejmap#events:displaytextrendering) event is triggered before rendering the data labels. You can use this event to customize the label text or change the text value.



{% highlight js %}
 
//The displayTextRendering event for maps

$("#container").ejMap({

    displayTextRendering: function (args) {
             //Do something
    }
	
});

{% endhighlight %}



<a class="" href="http://www.syncfusion.com/copyright" target="_blank">Copyright &copy; 2001 - 2015 Syncfusion Inc. All Rights Reserved</a>

