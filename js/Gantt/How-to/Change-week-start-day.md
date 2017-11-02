---
layout: post
title: Change-Week-start-day
description: Week start day customization
platform: js
control: Gantt
documentation: ug
---

#Change week start day in Time scale modes

## In month timescaleStartDateMode

By default week header in month schedule mode will be rendered with month start day in timescaleStartDateMode as month. Using below code example we can customize the week start day in month schedule mode

{% highlight javascript %}

$("#Gantt").ejGantt ({
       scheduleHeaderSettings: {
                    scheduleHeaderType: ej.Gantt.ScheduleHeaderType.Month,
					timescaleStartDateMode: ej.Gantt.TimescaleRoundMode.Month,
                    weekStartDay: 1,
                    monthHeaderFormat: "MMM yyyy",
                    weekHeaderFormat: "M/dd"
                },
       load: function () {         
                    this._enableMonthStart = false;
                }
});

{% endhighlight %}

![](/js/Gantt/How-to/Change-Weekstart-Day-images/image-1.png)

## In year timescaleStartDateMode

By default month header in month schedule mode will be rendered with year starting date in timescaleStartDateMode as year. Using below code example we can customize the week start day in month schedule mode

{% highlight javascript %}

$("#Gantt").ejGantt ({
        scheduleHeaderSettings: {
                    scheduleHeaderType: ej.Gantt.ScheduleHeaderType.Month,
                    timescaleStartDateMode: ej.Gantt.TimescaleRoundMode.Year,
                    weekStartDay: 5,                 
                    weekHeaderFormat: "M/dd"
                },
       load: function () {         
                    this._enableMonthStart = false;
                }
});
{% endhighlight %}
![](/js/Gantt/How-to/Change-Weekstart-Day-images/image-2.png)

By default _enableMonthStart property will be true. Week header in month schedule mode will be rendered with month/year start day. To customize the week start day in month mode we need to set _enableMonthStart as false.
