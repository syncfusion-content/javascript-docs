---
layout: post
title: State Persistence
description: DatePicker - State persistence properties 
platform: js
control: DatePicker
documentation: ug
api: /api/js/ejdatepicker
---
# State Persistence

You can sustain the entire widget model of DatePicker even after form post or browser refresh by using [enablePersistence](https://help.syncfusion.com/api/js/ejdatepicker#members:enablepersistence) property. So the entire model values such as 

* Selected date
* Highlighted date
* Start and depth level 

are stored in local storage / cookies of browser before page refreshes and reinitialized with the restored model after refresh.


{% highlight javascript %}

        $(function () {

            // creates DatePicker from input

            $("#datePicker").ejDatePicker({

                enablePersistence: true // persists the DatePicker model

            });

        });

{% endhighlight %}

