---
layout: post
title: Editing
description: editing
platform: js
control: Gantt
documentation: ug
api: /api/js/ejgantt
---

# Editing

The Gantt control provides in-built support to add, insert and update the tasks. The following are the types of editing available in Gantt.

* Cell Editing
* Normal Editing
* Taskbar Editing
* Dependency Editing

## Cell Editing

### Initialize cell edit mode

Update the task details through grid cell editing by setting [`editMode`](/api/js/ejgantt#members:editsettings-editmode "editSettings.editMode") as `cellEditing`.

The following code example shows you how to enable the `cellEditing` in Gantt control.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        editSettings: {
            allowEditing: true,
            editMode: "cellEditing"
        }
    });

{% endhighlight %}

The output of Gantt with cellEditing is as follows.

![](/js/Gantt/Editing_images/Editing_img1.png)

### Save editing cell

Currently editing cell value can be saved by clicking the save toolbar icon or clicking on any other cell element in the grid and also editing cell can be saved by using [`saveEdit`](/api/js/ejgantt#methods:saveedit) method, using this method we can save the current editing cell dynamically on any action like external button click, please refer the following code example.

{% highlight javascript %}

    $("#save_button").click(function () {
        $("#GanttContainer").ejGantt("instance").saveEdit();
    });

{% endhighlight %}

### Cancel editing cell

Currently editing cell value can be restored with old value by using cancel toolbar icon or by pressing <kbd>Esc</kbd> key. And also this can be done by using [`cancelEdit`](/api/js/ejgantt#methods:canceledit) method on any other external actions like button click, please refer the following code example.

{% highlight javascript %}

    $("#cancel_button").click(function () {
        $("#GanttContainer").ejGantt("instance").cancelEdit();
    });

{% endhighlight %}

### Prevent Cell Editing

In cell editing action [`beginEdit`](/api/js/ejgantt#events:beginedit) and [`endEdit`](/api/js/ejgantt#events:endedit) events are triggered before and after the editing action.
Cell editing for particular column or specific cell can be prevented by using [`beginEdit`](/api/js/ejgantt#events:beginedit) event, please refer following code example for this.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        editSettings: {
            allowEditing: true,
            editMode: "cellEditing"
        },
        beginEdit: function (args) {
            if (args.columnIndex == 1)
                args.cancel = true;
        },
    });

{% endhighlight %}


## Normal Editing

### Initialize Normal edit mode

Update the task details through edit dialog by setting [`editMode`](/api/js/ejgantt#members:editsettings-editmode "editSettings.editMode") as `normal`.

The following code example shows you how to enable normal editing in Gantt control.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        editSettings: {
            allowEditing: true,
            editMode: "normal"
        }
    });

{% endhighlight %}

The following screenshot shows the output of `normal` editing.

![](/js/Gantt/Editing_images/Editing_img2.png)

### Define required fields in add/edit dialog

In Gantt we can define the editing fields available in add and edit dialogs by using [`addDialogFields`](/api/js/ejgantt#members:adddialogfields) and [`editDialogFields`](/api/js/ejgantt#members:editdialogfields) properties. Each editing fields are defined with [`field`](/api/js/ejgantt#members:editdialogfields-field "editDialogFields.field") and [`editType`](/api/js/ejgantt#members:editdialogfields-edittype "editDialogFields.editType") properties. The following code example shows how to define [`editDialogFields`](/api/js/ejgantt#members:editdialogfields) property.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        editSettings: {
            allowEditing: true,
            editMode: "normal"
        },
        editDialogFields: [
            { field: "taskID", editType: "stringedit" },
            { field: "taskName", editType: "stringedit" },
            { field: "startDate", editType: "datepicker" },
            { field: "endDate", editType: "datepicker" },
            { field: "duration", editType: "stringedit" },
        ],
    });

{% endhighlight %}

The following screenshot show the output of above code example.
![](/js/Gantt/Editing_images/Editing_img4.png)

