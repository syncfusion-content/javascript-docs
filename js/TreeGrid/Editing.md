---
layout: post
title: Editing
description: editing
platform: js
control: TreeGrid
documentation: ug
---

# Editing

## Editing Modes

The TreeGrid control provides built-in support to add, insert and update the tasks. The following are the types of edit modes available in TreeGrid. 

* Cell Editing
* Row Editing
* Dialog Editing

### Cell Editing

Update the task details through cell editing by setting `editMode` as `cellEditing`.

The following code example shows you how to enable `cellEditing` in TreeGrid control.

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

Update the task details through row editing by setting editMode as rowEditing.

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

Set `editMode` as `dialogEditing` to edit/add record using a dialog box, which displays the fields associated with the records.

The following code example shows you how to enable `dialogEditing` in TreeGrid control.

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
To edit/add the records using dialog template form, set `editMode` as `dialogEditing` and specify the template id to `dialogEditorTemplateID` property of `editSettings`.

N> 1. `value` attribute is used to bind the corresponding field value while editing.
N> 2. `name` attribute is used to get the changed field values while saving the edited record.
N> 3.  `id` attribute must to be set in the format of ( treegrid control id + fieldname).

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

#### Public Method

You can open the add dialog box dynamically by using public method called `showAddDialog()`.

You can open the edit dialog box dynamically by using public method called `showEditDialog(index)` by passing the row index as an argument.

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