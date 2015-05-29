---
layout: post
title: enabling-the-progressbar
description: enabling the progressbar
platform: js
control: Progress Bar
documentation: ug
---

# Enabling the ProgressBar

The **ProgressBar** is enabled by using the ‘**enabled**’ Property. When this property is set to ‘**false**’, it disables the **ProgressBar** widget. By default, ‘**enabled**’ property is set to ‘**true**’ in the **ProgressBar** widget.

The following steps explain how to disable the **ProgressBar** widget when ‘**enabled**’ property is set to ‘**false**’.

* In the **HTML** page, add a **&lt;div&gt;** element to render the **ProgressBar** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="control"&gt;        &lt;div id="progressbar"&gt;&lt;/div&gt;&lt;/div&gt;        </td></tr>
<tr>
<td>
	<b>[JavaScript]</b>// Add the ‘enabled’ property as follows.&lt;script type="text/javascript"&gt;    $(function () {//Declaration.        $("#Progrssbar").ejProgressBar({            <b>enabled: false,</b>            value: 40,            width: 500,            height: 40        });        var progress = $("#progressbar").data("ejProgressBar");        progress.setModel({ text: progress.getValue() + " %" });    });&lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[CSHTML]</b><b>// Add the following code example to the corresponding CSHTML page to disable the ProgressBar control.</b>@Html.EJ().ProgressBar("progressbar").Value(70).Height("20").Width("500").<b>Enabled(false)</b></td></tr>
<tr>
<td>
<b>[JavaScript]</b>   &lt;script&gt;            var progress;            $(document).ready(function () {                progress = $("#progressbar").data("ejProgressBar");                progress.setModel({ text: progress.getValue() + " %"});                         });    &lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[ASPX]</b><b>// Add the following code example to the corresponding ASPX page to disable the ProgressBar control</b>&lt;ej:ProgressBar ID="progressbar" runat="server" Value="70"  Height="20" Width="500" Enabled="false" &gt;&lt;/ej:ProgressBar&gt;       </td></tr>
<tr>
<td>
<b>[JavaScript]</b>   &lt;script&gt;            var progress;            $(document).ready(function () {                progress = $("#progressbar").data("ejProgressBar");                progress.setModel({ text: progress.getValue() + " %"});                         });    &lt;/script&gt;</td></tr>
</table>


* The following screenshot displays the output for the above code.

{% include image.html url="\js\ProgressBar\concepts-and-features\enabling-the-progressbar_images\enabling-the-progressbar_img1.png" Caption="Figure 122: Disabled Progress BarProgressBar"%}

