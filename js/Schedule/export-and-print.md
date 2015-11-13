## Export and Print

### Export Appointments

The Appointments can be exported as a whole collection or else a single appointment alone can be exported from the Scheduler. By default, the appointments are exported to .ics format which can then be imported and used in any of the other external calendars.

#### Single Appointment Exporting

A single appointment can be exported by making use of its Id. You can achieve this functionality by making use of an **[exportSchedule](http://help.syncfusion.com/js/api/ejschedule#methods:exportschedule "")** method by passing the id of an appointment to export as one of its parameter. 

It can also be achieved in another way by enabling the context menu settings and then adding a custom menu option for export appointment functionality. When right clicked on an appointment, and **export** **Appointment** option is chosen, the exporting functionality can be handled through the **[menuItemClick](http://help.syncfusion.com/js/api/ejschedule#events:menuitemclick "")** event, within which the **exportSchedule** method should be defined with the following parameters,

* Action name (to be called in the server-side)
* Server Event (optional)
* Appointment Id (mandatory for single Appointment exporting)

The following code example shows the way to export single appointment from the Scheduler.

{% highlight html %}


<!--Container for ejScheduler widget-->

<div id="Schedule1"></div>



<script type="text/javascript">

$(function () {

$("#Schedule1").ejSchedule({

currentDate: new Date(2015, 11, 2),

contextMenuSettings: {

enable: true,

menuItems: {

appointment: [

{ id: "open", text: "Open Appointment" },

{ id: "delete", text: "Delete Appointment" },

{ id: "export", text: "Export Appointment" }

]

}

},

menuItemClick: "onMenuItemClick",

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

// This function executes, when any of the menu options are clicked in the context menu

function onMenuItemClick(args) {

if (args.events.ID == "export") {

var obj = $("#Schedule1").data("ejSchedule");

// exportSchedule() method will send a post to the server-side to call a specified action.

obj.exportSchedule("ExportToICS", null, args.targetInfo.Id);

}

}

</script>





{% endhighlight %}

**Note**: The Id value of the appointment passed in the above code example can be retrieved in the server-side action through Request.Form["AppointmentId"], as the id passed from the script is stored as hidden value in the input field of the form under this name internally.

#### Exporting all Appointments

To export the entire appointments, the same **[exportSchedule](http://help.syncfusion.com/js/api/ejschedule#methods:exportschedule "")** method can be used without passing the id value to its parameter list. To achieve this, keep an individual button to export, and when it is clicked - the Scheduler can be allowed to export all the appointments.

The following code example depicts the way to export all the Scheduler appointments as a whole.

{% highlight html %}


<!--Container for ejScheduler widget-->

<div id="Schedule1"></div>

<!-- Button div for Export Option-->

<button id="Btn">Export</button>



<script type="text/javascript">

$(function () {

$("#Btn").ejButton({ width: "70px", height: "30px", click: "onClick" });

$("#Schedule1").ejSchedule({

currentDate: new Date(2015, 11, 2),

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

// Clicking on the export button will call this method

function onClick(args) {

var obj = $("#Schedule1").data("ejSchedule");

// Calls the server-side action ExportToICS

obj.exportSchedule("ExportToICS", null, null);

}

</script>





{% endhighlight %}

The server-side action **ExportToICS** contains the following code example to export the Scheduler appointments.

{% highlight html %}
public void ExportToICS(FormCollection form)

{

IEnumerable data;

string JSONModel = Request.Form["ScheduleModel"];

var model = JsonConvert.DeserializeObject<Dictionary<string, object>>(JSONModel);

var Id = Request.Form["AppointmentId"];

if(Id != null)

// To export single appointment

data = db.DefaultSchedules.Where(app => app.Id.ToString() == Id.ToString()).ToList();

else

// To export all the appointments

data = db.DefaultSchedules.ToList();

ScheduleExport obj = new ScheduleExport(model, data);

}

</script>





{% endhighlight %}

### Print

Two types of Print options are available – either to print the entire Scheduler layout including all the appointments in it or else to print any particular appointment alone. The public method **[print](http://help.syncfusion.com/js/api/ejschedule#methods:print "")** is used to print the entire Scheduler.

#### Print the Scheduler

The following code example shows the way to print the entire Scheduler, by keeping an extra button in a page – on which clicking the button will print the entire Scheduler.

{% highlight html %}


<!--Container for ejScheduler widget-->

<div id="Schedule1"></div>

<!—Button div for Print Option-->

<button id="Btn">Print</button>



<script type="text/javascript">

$(function () {

$("#Btn").ejButton({ width: "70px", height: "30px", click: "onClick" });

$("#Schedule1").ejSchedule({

currentDate: new Date(2015, 11, 2),

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

function onClick(args) {

var obj = $("#Schedule1").data("ejSchedule");

obj.print();

}

</script>





{% endhighlight %}

#### Printing specific appointments

To print a particular appointment, the context menu **print** option can be used. The print option is handled internally by default, so that when an appointment is right clicked – choosing print option from the context menu that pops-out will automatically print that appointment.

**Note**: To handle this functionality, the context menu settings needs to be enabled with print option added to the appointment items.

The following code example depicts the way to print a particular appointment.

{% highlight html %}
<!--Container for ejScheduler widget-->

<div id="Schedule1"></div>

<script type="text/javascript">

$(function () {

$("#Schedule1").ejSchedule({

currentDate: new Date(2015, 11, 2),

contextMenuSettings: {

enable: true,

menuItems: {

appointment: [

{ id: "open", text: "Open Appointment" },

{ id: "delete", text: "Delete Appointment" },

{ id: "print", text: "Print Appointment" }

]

}

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

