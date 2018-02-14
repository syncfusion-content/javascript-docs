---
layout: post
title: Customization
description: Customization
platform: Js
control: Gantt
documentation: ug
api: /api/js/ejgantt
---
# Customizations 

Gantt provides support for the following UI customizations,

* Taskbar template
* Task label template
* Tooltip template

## Taskbar template

You can design your own taskbars to view the tasks in Gantt by using [`taskbarTemplate`](/api/js/ejgantt#members:taskbartemplate "taskbarTemplate") property. And it is possible to map the JsRender script or script element’s ID to this property. It is also possible to customize the parent taskbars and milestones with custom templates by using [`parentTaskbarTemplate`](/api/js/ejgantt#members:parenttaskbartemplate "parentTaskbarTemplate") and [`milestoneTemplate`](/api/js/ejgantt#members:milestonetemplate "milestoneTemplate") properties. 

The following code example shows how to define template for taskbars in Gantt. 

{% highlight html %}
<div id="GanttContainer" style="height:450px;width:100%;" />
{% endhighlight %}

{% highlight javascript %}
<script type="text/x-jsrender" id="taskbarTemplate">

    <div class="e-gantt-template-taskbar bg-color">

        <div>

            //…

        </div>

        <div class="e-gantt-template-progressbar">

        </div>

    </div>

</script>

<script type="text/x-jsrender" id="parentTaskbarTemplate">

    <div class="e-gantt-template-taskbar">

        //…

        <div class="e-gantt-template-progressbar">

        </div>

    </div>

</script>

<script type="text/x-jsrender" id="milestoneTemplate">

    <div class="e-gantt-template-milestone" style="background-color:transparent;">

        <div class="e-gantt-milestone milestone-top"></div>

        <div class="e-gantt-milestone milestone-bottom"></div>

    </div>

</script>

<script>
    $(function() {

        $("#GanttContainer").ejGantt({

            //…

            taskbarTemplate: "#taskbarTemplate",

            parentTaskbarTemplate: "#parentTaskbarTemplate",

            milestoneTemplate: "#milestoneTemplate",

        });

    });
</script>

{% endhighlight %}

The DOM structure and class names mentioned in the above code snippet is mandatory for providing the editing support in custom templates.

[Click](http://js.syncfusion.com/demos/web/#!/bootstrap/gantt/customizations/taskbartemplate) here to view the online demo sample for Taskbar templates in Gantt.

The following screenshot shows the template for taskbars in Gantt.

![](/js/Gantt/Customization_images/Customization_img1.png)

## Task label template

By default, task name will be displayed to the left and resource names will be displayed to the right of the taskbars as task labels. We can enable/disable this default task labels by using [`showTaskNames`](/api/js/ejgantt#members:showtasknames) and [`showResourceNames`](/api/js/ejgantt#members:showresourcenames) properties. But these task labels are customizable.

### Mapping data source fields as task labels

It is also possible to set any data source fields as task labels using [`rightTaskLabelMapping`](/api/js/ejgantt#members:righttasklabelmapping "rightTaskLabelMapping") and [`leftTaskLabelMapping`](/api/js/ejgantt#members:lefttasklabelmapping "leftTaskLabelMapping") properties.

The following code example explains how to set task name field as right label and task ID field as left label,

{% highlight javascript %}

    $(function() {

        $("#GanttContainer").ejGantt({

            //...

            rightTaskLabelMapping: "taskName",

            leftTaskLabelMapping: "taskID",

        });

    });

{% endhighlight %}

The following screenshot shows Gantt with task labels mapped with different data source fields

![](/js/Gantt/Customization_images/Customization_img4.png)

### Task label templates

It is possible to customize the task labels with templates, by using [`rightTaskLabelTemplate`](/api/js/ejgantt#members:righttasklabeltemplate "rightTaskLabelTemplate") and [`leftTaskLabelTemplate`](/api/js/ejgantt#members:lefttasklabeltemplate "leftTaskLabelTemplate") properties.

The following code example explains how to map custom templates to task labels.

{% highlight html %}
<div id="GanttContainer" style="width:100%;height:450px;" />
{% endhighlight %}

{% highlight javascript %}
<script id="rightLabelTemplate" type="text/x-jsrender">

    {{"{{"}}if #data['resourceNames']{{}}}}

    <div>

        {{"{{"}}for resourceInfo{{}}}}

        <img src="14.2.0.26/themes/web/content/images/gantt/{{"{{"}}:resourceName{{}}}}.png" height="30px" />

        <span style="margin-left:5px;">{{"{{"}}:resourceName{{}}}}</span> {{"{{"}}:~_getSeparator(#get("array").data.length,#index){{}}}} {{"{{"}}/for{{}}}}

    </div>

    {{/if}}

</script>

<script id="leftLabelTemplate" type="text/x-jsrender">

    <div style="padding-top:5px;">

        <span>{{"{{"}}:#data['taskName']{{}}}}  [{{"{{"}}:status{{}}}}%]</span>

    </div>

</script>

<script>
    $(function() {

        $("#GanttContainer").ejGantt({

            //...

            rightTaskLabelTemplate: "#rightLabelTemplate",

            leftTaskLabelTemplate: "#leftLabelTemplate",

        });

    });
</script>
{% endhighlight %}

You can find the online demo sample for task label templates in Gantt [here](http://js.syncfusion.com/demos/web/#!/bootstrap/gantt/customizations/tasklabeltemplate)

The following screenshot shows Gantt with task label templates.

![](/js/Gantt/Customization_images/Customization_img2.png)

## Tooltip template

### Taskbar tooltip

The default tooltip in Gantt can be customized by using the [`taskbarTooltipTemplateId`](/api/js/ejgantt#members:taskbartooltiptemplateid "taskbarTooltipTemplateId") property. We need to map the JsRender script element’s ID value to this property.

The following code example shows how to customize the tooltip.

{% highlight html %}
<div id="GanttContainer" style="width:100%;height:450px;" />
{% endhighlight %}

{% highlight javascript %}
<script type="text/x-jsrender" id="tooltipTemplate">

    <table>

       {{"{{"}}if #data['resourceNames']{{}}}}

        <tr>

            <td rowspan="3" style="padding:3px"><img src="14.2.0.26/themes/web/content/images/gantt/{{"{{"}}:#data['resourceNames']{{}}}}.png" height="40px" /></td>

            <td style="padding:3px"><b>Task done By:</b></td>

            <td style="padding:3px">{{"{{"}}:#data['resourceNames']{{}}}}</td>

        </tr>

        {{/if{{}}}}

        <tr>

            <td style="padding:3px"><b>Starts On:</b></td>

            <td style="padding:3px">{{"{{"}}:~_ganttDateFormatter("startDate"){{}}}}</td>

        </tr>

        <tr>

            <td style="padding:3px"><b>Ends On:</b></td>

            <td style="padding:3px">{{"{{"}}:~_ganttDateFormatter("endDate"){{}}}}</td>

        </tr>

    </table>

</script>

$(function () { $("#GanttContainer").ejGantt({ //… taskbarTooltipTemplateId: "tooltipTemplate",  });

</script>
{% endhighlight %}

The following screenshot shows Gantt with task tooltip customization.

![](/js/Gantt/Customization_images/Customization_img3.png)

### Dependency tooltip

The default dependency tooltip in Gantt can be customized by using [`predecessorTooltipTemplate`](/api/js/ejgantt#members:predecessortooltiptemplate "predecessorTooltipTemplate") property. We can map value to this property as  JsRender template script id with prefix of '#' or HTML elements in string format. The following code example shows how to use the [`predecessorTooltipTemplate`](/api/js/ejgantt#members:predecessortooltiptemplate "predecessorTooltipTemplate") property.

{% highlight javascript %}

<script type="text/javascript">
    $("#GanttContainer").ejGantt({
        //...
        enableTaskbarTooltip: true,
        predecessorTooltipTemplate: "#ToolTipTemplate",
    })

    $.views.helpers({
        _Type: getType,
        _Lag: getLag
    });

    function getType() {
        return this.data.linkText;
    }

    function getLag() {
        return this.data.offset + " " + this.data.offsetUnit;        
    }
</script>

<script id="ToolTipTemplate" type="text/x-jsrender">

    <table>
            <tr>
                <td><b>Type:</b></td>
                <td><i>{{:~_Type()}}</i></td>
            </tr>
            <tr>
                <td><b>Lag:</b></td>
                <td><i>{{:~_Lag()}}</i></td>
            </tr>
    </table>

</script>

{% endhighlight %}

The following screenshot show the output of above code example.
![](/js/Gantt/Customization_images/Customization_img8.png)

You can find the JS playground sample for dependency tooltip template [here](http://jsplayground.syncfusion.com/Sync_f5fvhwfi).

### Cell tooltip 

TreeGrid part tooltip can also be customized using [`cellTooltipTemplate`](/api/js/ejgantt#members:celltooltiptemplate) property. We need to map the script element or element id to this property. The following code explains how to customize the cell tooltip in Gantt.

{% highlight javascript %}
<script type="text/javascript">
    $("#GanttContainer").ejGantt({

        //...

        showGridCellTooltip: true,

        cellTooltipTemplate: "#CustomToolTip",

    })

    $.views.helpers({
        _TaskID: getTaskID,
        _TaskName: getTaskName
    });

    function getTaskID() {

        return this.data.record["taskId"];

    }

    function getTaskName() {

        return this.data.record["taskName"];

    }
</script>

<script id="CustomToolTip" type="text/x-jsrender">

    <table>

        <tr>

            <td>Id:</td>

            <td>{{"{{"}}:~_TaskID(){{}}}}</td>

        </tr>

        <tr>

            <td>Name:</td>

            <td>{{"{{"}}:~_TaskName(){{}}}}</td>

        </tr>

    </table>

</script>
{% endhighlight %}
![](/js/Gantt/Customization_images/Customization_img5.png)

You can find the online demo sample for tooltip templates for taskbars [here](http://js.syncfusion.com/demos/web/#!/bootstrap/gantt/customizations/tooltiptemplate)

### Taskbar Editing Tooltip

Editing tooltip is used to show the updated start date, end date, duration and progress values of a task while resizing, dragging and progress bar resizing actions. Currently two editing tooltips are available in Gantt.

* Taskbar editing tooltip
* Progress bar editing tooltip

We can customize the default taskbar editing tooltip and progress bar editing tooltip in Gantt.

#### Customize taskbar editing tooltip

Taskbar editing tooltip can be customized by using [`taskbarEditingTooltipTemplate`](/api/js/ejgantt#members:taskbareditingtooltiptemplate) and [`taskbarEditingTooltipTemplateId`](/api/js/ejgantt#members:taskbareditingtooltiptemplateid) properties. The below code example shows how to customize the taskbar editing tooltip in Gantt.

{% highlight javascript %}

<script id="taskbar_editing_tooltip_template" type="text/x-jsrender">
    <table>
        <tr>
            <td colspan="2" style="padding:3px;font-weight:bold;font-style:italic">{{:taskName}}</td>
        </tr>
        <tr>
            <td style="padding:3px;font-weight:bold">Start Date</td>
            <td style="padding:3px">{{:~getStartDate(#data)}}</td>
        </tr>
        <tr>
            <td style="padding:3px;font-weight:bold">End Date</td>
            <td style="padding:3px">{{:~getEndDate(#data)}}</td>
        </tr>
        <tr>
            <td style="padding:3px;font-weight:bold">Duration</td>
            <td style="padding:3px">{{:duration}} {{:durationUnit}}</td>
        </tr>
    </table>
</script>
<script>
    $.views.helpers({
            getStartDate: function () {
                return ej.format(this.data.startDate, "MM/dd/yyyy", "en-US");
            },
            getEndDate: function () {
                return ej.format(this.data.endDate, "MM/dd/yyyy", "en-US");
            }
        });

    $(function() {
        $("#GanttContainer").ejGantt({
            //...
            taskbarEditingTooltipTemplateId: "taskbar_editing_tooltip_template",
        });
    });
</script>
{% endhighlight %}

The below screenshot shows the output of above code example.
![](/js/Gantt/Customization_images/Customization_img6.png)

You can find the JS playground sample for this property [here](http://jsplayground.syncfusion.com/Sync_khndhguw).

#### Customize progress bar editing tooltip

Progress bar editing tooltip can be customized by using [`progressbarTooltipTemplate`](/api/js/ejgantt#members:progressbartooltiptemplate) and [`progressbarTooltipTemplateId`](/api/js/ejgantt#members:progressbartooltiptemplateid) properties. The below code example shows how to customize the progress bar editing tooltip in Gantt.

{% highlight javascript %}

<script id="progressbar_editing_tooltip_template" type="text/x-jsrender">
    <table>
        <tr>
            <td colspan="2" style="padding:3px;font-weight:bold;font-style:italic">{{:taskName}}</td>
        </tr>
        <tr>
            <td style="padding:3px;font-weight:bold">Task Status</td>
            <td style="padding:3px">{{:status}}%</td>
        </tr>
    </table>
</script>
<script>
    $(function() {
        $("#GanttContainer").ejGantt({
            //...
            progressbarTooltipTemplateId: "progressbar_editing_tooltip_template",
        });
    });
</script>
{% endhighlight %}

The below screenshot shows the output of above code example.
![](/js/Gantt/Customization_images/Customization_img7.png)

You can find the JS playground sample for this property [here](http://jsplayground.syncfusion.com/Sync_aakdzajo).
