---
layout: post
title: getting-started
description: getting started
platform: js
control: TimePicker
documentation: ug
---

# Getting Started

This section explains briefly about how to create a **TimePicker** in your application with **JavaScript** and **ASP.NET MVC.**

## Create your first TimePicker in JavaScript

The **Essential JavaScript****TimePicker** provides support to display a **TimePicker** in your webpage and allows you to pick a time from the given **TimePicker**. Here, you can learn how to customize two dates and **TimePickers** in a real-time hotel table booking application. 

The following screenshot illustrates the functionality of a **TimePicker** with a time range of morning to evening. You can select a time to book a table, from a period of 9.00 AM to 6.00 PM for the current day. This avoids selecting a time prior to the morning.



![](getting-started_images\getting-started_img1.png)

_Figure_ _1__:_ _TimePicker_



**Create a TimePicker** 

**Essential JavaScript TimePicker** widget renders built-in features such as keyboard navigation, other time navigation with animations and flexible APIs. You can easily create the **TimePicker** widget by using simple input textbox element as follows.

* Create an **HTML** file and add the following template to the **HTML** file.

{% highlight html %}

<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8"  />
    <!-- Style sheet for default theme (flat azure) -->
<linkhref="[http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css](http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css)"rel="stylesheet"/>

    <!--Scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"> </script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>

<scriptsrc="[http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js](http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js)"></script>
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





* The following screenshot displays a **TimePicker** control.



{% include image.html url="\js\TimePicker\getting-started_images\getting-started_img2.png" Caption="Figure 2: TimePicker with booking"%}

### 

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

![](getting-started_images\getting-started_img3.png)

_Figure_ _3__:_ _TimePicker__s_ _with Min/Max Date and Time_

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
                iInterval: 60            
            });  
      });
</script>



{% endhighlight %}



Execute the above code to achieve the desired result. You can select the date and time in **TimePicker** within the given range of one hour interval. This scenario is illustrated in the following screenshot.



![](getting-started_images\getting-started_img4.png)



_Figure_ _4__:_ _TimePicker_ _with a_ _one hour interval_

### Display the Acknowledgement Message

The **acknowledgement****message** is displayed when you click the ‘**Book’** button.

The following code example shows how to display the **acknowledgement****message**.



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
                iInterval: 60            
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

The following screenshot displays the **acknowledgement****message**.

{% include image.html url="\js\TimePicker\getting-started_images\getting-started_img5.png" Caption="Figure 5: Acknowledgement Message"%}

### Create Two TimePickers

You can select the **Start****time** in the first **TimePicker** and then the **End****time** in the second **TimePicker**. The validation process is done after the selection of **Start****time** and the changes are reflected in the **End****time** selection **TimePicker**. You can manipulate this process in the **Select** event of **Start Time** selection **TimePicker**. 

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
                iInterval: 60,
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

{% include image.html url="\js\TimePicker\getting-started_images\getting-started_img6.png" Caption="Figure 6: Two TimePickers"%}



You can also add additional functionalities such as localization and time formats to the **TimePicker**. 



## Create your first TimePicker in MVC

**Essential MVC****TimePicker** provides support to display the time in your webpage and allows you to pick a time from the list. In this section you can learn how to customize **TimePickers** in a real-time application. The following example shows you how to use the **TimePicker** control to book a hotel dining table booking application, within a limited time, in any day.



{% include image.html url="\js\TimePicker\getting-started_images\getting-started_img7.png" Caption="Figure 7: TimePicker"%}



The above screenshot illustrates the functionality of a **TimePicker,** with a time range from morning to evening. You can select the time to book a table ranging from 9.00 AM to 10.00 PM in the current day. This avoids selecting a time prior to that day.



**Create a TimePicker**

**Essential MVC TimePicker** widget has built-in features such as keyboard navigation, other time navigation with animations, and flexible APIs. You can easily create the **TimePicker** widget using simple **TimePicker** element as follows.

1. You can create an **MVC** Project and add necessary assemblies and scripts to it. Refer [MVC-Getting Started](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm)Documentation.

2. Add the following code to the corresponding view page to render the **TimePicker**.



