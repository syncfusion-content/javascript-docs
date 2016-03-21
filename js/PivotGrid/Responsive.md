---
layout: post
title: Responsive
description: responsive
platform: js
control: PivotGrid
documentation: ug
---

#Responsive
PivotGrid and PivotTable Field list control supports responsive rendering based on the target device (desktop & tablet) resolution. It supports resolution upto 1024x600. You can enable responsiveness in PivotGrid by setting [`isResponsive`](/js/api/ejpivotgrid#members:isresponsive) property to true. 

On resizing the browser, the PivotTable Field list will get collapse and an icon will appear on the left-hand side of the browser. User can toggle its view and perform UI interaction.

{% highlight javascript %}

$(function() {
    $("#PivotGrid1").ejPivotGrid({
        url: "../wcf/PivotGridService.svc",
        isResponsive: true
    });
});

{% endhighlight %}

![](Responsive_images/normal.png)

Normal PivotGrid
{:.caption}

![](Responsive_images/responsive.png)

Responsive PivotGrid
{:.caption}

![](Responsive_images/res-schema.png)

Responsive PivotTable Field List - Collapsed
{:.caption}

![](Responsive_images/res-schema1.png)

Responsive PivotTable Field List - Expanded
{:.caption}