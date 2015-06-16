---
layout: post
title: Display-Inline
description: display inline
platform: js
control: DatePicker
documentation: ug
---

# Display Inline

**Display****Inline** allows you to make **DatePicker** widget similar to a **Calendar date**. Also associate **DatePicker** with **&lt;div&gt; element instead of input. Default value for **displayInline** property is set as '**false**' 

The following steps explain you how to get the **Calendar** control using **DatePicker**.

* In the **HTML** page, add a **&lt;div&gt;** element to render **DatePicker** widget


  {% highlight html %}

      <input id="datepicker" type="text" />
      
  {% endhighlight %}
  
  {% highlight js %}

<script type="text/javascript">
  // Add the code to get the Calendar control using DatePicker
$(function () {
            // declaration
            $("#datepicker").ejDatePicker({
                displayInline: true
            });
        });
    </script>

  {% endhighlight %}




* The following screenshot displays the output for the above code.

{% include image.html url="/js/DatePicker/Concepts-and-Features/Display-Inline_images/Display-Inline_img1.png" Caption="Figure 15: Calendar date in DatePicker"%}

