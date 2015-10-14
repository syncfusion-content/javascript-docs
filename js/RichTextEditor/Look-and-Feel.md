---
layout: post
title: Look-and-Feel
description: look and feel
platform: js
control: RichTextEditor
documentation: ug
---

# Look and Feel

**RTE** control supports a rich appearance. This control consist of six flat themes and six gradient themes. To use these twelve themes, you can refer to the themes files in **HTML**. 

Two style sheets are required to apply styles to **RTE** control, **ej.widgets.core.min.css** and **ej.theme.min.css**. When you use **ej.widgets.all.min.css**, do not use **ej.widgets.core.min.css** and **ej.theme.min.css** as **ej.widgets.all.min.css** is a combination of these two.

The core style sheet applies styles related to positioning and size, but are not related to the color scheme and are always required for the control to look right and function properly. The theme style sheet applies theme-specific styles, like colors and backgrounds.

The following is the list of the twelve themes supported by **RTE**. 

* default-theme
* flat-azure-dark
* flat-lime
* flat-lime-dark
* flat-saffron
* flat-saffron-dark
* gradient-azure
* gradient-azure-dark
* gradient-lime
* gradient-lime-dark
* gradient-saffron
* gradient-saffron-dark





Add the following code example in your **HTML** page to initialize the **RTE** with gradient-azure-dark theme.


{% highlight html %}

<div class="rte">
    <textarea id="rteSample"></textarea>
</div>

{% endhighlight %}

{% highlight js %}

     //Add the following code in the script section to initialize the RTE with gradient-azure-dark theme.
    $(function () {
        $("#rteSample").ejRTE();
    });
 
{% endhighlight %}


![](Look-and-Feel_images/Look-and-Feel_img1.png)


## Css Class

**RTE** control also allows you to customize its appearance by using user-defined CSS and custom skin options for colors and backgrounds. To apply custom themes, use **cssClass** property. **cssClass** property sets the root class for **RTE** theme.

You can override the existing styles under the theme style sheet by using this property. The theme style sheet applies theme-specific styles like colors and backgrounds. In the following example, the value of **cssClass** property is set as “light-Pink”. ” light-Pink [http://www.w3schools.com/tags/ref_color_tryit.asp?color=DeepPink](http://www.w3schools.com/tags/ref_color_tryit.asp?color=DeepPink)” is added as the root class to **RTE** control at runtime. From this root class, you can customize the **RTE** control theme.

Add the following code example in your **HTML** page.


{% highlight html %}

<div class="rte">
    <textarea id="rteSample"></textarea>
</div>

{% endhighlight %}

{% highlight js %}

    // Add the following code in your script section to render the RTE with cssClass “light-Pink”.
    $(function () {
        $("#rteSample").ejRTE({ cssClass: "light-Pink" });
    });

{% endhighlight %}


In the following style sheet, the active theme style sheet file is overridden by using root class “light-Pink”.

Add the following styles in your styles section.

{% highlight css %}

<style>
    .light-Pink .e-toolbar {
        color: black;
    }
    .light-Pink .e-toolbarspan {
        background-color: #E9A1CE;
    }
    .light-Pink .e-toolbar .e-active {
        background-color: #4C0F2E;
    }
    .light-Pink .editarea {
        background-color: pink;
    }
</style>

{% endhighlight %}



![](Look-and-Feel_images/Look-and-Feel_img2.png)

