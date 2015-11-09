---
layout: post
title: Checkbox-Support
description: checkbox support
platform: js
control: DropDownList
documentation: ug
---

# Checkbox Support

## Show Checkbox 

You can enable the checkbox in the **DropdownList** with this property. The data type of **showCheckbox** value is Boolean type. It maintains multiple selection and gets the checked items on its dropdown client side events.  

## Check All

You can check all the check box in the list by using this property. The data type of **checkAll** needs to be in Boolean type. To achieve this, you need to set **showCheckbox** property as true

## Uncheck All

You can uncheck all the check box in the list by using this property. The data type of **uncheckAll** is Boolean type. To achieve this, set **showCheckbox** property as true.

## Defining the Checkbox support

The following steps explains you the configuration of checkbox options in **DropdownList**

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

    // Initialize the control in JavaScript      
    $(function () {
        $('#dropdownlist').ejDropDownList({
            targetID: "list",
            width: "200px",
            showCheckbox: true,
            checkAll: true                
        });
    });

{% endhighlight %}

Output of the above steps

![](/js/DropDownList/Checkbox-Support_images/Checkbox-Support_img1.png) 
