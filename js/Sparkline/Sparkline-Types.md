---
layout: post
title: Sparkline types
description: What are the different types of Sparkline available in Essential JavaScript Chart.
platform: js
control: Sparkline
documentation: ug
api: /api/js/ejsparkline
---

# Sparkline Types

## Line Type

To render a Line type Sparkline, set the [`type`](../api/ejsparkline#members:type) as **line**. To change the color and width of the line, you can use the [`fill`](../api/ejsparkline#members:fill) and [`width`](../api/ejsparkline#members:width) property.	

{% highlight javascript %}

$("#container").ejSparkline({
            // ...
            width: 3,
            fill: "#33ccff", 
            // ...
        });

{% endhighlight %}

![](/js/Sparkline/Sparkline-Types_images/Sparkline-Types_img1.png)

## Column Type

To render a Column Sparkline, set the type as **column** To change the color of the column, you can use the [`fill`](../api/ejsparkline#members:fill) property.

{% highlight javascript %}

$("#container").ejSparkline({
            // ...
            type: 'column',
            fill: "#33ccff",
            // ...
        });

{% endhighlight %}

![](/js/Sparkline/Sparkline-Types_images/Sparkline-Types_img2.png)

## Area Type

To render an Area Sparkline, you can specify the type as **area**. To change the Area color, you can use the [`fill`](../api/ejsparkline#members:fill) property

{% highlight javascript %}

$("#container").ejSparkline({
            // ...
            type: 'area',
            fill: '#69D2E7'
            // ...
        });

{% endhighlight %}

![](/js/Sparkline/Sparkline-Types_images/Sparkline-Types_img3.png)

## WinLoss Type

WinLoss Sparkline render as a column segment and it show the positive, negative and neutral values. You can customize the positive and negative color of the win-loss type.

{% highlight javascript %}

$("#container").ejSparkline({
            // ...
            type: 'winLoss',
            fill: '#69D2E7'
            // ...
        });

{% endhighlight %}

![](/js/Sparkline/Sparkline-Types_images/Sparkline-Types_img4.png)

## Pie Type

You can create a pie type sparkline by setting the type as **pie**. Colors for the pie can be customize using [`palette`](../api/ejsparkline#members:palette) property.

{% highlight javascript %}

$("#container").ejSparkline({
            // ...
            type: 'pie',
            palette: ['#ff3399', "#33ccff"],
            // ...
        });

{% endhighlight %}

![](/js/Sparkline/Sparkline-Types_images/Sparkline-Types_img5.png)
