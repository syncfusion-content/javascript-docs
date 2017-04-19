---
layout: post
title: Time-Format
description: time format
platform: js
control: TimePicker
documentation: ug
api: /api/js/ejtimepicker
---

# Time Format

**TimePicker** widget provides you an option to change the time format.

## Steps to change Time Format of TimePicker widget

The following steps explains you to change the time format for the **TimePicker**.

In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.

{% highlight html %}

<input type="text" id="time" />

{% endhighlight %}

{% highlight javascript %}

    // Change time format for TimePicker controls as follows.
    $(function () {
        $('#time').ejTimePicker({
            timeFormat: "h:mm:ss tt"
        });
    });
    
{% endhighlight %}


Execute the above code to render the following output.



![](/js/TimePicker/Time-Format_images/Time-Format_img1.png) 

