---
layout: post
title: Template-Support
description: template support
platform: js
control: DropDownList
documentation: ug
---

# Template Support

**Dropdown** widget provides the template support for the **Dropdownlist**, when binding the data’s for the dropdown. For this behaviour you need to set the common syntax /element in template property. You can add any Html mark-up element inside of dropdown list using this property.

The following steps explains you the behaviour of template support with **Dropdownlist**

* In an **HTML** page, add a **&lt;input&gt;** element to configure **Dropdownlist** widget

> {% include image.html url="/js/DropDownList/Concepts-and-Features/Template-Support_images/Template-Support_img1.png" Caption=""%}_**Note: Images for this sample are available in ‘installed location /themes/images’**_ 


<table>
<tr>
<td>
<b>[HTML]   </b>     &lt;div class="control"&gt;            <div class="ctrllabel">Select an expert</div>            &lt;input type="text" id="dropdownlist" /&gt;        &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript] </b>// Initialize the control in <b>JavaScript</b><b> </b>   &lt;script type="text/javascript"&gt;        var empList = [                { text: "Erik Linden", eimg: "3", desig: "Representative", country: "England" }, { text: "John Linden", eimg: "6", desig: "Representative", country: "Norway" },                { text: "Louis", eimg: "7", desig: "Representative", country: "Australia" }, { text: "Lawrence", eimg: "8", desig: "Representative", country: "India" }        ];        $(function () {            $('#dropdownlist').ejDropDownList({                dataSource: empList,                width: "200px",<b>                template: '&lt;img class="eimg" src="../images/Employee/${eimg}.png" alt="employee" height="50px" width="50px"/&gt;' +</b><b>                        '&lt;div class="customalign"&gt;&lt;div class="ename"&gt; ${text} &lt;/div&gt;&lt;div class="desig"&gt; ${desig} &lt;/div&gt;&lt;div class="cont"&gt; ${country} &lt;/div&gt;&lt;/div&gt;'</b>            });        });    &lt;/script&gt;</td></tr>
</table>


* Customize the template in CSS. 


{% highlight css %}

[CSS]  
  <style type="text/css">
        .customalign {
            display: inline;
            float: right;
        }
    </style>


{% endhighlight %}



* Output of the above steps.


{% include image.html url="/js/DropDownList/Concepts-and-Features/Template-Support_images/Template-Support_img2.png" Caption=""%}

_Figure 31: Dropdown with template support_  

