---
layout: post
title: behaviour-settings
description: behaviour settings
platform: js
control: TimePicker
documentation: ug
---

# Behaviour Settings

## Set value of the TimePicker widget

You can use value property to set default time for the **TimePicker**.

The following steps explains you on how to set the default value of the **TimePicker**.

* In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.



<table>
<tr>
<td>
<b>[HTML]</b>         &lt;input type="text" id="time" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// Set default value of the TimePicker as follows.</b>$(function () {            $('#time').ejTimePicker({             value: "10:10 AM"              });});</td></tr>
</table>


**[_cshtml]**

**// Add the following code in your view page to render RTE with given time value.**



       @Html.EJ().TimePicker("time").**Value("10:10 AM")**



**[_**aspx**]**

**//** Add the code in ASPX page to render RTE with given time value

      &lt;ej:TimePicker ID="time" Value="10:10 AM" runat="server"&gt;&lt;/ej:TimePicker&gt;



Execute the above code to render the following output.

![](behaviour-settings_images\behaviour-settings_img1.png)

_Figure___ _11__24__:_ _TimePicker_ _default value_

## Enable/Disable TimePicker widget

**TimePicker** widget provides you an option to enable /disable the widget. You can disable the TimePicker by setting the “**eEnabled**” property value as **false**.

The following steps explain you to enable/disable property in **TimePicker** widget.

* In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.



<table>
<tr>
<td>
<b>[HTML]</b>         &lt;input type="text" id="time" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// To enable/disable TimePicker controls use the following code example.</b><br><b>Enable Timepicker:</b>$(function () {            $('#time').ejTimePicker();            var timeObj = $('#time').data("ejTimePicker");            timeObj.enable();        });<b>Disable Timepicker:</b>$(function () {            $('#time').ejTimePicker();            var timeObj = $('#time').data("ejTimePicker");            timeObj.disable();        });</td></tr>
</table>


**[_cshtml]**

**// Add the following code in your view page to render disabled TimePicker.**



@Html.EJ().TimePicker("timepick").**Enabled(false)**





**[_**aspx**]**

**//** Add the code in ASPX page to render Disabled TimePicker

        &lt;ej:TimePicker ID="Timepick" Enabled="true" runat="server"&gt;&lt;/ej:TimePicker&gt;



Execute the above code to render the following output.


<table>
<tr>
<td>
<img src="behaviour-settings_images\behaviour-settings_img2.png" alt="" width="246pt" height="114pt"<i>Figure </i><i>12</i><i>25</i><i>: Enable </i><i>TimePicker</i><i> widget.</i></td><td>
<img src="behaviour-settings_images\behaviour-settings_img3.png" alt="" width="246pt" height="112pt"<i>Figure </i><i>13</i><i>26</i><i>: </i><i>Disable </i><i>TimePicker</i><i> widget.</i></td></tr>
</table>
## Restrict editing

**TimePicker** widget provides **readOnly** property to disable editing in the control. Therefore you can only read the value set to **TimePicker** and cannot modify it. The **value** property allows you to set the default value for **TimePicker** widget when it is created.

### Configure TimePicker textbox to restrict editing

The following steps allows you to disable editing value in **TimePicker**.

* In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget



<table>
<tr>
<td>
<b>[HTML]</b>         &lt;input type="text" id="time" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// Configure delay time for PopUp panel in TimePicker control as follows,</b>    $('#time')$('#time).ejTimePicker({                <b>readOnly:true</b>                });</td></tr>
</table>


**[_cshtml]**

**// Add the following code in your view page to render timepicker.**



         @Html.EJ().TimePicker("time").**ReadOnly(true)**



[_aspx]

**//** Add the code in ASPX page to render TimePicker

  &lt;ej:TimePicker ID="time" ReadOnly="true" runat="server"&gt;&lt;/ej:TimePicker&gt;



The following screenshot illustrates a **TimePicker** textbox configured to restrict editing.



![](behaviour-settings_images\behaviour-settings_img4.png)

_Figure_ _27__14__:_ _TimePicker_ _with_ _PopUp_ _button and enable readOnly property_

## Rounded Corner

You can customize the shape of the **TimePicker** widget from regular rectangular shape to rounded rectangle shape using **showRroundedCorner** property that is set to **false** by default.

### Configure Rounded corner to TimePicker Text box

The following steps explain you to change the edges of the textbox to rounded corner.

* In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.



<table>
<tr>
<td>
<b>[HTML]</b>         &lt;input type="text" id="time" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// You can configure Rounded Corner  in TimePicker control as follows,</b>    $('#time')$('#time).ejTimePicker({                <b>showRoundedCorner:true</b>,                });</td></tr>
</table>


**[_cshtml]**

**// Add the following code in your view page to render TimePicker.**



         @Html.EJ().TimePicker("time").**ShowRoundedCorner(true)**



[_aspx]

**//** Add the code in ASPX page to render TimePicker

&lt;ej:TimePicker ID="time" ShowRoundedCorner="true" runat="server"&gt;&lt;/ej:TimePicker&gt;



The following screenshot illustrates a **TimePicker** when **showRoundedCorner** is set to “**true**”.



![](behaviour-settings_images\behaviour-settings_img5.png)

_Figure_ _15__28__: Rounded corner of_ _**TimePicker**_ _Textbox_

## Scaling

**TimePicker** widget provides you options to change its height, width and also to change popup height and width.

### Change TimePicker widget Height and width

You can use **hHeight** and **width** property to customize **TimePicker** width and height.

