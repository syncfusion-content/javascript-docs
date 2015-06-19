---
layout: post
title: Behavior-Settings
description: behavior settings
platform: js
control: DatePicker
documentation: ug
---

# Behavior Settings

## Button Text

Set the display text for the **Button** in the **DatePicker** popup. By default, **buttonText** is set **Today** (String). Change this default value by using **ButtonText** property to change the **Button Text**.

The following steps explains how to set the **Button Text** for **DatePicker** widget.

* In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget.

<table>
<tr>
<td>
<b>[HTML]</b>    &lt;input id="datepicker" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the code to set the Button Text of DatePicker widget&lt;script type="text/javascript"&gt;        $(function () {            // declaration            $("#datepicker").ejDatePicker({                buttonText: "Todaydate"             });        });    &lt;/script&gt;</td></tr>
</table>
The following screenshot displays the output for the above code.

{% include image.html url="/js/DatePicker/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img1.png" Caption="Button Text in DatePicker	  		"%}

## Display Default Date

You can allow to display default date value in input textbox. By default “**displayDefaultDate**” property is set to ‘**true**’ in **DatePicker** widget. 

The following steps explain **displayDefaultDate** in **DatePicker** widget.	

* In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget

<table>
<tr>
<td>
<b>[HTML]</b>    &lt;input id="datepicker" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the code to set the displayDefaultDate in DatePicker widget&lt;script type="text/javascript"&gt;        $(function () {            // declaration            $("#datepicker").ejDatePicker({                displayDefaultDate: false,                value: new Date("5/8/2014")                            });        });    &lt;/script&gt;</td></tr>
</table>
## Enabled

You can **Enable** or **Disable** the **DatePicker** widget. By default “**enabled**” property is set to ‘**true**’ in **DatePicker** widget. You can disable the **DatePicker** widget by setting “**enabled**” property as ‘**false**’.

The following steps explain you how to disable the **DatePicker** widget.

* In the HTML page, add a **&lt;input&gt;** element to render **DatePicker** widget.

<table>
<tr>
<td>
<b>[HTML]</b>    &lt;input id="datepicker" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the code to disable the DatePicker widget&lt;script type="text/javascript"&gt;        $(function () {            // declaration            $("#datepicker").ejDatePicker({                enabled: false            });        });    &lt;/script&gt;</td></tr>
</table>
## Enable strict mode

When **enableStrictMode** is set to ‘**true**’, **DatePicker** doesn’t allow the value out of the range, it is internally changed to the correct value. . By default “**enableStrictMode**” property is set as ‘**false**’ in **DatePicker**.

The following steps explain you how to enable the “**enableStrictMode**” for **DatePicker** widget.

* In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** Widget

<table>
<tr>
<td>
<b>[HTML]</b>    &lt;input id="datepicker" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the code to enable the enableStrictMode for DatePicker widget&lt;script type="text/javascript"&gt;        $(function () {            // declaration            $("#datepicker").ejDatePicker({                enableStrictMode: true            });        });    &lt;/script&gt;</td></tr>
</table>
## Fields

You can specify the **fields****mapping** in **DatePicker**. You can also provide the support to add image, image styles, sprite css class, query, and HTML attributes.

The **DatePicker** widget provides support to customize the particular date. i.e. you can customize the date with image and tooltip options. The following table specifies the special date fields and its configuration.

_Special dates fields table_

<table>
<tr>
<td>
<b>Name</b></td><td>
<b>Description</b></td><td>
<b>Default value</b></td><td>
<b>Data type</b></td></tr>
<tr>
<td>
date</td><td>
The date that needs to be customized. </td><td>
Null </td><td>
String </td></tr>
<tr>
<td>
tooltip</td><td>
Shows  the tooltip to mention date while mouse hovering </td><td>
Null </td><td>
String </td></tr>
<tr>
<td>
icon </td><td>
You can set the customized css with this property. Note: You need to set the image as background url and its styles within this class</td><td>
Null </td><td>
String</td></tr>
</table>
The following steps explain you how to specify the **fields****mapping** in **DatePicker** widget.

* In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget

<table>
<tr>
<td>
<b>[HTML]</b>    &lt;input id="datepicker" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the code to specify the fields mapping in DatePicker widget&lt;script type="text/javascript"&gt;    $(function () {        var today = new Date(),                       spldays = [                              { date: new Date(today.getFullYear(), today.getMonth(), 1), tooltip: "In America", icon: "flag-am" },                              { date: new Date(today.getFullYear(), today.getMonth() + 1, 6), tooltip: "In Argendina", icon: "flag-ar" },                              { date: new Date(today.getFullYear(), today.getMonth() + 1, 27), tooltip: "In Bangladesh", icon: "flag-bd" },                              { date: new Date(today.getFullYear(), today.getMonth() - 1, 3), tooltip: "In Brasil", icon: "flag-br" },                              { date: new Date(today.getFullYear(), today.getMonth() - 2, 22), tooltip: "In Canada", icon: "flag-ca" },                       ]        // declaration        $("#datepicker").ejDatePicker({            specialDates: spldays,            fields: { date: "date", tooltip: "tooltip", icon: "icon" }        });    });&lt;/script&gt;</td></tr>
</table>
* Add the following styles to specify the **fields mapping** in **DatePicker** widget.



> _**Note: Images for this example are available in ‘installed location /Content/images’ and you need to define images in mentioned CSS. Henceforth the images are displayed.**_



{% highlight css %}

**[CSS]**
<style type="text/css" class="cssStyles">
    .flag .e-image {
        background: url("../Content/flags.png") no-repeat scroll -50px -75px rgba(0, 0, 0, 0);
        float: left;
        height: 15px;
        margin-left: 5px;
        margin-top: 3px;
        width: 20px;
    }

    .e-datepicker.e-calendar {
        width: 350px;
    }
</style>


{% endhighlight %}

The following screenshot displays the output for the above code.

{% include image.html url="/js/DatePicker/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img2.png" Caption="Fields mapping in DatePicker"%}

## Define start day of the week

It specifies the **start day of the week** in **DatePicker** calendar. By default “**value**” is set to **0** (Sunday). 

The following steps explain you how to specify the **start day of the week** in **DatePicker** widget.

* In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget

<table>
<tr>
<td>
<b>[HTML]</b>    &lt;input id="datepicker" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the code to specify the start day of the week in DatePicker widget&lt;script type="text/javascript"&gt;        $(function () {            // declaration            $("#datepicker").ejDatePicker({                startDay: 2            });        });    &lt;/script&gt;</td></tr>
</table>
The following screenshot displays the output for the above code.

{% include image.html url="/js/DatePicker/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img3.png" Caption="Start day of the week in DatePicker"%}

## Step months

It specifies the number of months to navigate at one click in next and previous button that is achieved by “**stepMonths”** property**.** You can change the **step months** by changing the default value using “**stepMonths”** property. 

The following steps explain you how to specify the number of months to navigate at one click

*  In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget

<table>
<tr>
<td>
<b>[HTML]</b>    &lt;input id="datepicker" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the code to specify the number of months to navigate at one click&lt;script type="text/javascript"&gt;        $(function () {            // declaration            $("#datepicker").ejDatePicker({                stepMonths: 2            });        });    &lt;/script&gt;</td></tr>
</table>
##  Define value

It specifies the selected date value. You can specify the selected date value by using “**value”** property.

The following steps explain you how to specify the selected value.

*  In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget

<table>
<tr>
<td>
<b>[HTML]</b>    &lt;input id="datepicker" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the code to specify the selected date value&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#datepicker").ejDatePicker({            value: new Date("5/8/2014")        });    });    &lt;/script&gt;</td></tr>
</table>
The following screenshot displays the output for the above code.

{% include image.html url="/js/DatePicker/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img4.png" Caption="Value in DatePicker"%}

## Watermark Text

It specifies the **Watermark Text** to display the input text in **DatePicker**. By default “**watermarkText”** property is set as “**select date**” in **DatePicker**. 

The following steps explain you how to specify the **watermark Text** in **DatePicker** widget

*  In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget

<table>
<tr>
<td>
<b>[HTML]</b>    &lt;input id="datepicker" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the code to specify Watermark Text to be display in input text&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#datepicker").ejDatePicker({            watermarkText: "Enter date"        });    });&lt;/script&gt;</td></tr>
</table>
The following screenshot displays the output for the above code.

{% include image.html url="/js/DatePicker/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img5.png" Caption="Watermark Text in DatePicker"%}

