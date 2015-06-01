---
layout: post
title: Enabling-the-ProgressBar
description: enabling the progressbar
platform: js
control: ProgressBar
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


* The following screenshot displays the output for the above code.

{% include image.html url="/js/ProgressBar/Concepts-and-features/Enabling-the-ProgressBar_images/Enabling-the-ProgressBar_img1.png" Caption="Figure 12: Disabled ProgressBar"%}

