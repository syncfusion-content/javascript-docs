---
layout: post
title: Stripline
description: stripline
platform: js
control: Gantt
documentation: ug
---

# Stripline

Stripline in Gantt control is used to highlight the important event in Gantt chart part. By using this feature, you can add the striplines to highlight important days in your project. The following code example shows you how to add the stripline in Gantt control.

{% highlight js %}

    $("#GanttContainer").ejGantt({
        //...
        stripLines: [{
            day: "01/02/2014",
            label: "Project Release",
            lineStyle: "dotted",
            lineColor: "Darkblue",
            lineWidth: 2
        }]
    });

{% endhighlight %}

The following screenshot shows stripline in Gantt control.

{% include image.html url="/js/Gantt/Stripline_images/Stripline_img1.png"%}
