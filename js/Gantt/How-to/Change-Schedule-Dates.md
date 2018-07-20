---
layout: post
title: Change-Schedule-Dates
description: change to change schedule start and end date
platform: js
control: Gantt
documentation: ug
---

# Change schedule start and end date

In Gantt it is possible to change the schedule start date and end date programmatically in button click by using [`updateScheduleDates`](/api/js/ejgantt#methods:updatescheduledates) public method.
We can pass start date and end date as method arguments to calculate.

The follow code example explains how to changes dates in button click.

{% highlight javascript %}

<button onclick="updateScheduleDates()">Change Schedule dates</button>
<div id="gantt" style="height:450px;width:700px"></div>
<script type="text/javascript">
    $("#gantt").ejGantt({
        //...
    });

    function updateScheduleDates() {
            var ganttObj = $("#gantt").data("ejGantt");
            ganttObj.updateScheduleDates("01/30/2014","03/10/2014");
        }
</script>

{% endhighlight %}

![](/js/Gantt/How-to/Change-Schedule-Date_Images/image-1.png)