---
layout: post
title: RTL-Support
description: rtl support
platform: js
control: DatePicker
documentation: ug
---

# RTL Support

Right-to-left starts from the right of the page and continues to the left. By default, this option is set to “**false**” in the **DatePicker** widget. 

The **enableRTL** option allows the **DatePicker** widget to display it in the right to left direction.

The following steps explain you how to enable the **RTL** property of the **DatePicker** widget.

* In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget

{% highlight html %}

      <input id="datepicker" type="text" />
      
  {% endhighlight %}
  
  {% highlight js %}

  <script type="text/javascript">
    // Add the code to enable the RTL property of the DatePicker widget
        $(function () {
            // declaration
            $("#datepicker").ejDatePicker({
                enableRTL: true
            });
        });
    </script>

  {% endhighlight %}


*  The following screenshot displays the output for the above code.

{% include image.html url="/js/DatePicker/Concepts-and-Features/RTL-Support_images/RTL-Support_img1.png" Caption="Figure 21: RTL Support in DatePicker"%}

