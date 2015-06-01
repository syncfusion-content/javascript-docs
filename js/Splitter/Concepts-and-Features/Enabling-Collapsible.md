---
layout: post
title: Enabling-Collapsible
description: enabling collapsible
platform: js
control: Splitter
documentation: ug
---

# Enabling Collapsible

The **Splitter** provides you the option to enable or disable the pane collapse functionality. You can click the icon in **Splitbar** to collapse or expand the corresponding pane element in **Splitter**. Setting the **collapsible** property to “**false**” disables the pane collapse functionality in the **Splitter** widget.

## Configure Collapsible

The following steps explain the implementation of the **collapsible** option in **Splitter**.

* In the **HTML** page set the **&lt;div&gt;** element to render **Splitter** control.  



<table>
<tr>
<td>
<b>[HTML]</b>        &lt;div id="splitter"&gt;            &lt;div&gt;                &lt;div style="padding: 0px 15px;"&gt;                    <h3 class="h3">Tools &lt;/h3&gt;                    Essential Tools is an collection of user interface components used to create interactive                                    ASP.NET MVC applications.                &lt;/div&gt;            &lt;/div&gt;            &lt;div&gt;                &lt;div style="padding: 0px 15px;"&gt;                    <h3 class="h3">Grid &lt;/h3&gt;                    Essential Mvc Grid offers full featured a Grid control with extensive support for                                    Grouping and the display of hierarchical data.                &lt;/div&gt;            &lt;/div&gt;        &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>collapsible</b> property as “<b>True</b>” in <b>Splitter</b> properties. The default value of the <b>collapsible</b> property is “<b>True</b>” in <b>Splitter</b>.    &lt;script type="text/javascript"&gt;        $("#splitter").ejSplitter({            height: 280, width: 600,<b>           properties: [{collapsible: true}]</b>        });    &lt;/script&gt;</td></tr>
</table>


The output for **Splitter** when **collapsible** is set to “**True**” is as follows.



{% include image.html url="/js/Splitter/Concepts-and-Features/Enabling-Collapsible_images/Enabling-Collapsible_img1.png" Caption="Figure 3: Splitter with collapsible as true"%}

The output for Splitter when **collapsible** is “**false**”.

{% include image.html url="/js/Splitter/Concepts-and-Features/Enabling-Collapsible_images/Enabling-Collapsible_img2.png" Caption="Figure 4: Splitter with collapsible as false"%}



