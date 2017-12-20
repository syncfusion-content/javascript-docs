---
layout: post
title: Behavior-settings
description: behavior settings
platform: js
control: Rotator
documentation: ug
api: /api/js/ejrotator
---

# Behavior settings

## Enabling rotator

The [enabled](https://help.syncfusion.com/api/js/ejrotator#members:enabled) property enables or disables the **Rotator** control. The default value is ‘**true**’. The value set to this property is **Boolean** type. You can refer the following code example to set this property.

  {% highlight html %}

  
<div class="cols-sample-area">
   <ul id="sliderContent" accesskey="e">
      <li>
         <img class="image" src="../images/rotator/nature.jpg" title="Nature" />
      </li>
      <li>
         <img class="image" src="../images/rotator/bird.jpg" title="Beautiful Bird" />
      </li>
      <li>
         <img class="image" src="../images/rotator/sculpture.jpg" title="Amazing Sculptures" />
      </li>
      <li>
         <img class="image" src="../images/rotator/seaview.jpg" title="Sea-View" />
      </li>
      <li>
         <img class="image" src="../images/rotator/snowfall.jpg" title="Snow Fall" />
      </li>
      <li>
         <img class="image" src="../images/rotator/card.jpg" title="Credit Card" />
      </li>
      <li>
         <img class="image" src="../images/rotator/night.jpg" title="Colorful Night" />
      </li>
   </ul>
</div>


  {% endhighlight %}


  {% highlight javascript %}

    $(function () {
        // declaration
        $("#sliderContent").ejRotator({ enabled: true });
    });

  {% endhighlight %}
  
## Responsive rotator

The [isResponsive](https://help.syncfusion.com/api/js/ejrotator#members:isresponsive) property resizes the Rotator when the browser window is resized. The default value is ‘false’. The value set to this property is Boolean. 

{% highlight javascript %}


    $(function () {
        // declaration
        $("#sliderContent").ejRotator({ isResponsive : true });
    });

{% endhighlight %}

## Auto Play

The **Rotator** Items continuously rotate without user interference by enable the [enableAutoPlay](https://help.syncfusion.com/api/js/ejrotator#members:enableautoplay) property. The default value is ‘**false’**. The value set to this property is **Boolean**. 

{% highlight javascript %}

    $(function () {
        // declaration
        $("#sliderContent").ejRotator({ enableAutoPlay: true });
    });

{% endhighlight %}

## Stop on hover

The [stopOnHover](https://help.syncfusion.com/api/js/ejrotator#members:stoponhover) property pauses the **auto play** while hover on the **Rotator** content. The default value is ‘**false**’. The value set to this property is **Boolean**. 

{% highlight javascript %}

    $(function () {
        // declaration
        $("#sliderContent").ejRotator({ enableAutoPlay: true, stopOnHover: true });
    });


{% endhighlight %}

## Pager settings

### Pager position

The [pagerPosition](https://help.syncfusion.com/api/js/ejrotator#members:pagerposition) property specifies the position of the **showPager** in the **Rotator** Item. The default value is ‘**outside**’. The value set to this property is **string** or **enum**. 

* ej.Rotator.PagerPosition.BottomLeft
* ej.Rotator.PagerPosition.BottomRight
* ej.Rotator.PagerPosition.Outside
* ej.Rotator.PagerPosition.TopCenter
* ej.Rotator.PagerPosition.TopLeft
* ej.Rotator.PagerPosition.TopRight



{% highlight javascript %}

    
    $(function () {
        // declaration
        $("#sliderContent").ejRotator({
            pagerPosition: ej.Rotator.PagerPosition.BottomLeft,
            slideWidth: "630px",
            slideHeight: "350px"
        });
    });

{% endhighlight %}



![](/js/Rotator/Behavior-settings_images/Behavior-settings_img1.png)

### Show pager

The [showPager](https://help.syncfusion.com/api/js/ejrotator#members:showpager) property turns on or off the **pager** support in the **Rotator** control. The **Pager** is used to navigate the **Rotator** Items. The default value is ‘**true**’. The value set to this property is **Boolean**. 

{% highlight javascript %}

    $(function () {
        // declaration
        $("#sliderContent").ejRotator({ showPager: false });
    });

{% endhighlight %}



![](/js/Rotator/Behavior-settings_images/Behavior-settings_img2.png)

## Show options

### Show play button

The [showPlayButton](https://help.syncfusion.com/api/js/ejrotator#members:showplaybutton) property enables play / pause button on **Rotator**. The default value is ‘**false**’. The value set to this property is **Boolean**.

{% highlight javascript %}

    $(function () {
        // declaration
        $("#sliderContent").ejRotator({ slideWidth: "600px", showPlayButton: true });
    });

{% endhighlight %}



![](/js/Rotator/Behavior-settings_images/Behavior-settings_img3.png)

### Show navigate button

The [showNavigateButton](https://help.syncfusion.com/api/js/ejrotator#members:shownavigatebutton) property turns on or off the slide buttons (next and previous) in the **Rotator** Items. Slide buttons are used to navigate the **Rotator** Items. The default value is ‘**false**’. The value set to this property is **Boolean**. 

{% highlight javascript %}

    $(function () {
        // declaration
        $("#sliderContent").ejRotator({ slideWidth: "500px", showNavigateButton: true });
    });

{% endhighlight %}



![](/js/Rotator/Behavior-settings_images/Behavior-settings_img4.png) 

### Show caption

When the **Rotator** Item is an image, you can specify a [caption](https://help.syncfusion.com/api/js/ejrotator#members:showcaption) for the **Rotator** Item. The caption text for each **Rotator** Item is set by using the title attribute of the respective **&lt;image&gt;** tag. The caption cannot be displayed when multiple **Rotator** Items are present. The default value is ‘**false**’. The value set to this property is **Boolean**. 

{% highlight javascript %}

    $(function () {
        // declaration
        $("#sliderContent").ejRotator({ slideWidth: "500px", showCaption: true });
    });

{% endhighlight %}



![](/js/Rotator/Behavior-settings_images/Behavior-settings_img5.png) 

