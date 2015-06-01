---
layout: post
title: RTL-Support
description: rtl support
platform: js
control: ProgressBar
documentation: ug
---

# RTL Support

Right-to-left starts from the right of the page and continues to the left. By default, this option is set to ‘**false**’ in the **ProgressBar** control. The **enableRTL** option allows the **ProgressBar** control to display it in the right to left direction.

The following steps explain how to **enable** the **RTL** property of the **ProgressBar** control.

* In the **HTML** page, add a **&lt;div&gt;** element to render the **ProgressBar** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="control"&gt;            &lt;div id="progressbar"&gt;&lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the following code example to enable the RTL property of the ProgressBar control.&lt;script type="text/javascript"&gt;            $(function () {//Declaration.                $("#progressbar").ejProgressBar({<b>                    enableRTL: true,</b>                    value: 80,                    height: 20,                    width: 500                });                var progress = $("#progressbar").data("ejProgressbar");                progress.setModel({ text: progress.getValue() + " % Completed" });            });</td></tr>
</table>




* The following screenshot displays the output.

{% include image.html url="/js/ProgressBar/Concepts-and-features/RTL-Support_images/RTL-Support_img1.png" Caption="Figure 14: RTL Support in ProgressBar"%}























