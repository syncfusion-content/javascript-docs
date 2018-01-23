---
layout: post
title: Change-Weekend
description: change weekend/Non-working day
platform: js
control: Gantt
documentation: ug
---

# Change Week end/Non-working day
Non-working days/weekend are used to represent the non-productive days in a project. It is possible to change the non-working days in a week using the [`workWeek`](/api/js/ejgantt#members:workweek) property in Gantt.

By default, Saturdays and Sundays are considered as non-working days/weekend in a project. 

The following code example explains how to change weekend/non-working days

{% highlight javascript %}

$("#gantt").ejGantt({
     // ...     
     workWeek: ["Sunday","Monday","Tuesday","Wednesday","Thursday"],
     // ...
});

{% endhighlight %}

The above code example makes Fridays and Saturdays as non-working days in a week.

![](/js/Gantt/How-to/Change-Workweek_images/Change_Workweek_img1.png)

The above screen shot will be displayed after changing the non-working days in Gantt.
{:.caption}

N> In Gantt, we can make weekend as working day by setting [`includeWeekend`](/api/js/ejgantt#members:includeweekend) property as `true`.