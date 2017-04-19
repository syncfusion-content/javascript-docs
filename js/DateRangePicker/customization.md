---
layout: post
title: customization
description: customization
platform: js
control: DateRangePicker
documentation: ug
api: /api/js/ejdaterangepicker
---

## Customization

With available flexible options customization of DateRangePicker will be easier.

### Setting Dimension

**Height** and **width** of the DateRangePicker can be changed using corresponding API (**height,width**) like below code examples.

{% highlight html %}

        $("#daterange").ejDateRangePicker({

            height: 50,

            width: 300

        });
        
{% endhighlight %}

        
### Rounded Corners

You can make use of **showRoundedCorner** property in order to add rounded borders to the input and popup elements. By default, in DateRangePicker this will be disabled state we can enable this by setting true to this API.

// creates DateRangePicker and setting rounded corner dynamically


{% highlight html %}


        $("#daterange").ejDateRangePicker();

        dateObj = $("#daterange").ejDateRangePicker("instance");

        dateObj.option("showRoundedCorner", true);

{% endhighlight %}



