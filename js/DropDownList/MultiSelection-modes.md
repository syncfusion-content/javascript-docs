---
layout: post
title: MultiSelection-modes
description: multiselection modes
platform: js
control: DropDownList
documentation: ug
---

# MultiSelection modes

**DropdownList** widget allows you to select multiple values from the suggestion list using **allowMultiSelection** property. You can select Multiple values by setting allowMultiSelection value to true.

## Configuring MultiSelection Mode

The following steps explain you the configuration of the **allowMultiSelection** for a **DropdownList** textbox.

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
   </ul>
</div>

{% endhighlight %}

{% highlight js %}

    // Configure multiSelectMode type for Dropdownlist control
    $(function () {
        $('#dropdownlist').ejDropDownList({
            targetID: "list",
            width: "200px",
            showCheckbox: true,
            allowMultiSelection: true
        });
    });

{% endhighlight %}

Output for Dropdown control that provides multiple selection is as follows.

![]("/js/DropDownList/MultiSelection-modes_images/MultiSelection-modes_img1.png") 

