---
layout: post
title: Customization for Essential JavaScript Sparkline
description: Learn how to customize the Sparkline .
platform: js
control: Sparkline
documentation: ug
api: /api/js/ejsparkline
---

# Sparkline Customization

This section explains you the customization options available to make changes in the Sparkline for getting better appearance.

## Sparkline background

You can specify the background color for the Sparkline using [`background`](../api/ejsparkline#members:background) property. When you don't specify the [`background`](../api/ejsparkline#members:background), it takes "transparent" as background color. 

{% highlight javascript %}

$("#container").ejSparkline({
            // ...
            //Specifies background color for sparkline
            background : "gray"
            // ...
});

{% endhighlight %} 

![](/js/Sparkline/Sparkline-Customization_images/Sparkline-Customization_img1.png)

## Stroke color and width

You can customize the series border color and width using [`stroke`](../api/ejsparkline#members:stroke) and [`width`](../api/ejsparkline#members:width). This is applicable for Sparkline types line and area.

{% highlight javascript %}

$("#container").ejSparkline({
            // ...
            //Specifies border color and width for line and area series
            stroke: "green",
            width: 3
            // ...
});

{% endhighlight %} 

![](/js/Sparkline/Sparkline-Customization_images/Sparkline-Customization_img2.png)

## Sparkline border

You can customize the [`border`](../api/ejsparkline#members:border) width and height of the Sparkline using [`border width`](../api/ejsparkline#members:border-color) and [`border height`](../api/ejsparkline#members:border-width) properties. This is applicable for column, win-loss and pie series.

{% highlight javascript %}

$("#container").ejSparkline({
            // ...
            //Specifies border width and color for column, winLoss and pie series
            border: { color: "green", width: 2 },
            // ...
});

{% endhighlight %} 

![](/js/Sparkline/Sparkline-Customization_images/Sparkline-Customization_img3.png)

## Opacity

By default [`opacity`](../api/ejsparkline#members:opacity) of the Sparkline is 1. You can specify the opacity value from 0 to 1. This is applicable for all types of series. 

{% highlight javascript %}

$("#container").ejSparkline({
            // ...
            //Specifies the opacity of the sparkline
            opacity: 0.5
            // ...
});

{% endhighlight %} 

![](/js/Sparkline/Sparkline-Customization_images/Sparkline-Customization_img4.png)

## Localization

Sparkline is having support for localization as well. Default culture is "en-US". You can modify the culture using the property [`locale`](../api/ejsparkline#members:locale).

**Enable Group Separator** is used to Convert the date object to string while using the locale settings, you can set [`enableGroupSeparator`](../api/ejsparkline#members:enablegroupseparator) property as **true**.

{% highlight javascript %}

$("#container").ejSparkline({
            // ...
            //Culture for the sparkline
            locale: "fr-FR",
            enableGroupSeparator: true
            // ...
});

{% endhighlight %} 

## Padding for Sparkline

[`Padding`](../api/ejsparkline#members:padding) is used to specify the padding value between the container and Sparkline. By default padding value of the Sparkline is 5. 

{% highlight javascript %}

$("#container").ejSparkline({
            // ...
            //Padding for the sparkline
            padding: 20,
            // ...
});

{% endhighlight %} 

![](/js/Sparkline/Sparkline-Customization_images/Sparkline-Customization_img5.png)

## Canvas support

You can control whether Sparkline has to be rendered as SVG or [`Canvas`](../api/ejsparkline#members:enablecanvasrendering). Canvas rendering supports all the functionalities supported in SVG rendering.

{% highlight javascript %}

$("#container").ejSparkline({
            // ...
            //enables canvas rendering
            enableCanvasRendering : true
            // ...
});

{% endhighlight %} 

## Themes

You can specify different [`themes`](../api/ejsparkline#members:theme) for Sparkline control.

{% highlight javascript %}

$("#container").ejSparkline({
            // ...
            //theme for sparkline
            theme:"flatdark",
            // ...
});

{% endhighlight %} 

![](/js/Sparkline/Sparkline-Customization_images/Sparkline-Customization_img6.png)