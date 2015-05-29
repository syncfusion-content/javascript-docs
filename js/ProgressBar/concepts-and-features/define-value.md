---
layout: post
title: define-value
description: define value
platform: js
control: Progress Bar
documentation: ug
---

# Define value

## Value

The **vValue** for the **ProgressBar** is set by using **‘value’** property. The **vValue** should be between the minimum (min) and the maximum (max) values (number) of the **ProgressBar**. By default, the **minValue** is **0** and the **maxValue** is **100** in **ProgressBar**, and the ‘**value**’ is set to **0**(number).

The following steps explain you on how to set the **vValue** for the **ProgressBar** widget.

* In the **HTML** page, add a **&lt;div&gt;** element to render the **ProgressBar** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="control"&gt;            &lt;div id="progressbar"&gt;&lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the following code example to set the value for the ProgressBar widget.&lt;script type="text/javascript"&gt;    $(function () {//Declaration.        $("#progressbar").ejProgressBar({            minValue: 40,            maxValue: 80,<b>            value: 60,</b>            height: 20,            width: 500        });        var progress = $("#progressbar").data("ejProgressBar");        progress.setModel({ text: progress.getValue()});    });&lt;/script&gt;</td></tr>
</table>




<table>
<tr>
<td>
<b>[CSHTML]</b><b>// Add the following code example to the corresponding CSHTML page to render the ProgressBar control with customized value.</b>@Html.EJ().ProgressBar("progressbar").MinValue(40).MaxValue(80).<b>Value(60).</b>Height("20").Width("500")</td></tr>
<tr>
<td>
<b>[JavaScript]</b>&lt;script&gt;            var progress;            $(document).ready(function () {                progress = $("#progressbar").data("ejProgressBar");                progress.setModel({ text: progress.getValue()});                         });        &lt;/script&gt;</td></tr>
</table>




<table>
<tr>
<td>
<b>[ASPX]</b><b>// Add the following code example to the corresponding ASPX page to render ProgressBar control with customized value.</b><b>         </b>&lt;ej:ProgressBar ID="progressbar" runat="server" Value="60" MinValue="40" MaxValue="80" Height="20" Width="500" &gt;&lt;/ej:ProgressBar&gt;    </td></tr>
<tr>
<td>
<b>[JavaScript]</b>     &lt;script&gt;            var progress;            $(document).ready(function () {                progress = $("#progressbar").data("ejProgressBar");                progress.setModel({ text: progress.getValue()});                         });        &lt;/script&gt;</td></tr>
</table>


* The following screenshot displays the output for the above code.

{% include image.html url="\js\ProgressBar\concepts-and-features\define-value_images\define-value_img1.png" Caption="Figure 16: Assigning value to ProgressBar"%}



##  Percentage

The **ProgressBar** value is set in **Percentage** by using the **‘percentage’** property. The value should be between the min and max values (number) of the **ProgressBar**. By default, the **minValue** is **0** and the **maxValue** is **100** in **ProgressBar**, and **percentage** is set to **0** (number).

The following steps explain you on how to set the value in **pPercentage** for the **ProgressBar** widget. 

* In the **HTML** page, add a **&lt;div&gt;** element to render the **ProgressBar** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="control"&gt;            &lt;div id="progressbar"&gt;&lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the following code example to set the value in percentage for the ProgressBar widget.&lt;script type="text/javascript"&gt;    $(function () {//Declaration.        $("#progressbar").ejProgressBar({           minValue: 40,           maxValue: 80,           <b>percentage: 60,</b>           width: 500,           height: 20        });        var progress = $("#progressbar").data("ejProgressBar");        progress.setModel({ text: progress.getValue() + " %" });    });&lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[CSHTML]</b><b>// Add the following code example to the corresponding CSHTML page to render the ProgressBar control with customized percentage.</b>@Html.EJ().ProgressBar("progressbar").MinValue(40).MaxValue(80).<b>Percentage(60).</b>Height("20").Width("500")</td></tr>
<tr>
<td>
<b>[JavaScript]</b>&lt;script&gt;            var progress;            $(document).ready(function () {                progress = $("#progressbar").data("ejProgressBar");                progress.setModel({ text: progress.getPercentage() + " %"});                         }); &lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[ASPX]</b><b>// Add the following code example to the corresponding ASPX page to render ProgressBar control with customized percentage.</b>        &lt;ej:ProgressBar ID="progressbar" runat="server" Percentage="60" MinValue="40" MaxValue="80" Height="20" Width="500" &gt;&lt;/ej:ProgressBar&gt;            </td></tr>
<tr>
<td>
<b>[JavaScript]</b>     &lt;script&gt;          var progress;          $(document).ready(function () {              progress = $("#progressbar").data("ejProgressBar");              progress.setModel({ text: progress.getPercentage() + " %"});          });    &lt;/script&gt;</td></tr>
</table>


* The following screenshot displays the output.

![](define-value_images\define-value_img2.png)

![](define-value_images\define-value_img3.png)

_Figure_ _1__7__:_ _Percentage in_ _Progress Bar__ProgressBar_

