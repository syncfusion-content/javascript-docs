---
title: Working with appointments
description: How to work with appointments with recurrence also
platform: js
control: schedule
documentation: ug
keywords: appointments, appointment, recurrence, recurring appoitnment, all day 
---
## Working with Appointments

An appointment represents a certain time interval in a schedule cell depicting a plan made for the specified time interval. 

### Appointment Types

The types of appointments available within Scheduler can be categorized as follows 

#### Normal 

Represents an appointment that is created for a certain time interval on a single or more number of days. If the normal appointment is created for more than 24 hours, then those longer appointments will be rendered on the all-day row.

**Note**: If the normal appointment is to be created for two days (say from November 25, 2015 – 11.00 PM to November 26, 2015 2.00 AM) but less than 24 hour time interval, then the appointment is split into two parts and will be displayed appropriately on both the days.

#### All-Day 

Represents an appointment that is created for an entire day such as holiday events. It renders separately in an All-day cell, a separate place for all-day appointments. In Timeline (horizontal) view, all-day appointment renders in the usual work cells, as no all-day cells are present in that view. 

**Note**: An all-day row is normally visible on the Scheduler, as the **[showAllDayRow](#_Show/Hide_All-Day_Row "")** property is set to true by default. 

#### Recurrence

Represents an appointment that is created for a certain time interval that occurs repeatedly in a daily, weekly, monthly or yearly basis at the same time interval based on the Recurrence rule. The other available options and validations that can be performed on recurrence appointments can be referred from [here](#_Recurrence_Options "").

### CRUD operation 

Appointments play a dynamic role within the Schedule control with which the users mostly interact. You can manipulate (add/edit/delete/drag/resize) the required appointments that reveals one of the main purpose of the Schedule control.

#### Add/Edit Appointments

The appointments can be added/edited in the Scheduler using any one of the following ways,

* Quick window
* Default appointment window
* [Context menu](#_Context_Menu "")
* Through programmatically
##### Quick Window


The Quick window usually pops out while single clicking on the Scheduler cells or appointments. It requires the user to enter the Subject to proceed with the appointment creation. It also includes an **Edit** **Appointment** option displayed at the bottom left corner – on selection which opens up the normal appointment window.

On single clicking the scheduler appointments, the pop-up that shows up contains the appointment information along with the other options that are listed below,

* Edit Appointment
* Edit Series (only for the recurrence appointments)
* Delete icon

The quick window option can be enabled/disabled by using **[showQuickWindow](http://help.syncfusion.com/js/api/ejschedule#members:showquickwindow "")** API, whereas its default value is set to **true**.

{% highlight html %}
<!-- HTML element will initialize as a ejSchedule -->

<div id="schedule"></div>

<script>

$("#schedule").ejSchedule({

//disables the quick window 

showQuickWindow: false,

currentDate: new Date(2015, 11, 7),

appointmentSettings: {

//Array of JSON data configure in dataSource

dataSource: [

{

Id: 1,

Subject: "Music Class",

StartTime: new Date("2015/11/7 06:00 AM"),

EndTime: new Date("2015/11/7 07:00 AM")

},

{

Id: 2,

Subject: "School",

StartTime: new Date("2015/11/7 9:00 AM"),

EndTime: new Date("2015/11/7 02:30 PM")

}]

}

});

</script>



{% endhighlight %}

**Note**: Select multiple cells either using mouse or keyboard access keys (shift + arrow keys) and press <enter> key, so that the quick window opens up for the selected date/time range.

Another way to disable the quick window option at dynamic time can be achieved through the **[cellClick](http://help.syncfusion.com/js/api/ejschedule#events:cellclick "")** and **[appointmentClick](http://help.syncfusion.com/js/api/ejschedule#events:appointmentclick "")** events. The below code example shows the way to disable the quick appointment window only while clicking on the cells, but displays for appointments.

{% highlight html %}
<!-- HTML element will initialize as a ejSchedule -->

<div id="schedule"></div>

<script>

$("#schedule").ejSchedule({

currentDate: new Date(2015, 11, 7),

showQuickWindow: true,

appointmentSettings: {

//Array of JSON data configure in dataSource

dataSource: [

{

Id: 1,

Subject: "Music Class",

StartTime: new Date("2015/11/7 06:00 AM"),

EndTime: new Date("2015/11/7 07:00 AM")

},

{

Id: 2,

Subject: "School",

StartTime: new Date("2015/11/7 9:00 AM"),

EndTime: new Date("2015/11/7 02:30 PM")

}]

},

cellClick: "onCellClick"

});

function onCellClick(args) {

args.cancel = true; // Prevents the display of quick window on clicking the cells.

}

</script>



{% endhighlight %}

##### Default Appointment Window

The default appointment window is availed with options like 

* Subject
* Start and End Time
* All-Day
* Time Zone (for both Start and End time)
* Repeat options
* Description

The other additional options available are listed below for which the appropriate API’s are needed to be configured to display these options on the appointment window.

* Location ([showLocationField](#_Show/Hide_Location_field ""))
* Priority ([prioritySettings](#_Priority ""))
* Categorize ([categorizeSettings](#_Categorization ""))
* [Resources](#_Resources "")    

The appointments can be created by double-clicking on the Scheduler cells across the required time slots, which makes the create Appointment window to pop-up. The start and end time will gets automatically populated, according to the time-slot selection. Clicking on the done button in an appointment window will create the appointment for the selected time cells.

**Note**: Select multiple cells both using mouse or keyboard access keys (shift + arrow keys) and press <Alt + N> key, so that the default appointment window opens up for the selected date/time range with the Start and End time fields automatically filled in.

To prevent the display of default appointment window on double clicking the Scheduler cells, either the **[appointmentWindowOpen](http://help.syncfusion.com/js/api/ejschedule#events:appointmentwindowopen "")** or **[cellDoubleClick](http://help.syncfusion.com/js/api/ejschedule#events:celldoubleclick "")** event can be used, within which the **args.cancel** needs to be set to true. This behaviour is depicted in the below code example.

{% highlight html %}


<div id="Schedule1"></div>

$(function () {

// defining Schedule control

$("#Schedule1").ejSchedule({

width: "100%",

height: "525px",

currentDate:new Date(2015,11,5),

appointmentSettings: {

dataSource: [{

Id: 101,

Subject: "Talk with Nature",

StartTime: new Date(2015, 11, 5, 10, 00),

EndTime: new Date(2015, 11, 5, 11, 00)

}]

},

appointmentWindowOpen: "onAppointmentWindowOpen"

});

});

function onAppointmentWindowOpen(args) {

args.cancel = true; // prevents the display of default appointment window

}





{% endhighlight %}


##### Through Programmatically

You can add/edit the appointments dynamically through the public method - **[saveAppointment](http://help.syncfusion.com/js/api/ejschedule#methods:saveappointment "")**. It accepts the JSON Object data (either a new or updated appointment object) as its argument.

{% highlight html %}
<body>

<button id="btnAdd" value="Add" onclick="addAppointment()">Add</button>

<!-- HTML element will initialize as a ejSchedule -->

<div id="schedule"></div>

<script>

$("#schedule").ejSchedule({

currentDate: new Date(2015, 11, 7),

appointmentSettings: {

//Array of JSON data configure in dataSource

dataSource: [

{

Id: 1,

Subject: "Music Class",

StartTime: new Date("2015/11/7 06:00 AM"),

EndTime: new Date("2015/11/7 07:00 AM")

},

{

Id: 2,

Subject: "School",

StartTime: new Date("2015/11/7 9:00 AM"),

EndTime: new Date("2015/11/7 02:30 PM")

}]

}

});

//addAppointment is a function, gets called on clicking the Add button

function addAppointment() {

//appointment details 

var appointment = {

Subject: "Gym",

StartTime: new Date("2015/11/7 03:30 AM"),

EndTime: new Date("2015/11/7 04:30 AM")

};

//create the schedule object 

var schObj = $("#schedule").data("ejSchedule");

//pass the JSON object in the public method 

schObj.saveAppointment(appointment);

}

</script>



{% endhighlight %}

#### Delete Appointments

The appointments can be deleted using either of the following ways,

* Selecting an appointment and clicking on the delete icon in the quick appointment window.
* Hovering the mouse over appointments and clicking on Inline delete option which is enabled by default for all the appointments.
* Selecting an appointment and pressing <**Delete**> key.
* [Through Programmatically](#_Through_Programmatically "").

A pop-up with a confirmation message will get displayed before deleting an appointment, which can be customized as mentioned [here](#_Localizing_Specific_Words "").

**For** **example**, to localize only the delete confirmation message in the delete window - 

{% highlight html %}
<script>

var deleteCustomizationMessage = {

// customize the confirmation message

DeleteConfirmation: "Do you want to delete this Event?",

// customize the delete window title

MouseOverDeleteTitle: "Delete Event",

// customize the recurrence delete window title

RecurrenceDeleteTitle: "Delete Repeat Event"

};

// Extend only the required changes to the original locale collection

$.extend(ej.Schedule.Locale["en-US"], deleteCustomizationMessage);

$(function () {

// defining Schedule control

$("#Schedule1").ejSchedule({

width: "100%",

height: "525px",

currentDate:new Date(2015,11,5),

appointmentSettings: {

dataSource: [{

Id: 101,

Subject: "Talk with Nature",

StartTime: new Date(2015, 11, 5, 10, 00),

EndTime: new Date(2015, 11, 5, 11, 00)

}]

}

});

});

</script>



{% endhighlight %}

**Note**: All these CRUD operations on appointments (add/edit/delete) can also be done through the default [context menu](#_Default_Menu_options "") options **Add** **Appointment**, **Edit** **Appointment** and **Delete** **Appointment** which is available, when context menu settings is enabled within Scheduler.

##### Through Programmatically

You can delete the appointments dynamically through the public method **[deleteAppointment](http://help.syncfusion.com/js/api/ejschedule#methods:deleteappointment "")**, which accepts the Guid of the appointment data as its argument. The Guid is availed as one of the appointment element’s attribute.

For example, here the below code example depicts the way to delete the appointments programmatically by calling the **deleteAppointment** function within the **[appointmentClick](http://help.syncfusion.com/js/api/ejschedule#events:appointmentclick "")** event, which triggers whenever the user clicks on an appointment.

{% highlight html %}
<body>

<!-- HTML element will initialize as a ejSchedule -->

<div id="schedule"></div>

<script>

$("#schedule").ejSchedule({

currentDate: new Date(2015, 11, 7),

appointmentSettings: {

//Array of JSON data configure in dataSource

dataSource: [

{

Id: 1,

Subject: "Music Class",

StartTime: new Date("2015/11/7 06:00 AM"),

EndTime: new Date("2015/11/7 07:00 AM")

},

{

Id: 2,

Subject: "School",

StartTime: new Date("2015/11/7 9:00 AM"),

EndTime: new Date("2015/11/7 02:30 PM")

}]

},

appointmentClick: "onAppointmentClick"

});

//addAppointment is a function, gets called on clicking the Add button

function onAppointmentClick(args) {

var schObj = $("#schedule").data("ejSchedule");

schObj.deleteAppointment(args.appointment.Guid);

// $($(".e-appointment")[0]).attr("guid") --> To get the guid attribute value of an element directly.

}



</script>



{% endhighlight %}

### Handling Appointment Actions

It is possible to define some specific actions to take place after the CRUD operation occurs on the Scheduler appointments through the following available client-side events,

* appointmentSaved
* appointmentEdited
* appointmentDeleted

**[appointmentSaved](http://help.syncfusion.com/js/api/ejschedule#events:appointmentsaved "")** – Triggers before saving a new appointment.

**[appointmentEdited](http://help.syncfusion.com/js/api/ejschedule#events:appointmentedited "")** – Triggers when an appointment is edited and before it is being updated to the dataSource.

**[appointmentDeleted](http://help.syncfusion.com/js/api/ejschedule#events:appointmentdeleted "")** – Triggers before deleting an existing appointment.

To stop the save, edit and delete actions on the Scheduler appointments, following code example can be used.

{% highlight html %}


<div id="Schedule1"></div>

$(function () {

// defining Schedule control

$("#Schedule1").ejSchedule({

width: "100%",

height: "525px",

currentDate:new Date(2015,11,5),

appointmentSettings: {

dataSource: [{

Id: 101,

Subject: "Talk with Nature",

StartTime: new Date(2015, 11, 5, 10, 00),

EndTime: new Date(2015, 11, 5, 11, 00)

}]

},

appointmentSaved: "onAppointmentSave",

appointmentEdited: "onAppointmentEdit",

appointmentDeleted: "onAppointmentDelete"

});

});

function onAppointmentSave(args) {

args.cancel = true; // cancels the save action on appointments.

}

function onAppointmentEdit(args) {

args.cancel = true; // cancels the edit action on appointments.

}

function onAppointmentDelete(args) {

args.cancel = true; // cancels the delete action on appointments.

}





{% endhighlight %}

### Read Only

An interaction with the appointments of the Scheduler can be enabled/disabled through the **readOnly** property. When the **readOnly** property is set to **true**, it is not possible to do any actions on the appointments, but you can navigate between the schedule dates, views and can also be able to see the appointment details in the quick window. By default, this property is set to **false**.

{% highlight html %}
<!-- HTML element will initialize as a ejSchedule -->

<div id="schedule"></div>

<script>

$(function () {

$("#schedule").ejSchedule({

//set the Schedule as read only,

readOnly:true,

currentDate: new Date(2015, 11, 7),

appointmentSettings: {

//Array of JSON data configure in dataSource

dataSource: [

{

Id: 1,

Subject: "Music Class",

StartTime: new Date("2015/11/7 09:00 AM"),

EndTime: new Date("2015/11/7 10:00 AM")

},

{

Id: 2,

Subject: "School",

StartTime: new Date("2015/11/7 02:00 PM"),

EndTime: new Date("2015/11/7 06:30 PM")

}]

}

});

})

</script>



{% endhighlight %}

**Note**: When the **readOnly** property is set to true – double clicking the cells will open the appointment window filled with appointment details, which can be allowed to view but cannot be edited or saved.

### Drag and Drop

The appointment time can be modified through the drag and drop behaviour, by dragging and dropping it to the new location, so that the start time and end time of the appointment gets changed automatically. We can enable/disable the drag and drop functionality through the **allowDragDrop** property. By default, it is set to **true**.

{% highlight html %}
<!-- HTML element will initialize as a ejSchedule -->

<div id="schedule"></div>

<script>

$(function () {

$("#schedule").ejSchedule({

//disable appointment drag and drop,

allowDragDrop: false,

currentDate: new Date(2015, 11, 7),

appointmentSettings: {

//Array of JSON data configure in dataSource

dataSource: [

{

Id: 1,

Subject: "Music Class",

StartTime: new Date("2015/11/7 09:00 AM"),

EndTime: new Date("2015/11/7 10:00 AM")

},

{

Id: 2,

Subject: "School",

StartTime: new Date("2015/11/7 02:00 PM"),

EndTime: new Date("2015/11/7 06:30 PM")

}]

}

});

})

</script>



{% endhighlight %}

#### Handling Drag Actions Dynamically

The drag and drop functionality can be handled with the following three events,

* dragStart
* drag
* dragStop

**[dragStart](http://help.syncfusion.com/js/api/ejschedule#events:dragstart "")** – Triggers when the appointments are started to drag from its source location.

**[drag](http://help.syncfusion.com/js/api/ejschedule#events:drag "")** – Triggers when the appointments are being dragged over.

**[dragStop](http://help.syncfusion.com/js/api/ejschedule#events:dragstop "")** – Triggers when the appointments are dropped on a destined location.

The following code example shows how to cancel the dragging functionality with the help of one of these events.

{% highlight html %}


<div id="Schedule1"></div>

$(function () {

// defining Schedule control

$("#Schedule1").ejSchedule({

width: "100%",

height: "525px",

currentDate:new Date(2015,11,5),

appointmentSettings: {

dataSource: [{

Id: 101,

Subject: "Talk with Nature",

StartTime: new Date(2015, 11, 5, 10, 00),

EndTime: new Date(2015, 11, 5, 11, 00)

}]

},

dragStop: "onDragStop"

});

});

function onDragStop(args) {

args.cancel = true; // cancels the drag action on appointments.

}





{% endhighlight %}

### Resize

Resizing an appointment is another way to change its start or end time. Mouse hover on the appointments, so that the resizing handlers gets displayed on either sides of the appointment which allows resizing. The resizing functionality can be enabled/disabled by setting the **enableAppointmentResize** property. By default it is set to **true**.

{% highlight html %}
<!-- HTML element will initialize as a ejSchedule -->

<div id="schedule"></div>

<script>

$(function () {

$("#schedule").ejSchedule({

//disable appointment resizes,

enableAppointmentResize: false,

currentDate: new Date(2015, 11, 7),

appointmentSettings: {

//Array of JSON data configure in dataSource

dataSource: [

{

Id: 1,

Subject: "Music Class",

StartTime: new Date("2015/11/7 09:00 AM"),

EndTime: new Date("2015/11/7 10:00 AM")

},

{

Id: 2,

Subject: "School",

StartTime: new Date("2015/11/7 02:00 PM"),

EndTime: new Date("2015/11/7 06:30 PM")

}]

}

});

})

</script>



{% endhighlight %}

#### Handling Resize Actions Dynamically

The appointment resizing functionality can be handled through the following three events,

* resizeStart
* resize
* resizeStop

**[resizeStart](http://help.syncfusion.com/js/api/ejschedule#events:resizestart "")** – Triggers when the appointments are started resizing from its original time.

**[resize](http://help.syncfusion.com/js/api/ejschedule#events:resize "")** – Triggers when the appointment resizing is in progress.

**[resizeStop](http://help.syncfusion.com/js/api/ejschedule#events:resizestop "")** – Triggers when the appointment resizing is done.

The following code example shows how to cancel the resizing functionality with the help of one of these events.

{% highlight html %}


<div id="Schedule1"></div>

$(function () {

// defining Schedule control

$("#Schedule1").ejSchedule({

width: "100%",

height: "525px",

currentDate:new Date(2015,11,5),

appointmentSettings: {

dataSource: [{

Id: 101,

Subject: "Talk with Nature",

StartTime: new Date(2015, 11, 5, 10, 00),

EndTime: new Date(2015, 11, 5, 11, 00)

}]

},

resizeStart: "onResizeStart"

});

});

function onResizeStart(args) {

args.cancel = true; // Blocks the resize action on appointments.

}





{% endhighlight %}

### Categorization

It allows to differentiate the appointments with various categorize options and individual colors. You can also denote the status of the appointments using this categorize option and can specify your own user-defined category collection. It is also possible to select multiple categorize for a single appointment.

**Categorize Settings**

The **[categorizeSettings](http://help.syncfusion.com/js/api/ejschedule#members:categorizesettings "")** is an object collection that holds below categorize related properties such as,

* **[enable](help.syncfusion.com/js/api/ejschedule#members:categorizesettings-enable "")** - It accepts true or false value, denoting whether to enable/disable the categorize option. Its default value is **false**.
* **[allowMultiple](http://help.syncfusion.com/js/api/ejschedule#members:categorizesettings-allowmultiple "")** – It enables or disables the multiple selection of categories for each appointments in the appointment window as well as in the context menu. Its default value is **false**.
* **[dataSource](http://help.syncfusion.com/js/api/ejschedule#members:categorizesettings-datasource "")** – Bind the categorize collection. This property should be assigned with the JSON data array collection or instance of **[‘ej.DataManger’](http://help.syncfusion.com/js/datamanager/overview# "")**. We have below 6 default values for data source collection.

{% highlight js %}

categorizeSettings: {

dataSource: [

{ text: "Blue Category", id: 1, color: "#7499e1", fontColor: "green" },

{ text: "Green Category", id: 2, color: "#7cce6e", fontColor: "green" },

{ text: "Orange Category", id: 3, color: "#f19d5a", fontColor: "green" },

{ text: "Purple Category", id: 4, color: "#937bd1", fontColor: "green" },

{ text: "Red Category", id: 5, color: "#d98889", fontColor: "green" },

{ text: "Yellow Category", id: 6, color: "#f8f264", fontColor: "green" }

]

}



{% endhighlight %}

The below categorize fields holds the appropriate column names from the dataSource - 

<table>
<tr>
<th>
Field name<br/><br/></th><th>
Description<br/><br/></th></tr>
<tr>
<td>
**id**<br/><br/></td><td>
It holds the binding name for **id** field in the categorize dataSource<br/><br/></td></tr>
<tr>
<td>
**text**<br/><br/></td><td>
It holds the binding name for **text** field in the categorize dataSource<br/><br/></td></tr>
<tr>
<td>
**color**<br/><br/></td><td>
It holds the binding name for **color** field in the categorize dataSource.<br/><br/></td></tr>
<tr>
<td>
**{{'[fontColor](http://help.syncfusion.com/js/api/ejschedule#members:categorizesettings-fontcolor"")'| markdownify }}**<br/><br/></td><td>
It holds the binding name for **fontcolor** field in the categorize dataSource. This font color apply in the appointment.<br/><br/></td></tr>
</table>
{% highlight html %}
<!-- HTML element will initialize as a ejSchedule -->

<div id="schedule"></div>

<script>

$(function () {

$("#schedule").ejSchedule({

currentDate: new Date(2015, 11, 7),

//Configure the categorize settings

categorizeSettings: {

//Enable the categorize options

enable: true,

//enable multiple selection options

allowMultiple: true,

//data source collection binding

dataSource: [

{ text: "Blue Category", id: 1, color: "#7499e1", fontColor: "green" },

{ text: "Green Category", id: 2, color: "#7cce6e", fontColor: "green" },

{ text: "Orange Category", id: 3, color: "#f19d5a", fontColor: "green" },

{ text: "Purple Category", id: 4, color: "#937bd1", fontColor: "green" },

{ text: "Red Category", id: 5, color: "#d98889", fontColor: "green" },

{ text: "Yellow Category", id: 6, color: "#f8f264", fontColor: "green" }

],

//text mapper field

text: "text",

//id mapper field 

id: "id",

//categorize color mapper field

color: "color",

//categorize appointment font color mapper field.

fontColor: "fontColor"

},

appointmentSettings: {

categorize: "categorize",

//Array of JSON data configure in dataSource

dataSource: [

{

Id: 1,

Subject: "Music Class",

StartTime: new Date("2015/11/7 09:00 AM"),

EndTime: new Date("2015/11/7 10:00 AM"),

categorize: "3",

},

{

Id: 2,

Subject: "School",

StartTime: new Date("2015/11/7 02:00 PM"),

EndTime: new Date("2015/11/7 06:30 PM"),

categorize: "1,2,6" // Multiple categorize id passing 

}]

}

});

})

</script>



{% endhighlight %}

### Priority

This option prioritize the appointments based on its importance and it can be differentiated with each individual icons/images. By default, there are some specific set of default priority collection and you can also customize it with your own priority collection.

**Priority Settings**

The **[prioritySettings](http://help.syncfusion.com/js/api/ejschedule#members:prioritysettings "")** is an object collection that holds the below priority related properties such as,

* **[enable](http://help.syncfusion.com/js/api/ejschedule#members:prioritysettings-enable "")** - It accepts true or false value, denoting whether to enable/disable the priority option. Its default value is **false**.
* **template** **–** Customize the priority icon/images using template options. Refer this [priority template](#_Priority_settings_template "") topic.
* **[dataSource](http://help.syncfusion.com/js/api/ejschedule#members:prioritysettings-datasource "")** – binds the priority collection. This property should be assigned with the JSON data array collection or instance of ‘**[ej.DataManger’](http://help.syncfusion.com/js/datamanager/overview# "")**. We have below 4 default values for priority data source collection.

{% highlight js %}

prioritySettings: {

dataSource: [

{ text: "None", value: "none" },

{ text: "High", value: "high" },

{ text: "Medium", value: "medium" },

{ text: "Low", value: "low" }

]

}



{% endhighlight %}

The below priority fields holds the appropriate column names from the dataSource,

<table>
<tr>
<th>
Field name<br/><br/></th><th>
Description<br/><br/></th></tr>
<tr>
<td>
**Text**<br/><br/></td><td>
It holds the binding name for **text** field in the priority dataSource<br/><br/></td></tr>
<tr>
<td>
**Value**<br/><br/></td><td>
It holds the binding name for **value** field in the priority dataSource.<br/><br/></td></tr>
</table>
{% highlight html %}
<!-- HTML element will initialize as a ejSchedule -->

<div id="schedule"></div>

<script>

$(function () {

$("#schedule").ejSchedule({

currentDate: new Date(2015, 11, 7),

//Configure the categorize settings

prioritySettings: {

//enable the priority option

enable: true,

//Configure the priority data source 

dataSource: [

{ text: "None", value: "none" },

{ text: "High", value: "high" },

{ text: "Low", value: "low" }

],

//mapper field for text 

text: "text",

//mapper field for value 

value: "value"

},

appointmentSettings: {

//set the priority mapper field for appointment data collection

priority: "priority",

//Array of JSON data configure in dataSource

dataSource: [

{

Id: 1,

Subject: "Music Class",

StartTime: new Date("2015/11/7 09:00 AM"),

EndTime: new Date("2015/11/7 10:00 AM"),

priority: "low", //pass the priority value

},

{

Id: 2,

Subject: "School",

StartTime: new Date("2015/11/7 02:00 PM"),

EndTime: new Date("2015/11/7 06:30 PM"),

priority: "high" //pass the priority value

}]

}

});

})

</script>



{% endhighlight %}


### Search or Filter Appointments

#### Appointment Search

The public method **[searchAppointment](http://help.syncfusion.com/js/api/ejschedule#methods:searchappointments "")** is used to search the appointments in the scheduler dataSource. It contains below four arguments such as search string, search field, filter operator and ignorecase.

**searchString** - It is used to search the given word / sentence with in the appointments data.

**fields** - It is the field, with which the search operation takes place. It’s an optional argument.

**filterOperator** – It contains the filter type like contains, greaterthan or lessthan. It’s an optional argument.

**ignoreCase** – It is a boolean value to set the search string as case sensitive or not. It’s an optional argument.

{% highlight html %}
<!-- HTML element will initialize as a ejSchedule -->

<input id="txtSearch" type="text" />

<input id="btnSearch" class="searchApp" type="button" value="Search" />

<div id="grid1">

</div>

<br />

<div style="float: left" id="Schedule1" />  

<script>

$(function () {

var dManager = ej.DataManager(window.Default).executeLocal(ej.Query().take(10));

$("#Schedule1").ejSchedule({

currentDate: new Date(2015, 11, 7),

appointmentSettings: {

//Array of JSON data configure in dataSource

dataSource: [

{

Id: 1,

Subject: "Music Class",

StartTime: new Date("2015/11/7 06:00 AM"),

EndTime: new Date("2015/11/7 07:00 AM")

},

{

Id: 2,

Subject: "School",

StartTime: new Date("2015/11/7 9:00 AM"),

EndTime: new Date("2015/11/7 02:30 PM")

}]

},

});

// To bind the click event to the button

$('.searchApp').bind("click", function () {

var _searchString = $("#txtSearch").val();

var schObj = $("#Schedule1").data("ejSchedule");

// method to retrieve the appointment based on search string

var result = schObj.searchAppointments(_searchString);

showResult(result, _searchString);

});

});

// method to show the result in a grid

function showResult(list, _searchString) {

if (!ej.isNullOrUndefined(list) && list.length != 0 && _searchString != "") {

$("#grid1").show();

$("#grid1").data("ejGrid") && $("#grid1").ejGrid("destroy");

$("#grid1").ejGrid({

allowScrolling: true,

dataSource: list,

allowPaging: true

});

}

}

</script>



{% endhighlight %}

#### Appointment Filters

The appointments can be filtered or shortlisted based on the simple or complex conditions with four available properties such as **field**, **operator**, **value** and **predicate** which is passed to the public method [filterAppointments](http://help.syncfusion.com/js/api/ejschedule#methods:filterappointments "").

**field** - It is the field, with which the search operation takes place. It’s an optional argument.

**operator** – It is generally used to specify the [filter](http://help.syncfusion.com/js/datamanager/filtering# "") type. 

**value** – It is the filter keyword based on which the records are filtered.

**predicate** – Add more than one condition query using **and****,** **or** [predicate](http://help.syncfusion.com/js/datamanager/filtering#and-predicate "").

{% highlight html %}
<!-- HTML element will initialize as a ejSchedule -->

<input id="btnSearch" class="searchApp" type="button" value="Filter" />

<div id="grid1">

</div>

<br />

<div style="float: left" id="Schedule1" />

<script>

$(function () {

var dManager = ej.DataManager(window.Default).executeLocal(ej.Query().take(10));

$("#Schedule1").ejSchedule({

currentDate: new Date(2015, 11, 7),

appointmentSettings: {

//Array of JSON data configure in dataSource

dataSource: [

{

Id: 1,

Subject: "Music Class",

StartTime: new Date("2015/11/7 06:00 AM"),

EndTime: new Date("2015/11/7 07:00 AM")

},

{

Id: 2,

Subject: "School",

StartTime: new Date("2015/11/7 9:00 AM"),

EndTime: new Date("2015/11/7 02:30 PM")

}]

}

});

// Method to bind the button click event

$('.searchApp').bind("click", function () {

// Add the filter data as like in the below format

var filter = [{

field: "Subject", // field configure

operator: "contains",

value: "Music",

predicate: "or"// predicate 

}, {

field: "Subject",// field configure

operator: "contains",

value: "School",

predicate: "or" // predicate

}];

var schObj = $("#Schedule1").data("ejSchedule");

// Method to get the Filtered appointment

var result = schObj.filterAppointments(filter);

showResult(result);

});

});

// method to show the result in a grid

function showResult(list) {

if (!ej.isNullOrUndefined(list) && list.length != 0) {

$("#grid1").show();

$("#grid1").data("ejGrid") && $("#grid1").ejGrid("destroy");

$("#grid1").ejGrid({

dataSource: list,

allowPaging: true,

});

}

}

</script>



{% endhighlight %}


### Recurrence Options

There are scenarios where you require the same appointments to be repeatedly created for multiple days on daily, weekly, monthly, and yearly or every weekday basis. 

In appointment data collection, **recurrence** and **recurrenceRule** are depended fields. While creating or binding the recurrence appointment, the **recurrence** field is set to **true** and **recurrenceRule** contains recurrence pattern details in string format.

#### Recurrence Rule

The recurrence appointments are created based on the recurrence rule. The RecurrenceRule is a string value that contains the details of the recurrence appointments like 

* repeat type - daily/weekly/monthly/yearly 
* how many times it needs to be repeated 
* the interval duration
* the time period to render the appointment, etc.,

It has the following properties based on which the recurrence appointments are rendered in the **Schedule** control with its respective time period.

<table>
<tr>
<th>
S.No<br/><br/></th><th>
Property<br/><br/></th><th>
**Purpose**<br/><br/></th></tr>
<tr>
<td>
1<br/><br/></td><td>
FREQ<br/><br/></td><td>
Maintains the Repeat type value of the appointment. <br/><br/>(**Example**: Daily, Weekly, Monthly, Yearly, Every week day)<br/><br/>Example: **FREQ=DAILY**;INTERVAL=1<br/><br/></td></tr>
<tr>
<td>
2<br/><br/></td><td>
INTERVAL<br/><br/></td><td>
Maintains the interval value of the appointments.<br/><br/>**For example**, when you create the daily appointment at an interval of 2, the appointments are rendered on the days Monday, Wednesday and Friday. (Creates an appointment on all days by leaving the interval of one day gap)<br/><br/>Example: FREQ=DAILY;**INTERVAL=2**<br/><br/></td></tr>
<tr>
<td>
3<br/><br/></td><td>
COUNT<br/><br/></td><td>
It holds the appointment’s count value. <br/><br/>**For example**, When the recurrence appointment count value is 10, which means that 10 instances of appointments are created in the recurrence series.<br/><br/>Example: FREQ=DAILY;INTERVAL=1;**COUNT=10**<br/><br/></td></tr>
<tr>
<td>
4<br/><br/></td><td>
UNTIL<br/><br/></td><td>
This property is used to store the recurrence end date value. <br/><br/>**For example**, when you set the end date of appointment as 11/30/2015, the UNTIL property holds the end date value denoting when the recurrence actually ends.<br/><br/>Example: FREQ=DAILY;INTERVAL=1;**UNTIL=11/30/2015**<br/><br/></td></tr>
<tr>
<td>
5<br/><br/></td><td>
BYDAY<br/><br/></td><td>
It holds the **DAY** values, representing on which the appointments actually renders. <br/><br/>**For example**, Create the weekly appointment, and select the day(s) from the day options (Monday/Tuesday/Wednesday/Thursday/Friday/Saturday/Sunday). When Monday is selected, the first two letters of the selected day “MO” is saved in the **BYDAY** property. When multiple days are selected, the values are separated by commas.<br/><br/>Example: FREQ=WEEKLY;INTERVAL=1;**BYDAY=MO,WE**;COUNT=10<br/><br/></td></tr>
<tr>
<td>
6<br/><br/></td><td>
BYMONTHDAY<br/><br/></td><td>
This property is used to store the date value of the Month, while creating the Month recurrence appointment.<br/><br/>**For example**, when you create a Monthly recurrence appointment for every 3rd day of the month, then **BYMONTHDAY** holds the value 3 and creates the appointment on 3rd day of every month.<br/><br/>Example: FREQ=MONTHLY;**BYMONTHDAY=3**;INTERVAL=1;COUNT=10<br/><br/></td></tr>
<tr>
<td>
7<br/><br/></td><td>
BYMONTH<br/><br/></td><td>
This property is used to store the index value of the selected Month while creating the yearly appointments.<br/><br/>**For example**, when you create the yearly appointment on June month, the index value of June month 6 will get stored in the BYMONTH field. The appointment is created on every 6th month of a year.<br/><br/>Example: FREQ=YEARLY;BYMONTHDAY=16;**BYMONTH=6**;INTERVAL=1;COUNT=10<br/><br/></td></tr>
<tr>
<td>
8<br/><br/></td><td>
BYSETPOS<br/><br/></td><td>
This property is used to store the index value of the week. <br/><br/>**For example**, when you create the monthly appointment in second week of a month, the index value of the second week (2) is stored in BYSETPOS.<br/><br/>Example: FREQ=MONTHLY;BYDAY=MO;**BYSETPOS=2**;UNTIL=8/11/2015<br/><br/></td></tr>
<tr>
<td>
9<br/><br/></td><td>
WKST<br/><br/></td><td>
This property is used to store the start day value of a week.<br/><br/>**For example**, when you render the workweek the “WKST” value is Monday.<br/><br/></td></tr>
<tr>
<td>
10 <br/><br/></td><td>
EXDATE<br/><br/></td><td>
EXDATE is used to hold the modified appointment date details (date value) in the recurrence appointment series.<br/><br/>**For example**, when you change the recurrence appointment instance under the date “6/19/2015”, then this date is added to the recurrence rule EXDATE field. “EXDATE” is also used to differentiate the edited occurrence of the recurrence series for some internal process while doing the “Edit Series or Delete series” actions.<br/><br/>Example: FREQ=WEEKLY;BYDAY=MO,TU,WE,TH,FR;COUNT=10;**EXDATE=6/18/2015,6/20/2015**;RECUREDITID=1651<br/><br/></td></tr>
<tr>
<td>
11<br/><br/></td><td>
RECUREDITID<br/><br/></td><td>
This property contains the Parent Id value of the edited appointment. It is used to track the edited appointment occurrence with its parent recurrence appointment series.<br/><br/>**For example**, when you edit the particular occurrence of the recurrence appointment series, the “RECUREDITID” is added to that edited appointment depicting its parent Id.<br/><br/>Example:<br/><br/>FREQ=WEEKLY;BYDAY=MO,TU,WE,TH,FR;COUNT=10;EXDATE=6/18/2015,6/20/2015;**RECUREDITID=1651**<br/><br/></td></tr>
</table>
To know more about other possible combinations of above specified recurrence rule properties, refer [here](http://www.syncfusion.com/kb/3719/what-is-recurrencerule-in-the-schedule-control# "").

{% highlight html %}
<!-- HTML element will initialize as a ejSchedule -->

<div id="schedule"></div>

<script>

$("#schedule").ejSchedule({

currentDate: new Date(2015, 11, 7),

appointmentSettings: {

//Recurrence mapper field

recurrence: "Recurrence",

recurrenceRule: "RecurrenceRule",

//Array of JSON data configure in dataSource

dataSource: [

{

Id: 1,

Subject: "Music Class",

StartTime: new Date("2015/11/7 06:00 AM"),

EndTime: new Date("2015/11/7 07:00 AM")

},

{

Id: 2,

Subject: "School",

StartTime: new Date("2015/11/7 9:00 AM"),

EndTime: new Date("2015/11/7 02:30 PM"),

Recurrence: true,//enable recurrence options

RecurrenceRule: "FREQ=DAILY;INTERVAL=1;COUNT=5" //Recurrence rule.

}]

}

});

</script>



{% endhighlight %}

#### Recurrence Validation

The default recurrence validation has been included for recurrence appointments similar to the one available in outlook. The validation occurs during the recurrence appointment creation, drag and drop of the recurrence appointments and also if any single occurrence changes. The validation can be disabled by setting the **enableRecurrenceValidation** to **false**.

{% highlight html %}
<!-- HTML element will initialize as a ejSchedule -->

<div id="schedule"></div>

<script>

$("#schedule").ejSchedule({

currentDate: new Date(2015, 11, 7),

//disable the recurrence validation

enableRecurrenceValidation:false,

appointmentSettings: {

//Recurrence mapper field

recurrence: "Recurrence",

recurrenceRule: "RecurrenceRule",

//Array of JSON data configure in dataSource

dataSource: [

{

Id: 1,

Subject: "Music Class",

StartTime: new Date("2015/11/7 06:00 AM"),

EndTime: new Date("2015/11/7 07:00 AM")

},

{

Id: 2,

Subject: "School",

StartTime: new Date("2015/11/7 9:00 AM"),

EndTime: new Date("2015/11/7 02:30 PM"),

Recurrence: true,//enable recurrence options

RecurrenceRule: "FREQ=DAILY;INTERVAL=1;COUNT=5" //Recurrence rule.

}]

}

});

</script>



{% endhighlight %}



**Note**: You can parse the **RecurrenceRule** of an appointment from the server-side by making use of a new generic utility class **RecurrenceHelper**. Refer this [KB document](https://www.syncfusion.com/kb/5390/how-to-parse-the-recurrencerule-in-server-side# "").

### Reminder

Reminder option notifies all the appointments before some specific time. By default, it notifies before 5 minutes. Each and every appointment triggers the **[reminder](http://help.syncfusion.com/js/api/ejschedule#events:reminder "")** event and can utilize this event for other user actions like mailing particular event to someone or to do any kind of manipulations with the reminder appointments and so on.

**Enable**

To enable the reminder settings of the Schedule control, set the **enable** property as **true** within the **[reminderSettings](http://help.syncfusion.com/js/api/ejschedule#members:remindersettings "")** option.

**Alert Before**

The **reminderSettings** option includes another optional property **alertBefore** that accepts integer value to denote the time before how long the reminder should be notified to the user.

{% highlight html %}
<!-- HTML element will initialize as a ejSchedule -->

<div id="schedule"></div>

<script>

$("#schedule").ejSchedule({

//Reminder configuration 

reminderSettings: {

//enable the reminder options 

enable: true,

//notify before 10 mins

alertBefore:10

},

timeZone:"UTC 00:00",

//Reminder event configure 

reminder:"reminderCustom",

appointmentSettings: {

//Array of JSON data configure in dataSource

dataSource: [

{

Id: 1,

Subject: "Music Class",

StartTime: new Date(new Date().setMinutes(new Date().getMinutes() + 11)),// new Date("2015/11/7 06:00 AM"),

EndTime: new Date(new Date().setHours(new Date().getHours() + 1))// new Date("2015/11/7 07:00 AM")

},

{

Id: 2,

Subject: "School",

StartTime: new Date(new Date().setHours(new Date().getHours() + 2)),

EndTime: new Date(new Date().setHours(new Date().getHours() + 4))

}]

},

});

function reminderCustom(args) {

alert("Reminder Appointment");

}

</script>



{% endhighlight %}

**Note**: Whenever the reminder setting is enabled in the Scheduler with some specific value (in minutes) assigned to the **alertBefore** property, the **reminder** event gets triggered before this specified value. It includes the reminder appointment’s entire information in its arguments.

