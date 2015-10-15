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

## Defining the RTL property

The following steps explains you the configuration of **enableRTL** properties in **DropdownList**.

In an **HTML** page, add a **&lt;input&gt;** element to configure **DropdownList** widget

{% highlight html %}

<input type="text" id="dropdownlist" />

<div id="list">
    <ul>
        <li>Art</li>
        <li>Architecture</li>
        <li>Biography</li>
        <li>comics</li>
        <li>Sports</li>
        <li>Science</li>
    </ul>
</div>

{% endhighlight %}

{% highlight js %}

    // Initialize the control in JavaScript
    
    $(function () {
            $('#dropdownlist').ejDropDownList({
                targetID: "list",
                enableRTL:true
            });
       }); 

{% endhighlight %}

Output of the above steps

{% include image.html url="/js/DropDownList/RTL_images/RTL_img1.png" %}