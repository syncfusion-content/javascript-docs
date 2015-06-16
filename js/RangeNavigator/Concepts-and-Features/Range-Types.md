---
layout: post
title: Range-Types
description: Range Types
platform: js
control: RangeNavigator
documentation: ug
---

### Range Types

**RangeNavigator** control is designed to visualize large number of data and navigate to particular data from the large collection at ease. The data for the **RangeNavigator** is either numeric values or **DateTime** values and the **valueType** property in **RangeNavigator** indicates the type of the data that should be passed for the control. By default the **valueType** of **RangeNavigator** is **DateTime**

* Numeric                   

* DateTime

## Numeric Type

**RangeNavigator** is also used with numeric data and the **valueType** for this data is “**numeric**”

{% highlight js %}


    $("#rangecontainer").ejRangeNavigator({
      //...
        valueType: "numeric",
      //...	
    });


{% endhighlight %}


The following screenshot displays the **RangeNavigator** with numeric data.



{% include image.html url="/js/RangeNavigator/Concepts-and-features_images/Concepts-and-features_img1.png" Caption="Figure 7: RangeNavigator with numeric data."%}

## DateTime

By default the **valueType** of the **RangeNavigator** is “**datetime**” and represents the **DateTime** values.

{% highlight js %}


$("#rangecontainer").ejRangeNavigator({
      //...
        valueType: "datetime",
      //...	
       });


{% endhighlight %}



{% include image.html url="/js/RangeNavigator/Concepts-and-features_images/Concepts-and-features_img2.png" Caption="Figure 8: RangeNavigator with DateTime values"%}

## DateTime Intervals

The **DateTime** range type contains an **intervalType** property that sets the **DateTime** interval to one of the following:

* Years

* Quarters

* Months

* Weeks

* Days 

* Hours

* By default **intervalType** for higher level labels are **years** and for lower level labels its **quarters.**


{% highlight js %}


$("#rangecontainer").ejRangeNavigator({
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





{% include image.html url="/js/RangeNavigator/Concepts-and-features_images/Concepts-and-features_img3.png" Caption="Figure 9: Date Time property"%}
