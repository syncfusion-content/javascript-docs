---
layout: post
title: Columns
description: columns
platform: js
control: TreeGrid
documentation: ug
api: /api/js/ejtreegrid
---

# Columns

Column definitions specified in the [`columns`](/api/js/ejtreegrid#members:columns) option defines how the data in the **dataSource** have to be displayed, formatted and edited in TreeGrid. The values in the **dataSource** can be mapped to the appropriate column using the [`field`](/api/js/ejtreegrid#members:columns-field "columns.field") property of the corresponding column object.

## Editing type

The edit type of a column can be defined using the [`editType`](/api/js/ejtreegrid#members:columns-edittype "columns.edittype") property of the column object.

The following example shows how to define the edit type in a column,

{% highlight js %}

        $("#treegrid").ejTreeGrid({
            columns: [
                {
                  editType: ej.TreeGrid.EditingType.Numeric
                },
                {
                    editType: ej.TreeGrid.EditingType.Boolean
                }]
        });

{% endhighlight %}

The column editors can be further customized using the [`editParams`](/api/js/ejtreegrid#members:columns-editparams "columns.editparams") property of the column object. 

The following example shows how to define additional properties to customize the date edit type,

{% highlight js %}

        $("#treegrid").ejTreeGrid({
              columns: [
                    {
                    editType: "datepicker",
                    editParams: {highlightWeekend : true }
                    }
                ],
        });

{% endhighlight %}


## Formatting

The values in each column can be formatted using the [`format`](/api/js/ejtreegrid#members:columns-format "columns.format") property of the column object.

The following example shows how to specify the numeric format string to display currency, percentage symbols and date values in a column.

{% highlight js %}

    $(function () {
        $("#TreeGridContainer").ejTreeGrid({
            //...
            columns: [
                { field: "Percentage", headerText: "Percentage", format: "{0:P0}"},
                { field: "Currency", headerText: "Currency", format: "{0:C2}" },
                { field: "startDate", headerText: "Start Date", format: "{0:MM/dd/yyyy}" },
                { field: "endDate", headerText: "End Date", format: "{0:MM/dd/yyyy hh:mm:ss}"}
            ]
        });
    });

{% endhighlight %}

N>
For more numeric format strings, please refer this [link](https://msdn.microsoft.com/library/dwhawy9k(v=vs.100).aspx).

For more date format strings, please refer this [link](https://msdn.microsoft.com/library/az4se3k1(v=vs.100).aspx).

## Defining column width

In TreeGrid, it is possible to define width for a specific column by setting [`width`](/api/js/ejtreegrid#members:columns-width "columns.width") property of column.

The below code snippet shows how to set width for specific column.

{% highlight js %}

    $(function () {
        $("#TreeGridContainer").ejTreeGrid({
            //...
            columns: [
                { field: "taskID", headerText: "Task Id", width:50},
                { field: "taskName", headerText: "Task Name", width:150 },
                { field: "startDate", headerText: "Start Date", width:100 },
                { field: "endDate", headerText: "End Date", width:100 }
                { field: "duration", headerText: "Duration", width:100 }                    
            ]
            //..
        })
    });

{% endhighlight %}

The below screenshot shows TreeGrid render with specific column width.

![](/js/TreeGrid/Columns_images/Columns_img13.png)

### Defining common width for the columns

The TreeGrid control provide the support to set same width for all the columns in tree grid using [`commonWidth`](/api/js/ejtreegrid#members:commonwidth) property.

The below code snippet shows how to set common width for tree grid columns.

{% highlight js %}

    $(function () {
        $("#TreeGridContainer").ejTreeGrid({
            //...
            commonWidth:140,
            //...
        })
    });

{% endhighlight %}

The below screenshot shows TreeGrid render with common width. 

![](/js/TreeGrid/Columns_images/Columns_img16.png)

## Headers

### Header text

Using the [`headerText`](/api/js/ejtreegrid#members:columns-headertext "columns.headerText") property, you can provide the title for a specific column. The below code snippet shows how to set header text for the columns.

{% highlight js %}

    $(function () {
        $("#TreeGridContainer").ejTreeGrid({
            //...
            columns: [
                { field: "taskID", headerText: "Task Id"},
                { field: "taskName", headerText: "Task Name" },
                { field: "startDate", headerText: "Start Date" },
                { field: "endDate", headerText: "End Date" }                   
            ]
        })
    });

{% endhighlight %}

### Text wrapping

It is possible to wrap the header text or the title for the column, when the content exceeds the column width using the [`headerTextOverflow`](/api/js/ejtreegrid#members:headertextoverflow) property. By default this property is set to **none**. To enable wrapping of header text, you have to set the [`headerTextOverflow`](/api/js/ejtreegrid#members:headertextoverflow) property to **‘wrap’**. The below code snippet demonstrates this.

{% highlight js %}

    $("#TreeGridContainer").ejTreeGrid({
        //...
        headerTextOverflow: "wrap",
    });

{% endhighlight %}

### Header Template

Using the [`headerTemplateID`](/api/js/ejtreegrid#members:columns-headertemplateid "columns.headerTemplateID") property, you can specify the Id of the script element, which contains the JsRender template, to the specific column.

Following code snippet shows how to set the header template,

{% highlight html %}

    <script type="text/x-jsrender" id="resource">
        <div>
            <div class="name">
                <img src="13.4.0.53/themes/web/images/treegrid/icon-03.png" width="20" height="20" />
            </div>
            <div style="position:relative; top:3px;">
                Resources
            </div>
        </div>
    </script>
    
    <script type="text/x-jsrender" id="projectName">
        <div>
            <div>
                <img src="13.4.0.53/themes/web/images/treegrid/icon-01.png" width="20" height="20" />
            </div>
            <div style="position:relative; top:3px;">
                Task Name
            </div>
        </div>
    </script>

{% endhighlight %}

{% highlight js %}

    $(function () {
        $("#TreeGridContainer").ejTreeGrid({
            //...
            columns: [{
                field: "taskName",
                editType: "stringedit",
                headerTemplateID: "#projectName"
            }, {
                field: "startDate",
                editType: "datepicker"
            }, {
                field: "resourceId",
                editType: "dropdownedit",
                dropdownData: projectResources,
                headerTemplateID: "#resource"
            }, {
                field: "progress",
                editType: "numericedit"
            }]
        })
    });

{% endhighlight %}

The below screenshot depicts column headers with custom templates.

![](/js/TreeGrid/Columns_images/Columns_img1.png)

## Frozen Columns

Specific columns can be frozen by enabling the [`isFrozen`](/api/js/ejtreegrid#members:columns-isfrozen "columns.isFrozen") property of the respective column object. The columns which are frozen remain static while scrolling the content horizontally. You can also freeze or unfreeze a column during runtime, by selecting Freeze or Unfreeze menu item in the column menu. These set of menu options will be displayed in all the columns when the [`isFrozen`](/api/js/ejtreegrid#members:columns-isfrozen "columns.isFrozen") property is enabled in any of the columns. However you can control the visibility of these menu options in a particular column by enabling/disabling the [`allowFreezing`](/api/js/ejtreegrid#members:columns-allowfreezing "columns.allowFreezing") property of that specific column.

{% highlight js %}

    $(function () {
        $("#TreeGridContainer").ejTreeGrid({
            //...
            showColumnChooser: true,
            columns: [
                { field: "taskID", headerText: "ID", width: 60, isFrozen: true, allowFreezing: false },
                { field: "taskName", headerText: "Task Name", width: 200, isFrozen: true },
                { field: "startDate", headerText: "Start Date" },
                { field: "endDate", headerText: "End Date" },
                { field: "duration", headerText: "Duration" },
            ]
        });
    });

{% endhighlight %}

The below screenshot depicts TreeGrid with frozen columns,

![](/js/TreeGrid/Columns_images/Columns_img2.png)

It is also possible to freeze all the preceding columns at run-time by choosing *Freeze Preceding Columns* option in the column menu or by using the [`freezePrecedingColumns`](https://help.syncfusion.com/api/js/ejtreegrid#methods:freezeprecedingcolumns "freezePrecedingColumns") method, the column field name, for which the columns preceding it to be frozen should be passed as the method parameter.

![](/js/TreeGrid/Columns_images/Columns_img3.png)

### Freezing columns using method

Columns can also be frozen or unfrozen with custom actions using the [`freezeColumn`](/api/js/ejtreegrid#methods:freezecolumn "freezeColumn") method.
The column's field name which is to be frozen/unfrozen should be passed as the method parameter, along with the freeze state.

{% highlight js %}

        var treegridObj = $("#treegrid").data("ejTreeGrid");
        treegridObj.freezeColumn(field, true);

{% endhighlight %}

## Resizing

You can resize the column width to view the hidden text of the cell. This feature can be enabled by setting the [`allowColumnResize`](/api/js/ejtreegrid#members:allowcolumnresize) property to true.

{% highlight js %}

    $("#TreeGridContainer").ejTreeGrid({

        //...
        allowColumnResize: true,
    });

{% endhighlight %}

### Column resize mode

In Treegrid, it is possible to provide different column resizing mode using [`columnResizeMode`](/api/js/ejtreegrid#members:columnresizesettings-columnresizemode "columnResizeSettings.columnResizeMode") property of [`columnResizeSettings`](/api/js/ejtreegrid#members:columnresizesettings).

The below are the types of column resize modes available in TreeGrid,

* Normal - Columns are stretched with control width at load time. When resizing the column, the current column width is updated based on next column.
* Next column - Columns are stretched with control width at load time. When resize the column the current column width is updated based on stretching columns in control width.
* Fixed Columns - Column are rendered with given width value at load time. Only the current column width is changed while resizing the column.

The following code snippet explains how to set column resize mode in tree grid.

{% highlight js %}

   $("#TreeGridContainer").ejTreeGrid({
    //...
    columnResizeSettings:{
        columnResizeMode: ej.TreeGrid.ColumnResizeMode.FixedColumns
    }
    //...
});

{% endhighlight %}

![](/js/TreeGrid/Columns_images/Columns_img15.png)

The above screenshot shows the tree grid render with `FixedColumns` resize mode.
{:.caption}

### Customize column resize action

In TreeGrid, [`columnResizeStart`](https://help.syncfusion.com/api/js/ejtreegrid#events:columnresizestart), [`columnResizeEnd`](https://help.syncfusion.com/api/js/ejtreegrid#events:columnresizeend) and [`columnResized`](https://help.syncfusion.com/api/js/ejtreegrid#events:columnresized) events are triggered on column resize action. Using this event we can prevent column resize for particular column.

The below code example shows how to prevent the column resize for particular column

{% highlight js %}

   $("#TreeGridContainer").ejTreeGrid({
    //...
    allowColumnResize: true,
    columnResizeStart:function(args)
    {
        if (args.column.field == "taskName") // Prevent the column resize for Task Name column
            args.cancel = true;
    },
    //...
});
{% endhighlight %}

## Checkbox column 

It is possible to display a column as checkbox column in TreeGrid by enabling the [`displayAsCheckbox`](/api/js/ejtreegrid#members:columns-displayascheckbox "columns.displayAsCheckbox") property and by setting the `editType` property as `Boolean` for the column .  If the [`displayAsCheckbox`](/api/js/ejtreegrid#members:columns-displayascheckbox "columns.displayAsCheckbox") property is set as false, then the column will be displayed as string column with the value mapped from the data source.
The following code snippet explains how to display a checkbox column in TreeGrid.

{% highlight js %}

   $("#TreeGridContainer").ejTreeGrid({
    //...
    columns: [
        //...
        {
            field: "approved",
            headerText: "Approved",
            editType: "booleanedit",
            displayAsCheckbox: true
        }
    ],
});

{% endhighlight %}

The below screen shot depicts the `Approved` column in TreeGrid displayed as a checkbox column.

![](/js/TreeGrid/Columns_images/Columns_img8.png)

The index of the checkbox column can be changed at run-time using the [`updateCheckboxColumn`](https://help.syncfusion.com/api/js/ejtreegrid#methods:updatecheckboxcolumn "updateCheckboxColumn") method. The index of the column in which the checkbox should be displayed is passed as the method parameter.

## Column Template

Columns can be customized either by using JsRender templates or by AngularJS templates.

One of the following property is used for set column template in TreeGrid.

* [`templateID`](/api/js/ejtreegrid#members:columns-templateid "columns.templateID") - Using the [`templateID`](/api/js/ejtreegrid#members:columns-templateid "columns.templateID") property, you can specify the Id of the script element, which contains the template for the column.
* [`template`](/api/js/ejtreegrid#members:columns-template "columns.template") - HTML templates can be specified in the [`template`](/api/js/ejtreegrid#members:columns-template "columns.template") property of the particular column as a string (HTML element).
* [`angularTemplate`](/api/js/ejtreegrid#members:columns-angulartemplate "angularTemplate") - Specifies the template ID or the template string of the AngularJS script element for specific column.

However, you need to enable the [`isTemplateColumn`](/api/js/ejtreegrid#members:columns-istemplatecolumn "columns.isTemplateColumn") property for the specific column to display the custom template instead of default template.

Following code example show how to define template for the column.

{% highlight html %}

    // JsRender template definition.
    <script type="text/x-jsrender" id="columnTemplate">
        {{if #data['resourceNames']}}
           <div style="display:inline-block;position:relative;left:10px;top:1px">
               <img src="../images/gantt/{{:#data['resourceNames']}}.png" height="40" />
           </div>
        {{/if}}
    </script>
    
{% endhighlight %}

{% highlight js %}

    <script type="text/javascript">         
        $(function () {
            $("#TreeGridContainer").ejTreeGrid({
               //...
               rowHeight:50,
               columns: [
                    { field: "taskID", headerText: "Task Id", width: "45" },
                    { field: "taskName", headerText: "Task Name" },
                    { headerText: "Resource", isTemplateColumn: true, templateID: "columnTemplate", textAlign: "center" },
                    { field: "resourceNames", headerText: "Resource Name" },
               ]
            })
        });
    </script>

{% endhighlight %}

![](/js/TreeGrid/Columns_images/Columns_img4.png)

## Column Menu

Column menu can be displayed in column header by enabling the [`showColumnChooser`](/api/js/ejtreegrid#members:showcolumnchooser).

Following are the items displayed in the column menu,

* **Column Chooser** – Displays all the column names, you can enable or disable a column by selecting or deselecting the respective column name in the column chooser menu.
* **Sort Ascending & Sort Descending** – Used to sort the items in the column. These menu options will be displayed only when you set the [`allowSorting`](/api/js/ejtreegrid#members:allowsorting) property as true. To perform multilevel sorting, the [`allowMultiSorting`](/api/js/ejtreegrid#members:allowmultisorting) property should be enabled.
* **Freeze, Unfreeze & Freeze Preceding Columns** – Used to freeze or unfreeze the columns. These set of menu options will be displayed in all the columns when the [`isFrozen`](/api/js/ejtreegrid#members:columns-isfrozen "columns.isFrozen") property is enabled in any of the columns. However, you can control the visibility of these menu options in a particular column by enabling/disabling the [`allowFreezing`](/api/js/ejtreegrid#members:columns-allowfreezing "columns.allowFreezing") property of that specific column.

{% highlight js %}

    $("#treegrid1").ejTreeGrid(
    {   
        // ...     
        showColumnChooser: true,
        allowSorting: true,
        allowMultiSorting: true,
        columns:[
            // ...  
            { field: "duration", headerText: "Duration", visible: false }
            // ...  
        ],
        // ...             
    });

{% endhighlight %}

![](/js/TreeGrid/Columns_images/Columns_img5.png)


The column menu also provides support for some of the additional column options such as,

* Insert column left
* Insert column right 
* Delete column
* Rename column

The column options can be enabled or disabled with the [`showColumnOptions`](/api/js/ejtreegrid#members:showcolumnoptions) property, default value of this property is `false`.

Following code example shows how to enable the column option in tree grid.

{% highlight js %}

        $("#treegrid1").ejTreeGrid(   
        {   
            // ...     
            showColumnOptions:true,
            // ...             
        });

{% endhighlight %}

![](/js/TreeGrid/Columns_images/Columns_img17.png)

![](/js/TreeGrid/Columns_images/Columns_img18.png)

The above screenshot shows insert column dialog in TreeGrid  
{:.caption}

The TreeGrid columns can also be renamed or deleted at run-time with custom actions using the [`renameColumn`](https://help.syncfusion.com/api/js/ejtreegrid#methods:renamecolumn "renameColumn") and [`deleteColumn`](https://help.syncfusion.com/api/js/ejtreegrid#methods:deletecolumn "deleteColumn") methods.

### Customizing the insert column dialog.

It is possible to add or remove the [`columns`](/api/js/ejtreegrid#members:columns) properties in insert column dialog using [`columnDialogFields`](/api/js/ejtreegrid#members:columndialogfields) property. In insert column option [`field`](/api/js/ejtreegrid#members:columns-field "columns.field"), [`headerText`](/api/js/ejtreegrid#members:columns-headertext "columns.headerText") and [`editType`](/api/js/ejtreegrid#members:columns-edittype "columns.editType") properties are necessary to create a new column, so this fields are unable to remove from insert column option.

Following code example shows how to customize the insert column option in tree grid.

{% highlight js %}
        $("#treegrid1").ejTreeGrid(
        {
            // ...     
            allowSorting: true,
            showColumnOptions: true,
            columnDialogFields: ["field", "headerText", "editType", "width", "visible", "allowSorting", "textAlign", "headerTextAlign"],
            // ...             
        });


{% endhighlight %}

![](/js/TreeGrid/Columns_images/Columns_img19.png)

The above screenshot shows customized insert column dialog in tree grid.  
{:.caption}


### Hide specific column in column chooser list
It is possible to hide the specific column in column chooser list by settings [`showInColumnChooser`](/api/js/ejtreegrid#members:columns-showincolumnchooser "columns.showInColumnChooser") as `false` in the column definition.

Following code example shows how to hide specific column in column chooser list

{% highlight js %}

    $("#treegrid1").ejTreeGrid(
    {   
        // ...     
        showColumnChooser: true,
        columns:[
            // ...  
            { field: "taskID", headerText: "Task Id", showInColumnChooser: false }
            // ...  
        ],
        // ...             
    });

{% endhighlight %}

![](/js/TreeGrid/Columns_images/Columns_img14.png)

The above screenshot shows TreeGrid column chooser rendered without `Task Id` column. 
{:.caption}

## Show/Hide columns using method

It is possible to toggle the visibility of the columns using the [`hideColumn`](/api/js/ejtreegrid#methods:hidecolumn "hideColumn") and [`showColumn`](/api/js/ejtreegrid#methods:showcolumn "showColumn") methods. The column's header text should be passed as the method parameter which is to be hidden.

{% highlight js %}

        var treegridObj = $("#treegrid").data("ejTreeGrid");
        treegridObj.hideColumn("Task Name");
        treegridObj.showColumn("Order ID");

{% endhighlight %}


## Command Column

### Default action buttons

Using command columns in TreeGrid, we can display a separate column to perform CRUD operations.It is also possible to perform any custom actions by using custom command buttons. Command column can be defined in TreeGrid using the [`commands`](/api/js/ejtreegrid#members:columns-commands "columns.commands") property.
A command column can be customized by using [`type`](/api/js/ejtreegrid#members:columns-commands-type "columns.commands.type") and [`buttonOptions`](/api/js/ejtreegrid#members:columns-commands-buttonoptions "columns.commands.buttonOptions") properties.

* **type** – Using this property we can add required action buttons in TreeGrid command column such as edit, delete, save and cancel.
* **buttonOptions** - Using this property we can customize the button in the command column with the properties available in the [ejButton](https://help.syncfusion.com/api/js/ejbutton#members "ejButton").

{% highlight js %} 
	$("#TreeGrid").ejTreeGrid({
		editSettings : {
			allowEditing : true,
			allowAdding : true,
			allowDeleting : true
		},
		columns : [{
				headerText : "Command Column",
				commands : [
					{ type : "edit", buttonOptions : { text : "Edit" } },
					{ type : "delete", buttonOptions : { text : "Delete" } },
					{ type : "save", buttonOptions : { text : "Save" } }, 
					{ type : "cancel", buttonOptions : { text : "Cancel" } }
				],
				width : 150
			}
		]
	});

{% endhighlight %}

![](/js/TreeGrid/Columns_images/Columns_img9.png)

### Custom buttons

We can also add custom buttons to the command column by specifying text value other than default buttons to the type property. We can also bind actions to the custom button using the [click](https://help.syncfusion.com/api/js/ejbutton#events:click "click") client-side event of ejButton.

{% highlight javascript %}
$(function () {
	$("#TreeGrid").ejTreeGrid({
		columns : [{
               headerText: "Details",
               commands: [
                            { type: "details", buttonOptions: { text: "Details", click:"onClick"} }]}]
	});
});

function onClick(args) {
            var $tr = $(args.e.target).closest('tr'),
                treeObj = $("#TreeGrid").data("ejTreeGrid"),
                rowIndex = treeObj.getIndexByRow($tr),
                record = treeObj.model.currentViewData[rowIndex];
            alert("Task Name: " + record.item.taskName);
        }
{% endhighlight %}

![](/js/TreeGrid/Columns_images/Columns_img10.png)


## Tree column/ Expander column 

The position of the expander column which acts as tree column, can be changed using the [`treeColumnIndex`](/api/js/ejtreegrid#members:treecolumnindex) property.

Following code example shows how to change the position of the expander column.

{% highlight js %}

    $("#TreeGridContainer").ejTreeGrid({
        //...
        treeColumnIndex: 2,
    });

{% endhighlight %}

The tree column index can be also be changed at run-time by using the [`columnIndex`](https://help.syncfusion.com/api/js/ejtreegrid#methods:columnindex "columnIndex")

## Visibility

Columns can be hidden on loading by setting the [`visible`](/api/js/ejtreegrid#members:columns-visible "columns.visible") property as false.

Following code example explains how to hide the fourth column.

{% highlight js %}

    $(function () {
        $("#TreeGridContainer").ejTreeGrid({
            //...
            columns: [
                { field: "taskID", headerText: "Task Id", width: "45" },
                { field: "taskName", headerText: "Task Name" },
                { field: "startDate", headerText: "Start Date" },
                { field: "endDate", headerText: "End Date", visible: false },
                { field: "progress", headerText: "Progress" }
            ]
        })
    });
        
{% endhighlight %}

![](/js/TreeGrid/Columns_images/Columns_img6.png)

## Read-only

A column can be made read-only by setting the [`allowEditing`](/api/js/ejtreegrid#members:columns-allowediting "columns.allowEditing") property as false.

N>
By setting columns.allowEditing as false that specific column alone is made as read only, and by setting the editSettings.allowEditing as false the entire TreeGrid is made read-only.

The below code snippet demonstrates this.

{% highlight js %}

    $(function () {
        $("#TreeGridContainer").ejTreeGrid({
            //...
            columns: [
                { field: "taskID", headerText: "Task Id"},
                { field: "taskName", headerText: "Task Name",allowEditing: false },
                { field: "startDate", headerText: "Start Date"},
                { field: "endDate", headerText: "End Date" }
            ]
        })
    });

{% endhighlight %}

## Validation Rules

At some occasions, we will need to validate the data before updating it to the database. In TreeGrid it is possible to validate the data while performing adding and editing actions. The validation rules must be provided in the column definition using [`validationRules`](/api/js/ejtreegrid#members:columns-validationrules "columns.validationRules") property. TreeGrid has built-in support for the below validation rules.

* **maxlength** – Makes the value require a given maximum text length.
* **minlength** – Makes the value require a given minimum text length.
* **required** – Makes the value required. 
* **number** – Makes the value require a decimal number.
* **range** – Makes the value require a given value range.

The below code example explains defining the validation rules for the column.

{% highlight js %}

 $("#TreeGridContainer").ejTreeGrid({
            //...
            columns: [{
                    field: "taskID",
                    headerText: "Task Id",
                    validationRules: {
                        number: true,
                        required: true
                    }
                },
                {
                    field: "taskName",
                    headerText: "Task Name",
                    allowEditing: false,
                    validationRules: {
                        maxlength: 5,
                        minlength: 2
                    }
                },
                {
                    field: "progress",
                    headerText: "Progress",
                    validationRules: {
                        range: [0, 100]
                    }
                },

                //...
            ]
        });

{% endhighlight %}

Custom validation error messages can also be defined in the column object. The below code example explains defining the custom error message. 

{% highlight js %}

        $("#TreeGridContainer").ejTreeGrid({
            //...
            columns: [{
                field: "taskID",
                headerText: "Task Id",
                validationRules: {
                    number: true,
                    required: true,
                    messages: {
                        "required": "This field should not left blank"
                    }
                }
            }, ]
        });

{% endhighlight %}

### Custom Validation rules
Apart by the in-built validation rules, any custom validation rules can also be defined for the column. The below code example explains defining custom validation rule for a column.

{% highlight js %}

   // Custom validation rule definition
   $.validator.addMethod("customCompare", function(value, element, params) {
       return element.value > params[0] && element.value < params[1]
   }, "progress value must be between 0 and 100");


   $("#TreeGridContainer").ejTreeGrid({
       //...
       columns: [{
           field: "progress",
           headerText: "Progress",
           validationRules: {
               customCompare: [0, 100]
           }
       }]
   })

{% endhighlight %}

The below image displays the TreeGrid with validation rule applied for a date column.
![](/js/TreeGrid/Columns_images/Columns_img7.png)

## Column Reorder
Column reorder is used to change the order of the column. In ejTreeGrid, [`allowColumnReordering`](/api/js/ejtreegrid#members:allowcolumnreordering) property is used to enable the column re-order, default value of this property is false.

Following code example explains how to enable column reorder in tree grid

{% highlight js %}

    $(function () {
        $("#TreeGridContainer").ejTreeGrid({
            //...
            allowColumnReordering : true,
            //...
        })
    });
        
{% endhighlight %}

![](/js/TreeGrid/Columns_images/Columns_img11.png)

The above screenshot shows the column reorder in tree grid.
{:.caption}

The TreeGrid columns can also be reordered using the [`reorderColumn`](https://help.syncfusion.com/api/js/ejtreegrid#methods:reordercolumn "reorderColumn") method, where the column field name and the target index should be passed as the method parameters.

### Customize the column reorder action

In TreeGrid, [`columnDragStart`](https://help.syncfusion.com/api/js/ejtreegrid#events:columndragstart), [`columnDrag`](https://help.syncfusion.com/api/js/ejtreegrid#events:columndrag) and [`columnDrop`](https://help.syncfusion.com/api/js/ejtreegrid#events:columndrop) events are triggered on column reorder action. Using this event we can prevent the column reorder for specific column.

The below code example shows how to prevent column reorder in TreeGrid.

{% highlight js %}

    $(function () {
        $("#TreeGridContainer").ejTreeGrid({
            //...
            allowColumnReordering : true,
            columnDragStart : function(args)
            {
                if (args.draggedColumn.field == "taskName")
                    args.cancel = true;
            },
            //...
        })
    });
        
{% endhighlight %}

## Text Alignment
In ejTreeGrid, it is possible to align both content and header text of particular column using the [`textAlign`](/api/js/ejtreegrid#members:columns-textalign "columns.textAlign") and [`headerTextAlign`](/api/js/ejtreegrid#members:columns-headertextalign "columns.headerTextAlign") property of columns.
There are four possible ways to align content and header text of column, they are

1. Left
2. Right
3. Center
4. Justify

N> 1. The textAlign property will affect both content and header text of the grid, when headerTextAlign is not set in column definition.

Following code example explains how to set text alignment for content and header text in tree grid

{% highlight js %}

    $(function () {
        $("#TreeGridContainer").ejTreeGrid({
            //...
            columns: [
                { field: "taskID", headerText: "Task Id"},
                { field: "taskName", headerText: "Task Name" },
                { field: "startDate", headerText: "Start Date",textAlign:"right",headerTextAlign:"left"},
                { field: "endDate", headerText: "End Date",textAlign:"center" },
                { field: "duration", headerText: "Duration" }
            ]
        })
    });

{% endhighlight %}

![](/js/TreeGrid/Columns_images/Columns_img12.png)

The above screenshot shows tree grid render with text alignment and header text alignment.
{:.caption}

### Customize the column at initial load
In TreeGrid, it is possible to customize the column at load time using [`load`](https://help.syncfusion.com/api/js/ejtreegrid#events:load) event.

The following code examples shows how to customize the column at load time

{% highlight js %}

    $(function () {
        $("#TreeGridContainer").ejTreeGrid({
            //...
            columns: [
                { field: "taskID", headerText: "Task Id"},
                { field: "taskName", headerText: "Task Name" },
                { field: "startDate", headerText: "Start Date"},
                { field: "endDate", headerText: "End Date" },
                { field: "duration", headerText: "Duration" }
            ],
            load:function(args)
            {
                var columns = args.model.columns;
                columns[0].isFrozen = true;
                columns[3].textAlign = "center";
                columns[4].visible = false;
                
            }
        })
    });

{% endhighlight %}

![](/js/TreeGrid/Columns_images/Columns_img20.png)

The above screen shot shows tree grid render with column customization

## Column object

The column object which consists the list of columns available in TreeGrid can be retrieved using the [`getColumnByHeaderText`](https://help.syncfusion.com/api/js/ejtreegrid#methods:getcolumnbyheadertext "getColumnByHeaderText") and [`getColumnByField`](https://help.syncfusion.com/api/js/ejtreegrid#methods:getcolumnbyfield "getColumnByField") methods.In the method `getColumnByHeaderText` the header text defined for the column should be passed as the method parameter while in the method `getColumnByField` the column field name should be passed as method parameter.

To fetch the column index using the column field name, the method [`getColumnIndexByField`](https://help.syncfusion.com/api/js/ejtreegrid#methods:getcolumnindexbyfield "getColumnIndexByField") should be called with field name as parameter. And to retrieve the datasource field name assigned to a column by using the column header text the method [`getFieldNameByHeaderText`](https://help.syncfusion.com/api/js/ejtreegrid#methods:getfieldnamebyheadertext "getFieldNameByHeaderText") should be called.
