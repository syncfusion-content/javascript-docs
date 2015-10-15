---
layout: post
title: Appearance-and-Styling
description: appearance and styling
platform: js
control: AutoComplete
documentation: ug
---

# Appearance and Styling

## Adjusting AutoComplete size

**AutoComplete** widget allows you to set the height and width of the textbox element in AutoComplete. The **height** and **width** properties take pixel values to set the dimension accordingly.

### Define height and width for AutoComplete textbox

The following steps explain the **dimensional** properties of an AutoComplete textbox.

 In the **HTML** page, add an **&lt;input&gt;** element to configure AutoComplete widget.

{% highlight html %}

    <input type="text" id="autocomplete" />

{% endhighlight %}

 Configure dimensions for **AutoComplete** control as follows.

{% highlight js %}

     $('#autocomplete').ejAutocomplete({
         height: "50px",
         width: "250px",
         multiSelectMode: ej.MultiSelectMode.Delimiter,
         dataSource: carList
     });	 

{% endhighlight %}

The following image is the output for **AutoComplete** textbox with customized dimensions.

{% include image.html url="/js/Autocomplete/Appearance-and-Styling_images/Appearance-and-Styling_img1.png"%}

## Rounded corner

By enabling the **showRoundedCorner** property, you can customize the shape of the AutoComplete widget from a regular rectangular shape to a rounded rectangle shape that is set to ‘**False**’ by default.

### Enabling Rounded corner 

The following steps explain enabling the **showRoundedCorner** property for an AutoComplete.

In the **HTML** page, add an **&lt;input&gt;** element to configure **AutoComplete** widget.

{% highlight html %}

<input type="text" id="autocomplete" />


{% endhighlight %}



 Enable **showRoundedCorner** for AutoComplete control as follows.

{% highlight js %}

    $('#autocomplete').ejAutocomplete({
       width: 205,
       dataSource: carList,
       showRoundedCorner: true
    });

{% endhighlight %}



The following image is the output for AutoComplete when **showRoundedCorner** is set to “**True**”.

{% include image.html url="/js/Autocomplete/Appearance-and-Styling_images/Appearance-and-Styling_img2.png"%}

## Watermark text

**Watermark text** property provides you with an option to display a faded text in the AutoComplete textbox when the textbox is empty.

### Defining Watermark text 

The following steps explain you how to configure **watermarkText** property for an AutoComplete textbox.

In the **HTML** page, add an **&lt;input&gt;** element to configure **AutoComplete** widget.

{% highlight html %}

<input type="text" id="autocomplete" />


{% endhighlight %}



 Enable **watermark** text for AutoComplete control as follows.

{% highlight js %}

    $('#autocomplete').ejAutocomplete({
      width: 205,
      dataSource: carList,
      watermarkText: "Select an item"
    });

{% endhighlight %}



The following image is the output for AutoComplete when **watermarkText** is defined.

{% include image.html url="/js/Autocomplete/Appearance-and-Styling_images/Appearance-and-Styling_img3.png"%}

## Adjusting Suggestion list size

AutoComplete widget provides you with a property to define the dimensions of the popup panel that holds the suggestions list items. The **popupHeight** and **popupWidth** properties allow you to set the maximum height and width of the popup element for use when the content exceeds the default dimensions.

### Configure dimensions of PopUp panel

The following steps help you set height and width of the popup panel of an **AutoComplete** textbox.

 In the **HTML** page, add an **&lt;input&gt;** element to configure AutoComplete widget.

{% highlight html %}

<input type="text" id="autocomplete" />


{% endhighlight %}



Configure dimensions for popup panel in **AutoComplete** control as follows.

{% highlight js %}

    $('#autocomplete').ejAutocomplete({
      width: 205,
      dataSource: carList,
      filterType: "startswith",
      popupHeight: "80px",
      popupWidth: "350px"
    });

{% endhighlight %}


The following image is the output for **AutoComplete,** after configuring the height and width of the popup panel.

{% include image.html url="/js/Autocomplete/Appearance-and-Styling_images/Appearance-and-Styling_img4.png"%}

## PopUp Time Delay

AutoComplete widget allows you to set the time delay to fetch the list items. The value of **delaySuggestionTimeout** is set in milliseconds, so that data search time can be configured. This enhances the turnaround time to populate the list items.

### Configure Time delay of PopUp panel

The following steps are used to set the time delay to load the popup panel of an AutoComplete textbox.

 In the **HTML** page, add an **&lt;input&gt;** element to configure the AutoComplete widget.

{% highlight html %}

<input type="text" id="autocomplete" />


{% endhighlight %}



Configure the delay time for popup panel in **AutoComplete** control as follows.

{% highlight js %}

    $('#autocomplete').ejAutocomplete({
      width: 205,
      dataSource: carList,
      filterType: "startswith",
      delaySuggestionTimeout: 1000
    });

{% endhighlight %}


This takes 1000ms to display the popup panel list items.

## Theme

AutoComplete control’s style and appearance are controlled based on CSS classes. In order to apply styles to the AutoComplete control, you can refer 2 files namely, **ej.widgets.core.min.css** and **ej.theme.min.css**. When the file **ej.widgets.all.min.css** is referred, then it is not necessary to include the files **ej.widgets.core.min.css** and **ej.theme.min.css** in your project**,** as **ej.widgets.all.min.css** is the combination of these two. 

By default, there are 12 theme supports available for AutoComplete control namely:

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

**CSS class** is used to customize the AutoComplete control’s appearance. Define CSS class as per requirement and assign the class name to cssClass property.

#### Configure AutoComplete textbox using CSS class

The following steps allow you to configure **CSS** class** for an AutoComplete textbox.

 In the **HTML** page, add an **&lt;input&gt;** element to configure the **AutoComplete** widget.

{% highlight html %}

<input type="text" id="autocomplete" />


{% endhighlight %}



 Define CSS class to customize the AutoComplete widget.

{% highlight css %}

   <style type="text/css" class="cssStyles">
        /* Customize the PopUp panel */
        .customCss
        {
            border-color:Purple;
            background-color: #E0E0E0;
        }
        /* Customize the AutoComplete input textbox */
       .customCss .e-autocomplete
       {
          background-color: #FFFFCC;
          font-weight:bold;
          font-family: sans-serif;
       }
    </style>




{% endhighlight %}



Add the **cssClass** property to **AutoComplete** textbox.

{% highlight js %}

    $('#autocomplete').ejAutocomplete({
      width: 205,
      dataSource: carList,
      cssClass: "customCss"
    });

{% endhighlight %}



The following image is of an AutoComplete textbox configured based on CSS class.

{% include image.html url="/js/Autocomplete/Appearance-and-Styling_images/Appearance-and-Styling_img5.png"%}

