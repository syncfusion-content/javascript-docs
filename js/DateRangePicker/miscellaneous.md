---
layout: post
title: miscellaneous 
description: miscellaneous 
platform: js
control: DateRangePicker
documentation: ug
---

## Miscellaneous 

### Enable / Disable

The control can be enabled / disabled using public methods, **enable** or **disable**. 

{% highlight html %}

      $("#daterange").ejDateRangePicker();
       
      $("#daterange").ejDateRangePicker("disable");

{% endhighlight %}


{% highlight html %}

      $("#daterange").ejDateRangePicker("enable");

{% endhighlight %}


### Allow Editing

Editing in input box can be disabled by setting the false value to **allowEdit** API. By default this will be false and we can edit the value in input box

{% highlight html %}

        $("#daterange").ejDateRangePicker({

            allowEdit: false

        });
        
{% endhighlight %}


### Clear ranges

To clear the all selection and ranges in a popup we can make use of **clearRanges** method.

{% highlight html %}

        $("#daterange").ejDateRangePicker("clearRanges");

{% endhighlight %}

