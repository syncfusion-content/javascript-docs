---
layout: post
title: ejmRating
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html rating control.





$(element).ejmRating<span class="signature">()</span>






Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="rating" &gt;&lt;/div&gt;
&lt;script&gt; // Create rating control $("#rating").ejmRating(); &lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="rating" data-role="ejmrating" &gt;&lt;/div&gt;
</code></pre>



Requires
{:.require}


* module:jQuery

* module:ej.mobile.application

* module:ej.core

* module:ej.unobtrusive

* module:ej.mobile.core

* module:ej.data

* module:ej.touch


## Members




### enabled<span class="type-signature type bool">bool</span>




Specifies whether to enable or disable the control.


Default Value:
{:.param}



* true




Example
{:.example}
<pre class="prettyprint"><code> //Set the enabled property in unobtrusive way.&lt;div id="rating" data-role="ejmrating" data-ej-enabled=true &gt;&lt;/div&gt;
</code></pre><pre class="prettyprint"><code> // Set enabled on initialization. &lt;div id="rating"&gt;&lt;/div&gt;&lt;script&gt;//To set enabled API value $("#rating").ejmRating ({ enabled: true });                     &lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;script&gt;//Get or set the rating enabled, after initialization:
// Get the enabled API value.            $("#rating").ejmRating ("option", "enabled");                  // Set the enabled API$("#rating").ejmRating ("option", "enabled", true); &lt;/script&gt;</code></pre>



### enablePersistence<span class="type-signature type bool">bool</span>




Specifies to maintain the current model value to browser cookies for state maintenance. While refresh the page, the model value will get apply to the control from browser cookies.


Default Value:
{:.param}



* false




Example
{:.example}
<pre class="prettyprint"><code> //Set the enablePersistence property in unobtrusive way.&lt;div id="rating" data-role="ejmrating" data-ej-enablePersistence=false &gt;&lt;/div&gt;
</code></pre><pre class="prettyprint"><code> // Set enablePersistence on initialization. &lt;div id="rating"&gt;&lt;/div&gt;&lt;script&gt;//To set enablePersistence API value $(function(){$("#rating").ejmRating({enablePersistence:false});});&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;script&gt;//Get or set the rating enablePersistence, after initialization:
// Get the enablePersistence API value.          $("#rating").ejmRating ("option", "enablePersistence");                        // Set the enablePersistence API$("#rating").ejmRating ("option", "enablePersistence", false);   &lt;/script&gt;</code></pre>



### incrementStep<span class="type-signature type int">int</span>




Specifies the step value for incrementation.


Default Value:
{:.param}



* 1




Example
{:.example}
<pre class="prettyprint"><code> //Set the incrementStep property in unobtrusive way.&lt;div id="rating" data-role="ejmrating" data-ej-incrementstep=1 &gt;&lt;/div&gt;
</code></pre><pre class="prettyprint"><code> // Set incrementStep on initialization. &lt;div id="rating"&gt;&lt;/div&gt;&lt;script&gt;//To set incrementStep API value$("#rating").ejmRating ({ incrementStep: 1 });  &lt;/script&gt;                         </code></pre><pre class="prettyprint"><code> &lt;script&gt;//Get or set the rating incrementStep, after initialization:
// Get the incrementStep API value.              $("#rating").ejmRating ("option", "incrementStep");                    // Set the incrementStep API$("#rating").ejmRating ("option", "incrementStep", 1);      &lt;/script&gt;</code></pre>



### maxValue<span class="type-signature type int">int</span>




Specifies the maximum value.


Default Value:
{:.param}



* 5




Example
{:.example}
<pre class="prettyprint"><code> //Set the maxValue property in unobtrusive way.&lt;div id="rating" data-role="ejmrating" data-ej-maxvalue=5 &gt;&lt;/div&gt;
</code></pre><pre class="prettyprint"><code> // Set rating maxValue on initialization. &lt;div id="rating"&gt;&lt;/div&gt;&lt;script&gt;//To set maximum API value$("#rating").ejmRating ({ maxValue: 5 });       &lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;script&gt;//Get or set the rating maxValue, after initialization:
// Get the maximum API value.            $("#rating").ejmRating ("option", "maxValue");                 // Set the maximum value API$("#rating").ejmRating ("option", "maxValue", 5);    &lt;/script&gt;</code></pre>



