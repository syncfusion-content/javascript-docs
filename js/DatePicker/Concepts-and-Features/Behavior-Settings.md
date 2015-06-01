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
<b>[JavaScript]</b><b>// </b>Add the code to set the <b>Button Text</b> of <b>DatePicker</b> widget&lt;script type="text/javascript"&gt;        $(function () {            // declaration            $("#datepicker").ejDatePicker({<b>                buttonText: "Todaydate" </b>            });        });    &lt;/script&gt;</td></tr>
</table>


* The following screenshot displays the output for the above code.



{% include image.html url="/js/DatePicker/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img1.png" Caption="Figure 6: Button Text in DatePicker"%}



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
<b>[JavaScript]</b><b>//</b> Add the code to set the <b>displayDefaultDate</b> in <b>DatePicker</b> widget&lt;script type="text/javascript"&gt;        $(function () {            // declaration            $("#datepicker").ejDatePicker({<b>                displayDefaultDate: false,</b><b>                </b>value: new Date("5/8/2014")<b>                </b>            });        });    &lt;/script&gt;</td></tr>
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
<b>[JavaScript]</b><b>// </b>Add the code to disable the <b>DatePicker</b> widget&lt;script type="text/javascript"&gt;        $(function () {            // declaration            $("#datepicker").ejDatePicker({<b>                enabled: false</b>            });        });    &lt;/script&gt;</td></tr>
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
<b>[JavaScript]</b><b>// </b>Add the code to enable the <b>enableStrictMode</b> for <b>DatePicker</b> widget&lt;script type="text/javascript"&gt;        $(function () {            // declaration            $("#datepicker").ejDatePicker({<b>                enableStrictMode: true</b>            });        });    &lt;/script&gt;</td></tr>
</table>


## Fields

You can specify the **fields****mapping** in **DatePicker**. You can also provide the support to add image, image styles, sprite css class, query, and HTML attributes.

The **DatePicker** widget provides support to customize the particular date. i.e. you can customize the date with image and tooltip options. The following table specifies the special date fields and its configuration.

_Table_ _1__:_ _special dates fields____table_

<table>
<tr>
<td>
Name</td><td>
Description</td><td>
Default value</td><td>
Data type</td></tr>
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
you can set the customized css with this property. > <img src="Behavior-Settings_images\Behavior-Settings_img2.jpeg" alt="" width="18pt" height="18pt"<i><b>Note: You need to set the image as background url and its styles within this class</b></i></td><td>
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
<b>[JavaScript]</b><b>// </b>Add the code to specify the <b>fields mapping</b> in <b>DatePicker</b> widget&lt;script type="text/javascript"&gt;    $(function () {        var today = new Date(),                       spldays = [                              { date: new Date(today.getFullYear(), today.getMonth(), 1), tooltip: "In America", icon: "flag-am" },                              { date: new Date(today.getFullYear(), today.getMonth() + 1, 6), tooltip: "In Argendina", icon: "flag-ar" },                              { date: new Date(today.getFullYear(), today.getMonth() + 1, 27), tooltip: "In Bangladesh", icon: "flag-bd" },                              { date: new Date(today.getFullYear(), today.getMonth() - 1, 3), tooltip: "In Brasil", icon: "flag-br" },                              { date: new Date(today.getFullYear(), today.getMonth() - 2, 22), tooltip: "In Canada", icon: "flag-ca" },                       ]        // declaration        $("#datepicker").ejDatePicker({            specialDates: spldays,            <b>fields: { date: "date", tooltip: "tooltip", icon: "icon" }</b>        });    });&lt;/script&gt;</td></tr>
</table>




* Add the following styles to specify the **fields mapping** in **DatePicker** widget.

> {% include image.html url="/js/DatePicker/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img3.jpeg" Caption=""%}_**Note: Images for this example are available in ‘installed location /Content/images’ and you need to define images in mentioned CSS. Henceforth the images are displayed.**_



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





*  The following screenshot displays the output for the above code.

{% include image.html url="/js/DatePicker/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img4.png" Caption="Figure 7: Fields mapping in DatePicker"%}

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
<b>[JavaScript]</b><b>// </b>Add the code to specify the <b>start day of the week</b> in <b>DatePicker</b> widget&lt;script type="text/javascript"&gt;        $(function () {            // declaration            $("#datepicker").ejDatePicker({<b>                startDay: 2</b>            });        });    &lt;/script&gt;</td></tr>
</table>


* The following screenshot displays the output for the above code.

{% include image.html url="/js/DatePicker/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img5.png" Caption="Figure 8: Start day of the week in DatePicker"%}

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
<b>[JavaScript]</b><b>// </b>Add the code to specify the number of months to navigate at one click&lt;script type="text/javascript"&gt;        $(function () {            // declaration            $("#datepicker").ejDatePicker({<b>                stepMonths: 2</b>            });        });    &lt;/script&gt;</td></tr>
</table>


## Define value

It specifies the selected date value. You can specify the selected date value by using “**value”** property.

The following steps explain you how to specify the selected value.

*  In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget

<table>
<tr>
<td>
<b>[HTML]</b>    &lt;input id="datepicker" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the code to specify the selected date value&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#datepicker").ejDatePicker({            <b>value: new Date("5/8/2014")</b>        });    });    &lt;/script&gt;</td></tr>
</table>


*  The following screenshot displays the output for the above code.



{% include image.html url="/js/DatePicker/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img6.png" Caption="Figure 9: Value in DatePicker"%}

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
<b>[JavaScript]</b><b>// </b>Add the code to specify <b>Watermark</b> <b>Text</b> to be display in input text&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#datepicker").ejDatePicker({            <b>watermarkText: "Enter date"</b>        });    });&lt;/script&gt;</td></tr>
</table>


* The following screenshot displays the output for the above code.



{% include image.html url="/js/DatePicker/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img7.png" Caption="Figure 10: Watermark Text in DatePicker"%}

