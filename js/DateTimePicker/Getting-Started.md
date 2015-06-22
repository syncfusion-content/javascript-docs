---
layout: post
title: Getting-Started
description: getting started
platform: js
control: DateTimePicker
documentation: ug
---

# Getting Started

This section explains briefly about how to create a **DateTimePicker** in your application with **JavaScript**.

## Create your first DateTimePicker in JavaScript	

**Essential JavaScript** **DateTimePicker** provides support to display a calendar within a webpage and allows you to pick a date and time from the calendar. In this example, you can learn how to customize **DateTimePicker** in a real-time application for an appointment and to choose current time for one week. 

The following screenshot illustrates the functionality of a **DateTimePicker** with date range of maximum one week.



{% include image.html url="/js/DateTimePicker/Getting-Started_images/Getting-Started_img1.png" Caption="DateTimePicker"%}

### Create DateTimePicker 

**The DateTimePicker** widget has built-in features such as keyboard navigation, other navigation with animations and flexible APIs. You can easily create the **DateTimePicker** widget by using simple input **&lt;textbox&gt;** element as follows.

Create an **HTML** file and add the following template to the **HTML** file.



{% highlight html %}

<!DOCTYPE html>
<html>
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
    <!-- Style sheet for default theme (flat azure) -->
    <link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />

    <!--Scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"> </script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"> </script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>

    <script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js"></script>
    <!--Add custom scripts here -->
</head>
<body>
    <!-- add DateTimePicker element here  	-->
</body>
</html>



{% endhighlight %}



Add **&lt;input&gt;** element to render a **DateTimePicker**.



{% highlight html %}


<div class="content-container-fluid">
    <div class="row">
        <div class="cols-sample-area">
            <div class="frame">
                <div class="control">
                    <input type="text" id="dateTime" />
                </div>
            </div>
        </div>
    </div>
</div>


{% endhighlight %}



Add the following styles to show the **DateTimePicker** control in the horizontal order.



{% highlight css %}

<style type="text/css" class="cssStyles">
    .control {
        margin: 0 auto;
        width: 210px;
    }
</style>


{% endhighlight %}



Initialize **DateTimePicker** in the script.



{% highlight js %}

    $(function () {
        $('#dateTime').ejDateTimePicker({ width: '180px', value: new Date() });
    });


{% endhighlight %}



The following screenshot displays a **DateTimePicker** control.

{% include image.html url="/js/DateTimePicker/Getting-Started_images/Getting-Started_img2.png" Caption="DateTimePicker"%}

### Set the Min and Max Date with Time Interval

In a real-time appointment scenario, the appointment is open only for a limited number of days. You have to select a date and time within the given range. This can be achieved by using the properties **min** and **max** that enables the specified date range in the **DateTimePicker** control.

{% highlight js %}

    $(function () {
        $('#dateTime').ejDateTimePicker({ width: '180px', value: new Date(), minDateTime: "05/23/2014 09:00 AM", maxDateTime: "05/29/2014 09:00 PM" });
    }); 


{% endhighlight %}



The following screenshot shows the output for the above code example.

{% include image.html url="/js/DateTimePicker/Getting-Started_images/Getting-Started_img3.png" Caption="DateTimePickers with Min/Max Date with Time Intervals"%}

