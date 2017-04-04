---
layout: post
title: Responsive
description: responsive
platform: js
control: TreeGrid
documentation: ug
---
# Responsive

The TreeGrid control has support for responsive behavior based on client browser's width and height. To enable responsive support in TreeGrid, `isResponsive` property should be true.

Please find the example describes the above behavior.

{% highlight html %}
<div id="TreeGridContainer"/>
{% endhighlight %}

{% highlight js %}
$("#TreeGridContainer").ejTreeGrid({
    //...
    isResponsive: true,
});
{% endhighlight %}

The following output is displayed as a result of the above code example

![](Responsive/adaptive-mob.png)
{:caption}
Responsive TreeGrid in Mobile layout.

![](Responsive/adaptive.png)
{:caption}
Responsive TreeGrid in tablet layout.

## Layout

There are three modes of responsive layout is available in TreeGrid based on client width. They are.

* Mobile(<321px)
* Tablet(321px to 768px)
* Desktop(>768px)

## Mobile Layout

The customized layout for filtering, column chooser operations and add/edit operations in mobile device can be seen following screen shots.

![](Responsive/adaptive-mob-filter.png)
{:caption}
filtering in mobile layout.

![](Responsive/adaptive-mob-edit.png)
{:caption}
Add/edit in mobile layout

![](Responsive/adaptive-mob-colchooser.png)
{:caption}
Column chooser in mobile layout

![](Responsive/adaptive-mob-insert.png)
{:caption}
Insert column options in mobile layout

## Tablet Layout

The customized layout for filtering, column chooser operations and add/edit operations in tablet device can be seen following screen shots.

![](Responsive/adaptive-filter.png)
{:caption}
filtering in tablet layout.

![](Responsive/adaptive-edit.png)
{:caption}
Add/edit in tablet layout

![](Responsive/adaptive-colchooser.png)
{:caption}
Column chooser in tablet layout

![](Responsive/adaptive-insert.png)
{:caption}
Insert column options in tablet layout

## Public Method

You can change the minimum responsive width dynamically by using public method called `updateResponsiveMinWidth(width)` by passing the width as an argument.
The TreeGrid control get works in responsive mode only when the window width is below the minimum responsive width.

Please find the example describes the above behavior.

{% highlight html %}
<div id="TreeGridContainer"/>
<button id="minResponsiveWidth">minResponsiveWidth</button>
{% endhighlight %}

{% highlight js %}
$("#TreeGridContainer").ejTreeGrid({
    //...
    isResponsive: true,
});
{% endhighlight %}

{% highlight js %}
<script>

$("#minResponsiveWidth").click(function (args) {
                treegridObj = $("# TreeGridContainer ").data("ejTreeGrid");
                treegridObj.updateResponsiveMinWidth(600);
            })

</script>
{% endhighlight %}

The following output is displayed as a result of the above code example

![](Responsive/adaptive-publicmethod.png)