### minValue<span class="type-signature type int">int</span>




Specifies the minimum value.


Default Value:
{:.param}



* 0




Example
{:.example}
<pre class="prettyprint"><code> //Set the minValue property in unobtrusive way.&lt;div id="rating" data-role="ejmrating" data-ej-minvalue=0 &gt;&lt;/div&gt;
</code></pre><pre class="prettyprint"><code> // Set rating minValue on initialization. &lt;div id="rating"&gt;&lt;/div&gt;&lt;script&gt;//To set minimum API value $("#rating").ejmRating ({ minValue: 0 });               &lt;/script&gt;                 </code></pre><pre class="prettyprint"><code> &lt;script&gt;//Get or set the rating minValue, after initialization:
// Get the minimum API value.            $("#rating").ejmRating ("option", "minValue");                 // Set the minValue API$("#rating").ejmRating ("option", "minValue", 0);   &lt;/script&gt;</code></pre>



### orientation<span class="type-signature type enum">enum</span>




Specifies whether the orientation is horizontal or vertical. See <a href="global.html#Orientation">Orientation</a>


Default Value:
{:.param}



* ej.mobile.Rating.Orientation.Horizontal.




Example
{:.example}
<pre class="prettyprint"><code> //Set the orientation property in unobtrusive way.&lt;div id="rating" data-role="ejmrating" data-ej-orientation="horizontal" &gt;&lt;/div&gt;
</code></pre><pre class="prettyprint"><code> // Set orientation on initialization. &lt;div id="rating"&gt;&lt;/div&gt;&lt;script&gt;//To set orientation API value $(function(){$("#rating").ejmRating ({ orientation: ej.mobile.Rating.Orientation.Horizontal });});&lt;/script&gt;                 </code></pre><pre class="prettyprint"><code> &lt;script&gt;//Get or set the rating orientation, after initialization:
// Get the orientation API value.                $("#rating").ejmRating ("option", "orientation");                      // Set the orientation API$("#rating").ejmRating ("option", "orientation", ej.mobile.Rating.Orientation.Horizontal);     &lt;/script&gt;</code></pre>



### precision<span class="type-signature type enum">enum</span>




Specifies the precision value. See <a href="global.html#Precision">Precision</a>


Default Value:
{:.param}



* ej.mobile.Rating.Precision.Full.




Example
{:.example}
<pre class="prettyprint"><code> //Set the precision property in unobtrusive way.&lt;div id="rating" data-role="ejmrating" data-ej-precision="full" &gt;&lt;/div&gt;
</code></pre><pre class="prettyprint"><code> // Set precision on initialization. //To set precision API value &lt;div id="rating"&gt;&lt;/div&gt;&lt;script&gt;$(function(){$("#rating").ejmRating ({ precision: ej.mobile.Rating.Precision.Full });                });&lt;/script&gt;                 </code></pre><pre class="prettyprint"><code> &lt;script&gt;//Get or set the rating precision, after initialization:
// Get the precision API value.          $("#rating").ejmRating ("option", "precision");                        // Set the precision API$("#rating").ejmRating ("option", "precision", ej.mobile.Rating.Precision.Full);  &lt;/script&gt;</code></pre>



### readOnly<span class="type-signature type bool">bool</span>




Specifies whether the control is read only.


Default Value:
{:.param}



* false




Example
{:.example}
<pre class="prettyprint"><code> //Set the read only property in unobtrusive way.&lt;div id="rating" data-role="ejmrating" data-ej-readonly=false &gt;&lt;/div&gt;
</code></pre><pre class="prettyprint"><code> // Set read only on initialization. &lt;div id="rating"&gt;&lt;/div&gt;&lt;script&gt;//To set read only API value $("#rating").ejmRating ({ readOnly: false });                   &lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;script&gt;//Get or set the rating read only, after initialization:
// Get the read only API value.          $("#rating").ejmRating ("option", "readOnly");                 // Set the read only API$("#rating").ejmRating ("option", "readOnly", false);      &lt;/script&gt;</code></pre>



### renderMode<span class="type-signature type enum">enum</span>




Specifies the rendering mode of the control. See <a href="global.html#RenderMode">RenderMode</a>


Default Value:
{:.param}



* auto




