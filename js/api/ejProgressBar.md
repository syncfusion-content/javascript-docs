---
layout: post
title: ejProgressBar
documentation: API
platform: js
metaname: 
metacontent: 
---

# ejProgressBar




The ProgressBar control is a graphical control element used to visualize the changing status of an extended operation.










$(element).ejProgressBar<span class="signature">()</span>











Example
{:.example}


{% highlight html %}
<div id="progress"></div>
<script>
$("#progress").ejProgressBar({value: 50});
</script>{% endhighlight %}







Requires
{:.require}




* module:jQuery


* module:jquery.easing.1.3.js


* module:ej.core.js


* module:ej.progressbar.js




## Members








### cssClass<span class="type-signature type string">String</span>
{:#members:cssclass}








Sets the root class for ProgressBar theme. This cssClass API helps to use custom skinning option for ProgressBar control. By defining the root class using this API, we need to include this root class in CSS.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="progress"></div>
<script>
//Initialize the ProgressBar with the cssClass value specified
$("#progress").ejProgressBar({ cssClass: 'gradient-lime ',value: 50  });
</script>{% endhighlight %}







### enabled<span class="type-signature type boolean">boolean</span>
{:#members:enabled}








When this property sets to false, it disables the ProgressBar control




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
<div id="progress"></div>
<script>
//Initialize the ProgressBar with the enabled value specified
$("#progress").ejProgressBar({ enabled: true,value: 50 });
</script>{% endhighlight %}







### enablePersistence<span class="type-signature type boolean">boolean</span>
{:#members:enablepersistence}








Save current model value to browser cookies for state maintains. While refresh the progressBar control page retains the model value apply from browser cookies




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="progress"></div>
<script>
//Initialize the Progress bar with the persist value specified
$("#progress").ejProgressBar({ enablePersistence: true,value: 50 });
</script>{% endhighlight %}







### enableRTL<span class="type-signature type boolean">boolean</span>
{:#members:enablertl}








Sets the ProgressBar direction as right to left alignment.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
<div id="progress"></div>
<script>
//Initialize the Progress bar with the rtl value specified
$("#progress").ejProgressBar({ enableRTL: true,value: 50 });
</script>{% endhighlight %}







### height<span class="type-signature type number/string">Number/String</span>
{:#members:height}








Defines the height of the ProgressBar.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="progress"></div>
<script>
//Initialize the ProgressBar with the height value specified
$("#progress").ejProgressBar({ height: 20,value: 50 });
</script>{% endhighlight %}







### maxValue<span class="type-signature type number">Number</span>
{:#members:maxvalue}








Sets the maximum value of the ProgressBar.




Default Value:
{:.param}






* 100








Example
{:.example}


{% highlight html %}
 
<div id="progress"></div>
<script>
//Initialize the ProgressBar with the max value specified
$("#progress").ejProgressBar({ maxValue: 200 ,value: 200 });
</script>{% endhighlight %}







### minValue<span class="type-signature type number">Number</span>
{:#members:minvalue}








Sets the minimum value of the ProgressBar.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="progress"></div>
<script>
//Initialize the ProgressBar with the min value specified
$("#progress").ejProgressBar({ minValue: 50,value: 50});
</script>{% endhighlight %}







### percentage<span class="type-signature type number">Number</span>
{:#members:percentage}








Sets the ProgressBar value in percentage. The value should be in between 0 to 100.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="progress"></div>
<script>
//Initialize the ProgressBar with the progress value specified in percent
$("#progress").ejProgressBar({ percentage : 35 });
</script>{% endhighlight %}







### text<span class="type-signature type string">String</span>
{:#members:text}








Sets the custom text for the ProgressBar. The text placed in the middle of the ProgressBar and it can be customizable using the class 'e-progress-text'.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="progress"></div>
<script> 
//To set the text API value during initialization  
$("#progress").ejProgressBar({ text: 'loading...',value: 50 });
</script>{% endhighlight %}







### value<span class="type-signature type number">Number</span>
{:#members:value}








Sets the ProgressBar value. The value should be in between min and max values.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="progress"></div>
<script>
//Initialize the ProgressBar with the progress value specified
$("#progress").ejProgressBar({ value: 70 });
</script>{% endhighlight %}







### width<span class="type-signature type number/string">Number/String</span>
{:#members:width}








Defines the width of the ProgressBar.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="progress"></div>
<script>
//Initialize the ProgressBar with the width value specified
$("#progress").ejProgressBar({ width: 200,value: 50});
</script>{% endhighlight %}





## Methods








### destroy<span class="signature">()</span>
{:#methods:destroy}








Destroy the progressbar widget





Example
{:.example}


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







### disable<span class="signature">()</span>
{:#methods:disable}








Disables the progressbar control





Example
{:.example}


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







### enable<span class="signature">()</span>
{:#methods:enable}








Enables the progressbar control





Example
{:.example}


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







### getPercent<span class="signature">()</span>
{:#methods:getpercent}








Returns the current progress value in percent.





Example
{:.example}


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







### getValue<span class="signature">()</span>
{:#methods:getvalue}








Returns the current progress value





Example
{:.example}


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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from progressbar
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ProgressBar model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
percentage{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current progress percentage</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current progress value</td>
</tr>
</tbody>
</table>




Example
{:.example}


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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from progressbar
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ProgressBar model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
percentage{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current progress percentage</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current progress value</td>
</tr>
</tbody>
</table>




Example
{:.example}


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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from progressbar
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the progressbar model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from progressbar
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the progressbar model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from progressbar
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ProgressBar model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
percentage{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current progress percentage</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current progress value</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="progress"></div>
<script>
//initial start event
$("#progress").ejProgressBar({
value: 50,
        start: function(args) {}
});
</script>{% endhighlight %}







<a class="" href="http://www.syncfusion.com/copyright" target="_blank">Copyright &copy; 2001 - 2015 Syncfusion Inc. All Rights Reserved</a>





<script type="text/javascript">
prettyPrint();
</script><script src="scripts/linenumber.js" type="text/javascript">
</script><script src="scripts/main.js" type="text/javascript">
</script>
