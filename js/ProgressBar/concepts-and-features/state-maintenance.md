---
layout: post
title: state-maintenance
description: state maintenance
platform: js
control: Progress Bar
documentation: ug
---

# State Maintenance

Save current model value to cookies for **State Maintenance**. While refreshing the **ProgressBar** widget, page retains the model value applied from browser cookies. By default, the ‘**enablePersistence**’ property is set to ‘**false**’ in the **ProgressBar**.

The following steps explain the **State Maintenance** in the **ProgressBar** control.

* In the **HTML** page, add a **&lt;div&gt;** element to render the **ProgressBar** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="control"&gt;        &lt;div id="progressbar"&gt;&lt;/div&gt;&lt;/div&gt;        </td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the following script to enable State Maintenance.&lt;script type="text/javascript"&gt;    $(function () {//Declaration.        $("#progressBar").ejProgressBar({            <b>enablePersistence: true,</b>            value: 40,            width: 500,            height: 40        });        var progress = $("#progressbar").data("ejProgressBar");        progress.setModel({ text: progress.getValue() + " %" });    });&lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[CSHTML]</b><b>// Add the following code example to the corresponding CSHTML page to enable the state maintenance in the ProgressBar control.</b>@Html.EJ().ProgressBar("progressbar").Value(70).Height("20").Width("500").<b>EnablePersistence(true)</b></td></tr>
<tr>
<td>
<b>[JavaScript]</b>     &lt;script&gt;            var progress;            $(document).ready(function () {                progress = $("#progressbar").data("ejProgressBar");                progress.setModel({ text: progress.getValue() + " %"});          });     &lt;/script&gt;        </td></tr>
</table>


<table>
<tr>
<td>
<b>[ASPX]</b><b>// Add the following code example to the corresponding ASPX page to enable the state maintenance in ProgressBar control.</b>  &lt;ej:ProgressBar ID="progressbar" runat="server" Value="70"  Height="20" Width="500" EnablePersistence="true"&gt;<b>&lt;/ej:ProgressBar&gt;</b>   </td></tr>
<tr>
<td>
<b>[JavaScript]</b>     &lt;script&gt;            var progress;            $(document).ready(function () {                progress = $("#progressbar").data("ejProgressBar");                progress.setModel({ text: progress.getValue() + " %"});          });     &lt;/script&gt;        </td></tr>
</table>


* The following screenshot displays the output.

{% include image.html url="\js\ProgressBar\concepts-and-features\state-maintenance_images\state-maintenance_img1.png" Caption="Figure 123: State Maintenance in ProgressBar"%}

