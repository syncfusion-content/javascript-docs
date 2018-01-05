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

The Holidays in Gantt control is used to highlight the non-working days in Gantt control and it can be initialized by using [`holidays`](/api/js/ejgantt#members:holidays) property. Each holiday can be defined with [`day`](/api/js/ejgantt#members:holidays-day), [`label`](/api/js/ejgantt#members:holidays-label), [`background`](/api/js/ejgantt#members:holidays-background) properties. The following code example shows how to initialize the Holidays in Gantt control.

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

