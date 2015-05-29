---
layout: post
title: checkbox-support
description: checkbox support
platform: js
control: DropDownList
documentation: ug
---

# Checkbox Support

**Show Checkbox** 

You can enable the checkbox in the **DropdownList****Dropdownlist** with this property. The data type of **showCheckbox** value is Boolean type. It maintains multiple selection and gets the checked items on its dropdown client side events.  

**Check All** 

You can check all the check box in the list by using this property. The data type of **checkAll** needs to be in Boolean type. To achieve this, you need to set **showCheckbox** property as true

**Uncheck All**

You can uncheck all the check box in the list by using this property. The data type of **uncheckAll** is Boolean type. To achieve this, set **showCheckbox** property as true.

**Defining the Checkbox support**

The following steps explains you the configuration of checkbox options in **DropdownList****Dropdownlist**

1. In an **HTML** page, add a &lt;input&gt; element to configure **DropdownList****Dropdownlist** widget


<table>
<tr>
<td>
<b>[HTML]</b>&lt;input type="text" id="dropdownlist" /&gt;  &lt;div id="list"&gt;            &lt;ul&gt;                <li>Art</li>                <li>Architecture</li>                <li>Biography</li>                <li>comics</li>                <li>Sports</li>            &lt;/ul&gt;        &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;              $(function () {            $('#dropdownlist').ejDropDownList({                targetID: "list",                width: "200px",                <b>showCheckbox</b>: true,                <b>checkAll</b>: true                            });        });   &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

// Add a DropDownList element using the helper class in CSHTML



@Html.EJ().DropDownList("dropdownlist").TargetID("list").**ShowCheckbox**(true).**CheckAll**(true).Width("200px")

  &lt;div id="list"&gt;

            &lt;ul&gt;

                <li>Art</li>

                <li>Architecture</li>

                <li>Biography</li>

                <li>Comics</li>

                <li>Sports</li>

                <li>Science</li>

            &lt;/ul&gt;



        &lt;/div&gt;



**[ASPX]**

// Add Dropdown list widget in ASPX page



     &lt;div class="control"&gt;

      &lt;ej:DropDownList ID="dropdownlist" TargetID="list" Width="200px" ShowCheckbox="true" CheckAll="true" runat="server"&gt;

      &lt;/ej:DropDownList&gt;

     &lt;div id="list"&gt;

            &lt;ul&gt;

                <li>Art</li>

                <li>Architecture</li>

                <li>Biography</li>

                <li>Comics</li>

                <li>Sports</li>

                <li>Science</li>

             &lt;/ul&gt;

     &lt;/div&gt;

&lt;/div&gt;



Output of the above steps



![](checkbox-support_images\checkbox-support_img1.png)

_Figure_ _45__19__: Dropdown with checkbox property_  

