---
layout: post
title: Define-value
description: define value
platform: js
control: ProgressBar
documentation: ug
---

# Define value

## Value

The **value** for the **ProgressBar** is set by using **‘value’** property. The **value** should be between the minimum (min) and the maximum (max) values (number) of the **ProgressBar**. By default, the **minValue** is **0** and the **maxValue** is **100** in **ProgressBar**, and the ‘**value**’ is set to **0**(number).

The following steps explain you on how to set the **value** for the **ProgressBar** widget.

* In the **HTML** page, add a **&lt;div&gt;** element to render the **ProgressBar** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="control"&gt;            &lt;div id="progressbar"&gt;&lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the following code example to set the value for the ProgressBar widget.&lt;script type="text/javascript"&gt;    $(function () {//Declaration.        $("#progressbar").ejProgressBar({            minValue: 40,            maxValue: 80,<b>            value: 60,</b>            height: 20,            width: 500        });        var progress = $("#progressbar").data("ejProgressBar");        progress.setModel({ text: progress.getValue()});    });&lt;/script&gt;</td></tr>
</table>




* The following screenshot displays the output for the above code.

{% include image.html url="/js/ProgressBar/Concepts-and-features/Define-value_images/Define-value_img1.png" Caption="Figure 6: Assigning value to ProgressBar"%}



##  Percentage

The **ProgressBar** value is set in **Percentage** by using the **‘percentage’** property. The value should be between the min and max values (number) of the **ProgressBar**. By default, the **minValue** is **0** and the **maxValue** is **100** in **ProgressBar**, and **percentage** is set to **0** (number).

The following steps explain you on how to set the value in **percentage** for the **ProgressBar** widget. 

* In the **HTML** page, add a **&lt;div&gt;** element to render the **ProgressBar** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="control"&gt;            &lt;div id="progressbar"&gt;&lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the following code example to set the value in percentage for the ProgressBar widget.&lt;script type="text/javascript"&gt;    $(function () {//Declaration.        $("#progressbar").ejProgressBar({           <b>percentage: 60,</b>           width: 500,           height: 20        });        var progress = $("#progressbar").data("ejProgressBar");        progress.setModel({ text: progress.getValue() + " %" });    });&lt;/script&gt;</td></tr>
</table>


* The following screenshot displays the output.

{% include image.html url="/js/ProgressBar/Concepts-and-features/Define-value_images/Define-value_img2.png" Caption=""%}



_Figure_ _7__:_ _Percentage in_ _ProgressBar_

