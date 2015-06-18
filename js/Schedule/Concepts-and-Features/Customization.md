---
layout: post
title: Customization
description: customization
platform: js
control: Schedule
documentation: ug
---

# Customization

## Customized Appointment window 

* You can display your own customized appointment window instead of the default appointment window while double-clicking on the cells. To achieve this, you can use the event **appointmentWindowOpen**. 

* The customized window is designed with the dialog control separately.

This example explains you on how to add the customized appointment window using the following code example.



{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title>Schedule JS Default Functionalities</title>
    //Refer the required script files here


</head>

<body>
    <!-- Schedule div-->
    <div id="Div1">
    </div>

    <!-- div For Customized appointment window dialog-->
    <div id="**customWindow**" style="display: none">
        <form id="custom">
            <table width="100%" cellpadding="5">
                <tbody>
                    <tr style="display: none">
                        <td>Id:
                        </td>
                        <td colspan="2">
                            <input id="customId" type="text" name="Id" />
                        </td>
                    </tr>
                    <tr>
                        <td>Subject:
                        </td>
                        <td colspan="2">
                            <input id="subject" type="text" value="" name="Subject" onfocus="temp()" style="width: 100%" />
                        </td>
                    </tr>
                    <tr>
                        <td>Description:
                        </td>
                        <td colspan="2">
                            <textarea id="customdescription" name="Description" rows="3" cols="50" style="width: 100%; resize: vertical"></textarea>
                        </td>
                    </tr>
                    <tr>
                        <td>StartTime:
                        </td>
                        <td>
                            <input id="StartTime" type="text" value="" name="StartTime" />
                        </td>
                    </tr>
                    <tr>
                        <td>EndTime:
                        </td>
                        <td>
                            <input id="EndTime" type="text" value="" name="EndTime" />
                        </td>
                    </tr>
                    <tr>
                        <td colspan="3">
                            <div class="customcheck">AllDay:</div>
                            <div class="customcheck">
                                <input id="allday" type="checkbox" name="AllDay" onchange="alldayCheck()" />
                            </div>
                            <div class="customcheck">Recurrence:</div>
                            <div>
                                <input id="recurrence" type="checkbox" name="Recurrence" onchange="recurCheck()" />
                            </div>
                        </td>
                    </tr>
                    <tr class="recurrence" style="display: none">
                        <td>Type:
                        </td>
                        <td>
                            <select id="rType" name="freq">
                                <option value="daily">Daily</option>
                                <option value="weekly">Weekly</option>
                                <option value="monthly">Monthly</option>
                                <option value="yearly">Yearly</option>
                            </select>
                        </td>
                    </tr>
                </tbody>
            </table>
        </form>
        <div>
            <button type="submit" onclick="save()">
                Submit</button>
            <button type="submit" onclick="cancel()">
                Cancel</button>
        </div>
    </div>
</body>
</html>

{% endhighlight %}

{% highlight css %}

// Styles to be used for the control within the custom appointment window

.customcheck {
float: left;
margin-right: 10px;
}

.error {
background-color: #FF8A8A;
}

{% endhighlight %}

{% highlight js %}

 $(function () {

        // For schedule control
        var dManager = window.Startend;
        $("#Schedule1").ejSchedule({
            width: "100%",
            height: "525px",
            appointmentSettings: {
                dataSource: dManager,
                id: "Id",
                subject: "Subject",
                startTime: "StartTime",
                endTime: "EndTime",
                allDay: "AllDay",
                recurrence: "Recurrence",
                recurrenceRule: "RecurrenceRule"
            },
           appointmentWindowOpen: "onAppointmentWindowOpen"
        });

        // For sub-controls used within the custom appointment window
        $("#StartTime").ejDateTimePicker({ width: "150px" });
        $("#EndTime").ejDateTimePicker({ width: "150px" });

        // For dialog control which is to be used as customized appointment window
        $("#customWindow").ejDialog({
            width: 600,
            height: "auto",
            position: { X: 200, Y: 100 },
            showOnInit: false,
            enableModal: true,
            title: "Create Appointment",
            enableResize: false,
            allowKeyboardNavigation: false,
            close: "clearFields"
        });

    });

    // this method called before the default appointment window gets opened.
    function onAppointmentWindowOpen(args) {

        // setting true for args.cancel will prevent the opening of default appointment window
        args.cancel = true;

        var quickobj = $("#Schedule1AppointmentQuickWindow").data("ejDialog");
        quickobj.close();
        $("#StartTime").ejDateTimePicker({ value: args.startTime });
        $("#EndTime").ejDateTimePicker({ value: args.endTime });
        if(!ej.isNullOrUndefined(args.target)){
            if ($(args.target.currentTarget).hasClass("e-alldaycells"))
                $("#allday").prop("checked", true);
        }
        // To open the custom appointment window
        $("#customWindow").ejDialog("open");
    }

    // Function called while clicking the submit button on the appointment window
    function save() {
        if ($("#subject").val().trim() == "") {
            $("#subject").addClass("error");
            return false;
        }
        var obj = {}, temp = {}, rType;
        formelement = $("#customWindow").find("#custom").get(0);
        for (var index = 0; index < formelement.length; index++) {
            var columnName = formelement[index].name, $element = $(formelement[index]);
            if (columnName != undefined) {
                if (columnName == "")
                    columnName = formelement[index].id.replace(this._id, "");
                if (columnName != "" && obj[columnName] == null) {
                    var value = formelement[index].value;
                    if (columnName == "Id" && value != "")
                        value = parseInt(value);
                    if ($element.hasClass("e-datetimepicker"))
                        value = new Date(value);
                    if (formelement[index].type == "checkbox")
                        value = formelement[index].checked;
                    if (columnName == "freq") {
                        if (formelement[index].type == "select-one") {
                            rType = document.getElementById("rType");
                            temp[columnName] = rType.options[rType.selectedIndex].value;
                        }
                    }
                    obj[columnName] = value;
                }
            }
        }
        if (obj.Recurrence) {
            if (temp.freq.toUpperCase() == "DAILY")
                obj["RecurrenceRule"] = "FREQ=DAILY;INTERVAL=1;COUNT=5";
            else if (temp.freq.toUpperCase() == "WEEKLY")
                obj["RecurrenceRule"] = "FREQ=WEEKLY;BYDAY=MO,WE,TH;INTERVAL=1;COUNT=10";
            else if (temp.freq.toUpperCase() == "MONTHLY")
                obj["RecurrenceRule"] = "FREQ=MONTHLY;BYMONTHDAY=" + obj.StartTime.getDate() + ";INTERVAL=1;COUNT=5";
            else if (temp.freq.toUpperCase() == "YEARLY")
                obj["RecurrenceRule"] = "FREQ=YEARLY;BYMONTHDAY=" + obj.StartTime.getDate() + ";BYMONTH=" + (obj.StartTime.getMonth() + 1) + ";INTERVAL=1;COUNT=3";
        }
        else
            obj["RecurrenceRule"] = null;
        $("#customWindow").ejDialog("close");
        var object = $("#Schedule1").data("ejSchedule");

        // Saves the appointment object to the schedule control
        object.saveAppointment(obj);
        clearFields();
    }

    function clearFields() {
        $("#customId").val("");
        $("#subject").val("");
        $("#customdescription").val("");
        $("#allday").prop("checked", false);
        $("#recurrence").prop("checked", false);
        document.getElementById("rType").selectedIndex = "0";
        $("tr.recurrence").css("display", "none");
    }

    function recurCheck() {
        if ($("#recurrence").get(0).checked == true)
            $("tr.recurrence").css("display", "table-row");
        else
            $("tr.recurrence").css("display", "none");
    }

    function alldayCheck() {
        $("#StartTime,#EndTime").ejDateTimePicker({ enabled: ($("#allday").prop("checked")) ? false : true });
    }

    function temp() {
        $("#subject").removeClass("error");
    }

    function cancel() {
        clearFields();
        $("#customWindow").ejDialog("close");
    }

{% endhighlight %}

Execute the above code and then double-click on the required **Schedule** cells. The customized appointment window is opened instead of the default appointment window as follows.

{% include image.html url="/js/Schedule/Customization_images/Customization_img1.png" Caption="schedule with Customized appointment window."%}


* Add the required details on the above displayed appointment window and then click **Submit** button to save the appointment.


## Editing Customized Appointment window

* To edit the appointments in customized appointment window, you can use **appointmentWindowOpen** event to avoid displaying the default appointment window when you double-click the appointments. 

* The customized window is designed with the dialog control separately and it is display when you double-click appointments. 

The following code example is added to the previous code example of appointment creation for Customized Appointment window.


{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title>Schedule JS Default Functionalities</title>

</head>

<body>
    <!-- Schedule div-->
    <div id="Div1">
    </div>

    <!-- div For Customized appointment window dialog-->
    <div id="**customWindow**" style="display: none">
        <form id="custom">
            <table width="100%" cellpadding="5">
                <tbody>
                    <tr style="display: none">
                        <td>Id:
                        </td>
                        <td colspan="2">
                            <input id="customId" type="text" name="Id" />
                        </td>
                    </tr>
                    <tr>
                        <td>Subject:
                        </td>
                        <td colspan="2">
                            <input id="subject" type="text" value="" name="Subject" onfocus="temp()" style="width: 100%" />
                        </td>
                    </tr>
                    <tr>
                        <td>Description:
                        </td>
                        <td colspan="2">
                            <textarea id="customdescription" name="Description" rows="3" cols="50" style="width: 100%; resize: vertical"></textarea>
                        </td>
                    </tr>
                    <tr>
                        <td>StartTime:
                        </td>
                        <td>
                            <input id="StartTime" type="text" value="" name="StartTime" />
                        </td>
                    </tr>
                    <tr>
                        <td>EndTime:
                        </td>
                        <td>
                            <input id="EndTime" type="text" value="" name="EndTime" />
                        </td>
                    </tr>
                    <tr>
                        <td colspan="3">
                            <div class="customcheck">AllDay:</div>
                            <div class="customcheck">
                                <input id="allday" type="checkbox" name="AllDay" onchange="alldayCheck()" />
                            </div>
                            <div class="customcheck">Recurrence:</div>
                            <div>
                                <input id="recurrence" type="checkbox" name="Recurrence" onchange="recurCheck()" />
                            </div>
                        </td>
                    </tr>
                    <tr class="recurrence" style="display: none">
                        <td>Type:
                        </td>
                        <td>
                            <select id="rType" name="freq">
                                <option value="daily">Daily</option>
                                <option value="weekly">Weekly</option>
                                <option value="monthly">Monthly</option>
                                <option value="yearly">Yearly</option>
                            </select>
                        </td>
                    </tr>
                </tbody>
            </table>
        </form>
        <div>
            <button type="submit" onclick="save()">
                Submit</button>
            <button type="submit" onclick="cancel()">
                Cancel</button>
        </div>
    </div>
</body>
</html>
{% endhighlight %}


{% highlight css %}

.customcheck {
float: left;
margin-right: 10px;
}

.error {
background-color: #FF8A8A;
}

{% endhighlight %}

{% highlight js %}

$(function () {

        // For schedule control
        var dManager = window.Startend;
        $("#Schedule1").ejSchedule({
            width: "100%",
            height: "525px",
            currentDate: new Date (2014,4,5),
            appointmentSettings: {
                dataSource: dManager,
                id: "Id",
                subject: "Subject",
                startTime: "StartTime",
                endTime: "EndTime",
                allDay: "AllDay",
                recurrence: "Recurrence",
                recurrenceRule: "RecurrenceRule"
            },
        **appointmentWindowOpen: "onAppointmentWindowOpen"**
        });

        // For sub-controls used within the custom appointment window
        $("#StartTime").ejDateTimePicker({ width: "150px" });
        $("#EndTime").ejDateTimePicker({ width: "150px" });

        // For dialog control which is to be used as customized appointment window
        $("#customWindow").ejDialog({
            width: 600,
            height: "auto",
            position: { X: 200, Y: 100 },
            showOnInit: false,
            enableModal: true,
            title: "Create Appointment",
            enableResize: false,
            allowKeyboardNavigation: false,
            close: "clearFields"
        });

    });

    // this method called before the default appointment window gets opened.
    function onAppointmentWindowOpen(args) {

        // setting true for args.cancel will prevent the opening of default appointment window
        args.cancel = true;

        var quickobj = $("#Schedule1AppointmentQuickWindow").data("ejDialog");
        quickobj.close();
        $("#StartTime").ejDateTimePicker({ value: args.startTime });
        $("#EndTime").ejDateTimePicker({ value: args.endTime });
        if(!ej.isNullOrUndefined(args.target)){
            if ($(args.target.currentTarget).hasClass("e-alldaycells"))
                $("#allday").prop("checked", true);
        }

        if (!ej.isNullOrUndefined(args.appointment)) {
            // Opens the custom appointment window with filled-in details, when double-clicked on the appointments
              $("#customId").val(args.appointment.Id);
              $("#subject").val(args.appointment.Subject);
              $("#customdescription").val(args.appointment.Description);
              $("#StartTime").ejDateTimePicker({ value: new Date(args.appointment.StartTime) });
              $("#EndTime").ejDateTimePicker({ value: new Date(args.appointment.EndTime) });
              $("#allday").prop("checked", args.appointment.AllDay);
              $("#recurrence").prop("checked", args.appointment.Recurrence);
              if(args.appointment.Recurrence){
              $("#rType").val(args.appointment.RecurrenceRule.split(";")[0].split("=")[1].toLowerCase());
              $("tr.recurrence").css("display", "table-row");
              }
              $("#customWindow").ejDialog("open");
            }
        else // Opens the custom appointment window when double clicked on the schedule cells.
            $("#customWindow").ejDialog("open");
    }

    // Function called while clicking the submit button on the appointment window
    function save() {
        if ($("#subject").val().trim() == "") {
            $("#subject").addClass("error");
            return false;
        }
        var obj = {}, temp = {}, rType;
        formelement = $("#customWindow").find("#custom").get(0);
        for (var index = 0; index < formelement.length; index++) {
            var columnName = formelement[index].name, $element = $(formelement[index]);
            if (columnName != undefined) {
                if (columnName == "")
                    columnName = formelement[index].id.replace(this._id, "");
                if (columnName != "" && obj[columnName] == null) {
                    var value = formelement[index].value;
                    if (columnName == "Id" && value != "")
                        value = parseInt(value);
                    if ($element.hasClass("e-datetimepicker"))
                        value = new Date(value);
                    if (formelement[index].type == "checkbox")
                        value = formelement[index].checked;
                    if (columnName == "freq") {
                        if (formelement[index].type == "select-one") {
                            rType = document.getElementById("rType");
                            temp[columnName] = rType.options[rType.selectedIndex].value;
                        }
                    }
                    obj[columnName] = value;
                }
            }
        }
        if (obj.Recurrence) {
            if (temp.freq.toUpperCase() == "DAILY")
                obj["RecurrenceRule"] = "FREQ=DAILY;INTERVAL=1;COUNT=5";
            else if (temp.freq.toUpperCase() == "WEEKLY")
                obj["RecurrenceRule"] = "FREQ=WEEKLY;BYDAY=MO,WE,TH;INTERVAL=1;COUNT=10";
            else if (temp.freq.toUpperCase() == "MONTHLY")
                obj["RecurrenceRule"] = "FREQ=MONTHLY;BYMONTHDAY=" + obj.StartTime.getDate() + ";INTERVAL=1;COUNT=5";
            else if (temp.freq.toUpperCase() == "YEARLY")
                obj["RecurrenceRule"] = "FREQ=YEARLY;BYMONTHDAY=" + obj.StartTime.getDate() + ";BYMONTH=" + (obj.StartTime.getMonth() + 1) + ";INTERVAL=1;COUNT=3";
        }
        else
            obj["RecurrenceRule"] = null;
        $("#customWindow").ejDialog("close");
        var object = $("#Schedule1").data("ejSchedule");

        // Saves the appointment object to the schedule control
        object.saveAppointment(obj);
        clearFields();
    }

    function clearFields() {
        $("#customId").val("");
        $("#subject").val("");
        $("#customdescription").val("");
        $("#allday").prop("checked", false);
        $("#recurrence").prop("checked", false);
        document.getElementById("rType").selectedIndex = "0";
        $("tr.recurrence").css("display", "none");
    }

    function recurCheck() {
        if ($("#recurrence").get(0).checked == true)
            $("tr.recurrence").css("display", "table-row");
        else
            $("tr.recurrence").css("display", "none");
    }

    function alldayCheck() {
        $("#StartTime,#EndTime").ejDateTimePicker({ enabled: ($("#allday").prop("checked")) ? false : true });
    }

    function temp() {
        $("#subject").removeClass("error");
    }

    function cancel() {
        clearFields();
        $("#customWindow").ejDialog("close");
    }


{% endhighlight %}





* Only the bolded texts in the above code examples are added to open the custom appointment window when you double-click the appointments. Execute the above code and then double-click on the appointment, the custom appointment window is displayed as follows.

{% include image.html url="/js/Schedule/Customization_images/Customization_img2.png" Caption="schedule with appointment using customized appointment window."%}


* You can change the details in the above window and then click **Submit** button to save the updated values.


## Hour Customization

**Schedule Start/End Hour**

You can customize the appearance of the **Schedule** control by setting the specific start and end hour to it. To set the specific start/end hour for a **Schedule** control, the following properties are required to be used.

**startHour**

* Specify the start hour to set for the **Schedule** control.

**endHour**

* Specify the end hour to set for the **Schedule** control.


{% highlight html %}

<div id="Schedule1"></div>

{% endhighlight %}


{% highlight js %}

 $(function () {
        $("#Schedule1").ejSchedule({
            width: "100%",
            height: "525px",
            // setting the schedule start and end hour
          startHour: 8,
          endHour: 18
        });
    });


{% endhighlight %}



Execute the above code to render the output as follows with the **Schedule** control beginning with 08.00am and ending with 06.00pm.

{% include image.html url="/js/Schedule/Customization_images/Customization_img3.png" Caption="schedule with hour customization."%}


**Business hours**

* There is an option **highlightBusinessHours** in the **Schedule** control to enable/disable the action of highlighting the business hours. 

* It is controlled with two additional options **businessStartHour** and **businessEndHour** to specify the time range to be defined as the business hours. By default, the business hours are highlighted in the **Schedule** control.

**businessStartHour**

* It allows you to specify the start time to indicate the business start hour.

**businessEndHour**

* It allows you to specify the end time to indicate the business end hour.





* To enable the **highlightBusinessHours** and to customize the business start and end hours, refer the following code example.

{% highlight html %}

<div id="Schedule1"></div>

{% endhighlight %}


{% highlight js %}

$(function () {
        var dManager =
        ej.DataManager(window.Default).executeLocal(ej.Query().take(10));

        $("#Schedule1").ejSchedule({
            width: "100%",
            height: "525px",
            appointmentSettings: {
                dataSource: dManager,
                id: "Id",
                subject: "Subject",
                startTime: "StartTime",
                endTime: "EndTime",
                allDay: "AllDay",
                recurrence: "Recurrence",
                recurrenceRule: "RecurrenceRule"
            },
          highlightBusinessHours: true,
            // setting the business start and end hour to be highlighted in the schedule.
          BusinessStartHour: 10,
          BusinessEndHour: 3
        });
    });


{% endhighlight %}


Execute the above code to render the following output that explains the highlighting of business hours in the **Schedule** control from 10.00am to 3.00pm.

{% include image.html url="/js/Schedule/Customization_images/Customization_img4.png" Caption="schedule with Business hours."%}


## Date/Time Customization

**Current date**

* By default, the **Schedule** control displays the current system date. 

* You can change the current date of the **Schedule** control by setting the **currentDate** option with the required date value. 

The following code example explains how to change the current date of the **Schedule** control.

{% highlight html %}

<div id="Schedule1"></div>

{% endhighlight %}


{% highlight js %}
 $(function () {
        var dManager =
        ej.DataManager(window.Default).executeLocal(ej.Query().take(10));

        $("#Schedule1").ejSchedule({
            width: "100%",
            height: "525px",
            currentDate: new Date(2014,04,05),
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



{% endhighlight %}



Execute the above code and the following screenshot displays the **Schedule** control with the current date set to (May 05, 2014).

{% include image.html url="/js/Schedule/Customization_images/Customization_img5.png" Caption="schedule with  current time."%}

**Date Format**

* The **Schedule** control uses different types of date formats to denote the dates used in it. You can specify your required format for the dates by using the **dateFormat** property. 

* When the date format is explicitly defined with particular value such as “**dd-MM-yyyy**”, then the **datepicker** control that is used within the **Schedule** control make use of this specific format.

The following code example explains how to change the **dateFormat** of the **Schedule** control.  

{% highlight html %}

<div id="Schedule1"></div>

{% endhighlight %}



{% highlight js %}
$(function () {
        var dManager = ej.DataManager(window.Default).executeLocal(ej.Query().take(10));
        $("#Schedule1").ejSchedule({
            width: "100%",
            height: "525px",

            // Setting the dateFormat to the schedule

            dateFormat:"dd-MM-yyyy",
            currentDate: "19-11-2014",
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


{% endhighlight %}



The following screenshot displays the **Schedule** control with the **dateFormat** set as “**dd-MM-yyyy**”.

{% include image.html url="/js/Schedule/Customization_images/Customization_img6.png" Caption="schedule with  dateformat set as dd-MM-yyyy."%}


**Minimum and Maximum Dates**

* This feature allows you to specify the minimum and maximum dates for the **Schedule** control. It can be defined with the **minDate** and **maxDate** properties. 

* Specifying minimum and maximum dates is especially useful when scheduling appointments for a project with fixed start and end dates.

* When these minimum and maximum dates are set, the dates apart from the specified range act as invalid/disabled dates and navigation beyond those dates are not possible.

The following code example explains how to set the minimum and maximum date of the **Schedule** control.  

{% highlight html %}

<div id="Schedule1"></div>

{% endhighlight %}

{% highlight js %}
$(function () {
        var dManager = ej.DataManager(window.Default).executeLocal(ej.Query().take(10));
        $("#Schedule1").ejSchedule({
            width: "100%",
            height: "525px",
            // Sets minimum and maximum date to the schedule.
            minDate:new Date("11/25/2014"),
            maxDate:new Date("12/4/2014"),
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



{% endhighlight %}



The following screenshot displays the **Schedule** control with **MinDate** and **MaxDate** set to **11/25/2014** and **12/4/2014,** respectively.

{% include image.html url="/js/Schedule/Customization_images/Customization_img7.png" Caption="schedule with Min and Max Dates set to 11/25/2014 and 12/4/2014 respectively."%}


**Timemode**

* You can set two types of time mode, either 12 or 24 hour format for the **Schedule** control.  It accepts the following enum values,

  * ej.Schedule.TimeMode.Hour12

  * ej.Schedule.TimeMode.Hour24

* Set the **Schedule** control to 24 hour time mode using the following code example.


{% highlight html %}

<div id="Schedule1"></div>

{% endhighlight %}


{% highlight js %}
 $(function () {
        $("#Schedule1").ejSchedule({
            // setting the 24 hour mode for the schedule
         timeMode: ej.Schedule.TimeMode.Hour24,
});
    });

{% endhighlight %}


The following screenshot displays the **Schedule** control when time mode is set to 24 hour mode.

{% include image.html url="/js/Schedule/Customization_images/Customization_img8.png" Caption="schedule with time customization."%}


**TimeZone**

* Appointments within the **Schedule** control is displayed based on the provided timezone. 

* If no specific timezones are set for the **Schedule** control, then it takes the local system timezone into consideration.

* [Click here](http://en.wikipedia.org/wiki/List_of_tz_database_time_zones) to see the complete list of supported timezones.



You can set the timezone to the **Schedule** control as follows.

{% highlight html %}

<div id="Schedule1"></div>

{% endhighlight %}

{% highlight js %}

 $(function () {
            var dManager =
            ej.DataManager(window.Default).executeLocal(ej.Query().take(10));
            $("#Schedule1").ejSchedule({
                width: "100%",
                height: "525px",
                // setting the timezone to be followed in the schedule
                timeZone: "UTC +2:00",
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



{% endhighlight %}



* Add new appointments to the **Schedule** control. The appointments are rendered based on the time difference that tends to the timezone set to it.

{% include image.html url="/js/Schedule/Customization_images/Customization_img9.png" Caption="schedule with timezone."%}


* In the above output, an appointment is initially created in the time-range 7.00am - 8.30am, it is saved in the timeslot between 9.00am – 10.30 am due to the time zone set to “UTC +2:00” in the **Schedule** control.


**Current Time indicator**

* The **current time indicator** denotes the current system time and it is marked on the **Schedule** control with a horizontal line drawn across the current date. 

* The **showCurrentTimeIndicator** property allows you to show/hide the time indicator on the **Schedule** control.

The following screenshot displays the **Schedule** control with the current time indicator marked with 5.41 AM across the date 30 April, 2014,


{% include image.html url="/js/Schedule/Customization_images/Customization_img10.png" Caption="schedule with time customization."%}

The following code example explains how to disable the current time indicator from the **Schedule** control. 

{% highlight html %}

<div id="Schedule1"></div>

{% endhighlight %}

{% highlight js %}

 $(function () {
        var dManager =
        ej.DataManager(window.Default).executeLocal(ej.Query().take(10));

        $("#Schedule1").ejSchedule({
            width: "100%",
            height: "525px",
            showCurrentTimeIndicator: false,
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


{% endhighlight %}



* After setting **showCurrentTimeIndicator** property to ‘false’, the **Schedule** control is displayed without the current time indicator as follows.

{% include image.html url="/js/Schedule/Customization_images/Customization_img11.png" Caption="schedule with show current time indicator."%}

