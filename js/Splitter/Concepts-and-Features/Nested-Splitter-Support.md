---
layout: post
title: Nested-Splitter-Support
description: nested splitter support
platform: js
control: Splitter
documentation: ug
---

# Nested Splitter Support

The **Splitter** provides nested pane support that allows you to add a pane between two pane elements.

## Configure Nested Splitter

The following steps explain the implementation of the “nested****splitter”****option.

* In the **HTML** page set the corresponding **&lt;div&gt;** elements for outer and inner **Splitter** control. 



<table>
<tr>
<td>
<b>[HTML]</b>        &lt;div id="outersplitter"&gt;            &lt;div&gt;                &lt;div style="padding: 0px 15px;"&gt;                    <h3 class="h3">ASP.NET MVC &lt;/h3&gt;                &lt;/div&gt;            &lt;/div&gt;            &lt;div id="innersplitter"&gt;                &lt;div&gt;                    &lt;div style="padding: 0px 15px;"&gt;                        <h3 class="h3">Tools &lt;/h3&gt;                        Essential Tools is an collection of user interface components used to create interactive                                    ASP.NET MVC applications.                    &lt;/div&gt;                &lt;/div&gt;                &lt;div&gt;                    &lt;div style="padding: 0px 15px;"&gt;                        <h3 class="h3">Chart &lt;/h3&gt;                        Essential Chart is a business-oriented charting component.                    &lt;/div&gt;                &lt;/div&gt;                &lt;div&gt;                    &lt;div style="padding: 0px 15px;"&gt;                        <h3 class="h3">Grid &lt;/h3&gt;                        Essential Mvc Grid offers full featured a Grid control with extensive support for                                    Grouping and the display of hierarchical data.                    &lt;/div&gt;                &lt;/div&gt;            &lt;/div&gt;        &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the pane properties to both inner and outer Splitter widget.    &lt;script type="text/javascript"&gt;            $("#outersplitter").ejSplitter({                height: 280, width: 600,                orientation: ej.Orientation.Vertical,                <b>properties: [{ paneSize: 60 }]</b>            });            $("#innersplitter").ejSplitter({                width: 600,                <b>properties: [{ paneSize: 200 }, { paneSize: 170 }]</b>            });    &lt;/script&gt;</td></tr>
</table>


The output for **nested Splitter**.



{% include image.html url="/js/Splitter/Concepts-and-Features/Nested-Splitter-Support_images/Nested-Splitter-Support_img1.png" Caption="Figure 7: Nested Splitter"%}

