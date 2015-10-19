---
layout: post
title: Template-Support
description: template support
platform: js
control: Toolbar
documentation: ug
---

# Template Support

Template allows you to insert custom controls inside the toolbar items. Also you can design simple drop down buttons listing the items and radio button inside the **Toolbar**.

Set the list for **DropDown control** inside a list tag and define this tag as a **Toolbar** item. You can use all simple controls as a **Toolbar** item. To add RadioButton and DropDownList to **Toolbar**, use the following code example.

{% highlight html %}

<div id="toolbarcontent">
   <ul>
      <li>
         <div>
            <input type="radio" name="small" id="Radio1" />
         </div>
         option
      </li>
      <li id="Dropdown" title="Dropdown Control">
         <input id="selectcar" type="text" />
         <div id="cars">
            <ul>
               <li>Audi A4</li>
               <li>Audi A5</li>
               <li>Audi A6</li>
               <li>Audi A7</li>
            </ul>
         </div>
      </li>
   </ul>
</div>

{% endhighlight %}

{% highlight js %}

    $(function () {
        // declaration
        $("#Radio1").ejRadioButton({ checked: false });
        $('#selectcar').ejDropDownList({ height: "23px", width: "100px", targetID: "cars", selectedItemIndex: 0 });
        $("#toolbarcontent").ejToolbar({ width: "250px", height: "28px" });
    });


{% endhighlight %}


The following screenshot displays a Toolbar with embedded controls.

![](/js/Toolbar/Template-Support_images/Template-Support_img1.png)
