---
layout: post
title: Image-with-Contents
description: image with contents 
platform: js
control: Rotator
documentation: ug
---

# Image with Contents 

This feature allows you to add text along with the **image** in **Rotator** control. This is achieved by splitting the content into two panels. In the following code example, image is given in the left panel and text is given in the right panel.

<table>
<tr>
<td>
<b>[HTML]           </b>&lt;div class="cols-sample-area"&gt;    &lt;ul id="slidercontent"&gt;        &lt;li&gt;            &lt;div class="leftPanel"&gt;                &lt;img src="../images/rotator/tablet.jpg" /&gt;            &lt;/div&gt;            &lt;div class="rightPanel blck"&gt;                <div class="contentPanel">Tablet &lt;/div&gt;                &lt;ul&gt;                    <li>A tablet computer, or simply tablet, is a mobile computer with display, circuitry and battery in a single unit.&lt;/li&gt;                    &lt;li&gt;                    Tablets are equipped with sensors, including cameras, microphone, accelerometer and touchscreen,                &lt;/ul&gt;            &lt;/div&gt;        &lt;/li&gt;        &lt;li&gt;            &lt;div class="leftPanel"&gt;                &lt;img src="../images/rotator/nature.jpg" /&gt;            &lt;/div&gt;            &lt;div class="rightPanel"&gt;                <div class="contentPanel">Nature &lt;/div&gt;                &lt;ul&gt;                    <li>The health of the natural environment is critical to the long-term future of the planet</li>                    <li>Nature, in the broadest sense, is equivalent to the natural, physical, or material world or universe.&lt;/li&gt;                &lt;/ul&gt;            &lt;/div&gt;        &lt;/li&gt;        &lt;li&gt;            &lt;div class="leftPanel"&gt;                &lt;img src="../images/rotator/card.jpg" /&gt;            &lt;/div&gt;            &lt;div class="rightPanel credit"&gt;                <div class="contentPanel">Credit card &lt;/div&gt;                &lt;ul&gt;                    <li>A credit card is a payment card issued to users as a system of payment</li>                    <li>It allows the cardholder to pay for goods and services based on the holder's promise to pay for them</li>                &lt;/ul&gt;            &lt;/div&gt;        &lt;/li&gt;        &lt;li&gt;            &lt;div class="leftPanel"&gt;                &lt;img src="../images/rotator/rose.jpg" /&gt;            &lt;/div&gt;            &lt;div class="rightPanel"&gt;                <div class="contentPanel">Rose &lt;/div&gt;                &lt;ul&gt;                    <li>A rose is a woody perennial of the genus Rosa, within the family Rosaceae</li>                    <li>Flowers vary in size and shape and are usually large and showy,                    There are over 100 species                    &lt;/li&gt;                &lt;/ul&gt;            &lt;/div&gt;        &lt;/li&gt;        &lt;li&gt;            &lt;div class="leftPanel"&gt;                &lt;img src="../images/rotator/snowfall.jpg" /&gt;            &lt;/div&gt;            &lt;div class="rightPanel rightSide"&gt;                <div class="contentPanel">Snowfall &lt;/div&gt;                &lt;ul&gt;                    <li>Mt. Baker ski area in Washington State has the world record for snowfall at 1,140 inches of snow in the 1998/1999 winter season</li>                    <li>Mt. Baker ski area is located near but not on the real 10,781 Mount Baker</li>                &lt;/ul&gt;            &lt;/div&gt;        &lt;/li&gt;    &lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration            $("#slidercontent").ejRotator({            slideWidth: "600px",            displayItemsCount: "1",            slideHeight: "300px",            navigateSteps: "1",            enableResize: true,            pagerPosition: ej.Rotator.PagerPosition.Outside,            orientation: ej.Orientation.Horizontal,            showPager: true,            enabled: true,            showCaption: false,            allowKeyboardNavigation: true,            showPlayButton: true,            animationType: "slide",            enableRTL: true,        });    });&lt;/script&gt;</td></tr>
</table>


{% highlight css %}

**[CSS]**
<style type="text/css" class="cssStyles">
    #slidercontent > li {
        background-color: #9ee8d8;
    }

        #slidercontent > li .leftPanel {
            float: left;
            width: 700px;
            height: 300px;
            padding-right: 0px;
        }

            #slidercontent > li .leftPanel img {
                width: 700px;
                height: 300px;
            }

    #slidercontent .rightPanel {
        background-color: #FFFFFF;
        height: 259px;
        margin-left: 410px;
        margin-top: 21px;
        opacity: 0.5;
        padding-left: 10px;
        position: absolute;
        width: 260px;
    }

        #slidercontent .rightPanel.credit {
            opacity: 0.6;
        }

        #slidercontent .rightPanel.blck {
            background-color: black;
        }

            #slidercontent .rightPanel.blck li {
                color: white;
                list-style: none;
                line-height: 2;
            }

            #slidercontent .rightPanel.blck .contentPanel {
                padding-top: 30px;
                color: white;
            }

        #slidercontent .rightPanel .contentPanel {
            color: #000000;
            font-size: large;
            font-weight: bold;
            left: 16px;
            padding-top: 30px;
            position: relative;
        }

        #slidercontent .rightPanel li {
            color: black;
            list-style: none;
            line-height: 2;
        }

        #slidercontent .rightPanel.rightSide {
            margin-left: 20px;
            background-color: black;
        }

            #slidercontent .rightPanel.rightSide li {
                color: white;
                list-style: none;
                line-height: 2;
            }

            #slidercontent .rightPanel.rightSide .contentPanel {
                padding-top: 30px;
                color: white;
            }

    .rightPanel > ul {
        padding: 6px 17px 17px;
    }
