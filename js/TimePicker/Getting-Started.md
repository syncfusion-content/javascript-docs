---
layout: post
title: Getting-Started
description: getting started
platform: js
control: TimePicker
documentation: ug
---

# Getting Started

This section explains briefly about how to create a **TimePicker** in your application with **JavaScript.**

## Create your first TimePicker in JavaScript

The **Essential JavaScript** **TimePicker** provides support to display a **TimePicker** in your webpage and allows you to pick a time from the given **TimePicker**. Here, you can learn how to customize two dates and **TimePickers** in a real-time hotel table booking application. 

The following screenshot illustrates the functionality of a **TimePicker** with a time range of morning to evening. You can select a time to book a table, from a period of 9.00 AM to 6.00 PM for the current day. This avoids selecting a time prior to the morning.

{% include image.html url="/js/TimePicker/Getting-Started_images/Getting-Started_img1.png" Caption="TimePicker"%}

**Create a TimePicker** 

**Essential JavaScript TimePicker** widget renders built-in features such as keyboard navigation, other time navigation with animations and flexible APIs. You can easily create the **TimePicker** widget by using simple input textbox element as follows.

* Create an **HTML** file and add the following template to the **HTML** file.

{% highlight html %}

<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8"  />
    <!-- Style sheet for default theme (flat azure) -->
<link href="[http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css](http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css)"rel="stylesheet"/>

    <!--Scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"> </script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>

<script src="[http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js](http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js)"></script>
    <!--Add custom scripts here -->
</head>
<body>
    <!-- add time picker element here -->
</body>
</html>



{% endhighlight %}



* Add input element to render a **TimePicker**.



{% highlight html %}

<table>
    <tr>
<td class="tdclass">Select date</td>
       <td class="tdclass">Select time</td>
<td class="tdclass">Select party size</td>
     </tr>
     <tr>
<td class="tdclass">
<span class="innerdp">
<input id="datepick" type="text" />
</span>
</td>
<td class="tdclass">
<span class="innerdp">
<input id="time" type="text" />
</span>
</td>
<td class="tdclass">
<span class="innerdp">
<select name="party_size">
<option name="party_size" value="default">select people</option>
<option name="party_size" value="5">5 people</option>
<option name="party_size" value="10">10 people</option>
<option name="party_size" value="15">15 people</option>
<option name="party_size" value="20">20 people</option>
</select>
</span>
</td>
   </tr>
   <tr>
   	<td class="tdclass">
<button class="book">Book</button>
</td>
   </tr>
</table>


{% endhighlight %}



* Initialize **TimePicker** using the following code example.



{% highlight js %}

<script type="text/javascript">
$(function () {
// document ready
// simple time picker creation
       $("#datepick").ejDatePicker();
       $("#time").ejTimePicker();
});
</script>


{% endhighlight %}



* Add the following styles to show **Time Picker** control.



{% highlight css %}

<style type="text/css" class="cssStyles">
        .tdclass
        {
            width: 200px;
            font-weight: bold;
        }
        .innerdp
        {
            display: inline-block;
        }
</style>



{% endhighlight %}



The following screenshot displays a **TimePicker** control.

{% include image.html url="/js/TimePicker/Getting-Started_images/Getting-Started_img2.png" Caption="TimePicker with booking"%}

### Set the Min and Max Values

In a real-time hotel table booking scenario, the booking is open only for a limited time and limited number of days. You have to select a time and date from the given range. This is achieved by using the properties **minTime** and **maxTime**, **minDate** and **maxDate**. By this way, only times ranging between **minTime** and **maxTime**, **minDate** and **maxDate** are enabled in the **TimePicker**.

{% highlight js %}

<script type="text/javascript">
var curdate = new Date();// mentions the current date.
var mintime = "9:00 AM"; // mentions the start time.
var maxtime = "6:00 PM"; // mentions the start time.
// the following code sets the date range to 30 days from the current date.
var rangeDate=new Date(curdate.getFullYear(), curdate.getMonth(), curdate.getDate() + 30);       
 $(function () {            
            // declaration
            $("#datepick").ejDatePicker({
                value: curdate, // the current date is used as default value
                minDate: curdate,// Default date as mindate.
                maxDate: rangeDate // 30 –days of interval from min date.
            });
            $("#time").ejTimePicker({
                minTime: mintime, // Start time as mintime.
                maxTime: maxtime // End time as maxtime.
            });  
      });
    </script>


{% endhighlight %}



The above code example displays the following output.

{% include image.html url="/js/TimePicker/Getting-Started_images/Getting-Started_img3.png" Caption="TimePickers with Min/Max Date and Time"%}__

### Set Time Interval

You can select the **Time** in **TimePicker** with the interval of one hour. You need to set the property **interval** as 60.

The following code example shows how to set **Time****interval**.

{% highlight js %}

<script type="text/javascript">
        var curdate = new Date();// mentions the current date.
var mintime = "9:00 AM"; // mentions the start time.
var maxtime = "6:00 PM"; // mentions the start time.
// the following code sets the date range to 30 days from the current date.
var rangeDate=new Date(curdate.getFullYear(), curdate.getMonth(), curdate.getDate() + 30);       
 $(function () {            
            // declaration
            $("#datepick").ejDatePicker({
                value: curdate, // the current date is used as default value
                minDate: curdate,// Default date as mindate.
                maxDate: rangeDate // 30 –days of interval from min date.
            });
            $("#time").ejTimePicker({
                minTime: mintime, // Start time as mintime.
                maxTime: maxtime, // End time as maxtime.
                interval: 60            
            });  
      });
