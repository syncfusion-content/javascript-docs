---
layout: post
title: RTL-Support
description: rtl support
platform: js
control: Dialog
documentation: ug
---

# RTL Support

The **Dialog** supports Right-To-Left feature. The alignment of **Dialog** content can be changed from Left-To-Right into Right-To-Left.

## Enable RTL Support

The following steps explain enabling the right-to-left property for **Dialog** control.

1. In the **HTML** page set a **&lt;div&gt;** element with dialog content for rendering the **Dialog** control. 



<table>
<tr>
<td>
<b>[HTML]</b>        &lt;div id="rtlDialog" title="WinRT"&gt;        Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications <span>including grid, chart, map, tree map, SSRS report viewer, rich-text editor, pdf viewer, gauges, barcode, editors, and much more.&lt;/span&gt;        It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.        &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Enable <b>RTL</b> to the <b>Dialog</b> control by setting <b>enableRTL</b> property as true    &lt;script type="text/javascript"&gt;        $("#rtlDialog").ejDialog({            <b>enableRTL: true,</b>            width: 550                    });     &lt;/script&gt;</td></tr>
</table>


2. The output for **Dialog** when **enabelRTL** is “**True**” is as follows.

{% include image.html url="/js/Dialog/Concepts-and-Features/RTL-Support_images/RTL-Support_img1.png" Caption="Dialog with enableRTL"%}

