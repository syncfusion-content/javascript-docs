---
layout: post
title: Change series type in JavaScript RangeNavigator Control | Syncfusion
description: Learn here about change series type support in Syncfusion Essential JavaScript RangeNavigator Control, its elements, and more.
platform: js
control: RangeNavigator
documentation: ug
---

# Change the default type of the series in JavaScript RangeNavigator

The **type** property in **series** is used to change the type of the series rendered within **RangeNavigator**. By default line series will be rendered to represent the data in **RangeNavigator**.



{% highlight javascript %}


$("#container").ejRangeNavigator({
               {   
                   // ...              
                   series: [{
                        type: 'column',
                        // ...              
                      },
                  // ...             
               });


{% endhighlight %}



![JavaScript RangeNavigator Change series type](/js/RangeNavigator/How-to/Change-series-type_images/Change-series-type_img1.png) 


When using multiple series in **RangeNavigator**, **type** property in **seriesSettings** is used to set a type common for all the series.



{% highlight javascript %}


$("#container").ejRangeNavigator({
               {   
                   // Using a common series type for all the series              
                   seriesSettings: {
                        type: 'stackingcolumn',
                        // ...              
                      },
                  // ...             
               });


{% endhighlight %}

![JavaScript RangeNavigator Multiple series type](/js/RangeNavigator/How-to/Change-series-type_images/Change-series-type_img2.png) 


