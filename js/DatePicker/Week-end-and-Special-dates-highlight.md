---
layout: post
title: Week-end-and-Special-dates-highlight
description: week end and special dates highlight
platform: js
control: DatePicker
documentation: ug
---

# Week end and Special dates highlight

**Week end and special dates** are highlighted in **DatePicker** widget for your identification as per your requirement.

You can highlight the **week end** by using “**highlightWeekend”** property and **special dates** are highlighted by using **“specialDates”** property.

You can find the sprite images in the following location when you have installed essential studio, otherwise you can use your own image.

**[Installed Drive]**:\Users\[username]\AppData\Local\Syncfusion\EssentialStudio\{{ site.releaseversion }}\JavaScript\samples\web\images\autocomplete\flags.png

The following steps explain how to get the highlighted week end and special dates.

In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget


{% highlight html %}

<input id="datepicker" type="text" />
      
{% endhighlight %}
  
{% highlight js %}

    // Add the code to get the highlighted week end and special dates
    $(function() {
       //inserting a image for special dates to highlight a some special dates
       var today = new Date(),
          spldays = [{
             date: new Date(today.getFullYear(), today.getMonth(), 1),
             iconClass: "flag-am"
          }, ]
          // declaration 
       $("#datepicker").ejDatePicker({
          specialDates: spldays,
          highlightWeekend: true
       });
    });

{% endhighlight %}



Add the following styles to get the special dates highlighted.



{% highlight css %}

<style type="text/css" class="cssStyles">
   .flag .e-image {
       background: url(/images/flags.png) no-repeat left center;
       width: 25px;
       height: 15px;
   }
   .e-datepicker.e-calendar {
       width: 350px;
   }
</style>

{% endhighlight %}



The following screenshot displays the output for the above code example.



![]("/js/DatePicker/Week-end-and-Special-dates-highlight_images/Week-end-and-Special-dates-highlight_img1.png")

