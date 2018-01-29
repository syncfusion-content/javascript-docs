---
layout: post
title: Critical-feature
description: Critical-feature
platform: js
control: Gantt
documentation: ug
api: /api/js/ejgantt
---
# Critical Path

The critical path in a project is indicated by a single task or a series of tasks in a project, critical path describes the calculated start date or end date of a project. If a task in a critical path is delayed, then the entire project will be delayed.

The critical path can be enabled in Gantt by using built-in toolbar button or [`showCriticalPath`](/api/js/ejgantt#methods:showcriticalpath "showCriticalPath(isShown)") method.

## Using Toolbar Icon

You can enable/disable the critical path in Gantt by using toolbar button, and this button can be enabled in the Gantt toolbar by using the following code example.

{% highlight html %}
 
<div id="GanttContainer"></div> 
<script>                   
       $("#GanttContainer").ejGantt(
                        {
                       //...
        toolbarSettings: {
                   showToolbar: true,
                   toolbarItems: [
                          //..
                   ej.Gantt.ToolbarItems.CriticalPath,
                                 ],
                         },
             });                   
</script>

{% endhighlight %}

![](/js/Gantt/criticalfeature_images/criticalfeature_img1.jpeg)

[Click](http://js.syncfusion.com/demos/web/#!/bootstrap/gantt/schedulingconcepts/criticalpath) here to view the online demo sample for critical path in Gantt.


## Using Method

You can enable the critical path by using [`showCriticalPath`](/api/js/ejgantt#methods:showcriticalpath "showCriticalPath(isShown)") method with parameter as `true`. And critical path can be disabled using the same method with parameter as `false`.

{% highlight html %}
 
<script>                   
$("#buttonOn").click(function (args) {
                ganttObj = $("#GanttContainer").data("ejGantt");
                ganttObj.showCriticalPath(true);
            })
$("#buttonOff").click(function (args) {
                ganttObj = $("#GanttContainer").data("ejGantt");
                ganttObj.showCriticalPath(false);
            })              
</script>

{% endhighlight %}

![](/js/Gantt/criticalfeature_images/criticalfeature_img2.jpeg)


## Customizing critical path background

You can customize the critical task background by setting custom color codes to the critical task elements’ class names,

Taskbar–.e-ganttchart .e-criticaltaskbar 

Progressbar–.e-ganttchart .e-criticalprogressbar     

Connector line–.e-ganttchart .e-criticalconnectorline       

Connector line left arrow– .e-ganttchart .e-criticalconnectorlineleftarrow  

Connector line right arrow–  .e-ganttchart .e-criticalconnectorlinerightarrow 

{% highlight html %}
 
<style>
    .e-ganttchart .e-criticaltaskbar {
                background-color : #ffb366!important;
                border-color : gray!important
    }
    .e-ganttchart .e-criticalprogressbar {
                background-color : #ff99cc!important;
                border-color : #b35900!important
    }
    .e-ganttchart .e-criticalconnectorline {
                background-color : #b800e6!important;
    }
    .e-ganttchart .e-criticalconnectorlineleftarrow {
                border-right-color : #b800e6!important;
    }
    .e-ganttchart .e-criticalconnectorlinerightarrow{
                border-left-color : #b800e6!important;
    }
</style>


{% endhighlight %}

![](/js/Gantt/criticalfeature_images/criticalfeature_img3.jpeg)


