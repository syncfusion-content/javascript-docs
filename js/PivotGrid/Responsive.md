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

{% highlight js %}

$(function() {
    $("#PivotGrid1").ejPivotGrid({
        url: "../wcf/PivotGridService.svc",
        isResponsive: true
    });
});

{% endhighlight %}

![](Responsive_images/normal.png)

_Normal PivotGrid_

![](Responsive_images/responsive.png)

_Responsive PivotGrid_

![](Responsive_images/res-schema.png)

_Responsive PivotTable Field List - Collapsed_

![](Responsive_images/res-schema1.png)

_Responsive PivotTable Field List - Expanded_
