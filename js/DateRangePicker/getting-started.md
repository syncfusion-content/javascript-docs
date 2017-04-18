---
layout: post
title: getting started
description: getting started
platform: js
control: DateRangePicker
documentation: ug
api: /api/js/ejdaterangepicker
---

# Getting Started

## New HTML Document and required codes:

To get start with **DateRangePicker**, create a new HTML file and refer the below specified dependent CSS file as well as scripts files.

**CSS file**

**ej.web.all.min.css** – includes all widgets styles (To know more about theme, refer Theming in Essential JavaScript Component)

**External script files**

**jQuery** (from the version 1.7.1 to 3.1.0)

**Internal script files**

<table>
<tr>
<td>
File </td><td>
Description / Usage</td></tr>
<tr>
<td>
ej.core.min.js<br></td><td>
Includes only the widget basic functions and Framework features. Must be referred always before using all the JS controls<br></td></tr>
<tr>
<td>
ej.scroller.min.js</td><td>
To enable the scroll bar with preset ranges if count exceeded</td></tr>
<tr>
<td>
ej.globalize.min.js<br></td><td>
To support the globalization.<br></td></tr>
<tr>
<td>
ej.datepicker.min.js<br></td><td>
DatePicker plugin.</td></tr>
<tr>
<td>
ej.timepicker.min.js</td><td>
TimePicker plugin</td></tr>
<tr>
<td>
ej.daterangepicker.min.js</td><td>
DateRangePicker Plugin</td></tr>
</table>
You can make use of ‘ej.web.all.min.js’ file which encapsulates all ‘ej’ web components and frameworks in single file.



**ej.web.all.min.js** – includes all web widgets.

**A simple HTML file with required CSS and script reference added to create DateRangePicker**


{% highlight html %}



<!DOCTYPE html>

<html>

<head>

    <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />

    <!-- style sheet for default theme(flat azure) -->

    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />

    <!--scripts-->

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.11.3.min.js"></script>

    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>

</head>

<body>

    <!--Place input element to create DateRangePicker-->

    <script>

            // Place your script code here to initialize DateRangePicker

    </script>

</body>

</html>


{% endhighlight %}



## DateRangePicker Initialization

DateRangePicker can be created using “input” tag.

{% highlight html %}

<!--input element to create DateRangePicker-->

    <input id="dateRangePicker" />
 
$(function () {

            // initialize DateRangePicker component

            $("#dateRangePicker").ejDateRangePicker();

        });

{% endhighlight %}


## Get/Set Value

DateRangePicker provides an options to configure all its properties and to get its value. DateRangePicker value can be assigned during initialization or at run time. Below code shows how to assign the values at initialization.

{% highlight js %}

$(function () {



            // initialize DateRangePicker component with Value API



            $("#dateRangePicker").ejDateRangePicker({

                value: "11/1/2013 - 12/3/2019", // sets the date range



            });



        });

{% endhighlight %}


You can assign values after initialization in DateRangePicker (‘it helps to get or set value at run time). Let’s consider that going to set date range at button click.


{% highlight html %}


//bind below onClick action to button



        function onClick() {



            //create instance for dateRangePicker.



            // create instance only after control creation, to get dateRangeObj otherwise it throws exception.



            var dateRangeObj = $("#dateRangePicker").ejDateRangePicker('instance');



            //set value using date range picker object



            dateRangeObj.option('value', "11/1/2013 - 12/3/2019");



            //get value using date range object and displays in alert box



            alert(dateRangeObj.option('value'));



        }


{% endhighlight %}