&lt;table&gt;

    &lt;tr&gt;

        <td class="tdclass">Date</td>

        <td class="tdclass">Time</td>

        <td class="tdclass">Person</td>

         &lt;/tr&gt;

    &lt;tr&gt;

        &lt;td class="tdclass"&gt;

            &lt;span class="innerdp"&gt;

                @Html.EJ().DatePicker("startDate")

            &lt;/span&gt;

        &lt;/td&gt;

        &lt;td class="tdclass"&gt;

            &lt;span class="innerdp"&gt;

                @Html.EJ().TimePicker("timestart")

               &lt;/span&gt;

        &lt;/td&gt;

      &lt;td class="tdclass"&gt;

            &lt;span class="innerdp"&gt;

                @Html.EJ().NumericTextbox("NumericTextbox").Value("0")

            &lt;/span&gt;

        &lt;/td&gt;

    &lt;/tr&gt;

    &lt;tr&gt;

        &lt;td&gt;&lt;/td&gt;

        &lt;td&gt;&lt;/td&gt;

         &lt;td class="tdclass"&gt;

            &lt;span class="innerdp"&gt;               @Html.EJ().Button("Submit").Width("100px").Size(ButtonSize.Small).Text("Submit").ClientSideEvents(s => s.Click("button"))

            &lt;/span&gt;

        &lt;/td&gt;

       &lt;/tr&gt;

&lt;/table&gt;         



3.   Add the following styles to show the **TimePicker** control in horizontal order in the Content folder.



&lt;style type="text/css" class="cssStyles"&gt;

    .tdclass {

        width: 70px;

        height: 10px;

        font-weight: bold;

        padding: 10px;

    }

   .innerdp {

        display: inline-block;

    }



&lt;/style&gt;





4.  Add the following code to the Layout page for **DatePicker** and **TimePicker** initialization.



&lt;script type="text/javascript"&gt;



            function button()

            {

                alert("You have Successfully booked");

            }



       &lt;/script&gt;

__

{% include image.html url="\js\TimePicker\getting-started_images\getting-started_img8.png" Caption="Figure 8: TimePicker, DatePicker, Numeric Textbox"%}



Run the application to render the following output.



{% include image.html url="\js\TimePicker\getting-started_images\getting-started_img9.png" Caption="Figure 9: TimePicker with alert"%}

**Set Min and Max Date**

In a real-time scenario, the booking is open only for a limited time. You can select a date and time from the given range using the properties **minDate, minTime** and **maxDate, maxTime** that enables only the dates and times ranging between the **minDate, minTime** and **maxDate, maxTime** in the **DatePicker** and **TimePicker**.****



&lt;table&gt;

    &lt;tr&gt;

        <td class="tdclass">Date</td>

        <td class="tdclass">StartTime</td>

        <td class="tdclass">EndTime</td>

        <td class="tdclass">Person</td>

         &lt;/tr&gt;

    &lt;tr&gt;

        &lt;td class="tdclass"&gt;

            &lt;span class="innerdp"&gt;

                @Html.EJ().DatePicker("startDate")

            &lt;/span&gt;

        &lt;/td&gt;

        &lt;td class="tdclass"&gt;

            &lt;span class="innerdp"&gt;

               @Html.EJ().TimePicker("timestart")

 &lt;/span&gt;

        &lt;/td&gt;

        &lt;td class="tdclass"&gt;

            &lt;span class="innerdp"&gt;

               @Html.EJ().TimePicker("timeend")

            &lt;/span&gt;

        &lt;/td&gt;

        &lt;td class="tdclass"&gt;

            &lt;span class="innerdp"&gt;

                @Html.EJ().NumericTextbox("NumericTextbox").Value("0")

            &lt;/span&gt;

        &lt;/td&gt;

    &lt;/tr&gt;

    &lt;tr&gt;

        &lt;td&gt;&lt;/td&gt;

        &lt;td&gt;&lt;/td&gt;

        &lt;td&gt;&lt;/td&gt;

        &lt;td class="tdclass"&gt;

            &lt;span class="innerdp"&gt;                @Html.EJ().Button("Submit").Width("100px").Size(ButtonSize.Small).Text("Submit").ClientSideEvents(s => s.Click("button"))

            &lt;/span&gt;

        &lt;/td&gt;

        &lt;/tr&gt;

&lt;/table&gt;

Add the following code to the script.



