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

In an HTML page, add a &lt;input&gt; element to configure DropdownList widget

{% highlight html %}

     <input type="text" id="dropdownlist" />

      <div id="list">
            <ul>
                <li>Art</li>
                <li>Architecture</li>
                <li>Biography</li>
                <li>comics</li>
                <li>Sports</li>
            </ul>

        </div>

{% endhighlight %}

{% highlight js %}

        $(function () {
            $('#dropdownlist').ejDropDownList({
                targetID: "list",                
                width: "200px",               
                showRoundedCorner: true,
                enableIncrementalSearch: true,
                caseSensitiveSearch:false
            });
        });

{% endhighlight %}

Output of the above steps

{% include image.html url="/js/DropDownList/Search-Options_images/Search-Options_img1.png" Caption="Dropdown with incremental search with case sensitive property"%}
