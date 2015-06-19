---
layout: post
title: Search-Options
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

The following steps explains you the configuration of search options in **DropdownList**

* In an **HTML** page, add a **&lt;input&gt;** element to configure **DropdownList** widget


<table>
<tr>
<td>
<b>[HTML]</b>&lt;input type="text" id="dropdownlist" /&gt;  &lt;div id="list"&gt;            &lt;ul&gt;                <li>Art</li>                <li>Architecture</li>                <li>Biography</li>                <li>comics</li>                <li>Sports</li>            &lt;/ul&gt;        &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>&lt;script type="text/javascript"&gt;              $(function () {            $('#dropdownlist').ejDropDownList({                targetID: "list",                                width: "200px",                               showRoundedCorner: true,<b>                enableIncrementalSearch: true,</b><b>                caseSensitiveSearch:false</b>            });        });   &lt;/script&gt;</td></tr>
</table>
Output of the above steps

{% include image.html url="/js/DropDownList/Concepts-and-Features/Search-Options_images/Search-Options_img1.png" Caption=""%}

_Figure 18: Dropdown with incremental search with case sensitive property_  

