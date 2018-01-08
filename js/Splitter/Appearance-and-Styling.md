---
layout: post
title: Appearance-and-Styling
description: appearance and styling 
platform: js
control: Splitter
documentation: ug
api: /api/js/ejsplitter
---

# Appearance and Styling 

## Responsive

The **enableAutoResize** option allows the **Splitter** control to adapt its rendering based on the parent container where it is actually placed. When this option is set to true, the **Splitter** control adjusts its height and width based on the outer container that contains it, and also the sub-elements within it adjust to its height, width and position, appropriately.

## Enabling Auto Resize

The following steps explain the implementation of **AutoResize** option in the **Splitter** control. 

In the **HTML** page set the corresponding **&lt;div&gt;** elements for outer and inner splitter control. 

{% highlight html %}

<div id="outerSplitter">
    <div>
        <div style="padding: 0px 15px;">
            <h3 class="h3">JavaScript </h3>
        </div>
    </div>
    <div id="innerSplitter">
        <div>
            <div style="padding: 0px 15px;">
                <h3 class="h3">Tools </h3>
                Essential Tools is an collection of user interface components used to create interactive
                            JavaScript applications.
            </div>
        </div>
        <div>
            <div style="padding: 0px 15px;">
                <h3 class="h3">Grid </h3>
                Essential JavaScript Grid offers full featured a Grid control with extensive support for
                            Grouping and the display of hierarchical data.
            </div>
        </div>
    </div>
</div>

{% endhighlight %}

{% highlight javascript %}

    $("#outerSplitter").ejSplitter({
        height: 280, width: "100%",
        orientation: ej.Orientation.Vertical,
        properties: [{ paneSize: 60 }],
        enableAutoResize: true
    });
    
    $("#innerSplitter").ejSplitter({           
        enableAutoResize: true           
    });

{% endhighlight %}


## Animation Support

