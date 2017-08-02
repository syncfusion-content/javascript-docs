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

Resources are represented by staff, equipment and materials etc. In Gantt control you can show /allocate the resources (human resources) for each task.

## Resource Collection

Resource collection contains details about the resources that are used in the project. Resources are `JSON` object that contains id and name of the resources and assign it to `resources` property.
Id and name field of the resources are identified by the `resourceIdMapping` and `resourceNameMapping` properties.
The following code snippets shows resource collection object and how it assinged to Gantt control.

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

## Assign Resource
We can specify the resources for a particular task as collection of resource id values in `dataSource` and this values are identified by using `resourceInfoMapping` property.
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

## Assign Resources with Unit
Resource units are used to indicate the percentage of working time assinged to task. We can specify the resource unit for each resource assinged for a particular task.
Resource unit value is assigned in `dataSource` and it is mapped by using `resourceUnitMapping` property.
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
        resourceUnitMapping: "unit", //Field name wihich contains resource unit value in data source
        dataSource: dataSource
    });

{% endhighlight %}

The following screenshot shows Gantt control with resource units.

![](/js/Gantt/Resources_images/Resources_img2.png)

## Edit Resource Collection
By using cell edit option we can add/remove the resource for particular task and by using dialog edit support we can modify the resource unit value also.
Refer this [link](editing) to know more about editing in Gantt control.
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
N> Resource unit values are updated in datasource only when we provide the value for `resourceUnitMapping` property.
N> Resource unit will be changed on editing duration and work field with respective of [Task Type](/js/gantt/work-fied "Task types available in Gantt") value.