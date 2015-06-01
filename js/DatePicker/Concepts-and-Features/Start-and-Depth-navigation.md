---
layout: post
title: Start-and-Depth-navigation
description: start and depth navigation
platform: js
control: DatePicker
documentation: ug
---

# Start and Depth navigation

## Start Level

It specifies the **Start Level** view in **DatePicker** calendar. By default “**startLevel”** property is set to **ej.DatePicker.Level.Month.**

_Table_ _3__: Start level_

<table>
<tr>
<td>
<b>Name </b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
month</td><td>
Starts from month level view.</td></tr>
<tr>
<td>
year</td><td>
Starts from year level view.</td></tr>
<tr>
<td>
decade</td><td>
Starts from decade level view.</td></tr>
<tr>
<td>
century</td><td>
Starts from century level view.</td></tr>
</table>


The following steps explain you how to specify the **Start Level** view in **DatePicker** widget.

* In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget

<table>
<tr>
<td>
<b>[HTML]</b>    &lt;input id="datepicker" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Add the code to specify the <b>Start Level</b> view in <b>DatePicker</b> widget&lt;script type="text/javascript"&gt;        $(function () {            // declaration            $("#datepicker").ejDatePicker({<b>                startLevel: ej.DatePicker.Level.Century</b>            });        });    &lt;/script&gt;</td></tr>
</table>


* The following screenshot displays the output for the above code.

{% include image.html url="/js/DatePicker/Concepts-and-Features/Start-and-Depth-navigation_images/Start-and-Depth-navigation_img1.png" Caption="Figure 19:Start level view in DatePicker               "%}

## Depth Level

It specifies the drill down level of **DatePicker**. You can restrict the drill down **Depth Level** using “**depthLevel”** property. 

It accepts the following values. 

_Table_ _4__: Depth level_

<table>
<tr>
<td>
<b>Value</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
month</td><td>
Starts from month level view.</td></tr>
<tr>
<td>
year</td><td>
Starts from year level view.</td></tr>
<tr>
<td>
decade</td><td>
Starts from year decade level view.</td></tr>
<tr>
<td>
century</td><td>
Starts from century level view. </td></tr>
</table>


The following steps explain you how to get the **Depth Level.**

* In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget

<table>
<tr>
<td>
<b>[HTML]</b>    &lt;input id="datepicker" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Add the code to render the <b>Depth Level</b>&lt;script type="text/javascript"&gt;        $(function () {            // declaration            $("#datepicker").ejDatePicker({            startLevel:ej.DatePicker.Level.Century,             <b>depthLevel: ej.DatePicker.Level.Year</b>            });        });  &lt;/script&gt;</td></tr>
</table>


* The following screenshot displays the output for the above code.

{% include image.html url="/js/DatePicker/Concepts-and-Features/Start-and-Depth-navigation_images/Start-and-Depth-navigation_img2.png" Caption="Figure 20: Depth Level in DatePicker"%}

