---
layout: post
title: Properties,methods and events of Essential JS ejProgressBar widget
description: API reference for ejProgressBar
documentation: API
platform: js
keywords: ProgressBar, ejProgressBar, syncfusion, ProgressBar api 
---

# ejProgressBar




The ProgressBar control is a graphical control element used to visualize the changing status of an extended operation.








#### Syntax

{% highlight javascript %}

$(element).ejProgressBar()

{% endhighlight %}













#### Example



{% highlight html %}
<div id="progress"></div>
<script>
$("#progress").ejProgressBar({value: 50});
</script>{% endhighlight %}







#### Requires


* module:jQuery


* module:jquery.easing.1.3.js


* module:ej.core.js


* module:ej.progressbar.js




## Members








### cssClass `string`
{:#members:cssclass}








Sets the root CSS class for ProgressBar theme, which is used customize. 




#### Default Value







* null








#### Example



{% highlight html %}
 
<div id="progress"></div>
<script>
//Initialize the ProgressBar with the cssClass value specified
$("#progress").ejProgressBar({ cssClass: 'gradient-lime ',value: 50  });
</script>{% endhighlight %}







### enabled `boolean`
{:#members:enabled}








When this property sets to false, it disables the ProgressBar control




#### Default Value







* true








#### Example



{% highlight html %}
<div id="progress"></div>
<script>
//Initialize the ProgressBar with the enabled value specified
$("#progress").ejProgressBar({ enabled: true,value: 50 });
</script>{% endhighlight %}







### enablePersistence `boolean`
{:#members:enablepersistence}








Save current model value to browser cookies for state maintains. While refresh the progressBar control page retains the model value apply from browser cookies




#### Default Value







* false








#### Example



{% highlight html %}
 
<div id="progress"></div>
<script>
//Initialize the Progress bar with the persist value specified
$("#progress").ejProgressBar({ enablePersistence: true,value: 50 });
</script>{% endhighlight %}







### enableRTL `boolean`
{:#members:enablertl}








Sets the ProgressBar direction as right to left alignment.




#### Default Value







* false








#### Example



{% highlight html %}
<div id="progress"></div>
<script>
//Initialize the Progress bar with the rtl value specified
$("#progress").ejProgressBar({ enableRTL: true,value: 50 });
</script>{% endhighlight %}







### height `number|string`
{:#members:height}








Defines the height of the ProgressBar.




#### Default Value







* null








#### Example



{% highlight html %}
 
<div id="progress"></div>
<script>
//Initialize the ProgressBar with the height value specified
$("#progress").ejProgressBar({ height: 20,value: 50 });
</script>{% endhighlight %}



### htmlAttributes `object`
{:#members:htmlattributes}

It allows to define the characteristics of the progressBar control. It will helps to extend the capability of an HTML element.

#### Default Value

* {}

#### Example

{% highlight html %}
 
<div id="progress"></div>
<script>
//Initialize the ProgressBar with htmlAttributes specified
$("#progress").ejProgressBar({ htmlAttributes: { title: "Demo" } });
</script>{% endhighlight %}




### maxValue `number`
{:#members:maxvalue}








Sets the maximum value of the ProgressBar.




#### Default Value







* 100








#### Example



{% highlight html %}
 
<div id="progress"></div>
<script>
//Initialize the ProgressBar with the max value specified
$("#progress").ejProgressBar({ maxValue: 200 ,value: 200 });
</script>{% endhighlight %}







### minValue `number`
{:#members:minvalue}








Sets the minimum value of the ProgressBar.




#### Default Value







* 0








#### Example



{% highlight html %}
<div id="progress"></div>
<script>
//Initialize the ProgressBar with the min value specified
$("#progress").ejProgressBar({ minValue: 50,value: 50});
</script>{% endhighlight %}







### percentage `number`
{:#members:percentage}








Sets the ProgressBar value in percentage. The value should be in between 0 to 100.




#### Default Value







* 0








#### Example



{% highlight html %}
<div id="progress"></div>
<script>
//Initialize the ProgressBar with the progress value specified in percent
$("#progress").ejProgressBar({ percentage : 35 });
</script>{% endhighlight %}



### showRoundedCorner `boolean`
{:#members:showroundedcorner}

Displays rounded corner borders on the progressBar control.

#### Default Value

* false

#### Example

{% highlight html %}
<div id="progress"></div>
<script>
//Initialize the ProgressBar with the rounded corner support.
$("#progress").ejProgressBar({ showRoundedCorner: true });
</script>{% endhighlight %}



### text `string`
{:#members:text}








Sets the custom text for the ProgressBar. The text placed in the middle of the ProgressBar and it can be customizable using the class 'e-progress-text'.




#### Default Value







* null








#### Example



{% highlight html %}
 
<div id="progress"></div>
<script> 
//To set the text API value during initialization  
$("#progress").ejProgressBar({ text: 'loading...',value: 50 });
</script>{% endhighlight %}







### value `number`
{:#members:value}








Sets the ProgressBar value. The value should be in between min and max values.




#### Default Value







* 0








#### Example



{% highlight html %}
<div id="progress"></div>
<script>
//Initialize the ProgressBar with the progress value specified
$("#progress").ejProgressBar({ value: 70 });
</script>{% endhighlight %}







### width `number|string`
{:#members:width}








Defines the width of the ProgressBar.




#### Default Value







* null








#### Example



{% highlight html %}
 
<div id="progress"></div>
<script>
//Initialize the ProgressBar with the width value specified
$("#progress").ejProgressBar({ width: 200,value: 50});
</script>{% endhighlight %}





## Methods








### destroy()
{:#methods:destroy}








Destroy the progressbar widget





#### Example



{% highlight html %}
<div id="progress"></div>
<script>
$("#progress").ejProgressBar({value: 50});
// Create Progressbar instance
var proObj = $("#progress").data("ejProgressBar");
proObj.destroy(); //destroy the Progressbar control
</script>
        {% endhighlight %}


{% highlight html %}
<div id="progress"></div>
<script>
$("#progress").ejProgressBar({value: 50});
        // To destroy the Progressbar control
$("#progress").ejProgressBar("destroy");
</script>{% endhighlight %}







### disable()
{:#methods:disable}








Disables the progressbar control





#### Example



{% highlight html %}
<div id="progress"></div>
<script>
$("#progress").ejProgressBar({value: 50});
// Create Progressbar instance
var proObj = $("#progress").data("ejProgressBar");
proObj.disable(); //disables the Progressbar control
</script>
        {% endhighlight %}


{% highlight html %}
<div id="progress"></div>
<script>
$("#progress").ejProgressBar({value: 50});
        //To disables the Progressbar control
$("#progress").ejProgressBar("disable");
</script>{% endhighlight %}







### enable()
{:#methods:enable}








Enables the progressbar control





#### Example



{% highlight html %}
<div id="progress"></div>
<script>
$("#progress").ejProgressBar({value: 50});
// Create Progressbar instance
var proObj = $("#progress").data("ejProgressBar");
proObj.enable(); // enables the Progressbar control
</script>
        {% endhighlight %}


{% highlight html %}
<div id="progress"></div>
<script>
$("#progress").ejProgressBar({value: 50});
        // To enables the Progressbar control
$("#progress").ejProgressBar("enable");
</script>{% endhighlight %}







### getPercentage()
{:#methods:getpercent}




Returns the current progress value in percent.


#### Returns:
{:#methods:returns:}

number





#### Example



{% highlight html %}
<div id="progress"></div>
<script>
$("#progress").ejProgressBar({value: 50});
// Create Progressbar instance
var proObj = $("#progress").data("ejProgressBar");
proObj.getPercentage(); // get the percent of Progressbar control
</script>
        {% endhighlight %}


{% highlight html %}
<div id="progress"></div>
<script>
$("#progress").ejProgressBar({value: 50});
        // To get the percent of Progressbar control
$("#progress").ejProgressBar("getPercentage");
</script>{% endhighlight %}







### getValue()
{:#methods:getvalue}




Returns the current progress value



#### Returns:
{:#methods:returns:}

number





#### Example



{% highlight html %}
<div id="progress"></div>
<script>
$("#progress").ejProgressBar({value: 50});
// Create Progressbar instance
var proObj = $("#progress").data("ejProgressBar");
proObj.getValue(); // get the value of Progressbar control
</script>
        {% endhighlight %}


{% highlight html %}
<div id="progress"></div>
<script>
$("#progress").ejProgressBar({value: 50});
        // To get the value of Progressbar control 
$("#progress").ejProgressBar("getValue");
</script>{% endhighlight %}





## Events








### change
{:#events:change}








Event triggers when the progress value changed


<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns the cancel option value</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.ProgressBar.Model"/><span class="param-type">object</span></td>
<td class="description">returns the ProgressBar model</td>
</tr>
<tr>
<td class="name">
percentage</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the current progress percentage</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
value</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the current progress value</td>
</tr>
</tbody>
</table>





#### Example



{% highlight html %}
<div id="progress"></div>
<script>
//initial complete event
$("#progress").ejProgressBar({
        value: 50,
        change: function(args) {}
});
</script>{% endhighlight %}







### complete
{:#events:complete}








Event triggers when the process completes (at 100%)


<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns the cancel option value</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.ProgressBar.Model"/><span class="param-type">object</span></td>
<td class="description">returns the ProgressBar model</td>
</tr>
<tr>
<td class="name">
percentage</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the current progress percentage</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
value</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the current progress value</td>
</tr>
</tbody>
</table>





#### Example



{% highlight html %}
<div id="progress"></div>
<script>
//initial complete event
$("#progress").ejProgressBar({
        value: 50,
        complete: function(args) {}
});
</script>{% endhighlight %}







### create
{:#events:create}








Event triggers when the progressbar are created


<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.ProgressBar.Model"/><span class="param-type">object</span></td>
<td class="description">returns the progressbar model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>





#### Example



{% highlight html %}
 
<div id="progress"></div> 
 
<script>
//create event for progressbar
$("#progress").ejProgressBar({
        value: 50,
        create: function(args) {}
});
</script>{% endhighlight %}







### destroy
{:#events:destroy}








Event triggers when the progressbar are destroyed


<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.ProgressBar.Model"/><span class="param-type">object</span></td>
<td class="description">returns the progressbar model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>





#### Example



{% highlight html %}
 
<div id="progress"></div> 
 
<script>
//destroy event for progressbar
$("#progress").ejProgressBar({
        value: 50,
        destroy: function(args) {}
});
</script>{% endhighlight %}







### start
{:#events:start}








Event triggers when the process starts (from 0%)


<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns the cancel option value</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.ProgressBar.Model"/><span class="param-type">object</span></td>
<td class="description">returns the ProgressBar model</td>
</tr>
<tr>
<td class="name">
percentage</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the current progress percentage</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
value</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the current progress value</td>
</tr>
</tbody>
</table>





#### Example



{% highlight html %}
<div id="progress"></div>
<script>
//initial start event
$("#progress").ejProgressBar({
        value: 50,
        start: function(args) {}
});
</script>{% endhighlight %}