* In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;input type="text" id="time" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// You can customize the width and height of the TimePicker as follows.</b>$(function () {                $('#time').ejTimePicker({                 wWidth: 150,                hHeight: 50        }); });</td></tr>
</table>


**[_cshtml]**

**// Add the following code to render TimePicker with specified height and width.**



     @Html.EJ().TimePicker("time").**Height**("50").**Width**("150")



**[_aspx]**

**//** Add the code in ASPX page to render TimePicker with specified height and width



    &lt;ej:TimePicker ID="time" Height="50" Width="150" runat="server"&gt;&lt;/ej:TimePicker&gt;



Execute the above code to render the following output.



![](behaviour-settings_images\behaviour-settings_img6.png)![](behaviour-settings_images\behaviour-settings_img7.png)

_Figure_ _16__29__: Changing width and height of the TimePicker._

### Changing TimePicker PopupHeight and PopupWidth

You can use **popupHeight** and **popupWidth** property to customize **TimePicker** width and height.

* In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.


<table>
<tr>
<td>
<b>[HTML]</b>       &lt;input type="text" id="time" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// Use popupHeight and popupWidth property for the TimePicker as follows.</b>$(function () {                $('#time').ejTimePicker({                 popupHeight: 170,                popupWidth: 120        }); });</td></tr>
</table>


**[_cshtml]**

**// In Html page, add a &lt;input&gt; element to configure TimePicker widget.**

****

      @Html.EJ().TimePicker("time").**PopupHeight**("170").**PopupWidth**("120")



**[_aspx]**

**//** Add the code in ASPX page 

      &lt;ej:TimePicker ID="time" PopupHeight="50" PopupWidth="150" runat="server"&gt;&lt;/ej:TimePicker&gt;



Execute the above code to render the following output.



![](behaviour-settings_images\behaviour-settings_img8.png)

_Figure_ _17__30__: Changing popup height and width_

## State persistence

**TimePicker** widget provide options to maintain the selected value after you refresh the page by using **enableState pPersistence** property.

### Steps to use State persistence of the TimePicker

The following steps explains you to use **enablePersistence** property.

* In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;input type="text" id="time" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// Use enablePersistence property to maintain selected value as follows.</b>$(function () {                $('#time').ejTimePicker({                 value:"10:00 AM"”10:00 AM”,                <b>enablePersistence: true</b>        }); });</td></tr>
</table>


**[_cshtml]**

**// Add the following code in your view page to render TimePicker.**



       @Html.EJ().TimePicker("time").Value("10:10 AM").**EnablePersistence**(**true**)





**[_aspx]**

**//** Add the code in ASPX page to render TimePicker

 &lt;ej:TimePicker ID="time" Value="10:10 AM" EnablePersistence="true" runat="server"&gt;&lt;/ej:TimePicker&gt;

## Strict mode of the TimePicker

**TimePicker** widget provides you an option to set default value when there is no default value between minTime and maxTime by using **enableStrictMode** property.  

### Steps to use StrictMode property

The following steps explains you to use strict mode property.

* In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.


<table>
<tr>
<td>
<b>[HTML]</b>       &lt;input type="text" id="time" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// Use enableStrictMode property to set default value as follows.</b>    $(function () {        $('#time').ejTimePicker({         value : "9:00 AM",        enableStrictMode: true,        minTime: "10:00 AM",        maxTime: "9:00 PM"    });});$(function () {                $('#time').ejTimePicker({                value = "9:00 AM";                enableStrictMode: true                minTime:”10:00 AM”,                maxTime: ”9:00 PM”        }); });</td></tr>
</table>


**[_cshtml]**

**// Add the following code in your view page to render TimePicker with specified min and max time.**



       @Html.EJ().TimePicker("time").Value("09:00 AM").MinTime("10:00 AM").MaxTime("09:00 PM").**EnableStrictMode**(**true**)





**[_aspx]**

**//** Add the code in ASPX page to render TimePicker with specified min and max time

&lt;ej:TimePicker ID="time" Value="09:00 AM" EnableStrictMode="true" MinTime="10:00 AM" MaxTime="09:00 PM" runat="server"&gt;&lt;/ej:TimePicker&gt;



Execute the above code to render the following output.


![](behaviour-settings_images\behaviour-settings_img9.png)

_Figure_ _3__1__8__: Using_ _enableStrictMode_ _property_

## Interval

**TimePicker** widget provides you an option to change the interval of the hour, minute and seconds. 

### Steps to change the Time interval of the TimePicker control

The following steps explains you to change the Time Interval of the **TimePicker**.

* In the **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;input type="text" id="time" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// Change Time Interval using hourInterval, minuteInterval and secondInterval property.</b>$(function () {                $('#time').ejTimePicker({                 value : = "9:00 AM",                timeFormat: "h:mm:ss tt"”h:mm:ss tt”,                hourInterval:2,                minutesInterval:30,                secondsInterval:20        }); });</td></tr>
</table>


**[_cshtml]**

**// Add the following code in your view page to render TimePicker.**



@{Html.EJ().TimePicker("time").Value("09:00 AM")

.TimeFormat("h:mm:ss tt")

.**HourInterval**(2).**MinutesInterval**(30).**SecondsInterval**(20).Render();}



**[_aspx]**

**//** Add the code in ASPX page to render TimePicker

      &lt;ej:TimePicker ID="time" Value="09:00 AM" TimeFormat="hh:mm:ss tt" HourInterval="2" MinutesInterval="30" SecondsInterval="20" runat="server"&gt;&lt;/ej:TimePicker&gt;



