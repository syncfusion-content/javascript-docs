---
layout: post
title: Work Breakdown Structure
description: Work Breakdown Structure
platform: js
control: Gantt
documentation: ug
api: /api/js/ejgantt
---

# Work Breakdown Structure

Work Breakdown Structure(WBS) in Gantt represents the entire project activities in various sub modules. It is used to split the large tasks into manageable small tasks. WBS value and WBS predecessor value of Gantt tasks are displayed in WBS column and WBS predecessor column. This can be enabled in Gantt by using [`enableWBS`](/api/js/ejgantt#members:enablewbs) and [`enableWBSPredecessor`](/api/js/ejgantt#members:enablewbspredecessor) properties. The following code example shows how to enable WBS columns in Gantt.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        enableWBS: true,
        enableWBSPredecessor: true,
    });

{% endhighlight %}

The below screenshot depicts the output of above code example.

![](/js/Gantt/WorkBreakdownStructure_images/wbs_img1.png)

[Click](http://js.syncfusion.com/demos/web/#!/bootstrap/gantt/schedulingconcepts/workbreakdownstrcture) here to view the online demo sample for WBS in Gantt.





