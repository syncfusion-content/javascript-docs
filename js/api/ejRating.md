---
layout: post
title: ejRating
documentation: API
platform: js
metaname: 
metacontent: 
---


# Class: ejRating

# Custom Design for Html Rating control.





$(element).ejRating<span class="signature">()</span>






Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
// Create Rating
$('#rating').ejRating(); 
&lt;/script&gt;</code>
</pre>



Requires
{:.require}


* module:jQuery

* module:jquery.easing.1.3.js

* module:ej.core.js

* module:ej.rating.js


## Members




### allowReset<span class="type-signature type boolean">boolean</span>
{:#allowreset}
{:#allowReset}




Enables the rating control with reset button.It can be used to reset the rating control value.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
//To set allowReset API value during initialization  
        $("#rating").ejRating({allowReset: true});
&lt;/script&gt;</code>
</pre>



### cssClass<span class="type-signature type string">string</span>
{:#cssclass}
{:#cssClass}




Specify the CSS class to rating to achieve custom theme.


Default Value:
{:.param}



* ""




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
// Set the cssClass during initialization.
        $("#rating").ejRating({  cssClass : "gradient-lime" });
&lt;/script&gt;</code>
</pre>



### enabled<span class="type-signature type boolean">boolean</span>
{:#enabled}
{:#enabled}




When this property is set to false, it disables the rating control.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
//To set enabled API value during initialization  
        $("#rating").ejRating({enabled: true });
&lt;/script&gt;</code>
</pre>



### enablePersistence<span class="type-signature type boolean">boolean</span>
{:#enablepersistence}
{:#enablePersistence}




Save current model value to browser cookies for state maintanence. While refresh the page Rating control values are retained.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
//To set persist API value during initialization  
        $("#rating").ejRating({enablePersistence: true });
&lt;/script&gt;</code>
</pre>



### height<span class="type-signature type string">string</span>
{:#height}
{:#height}




Specifies the height of the Rating control wrapper.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code>&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
//To set height API value during initialization  
        $("#rating").ejRating({height: "50" });
&lt;/script&gt;</code>
</pre>



### incrementStep<span class="type-signature type number">number</span>
{:#incrementstep}
{:#incrementStep}




Specifies the value to be increased while navigating between shapes(stars) in Rating control.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code>&lt;/br&gt;
&lt;/br&gt;
&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
//To set incrementStep API value during initialization  
        $("#rating").ejRating({incrementStep: 2 });
&lt;/script&gt;</code>
</pre>



### maxValue<span class="type-signature type number">number</span>
{:#maxvalue}
{:#maxValue}




Allow to render the maximum number of Rating shape(star).


Default Value:
{:.param}



* 5




Example
{:.example}

<pre class="prettyprint">
<code>&lt;/br&gt;
&lt;/br&gt;
&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
//To set maxValue API value during initialization  
        $("#rating").ejRating({maxValue: 10 });
&lt;/script&gt;</code>
</pre>



### minValue<span class="type-signature type number">number</span>
{:#minvalue}
{:#minValue}




Allow to render the minimum number of Rating shape(star).


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;/br&gt;
&lt;/br&gt;
&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
//To set minValue API value during initialization  
        $("#rating").ejRating({minValue: 3 });
&lt;/script&gt;</code>
</pre>



### orientation<span class="type-signature type enum">enum</span>
{:#orientation}
{:#orientation}




Specifies the orientation of Rating control. See <a href="global.html#Orientation">Orientation</a>


Default Value:
{:.param}



* ej.Rating.Orientation.Horizontal




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
//To set orientation API value during initialization  
        $("#rating").ejRating({orientation: ej.Rating.Orientation.Horizontal });
&lt;/script&gt; </code>
</pre>



### precision<span class="type-signature type enum">enum</span>
{:#precision}
{:#precision}




Helps to provide more precise ratings.Rating control supports three precision modes - full, half, and exact. See <a href="global.html#Precision">Precision</a>


Default Value:
{:.param}



* "full"




Example
{:.example}

<pre class="prettyprint">
<code>&lt;/br&gt;
&lt;/br&gt;
&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
//To set precision API value during initialization  
        $("#rating").ejRating({precision: ej.Rating.Precision.Half});
&lt;/script&gt;</code>
</pre>



### readOnly<span class="type-signature type boolean">boolean</span>
{:#readonly}
{:#readOnly}




Interaction with Rating control can be prevented by enabling this API.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
//To set readOnly API value during initialization  
        $("#rating").ejRating({readOnly: true});
&lt;/script&gt;</code>
</pre>



### shapeHeight<span class="type-signature type number">number</span>
{:#shapeheight}
{:#shapeHeight}




To specify the height of each shape in Rating control.


Default Value:
{:.param}



* 23




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
//To set shapeHeight API value during initialization  
        $("#rating").ejRating({shapeHeight: 25 });
&lt;/script&gt;</code>
</pre>



### shapeWidth<span class="type-signature type number">number</span>
{:#shapewidth}
{:#shapeWidth}




To specify the width of each shape in Rating control.


Default Value:
{:.param}



* 23




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
//To set shapeWidth API value during initialization  
        $("#rating").ejRating({shapeWidth: 25 });
&lt;/script&gt;</code>
</pre>



### showTooltip<span class="type-signature type boolean">boolean</span>
{:#showtooltip}
{:#showTooltip}




Enables the tooltip option.Currently selected value value will be displayed in tooltip.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;/br&gt;
&lt;/br&gt;
&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
//To set showTooltip API value during initialization  
        $("#rating").ejRating({showTooltip: true});
&lt;/script&gt;</code>
</pre>



### value<span class="type-signature type number">number</span>
{:#value}
{:#value}




To specify the number of stars to be selected while rendering.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;/br&gt;
&lt;/br&gt;
&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
//To set value API value during initialization  
        $("#rating").ejRating({value: 3 });
&lt;/script&gt;</code>
</pre>



### width<span class="type-signature type string">string</span>
{:#width}
{:#width}




Specifies the width of the Rating control wrapper.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code>&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
//To set width API value during initialization  
        $("#rating").ejRating({width: "200" });
&lt;/script&gt;</code>
</pre>


## Methods




### destroy<span class="signature">()</span>
{:#destroy}
{:#destroy}




destroy the Rating widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;rating id="rating"&gt;Rating&lt;/rating&gt; 
 
&lt;script&gt;
$("#rating").ejRating();
// Create Rating
var ratingObj = $("#rating").data("ejRating");
ratingObj.destroy(); // destroy the button
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;rating id="rating"&gt;Rating&lt;/rating&gt; 
 
&lt;script&gt;
$("#rating").ejRating();
// destroy the rating
$("#rating").ejRating("destroy");
&lt;/script&gt;</code>
</pre>



### getValue<span class="signature">()</span>
{:#getvalue}
{:#getValue}




To get the current value of rating control



#### Returns:
{:#returns:}
{:#Returns:}

Rating value

Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
$("#rating").ejRating();
// Get current value of rating
var ratingObj = $("#rating").data("ejRating");
ratingObj.getValue(); // get the current value of rting
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
$("#rating").ejRating();
// To get the current value of rating
$("#rating").ejRating("getValue");
&lt;/script&gt;</code>
</pre>



### hide<span class="signature">()</span>
{:#hide}
{:#hide}




To hide the rating control



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
$("#rating").ejRating();
// Hide Rating
var ratingObj = $("#rating").data("ejRating");
ratingObj.hide(); // hides the rating control
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
$("#rating").ejRating();
// hide the rating control
$("#rating").ejRating("hide");
&lt;/script&gt;</code>
</pre>



### refresh<span class="signature">()</span>
{:#refresh}
{:#refresh}




user can refresh the rating control to identify changes



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
$("#rating").ejRating();
// Refresh the rating control
var ratingObj = $("#rating").data("ejRating");
ratingObj.refresh(); // refreshes the rating control
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
$("#rating").ejRating();
// To refresh the rating values
$("#rating").ejRating("refresh");
&lt;/script&gt;</code>
</pre>



### reset<span class="signature">()</span>
{:#reset}
{:#reset}




To reset the rating value



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
$("#rating").ejRating();
// Reset Rating
var ratingObj = $("#rating").data("ejRating");
ratingObj.reset(); // reset the rating values
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
$("#rating").ejRating();
// reset the rating values
$("#rating").ejRating("reset");
&lt;/script&gt;</code>
</pre>



### setValue<span class="signature">()</span>
{:#setvalue}
{:#setValue}




To set the current value of rating control



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
$("#rating").ejRating();
// Set current value of rating
var ratingObj = $("#rating").data("ejRating");
ratingObj.setValue(); // set the current value of rating
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
$("#rating").ejRating();
// To set the current value of rating
$("#rating").ejRating("setValue");
&lt;/script&gt;</code>
</pre>



### show<span class="signature">()</span>
{:#show}
{:#show}




To show the rating control



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
$("#rating").ejRating();
// Show Rating
var ratingObj = $("#rating").data("ejRating");
ratingObj.show(); // shows the rating control
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
$("#rating").ejRating();
// show the rating control
$("#rating").ejRating("show");
&lt;/script&gt;</code>
</pre>


## Events




### change
{:#change}
{:#change}




Fires when Rating value changes.

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
<td class="description last">Event parameters from rating
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
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current value.</td>
</tr>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the rating model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>event</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the mouse click event args values.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
//mouseover event for button
$("#rating").ejRating({
   change: function (args) {}
});
&lt;/script&gt;</code>
</pre>



### click
{:#click}
{:#click}




Fires when Rating control is clicked successfully.

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
<td class="description last">Event parameters from rating
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
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current value.</td>
</tr>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the rating model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>event</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the mouse click event args values.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
//click event for button
$("#rating").ejRating({
   click: function (args) {}
});
&lt;/script&gt;</code>
</pre>



### create
{:#create}
{:#create}




Fires when Rating control is created.

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
<td class="description last">Event parameters from rating
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
<td class="description last">returns the rating model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
//create event for rating
$("#rating").ejRating({
   create: function (args) {}
});
&lt;/script&gt;</code>
</pre>



### destroy
{:#destroy}
{:#destroy}




Fires when Rating control is destroyed successfully.

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
<td class="description last">Event parameters from rating
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
<td class="description last">returns the rating model</td>
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


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
//destroy event for rating
$("#rating").ejRating({
   destroy: function (args) {}
});
&lt;/script&gt;</code>
</pre>



### mouseout
{:#mouseout}
{:#mouseout}




Fires when mouse hover is removed from Rating control

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
<td class="description last">Event parameters from rating
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
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current value.</td>
</tr>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the rating model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>event</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the mouse click event args values.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
//mouseover event for button
$("#rating").ejRating({
   mouseout: function (args) {}
});
&lt;/script&gt;</code>
</pre>



### mouseover
{:#mouseover}
{:#mouseover}




Fires when mouse hovered over the Rating control

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
<td class="description last">Event parameters from rating
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
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current value.</td>
</tr>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the rating model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>event</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the mouse click event args values.</td>
</tr>
<tr>
<td class="name"><code>index</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current index value.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="rating"&gt;&lt;/input&gt; 
 
&lt;script&gt;
//mouseover event for button
$("#rating").ejRating({
   mouseover: function (args) {}
});
&lt;/script&gt;</code>
</pre>



