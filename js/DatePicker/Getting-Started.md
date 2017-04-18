---
layout: post
title: Getting started with DatePicker
description: To get start with DatePicker by adding references.
platform: js
control: DatePicker
documentation: ug
api: /api/js/ejdatepicker
---
# Getting Started

## A new HTML document and required codes

To get start with DatePicker, create a new HTML file and refer the below specified dependent CSS file as well as scripts files.

CSS file

* [ej.web.all.min.css](http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css) – includes all widgets styles (To know more about theme refer [Theming in Essential JavaScript Component](https://help.syncfusion.com/js/theming-in-essential-javascript-components#))

External script files

* [jQuery](http://jquery.com/#) (from the version 1.7.1 to 3.1.0)

N> From V13.4.0.53 onwards, jQuery.globalize.min.js file has been replaced with our script file ej.globalize.min.js to support the globalization for our widgets. For version lower than 13.4.0.53, refer jQuery.globalize.min.js. jQuery.easing external dependency has been removed from version 14.3.0.49 onwards. Kindly include this jQuery.easing dependency for versions lesser than 14.3.0.49 in order to support animation effects.

Internal script files

<table>
<tr>
<th>
File </th><th>
Description / Usage </th></tr>
<tr>
<td>
ej.core.min.js<br/><br/></td><td>
Includes only the widget basic functions and Framework features. Must be referred always before using all the JS controls<br/><br/></td></tr>
<tr>
<td>
ej.globalize.min.js<br/><br/></td><td>
To support the globalization.<br/><br/></td></tr>
<tr>
<td>
ej.datepicker.min.js<br/><br/></td><td>
DatePicker plugin.<br/><br/></td></tr>
</table>

N> From V13.4.0.53 onwards, jQuery.globalize.min.js file has been replaced with our script file ej.globalize.min.js to support the globalization for our widgets. For version lower than 13.4.0.53, refer jQuery.globalize.min.js.

You can make use of ‘ej.web.all.min.js’ file which encapsulates all ‘ej’ web components and frameworks in single file.

* [ej.web.all.min.js](http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js) – includes all web widgets.

N>  In production, we highly recommend you to use our [custom script generator](https://help.syncfusion.com/js/include-only-the-needed-widgets#) to create custom script file with required controls and its dependencies only. Also to reduce the file size further please use [GZip compression](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer?hl=en#text-compression-with-gzip) in your server. 

A simple HTML file with required CSS and script reference added to create DatePicker

{% highlight html %}

    <!DOCTYPE html>

    <html>

    <head>

        <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />

        <!-- style sheet for default theme(flat azure) -->

        <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css"
              rel="stylesheet" />

        <!--scripts-->

        <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.11.3.min.js"></script>

        <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>

    </head>

    <body>

        <!--Place input element to create DatePicker-->

        <script>

            // Place your script code here to initialize DatePicker

        </script>

    </body>

    </html>

{% endhighlight %}

## DatePicker Initialization

DatePicker can be created using ‘input’ element

{% highlight html %}

    <!--input element to create DatePicker-->

    <input id="datePicker" />

{% endhighlight %}

{% highlight javascript %}

        $(function () {

            // initialize DatePicker component

            $("#datePicker").ejDatePicker();

        });

{% endhighlight %}

N>  DatePicker is a form control, so on form submitting its value can be retrieved by its **name**. By default **id** has been treated as name, if ‘name’ attribute is not specified.

## Get / Set value

DatePicker provides an options to configure all its properties and get its value. DatePicker value can be assigned during initialization or at run time. Below code shows how to assign values at initialization.

{% highlight javascript %}


        $(function () {

            // create DatePicker from input with current date value.

            $("#datePicker").ejDatePicker({

                value: new Date(), // sets the current date

                dateFormat: "yyyy/MM/dd" // sets the date format

            });

        });

{% endhighlight %}

You can assign values after initialization in DatePicker (‘it helps to get or set value at run time). Let’s consider that going to set date value at button click.

{% highlight javascript %}

        //bind below onClick action to button

        function onClick() {

            //create instance for datePicker.

            // only after control creation we can get dateObj otherwise it throws exception.

            var dateObj = $("#datePicker").ejDatePicker('instance');

            //set value using date object

            dateObj.option('value', new Date());

            //get value using date object and displays in alert box

            alert(dateObj.option('value'));

        }

{% endhighlight %}

N>  Existing DatePicker instance can be created by [jQuery.data()](http://api.jquery.com/jQuery.data/#) and you can control the API’s of DatePicker behavior.

