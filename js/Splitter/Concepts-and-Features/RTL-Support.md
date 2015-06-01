---
layout: post
title: RTL-Support
description: rtl support
platform: js
control: Splitter
documentation: ug
---

# RTL Support

The **Splitter** provides you with **RTL** (**Right-To-Left**) support. The alignment of **Splitter** can be changed from **Left-To-Right** to **Right-To-Left**.

## Enable RTL

The following steps explain enabling the right-to-left property for **Splitter** widget.

* In the **HTML** page set the corresponding **&lt;div&gt;** elements for outer and inner **Splitter** control.



<table>
<tr>
<td>
<b>[HTML]</b>        &lt;div id="outersplitter"&gt;            &lt;div&gt;                &lt;div style="padding: 0px 15px;"&gt;                    <h3 class="h3">ASP.NET MVC &lt;/h3&gt;                &lt;/div&gt;            &lt;/div&gt;            &lt;div id="innersplitter"&gt;                &lt;div&gt;                    &lt;div style="padding: 0px 15px;"&gt;                        <h3 class="h3">Tools &lt;/h3&gt;                        Essential Tools is an collection of user interface components used to create interactive                                    ASP.NET MVC applications.                    &lt;/div&gt;                &lt;/div&gt;                &lt;div&gt;                    &lt;div style="padding: 0px 15px;"&gt;                        <h3 class="h3">Chart &lt;/h3&gt;                        Essential Chart is a business-oriented charting component.                    &lt;/div&gt;                &lt;/div&gt;                &lt;div&gt;                    &lt;div style="padding: 0px 15px;"&gt;                        <h3 class="h3">Grid &lt;/h3&gt;                        Essential Mvc Grid offers full featured a Grid control with extensive support for                                    Grouping and the display of hierarchical data.                    &lt;/div&gt;                &lt;/div&gt;            &lt;/div&gt;        &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>//</b> Set <b>enableRTL</b> as “<b>true</b>” in the <b>ejSplitter</b> function.    &lt;script type="text/javascript"&gt;            $("#outersplitter").ejSplitter({                height: 250, width: 600,                orientation: ej.Orientation.Vertical,                <b>enableRTL: true,</b>                properties: [{ paneSize: 60 }]            });            $("#innersplitter").ejSplitter({                width: 600,                properties: [{ paneSize: 200 }, { paneSize: 170 }]            });    &lt;/script&gt;</td></tr>
</table>


The output for **Splitter** when **enableRTL** is “**true**”.



{% include image.html url="/js/Splitter/Concepts-and-Features/RTL-Support_images/RTL-Support_img1.png" Caption="Figure 19: Splitter with enableRTL "%}







__

