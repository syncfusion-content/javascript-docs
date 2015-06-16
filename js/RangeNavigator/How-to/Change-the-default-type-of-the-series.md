---
layout: post
title: Change-the-default-type-of-the-series
description: change the default type of the series
platform: js
control: RangeNavigator
documentation: ug
---

### Change the default type of the series

The **type** property in **series** is used to change the type of the series rendered within **RangeNavigator**. By default line series will be rendered to represent the data in **RangeNavigator**.



{% highlight js %}


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



{% include image.html url="/js/RangeNavigator/How-to/Change-the-default-type-of-the-series_images/Change-the-default-type-of-the-series_img1.png" Caption="Range Navigator with column series"%}


When using multiple series in **RangeNavigator**, **type** property in **seriesSettings** is used to set a type common for all the series.



{% highlight js %}


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

{% include image.html url="/js/RangeNavigator/How-to/Change-the-default-type-of-the-series_images/Change-the-default-type-of-the-series_img2.png" Caption="Range Navigator using ‘stacking column’ as series type common for all the series"%}


