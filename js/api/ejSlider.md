---
layout: post
title: Properties, Methods and Events of ejSlider Widget
description: API reference for ejSlider
documentation: API
platform: js
keywords: Slider, ejSlider, syncfusion, Slider api 
---

# ejSlider




The Slider provides support to select a value from a particular range as well as selects a range value. The Slider has a sliding base on which the handles are moved. There are three types of Sliders such as default Slider, min-range Slider and range Slider.









#### Syntax

{% highlight javascript %}

$(element).ejSlider()

{% endhighlight %}












#### Example



{% highlight html %}
 
<div id="slider"> </div> 
 
<script> 
// Create Slider 
$('#slider').ejSlider(); 
</script>
{% endhighlight %}







#### Requires





* module:jQuery


* module:jquery.easing.1.3.js


* module:ej.core.js


* module:ej.slider.js




## Members








### allowMouseWheel `boolean`
{:#members:allowmousewheel}








Specifies the allowMouseWheel of the slider.




#### Default Value







* false








### Example



{% highlight html %}
 
<div id="slider"> </div> 
<script>
//To set allowMouseWheel API value during initialization  
$("#slider").ejSlider({ allowMouseWheel: true});
</script>

{% endhighlight %}







### animationSpeed `number`
{:#members:animationspeed}








Specifies the animationSpeed of the slider.




#### Default Value







* 500








#### Example



{% highlight html %}
 
<div id="slider"> </div> 
<script>
//To set animationSpeed API value during initialization  
$("#slider").ejSlider({ animationSpeed: 500});
</script>{% endhighlight %}







### cssClass `string`
{:#members:cssclass}








Specify the CSS class to slider to achieve custom theme.




#### Default Value







* ""








#### Example



{% highlight html %}
 
<div id="slider"> </div> 
<script>
//To set cssClass API value during initialization  
        $("#slider").ejSlider({ cssClass: "gradient-lime"});
</script>{% endhighlight %}







### enableAnimation `boolean`
{:#members:enableanimation}








Specifies the animation behavior of the slider.




#### Default Value







* true








#### Example



{% highlight html %}
 
<div id="slider"> </div> 
<script>
//To set enableAnimation API value during initialization  
        $("#slider").ejSlider({ enableAnimation: false});
</script>{% endhighlight %}







### enabled `boolean`
{:#members:enabled}








Specifies the state of the slider.




#### Default Value







* true








#### Example



{% highlight html %}
<div id="slider"> </div> 
<script>
//To set enabled API value during initialization  
        $("#slider").ejSlider({ enabled: false});
</script>{% endhighlight %}







### enablePersistence `boolean`
{:#members:enablepersistence}








Specify the enablePersistence to slider to save current model value to browser cookies for state maintains




#### Default Value







* false








#### Example



{% highlight html %}
<div id="slider"> </div> 
<script>
//To set enablePersistence API value during initialization  
        $("#slider").ejSlider({ enablePersistence: false});
</script>{% endhighlight %}







### enableRTL `boolean`
{:#members:enablertl}








Specifies the Right to Left Direction of the slider.




#### Default Value







* false








#### Example



{% highlight html %}
 
</br>
</br>
<div id="slider"> </div> 
<script>
//To set enableRTL API value during initialization  
        $("#slider").ejSlider({ enableRTL: false});
</script>{% endhighlight %}







### height `string`
{:#members:height}








Specifies the height of the slider.




#### Default Value







* 14








#### Example



{% highlight html %}
<div id="slider"> </div> 
<script>
//To set height API value during initialization  
        $("#slider").ejSlider({ height: 14});
</script>{% endhighlight %}







### htmlAttributes `object`
{:#members:htmlattributes}








Specifies the HTML Attributes of the ejSlider.




#### Default Value







* {}








#### Example



{% highlight html %}
<div id="slider"> </div> 
<script>
//To set htmlAttributes API value during initialization  
        $("#slider").ejSlider({ htmlAttributes: {disabled:"disabled"}});
</script>{% endhighlight %}







### incrementStep `number`
{:#members:incrementstep}








Specifies the incremental step value of the slider.




#### Default Value







* 1








#### Example



{% highlight html %}
</br>
</br>
<div id="slider"> </div> 
<script>
//To set incrementStep API value during initialization  
        $("#slider").ejSlider({ incrementStep: 2});
</script>{% endhighlight %}







### largeStep `number`
{:#members:largestep}








Specifies the distance between two major (large) ticks from the scale of the slider.




#### Default Value







* 10








#### Example



{% highlight html %}
</br>
</br>
<div id="slider"> </div> 
<script>
//To set largeStep API value during initialization  
        $("#slider").ejSlider({ largeStep: 2});
</script>{% endhighlight %}







### maxValue `number`
{:#members:maxvalue}








Specifies the ending value of the slider.




#### Default Value







* 100








#### Example



{% highlight html %}
</br>
</br>
<div id="slider"> </div> 
<script>
//To set maxValue API value during initialization  
        $("#slider").ejSlider({ maxValue: 60});
</script>{% endhighlight %}







### minValue `number`
{:#members:minvalue}








Specifies the starting value of the slider.




#### Default Value







* 0








#### Example



{% highlight html %}
 
</br>
</br>
<div id="slider"> </div> 
<script>
//To set minValue API value during initialization  
        $("#slider").ejSlider({ minValue: 0});
</script>{% endhighlight %}







### orientation `enum`
{:#members:orientation}



<ts ref="ej.Orientation"/>




Specifies the orientation of the slider. 




<table class="props">
<thead>
<tr>
<th>Name</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Horizontal</td>
<td class="description">Used to set horizontal organizational chart orientation</td>
</tr>
<tr>
<td class="name">
Vertical</td>
<td class="description">Used to set vertical organizational chart orientation</td>
</tr>
</tbody>
</table>




#### Default Value







* ej.orientation.Horizontal








#### Example



{% highlight html %}
<div id="slider"> </div> 
<script>
//To set orientation API value during initialization
$("#slider").ejSlider({ orientation: ej.Orientation.Vertical});
</script>{% endhighlight %}







### readOnly `boolean`
{:#members:readonly}








Specifies the readOnly of the slider.




#### Default Value







* false








#### Example



{% highlight html %}
<div id="slider"> </div> 
<script>
//To set readOnly API value during initialization  
        $("#slider").ejSlider({ readOnly: true});
</script>{% endhighlight %}







### showRoundedCorner `boolean`
{:#members:showroundedcorner}








Specifies the rounded corner behavior for slider.




#### Default Value







* false








#### Example



{% highlight html %}
<div id="slider"> </div> 
<script>
//To set showRoundedCorner API value during initialization  
        $("#slider").ejSlider({ showRoundedCorner: true});
</script>{% endhighlight %}







### showScale `boolean`
{:#members:showscale}








Shows/Hide the major (large) and minor (small) ticks in the scale of the slider.




#### Default Value







* false








#### Example



{% highlight html %}

<div id="slider"> </div> 
<script>
//To set enabled API value during initialization
        $("#slider").ejSlider({ showScale: false});
</script>{% endhighlight %}







### showSmallTicks `boolean`
{:#members:showsmallticks}








Specifies the small ticks from the scale of the slider.




#### Default Value







* true








#### Example



{% highlight html %}

<div id="slider"> </div> 
<script>
//To set showSmallTicks API value during initialization  
        $("#slider").ejSlider({ showSmallTicks: false});
</script> {% endhighlight %}







### showTooltip `boolean`
{:#members:showtooltip}








Specifies the showTooltip to shows the current Slider value, while moving the Slider handle or clicking on the slider handle of the slider.




#### Default Value







* true








#### Example



{% highlight html %}
 

<div id="slider"> </div> 
<script>
//To set showTooltip API value during initialization  
        $("#slider").ejSlider({ showTooltip: true});
</script>{% endhighlight %}







### sliderType `enum`
{:#members:slidertype}




<ts name = "ej.slider.sliderType"/>



Specifies the sliderType of the slider.



<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Default</td>
<td class="description">Shows default slider</td>
</tr>
<tr>
<td class="name">
MinRange</td>
<td class="description">Shows minRange slider</td>
</tr>
<tr>
<td class="name">
Range</td>
<td class="description">Shows Range slider</td>
</tr>
</tbody>
</table>



#### Default Value







* ej.SliderType.Default








#### Example



{% highlight html %}
 
<div id="slider"> </div> 
<script>
//To set sliderType API value during initialization
$("#slider").ejSlider({ sliderType: ej.SliderType.Default});
</script>{% endhighlight %}







### smallStep `number`
{:#members:smallstep}








Specifies the distance between two minor (small) ticks from the scale of the slider.




#### Default Value







* 1








#### Example



{% highlight html %}

<div id="slider"> </div> 
<script>
//To set smallStep API value during initialization  
        $("#slider").ejSlider({ smallStep: 2});
</script>{% endhighlight %}







### value `number`
{:#members:value}








Specifies the value of the slider. But it's not applicable for range slider. To range slider we can use values property. 




#### Default Value







* 0








#### Example



{% highlight html %}

<div id="slider"> </div> 
<script>
//To set value API  during initialization
        $("#slider").ejSlider({ value: 60});
</script>{% endhighlight %}







### values `array`
{:#members:values}








Specifies the values of the range slider. But it's not applicable for default and minRange sliders. we can use value property for default and minRange sliders. 




#### Default Value







* [minValue,maxValue]








#### Example



{% highlight html %}

<div id="slider"> </div> 
<script>
//To set values API during initialization
        $("#slider").ejSlider({ values: [30,60]});
</script>{% endhighlight %}







### width `string`
{:#members:width}








Specifies the width of the slider.




#### Default Value







* 100%








#### Example



{% highlight html %}
 
<div id="slider"> </div> 
<script>
//To set width API value during initialization
        $("#slider").ejSlider({ width: "300px"});
</script>{% endhighlight %}





## Methods








### disable()
{:#methods:disable}








To disable the slider





#### Example



{% highlight html %}
 
<div id="slider"> </div> 
 
<script>
$("#slider").ejSlider();
// Create slider control object
var sliderObj = $("#slider").data("ejSlider");
sliderObj.disable(); // disable the slider control
</script>{% endhighlight %}


{% highlight html %}
 
<div id="slider"> </div> 
 
<script>
$("#slider").ejSlider();
// disable the slider control
$("#slider").ejSlider("disable");
</script>{% endhighlight %}







### enable()
{:#methods:enable}








To enable the slider





#### Example



{% highlight html %}
 
<div id="slider"> </div> 
 
<script>
$("#slider").ejSlider();
// Create slider control object
var sliderObj = $("#slider").data("ejSlider");
sliderObj.enable(); // enable the slider control
</script>{% endhighlight %}


{% highlight html %}
 
<div id="slider"> </div> 
 
<script>
$("#slider").ejSlider();
// enable the slider control
$("#slider").ejSlider("enable");
</script>{% endhighlight %}







### getValue()
{:#methods:getvalue}







To get value from slider handle





#### Returns:
{:#methods:returns:}

number



#### Example



{% highlight html %}
 
<div id="slider"> </div> 
<script>
$("#slider").ejSlider();
// Create slider control object
var sliderObj = $("#slider").data("ejSlider");
sliderObj.getValue(); // get value from the slider handle
</script>
                 
  {% endhighlight %}


{% highlight html %}
 
<div id="slider"> </div> 
 
<script>
$("#slider").ejSlider();
// get value from slider handle
$("#slider").ejSlider("getValue");
</script>{% endhighlight %}





### setValue(value ,[enableAnimation])
{:#methods:setValue}








To set value to slider handle.By default animation is false while set the value. If you want to enable the animation, pass the `enableAnimation` as true to this method. 





#### Example



{% highlight html %}
 
<div id="slider"> </div> 
<script>
$("#slider").ejSlider();
// Create slider control object
var sliderObj = $("#slider").data("ejSlider");
sliderObj.setValue(10); // set value to the slider handle
</script>
                 
  {% endhighlight %}
  
  
  {% highlight html %}
 
<div id="slider"> </div> 
<script>
$("#slider").ejSlider();
// Create slider control object
var sliderObj = $("#slider").data("ejSlider");
sliderObj.setValue(30, true); // enable the slider animation 
</script>
                 
  {% endhighlight %}


{% highlight html %}
 
<div id="slider"> </div> 
 
<script>
$("#slider").ejSlider();
// set value to slider handle
$("#slider").ejSlider("setValue",10);
</script>{% endhighlight %}





## Events








### change
{:#events:change}








Fires once Slider control value is changed successfully.

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
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from slider control
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
sliderIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns current handle number or index</td>
</tr>
<tr>
<td class="name">
id</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns slider id.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.Slider.Model"/><span class="param-type">object</span></td>
<td class="description">returns the slider model.</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
<tr>
<td class="name">
value</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns the slider value.</td>
</tr>
<tr>
<td class="name">
isInteraction</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns true if event triggered by interaction else returns false. </td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<div id="slider"> </div> 
<script>
//change event for slider control
$("#slider").ejSlider({
   change: function (args) {}
});
</script>{% endhighlight %}







### create
{:#events:create}








Fires once Slider control has been created successfully.

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
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from slider control
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
<td class="type"><ts ref="ej.Slider.Model"/><span class="param-type">object</span></td>
<td class="description">returns the slider model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<div id="slider"> </div> 
<script>
//create event for slider control
$("#slider").ejSlider({
   create: function (args) {}
});
</script>{% endhighlight %}







### destroy
{:#events:destroy}








Fires when Slider control has been destroyed successfully.

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
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from slider control
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
<td class="type"><ts ref="ej.Slider.Model"/><span class="param-type">object</span></td>
<td class="description">returns the slider model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<div id="slider"> </div> 
<script>
//destroy event for slider control
$("#slider").ejSlider({
   destroy: function (args) {}
});
</script>{% endhighlight %}







### slide
{:#events:slide}








Fires once Slider control is sliding successfully.


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
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from slider control
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
sliderIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns current handle number or index</td>
</tr>
<tr>
<td class="name">
id</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns slider id</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.Slider.Model"/><span class="param-type">object</span></td>
<td class="description">returns the slider model</td>
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
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns the slider value</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<div id="slider"> </div> 
<script>
//slide event for slider control
$("#slider").ejSlider({
   slide: function (args) {}
});
</script>{% endhighlight %}







### start
{:#events:start}








Fires once Slider control is started successfully.

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
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from slider control
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
sliderIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns current handle number or index</td>
</tr>
<tr>
<td class="name">
id</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns slider id</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.Slider.Model"/><span class="param-type">object</span></td>
<td class="description">returns the slider model</td>
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
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns the slider value</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<div id="slider"> </div> 
<script>
//start event for slider control
$("#slider").ejSlider({
   start: function (args) {}
});
</script>{% endhighlight %}







### stop
{:#events:stop}








Fires when Slider control is stopped successfully.

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
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from slider control
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
sliderIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns current handle number or index</td>
</tr>
<tr>
<td class="name">
id</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns slider id</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.Slider.Model"/><span class="param-type">object</span></td>
<td class="description">returns the slider model</td>
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
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns the slider value</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<div id="slider"> </div> 
<script>
//stop event for slider control
$("#slider").ejSlider({
   stop: function (args) {}
});
</script>{% endhighlight %}




### tooltipChange
{:#events:tooltipchange}




Fires when display the custom tooltip




#### Example



{% highlight html %}
 
<div id="slider"> </div> 
<script>
//tooltipChange event for slider control
$("#slider").ejSlider({
   tooltipChange: function (args) {}
});
</script>{% endhighlight %}