Example
{:.example}
<pre class="prettyprint"><code> //Set the renderMode property in unobtrusive way.&lt;div id="rating" data-role="ejmrating" data-ej-rendermode="auto" &gt;&lt;/div&gt;
</code></pre><pre class="prettyprint"><code> // Set rendermode on initialization. &lt;div id="rating"&gt;&lt;/div&gt;&lt;script&gt;//To set renderMode API value $(function(){$("#rating").ejmRating ({ renderMode: ej.mobile.RenderMode.Auto });     });&lt;/script&gt;                 </code></pre><pre class="prettyprint"><code> &lt;script&gt;//Get or set the rating rendermode, after initialization:
// Get the renderMode API value.                 $("#rating").ejmRating ("option", "renderMode");                       // Set the renderMode API$("#rating").ejmRating ("option", "renderMode", ej.mobile.RenderMode.Auto);   &lt;/script&gt;</code></pre>



### shape<span class="type-signature type enum">enum</span>




Specifies the shape. See <a href="global.html#Shape">Shape</a>


Default Value:
{:.param}



* ej.mobile.Rating.Shape.Star.




Example
{:.example}
<pre class="prettyprint"><code> //Set the shape property in unobtrusive way.&lt;div id="rating" data-role="ejmrating" data-ej-shape="star" &gt;&lt;/div&gt;
</code></pre><pre class="prettyprint"><code> // Set shape on initialization. &lt;div id="rating"&gt;&lt;/div&gt;&lt;script&gt;//To set shape API value $(function(){$("#rating").ejmRating ({ shape: ej.mobile.Rating.Shape.Star });});&lt;/script&gt;                 </code></pre><pre class="prettyprint"><code> &lt;script&gt;//Get or set the rating shape, after initialization:
// Get the shape API value.              $("#rating").ejmRating ("option", "shape");                    // Set the shape API$("#rating").ejmRating ("option", "shape", ej.mobile.Rating.Shape.Star);          &lt;/script&gt;</code></pre>



### shapeHeight<span class="type-signature type int">int</span>




Specifies the shape height.


Default Value:
{:.param}



* 25




Example
{:.example}
<pre class="prettyprint"><code> //Set the shape height property in unobtrusive way.&lt;div id="rating" data-role="ejmrating" data-ej-shapeheight=25 &gt;&lt;/div&gt;
</code></pre><pre class="prettyprint"><code> // Set shape height on initialization. &lt;div id="rating"&gt;&lt;/div&gt;&lt;script&gt;//To set shape height API value $("#rating").ejmRating ({ shapeHeight: 25 });   &lt;/script&gt;                 </code></pre><pre class="prettyprint"><code> &lt;script&gt;//Get or set the rating shape height, after initialization:
// Get the shape height API value.               $("#rating").ejmRating ("option", "shapeHeight");                      // Set the shape height API$("#rating").ejmRating ("option", "shapeHeight", 25);  &lt;/script&gt;</code></pre>



### shapeWidth<span class="type-signature type int">int</span>




Specifies the shape width.


Default Value:
{:.param}



* 25




Example
{:.example}
<pre class="prettyprint"><code> //Set the shape width property in unobtrusive way.&lt;div id="rating" data-role="ejmrating" data-ej-shapewidth=25 &gt;&lt;/div&gt;
</code></pre><pre class="prettyprint"><code> // Set shape width on initialization. &lt;div id="rating"&gt;&lt;/div&gt;&lt;script&gt;//To set shape width API value $("#rating").ejmRating ({ shapeWidth: 25 });    &lt;/script&gt;                 </code></pre><pre class="prettyprint"><code> &lt;script&gt;//Get or set the rating shape width, after initialization:
// Get the shape width API value.                $("#rating").ejmRating ("option", "shapeWidth");                       // Set the shape width API$("#rating").ejmRating ("option", "shapeWidth", 25);       &lt;/script&gt;</code></pre>



### spaceBetweenShapes<span class="type-signature type int">int</span>




Specifies the space between shapes.


Default Value:
{:.param}



* 25




