---
layout: post
title: Customization in Tooltip widget for Syncfusion Essential JS
description: Customization in Tooltip widget for Syncfusion Essential JS
platform: js
control: Tooltip
documentation: ug
keywords : ejTooltip, Tooltip, js Tooltip, Tooltip widget, Tooltip template,
api: /api/js/ejtooltip
---

# Customization

## Template Support

By default you can add any text or image to the Tooltip. To customize the tooltip layout or to create your own visualized elements you can use this template support.

{% highlight html %}

<div class="ctrl" id="centerImg">
    <img class="ctrImg" src="http://js.syncfusion.com/demos/web/images/tooltip/template-04.png" />
    <div class="new">Roslyn Succinctly</div>
</div>
<script type="text/javascript">
    $("#centerImg").ejTooltip(
    {
        width: "350px",
        content: '<div class="main"> <div class="poster"> <img src="http://js.syncfusion.com/demos/web/images/tooltip/template-2.png" width="150px" height="120px"> </div> <div class="def"> <h4> Roslyn Succinctly </h4><div class="description">Microsoft has only recently embraced the world of open source software, offering <a href="#">More...</a> </div>'
    });
</script>
<style>
    h4 {
        margin-top: 0px;
        margin-bottom: 2px;
    }
    .e-tooltip-wrap .e-tipContainer .e-tipcontent {
        padding: 5px 0px;
    }
    .poster {
        float: left;
        padding: 4px 0px;
    }
    .new {
        text-align: center;
    }
    .def {
        float: right;
    }
    .ctrl {
        border: 1px solid #ebebe0;
        width: 150px;
        padding: 5px;
        height: 180px;
        margin-top: 239px;
        margin-left: 250px;
    }
    .ctrImg {
        width: 150px;
        height: 160px;
    }
    .category {
        margin-left: 10px;
    }
    .description {
        width: 200px;
        height: 60px;
        line-height: 22px;
        margin-top: 10px;
    }
</style>
    
{% endhighlight %}

![](Customization_images/template.png)

### Tooltip’s title customization

Tooltip title using [title](https://help.syncfusion.com/api/js/ejtooltip#members:title) can be customized with the image or any HTML element. 

{% highlight html %}
    
<div class="ctrl" id="centerImg">
    <img class="ctrImg" src="http://js.syncfusion.com/demos/web/images/tooltip/template-04.png" />
    <div class="new">Roslyn Succinctly</div>
</div>
<script type="text/javascript">
    $("#centerImg").ejTooltip(
    {
        title : '<div><img class="titleImg" src="http://js.syncfusion.com/demos/web/images/tooltip/template-2.png" /> <div class="description"> Roslyn Succinctly </div> </div> ',
        content: '<div>Microsoft has only recently embraced the world of open source software, offering <a href="#">More...</a> </div>'
    });
</script>
<style>
    .titleImg {
        width: 20px;
        height: 20px;
        float: left;
        margin-right: 10px;
    }
    #centerImg{
        margin-left : 300px;
        margin-top : 250px;
        position : absolute;
        border: 1px solid grey;
    }
    .description {
        height: 20px;
    }
</style>

{% endhighlight %}

![](Customization_images/title.png)

## Animation Effects

Determines the type of effect that takes place when showing/hiding the tooltip.