N> Similarly we can define the required fields in add dialog with [`field`](/api/js/ejgantt#members:adddialogfields-field "addDialogFields.field") and [`editType`](/api/js/ejgantt#members:adddialogfields-edittype "addDialogFields.editType") properties.

### Add custom column fields in General tab

By default custom column fields are included in add/edit dialog's custom field tab but we can display this column field in General tab by setting [`displayInGeneralTab`](/api/js/ejgantt#members:editdialogfields-displayingeneraltab "editDialogFields.displayInGeneralTab") property as `true` in [`addDialogFields`](/api/js/ejgantt#members:adddialogfields) and [`editDialogFields`](/api/js/ejgantt#members:editdialogfields) properties. The following code example shows how to add custom column field in General tab of edit dialog.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        editSettings: {
            allowEditing: true,
            editMode: "normal"
        },
        editDialogFields: [
            { field: "taskID", editType: "stringedit" },
            { field: "taskName", editType: "stringedit" },
            { field: "startDate", editType: "datepicker" },
            { field: "endDate", editType: "datepicker" },
            { field: "duration", editType: "stringedit" },
            { field: "customField", editType: "stringedit", displayInGeneralTab: true }
        ],
        load: function (args) {
            var column = { field: "customField", mappingName: "customField", headerText: "Custom Field" };
                this.getColumns().push(column);
        }
    });

{% endhighlight %}

The following screenshot show the output of above code example.
![](/js/Gantt/Editing_images/Editing_img5.png)

N> Similarly we can include custom fields in add dialog's General tab by setting [`displayInGeneralTab`](/api/js/ejgantt#members:adddialogfields-displayingeneraltab "addDialogFields.displayInGeneralTab") as `true` in [`addDialogFields`](/api/js/ejgantt#members:adddialogfields) collection.

N> Default columns predecessors, resources and notes are displayed in separate tabs, we can't include this in General tab of add/edit dialog.

### Open add/edit dialog dynamically

Gantt add and edit dialogs can be opened dynamically by using [`openAddDialog`](/api/js/ejgantt#methods:openadddialog) and [`openEditDialog`](/api/js/ejgantt#methods:openeditdialog) methods. The following code example shows how to open add and dialog on separate button click actions.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        editSettings: {
            allowEditing: true,
            editMode: "normal"
        }
    });

    $("#openAddDialog").click(function(){
        $("#GanttContainer").ejGantt("instance").openAddDialog();
    });

    $("#openEditDialog").click(function(){
        $("#GanttContainer").ejGantt("instance").openEditDialog();
    });

{% endhighlight %}

N> We should select any one of the row in Gantt to open the edit dialog.

## Taskbar Editing

Update the task details by interactions such as resizing and dragging the taskbar. Taskbar editing can be enabled by setting [`allowGanttChartEditing`](/api/js/ejgantt#members:allowganttchartediting) as `true`. The following code example shows you how to enable taskbar resizing in Gantt control.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        allowGanttChartEditing: true
    });

{% endhighlight %}

You can also enable or disable the progress bar resizing by using the [`enableProgressbarResizing`](/api/js/ejgantt#members:enableprogressbarresizing). The following code example shows how to disable this property.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        enableProgressBarResizing: false,
    });

{% endhighlight %}

### Prevent taskbar editing for particular task

On taskbar edit action [`taskbarEditing`](/api/js/ejgantt#events:taskbarediting) and [`taskbarEdited`](/api/js/ejgantt#events:taskbaredited) event will be triggered. We can prevent the taskbar from editing by using [`taskbarEditing`](/api/js/ejgantt#events:taskbarediting) event and we can revert taskbar edit action by using [`taskbarEdited`](/api/js/ejgantt#events:taskbaredited) event. The following code example shows how to achieve this.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        allowGanttChartEditing: true,
        taskbarEditing: function (args) {
            if (args.rowData.taskId == 4) // We can't edit Task Id 4
                args.cancel = true;
        },
        taskbarEdited: function (args) { // We can edit task id 5 task but changes reverted on mouse up action
            if (args.data.taskId == 5)
                args.cancel = true;
        },
        
    });

{% endhighlight %}

You can find the JS playground sample for this [here](http://jsplayground.syncfusion.com/Sync_p3zjn5kw "Demo Link").

## Dependency Editing

In Gantt, we can add, edit, update the task dependencies by mouse interactions, edit dialog and public methods. The code example shows how to enable dependency editing in Gantt.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        dataSource: data,
        allowGanttChartEditing: true,
        predecessorMapping: "predecessor",
    });

{% endhighlight %}

### Add Dependency

Task dependency can be added by mouse interactions by connecting connector points in predecessor and successor tasks. The following screen shot shows the add dependency action.

![](/js/Gantt/Editing_images/Editing_img3.png)

