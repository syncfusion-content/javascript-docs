---
layout: post
title: Range-Padding
description: Range Padding
platform: js
control: RangeNavigator
documentation: ug
---

### Range Padding

**Range Padding** adds padding for range in **RangeNavigator**. It allows you to space the grid lines in the **RangeNavigator**.  By default, this property is set to **none**.

#### Numeric

The **rangePadding** property allows you to customize the automatic range calculation using the default auto range calculation for **RangeNavigator**.

{% highlight js %}


$("#rangecontainer").ejRangeNavigator({
   //...
        valueType: "numeric",
        rangePadding: 'none ',
   //...	
  });


{% endhighlight %}

##### None

By default, the **rangePadding** for numerical range is none. The range is calculated from the minimum value to the maximum value of data in the RangeNavigator.

The following screenshot illustrates a **RangeNavigator** with **rangePadding** set to none.



{% include image.html url="/js/RangeNavigator/Concepts-and-features_images/Concepts-and-features_img4.png" Caption="Figure 29: RangeNavigator with rangePadding set to none"%}

##### Additional

When you set the **rangePadding** for numerical range to **Additional**, range is padded with an interval.

The following screenshot illustrates a **RangeNavigator** with **rangePadding** set to additional.



{% include image.html url="/js/RangeNavigator/Concepts-and-features_images/Concepts-and-features_img5.png" Caption="Figure 10: RangeNavigator with rangePadding set to additional"%}

##### Normal

In normal **rangePadding**, automatic range calculation differs based on the data. 

The following screenshot illustrates **RangeNavigator** with **rangePadding** set to normal

{% include image.html url="/js/RangeNavigator/Concepts-and-features_images/Concepts-and-features_img6.png" Caption="Figure 11: RangeNavigator with rangePadding set to normal"%}

##### Round

Round **rangePadding** for a numerical range rounds the range of the control to the nearest possible value that is divisible by the interval.

The following screenshot illustrates a **RangeNavigator** with **rangePadding** set to **Round**.

{% include image.html url="/js/RangeNavigator/Concepts-and-features_images/Concepts-and-features_img7.png" Caption="Figure 12: RangeNavigator with rangePadding set to Round"%}

#### DateTime

Using the default range calculation for **RangeNavigator**, the **rangePadding** property allows you to customize the range.

{% highlight js %}


$("#rangecontainer").ejRangeNavigator({
   //...
        rangePadding: 'none ',
   //...	
  });


{% endhighlight %}

##### None

By default, the **rangePadding** for **DateTime** range is none. The range is calculated from the minimum value to the maximum value of data in the RangeNavigator

The following screenshot illustrates a **RangeNavigator** with **rangePadding** set to none.

{% include image.html url="/js/RangeNavigator/Concepts-and-features_images/Concepts-and-features_img8.png" Caption="Figure 13: RangeNavigator with rangePadding set to none"%}

##### Round

Round **rangePadding** for a **DateTime** range rounds the range of the control to the nearest possible value.

The following screenshot illustrates a **RangeNavigator** with **rangePadding** set to Round.

{% include image.html url="/js/RangeNavigator/Concepts-and-features_images/Concepts-and-features_img9.png" Caption="Figure 14: RangeNavigator with rangePadding set to Round"%}

### Customize axis range of navigator

**RangeNavigator** calculates the range automatically based on the values of series data points. However you can explicitly specify the range using the **start**, **end** properties in **rangeSettings** that is not possible when data is provided.

The following code example renders a RangeNavigator with a range from 2010 January 1st to 2013 January 1st.

{% highlight js %}


$("#rangecontainer").ejRangeNavigator({
   //...
         rangeSettings: {
                    start: "2010/1/1", end: "2012/13/1"
                },  
   //...	
  });


{% endhighlight %}


{% include image.html url="/js/RangeNavigator/Concepts-and-features_images/Concepts-and-features_img10.png" Caption="Figure 15: RangeNavigator"%}
