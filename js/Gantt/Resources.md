---
layout: post
title: Resources
description: resources
platform: js
control: Gantt
documentation: ug
api: /api/js/ejgantt
---

# Resources

The resources are represented by staff, equipment and materials etc. In Gantt control you can show or allocate the resources (human resources) for each task.

## Resource collection

The resource collection contains details about resources that are used in the project. Resources are `JSON` object that contains id and name of the resources and this collection is mapped to the Gantt control using the [`resources`](/api/js/ejgantt#members:resources) property.
Id and name field of the resources are mapped by using the [`resourceIdMapping`](/api/js/ejgantt#members:resourceidmapping) and [`resourceNameMapping`](/api/js/ejgantt#members:resourcenamemapping) properties.
The following code snippets shows resource collection object and how it assigned to Gantt control.

{% highlight javascript %}

 var projectResources = [{
        resourceId: 1,
        resourceName: "Project Manager"
    }, {
        resourceId: 2,
        resourceName: "Software Analyst"
    }, {
        resourceId: 3,
        resourceName: "Developer"
    }, {
        resourceId: 4,
        resourceName: "Testing Engineer"
    }];

    $("#GanttContainer").ejGantt({
        //...
        resources: projectResources, //resource collection dataSource
        resourceNameMapping: "resourceName", //resource Name mapping
        resourceIdMapping: "resourceId", //resource Id Mapping
    });

{% endhighlight %}

## Assign resource
We can assign resources for a task at initial load, using the resource id value of the resources as a collection. This collection is mapped  from the [`dataSource`](/api/js/ejgantt#members:datasource) to the Gantt control using the [`resourceInfoMapping`](/api/js/ejgantt#members:resourceinfomapping) property.
The following code snippet shows how to assign the resource for each task and map to Gantt control.
{% highlight javascript %}

var dataSource = [
    //..
    {
       "taskId": 3,
        "taskName": "Software Specification",
        //...
	    "resourceId": [2]
    }
    //..
    ];
    $("#GanttContainer").ejGantt({
        //...
        resourceInfoMapping: "resourceId", //Field name which contains resource details for the task in datasource
        dataSource: dataSource
    });

{% endhighlight %}

The following screenshot shows Gantt control with resources.

![](/js/Gantt/Resources_images/Resources_img1.png)

## Assign resources with unit
Resource units indicates the amount of work done by a resource for the task. We can specify the resource unit for the each assigned resource for a particular task.
Resource unit value is mapped to the Gantt tasks from the datasource using the [`resourceUnitMapping`](/api/js/ejgantt#members:resourceunitmapping) property.
The below code snippets shows how to assign resource unit value.

{% highlight javascript %}
 var dataSource = [
    //..
    {
       "taskId": 3,
        "taskName": "Software Specification",
        //...
	    "resourceId": [{ resourceId: 2, unit: 50 }]
    }
    //..
    ];

   $("#GanttContainer").ejGantt({
        //...
        resourceInfoMapping: "resourceId",
        resourceIdMapping: "resourceId",
        resourceNameMapping: "resourceName",
        resourceUnitMapping: "unit", //Field name which contains resource unit value in data source
        dataSource: dataSource
    });

{% endhighlight %}

The following screenshot shows Gantt control with resource units.

![](/js/Gantt/Resources_images/Resources_img2.png)

## Edit resource collection
By using cell edit option we can add/remove the resource for particular task and by using dialog edit support we can modify the resource unit value also.
Refer this [link](/js/gantt/editing) to know more about editing in Gantt control.
The following screenshot shows the resource edit option in Gantt.

![](/js/Gantt/Resources_images/Resources_img4.png)
Editing resource with cell edit
{:.caption}

![](/js/Gantt/Resources_images/Resources_img3.png)
Editing resource with edit dialog
{:.caption}

N> While editing, resource values are saved with resource unit value when resource unit is not equal to 100% like below.
{% highlight javascript %}
   {
       "taskId": 3,
        //...
	    "resourceId": [{ resourceId: 2, unit: 50 }]
    }
{% endhighlight %}
N> When resource unit is 100%, resource value is stored with ID only.
{% highlight javascript %}
    {
       "taskId": 3,
        //...
	    "resourceId": [2]
    }
{% endhighlight %}
N> The unit values are updated to the resources assigned to the Gantt tasks, only when mapping resource units data source field using the [`resourceUnitMapping`](/api/js/ejgantt#members:resourceunitmapping) property.
N> Resource unit will be updated while editing the duration and work fields with respective to [task type](/js/gantt/work-fied "Task types available in Gantt").