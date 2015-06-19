---
layout: post
title: Start-and-Depth-level
description: start and depth level
platform: js
control: DateTimePicker
documentation: ug
---

# Start and Depth level

## Start Level

**DateTimePicker** allows you to change the starting level view of Calendar inside the **DateTimePicker** popup. Consider you are creating a login form for your blog. If the “Birth date” field in the form starts from year, it is easy to select date from year, month and date. By default, the Start Level of **DateTimePicker** is “Month” level view. Refer the following table to know the different types of start level.

_Table_ _3__: Start Level_

<table>
<tr>
<td>
<b>Start Level</b></td><td>
<b>Syntax</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
month</td><td>
startLevel: “month”</td><td>
Starts from month level view.</td></tr>
<tr>
<td>
year</td><td>
startLevel: “year”</td><td>
Starts from year level view.</td></tr>
<tr>
<td>
decade</td><td>
startLevel: “decade”</td><td>
Starts from year decade level view.</td></tr>
<tr>
<td>
century</td><td>
startLevel: “century”</td><td>
Starts from century level view.</td></tr>
</table>


In the following example **DateTimePicker** popup start level view is set to “century level” when you drop down the **DateTimePicker** popup.



* Add the following code in your **HTML** page.



<table>
<tr>
<td>
<b>[HTML]    </b>&lt;div class="control"&gt;        &lt;input type="text" id="dateTime" /&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Add the code in your script section with start level as century in <b>DateTimePicker</b> popup        $('#dateTime').ejDateTimePicker({            <b>startLevel: "century",</b>        });</td></tr>
</table>


{% include image.html url="/js/DateTimePicker/Concepts-and-Features/Start-and-Depth-level_images/Start-and-Depth-level_img1.png" Caption="Figure 7: Showcase for DateTimePicker with century level in DateTimePicker popup"%}

## Depth Level

**DateTimePicker** enables you to set the drill down level of **DateTimePicker**. Consider, you are going to take the monthly report of sales in your company. In that case, there is no need for selecting date from month view. You can restrict the drill-down of **DateTimePicker** popup to month view.

In the following example, start level is set from century and drill down is set to year view. So drill-down to month is restricted. So you can avoid selecting the day of the month. By default, the current day of the month is maintained in the day number field. Refer the following code to set drill down value to year view.

The following code snippet is set to depth level in **DateTimePicker.**



{% highlight js %}

**[JavaScript]**
               $('#dateTime').ejDateTimePicker({  
                   startLevel:"century",
                   depthLevel:"year",
                   width: '200px', 
               });       


{% endhighlight %}



{% include image.html url="/js/DateTimePicker/Concepts-and-Features/Start-and-Depth-level_images/Start-and-Depth-level_img2.png" Caption="Figure 8: Showcase of DateTimePicker with Depth level “year”"%}

