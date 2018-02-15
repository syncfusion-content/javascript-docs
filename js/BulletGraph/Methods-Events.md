---
layout: post
title: Methods-Events
description: methods and events in bullet graph
platform: js
control: BulletGraph	
documentation: ug
api: /api/js/ejbulletgraph
---

# Methods

## destroy()

[`Destroy`](../api/ejbulletgraph#methods:destroy) method is used to destroy the bullet graph control.

#### Returns: void

{% highlight html %}
 
<div id="bulletgraph1">Bullet Graph</div> 
 
<script>
// Destroy Bullet graph
var graphObj = $("#bulletGraph1").data("ejBulletGraph");
graphObj.destroy(); // destroy the graph
</script>

{% endhighlight %}



## redraw()

[`Redraw`](../api/ejbulletgraph#methods:redraw) method is used to redraw the bullet graph with updated values.

#### Returns: void

{% highlight html %}
 
<div id="bulletgraph1">Bullet Graph</div> 
 
<script>
// Create Bullet graph
var graphObj = $("#bulletGraph1").data("ejBulletGraph");
graphObj.redraw(); // redraw the graph
</script>

{% endhighlight %}



## setComparativeMeasureSymbol(index, measure)

To set the comparative measure in bullet graph, you can use [`setComparativeMeasureSymbol`](../api/ejbulletgraph#methods:setcomparativemeasuresymbol) method.


#### Returns: void

{% highlight html %}
 
<div id="bulletGraph1">BulletGraph</div> 
 
<script>
// set the value for comparative measure
var btnObj = $("#bulletGraph1").data("ejBulletGraph");
btnObj.setComparativeMeasureSymbol(1,7); // set the value
</script>

{% endhighlight %}


{% highlight html %}
 
<div id="bulletGraph1">BulletGraph</div> 
 
<script>
// set the value for comparative measure
$("#bulletGraph1").ejBulletGraph("setComparativeMeasureSymbol(1,7)");   
</script>

{% endhighlight %}

## setFeatureMeasureBarValue(index, measure)

To set the value for feature measure bar, you can use [`setFeatureMeasureBarValue`](../api/ejbulletgraph#methods:setfeaturemeasurebarvalue) method.


#### Returns: void

{% highlight html %}
 
<div id="bulletGraph1">Bulletgraph</div> 
 
<script>
// To set the value for feature measure bar.
var btnObj = $("#bulletGraph1").data("ejBulletGraph");
btnObj.setFeatureMeasureBarValue(1,8); // set the value
</script>

{% endhighlight %}


{% highlight html %}
 
<div id="bulletGraph1">BulletGraph</div> 
 
<script>
// To set the value for feature measure bar.
$("#bulletGraph1").ejBulletGraph("setFeatureMeasureBarValue(1,8)");     
</script>

{% endhighlight %}

# Events

## drawCaption

[`drawCaption`](../api/ejbulletgraph#events:drawcaption) event will fire before rendering bullet graph caption.

{% highlight html %}
 
<script>
//drawCaption event for bulletgraph
$("#bulletGraph1").ejBulletGraph({
   drawCaption: function (args) {}
});
</script>

{% endhighlight %}

## drawCategory

[`drawCategory`](../api/ejbulletgraph#events:drawcategory) event will fire while rendering the category.

{% highlight html %}

<script> 
//drawCategory event for bulletgraph
$("#bulletGraph1").ejBulletGraph({
   drawCategory: function (args) {}
});
</script>

{% endhighlight %}

## drawComparativeMeasureSymbol

[`drawComparativeMeasureSymbol`](../api/ejbulletgraph#events:drawcomparativemeasuresymbol) event fires on rendering the comparative measure symbol.

{% highlight html %}
 
<script>
//drawComparativeMeasureSymbol event for bulletgraph
$("#bulletGraph1").ejBulletGraph({
   drawComparativeMeasureSymbol: function (args) {}
});
</script>

{% endhighlight %}

## drawFeatureMeasureBar

[`drawFeatureMeasureBar`](../api/ejbulletgraph#events:drawfeaturemeasurebar) event fires on rendering the feature measure bar.

{% highlight html %}
 
<script>
//drawFeatureMeasureBar event for bulletgraph
$("#bulletGraph1").ejBulletGraph({
   drawFeatureMeasureBar: function (args) {}
});
</script>

{% endhighlight %}

## drawIndicator

[`drawIndicator`](../api/ejbulletgraph#events:drawindicator) event fires on rendering the indicator of the bullet graph.

{% highlight html %}
 
<script>
//drawIndicator event for bulletgraph
$("#bulletGraph1").ejBulletGraph({
   drawIndicator: function (args) {}
});
</script>

{% endhighlight %}

## drawLabels

[`drawLabels`](../api/ejbulletgraph#events:drawlabels) event fires on rendering the bullet graph labels.

{% highlight html %}
 
<script>
//drawLabels event for bulletgraph
$("#bulletGraph1").ejBulletGraph({
   drawLabels: function (args) {}
});
</script>

{% endhighlight %}

## drawTicks

[`drawTicks`](../api/ejbulletgraph#events:drawticks) event fires while drawing the ticklines of the bullet graph.

{% highlight html %}
 
<script>
//drawTicks event for bulletgraph
$("#bulletGraph1").ejBulletGraph({
   drawTicks: function (args) {}
});
</script>

{% endhighlight %}

## drawQualitativeRanges

[`drawQualitativeRanges`](../api/ejbulletgraph#events:drawqualitativeranges) event fires while rendering the qualitative ranges.

{% highlight html %}
 
<script>
//drawQualitativeRanges event for bulletgraph
$("#bulletGraph1").ejBulletGraph({
   drawQualitativeRanges: function (args) {}
});
</script>

{% endhighlight %}

## load

[`load`](../api/ejbulletgraph#events:load) event fires on loading the bullet graph.

{% highlight html %}
 
<script>
//drawTicks event for bulletgraph
$("#bulletGraph1").ejBulletGraph({
   load: function (args) {}
});
</script>

{% endhighlight %}

## click

[`click`](../api/ejbulletgraph#events:click) event fires on clicking the bullet graph.

{% highlight html %}
 
<script>
//click event for bulletgraph
$("#bulletGraph1").ejBulletGraph({

    click: function (args) {
              //Do something
    }
   
});
</script>

{% endhighlight %}


## doubleClick

[`doubleClick`](../api/ejbulletgraph#events:doubleclick) event fires on double clicking the bullet graph.

{% highlight html %}
 
<script>
//doubleClick event for bulletgraph
$("#bulletGraph1").ejBulletGraph({

    doubleClick: function (args) {
              //Do something
    }
   
});
</script>

{% endhighlight %}


## rightClick

[`rightClick`](../api/ejbulletgraph#events:rightclick) event fires on right clicking the bullet graph.


{% highlight html %}
 
<script>
//rightClick event for bulletgraph
$("#bulletGraph1").ejBulletGraph({
    rightClick: function (args) {
              //Do something
    }
   
});
</script>

{% endhighlight %}
