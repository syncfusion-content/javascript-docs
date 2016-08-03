---
layout: post
title: ejRadialSlider
documentation: API
platform: js
keywords: ejRadialSlider, API, Essential JS RadialSlider
---

# ejRadialSlider

The RadialSlider provides an optimized interface for selecting a numeric value using a touch interface. Value is returned based on direct needle selection or needle move. It can also be customized as a full circle, half circle, or any portion of a circle, based on startAngle and endAngle



#### Syntax

{% highlight js %}
 
    $(element).ejRadialSlider()

{% endhighlight %}


#### Example

{% highlight html %}
 
    <script>
    $("#radialSlider").ejRadialSlider();
    </script>
    <div id="radialSlider">
    </div>
   
{% endhighlight %}




#### Requires

* module:jQuery

* module:ej.core

* module:ej.touch

* module:ej.radialslider


## Members

### autoOpen `Boolean`
{:#members:autoopen}


To show the RadialSlider in initial render.


#### Default Value:

* false


#### Example


{% highlight html %}
 
    // Set RadialSlider autoOpen on initialization. 
    //To set autoOpen API 
    <div id="radialSlider">
    </div>
    <script>
    $(function()
    {
    $("#radialSlider").ejRadialSlider({autoOpen:true});
    });
    </script>
    
{% endhighlight %}




### cssClass `String`
{:#members:cssclass}


Sets the root class for RadialSlider theme. This cssClass API helps to use custom skinning option for RadialSlider control. By defining the root class using this API, we need to include this root class in CSS.


#### Default Value:

* ""


#### Example 


{% highlight html %}
 
    // Set RadialSlider cssClass on initialization. 
    //To set cssClass API 
    <div id="radialSlider">
    </div>
    <script>
    $(function()
    {
    $("#radialSlider").ejRadialSlider({cssClass:"customclass"});
    });
    </script>

{% endhighlight %}


### enableAnimation `Boolean`
{:#members:enableanimation}


To enable Animation for Radial Slider.


#### Default Value:

* true


####Example



{% highlight html %}
 
    // Set Radialslider enableAnimation on initialization. 
    //To set enableAnimation API 
    <div id="radialSlider">
    </div>
    <script>
    $(function()
    {
    $("#radialSlider").ejRadialSlider({ enableAnimation:false });
    });
    </script>
    
{% endhighlight %}





### enableRoundOff  `Boolean`
{:#members:enableroundoff}


Enable/Disable the Roundoff property of RadialSlider


#### Default Value:

* true


#### Example


{% highlight html %}
 
    // Set Radialslider enableRoundOff on initialization. 
    //To set enableRoundOff API 
    <div id="radialSlider">
    </div>
    <script>
    $(function()
    {
    $("#radialSlider").ejRadialSlider({ enableRoundOff :false });
    });
    </script>

{% endhighlight %}






### endAngle  `Number`
{:#members:endangle}


Specifies the endAngle value for radial slider circle.


#### Default Value:

* 360




#### Example


{% highlight html %}
 
    // Set Radialslider endAngle on initialization. 
    //To set endAngle API 
    <div id="radialSlider">
    </div>
    <script>
    $(function()
    {
    $("#radialSlider").ejRadialSlider({ endAngle:180 });
    });
    </script>

{% endhighlight %}



### inline  `Boolean`
{:#members:inline}


Specifies the inline for label show or not on given radius.


#### Default Value:

* false




#### Example

{% highlight html %}
 
    // Set Radialslider inline on initialization. 
    //To set inline API 
    <div id="radialSlider">
    </div>
    <script>
    $(function(){
    $("#radialSlider").ejRadialSlider({ inline: true });
    });
    </script>

{% endhighlight %}



### innerCircleImageClass `String`
{:#members:innercircleimageclass}


Specifies innerCircleImageClass, using this property we can give images for center radial circle through CSS classes.


#### Default Value:

* null




#### Example


{% highlight html %}
 
    // Set Radialslider innerCircleImageClass on initialization. 
    //To set innerCircleImageClass API 
    <div id="radialSlider">
    </div>
    <script>
    $(function()
    {
    $("#radialSlider").ejRadialSlider({ innerCircleImageClass:"slider" }); 
    });
    </script>

{% endhighlight %}



### innerCircleImageUrl `String`
{:#members:innercircleimageurl}


Specifies the file name of center circle icon


#### Default Value:

* null


#### Example

{% highlight html %}
 
    // Set Radialslider innerCircleImageClass on initialization. 
    //To set innerCircleImageClass API 
    <div id="radialSlider">
    </div>
    <script>
    $(function()
    {
    $("#radialSlider").ejRadialSlider({ innerCircleImageUrl:"../images/radialslider/chevron-right.png" });
    });
    </script>

{% endhighlight %}



### labelSpace `Number`
{:#members:labelspace}


Specifies the Space between the radial slider element and the label.


#### Default Value:

* 30



#### Example



{% highlight html %}
 
    // Set Radialslider labelSpace on initialization. 
    //To set labelSpace API  
    <div id="radialSlider">
    </div>
    <script>
    $(function()
    {
    $("#radialSlider").ejRadialSlider({ labelSpace:100 });
    });
    </script>

{% endhighlight %}





### radius `Number`
{:#members:radius}


Specifies the radius of radial slider


#### Default Value:

* 200



#### Example



{% highlight html %}
 
    // Set Radialslider radius on initialization. 
    //To set radius API  
    <div id="radialSlider">
    </div>
    <script>
    $(function()
    {
    $("#radialSlider").ejRadialSlider({ radius:100 });
    });
    </script>

{% endhighlight %}




### showInnerCircle  `Boolean`
{:#members:showinnercircle}


To show the RadialSlider inner circle.


#### Default Value:

* true




#### Example


{% highlight html %}
 
    // Set Radialslider showInnerCircle on initialization. 
    //To set showInnerCircle API 
    <div id="radialSlider">
    </div>
    <script>
    $(function()
    {
    $("#radialSlider").ejRadialSlider({ showInnerCircle:false });
    });
    </script>

{% endhighlight %}





### startAngle  `Number`
{:#members:startangle}


Specifies the endAngle value for radial slider circle.


#### Default Value:

* 0




#### Example


{% highlight html %}
 
    // Set Radialslider startAngle on initialization. 
    //To set startAngle API 
    <div id="radialSlider">
    </div>
    <script>
    $(function()
    {
    $("#radialSlider").ejRadialSlider({ startAngle:180 });
    });
    </script>

{% endhighlight %}




### strokeWidth  `Number`
{:#members:strokewidth}


Specifies the  strokeWidth for customize the needle, outer circle and inner circle.


#### Default Value:

* 2


#### Example


{% highlight html %}
 
    // Set RadialSlider strokeWidth on initialization. 
    //To set strokeWidth API 
    <div id="radialSlider">
    </div>
    <script>
    $(function(){
    $("#radialSlider").ejRadialSlider({ strokeWidth:4 });
    });
    </script>

{% endhighlight %}



## ticks `Array`
{:#members:ticks}


Specifies the ticks value of radial slider


#### Example



{% highlight html %}
 
    // Set Radialslider ticks value on initialization. 
    //To set ticks API  
    <div id="radialSlider">
    </div>
    <script>
    $(function()
    {
    $("#radialSlider").ejRadialSlider({ ticks:[0, 10, 20, 30, 40, 50, 60, 70, 80, 90, 100] });
    });
    </script>

{% endhighlight %}






### value `Number`
{:#members:value}


Specifies the value of radial slider


#### Default Value:

* 10



#### Example



{% highlight html %}
 
    // Set Radialslider value on initialization. 
    //To set value API  
    <div id="radialSlider">
    </div>
    <script>
    $(function()
    {
    $("#radialSlider").ejRadialSlider({ value:40 });
    });
    </script>

{% endhighlight %}






## Methods




### show()
{:#methods:show}

To show the radialslider



#### Example


{% highlight html %}
 
    <div id="radialSlider"></div>
 
    <script>
    var obj = $("#radialSlider").ejRadialSlider(); // render radial slider control
    obj.show(); // call the show method of Radial slider
    </script>

{% endhighlight %}




### hide()
{:#methods:hide}


To hide the radialslider



#### Example


{% highlight html %}
 
    <div id="radialSlider"></div>
 
    <script>
    var obj = $("#radialSlider").ejRadialSlider(); // render the radial slider control
    obj.hide(); // call the hide method of Radial slider
    </script>
    
{% endhighlight %}



## Events




### change
{:#events:change}


Event triggers when the change occurs.

<table class="params" border="1">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>

<tbody>

<tr>
<td> model </td>
<td> Object </td>
<td> returns the Radialslider model </td>
</tr>

<tr>
<td> cancel </td>
<td> boolean </td>
<td> if the event should be canceled; otherwise, false. </td>
</tr>

<tr>
<td> oldValue </td>
<td> Number </td>
<td> returns the initial value of Radial slider </td>
</tr>

<tr>
<td> type </td>
<td> string </td>
<td> returns the name of the event </td>
</tr>

<tr>
<td> value </td>
<td> Number </td>
<td> returns the current value of the Radial slider </td>
</tr>

</tbody>
</table>


#### Example



{% highlight html %}
 
    //Change event for Radialslider
 
    <div id="radialSlider"></div>

    <script>
    $("#radialSlider").ejRadialSlider ({
    change: function (args) 
    { 
    //handle the event
    }
    });         
    </script>
    
    
{% endhighlight %}




### create
{:#events:create}


Event triggers when the radial slider is created.

<table class="params" border="1">
<thead>
<tr>
<th> Name </th>
<th> Type </th>
<th> Description </th>
</tr>
</thead>

<tbody>
<tr>
<td> cancel </td>
<td> boolean </td>
<td> if the event should be canceled; otherwise, false. </td>
</tr>

<tr>
<td> model </td>
<td> object </td>
<td> returns the Radialslider model /td>
</tr>

<tr>
<td> type </td>
<td> string </td>
<td> returns the name of the event </td>
</tr>

</tbody>
</table>


#### Example


{% highlight html %}
 
    //Create event for Radialslider

    <div id="radialSlider"></div>

    <script>
    $("#radialSlider").ejRadialSlider ({
    create: function (args) 
    { 
    //handle the event
    }
    });         
    </script>
    
    
{% endhighlight %}




### mouseover
{:#events:mouseover}


Event triggers when the mouse pointer is dragged over the radial slider.

<table class="params" border="1">
<thead>
<tr>
<th> Name </th>
<th> Type </th>
<th> Description </th>
</tr>
</thead>

<tbody>
<tr>
<td> cancel </td>
<td> boolean </td>
<td> if the event should be canceled; otherwise, false. </td>
</tr>

<tr>
<td> model </td>
<td> Object </td>
<td> returns the Radialslider model </td>
</tr>

<tr>
<td> selectedValue </td>
<td> Number </td>
<td> returns the value selected </td>
</tr>

<tr>
<td> type </td>
<td> string </td>
<td> returns the name of the event </td>
</tr>


<tr>
<td> value </td>
<td> Number </td>
<td> returns the current value selected in Radial slider </td>
</tr>

</tbody>
</table>



#### Example


{% highlight html %}
 
    //mouseover event for Radialslider

    <div id="radialSlider"></div>
    <script>
    $("#radialSlider").ejRadialSlider ({
    mouseover: function (args) 
    { 
    //handle the event
    }
    });         
    </script>
    
{% endhighlight %}




### slide
{:#events:slide}


Event triggers when the Radial slider slides.

<table class="params" border="1">
<thead>
<tr>
<th> Name </th>
<th> Type </th>
<th> Description </th>
</tr>
</thead>

<tbody>
<tr>
<td>
cancel
</td>
<td> boolean </td>
<td> if the event should be canceled; otherwise, false. </td>
</tr>

<tr>
<td> model </td>
<td> Object </td>
<td> returns the Radialslider model </td>
</tr>

<tr>
<td> selectedValue </td>
<td> Number </td>
<td> returns the value selected in Radial slider </td>
</tr>

<tr>
<td> type </td>
<td> string </td>
<td> returns the name of the event </td>
</tr>

<tr>
<td> value </td>
<td> Number </td>
<td> returns the currently selected value </td>
</tr>

</tbody>
</table>


#### Example


{% highlight html %}

 
    //Slide event for Radialslider

    <div id="radialSlider"></div>
    
    <script>
    $("#radialSlider").ejRadialSlider ({
    slide: function (args) 
    { 
    //handle the event
    }
    });         
    </script>
    
 {% endhighlight %}   




### start
{:#events:start}




Event triggers when the radial slider starts.

<table class="params" border="1">
<thead>
<tr>
<th> Name </th>
<th> Type </th>
<th> Description </th>
</tr>
</thead>

<tbody>

<tr>
<td> cancel </td>
<td> boolean </td>
<td> if the event should be canceled; otherwise, false. </td>
</tr>

<tr>
<td> model </td>
<td> Object </td>
<td> returns the Radialslider model </td>
</tr>

<tr>
<td> type </td>
<td> string </td>
<td> returns the name of the event </td>
</tr>

<tr>
<td> value </td>
<td> Number </td>
<td> returns the current value selected in Radial slider </td>
</tr>

</tbody>
</table>


#### Example



{% highlight html %}
 
    //Start event for Radialslider

    <div id="radialSlider"></div>

    <script>
    $("#radialSlider").ejRadialSlider ({
    start: function (args) 
    { 
    //handle the event
    }
    });         
    </script>
    
    
{% endhighlight %}




### stop
{:#events:stop}


Event triggers when the radial slider stops.

<table class="params" border="1">
<thead>
<tr>
<th> Name </th>
<th> Type </th>
<th> Description </th>
</tr>
</thead>

<tbody>

<tr>
<td> cancel </td>
<td> boolean </td>
<td> if the event should be canceled; otherwise, false. </td>
</tr>

<tr>
<td> model </td>
<td> Object </td>
<td> returns the Radialslider model </td>
</tr>

<tr>
<td> type </td>
<td> string </td>
<td> returns the name of the event </td>
</tr>

<tr>
<td> value </td>
<td> Number </td>
<td> returns the current value selected in Radial slider </td>
</tr>

</tbody>
</table>


#### Example


{% highlight html %}
 
    //Stop event for Radialslider

    <div id="radialSlider"></div>

    <script>
    $("#radialSlider").ejRadialSlider ({
    stop: function (args) 
    { 
    //handle the event
    }
    });         
    </script>
    
    
{% endhighlight %}