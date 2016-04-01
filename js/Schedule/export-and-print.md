---
title: Export and print the Schedule with its appointments	
description: Export/Print the complete Scheduler or specific appointment alone
platform: js
control: schedule
documentation: ug
keywords: export, import and print 
---
# Export and Print

## Export Appointments to ICS file

The Appointments can be exported as a whole collection or else a single appointment alone can be exported from the Scheduler. By default, the appointments are exported to .ics format which can then be imported and used in any of the other external calendars.

### Single Appointment Exporting

A single appointment can be exported by making use of its Id. You can achieve this functionality by making use of an [exportSchedule](/js/api/ejschedule#methods:exportschedule) method by passing the id of an appointment to export as one of its parameter. 

It can also be achieved in another way by enabling the context menu settings and then adding a custom menu option for export appointment functionality. When right clicked on an appointment, and **export Appointment** option is chosen, the exporting functionality can be handled through the [menuItemClick](/js/api/ejschedule#events:menuitemclick) event, within which the **exportSchedule** method should be defined with the following parameters,

* Action name (to be called in the server-side)
* Server Event (optional)
* Appointment Id (mandatory for single Appointment exporting)

The following code example shows the way to export single appointment from the Scheduler.

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="Schedule1"></div>

<script type="text/javascript">
$(function() {
    $("#Schedule1").ejSchedule({
        currentDate: new Date(2015, 11, 2),
        contextMenuSettings: {
            enable: true,
            menuItems: {
                appointment: [{
                    id: "open",
                    text: "Open Appointment"
                }, {
                    id: "delete",
                    text: "Delete Appointment"
                }, {
                    id: "export",
                    text: "Export Appointment"
                }]
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

N> The Id value of the appointment passed in the above code example can be retrieved in the server-side action through Request.Form["AppointmentId"], as the id passed from the script is stored as hidden value in the input field of the form under this name internally.

### Exporting all Appointments

To export the entire Scheduler appointments, the same [exportSchedule](/js/api/ejschedule#methods:exportschedule) method can be used without passing the id value to its parameter list. To achieve this, keep an individual button to export, and when it is clicked - the Scheduler can be allowed to export all the appointments.

The following code example depicts the way to export all the Scheduler appointments as a whole.

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="Schedule1"></div>

<!-- Button div for Export Option-->
<button id="Btn">Export</button>

<script type="text/javascript">
$(function() {
    $("#Btn").ejButton({
        width: "70px",
        height: "30px",
        click: "onClick"
    });
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

{% highlight c# %}

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

{% endhighlight %}

## PDF Export

Scheduler supports exporting it along with all its appointments in PDF format, for which the same [exportSchedule](/js/api/ejschedule#methods:exportschedule) method can be used without passing any id value to its parameter list. To achieve this, keep an individual button to export and when it is clicked, the Scheduler with appointments can be allowed to export as PDF.

The following code example depicts the way to export the Scheduler with appointments in PDF format.

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="Schedule1"></div>

<!-- Button div for Export Option-->
<button id="btnExport">Export</button>

<script type="text/javascript">
    $(function () {
        $("#btnExport").ejButton({
            width: "80px",
            height: "30px",
            click: "onExportClick"
        });
        $("#Schedule1").ejSchedule({
            width: "100%",
            height: "525px",
			currentDate:new Date(2014,4,5),
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

{% highlight javascript %}

function onExportClick(e) {
    var obj = $("#Schedule1").data("ejSchedule");
    obj.exportSchedule("http://js.syncfusion.com/ScheduleExport/api/JSScheduleExport/PDFExport", null, null);
    e.cancel = true;
}

{% endhighlight %}

The server-side action **PDFExport** contains the following code example to export the Scheduler.

{% highlight c# %}

public ActionResult PDFExport(string scheduleModel)
{
    PdfExport exp = new PdfExport();
    PdfDocument document = exp.Export(Request.Form["ScheduleModel"], Request.Form["ScheduleProcesedApps"], "flat-saffron", Request.Form["locale"], PdfPageOrientation.Landscape);
    document.Save("Schedule.pdf", HttpContext.ApplicationInstance.Response, HttpReadType.Save);
    return RedirectToAction("PDFExportController");
}

{% endhighlight %}

## Print

Two types of Print options are available – either to print the entire Scheduler layout including all the appointments in it or else to print any particular appointment alone. The public method [print](/js/api/ejschedule#methods:print) is used to print the entire Scheduler.

### Print the Scheduler

The following code example shows the way to print the entire Scheduler, by keeping an extra button in a page – on which clicking the button will print the entire Scheduler.

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="Schedule1"></div>

<!--Button div for Print Option-->
<button id="Btn">Print</button>

<script type="text/javascript">
$(function() {
	
    $("#Btn").ejButton({
        width: "70px",
        height: "30px",
        click: "onClick"
    });

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

### Printing Specific Appointments

To print a particular appointment, either the default context menu **print** option can be used or else the [print](/js/api/ejschedule#methods:print) method can be used by passing the id of the appointment to be printed as its argument. 

#### Using Context Menu

Here, the print action is handled internally by default, so that when an appointment is right clicked – choosing print option from the context menu that pops-out will automatically print that particular appointment.

N> To handle this functionality, the context menu settings needs to be enabled with print option added to the appointment items.

The following code example depicts the way to print a particular appointment.

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="Schedule1"> </div>

<script type="text/javascript">
$(function() {
    $("#Schedule1").ejSchedule({
        currentDate: new Date(2015, 11, 2),
        contextMenuSettings: {
            enable: true,
            menuItems: {
                appointment: [{
                    id: "open",
                    text: "Open Appointment"
                }, {
                    id: "delete",
                    text: "Delete Appointment"
                }, {
                    id: "print",
                    text: "Print Appointment"
                }]
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

#### Using print() method

The public method `print` needs to be used here by passing the appointment object as its argument, that needs to be printed.

For example, here the below code example depicts the way to print the particular appointment programmatically by calling the **print** function within the [appointmentClick](/js/api/ejschedule#events:appointmentclick) event, which triggers whenever the user clicks on an appointment.

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="Schedule1"> </div>

<script type="text/javascript">
$(function() {
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
        },
        appointmentClick: "onAppointmentClick"
    });
}); 

function onAppointmentClick(args) {
    var schObj = $("#Schedule1").data("ejSchedule");
    schObj.print(args.appointment);
}  
</script>

{% endhighlight %}

## Import Appointments

To import appointments into the Scheduler, server-side method `renderingImportAppointments` needs to be used, which returns the list of appointments retrieved from the specified file path.

Refer the following code example to import the appointments into Scheduler.

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="Schedule1"></div>

<!--Button div for Print Option-->
<button id="Btn">Import</button>

<script type="text/javascript">
$(function() {
    $("#Btn").ejButton({ width: "70px", height: "30px", click: "ScheduleImport" });
    $("#Schedule1").ejSchedule({
        width: "100%",
        height: "525px",
        currentDate: new Date(2015, 11, 2),
        appointmentSettings: {
            id: "Id",
            subject: "subject",
            startTime: "startTime",
            endTime: "endTime",
            allDay: "allDay",
            recurrence: "recurrence",
            recurrenceRule: "recurrenceRule"
        }
    });
});

function ScheduleImport() {
    var dataManger = ej.DataManager({ url: '@Url.Action("ScheduleImportData", "Schedule")', crossDomain: true });
    $("#Schedule1").ejSchedule({
        appointmentSettings: {
            dataSource: dataManger
        }
    });
}
</script>

{% endhighlight %}

The server-side action `ScheduleImportData` contains the following code example to import the Scheduler appointments.

{% highlight c# %}

public JsonResult ScheduleImportData() {
    var destinationPath = @"Filepath\iCalender.ics";
    ScheduleImport importApps = new ScheduleImport();
    var app = importApps.renderingImportAppointments(destinationPath);
    int intMax = app.Max(a => a.Id);
    List<ScheduleAppointmentsObjData> result = new List<ScheduleAppointmentsObjData>();
    for (var i = 0; i < app.Count; i++) {
        app[i].Id = intMax + 1;
        ScheduleAppointmentsObjData row = new ScheduleAppointmentsObjData(app[i].Id, app[i].Subject, app[i].Location, app[i].StartTime, app[i].EndTime, app[i].Description, null, null, app[i].Recurrence, null, null, app[i].AppointmentCategorize, null, app[i].AllDay, null, null, app[i].RecurrenceRules, null, null);
        result.Add(row);
        intMax = app[i].Id;
    }
    return Json(result, JsonRequestBehavior.AllowGet);
}

{% endhighlight %}
