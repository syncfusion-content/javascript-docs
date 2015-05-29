---
layout: post
title: search-options-
description: search options 
platform: js
control: DropDownList
documentation: ug
---

# Search Options 

**Incremental Search** 

This feature provides support to **Dropdown List** with search options that enables the search options by quick typing in the textbox when popup is displayed. In case if the matched options is not available in list, it automatically selects the last one in the list.  The data type of **enableIncrementalSearch** is Boolean type.

**Case-Sensitive Search** 

This features provides support to search option with case sensitive. To achieve this you need to enable the incremental search on dropdown and the data type of **caseSensitiveSearch** is Boolean type. 

**Define the Incremental Search with Case-Sensitive** 

The following steps explains you the configuration of search options in **DropdownList****Dropdownlist**

* In an **HTML** page, add a **&lt;input&gt;** element to configure **DropdownList****Dropdownlist** widget


<table>
<tr>
<td>
<b>[HTML]</b>&lt;input type="text" id="dropdownlist" /&gt;  &lt;div id="list"&gt;            &lt;ul&gt;                <li>Art</li>                <li>Architecture</li>                <li>Biography</li>                <li>comics</li>                <li>Sports</li>            &lt;/ul&gt;        &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>&lt;script type="text/javascript"&gt;              $(function () {            $('#dropdownlist').ejDropDownList({                targetID: "list",                                width: "200px",                               showRoundedCorner: true,<b>                enableIncrementalSearch: true,</b><b>                caseSensitiveSearch:false</b>            });        });   &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

// Add a DropDownList element using the helper class in CSHTML



@Html.EJ().DropDownList("dropdownlist").TargetID("list") .Width("200px").ShowRoundedCorner(true).**EnableIncrementalSearch**(true).**CaseSensitiveSearch**(false)



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

      &lt;ej:DropDownList ID="dropdownlist" TargetID="list" Width="200px" EnableIncrementalSearch="true" CaseSensitiveSearch="false" ShowRoundedCorner="true" runat="server"&gt;

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

![C:\Users\ApoorvahR\Desktop\4.png](search-options-_images\search-options-_img1.png)

_Figure_ _44__18__: Dropdown with incremental search with case sensitive property_  

