---
layout: post
title: RTL-Support
description: rtl support
platform: js
control: Rotator
documentation: ug
api: /api/js/ejrotator
---

# RTL Support

This feature supports to change the left-to-right alignment of the **Rotator** to right-to-left (RTL). (I.e.) Sets the **Rotator** to do its actions from right to left. The property [enableRTL](https://help.syncfusion.com/api/js/ejrotator#members:enablertl) sets the **Rotator** from right to left. The value set to this property is **boolean** type.

{% highlight javascript %}

    $(function () {
        // declaration
        $("#sliderContent").ejRotator({ slideWidth: 500, enableRTL: true });
    });

{% endhighlight %}



