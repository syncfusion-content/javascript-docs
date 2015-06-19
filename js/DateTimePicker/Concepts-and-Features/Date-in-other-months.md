---
layout: post
title: Date-in-other-months
description: date in other months
platform: js
control: DateTimePicker
documentation: ug
---

# Date in other months

**DateTimePicker** calendar can display the dates in other months at the start or end of the current month. To enable or disable the display of other month dates in the current month, you can use the property called **showOtherMonths**. By setting this property value as **“True”** you can display the dates in other months at the start or end of the current month. By default the value of this property is **“True”**. 

Consider you are going to calculate the monthly report of your company’s employee attendance. To avoid the mistake of selecting other month dates while calculating current month report, you can disable showing other month dates in the current month. You can achieve this requirement by setting **showOtherMonths** value as **“False”.**

* Add the following code in your **HTML** page.



<table>
<tr>
<td>
<b>[HTML]    </b> &lt;div class="control"&gt;        &lt;input type="text" id="dateTime" /&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>//  Add the code in your script section to render <b>DateTimePicker</b> without displaying other month dates in current month           $('#dateTime').ejDateTimePicker({               showOtherMonths: false,               width: '200px',           });</td></tr>
</table>
{% include image.html url="/js/DateTimePicker/Concepts-and-Features/Date-in-other-months_images/Date-in-other-months_img1.png" Caption="Figure 9: Showcase for DateTimePicker without other month dates"%}

