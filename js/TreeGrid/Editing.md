---
layout: post
title: Editing
description: editing
platform: js
control: TreeGrid
documentation: ug
api: /api/js/ejtreegrid
---

# Editing

## Editing Modes

The TreeGrid provides support to add, edit and delete the records and the following are the types of editing modes available. 

* Cell Editing
* Row Editing
* Dialog Editing

You can enable editing in TreeGrid by enabling the property [allowEditing](/api/js/ejtreegrid#members:editsettings-allowediting "editSettings.allowEditing").

### Cell Editing

Update the record through editing a cell by setting [editMode](/api/js/ejtreegrid#members:editsettings-editmode "editSettings.editMode") as the `cellEditing`.

The following code example shows you how to enable the `cellEditing` in TreeGrid control.

{% highlight js %}

    $("#TreeGridContainer").ejTreeGrid({
        //...
        editSettings: {
            allowEditing: true,
            editMode: "cellEditing"

        },
    });

{% endhighlight %}

The output of the TreeGrid with `cellEditing` is as follows.

![](/js/TreeGrid/Editing_images/cellEditing.png)

### Row Editing

It is possible to make the entire row to editable state and to update a record by setting [editMode](/api/js/ejtreegrid#members:editsettings-editmode "editSettings.editMode") as rowEditing.

The following code example shows you how to enable rowEditing in TreeGrid control.

{% highlight js %}

    $("#TreeGridContainer").ejTreeGrid({
        //...
        editSettings: {
            allowEditing: true,
            editMode: "rowEditing"

        },
    });

{% endhighlight %}

The following output is displayed as a result of the above code example.

![](/js/TreeGrid/Editing_images/rowEditing.png)

### Dialog Editing

Set the [editMode](/api/js/ejtreegrid#members:editsettings-editmode "editSettings.editMode") as dialogEditing to edit/add a record using dialog.

The following code example shows you how to enable the `dialogEditing` in TreeGrid control.

{% highlight js %}

    $("#TreeGridContainer").ejTreeGrid({
        //...
        editSettings: {
            allowEditing: true,
            editMode: "dialogEditing"

        },
    });

{% endhighlight %}

The output of the TreeGrid with `dialogEditing` is as follows.

![](/js/TreeGrid/Editing_images/dialogEditing.png)

#### Dialog Template

You can edit any of the fields pertaining to a single record of data and apply it to a template so that the same format is applied to all the other records that you may edit later.
Using this template support, you can edit/add the fields that are not bound to TreeGrid columns.
To edit/add the records using dialog template form, set `editMode` as `dialogEditing` and specify the template id to [dialogEditorTemplateID](/api/js/ejtreegrid#members:editsettings-dialogeditortemplateid "editSettings.dialogEditorTemplateID") property of `editSettings`.

N> 1. The `value` attribute is used to bind the corresponding field value while editing.
N> 2. The `name` attribute is used to get the changed field values while saving the edited record.
N> 3.  The `id` attribute must to be set in the format of ( treegrid control id + fieldname).

The following code example describes the above behavior.

{% highlight js %}

<script type="text/x-jsrender" id="template">
    <div>
        <b>Task Details</b>
        <table cellspacing="10" class="beta">
            <tr>
                <td style="text-align:right;padding: 10px;">
                    TaskID
                </td>
                <td style="text-align: left;padding: 10px;">
                    <input id="TreeGridContainertaskID" type="number" name="taskID" value="{{'{{'}}:taskID{{}}}}" disabled="disabled" class="e-field e-ejinputtext valid e-disable"/>
                </td>
                <td style="text-align: right;padding: 10px;">
                    TaskName
                </td>
                <td style="text-align: left;padding: 10px;">
                    <input id="TreeGridContainertaskName" name="taskName" value="{{'{{'}}:taskName{{}}}}" class="e-field e-ejinputtext valid"/>
                </td>
            </tr>
            <tr>
                <td style="text-align: right;padding: 10px;">
                    StartDate
                </td>
                <td style="text-align: left;padding: 10px;">
                    <input type="text" id="TreeGridContainerstartDate" name="startDate" value="{{'{{'}}:startDate{{}}}}" class="e-field e-ejinputtext valid" />
                </td>
                <td style="text-align: right;padding: 10px;">
                    EndDate
                </td>
                <td style="text-align: left;padding: 10px;">
                    <input id="TreeGridContainerendDate" type="text" name="endDate" value="{{'{{'}}:endDate{{}}}}" class="e-field e-ejinputtext valid"  />
                </td>
            </tr>
        </table>
    </div>
</script>

{% endhighlight %}


{% highlight js %}

    $("#TreeGridContainer").ejTreeGrid({
        //...
        editSettings: {
            allowEditing: true,
            editMode: "dialogEditing",
            dialogEditorTemplateID: "#template"

        },
    });

{% endhighlight %}

The following output is displayed as a result of the above code example.

![](/js/TreeGrid/Editing_images/dialogTemplate.png)

#### Using methods to open dialog

It is possible to open the add dialog dynamically with a custom using the method showAddDialog..

Similarly, open the Edit dialog dynamically using the method showEditDialog(index), with the index of the row to be edited as parameter.

{% highlight js %}
<script>
$("#add").click(function (args) {
    treegridObj = $("# TreeGridContainer ").data("ejTreeGrid");
    treegridObj.showAddDialog();
    })
$("#edit").click(function (args) {
    treegridObj = $("# TreeGridContainer ").data("ejTreeGrid ");
    treegridObj.showEditDialog(3);
    })
</script>
{% endhighlight %}

## Cell Edit Template

Edit template is used to create custom editor for editing the column values. It can be created by using the [editTemplate](/api/js/ejtreegrid#members:columns-edittemplate "columns.editTemplate") property of `columns`.

The following are the functions available for edit template.

* `create` - It is used to create the control at time of initialize.
* `read` - It is used to read the input value at time of save.
* `write` - It is used to assign the value to control at time of editing.

The following code example describes edit template behavior.

{% highlight js %}

<script>
    var autocompleteData = ["Planning", "Plan Timeline", "Plan Budget", "Allocate Resources", "Planning Complete"];
    $("#treegrid").ejTreeGrid({
        //...
        editSettings: {
            allowAdding: true,
            allowEditing: true,
            allowDeleting: true
        },
        columns: [{
            field: "taskName",
            headerText: "Task Name",
            editTemplate: {
                create: create,
                write: write,
                read: read,
            }
        }],
        //...
    });

    function create() {
        return "<input>";
    }

    function write(args) {
        args.element.ejAutocomplete({
            width: "100%",
            dataSource: autocompleteData,
            enableDistinct: true,
            value: args.rowData !== undefined ? args.rowData["taskName"] : ""
        });
    }

    function read(args) {
        args.ejAutocomplete('suggestionList').css('display', 'none');
        return args.ejAutocomplete("getValue");
    }
</script>

{% endhighlight %}

The output of the TreeGrid width editTemplate as follows.

![](/js/TreeGrid/Editing_images/editTemplate.png)

## Delete confirmation message

Delete confirmation message is used to get the confirmation from the user before delete the record. This confirmation message can be enabled by setting [showDeleteConfirmDialog](/api/js/ejtreegrid#members:editsettings-showdeleteconfirmdialog "editSettings.showDeleteConfirmDialog") property as `true`.

The following code snippet explains how to enable delete confirmation message in tree grid.

{% highlight js %}
$("#TreeGrid").ejTreeGrid({
    //...
    editSettings: {
        allowDeleting: true,
	    showDeleteConfirmDialog: true
    },
    //...
});

{% endhighlight %}

![](/js/TreeGrid/Editing_images/deleteConfirmation.png)

The above screen shot shows the appearance of delete confirmation message in treegrid.