The **Splitter** provides you animation support when you expand or collapse the pane. The animation speed can be modified by using the [animationSpeed](https://help.syncfusion.com/api/js/ejsplitter#members:animationspeed) property, that has values in milliseconds.

### Enabling Animation with Animation speed

The following steps explain the implementation of [enableAnimation](https://help.syncfusion.com/api/js/ejsplitter#members:enableanimation) option in the **Splitter** widget.

In the **HTML** page set the corresponding **&lt;div&gt;** element for rendering **Splitter** control. 

{% highlight html %}

<div id="splitter">
    <div>
        <div style="padding: 0px 15px;">
            <h3 class="h3">Tools </h3>
            Essential Tools is an collection of user interface components used to create interactive
            ASP.NET MVC applications.
        </div>
    </div>
    <div>
        <div style="padding: 0px 15px;">
            <h3 class="h3">Grid </h3>
            Essential MVC Grid offers full featured a Grid control with extensive support for
            Grouping and the display of hierarchical data.
        </div>
    </div>
</div>

{% endhighlight %}


{% highlight javascript %}
    
    $("#splitter").ejSplitter({
        height: 280, width: 600,
        enableAnimation: true,
        animationSpeed: 300        
        properties: [{}, { collapsible: true}]
    });

{% endhighlight %}

The output for **Splitter** when **enableAnimation** is “**true**”. Expanding or collapsing the outer pane in the **Splitter** produces the animation effect with the animation speed.

![](/js/Splitter/Appearance-and-Styling_images/Appearance-and-Styling_img3.png) 

## Adjusting Splitter Size

### Height

The height of **Splitter** can be modified by using the [height](https://help.syncfusion.com/api/js/ejsplitter#members:height) property. The default value for **height** property is **null** in **Splitter**. You can set the **height** property by pixel or percentage values.

### Width

The width of **Splitter** can be modified by using the [width](https://help.syncfusion.com/api/js/ejsplitter#members:width) property. The default value for **width** property is **null** in **Splitter**. You can set the **width** property by pixel or percentage values.

### Max Size

Defines the maximum resizable size of the pane when you resize the **Splitter** widget. The default value of **maxSize** is **null** in **Splitter**. You can set the **maxSize** property by pixel values.

### Min Size

Defines the minimum resizable size of the pane when you resize  the **Splitter** widget. The default value of **minSize** is **10** in **Splitter**. You can set the **minSize** property by pixel values.

### Pane Size

Defines the pane size in the **Splitter** widget. The default value of **paneSize** is **0px** in **Splitter**. You can set the **paneSize** property by pixel or percentage values.

## Resizable

Defines whether the pane in the **Splitter** is resizable or not. Setting the **resizable** property as “**false”** disables the resize option to the pane. The default value of **resizable** property is true in **Splitter**.

The following steps explain the implementation of **Splitter** properties. 

In the **HTML** page set the **&lt;div&gt;** element for rendering **Splitter** widget.

{% highlight html %}

<div id="splitter">
    <div>
        <div style="padding: 0px 15px;">
            <h3 class="h3">Tools </h3>
            Essential Tools is an collection of user interface components used to create interactive
            ASP.NET MVC applications.
        </div>
    </div>
    <div>
        <div style="padding: 0px 15px;">
            <h3 class="h3">Grid </h3>
            Essential MVC Grid offers full featured a Grid control with extensive support for
            Grouping and the display of hierarchical data.
        </div>
    </div>
</div>

{% endhighlight %}

{% highlight javascript %}

    $("#splitter").ejSplitter({
        height: 280, width: 600,
        properties: [{}, { collapsible: true, minSize: 100, maxSize: 800, paneSize: 300, resizable: true }]
    });

{% endhighlight %}

The output for **Splitter** after adding the properties.

![](/js/Splitter/Appearance-and-Styling_images/Appearance-and-Styling_img4.png) 

![](/js/Splitter/Appearance-and-Styling_images/Appearance-and-Styling_img5.png) 

![](/js/Splitter/Appearance-and-Styling_images/Appearance-and-Styling_img6.png) 

![](/js/Splitter/Appearance-and-Styling_images/Appearance-and-Styling_img7.png) 

## Theme

**Splitter** control’s style and appearance can be controlled based on CSS classes. In order to apply styles to the **Splitter** control, refer 2 files namely: **ej.widgets.core.min.css** and **ej.theme.min.css**. If the file **ej.widgets.all.min.css** is referred, then it is not necessary to include the files **ej.widgets.core.min.css** and **ej.theme.min.css** in your project**,** as **ej.widgets.all.min.css** is the combination of these two. 

By default, there are 12 themes support available for Autocomplete control namely

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

### CSS Class

The CSS properties can be customized by using **cssClass** in the **Splitter** widget. The following steps explain the implementation of [cssClass](https://help.syncfusion.com/api/js/ejsplitter#members:cssclass) option in the **Splitter** widget.

In the **HTML** page set the corresponding **&lt;div&gt;** element for rendering **Splitter** control. 

{% highlight html %}

<div id="splitter">
    <div>
        <div style="padding: 0px 15px;">
            <h3 class="h3">Tools </h3>
            Essential Tools is an collection of user interface components used to create interactive
            ASP.NET MVC applications.
        </div>
    </div>
    <div>
        <div style="padding: 0px 15px;">
            <h3 class="h3">Grid </h3>
            Essential MVC Grid offers full featured a Grid control with extensive support for
            Grouping and the display of hierarchical data.
        </div>
    </div>
</div> 

{% endhighlight %}

{% highlight javascript %}

    $("#splitter").ejSplitter({
        height: 280, width: 600,
        cssClass: "customCSS"
    });

{% endhighlight %}

Customize the **CSS** class by setting **CSS** properties. 

{% highlight css %}

<style>
    .customCSS {            
        border-color: #661e19;
    }

    /*Customize Splitbar*/
    .customCSS .e-splitbar {
        background-color: #f9c89f;
    }

    /*Customize Splitter pane*/
    .customCSS .e-pane {
        color: #b21010;
        background-color: #f6e492;
    }     
</style>

{% endhighlight %}

The output for **Splitter** after customizing the CSS class.

![](/js/Splitter/Appearance-and-Styling_images/Appearance-and-Styling_img8.png) 

