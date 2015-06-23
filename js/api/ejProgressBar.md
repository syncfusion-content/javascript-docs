---
layout: post
title: ejProgressBar
documentation: API
platform: js
metaname: 
metacontent: 
---

Custom Design for Progressbar control.










#### $(element).ejProgressBar<span class="signature">()</span>











##### Example

<pre class="prettyprint">
<code>&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt;
$("#progress").ejProgressBar({value: 50});
&lt;/script&gt;</code>
</pre>






### Requires




* module:jQuery


* module:jquery.easing.1.3.js


* module:ej.core.js


* module:ej.progressbar.js




### Members








#### cssClass<span class="type-signature type string">String</span>








Sets the root class for ProgressBar theme. This cssClass API helps to use custom skinning option for ProgressBar control. By defining the root class using this API, we need to include this root class in CSS.




Default Value:
{:.param}






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt;
//Initialize the ProgressBar with the cssClass value specified
$("#progress").ejProgressBar({ cssClass: 'gradient-lime ',value: 50  });
&lt;/script&gt;</code>
</pre>






#### enabled<span class="type-signature type boolean">boolean</span>








When this property sets to false, it disables the ProgressBar control




Default Value:
{:.param}






* true








##### Example

<pre class="prettyprint">
<code>&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt;
//Initialize the ProgressBar with the enabled value specified
$("#progress").ejProgressBar({ enabled: true,value: 50 });
&lt;/script&gt;</code>
</pre>






#### enablePersistence<span class="type-signature type boolean">boolean</span>








Save current model value to browser cookies for state maintains. While refresh the progressBar control page retains the model value apply from browser cookies




Default Value:
{:.param}






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt;
//Initialize the Progress bar with the persist value specified
$("#progress").ejProgressBar({ enablePersistence: true,value: 50 });
&lt;/script&gt;</code>
</pre>






#### enableRTL<span class="type-signature type boolean">boolean</span>








Sets the ProgressBar direction as right to left alignment.




Default Value:
{:.param}






* false








##### Example

<pre class="prettyprint">
<code>&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt;
//Initialize the Progress bar with the rtl value specified
$("#progress").ejProgressBar({ enableRTL: true,value: 50 });
&lt;/script&gt;</code>
</pre>






#### height<span class="type-signature type number/string">Number/String</span>








Defines the height of the ProgressBar.




Default Value:
{:.param}






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt;
//Initialize the ProgressBar with the height value specified
$("#progress").ejProgressBar({ height: 20,value: 50 });
&lt;/script&gt;</code>
</pre>






#### maxValue<span class="type-signature type number">Number</span>








Sets the maximum value of the ProgressBar.




Default Value:
{:.param}






* 100








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt;
//Initialize the ProgressBar with the max value specified
$("#progress").ejProgressBar({ maxValue: 200 ,value: 200 });
&lt;/script&gt;</code>
</pre>






#### minValue<span class="type-signature type number">Number</span>








Sets the minimum value of the ProgressBar.




Default Value:
{:.param}






* 0








##### Example

<pre class="prettyprint">
<code>&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt;
//Initialize the ProgressBar with the min value specified
$("#progress").ejProgressBar({ minValue: 50,value: 50});
&lt;/script&gt;</code>
</pre>






#### percentage<span class="type-signature type number">Number</span>








Sets the ProgressBar value in percentage. The value should be in between 0 to 100.




Default Value:
{:.param}






* 0








##### Example

<pre class="prettyprint">
<code>&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt;
//Initialize the ProgressBar with the progress value specified in percent
$("#progress").ejProgressBar({ percentage : 35 });
&lt;/script&gt;</code>
</pre>






#### text<span class="type-signature type string">String</span>








Sets the custom text for the ProgressBar. The text placed in the middle of the ProgressBar and it can be customizable using the class 'e-progress-text'.




Default Value:
{:.param}






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt; 
//To set the text API value during initialization  
$("#progress").ejProgressBar({ text: 'loading...',value: 50 });
&lt;/script&gt;</code>
</pre>






#### value<span class="type-signature type number">Number</span>








Sets the ProgressBar value. The value should be in between min and max values.




Default Value:
{:.param}






* 0








##### Example

<pre class="prettyprint">
<code>&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt;
//Initialize the ProgressBar with the progress value specified
$("#progress").ejProgressBar({ value: 70 });
&lt;/script&gt;</code>
</pre>






#### width<span class="type-signature type number/string">Number/String</span>








Defines the width of the ProgressBar.




Default Value:
{:.param}






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt;
//Initialize the ProgressBar with the width value specified
$("#progress").ejProgressBar({ width: 200,value: 50});
&lt;/script&gt;</code>
</pre>




### Methods








