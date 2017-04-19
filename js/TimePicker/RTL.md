---
layout: post
title: RTL
description: rtl
platform: js
control: TimePicker
documentation: ug
api: /api/js/ejtimepicker
---

# RTL

This feature supports to change the left-to-right alignment of the **TimePicker** widget to right-to-left(**RTL**). The custom template **TimePicker** also supports **RTL**.

## Enabling Right-To-Left Support

The following steps explains you in enabling the right-to-left property for the **TimePicker**.

In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.   

{% highlight html %}

<input type="text" id="time" />

{% endhighlight %}

{% highlight javascript %}

    // Enable RTL for TimePicker controls as follows.
    $(function () {
        $('#time').ejTimePicker({
            enableRTL: true
        });
    });
    
{% endhighlight %}


The following screenshot illustrates a **TimePicker** control when **enableRTL** is set to **“true”**

![](/js/TimePicker/RTL_images/RTL_img1.png) 

