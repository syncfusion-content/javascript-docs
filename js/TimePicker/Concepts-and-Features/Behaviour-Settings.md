---
layout: post
title: Behaviour-Settings
description: behaviour settings
platform: js
control: TimePicker
documentation: ug
---

# Behaviour Settings

## Set value of the TimePicker widget

You can use value property to set default time for the **TimePicker**.

The following steps explains you on how to set the default value of the **TimePicker**.

In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.



<table>
<tr>
<td>
<b>[HTML]</b>         &lt;input type="text" id="time" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// Set default value of the TimePicker as follows.</b>$(function () {            $('#time').ejTimePicker({             value: "10:10 AM"              });});</td></tr>
</table>
Execute the above code to render the following output.

{% include image.html url="/js/TimePicker/Concepts-and-Features/Behaviour-Settings_images/Behaviour-Settings_img1.png" Caption="TimePicker default value"%}

## Enable/Disable TimePicker widget

**TimePicker** widget provides you an option to enable /disable the widget. You can disable the TimePicker by setting the “**enabled**” property value as **false**.

The following steps explain you to enable/disable property in **TimePicker** widget.

In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.



<table>
<tr>
<td>
<b>[HTML]</b>         &lt;input type="text" id="time" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// To enable/disable TimePicker controls use the following code example.</b><br><b>Enable Timepicker:</b>$(function () {            $('#time').ejTimePicker();            var timeObj = $('#time').data("ejTimePicker");            timeObj.enable();        });<b>Disable Timepicker:</b>$(function () {            $('#time').ejTimePicker();            var timeObj = $('#time').data("ejTimePicker");            timeObj.disable();        });</td></tr>
</table>


Execute the above code to render the following output.

{% include image.html url="/js/TimePicker/Concepts-and-Features/Behaviour-Settings_images/Behaviour-Settings_img2.png" Caption="Enable TimePicker widget"%}

{% include image.html url="/js/TimePicker/Concepts-and-Features/Behaviour-Settings_images/Behaviour-Settings_img3.png" Caption="Disable TimePicker widget."%}

## Restrict editing

**TimePicker** widget provides **readOnly** property to disable editing in the control. Therefore you can only read the value set to **TimePicker** and cannot modify it. The **value** property allows you to set the default value for **TimePicker** widget when it is created.

### Configure TimePicker textbox to restrict editing

The following steps allows you to disable editing value in **TimePicker**.

In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.



<table>
<tr>
<td>
<b>[HTML]</b>         &lt;input type="text" id="time" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// Configure delay time for PopUp panel in TimePicker control as follows,</b>    $('#time').ejTimePicker({                <b>readOnly:true</b>                });</td></tr>
</table>


The following screenshot illustrates a **TimePicker** textbox configured to restrict editing.

{% include image.html url="/js/TimePicker/Concepts-and-Features/Behaviour-Settings_images/Behaviour-Settings_img4.png" Caption="TimePicker with PopUp button and enable readOnly property"%}

## Rounded Corner

You can customize the shape of the **TimePicker** widget from regular rectangular shape to rounded rectangle shape using **showRoundedCorner** property that is set to **false** by default.

### Configure Rounded corner to TimePicker Text box

The following steps explain you to change the edges of the textbox to rounded corner.

In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.



<table>
<tr>
<td>
<b>[HTML]</b>         &lt;input type="text" id="time" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// You can configure Rounded Corner  in TimePicker control as follows,</b>    $('#time').ejTimePicker({                <b>showRoundedCorner:true</b>,                });</td></tr>
</table>
The following screenshot illustrates a **TimePicker** when **showRoundedCorner** is set to “**true**”.

{% include image.html url="/js/TimePicker/Concepts-and-Features/Behaviour-Settings_images/Behaviour-Settings_img5.png" Caption="Rounded corner of TimePicker Textbox"%}

## Scaling

**TimePicker** widget provides you options to change its height, width and also to change popup height and width.

### Change TimePicker widget Height and width

You can use **height** and **width** property to customize **TimePicker** width and height.

In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;input type="text" id="time" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// You can customize the width and height of the TimePicker as follows.</b>$(function () {                $('#time').ejTimePicker({                 width: 150,                height: 50        }); });</td></tr>
</table>


Execute the above code to render the following output.

{% include image.html url="/js/TimePicker/Concepts-and-Features/Behaviour-Settings_images/Behaviour-Settings_img6.png" Caption="Changing width and height of the TimePicker."%}

### Changing TimePicker PopupHeight and PopupWidth

You can use **popupHeight** and **popupWidth** property to customize **TimePicker** width and height.

In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.


<table>
<tr>
<td>
<b>[HTML]</b>       &lt;input type="text" id="time" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// Use popupHeight and popupWidth property for the TimePicker as follows.</b>$(function () {                $('#time').ejTimePicker({                 popupHeight: 170,                popupWidth: 120        }); });</td></tr>
</table>


Execute the above code to render the following output.

{% include image.html url="/js/TimePicker/Concepts-and-Features/Behaviour-Settings_images/Behaviour-Settings_img7.png" Caption="Changing popup height and width"%}

## State persistence

**TimePicker** widget provide options to maintain the selected value after you refresh the page by using **enablePersistence** property.

### Steps to use State persistence of the TimePicker

The following steps explains you to use **enablePersistence** property.

In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;input type="text" id="time" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// Use enablePersistence property to maintain selected value as follows.</b>$(function () {                $('#time').ejTimePicker({                 value:"10:00 AM",                <b>enablePersistence: true</b>        }); });</td></tr>
</table>
## Strict mode of the TimePicker

**TimePicker** widget provides you an option to set default value when there is no default value between minTime and maxTime by using **enableStrictMode** property.  

### Steps to use StrictMode property

The following steps explains you to use strict mode property.

In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.


<table>
<tr>
<td>
<b>[HTML]</b>       &lt;input type="text" id="time" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// Use enableStrictMode property to set default value as follows.</b>    $(function () {        $('#time').ejTimePicker({         value : "9:00 AM",        enableStrictMode: true,        minTime: "10:00 AM",        maxTime: "9:00 PM"    });});</td></tr>
</table>


Execute the above code to render the following output.


{% include image.html url="/js/TimePicker/Concepts-and-Features/Behaviour-Settings_images/Behaviour-Settings_img8.png" Caption="Using enableStrictMode property"%}

## Interval

**TimePicker** widget provides you an option to change the interval of the hour, minute and seconds. 

### Steps to change the Time interval of the TimePicker control

The following steps explains you to change the Time Interval of the **TimePicker**.

In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;input type="text" id="time" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// Change Time Interval using hourInterval, minuteInterval and secondInterval property.</b>$(function () {                $('#time').ejTimePicker({                 value : "9:00 AM",                timeFormat: "h:mm:ss tt",                hourInterval:2,                minutesInterval:30,                secondsInterval:20        }); });</td></tr>
</table>


