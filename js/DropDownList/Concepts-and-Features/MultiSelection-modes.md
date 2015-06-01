---
layout: post
title: MultiSelection-modes
description: multiselection modes
platform: js
control: DropDownList
documentation: ug
---

# MultiSelection modes

**DropdownList** widget allows you to select multiple values from the suggestion list using **allowMultiSelection** property. You can select Multiple values by setting allowMultiSelection value to true.

**Configuring MultiSelection Mode**

The following steps explain you the configuration of the **allowMultiSelection** for a **DropdownList** textbox.

* In an **HTML** page, add a **&lt;input&gt;** element to configure **DropdownList** widget



<table>
<tr>
<td>
<b>[HTML]</b>         &lt;input type="text" id="dropdownlist" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Configure multiSelectMode type for <b>Dropdownlist</b> control&lt;script type="text/javascript"&gt;        $(function () {            $('#dropdownlist').ejDropDownList({                targetID: "list",                width: "200px",                <b>showCheckbox</b>: true,                <b>allowMultiSelection</b>: true            });        });   &lt;/script&gt;</td></tr>
</table>




Output for Dropdown control that provides multiple selection is as follows.


{% include image.html url="/js/DropDownList/Concepts-and-Features/MultiSelection-modes_images/MultiSelection-modes_img1.png" Caption=""%}

_Figure 20: Dropdown with_ allowMultiSelection _property_ 