#### destroy<span class="signature">()</span>








Destroy the progressbar widget





##### Examples

<pre class="prettyprint">
<code>&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt;
$("#progress").ejProgressBar({value: 50});
// Create Progressbar instance
var proObj = $("#progress").data("ejProgressBar");
proObj.destroy(); //destroy the Progressbar control
&lt;/script&gt;
        </code>
</pre>
<pre class="prettyprint">
<code>&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt;
$("#progress").ejProgressBar({value: 50});
        // To destroy the Progressbar control
$("#progress").ejProgressBar("destroy");
&lt;/script&gt;</code>
</pre>






#### disable<span class="signature">()</span>








Disables the progressbar control





##### Examples

<pre class="prettyprint">
<code>&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt;
$("#progress").ejProgressBar({value: 50});
// Create Progressbar instance
var proObj = $("#progress").data("ejProgressBar");
proObj.disable(); //disables the Progressbar control
&lt;/script&gt;
        </code>
</pre>
<pre class="prettyprint">
<code>&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt;
$("#progress").ejProgressBar({value: 50});
        //To disables the Progressbar control
$("#progress").ejProgressBar("disable");
&lt;/script&gt;</code>
</pre>






#### enable<span class="signature">()</span>








Enables the progressbar control





##### Examples

<pre class="prettyprint">
<code>&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt;
$("#progress").ejProgressBar({value: 50});
// Create Progressbar instance
var proObj = $("#progress").data("ejProgressBar");
proObj.enable(); // enables the Progressbar control
&lt;/script&gt;
        </code>
</pre>
<pre class="prettyprint">
<code>&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt;
$("#progress").ejProgressBar({value: 50});
        // To enables the Progressbar control
$("#progress").ejProgressBar("enable");
&lt;/script&gt;</code>
</pre>






#### getPercent<span class="signature">()</span>








Returns the current progress value in percent.





##### Examples

<pre class="prettyprint">
<code>&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt;
$("#progress").ejProgressBar({value: 50});
// Create Progressbar instance
var proObj = $("#progress").data("ejProgressBar");
proObj.getPercentage(); // get the percent of Progressbar control
&lt;/script&gt;
        </code>
</pre>
<pre class="prettyprint">
<code>&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt;
$("#progress").ejProgressBar({value: 50});
        // To get the percent of Progressbar control
$("#progress").ejProgressBar("getPercentage");
&lt;/script&gt;</code>
</pre>






#### getValue<span class="signature">()</span>








Returns the current progress value





##### Examples

<pre class="prettyprint">
<code>&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt;
$("#progress").ejProgressBar({value: 50});
// Create Progressbar instance
var proObj = $("#progress").data("ejProgressBar");
proObj.getValue(); // get the value of Progressbar control
&lt;/script&gt;
        </code>
</pre>
<pre class="prettyprint">
<code>&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt;
$("#progress").ejProgressBar({value: 50});
        // To get the value of Progressbar control 
$("#progress").ejProgressBar("getValue");
&lt;/script&gt;</code>
</pre>




### Events








#### change








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ProgressBar model</td>
</tr>
<tr>
<td class="name"><code>percentage</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current progress percentage</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current progress value</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code>&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt;
//initial complete event
$("#progress").ejProgressBar({
        value: 50,
        change: function(args) {}
});
&lt;/script&gt;</code>
</pre>






#### complete








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ProgressBar model</td>
</tr>
<tr>
<td class="name"><code>percentage</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current progress percentage</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current progress value</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code>&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt;
//initial complete event
$("#progress").ejProgressBar({
        value: 50,
        complete: function(args) {}
});
&lt;/script&gt;</code>
</pre>






#### create








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the progressbar model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="progress"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//create event for progressbar
$("#progress").ejProgressBar({
        value: 50,
        create: function(args) {}
});
&lt;/script&gt;</code>
</pre>






#### destroy








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the progressbar model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="progress"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//destroy event for progressbar
$("#progress").ejProgressBar({
        value: 50,
        destroy: function(args) {}
});
&lt;/script&gt;</code>
</pre>






#### start








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ProgressBar model</td>
</tr>
<tr>
<td class="name"><code>percentage</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current progress percentage</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current progress value</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code>&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt;
//initial start event
$("#progress").ejProgressBar({
value: 50,
        start: function(args) {}
});
&lt;/script&gt;</code>
</pre>






<a class="" href="http://www.syncfusion.com/copyright" target="_blank">Copyright &copy; 2001 - 2015 Syncfusion Inc. All Rights Reserved</a>





<script type="text/javascript">
prettyPrint();
</script><script src="scripts/linenumber.js" type="text/javascript">
</script><script src="scripts/main.js" type="text/javascript">
</script>