&lt;script type="text/javascript"&gt;

        var curdate = new Date();// mentions the current date.

        var mintime = "9:00 AM";

        var maxtime = "10:00 PM";

        var minTimepicker;

        // the following code sets the date range to 60 days from the current date.

        var rangeDate = new Date(curdate.getFullYear(), curdate.getMonth(), curdate.getDate() + 30);

        $(function () {

            // declaration

            $("#startDate").ejDatePicker({

                value: curdate, // the current date is used as default value

                minDate: curdate,// Default date as mindate.

                maxDate: rangeDate // 60 –days of interval from min date.

            });

         $('#timestart').ejTimePicker({

                minTime: mintime,

                maxTime: maxtime,

                interval: 60,

                select: "selectedStartTime"

            });

            $('#timeend').ejTimePicker({

                minTime: mintime,

                maxTime: maxtime,

                interval: 60,

            });

          });

     function selectedStartTime(sender) {

            var selDate = sender.value; // mentions the selected time.

            minTimepicker = $("#timeend").data("ejTimePicker");// creating TimePicker object

            minTimepicker.setModel({ "minTime": selDate });// setting minTime property through setModel of TimePicker object.

        }

    &lt;/script&gt;



   &lt;script type="text/javascript"&gt;



            function button()



            {

               alert("You have successfully booked");



            }



        &lt;/script&gt;



Execute the above code to render the following output.



{% include image.html url="\js\TimePicker\getting-started_images\getting-started_img10.png" Caption="Figure 10: Two TimePickers"%}



You can select the Start time in the first **TimePicker** and select the End time within the given range. The second **TimePicker** start value is based on the first **TimePicker**’s selected value. This is illustrated in the following screenshots.



{% include image.html url="\js\TimePicker\getting-started_images\getting-started_img11.png" Caption="Figure 11: Two TimePicker with MinValue"%}



{% include image.html url="\js\TimePicker\getting-started_images\getting-started_img12.png" Caption="Figure 12: Two TimePicker with MaxValue"%}



**Display Reserved Time** 

An acknowledgement message appears when you click the Submit button. 

You can specify the alert message in the script as follows.

&lt;script type="text/javascript"&gt;

        function button()

            {



                    var a = $('#startDate').val();



                    var b = $('#timestart').val();



                    var d = $('#timeend').val();



                    var c = $('#NumericTextbox').val();



                    alert("You have successfully booked\nDate    : " + a + "\nStartTime: " + b + "\nEndTime: " + d + " \nPerson   :  " + c);



            }

&lt;/script&gt;







{% include image.html url="\js\TimePicker\getting-started_images\getting-started_img13.png" Caption="Figure 13: TimePicker with Acknowledgment Message"%}



## Create your first TimePicker in ASP.NET

The **Essential ASP.NET****TimePicker** provides support to display a **TimePicker** in your webpage and allows you to pick a time from the given **TimePicker**. Here, you can learn how to customize two dates and TimePickers in a real-time hotel table booking application. 

The following screenshot illustrates the functionality of a **TimePicker** with a time range of morning to evening. You can select a time to book a table, from a period of 9.00 AM to 6.00 PM for the current day. This avoids selecting a time prior to the morning.



![](getting-started_images\getting-started_img14.png)

_Figure_ _14__:_ _TimePicker_



**Create a TimePicker** 

**Essential ASP.NET TimePicker** widget renders built-in features such as keyboard navigation, other time navigation with animations and flexible APIs. You can easily create the **TimePicker** widget by using simple input textbox element as follows.

1. You can create an ASP.NET Web Forms Project and add necessary Dll’s and scripts with the help of the given[ASP.NET WebForms-Getting Started](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm) Documentation.

2. Add the following code to the corresponding ASPX page to render the **TimePicker**.



**[ASPX]**

