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

Resources are represented by staff, equipment and materials etc. In Gantt control you can show /allocate the resources (human resources) for each task. The following steps explain how to configure Gantt with Resources

**Step 1**: Create a collection of `JSON` object, that contains id and name of the resource and assign it to `resources` property.

**Step 2**:  Then, specify the field name for id and name of the resource in the resource collection to `resourceIdMapping` and `resourceNameMapping` properties. 

**Step 3**: The name of the field, which contains the actual resources assigned for a particular task in the dataSource is specified using `resourceInfoMapping`.

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
        resourceInfoMapping: "resourceId", //Field name which contains resource details for the task
        resourceNameMapping: "resourceName", //resource Name mapping
        resourceIdMapping: "resourceId", //resource Id Mapping
        resources: projectResources, //resource collection dataSource
        showResourceNames: true,
    });


{% endhighlight %}

The following screenshot shows Gantt control with Resources.

![](/js/Gantt/Resources_images/Resources_img1.png)

You can find the online demo sample for allocating resources in Gantt [here](http://js.syncfusion.com/demos/web/#!/bootstrap/gantt/schedulingconcepts/resourceallocation)