</style>


{% endhighlight %}





{% include image.html url="/js/Rotator/Concepts-and-Features/Image-with-Contents_images/Image-with-Contents_img1.png" Caption="Figure 12: Rotator control with image and text"%}

## Display items

### Display Items count 

This property specifies the number of **Rotator** Items to be displayed. The default value is ‘**1’**. The value set to this property is **string** or **number**.

{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
       // declaration
        $("#slidercontent").ejRotator({ slideWidth: "200px", **displayItemsCount: 3**,
slideHeight: "165px"
        });
    });
</script>
**[CSS]**
<style type="text/css" class="cssStyles">
    #slidercontent > li .image {
        width:200px;
        height:165px;
    }
</style>


{% endhighlight %}



{% include image.html url="/js/Rotator/Concepts-and-Features/Image-with-Contents_images/Image-with-Contents_img2.png" Caption="Figure 13: Rotator control with display item count"%}

### Navigate steps

This property specifies the number of **Rotator** Items to **navigate** on a single click (next/previous/play buttons). The **navigateSteps** property value must be less than or equal to the **displayItemsCount** property value. The default value is ‘**1**’. The value set to this property is **string** or **number**.

{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#slidercontent").ejRotator({ slideWidth: 200, slideHeight: 165, displayItemsCount: 2, **navigateSteps: 2** });
    });
</script>
**[CSS]**
<style type="text/css" class="cssStyles">
    #slidercontent > li .image {
        width:200px;
        height:165px;
    }
</style>


{% endhighlight %}



{% include image.html url="/js/Rotator/Concepts-and-Features/Image-with-Contents_images/Image-with-Contents_img3.png" Caption="Figure 14: Rotator control with navigate steps"%}

### Start index

This property sets the **index** of the slide that is displayed first. The default value is ‘1’. The value set to this property is **string** or **number**.

{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#slidercontent").ejRotator({ slideWidth: 500, **startIndex: 4** });
    });
</script>


{% endhighlight %}



{% include image.html url="/js/Rotator/Concepts-and-Features/Image-with-Contents_images/Image-with-Contents_img4.png" Caption="Figure 15: Rotator control with start index	"%}

### Frame space

This property sets the space between the **Rotator** Items. The value set to this property is **string** or **number**.

{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#slidercontent").ejRotator({ slideWidth: "500px", slideHeight: "300px", displayItemsCount: 2, **frameSpace: "30px"** });
    });
</script>


{% endhighlight %}

## Animation 

**animationType** property specifies the **Animation** type for the **Rotator** Item. **animationType** options include slide, fastSlide, slowSlide, and other custom easing animationTypes. The default value is ‘**slide**’. The value set to this property is **string**. 

{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#slidercontent").ejRotator({ slideWidth: "500px", **animationType: "slowSlide"** });
    });
</script>


{% endhighlight %}

### Animation speed

This property sets the **speed** of slide transition. The default value is ‘**600**’. The value set to this property is **string** or **number**.

{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#slidercontent").ejRotator({ slideWidth: "500px", **animationSpeed: 3000** });
    });
</script>


{% endhighlight %}

### Delay

This property sets the **delay** between the **Rotator** Items to move after the slide transition. The default value is **500**. The value set to this property is **string** or **number.**

{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#slidercontent").ejRotator({ slideWidth: "500px", **delay: 5000** });
    });
</script>


{% endhighlight %}

## Theme

**Rotator** control’s style and appearance are controlled based on **CSS****classes**. In order to apply styles to the **Rotator** control, you can refer 2 files namely, **ej.widgets.core.min.css** and **ej.theme.min.css**. When the file **ej.widgets.all.min.css** is referred, then it is not necessary to include the files **ej.widgets.core.min.css** and **ej.theme.min.css** in your project**,** as **ej.widgets.all.min.css** is the combination of these both. 

By default, there are 12 themes support available for **Rotator** control as follows,

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

### Css class

This property is used to set **root****class** for **Rotator** control theme. The value set to this property is **string** type.

{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#slidercontent").ejRotator({ slideWidth: 500, slideHeight: 300, cssClass: "flat-lime" });
    });
</script>


{% endhighlight %}

Add the following code in your **Css**.

{% highlight css %}

**[CSS]**
<style>
    .flat-lime {
        background-color: yellowgreen;
    }
</style>


{% endhighlight %}





{% include image.html url="/js/Rotator/Concepts-and-Features/Image-with-Contents_images/Image-with-Contents_img5.png" Caption="Figure 16: Rotator control with cssClass"%}

