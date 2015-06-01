---
layout: post
title: Checkbox-Support
description: checkbox support
platform: js
control: DropDownList
documentation: ug
---

# Checkbox Support

**Show Checkbox** 

You can enable the checkbox in the **DropdownList** with this property. The data type of **showCheckbox** value is Boolean type. It maintains multiple selection and gets the checked items on its dropdown client side events.  

**Check All** 

You can check all the check box in the list by using this property. The data type of **checkAll** needs to be in Boolean type. To achieve this, you need to set **showCheckbox** property as true

**Uncheck All**

You can uncheck all the check box in the list by using this property. The data type of **uncheckAll** is Boolean type. To achieve this, set **showCheckbox** property as true.

**Defining the Checkbox support**

The following steps explains you the configuration of checkbox options in **DropdownList**

1. In an **HTML** page, add a &lt;input&gt; element to configure **DropdownList** widget


<table>
<tr>
<td>
<b>[HTML]</b>&lt;input type="text" id="dropdownlist" /&gt;  &lt;div id="list"&gt;            &lt;ul&gt;                <li>Art</li>                <li>Architecture</li>                <li>Biography</li>                <li>comics</li>                <li>Sports</li>            &lt;/ul&gt;        &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;              $(function () {            $('#dropdownlist').ejDropDownList({                targetID: "list",                width: "200px",                <b>showCheckbox</b>: true,                <b>checkAll</b>: true                            });        });   &lt;/script&gt;</td></tr>
</table>


Output of the above steps



{% include image.html url="/js/DropDownList/Concepts-and-Features/Checkbox-Support_images/Checkbox-Support_img1.png" Caption=""%}

_Figure 19: Dropdown with checkbox property_  

