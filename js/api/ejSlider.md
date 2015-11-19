---
layout: post
title: ejSlider
documentation: API
platform: js
metaname: 
metacontent: 
---

# ejSlider




The Slider provides support to select a value from a particular range as well as selects a range value. The Slider has a sliding base on which the handles are moved. There are three types of Sliders such as default Slider, min-range Slider and range Slider.










$(element).ejSlider<span class="signature">()</span>











Example
{:.example}


{% highlight html %}
 
<div id="slider"> </div> 
 
<script> 
// Create Slider 
$('#slider').ejSlider(); 
</script> 
{% endhighlight %}







Requires
{:.require}




* module:jQuery


* module:jquery.easing.1.3.js


* module:ej.core.js


* module:ej.slider.js




## Members








### animationSpeed<span class="type-signature type number">number</span>
{:#members:animationspeed}








Specifies the animationSpeed of the slider.




Default Value:
{:.param}






* 500








Example
{:.example}


{% highlight html %}
 
<div id="slider"> </div> 
<script>
//To set animationSpeed API value during initialization  
$("#slider").ejSlider({ animationSpeed: 500});
</script>{% endhighlight %}







### cssClass<span class="type-signature type string">string</span>
{:#members:cssclass}








Specify the CSS class to slider to achieve custom theme.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="slider"> </div> 
<script>
//To set cssClass API value during initialization  
        $("#slider").ejSlider({ cssClass: "gradient-lime"});
</script>{% endhighlight %}







### enableAnimation<span class="type-signature type boolean">boolean</span>
{:#members:enableanimation}








Specifies the animation behavior of the slider.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="slider"> </div> 
<script>
//To set enableAnimation API value during initialization  
        $("#slider").ejSlider({ enableAnimation: false});
</script>{% endhighlight %}







### enabled<span class="type-signature type boolean">boolean</span>
{:#members:enabled}








Specifies the state of the slider.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
<div id="slider"> </div> 
<script>
//To set enabled API value during initialization  
        $("#slider").ejSlider({ enabled: false});
</script>{% endhighlight %}







### enablePersistence<span class="type-signature type boolean">boolean</span>
{:#members:enablepersistence}








Specify the enablePersistence to slider to save current model value to browser cookies for state maintains




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
<div id="slider"> </div> 
<script>
//To set enablePersistence API value during initialization  
        $("#slider").ejSlider({ enablePersistence: false});
</script>{% endhighlight %}







### enableRTL<span class="type-signature type boolean">boolean</span>
{:#members:enablertl}








Specifies the Right to Left Direction of the slider.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
</br>
</br>
<div id="slider"> </div> 
<script>
//To set enableRTL API value during initialization  
        $("#slider").ejSlider({ enableRTL: false});
</script>{% endhighlight %}







### height<span class="type-signature type string">String</span>
{:#members:height}








Specifies the height of the slider.




Default Value:
{:.param}






* 14








Example
{:.example}


{% highlight html %}
<div id="slider"> </div> 
<script>
//To set height API value during initialization  
        $("#slider").ejSlider({ height: 14});
</script>{% endhighlight %}







### incrementStep<span class="type-signature type number">number</span>
{:#members:incrementstep}








Specifies the incremental step value of the slider.




Default Value:
{:.param}






* 1








Example
{:.example}


{% highlight html %}
</br>
</br>
<div id="slider"> </div> 
<script>
//To set incrementStep API value during initialization  
        $("#slider").ejSlider({ incrementStep: 2});
</script>{% endhighlight %}







### largeStep<span class="type-signature type number">number</span>
{:#members:largestep}








Specifies the distance between two major (large) ticks from the scale of the slider.




Default Value:
{:.param}






* 10








Example
{:.example}


{% highlight html %}
</br>
</br>
<div id="slider"> </div> 
<script>
//To set largeStep API value during initialization  
        $("#slider").ejSlider({ largeStep: 2});
</script>{% endhighlight %}







### maxValue<span class="type-signature type number">number</span>
{:#members:maxvalue}








Specifies the ending value of the slider.




Default Value:
{:.param}






* 100








Example
{:.example}


{% highlight html %}
</br>
</br>
<div id="slider"> </div> 
<script>
//To set maxValue API value during initialization  
        $("#slider").ejSlider({ maxValue: 60});
</script>{% endhighlight %}







### minValue<span class="type-signature type number">number</span>
{:#members:minvalue}








Specifies the starting value of the slider.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
</br>
</br>
<div id="slider"> </div> 
<script>
//To set minValue API value during initialization  
        $("#slider").ejSlider({ minValue: 0});
</script>{% endhighlight %}







### orientation<span class="type-signature type enum">enum</span>
{:#members:orientation}








Specifies the orientation of the slider.See orientation




Default Value:
{:.param}






* ej.orientation.Horizontal








Example
{:.example}


{% highlight html %}
<div id="slider"> </div> 
<script>
//To set orientation API value during initialization
$("#slider").ejSlider({ orientation: ej.Orientation.Vertical});
</script>{% endhighlight %}







### readOnly<span class="type-signature type boolean">boolean</span>
{:#members:readonly}








Specifies the readOnly of the slider.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
<div id="slider"> </div> 
<script>
//To set readOnly API value during initialization  
        $("#slider").ejSlider({ readOnly: true});
</script>{% endhighlight %}







### showRoundedCorner<span class="type-signature type boolean">boolean</span>
{:#members:showroundedcorner}








Specifies the rounded corner behavior for slider.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
<div id="slider"> </div> 
<script>
//To set showRoundedCorner API value during initialization  
        $("#slider").ejSlider({ showRoundedCorner: true});
</script>{% endhighlight %}







### showScale<span class="type-signature type boolean">boolean</span>
{:#members:showscale}








Specifies the major (large) and minor (small) ticks of the slider.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
</br>
</br>
<div id="slider"> </div> 
<script>
//To set enabled API value during initialization
        $("#slider").ejSlider({ showScale: false});
</script>{% endhighlight %}







### showSmallTicks<span class="type-signature type boolean">boolean</span>
{:#members:showsmallticks}








Specifies the showSmallTicks of the slider.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
</br>
</br>
<div id="slider"> </div> 
<script>
//To set showSmallTicks API value during initialization  
        $("#slider").ejSlider({ showSmallTicks: false});
</script> {% endhighlight %}







### showTooltip<span class="type-signature type boolean">boolean</span>
{:#members:showtooltip}








Specifies the showTooltip to shows the current Slider value, while moving the Slider handle of the slider.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
</br>
</br>
<div id="slider"> </div> 
<script>
//To set showTooltip API value during initialization  
        $("#slider").ejSlider({ showTooltip: true});
</script>{% endhighlight %}







### sliderType<span class="type-signature type enum">enum</span>
{:#members:slidertype}








Specifies the sliderType of the slider.




Default Value:
{:.param}






* ej.SliderType.Default








Example
{:.example}


{% highlight html %}
 
<div id="slider"> </div> 
<script>
//To set sliderType API value during initialization
$("#slider").ejSlider({ sliderType: ej.SliderType.Default});
</script>{% endhighlight %}







### smallStep<span class="type-signature type number">number</span>
{:#members:smallstep}








Specifies the distance between two minor (small) ticks from the scale of the slider.




Default Value:
{:.param}






* 1








Example
{:.example}


{% highlight html %}
</br>
</br>
<div id="slider"> </div> 
<script>
//To set smallStep API value during initialization  
        $("#slider").ejSlider({ smallStep: 2});
</script>{% endhighlight %}







### value<span class="type-signature type number">number</span>
{:#members:value}








Specifies the value of the slider.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
</br>
</br>
<div id="slider"> </div> 
<script>
//To set value API  during initialization
        $("#slider").ejSlider({ value: 60});
</script>{% endhighlight %}







### values<span class="type-signature type array">array</span>
{:#members:values}








Specifies the values of the range slider.




Default Value:
{:.param}






* [minValue,maxValue]








Example
{:.example}


{% highlight html %}
</br>
</br>
<div id="slider"> </div> 
<script>
//To set values API during initialization
        $("#slider").ejSlider({ values: [30,60]});
</script>{% endhighlight %}







### width<span class="type-signature type string">String</span>
{:#members:width}








Specifies the width of the slider.




Default Value:
{:.param}






* 100%








Example
{:.example}


{% highlight html %}
 
<div id="slider"> </div> 
<script>
//To set width API value during initialization
        $("#slider").ejSlider({ width: "300px"});
</script>{% endhighlight %}





## Methods








### disable<span class="signature">()</span>
{:#methods:disable}








To disable the slider





Example
{:.example}


{% highlight html %}
 
<div id="slider"> </div> 
 
<script>
$("#slider").ejSlider();
// Create slider control
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







### enable<span class="signature">()</span>
{:#methods:enable}








To enable the slider





Example
{:.example}


{% highlight html %}
 
<div id="slider"> </div> 
 
<script>
$("#slider").ejSlider();
// Create slider control
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







### getValue<span class="signature">()</span>
{:#methods:getvalue}








To get value from slider handle





Example
{:.example}


{% highlight html %}
 
<div id="slider"> </div> 
<script>
$("#slider").ejSlider();
// Create Editors
var sliderObj = $("#slider").data("ejSlider");
sliderObj.getValue(); // getValue the slider handle
</script>
                 {% endhighlight %}


{% highlight html %}
 
<div id="slider"> </div> 
 
<script>
$("#slider").ejSlider();
// get value from slider handle
$("#slider").ejSlider("getValue");
</script>{% endhighlight %}





## Events








### change
{:#events:change}








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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
sliderIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns current handle number or index</td>
</tr>
<tr>
<td class="name">{% highlight html %}
id{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns slider id</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the slider model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the slider value</td>
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
 
<div id="slider"> </div> 
<script>
//change event for slider control
$("#slider").ejSlider({
   change: function (args) {}
});
</script>{% endhighlight %}







### create
{:#events:create}








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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the slider model</td>
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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the slider model</td>
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
 
<div id="slider"> </div> 
<script>
//destroy event for slider control
$("#slider").ejSlider({
   destroy: function (args) {}
});
</script>{% endhighlight %}







### slide
{:#events:slide}








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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
sliderIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns current handle number or index</td>
</tr>
<tr>
<td class="name">{% highlight html %}
id{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns slider id</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the slider model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the slider value</td>
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
 
<div id="slider"> </div> 
<script>
//slide event for slider control
$("#slider").ejSlider({
   slide: function (args) {}
});
</script>{% endhighlight %}







### start
{:#events:start}








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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
sliderIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns current handle number or index</td>
</tr>
<tr>
<td class="name">{% highlight html %}
id{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns slider id</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the slider model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the slider value</td>
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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
sliderIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns current handle number or index</td>
</tr>
<tr>
<td class="name">{% highlight html %}
id{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns slider id</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the slider model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the slider value</td>
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
 
<div id="slider"> </div> 
<script>
//stop event for slider control
$("#slider").ejSlider({
   stop: function (args) {}
});
</script>{% endhighlight %}




