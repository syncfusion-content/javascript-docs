## Data Binding

### Appointment Fields

The below listed names are the appointment fields which holds the appropriate column names from the dataSource.

<table>
<tr>
<th>
Field name<br/><br/></th><th>
Description<br/><br/></th></tr>
<tr>
<td>
**id**<br/><br/></td><td>
Binds the id field name for indexing and performing CRUD operation on the appointments. It’s optional.<br/><br/></td></tr>
<tr>
<td>
**startTime**<br/><br/></td><td>
Binds the appointment start time field name which is **mandatory**.<br/><br/></td></tr>
<tr>
<td>
**startTimeZone**<br/><br/></td><td>
Binds the name of the start timezone field in the dataSource. If the startTimeZone field is not mentioned, then the appointment makes use of the **Scheduler** **timeZone** **or** **System** **timeZone**.<br/><br/></td></tr>
<tr>
<td>
**endTime**<br/><br/></td><td>
Binds the appointment end time field name which is **mandatory**.<br/><br/></td></tr>
<tr>
<td>
**endTimeZone**<br/><br/></td><td>
Binds the name of the end timezone field in the dataSource. If the endTimeZone field is not mentioned, then the appointment makes use of the **Scheduler** **timeZone** **or** **System** **timeZone**.<br/><br/></td></tr>
<tr>
<td>
**subject**<br/><br/></td><td>
Binds the appointment subject field name which holds the summary of the appointment. <br/><br/></td></tr>
<tr>
<td>
**location**<br/><br/></td><td>
Binds the name of the location field. It indicates the appointment location/occurrence place. This field should be bind to the Scheduler, when the **{{'[showLocationField](#_Show/Hide_Location_field"")'| markdownify }}** is set to true.<br/><br/></td></tr>
<tr>
<td>
**description**<br/><br/></td><td>
Binds the appointment description field name.<br/><br/></td></tr>
<tr>
<td>
**allDay**<br/><br/></td><td>
Binds the name of the allDay field. It accepts the **Boolean** value and indicates whether the appointment is an allday appointment or not.<br/><br/></td></tr>
<tr>
<td>
**categorize**<br/><br/></td><td>
Binds the name of the categorize field. It indicates the category or status value (red categorize, green, yellow and so on). <br/><br/></td></tr>
<tr>
<td>
**priority**<br/><br/></td><td>
Binds the name of the priority field and indicates the priority (high, low, medium and none) of the appointments. This field should be bind to the Scheduler, when “**prioritySettings****.****enable**” is set to true.<br/><br/></td></tr>
<tr>
<td>
**resourceFields**<br/><br/></td><td>
Binds one or more fields in the resource collection. It maps the resource field names with the appointments, denoting to which resource the appointments actually belongs.<br/><br/></td></tr>
<tr>
<td>
**recurrence**<br/><br/></td><td>
Binds the name of the recurrence field. It accepts the **Boolean** value and indicates whether the appointment is a recurrence appointment or not.<br/><br/></td></tr>
<tr>
<td>
**recurrenceRule**<br/><br/></td><td>
Binds the name of the recurrenceRule field. It holds the recurrence pattern associated with the appointments.<br/><br/></td></tr>
<tr>
<td>
**recurrenceId**<br/><br/></td><td>
Binds the recurrence Id field which acts as a parent id for Scheduler recurrence appointments.<br/><br/></td></tr>
<tr>
<td>
**recurrenceExDate**<br/><br/></td><td>
Binds the recurrence Exception field which accepts the recurrence Exception date values.<br/><br/></td></tr>
</table>
{% highlight html %}
<!-- HTML element will initialize as a ejSchedule -->

<div id="schedule"></div>

<script>

$(function () {

$("#schedule").ejSchedule({

currentDate: new Date(2015, 11, 7),

showLocationField: true,

categorizeSettings: { enable: true },

prioritySettings: { enable: true },

group: { resources: [ "Owners"] },

resources: [{

field: "ownerId",

title: "Owner",

name: "Owners",

resourceSettings: { dataSource: [

{ text: "Nancy", id: 1, color: "#f8a398" },

{ text: "Steven", id: 3, color: "#56ca85" },

{ text: "Michael", id: 5, color: "#51a0ed" }],

text: "text", id: "id", color: "color"

}

}],

appointmentSettings: {

resourceFields: "ownerId",

dataSource: [{

Id: 1,

Subject: "Music Class",

StartTime: new Date("2015/11/7 06:00 AM"),

StartTimeZone: "UTC +05:30",

EndTime: new Date("2015/11/7 07:00 AM"),

EndTimeZone: "UTC +05:30",

Description: "Never Giveup on Obstacles",

location: "US",

AllDay: false,

Recurrence: true,

RecurrenceRule: "FREQ=WEEKLY;BYDAY=MO,TU;INTERVAL=1;COUNT=15",

Categorize: "1",

Priority: "medium",

ownerId: 3,

RecurrenceId: 1,

RecurrenceExDate: null

}]

}

});

});

</script>



{% endhighlight %}

### Binding to JSON Data Array

To bind the Scheduler events data as array of JSON objects in JavaScript, refer the below code example.

**Example** - Array of JSON Data Binding

{% highlight html %}
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

</script>



{% endhighlight %}

### Binding Remote Data Service

