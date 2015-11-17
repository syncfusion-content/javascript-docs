---
title: How-to
description: How to create custom configuration using schedule control
platform: js
control: schedule
documentation: ug
keywords: globalize, localize, localization, globalization 
---
## How To

### Validate the Custom Appointment Window Fields

The client-side validation of the fields present within the custom appointment window can be handled before submitting it, by adding appropriate validation classes to each field.

Refer the steps [here](#_Appointment_Window_Customization "") and create a sample for Custom Appointment window, before proceeding with the following validations.

In the custom appointment window sample, create an additional css class **validation** as mentioned below to add it to the appropriate fields, if the validation of such fields fails.

{% highlight html %}
<style> 

.validation {

border-color: red;

}

</style>





{% endhighlight %}

The sample contains the fields like Subject, Description, StartTime and EndTime which needs to be validated at client-side. To do so, add the required validation code within the script section as follows.

{% highlight html %}
<script type="text/javascript">

// To Validate the Subject field.

$("#subject").focusout(function () {

if ($.trim($("#subject").val()) == "") {

$("#subject").addClass("validation");  

return false;

}

})

// To Validate the Description field.

$("#customdescription").focusout(function () {

if ($.trim($("#customdescription").val()) == "") {

$("#customdescription").addClass("validation");  

return false;

}

})

// To Validate the Time duration of the appointments

$("#EndTime").focusout(function () {

if (new Date($("#EndTime").val()).getDate() >= new Date($("#StartTime").val()).getDate()) {

if (new Date($("#StartTime").val()).getTime() >= new Date($("#EndTime").val()).getTime())

alert("EndTime value is lesser than the StartTime value");

}

})

</script>





{% endhighlight %}

Now, after adding the above validations – whenever the fields within the custom appointment window are skipped without filling any information, it will be notified to the users appropriately.

### Highlight Different Work Hours for Each Resources

By default, the workhours of the Scheduler is highlighted based on the start and end values provided within the **[workHours](#_Working_Hours "")** object. It remains same for all the resources, when the Scheduler is rendered with multiple resources. To customize this behaviour so as to highlight different workhour range for each of the resources, the following workaround can be utilised by making use of the Scheduler events **create** and **[actionComplete](http://help.syncfusion.com/js/api/ejschedule#events:actioncomplete "")**.

Initially, set the **highlight** as false for the **workHours**, so as to disable the highlighting of default work hour range.

{% highlight html %}
<!--Container for ejScheduler widget-->

<div id="Schedule1"></div>

<script type="text/javascript">

$(function () {

$("#Schedule1").ejSchedule({

currentDate: new Date(2015, 11, 2),

showCurrentTimeIndicator: false,

workHours: { 

highlight: false 

},

group: {

resources: ["Owners"]

},

resources: [{

field: "ownerId", title: "Owner", name: "Owners",

resourceSettings: {

dataSource: [

{ text: "Nancy", id: 1, color: "#f8a398" },

{ text: "Steven", id: 3, color: "#56ca85" },

{ text: "Michael", id: 5, color: "#51a0ed" }],

text: "text", id: "id", color: "color"

}

}],

appointmentSettings: {

resourceFields: "ownerId",

dataSource: [{

Id: 100,

Subject: "Wild Discovery",

StartTime: new Date(2015, 11, 2, 9, 00),

EndTime: new Date(2015, 11, 2, 10, 30),

ownerId: 3,

Location: "CHINA"

}]

},

create: "onCreate",

actionComplete: "onCreate"

});

});

// This function executes during the initial control creation and also on completion of each action like date/view navigation.

function onCreate(args) {

if (args.requestType == "viewNavigate" || args.requestType == "dateNavigate" || args.type == "create") {

// declare different start and end work hour values for each resources

var resourceOneStart = 9, resourceOneEnd = 18;

var resourceTwoStart = 13, resourceTwoEnd = 18;

var resourceThreeStart = 10, resourceThreeEnd = 18;

this.option("workHours.highlight", (this.currentView() != "month") ? false : true);

// Get the Scheduler workcell rows

var trElements = this.$WorkCellDiv.find("tr");

for (var i = 0; i < trElements.length; i++) {

// Get the Scheduler workcell columns

var tdElements = $(trElements[i]).find("td");

for (var j = 0; j < tdElements.length; j++) {

switch (this.currentView()) {

case "day":

switch (j) {

case 0: // column index 0 represents first resource in day view

$(tdElements[j]).addClass(((i > (resourceOneStart * 2) - 1) && (i <= (resourceOneEnd * 2) - 1)) ? "e-businesshighlightworkcells" : "");

break;

case 1: // column index 1 represents second resource in day view

$(tdElements[j]).addClass(((i > (resourceTwoStart * 2) - 1) && (i <= (resourceTwoEnd * 2) - 1)) ? "e-businesshighlightworkcells" : "");

break;

case 2: // column index 2 represents third resource in day view

$(tdElements[j]).addClass(((i > (resourceThreeStart * 2) - 1) && (i <= (resourceThreeEnd * 2) - 1)) ? "e-businesshighlightworkcells" : "");

break;

}

break;

case "week":

switch (j) {

case 0: case 1: case 2: case 3: case 4: case 5: case 6: // column indexes 0 to 6 belongs to first resource in week view (7 days)

$(tdElements[j]).addClass(((i > (resourceOneStart * 2) - 1) && (i <= (resourceOneEnd * 2) - 1)) ? "e-businesshighlightworkcells" : "");

break;

case 7: case 8: case 9: case 10: case 11: case 12: case 13: // column indexes 7 to 13 belongs to second resource in week view (7 days)

$(tdElements[j]).addClass(((i > (resourceTwoStart * 2) - 1) && (i <= (resourceTwoEnd * 2) - 1)) ? "e-businesshighlightworkcells" : "");

break;

case 14: case 15: case 16: case 17: case 18: case 19: case 20: // column indexes 14 to 20 belongs to third resource in week view (7 days)

$(tdElements[j]).addClass(((i > (resourceThreeStart * 2) - 1) && (i <= (resourceThreeEnd * 2) - 1)) ? "e-businesshighlightworkcells" : "");

break;

}

break;

case "workweek":

switch (j) {

case 0: case 1: case 2: case 3: case 4:        // column indexes 0 to 4 belongs to first resource in workweek view (5 days)

$(tdElements[j]).addClass(((i > (resourceOneStart * 2) - 1) && (i <= (resourceOneEnd * 2) - 1)) ? "e-businesshighlightworkcells" : "");

break;

case 5: case 6: case 7: case 8: case 9:

// column indexes 5 to 9 belongs to second resource in workweek view (5 days)

$(tdElements[j]).addClass(((i > (resourceTwoStart * 2) - 1) && (i <= (resourceTwoEnd * 2) - 1)) ? "e-businesshighlightworkcells" : "");

break;

case 10: case 11: case 12: case 13: case 14:

// column indexes 10 to 14 belongs to third resource in workweek view (5 days)

$(tdElements[j]).addClass(((i > (resourceThreeStart * 2) - 1) && (i <= (resourceThreeEnd * 2) - 1)) ? "e-businesshighlightworkcells" : "");

break;

}

break;

}

}

}

}

}

</script>





{% endhighlight %}

### Display Scheduler with Appointments Filtered by Subject

It is possible to display the Scheduler with the appointments, which is filtered based on the Subject. For example, if we keep a text box and start typing a character – the appointment’s subject that matches the typed character alone will be shown on the Scheduler. The following code example depicts the way to achieve this.

{% highlight html %}
<!--textbox for entering search character-->

<input id='txtSearch' type='text' onkeyup='searchKeyUp()' />

<!--Container for ejScheduler widget-->

<div id="Schedule1"></div>

<script type="text/javascript">

// Appointment data to be bound to the Scheduler

window.Default = [

{

Id: 101,

Subject: "Bering Sea Gold",

StartTime:new Date(2015,11,5,10,00),

EndTime: new Date(2015,11,5,11,00),

Description:"",

AllDay: false,

Recurrence: false,

Categorize: "1,3"

},

{

Id: 102,

Subject: "Bering Sea Gold",

StartTime:new Date(2015,11,2,16,00),

EndTime:new Date(2015,11,2,17,30),

Description:"",

AllDay: false,

Recurrence: false,

Categorize: "2,5"

}, {

Id: 104,

Subject: "What Happened Next?",

StartTime: new Date(2015,11,5,12,30),

EndTime: new Date(2015,11,5,15,00),

Description:"",

AllDay: false,

Recurrence: false,

Categorize: "4,1"

}, {

Id: 105,

Subject: "Daily Planet",

StartTime: new Date(2015,11,3,01,00),

EndTime:new Date(2015,11,3,02,00),

Description:"",

AllDay: false,

Recurrence: false,

Categorize: "1,3,6"

}, {

Id: 107,

Subject: "How It's Made",

StartTime: new Date(2015,11,1,06,00),

EndTime: new Date(2015,11,1,07,30),

Description:"",

AllDay: false,

Recurrence: true,

RecurrenceRule: "FREQ=WEEKLY;BYDAY=MO,TU;INTERVAL=1;COUNT=15",

Categorize: "2,3,6"

}, {

Id: 108,

Subject: "Deadest Catch",

StartTime: new Date(2015,11,3,16,00),

EndTime: new Date(2015,11,3,17,00),

Description:"",

AllDay: false,

Recurrence: false,

Categorize: "2,4,6,1"

}, {

Id: 109,

Subject: "MayDay",

StartTime: new Date(2015,3,30,06,30),

EndTime: new Date(2015,3,30,07,30),

Description:"",

AllDay: false,

Recurrence: false,

Categorize: "5,3"

}, {

Id: 115,

Subject: "Cash Cab",

StartTime:new Date(2015,3,30,15,00),

EndTime: new Date(2015,3,30,16,30),

Description:"",

AllDay: false,

Recurrence: true,

RecurrenceRule: "FREQ=DAILY;INTERVAL=1;COUNT=5",

Categorize: "1,3"



}];

$(function () {

// For Scheduler

$("#Schedule1").ejSchedule({

currentDate: new Date(2015, 11, 5),

showCurrentTimeIndicator: false,

appointmentSettings: {

dataSource: dManager

}

});

});

// This function executes when a character is entered in the textbox

function searchKeyUp() {

var searchString = $("#txtSearch").val();

var schObj = $("#Schedule1").data("ejSchedule");

var result = schObj.searchAppointments(searchString);

schObj.option("appointmentSettings", { dataSource: [] });

if (!ej.isNullOrUndefined(result) && result.length != 0 && searchString != "")

schObj.option("appointmentSettings", { dataSource: result });

else

schObj.option("appointmentSettings", { dataSource: window.Default });

}

</script>



{% endhighlight %}

### Customize the Default Appointment Window

Apart from the custom appointment window, it is possible to customize the default appointment window by adding/removing the required number of fields into it. This can be achieved through the **create** event of the scheduler.

The following code example depicts the way to achieve the customization of default appointment window.

{% highlight html %}
<!--Container for ejScheduler widget-->

<div id="Schedule1"></div>

<script type="text/javascript">

$(function () {

// For Scheduler

$("#Schedule1").ejSchedule({

currentDate: new Date(2015, 11, 2),

showCurrentTimeIndicator: false,

create: "onCreate",

appointmentWindowOpen: "onAppointmentOpen",

appointmentSettings: {

dataSource: [{

Id: 100,

Subject: "Wild Discovery",

StartTime: new Date(2015, 11, 2, 9, 00),

EndTime: new Date(2015, 11, 2, 10, 30),

Location: "CHINA",

AppointmentType: "Tentative",

Status: "90%"

}]

}

});

});

// This function executes when the checkboxes are checked/unchecked

function onCreate(args) {

var customDesign = "<tr class='customfields'><td class='e-textlabel'>Event Type</td><td><input class='apptype' type='text'/></td><td class='e-textlabel'>Event Status </td><td><input class='status' type='text'/></td></tr>";

$("." + this._id + "parrow").after(customDesign);

}

// This function executes before the appointment window gets opened.

function onAppointmentOpen(args) {

if (!ej.isNullOrUndefined(args.appointment)) {

// if double clicked on the appointments, retrieve the custom field values from the appointment object and fills it in the appropriate fields.               this._appointmentAddWindow.find(".apptype").val(args.appointment.AppointmentType);

this._appointmentAddWindow.find(".status").val(args.appointment.Status);

}

else {

// if double clicked on the cells, clears the field values.               

this._appointmentAddWindow.find(".apptype").val("");

this._appointmentAddWindow.find(".status").val("");

}

}

</script>





{% endhighlight %}

