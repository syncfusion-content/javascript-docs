---
layout: post
title: Get taskbar information on click action
description: Get taskbar information on click action
platform: js
control: Gantt
documentation: ug
---

# Get taskbar information on click action

When we click on the taskbar, [`taskbarClick`](/api/js/ejgantt#events:taskbarclick) event will be triggered, using this event and it's arguments, we can do any action related to taskbar. The following code example shows how to use this event.

{% highlight javascript %}
    
    $("#Gantt").ejGantt({
        //...
        taskbarClick: function(args) {
            var taskbarElement = args.taskbarElement,
                taskData = args.data,
                target = args.target;
            //...
            //your code goes here
        },
    });

{% endhighlight %}

You can find the JS playground sample for this [here](http://jsplayground.syncfusion.com/Sync_250vjsjl "Demo Link").
