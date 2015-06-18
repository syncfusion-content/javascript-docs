---
layout: post
title: Getting-Started
description: getting started
platform: js
control: Gantt
documentation: ug
---

# Getting Started

This section explains briefly about how to create a **Gantt****chart** in your application with **JavaScript**.

## Create your first Gantt in JavaScript

### Control Structure

Gantt chart is used to edit and visualize project schedule, and also to track progress of a task. The following screenshot illustrates the elements that constitute a **Gantt** chart.

{% include image.html url="/js/Gantt/Getting-Started_images/Getting-Started_img1.png" Caption="Figure 1:Gantt chart"%}

* **Toolbar** – It is a collection of toolbar buttons to add, edit, or delete a task. You can indent or outdent a task, using their respective buttons. Following screenshot illustrates the function of each toolbar button,

{% include image.html url="/js/Gantt/Getting-Started_images/Getting-Started_img2.png" Caption="Figure 2:Toolbar of Gantt chart"%}

* **Search Textbox** – It is used to search tasks that contain a search string.

* **Resource Names** – It displays the names of the resources assigned to a task.

* **Task bar** – It is a graphical representation of the duration of task.

* **Task Progress** – It displays the percentage of the task completed.

* **Header** – It represents time-scale based on which a task bar is drawn.

* **Tree Grid** – It displays the tasks and its sub tasks in a hierarchical table.

* **Task Relationship** – It determines when to start or finish a task.

* **Interactive Editing** – You can edit the duration of a task, by simply dragging or resizing the task bar. Following screenshot illustrates how this works.

{% include image.html url="/js/Gantt/Getting-Started_images/Getting-Started_img3.png" Caption="Figure 3:Customization of Gantt "%}

### Create your Gantt chart

In this tutorial, you can learn how to create a simple Gantt chart, add tasks or subtasks, and set relationship between tasks during the design phase of a software project. The following screenshot displays the desired output after completing this tutorial,

{% include image.html url="/js/Gantt/Getting-Started_images/Getting-Started_img4.png" Caption="Figure 4:Simple Gantt chart"%}

1.Create an HTML file and add the following template to the HTML file.

{% highlight html %}

    <!DOCTYPE html>

    <html xmlns="http://www.w3.org/1999/xhtml">

    <head>

        <title>Getting Started with Gantt Control for JavaScript</title>

        <!-- style sheet for default theme(flat azure) -->
        <link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />

        <!--scripts-->
        <script src="http://code.jquery.com/jquery-1.10.2.min.js"></script>

        <script src="http://borismoore.github.io/jsrender/jsrender.min.js"></script>

        <script src="http://ajax.aspnetcdn.com/ajax/globalize/0.1.1/globalize.js"></script>

        <script src="http://cdnjs.cloudflare.com/ajax/libs/jquery-easing/1.3/jquery.easing.min.js"></script>

        <script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js "></script>

    </head>

    <body>
        <!--Add  Gantt control here-->
    </body>

    </html>


{% endhighlight %}



2.Add a **&lt;div&gt;** element with in the &lt;Body&gt; tag.

{% highlight html %}

    <body>    
        <!--Add  Gantt control here-->    
        <div id="GanttContainer"></div>    
    </body>

{% endhighlight %}



3.Create data source for ejGantt.

{% highlight js %}

    var data = [{
        taskID: 1,
        taskName: "Design",
        startDate: "02/10/2014",
        endDate: "02/14/2014",
        duration: 6,          
        subtasks: [
            {
                taskID: 2,
                taskName: "Software Specification",
                startDate: "02/10/2014",
                endDate: "02/12/2014",
                duration: 4,
                progress: "60",
                resourceId: [2]
            },
            {
                taskID: 3,
                taskName: "Develop prototype",
                startDate: "02/10/2014",
                endDate: "02/12/2014",
                duration: 4,
                progress: "70",
                resourceId: [3]
            },
            {
                taskID: 4,
                taskName: "Get approval from customer",
                startDate: "02/12/2014",
                endDate: "02/14/2014",
                duration: 2,
                progress: "80",
                predecessor: "3FS",
                resourceId: [1]
            },
            {
                taskID: 5,
                taskName: "Design complete",
                startDate: "02/14/2014",
                endDate: "02/14/2014",
                duration: 0,
                predecessor: "4FS"
            }
        ]
    }];

{% endhighlight %}



4. Initialize the **ejGantt** with data source created in the last step.

{% highlight js %}

    $(function() {
        $("#GanttContainer").ejGantt({
            dataSource: data, //Provides data source for Gantt
            taskIdMapping: "taskID", //Provide name of the property which contains task id in the data source
            taskNameMapping: "taskName", //Provide name of the property which contains task name in the data source
            scheduleStartDate: "02/01/2014", //Provide schedule header start date
            scheduleEndDate: "03/14/2014", //Provide schedule header end date
            startDateMapping: "startDate", //Provide name of the property which contains start date of the task in the data source
            durationMapping: "duration", //Provide name of the property which contains duration of the task in the data source
            progressMapping: "progress", //Provide name of the property which contains progress of the task in the data source
            childMapping: "subtasks", //Provide name of the property which contains subtask of the task in the data source
        });
    });

{% endhighlight %}



A **Gantt** chart is created as shown in the following screen shot.

{% include image.html url="/js/Gantt/Getting-Started_images/Getting-Started_img5.png" Caption="Gantt Chart"%}

### Enable Toolbar

Gantt control contains toolbar options to edit, search, expand or collapse all records, indent, outdent, delete, and add a task. You can enable toolbar using the **toolbar** option.

