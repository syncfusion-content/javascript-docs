---
layout: post
title: Persistence-Support
description: persistence support
platform: js
control: Slider
documentation: ug
---

# Persistence Support

This feature supports you to save current model value to browser cookies for state maintenance. When you refresh the web page, the **Slider** control retains the model value apply from browser cookies. The data type of **enablePersistence** is Boolean type. 

The following steps explain you on how to enable the **enablePersistence** property.

* In an **HTML** page, add a **&lt;div&gt;** element to render it as a **Slider** widget.



<table>
<tr>
<td>
[<b>HTML</b>]&lt;div id="ejSlider"&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
[<b>JavaScript</b>]// When initializing the Slider widget, enable the enablePersistence property as follows.    &lt;script&gt;        $("#ejSlider").ejSlider({            height: "15",            width: "500",<b>            enablePersistence:true</b>        });    &lt;/script&gt;</td></tr>
</table>


