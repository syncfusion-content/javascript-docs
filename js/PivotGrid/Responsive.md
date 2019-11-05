---
layout: post
title: Responsive with PivotGrid widget for Syncfusion Essential JS
description: This document illustrates that how to enable responsive layout rendering in JavaScript PivotGrid control
platform: js
control: PivotGrid
documentation: ug
api: /api/js/ejpivotgrid
---

# Responsive

PivotGrid and PivotTable field list control supports responsive rendering based on the target device (desktop and tablet) resolution. It supports resolution upto 1024x600. You can enable the responsiveness in PivotGrid by setting the [`isResponsive`](/api/js/ejpivotgrid#members:isresponsive) property to true.

On resizing the browser, the PivotTable field list will get collapse and an icon will appear on the left-hand side of the browser. You can toggle its view and perform the UI interaction.

{% highlight js %}

$(function() {
    $("#PivotGrid1").ejPivotGrid({
        url: "/OLAPService",
        isResponsive: true
    });
});

{% endhighlight %}

![JavaScript pivot grid control with normal layout](Responsive_images/normal.png)

_Normal PivotGrid_
{:.caption}

![JavaScript pivot grid control with responsive layout](Responsive_images/responsive.png)

_Responsive PivotGrid_
{:.caption}

![JavaScript pivot table field list in collapsed state](Responsive_images/res-schema.png)

_Responsive PivotTable Field List - Collapsed_
{:.caption}

![JavaScript pivot table field list in expanded state](Responsive_images/res-schema1.png)

_Responsive PivotTable Field List - Expanded_
{:.caption}

