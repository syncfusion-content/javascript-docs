---
layout: post
title: Reminder
description: reminder
platform: js
control: Schedule
documentation: ug
---

# Reminder

* **Reminder** option provides the list of reminder appointments and you can use those appointments for your own customized scenarios like displaying it as an end-user notification. To enable the reminder settings for the **Schedule** control, you can set the **enable** property as ‘**true’** within the **reminderSettings** option. 

* The **reminderSettings** option includes another optional property **alertBefore** that accepts integer value to denote the time before how long the reminder is notified to the user.

* For such case, you can also use an in-built event **reminder** that triggers when there is a reminder appointment. It provides the details of the list of reminder appointment details.

The following code example explains how to get the reminder list and display it as a notification for users.



{% highlight js %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<title>Schedule JS Reminder options</title>
</head>
<body>
<!-- For Reminder list div elements-->
<div id="reminder" class="media" data-content=" ">
<a class="pull-left" href="#" style="margin-top: 9px; outline: medium none;">
<div class="reminder-icon"></div>
<span id="reminderCount" class="badge badge-success pull-right">0</span>
</a>
</div>

<!-- Notification div element-->
<div class='notifications top-right'></div>

<!-- Schedule div element-->
<div style="float: left" id="Schedule1">
</div>
<div id="Schedule1"> </div>

<!-- Styles applied for the reminder list divs and notification -->
<style>
#reminderCount
{
position: relative;
min-width: 6px;
top: -36px;
left: 10px;
background-color: #FF0000;
}
#reminder
{
width: 50px;
height: 40px;
margin-top: 1px;
float: right;
}
.reminder-icon
{
background: url("../images/schedule/bell.png") no-repeat scroll 8px 6px rgba(0, 0, 0, 0);
border: 1px solid #BBBCBB;
height: 28px;
width: 28px;
border-radius: 6px;
}
.popover.bottom .arrow
{
margin-top: 0px;
}
.popover
{
width: 300px;
}
.outerDiv
{
border-bottom: 1px solid #BBBCBB;
padding-bottom: 5px;
}
.notifications.top-right
{
top: 25% !important;
}
</style>

<script type="text/javascript">
$(function () {
var dManager = ej.DataManager(window.Default).executeLocal(ej.Query().take(10));
$("#Schedule1").ejSchedule({
width: "100%",
height: "500px",
reminder: "ongetReminderList",
reminderSettings: {
enable: true
},
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

//Append the reminder list to the Schedule header
$("#Schedule1").find("tr.e-scheduleheader td").first().append($("#reminder"));

// Reminder list load to the popover control
$("#reminder").popover({ placement: 'bottom' });

//popover content has been updated
$('#reminder').on('shown.bs.popover', function () {
if (parseInt($("#reminderCount").text()) == 0)
return false;
$(".popover-content").html($_remList);
$(".outerDiv .close").on("click", function () {
$(this).parents(".outerDiv").remove();
$_remList = $(".popover-content").html();
$("#reminderCount").html(parseInt($("#reminderCount").text()) - 1);
checkList();
});
$(".outerDiv").on("mouseover", function () {
$(this).find(".close").show();
});
$(".outerDiv").on("mouseout", function () {
$(this).find(".close").hide();
});
});
});

function checkList() {
if (parseInt($("#reminderCount").text()) == 0)
$("#reminderCount").hide();
else
$("#reminderCount").show();
}
var $_remList = "";

function ongetReminderList(args) {
$("#reminderCount").html(parseInt($("#reminderCount").text()) + 1);
checkList();
$_remList += "<div class='outerDiv'><span class='e-quicksubject'>" + args.reminderAppointment.Subject +
"</span><div class='e-quickstartendtime'>" + args.reminderAppointment.StartTime +
"</div><a class='close pull-right' href='#' style='margin-top: -56px;display: none;'>×</a></div>";
var notifiList = "<div><span class='e-quicksubject'>" + args.reminderAppointment.Subject +
"</span><div class='e-quickstartendtime'>" + args.reminderAppointment.StartTime +
"</div></div>";

// Show the notification div
$('.top-right').notify({
message: { html: notifiList },
type: "info",
fadeOut: {
enabled: false
}
}).show();
}
</script>
</body>
</html>



{% endhighlight %}



Execute the above code to render the following output.



![](Reminder_images/Reminder_img1.png)
{:.image }


{:.caption }


___Figure_ _106__:___ _schedule with_ _Reminder._



