---
layout: post
title: Resource Histogram View
description: resource histogram view
platform: js
control: Gantt
documentation: ug
api: /api/js/ejgantt
---

# Resource Histogram

A resource histogram displays the scheduled working time range of resources for its assigned tasks. Using this, you can easily identify the resource's availability and its working time. The resource histogram is used to allocate the resources properly throughout the project and find the details about allocated resources and the allocated time ranges of a specific resource.

## Databinding
You can render the histogram view for both project view Gantt and resource view Gantt by using the [`viewType`](/api/js/ejgantt#members:viewtype) as `ej.Gantt.ViewType.HistogramView`. 
The following code example explains how to bind the resource histogram view for project view Gantt.
{% highlight javascript %}
<div id="GanttContainer" style="height:310px;width:100%;"></div>
<div id="HistogramContainer" style="height:300px;width:100%;" />

<script type="text/javascript">
    $("#GanttContainer").ejGantt({
        dataSource: histogramResourcesData,
        viewType: ej.Gantt.ViewType.ProjectView,
        taskIdMapping: "TaskId",
        taskNameMapping: "TaskName",
        startDateMapping: "StartDate",
        durationMapping: "Duration",
        progressMapping: "Progress",
        childMapping: "Children",
        resourceUnitMapping: "Unit",
        resourceInfoMapping: "Resources",
        resourceNameMapping: "Name",
        resourceIdMapping: "Id",
        resources: resources,
        //..			
    });
    $("#HistogramContainer").ejGantt({
        dataSource: histogramResourcesData,
        viewType: ej.Gantt.ViewType.HistogramView,
        taskIdMapping: "TaskId",
        taskNameMapping: "TaskName",
        startDateMapping: "StartDate",
        durationMapping: "Duration",
        progressMapping: "Progress",
        childMapping: "Children",
        resourceUnitMapping: "Unit",
        resourceInfoMapping: "Resources",
        resourceNameMapping: "Name",
        resourceIdMapping: "Id",
        resources: resources,
        load: function(args) {
            this.isProjectViewData = true;
        },
    });
</script>
{% endhighlight %}
N> You should bind the data source and necessary mapping properties to render the histogram view. You can differentiate whether the bound data source is project view data or resource view data using the `ganttObject.isProjectViewData` boolean property and [`load`](/api/js/ejgantt#events:load) event. Set this property to `true` if the provided data is project view and set to `false` for resource view data.

## Synchronize resource histogram view Gantt with other views

You can synchronize the splitter position and horizontal scroller position in chart side and task values of the project view/resource view Gantt control with resource histogram view Gantt by using the [`actionComplete`](/api/js/ejgantt#events:actioncomplete) and [`splitterResized`](/api/js/ejgantt#events:splitterresized) events.

### Synchronize with project view

The following code snippet shows how to synchronize the resource histogram view Gantt with project view Gantt.

{% highlight javascript %}
<script type="text/javascript">
    $("#GanttContainer").ejGantt({
        dataSource: histogramResourcesData,
        viewType: ej.Gantt.ViewType.ProjectView,
        splitterResized: splitterResized,
        actionComplete: actionComplete,
        //..			
    });
    $("#HistogramContainer").ejGantt({
        dataSource: histogramResourcesData,
        viewType: ej.Gantt.ViewType.HistogramView,
        splitterResized: splitterResized,
        actionComplete: actionComplete,

    });

    function splitterResized(args) {
        if (args.isOnResize == false) return;
        if (this._id == "GanttContainer") {
            $("#HistogramContainer").ejGantt("setSplitterPosition", args.currentSplitterPosition);
        } else if (this._id == "HistogramContainer") {
            $("#GanttContainer").ejGantt("setSplitterPosition", args.currentSplitterPosition);
        }
    }

    function actionComplete(args) {
        if (args.requestType == "scroll" && args.scrollDirection == "horizontal") {
            var scrollLeft = args.scrollLeft;
            if (this._id == "GanttContainer" && !args.isScrollByMethod) {
                $("#HistogramContainer").ejGantt("setChartScrollLeft", scrollLeft);
            } else if (this._id == "HistogramContainer" && !args.isScrollByMethod) {
                $("#GanttContainer").ejGantt("setChartScrollLeft", scrollLeft);
            }
        } else if (args.requestType == "recordUpdate") {
            $("#HistogramContainer").ejGantt("updateHistogramTask", args.data, "update");
            if (args.updatedRecords && args.updatedRecords.length > 0) {
                for (var count = 0; count < args.updatedRecords.length; count++) {
                    $("#HistogramContainer").ejGantt("updateHistogramTask", args.updatedRecords[count], "update");
                }
            }
        } else if (args.requestType == "save" && args.modifiedRecord) {
            $("#HistogramContainer").ejGantt("updateHistogramTask", args.modifiedRecord, "update");
        } else if (args.requestType == "save" && args.addedRecord) {
            $("#HistogramContainer").ejGantt("updateHistogramTask", args.addedRecord, "add");
        } else if (args.requestType == "delete") {
            $("#HistogramContainer").ejGantt("updateHistogramTask", args.data, "delete");
        }
    }
</script>
{% endhighlight %}

The following screenshot shows the resource histogram with project view Gantt.
![](/js/Gantt/HistogramView_images/HistogramView_1.png)

Please find our online demo sample for further reference
[ResourceHistogram](https://js.syncfusion.com/demos/web/#!/bootstrap/gantt/resourcehistogram)

### Synchronize with resource view
The following code snippet shows how to synchronize the resource histogram view Gantt with resource view Gantt.

{% highlight javascript %}
<script type="text/javascript">
    $("#GanttContainer").ejGantt({
        dataSource: histogramResourcesData,
        viewType: ej.Gantt.ViewType.ResourceView,
        splitterResized: splitterResized,
        actionComplete: actionComplete,
        //..			
    });
    $("#HistogramContainer").ejGantt({
        dataSource: histogramResourcesData,
        viewType: ej.Gantt.ViewType.HistogramView,
        splitterResized: splitterResized,
        actionComplete: actionComplete,
        load: function(args) {
            this.isProjectViewData = false;
        },

    });

    function splitterResized(args) {
        if (args.isOnResize == false) return;
        if (this._id == "GanttContainer") {
            $("#HistogramContainer").ejGantt("setSplitterPosition", args.currentSplitterPosition);
        } else if (this._id == "HistogramContainer") {
            $("#GanttContainer").ejGantt("setSplitterPosition", args.currentSplitterPosition);
        }
    }

    function actionComplete(args) {
        if (args.requestType == "scroll" && args.scrollDirection == "horizontal") {
            var scrollLeft = args.scrollLeft;
            if (this._id == "GanttContainer" && !args.isScrollByMethod) {
                $("#HistogramContainer").ejGantt("setChartScrollLeft", scrollLeft);
            } else if (this._id == "HistogramContainer" && !args.isScrollByMethod) {
                $("#GanttContainer").ejGantt("setChartScrollLeft", scrollLeft);
            }
        }
        //task drag and drop action and edit action
        else if (args.requestType == "save" && args.modifiedRecord || args.requestType == "recordUpdate") {
            var data = args.requestType == "save" ? args.modifiedRecord : args.item ? args.item : args.data;
            $("#HistogramContainer").ejGantt("updateHistogramTask", data, "update");
            //row delete & group delete
            if (args.updatedRecords) {
                for (var i = 0; i < args.updatedRecords.length; i++) {
                    var data = args.updatedRecords[i];
                    $("#HistogramContainer").ejGantt("updateHistogramTask", data, "update");
                }
            }
        }
        //add row
        else if (args.requestType == "save" && args.addedRecord) {
            $("#HistogramContainer").ejGantt("updateHistogramTask", args.addedRecord, "add");
        }
        //task delete
        else if (args.requestType == "delete") {
            $("#HistogramContainer").ejGantt("updateHistogramTask", args.data, "delete");
        }
    }
</script>
{% endhighlight %}

The following screenshot shows the resource histogram for resource view Gantt.
![](/js/Gantt/HistogramView_images/HistogramView_2.png)
