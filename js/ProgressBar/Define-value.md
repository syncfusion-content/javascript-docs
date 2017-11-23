---
layout: post
title: Define-value
description: define value
platform: js
control: ProgressBar
documentation: ug
api: /api/js/ejprogressbar
---

# Define value

## Value

The value for the ProgressBar is set by using [value](https://help.syncfusion.com/api/js/ejprogressbar#members:value) property. The value should be between the minimum (min) and the maximum (max) values (number) of the ProgressBar. By default, the [minValue](https://help.syncfusion.com/api/js/ejprogressbar#members:minvalue) is **0** and the [maxValue](https://help.syncfusion.com/api/js/ejprogressbar#members:maxvalue) is **100** in ProgressBar, and the ‘**value**’ is set to **0**(number).

The following steps explain you on how to set the **value** for the ProgressBar widget.

 In the **HTML** page, add a **&lt;div&gt;** element to render the ProgressBar widget.

{% highlight html %}




<div class="control">
   <div id="progressbar"></div>
</div>



{% endhighlight %}

{% highlight javascript %}


    // Add the following code example to set the value for the ProgressBar widget.
    $(function () {
        //Declaration.
        $("#progressbar").ejProgressBar({
            minValue: 40,
            maxValue: 80,
            value: 60,
            height: 20,
            width: 500
        });
        var progress = $("#progressbar").data("ejProgressBar");
        progress.setModel({ text: progress.getValue()});
    });


{% endhighlight %}


The following screenshot displays the output for the above code.

![](/js/ProgressBar/Define-value_images/Define-value_img1.png) 



##  Percentage

The ProgressBar value is set in ProgressBar by using the [percentage](https://help.syncfusion.com/api/js/ejprogressbar#members:percentage) property. The value should be between the min and max values (number) of the ProgressBar. By default, the **minValue** is **0** and the **maxValue** is **100** in ProgressBar, and **percentage** is set to **0** (number).

The following steps explain you on how to set the value in **percentage** for the ProgressBar widget. 

In the **HTML** page, add a **&lt;div&gt;** element to render the ProgressBar widget.



{% highlight html %}


   <div class="control">
        <div id="progressbar"></div>
   </div>

{% endhighlight %}

{% highlight javascript %}


    // Add the following code example to set the value in percentage for the ProgressBar widget.
    $(function () {
        //Declaration.
        $("#progressbar").ejProgressBar({
           percentage: 60,
           width: 500,
           height: 20
        });
        var progress = $("#progressbar").data("ejProgressBar");
        progress.setModel({ text: progress.getValue() + " %" });
    });

{% endhighlight %}

The following screenshot displays the output.

![](/js/ProgressBar/Define-value_images/Define-value_img2.png) 
