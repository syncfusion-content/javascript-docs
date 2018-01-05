---
layout: post
title: Stripline
description: stripline
platform: js
control: Gantt
documentation: ug
api: /api/js/ejgantt
---

# Stripline

The strip line in Gantt control is used to highlight the important event in Gantt chart part. By using this feature, you can add the strip lines to highlight important days in your project. Strip lines in Gantt can be initialized by using [`stripLines`](/api/js/ejgantt#members:striplines) property and we can define date and label of the strip line by using [`day`](/api/js/ejgantt#members:striplines-day) and [`label`](/api/js/ejgantt#members:striplines-label) properties. Strip lines are formatted by using [`lineStyle`](/api/js/ejgantt#members:striplines-linestyle), [`lineColor`](/api/js/ejgantt#members:striplines-linecolor) and [`lineWidth`](/api/js/ejgantt#members:striplines-linewidth) properties. The following code example shows you how to add the strip line in Gantt control.


{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        stripLines: [{
            day: "01/02/2014",
            label: "Project Release",
            lineStyle: "dotted",
            lineColor: "blue",
            lineWidth: 2
        }]
    });

{% endhighlight %}

The following screenshot shows stripline in Gantt control.

![](/js/Gantt/Stripline_images/Stripline_img1.png)
