---
layout: post
title: Dates-in-Other-Month
description: dates in other month
platform: js
control: DatePicker
documentation: ug
---

# Dates in Other Month

**Dates** from the previous and next month are showed in **DatePicker** calendar. 

You can set the other month date in **DatePicker** by using **“showOtherMonths”** property. By default **showOtherMonths** (Boolean) is set to ‘**true**’ that enables the other month date.

The Current month date alone is displayed by setting **Boolean** as ‘**false**’.

The following steps explain you how to get the current month date alone

In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget

{% highlight html %}
  
<input id="datepicker" type="text" />
      
{% endhighlight %}
  
{% highlight js %}

    // Add the code to get the current month date
    $(function() {
       // declaration
       $("#datepicker").ejDatePicker({
          showOtherMonths: false
       });
    });

{% endhighlight %}


The following screenshot displays the output for the above code.

![]("/js/DatePicker/Dates-in-Other-Month_images/Dates-in-Other-Month_img1.png")

