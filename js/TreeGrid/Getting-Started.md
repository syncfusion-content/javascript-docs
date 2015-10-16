---
layout: post
title: Getting-Started
description: getting started
platform: js
control: TreeGrid
documentation: ug
---

# Getting Started

## Create your first TreeGrid in JavaScript

The **Essential Javascript TreeGrid** has been designed to represent and edit the hierarchical data. 

This section explains how to create a TreeGrid widget in your application with hierarchical data source and enable sorting and editing. The following screenshot displays the output.

![](/js/TreeGrid/Getting-Started_images/Getting-Started_img1.png)

1.Create an HTML file and add the following template to the HTML file.

{% highlight html %}

    <!DOCTYPE html>
    <html xmlns="http://www.w3.org/1999/xhtml">
        <head>
            <meta name="viewport"content="width=device-width, initial-scale=1.0"/>
            <meta charset="utf-8" />
            <link href=" http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet"/>
            <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
            <script src="http://cdn.syncfusion.com/js/assets/external/jsrender.min.js"></script>
            <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"></script>
            <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>
            <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js" type="text/javascript"></script>
        </head>
        <body>
        <!--Add TreeGrid control here -->
        </body>
    </html>

{% endhighlight %}

2.Add **&lt;div&gt;** element with in the **&lt;Body&gt;** tag.

{% highlight html %}

    <body style="width:100%;height:100%;position:static;">
       <!--Add  TreeGrid control here-->
       <div id="TreeGridContainer" style="width:60%;height:80%;position:absolute;"></div>
    </body>

{% endhighlight %}

3.Create the TreeGrid with the empty data source.

{% highlight js %}

     $(function () {
         $("#TreeGridContainer").ejTreeGrid({                
             columns: [                    
                 { field: "taskName", headerText: "Task Name" },
                 { field: "startDate", headerText: "Start date"},
                 { field: "endDate", headerText: "End Date" },
                 { field: "duration", headerText: "Duration"},
                 { field: "progress", headerText: "Progress"}
             ]
         });

     });


{% endhighlight %}

![](/js/TreeGrid/Getting-Started_images/Getting-Started_img2.png)

TreeGrid with empty datasource 
{:.caption}

4.Create data source for TreeGrid.

{% highlight js %}

        var treeGridDataSource = [
                {
                    taskID: 2,
                    taskName: "Planning",
                    startDate: "02/03/2014",
                    endDate: "02/07/2014",
                    duration: 10,
                    progress: 56,
                    subtasks: [
                        {
                            taskID: 3,
                            taskName: "Plan timeline",
                            startDate: "02/03/2014",
                            endDate: "02/07/2014",
                            duration: 5,
                            progress: "100"
                        },
                        {
                            taskID: 4,
                            taskName: "Plan budget",
                            startDate: "02/03/2014",
                            endDate: "02/07/2014",
                            duration: 5,
                            progress: "100"
                        },
                        {
                            taskID: 5,
                            taskName: "Allocate resources",
                            startDate: "02/03/2014",
                            endDate: "02/07/2014",
                            duration: 5,
                            progress: "100"
                        },
                        {
                            taskID: 6,
                            taskName: "Planning complete",
                            startDate: "02/07/2014",
                            endDate: "02/07/2014",
                            duration: 0,
                            progress: 40
                        }
                    ]
                },
                {
                    taskID: 7,
                    taskName: "Design",
                    startDate: "02/10/2014",
                    endDate: "02/14/2014",
                    duration: 10,
                    progress: 76,
                    subtasks: [
                        {
                            taskID: 8,
                            taskName: "Software Specification",
                            startDate: "02/10/2014",
                            endDate: "02/12/2014",
                            duration: 3,
                            progress: "60"
                        },
                        {
                            taskID: 9,
                            taskName: "Develop prototype",
                            startDate: "02/10/2014",
                            endDate: "02/12/2014",
                            duration: 3,
                            progress: "100"
                        },
                        {
                            taskID: 10,
                            taskName: "Get approval from customer",
                            startDate: "02/13/2014",
                            endDate: "02/14/2014",
                            duration: 2,
                            progress: "100"
                        },
                        {
                            taskID: 11,
                            taskName: "Design complete",
                            startDate: "02/14/2014",
                            endDate: "02/14/2014",
                            duration: 0,
                            predecessor: "10FF",
                            progress: 65
                        }
                    ]
                }

        ]; 

{% endhighlight %}

5.Initialize the TreeGrid with data source created in last step.

{% highlight js %}

     $(function () {
         $("#TreeGridContainer").ejTreeGrid({
             dataSource: treeGridDataSource,
             //Map the child mapping to render the hierarchical data
             childMapping: "subtasks",                
             columns: [                    
                 { field: "taskName", headerText: "Task Name" },
                 { field: "startDate", headerText: "Start Date"},
                 { field: "endDate", headerText: "End Date" },
                 { field: "duration", headerText: "Duration"},
                 { field: "progress", headerText: "Progress"}
             ]
         });

     });

{% endhighlight %}

TreeGrid widget is displayed as the output in the following screenshot.

![](/js/TreeGrid/Getting-Started_images/Getting-Started_img3.png)

### Enable Sorting

The TreeGrid control has sorting functionality, to arrange the data in ascending or descending order based on a particular column.

#### Multicolumn Sorting

Enable the multicolumn sorting in TreeGrid by setting [`allowMultiSorting`](/js/api/ejtreegrid#allowmultisortingspan-classtype-signature-type-booleanbooleanspan "allowMultiSorting") as `true`. You can sort multiple columns in TreeGrid, by selecting the desired column header while holding the `Ctrl` key.

{% highlight js %}

        $("#TreeGridContainer").ejTreeGrid({
            //...
            allowSorting: true,
            allowMultiSorting:true           
        });

{% endhighlight %}

![](/js/TreeGrid/Getting-Started_images/Getting-Started_img4.png)

### Enable Editing

You can enable Editing in TreeGrid by using the [`editSettings`](/js/api/ejtreegrid#editsettingsspan-classtype-signature-type-objectobjectspan "editSettings") property as follows.

{% highlight js %}

    $("#TreeGridContainer").ejTreeGrid({
        //...
        editSettings: {
            allowEditing: true,
            editMode: "cellEditing"
        }
    });

{% endhighlight %}

And also, the following editors are provided for support in TreeGrid control.

* stringedit
* booleanedit
* numericedit
* dropdownedit
* datepicker
* datetimepicker

You can set the editor type for a particular column as follows.

{% highlight js %}

    $("#TreeGridContainer").ejTreeGrid({
        //...
        columns: [{
            field: "startDate",
            headerText: "Start Date",
            editType: "datepicker"
        }, {
            field: "endDate",
            headerText: "End Date"
        }, {
            field: "duration",
            headerText: "Duration",
            editType: "numericedit"
        }, ]
    })

{% endhighlight %}

The output of the DateTimePicker editor in TreeGrid control is as follows.

![](/js/TreeGrid/Getting-Started_images/Getting-Started_img5.png)

