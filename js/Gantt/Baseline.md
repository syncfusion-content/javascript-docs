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

Baseline is used to describe the original plan of the task and it can be the same as current duration of the task or different. Baseline can be enabled by setting [`renderBaseline`](/api/js/ejgantt#members:renderbaseline) as `true` and baseline color can be changed by [`baselineColor`](/api/js/ejgantt#members:baselinecolor) property. To render the baseline you have to map the baseline start date and baseline end date values from data source. This can be done by using [`baselineStartDateMapping`](/api/js/ejgantt#members:baselinestartdatemapping) and [`baselineEndDateMapping`](/api/js/ejgantt#members:baselineenddatemapping) properties. The following code example shows how to enable baseline in Gantt control.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        baselineStartDateMapping: "baselineStartDate", //Mapping BaselineStartDate to Gantt
        baselineEndDateMapping: "baselineEndDate", //Mapping BaselineEndDate to Gantt
        renderBaseline: true //Show/Hide the baseline in Gantt
        baselineColor:"#fba41c"
    });

{% endhighlight %}

[Click](http://js.syncfusion.com/demos/web/#!/bootstrap/gantt/schedulingconcepts/baseline) here to view the online demo sample for baselines in Gantt.

The following screenshot shows the baseline in Gantt control.

![](/js/Gantt/Baseline_images/Baseline_img1.png)

