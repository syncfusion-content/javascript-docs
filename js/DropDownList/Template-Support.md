---
layout: post
title: Template-Support
description: template support
platform: js
control: DropDownList
documentation: ug
---

# Template Support

**Dropdown** widget provides the template support for the **Dropdownlist**, when binding the data’s for the dropdown. For this behavior you need to set the common syntax /element in template property. You can add any Html mark-up element inside of dropdown list using this property.

The following steps explains you the behavior of template support with **Dropdownlist**

 In an **HTML** page, add a **&lt;input&gt;** element to configure **Dropdownlist** widget

> {% include image.html url="/js/DropDownList/Concepts-and-Features/Template-Support_images/Template-Support_img1.png" Caption=""%}**Note**: Images for this sample are available in ‘installed location /themes/images’ 

{% highlight html %}

        <div class="control">
            <div class="ctrllabel">Select an expert</div>
            <input type="text" id="dropdownlist" />
        </div>

{% endhighlight %}

{% highlight js %}

       // Initialize the control in JavaScript
        var empList = [
                { text: "Erik Linden", eimg: "3", desig: "Representative", country: "England" }, { text: "John Linden", eimg: "6", desig: "Representative", country: "Norway" },
                { text: "Louis", eimg: "7", desig: "Representative", country: "Australia" }, { text: "Lawrence", eimg: "8", desig: "Representative", country: "India" }
        ];
        $(function () {
            $('#dropdownlist').ejDropDownList({
                dataSource: empList,
                width: "200px",
                template: '<img class="eimg" src="../images/Employee/${eimg}.png" alt="employee" height="50px" width="50px"/>' +
                        '<div class="customalign"><div class="ename"> ${text} </div><div class="desig"> ${desig} </div><div class="cont"> ${country} </div></div>'
            });
        });

{% endhighlight %}

 Customize the template in CSS. 


{% highlight css %}
 
  <style type="text/css">
        .customalign {
            display: inline;
            float: right;
        }
  </style>


{% endhighlight %}



 Output of the above steps.


{% include image.html url="/js/DropDownList/Concepts-and-Features/Template-Support_images/Template-Support_img2.png" Caption="Dropdown with template support"%}
 

