---
layout: post
title: Data-Binding
description: data binding
platform: js
control: TreeGrid
documentation: ug
---

# Data Binding

**Data Binding** is the process that establishes a connection between the application and different kinds of data sources such as business objects.

**Local Data Binding**

In **Local Data Binding**, datasource for rendering the **TreeGrid** control is retrieved from the same application locally.

Two types of **Data Binding** are possible with **TreeGrid** control, 

* Hierarchical Datasource Binding

* Self-Referential Data Binding (Flat Data)

**Hierarchy Datasource Binding**

The following code example shows you how to bind the **Hierarchical** local data into the **TreeGrid** control.

{% highlight js %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">

<head>
    <title>Getting Started with TreeGrid Control for JavaScript</title>
    <meta charset="utf-8" />   
    <!-- style sheet for default theme(flat azure) -->
    <link href=" http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />   
    <!--scripts-->  
    <script src="http://code.jquery.com/jquery-1.10.2.min.js"></script>
    <script src="http://borismoore.github.io/jsrender/jsrender.min.js"></script>
    <script src="http://ajax.aspnetcdn.com/ajax/globalize/0.1.1/globalize.js"></script>
    <script src="http://cdnjs.cloudflare.com/ajax/libs/jquery-easing/1.3/jquery.easing.min.js"></script>
    <script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js" type="text/javascript"></script>

    <script type="text/javascript">


var projectData = [
     {
         taskID: 1,
         taskName: "Planning",
         startDate: "02/03/2014",
         endDate: "02/07/2014",
         progress: 100,
         duration:5,
         subtasks: [
             {
               taskID: 2,
               taskName: "Plan timeline",
               startDate: "02/03/2014",
               endDate: "02/07/2014",
               duration: 5,
               progress: 100 },
             {
               taskID: 3,
               taskName: "Plan budget",
               startDate: "02/03/2014",
               endDate: "02/07/2014",
               duration: 5,
               progress: 100 },

               //...
               //...
            ]
     },

    //...
    //...

];
  </script>
</head>

<body>
<script type="text/javascript">        

        $(function () {

            $("#TreeGridContainer").ejTreeGrid({
                dataSource: projectData,
                childMapping: "subtasks",
                treeColumnIndex:1,
                columns: [
                    { field: "taskID", headerText: "Task Id", width: "45" },
                    { field: "taskName", headerText: "Task Name" },
                    { field: "startDate", headerText: "Start Date" },
                    { field: "endDate", headerText: "End Date" },
                    { field: "duration", headerText: "Duration" },
                    { field: "progress", headerText: "Progress" }
                ]
            })
        });

    </script>
</body>

</html>


{% endhighlight %}



The output of the above steps is as follows:

{% include image.html url="/js/TreeGrid/Concepts-and-Features/Data-Binding_images/Data-Binding_img1.png" Caption="Hierarchy Datasource Binding"%}

**Self-Referential Data Binding (Flat Data)**

**TreeGrid** is rendered from **Self-Referential** data structures by providing two fields: **ID** field and **parent ID** field.

* **ID Field**- This field contains unique values used to identify nodes. Its name is assigned to the **idMapping** property.

* **Parent ID Field**- This field contains values that indicate parent nodes. Its name is assigned to the **parentIdMapping** property.



{% highlight js %}

//...
<script type="text/javascript">      

 var projectData1 = [

             { taskID: 1, taskName: "Task 1", startDate: "02/03/2014", endDate: "03/07/2014", duration: 5},

            { taskID: 2, pId: 1, taskName: "Child Task 1", startDate: "02/03/2014", endDate: "02/07/2014", duration: 5},

            { taskID: 3, pId: 1, taskName: "Child Task 2", startDate: "02/03/2014", endDate: "02/07/2014", duration: 5, progress: "100" },

            { taskID: 22, pId: 2, taskName: "Sub Child Task 1", startDate: "02/03/2014", endDate: "02/07/2014", duration: 5 },

            { taskID: 23, pId: 2, taskName: "Sub Child Task 2", startDate: "02/03/2014", endDate: "02/07/2014", duration: 5, progress: "100" },

            { taskID: 12, pId: 22, taskName: "Inner Child Task 1", startDate: "02/03/2014", endDate: "02/07/2014", duration: 5},

            { taskID: 13, pId: 22, taskName: "Inner Child Task 2", startDate: "02/03/2014", endDate: "02/07/2014", duration: 5, progress: "100"}, 

            //...

            //...

        ];

     $(function () {

            $("#TreeGridContainer").ejTreeGrid({
                dataSource: projectData1,
                childMapping: "subtasks",
                treeColumnIndex:1,
                idMapping:"taskID",
                parentIdMapping:"pId",
                columns: [
                    { field: "taskID", headerText: "Task Id", width: "45" },
                    { field: "taskName", headerText: "Task Name" },
                    { field: "startDate", headerText: "Start Date" },
                    { field: "endDate", headerText: "End Date" },
                    { field: "duration", headerText: "Duration" },
                    { field: "progress", headerText: "Progress" }
                ]
            })
        });

    </script>


{% endhighlight %}



The following screenshot shows the output of the above steps,

{% include image.html url="/js/TreeGrid/Concepts-and-Features/Data-Binding_images/Data-Binding_img2.png" Caption="Self-Referential DataBinding"%}

