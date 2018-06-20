---
title: How-to
description: Custom Configuration with Schedule control
platform: js
control: schedule
documentation: ug
keywords: validation and customization of appointment window fields, highlight different work-hours, Appointment filters
api: /api/js/ejschedule 
---
# How To

## Validate the Custom Appointment Window Fields

The client-side validation of the fields present within the custom appointment window can be handled before submitting it, by adding appropriate validation classes to each field.

Refer the steps [here](/js/schedule/customization#appointment-window-customization) and create a sample for Custom Appointment window, before proceeding with the following validations.

In the custom appointment window sample, create an additional CSS class **validation** as mentioned below to add it to the appropriate fields, if the validation of such fields fails.

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
$("#subject").focusout(function() {
    if ($.trim($("#subject").val()) == "") {
        $("#subject").addClass("validation");
        return false;
    }
})

// To Validate the Description field.
$("#customDescription").focusout(function() {
    if ($.trim($("#customDescription").val()) == "") {
        $("#customDescription").addClass("validation");
        return false;
    }
})

// To Validate the Time duration of the appointments
$("#EndTime").focusout(function() {
    if (new Date($("#EndTime").val()).getDate() >= new Date($("#StartTime").val()).getDate()) {
        if (new Date($("#StartTime").val()).getTime() >= new Date($("#EndTime").val()).getTime())
            alert("EndTime value is lesser than the StartTime value");
    }
})

</script>

{% endhighlight %}

Now, after adding the above validations – whenever the fields within the custom appointment window are skipped without filling any information, it will be notified to the users appropriately.

## Highlight Different Work Hours for Each Resources

By default, the work hours of the Scheduler is highlighted based on the start and end values provided within the [workHours](/js/schedule/customization#hour-customization:working-hours) object. It remains same for all the resources, when the Scheduler is rendered with multiple resources. To customize this behavior so as to highlight different work hours range for each of the resources, the following workaround can be utilized by making use of the Scheduler events **create** and [actionComplete](/api/js/ejschedule#events:actioncomplete).

Initially, set the **highlight** as false for the **workHours**, so as to disable the highlighting of default work hour range.

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="Schedule1"></div>

<script type="text/javascript">

$(function() {
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
            field: "ownerId",
            title: "Owner",
            name: "Owners",
            resourceSettings: {
                dataSource: [
                    {
                        text: "Nancy",
                        id: 1,
                        color: "#f8a398"
                    },
                    {
                        text: "Steven",
                        id: 3,
                        color: "#56ca85"
                    },
                    {
                        text: "Michael",
                        id: 5,
                        color: "#51a0ed"
                    }
                ],
                text: "text",
                id: "id",
                color: "color"
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
        var resourceOneStart = 9,
            resourceOneEnd = 18;

        var resourceTwoStart = 13,
            resourceTwoEnd = 18;

        var resourceThreeStart = 10,
            resourceThreeEnd = 18;

        this.option("workHours.highlight", (this.currentView() != "month") ? false : true);

        // Get the Scheduler work cell rows
        var trElements = this.$WorkCellDiv.find("tr");

        for (var i = 0; i < trElements.length; i++) {

            // Get the Scheduler work cell columns
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
                            case 0:
                            case 1:
                            case 2:
                            case 3:
                            case 4:
                            case 5:
                            case 6: // column indexes 0 to 6 belongs to first resource in week view (7 days)
                                $(tdElements[j]).addClass(((i > (resourceOneStart * 2) - 1) && (i <= (resourceOneEnd * 2) - 1)) ? "e-businesshighlightworkcells" : "");
                                break;
                            case 7:
                            case 8:
                            case 9:
                            case 10:
                            case 11:
                            case 12:
                            case 13: // column indexes 7 to 13 belongs to second resource in week view (7 days)
                                $(tdElements[j]).addClass(((i > (resourceTwoStart * 2) - 1) && (i <= (resourceTwoEnd * 2) - 1)) ? "e-businesshighlightworkcells" : "");
                                break;
                            case 14:
                            case 15:
                            case 16:
                            case 17:
                            case 18:
                            case 19:
                            case 20: // column indexes 14 to 20 belongs to third resource in week view (7 days)
                                $(tdElements[j]).addClass(((i > (resourceThreeStart * 2) - 1) && (i <= (resourceThreeEnd * 2) - 1)) ? "e-businesshighlightworkcells" : "");
                                break;
                        }
                        break;
                    case "workweek":
                        switch (j) {
                            case 0:
                            case 1:
                            case 2:
                            case 3:
                            case 4: // column indexes 0 to 4 belongs to first resource in workweek view (5 days)
                                $(tdElements[j]).addClass(((i > (resourceOneStart * 2) - 1) && (i <= (resourceOneEnd * 2) - 1)) ? "e-businesshighlightworkcells" : "");
                                break;
                            case 5:
                            case 6:
                            case 7:
                            case 8:
                            case 9:
                                // column indexes 5 to 9 belongs to second resource in workweek view (5 days)
                                $(tdElements[j]).addClass(((i > (resourceTwoStart * 2) - 1) && (i <= (resourceTwoEnd * 2) - 1)) ? "e-businesshighlightworkcells" : "");
                                break;
                            case 10:
                            case 11:
                            case 12:
                            case 13:
                            case 14:
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

## Display Scheduler with Appointments Filtered by Subject

It is possible to display the Scheduler with appointments, which is filtered based on the Subject. For example, if we keep a text box and start typing a character – the list of appointments whose subject matches the typed character alone will be shown on the Scheduler. The following code example depicts the way to achieve this.

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
        StartTime: new Date(2015, 11, 5, 10, 00),
        EndTime: new Date(2015, 11, 5, 11, 00),
        Description: "",
        AllDay: false,
        Recurrence: false,
        Categorize: "1,3"
    },
    {
        Id: 102,
        Subject: "Bering Sea Gold",
        StartTime: new Date(2015, 11, 2, 16, 00),
        EndTime: new Date(2015, 11, 2, 17, 30),
        Description: "",
        AllDay: false,
        Recurrence: false,
        Categorize: "2,5"
    }, 
    {
        Id: 104,
        Subject: "What Happened Next?",
        StartTime: new Date(2015, 11, 5, 12, 30),
        EndTime: new Date(2015, 11, 5, 15, 00),
        Description: "",
        AllDay: false,
        Recurrence: false,
        Categorize: "4,1"
    }, 
    {
        Id: 105,
        Subject: "Daily Planet",
        StartTime: new Date(2015, 11, 3, 01, 00),
        EndTime: new Date(2015, 11, 3, 02, 00),
        Description: "",
        AllDay: false,
        Recurrence: false,
        Categorize: "1,3,6"
    }, {
        Id: 107,
        Subject: "How It's Made",
        StartTime: new Date(2015, 11, 1, 06, 00),
        EndTime: new Date(2015, 11, 1, 07, 30),
        Description: "",
        AllDay: false,
        Recurrence: true,
        RecurrenceRule: "FREQ=WEEKLY;BYDAY=MO,TU;INTERVAL=1;COUNT=15",
        Categorize: "2,3,6"
    }, {
        Id: 108,
        Subject: "Deadest Catch",
        StartTime: new Date(2015, 11, 3, 16, 00),
        EndTime: new Date(2015, 11, 3, 17, 00),
        Description: "",
        AllDay: false,
        Recurrence: false,
        Categorize: "2,4,6,1"
    }, {
        Id: 109,
        Subject: "MayDay",
        StartTime: new Date(2015, 3, 30, 06, 30),
        EndTime: new Date(2015, 3, 30, 07, 30),
        Description: "",
        AllDay: false,
        Recurrence: false,
        Categorize: "5,3"
    }, {
        Id: 115,
        Subject: "Cash Cab",
        StartTime: new Date(2015, 3, 30, 15, 00),
        EndTime: new Date(2015, 3, 30, 16, 30),
        Description: "",
        AllDay: false,
        Recurrence: true,
        RecurrenceRule: "FREQ=DAILY;INTERVAL=1;COUNT=5",
        Categorize: "1,3"
    }
];

$(function() {
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

## Customize the Default Appointment Window

Apart from the custom appointment window, it is possible to customize the default appointment window by adding/removing the required number of fields into it. This can be achieved through the **create** event of the scheduler.

The following code example depicts the way to achieve the customization of default appointment window.

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="Schedule1"></div>

<script type="text/javascript">

$(function() {
    // For Scheduler
    $("#Schedule1").ejSchedule({
        currentDate: new Date(2015, 11, 2),
        showCurrentTimeIndicator: false,
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

// This function executes before the appointment window gets opened.
function onAppointmentOpen(args) {
    // to add custom element in default appointment window
    if (this._appointmentAddWindow.find(".custom-fields").length == 0) {
	    var customDesign = "<tr class='custom-fields'><td class='e-textlabel'>Event Type</td><td><input class='app-type' type='text'/></td><td class='e-textlabel'>Event Status </td><td><input class='status' type='text'/></td></tr>";
		$(customDesign).insertAfter(this._appointmentAddWindow.find("." + this._id + "appointmentArrow"));
    }
            
	if (!ej.isNullOrUndefined(args.appointment)) {
	    // if double clicked on the appointments, retrieve the custom field values from the appointment object and fills it in the appropriate fields.               this._appointmentAddWindow.find(".app-type").val(args.appointment.AppointmentType);
		this._appointmentAddWindow.find(".status").val(args.appointment.Status);
	} else {
	    // if double clicked on the cells, clears the field values.               
		this._appointmentAddWindow.find(".app-type").val("");
		this._appointmentAddWindow.find(".status").val("");
	}
}

</script>

{% endhighlight %}

## Synchronize the Schedule with Outlook

Schedule appointments can be synchronized with Outlook and vice versa, by making use of the Microsoft Outlook 12/15 Object library. 

The following code example depicts the way to synchronize the Schedule with Outlook.

{% highlight html %}

<body>
    <div class="content-container-fluid">
        <div class="row">
            <div class="cols-sample-area">
                <div style="float: left" id="Schedule1">
                </div>
            </div>
        </div>
        <script type="text/javascript">
            $(function () {
                var dataManager = ej.DataManager({
                    url: '@Url.Action("GetApp", "Home")',
                    crudUrl: '@Url.Action("Batch","Home")',
                    crossDomain: true
                });
                dataManager.adaptor = new ej.UrlAdaptor();
                $("#Schedule1").ejSchedule({
                    width: "100%",
                    height: "525px",
                    currentDate: new Date(2015, 5, 15),
                    appointmentSettings: {
                        dataSource: dataManager,
                        id: "Id",
                        subject: "Subject",
                        startTime: "StartTime",
                        endTime: "EndTime",
                        startTimeZone: "StartTimeZone",
                        endTimeZone: "EndTimeZone",
                        allDay: "AllDay",
                        recurrence: "Recurrence",
                        recurrenceRule: "RecurrenceRule"
                    }
                });

            });
        </script>
</body>

{% endhighlight %}

Schedule control is not directly compatible with the Outlook calendar object, as it returns the COM object. Therefore, in order to bind the schedule control with those data retrieved from outlook, then it is necessary to convert the COM object into the schedule acceptable object format. To do so add the following code example in your code behind. 
 
{% highlight c# %}

using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.Mvc;
using System.ComponentModel;
using System.Configuration;
using System.Data;
using System.Data.SqlClient;
using Microsoft.Office.Interop.Outlook; // required Microsoft Assembly 
using System.Web.Script.Serialization;
using System.Web.UI;
using System.Web.UI.WebControls;
using ScheduleCRUDJS.Models;
using System.Collections;
namespace ScheduleCRUDJS.Controllers
{
    public class HomeController : Controller
    {
        ScheduleDataDataContext db = new ScheduleDataDataContext();

        public ActionResult Index()
        {
            return View();
        }

        [HttpPost]
        public JsonResult GetApp() // function to display the outlook appointments in Schedule initially
        {
            IEnumerable data = GetData(); 
            return Json(data, JsonRequestBehavior.AllowGet);
        }
        public List<MultipleResource> GetData() // function to return the outlook appointments
        {
            Microsoft.Office.Interop.Outlook.Application oApp = new Microsoft.Office.Interop.Outlook.Application();
            Microsoft.Office.Interop.Outlook.NameSpace mapNamespace = oApp.GetNamespace("MAPI");
            Microsoft.Office.Interop.Outlook.MAPIFolder CalendarFolder = mapNamespace.GetDefaultFolder(Microsoft.Office.Interop.Outlook.OlDefaultFolders.olFolderCalendar);
            Microsoft.Office.Interop.Outlook.Items outlookCalendarItems = CalendarFolder.Items;
            List<Microsoft.Office.Interop.Outlook.AppointmentItem> appointmentList = new List<Microsoft.Office.Interop.Outlook.AppointmentItem>();

            foreach (Microsoft.Office.Interop.Outlook.AppointmentItem item in outlookCalendarItems)
            {
                appointmentList.Add(item);
            }

            List<MultipleResource> newApp = new List<MultipleResource>();
            // converting COM object into IEnumerable object
            for (var i = 0; i < appointmentList.Count; i++)
            {
                MultipleResource app = new MultipleResource();
                app.Id = i;
                app.Subject = appointmentList[i].Subject;
                app.AllDay = appointmentList[i].AllDayEvent;
                app.StartTime = Convert.ToDateTime(appointmentList[i].Start.ToString());
                string endTime = appointmentList[i].End.ToString();
                DateTime appEndDate = Convert.ToDateTime(endTime);
                if (endTime.Contains("12:00:00 AM") && app.AllDay == true)
                    app.EndTime = appEndDate.AddMinutes(-1);
                else
                    app.EndTime = appEndDate;
                app.Recurrence = false;
                app.RecurrenceRule = null;
                newApp.Add(app);
            }
            return newApp;
        }
        public JsonResult Batch(EditParams param)
        {
            if (param.action == "insert" || (param.action == "batch" && param.added != null))          // this block of code will execute while inserting the appointments
            {
                var value = param.action == "insert" ? param.value : param.added[0];
                int intMax = db.MultipleResources.ToList().Count > 0 ? db.MultipleResources.ToList().Max(p => p.Id) : 1;
                DateTime startTime = Convert.ToDateTime(value.StartTime);
                DateTime endTime = Convert.ToDateTime(value.EndTime);
                MultipleResource appoint = new MultipleResource()
                {
                    Id = intMax + 1,
                    StartTime = startTime,
                    EndTime = endTime,
                    StartTimeZone = value.StartTimeZone,
                    EndTimeZone = value.EndTimeZone,
                    Subject = value.Subject,
                    OwnerId = value.OwnerId,
                    AllDay = value.AllDay,
                    Recurrence = value.Recurrence,
                    RecurrenceRule = value.RecurrenceRule
                };
                db.MultipleResources.InsertOnSubmit(appoint);
                db.SubmitChanges();
                Microsoft.Office.Interop.Outlook.Application outlookApp = new Microsoft.Office.Interop.Outlook.Application();
                Microsoft.Office.Interop.Outlook.AppointmentItem newAppointment = null;
                newAppointment = (Microsoft.Office.Interop.Outlook.AppointmentItem)outlookApp.CreateItem(Microsoft.Office.Interop.Outlook.OlItemType.olAppointmentItem);
                newAppointment.Start = Convert.ToDateTime(value.StartTime).ToUniversalTime();
                newAppointment.End = Convert.ToDateTime(value.EndTime).ToUniversalTime();
                newAppointment.Subject = value.Subject.ToString();
                newAppointment.Save();
            }
            IEnumerable data = new ScheduleDataDataContext().MultipleResources.Take(200);
            return Json(data, JsonRequestBehavior.AllowGet);
        }
    }
}

{% endhighlight %}

N> In order to achieve the above scenario, need to refer the Microsoft assembly in your application (Microsoft Outlook 12/15 Object library [Microsoft.Office.Interop.Outlook] and refer it in the controller page as shown above).