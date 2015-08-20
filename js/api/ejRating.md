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


{% highlight html %}
 
<input id="rating"></input> 
 
<script>
// Create Rating
$('#rating').ejRating(); 
</script>{% endhighlight %}




Requires
{:.require}


* module:jQuery

* module:jquery.easing.1.3.js

* module:ej.core.js

* module:ej.rating.js


## Members




### allowReset<span class="type-signature type boolean">boolean</span>
{:#members:allowreset}




Enables the rating control with reset button.It can be used to reset the rating control value.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<input id="rating"></input> 
 
<script>
//To set allowReset API value during initialization  
        $("#rating").ejRating({allowReset: true});
</script>{% endhighlight %}




### cssClass<span class="type-signature type string">string</span>
{:#members:cssclass}




Specify the CSS class to rating to achieve custom theme.


Default Value:
{:.param}



* ""




Example
{:.example}


{% highlight html %}
 
<input id="rating"></input> 
 
<script>
// Set the cssClass during initialization.
        $("#rating").ejRating({  cssClass : "gradient-lime" });
</script>{% endhighlight %}




### enabled<span class="type-signature type boolean">boolean</span>
{:#members:enabled}




When this property is set to false, it disables the rating control.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<input id="rating"></input> 
 
<script>
//To set enabled API value during initialization  
        $("#rating").ejRating({enabled: true });
</script>{% endhighlight %}




### enablePersistence<span class="type-signature type boolean">boolean</span>
{:#members:enablepersistence}




Save current model value to browser cookies for state maintanence. While refresh the page Rating control values are retained.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<input id="rating"></input> 
 
<script>
//To set persist API value during initialization  
        $("#rating").ejRating({enablePersistence: true });
</script>{% endhighlight %}




### height<span class="type-signature type string">string</span>
{:#members:height}




Specifies the height of the Rating control wrapper.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
<input id="rating"></input> 
 
<script>
//To set height API value during initialization  
        $("#rating").ejRating({height: "50" });
</script>{% endhighlight %}




### incrementStep<span class="type-signature type number">number</span>
{:#members:incrementstep}




Specifies the value to be increased while navigating between shapes(stars) in Rating control.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
</br>
</br>
<input id="rating"></input> 
 
<script>
//To set incrementStep API value during initialization  
        $("#rating").ejRating({incrementStep: 2 });
</script>{% endhighlight %}




### maxValue<span class="type-signature type number">number</span>
{:#members:maxvalue}




Allow to render the maximum number of Rating shape(star).


Default Value:
{:.param}



* 5




Example
{:.example}


{% highlight html %}
</br>
</br>
<input id="rating"></input> 
 
<script>
//To set maxValue API value during initialization  
        $("#rating").ejRating({maxValue: 10 });
</script>{% endhighlight %}




### minValue<span class="type-signature type number">number</span>
{:#members:minvalue}




Allow to render the minimum number of Rating shape(star).


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
</br>
</br>
<input id="rating"></input> 
 
<script>
//To set minValue API value during initialization  
        $("#rating").ejRating({minValue: 3 });
</script>{% endhighlight %}




### orientation<span class="type-signature type enum">enum</span>
{:#members:orientation}




Specifies the orientation of Rating control. See <a href="global.html#Orientation">Orientation</a>


Default Value:
{:.param}



* ej.Rating.Orientation.Horizontal




Example
{:.example}


{% highlight html %}
 
<input id="rating"></input> 
 
<script>
//To set orientation API value during initialization  
        $("#rating").ejRating({orientation: ej.Rating.Orientation.Horizontal });
</script> {% endhighlight %}




### precision<span class="type-signature type enum">enum</span>
{:#members:precision}




Helps to provide more precise ratings.Rating control supports three precision modes - full, half, and exact. See <a href="global.html#Precision">Precision</a>


Default Value:
{:.param}



* "full"




Example
{:.example}


{% highlight html %}
</br>
</br>
<input id="rating"></input> 
 
<script>
//To set precision API value during initialization  
        $("#rating").ejRating({precision: ej.Rating.Precision.Half});
</script>{% endhighlight %}




### readOnly<span class="type-signature type boolean">boolean</span>
{:#members:readonly}




Interaction with Rating control can be prevented by enabling this API.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<input id="rating"></input> 
 
<script>
//To set readOnly API value during initialization  
        $("#rating").ejRating({readOnly: true});
</script>{% endhighlight %}




### shapeHeight<span class="type-signature type number">number</span>
{:#members:shapeheight}




To specify the height of each shape in Rating control.


Default Value:
{:.param}



* 23




Example
{:.example}


{% highlight html %}
 
<input id="rating"></input> 
 
<script>
//To set shapeHeight API value during initialization  
        $("#rating").ejRating({shapeHeight: 25 });
</script>{% endhighlight %}




### shapeWidth<span class="type-signature type number">number</span>
{:#members:shapewidth}




To specify the width of each shape in Rating control.


Default Value:
{:.param}



* 23




Example
{:.example}


{% highlight html %}
 
<input id="rating"></input> 
 
<script>
//To set shapeWidth API value during initialization  
        $("#rating").ejRating({shapeWidth: 25 });
</script>{% endhighlight %}




### showTooltip<span class="type-signature type boolean">boolean</span>
{:#members:showtooltip}




Enables the tooltip option.Currently selected value value will be displayed in tooltip.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
</br>
</br>
<input id="rating"></input> 
 
<script>
//To set showTooltip API value during initialization  
        $("#rating").ejRating({showTooltip: true});
</script>{% endhighlight %}




### value<span class="type-signature type number">number</span>
{:#members:value}




To specify the number of stars to be selected while rendering.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
</br>
</br>
<input id="rating"></input> 
 
<script>
//To set value API value during initialization  
        $("#rating").ejRating({value: 3 });
</script>{% endhighlight %}




### width<span class="type-signature type string">string</span>
{:#members:width}




Specifies the width of the Rating control wrapper.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
<input id="rating"></input> 
 
<script>
//To set width API value during initialization  
        $("#rating").ejRating({width: "200" });
</script>{% endhighlight %}



## Methods




### destroy<span class="signature">()</span>
{:#methods:destroy}




destroy the Rating widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.



Example
{:.example}


{% highlight html %}
 
<rating id="rating">Rating</rating> 
 
<script>
$("#rating").ejRating();
// Create Rating
var ratingObj = $("#rating").data("ejRating");
ratingObj.destroy(); // destroy the button
</script>{% endhighlight %}


{% highlight html %}
 
<rating id="rating">Rating</rating> 
 
<script>
$("#rating").ejRating();
// destroy the rating
$("#rating").ejRating("destroy");
</script>{% endhighlight %}




### getValue<span class="signature">()</span>
{:#methods:getvalue}




To get the current value of rating control



#### Returns:
{:#methods:returns:}

Rating value

Example
{:.example}


{% highlight html %}
 
<input id="rating"></input> 
 
<script>
$("#rating").ejRating();
// Get current value of rating
var ratingObj = $("#rating").data("ejRating");
ratingObj.getValue(); // get the current value of rting
</script>{% endhighlight %}


{% highlight html %}
 
<input id="rating"></input> 
 
<script>
$("#rating").ejRating();
// To get the current value of rating
$("#rating").ejRating("getValue");
</script>{% endhighlight %}




### hide<span class="signature">()</span>
{:#methods:hide}




To hide the rating control



Example
{:.example}


{% highlight html %}
 
<input id="rating"></input> 
 
<script>
$("#rating").ejRating();
// Hide Rating
var ratingObj = $("#rating").data("ejRating");
ratingObj.hide(); // hides the rating control
</script>{% endhighlight %}


{% highlight html %}
 
<input id="rating"></input> 
 
<script>
$("#rating").ejRating();
// hide the rating control
$("#rating").ejRating("hide");
</script>{% endhighlight %}




### refresh<span class="signature">()</span>
{:#methods:refresh}




user can refresh the rating control to identify changes



Example
{:.example}


{% highlight html %}
 
<input id="rating"></input> 
 
<script>
$("#rating").ejRating();
// Refresh the rating control
var ratingObj = $("#rating").data("ejRating");
ratingObj.refresh(); // refreshes the rating control
</script>{% endhighlight %}


{% highlight html %}
 
<input id="rating"></input> 
 
<script>
$("#rating").ejRating();
// To refresh the rating values
$("#rating").ejRating("refresh");
</script>{% endhighlight %}




### reset<span class="signature">()</span>
{:#methods:reset}




To reset the rating value



Example
{:.example}


{% highlight html %}
 
<input id="rating"></input> 
 
<script>
$("#rating").ejRating();
// Reset Rating
var ratingObj = $("#rating").data("ejRating");
ratingObj.reset(); // reset the rating values
</script>{% endhighlight %}


{% highlight html %}
 
<input id="rating"></input> 
 
<script>
$("#rating").ejRating();
// reset the rating values
$("#rating").ejRating("reset");
</script>{% endhighlight %}




### setValue<span class="signature">()</span>
{:#methods:setvalue}




To set the current value of rating control



Example
{:.example}


{% highlight html %}
 
<input id="rating"></input> 
 
<script>
$("#rating").ejRating();
// Set current value of rating
var ratingObj = $("#rating").data("ejRating");
ratingObj.setValue(); // set the current value of rating
</script>{% endhighlight %}


{% highlight html %}
 
<input id="rating"></input> 
 
<script>
$("#rating").ejRating();
// To set the current value of rating
$("#rating").ejRating("setValue");
</script>{% endhighlight %}




### show<span class="signature">()</span>
{:#methods:show}




To show the rating control



Example
{:.example}


{% highlight html %}
 
<input id="rating"></input> 
 
<script>
$("#rating").ejRating();
// Show Rating
var ratingObj = $("#rating").data("ejRating");
ratingObj.show(); // shows the rating control
</script>{% endhighlight %}


{% highlight html %}
 
<input id="rating"></input> 
 
<script>
$("#rating").ejRating();
// show the rating control
$("#rating").ejRating("show");
</script>{% endhighlight %}



## Events




### change
{:#events:change}




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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current value.</td>
</tr>
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
<td class="description last">returns the rating model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
event{% endhighlight %}</td>
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


{% highlight html %}
 
<input id="rating"></input> 
 
<script>
//mouseover event for button
$("#rating").ejRating({
   change: function (args) {}
});
</script>{% endhighlight %}




### click
{:#events:click}




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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current value.</td>
</tr>
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
<td class="description last">returns the rating model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
event{% endhighlight %}</td>
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


{% highlight html %}
 
<input id="rating"></input> 
 
<script>
//click event for button
$("#rating").ejRating({
   click: function (args) {}
});
</script>{% endhighlight %}




### create
{:#events:create}




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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the rating model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
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


{% highlight html %}
 
<input id="rating"></input> 
 
<script>
//create event for rating
$("#rating").ejRating({
   create: function (args) {}
});
</script>{% endhighlight %}




### destroy
{:#events:destroy}




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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the rating model</td>
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
 
<input id="rating"></input> 
 
<script>
//destroy event for rating
$("#rating").ejRating({
   destroy: function (args) {}
});
</script>{% endhighlight %}




### mouseout
{:#events:mouseout}




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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current value.</td>
</tr>
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
<td class="description last">returns the rating model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
event{% endhighlight %}</td>
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


{% highlight html %}
 
<input id="rating"></input> 
 
<script>
//mouseover event for button
$("#rating").ejRating({
   mouseout: function (args) {}
});
</script>{% endhighlight %}




### mouseover
{:#events:mouseover}




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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current value.</td>
</tr>
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
<td class="description last">returns the rating model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
event{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the mouse click event args values.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
index{% endhighlight %}</td>
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


{% highlight html %}
 
<input id="rating"></input> 
 
<script>
//mouseover event for button
$("#rating").ejRating({
   mouseover: function (args) {}
});
</script>{% endhighlight %}




