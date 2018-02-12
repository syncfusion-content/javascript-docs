---
layout: post
title: Miscellaneous
description: miscellaneous
platform: js
control: ColorPicker
documentation: ug
api: /api/js/ejcolorpicker
---

# Miscellaneous

## getValue

The **getValue**() method in **ColorPicker** returns the hexadecimal value.

In the **HTML** page, add a **&lt;input&gt;** element to render **ColorPicker** widget

{% highlight html %}

<input type="text" id="colorPicker" />    

{% endhighlight %}

{% highlight javascript %}

 
    var ColorObj;
    jQuery(function ($) {
        ColorObj = $("#colorPicker").ejColorPicker({ value: "#278787" }).data('ejColorPicker');
        ColorObj.getValue();
    });

{% endhighlight %}


## setValue

The **setValue**() method in **ColorPicker** is used to set the color value. The given value is in hexadecimal form.

In the **HTML** page, add a **&lt;input&gt;** element to render **ColorPicker** widget

{% highlight html %}


<input type="text" id="colorPicker" />    

{% endhighlight %}

{% highlight javascript %}
 
    var ColorObj;
    jQuery(function ($) {
        ColorObj = $("#colorPicker").ejColorPicker().data('ejColorPicker');
        ColorObj.setValue("#278787");
    });

{% endhighlight %}


## getColor

The **getColor**() method in **ColorPicker** control returns the color value in r,g,b,a form.

In the **HTML** page, add a **&lt;input&gt;** element to render **ColorPicker** widget

{% highlight html %}


<input type="text" id="colorPicker" />    

{% endhighlight %}

{% highlight javascript %}

 
    var ColorObj;
    jQuery(function ($) {
        ColorObj = $("#colorPicker").ejColorPicker({ value: "#278787" }).data('ejColorPicker');
        ColorObj.getColor();
    });

{% endhighlight %}

## Enable/Disable Colorpicker widget

**Colorpicker** widget provides you an option to enable /disable the widget. You can disable the TimePicker by setting the “**enabled**” property value as **false**.

The following steps explain you to enable/disable property in **Colorpicker** widget.

In the **HTML** page, add a **&lt;input&gt;** element to configure **Button** widget.

{% highlight html %}


    <input type="text" id="colorPicker"/> 

{% endhighlight %}

{% highlight javascript %}

    // To enable/disable Button controls use the following code example.
    //disable Button:
    $(function () {
       $('#colorPicker').ejColorPicker({ value: "#278787" });
        // Create ColorPicker instance
        var colorObj = $("#colorPicker").data("ejColorPicker");
        colorObj.disable(); // disables the colorPicker
    });

    //enable Button:
    $(function () {
      $('#colorPicker').ejColorPicker({ value: "#278787" });
        // Create ColorPicker instance
        var colorObj = $("#colorPicker").data("ejColorPicker");
        colorObj.enable(); // enables the colorPicker
    });

{% endhighlight %}



## showTooltip

The **showTooltip** property of the colorpicker control allows to shows tooltip to notify the slider value in color picker control

{% highlight html %}


    <input type="text" id="colorPicker"/>    

{% endhighlight %}

{% highlight javascript %}

    $(function () {
       $('#colorPicker').ejColorPicker({ value: "#278787", showTooltip: true});
    });

{% endhighlight %}


## showSwitcher

The **showSwitcher** property of the colorpicker control allows show/hides the switcher button in ColorPicker control.It helps to switch palette or picker mode in colorpicker.its default value is **true**

{% highlight html %}


    <input type="text" id="colorPicker"/>    

{% endhighlight %}

{% highlight javascript %}

    $(function () {
       $('#colorPicker').ejColorPicker({ value: "#278787", showSwitcher: false}); // hide the switcher button in colorpicker control.
    });

{% endhighlight %}


## showApplyCancel

The **showApplyCancel** property of the colorpicker control allows to show/hides the apply and cancel buttons in ColorPicker control.its default value is **true**.

{% highlight html %}


    <input type="text" id="colorPicker"/>    

{% endhighlight %}

{% highlight javascript %}

    $(function () {
       $('#colorPicker').ejColorPicker({ value: "#278787", showApplyCancel: false});
    });

{% endhighlight %}


## showClearButton

The **showClearButton** property of the colorpicker control allows to show/hides the clear button in ColorPicker control.its default value is **true**.

{% highlight html %}

    <input type="text" id="colorPicker"/>    

{% endhighlight %}

{% highlight javascript %}

    $(function () {
       $('#colorPicker').ejColorPicker({ value: "#278787", showClearButton: false});
    });

{% endhighlight %}
