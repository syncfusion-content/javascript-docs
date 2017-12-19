---
layout: post
title: Range-Types
description: Range Types
platform: js
control: RangeNavigator
documentation: ug
api: /api/js/ejrangenavigator
---

### Range Types

**RangeNavigator** control is designed to visualize large number of data and navigate to particular data from the large collection at ease. The data for the **RangeNavigator** is either numeric values or **DateTime** values and the [`valueType`](../api/ejrangenavigator#members:valuetype) property in **RangeNavigator** indicates the type of the data that should be passed for the control. By default the [`valueType`](../api/ejrangenavigator#members:valuetype) of **RangeNavigator** is **DateTime**

* Numeric                 
* DateTime

## Numeric Type

**RangeNavigator** is also used with numeric data and the [`valueType`](../api/ejrangenavigator#members:valuetype) for this data is “**numeric**”

{% highlight javascript %}


    $("#container").ejRangeNavigator({
      //...
        valueType: "numeric",
      //...	
    });


{% endhighlight %}


The following screenshot displays the **RangeNavigator** with numeric data.



![](/js/RangeNavigator/Range-Types_images/Range-Types_img1.png) 

## DateTime

By default the [`valueType`](../api/ejrangenavigator#members:valuetype) of the **RangeNavigator** is “**datetime**” and represents the **DateTime** values.

{% highlight javascript %}


$("#container").ejRangeNavigator({
      //...
        valueType: "datetime",
      //...	
       });


{% endhighlight %}



![](/js/RangeNavigator/Range-Types_images/Range-Types_img2.png) 

## DateTime Intervals

The **DateTime** range type contains an [`intervalType`](../api/ejrangenavigator#members:labelsettings-higherlevel-intervaltype) property that sets the **DateTime** interval to one of the following:

* Years
* Quarters
* Months
* Weeks
* Days 
* Hours

By default [`intervalType`](../api/ejrangenavigator#members:labelsettings-higherlevel-intervaltype) for higherLevel labels are **years** and [`intervalType`](../api/ejrangenavigator#members:labelsettings-lowerlevel-intervaltype) for lowerLevel labels its **quarters.**


{% highlight javascript %}


$("#container").ejRangeNavigator({
   //...
     labelSettings:
      { 
          higherLevel:
            {
                intervalType: 'years',
            },
        lowerLevel:
           {
               intervalType: ' quarters',
           }
      },    
  //...	
  });


{% endhighlight %}





![](/js/RangeNavigator/Range-Types_images/Range-Types_img3.png) 
