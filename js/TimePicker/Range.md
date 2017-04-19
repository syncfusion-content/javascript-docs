---
layout: post
title: Range
description: range
platform: js
control: TimePicker
documentation: ug
api: /api/js/ejtimepicker
---

# Range

**TimePicker** widget provide options to set the Range (minTime & maxTime) for the time.

## Steps to change minTime & maxTime of the TimePicker

The following steps explains you to change the Range of the **TimePicker**.

In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.

{% highlight html %}

<input type="text" id="time" />

{% endhighlight %}

{% highlight javascript %}

    // Use minTime and maxTime property to change the Range of the TimePicker.
    $(function () {
        $('#time').ejTimePicker({
            minTime: "10:00 AM",
            maxTime: "9:00 PM"
        });
    });
    
{% endhighlight %}


Execute the above code to render the following output.



![](/js/TimePicker/Range_images/Range_img1.png) 

