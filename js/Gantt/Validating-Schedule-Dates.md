---
layout: post
title: Validating-Schedule-Dates
description: validating schedule dates
platform: js
control: Gantt
documentation: ug
api: /api/js/ejgantt
---

# Validating Schedule Dates

Validating schedule dates is used to change the schedule start date and end date dynamically. By this support, `scheduleStartDate` and `scheduleEndDate` can be automatically updated from the data source. When you change the date of any task item to the date that is beyond `scheduleStartDate` or `ScheduleEndDate` through cell editing, taskbar editing, dialog editing or toolbar operation, then the `scheduleStartDate` and `ScheduleEndDate` can be dynamically updated based on that task item’s date.

`PrevTimeSpan` and `NextTimeSpan` toolbar items are used to create new time span based on the schedule mode.

{% highlight javascript %}

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

![](/js/Gantt/Validating-Schedule-Dates_images/Validating-Schedule-Dates_img1.png)