Example
{:.example}
<pre class="prettyprint"><code> //Set the space between shapes property in unobtrusive way.&lt;div id="rating" data-role="ejmrating" data-ej-spacebetweenshapes=15 &gt;&lt;/div&gt;
</code></pre><pre class="prettyprint"><code> // Set space between shapes on initialization. &lt;div id="rating"&gt;&lt;/div&gt;&lt;script&gt;//To set space between shapes API value $("#rating").ejmRating ({ spaceBetweenShapes: 15 });            &lt;/script&gt;                 </code></pre><pre class="prettyprint"><code> &lt;script&gt;//Get or set the rating space between shapes, after initialization:
// Get the space between shapes API value.               $("#rating").ejmRating ("option", "spaceBetweenShapes");                       // Set the space between shapes API$("#rating").ejmRating ("option", "spaceBetweenShapes", 15);            &lt;/script&gt;</code></pre>



### theme<span class="type-signature type enum">enum</span>




Specifies the theme. See <a href="global.html#Theme">Theme</a>


Default Value:
{:.param}



* auto




Example
{:.example}
<pre class="prettyprint"><code> //Set the theme property in unobtrusive way.&lt;div id="rating" data-role="ejmrating" data-ej-theme="auto" &gt;&lt;/div&gt;
</code></pre><pre class="prettyprint"><code> // Set theme on initialization. &lt;div id="rating"&gt;&lt;/div&gt;&lt;script&gt;//To set theme API value $(function(){$("#rating").ejmRating ({ theme: ej.mobile.Theme.Auto });               });&lt;/script&gt;                 </code></pre><pre class="prettyprint"><code> &lt;script&gt;//Get or set the rating theme, after initialization:
// Get the theme API value.              $("#rating").ejmRating ("option", "theme");                    // Set the theme API$("#rating").ejmRating ("option", "theme", ej.mobile.Theme.Auto);            &lt;/script&gt;</code></pre>



### value<span class="type-signature type int">int</span>




Specifies the current value.


Default Value:
{:.param}



* 1




Example
{:.example}
<pre class="prettyprint"><code> //Set the current value property in unobtrusive way.&lt;div id="rating" data-role="ejmrating" data-ej-value=1 &gt;&lt;/div&gt;
</code></pre><pre class="prettyprint"><code> // Set rating current value on initialization. &lt;div id="rating"&gt;&lt;/div&gt;&lt;script&gt;//To set current value API value $("#rating").ejmRating ({ value: 1 });          &lt;/script&gt;                         </code></pre><pre class="prettyprint"><code> &lt;script&gt;//Get or set the rating current value, after initialization:
// Get the current value API value.              $("#rating").ejmRating ("option", "value");                    // Set the current value API$("#rating").ejmRating ("option", "value", 1);   &lt;/script&gt;</code></pre>


## Methods




### disable<span class="signature">()</span>




