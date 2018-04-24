---
layout: post
title: Resource Allocation View
description: resource allocation view
platform: js
control: Gantt
documentation: ug
api: /api/js/ejgantt
---

# Resource Allocation View
The resource allocation view is used to visualize the resource usage in a project. Resources are displayed in separate rows and all the tasks assigned to a specific resource will be displayed in the chart side. In this view, a user can able to easily identify the overallocation of resources in a project. Resource allocation view can be initialized by setting [`viewType`](/api/js/ejgantt#members:viewtype) property as "resourceView".

![](/js/Gantt/Resource-Allocation-View_images/ResourceView_1.png)

## Data Binding
User can bind two types of data structure to Gantt in resource allocation view.

* Hierarchical data source binding
* Flat data binding

### Hierarchical data source binding
The following code example explains how to bind the hierarchical data.

{% highlight javascript %}

<div id="resourceGantt" style="height:450px;width:100%;" />
<script type="text/javascript">

var resourceGanttData = [{ 
      resourceName: "Anne Dodsworth",
	  tasks:[
	  { taskID: 1, taskName: "Plan timeline", startDate: new Date( "02/06/2017"), endDate: new Date( "02/10/2017"), duration: 5, progress: "50"},
	  { taskID: 2, taskName: "Plan budget", startDate: new Date( "02/13/2017"), endDate: new Date( "02/17/2017"), duration: 5, progress: "50"},
	  { taskID: 3, taskName: "Allocate resources", startDate: new Date( "02/20/2017"), endDate: new Date( "02/24/2017"), duration: 5, progress: "0"},
	  ]	
	},
//…

$(function () {
    $("#resourceGantt").ejGantt({
        dataSource: resourceGanttData,
        viewType: ej.Gantt.ViewType.ResourceView,
        resourceCollectionMapping: "resources",
        taskCollectionMapping: "tasks",
        resourceNameMapping: "resourceName",
//…
    });
});    
</script>

{% endhighlight %}

N> In Hierarchical data source resource collections are identified by using [`resourceCollectionMapping`](/api/js/ejgantt#members:resourcecollectionmapping) and tasks are identified by using [`taskCollectionMapping`](/api/js/ejgantt#members:taskcollectionmapping) properties.

### Flat data binding
The following code example explains how to bind the flat data.

{% highlight javascript %}

<div id="resourceGantt" style="height:450px;width:100%;" />
<script type="text/javascript">        

var resources = [
    { resourceId: 1, resourceName: "Anne Dodsworth", groupId: 1 },
    { resourceId: 2, resourceName: "David William", groupId: 1 },
    { resourceId: 3, resourceName: "Nancy Davolio", groupId: 2 },
    //…
];

var resourceGanttData = [
    { taskID: 1, taskName: "Plan timeline", startDate: new Date("02/06/2017"), endDate: new Date("02/10/2017"), duration: 5, progress: "50", resourceId: [1] },
    { taskID: 2, taskName: "Plan budget", startDate: new Date("02/13/2017"), endDate: new Date("02/17/2017"), duration: 5, progress: "50", resourceId: [1] },
    { taskID: 3, taskName: "Allocate resources", startDate: new Date("02/20/2017"), endDate: new Date("02/24/2017"), duration: 5, progress: "0", resourceId: [1] },
//…
]

$(function () {
    $("#resourceGantt").ejGantt({
        dataSource: resourceGanttData,
        viewType: ej.Gantt.ViewType.ResourceView,
        resources: resources,
        resourceIdMapping: "resourceId",
        resourceNameMapping: "resourceName",
        resourceInfoMapping: "resourceId",
        taskIdMapping: "taskID",
        //…
    });
});    
</script>

{% endhighlight %}

![](/js/Gantt/Resource-Allocation-View_images/ResourceView_2.png)

## Grouping
The resources and the tasks assigned to those resources can be grouped into categories. The property [`groupCollection`](/api/js/ejgantt#members:groupcollection) is used to define the groups to be displayed in the project. The properties [`groupIdMapping`](/api/js/ejgantt#members:groupidmapping) and [`groupNameMapping`](/api/js/ejgantt#members:groupnamemapping) are used to map the group details.

The below code snippet explains grouping of the resources in resource allocation view.

{% highlight javascript %}

<div id="resourceGantt" style="height:450px;width:100%;" />
<script type="text/javascript">

var resourceGroups = [
    { groupId: 1, groupName: "Planning Team" },
    { groupId: 2, groupName: "Development Team" },
    { groupId: 3, groupName: "Testing Team" }
];

var resources = [
    { resourceId: 1, resourceName: "Anne Dodsworth", groupId: 1 },
    { resourceId: 2, resourceName: "David William", groupId: 1 },
    { resourceId: 3, resourceName: "Nancy Davolio", groupId: 2 },
    //…
];

$(function () {
    $("#resourceGantt").ejGantt({
        dataSource: resourceGanttData,
        viewType: ej.Gantt.ViewType.ResourceView,
        groupCollection: resourceGroups,
        resources: resources,
        groupNameMapping: "groupName",
        groupIdMapping: "groupId",
        resourceIdMapping: "resourceId",
        resourceNameMapping: "resourceName",
        resourceInfoMapping: "resourceId",
        taskIdMapping: "taskID",
        //…
    });
}); 
</script>
{% endhighlight %}

The below screen shot depicts a resource view in a project with 3 groups.

![](/js/Gantt/Resource-Allocation-View_images/ResourceView_3.png)

## CRUD data operations

### Adding a task
It is possible to add a task dynamically either by using toolbar insert icon or by context menu add option. The below screen shot shows the toolbar add and context menu add options.

![](/js/Gantt/Resource-Allocation-View_images/ResourceView_4.png)

![](/js/Gantt/Resource-Allocation-View_images/ResourceView_5.png)

When the insert option is clicked, the add dialog will be displayed prompting the user to provide the task details. After providing the task details, when user click the save button without providing the resource information or without assigning any resource to the task, the task will be added at the top by default.

![](/js/Gantt/Resource-Allocation-View_images/ResourceView_6.png)

![](/js/Gantt/Resource-Allocation-View_images/ResourceView_7.png)

If the newly added task should be assigned to a specific resource, user can able to select the resource information in the resource tab of add dialog.

![](/js/Gantt/Resource-Allocation-View_images/ResourceView_8.png)

The below screen shot depicts a new task being assigned to a resource `Anne Dodsworth`.

![](/js/Gantt/Resource-Allocation-View_images/ResourceView_9.png)

N> It is not possible to add a resource to the project dynamically.
N> A task can be assigned to one or more resource while adding.

### Editing

#### Editing a Task
A task can be edited either by using edit dialog or by mouse interactions. A user can edit a task using edit dialog by performing double click action on the taskbar, user can then edit the task information in the edit dialog.

![](/js/Gantt/Resource-Allocation-View_images/ResourceView_10.png)
![](/js/Gantt/Resource-Allocation-View_images/ResourceView_11.png)

A task’s schedule can be changed by left resizing, right resizing or dragging the task across the dates.

![](/js/Gantt/Resource-Allocation-View_images/ResourceView_12.png)

#### Update task values dynamically
In resource allocation view also, we can update the task details dynamically on any action like external button click by using [`updateRecordByTaskId`](/api/js/ejgantt#methods:updaterecordbytaskid "updateRecordByTaskId(data)") method. The below code example explains how to use this method in resource allocation view.

{% highlight javascript %}

<div id="resourceGantt" style="height:450px;width:100%;" />
<button id="update">Update Tasks</button>

<script type="text/javascript">

$(function () {
    $("#resourceGantt").ejGantt({
        dataSource: resourceGanttData,
        viewType: ej.Gantt.ViewType.ResourceView,
        //…
    });
});

$("#update").click(function () {
    var ganttObject = $("#resourceGantt").ejGantt("instance");
    var task = {};
    task.taskID = 3;
    task.resourceId = [1, 2, 3];
    task.startDate = new Date("02/25/2017")
    task.duration = 10;
    task.taskName = task.taskID + " - Name Changed";
    ganttObject.updateRecordByTaskId(task);
});
</script>

{% endhighlight %}

The below screenshot shows the result of above code example.

![](/js/Gantt/Resource-Allocation-View_images/ResourceView_19.png)
Before update
{:.caption}

![](/js/Gantt/Resource-Allocation-View_images/ResourceView_20.png)
After update
{:.caption}

### Deleting

#### Deleting Task
User should select a task to be removed from the project, and then the task can be deleted using context menu delete button.

![](/js/Gantt/Resource-Allocation-View_images/ResourceView_13.png)

#### Deleting Resource
User can able to delete a resource and the tasks assigned to it using toolbar and context menu delete options. After selecting the resource row, by clicking the delete toolbar icon the resource will be removed from the project and the tasks assigned to that resource will be listed in unassigned tasks list. The same will happen for context menu delete option.

![](/js/Gantt/Resource-Allocation-View_images/ResourceView_14.png)

The below screen shot depicts the tasks of the removed resource added as unassigned tasks to the project.

![](/js/Gantt/Resource-Allocation-View_images/ResourceView_15.png)

## Unassigned Tasks and Resources
There may be some instances, where one or more resources are not yet included in the project plan. Therefore, those resources are left with no tasks assigned to them. Those resources are termed as `unassigned resource`. The right side of the resource row will be left blank with no tasks.
The below code snippet shows a resource with no tasks assigned to it.

{% highlight javascript %}

var resourceGanttData = [
{
    groupName: "Planning Team",
    resources: [{ 
        resourceName: "Anne Dodsworth",
	    tasks:[
	        { taskID: 1, taskName: "Plan timeline", startDate: new Date( "02/06/2017"), endDate: new Date( "02/10/2017"), duration: 5, progress: "50"},
            //…
        ]},
    //…
    { resourceName: "Nancy Davolio", tasks: []},
   //…
}]

{% endhighlight %}

In the below screen shot, the resource `Nancy Davolio` is the unassigned resource.

![](/js/Gantt/Resource-Allocation-View_images/ResourceView_16.png)

There may be instances where some tasks are not yet assigned with resources. Those tasks that are not assigned to any resources are termed as unassigned tasks. The Unassigned tasks are displayed at bottom, with resource name as `Unassigned Task`. Also, the Unassigned tasks can be assigned to any resources in the project.
The below code snippet shows a task with no resource assigned to it.

{% highlight javascript %}

var resources = [
    { resourceId: 1, resourceName: "Anne Dodsworth", groupId: 1 },
    { resourceId: 2, resourceName: "David William", groupId: 1 },
    { resourceId: 3, resourceName: "Nancy Davolio", groupId: 2 },
    //…
];

var resourceGanttData = [
//…
    { taskID: 1, taskName: "Plan timeline", startDate: new Date("02/06/2017"), endDate: new Date("02/10/2017"), duration: 5, progress: "50" },
//…
]

{% endhighlight %}

In the below screen shot, there more instances of unassigned tasks.

![](/js/Gantt/Resource-Allocation-View_images/ResourceView_17.png)

## Resource Overallocation
By default, a resource can work 8 hours a work day but when a resource is forced to work more than 8 hours it is termed as overallocation. When a resource is assigned with two or more tasks which is occurring in a same date range, this state is termed as over allocation for a resource. The overlapped tasks are highlighted like in the below screen shot. The overlapped tasks will be displayed one below the other with an overlapped highlighted region.

![](/js/Gantt/Resource-Allocation-View_images/ResourceView_18.png)