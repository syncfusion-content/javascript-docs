---
layout: post
title: RTL
description: rtl
platform: js
control: DropDownList
documentation: ug
---

# RTL

This feature supports to change the left-to-right alignment of the **Dropdown** widget to right-to-left (**RTL**). 

**Defining the RTL property**

The following steps explains you the configuration of **enableRTL** properties in **DropdownList****.**

* In an **HTML** page, add a **&lt;input&gt;** element to configure **DropdownList** widget


<table>
<tr>
<td>
<b>[HTML]</b>&lt;input type="text" id="dropdownlist" /&gt;        &lt;div id="list"&gt;            &lt;ul&gt;                <li>Art</li>                <li>Architecture</li>                <li>Biography</li>                <li>comics</li>                <li>Sports</li>                <li>Science</li>            &lt;/ul&gt;        &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]  </b>// Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;   $(function () {            $('#dropdownlist').ejDropDownList({                targetID: "list",                <b>enableRTL</b>:true            });       }); &lt;/script&gt;</td></tr>
</table>


Output of the above steps


{% include image.html url="/js/DropDownList/Concepts-and-Features/RTL_images/RTL_img1.png" Caption=""%}

_Figure 32: Dropdown with enableRTL property_  

