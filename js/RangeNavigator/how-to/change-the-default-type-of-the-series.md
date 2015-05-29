---
layout: post
title: change-the-default-type-of-the-series
description: change the default type of the series
platform: js
control: RangeNavigator
documentation: ug
---

### Change the default type of the series

The **type** property in **series** is used to change the type of the series rendered within **RangeNavigator**. By default line series will be rendered to represent the data in **RangeNavigator**.



{% highlight js %}

**[JS]**
$("#rangecontainer").ejRangeNavigator({
               {   
                   // ...              
                   series: [{
                        type: 'column',
                        // ...              
                      },
                  // ...             
               });


{% endhighlight %}



![](change-the-default-type-of-the-series_images\change-the-default-type-of-the-series_img1.png)

_Figure 29: Range Navigator with column series_



When using multiple series in **RangeNavigator**, **type** property in **seriesSettings** is used to set a type common for all the series.



{% highlight js %}

**[JS]**
$("#rangecontainer").ejRangeNavigator({
               {   
                   // Using a common series type for all the series              
                   seriesSettings: {
                        type: 'stackingcolumn',
                        // ...              
                      },
                  // ...             
               });


{% endhighlight %}

![](change-the-default-type-of-the-series_images\change-the-default-type-of-the-series_img2.png)

_Figure_ _30: Range Navigator using ‘stacking column’ as series type common for all the series_