To disable the rating.



Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="rating" data-role="ejmrating" &gt;&lt;/div&gt;
&lt;script&gt;$(function(){// To get the instance of the rating controlvar rating = $("#rating").data("ejmRating");rating.disable(); // it will disable the rating control});&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="rating" &gt;&lt;/div&gt;
&lt;script&gt;$("#rating").ejmRating();       $(function(){// To disable the Rating control$("#rating").ejmRating("disable");});   &lt;/script&gt;</code></pre>



### enable<span class="signature">()</span>




To enable the rating.



Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="rating" data-role="ejmrating" &gt;&lt;/div&gt;
&lt;script&gt;$(function(){// To get the instance of the rating controlvar rating = $("#rating").data("ejmRating");rating.enable(); // it will enable the rating control});&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="rating" &gt;&lt;/div&gt;
&lt;script&gt;$("#rating").ejmRating();       $(function(){// To enable the Rating control$("#rating").ejmRating("enable");});   &lt;/script&gt;</code></pre>



### getValue<span class="signature">()</span>




To get the current value.



Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="rating" data-role="ejmrating"&gt;&lt;/div&gt;
&lt;script&gt;$(function(){// To get the instance of rating controlvar rating = $("#rating").data("ejmRating");rating.getValue(); // it will return the current value of rating});&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="rating"&gt;&lt;/div&gt;
&lt;script&gt;// To get the current value of Rating control$("#rating").ejmRating("getValue");     &lt;/script&gt;</code></pre>



### hide<span class="signature">()</span>




To hide the rating.



Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="rating" data-role="ejmrating" &gt;&lt;/div&gt;
&lt;script&gt;$(function(){// To get the instance of the rating controlvar rating = $("#rating").data("ejmRating");rating.hide(); // it will hide the rating control});&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="rating" &gt;&lt;/div&gt;
&lt;script&gt;$("#rating").ejmRating();       $(function(){// To hide the Rating control$("#rating").ejmRating("hide"); });&lt;/script&gt;</code></pre>



### reset<span class="signature">()</span>




To reset the value.



Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="rating" data-role="ejmrating"&gt;&lt;/div&gt;
&lt;script&gt;$(function(){// To get the instance of rating controlvar rating = $("#rating").data("ejmRating");rating.reset(); // it will reset the value of rating});&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="rating"&gt;&lt;/div&gt;
&lt;script&gt;// To reset value of Rating control$("#rating").ejmRating("reset");        &lt;/script&gt;</code></pre>



### setValue<span class="signature">()</span>




To set the value.



Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="rating" data-role="ejmrating"&gt;&lt;/div&gt;
&lt;script&gt;$(function(){// To get the instance of rating controlvar rating = $("#rating").data("ejmRating");rating.setValue(3); // it will set the value of rating});&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="rating"&gt;&lt;/div&gt;
&lt;script&gt;// To set the value of Rating control$("#rating").ejmRating("setValue",3);   &lt;/script&gt;</code></pre>



### show<span class="signature">()</span>




To show the rating.



Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="rating" data-role="ejmrating" &gt;&lt;/div&gt;
&lt;script&gt;$(function(){// To get the instance of the rating controlvar rating = $("#rating").data("ejmRating");rating.show(); // it will show the rating control});&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="rating" &gt;&lt;/div&gt;
&lt;script&gt;$("#rating").ejmRating();       $(function(){// To show the Rating control$("#rating").ejmRating("show");});   &lt;/script&gt;</code></pre>


## Events




### change




Event triggers when the value changed.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from rating.<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">returns true if the event should be cancelled; otherwise, false.</td></tr><tr><td class="name"><code>type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event.</td></tr><tr><td class="name"><code>model</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">returns the model value of the control.</td></tr><tr><td class="name"><code>value</code></td><td class="type"><span class="param-type">int</span></td><td class="description last">returns the current element associated value.</td></tr></tbody></table></td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="rating" data-role="ejmrating" data-ej-change="onChange"&gt;&lt;/div&gt;
&lt;script&gt; // change event for Rating  function onChange(args){ //handle the event}&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="rating"&gt;&lt;/div&gt;&lt;script&gt;//change event for Rating$("#rating").ejmRating({  change: function (args) { //handle the event }});           &lt;/script&gt;</code></pre>



### tap




Event triggers when touch happens on the control.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from rating.<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">returns true if the event should be cancelled; otherwise, false.</td></tr><tr><td class="name"><code>type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event.</td></tr><tr><td class="name"><code>model</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">returns the model value of the control.</td></tr><tr><td class="name"><code>value</code></td><td class="type"><span class="param-type">int</span></td><td class="description last">returns the current element associated value.</td></tr></tbody></table></td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="rating" data-role="ejmrating" data-ej-tap="onTap"&gt;&lt;/div&gt;
&lt;script&gt; // Change event for Rating  function onTap(args){ //handle the event}&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="rating"&gt;&lt;/div&gt;&lt;script&gt; //Change event for Rating$("#rating").ejmRating({ tap: function (args) { //handle the event }});     &lt;/script&gt;                 </code></pre>



### touchMove




Event triggers when touch move happens on the control.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from rating.<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">returns true if the event should be cancelled; otherwise, false.</td></tr><tr><td class="name"><code>type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event.</td></tr><tr><td class="name"><code>model</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">returns the model value of the control.</td></tr><tr><td class="name"><code>value</code></td><td class="type"><span class="param-type">int</span></td><td class="description last">returns the current element associated value.</td></tr></tbody></table></td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="rating" data-role="ejmrating" data-ej-touchmove="ontouchMove"&gt;&lt;/div&gt;
&lt;script&gt; // Change event for Rating  function ontouchMove(args){ //handle the event}&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="rating"&gt;&lt;/div&gt;&lt;script&gt;//change event for Rating$("#rating").ejmRating({  touchMove: function (args) { //handle the event }});           &lt;/script&gt;</code></pre>


