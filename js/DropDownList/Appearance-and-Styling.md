---
layout: post
title: Appearance-and-Styling
description: appearance and styling
platform: js
control: DropDownList
documentation: ug
---

# Appearance and Styling

## Popup Customization  

### Popup Height

**DropdownList** widget provides you support to customize the dimensions of the dropdown popup. By using **popupHeight** property, you can set the height of the popup list. Its data type is string. 

### Popup Width

Dropdown list widget provides you support to customize the dimensions of the dropdown popup. By using **popupWidth** property, you can set the width of the popup list. Its data type is string. 

### Defining the popup customizing properties

The following steps explains you the configuration of **popupHeight** & **popupWidth** properties in **DropdownList**

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
        <li>Science</li>
    </ul>
</div>

{% endhighlight %}

{% highlight js %}

         // Initialize the control in JavaScript
         $(function () {
            $('#dropdownlist').ejDropDownList({
                targetID: "list",
                width:"250px",
                popupWidth: "250px",
                popupHeight: "100px"              
            });
        });

{% endhighlight %}

 Output of the above steps

{% include image.html url="/js/DropDownList/Appearance-and-Styling_images/Appearance-and-Styling_img1.png" %}

## Adjusting Dropdown size

### Width

DropdownList widget provides you support to customize the dimensions of the dropdown textbox. By using **width** property you can set the width of the dropdown textbox. Its data type is string.

### Height

DropdownList widget provides you support to customize the dimensions of the dropdown textbox. By using **height** property, you can set the height of the dropdown textbox. Its data type is string.

### Defining the dropdown size properties

The following steps explains you the configuration of **height** & **width** properties in **DropdownList**

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
        <li>Science</li>
    </ul>
</div>

{% endhighlight %}

{% highlight js %}
 
    // Initialize the control in JavaScript
    $(function () {
        $('#dropdownlist').ejDropDownList({
            targetID: "list",
            width: "250px",
            height: "50px"                 
        });
    });

{% endhighlight %}

Output of the above steps


{% include image.html url="/js/DropDownList/Appearance-and-Styling_images/Appearance-and-Styling_img2.png" %}  

## Water Mark

**DropdownList** widget provides the support to water mark of the dropdown textbox. The **watermarkText** defines the text that display on page load. Its data type is string.

### Defining the Water Mark property

The following steps explains the configuration of **watermarkText** properties in DropdownList.

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
        <li>Science</li>
    </ul>
</div>

{% endhighlight %}

{% highlight js %}
  
    // Initialize the control in JavaScript
    $(function () {
        $('#dropdownlist').ejDropDownList({
            targetID: "list",
            watermarkText: "Select"
        });
    }); 

{% endhighlight %}

Output of the above steps


{% include image.html url="/js/DropDownList/Appearance-and-Styling_images/Appearance-and-Styling_img3.png" %}  

## Enabling Rounded corner

**DropdownList** widget provides you support to change the appearance of dropdown textbox. By using **showRoundedCorner** you can create a rounded corner on the dropdown textbox. Its data type is Boolean.

The following steps explains you  the configuration of Rounded corner of the **DropdownList**

In an HTML page, add a &lt;input&gt; element to configure DropdownList widget.

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
            showRoundedCorner:true
        });
    });	

{% endhighlight %}

Output of the above steps
 
{% include image.html url="/js/DropDownList/Appearance-and-Styling_images/Appearance-and-Styling_img4.png" %}  

## Icons Support

You can add the icons or images with list items in dropdown popup by using sprite **CSS** class. The following steps explains you the configuration about the icons support with **DropdownList**



> **Note:** Images for this sample are available in ‘installed location /themes/images’ and you need to define images in mentioned CSS. Henceforth the images display. 

In an HTML page, add a &lt;input&gt; element to configure DropdownList widget

{% highlight html %}

<input type="text" id="dropdownlist" />

<div id="mailtoolslist">
    <ul>
        <li>
            <div class="mailtools categorize"></div>
            Categorize and Move</li>
        <li>
            <div class="mailtools done"></div>
            Done</li>
        <li>
            <div class="mailtools flag"></div>
            Flag & Move</li>
        <li>
            <div class="mailtools forward"></div>
            Forward</li>
        <li>
            <div class="mailtools movetofolder"></div>
            Move to Folder</li>
        <li>
            <div class="mailtools newmail"></div>
            New E-mail</li>
        <li>
            <div class="mailtools meeting"></div>
            New Meeting</li>
        <li>
            <div class="mailtools reply"></div>
            Reply & Delete</li>
    </ul>
