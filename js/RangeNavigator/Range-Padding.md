---
layout: post
title: Range-Padding
description: Range Padding
platform: js
control: RangeNavigator
documentation: ug
api: /api/js/ejrangenavigator
---

### Range Padding

**Range Padding** adds padding for range in **RangeNavigator**. It allows you to space the grid lines in the **RangeNavigator**.  By default, this property is set to **none**.

#### Numeric

The [`rangePadding`](../api/js/ejrangenavigator#members:rangepadding) property allows you to customize the automatic range calculation using the default auto range calculation for **RangeNavigator**.

{% highlight javascript %}


$("#container").ejRangeNavigator({
   //...
        valueType: "numeric",
        rangePadding: 'none ',
   //...	
  });


{% endhighlight %}

##### None

By default, the [`rangePadding`](../api/js/ejrangenavigator#members:rangepadding) for numerical range is none. The range is calculated from the minimum value to the maximum value of data in the RangeNavigator.

The following screenshot illustrates a **RangeNavigator** with [`rangePadding`](../api/js/ejrangenavigator#members:rangepadding) set to none.



![](/js/RangeNavigator/Range-Padding_images/Range-Padding_img1.png) 

##### Additional

When you set the [`rangePadding`](../api/js/ejrangenavigator#members:rangepadding) for numerical range to **Additional**, range is padded with an interval.

The following screenshot illustrates a **RangeNavigator** with [`rangePadding`](../api/js/ejrangenavigator#members:rangepadding) set to additional.



![](/js/RangeNavigator/Range-Padding_images/Range-Padding_img2.png) 

##### Normal

In normal [`rangePadding`](../api/js/ejrangenavigator#members:rangepadding), automatic range calculation differs based on the data. 

The following screenshot illustrates **RangeNavigator** with [`rangePadding`](../api/js/ejrangenavigator#members:rangepadding) set to normal

![](/js/RangeNavigator/Range-Padding_images/Range-Padding_img3.png) 

##### Round

Round [`rangePadding`](../api/js/ejrangenavigator#members:rangepadding) for a numerical range rounds the range of the control to the nearest possible value that is divisible by the interval.

The following screenshot illustrates a **RangeNavigator** with [`rangePadding`](../api/js/ejrangenavigator#members:rangepadding) set to **Round**.

![](/js/RangeNavigator/Range-Padding_images/Range-Padding_img4.png) 

#### DateTime

Using the default range calculation for **RangeNavigator**, the [`rangePadding`](../api/js/ejrangenavigator#members:rangepadding) property allows you to customize the range.

{% highlight javascript %}


$("#container").ejRangeNavigator({
   //...
        rangePadding: 'none ',
   //...	
  });


{% endhighlight %}

##### None

By default, the [`rangePadding`](../api/js/ejrangenavigator#members:rangepadding) for **DateTime** range is none. The range is calculated from the minimum value to the maximum value of data in the RangeNavigator

The following screenshot illustrates a **RangeNavigator** with [`rangePadding`](../api/js/ejrangenavigator#members:rangepadding) set to none.

![](/js/RangeNavigator/Range-Padding_images/Range-Padding_img5.png) 

##### Round

Round [`rangePadding`](../api/js/ejrangenavigator#members:rangepadding) for a **DateTime** range rounds the range of the control to the nearest possible value.

The following screenshot illustrates a **RangeNavigator** with [`rangePadding`](../api/js/ejrangenavigator#members:rangepadding) set to Round.

![](/js/RangeNavigator/Range-Padding_images/Range-Padding_img6.png) 

### Padding

The gap between the container and the **RangeNavigator** can be specified using [`padding`](../api/js/ejrangenavigator#members:padding) property.

{% highlight javascript %}

$("#container").ejRangeNavigator({
   //...
       padding: "15"; 
   //...	
  });

{% endhighlight %}


### AllowSnapping

An [`allowSnapping`](../api/js/ejrangenavigator#members:allowsnapping) property toggles the placement of slider exactly on the place it left or on the nearest interval.

{% highlight javascript %}

$("#container").ejRangeNavigator({
   //...
      allowSnapping: true;
   //...	
  });

{% endhighlight %}

### Responsive

Set [`isResponsive`](../api/js/ejrangenavigator#members:isresponsive) value to make the **RangeNavigator** responsive on resize.

{% highlight javascript %}

$("#container").ejRangeNavigator({
   //...
      isResponsive: true;
   //...	
  });

{% endhighlight %}

### Auto Resizing

Enable [`enableAutoResizing`](../api/js/ejrangenavigator#members:enableautoresizing) option to resize the **RangeNavigator**.

{% highlight javascript %}

$("#container").ejRangeNavigator({
   //...
      enableAutoResizing: true;
   //...	
  });

{% endhighlight %}

### Customize range Navigator border

**RangeNavigator** provides options to customize the [`color`](../api/js/ejrangenavigator#members:border-color), [`opacity`](../api/js/ejrangenavigator#members:border-opacity) and [`width`](../api/js/ejrangenavigator#members:border-width) of range navigator [`border`](../api/js/ejrangenavigator#members:border).

{% highlight javascript %}

$("#container").ejRangeNavigator({
   //...
     border: { 
            color: "green",
            opacity: 0.5,
            width: 2 
            } 
   //...	
  });

{% endhighlight %}

### Customize size of range navigator

The [`height`](../api/js/ejrangenavigator#members:sizesettings-height) and [`width`](../api/js/ejrangenavigator#members:sizesettings-width) of **RangeNavigator** can be customized using [`sizeSettings`](../api/js/ejrangenavigator#members:sizesettings) property.

{% highlight javascript %}

$("#container").ejRangeNavigator({
   //...
     sizeSettings: { 
            height: "130",
            width: "900"
            } 
   //...	
  });

{% endhighlight %}

### Customize axis range of navigator

**RangeNavigator** calculates the range automatically based on the values of series data points. However you can explicitly specify the range using the [`start`](../api/js/ejrangenavigator#members:rangesettings-start), [`end`](../api/js/ejrangenavigator#members:rangesettings-end) properties in [`rangeSettings`](../api/js/ejrangenavigator#members:rangesettings) that is not possible when data is provided.

The following code example renders a RangeNavigator with a range from 2010 January 1st to 2013 January 1st.

{% highlight javascript %}


$("#container").ejRangeNavigator({
   //...
         rangeSettings: {
                    start: "2010/1/1", end: "2012/13/1"
                },  
   //...	
  });


{% endhighlight %}


![](/js/RangeNavigator/Range-Padding_images/Range-Padding_img7.png) 
