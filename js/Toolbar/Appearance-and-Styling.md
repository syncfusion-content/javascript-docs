---
layout: post
title: Appearance-and-Styling
description: appearance and styling 
platform: js
control: Toolbar
documentation: ug
---

# Appearance and Styling 

## Adjusting Toolbar size

### Height

The **height** property is used to set height of the **Toolbar**. Set the value to this property as **number** or **string** type.

{% highlight html %}

    $(function () {
        // declaration
        $("#toolbarcontent").ejToolbar({ height: 300 });
    });
    
{% endhighlight %}

### Width

The **width** property is used to set width of the **Toolbar**. Set the value to this property as **number** or **string** type.

{% highlight html %}

    $(function () {
        // declaration
        $("#toolbarcontent").ejToolbar({ height: "300px" });
    });

{% endhighlight %}

## Enabling Rounded Corner 

The **showRoundedCorner** property is used to enable rounded corner for **Toolbar**. Set the value to this property as **Boolean** type.


{% highlight js %}

    $(function () {
        // declaration
        $("#toolbarcontent").ejToolbar({ showRoundedCorner: true });
    });

{% endhighlight %}

{% include image.html url="/js/Toolbar/Appearance-and-Styling_images/Appearance-and-Styling_img1.png"%}


## Enabling Separator 

The **enableSeparator** property is used to set separator between **Toolbar** items. It separates one or more list items. When you want to separate two set of items, then define them in two separate ‘**ul’** tags and set the value to this property as **Boolean** type.



{% highlight js %}

    $(function () {
        // declaration
        $("#toolbarcontent").ejToolbar({ enableSeparator: true });
    });

{% endhighlight %}



{% include image.html url="/js/Toolbar/Appearance-and-Styling_images/Appearance-and-Styling_img2.png"%}

## Themes

You can control the **style and appearance of the Toolbar** based on **CSS** classes. In order to apply styles to the Toolbar control, you can refer two files - **ej.widgets.core.min.css** and **ej.theme.min.css**. When you refer **ej.widgets.all.min.css** file, it is not necessary to include the files **ej.widgets.core.min.css** and **ej.theme.min.css** in your project**,** as **ej.widgets.all.min.css** is the combination of these two. 

By default, there are 12 themes support available for **Toolbar** control namely

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

## CssClass 

The **cssClass** property is used to set root class for **Toolbar** control theme. Set the value to this property as **string** type.



{% highlight js %}

    $(function () {
        // declaration
        $("#toolbarcontent").ejToolbar({ width: "290px", cssClass: "gradient-lime" });
    });

{% endhighlight %}



{% highlight css %}

<style>
    .gradient-lime {
        background-color: yellowgreen;
    }
</style>


{% endhighlight %}



{% include image.html url="/js/Toolbar/Appearance-and-Styling_images/Appearance-and-Styling_img3.png"%}

