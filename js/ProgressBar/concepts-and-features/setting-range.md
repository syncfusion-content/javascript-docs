---
layout: post
title: setting-range
description: setting range
platform: js
control: Progress Bar
documentation: ug
---

# Setting Range

The **range** of the **ProgressBar** is set by using minimum and maximum values. The Minimum value specifies the value where the **ProgressBar** shows the process to have started. The Maximum value specifies the value where the process is completed. You can set the range by using the **‘mMinValue’** and **‘mMaxValue’** property.

* In the **HTML** page, add a **&lt;div&gt;** element to render the **ProgressBar** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="control"&gt;        &lt;div id="progressbar"&gt;&lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add Range for the ProgressBar widget as follows.&lt;script type="text/javascript"&gt;                      $(function () {//Declaration.                $("#progressbar").ejProgressBar({                    <b>minValue: 40,</b><b>                    maxValue: 80,</b>                    value: 80,                    height: 20,                    width: 500                });                var progress = $("#progressbar").data("ejProgressBar");                progress.setModel({ text: progress.getPercentage() + " % Completed" });            });&lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b> [CSHTML]</b><b>// Add the following code example to the corresponding CSHTML page to render the ProgressBar control with customized range.</b>@Html.EJ().ProgressBar("progressbar").<b>MinValue(40).MaxValue(80</b>).Value(80).Height("20").Width("500")</td></tr>
<tr>
<td>
 <b>[JavaScript]</b>&lt;script&gt;            var progress;            $(document).ready(function () {                progress = $("#progressbar").data("ejProgressBar");                progress.setModel({ text: progress.getPercentage() + " %" });            });        &lt;/script&gt;        </td></tr>
</table>


<table>
<tr>
<td>
<b>[ASPX]</b><b>// Add the following code example to the corresponding ASPX page to render ProgressBar control with customized range.</b> &lt;ej:ProgressBar ID="progressbar" runat="server" Value="80" MinValue="40" MaxValue="80" Height="20" Width="500" &gt;&lt;/ej:ProgressBar&gt;        </td></tr>
<tr>
<td>
 <b>[JavaScript]</b>&lt;script&gt;          var progress;          $(document).ready(function () {              progress = $("#progressbar").data("ejProgressBar");              progress.setModel({ text: progress.getPercentage() + " %"});          });    &lt;/script&gt;        </td></tr>
</table>


*  The following screenshot displays the output.

{% include image.html url="\js\ProgressBar\concepts-and-features\setting-range_images\setting-range_img1.png" Caption="Figure 18: Range in Progress BarProgressBar"%}

