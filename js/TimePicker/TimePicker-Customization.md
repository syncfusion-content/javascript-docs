---
layout: post
title: TimePicker-Customization
description: timepicker customization
platform: js
control: TimePicker
documentation: ug
api: /api/js/ejtimepicker
---

# TimePicker Customization

The **TimePicker** provides support to display a **TimePicker** in your web page and allows you to pick a time from it.

## Creating TimePicker Widget

The following steps explains you to create a **TimePicker** widget.

In an **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.

{% highlight html %}

<input type="text" id="time" />

{% endhighlight %}

{% highlight javascript %}

    // You can render TimePicker control as follows.
    $(function () {
        $('#time').ejTimePicker();
    });
    
{% endhighlight %}


The following screenshot illustrates you a default **TimePicker**.



![](/js/TimePicker/TimePicker-Customization_images/TimePicker-Customization_img1.png) 

