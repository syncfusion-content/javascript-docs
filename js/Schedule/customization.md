---
title: Schedule - Customization	
description: Customization of working hours, date, and appointment window
platform: js
control: schedule
documentation: ug
keywords: customization, work hours, appointment window, display hours 
---
# Customization

The Scheduler can be customized in various aspects like - 

* Setting different Start/end hour limits
* Highlighting the working hours 
* Setting different [date format](/js/schedule/globalization-and-localization#date-format)
* Specifying minimum and maximum date ranges 
* Customize the entire appointment window with the user required fields

## Hour Customization


It includes customization of displaying Scheduler with specific Start/End hours and also defining the working hour time range which is differentiated as business hours.

### Schedule Display Hours

It denotes the start and end hour time limits to be displayed on the Scheduler. To set this time limit, two properties namely [startHour](/js/api/ejschedule#members:starthour) and [endHour](/js/api/ejschedule#members:endhour) can be used. 

* **startHour** - Sets the start time. The hour from which the Scheduler time display actually starts.
* **endHour** - Sets the end time. The hour on which the Scheduler time display should end.

The following code example renders the scheduler from 7.00 AM to 6.00 PM.

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="Schedule1"></div>

<script type="text/javascript">
	$(function () {
		$("#Schedule1").ejSchedule({
			width: "100%",
			currentDate: new Date(2015, 04, 05),
			startHour: 7,
			endHour: 18,
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

### Working Hours

Working hours indicates the work hour limit within the Scheduler. To enable the highlighting of work hours on the Scheduler, set the **highlight** option available within the workHours property to **true**. By default, it is set to true. [workHour](/js/api/ejschedule#members:workhours) is a object property which contains the below specified options,

* **[highlight](/js/api/ejschedule#members:workhours-highlight)** – enables/disables the work hour highlighting functionality.
* **[start](/js/api/ejschedule#members:workhours-start)** - sets the time to be depicted as the start of the working/business hour in a day. 
* **[end](/js/api/ejschedule#members:workhours-end)** - sets the time limit to denote the end of the working/business hour in a day. 

The work hours are differentiated from other normal hours, by depicting the Scheduler cells in different color shade that belongs to this working hour time range. 

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="Schedule1"></div>

<script type="text/javascript">
	$(function () {
		$("#Schedule1").ejSchedule({
			workHours: {
				highlight: true,
				start: 8,
				end: 16
			},
			currentDate: new Date(2015,11,5),
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

N> By default, work hour **start** is set to **9** and work hour **end** is set to **18**. Also, the Scheduler cells automatically scrolls up or down based on the work start hour that is set to it, to make the user to view that particular time initially.

## Date Customization

The dates in the Scheduler can be customized by setting specific minimum and maximum date ranges and also defining various date formats to it.

### Current Date

The Current date indicates the date with which the Scheduler loads initially and based on which the appropriate date range displays in the week/workweek/month/agenda views. To set the current date to the Scheduler – use the following code example,

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="Schedule1"></div>

<script type="text/javascript">
	$(function () {
		$("#Schedule1").ejSchedule({
			currentDate: new Date(2015,11,5),
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

N> By default, the System current date will be taken as Scheduler’s Current date.

### MinDate and MaxDate

Providing the [minDate](/js/api/ejschedule#members:mindate) and [maxDate](/js/api/ejschedule#members:maxdate) property with some date values, allows the Scheduler to set the minimum and maximum date range. The Scheduler dates that lies beyond these minimum and maximum date range will be in a disabled state, so that the date navigation is blocked beyond these specified date range. Also, the appointments that belongs beyond these date ranges will not be displayed on the Scheduler.  

The following code example show how to set the minDate and maxDate properties of the Scheduler.

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="Schedule1"></div>

<script type="text/javascript">
	$(function () {
		$("#Schedule1").ejSchedule({
			minDate: new Date(2015,11,4),
			maxDate: new Date(2015,11,8),
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

N> The **maxDate** value provided should always be greater than that of **minDate** value.

## Appointment Window Customization

It is possible to use the custom appointment window option to design it with the user-required extra fields apart from the other default available fields. To make use of the customized appointment window, it is necessary to use the [appointmentWindowOpen](/js/api/ejschedule#events:appointmentwindowopen) event within which the display of default appointment window is prevented.

The following code example lets you create the custom appointment with a single extra field for defining the appointment type.

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="Schedule1"></div>

<div id="customWindow" style="display: none">
	<form id="custom">
		<table width="100%" cellpadding="5">
			<tbody>
				<tr style="display: none">
					<td>Id:</td>
					<td colspan="2"><input id="customId" type="text" name="Id" /></td>
				</tr>
				<tr>
					<td>Subject:</td>
					<td colspan="2"><input id="subject" type="text" value="" name="Subject" onfocus="temp()" style="width: 100%" /></td>
				</tr>
				<tr>
					<td>Description:</td>
					<td colspan="2"><textarea id="customdescription" name="Description" rows="3" cols="50" style="width: 100%; resize: vertical"></textarea></td>
				</tr>
				<tr>
					<td>StartTime:</td>
					<td><input id="StartTime" type="text" value="" name="StartTime" /></td>
				</tr>
				<tr>
					<td>EndTime:</td>
					<td><input id="EndTime" type="text" value="" name="EndTime" /></td>
				</tr>
				<tr>
					<td>Appointment Type:</td>
					<td><input type="text" id="AppointmentType" /></td>
				</tr>
				<tr>
					<td colspan="3">
						<div class="customcheck">AllDay:</div>
						<div class="customcheck">
							<input id="allday" type="checkbox" name="AllDay" onchange="alldayCheck()" />
						</div>
						<div class="customcheck">Recurrence:</div>
						<div><input id="recurrence" type="checkbox" name="Recurrence" onchange="recurCheck()" /></div>
					</td>
				</tr>
				<tr class="recurrence" style="display: none">
					<td>Type:</td>
					<td><select id="rType" name="freq">
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
		<button type="submit" onclick="cancel()" id="btncancel" style="float:right;margin-right:20px;margin-bottom:10px;">Cancel</button>
		<button type="submit" onclick="save()" id="btnsubmit"style="float:right;margin-right:20px;margin-bottom:10px;">Submit</button>
	</div>
</div>

{% endhighlight %}

The styles to be applied for the controls within the custom appointment window are as follows.

{% highlight html %}

<style>
	.customcheck {
		float: left;
		margin-right: 10px;
	}
	
	.error {
		background-color: #FF8A8A;
	}
	
	#custom table td {
		padding:5px;
	}
</style>

{% endhighlight %}

Now, define the Schedule control with custom window within script as shown below.

{% highlight html %}

<script>
	$(function () {
		// defining sub-controls used within custom appointment window
		$("#btncancel").ejButton({ width:'85px' });
		$("#btnsubmit").ejButton({ width:'85px'});
		$("#StartTime").ejDateTimePicker({ width: "150px" });
		$("#EndTime").ejDateTimePicker({ width: "150px" });
		// DataSource values for the appointment type field
		var types = [{ text: "Tentative", id: 1 },
					 { text: "Busy", id: 3 },
					 { text: "Free", id: 5 },
					 { text: "Out Of Office", id: 7 }];
		// defining dropdown controls to be used within custom appointment window
		$("#AppointmentType").ejDropDownList({
			dataSource: types,
			fields: { text: "text", id: "id", value: "text" }
		});
		// defining dialog control to be used as custom appointment window
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
					EndTime: new Date(2015, 11, 5, 11, 00),
					AppointmentType: "Busy"
				}]
			},
			appointmentWindowOpen: "onAppointmentWindowOpen"
		});
	});
</script>

{% endhighlight %}

The following function needs to be defined within script section, which gets called before the default appointment window opens.

{% highlight html %}

<script>
	function onAppointmentWindowOpen(args) {
		args.cancel = true; // prevents the display of default appointment window
		// When double clicked on the Scheduler cells, fills the StartTime and EndTime fields appropriately
		$("#StartTime").ejDateTimePicker({ value: args.startTime });
		$("#EndTime").ejDateTimePicker({ value: args.endTime });
		if(!ej.isNullOrUndefined(args.target)) {                
			// When double clicked on the Scheduler cells, if the target is allday or month cells – only then enable check mark on the allday checkbox
			if ($(args.target.currentTarget).hasClass("e-alldaycells"))
				$("#allday").prop("checked", true);
			else
				args.model.currentView == "month" ? $("#allday").prop("checked", true) : $("#allday").prop("checked", false);
			// If the target is allday or month cells – disable the StartTime and EndTime fields
			$("#StartTime,#EndTime").ejDateTimePicker({ enabled: ($(args.target.currentTarget).hasClass("e-alldaycells") || $(args.target.currentTarget).hasClass("e-monthcells")||args.model.currentView=="month") ? false : true });
		}
		
		// If double clicked on the appointments, fill the custom appointment window fields with appropriate values.
		if (!ej.isNullOrUndefined(args.appointment)) {
			$("#customId").val(args.appointment.Id);
			$("#subject").val(args.appointment.Subject);
			$("#customdescription").val(args.appointment.Description);
			$("#StartTime").ejDateTimePicker({ value: new Date(args.appointment.StartTime) });
			$("#EndTime").ejDateTimePicker({ value: new Date(args.appointment.EndTime) });
			// Fills the Appointment type dropdown with its value
			var value = args.appointment.AppointmentType;
			$("#AppointmentType").ejDropDownList("clearText");
			$("#AppointmentType").ejDropDownList({ text: value, value: value });
			$("#allday").prop("checked", args.appointment.AllDay);
			$("#recurrence").prop("checked", args.appointment.Recurrence);
			if(args.appointment.Recurrence) {
				$("#rType").val(args.appointment.RecurrenceRule.split(";")[0].split("=")[1].toLowerCase());
				$("tr.recurrence").css("display", "table-row");
			}
			$("#customWindow").ejDialog("open");
		}
		else
			$("#customWindow").ejDialog("open");
	}
</script>

{% endhighlight %}

On clicking the **Submit** button within the Custom Appointment window, the following function gets executed – which will validate the appointment fields and then save it appropriately.

{% highlight html %}

<script>
	function save() {
		// checks if the subject value is not left blank before saving it.
		if ($.trim($("#subject").val()) == "") {
			$("#subject").addClass("error");
			return false;
		}
		var obj = {}, temp = {}, rType;
		var formelement = $("#customWindow").find("#custom").get(0);
		// looping through the custom form elements to get each value and form a JSON object
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
		var appTypeObj = $("#AppointmentType").data("ejDropDownList");
		obj["AppointmentType"] = appTypeObj.getSelectedValue();
		$("#customWindow").ejDialog("close");
		var object = $("#Schedule1").data("ejSchedule");
		object.saveAppointment(obj);
		clearFields();
	}

	// Clears all the field values of the custom window after saving appointments
	function clearFields() {
		$("#customId").val("");
		$("#subject").val("");
		$("#customdescription").val("");
		$("#AppointmentType").val("");
		$("#allday").prop("checked", false);
		$("#recurrence").prop("checked", false);
		document.getElementById("rType").selectedIndex = "0";
		$("tr.recurrence").css("display", "none");
		$("#StartTime,#EndTime").ejDateTimePicker({ enabled: true });
	}

	// This function executes when the recurrence checkbox is checked in the custom appointment window
	function recurCheck() {
		// Displays the recurrence field, when recurrence checkbox is checked.
		if ($("#recurrence").get(0).checked == true)
			$("tr.recurrence").css("display", "table-row");
		else
			$("tr.recurrence").css("display", "none");
	}

	// This function executes when the All-day checkbox is checked in the custom appointment window
	function alldayCheck() {
		// Disables and sets the specific hours to the StartTime and EndTime fields, when the all-day checkbox is checked
		if ($("#allday").prop("checked")) {
			var a = $("#StartTime").data("ejDateTimePicker").model.value;
			a.setHours(0, 0, 0);
			var b = $("#EndTime").data("ejDateTimePicker").model.value;
			b.setHours(23, 59, 0);
			$("#StartTime").ejDateTimePicker({ value: new Date(a), enabled: false });
			$("#EndTime").ejDateTimePicker({ value: new Date(b), enabled: false });
		}
		else {
			$("#StartTime").ejDateTimePicker({ enabled: true });
			$("#EndTime").ejDateTimePicker({ enabled: true });
		}
	}

	// This function executes when the subject text field is currently being focussed
	function temp() {
		$("#subject").removeClass("error");
	}

	// This function executes when the cancel button in the custom appointment window is pressed.
	function cancel() {
		clearFields();
		$("#customWindow").ejDialog("close");
	}
</script>

{% endhighlight %}

