---
layout: post
title: Date-Range
description: date range
platform: js
control: DatePicker
documentation: ug
---

# Date Range

**Date Range** from minimum to maximum value is set for **DatePicker** widget using “**minDate”** and “**maxDate”** properties respectively. This allows you to restrict the date selection between the **minDate** and **maxDate**. This disables the dates below the **minDate** and dates above the **maxDate**.

The following steps explain you how to get the **Date Range** of **DatePicker** widget.

In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget

{% highlight html %}
  
<input id="datepicker" type="text" />
      
{% endhighlight %}
  
{% highlight js %}

    // Add the code to set the Date Range of DatePicker widget
    $(function() {
       // declaration
       $("#datepicker").ejDatePicker({
          minDate: new Date("2014/06/03"),
          maxDate: new Date("2014/06/19")
       });
    });

{% endhighlight %}




The following screenshot displays the output for the above code.

{% include image.html url="/js/DatePicker/Date-Range_images/Date-Range_img1.png"%}

