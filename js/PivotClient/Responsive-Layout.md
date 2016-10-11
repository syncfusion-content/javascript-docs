---
layout: post
title: Responsive-Layout
description: responsive layout
platform: js
control: PivotClient
documentation: ug
---

# Responsive Layout

PivotClient widget supports responsive rendering based on the target device (desktop & tablet) resolution. It supports resolution up to 1024x600. You can enable responsiveness in PivotClient by setting [`isResponsive`](/js/api/ejpivotclient#members:displaysettings-isresponsive) property to true.

{% highlight javascript %}

            $("#PivotClient1").ejPivotClient({
                //...
                isResponsive: true,
            });

{% endhighlight %}

![](Responsive-Layout_images/responsive.png)




