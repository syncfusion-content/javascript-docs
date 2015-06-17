---
layout: post
title: Holidays
description: holidays
platform: js
control: Gantt
documentation: ug
---

# Holidays

**Holidays** in **Gantt** control is used to highlight the non-working days in **Gantt** control and it can be initialized with **Gantt** control by using the following code example.

{% highlight js %}


    $("#GanttContainer").ejGantt({
        //...
        holidays: [ {
            day: "2/11/2014",
            label: " Public holiday",
            background: "yellowgreen "
        }]
    });


{% endhighlight %}



The following screenshot shows the output of **Holidays** in **Gantt** control.

{% include image.html url="/js/Gantt/Concepts-and-Features/Holidays_images/Holidays_img1.png" Caption="Holidays"%}

