---
layout: post
title: Properties, Methods and Events of ejRating Widget
description: API reference for ejRating
documentation: API
platform: js
keywords: Rating, ejRating, syncfusion, Rating api 
---

# ejRating


The Rating control provides an intuitive Rating experience that enables you to select a number of stars that represent a Rating. You can configure the item size, orientation and the number of displayed items in the Rating control. You can also customize the Rating star image by using custom CSS.


#### Syntax

{% highlight javascript %}

$(element).ejRating()

{% endhighlight %}


#### Example


{% highlight html %}
 
    <input id="rating"></input>

    <script>
        // Create Rating
        $('#rating').ejRating();
    </script>

{% endhighlight %}


#### Requires


* module:jQuery

* module:jquery.easing.1.3.js

* module:ej.core.js

* module:ej.rating.js


## Members

### allowReset `boolean`
{:#members:allowreset}

Enables the rating control with reset button.It can be used to reset the rating control value.


#### Default Value


* true


#### Example


{% highlight html %}
 
    <input id="rating"></input>

    <script>
        //To set allowReset API value during initialization
        $("#rating").ejRating({ allowReset: true });
    </script>

{% endhighlight %}


### cssClass `string`
{:#members:cssclass}


Specify the CSS class to achieve custom theme.


#### Default Value


* ""

#### Example


{% highlight html %}
 
    <input id="rating"></input>

    <script>
        // Set the cssClass during initialization.
        $("#rating").ejRating({ cssClass: "gradient-lime" });
    </script>

{% endhighlight %}



### enabled `boolean`
{:#members:enabled}

When this property is set to false, it disables the rating control.

#### Default Value

* true

#### Example


{% highlight html %}
 
    <input id="rating"></input>

    <script>
        //To set enabled API value during initialization
        $("#rating").ejRating({ enabled: true });
    </script>

{% endhighlight %}


### enablePersistence `boolean`
{:#members:enablepersistence}

Save current model value to browser cookies for state maintenance. While refresh the page Rating control values are retained.

#### Default Value

* false

#### Example


{% highlight html %}
 
    <input id="rating"></input>

    <script>
        //To set persist API value during initialization
        $("#rating").ejRating({ enablePersistence: true });
    </script>

{% endhighlight %}


### height `string`
{:#members:height}


Specifies the height of the Rating control wrapper.

#### Default Value

* null

#### Example


{% highlight html %}

    <input id="rating"></input>

    <script>
        //To set height API value during initialization
        $("#rating").ejRating({ height: "50" });
    </script>

{% endhighlight %}

### htmlAttributes `object`

{:#members:htmlattributes}

Specifies the list of HTML attributes to be added to rating control.

#### Default Value

* {}

#### Example

{% highlight html %}

    <input id="rating"></input>

    <script>
        //To set htmlAttributes API value during initialization
        $("#rating").ejRating({ htmlAttributes:{"aria-label":"rating"} });
    </script>

{% endhighlight %}


### incrementStep `number`
{:#members:incrementstep}


Specifies the value to be increased while navigating between shapes(stars) in Rating control.


#### Default Value


* 1


#### Example


{% highlight html %}

    <input id="rating"></input>

    <script>
        //To set incrementStep API value during initialization
        $("#rating").ejRating({ incrementStep: 2 });
    </script>

{% endhighlight %}


### maxValue `number`
{:#members:maxvalue}

Allow to render the maximum number of Rating shape(star).

#### Default Value

* 5

#### Example


{% highlight html %}

    <input id="rating"></input>

    <script>
        //To set maxValue API value during initialization
        $("#rating").ejRating({ maxValue: 10 });
    </script>

{% endhighlight %}




### minValue `number`
{:#members:minvalue}


Allow to render the minimum number of Rating shape(star).


#### Default Value

* 0


#### Example

{% highlight html %}
 
    <input id="rating"></input>

    <script>
        //To set minValue API value during initialization
        $("#rating").ejRating({ minValue: 3 });
    </script>

{% endhighlight %}


### orientation `enum`
{:#members:orientation}


<ts ref="ej.Orientation" />


Specifies the orientation of Rating control. See <a href="global.html#Orientation">Orientation</a>

<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Horizontal</td>
<td class="type">string</td>
<td class="default">horizontal</td>
<td class="description">Used to set Orientation as Horizontal</td>
</tr>
<tr>
<td class="name">
Vertical</td>
<td class="type">string</td>
<td class="default">vertical</td>
<td class="description">Used to set Orientation as Vertical</td>
</tr>
</tbody>
</table>


#### Default Value


* ej.Rating.Orientation.Horizontal


#### Example



{% highlight html %}
 
    <input id="rating"></input>

    <script>
        //To set orientation API value during initialization
        $("#rating").ejRating({ orientation: ej.Rating.Orientation.Horizontal });
    </script> 

{% endhighlight %}




### precision `enum`
{:#members:precision}

<ts name="ej.Rating.Precision" />

Helps to provide more precise ratings.Rating control supports three precision modes - full, half, and exact. See <a href="global.html#Precision">Precision</a>


<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Exact</td>
<td class="type">string</td>
<td class="default">exact</td>
<td class="description">Used to set Precision as Exact</td>
</tr>
<tr>
<td class="name">
Full</td>
<td class="type">string</td>
<td class="default">full</td>
<td class="description">Used to set Precision as Full</td>
</tr>
<tr>
<td class="name">
Half</td>
<td class="type">string</td>
<td class="default">half</td>
<td class="description">Used to set Precision as Half</td>
</tr>
</tbody>
</table>


#### Default Value


* "full"


#### Example


{% highlight html %}

    <input id="rating"></input>

    <script>
        //To set precision API value during initialization
        $("#rating").ejRating({ precision: ej.Rating.Precision.Half });
    </script>

{% endhighlight %}

### readOnly `boolean`
{:#members:readonly}


Interaction with Rating control can be prevented by enabling this API.


#### Default Value


* false


#### Example


{% highlight html %}
 
    <input id="rating"></input>

    <script>
        //To set readOnly API value during initialization
        $("#rating").ejRating({ readOnly: true });
    </script>

{% endhighlight %}

### shapeHeight `number`
{:#members:shapeheight}

To specify the height of each shape in Rating control.

#### Default Value

* 23


#### Example


{% highlight html %}
 
    <input id="rating"></input>

    <script>
        //To set shapeHeight API value during initialization
        $("#rating").ejRating({ shapeHeight: 25 });
    </script>

{% endhighlight %}


### shapeWidth `number`
{:#members:shapewidth}


To specify the width of each shape in Rating control.


#### Default Value


* 23


#### Example

{% highlight html %}
 
    <input id="rating"></input>

    <script>
        //To set shapeWidth API value during initialization
        $("#rating").ejRating({ shapeWidth: 25 });
    </script>

{% endhighlight %}


### showTooltip `boolean`
{:#members:showtooltip}

Enables the tooltip option.Currently selected value will be displayed in tooltip.


#### Default Value


* true


#### Example


{% highlight html %}
 
    <input id="rating"></input>

    <script>
        //To set showTooltip API value during initialization
        $("#rating").ejRating({ showTooltip: true });
    </script>

{% endhighlight %}


### value `number`
{:#members:value}

To specify the number of stars to be selected while rendering.


#### Default Value


* 1

#### Example


{% highlight html %}
 
    <input id="rating"></input>

    <script>
        //To set value API value during initialization
        $("#rating").ejRating({ value: 3 });
    </script>

{% endhighlight %}


### width `string`
{:#members:width}


Specifies the width of the Rating control wrapper.


#### Default Value


* null


#### Example


{% highlight html %}

    <input id="rating"></input>

    <script>
        //To set width API value during initialization
        $("#rating").ejRating({ width: "200" });
    </script>

{% endhighlight %}

## Methods

### destroy()
{:#methods:destroy}

Destroy the Rating widget all events bound will be unbind automatically and bring the control to pre-init state.

#### Example

{% highlight html %}
 
    <input id="rating"></input>

    <script>
        // Create Rating
        $("#rating").ejRating();
        
        // Create Rating Object
        var ratingObj = $("#rating").data("ejRating");
        ratingObj.destroy();
        
    </script>

{% endhighlight %}


{% highlight html %}
 
    <input id="rating"></input>

    <script>
        $("#rating").ejRating();
        // destroy the rating
        $("#rating").ejRating("destroy");
    </script>

{% endhighlight %}

### getValue()
{:#methods:getvalue}

To get the current value of rating control.


#### Returns:
{:#methods:returns:}

number

#### Example


{% highlight html %}
 
    <input id="rating"></input>

    <script>
        // Create rating
        $("#rating").ejRating();
        
        // Create rating object
        var ratingObj = $("#rating").data("ejRating");

        // Get current value of rating
        ratingObj.getValue();

     </script>

{% endhighlight %}


{% highlight html %}
 
    <input id="rating"></input>

    <script>
        $("#rating").ejRating();
        // To get the current value of rating
        $("#rating").ejRating("getValue");
    </script>

{% endhighlight %}




### hide()
{:#methods:hide}




To hide the rating control.



#### Example



{% highlight html %}
 
    <input id="rating"></input>

    <script>
       
        $("#rating").ejRating();
        
        //Create rating object
        var ratingObj = $("#rating").data("ejRating");

        // hides the rating control
        ratingObj.hide(); 
        
    </script>

{% endhighlight %}


{% highlight html %}
 
    <input id="rating"></input>

    <script>
        $("#rating").ejRating();
        // hide the rating control
        $("#rating").ejRating("hide");
    </script>

{% endhighlight %}


### refresh()
{:#methods:refresh}

User can refresh the rating control to identify changes.


#### Example

{% highlight html %}
 
    <input id="rating"></input>

    <script>
        $("#rating").ejRating();
        // Create rating control object
        var ratingObj = $("#rating").data("ejRating");
        // Refresh the rating control
        ratingObj.refresh(); 
    </script>

{% endhighlight %}


{% highlight html %}
 
    <input id="rating"></input>

    <script>
        $("#rating").ejRating();
        // To refresh the rating values
        $("#rating").ejRating("refresh");
    </script>

{% endhighlight %}


### reset()
{:#methods:reset}

To reset the rating value.

#### Example

{% highlight html %}
 
    <input id="rating"></input>

    <script>
        $("#rating").ejRating();
        //  Create the rating object.
        var ratingObj = $("#rating").data("ejRating");
        
        // reset the rating values
        ratingObj.reset(); 
    </script>

{% endhighlight %}


{% highlight html %}
 
    <input id="rating"></input>

    <script>
        $("#rating").ejRating();
        // reset the rating values
        $("#rating").ejRating("reset");
    </script>

{% endhighlight %}

### setValue(value)
{:#methods:setvalue}

To set the rating value.

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
value</td>
<td class="type"><span class="param-type">string|number</span></td>
<td class="description">Specifies the rating value.</td>
</tr>
</tbody>
</table>

#### Example


{% highlight html %}

    <input id="rating"></input>

    <script>
    
        $("#rating").ejRating();
        
        // Create the rating object
        var ratingObj = $("#rating").data("ejRating");
        
        // Set current value of rating
        ratingObj.setValue(4); 
        
    </script>

{% endhighlight %}


{% highlight html %}
 
    <input id="rating"></input>

    <script>
        $("#rating").ejRating();
        // To set the current value of rating
        $("#rating").ejRating("setValue", 4);
    </script>

{% endhighlight %}


### show()
{:#methods:show}

To show the rating control

#### Example


{% highlight html %}
 
    <input id="rating"></input>

    <script>

        $("#rating").ejRating();

        // Create rating object
        var ratingObj = $("#rating").data("ejRating");

        // shows the rating control
        ratingObj.show();

    </script>

{% endhighlight %}


{% highlight html %}
 
    <input id="rating"></input>

    <script>
        $("#rating").ejRating();
        // show the rating control
        $("#rating").ejRating("show");
    </script>

{% endhighlight %}

## Events

### change
{:#events:change}

Fires when Rating value changes.

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
<td class="description">Event parameters from rating
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
value</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns the current value.</td>
</tr>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.Rating.Model"/><span class="param-type">object</span></td>
<td class="description">returns the rating model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
event</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the mouse click event args values.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
    <input id="rating"></input>

    <script>
        //change event for rating
        $("#rating").ejRating({
            change: function (args) { }
        });
    </script>

{% endhighlight %}


### click
{:#events:click}

Fires when Rating control is clicked successfully.

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
<td class="description">Event parameters from rating
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
value</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns the current value.</td>
</tr>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.Rating.Model"/><span class="param-type">object</span></td>
<td class="description">returns the rating model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
event</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the mouse click event args values.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
    <input id="rating"></input>

    <script>
        //click event for rating
        $("#rating").ejRating({
            click: function (args) { }
        });
    </script>

{% endhighlight %}

### create
{:#events:create}

Fires when Rating control is created.

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
<td class="description">Event parameters from rating
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
<td class="type"><ts ref="ej.Rating.Model"/><span class="param-type">object</span></td>
<td class="description">returns the rating model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
    <input id="rating"></input>

    <script>
        //create event for rating
        $("#rating").ejRating({
            create: function (args) { }
        });
    </script>

{% endhighlight %}

### destroy
{:#events:destroy}

Fires when Rating control is destroyed successfully.

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
<td class="description">Event parameters from rating
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
<td class="type"><ts ref="ej.Rating.Model"/><span class="param-type">object</span></td>
<td class="description">returns the rating model</td>
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
 
    <input id="rating"></input>

    <script>
        //destroy event for rating
        $("#rating").ejRating({
            destroy: function (args) { }
        });
    </script>

{% endhighlight %}

### mouseout
{:#events:mouseout}


Fires when mouse hover is removed from Rating control.

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
<td class="description">Event parameters from rating
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
value</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns the current value.</td>
</tr>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.Rating.Model"/><span class="param-type">object</span></td>
<td class="description">returns the rating model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
event</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the mouse click event args values.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
    <input id="rating"></input>

    <script>
        //mouseout event for Rating
        $("#rating").ejRating({
            mouseout: function (args) { }
        });
    </script>

{% endhighlight %}

### mouseover
{:#events:mouseover}

Fires when mouse hovered over the Rating control.

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
<td class="description">Event parameters from rating
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
value</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns the current value.</td>
</tr>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.Rating.Model"/><span class="param-type">object</span></td>
<td class="description">returns the rating model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
event</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the mouse click event args values.</td>
</tr>
<tr>
<td class="name">
index</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the current index value.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
    <input id="rating"></input>

    <script>
        //mouseover event for rating
        $("#rating").ejRating({
            mouseover: function (args) { }
        });
    </script>

{% endhighlight %}




