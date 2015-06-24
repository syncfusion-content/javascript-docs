---
layout: post
title: Columns
description: columns
platform: js
control: Gantt
documentation: ug
---

# Columns

The TreeGrid column displays the information from a bounded data source and it will be editable to update the task details through **TreeGrid**.

### Column Resizing

You can change the width of the column in TreeGrid to show the entire text of the column by resizing the column. The following code example shows you how to enable the Column Resize feature at **Gantt** initialize.

{% highlight js %}

     $("#GanttContainer").ejGantt({
        //...
        allowColumnResize: true
    });

{% endhighlight %}

### Column Template

Column template is used to customize the column’s look and feel, based on requirement. 

The following code example shows you how to display the icon in the TreeGrid column.

{% highlight html %}

        <script type="text/x-jsrender" id="columnTemplate">        
                 <div  style='height:20px;width:20px;margin:auto;background-image:url(".../images/\{\{:\~className\(\)\}\}")'/>              
        </script>

{% endhighlight %}

{% highlight js %}

            $.views.helpers({ className: getClassName });

            function getClassName() {

                var cellValue = this.data.item && this.data.item["Platform"];

                switch (cellValue) {

                    case "ASP.NET":
                        cellValue = "asp.png";
                        break;

                    case "ASP.NET MVC":
                        cellValue = "mvc.png";
                        break;

                    case "JS":
                        cellValue = "js.png";
                        break;

                    case "Mobile MVC":
                        cellValue = "mob.png";
                        break;

                    case "Silverlight":
                        cellValue = "sl.png";
                        break;

                    case "Windows Forms":
                        cellValue = "wf.png";
                        break;

                    case "Windows Phone":
                        cellValue = "wp.png";
                        break;
                    default:
                }
                return cellValue;
            }


            var projectDetails = [
                {
                    "Id": 1,
                    "Platform": "ASP.NET",
                    "TaskName": "Volume 1 Release",
                    "StartDate": "01/06/2014",
                    "Duration": 5,
                    "Progress": 30,
                    "children": [
                        {
                            "Id": 2,
                            "Platform": "ASP.NET MVC",
                            "TaskName": "Volume1Sprint1",
                            "StartDate": "01/06/2014",
                            "Duration": 5,
                            "Progress": 100
                        },
                        {
                            "Id": 3,
                            "Platform": "JS",
                            "TaskName": "Volume1Sprint2",
                            "StartDate": "01/13/2014",
                            "Duration": 5,
                            "Progress": 100
                        },
                        {
                            "Id": 4,
                            "Platform": "Mobile MVC",
                            "TaskName": "Volume1Sprint3",
                            "StartDate": "01/20/2014",
                            "Duration": 5,
                            "Progress": 100
                        },
                        {
                            "Id": 5,
                            "Platform": "Silverlight",
                            "TaskName": "Volume1Sprint4",
                            "StartDate": "01/27/2014",
                            "Duration": 5,
                            "Progress": 100
                        },
                        {
                            "Id": 6,
                            "Platform": "Windows Forms",
                            "TaskName": "Volume1Sprint5",
                            "StartDate": "02/03/2014",
                            "Duration": 5,
                            "Progress": 100
                        },
                        {
                            "Id": 7,
                            "Platform": "Windows Phone",
                            "TaskName": "Volume1Sprint6",
                            "StartDate": "02/10/2014",
                            "Duration": 5,
                            "Progress": 100
                        }
                    ]
                }
            ];

            $(function () {

                $("#GanttContainer").ejGantt({
                    dataSource: projectDetails,
                    taskIdMapping: "Id",
                    taskNameMapping: "TaskName",
                    startDateMapping: "StartDate",
                    progressMapping: "Progress",
                    durationMapping: "Duration",
                    childMapping: "children",
                    scheduleStartDate: "1/06/2014",
                    scheduleEndDate: "02/28/2014",

                    load: function () {
                        var columns = this.getColumns();
                        columns.splice(1, 0,
                            {
                                field: "Platform",
                                headerText: "Product",
                                isTemplateColumn: true,
                                templateID: "columnTemplate",
                                width: "60px"
                            });
                    }
                });
            });


{% endhighlight %}

The following screenshot displays the customized column in Gantt control.

{% include image.html url="/js/Gantt/Columns_images/Columns_img1.png"%}

### Column Chooser

Gantt supports enabling and disabling the visibility of the columns dynamically with the `showColumnChooser` property. The visibility of the custom columns can also be toggled with this property. Column chooser option is rendered as a sub menu item within the column menu in the Gantt columns. 

{% include image.html url="/js/Gantt/Columns_images/Columns_img2.png"%}

The column menu is enabled with the `showColumnChooser` property, where the default value for this property is `false`.

The column menu provides the following options:

* Sort Ascending
* Sort Descending
* Columns 

Sort Ascending and Sort Descending options can be enabled or disabled with the `allowSorting` property. Single level sorting can be performed with these options. To perform multilevel sorting, `allowMultiSorting` property should be enabled. You can also disable the visibility of a particular column in the column collection manually by setting the `visible` property to `false`.

{% highlight js %}

    $("#gantt").ejGantt(
    {   
        // ...     
          showColumnChooser: true,
          allowSorting: true,
          allowMultiSorting: true,
        // ...             
    });

{% endhighlight %}

The following screenshot displays the column chooser in the Gantt control.

{% include image.html url="/js/Gantt/Columns_images/Columns_img3.png"%}