We can specify the effect and the duration for the animation using [animation](https://help.syncfusion.com/api/js/ejtooltip#members:animation) property. 

<table>
<tr>
<td>
Effects<br/></td><td>
Description<br/></td></tr>
<tr>
<td>
Slide<br/></td><td>
Sliding animation effect takes place with a duration of 200ms.<br/></td></tr>
<tr>
<td>
Fade<br/></td><td>
Fading animation effect takes place with a duration of 800ms.<br/></td></tr>
<tr>
<td>
None (Default)<br/></td><td>
No effect takes place<br/></td></tr>
</table>

Let's create a Tooltip that slides down when shown using the [animation](https://help.syncfusion.com/api/js/ejtooltip#members:animation) property:

{% highlight html %}

<div class="control">
    TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
</div>

// Creates the Tooltip
<script>
    $("#test").ejTooltip(
    {
        content: "JavaScript is the programming language of HTML and the Web.",
        animation : { effect : "slide", speed :  1000 }
    });
</script>

{% endhighlight %}

### Custom Animation

Custom animation effect for both Tooltip show/hide can also be done by [show](https://help.syncfusion.com/api/js/ejtooltip#methods:show) and [hide](https://help.syncfusion.com/api/js/ejtooltip#methods:hide) method.

Show or Hide method may receive an optional 'callback' parameter, which represents a function you'd like to call which will animate the tooltip.

 
{% highlight html %}

<div class="control">
    TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
</div>
<button id="open">Open</button>

// Creates the Tooltip
<script>

    $("#test").ejTooltip(
    {
        content: "JavaScript is the programming language of HTML and the Web."
    });
    $("#open").ejButton({
        size: "large",
        showRoundedCorner: true,
        click: "onClick",
    });
    function onClick(args){
        tip = $("#test").data("ejTooltip");
        tip.show(null,"myFunc");
    }
    function myFunc(args) {
        tip = $("#test").data("ejTooltip");
        $(tip.tooltip).slideDown(200, "easeOutElastic");
    }
    
</script>

{% endhighlight %}

N> Show or Hide method can also receive an optional parameter “effect name”, (e.g any easing effect name) which specifies the type of effect taken place when showing/hiding of the tooltip, please refer to the following link for online demo - [link](http://jsplayground.syncfusion.com/Sync_sz1250aa).

## Modernize the tooltip’s content

It's easy to update a tooltip’s content – whether it’s open or closed.

{% highlight html %}

<div class="control">
    TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
    <button id="open">Update Content</button>
</div>

<script type="text/javascript">
    $(function (){
        $("#test").ejTooltip(
        {
            content: "JavaScript is the programming language of HTML and the Web."
        });
        $("#open").ejButton({
            size: "large",
            showRoundedCorner: true,
            click: "onClick"
        });
    });
    function onClick(args){
        tip = $("#test").data("ejTooltip");
        tip.setModel({ content: "JavaScript" });
        tip.show();
    }
</script>
    
{% endhighlight %}

## Closing Mode

By default, the Tooltip will be hidden when mouse leaves the target element. Different types of [close mode](https://help.syncfusion.com/api/js/ejtooltip#members:closemode) as follows 

<table>
<tr>
<td>
Types<br/></td><td>
Description<br/></td></tr>
<tr>
<td>
Auto<br/></td><td>
Tooltip will be hidden after a particular period of time.<br/></td></tr>
<tr>
<td>
Sticky<br/></td><td>
Tooltip rendered with the button, it will close the tooltip.<br/></td></tr>
<tr>
<td>
None (Default)<br/></td><td>
Tooltip will be hidden when mouse leaves the target element.<br/></td></tr>
</table>

### Auto

The tooltip will be visible only for the period of time specified in the [autoCloseTimeout](https://help.syncfusion.com/api/js/ejtooltip#members:autoclosetimeout).

Let see an example, this Tooltip will only hide after hovering the target for 2000ms

{% highlight html %}

<div class="control">
    TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
</div>

// Creates the Tooltip
<script>
    $("#test").ejTooltip(
    {
        content: "JavaScript is the programming language of HTML and the Web.",
        closeMode : "auto",
        autoCloseTimeout : 2000
    });
</script>
    
{% endhighlight %}

N> Time specified in the autoCloseTimeout will be in milliseconds and the default value is 4000ms

### Sticky

A close button will be shown with the Tooltip. The button element (i.e. close button) located by default at the top right of the Tooltip or title bar (if title is enabled). The tooltip gets closed when the button is clicked.

{% highlight html %}

<div class="control">
    TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
</div>

// Creates the Tooltip
<script>
    $("#test").ejTooltip(
    {
        content: "JavaScript is the programming language of HTML and the Web.",
        width : "200px",
        closeMode : "sticky"
    });
</script>

{% endhighlight %}

![](ClosingBehaviour_images/sticky.png)

You can also have Tooltip with a title, in which case the button will lye within it:

{% highlight html %}

<div class="control">
    TypeScript lets you write <a id="test"><u> JavaScript</u> </a>the way you really want to.
</div>

// Creates the Tooltip
<script>
    $("#test").ejTooltip(
    {
        content: "JavaScript is the programming language of HTML and the Web.",
        width : "200px",
        title : "JavaScript",
        closeMode : "sticky"
    });
</script>

{% endhighlight %}

![](ClosingBehaviour_images/title.png)

    
