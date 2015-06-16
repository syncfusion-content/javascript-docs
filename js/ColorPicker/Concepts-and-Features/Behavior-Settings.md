---
layout: post
title: Behavior-Settings
description: behavior settings
platform: js
control: ColorPicker
documentation: ug
---

# Behavior Settings

## showPreview

The **ColorPicker** control provides live preview support for current cursor selection color and selected color. **showPreview** property allows you to preview the selected color in the picker or from the palette.

The **showPreview** property is Boolean type and its default value is true.

* In the **HTML** page, add a **&lt;input&gt;** element to render **ColorPicker** widget

{% highlight html %}

**[HTML]**

     <input type="text" id="colorPicker" />    

{% endhighlight %}

{% highlight js %}

**[JAVASCRIPT]**
 
<script>
    jQuery(function ($) {
        $("#colorPicker").ejColorPicker({ value: "#278787", showPreview: true });
      });
</script>

{% endhighlight %}

The following screenshot displays the output of the above code example.

{% include image.html url="/js/ColorPicker/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img1.png" Caption="Figure 5: ColorPicker with Show Preview option"%}

## showRecentColors

The **ColorPicker** control allows you to store the color values in custom list by using **showRecentColors** property. The **ColorPicker** keeps up to 11 colors in a custom list.  By clicking the add button, the selected color from picker or palette gets added in the recent color list.  

The **showRecentColors** property is Boolean type and its default value is false.

* In the **HTML** page, add a **&lt;input&gt;** element to render **ColorPicker** widget

{% highlight html %}

**[HTML]**

     <input type="text" id="colorPicker" />    

{% endhighlight %}

{% highlight js %}

**[JAVASCRIPT]**
 
<script>
    jQuery(function ($) {
        $("#colorPicker").ejColorPicker({ value: "#278787", showRecentColors: true });
      });
</script>

{% endhighlight %}


The following screenshot displays the output of the above code example.

{% include image.html url="/js/ColorPicker/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img2.png" Caption="Figure 6: ColorPicker with Recent Color Swatches"%}

## enableOpacity

The **ColorPicker** control allows you to enable or disable the opacity slider. You can achieve this by using the **enableOpacity** property. 

The **enableOpacity** property is Boolean type and its default value is true.

* In the **HTML** page, add a **&lt;input&gt;** element to render **ColorPicker** widget

{% highlight html %}

**[HTML]**

    <input type="text" id="colorPicker" />    

{% endhighlight %}

{% highlight js %}

**[JAVASCRIPT]**
 
<script>
    jQuery(function ($) {
        $("#colorPicker").ejColorPicker({ value: "#278787", enableOpacity: false });
    });
</script>

{% endhighlight %}


The following screenshot displays the output of the above code example.

{% include image.html url="/js/ColorPicker/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img3.png" Caption="Figure 7: ColorPicker with Opacity Slider as disabled state"%}

## columns

The palette model consists of color values in the rows and columns order. Palette only consists of predefined colors and allows you to select anyone color from it. The **columns** property allows you to modify the number of columns in palette model. 

The **columns** property is Number type and its default value is 10.

* In the **HTML** page, add a **&lt;input&gt;** element to render **ColorPicker** widget

{% highlight html %}

**[HTML]**

    <input type="text" id="colorPicker" />    

{% endhighlight %}

{% highlight js %}

**[JAVASCRIPT]**
 
<script>
    jQuery(function ($) {
        $("#colorPicker").ejColorPicker({ value: "#278787", columns: 9 });
    });
</script>

{% endhighlight %}


The following screenshot displays the output of the above code example.

{% include image.html url="/js/ColorPicker/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img4.png" Caption="Figure 8: ColorPicker with Columns"%}

