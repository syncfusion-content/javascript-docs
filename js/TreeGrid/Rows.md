---
layout: post
title: Rows
description: rows
platform: js
control: TreeGrid
documentation: ug
api: /api/js/ejtreegrid
---

# Rows

The **TreeGrid** rows displays the information of each row from the bounded data source.

## Row Template

Row template is used to customize the **TreeGrid** rows based on requirements. In TreeGrid, the [`rowTemplateID`](/api/js/ejtreegrid#members:rowtemplateid) and [`altRowTemplateID`](/api/js/ejtreegrid#members:altrowtemplateid) properties are used for customizing the row.

The [`rowTemplateID`](/api/js/ejtreegrid#members:rowtemplateid) is used to customize all the rows in TreeGrid. For this property, ID of the row template is to be provided.

The [`altRowTemplateID`](/api/js/ejtreegrid#members:altrowtemplateid) is used to customize the alternative rows in TreeGrid. For this property, ID of the alternative row template is to be provided.

{% highlight css %}

      .e-treegrid .e-selectionbackground {
        background-color: #CED8F6;
        }

      .border {
        border-color: #BDBDBD;
        border-width: 1px;
        border-style: solid;
       }

{% endhighlight %}

{% highlight html %}

      <script id="rowTemplateScript" type="text/x-jsrender">

      <tr style="background-color:#F2F2F2;color:#000000;">

      <td class="border" style='height:30px;'>
         <div>{{"{{"}}:#data['EmployeeID']{{}}}}</div>
      </td>

      <td class="border" style='height:30px;'>
         <div style="font-size:14px;">
         {{"{{"}}:#data['Name']{{}}}}
         <p style="font-size:9px;">{{"{{"}}:#data['Designation']{{}}}}</p>
         </div>
      </td>

      <td class="border">
      <div style="padding-top:5px;">
      <div style="display:inline-flex !important;">
      <img src="../images/treegrid/{{"{{"}}:#data['Full Name']{{}}}}.png"/></div>
      <div style="display:inline-block;padding-left:10px;">
      {{"{{"}}:#data['Address']{{}}}}
      <p>{{"{{"}}:#data['Country']{{}}}}</p>
      <p style="font-size:12px;">{{"{{"}}:#data['Contact']{{}}}}</p>
      </div>
      </div>
      </td>

      <td class="border" style='height:30px;'>
      <div>{{"{{"}}:#data['DOB']{{}}}}</div>
      </td>
      
      </tr>
      </script>

      <script id="altRowTemplateScript" type="text/x-jsrender">

      <tr style="background-color:#E6E6E6;color:#000000;">

       <td class="border" style='height:30px;'>
       <div>{{"{{"}}:#data['EmployeeID']{{}}}}</div>
       </td>

      <td class="border" style='height:30px;'>
      <div style="font-size:14px;">{{"{{"}}:#data['Name']{{}}}}
      <p style="font-size:9px;">{{"{{"}}:#data['Designation']{{}}}}</p>
      </div>
      </td>

      <td class="border">
      <div style="padding-top:5px;">
      <div style="display:inline-flex !important;">
      <img src="../images/treegrid/{{"{{"}}:#data['Full Name']{{}}}}.png"/></div>
      <div style="display:inline-block;padding-left:10px;">
      {{"{{"}}:#data['Address']{{}}}}
      <p>{{"{{"}}:#data['Country']{{}}}}</p>
      <p style="font-size:12px;">{{"{{"}}:#data['Contact']{{}}}}</p>
      </div>
      </div>
      </td>     

      <td class="border" style='height:30px;'>
      <div>{{"{{"}}:#data['DOB']{{}}}}</div>
      </td>
   
      </tr>
      </script>
{% endhighlight %}

{% highlight js %}

        var treeData = [{
            "Name": "Robert King",
            "Full Name": "Robert King",
            "Designation": "Chief Executive Officer",
            "EmployeeID": "EMP001",
            "Address": "507 - 20th Ave. E.Apt. 2A, Seattle",
            "Contact": "(206) 555-9857",
            "Country": "USA",
            "DOB": "2/15/1963",

            "Children": [{
                "Name": "David William",
                "Full Name": "David William",
                "Designation": "Vice President",
                "EmployeeID": "EMP004",
                "Address": "722 Moss Bay Blvd., Kirkland",
                "Country": "USA",
                "Contact": "(206) 555-3412",
                "DOB": "5/20/1971",
                 // ...

            }]
        }];
        
      $(function () {

       $("#TreeGridContainer").ejTreeGrid({

            dataSource: treeData,
            childMapping: "Children",
            allowColumnResize: true,
            rowTemplateID: "rowTemplateScript",
            altRowTemplateID: "altRowTemplateScript",
            editSettings: { allowEditing: true, editMode: "cellEditing" },
            columns: [
                   {headerText: "Employee ID", width: "180" },
                   { field: "Name", headerText: "Employee Name" },
                   { field: "Address", headerText: "Employee picture", width: "300" },
                   { field: "DOB", headerText: "DOB", editType: "datepicker" },
            ]
       })
    });

{% endhighlight %}

The output of TreeGrid with **Row Template** is as follows.

![](/js/TreeGrid/Rows_images/Rows_img1.png)

## Row Height
The [`rowHeight`](/api/js/ejtreegrid#members:rowheight) property is used to change the height of row in tree grid, default value of this property is 30.

The following code example explains how to change the row height in tree grid

{% highlight js %}

      $("#treegrid").ejTreeGrid({
          //...     
          rowHeight: 50,
          // ...
       });

{% endhighlight %}

![](/js/TreeGrid/Rows_images/Rows_img5.png)

The above screenshot shows TreeGrid render with row height of 50.
{:.caption}

## Alternate row styling

Alternate row style is used to enable the different background color for every alternate row. The [`enableAltRow`](/api/js/ejtreegrid#members:enablealtrow) property is used to enable the alternate row style in tree grid, default value of this property is true.

The following code explains about enabling the alternate row style in tree grid

{% highlight js %}

      $("#treegrid").ejTreeGrid({
          //...     
          enableAltRow: true,
          // ...
       });

{% endhighlight %}

![](/js/TreeGrid/Rows_images/Rows_img4.png)

The above screenshot shows TreeGrid with alternate row style.
{:.caption}

## Row Drag and Drop

It is possible to dynamically re-arrange the rows in the TreeGrid control by using the [`allowDragAndDrop`](/api/js/ejtreegrid#members:allowdraganddrop) property. With this property, row drag and drop can be enabled or disabled. Rows can be inserted above, below as a sibling or as a child to the existing row with the help of this feature. A default tooltip is rendered while dragging the TreeGrid row and this tooltip can be customized by the [`dragTooltip`](/api/js/ejtreegrid#members:dragtooltip) property. This property has inner properties such as the [`showTooltip`](/api/js/ejtreegrid#members:dragtooltip-showtooltip "dragTooltip.showTooltip"), [`tooltipItems`](/api/js/ejtreegrid#members:dragtooltip-tooltipitems "dragTooltip.tooltipItems"), [`tooltipTemplate`](/api/js/ejtreegrid#members:dragtooltip-tooltiptemplate "dragTooltip.tooltipTemplate").

The [`showTooltip`](/api/js/ejtreegrid#members:dragtooltip-showtooltip "dragTooltip.showTooltip") property is used to enable or disable the tooltip. By default, this property value is `false`.

The following code explains about enabling the row drag and drop with the default tooltip in the TreeGrid.

{% highlight js %}

      $("#treegrid1").ejTreeGrid({
          //...     
          columns: [{
                  field: "taskID",
                  headerText: "Task Id"
              }, {
                  field: "taskName",
                  headerText: "Task Name"
              },
              //...
          ],
          allowDragAndDrop: true,
          dragTooltip: {
              showTooltip: true
          },
          // ...
       });

{% endhighlight %}

The following screenshot depicts a row drag and drop in the TreeGrid widget.

![](/js/TreeGrid/Rows_images/Rows_img2.png)

### Customizing Drag tooltip

The [`tooltipItems`](/api/js/ejtreegrid#members:dragtooltip-tooltipitems "dragTooltip.tooltipItems") property is used to customize the tooltip items. By using this property, specific fields can be rendered in the tooltip. By default this property value is `null`, and all the defined field items are rendered in the tooltip.

The following code shows how to render row drag tooltip with the desired field items.

{% highlight js %}

      $("#treegrid1").ejTreeGrid({
          //...     
          dragTooltip: {
              showTooltip: true,
              tooltipItems: [
                  "taskID",
                  "taskName",
                  "startDate",
                  "endDate"
              ]
          },
          //... 
      });

{% endhighlight %}

The [`tooltipTemplate`](/api/js/ejtreegrid#members:dragtooltip-tooltiptemplate "dragTooltip.tooltipTemplate") property renders the template tooltip for row drag and drop in the TreeGrid control by using the JsRender template. You can provide either the id value of the script element or the script element to the property.

The following code shows how to render row drag tooltip with tooltip template.	

{% highlight html %}

      <script id="customTooltip" type="text/x-jsrender">
      <tr>
         <td class="border" style='height:30px;'>
         <div>{{"{{"}}:#data['TaskId']{{}}}}</div>
         </td>
   
         <td class="border" style='height:30px;'>
         <div>{{"{{"}}:#data['TaskName']{{}}}}</div>
         </td>
      </tr>
      </script>

{% endhighlight %}

{% highlight js %}

        $("#treegrid1").ejTreeGrid({
            //...     
            dragTooltip: {
                showTooltip: true,
                tooltipTemplate: "#customTooltip",
            },
            //...             
        });

{% endhighlight %}

![](/js/TreeGrid/Rows_images/Rows_img3.png)

## Details row

Details row is used to provide a additional information about each row of tree grid. You can specify the detail row jsRender template id or HTML element as string to [`detailsTemplate`](/api/js/ejtreegrid#members:detailstemplate) property. However you need to enable the details template by setting [`showDetailsRow`](/api/js/ejtreegrid#members:showdetailsrow) property as `true`.

The following code example shows how to enable details tow in tree grid.

{% highlight HTML %}
<script id="descriptionTemplate" type="text/x-jsrender">
    <div style="position: relative; display: inline-block; float: left; font-weight: bold; width: 10%">
        <img src="../content/images/treegrid/{{:Name}}.png" style="margin-left: 10px;margin-top:15px;" />
    </div>
    <div style="padding-left: 10px; display: inline-block; width: 88%; text-wrap: normal;font-size:12px;font-family:'Segoe UI';margin-top:2px;">
        <div class="e-description" style="word-wrap: break-word;">
            <b>{{:Name}}</b> was born on {{:~_treeGridDateFormatter("DOB")}}. Now lives at {{:Address}},{{:Country}}. {{:Name}} holds a position of <b>{{:Designation}}</b> in our WA department, (Seattle USA). Joined our company on {{:~_treeGridDateFormatter("DOJ")}}.
        </div>
        <div class="e-description" style="word-wrap: break-word;margin-top:5px;">
         <b style="margin-right:10px;">Contact:</b>{{:Contact}}
        </div>
    </div>
</script>

<script>
    $("#TreeGrid").ejTreeGrid({
        //...     
        detailsTemplate:"descriptionTemplate",
        enableCollapseAll: true,
        //...
    });
</script>
{% endhighlight %}

![](/js/TreeGrid/Rows_images/Rows_img8.png)

The above screenshot shows details row in tree grid.
{:.caption}

[Click](https://js.syncfusion.com/demos/web/#!/bootstrap/treegrid/rows/detailstemplate) here to view the demo sample for details row template.

### Disable details row info column
On enabling details template, details row info column will be added in tree grid. It is used for show or hide the detail row of respective row. You can disable that column while enabling details template using [`showDetailsRowInfoColumn`](/api/js/ejtreegrid#members:showdetailsrowinfocolumn) property. If you disable details row info column, then the details row will render next to the respective row.

The following code example shows how to hide detail info column in tree grid. 

{% highlight javascript %}

$("#TreeGrid").ejTreeGrid({
    //...     
    detailsTemplate:"descriptionTemplate",
    enableCollapseAll: true,
    showDetailsRowInfoColumn:false,
    //...
});

{% endhighlight %}

![](/js/TreeGrid/Rows_images/Rows_img9.png)

The above screenshot shows details row rendered next to the respective row.
{:.caption}

### Defining row height for detail template

In TreeGrid, It is provide a support to change the detail template height using [`detailsRowHeight`](/api/js/ejtreegrid#members:detailsrowheight) property.

The following code example shows how to set details row height in tree grid. 

{% highlight javascript %}

$("#TreeGrid").ejTreeGrid({
    //...     
    detailsTemplate:"descriptionTemplate",
    enableCollapseAll: true,
    detailsRowHeight:150,
    //...
});

{% endhighlight %}

![](/js/TreeGrid/Rows_images/Rows_img10.png)

The above screenshot shows details row rendered with height of `150px`.
{:.caption}

## Expand/Collapse Row

In TreeGrid, parent rows are expanded/collapsed by using expand/collapse icons, expand all/collapse all toolbar items and by using public methods. By default all records in TreeGrid will be rendered in expanded state.

### Collapse parent records at initial load

It is possible to display all the records in collapsed state by setting [`enableCollapseAll`](/api/js/ejtreegrid#members:enablecollapseall) property as `true`. 

The following code example shows how to use this property.

{% highlight javascript %}

$("#TreeGrid").ejTreeGrid({
    //...     
    enableCollapseAll: true,
    //...
});

{% endhighlight %}

![](/js/TreeGrid/Rows_images/Rows_img6.png)

The above screenshot shows TreeGrid render with collapsed state.
{:.caption}

###  Define expand/collapse state of every record

In TreeGrid, it is possible to render records either in collapsed state or in expanded state, and this can done by mapping the expand state to the records from the data source by using [`expandStateMapping`](/api/js/ejtreegrid#members:expandstatemapping) property.

The following code example shows how to use this property.

{% highlight javascript %}

var data = [
    //...
    {
         taskID: 6,
         taskName: "Design",
         startDate: new Date("02/10/2014"),
         endDate: new Date("02/14/2014"),
         duration: 3,
         expandState:false,
         subtasks: [
             { 
                 taskID: 7, 
                 taskName: "Software Specification", 
                 startDate: new Date("02/10/2014"), 
                 endDate: new Date("02/12/2014"), 
                 duration: 3,
                 expandState:false },
            //...
         ]
     },
];
$("#TreeGrid").ejTreeGrid({
    //...     
    dataSource: data,
    expandStateMapping: "expandState",
    //...
});

{% endhighlight %}

The below screenshot shows the output of above code example..

![](/js/TreeGrid/Rows_images/Rows_img7.png)

### Expand/Collapse all the rows dynamically

All the rows in tree grid will be expanded/collapsed by clicking `expandAll` and `collapsedAll` toolbar items or by using [`expandAll`](/api/js/ejtreegrid#methods:expandall "expandAll()") and [`collapseAll`](/api/js/ejtreegrid#methods:collapseall "collapseAll()") methods. We can invoke this methods dynamically on any action like external button click. 

The below code example shows how to use this methods.

{% highlight js %}

$("#TreeGrid").ejTreeGrid({
    //...
    toolbarSettings: {
        showToolbar: true,
        toolbarItems: [
            ej.TreeGrid.ToolbarItems.Add,
            //..
            ej.TreeGrid.ToolbarItems.ExpandAll,
		    ej.TreeGrid.ToolbarItems.CollapseAll
        ]
    },
});

$("#expandAll").click(function () {
    var treegridObj = $("#TreeGrid").ejTreeGrid("instance");
        treegridObj.expandAll();
});

$("#collapseAll").click(function () {
    var treegridObj = $("#TreeGrid").ejTreeGrid("instance");
        treegridObj.collapseAll();
});

{% endhighlight %}


### Dynamically expand/Collapse the specific level row

The tree grid control provide the support to dynamically expand/collapse the specific level row by using [`expandAtLevel`](/api/js/ejtreegrid#methods:expandatlevel "expandAtLevel(index)") and [`collapseAtLevel`](/api/js/ejtreegrid#methods:collapseatlevel "collapseAtLevel(index)") methods. This methods are used to expand/ collapse the all rows which are in specific level.


The below code example shows how to use this methods.

{% highlight js %}

$("#TreeGrid").ejTreeGrid({
    //...
    dataSource:data,
    //..
});

$("#expandAtLevel").click(function () {
    var treegridObj = $("#TreeGrid").ejTreeGrid("instance");
        treegridObj.expandAtLevel(1);
});

$("#collapseAtLevel").click(function () {
    var treegridObj = $("#TreeGrid").ejTreeGrid("instance");
        treegridObj.collapseAtLevel(1);
});

{% endhighlight %}

## Summary Row

Summary rows in TreeGrid is used to summarize every hierarchy with the set of predefined summary types using the column values. Using the [`summaryRows`](https://help.syncfusion.com/api/js/ejtreegrid#members:summaryrows "summaryRows") property, user can define the summary rows in TreeGrid.
Title for each summary row can be defined using the [`summaryRows.title`](https://help.syncfusion.com/api/js/ejtreegrid#members:summaryrows-title "summaryRows.title") property. And using the [`summaryRows.summaryColumns`](https://help.syncfusion.com/api/js/ejtreegrid#members:summaryrows-summarycolumns "summaryRows.summaryColumns") property, it is possible to defined the summary for specific columns alone in a summary row.

### Defining summary columns

Using the [`summaryRows.summaryColumn.summaryType`](https://help.syncfusion.com/api/js/ejtreegrid#members:summaryrows-summarycolumns-summarytype "summaryRows.summaryColumn.summaryType") property, user can define the type of summary to be displayed in a column. The [`summaryRows.summaryColumns.dataMember`](https://help.syncfusion.com/api/js/ejtreegrid#members:summaryrows-summarycolumns-datamember "summaryRows.summaryColumns.dataMember") property is used the map the field values which is used for summary calculations. The [`summaryRows.summaryColumns.displayColumn`](https://help.syncfusion.com/api/js/ejtreegrid#members:summaryrows-summarycolumns-displaycolumn "summaryRows.summaryColumns.displayColumn") property is used to specify the column in which the summary to be displayed.
The [`summaryRows.summaryColumns.prefix`](https://help.syncfusion.com/api/js/ejtreegrid#members:summaryrows-summarycolumns-prefix "summaryRows.summaryColumns.prefix") and [`summaryRows.summaryColumns.suffix`](https://help.syncfusion.com/api/js/ejtreegrid#members:summaryrows-summarycolumns-suffix "summaryRows.summaryColumns.suffix") properties are used to define the text should be displayed along with the summary column value. The [`summaryRows.summaryColumns.format`](https://help.syncfusion.com/api/js/ejtreegrid#members:summaryrows-summarycolumns-format "summaryRows.summaryColumns.format") property is used for formatting the summary column value.
The below code snippet explains defining a summary row in TreeGrid,

{% highlight js %}

        $("#treegrid").ejTreeGrid({
            summaryRows: [
                       {
                           title: "Maximum",
                           summaryColumns: [
                               {
                                   summaryType: ej.TreeGrid.SummaryType.Maximum,
                                   dataMember: "TotalUnits",
                                   displayColumn: "TotalUnits",
                                   prefix: "Individual maximum unit = "
                               },
                               {
                                   summaryType: ej.TreeGrid.SummaryType.Maximum,
                                   dataMember: "TotalCosts",
                                   displayColumn: "TotalCosts",
                                   prefix: "Individual maximum Cost = ",
                                   format: "{0:C}"
                               }
                           ]
                       },
                       {
                           title: "Total",
                           summaryColumns: [
                               {
                                   summaryType: ej.TreeGrid.SummaryType.Sum,
                                   dataMember: "TotalCosts",
                                   displayColumn: "TotalCosts",
                                   prefix: "Total costs = ",
                                   format: "{0:C}"
                               },
                               {
                                   summaryType: ej.TreeGrid.SummaryType.Sum,
                                   dataMember: "UnitWeight",
                                   displayColumn: "UnitWeight",
                                   prefix: "Total weight = ",
                                   suffix: " Pounds"
                               }]
                       }
            ],
            //...
        });

{% endhighlight %}

The below screenshot shows the output of above code example..

![](/js/TreeGrid/Rows_images/Rows_img8.png)
