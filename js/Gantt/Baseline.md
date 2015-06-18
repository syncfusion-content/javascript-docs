---
layout: post
title: Baseline
description: baseline
platform: js
control: Gantt
documentation: ug
---

# Baseline

**Baseline** is used to describe the original plan of the task and it can be the same as current duration of the task or different. The following code example shows you how to enable baseline in **Gantt** control.

{% highlight js %}


    $("#GanttContainer").ejGantt({
        //...
        baselineStartDateMapping: "baselineStartDate",//MAPPING BASELINESTARTDATE TO GANTT
        baselineEndDateMapping: "baselineEndDate",//MAPPING BASELINEENDDATE TO GANTT
        renderBaseline: true//SHOW/HIDE THE BASELINE IN GANTT
    });


{% endhighlight %}



The following screenshot shows the baseline in **Gantt** control.

{% include image.html url="/js/Gantt/Baseline_images/Baseline_img1.png" Caption="Baseline"%}

