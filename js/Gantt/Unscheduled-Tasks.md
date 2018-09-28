---
layout: post
title: Unscheduled-Tasks
description: Unscheduled Tasks
platform: js
control: Gantt
documentation: ug
api: /api/js/ejgantt
---

# Unscheduled Tasks

Unscheduled tasks are planned for a project but do not have definite schedule dates.  Now, the Gantt control supports rendering the unscheduled tasks. You can create or update the tasks with anyone of start date, end date and duration values or none. You can enable or disable the unscheduled tasks by using the [`allowUnscheduledTask`](/api/js/ejgantt#members:allowUnscheduledTask)property.

## Unscheduled Task Types

Unscheduled tasks have various task types with only either start date, end date or duration.

#### Start Date Only

![](Unscheduled-Tasks_images/Start_Date_Only.png)

#### End Date Only

![](Unscheduled-Tasks_images/End_Date_Only.png)

#### Duration Only

![](Unscheduled-Tasks_images/Duration_Only.png)

#### Milestone

The milestone task, one without a start and end date, but having a duration value of zero is represented as follows.

![](Unscheduled-Tasks_images/Milestone.png)

## Define unscheduled tasks in data source

You can define the various types of unscheduled tasks in the data source as follows.

{% highlight javascript %}

var unscheduledData = [

    // Start date only
    { taskID: 3, taskName: "Plan timeline", startDate: new Date("02/01/2017"), progress: "60", resourceId: [1] },
    //Duration only
    { taskID: 4, taskName: "Plan budget", duration: 5, progress: "90", resourceId: [5] },
    //End Date only
    { taskID: 5, taskName: "Allocate resources", endDate: new Date("02/7/2017"), progress: "75", resourceId: [6] },
       //…
    //Milestone 
    { taskID: 8, taskName: "Software Specification", duration: 0, progress: "60", resourceInfo: [2] },
       //…        
];

$("#GanttContainer").ejGantt({
    //...
    dataSource: unscheduledData,
    allowUnscheduledTask: true,
    //...
});

{% endhighlight %}

The following screenshot displays the output of the above code. 

![](Unscheduled-Tasks_images/Image1.png)

N> If the [`allowUnscheduledTask`](/api/js/ejgantt#members:allowUnscheduledTask) property is set to `false` for unplanned task, the Gantt control will automatically calculate the scheduled dates with a default value of duration 1 and the project scheduled start date is considered as the start date for the task.

## Show/hide null text in Gantt columns

You can show/hide the null text cell value for start date, end date and duration columns by using the `showNullText` column property. This can be customized in load event of Gantt. You can change the `Null` string by using the `nullText` property in the localization text file of the Gantt control. The following code snippets explain this behavior.

{% highlight javascript %}

$("#GanttContainer").ejGantt({
    //...
    dataSource: unscheduledData,
    allowUnscheduledTask: true,
    load: loadEvent  // Client-side event triggered at load time.
    //...
});
function loadEvent(args) {
   //…
   var columns = this.getColumns();
       columns[1].showNullText = true;
       columns[2].showNullText = true;
       column[3].showNullText = false;
}
ej.Gantt.Locale["en-Us"] = {
   nullText: "null"
}

{% endhighlight %}

The following screenshot displays the output of the above code. 

![](Unscheduled-Tasks_images/Image2.png)
