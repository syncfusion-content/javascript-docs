---
layout: post
title: Methods and Events in Digital Gauge
description: explains the methods and events in digital gauge
platform: js
control: Digital Gauge
documentation: ug
api : /api/js/ejdigitalgauge
---

# Methods

## destroy

You can destroy the **Digital Gauge** widget by calling it's [`destroy()`](../api/ejdigitalgauge#methods:destroy) method.

{% highlight html %}

<div id="DigitalGauge1">Digital Gauge</div> 

<script>
$("#DigitalGauge1").ejDigitalGauge();
var graphObj = $("#DigitalGauge1").data("ejDigitalGauge");
graphObj.destroy();
</script>

{% endhighlight %}

## getPosition(itemIndex)

To get the location of an item that is displayed on the gauge you can use [`getPosition()`](../api/ejdigitalgauge#methods:getposition) method.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
itemIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Position value of an item that is displayed on the gauge.</td>
</tr>
</tbody>
</table>

#### Returns: object

{% highlight html %}
 
<div id="DigitalGauge1"></div> 
 
<script>
$("#DigitalGauge1").ejDigitalGauge();
var DigitalGaugeObj = $("#DigitalGauge1").data("ejDigitalGauge");
DigitalGaugeObj.getPosition(0); 
</script>

{% endhighlight %}

## getValue(itemIndex)

You can get the value of the item that is displayed on the gauge using [`getValue()`](../api/ejdigitalgauge#methods:getvalue) method.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
itemIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Index value of an item that displayed on the gauge</td>
</tr>
</tbody>
</table>

#### Returns: object

{% highlight html %}
 
<div id="DigitalGauge1"></div> 
 
<script>
$("#DigitalGauge1").ejDigitalGauge();
var DigitalGaugeObj = $("#DigitalGauge1").data("ejDigitalGauge");
DigitalGaugeObj.getValue(0);    
</script>

{% endhighlight %}

## refresh()

To refresh the **Digital Gauge**, you can call it's [`refresh`](../api/ejdigitalgauge#methods:refresh) method.

{% highlight html %}
 
<div id="DigitalGauge1"></div> 
 
<script>
$("#DigitalGauge1").ejDigitalGauge();
var GaugeObj = $("#DigitalGauge1").data("ejDigitalGauge");
GaugeObj.refresh();
</script>     

{% endhighlight %}

## setPosition(itemIndex, value)

Using [`setPosition()`](../api/ejdigitalgauge#methods:setposition) method, you can set the location of an item to be displayed in the digital gauge.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
itemIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Index value of the digital gauge item</td>
</tr>
<tr>
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Location value of the digital gauge</td>
</tr>
</tbody>
</table>

{% highlight html %}
 
<div id="DigitalGauge1"></div> 
 
<script>
$("#DigitalGauge1").ejDigitalGauge();
var DigitalGaugeObj = $("#DigitalGauge1").data("ejDigitalGauge");
DigitalGaugeObj.setPosition(0,{ x:50, y:40 });  
</script>

{% endhighlight %}

## setValue(itemIndex, value)

Using [`setValue`](../api/ejdigitalgauge#methods:setvalue) method,you can set the value of an item to be displayed in the digital gauge. 

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
itemIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Index value of the digital gauge item</td>
</tr>
<tr>
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Text value to be displayed in the gaugeS</td>
</tr>
</tbody>
</table>

{% highlight html %}
 
<div id="DigitalGauge1"></div> 
 
<script>
$("#DigitalGauge1").ejDigitalGauge();
var DigitalGaugeObj = $("#DigitalGauge1").data("ejDigitalGauge");
DigitalGaugeObj.setValue(0,"Welcome");
</script>

{% endhighlight %}

# Events

## init

[`init`](../api/ejdigitalgauge#events:init) event triggers, when gauge is initialized.

{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({
   init: function (args) {}
});      
</script>

{% endhighlight %}

## itemRendering

[`itemRendering`](../api/ejdigitalgauge#events:itemrendering) event triggers, when gauge item is rendering.

{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({
   itemRendering: function (args) {}
});      
</script>

{% endhighlight %}

## load

[`load`](../api/ejdigitalgauge#events:load) event triggers, when gauge is starting to load.

{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({
   load: function (args) {}
});      
</script>

{% endhighlight %}

## renderComplete

[`renderComplete`](../api/ejdigitalgauge#events:rendercomplete) event triggers, when gauge rendering is completed. 

{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({
   renderComplete: function (args) {}
});       
</script>

{% endhighlight %}

## click

[`click`](../api/ejdigitalgauge#events:click) event triggers on clicking the gauges. 


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({

    click: function (args) {
              //Do something
    }
   
});      
</script>

{% endhighlight %}


## doubleClick

[`doubleClick`](../api/ejdigitalgauge#events:doubleclick) event triggers on double clicking the gauges. 


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({

    doubleClick: function (args) {
              //Do something
    }
   
});       
</script>

{% endhighlight %}


### rightClick

[`rightClick`](../api/ejdigitalgauge#events:rightclick) event triggers on right clicking the gauges. 


{% highlight html %}
 
<div id="DigitalCore"></div> 
 
<script>
$("#DigitalCore").ejDigitalGauge({
    rightClick: function (args) {
              //Do something
    }
   
});       
</script>

{% endhighlight %}