</script>



{% endhighlight %}

Execute the above code to achieve the desired result. You can select the date and time in **TimePicker** within the given range of one hour interval. This scenario is illustrated in the following screenshot.



{% include image.html url="/js/TimePicker/Getting-Started_images/Getting-Started_img4.png" Caption="TimePicker with a one hour interval"%}

### Display the Acknowledgement Message

The **acknowledgement** **message** is displayed when you click the ‘**Book’** button.

The following code example shows how to display the **acknowledgement** **message**.

{% highlight js %}

<script type="text/javascript">
var curdate = new Date();// mentions the current date.
var mintime = "9:00 AM"; // mentions the start time.
var maxtime = "6:00 PM"; // mentions the start time.
// the following code sets the date range to 30 days from the current date.
var rangeDate=new Date(curdate.getFullYear(), curdate.getMonth(), curdate.getDate() + 30);       
 $(function () {            
            // declaration
            $("#datepick").ejDatePicker({
                value: curdate, // the current date is used as default value
                minDate: curdate,// Default date as mindate.
                maxDate: rangeDate // 30 –days of interval from min date.
            });
            $("#time").ejTimePicker({
                minTime: mintime, // Start time as mintime.
                maxTime: maxtime, // End time as maxtime.
                interval: 60            
            });  
      });
$(document).ready(function(){
$('.book').click(function(){
var a=$('#datepick').val();
var b=$('#time').val();
var c=$('select').val();
alert("You are booked the table with date "+a+" time "+b+ " Party_size is "+c);
});
_});_
</script>


{% endhighlight %}

The following screenshot displays the **acknowledgement** **message**.

{% include image.html url="/js/TimePicker/Getting-Started_images/Getting-Started_img5.png" Caption="Acknowledgement Message"%}

### Create Two TimePickers

You can select the **Start** **time** in the first **TimePicker** and then the **End** **time** in the second **TimePicker**. The validation process is done after the selection of **Start** **time** and the changes are reflected in the **End** **time** selection **TimePicker**. You can manipulate this process in the **Select** event of **Start Time** selection **TimePicker**. 

* Add input element to render **Two TimePickers**.



{% highlight html %}

<table>
    <tr>
<td class="tdclass">Select date</td>
       <td class="tdclass">Select start time</td>
       <td class="tdclass">Select end time</td>
<td class="tdclass">Select party size</td>
     </tr>
     <tr>
<td class="tdclass">
<span class="innerdp">
<input id="datepick" type="text" />
</span>
</td>
<td class="tdclass">
<span class="innerdp">
<input id="time" type="text" />
</span>
</td>
<td class="tdclass">
<span class="innerdp">
<input id="timeend" type="text" />
</span>
</td>
<td class="tdclass">
<span class="innerdp">
<select name="party_size">
<option name="party_size" value="default">select people</option>
<option name="party_size" value="5">5 people</option>
<option name="party_size" value="10">10 people</option>
<option name="party_size" value="15">15 people</option>
<option name="party_size" value="20">20 people</option>
</select>
</span>
</td>
   </tr>
   <tr>
   	<td class="tdclass">
<button class="book">Book</button>
</td>
   </tr>
</table>


{% endhighlight %}



* Initialize **Two TimePickers** using the following code example.

{% highlight js %}


<script type="text/javascript">
var curdate = new Date();// mentions the current date.
var mintime = "9:00 AM"; // mentions the start time.
var maxtime = "6:00 PM"; // mentions the start time.
var minTimepicker;
// the following code sets the date range to 30 days from the current date.
var rangeDate=new Date(curdate.getFullYear(), curdate.getMonth(), curdate.getDate() + 30);       
 $(function () {            
            // declaration
            $("#datepick").ejDatePicker({
                value: curdate, // the current date is used as default value
                minDate: curdate,// Default date as mindate.
                maxDate: rangeDate // 30 –days of interval from min date.
            });
            $("#time").ejTimePicker({
                minTime: mintime, // Start time as mintime.
                maxTime: maxtime, // End time as maxtime.
                interval: 60,
                select: "selectedStartTime"            
            });
            $('#timeend').ejTimePicker({
minTime: mintime,
maxTime: maxtime,
interval: 60,
});
      });
function selectedStartTime (sender) {
     var selDate = sender.value; // mentions the selected time.
      minTimepicker = $("#timeend").data("ejTimePicker");// creating TimePicker object
      minTimepicker.setModel({ "minTime": selDate });// setting minTime property through setModel of TimePicker object.
 }
   $(document).ready(function(){
  	$('.book').click(function(){
var a=$('#datepick').val();
var b=$('#time').val();
var c=$('select').val();
alert("You are booked the table with date "+a+" time "+b+ " Party_size is "+c);
});
  });

</script>


{% endhighlight %}

Execute the above code to achieve the desired result. By selecting the **Start Time** in the first **TimePicker**, you can select the End Time within the given range. This restricts you from selecting false time. This scenario is illustrated in the following screenshot.

{% include image.html url="/js/TimePicker/Getting-Started_images/Getting-Started_img6.png" Caption="Two TimePickers"%}



You can also add additional functionalities such as localization and time formats to the **TimePicker**. 

