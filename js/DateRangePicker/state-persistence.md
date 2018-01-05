---
layout: post
title: state persistence
description: state persistence
platform: js
control: DateRangePicker
documentation: ug 
api: /api/js/ejdaterangepicker
---

## State Persistence

The value of DateRangePicker can be sustained even after form post back and page refreshing by enabling the **enablePersistence** API like below code example.

{% highlight js %}

      $("#daterange").ejDateRangePicker({

            enablePersistence: true,

        });

{% endhighlight %}



The DateRangePicker Model value will be stored in local storage / cookies of browser before page refreshes and reinitialized with the restored model after refresh.

