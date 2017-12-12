---
layout: post
title: Holidays
description: holidays
platform: js
control: Gantt
documentation: ug
api: /api/js/ejgantt
---

# Holidays

The Holidays in Gantt control is used to highlight the non-working days in Gantt control and it can be initialized with Gantt control by using the following code example.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        holidays: [{
            day: "2/03/2014",
            label: " Public holiday",
            background: "yellow"
        }]
    });

{% endhighlight %}

The following screenshot shows the output of Holidays in Gantt control.

![](/js/Gantt/Holidays_images/Holidays_img1.png)

