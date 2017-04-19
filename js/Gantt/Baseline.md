---
layout: post
title: Baseline
description: baseline
platform: js
control: Gantt
documentation: ug
api: /api/js/ejgantt
---

# Baseline

Baseline is used to describe the original plan of the task and it can be the same as current duration of the task or different. The following code example shows you how to enable baseline in Gantt control.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        baselineStartDateMapping: "baselineStartDate", //MAPPING BASELINESTARTDATE TO GANTT
        baselineEndDateMapping: "baselineEndDate", //MAPPING BASELINEENDDATE TO GANTT
        renderBaseline: true //SHOW/HIDE THE BASELINE IN GANTT
    });

{% endhighlight %}

[Click](http://js.syncfusion.com/demos/web/#!/bootstrap/gantt/schedulingconcepts/baseline) here to view the online demo sample for baselines in Gantt.

The following screenshot shows the baseline in Gantt control.

![](/js/Gantt/Baseline_images/Baseline_img1.png)

