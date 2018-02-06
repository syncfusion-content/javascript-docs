---
layout: post
title: Responsive-Layout
description: responsive layout
platform: js
control: PivotClient
documentation: ug
api: /api/js/ejpivotclient
---

# Responsive layout

The pivot client widget supports responsive rendering based on the target device (desktop and tablet) resolution. It supports resolution up to 1024x600. You can enable the responsiveness in the pivot client by setting [`isResponsive`](/api/js/ejpivotclient#members:isresponsive) property to true.

{% highlight javascript %}

            $("#PivotClient1").ejPivotClient({
                //...
                isResponsive: true,
            });

{% endhighlight %}

![](Responsive-Layout_images/responsive.png)




