---
layout: post
title: Properties,Methods and Events of Essential JS ejSignature Widget
description: Methods, members, events available in ejSignature
documentation: API
platform: js
keywords: ejSignature, API, Essential JS Signature 
---

# ejSignature

The ejSignature is a JavaScript Plugin used to capture or drawing the smooth signatures, it captures signature as vector outlines of strokes. 
Using ejSignature we can customize the background, stroke width and stroke color and also convert captured signature to an image format. 

#### Syntax

{% highlight javascript %}
		
	$(element).ejSignature()

{% endhighlight %}

#### Example

{% highlight html %}
		
	<div id="signature"></div> 
	<script> 
	// Create signature 
	$('#signature').ejSignature({ 
		
	}); 
	</script>

{% endhighlight %}

#### Requires

* module:jQuery

* module:ej.core.js

* module:ej.signature.js

* module:ej.touch.js


## Members

### backgroundColor `string`
{:#members:backgroundColor}

This property is used to set the background color for the signature.  

#### Default Value: 

* "#ffffff"

#### Example 

{% highlight javascript %}

	$("#signature").ejSignature({ 
		backgroundColor: "yellow" 
	});

{% endhighlight %}

### backgroundImage `string`
{:#members:backgroundImage}

This property is used to set the background image for the signature.  

#### Example 

{% highlight javascript %}

	$("#signature").ejSignature({ 
		backgroundImage: "image.jpg" 
	});

{% endhighlight %}

### enabled `Boolean`
{:#members:enabled}

Enables or disables the **Signature** textbox widget.

#### Default Value: 

* true

#### Example 

{% highlight javascript %}

	$("#signature").ejSignature({
		enabled: false
	});

{% endhighlight %}
 
### height `string`
{:#members:height}

Sets the height of the Signature control.

#### Default Value:  

* "100%"

#### Example  

{% highlight javascript %}

	$("#signature").ejSignature({
		height: "400px"
	});

{% endhighlight %}
 
### isResponsive `Boolean`
{:#members:isResponsive}

 Enables/disables responsive support for the signature control (i.e) maintain the signature drawing during the window resizing time.

#### Default Value:

* false

#### Example  

{% highlight javascript %}

		$("#signature").ejSignature({
		isResponsive: true
	});

{% endhighlight %}
 
### saveImageFormat `Enum`
{:#members:saveImageFormat}

Allows the type of the image format to be saved when the signature image is saved.

#### Example  

{% highlight javascript %}

		$("#signature").ejSignature({
		saveImageFormat:ej.SaveImageFormat.jpg
	});

{% endhighlight %}


### saveWithBackground `Boolean`
{:#members:saveWithBackground}

Allows the signature image to be saved along with its background.

#### Default Value:  

* false
#### Example  

{% highlight javascript %}

		$("#signature").ejSignature({
		saveWithBackground:true,
		backgroundImage: "image.jpg" 

	});

{% endhighlight %}
 
### showRoundedCorner `Boolean`
{:#members:showRoundedCorner}

Enables or disables rounded corner.

#### Default Value:  

* true

#### Example  

{% highlight javascript %}

		$("#signature").ejSignature({
		showRoundedCorner: false 
	});

{% endhighlight %}
 
### strokeColor `string`
{:#members:strokeColor} 

Sets the stroke color for the stroke of the signature.

#### Default Value:  

* "#000000"

#### Example  

{% highlight javascript %}

		$("#signature").ejSignature({
		strokeColor: "blue" 
	});

{% endhighlight %}
 

### strokeWidth `Number`
{:#members:strokeMaxWidth} 

Sets the stroke width for the stroke of the signature.

#### Default Value:  

* 2

#### Example  

{% highlight javascript %}

		$("#signature").ejSignature({
		strokeWidth: 3 
	});

{% endhighlight %}
 
 
### width `string`
{:#members:width} 

Sets the width of the Signature control.

#### Default Value:  

* "100%"

#### Example  

{% highlight javascript %}

	$("#signature").ejSignature({
		height: "600px"
	});

{% endhighlight %}


## Methods

### clear()
{:#methods:clear}

Clears the strokes in the signature.

N> This method does not accept any arguments.

#### Example  

{% highlight javascript %}

	$("#signature").ejSignature("clearText");

{% endhighlight %}

### destroy()
{:#methods:destroy}

Destroys the signature widget.

N> This method does not accept any arguments.

#### Example  

{% highlight javascript %}

	$("#signature").ejSignature("destroy");

{% endhighlight %}

### disable()
{:#methods:disable}

Disables the signature widget.

N> This method does not accept any arguments.

#### Example  

{% highlight javascript %}

	$("#signature").ejSignature("disable");

{% endhighlight %}

### enable()
{:#methods:enable}

Enables the signature widget.

N> This method does not accept any arguments.

#### Example  

{% highlight javascript %}

	$("#signature").ejSignature("enable");

{% endhighlight %}

### hide()
{:#methods:hide}

Hides the signature widget.

N> This method does not accept any arguments.

#### Example  

{% highlight javascript %}

	$("#signature").ejSignature("hide");

{% endhighlight %}
            
### redo()
{:#methods:redo}

redo the last drawn stroke of the signature

N> This method does not accept any arguments.

#### Example  

{% highlight javascript %}

	$("#signature").ejSignature("redo");

{% endhighlight %}

### save()
{:#methods:save}

used to save the drawn image.

N> This method does not accept any arguments.

#### Example  

{% highlight javascript %}

	$("#signature").ejSignature("save");

{% endhighlight %}

### show()
{:#methods:show}

Used to Show the signature widget, if it is already hided. 

N> This method does not accept any arguments.

#### Example  

{% highlight javascript %}

	$("#signature").ejSignature("show");

{% endhighlight %}

### undo()
{:#methods:undo}

undo the last drawn stroke of the signature.

N> This method does not accept any arguments.

#### Example  

{% highlight javascript %}

	$("#signature").ejSignature("undo");

{% endhighlight %}

## Events

### change
{:#events:change}

Triggers when the stroke is changed.

<table>
<tr>
<th>Name<br/><br/></th>
<th>Type<br/><br/></th>
<th>Description<br/><br/></th>
</tr>
<tr>
<td>cancel<br/><br/></td>
<td>Boolean<br/><br/></td>
<td>Set this option to true to cancel the event.<br/><br/></td>
</tr>
<tr>
<td>model<br/><br/></td>
<td><ts ref="ej.Signature.Model"/>Object<br/><br/></td>
<td>Instance of the signature model object.<br/><br/></td>
</tr>
<tr>
<td>type<br/><br/></td>
<td>String<br/><br/></td>
<td>Name of the event.<br/><br/></td>
</tr>
<tr>
<td>lastImage<br/><br/></td>
<td>String<br/><br/></td>
<td>Gives the last stored image<br/><br/></td>
</tr>
</table>

#### Example  

{% highlight javascript %}

	$("#signature").ejSignature({
		change: function (argument) {
			//do something
		}
	}); 

{% endhighlight %}

### mousedown
{:#events:mousedown}
Triggerd when the pointer is clicked or touched in the signature canvas.
<table>
<tr>
<th>Name<br/><br/></th>
<th>Type<br/><br/></th>
<th>Description<br/><br/></th>
</tr>
<tr>
<td>cancel<br/><br/></td>
<td>Boolean<br/><br/></td>
<td>Set this option to true to cancel the event.<br/><br/></td>
</tr>
<tr>
<td>model<br/><br/></td>
<td><ts ref="ej.Signature.Model"/>Object<br/><br/></td>
<td>Instance of the signature model object.<br/><br/></td>
</tr>
<tr>
<td>type<br/><br/></td>
<td>String<br/><br/></td>
<td>Name of the event.<br/><br/></td>
</tr>
<tr>
<td>value<br/><br/></td>
<td>object<br/><br/></td>
<td>returns all the event values<br/><br/></td>
</tr>
</table>
#### Example  

{% highlight javascript %}

	$("#signature").ejSignature({
		mousedown: function (argument) {
			//do something
		}
	}); 

{% endhighlight %}

### mousemove
{:#events:mousemove}
Triggerd when the pointer is moved in the signature canvas.
<table>
<tr>
<th>Name<br/><br/></th>
<th>Type<br/><br/></th>
<th>Description<br/><br/></th>
</tr>
<tr>
<td>cancel<br/><br/></td>
<td>Boolean<br/><br/></td>
<td>Set this option to true to cancel the event.<br/><br/></td>
</tr>
<tr>
<td>model<br/><br/></td>
<td><ts ref="ej.Signature.Model"/>Object<br/><br/></td>
<td>Instance of the signature model object.<br/><br/></td>
</tr>
<tr>
<td>type<br/><br/></td>
<td>String<br/><br/></td>
<td>Name of the event.<br/><br/></td>
</tr>
<tr>
<td>value<br/><br/></td>
<td>object<br/><br/></td>
<td>returns all the event values<br/><br/></td>
</tr>
</table>

#### Example  

{% highlight javascript %}

	$("#signature").ejSignature({
		mousemove: function (argument) {
			//do something
		}
	}); 

{% endhighlight %}


### mouseup
{:#events:mouseup}
Triggerd when the pointer is released after click or touch in the signature canvas.
<table>
<tr>
<th>Name<br/><br/></th>
<th>Type<br/><br/></th>
<th>Description<br/><br/></th>
</tr>
<tr>
<td>cancel<br/><br/></td>
<td>Boolean<br/><br/></td>
<td>Set this option to true to cancel the event.<br/><br/></td>
</tr>
<tr>
<td>model<br/><br/></td>
<td><ts ref="ej.Signature.Model"/>Object<br/><br/></td>
<td>Instance of the signature model object.<br/><br/></td>
</tr>
<tr>
<td>type<br/><br/></td>
<td>String<br/><br/></td>
<td>Name of the event.<br/><br/></td>
</tr>
<tr>
<td>value<br/><br/></td>
<td>object<br/><br/></td>
<td>returns all the event values<br/><br/></td>
</tr>
</table>

#### Example  

{% highlight javascript %}

	$("#signature").ejSignature({
		mouseup: function (argument) {
			//do something
		}
	}); 

{% endhighlight %}


