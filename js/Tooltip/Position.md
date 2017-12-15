---
layout: post
title: Position attribute in Tooltip widget for Syncfusion Essential JS
description: Positionining support to Tooltip widget for Syncfusion Essential JS
platform: js
control: Tooltip
documentation: ug
keywords : ejTooltip, Tooltip, js Tooltip, Tooltip widget, Tooltip position, Tooltip collision
api: /api/js/ejtooltip
---

# Position

The position object defines various attributes of the Tooltip position, including the element it is positioned in relation to, and how the position is adjusted within the defined container.

Lets position using [position](https://help.syncfusion.com/api/js/ejtooltip#members:position) the Tooltips (stems) left center corner at the right center of the target element.

{% highlight html %}
 
<div class="img" id="sample">
    <a target="_blank" href="image/taj.png">
        <img src="http://js.syncfusion.com/demos/web/images/tooltip/template-05.png" alt="Delphi">
    </a>
    <div class="desc">Delphi Succinctly</div>
</div>

// Creates the Tooltip
<script>
    $("#sample").ejTooltip({
        content: "Learn the fundamentals of Delphi to build a variety of solutions for many devices and platforms.",
        position : {
            stem : {horizontal :"left", vertical : "center"},
            target :{horizontal: "right", vertical: "center"}
            }
    });
</script>
    
{% endhighlight %}

Apply the following styles to show the Tooltip.

{% highlight html %}

<style>
    div.img {
        border: 1px solid #ccc;
        float: left;
        box-sizing: border-box;
        height: 200px;
        width: 146px;
    }
    div.img img{
        width: 100%;
        height: 166px;
    }
    div.desc {
        padding: 6px;
        text-align: center;
    }
</style>
    
{% endhighlight %}

![](Position_images/position.png)

N> By default, the Tooltips "center bottom" corner is placed at the center top of the target element.

## Containment 

Determines the HTML element in which the Tooltip is appended to e.g. its containing element using [containment](https://help.syncfusion.com/api/js/ejtooltip#members:containment) property and The tooltip will be restricted to move only within the specified container element.

Let's append our Tooltip to a custom 'frame' container:

{% highlight html %}
 
<div class="frame">
    <div class="control">
        TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>
</div>

// Creates the Tooltip
<script>
    $("#test").ejTooltip(
    {
        content: "JavaScript is the programming language of HTML and the Web.",
        containment: ".frame"
    });
</script>
    
{% endhighlight %}

N> By default all Tooltips are appended to the document.body element.

## Associates 

 The Tooltip will be positioned in relation to target element. Can also be set to 'mouse' or the window, or an absolute x/y position on the page.
 
 Let's position the Tooltip in relation to the 'a' element inside the div element:
 
 {% highlight html %}
 
<div class="frame">
    <div class="control">
        TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>
</div>

// Creates the Tooltip
<script>
    $("#test").ejTooltip(
    {
        content: "JavaScript is the programming language of HTML and the Web."
    });
</script>
    
{% endhighlight %}
 
We can also position the Tooltip in relation to the mouse using [associate](https://help.syncfusion.com/api/js/ejtooltip#members:associate) property.
 
{% highlight html %}
 
<div class="frame">
    <div class="control">
        TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>
</div>

// Creates the Tooltip
<script>
    $("#test").ejTooltip(
    {
        content: "JavaScript is the programming language of HTML and the Web.",
        associate : "mousefollow"
    });
</script>
    
{% endhighlight %}

Position the tooltip at the current mouse position, once enter to the target element as follows

{% highlight html %}
 
<div class="frame">
    <div class="control">
        TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>
</div>

// Creates the Tooltip
<script>
    $("#test").ejTooltip(
    {
        content: "JavaScript is the programming language of HTML and the Web.",
        associate : "mouseenter"
    });
</script>
    
{% endhighlight %}


It also possible to place the tooltip relation to the window as follows

{% highlight html %}
 
<div class="frame">
    <div class="control">
        TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>
</div>

// Creates the Tooltip
<script>
    $("#test").ejTooltip(
    {
        content: "JavaScript is the programming language of HTML and the Web.",
        associate : "window",
        position : {
            target : {horizontal : "right", vertical: "bottom"}
        }
    });
</script>
    
{% endhighlight %}
    
And last but not least, absolute positioning via X,Y co-ordinates e.g. a Tooltip at 10px from left and top of the page:

{% highlight html %}
 
<div class="frame">
    <div class="control">
        TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>
</div>

// Creates the Tooltip
<script>
    $("#test").ejTooltip(
    {
        content: "JavaScript is the programming language of HTML and the Web.",
        associate : "axis",
        position : {
            target : {horizontal : 10, vertical: 10}
        }
    });
</script>
    
{% endhighlight %}

## Collision 

When the positioned element overflows the window in some direction, move it to an alternative position using [collision](https://help.syncfusion.com/api/js/ejtooltip#members:collision) property.

The following values determines the kind of positioning that takes place.

<table>
<tr>
<td>
Value<br/></td><td>
Description<br/></td></tr>
<tr>
<td>
Flip<br/></td><td>
Flips the element to the opposite side of the target if the collision detected.<br/></td></tr>
<tr>
<td>
Fit<br/></td><td>
Shift the element away from the edge of the window.<br/></td></tr>
<tr>
<td>
FlipFit(Default)<br/></td><td>
Ensure as much of the element is visible as possible to showcase.<br/></td></tr>
<tr>
<td>
None<br/></td><td>
Does not apply any collision detection.<br/></td></tr>
</table>

{% highlight html %}
 
<div class="frame">
    <div class="control">
        TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    </div>
</div>

// Creates the Tooltip
<script>
    $("#test").ejTooltip(
    {
        content: "JavaScript is the programming language of HTML and the Web.",
        collision : "fit"
    });
</script>
    
{% endhighlight %}