&lt;table&gt;

        &lt;tr&gt;

            &lt;td class="tdclass"&gt;

                Select date

            &lt;/td&gt;

            &lt;td class="tdclass"&gt;

                Select time

            &lt;/td&gt;

            &lt;td class="tdclass"&gt;

                Select party size

            &lt;/td&gt;

        &lt;/tr&gt;

        &lt;tr&gt;

            &lt;td class="tdclass"&gt;

                &lt;span class="innerdp"&gt;

                    &lt;ej:DatePicker ID="DatePicker" runat="server" /&gt;

                &lt;/span&gt;

            &lt;/td&gt;

            &lt;td class="tdclass"&gt;

                &lt;span class="innerdp"&gt;

                    &lt;ej:TimePicker ID="TimePicker" runat="server" /&gt;

                &lt;/span&gt;

            &lt;/td&gt;

            &lt;td class="tdclass"&gt;

                &lt;span class="innerdp"&gt;

                    &lt;ej:DropDownList name="party_size" ID="DropDownList" SelectedItemIndex="0" runat="server"&gt;

                        &lt;Items&gt;

                            &lt;ej:DropDownListItem Text="select people"&gt;

                            &lt;/ej:DropDownListItem&gt;

                            &lt;ej:DropDownListItem Text="5 people"&gt;

                            &lt;/ej:DropDownListItem&gt;

                            &lt;ej:DropDownListItem Text="10 people"&gt;

                            &lt;/ej:DropDownListItem&gt;

                            &lt;ej:DropDownListItem Text="15 people"&gt;

                            &lt;/ej:DropDownListItem&gt;

                            &lt;ej:DropDownListItem Text="20 people"&gt;

                            &lt;/ej:DropDownListItem&gt;

                        &lt;/Items&gt;

                    &lt;/ej:DropDownList&gt;

                &lt;/span&gt;

            &lt;/td&gt;

        &lt;/tr&gt;

        &lt;tr&gt;

            &lt;td class="tdclass"&gt;

                &lt;ej:Button ID="Book" Type="Button" Text="Book" ClientSideOnClick="acknowledge" runat="server"&gt;

                &lt;/ej:Button&gt;

            &lt;/td&gt;

        &lt;/tr&gt;

    &lt;/table&gt;



3. Add the following styles to show **Time Picker** control.



**[CSS]**

&lt;style type="text/css" class="cssStyles"&gt;

        .tdclass

        {

            width: 200px;

            font-weight: bold;

        }

        .innerdp

        {

            display: inline-block;

        }

    &lt;/style&gt;





4. The following screenshot displays a **TimePicker** control.



{% include image.html url="\js\TimePicker\getting-started_images\getting-started_img15.png" Caption="Figure 15: TimePicker with booking"%}

**Set the Min and Max Values**

In a real-time hotel table booking scenario, the booking is open only for a limited time and limited number of days. You have to select a time and date from the given range. This is achieved by using the properties **MinTime** and **MaxTime**, **MinDate** and **MaxDate**. By this way, only times ranging between **MinTime** and **MaxTime**, **MinDate** and **MaxDate** are enabled in the **TimePicker**.



**[CS]**

protected void Page_Load(object sender, EventArgs e)

        {

            DatePicker.MinDate = DateTime.Now.ToString();

            DatePicker.MaxDate = DateTime.Now.AddDays(30).ToString();

            TimePicker.MinTime = "9:00:00";

            TimePicker.MaxTime = "18:00:00";



        }



The above code example displays the following output.



![](getting-started_images\getting-started_img16.png)

_Figure_ _16__:_ _TimePicker__s with Min/Max Date and Time_

**Set Time Interval**

You can select the **Time** in **TimePicker** with the interval of one hour. You need to set the property **Interval** as 60.

The following code example shows how to set **Time****interval**.



**[ASPX]**

&lt;ej:TimePicker ID="TimePicker1" runat="server" Interval="60" /&gt;



Execute the above code to achieve the desired result. You can select the date and time in **TimePicker** within the given range of one hour interval. This scenario is illustrated in the following screenshot.



![](getting-started_images\getting-started_img17.png)___Figure_ _17__: TimePicker with an one hour interval_

**Display the Acknowledgement Message**

The **acknowledgement****message** is displayed when you click the ‘**Book’** button.

The following code example shows how to display the **acknowledgement****message**.



**[Script]**

&lt;script type="text/javascript"&gt;

        function acknowledge() {

            var a = $('#DatePicker').val();

            var b = $('#TimePicker').val();

            var c = $('#DropDownList').val();

            alert("You are booked the table with date " + a + " time " + b + " Party_size is " + c);

        }

    &lt;/script&gt;



The following screenshot displays the **acknowledgement****message**.



{% include image.html url="\js\TimePicker\getting-started_images\getting-started_img18.png" Caption="Figure 18: Acknowledgement Message"%}



**Create Two TimePickers**

