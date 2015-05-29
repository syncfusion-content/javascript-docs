---
layout: post
title: getting-started
description: getting started
platform: js
control: TreeGrid
documentation: ug
---

# Getting Started

## Create your first TreeGrid in JavaScript

The **Essential Javascript TreeGrid** has been designed to represent and edit the hierarchical data. 

This section explains how to create a **TreeGrid** control in your application with hierarchical data source and enable sorting and editing in **TreeGrid** control. The following screenshot displays the output.



{% include image.html url="\js\TreeGrid\getting-started_images\getting-started_img1.png" Caption="Figure 1: TreeGrid"%}



1. Create an **HTML** file and add the following template to the **HTML** file.



{% highlight html %}


<!DOCTYPE html>

<html xmlns="http://www.w3.org/1999/xhtml">

<head>

    <meta name="viewport" content="width=device-width, initial-scale=1.0" />

    <meta charset="utf-8" />

    <link href=" http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />

    <script src="http://code.jquery.com/jquery-1.10.1.min.js"></script>

    <script src="http://cdnjs.cloudflare.com/ajax/libs/jquery-easing/1.3/jquery.easing.min.js"></script>

    <script src="http://ajax.aspnetcdn.com/ajax/globalize/0.1.1/globalize.min.js"></script>

    <script src="http://borismoore.github.io/jsrender/jsrender.min.js"></script>

    <script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js" type="text/javascript"></script>
</head>

<body>
    <!--Add TreeGrid control here -->
</body>
</html>


{% endhighlight %}



2. Add **&lt;div&gt;** element with in the **&lt;Body&gt;** tag.



{% highlight js %}


<body style="width:100%;height:100%;position:static;">
   <!--Add  TreeGrid control here-->
   <div id="TreeGridContainer" style="width:60%;height:80%;position:absolute;"></div>
</body>


{% endhighlight %}



3. Create the **ejTreeGrid** with the empty data source.



{% highlight js %}

<script type="text/javascript">
     //...
     $(function () {
         $("#TreeGridContainer").ejTreeGrid({                
             columns: [                    
                 { field: "taskName", headerText: "Task Name" },
                 { field: "startDate", headerText: "Start date"},
                 { field: "endDate", headerText: "End Date" },
                 { field: "duration", headerText: "Duration”},
                 { field: "progress", headerText: "Progress"}
             ]
         });

     });
</script>


{% endhighlight %}



{% include image.html url="\js\TreeGrid\getting-started_images\getting-started_img2.png" Caption="Figure 2: TreeGrid with empty datasource "%}

4. Create data source for **ejTreeGrid.**



{% highlight js %}

<!DOCTYPE html>

<html xmlns="http://www.w3.org/1999/xhtml">

<head>
   //...
    <script type="text/javascript">

//data source for ejTreeGrid control

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
    </script>
</head>


{% endhighlight %}



5. Initialize the **ejTreeGrid** with data source created in last step.



{% highlight js %}

<script type="text/javascript">
     //...
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
</script>


{% endhighlight %}



A **TreeGrid** is displayed as the output in the following screenshot.



{% include image.html url="\js\TreeGrid\getting-started_images\getting-started_img3.png" Caption="Figure 3: TreeGrid with given datasource"%}



**Enable Sorting**

The **ejTreeGrid** control has sorting functionality, to arrange the data in ascending or descending order based on a particular column.

**Multicolumn Sorting**

Enable the multicolumn sorting in **ejTreeGrid** by setting **allowMultiSorting** as **True**. You can sort multiple columns in **ejTreeGrid,** by selecting the desired column header 	while holding the **CTRL** key.



{% highlight js %}

<script type="text/javascript">
    //...
    $("#TreeGridContainer").ejTreeGrid({
        //...
        allowSorting: true,
        allowMultiSorting:true           
    });
</script>


{% endhighlight %}



{% include image.html url="\js\TreeGrid\getting-started_images\getting-started_img4.png" Caption="Figure 4: TreeGrid enabled with sorting "%}



**Enable Editing**

You can enable Editing in **ejTreeGrid** by using the **Edit** option as follows.



{% highlight js %}

<script type="text/javascript">
    //...
    $("#TreeGridContainer").ejTreeGrid({
        //...
        edit: {
            allowEditing: true,
            editMode: "cellEditing"
        }
    });
</script>


{% endhighlight %}



And also, the following editors are provided for support in **ejTreeGrid** control.

* stringedit

* booleanedit

* numericedit

* dropdownedit

* datepicker

* datetimepicker

You can set the editor type for a particular column as follows.

{% highlight js %}

<script type="text/javascript">
    //...
    $("#TreeGridContainer").ejTreeGrid({
        //...
        columns: [
               { field: "startDate", headerText: "Start Date",editType:"datepicker"},
               { field: "endDate", headerText: "End Date" },
               { field: "duration", headerText: "Duration",editType:"numericedit"},
                 ]
    })
</script>


{% endhighlight %}



The output of the **DateTimePicker** editor in **TreeGrid** control is as follows.



{% include image.html url="\js\TreeGrid\getting-started_images\getting-started_img5.png" Caption="Figure 5: TreeGrid editing with DateTime Picker"%}

