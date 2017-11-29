---
layout: post
title: Getting-Started
description: getting started
platform: js
control: DateTimePicker
documentation: ug
api: /api/js/ejdatetimepicker
---

# Getting Started

This section explains briefly about how to create a **DateTimePicker** in your application with **JavaScript**.

**Essential JavaScript DateTimePicker** provides support to display a calendar within a web page and allows you to pick a date and time from the calendar. In this example, you can learn how to customize **DateTimePicker** in a real-time application for an appointment and to choose current time for one week. 

The following screenshot illustrates the functionality of a **DateTimePicker** with date range of maximum one week.



![](/js/DateTimePicker/Getting-Started_images/Getting-Started_img1.png)

## Create DateTimePicker 

The **DateTimePicker** widget has built-in features such as keyboard navigation, other navigation with animations and flexible APIs. You can easily create the **DateTimePicker** widget by using simple input **&lt;textbox&gt;** element as follows.

Create an **HTML** file and add the following template to the **HTML** file.



{% highlight html %}

<!DOCTYPE html>
<html>
   <head>
      <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
      <!-- Style sheet for default theme (flat azure) -->
      <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
      <!--Scripts-->
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"> </script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
      <!--Add custom scripts here -->
   </head>
   <body>
      <!-- add DateTimePicker element here -->
   </body>
</html>

{% endhighlight %}

N> jQuery.easing external dependency has been removed from version 14.3.0.49 onwards. Kindly include this jQuery.easing dependency for versions lesser than 14.3.0.49 in order to support animation effects.

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



{% highlight javascript %}

    $(function() {
       $('#dateTime').ejDateTimePicker({
          width: '180px'
       });
    });

{% endhighlight %}



The following screenshot displays a **DateTimePicker** control.

![](/js/DateTimePicker/Getting-Started_images/Getting-Started_img.png)


## Get / Set value

DateTimePicker provides an options to configure all its properties and get its value. DateTimePicker value can be assigned during initialization or at run time. Below code shows how to assign values at initialization.

{% highlight javascript %}


        $(function () {

            // create DateTimePicker from input with current datetime value.

            $("#dateTime").ejDateTimePicker({

                value: new Date(), // sets the current datetime value

            });

        });

{% endhighlight %}

You can assign values after initialization in DateTimePicker (‘it helps to get or set value at run time). Let’s consider that going to set datetime value at button click.

{% highlight javascript %}

        //bind below onClick action to button

        function onClick() {

            //create instance for dateTimePicker.

            // only after control creation we can get dateTimeObj otherwise it throws exception.

            var dateTimeObj = $("#dateTime").ejDateTimePicker('instance');

            //set value using datetime object

            dateTimeObj.option('value', new Date());

            //get value using dateTimeObj and displays in alert box

            alert(dateTimeObj.option('value'));

        }

{% endhighlight %}

The following screenshot displays a **DateTimePicker** control with datetime value.

![](/js/DateTimePicker/Getting-Started_images/Getting-Started_img2.png)


## Set the Min and Max Date with Time Interval

In a real-time appointment scenario, the appointment is open only for a limited number of days. You have to select a date and time within the given range. This can be achieved by using the properties **min** and **max** that enables the specified date range in the **DateTimePicker** control.

{% highlight javascript %}

    $(function() {
       $('#dateTime').ejDateTimePicker({
          width: '180px',
          value: new Date(),
          minDateTime: "05/23/2014 09:00 AM",
          maxDateTime: "05/29/2014 09:00 PM"
       });
    });

{% endhighlight %}



The following screenshot shows the output for the above code example.

![](/js/DateTimePicker/Getting-Started_images/Getting-Started_img3.png)

