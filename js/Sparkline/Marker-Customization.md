---
layout: post
title: Markers Customization
description: Learn how to add markers to Sparkline.
platform: js
control: Sparkline
documentation: ug
api: /api/js/ejsparkline
---

## Marker Customization

You can customize markers by initializing the [`markerSettings`](../api/ejsparkline#members:markersettings) property. The customization options allow you to change the [`visibility`](../api/ejsparkline#members:markersettings-visible), [`fill`](../api/ejsparkline#members:markersettings-fill), [`width`](../api/ejsparkline#members:markersettings-width), [`opacity`](../api/ejsparkline#members:markersettings-opacity)and [`border`](../api/ejsparkline#members:markersettings-border) options[`color`](../api/ejsparkline#members:markersettings-border-color), [`width`](../api/ejsparkline#members:markersettings-border-width), [`opacity`](../api/ejsparkline#members:markersettings-border-opacity) for marker. This customization only applicable for line, column and area type Sparkline.

{% highlight js %}

$("#container").ejSparkline({
            // ...
            markerSettings: {
                visible: true,
                width: 4,
                fill: "#ff14ae",
                border: {
                    width: 1
                }
            }
            // ...
});


{% endhighlight %}

![](/js/Sparkline/Marker-Customization_images/Marker-Customization_img1.png)
