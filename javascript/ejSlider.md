---
layout: post
title: ejSlider
metaname: 
metacontent: 
---

Custom Design for Html Slider control.










#### $(element).ejSlider<span class="signature">()</span>











##### Example

<pre class="prettyprint">
<code> 
&lt;div id="slider"&gt; &lt;/div&gt; 
 
&lt;script&gt; 
// Create Slider 
$('#slider').ejSlider(); 
&lt;/script&gt; 
</code>
</pre>






### Requires




* module:jQuery


* module:jquery.easing.1.3.js


* module:ej.core.js


* module:ej.slider.js




### Members








#### animationSpeed<span class="type-signature type number">number</span>








Specifies the animationSpeed of the slider.




Default Value:






* 500








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="slider"&gt; &lt;/div&gt; 
&lt;script&gt;
//To set animationSpeed API value during initialization  
$("#slider").ejSlider({ animationSpeed: 500});
&lt;/script&gt;</code>
</pre>






#### cssClass<span class="type-signature type string">string</span>








Specify the CSS class to slider to achieve custom theme.




Default Value:






* ""








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="slider"&gt; &lt;/div&gt; 
&lt;script&gt;
//To set cssClass API value during initialization  
        $("#slider").ejSlider({ cssClass: "gradient-lime"});
&lt;/script&gt;</code>
</pre>






#### enableAnimation<span class="type-signature type boolean">boolean</span>








Specifies the animation behaviour of the slider.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="slider"&gt; &lt;/div&gt; 
&lt;script&gt;
//To set enableAnimation API value during initialization  
        $("#slider").ejSlider({ enableAnimation: false});
&lt;/script&gt;</code>
</pre>






#### enabled<span class="type-signature type boolean">boolean</span>








Specifies the state of the slider.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code>&lt;div id="slider"&gt; &lt;/div&gt; 
&lt;script&gt;
//To set enabled API value during initialization  
        $("#slider").ejSlider({ enabled: false});
&lt;/script&gt;</code>
</pre>






#### enablePersistence<span class="type-signature type boolean">boolean</span>








Specify the enablePersistence to slider to save current model value to browser cookies for state maintains




Default Value:






* false








##### Example

<pre class="prettyprint">
<code>&lt;div id="slider"&gt; &lt;/div&gt; 
&lt;script&gt;
//To set enablePersistence API value during initialization  
        $("#slider").ejSlider({ enablePersistence: false});
&lt;/script&gt;</code>
</pre>






#### enableRTL<span class="type-signature type boolean">boolean</span>








Specifies the Right to Left Direction of the slider.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;/br&gt;
&lt;/br&gt;
&lt;div id="slider"&gt; &lt;/div&gt; 
&lt;script&gt;
//To set enableRTL API value during initialization  
        $("#slider").ejSlider({ enableRTL: false});
&lt;/script&gt;</code>
</pre>






#### height<span class="type-signature type string">String</span>








Specifies the height of the slider.




Default Value:






* 14








##### Example

<pre class="prettyprint">
<code>&lt;div id="slider"&gt; &lt;/div&gt; 
&lt;script&gt;
//To set height API value during initialization  
        $("#slider").ejSlider({ height: 14});
&lt;/script&gt;</code>
</pre>






#### incrementStep<span class="type-signature type number">number</span>








Specifies the incremental step value of the slider.




Default Value:






* 1








##### Example

<pre class="prettyprint">
<code>&lt;/br&gt;
&lt;/br&gt;
&lt;div id="slider"&gt; &lt;/div&gt; 
&lt;script&gt;
//To set incrementStep API value during initialization  
        $("#slider").ejSlider({ incrementStep: 2});
&lt;/script&gt;</code>
</pre>






#### largeStep<span class="type-signature type number">number</span>








Specifies the distance between two major (large) ticks from the scale of the slider.




Default Value:






* 10








##### Example

<pre class="prettyprint">
<code>&lt;/br&gt;
&lt;/br&gt;
&lt;div id="slider"&gt; &lt;/div&gt; 
&lt;script&gt;
//To set largeStep API value during initialization  
        $("#slider").ejSlider({ largeStep: 2});
&lt;/script&gt;</code>
</pre>






#### maxValue<span class="type-signature type number">number</span>








Specifies the ending value of the slider.




Default Value:






* 100








##### Example

<pre class="prettyprint">
<code>&lt;/br&gt;
&lt;/br&gt;
&lt;div id="slider"&gt; &lt;/div&gt; 
&lt;script&gt;
//To set maxValue API value during initialization  
        $("#slider").ejSlider({ maxValue: 60});
&lt;/script&gt;</code>
</pre>






#### minValue<span class="type-signature type number">number</span>