### Edit Dependency

Task dependency value can be edited by using edit dialog and [`updateDependency`](/api/js/ejgantt#methods:updatedependency) method. Dependency edit dialog can be opened by double clicking on corresponding dependency line.

Client side [`actionBegin`](/api/js/ejgantt#events:actionbegin) event will be triggered twice with different `requestType` argument values while opening of dependency dialog. First time, event will be triggered with `requestType` argument values as `beforeDependencyEditDialogOpen`, in this event we can get the current editing dependency line information, next [`actionBegin`](/api/js/ejgantt#events:actionbegin) will be triggered with `requestType` argument value as `afterDependencyEditDialogOpen`, in this event we can get the information about current editing dependency line and editing elements in edit dialog. Using this event we can customize the dependency edit dialog elements.

{% highlight javascript %}

$("#GanttContainer").ejGantt({
    //...
   actionBegin: "actionBegin"
});

function actionBegin(args) {
    if(args.requestType == "beforeDependencyEditDialogOpen") {

    }
    else if(args.requestType == "afterDependencyEditDialogOpen") {

    }
}

{% endhighlight %}

The following screen shot shows the dependency edit dialog.
![](/js/Gantt/Editing_images/Predecessor_Editing_Dialog.png)

You can find the JS playground sample for dependency editing methods and events [here](http://jsplayground.syncfusion.com/Sync_5eyi0dgr).

### Delete Dependency

Task dependency can be deleted by using edit dialog and [`deleteDependency`](/api/js/ejgantt#methods:deletedependency) method. The following screen shot shows the dependency edit dialog with delete option.

![](/js/Gantt/Editing_images/Predecessor_Editing_Dialog.png)

[Click](http://js.syncfusion.com/demos/web/#!/bootstrap/gantt/editing) here to view the online demo sample for editing in Gantt.

## Update Gantt record value dynamically

Gantt record's value can be dynamically updated by using [`updateRecordByTaskId`](/api/js/ejgantt#methods:updaterecordbytaskid "updateRecordByTaskId(data)") or [`updateRecordByIndex`](/api/js/ejgantt#methods:updaterecordbyindex "updateRecordByIndex(index, data)") method. [`updateRecordByTaskId`](/api/js/ejgantt#methods:updaterecordbytaskid "updateRecordByTaskId(data)") method used to update the Gantt record by using it's task id value and [`updateRecordByIndex`](/api/js/ejgantt#methods:updaterecordbyindex "updateRecordByIndex(index, data)") method was used to update Gantt record value by row index value. We can invoke this method on any external button click action, the following code example shows how to use this methods.

{% highlight js %}

$("#GanttContainer").ejGantt({
    //...
});

$("#updateRecordByTaskId").click(function () {
    var ganttObj = $("#GanttContainer").ejGantt("instance"),
        data = {
                taskID: 4,
                taskName: "Updated by task id",
                startDate: new Date("02/10/2014"),
                endDate: new Date("02/14/2014"),
                duration: 5,
                progress: "80",
                resourceId: [2]
            };
    ganttObj.updateRecordByTaskId(data);
});

$("#updateRecordByRowIndex").click(function () {
    var ganttObj = $("#GanttContainer").ejGantt("instance"),
        data = {
                taskID: 5,
                taskName: "Updated by index value",
                startDate: new Date("02/10/2014"),
                endDate: new Date("02/14/2014"),
                duration: 3, progress: "100",
                predecessor: "4SS",
                resourceId: [2]
        };
    ganttObj.updateRecordByIndex(4, data);
});

{% endhighlight %}

You can find the JS playground sample for this [here](http://jsplayground.syncfusion.com/Sync_w5suulh5).

N> Using these methods we can't update the task id value, refer this [link](/js/gantt/how-to/update-task-id-value) to know about how to update the task id value.

## Delete confirmation message

Delete confirmation message is used to get the confirmation from the user before delete the record. This confirmation message can be enabled by setting [`showDeleteConfirmDialog`](/api/js/ejgantt#members:editsettings-showdeleteconfirmdialog "editSettings.showDeleteConfirmDialog") property as `true`.

The following code snippet explains how to enable delete confirmation message in Gantt.

{% highlight js %}

$("#GanttContainer").ejGantt({
     //...
    editSettings: {
        allowDeleting: true,
	    showDeleteConfirmDialog: true
    },
    //...
});


{% endhighlight %}

![](/js/Gantt/Editing_images/deleteConfirmation.png)

The above screen shot shows the appearance of delete confirmation message in Gantt.

## Task Indent

Task indent option in Gantt was enabled by setting [`allowIndent`](/api/js/ejgantt#members:editsettings-allowindent "editSettings.allowIndent") as `true`. Tasks can be indented by clicking on indent toolbar item or by using [`indentItem`](/api/js/ejgantt#methods:indentitem) method. We can invoke this method dynamically on any action like external button click. The below code example shows how to enable indent option in Gantt.

{% highlight js %}

$("#GanttContainer").ejGantt({
     //...
    editSettings: {
        allowIndent: true
    },
    toolbarSettings: {
        showToolbar: true,
        toolbarItems: [ej.Gantt.ToolbarItems.Add,
        //..
        ej.Gantt.ToolbarItems.Indent]
    },
    //...
});

$("#indentTask").click(function () {
    var ganttObj = $("#GanttContainer").ejGantt("instance");
    if (ganttObj.selectedRowIndex() != -1)
        ganttObj.indentItem();
});

{% endhighlight %}

The following screenshots shows the output of above code example.

![](/js/Gantt/Editing_images/Editing_img6.png)

Before Indent
{:.caption}

![](/js/Gantt/Editing_images/Editing_img7.png)

After Indent
{:.caption}

N> We should select any one of the row in Gantt to perform task indent action.

## Task Outdent

Task outdent option in Gantt was enabled by setting [`allowIndent`](/api/js/ejgantt#members:editsettings-allowindent "editSettings.allowIndent") as `true`. Tasks can be outdent by clicking on outdent toolbar item or by using [`outdentItem`](/api/js/ejgantt#methods:outdentitem) method. We can invoke this method dynamically on any action like external button click. The below code example shows how to enable outdent option in Gantt.

{% highlight js %}

$("#GanttContainer").ejGantt({
     //...
    editSettings: {
        allowIndent: true
    },
    toolbarSettings: {
        showToolbar: true,
        toolbarItems: [ej.Gantt.ToolbarItems.Add,
        //..
        ej.Gantt.ToolbarItems.Outdent]
    },
    //...
});

$("#outdentTask").click(function () {
    var ganttObj = $("#GanttContainer").ejGantt("instance");
    if (ganttObj.selectedRowIndex() != -1)
        ganttObj.outdentItem();
});

{% endhighlight %}

The following screenshots shows the output of above code example.

![](/js/Gantt/Editing_images/Editing_img6.png)

Before Outdent
{:.caption}

![](/js/Gantt/Editing_images/Editing_img8.png)

After Outdent
{:.caption}

N> We should select any one of the row in Gantt to perform task outdent action.

## Task Delete

Task delete option in Gantt was enabled by setting [`allowDeleting`](/api/js/ejgantt#members:editsettings-allowdeleting "editSettings.allowDeleting") as `true`. Tasks can be delete by clicking on delete toolbar item or by using [`deleteItem`](/api/js/ejgantt#methods:deleteitem) method. We can invoke this method dynamically on any action like external button click. The below code example shows how to enable delete option in Gantt.

{% highlight js %}

$("#GanttContainer").ejGantt({
     //...
    editSettings: {
        allowDeleting: true
    },
    toolbarSettings: {
        showToolbar: true,
        toolbarItems: [ej.Gantt.ToolbarItems.Add,
        //..
        ej.Gantt.ToolbarItems.Delete]
    },
    //...
});

$("#deleteTask").click(function () {
    var ganttObj = $("#GanttContainer").ejGantt("instance");
    if (ganttObj.selectedRowIndex() != -1)
        ganttObj.deleteItem();
});

{% endhighlight %}

The following screenshots shows the output of above code example.

![](/js/Gantt/Editing_images/Editing_img6.png)
Before Delete
{:.caption}

![](/js/Gantt/Editing_images/Editing_img9.png)
After Delete
{:.caption}

N> We should select any one of the row in Gantt to perform task delete action.

## Read-only Gantt

In Gantt, all editing options can be disabled by setting [`readOnly`](/api/js/ejgantt#members:readonly) property as `true`. The following code example shows how to make Gantt control as read-only.

{% highlight js %}

$("#GanttContainer").ejGantt({
    //...
    readOnly: true,
});

{% endhighlight %}
