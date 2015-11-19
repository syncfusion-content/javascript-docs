---
title: Schedule - Template
description: Customize Scheduler with various available template options
platform: js
control: schedule
documentation: ug
keywords: appointment template, template, cell template, resource header 
---
# Template

Template is applicable to all the below specified elements of the Scheduler,

* Appointments
* Resource header
* Priority field
* Date and time columns in Agenda view
* Tooltip

## Appointment Template


The template design that applies on for the Scheduler appointments. The field names that are mapped from the dataSource to the appropriate field properties within the [appointmentSettings](/js/api/ejschedule#members:appointmentsettings) can be accessed within the template.

Apart from the dataSource field names, the template can also access the current view of the Scheduler using the name **View** – which can contain either of the following values in lowercase. 

* day
* week
* workweek
* agenda
* month
* customview

It is controlled by an API named [appointmentTemplateId](/js/api/ejschedule#members:appointmenttemplateid) which accepts the id value of the template design block preceded by a symbol **#**.

Usually, the appointments are displayed with its **Subject** and **Start/End time** on the Scheduler. If suppose, the subject needs to be accompanied with location text, it can be done with the following code example.

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="Schedule1"></div>

<script id="apptemplate" type="text/x-jsrender">
	{{if View !== "agenda"}}
		<div style="height:100%; background-color:orange; margin-left: 5px;">
			<div style="margin-left: 2px;">{{:Subject}}</div>
			<div style="margin-left: 2px;">{{:Location}}</div>
		</div>
	{{else}}
		<div>{{:Subject}}, {{:Location}}</div>
	{{/if}}
</script>

<script type="text/javascript">
$(function() {
    $("#Schedule1").ejSchedule({
        currentDate: new Date(2015, 11, 2),
        appointmentTemplateId: "#apptemplate",
        appointmentSettings: {
            dataSource: [{
                Id: 100,
                Subject: "Wild Discovery",
                StartTime: new Date(2015, 11, 2, 9, 00),
                EndTime: new Date(2015, 11, 2, 10, 30),
                Location: "CHINA"
            }]
        }
    });
});	
</script>

{% endhighlight %}

## Resource Header Template

The template structure that applies on the resource headers of the Scheduler. By default, only the resource names will be displayed on the resource header bar. Also, the way of rendering resource headers on the Scheduler is comparatively different for both vertical and horizontal scheduler views. 

The field names that are mapped from the dataSource to the appropriate field properties within the **resourceSettings** can be accessed within the resource header template.

### Resource Header Template in Vertical View

To customize the resource header with some additional images or other customizations in **vertical** **Scheduler** **View** – refer the below code example.

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="Schedule1"></div>

<script id="resTemplate" type="text/x-jsrender">
	<div style="height:100%">
		<div style="width:15px;height:15px;margin-left:275px;margin-top:2px;float:left;background:{{:ResourceColor}};"></div><div style="float:left;margin-left:5px;">{{:ResourceText}}</div> 
	</div>
</script>

<script type="text/javascript">
$(function() {
    $("#Schedule1").ejSchedule({
        width: "100%",
        currentDate: new Date(2015, 04, 05),
        resourceHeaderTemplateId: "#resTemplate",
        group: {
            resources: ["Rooms"]
        },
        resources: [{
            field: "roomId",
            title: "Room",
            name: "Rooms",
            allowMultiple: false,
            resourceSettings: {
                dataSource: [{
                    ResourceText: "ROOM1",
                    id: 1,
                    ResourceColor: "orange"
                }, {
                    ResourceText: "ROOM2",
                    id: 2,
                    ResourceColor: "#56ca85"
                }],
                text: "ResourceText",
                id: "id",
                color: "ResourceColor"
            }
        }],
        appointmentSettings: {
            resourceFields: "roomId",
            dataSource: [{
                Id: 101,
                Subject: "Talk with Nature",
                StartTime: new Date(2015, 11, 5, 10, 00),
                EndTime: new Date(2015, 11, 5, 11, 00),
                roomId: 2
            }]
        }
    });
});	
</script>

{% endhighlight %}

### Resource Header Template in Horizontal View

To perform the above specified same customization in **horizontal** **Scheduler** **view**, the template structure varies a little bit as depicted below.

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="Schedule1"></div>

<script id="resTemplate" type="text/x-jsrender">
	<div style="height:100%">
		<div style="width:15px;height:15px;margin-right:5px;margin-top:2px;float:left;background:{{:ResColor}};"></div><div>{{:ResText}}</div> 
	</div>
</script>

<script type="text/javascript">
$(function() {
    $("#Schedule1").ejSchedule({
        width: "100%",
        height: "500px",
        currentDate: new Date(2015, 04, 05),
        orientation: "horizontal",
        resourceHeaderTemplateId: "#resTemplate",
        group: {
            resources: ["Rooms"]
        },
        resources: [{
            field: "roomId",
            title: "Room",
            name: "Rooms",
            allowMultiple: false,
            resourceSettings: {
                dataSource: [{
                    ResText: "ROOM1",
                    id: 1,
                    ResColor: "orange"
                }, {
                    ResText: "ROOM2",
                    id: 2,
                    ResColor: "#56ca85"
                }],
                text: "ResText",
                id: "id",
                color: "ResColor"
            }
        }],
        appointmentSettings: {
            resourceFields: "roomId",
            dataSource: [{
                Id: 101,
                Subject: "Talk with Nature",
                StartTime: new Date(2015, 11, 5, 10, 00),
                EndTime: new Date(2015, 11, 5, 11, 00),
                roomId: 2
            }]
        }
    });
});	
</script>

{% endhighlight %}

N> In horizontal Scheduler, the header template makes use of an additional field namely **classname** which holds either **e-parentnode** or **e-childnode** value. The field **classname** can be used in the application scenario to check for the parent or child header node. You can apply the different template customization accordingly based on it.

## Priority Settings Template

The template design which can be applied to the content of the priority field in the appointment window. By default, the appropriate icons are displayed for each priority options such as **None**, **High**, **Medium** and **Low**. 

When template is applied for the [prioritySettings](/js/api/ejschedule#members:prioritysettings), these default icons will be replaced by the custom icons or styles defined newly. The following code example depicts the way to enable the priority settings and to define the new custom styles to replace the default icons in the Priority field.

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="Schedule1"></div>

<style type="text/css">
	.critical,
	.ultracritical,
	.none {
		height: 13px;
		width: 13px;
		float: left;
		margin-right: 4px;
		background-repeat: no-repeat;
		background-size: 60px;
		padding: 1px;
		margin-top: 2px;
	}

	.critical {
		background-color: orange;
		background-position: -13px;
	}

	.ultracritical {
		background-color: #56ca85;
		background-position: -59px;
	}

</style>

<script type="text/javascript">
$(function() {
    $("#Schedule1").ejSchedule({
        currentDate: new Date(2015, 11, 2),
        prioritySettings: {
            enable: true,
            template: "<div class='${value}'></div>",
            dataSource: [{
                text: "None",
                id: 1,
                value: "none"
            }, {
                text: "Critical",
                id: 2,
                value: "critical"
            }, {
                text: "Ultra Critical",
                id: 3,
                value: "ultracritical"
            }]
        },
        appointmentSettings: {
            priority: "Priority",
            dataSource: [{
                Id: 100,
                Subject: "Wild Discovery",
                StartTime: new Date(2015, 11, 2, 9, 00),
                EndTime: new Date(2015, 11, 2, 10, 30),
                Location: "CHINA",
                Priority: "critical"
            }]
        }
    });
});	
</script>

{% endhighlight %}

The custom style class names defined for the priority template should be same as that of the values defined for each priority option within the dataSource, so that it applies properly.

N> Additionally, the priority field within the [appointmentSettings](/js/api/ejschedule#members:appointmentsettings) should be defined with appropriate dataSource field name. When an appointment is assigned with a priority value, the custom style/icon defined for that priority option will get applied over that appointment.

## Tooltip Template

The tooltip can be applied with the customized template design. Currently the tooltip support is provided only for the appointments and the default tooltip displays the Subject and duration on hovering across the appointments. 

By making use of template feature with tooltip, all the field names that are mapped from the dataSource to the appropriate field properties within the **appointmentSettings** can be accessed.

To define the template option for tooltip, the [tooltipSettings](/js/api/ejschedule#members:tooltipsettings) must be enabled first. The following code example depicts the way to add the tooltip template.

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="Schedule1"></div>

<script id="tooltipTemplate" type="text/x-jsrender">
	<div style="width:145px">
		<div style="padding-top:3px;">
			<div style="float:left; font:13px Segoe UI; font-weight:bold;">Subject&nbsp;&nbsp;:&nbsp;</div>
			<div style="padding-top:2px; font:12px Segoe UI SemiBold;">{{:Subject}}</div>
		</div>
		<div style="padding-top:3px">
			<div style="float:left; font:13px Segoe UI; font-weight:bold;">Location:&nbsp;</div>
			<div style="padding-top:2px; font:12px Segoe UI SemiBold;">{{:Location}}</div>
		</div>
	</div>
</script>

<script type="text/javascript">
$(function() {
    $("#Schedule1").ejSchedule({
        currentDate: new Date(2015, 11, 2),
        tooltipSettings: {
            enable: true,
            template: "#tooltipTemplate"
        },
        appointmentSettings: {
            dataSource: [{
                Id: 100,
                Subject: "Wild Discovery",
                StartTime: new Date(2015, 11, 2, 9, 00),
                EndTime: new Date(2015, 11, 2, 10, 30),
                Location: "CHINA"
            }]
        }
    });
});	
</script>

{% endhighlight %}

## Agenda View Templates

Agenda View provides two separate templates – one for date column and another for time column. These templates allows the customization of the content of both the date and time columns. Apart from this, the event column can also be customized through the existing API named [appointmentTemplateId](/js/api/ejschedule#members:appointmenttemplateid).

The following code snippet shows how to customize the content of the date, time and event column.

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="Schedule1"></div>

// Template for date column
<script id="datetemplate" type="text/x-jsrender">
	<div style="height:100%">
		<div>
			<div>{{:~dateDisplay(StartTime)}}</div>
		</div>
	</div>
</script>

// Template for time column
<script id="timetemplate" type="text/x-jsrender">
	<div style="height:100%">
		<div>
			<div>{{:~timeDisplay(StartTime)}}</div>
		</div>
	</div>
</script>

// Template for appointment which applies for event column in agenda view.
<script id="apptemplate" type="text/x-jsrender">
	{{if View !== "agenda"}}
		<div style="height:100%; background-color:orange; margin-left: 5px;">
			<div style="margin-left: 2px;">{{:Subject}}</div>
			<div style="margin-left: 2px;">{{:Location}}</div>
		</div>
	{{else}}
		<div>{{:Subject}}, {{:Location}}</div>
	{{/if}}
</script>

<script type="text/javascript">
function _getDate(date) {
    var dateCol = new Date(date);
    return dateCol.toDateString();
}

function _getTime(date) {
    var time = new Date(date);
    return time.toLocaleTimeString();
}

//Here, used the helper function to get the date and time value part from the StartTime.
$.views.helpers({
    dateDisplay: _getDate,
    timeDisplay: _getTime
});

$(function() {
    $("#Schedule1").ejSchedule({
        currentDate: new Date(2015, 11, 2),
        appointmentTemplateId: "#apptemplate",
        agendaViewSettings: {
            dateColumnTemplateId: "#datetemplate",
            timeColumnTemplateId: "#timetemplate"
        },
        appointmentSettings: {
            dataSource: [{
                Id: 100,
                Subject: "Wild Discovery",
                StartTime: new Date(2015, 11, 2, 9, 00),
                EndTime: new Date(2015, 11, 2, 10, 30),
                Location: "CHINA"
            }]
        }
    });
});	
</script>

{% endhighlight %}

