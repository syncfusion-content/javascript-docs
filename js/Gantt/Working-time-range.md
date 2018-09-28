---
layout: post
title: Working-time-range
description: working time range
platform: js
control: Gantt
documentation: ug
api: /api/js/ejgantt
---

# Working Time Range

In Gantt control, working hours in a day for a project can be defined by using the [`dayWorkingTime`](/api/js/ejgantt#members:dayworkingtime) property. Based on the working hours, automatic date scheduling and duration validations for a task are performed.

The below code snippet explains on how to define the working time range for the project in Gantt,

{% highlight javascript %}

$("#GanttContainer").ejGantt({
    //...
    dayWorkingTime: [
        {"from": "08:00 AM", "to": "12:00 PM"},
        {"from": "01:00 PM", "to": "05:00 PM"}],
});

{% endhighlight %}

N> 1. Individual tasks can lie between any time within the defined working time range of the project.

N> 2. [`dayWorkingTime`](/api/js/ejgantt#members:dayworkingtime) property is used to define the working time for the whole project.

The below demo explains the working time range in Gantt.

[Working Time Range](http://js.syncfusion.com/demos/web/#!/bootstrap/gantt/schedulingconcepts/workingtimerange)

The following screen shot shows working time range in Gantt control. 

![](/js/Gantt/Working-time-range_images/Working-time-range_img1.png)

## Highlight working time range

Highlight the working time range with a background color by using the [`dayWorkingTime.background`](/api/js/ejgantt#members:dayworkingtime) property. You can highlight the non-working time ranges in a day. To do this, set the [`highlightNonWorkingTime`](/api/js/ejgantt#members:highlightnonworkingtime) property to `true`. To customize the non-working time background, use the [`nonWorkingBackground`](/api/js/ejgantt#members:nonworkingbackground) property.

The following code snippet explains how to define the working time range with background in Gantt.

{% highlight javascript %}

$("#GanttContainer").ejGantt({
    //...
	nonWorkingBackground:"#B7C3D0",
	highlightNonWorkingTime:true,
    dayWorkingTime: [
        {"from": "08:00 AM", "to": "12:00 PM" , background:"#EBF5FB"},
        {"from": "01:00 PM", "to": "05:00 PM" , background:"#EBF5FB"}]
});

{% endhighlight %}

N> The background colors of working time range are highlighted only when the [`scheduleHeaderSettings.scheduleHeaderType`](/api/js/ejgantt#members:scheduleheadersettings-scheduleheadertype) value as `day`.

The following screenshot shows the working time range with background colors.

![](/js/Gantt/Working-time-range_images/Working-time-range_img2.png)