Specifies the starting value of the slider.




Default Value:






* 0








##### Example

<pre class="prettyprint">
<code> 
&lt;/br&gt;
&lt;/br&gt;
&lt;div id="slider"&gt; &lt;/div&gt; 
&lt;script&gt;
//To set minValue API value during initialization  
        $("#slider").ejSlider({ minValue: 0});
&lt;/script&gt;</code>
</pre>






#### orientation<span class="type-signature type enum">enum</span>








Specifies the orientation of the slider.See orientation




Default Value:






* ej.orientation.Horizontal








##### Example

<pre class="prettyprint">
<code>&lt;div id="slider"&gt; &lt;/div&gt; 
&lt;script&gt;
//To set orientation API value during initialization
$("#slider").ejSlider({ orientation: ej.Orientation.Vertical});
&lt;/script&gt;</code>
</pre>






#### readOnly<span class="type-signature type boolean">boolean</span>








Specifies the readOnly of the slider.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code>&lt;div id="slider"&gt; &lt;/div&gt; 
&lt;script&gt;
//To set readOnly API value during initialization  
        $("#slider").ejSlider({ readOnly: true});
&lt;/script&gt;</code>
</pre>






#### showRoundedCorner<span class="type-signature type boolean">boolean</span>








Specifies the rounded corner behaviour for slider.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code>&lt;div id="slider"&gt; &lt;/div&gt; 
&lt;script&gt;
//To set showRoundedCorner API value during initialization  
        $("#slider").ejSlider({ showRoundedCorner: true});
&lt;/script&gt;</code>
</pre>






#### showScale<span class="type-signature type boolean">boolean</span>








Specifies the major (large) and minor (small) ticks of the slider.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code>&lt;/br&gt;
&lt;/br&gt;
&lt;div id="slider"&gt; &lt;/div&gt; 
&lt;script&gt;
//To set enabled API value during initialization
        $("#slider").ejSlider({ showScale: false});
&lt;/script&gt;</code>
</pre>






#### showSmallTicks<span class="type-signature type boolean">boolean</span>








Specifies the showSmallTicks of the slider.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code>&lt;/br&gt;
&lt;/br&gt;
&lt;div id="slider"&gt; &lt;/div&gt; 
&lt;script&gt;
//To set showSmallTicks API value during initialization  
        $("#slider").ejSlider({ showSmallTicks: false});
&lt;/script&gt; </code>
</pre>






#### showTooltip<span class="type-signature type boolean">boolean</span>








Specifies the showTooltip to shows the current Slider value, while moving the Slider handle of the slider.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;/br&gt;
&lt;/br&gt;
&lt;div id="slider"&gt; &lt;/div&gt; 
&lt;script&gt;
//To set showTooltip API value during initialization  
        $("#slider").ejSlider({ showTooltip: true});
&lt;/script&gt;</code>
</pre>






#### sliderType<span class="type-signature type enum">enum</span>








Specifies the sliderType of the slider.




Default Value:






* ej.SliderType.Default








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="slider"&gt; &lt;/div&gt; 
&lt;script&gt;
//To set sliderType API value during initialization
$("#slider").ejSlider({ sliderType: ej.SliderType.Default});
&lt;/script&gt;</code>
</pre>






#### smallStep<span class="type-signature type number">number</span>








Specifies the distance between two minor (small) ticks from the scale of the slider.




Default Value:






* 1








##### Example

<pre class="prettyprint">
<code>&lt;/br&gt;
&lt;/br&gt;
&lt;div id="slider"&gt; &lt;/div&gt; 
&lt;script&gt;
//To set smallStep API value during initialization  
        $("#slider").ejSlider({ smallStep: 2});
&lt;/script&gt;</code>
</pre>






#### value<span class="type-signature type number">number</span>








Specifies the value of the slider.




Default Value:






* 0








##### Example

<pre class="prettyprint">
<code>&lt;/br&gt;
&lt;/br&gt;
&lt;div id="slider"&gt; &lt;/div&gt; 
&lt;script&gt;
//To set value API  during initialization
        $("#slider").ejSlider({ value: 60});
&lt;/script&gt;</code>
</pre>






#### values<span class="type-signature type array">array</span>








Specifies the values of the range slider.




Default Value:






* [minValue,maxValue]








##### Example

<pre class="prettyprint">
<code>&lt;/br&gt;
&lt;/br&gt;
&lt;div id="slider"&gt; &lt;/div&gt; 
&lt;script&gt;
//To set values API during initialization
        $("#slider").ejSlider({ values: [30,60]});
&lt;/script&gt;</code>
</pre>






#### width<span class="type-signature type string">String</span>








Specifies the width of the slider.




Default Value:






* 100%








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="slider"&gt; &lt;/div&gt; 
&lt;script&gt;
//To set width API value during initialization
        $("#slider").ejSlider({ width: "300px"});
&lt;/script&gt;</code>
</pre>




### Methods








#### disable<span class="signature">()</span>








To disable the slider





##### Examples

<pre class="prettyprint">
<code> 
&lt;div id="slider"&gt; &lt;/div&gt; 
 
&lt;script&gt;
$("#slider").ejSlider();
// Create slider control
var sliderObj = $("#slider").data("ejSlider");
sliderObj.disable(); // disable the slider control
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="slider"&gt; &lt;/div&gt; 
 
&lt;script&gt;
$("#slider").ejSlider();
// disable the slider control
$("#slider").ejSlider("disable");
&lt;/script&gt;</code>
</pre>






#### enable<span class="signature">()</span>








To enable the slider





##### Examples

<pre class="prettyprint">
<code> 
&lt;div id="slider"&gt; &lt;/div&gt; 
 
&lt;script&gt;
$("#slider").ejSlider();
// Create slider control
var sliderObj = $("#slider").data("ejSlider");
sliderObj.enable(); // enable the slider control
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="slider"&gt; &lt;/div&gt; 
 
&lt;script&gt;
$("#slider").ejSlider();
// enable the slider control
$("#slider").ejSlider("enable");
&lt;/script&gt;</code>
</pre>






#### getValue<span class="signature">()</span>








To get value from slider handle





##### Examples

<pre class="prettyprint">
<code> 
&lt;div id="slider"&gt; &lt;/div&gt; 
&lt;script&gt;
$("#slider").ejSlider();
// Create Editors
var sliderObj = $("#slider").data("ejSlider");
sliderObj.getValue(); // getValue the slider handle
&lt;/script&gt;
                 </code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="slider"&gt; &lt;/div&gt; 
 
&lt;script&gt;
$("#slider").ejSlider();
// get value from slider handle
$("#slider").ejSlider("getValue");
&lt;/script&gt;</code>
</pre>




### Events








#### change








Fires when Slider control value is changed successfully.

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
<td class="description last">Event parameters from slider control
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
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>sliderIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns current handle number or index</td>
</tr>
<tr>
<td class="name"><code>id</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns slider id</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the slider model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the slider value</td>
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
&lt;div id="slider"&gt; &lt;/div&gt; 
&lt;script&gt;
//change event for slider control
$("#slider").ejSlider({
   change: function (args) {}
});
&lt;/script&gt;</code>
</pre>






#### create








Fires when Slider control has been created successfully.

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
<td class="description last">Event parameters from slider control
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
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the slider model</td>
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
&lt;div id="slider"&gt; &lt;/div&gt; 
&lt;script&gt;
//create event for slider control
$("#slider").ejSlider({
   create: function (args) {}
});
&lt;/script&gt;</code>
</pre>






#### destroy








Fires when Slider control has been destroyed successfully.

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
<td class="description last">Event parameters from slider control
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
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the slider model</td>
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
&lt;div id="slider"&gt; &lt;/div&gt; 
&lt;script&gt;
//destroy event for slider control
$("#slider").ejSlider({
   destroy: function (args) {}
});
&lt;/script&gt;</code>
</pre>






#### slide








Fires when Slider control is sliding successfully.

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
<td class="description last">Event parameters from slider control
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
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>sliderIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns current handle number or index</td>
</tr>
<tr>
<td class="name"><code>id</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns slider id</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the slider model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the slider value</td>
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
&lt;div id="slider"&gt; &lt;/div&gt; 
&lt;script&gt;
//slide event for slider control
$("#slider").ejSlider({
   slide: function (args) {}
});
&lt;/script&gt;</code>
</pre>






#### start








Fires when Slider control is started successfully.

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
<td class="description last">Event parameters from slider control
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
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>sliderIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns current handle number or index</td>
</tr>
<tr>
<td class="name"><code>id</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns slider id</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the slider model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the slider value</td>
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
&lt;div id="slider"&gt; &lt;/div&gt; 
&lt;script&gt;
//start event for slider control
$("#slider").ejSlider({
   start: function (args) {}
});
&lt;/script&gt;</code>
</pre>






#### stop








Fires when Slider control is stopped successfully.

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
<td class="description last">Event parameters from slider control
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
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>sliderIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns current handle number or index</td>
</tr>
<tr>
<td class="name"><code>id</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns slider id</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the slider model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the slider value</td>
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
&lt;div id="slider"&gt; &lt;/div&gt; 
&lt;script&gt;
//stop event for slider control
$("#slider").ejSlider({
   stop: function (args) {}
});
&lt;/script&gt;</code>
</pre>



