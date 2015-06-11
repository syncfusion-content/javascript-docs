---
layout: post
title: Columns
description: columns
platform: js
control: TreeGrid
documentation: ug
---

# Columns

The **TreeGrid** column displays the information from a bounded data source and it is editable to update the task details through **TreeGrid**.

### Column Resizing

You can change the width of the column in **TreeGrid** to show the entire text of the column by resizing the column. The following code example shows you how to enable the **Column Resize** feature at **Gantt** initialize.

{% highlight js %}


$("#TreeGridContainer").ejTreeGrid({

     //...
     allowColumnResize: true,
});



{% endhighlight %}

### Column Template

**Column Template** is used to customize the column’s look and feel based on requirement.

The following code example shows you how to display the icon in the **TreeGrid** column.

{% highlight js %}


<script type="text/x-jsrender" id="customColumnTemplate">     
     <div  style='height:20px;' unselectable='on'>{{if hasChildRecords}}<div class='intend' style='height:1px; float:left; width:{{:level*20}}px; display:inline-block;'></div>
       {{else !hasChildRecords}}
       <div class='intend' style='height:1px; float:left; width:{{:(level)*20}}px; display:inline-block;'></div>
       {{/if}}                         
       <div class='{{if expanded}}e-treegridexpand {{else hasChildRecords}}e-treegridcollapse {{/if}} {{if level===4}}e-doc{{/if}}' style='height:20px;width:30px;margin:auto;float:left;margin-left:10px;
       style='float: left;display:inline-block; unselectable='on'></div>
       <div class='e-cell' style='display:inline-block;width:100%' unselectable='on'>{{:#data['Name']}}</div>
     </div>
    </script>   

    <style type="text/css">
        .e-treegrid .e-treegridexpand {
            background-image: url(../images/treegrid/folder-open.png);
            background-repeat: no-repeat;
            width: 14px;
            height: 14px;
        }
        .e-treegrid .e-treegridcollapse {
            background-image: url(../images/treegrid/Folder.png);
            background-repeat: no-repeat;
            width: 14px;
            height: 14px;
        }
        .e-treegrid .e-doc {
            background-image: url(../images/treegrid/Document.png);
            background-repeat: no-repeat;
            width: 14px;
            height: 14px;
        }

        .e-treegrid .e-treegridexpand:before {
            content: none;
        }

        .e-treegrid .e-treegridcollapse:before {
            content: none;
        }
    </style>

    <script type="text/javascript">         

        $(function () {

            $("#TreeGridContainer").ejTreeGrid({
                dataSource: treeGridDataSource,
                childMapping: "Children",
                columns: [{ field: "Name", headerText: "Name", isTemplateColumn: true,        templateID: "customColumnTemplate" },
                          { field: "Type", headerText: "Type" },
                          { field: "DateCreated", headerText: "Date Created" },
                          { field: "DateModified", headerText: "Date Modified" }]
            })
        });

    </script>


{% endhighlight %}



The following screenshot displays the customized column in **TreeGrid** control.

{% include image.html url="/js/TreeGrid/Concepts-and-Features/Columns_images/Columns_img1.png" Caption="Customized Column"%}

### Column Filtering

Column Filtering in **TreeGrid** is used to filter the records by single or multiple column conditions. In **ejTreeGrid** control, column filtering can be enabled with **allowFiltering** property, by setting this property to ‘true’, a filter bar is rendered in all available columns, providing filtering support to every columns. You can also limit filtering to specific column by setting ‘false’ to **allowFiltering** property in each column object.

Filtering modes can be toggled between **immediate** and **onEnter** modes using **filterBarMode** property.

* immediate- In this mode, filtering starts with key press event.

* onEnter- In this mode, filtering starts when enter key is pressed.

Filtering type can be defined by **filterEditType** property in each column object.

**filterEditType**

* stringedit

* numericedit

* booleanedit

* dropdownlist

* datepicker

* datetimepicker



{% highlight js %}


$("#treegrid1").ejTreeGrid(
        {   
           // ...     
            filterBarMode: "immediate",
                allowFiltering: true,
                columns: [

                    { field: "taskID", headerText: "Task Id", width: "45", allowFiltering:false, editType: "numericedit" },
                    { field: "taskName", headerText: "Task Name", editType: "stringedit", filterEditType: "stringedit" },
                    { field: "startDate", headerText: "Start Date", editType: "datepicker", filterEditType: "datepicker" },
                    { field: "endDate", headerText: "End Date", editType: "datepicker", filterEditType: "datepicker" },
                    { field: "duration", headerText: "Duration", editType: "booleanedit", filterEditType: "numericedit" },
                    { field: "progress", headerText: "Progress", editType: "booleanedit", filterEditType: "numericedit" }
                ],
            // ...             
        });


{% endhighlight %}



The following screenshot displays the column filtering in **TreeGrid** control.

{% include image.html url="/js/TreeGrid/Concepts-and-Features/Columns_images/Columns_img2.png" Caption="Column filtering in TreeGrid control"%}

### Column Chooser

**TreeGrid** supports enabling and disabling the visibility of the columns dynamically with the **showColumnChooser** property. By using this property, the visibility of the custom columns can also be toggled. The **Column chooser** option is rendered as sub menu item within column menu in the **TreeGrid** columns.

{% include image.html url="/js/TreeGrid/Concepts-and-Features/Columns_images/Columns_img3.png" Caption="Column menu with column chooser                                                  "%}

The column menu is enabled with the **showColumnChooser** property and the default value for this property is **false**

The column menu provides the following options.

* Sort Ascending

* Sort Descending

* Columns 

The **Sort Ascending** and **Sort Descending** options are enabled or disabled by using the **allowSorting** property. With these options, single level sorting can be performed in the **TreeGrid** columns. To perform multilevel sorting, the **allowMultiSorting** property should be enabled. 

You can also disable the visibility of the particular column in column collection manually by setting the **visible** property to **false**.

{% highlight js %}


$("#treegrid1").ejTreeGrid(
{   
    // ...     
    showColumnChooser: true,
    allowSorting: true,
    allowMultiSorting: true,
    columns:[
              // ...  
              { field: "duration", headerText: "Duration", 
                visible: false
              }
              // ...  
            ],
    // ...             
});


{% endhighlight %}



{% include image.html url="/js/TreeGrid/Concepts-and-Features/Columns_images/Columns_img4.png" Caption="TreeGrid with column chooser"%}

