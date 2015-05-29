---
layout: post
title: multiselection-modes
description: multiselection modes
platform: js
control: DropDownList
documentation: ug
---

# MultiSelection modes

**DropdownList****Dropdownlist** widget allows you to select multiple values from the suggestion list using **allowMultiSelection** property. You can select Multiple values by setting allowMultiSelection value to true.

**Configuring MultiSelection Mode**

The following steps explain you the configuration of the **allowMultiSelection** for a **DropdownList****Dropdownlist** textbox.

* In an **HTML** page, add a **&lt;input&gt;** element to configure **DropdownList****Dropdownlist** widget



<table>
<tr>
<td>
<b>[HTML]</b>         &lt;input type="text" id="dropdownlist" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Configure multiSelectMode type for <b>Dropdownlist</b> control&lt;script type="text/javascript"&gt;        $(function () {            $('#dropdownlist').ejDropDownList({                targetID: "list",                width: "200px",                <b>showCheckbox</b>: true,                <b>allowMultiSelection</b>: true            });        });   &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

// Add a DropDownList element using the helper class in CSHTML



@Html.EJ().DropDownList("dropdownlist").TargetID("list").**AllowMultiSelection**(true).ShowCheckbox(true).Width("200px")

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

      &lt;ej:DropDownList ID="dropdownlist" TargetID="list" AllowMultiSelection="true" Width="200px" ShowCheckbox="true" runat="server"&gt;

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



Output for Dropdown control that provides multiple selection is as follows.


![](multiselection-modes_images\multiselection-modes_img1.png)

_Figure_ _46__20__:_ _Dropdown with_ allowMultiSelection _property_ 

