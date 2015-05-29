---
layout: post
title: validating-schedule-dates
description: validating schedule dates
platform: js
control: Gantt
documentation: ug
---

# Validating Schedule Dates

**Validating schedule dates** is used to change the schedule start date and end date dynamically. By this support, **scheduleStartDate** and **scheduleEndDate** can be****automatically updated from the data source. When you change the date of any task item to the date that is beyond **scheduleStartDate** or **ScheduleEndDate** through cell editing, taskbar editing, dialog editing or toolbar operation, then the **scheduleStartDate** and **ScheduleEndDate** can be dynamically updated based on that task item’s date.

**PrevTimeSpan** and **NextTimeSpan** toolbar items are used to create new time span based on the schedule mode.

{% highlight js %}


$(function () {
            $("#gantt").ejGantt({
                // ...
                //scheduleStartDate: "02/01/2014",
                //scheduleEndDate: "03/14/2016",
                toolbarSettings: {
                    showToolbar: true,
                    toolbarItems: [
                    ej.Gantt.ToolbarItems.PrevTimeSpan,
                    ej.Gantt.ToolbarItems.NextTimeSpan, ]
                 // ...
                },
            });
        });



{% endhighlight %}






The following screenshot illustrates the output of the above code.

{% include image.html url="\js\Gantt\concepts-and-features\validating-schedule-dates_images\validating-schedule-dates_img1.png" Caption="Figure 57: Validating schedule dates"%}