{% highlight js %}

    toolbarSettings: {
     showToolbar:true,
     toolbarItems:[
        ej.Gantt.ToolbarItems.Add,
        ej.Gantt.ToolbarItems.Edit,
        ej.Gantt.ToolbarItems.Delete,
        ej.Gantt.ToolbarItems.Update,
        ej.Gantt.ToolbarItems.Cancel,
        ej.Gantt.ToolbarItems.Indent,
        ej.Gantt.ToolbarItems.Outdent,
        ej.Gantt.ToolbarItems.ExpandAll,
        ej.Gantt.ToolbarItems.CollapseAll,
        ej.Gantt.ToolbarItems.Search
        ],
    }


{% endhighlight %}



The following screen shot displays a Tool bar in Gantt chart control:

{% include image.html url="/js/Gantt/Getting-Started_images/Getting-Started_img6.png" Caption="Figure 6:Toolbar in Gantt Chart"%}

> **Note:** Add, edit, delete options are enabled when enabling the allowEditing, allowAdding, allowDelete properties in the edit Options.

### Enable Sorting

The **ejGantt** control has sorting functionality to arrange the tasks in ascending or descending order based on a particular column.

#### Multicolumn Sorting

Enable the multicolumn sorting in **ejGantt** by setting **allowMultiSorting** as “_True_”. You can sort multiple columns in **ejGantt** ,by selecting the desired column header while holding the **CTRL** key.

{% highlight js %}

    $("#GanttContainer").ejGantt({
         //…
         allowSorting:true,
         allowMultiSorting: true,
    });


{% endhighlight %}

### Enable Editing

You can enable editing using **edit** and **allowGanttChartEditing** options**.**

#### Cell Editing

Modify the task details through the grid cell editing by setting the **editMode** as **cellEditing.**

#### Normal Editing

Modify the task details through the edit dialog by setting the **editMode** as **normal.**

#### Taskbar Editing

Modify the task details through user interaction such as resizing and dragging the taskbar.

#### Predecessor Editing

Modify the predecessor details of a task using mouse interactions by setting **allowGanttChartEditing** as true and setting the value for **predecessorMapping** property.

{% highlight js %}

    $("#GanttContainer").ejGantt({
        //...
        allowGanttChartEditing:true, //enable the taskbar editing 
        predecessorMapping:"predecessor" ,// Predecessor editing 
        editSettings: {
            allowEditing: true,
            allowAdding: true,
            allowDeleting: true,
            editMode:"normal",
        },
    });


{% endhighlight %}



The following screen shot displays a Gantt chart control with Enable Editing options.

{% include image.html url="/js/Gantt/Getting-Started_images/Getting-Started_img7.png" Caption="Figure 7: Gantt chart control with Enable Editing options"%}

> **Note:** Both cellEditing and  normal  editing operations are performed through double-click action.

### Enable Context Menu

You can enable the context menu in **ejGantt,** by setting the **enableContextMenu** as _**True**_.

{% highlight js %}

    $("#GanttContainer").ejGantt({   
        //...
        enableContextMenu:true
    });


{% endhighlight %}



The following screen shot displays **Gantt chart** in which Context menu option is enabled:

{% include image.html url="/js/Gantt/Getting-Started_images/Getting-Started_img8.png" Caption="Figure 8: Gantt chart with Context menu option enabled"%}

### Provide tasks relationship

In **ejGantt**, you have the predecessor support to show the relationship between two different tasks.

* **Start to Start (SS) -** You cannot start a task until the other task also starts.

* **Start to Finish (SF) -** You cannot finish a task until the other task finishes.

* **Finish to Start (FS) -** You cannot start a task until the other task completes.

* **Finish to Finish (FF) -** You cannot finish a task until the other task completes.

You can show the relationship in tasks, by using the **predecessorsMapping,** as shown in the following code example.

{% highlight js %}

    $("# GanttContainer ").ejGantt({                
       //...
       predecessorMapping: "predecessor"
    });


{% endhighlight %}



The following screenshot displays the relationship between tasks.

{% include image.html url="/js/Gantt/Getting-Started_images/Getting-Started_img9.png" Caption="Figure 9: Gantt chart with task relationship"%}

### Provide Resources

In **ejGantt** control, you can display and assign the resource for each task. Create a collection of **JSON** object, which contains id and name of the resource and assign it to **resourceCollection** option. Then, specify the field name for id and name of the resource in the resource collection to **resourceIdMapping** and **resourceNameMapping** options. The name of the field, which contains the actual resources assigned for a particular task in the **dataSource** is specified using **resourceInfoMapping.**

1.Create the resource collection to be displayed in ejGantt

{% highlight js %}

    var projectResources =[{
        resourceId: 1,
        resourceName: "Project Manager"
    },{
        resourceId: 2,
        resourceName: "Software Analyst"
    },{
        resourceId: 3,
        resourceName: "Developer"
    },{
        resourceId: 4,
        resourceName: "Testing Engineer"
    }];

{% endhighlight %}



2.Initialize the ejGantt with resources created in last step. 

{% highlight js %}

    $("# GanttContainer ").ejGantt({
        //...
        resourceInfoMapping: "resourceId", //Field name which contains resource details for the task 
        resourceNameMapping: "resourceName",//resource Name mapping
        resourceIdMapping: "resourceId",//resource Id Mapping
        resources: projectResources,//resource collection dataSource
    });


{% endhighlight %}



The following screenshot displays resource allocation for tasks in Gantt chart.

{% include image.html url="/js/Gantt/Getting-Started_images/Getting-Started_img10.png" Caption="Figure 10 :Gantt chart with resource allocation for tasks"%}

By following these steps, you have learnt how to provide data source to Gantt chart, how to configure Gantt to set task relationships, assign resources for each task, and add toolbar with necessary buttons.

