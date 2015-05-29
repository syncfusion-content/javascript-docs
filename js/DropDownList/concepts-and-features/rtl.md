---
layout: post
title: rtl
description: rtl
platform: js
control: DropDownList
documentation: ug
---

# RTL

This feature supports to change the left-to-right alignment of the **Dropdown** widget to right-to-left (**RTL**). 

**Defining the RTL property**

The following steps explains you the configuration of **enableRTL** properties in **DropdownList****Dropdownlist.**

* In an **HTML** page, add a **&lt;input&gt;** element to configure **DropdownList****Dropdownlist** widget


<table>
<tr>
<td>
<b>[HTML]</b>&lt;input type="text" id="dropdownlist" /&gt;        &lt;div id="list"&gt;            &lt;ul&gt;                <li>Art</li>                <li>Architecture</li>                <li>Biography</li>                <li>comics</li>                <li>Sports</li>                <li>Science</li>            &lt;/ul&gt;        &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]  </b>// Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;   $(function () {            $('#dropdownlist').ejDropDownList({                targetID: "list",                <b>enableRTL</b>:true            });       }); &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

// Add a DropDownList element using the helper class in CSHTML



@Html.EJ().DropDownList("dropdownlist").TargetID("list").**EnableRTL**(true) 

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

      &lt;ej:DropDownList ID="dropdownlist" TargetID="list" Width="200px" EnableRTL="true"  runat="server"&gt;

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


![](rtl_images\rtl_img1.png)

_Figure_ _58__32__: Dropdown with enableRTL property_  

