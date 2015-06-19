---
layout: post
title: Template-Support
description: template support
platform: js
control: Toolbar
documentation: ug
---

# Template Support

Template allows you to insert custom controls inside the toolbar items. Also you can design simple drop down buttons listing the items and radio button inside the **Toolbar**.

Set the list for **DropDown control** inside a list tag and define this tag as a **Toolbar** item. You can use all simple controls as a **Toolbar** item. To add RadioButton and DropDownList to **Toolbar**, use the following code example.

<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="toolbarcontent"&gt;    &lt;ul&gt;        &lt;li&gt;            &lt;div&gt;                &lt;input type="radio" name="small" id="Radio1" /&gt;            &lt;/div&gt;            option        &lt;/li&gt;        &lt;li id="Dropdown" title="Dropdown Control"&gt;            &lt;input id="selectcar" type="text" /&gt;            &lt;div id="cars"&gt;                &lt;ul&gt;                    <li>Audi A4</li>                    <li>Audi A5</li>                    <li>Audi A6</li>                    <li>Audi A7</li>                &lt;/ul&gt;            &lt;/div&gt;        &lt;/li&gt;    &lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
[JS]&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#Radio1").ejRadioButton({ checked: false });        $('#selectcar').ejDropDownList({ height: "23px", width: "100px", targetID: "cars", selectedItemIndex: 0 });        $("#toolbarcontent").ejToolbar({ width: "250px", height: "28px" });    });&lt;/script&gt;</td></tr>
</table>
The following screenshot displays a Toolbar with embedded controls.

{% include image.html url="/js/Toolbar/Concepts-and-Features/Template-Support_images/Template-Support_img1.png" Caption="Toolbar with Template"%}

