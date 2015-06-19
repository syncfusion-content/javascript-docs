---
layout: post
title: Behavior-settings
description: behavior settings
platform: js
control: Rotator
documentation: ug
---

# Behavior settings

## Enabling rotator

The **“enabled”** property enables or disables the **Rotator** control. The default value is ‘**true**’. The value set to this property is **Boolean** type. You can refer the following code example to set this property.

<table>
<tr>
<td>
<b>[HTML]               </b> &lt;div class="cols-sample-area"&gt;    &lt;ul id="slidercontent" accesskey="e"&gt;        &lt;li&gt;            &lt;img class="image" src="../images/rotator/nature.jpg" title="Nature" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img class="image" src="../images/rotator/bird.jpg" title="Beautiful Bird" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img class="image" src="../images/rotator/sculpture.jpg" title="Amazing Sculptures" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img class="image" src="../images/rotator/seaview.jpg" title="Sea-View" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img class="image" src="../images/rotator/snowfall.jpg" title="Snow Fall" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img class="image" src="../images/rotator/card.jpg" title="Credit Card" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img class="image" src="../images/rotator/night.jpg" title="Colorful Night" /&gt;&lt;/li&gt;    &lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#slidercontent").ejRotator({ <b>enabled: true</b> });    });&lt;/script&gt;</td></tr>
</table>
## Responsive rotator

The “**isResponsive”** property resizes the **Rotator** when the browser window is resized. The default value is ‘**false**’. The value set to this property is **Boolean**. 

{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#slidercontent").ejRotator({ **isResponsive: true** });
    });
</script>


{% endhighlight %}

## Auto Play

The **Rotator** Items continuously rotate without user interference by enable the **enableAutoPlay** property. The default value is ‘**false’**. The value set to this property is **Boolean**. 

{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#slidercontent").ejRotator({ **enableAutoPlay: true** });
    });
</script>


{% endhighlight %}

## Stop on hover

The **stopOnHover** property pauses the **auto play** while hover on the **Rotator** content. The default value is ‘**false**’. The value set to this property is **Boolean**. 

{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#slidercontent").ejRotator({ enableAutoPlay: true, **stopOnHover: true** });
    });
</script>


{% endhighlight %}

## Pager settings

### Pager position

This property specifies the position of the **showPager** in the **Rotator** Item. The default value is ‘**outside**’. The value set to this property is **string** or **enum**. 

* Syncfusion.JavaScript.PagerPosition.BottomLeft

* Syncfusion.JavaScript.PagerPosition.BottomRight

* Syncfusion.JavaScript.PagerPosition.Outside

* Syncfusion.JavaScript.PagerPosition.TopCentre

* Syncfusion.JavaScript.PagerPosition.TopLeft

* Syncfusion.JavaScript.PagerPosition.TopRight





{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#slidercontent").ejRotator({
**pagerPosition: ej.Rotator.PagerPosition.BottomLeft**,
            slideWidth: "630px",
            slideHeight: "350px",
        });
    });
</script>


{% endhighlight %}



{% include image.html url="/js/Rotator/Concepts-and-Features/Behavior-settings_images/Behavior-settings_img1.png" Caption="Figure 6: Rotator control with pager position"%}

### Show pager

The **“showPager”** property turns on or off the **pager** support in the **Rotator** control. The **Pager** is used to navigate the **Rotator** Items. The default value is ‘**true**’. The value set to this property is **Boolean**. 

{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#slidercontent").ejRotator({ **showPager: false** });
    });
</script>


{% endhighlight %}





{% include image.html url="/js/Rotator/Concepts-and-Features/Behavior-settings_images/Behavior-settings_img2.png" Caption="Figure 7: Rotator control with no pager"%}

## Show options

### Show play button

The “**showPlayButton**” property enables play / pause button on **Rotator**. The default value is ‘**false**’. The value set to this property is **Boolean**.

{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#slidercontent").ejRotator({ slideWidth: "600px", **showPlayButton: true** });
    });
</script>


{% endhighlight %}



{% include image.html url="/js/Rotator/Concepts-and-Features/Behavior-settings_images/Behavior-settings_img3.png" Caption="Figure 8: Rotator control with play button"%}

### Show navigate button

The “**showNavigateButton**” property turns on or off the slide buttons (next and previous) in the **Rotator** Items. Slide buttons are used to navigate the **Rotator** Items. The default value is ‘**false**’. The value set to this property is **Boolean**. 

{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#slidercontent").ejRotator({ slideWidth: "500px", **showNavigateButton: true** });
    });
</script>


{% endhighlight %}



{% include image.html url="/js/Rotator/Concepts-and-Features/Behavior-settings_images/Behavior-settings_img4.png" Caption="Figure 9: Rotator control with navigate button"%}

### Show caption

When the **Rotator** Item is an image, you can specify a caption for the **Rotator** Item. The caption text for each **Rotator** Item is set by using the title attribute of the respective **&lt;image&gt;** tag. The caption cannot be displayed when multiple **Rotator** Items are present. The default value is ‘**false**’. The value set to this property is **Boolean**. 

{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#slidercontent").ejRotator({ slideWidth: "500px", **showCaption: true** });
    });
</script>


{% endhighlight %}





{% include image.html url="/js/Rotator/Concepts-and-Features/Behavior-settings_images/Behavior-settings_img5.png" Caption="Figure 10: Rotator control with caption"%}

