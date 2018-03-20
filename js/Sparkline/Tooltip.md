---
layout: post
title: Tooltip
description: Learn how to add Tooltip to Sparkline .
platform: js
control: Sparkline
documentation: ug
api: /api/js/ejsparkline
---

## Tooltip  

A [`tooltip`](../api/ejsparkline#members:tooltip) follows the pointer movement and is used to indicate the value of a point. This feature is applicable for line, column, pie, and area Sparkline. You can enable the tooltip by setting it's [`visible`](../api/ejsparkline#members:tooltip-visible) property as **true**.

{% highlight js %}

$("#container").ejSparkline({
            // ...
            tooltip: {
                visible: true,
            },
            // ...
});

{% endhighlight %}

![](/js/Sparkline/Tooltip_images/Tooltip_img1.png)

## Tooltip Customization

You can customize the tooltip [`fill color`](../api/ejsparkline#members:tooltip-fill), [`border`](../api/ejsparkline#members:tooltip-border) properties [`border color`](../api/ejsparkline#members:tooltip-border-color), [`border width`](../api/ejsparkline#members:tooltip-border-width) and [`font`](../api/ejsparkline#members:tooltip-font) properties [`color`](../api/ejsparkline#members:tooltip-font-color), [`font family`](../api/ejsparkline#members:tooltip-font-fontfamily), [`font style`](../api/ejsparkline#members:tooltip-font-fontstyle), [`font weight`](../api/ejsparkline#members:tooltip-font-fontweight), [`opacity`](../api/ejsparkline#members:tooltip-font-opacity), [`size`](../api/ejsparkline#members:tooltip-font-size)

{% highlight js %}

$("#container").ejSparkline({
            // ...
            tooltip: {
                fill: 'red',
                border: {
                    color: "green",
                    width: 3
                },
                font: {
                    size: "12px",
                    fontFamily : "Algerian",
                    fontStyle : "italic",
                    fontWeight : "lighter",
                    opacity : 0.5,
                }
            },
            // ...
});

{% endhighlight %}

![](/js/Sparkline/Tooltip_images/Tooltip_img3.png)

## Tooltip Template   

HTML elements can be displayed in the tooltip by using the [`template`](../api/ejsparkline#members:tooltip-template) option of the tooltip. The template option takes the value of the id attribute of the HTML element. You can use the **#point.x#** and **#point.y#** as place holders in the HTML element to display the x and y values of the corresponding point.

{% highlight js %}

<div id="item" style="display: none;">
    <div>
        <div>#point.x#</div>
        <div>#point.y#</div>
    </div>
</div>
$("#container").ejSparkline({
            // ...
            tooltip: {
                visible: true,
                template: "item",
            },
            // ...
});

{% endhighlight %}

![](/js/Sparkline/Tooltip_images/Tooltip_img2.png)