---
layout: post
title: Change-Week-start-day
description: Week start day customization
platform: js
control: Gantt
documentation: ug
---

# Change week start day in month timescale mode

## Using start date mode as Month

When setting the [`timescaleStartDateMode`](/api/js/ejgantt#members:scheduleheadersettings-timescalestartdatemode "scheduleHeaderSettings.timescaleStartDateMode") property as `month`, the project will start from the first date of the same month of the first task in a project. Using below code example we can change the week start day of the project start date in month timescale mode.

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

## Using start date mode as Year

When setting the [`timescaleStartDateMode`](/api/js/ejgantt#members:scheduleheadersettings-timescalestartdatemode "scheduleHeaderSettings.timescaleStartDateMode") property as `year`, the project will start from the first date of the same year to which the first task in a project starts. Using below code example we can change the week start day of the project start date in year timescale mode.

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

By default _enableMonthStart property will be `true`. Week header in month schedule mode will be rendered with month/year start day. To customize the week start day in month mode we need to set _enableMonthStart as `false`.