The appointment data can be bound to the Scheduler through the [Odata](http://www.odata.org/# "") ([http://www.odata.org/](http://www.odata.org/# "")) remote services, where the service URL is mapped with [ejDatamanager](http://helpjs.syncfusion.com/js/datamanager/overview# "") and then configured to the Schedule dataSource API.

{% highlight html %}
<!-- HTML element will initialize as a ejSchedule -->

<div id="schedule"></div>

<script>

$(function () {

var dataManager = ej.DataManager({

// referring data from remote service (url binding)

url: "http://mvc.syncfusion.com/OdataServices/Northwnd.svc/"

});

// query to fetch the records from the specified table “Events”

var queryEvent = ej.Query().from("Events").take(10);

$("#schedule").ejSchedule({

currentDate: new Date(2014, 4, 5),

appointmentSettings: {

// Configure the dataSource with dataManager object

dataSource: dataManager,

query: queryEvent

}

});

});

</script>



{% endhighlight %}

### OData V4

The OData v4 is an improved version of OData protocols and the DataManager can also retrieve and consume appointment data from [OData v4](http://www.odata.org/documentation/# "") services. 

{% highlight html %}
<!-- HTML element will initialize as a ejSchedule -->

<div id="schedule"></div>

<script>

$(function () {

// get the appointments data from OData v4 service

var dataManager = ej.DataManager({

//OData v4 service 

url: "http://services.odata.org/V4/Northwind/Northwind.svc/Orders/",

adaptor: new ej.ODataV4Adaptor()

});

$("#schedule").ejSchedule({

currentDate: new Date(1997, 2, 23),

appointmentSettings: {

// Configure the dataSource with dataManager object

dataSource: dataManager,

subject: "ShipName",

startTime: "OrderDate",

endTime: "RequiredDate",

description: "ShipAddress"

}

});

});

</script>



{% endhighlight %}

### WebAPI Binding

The Schedule appointment data can be bound through the Web API service and it is a programmatic interface to define the request and response messages system that is mostly exposed in **JSON** or **XML**.

{% highlight html %}
<!-- HTML element will initialize as a ejSchedule -->

<div id="schedule"></div>

<script>

$(function () {

var dataManager = ej.DataManager({

// get the required appointments from Web API service

url: "http://mvc.syncfusion.com/OdataServices/api/ScheduleData/",

// enable cross domain

crossDomain: true

});

$("#schedule").ejSchedule({

currentDate: new Date(2014, 4, 5),

appointmentSettings: {

// Configure the dataSource with dataManager object

dataSource: dataManager

}

});

});

</script>



{% endhighlight %}

### ASP.Net Web Method Binding

The Schedule appointment data can retrieve data from ASP.Net Web methods. It can be achieved using the UrlAdaptor of ej.DataManager.

{% highlight html %}
<!-- HTML element will initialize as a ejSchedule -->

<div id="schedule"></div>

<script>

$(function () {

// get the appointments data from Web method

var dataManager = ej.DataManager({

url: "WebService1.asmx/GetDatas",  // This will trigger to bind the appointments data to schedule control

batchUrl: "WebService1.asmx/Crud", // This will trigger while saving the appointment through detail window

insertUrl: "WebService1.asmx/add",  // This will trigger while saving the appointment through quick window

updateUrl: "WebService1.asmx/update", //This will trigger while saving the resize or drag and drop the appointment 

removeUrl: "WebService1.asmx/remove", // This will trigger to delete the single appointment

adaptor: new ej.WebMethodAdaptor()

});

$("#schedule").ejSchedule({

currentDate: new Date(2014, 4, 5),

appointmentSettings: {

// Configure the dataSource with dataManager object

dataSource: dataManager

}

});

});

</script>



{% endhighlight %}

### MVC Controller Action Binding

The Schedule appointment data can retrieve data from MVC controller. This can be achieved by using the [UrlAdaptor](http://help.syncfusion.com/js/datamanager/data-adaptors#url-adaptor "") of [ej.DataManager](http://help.syncfusion.com/js/datamanager/overview# "").

{% highlight html %}
<!-- HTML element will initialize as a ejSchedule -->

<div id="schedule"></div>

<script>

$(function () {

// get the appointments data from Web method

var dataManager = ej.DataManager({

url: "Home/GetData",  // This will trigger to bind the appointments data to schedule control

batchUrl: "Home/Crud", // This will trigger while saving the appointment through detail window

insertUrl: "Home/add",  // This will trigger while saving the appointment through quick window

updateUrl: "Home/update", //This will trigger while saving the resize or drag and drop the appointment 

removeUrl: "Home/remove", // This will trigger to delete the single appointment

adaptor: new ej.UrlAdaptor()

});

$("#schedule").ejSchedule({

currentDate: new Date(2014, 4, 5),

appointmentSettings: {

// Configure the dataSource with dataManager object

dataSource: dataManager

}

});

});

</script>



{% endhighlight %}

### Loading Data on Demand

Load on demand feature allows the Scheduler to retrieve only the filtered appointment data (for the current Scheduler date range) from the service/database during **loading** **time**, and that too only for the current Scheduler view**.** There are 3 parameters made available on the server-side namely **CurrentDate**, **CurrentView** and **CurrentAction** through which only the necessary appointments are retrieved from the database and then assigned to the Scheduler dataSource. With this kind of action of Scheduler consuming only lesser data will reduce the usage of network bandwidth size and loading time. 

The **enableLoadOnDemand** property is used to enable or disable the load on demand functionality of the schedule.

{% highlight html %}
<!-- HTML element will initialize as a ejSchedule -->

<div id="schedule"></div>

<script>

$(function () {

var dataManager = ej.DataManager({

// get the required appointments from service

url: "http://mvc.syncfusion.com/OdataServices/api/ScheduleData/",

crossDomain: true

});

$("#schedule").ejSchedule({

// Enable Load on demand

enableLoadOnDemand: true,

currentDate: new Date(2014, 4, 5),

appointmentSettings: {

// Configure the dataSource with dataManager object

dataSource: dataManager,

}

});

});

</script>



{% endhighlight %}