</div>

{% endhighlight %}

{% highlight js %}

    // Initialize the control in JavaScript
    var target;
    $(function () {
        $('#dropdownlist').ejDropDownList({
            targetID: "mailtoolslist",
            width:"195px"
        });
    });	

{% endhighlight %}

Configure sprite **CSS** styles to **DropdownList**

{% highlight css %}

<style type="text/css" class="cssStyles">
    /*controls*/
    .mailtools {
        display: block;
        background-image: url('../images/iconsapps.png');
        height: 25px;
        width: 25px;
        background-position: center center;
        background-repeat: no-repeat;
    }

    .mailtools.done {
        background-position: 0 0;
    }

    .mailtools.movetofolder {
        background-position: 0 -22px;
    }

    .mailtools.categorize {
        background-position: 0 -46px;
    }

    .mailtools.flag {
        background-position: 0 -70px;
    }

    .mailtools.forward {
        background-position: 0 -94px;
    }

    .mailtools.newmail {
        background-position: 0 -116px;
    }

    .mailtools.reply {
        background-position: 0 -140px;
    }

    .mailtools.meeting {
        background-position: 0 -164px;
    }

    .control {
        margin-left: 20px;
    }

    .ctrllabel {
        padding-bottom: 3px;
    }
</style>

{% endhighlight %}


Output of the above steps

{% include image.html url="/js/DropDownList/Appearance-and-Styling_images/Appearance-and-Styling_img6.png" %}  

## Animation with Dropdown list

This feature adds some animation effect to dropdown widget when show /hide the popup list. This is achieved by setting Boolean value to **enableAnimation** property**.**

### Defining the Animation property

The following steps explains you the configuration of **enableAnimation** properties in **DropdownList**

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
        <li>Science</li>
    </ul>
</div>

{% endhighlight %}

{% highlight js %}

    // Initialize the control in JavaScript
    $(function () {
        $('#dropdownlist').ejDropDownList({
            targetID: "list",
            enableAnimation : true
        });
    }); 

{% endhighlight %}

## Theme

**DropdownList** control’s style and appearance can be controlled based on **CSS** classes. In order to apply styles to the **DropdownList** control, you need to refer two files namely, **ej.widgets.core.min.css** and **ej.theme.min.css**. If the file **ej.widgets.all.min.css** is referred, then it is not necessary to include the files **ej.widgets.core.min.css** and **ej.theme.min.css** in your project**,** as **ej.widgets.all.min.css** is the combination of these two. 

By default, there are 12 themes support available for **DropdownList** control namely

* bootstrap-theme
* default-theme
* flat-azure-dark
* fat-lime
* flat-lime-dark
* flat-saffron
* flat-saffron-dark
* gradient-azure
* gradient-azure-dark
* gradient-lime
* gradient-lime-dark
* gradient-saffron
* gradient-saffron-dark

## Custom class with dropdown 

**CSS** class can be used to customize the **Dropdown** control appearance. Define a **CSS** class as per your requirement and assign the class name to **cssClass** property. The data type of **cssClass** property is string. 

### Configuring the Custom CSS property

The following steps explains you the configuration of **cssClass** properties in **DropdownList**

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
        <li>Science</li>
    </ul>
</div>

{% endhighlight %}

{% highlight js %}
 
    // Initialize the control in JavaScript
    $(function () {
        $('#dropdownlist').ejDropDownList({
            targetID: "list",
            cssClass: "customclass"
        });
    });

{% endhighlight %}

Configure the **CSS** styles to apply on **DropdownList**

{% highlight css %}
  
<style type="text/css">
    .customclass {
        background-color: #FFFFCC;
        font-weight: bold;
        font-family: sans-serif;
    }
</style>

{% endhighlight %}

Output of the above steps

{% include image.html url="/js/DropDownList/Appearance-and-Styling_images/Appearance-and-Styling_img7.png" %} 