You can select the **Start****time** in the first **TimePicker** and then the **End****time** in the second **TimePicker**. The validation process is done after the selection of **Start****time** and the changes are reflected in the **End****time** selection **TimePicker**. You can manipulate this process in the **Select** event of **Start Time** selection **TimePicker**. 

1. Add input element to render **Two TimePickers**.



**[ASPX]**

&lt;table&gt;

        &lt;tr&gt;

            &lt;td class="tdclass"&gt;

                Select Date

            &lt;/td&gt;

            &lt;td class="tdclass"&gt;

                Select start time

            &lt;/td&gt;

            &lt;td class="tdclass"&gt;

                Select end time

            &lt;/td&gt;

            &lt;td class="tdclass"&gt;

                Select party size

            &lt;/td&gt;

        &lt;/tr&gt;

        &lt;tr&gt;

            &lt;td class="tdclass"&gt;

                &lt;span class="innerdp"&gt;

                    &lt;ej:DatePicker ID="DatePicker" runat="server" /&gt;

                &lt;/span&gt;

            &lt;/td&gt;

            &lt;td class="tdclass"&gt;

                &lt;span class="innerdp"&gt;

                    <ej:TimePicker ID="TimePicker" ClientSideOnSelect="selectedStartTime" MinTime="9:00:00"

                        MaxTime="18:00:00" Interval="60" runat="server" />

                &lt;/span&gt;

            &lt;/td&gt;

            &lt;td class="tdclass"&gt;

                &lt;span class="innerdp"&gt;

                    <ej:TimePicker ID="TimePickerEnd" MinTime="9:00:00" MaxTime="18:00:00" Interval="60"

                        runat="server" />

                &lt;/span&gt;

            &lt;/td&gt;

            &lt;td class="tdclass"&gt;

                &lt;span class="innerdp"&gt;

                    &lt;ej:DropDownList name="party_size" ID="DropDownList" SelectedItemIndex="0" runat="server"&gt;

                        &lt;Items&gt;

                            &lt;ej:DropDownListItem Text="select people"&gt;

                            &lt;/ej:DropDownListItem&gt;

                            &lt;ej:DropDownListItem Text="5 people"&gt;

                            &lt;/ej:DropDownListItem&gt;

                            &lt;ej:DropDownListItem Text="10 people"&gt;

                            &lt;/ej:DropDownListItem&gt;

                            &lt;ej:DropDownListItem Text="15 people"&gt;

                            &lt;/ej:DropDownListItem&gt;

                            &lt;ej:DropDownListItem Text="20 people"&gt;

                            &lt;/ej:DropDownListItem&gt;

                        &lt;/Items&gt;

                    &lt;/ej:DropDownList&gt;

                &lt;/span&gt;

            &lt;/td&gt;

        &lt;/tr&gt;

        &lt;tr&gt;

            &lt;td class="tdclass"&gt;

                &lt;ej:Button ID="Book" Type="Button" Text="Book" ClientSideOnClick="acknowledge" runat="server"&gt;

                &lt;/ej:Button&gt;

            &lt;/td&gt;

            &lt;td&gt;

            &lt;/td&gt;

            &lt;td class="tdclass"&gt;

            &lt;/td&gt;

            &lt;td class="tdclass"&gt;

            &lt;/td&gt;

        &lt;/tr&gt;

    &lt;/table&gt;



2. To display acknowledge message using following script.



**[Script]**

&lt;script type="text/javascript"&gt;

        function acknowledge() {

            var a = $('#DatePicker').val();

            var b = $('#TimePicker').val();

            var c = $('#DropDownList').val();

            alert("You are booked the table with date " + a + " time " + b + " Party_size is " + c);

        }

        function selectedStartTime(sender) {

            var selDate = sender.value; // mentions the selected time.

            minTimepicker = $("#TimePickerEnd").data("ejTimePicker"); // creating TimePicker object

            minTimepicker.setModel({ "minTime": selDate }); // setting minTime property through setModel of TimePicker object.

        }

    &lt;/script&gt;



Execute the above code to achieve the desired result. By selecting the **Start Time** in the first **TimePicker**, you can select the **End Time** within the given range. This restricts you from selecting false time. This scenario is illustrated in the following screenshot.



{% include image.html url="\js\TimePicker\getting-started_images\getting-started_img19.png" Caption="Figure 19: Two TimePickers"%}

You can also add additional functionalities such as localization and time formats to the **TimePicker**. 

