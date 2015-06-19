---
layout: post
title: Getting-Started
description: getting started
platform: js
control: DatePicker
documentation: ug
---

# Getting Started

This section explains briefly about how to create a **DatePicker** in your application with **JavaScript**.

## Create your first DatePicker in JavaScript

The **Essential JavaScript****DatePicker** provides support to display a calendar within your web page and allows you to pick a date from the calendar. In this example, you can learn how to customize two **DatePickers** in a real-time ticket booking application. The example shows you how to use the **DatePicker** control to book a ticket within a limited number of days. 

The following screenshot illustrates the functionality of a **DatePicker**with date range of maximum 60 days. You can select a date for Onward and Return journeys ranging for a period of 60 days from the current day. This avoids selecting a journey date prior to the current date.

{% include image.html url="/js/DatePicker/Getting-Started_images/Getting-Started_img1.png" Caption="DatePicker"%}

### Create a DatePicker 

**Essential JavaScript DatePicker** widget basically renders with built-in features such as keyboard navigation, other months navigation with animations and flexible **API’s**. You can easily create the **DatePicker** widget by using simple input textbox element as follows.

* Create an **HTML** file and paste the following template to the **HTML** file for **DatePicker** creation.

{% highlight html %}


<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
    <!-- style sheet for default theme(flat azure) -->
    <link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <!--scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"> </script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>
    <script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js"> </script>
</head>
<body>
    <!-- add datepicker element here  --->
</body>
    </html>


{% endhighlight %}

* Add input element to render a **DatePicker**.

{% highlight html %}


  <table>
      <tr>
         <td class="tdclass">Onward Date</td>
         <td class="tdclass">Return date</td>
      </tr>
      <tr>
         <td class="tdclass">
             <span class="innerdp">
                <input id="startDate" type="text" />
             </span>
         </td>
         <td class="tdclass">
             <span class="innerdp">
                <input id="endDate" type="text" />
             </span>
         </td>
       </tr>
  </table>



{% endhighlight %}

* Initialize **DatePicker** in script.

{% highlight js %}

<script type="text/javascript">
$(function () {
// document ready
// simple datepicker creation
$("#startDate").ejDatePicker();
       $("#endDate").ejDatePicker();
});
</script>



{% endhighlight %}

* Apply the following styles to show the **Date Picker** control in the **Horizontal** order.

{% highlight css %}

<style type="text/css" class="cssStyles">
        .tdclass
        {
            width: 300px;
            font-weight: bold;
        }
        .innerdp
        {
            display: inline-block;
        }
</style>



{% endhighlight %}

The following screenshot displays a **DatePicker** control.

{% include image.html url="/js/DatePicker/Getting-Started_images/Getting-Started_img2.png" Caption="DatePicker"%}

### Set the Min and Max Date

In a real time ticket booking scenario, the booking is open only for a limited number of days. You have to select a date from the given range. This can be achieved by using the properties **minDate** and **maxDate**. In this way, only those dates ranging between the **minDate** and **maxDate** are enabled in the **DatePicker**.

{% highlight js %}

<script type="text/javascript">
var curdate = new Date();// mentions the current date.
// the following code sets the date range to 60 days from the current date.
var rangeDate=new Date(curdate.getFullYear(), curdate.getMonth(), curdate.getDate() + 60);       
 $(function () {            
            // declaration
            $("#startDate").ejDatePicker({
                value: curdate, // the current date is used as default value
                minDate: curdate,// Default date as mindate.
                maxDate: rangeDate // 60 –days of interval from min date.
            });
            $("#endDate").ejDatePicker({
                value: curdate, // the current date is used as the default value
                minDate: curdate, // Default date as mindate.
                maxDate: rangeDate // 60 –days of interval from min date.
            });  
      });
    </script>


{% endhighlight %}

The following screenshot shows the output of the above code example.

{% include image.html url="/js/DatePicker/Getting-Started_images/Getting-Started_img3.png" Caption="DatePickers with Min/Max Date"%}

### Set Event to Process the Min and Max Date Validations

You can select the “Onward journey date” in the first **DatePicker** and then the “Return journey date” in the second **DatePicker**. The validation process is done after the selection of “Onward Journey date” and the changes are reflected in the “Return Date” selection **DatePicker**. You can manipulate this process in the “Select” Event of Onward Date Selection **DatePicker**. 

{% highlight js %}


<script type="text/javascript">
        var minDatepicker,maxDatepicker;
        var curdate = new Date();// mentions the current date.
        // Set the return date to60 days from the current date.
        var rangeDate=new Date(curdate.getFullYear(), curdate.getMonth(), curdate.getDate() + 60);

        $(function () {
            // declaration
            $("#startDate").ejDatePicker({
                value: curdate, // the current date is used as the default value
                minDate: curdate,// Default date is set to mindate.
                maxDate: rangeDate, // 60 –days of interval from min date.
                select: "selectedStartDate"//select event functionality.
            });
            $("#endDate").ejDatePicker({
                value: curdate, // the current date is used as the default value
                minDate: curdate, // Default date as mindate.
                maxDate: rangeDate, // 60 –days of interval from min date.
                select: " selectedEndDate"//select event functionality.
            });  

        });

        function selectedStartDate (sender) {
            var selDate = new Date(sender.value); // mentions the selected date.
            minDatepicker = $("#endDate").data("ejDatePicker");// creating DatePicker object
            minDatepicker.setModel({ "minDate": selDate });// setting minDate property through setModel of DatePicker object.

        }
        function selectedEndDate(sender) {
            var selDate = new Date(sender.value);
            maxDatepicker = $("#startDate").data("ejDatePicker");// creating DatePicker object
            maxDatepicker.setModel({ "maxDate": selDate });// setting maxDate property through setModel of DatePicker object.

        }
    </script>



{% endhighlight %}

You can execute the above code and achieve the desired result. By selecting the onward journey date in the first **DatePicker**, you can select the Return Journey date within the given range. This restricts you from selecting the false date. This scenario is illustrated in the following screen shot.

{% include image.html url="/js/DatePicker/Getting-Started_images/Getting-Started_img4.png" Caption="DatePickers with Min/Max Date"%}

By using the min/max date range property, you can select a date within a given range as follows.

{% include image.html url="/js/DatePicker/Getting-Started_images/Getting-Started_img5.png" Caption="DatePickers with Min/Max Date"%}

You can also add additional functionalities such as localization and date formats to the date picker. 

