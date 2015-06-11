---
layout: post
title: Template
description: template
platform: js
control: Schedule
documentation: ug
---

# Template

## Appointment Template

* The appointments are provided with rich template support, so that the customizations are done easily. You can add the appointment template to the **Schedule** control as follows.


{% highlight js %}

**[JavaScript]**
<div id="Schedule1"> </div>
<script>
$(function () {
var dManager = ej.DataManager(window.Default).executeLocal(ej.Query().take(10));

// the below function selects the images to be displayed on the appointments based on the day of the appointment’s startTime.

**// Note**: The below used images should be present in a separate images folder, so that it will be referred properly.

function _getImages(date) {
switch (new Date(date).getDay()) {
case 0:
return "<img src='../images/schedule/cake.png'/>"
break;
case 1:
return "<img src='../images/schedule/basketball.png'/>"
break;
case 2:
return "<img src='../images/schedule/rugby.png'/>"
break;
case 3:
return "<img src='../images/schedule/guitar.png'/>"
break;
case 4:
return "<img src='../images/schedule/music.png'/>"
break;
case 5:
return "<img src='../images/schedule/doctor.png'/>"
break;
case 6:
return "<img src='../images/schedule/beach.png'/>"
break;
}
}
$.views.helpers({ format: _getImages });


$("#Schedule1").ejSchedule({
// specify the template id
**appointmentTemplateId: "#apptemplate",**
currentDate: new Date (2014,4,5),
width: "100%",
height: "550px",
appointmentSettings: {
dataSource: dManager,
id: "Id",
subject: "Subject",
startTime: "StartTime",
endTime: "EndTime",
allDay: "AllDay",
recurrence: "Recurrence",
recurrenceRule: "RecurrenceRule"
}
});
});
</script>

// appointment template definition
**<script id="apptemplate" type="text/x-jsrender">**
**<div style="height:100%">**
**<div style='float:left; width:50px;'>**
**{{:~format(StartTime)}}**
**</div>**
**<div>**
**<div>{{:Subject}}</div>**
**</div>**
**</div>**
**</script>**




{% endhighlight %}



* The output for the above code is as follows that displays the appointment with the template defined for it.

![](Template_images/Template_img1.png)
{:.image }


{:.caption }


___Figure_ _82__:____schedule with_ _template._



## Resource Header Template

* The resources are provided with rich template support, so that the customizations are done easily. You can add the resource header template to the **Schedule** control as follows.



{% highlight js %}

**[JavaScript]**

<div id="Schedule1"> </div>
<script>
$(function () {
var dManager = ej.DataManager(window.ResourcesData).executeLocal(ej.Query().take(10));
$("#Schedule1").ejSchedule({
width: "100%",
height: "525px",
// specify the template id
resourceHeaderTemplateId: "#resourceHeaderTemplateId",
currentView: ej.Schedule.CurrentView.Workweek,
// Groups the resources listed out in the below collection
**group: {**
**resources: ["Rooms"]**
**},**
// resource data collection
**resources: [**
**{**
**field: "roomId",**
**title: "Room",**
**name: "Rooms",**
// disables the multiple selection of resources in the appointment window.
**allowMultiple: false,**
**resourceSettings: { dataSource: [**
**{ text: "Room1", id: 1, color: "#f8a398" },**
**{ text: "Room2", id: 2, color: "#56ca85"}],**
**text: "text", id: "id", color: "color"**
**}**
**}],**
appointmentSettings: {
dataSource: dManager,
id: "Id",
subject: "Subject",
startTime: "StartTime",
endTime: "EndTime",
allDay: "AllDay",
recurrence: "Recurrence",
recurrenceRule: "RecurrenceRule",
// bind the resource id fields collection of each level
**resourceFields: "roomId"**

}
});
});
// The appointment data along with resource data to be passed to the dataSource are as follows,

window.ResourcesData = [{
Id: 100,
Subject: "Bering Sea Gold",
StartTime: new Date().setHours(9, 0),
EndTime: new Date().setHours(10, 30),
AllDay: false,
Recurrence: true,
RecurrenceRule: "FREQ=DAILY;INTERVAL=2;COUNT=10",
roomId: 2
}, {
Id: 101,
Subject: "Hello Sea Gold",
StartTime: new Date().setHours(4, 0),
EndTime: new Date().setHours(5, 0),
AllDay: false,
Recurrence: false,
roomId: 2
}, {
Id: 105,
Subject: "Daily Planet",
StartTime: new Date(new Date().getTime() + 86400 * 1000 * 1).setHours(1, 0),
EndTime: new Date(new Date().getTime() + 86400 * 1000 * 1).setHours(2, 0),
AllDay: false,
Recurrence: false,
roomId: 1
}, {
Id: 106,
Subject: "Alaska: The Last Frontier",
StartTime: new Date(new Date().getTime() + 86400 * 1000 * 1).setHours(4, 0),
EndTime: new Date(new Date().getTime() + 86400 * 1000 * 2).setHours(5, 0),
AllDay: false,
Recurrence: false,
roomId: 1
}, {
Id: 109,
Subject: "MayDay",
StartTime: new Date(new Date().getTime() + 86400 * 1000 * -2).setHours(6, 30),
EndTime: new Date(new Date().getTime() + 86400 * 1000 * -2).setHours(7, 30),
AllDay: false,
Recurrence: false,
roomId: 2
}];
</script>
// resourceheader template definition
<script type="text/x-jsrender" id="resourceHeaderTemplateId">
<img style="width: 40px; height: 40px" src=".../images/schedule/{{:id}}.png" alt="{{:id}}" />  
</script>


{% endhighlight %}



{% highlight text %}

> _**Important: The above used images should be present in a separate images folder, so that it will be referred properly.The images name should be saved with id as same as given in the resourceSettings inorder to set unqiue images to all resources.**_


{% endhighlight %}



* The output for the above code which displays the resource with the template defined for it is given below.



![C:/Users/karthigeyan/Desktop/a.png](Template_images/Template_img2.png)
{:.image }


{:.caption }




























