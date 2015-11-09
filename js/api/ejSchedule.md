---
layout: post
title: ejSchedule
description: Methods, Members, Events available in ejSchedule
documentation: API
platform: js
keywords: ejSchedule, API, Essential JS Schedule
---

# ejSchedule

#### Syntax

{% highlight js %}

$(element).ejSchedule()

{% endhighlight %}

#### Example

{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$('#Schedule').ejSchedule();         
</script>

{% endhighlight %}


#### Requires

* module:jQuery
* module:jquery.easing.min.js
* module:jquery.globalize.min.js
* module:jsrender.min.js
* module:ej.core.js
* module:ej.data.js
* module:ej.schedule.js
* module:ej.scroller.js
* module:ej.radiobutton.js
* module:ej.editor.js
* module:ej.dropdownlist.js
* module:ej.autocomplete.js
* module:ej.menu.js
* module:ej.dialog.js
* module:ej.button.js
* module:ej.checkbox.js
* module:ej.datepicker.js
* module:ej.timepicker.js
* module:ej.navigationdrawer.js



## Members


### allowDragDrop 'boolean'
{:#members:allowdragdrop}

When set to true, Schedule allows the appointments to be dragged and dropped at required time.

#### Default Value

* true

#### Example

To disable the drag and drop functionality,

{% highlight html %}
 
<div id="Schedule"></div> 
 
<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
		        currentDate:new Date(2014,4,5),
                allowDragDrop: false,
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                } 
            });
        });
</script>

{% endhighlight %}


### allowKeyboardNavigation 'boolean'
{:#members:allowkeyboardnavigation}

When set to true, Schedule allows interaction through keyboard shortcut keys. 

#### Default Value

* true

#### Example

To disable the Keyboard interaction with Schedule,


{% highlight html %}
 
<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
		            allowKeyboardNavigation: false
            });
        });
</script>

{% endhighlight %}


### appointmentSettings 'object'
{:#members:appointmentsettings}

It includes the dataSource option and the fields related to Schedule appointments.


### appointmentSettings.dataSource 'object/Array'
{:#members:appointmentsettings-datasource}


#### Default Value

* Array

The dataSource option accepts either JSON object collection or DataManager ([ej.DataManager](http://helpjs.syncfusion.com/js/datamanager/overview)) instance that contains Schedule appointments.

#### Example

To set the dataSource with array of JSON object collection,

{% highlight html %}
       
<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                currentDate:new Date(2014,4,5),
		        appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 12, 00)
                    },
                    {
                        Id: 102,
                        Subject: "Play with pets",
                        StartTime: new Date(2014, 4, 5, 05, 00),
                        EndTime: new Date(2014, 4, 5, 07, 00)
                    }]
                }
            });
        });
</script>

{% endhighlight %}


#### Example


To set the dataSource with DataManager instance,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            // DataManager creation
            var dataManager = ej.DataManager({
                url: "http://mvc.syncfusion.com/OdataServices/Northwnd.svc/Events",
                crossDomain: true
            });

            $("#Schedule").ejSchedule({
                currentDate: new Date(2014, 4, 5),
                appointmentSettings: {
                    dataSource: dataManager // passing remote url
                }
            });
        });
</script>

{% endhighlight %}


### appointmentSettings.query 'string'
{:#members:appointmentsettings-query}

#### Default Value

* null

It holds either the ej.Query() object or simply the query string that retrieves the specified records from the table.

#### Example

To set the dataSource with DataManager instance and querying the datamanager to fetch specific records from the Events table,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            // DataManager creation
            var dataManager = ej.DataManager({
                url: "http://mvc.syncfusion.com/OdataServices/Northwnd.svc",
                crossDomain: true
            });
            // Query creation
            var query = ej.Query().from("Events").take(10);

            $("#Schedule").ejSchedule({
                currentDate: new Date(2014, 4, 5),
                appointmentSettings: {
                    dataSource: dataManager, // passing remote url
                    query: query // query to retrieve the records from “Events” table
                }
            });
        });
</script>

{% endhighlight %}

### appointmentSettings.tableName 'string'
{:#members:appointmentsettings-tablename}

#### Default Value

* null

Assign the table name from where the records are to be fetched for the Schedule.

#### Example

To set the dataSource with DataManager instance and to use tableName property to directly fetch all the records from it,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            // DataManager creation
            var dataManager = ej.DataManager({
                url: "http://mvc.syncfusion.com/OdataServices/Northwnd.svc",
                crossDomain: true
            });
            
            $("#Schedule").ejSchedule({
                currentDate: new Date(2014, 4, 5),
                appointmentSettings: {
                    dataSource: dataManager, // passing remote url
                    tableName: "Events" // tableName to retrieve the records from it
                }
            });
        });
</script>

{% endhighlight %}


The following are the appointment fields that holds the appropriate column names from the dataSource.

### appointmentSettings.id 'string'
{:#members:appointmentsettings-id}

Binds the id field name in dataSource to the id of Schedule appointments. It denotes the unique id assigned to appointments.

### appointmentSettings.startTime 'string'
{:#members:appointmentsettings-starttime}

Binds the name of startTime field in the dataSource with start time of the Schedule appointments. It indicates the date and Time when Schedule appointment actually starts.

### appointmentSettings.endTime 'string'
{:#members:appointmentsettings-endtime}

Binds the name of endTime field in dataSource with the end time of Schedule appointments. It indicates the date and time when Schedule appointment actually ends.

#### Example

To create a simple appointment with mandatory fields, id, startTime and endTime,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                  currentDate:new Date(2014,4,5),
        		  appointmentSettings: {
                    dataSource: [{
                        EventId: 101,
                        EventStartTime: new Date(2014, 4, 5, 10, 00),
                        EventEndTime: new Date(2014, 4, 5, 12, 00)
                    }],
                    id: "EventId",
                    startTime: "EventStartTime",
                    endTime: "EventEndTime"
                }
            });
        });
</script>

{% endhighlight %}

> **Note :The fields, id, startTime and endTime are mandatory fields to be specified to create an appointment.**

### appointmentSettings.subject 'string'
{:#members:appointmentsettings-subject}

Binds the name of subject field in the dataSource to appointment Subject. Indicates the Subject or title that gets displayed on Schedule appointments.

#### Example:

To create an appointment with a **Subject**,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                currentDate:new Date(2014,4,5),
		            appointmentSettings: {
                    dataSource: [{
                        EventId: 101,
                        EventStartTime: new Date(2014, 4, 5, 10, 00),
                        EventEndTime: new Date(2014, 4, 5, 12, 00),
                        EventSubject: "Play with pets"
                    }],
                    id: "EventId",
                    startTime: "EventStartTime",
                    endTime: "EventEndTime",
                    subject: "EventSubject"
                }
            });
        });
</script>

{% endhighlight %}

## appointmentSettings.description 'string'
{:#members:appointmentsettings-description}

Binds the description field name in dataSource. It indicates the appointment description.

#### Example

To create an appointment with a **description**,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                    currentDate:new Date(2014,4,5),
		            appointmentSettings: {
                    dataSource: [{
                        EventId: 101,
                        EventStartTime: new Date(2014, 4, 5, 10, 00),
                        EventEndTime: new Date(2014, 4, 5, 12, 00),
                        EventDescription: "Pet Lovers!!!"
                    }],
                    id: "EventId",
                    startTime: "EventStartTime",
                    endTime: "EventEndTime",
                    description: "EventDescription"
                }
            });
        });
</script>

{% endhighlight %}

> **Note: Unlike Subject field that is displayed as a label over an appointment, the description doesn’t show up on it, by default. To display description over appointments, the appointment template can be used. **

### appointmentSettings.recurrence 'string'
{:#members:appointmentsettings-recurrence}

Binds the name of recurrence field in dataSource. It indicates whether the appointment is a recurrence appointment or not.

### appointmentSettings.recurrenceRule 'string'
{:#members:appointmentsettings-recurrencerule}

Binds the name of recurrenceRule field in dataSource. It indicates the recurrence pattern associated with appointments.

#### Example
 
To create a **recurrence** appointment,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                    currentDate:new Date(2014,4,5),
		            appointmentSettings: {
                    dataSource: [{
                        EventId: 101,
                        EventSubject: "Play with Pets",
                        EventStartTime: new Date(2014, 4, 5, 10, 00),
                        EventEndTime: new Date(2014, 4, 5, 12, 00),
                        EventRecurrence: true,
                        EventRecurrenceRule: "FREQ=DAILY;INTERVAL=1;COUNT=10"
                    }],
                    id: "EventId",
                    startTime: "EventStartTime",
                    endTime: "EventEndTime",
                    subject: "EventSubject",
                    recurrence: "EventRecurrence",
                    recurrenceRule: "EventRecurrenceRule"
                }
            });
        });
</script>

{% endhighlight %}

> **Note:The recurrence and recurrenceRule fields are inter-dependent, as when the recurrence field is set to true, the recurrenceRule has to be defined mandatorily for an appointment.**

### appointmentSettings.allDay 'string'
{:#members:appointmentsettings-allday}

Binds the name of allDay field in dataSource. It indicates whether the appointment is an allday appointment or not.

#### Default Value

* AllDay

#### Example

To create an **all-day** appointment,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                currentDate: new Date(2014, 4, 5),
                appointmentSettings: {
                    dataSource: [{
                        EventId: 101,
                        EventSubject: "Play with Pets",
                        EventStartTime: new Date(2014, 4, 5, 10, 00),
                        EventEndTime: new Date(2014, 4, 5, 12, 00),
                        EventAllDay: true
                    }],
                    id: "EventId",
                    startTime: "EventStartTime",
                    endTime: "EventEndTime",
                    subject: "EventSubject",
                    allDay: "EventAllDay"
                }
            });
        });
</script>

{% endhighlight %}

### appointmentSettings.resourceFields 'string'
{:#members:appointmentsettings-resourcefields}

#### Default Value

* null

Binds one or more fields in resource collection dataSource. It maps the resource field names with appointments denoting the resource of appointments actually belongs.

#### Example:

To create appointments in multiple resources scenario,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                currentDate: new Date(2014, 4, 2),
                group: {
                    resources: ["Owners"]
                },
                resources: [{
                    field: "ownerId", title: "Owner", name: "Owners",
                    allowMultiple: true,
                    resourceSettings: {
                        dataSource: [
                         { text: "Nancy", id: 1, color: "#f8a398" },
                         { text: "Steven", id: 2, color: "#56ca85"}],
                        text: "text", id: "id", color: "color"
                    }
                }],
                appointmentSettings: {
                    dataSource: [{
                        EventId: 100,
                        EventSubject: "Research on Sky Miracles",
                        EventStartTime: new Date(2014, 4, 2, 9, 00),
                        EventEndTime: new Date(2014, 4, 2, 10, 30),
                        ownerId: 2
                    }],
                    id: "EventId",
                    startTime: "EventStartTime",
                    endTime: "EventEndTime",
                    subject: "EventSubject",
                    // bind one or more resources fields separated by commas
                    resourceFields: "ownerId" 
                }
            });
        });
</script>

{% endhighlight %}

### appointmentSettings.categorize 'string'
{:#members:appointmentsettings-categorize}

#### Default Value

* null

Binds the name of categorize field in dataSource. It indicates the categorize value, red categorize, green, yellow and so on applied to the appointments.

#### Example

To create appointments with categorize options,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                currentDate: new Date(2014, 4, 2),
                categorizeSettings: {
                    enable: true
                },
                appointmentSettings: {
                    dataSource: [{
                        EventId: 100,
                        EventSubject: "Research on Sky Miracles",
                        EventStartTime: new Date(2014, 4, 2, 9, 00),
                        EventEndTime: new Date(2014, 4, 2, 10, 30),
                        EventCategorize: "6"
                    }],
                    id: "EventId",
                    startTime: "EventStartTime",
                    endTime: "EventEndTime",
                    subject: "EventSubject",
                    categorize: "EventCategorize"
                }
            });
        });
</script>

{% endhighlight %}

> **Note: There are six default Categorize colors available for appointments, Blue, Green, Orange, Purple, Red and Yellow that can be accessed by its default id values ranging from 1 to 6 respectively. The default Categorize collection can also be replaced with user-specified collection.**


### appointmentSettings.location 'string'
{:#members:appointmentsettings-location}

#### Default Value

* null

Binds the name of location field in dataSource. It indicates the appointment location.

#### Example

To create appointments with categorize options,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                currentDate: new Date(2014, 4, 2),
                showLocationField: true,
                appointmentSettings: {
                    dataSource: [{
                        EventId: 100,
                        EventSubject: "Research on Sky Miracles",
                        EventStartTime: new Date(2014, 4, 2, 9, 00),
                        EventEndTime: new Date(2014, 4, 2, 10, 30),
                        EventLocation: "Hawaai"
                    }],
                    id: "EventId",
                    startTime: "EventStartTime",
                    endTime: "EventEndTime",
                    subject: "EventSubject",
                    location: "EventLocation"
                }
            });
        });
</script>

{% endhighlight %}

> **Note: To use the location field in Schedule, enable an additional API showLocationField that displays the location textbox on the default appointment window. **

### appointmentSettings.priority 'string'
{:#members:appointmentsettings-priority}

#### Default Value

* null

Binds the name of the priority field in dataSource. It indicates the priority, high, low, medium and none of the appointments.

#### Example

To create appointments with priority option,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                currentDate: new Date(2014, 4, 2),
                prioritySettings:{ enable:true },
                appointmentSettings: {
                    dataSource: [{
                        EventId: 100,
                        EventSubject: "Research on Sky Miracles",
                        EventStartTime: new Date(2014, 4, 2, 9, 00),
                        EventEndTime: new Date(2014, 4, 2, 10, 30),
                        EventPriority: "high"
                    }],
                    id: "EventId",
                    startTime: "EventStartTime",
                    endTime: "EventEndTime",
                    subject: "EventSubject",
                    priority: "EventPriority"
                }
            });
        });
</script>

{% endhighlight %}

> **Note: To use the priority field in Schedule, enable the prioritySettings that displays the priority textbox on the default appointment window.**

### appointmentSettings.startTimeZone 'string'
{:#members:appointmentsettings-starttimezone}

#### Default Value

* StartTimeZone

Binds the name of start timezone field in dataSource. It indicates the timezone of appointment start date. When startTimeZone field is not mentioned, the appointment uses the Schedule timeZone or System timeZone.


### appointmentSettings.endTimeZone 'string'
{:#members:appointmentsettings-endtimezone}

#### Default Value

* EndTimeZone

Binds the name of end timezone field in dataSource. It indicates the timezone of appointment end date. When the endTimeZone field is not mentioned, the appointment uses the Schedule timeZone or System timeZone.

#### Example

To create appointments with priority option,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                currentDate: new Date(2014, 4, 2),
                prioritySettings: { enable: true },
                appointmentSettings: {
                    dataSource: [{
                        EventId: 100,
                        EventSubject: "Research on Sky Miracles",
                        EventStartTime: new Date(2014, 4, 2, 9, 00),
                        EventEndTime: new Date(2014, 4, 2, 10, 30),
                        EventStartTimeZone: "UTC +00:00",
                        EventEndTimeZone: "UTC +00:00"
                    }],
                    id: "EventId",
                    startTime: "EventStartTime",
                    endTime: "EventEndTime",
                    subject: "EventSubject",
                    priority: "EventPriority",
                    startTimeZone: "EventStartTimeZone",
                    endTimeZone: "EventEndTimeZone"
                }
            });
        });
</script>

{% endhighlight %}

### appointmentTemplateId 'string'
{:#members:appointmenttemplateid }

#### Default Value

* null

Template design that applies on the Schedule appointments.
All the field names that are mapped from dataSource to the appropriate field properties within the appointmentSettings can be used within the template.

#### Example

To set the appointment template,

{% highlight html %}

<div id="Schedule"></div>
    
<script id="apptemplate" type="text/x-jsrender">
   <div style="height:100%">
      <div>{{:Description}}</div>
   </div>
</script>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                appointmentTemplateId: "#apptemplate",
	         currentDate:new Date(2014,4,5),
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00),
                        Description: "Splendid Nature!!!"
                    }]
                }
            });
        });
</script>

{% endhighlight %}

### cssClass 'string'
{:#members:cssclass  }

#### Default Value

* ""

Accepts the custom CSS class name that defines specific user-defined styles and themes to be applied for partial or complete elements of the Schedule. 

#### Example

To apply custom css class name to the Schedule and to customize only background color of its header element,

{% highlight html %}

<div id="Schedule"></div>

<style type="text/css">
    .customStyle .e-scheduleheader {
        background-color: Teal;
    }
</style>


<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                    cssClass: "customStyle",
	                currentDate:new Date(2014,4,5),
                    appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                } 
            });
        });
</script>

{% endhighlight %}

> **Note: For more information on applying custom themes to Syncfusion controls, refer [here](http://docs.syncfusion.com/js/theming-in-essential-javascript-components#customizing-themes).**

### categorizeSettings 'object'
{:#members:categorizesettings }

Sets various categorize colors to the Schedule appointments to differentiate it.

### categorizeSettings.allowMultiple 'boolean'
{:#members:categorizesettings-allowmultiple }

#### Default Value

* false

When set to true, enables the multiple selection of categories to be applied for the appointments.

#### Example

To enable multiple selection of categories,

{% highlight html %}

<div id="Schedule"></div>
    
<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                currentDate: new Date(2014, 4, 2),
                categorizeSettings: {
                    enable: true,
                    allowMultiple: true
                },
                appointmentSettings: {
                    dataSource: [{
                        Id: 100,
                        Subject: "Research on Sky Miracles",
                        StartTime: new Date(2014, 4, 2, 9, 00),
                        EndTime: new Date(2014, 4, 2, 10, 30),
                        EventCategorize: "6,4,3"
                    }],
                    categorize: "EventCategorize"
                }
            });
        });
</script>

{% endhighlight %}

### categorizeSettings.enable 'boolean'
{:#members:categorizesettings-enable }

#### Default Value

* false

When set to true, enables the categories option to be applied for the appointments.

#### Example

To enable the categorize option,

{% highlight html %}

<div id="Schedule"></div>
    
<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                currentDate: new Date(2014, 4, 2),
                categorizeSettings: {
                    enable: true
                },
                appointmentSettings: {
                    dataSource: [{
                        Id: 100,
                        Subject: "Research on Sky Miracles",
                        StartTime: new Date(2014, 4, 2, 9, 00),
                        EndTime: new Date(2014, 4, 2, 10, 30),
                        EventCategorize: "6"
                    }],
                    categorize: "EventCategorize"
                }
            });
        });
</script>

{% endhighlight %}

### categorizeSettings.dataSource 'array/object'
{:#members:categorizesettings-datasource }

#### Default Value

* Array

The dataSource option accepts either the JSON object collection or DataManager [[ej.DataManager](http://helpjs.syncfusion.com/js/datamanager/overview)] instance that contains the categorize data.

#### Example

To set the dataSource with array of JSON object collection,

{% highlight html %}
  
<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                currentDate: new Date(2014, 4, 2),
                categorizeSettings: {
                  enable: true,
                  dataSource: [
                   { text: "Good", id: 1, color: "#7499e1", fontColor: "red" },
                   { text: "Excellent", id: 2, color: "#7cce6e", fontColor: "white" },
                   { text: "Improve", id: 5, color: "#e04343", fontColor: "white" },
                   { text: "Better", id: 6, color: "#f8f264", fontColor: "black"}]
                },
                appointmentSettings: {
                    dataSource: [{
                        Id: 100,
                        Subject: "Research on Sky Miracles",
                        StartTime: new Date(2014, 4, 2, 9, 00),
                        EndTime: new Date(2014, 4, 2, 10, 30),
                        EventCategorize: "6"
                    }],
                    categorize: "EventCategorize"
                }
            });
        });
</script>

{% endhighlight %}

The following are the category fields that holds appropriate column names from dataSource.

### categorizeSettings.id 'string'
{:#members:categorizesettings-id}

Binds id field name in the dataSource to id of category data.

#### Default Value

* id

### categorizeSettings.text 'string'
{:#members:categorizesettings-text}

Binds text field name in the dataSource to category text.

#### Default Value

* text

### categorizeSettings.color 'string'
{:#members:categorizesettings-color}

Binds color field name in the dataSource to category color.

#### Default Value

* color

#### Example

To set the categorize options with id, text and color fields,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                currentDate: new Date(2014, 4, 2),
                categorizeSettings: {
                  enable: true,
                  dataSource: [
                   { CategoryText: "Good", Id: 1, CategoryColor: "#7499e1" },
                   { CategoryText: "Excellent", Id: 2, CategoryColor: "#7cce6e" },
                   { CategoryText: "Improve", Id: 5, CategoryColor: "#e04343" },
                   { CategoryText: "Better", Id: 6, CategoryColor: "#f8f264" }],
                   text: "CategoryText",
                   id: "Id",
                   color: "CategoryColor"
                },
                appointmentSettings: {
                    dataSource: [{
                        Id: 100,
                        Subject: "Research on Sky Miracles",
                        StartTime: new Date(2014, 4, 2, 9, 00),
                        EndTime: new Date(2014, 4, 2, 10, 30),
                        EventCategorize: "6"
                    }],
                    categorize: "EventCategorize"
                }
            });
        });
</script>

{% endhighlight %}

### categorizeSettings.fontColor 'string'
{:#members:categorizesettings-fontcolor}

Binds fontColor field name in the dataSource to category font.

#### Default Value

* fontColor

#### Example

To set categorize options with fontColor,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                currentDate: new Date(2014, 4, 2),
                categorizeSettings: {
                  enable: true,
                  dataSource: [
                   { text: "Good", id: 1, color: "#7499e1", fontColor: "red" },
                   { text: "Excellent", id: 2, color: "#7cce6e", fontColor: "red" }]
                },
                appointmentSettings: {
                    dataSource: [{
                        EventId: 100,
                        EventSubject: "Research on Sky Miracles",
                        EventStartTime: new Date(2014, 4, 2, 9, 00),
                        EventEndTime: new Date(2014, 4, 2, 10, 30),
                        EventCategorize: "2"
                    }],
                    id: "EventId",
                    startTime: "EventStartTime",
                    endTime: "EventEndTime",
                    subject: "EventSubject",
                    categorize: "EventCategorize"
                }
            });
        });
</script>

{% endhighlight %}

### cellHeight 'string'
{:#members:cellheight}

Sets the height for Schedule cells.

#### Default Value

* "20px"

#### Example

To set cell height for Schedule,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                currentDate:new Date(2014,4,5),
                cellHeight: "35px",
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                } 
            });
        });
</script>

{% endhighlight %}

### cellWidth 'string'
{:#members:cellwidth}

Sets the width for Schedule cells.

#### Default Value

* ""

#### Example

To set the cell width for Schedule,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
        		currentDate:new Date(2014,4,5),
                cellWidth: "180px",
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                } 
            });
        });
</script>

{% endhighlight %}

### contextMenuSettings 'object'
{:#members:contextmenusettings}

Holds all options related to the context menu settings of the Schedule.

### contextMenuSettings.enable 'boolean'
{:#members:contextmenusettings-enable}

#### Default Value

* false

When set to true, enables the context menu options available for the Schedule cells and appointments.

#### Example

To enable the context menu options for Schedule control,

{% highlight html %}

<div id="Schedule"></div>
    
<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                currentDate: new Date(2014, 4, 2),
                contextMenuSettings: {
                    enable: true
                },
                appointmentSettings: {
                    dataSource: [{
                        EventId: 100,
                        EventSubject: "Research on Sky Miracles",
                        EventStartTime: new Date(2014, 4, 2, 9, 00),
                        EventEndTime: new Date(2014, 4, 2, 10, 30)
                    }],
                    id: "EventId",
                    startTime: "EventStartTime",
                    endTime: "EventEndTime",
                    subject: "EventSubject"
                }
            });
        });
</script>

{% endhighlight %}

### contextMenuSettings.menuItems 'object'
{:#members:contextmenusettings-menuitems}

#### Default Value

* []

Contains all the default context menu options that are applicable for both Schedule cells and appointments. It also supports adding custom menu items to cells or appointment collection.

#### Example

Default context menu options available for Schedule cells and appointments,

{% highlight html %}

<div id="Schedule"></div>
    
<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                currentDate: new Date(2014, 4, 2),
                contextMenuSettings: {
                    enable: true,
                    menuItems: {
                      appointment: [
                        { id: "open", text: "Open Appointment" },
                        { id: "delete", text: "Delete Appointment" }
                      ],
                      cells: [
                        { id: "new", text: "New Appointment" },
                        { id: "recurrence", text: "New Recurring Appointment" },
                        { id: "today", text: "Today" },
                        { id: "gotodate", text: "Go to date" },
                        { id: "settings", text: "Settings" },
                        { id: "view", text: "View", parentId: "settings" },
                        { id: "timemode", text: "TimeMode", parentId: "settings" },
                        { id: "view_Day", text: "Day", parentId: "view" },
                        { id: "view_Week", text: "Week", parentId: "view" },
                        { id: "view_Workweek", text: "Workweek", parentId: "view" },
                        { id: "view_Month", text: "Month", parentId: "view" },
                        { id: "timemode_Hour12", text: "12 Hours", parentId: "timemode" },
                        { id: "timemode_Hour24", text: "24 Hours", parentId: "timemode" },
                        { id: "businesshours", text: "Business Hours", parentId: "settings" }
                      ]
                    }
                },
                appointmentSettings: {
                    dataSource: [{
                        EventId: 100,
                        EventSubject: "Research on Sky Miracles",
                        EventStartTime: new Date(2014, 4, 2, 9, 00),
                        EventEndTime: new Date(2014, 4, 2, 10, 30)
                    }],
                    id: "EventId",
                    startTime: "EventStartTime",
                    endTime: "EventEndTime",
                    subject: "EventSubject"
                }
            });
        });
</script>

{% endhighlight %}

#### Example

To add custom context menu option to the Schedule appointments,

{% highlight html %}

<div id="Schedule"></div>
    
<script type="text/javascript">
    $(function () {
            $("#Schedule").ejSchedule({
                currentDate: new Date(2014, 4, 2),
                contextMenuSettings: {
                    enable: true,
                    menuItems: {
                        appointment: [
                        { id: "open", text: "Open Appointment" },
                        { id: "delete", text: "Delete Appointment" },
                        { id: "custom1", text: "Customize" }
                      ],
                        cells: [
                        { id: "new", text: "New Appointment" },
                        { id: "recurrence", text: "New Recurring Appointment" },
                        { id: "today", text: "Today" },
                        { id: "gotodate", text: "Go to date" }
                      ]
                    }
                }, 
                menuItemClick: "onCustomMenuClick",
                appointmentSettings: {
                    dataSource: [{
                        EventId: 100,
                        EventSubject: "Research on Sky Miracles",
                        EventStartTime: new Date(2014, 4, 2, 9, 00),
                        EventEndTime: new Date(2014, 4, 2, 10, 30)
                    }],
                    id: "EventId",
                    startTime: "EventStartTime",
                    endTime: "EventEndTime",
                    subject: "EventSubject"
                }
            });
        });


        function onCustomMenuClick(args) {
            if (args.events.ID == "custom1") {
                $("#Appointment_" + args.targetInfo.EventId).find(".e-apptext").html("Custom Appointment"); 
                $("#Appointment_" + args.targetInfo.EventId).css("background", "orange");
            }
        }

</script>

{% endhighlight %}

> **Note:In the above code example, menuItemClick event is defined that triggers when any of the menu options are selected. Here, the condition is checked as, when the id of selected menu item option contains custom1, then the target appointment’s text and its color gets modified.**

### currentDate 'date'
{:#members:currentdate}

#### Default Value

* new Date()

Sets current date of the Schedule. The Schedule displays initially with the date that is provided here.

#### Example

To set current date for Schedule,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
		            currentDate:new Date(2014,4,5),
                    appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                } 
            });
        });
</script>

{% endhighlight %}

### currentView 'string'
{:#members:currentview}

#### Default Value

* week

Sets current view of the Schedule. Schedule displays initially with the view that is specified here. The available views are day, week, workweek and month, from where any one of the required view can be set to the Schedule.

#### Example

To set the current view as **Day** for Schedule,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
		        currentDate:new Date(2014,4,5),
                currentView: ej.Schedule.CurrentView.Day,
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                } 
            });
        });
</script>

{% endhighlight %}

### dateFormat 'string'
{:#members:dateformat}

#### Default Value

* ""

Sets the date format for Schedule. 

#### Example

To set date format for Schedule,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                currentDate: new Date(2014, 4, 5),
                dateFormat: "yyyy-MM-dd",
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                }
            });
        });
</script>

{% endhighlight %}

### enableAppointmentNavigation 'boolean'
{:#members:enableappointmentnavigation}

#### Default Value

* true

When set to true, enables the previous or next appointment navigation within the Schedule.  

#### Example

To disable the previous or next appointment navigation,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                currentDate: new Date(2014, 4, 5),
                enableAppointmentNavigation: false,
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                }
            });
        });
</script>

{% endhighlight %}


### enableAppointmentResize 'boolean'
{:#members:enableappointmentresize}

#### Default Value

* true

When set to true, enables the resize behaviour of appointments within the Schedule. 

#### Example

To disable the appointment resizing,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                currentDate: new Date(2014, 4, 5),
                enableAppointmentResize: false,
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                }
            });
        });
</script>

{% endhighlight %}

### enableLoadOnDemand 'boolean'
{:#members:enableloadondemand}

#### Default Value

* false

When set to true, enables the loading of Schedule appointments based on your demand. With this load on demand concept, the data consumption of the Schedule can be limited.

#### Example

To enable the load on demand functionality for Schedule,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            // DataManager creation
            var dataManager = ej.DataManager({
                // To get the required appointments from service
                url: "http://mvc.syncfusion.com/OdataServices/api/ScheduleData/",
                crossDomain: true
            });
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                // To enable Load on demand
                enableLoadOnDemand: true,
                appointmentSettings: {
                    dataSource: dataManager
                }
            });
        });
</script>

{% endhighlight %}

### enablePersistence 'boolean'
{:#members:enablepersistence}

#### Default Value

* false

Saves the current model value to browser cookies for state maintenance. When the page gets refreshed, Schedule control values are retained.

#### Example

To enable persistence for the Schedule,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                enablePersistence: true,
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                }
            });
        });
</script>

{% endhighlight %}

### enableRTL 'boolean'
{:#members:enablertl}

#### Default Value

* false

When set to true, changes the Schedule layout and behaviour as per the common RTL conventions.

#### Example

To enable RTL for the Schedule,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                enableRTL: true,
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                }
            });
        });
</script>

{% endhighlight %}

### endHour 'number'
{:#members:endhour}

#### Default Value

* 24

Sets the end hour time limit to be displayed on the Schedule.

#### Example


To set end hour on the Schedule,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                endHour: 18,
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                }
            });
        });
</script>

{% endhighlight %}

### group 'object'
{:#members:group}

To configure resource grouping on the Schedule.

#### Default Value

* null

### group.resources 'object'
{:#members:group-resources}

Holds the array of resource names to be grouped on the Schedule.

#### Example

To group the resources on the Schedule,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                currentDate: new Date(2014, 04, 05),
                group: {
                    resources: ["Owners"]
                },
                appointmentSettings: {
                    resourceFields: "ResourceId",
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00),
                        ResourceId: 3
                    }]
                },
                resources: [
                {
                    field: "ResourceId",
                    title: "Resource",
                    name: "Owners", allowMultiple: true,
                    resourceSettings: { dataSource: [
                      { text: "Nancy", id: 1, groupId: 1, color: "#f8a398" },
                      { text: "Steven", id: 3, groupId: 2, color: "#56ca85" },
                      { text: "Michael", id: 5, groupId: 1, color: "#51a0ed" }],
                    text: "text", id: "id", groupId: "groupId", color: "color"
                    }
                }]
            });
        });
</script>
  
{% endhighlight %}

### height 'string'
{:#members:height}

#### Default Value 

* "1120px"

Sets the height of the Schedule. Accepts both pixel and percentage values. 

#### Example 

To set the height of Schedule in pixels,


{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                height: "500px",
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                }
            });
        });
</script>

{% endhighlight %}

#### Example


To set height of Schedule in percentage,

> **Note: To set the percentage values for the Schedule height, define the parent element with some specific height that holds the Scheduler div. When the Schedule is not placed within any of the parent element, define the HTML and body tags explicitly with some height values either in pixel or percentage.**

{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml" style="height:100%">
  <head>
    <!--[CSS and SCRIPT reference section]-->
  </head>

  <body style="height:100%">

    <div id="Schedule"></div>
    <script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                height: "500px",
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                }
            });
        });
    </script>
  </body>
</html>

{% endhighlight %}


### workHours 'object'
{:#members:workhours}

To define the workHours display of the Schedule control.

### workHours.highlight 'boolean'
{:#members:workhours-hightlight}

#### Default Value

* true

When set to true, highlights the work hours of the Schedule.  

#### Example

To disable the highlighting of Schedule work hours,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                workHours:{
                    highlight:false
                },
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                }
            });
        });
</script>

{% endhighlight %}

### workHours.start 'number'
{:#members:workhours-start}

#### Default Value

* null

Sets the start time to depict the start of working or business hour in a day.

#### Example

To set the working start hour for Schedule,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                workHours:{
                    highlight:false,
                    start:9
                },
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                }
            });
        });
</script>

{% endhighlight %}

### workHours.end 'number'
{:#members:workhours-end}

#### Default Value

* null

Sets the end time to depict the end of working or business hour in a day.

#### Example

To set the working end hour for Schedule,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                workHours:{
                    highlight:false,
                    start:9,
                    end:18
                },
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                }
            });
        });
</script>

{% endhighlight %}



### isDST 'boolean'
{:#members:isdst}

#### Default Value 

* false

When set to true, enables the Schedule to observe Daylight Saving Time for supported timezones.  

#### Example

To enable the Daylight Saving time in Schedule,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                isDST: true,
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                }
            });
        });
</script>

{% endhighlight %}

### isResponsive 'boolean'
{:#members:isresponsive}

#### Default Value 

* true

When set to true, adapts the Schedule layout to fit the screen size of devices on which it renders.

#### Example

To make the Schedule adaptive,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                isResponsive: true,
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                }
            });
        });
</script>

{% endhighlight %}

### locale 'string'
{:#members:locale}

#### Default Value

* "en-US"


Sets the specific culture to the Schedule.

#### Example

To set the French culture on Schedule, set its locale as fr-FR,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                locale: "fr-FR",
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                }
            });
        });
</script>

{% endhighlight %}

> **Note: To set any culture for Schedule, refer to the required minified globalize files of the specific culture. For example, to use fr-FR culture in Schedule, refer to the globalize.culture.fr-FR.min script file. **

> **Also define the locale words of that specific culture properly. For example, define the locale words for fr-FR culture in a variable ej.Schedule.Locale[“fr-FR”] = { }; under script section.**

### maxDate 'date'
{:#members:maxdate}

#### Default Value

* new Date(2099, 12, 31)

Sets the maximum date limit to display on the Schedule. Setting maxDate with specific date value disallows the Schedule to navigate beyond that date.

#### Example

To set the maximum date on the Schedule,


{% highlight html %}
       
<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                maxDate: new Date(2014, 04, 06),
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                }
            });
        });
</script>
{% endhighlight %}

### minDate 'date'
{:#members:mindate}

#### Default Value
{:.param}

* new Date(1900, 01, 01)

Sets the minimum date limit to display on the Schedule. Setting minDate with specific date value disallows the Schedule to navigate beyond that date.

#### Example

To set the minimum date on the Schedule,


{% highlight html %}
       
<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                minDate: new Date(2014, 04, 03),
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                }
            });
        });
</script>

{% endhighlight %}

### orientation 'string'
{:#members:orientation}

#### Default Value

* vertical

Sets the mode of rendering the Schedule either in a vertical or horizontal direction.

#### Example

To render the Schedule in horizontal orientation,


{% highlight html %}
       
<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                orientation: "horizontal",
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                }
            });
        });
</script>

{% endhighlight %}


### prioritySettings 'object'
{:#members:prioritysettings}

Holds all the options related to priority settings of the Schedule.

### prioritySettings.enable 'boolean'
{:#members:prioritysettings-enable}

#### Default Value

* false

When set to true, enables the priority options available for the Schedule appointments.

#### Example

To enable the priority option in Schedule,


{% highlight html %}
       
<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                prioritySettings: { enable: true },
                appointmentSettings: {
                    priority: "Priority",
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00),
                        Priority: "high"
                    }]
                }
            });
        });
</script>

{% endhighlight %}

### prioritySettings.dataSource 'object/array'
{:#members:prioritysettings-datasource }

#### Default Value

* Array

The dataSource option can accept the JSON object collection that contains the priority related data.

#### Example

To set the dataSource with array of JSON object collection,


{% highlight html %}
       
<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                currentDate: new Date(2014, 4, 2),
                prioritySettings: {
                  enable: true,
                  dataSource: [
                     { text: "None", value: "none" },
                     { text: "High", value: "high" },
                     { text: "Medium", value: "medium" },
                     { text: "Low", value: "low" }]
                },
                appointmentSettings: {
                    dataSource: [{
                        Id: 100,
                        Subject: "Research on Sky Miracles",
                        StartTime: new Date(2014, 4, 2, 9, 00),
                        EndTime: new Date(2014, 4, 2, 10, 30),
                        EventPriority: "low"
                    }],
                    priority: "EventPriority"
                }
            });
        });
</script>

{% endhighlight %}

The following are the priority fields that holds the appropriate column names from dataSource.

### prioritySettings.text 'string'
{:#members:prioritysettings-text }

#### Default Value

* text

Binds text field name in the dataSource to prioritySettings text. These text gets listed out in priority field of the appointment window.

### prioritySettings.value 'string'
{:#members:prioritysettings-value }

#### Default Value

* value

Binds value field name in the dataSource to prioritySettings value. These field names usually accepts four priority values by default, high, low, medium and none.

#### Example

To set the priority options with text and value fields,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                currentDate: new Date(2014, 4, 2),
                prioritySettings: {
                  enable: true,
                  dataSource: [
                     { PriorityText: "None", PriorityValue: "none" },
                     { PriorityText: "Important", PriorityValue: "high" },
                     { PriorityText: "Normal", PriorityValue: "medium" },
                     { PriorityText: "Least", PriorityValue: "low" }],
                  text: "PriorityText",
                  value: "PriorityValue"
                },
                appointmentSettings: {
                    dataSource: [{
                        Id: 100,
                        Subject: "Research on Sky Miracles",
                        StartTime: new Date(2014, 4, 2, 9, 00),
                        EndTime: new Date(2014, 4, 2, 10, 30),
                        EventPriority: "low"
                    }],
                    priority: "EventPriority"
                }
            });
        });
</script>

{% endhighlight %}

### prioritySettings.template 'string'
{:#members:prioritysettings-template}

#### Default Value

* null

Allows priority field customization in the appointment window to add custom icons denoting the priority level for the appointments.

#### Example

To set the template for priority option in Schedule,

{% highlight html %}

<div id="Schedule"></div>

<style type="text/css">
    .high,
    .medium {
        height: 13px;
        width: 13px;
        float: left;
        margin-right: 4px;
        background-repeat: no-repeat;
        background-size: 60px;
        padding: 1px;
        margin-top: 2px;
    }

    .high {
        /*background: url('Content/ej/web/images/critical.png');*/
        background-color: orange;
        background-position: -13px;
    }

    .medium {
        /*background: url('Content/ej/web/images/ultracritical.png');*/
        background-color: #56ca85;
        background-position: -59px;
    }
</style>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                prioritySettings: { 
                  enable: true,
                  dataSource: [
                     { text: "High", value: "high" },
                     { text: "Normal", value: "medium" }],
                  text: "text", value: "value",
                  template: "<div class='${value}'></div>"
                },
                appointmentSettings: {
                    priority: "Priority",
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00),
                        Priority: "high"
                    }]
                }
            });
        });
</script>

{% endhighlight %}

> ** Note: Since the prioritySettings contains the default values in its dataSource like none, high, medium and low, the appropriate css classes has to be created with the same value names to apply it on the template.**

### readOnly 'boolean'
{:#members:readonly }

#### Default Value

* false

When set to true, disables the interaction with the Schedule appointments, simply allowing the date and view navigation to occur.

#### Example

To make the Schedule readOnly,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                readOnly: true,
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                }
            });
        });
</script>

{% endhighlight %}


### reminderSettings 'object'
{:#members:remindersettings }

Holds all the options related to reminder settings of the Schedule.

### reminderSettings.enable 'boolean'
{:#members:remindersettings-enable }

#### Default Value

* false

When set to true, enables the reminder option available for the Schedule appointments.

#### Example 

To enable the reminder option in Schedule,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                reminderSettings: { enable: true },
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                }
            });
        });
</script>

{% endhighlight %}

### reminderSettings.alertBefore 'number'
{:#members:remindersettings-alertbefore  }

#### Default Value

* 5

Sets the timing, when the reminders are to be alerted for the Schedule appointments.

#### Example

To set the alert for Schedule appointments,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                reminderSettings: { enable: true, alertBefore: 7 },
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                }
            });
        });
</script>

{% endhighlight %}

### renderDates 'object'
{:#members:renderdates}

#### Default Value

* null

Defines the specific start and end dates to be rendered in the Schedule control. To render such user-specified custom date ranges in the Schedule control, set the **currentView** property to **customview**.

### renderDates.start 'date'
{:#members:renderdates-start}

#### Default Value

* null

Sets the start of custom date range to be rendered in the Schedule.

### renderDates.end 'date'
{:#members:renderdates-end}

#### Default Value

* null

Sets the end limit of the custom date range.

#### Example

To set the custom date range in Schedule,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                views: ["Day", "Week", "WorkWeek", "Month", "CustomView"], 
                currentView: ej.Schedule.CurrentView.CustomView,
                renderDates: {
                    start: new Date(2014, 11, 7),
                    end: new Date(2014, 12, 10)
                },
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                }
            });
        });
</script>

{% endhighlight %}


### resourceHeaderTemplateId 'string'
{:#members:resourceheadertemplateid }

#### Default Value

* null

Template design that applies on the Schedule resource header.

All field names that are mapped from the dataSource to appropriate field properties within the resourceSettings can be used within the template.

#### Example

To set the resource header template,

{% highlight html %}

<div id="Schedule"></div>

<script id="resTemplate" type="text/x-jsrender">
  <div style="height:100%">
     <div style="width:15px;height:15px;margin-left:25px;margin-top:3px;float:left;background:{{:color}};"></div><div>{{:text}}</div> 
  </div>
</script>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                resourceHeaderTemplateId: "#resTemplate",
                group: {
                    resources: ["Rooms"]
                },
                resources: [
                {
                    field: "roomId",
                    title: "Room",
                    name: "Rooms", allowMultiple: false,
                    resourceSettings: { dataSource: [
                    { text: "ROOM1", id: 1, color: "#cb6bb2" },
                    { text: "ROOM2", id: 2, color: "#56ca85"}],
                        text: "text", id: "id", color: "color"
                    }
                }],
                appointmentSettings: {
                    resourceFields: "roomId",
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00),
                        roomId: 2
                    }]
                }
            });
        });
</script>

{% endhighlight %}


### resources 'array'
{:#members:resources }

#### Default Value

* null

Holds all the options related to the resources settings of the Schedule. It is a collection of one or more resource objects, where the levels of resources are rendered on the Schedule based on the order of the resource data provided within this collection.

### resources.fields 'string'
{:#members:resources-fields }

#### Default Value

* []

It holds the name of the resource field to be bound to the Schedule appointments that contains the resource Id.

#### Example

To specify the resource field,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                resources: [{
                    field: "ownerId", title: "Owner",
                    resourceSettings: {
                        dataSource: [
                         { text: "Nancy", id: 1, color: "#f8a398" },
                         { text: "Steven", id: 2, color: "#56ca85"}],
                        text: "text", id: "id", color: "color"
                    }
                }],
                appointmentSettings: {
                    dataSource: [{
                        Id: 100,
                        Subject: "Research on Sky Miracles",
                        StartTime: new Date(2014, 04, 05, 9, 00),
                        EndTime: new Date(2014, 04, 05, 10, 30),
                        ownerId: 2
                    }],
                    // bind one or more resources fields separated by commas
                    resourceFields: "ownerId"
                }
            });
        });
</script>


{% endhighlight %}


### resources.title 'string'
{:#members:resources-title }

#### Default Value

* []

It holds the title name of the resource field to be displayed on the Schedule appointment window.

#### Example

To specify the resource title,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
       $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                resources: [{
                    field: "ownerId", title: "Owner",
                    resourceSettings: {
                        dataSource: [
                         { text: "Nancy", id: 1, color: "#f8a398" },
                         { text: "Steven", id: 2, color: "#56ca85"}],
                        text: "text", id: "id", color: "color"
                    }
                }],
                appointmentSettings: {
                    dataSource: [{
                        Id: 100,
                        Subject: "Research on Sky Miracles",
                        StartTime: new Date(2014, 04, 05, 9, 00),
                        EndTime: new Date(2014, 04, 05, 10, 30),
                        ownerId: 2
                    }],
                    resourceFields: "ownerId"
                }
            });
        });
</script>

{% endhighlight %}


### resources.name 'string'
{:#members:resources-name }

#### Default Value

* []

A unique resource name that is used for differentiating various resource objects while grouping it in various levels.

#### Example

To specify the resource field,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                group: {
                    resources: ["Owners"],
                },
                resources: [{
                    field: "ownerId", title: "Owner",
                    name: "Owners",
                    resourceSettings: {
                        dataSource: [
                         { text: "Nancy", id: 1, color: "#f8a398" },
                         { text: "Steven", id: 2, color: "#56ca85"}],
                        text: "text", id: "id", color: "color"
                    }
                }],
                appointmentSettings: {
                    dataSource: [{
                        Id: 100,
                        Subject: "Research on Sky Miracles",
                        StartTime: new Date(2014, 04, 05, 9, 00),
                        EndTime: new Date(2014, 04, 05, 10, 30),
                        ownerId: 2
                    }],
                    // bind one or more resources fields separated by commas
                    resourceFields: "ownerId"
                }
            });
        });
</script>

{% endhighlight %}


### resources.allowMultiple 'string'
{:#members:resources-allowmultiple  }

#### Default Value

* []

When set to true, allows multiple selection of resource names, thus creating multiple instances of same appointment for the selected resources.

#### Example

To set allowMultiple option for a resource object,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                resources: [{
                    field: "ownerId", title: "Owner",
                    resourceSettings: {
                        dataSource: [
                         { text: "Nancy", id: 1, color: "#f8a398" },
                         { text: "Steven", id: 2, color: "#56ca95"}],
                        text: "text", id: "id", color: "color"
                    }
                },
                {
                    field: "roomId", title: "Room(s)",
                    allowMultiple: true,
                    resourceSettings: {
                        dataSource: [
                         { text: "Room1", id: 1, groupId: 1, color: "#f8a398" },
                         { text: "Room2", id: 2, groupId: 2, color: "#56ca85"},
                         { text: "Room3", id: 3, groupId: 2, color: "#56ac88"}],
                        text: "text", id: "id", color: "color", groupId: "groupId"

                    }
                }],
                appointmentSettings: {
                    dataSource: [{
                        Id: 100,
                        Subject: "Research on Sky Miracles",
                        StartTime: new Date(2014, 04, 05, 9, 00),
                        EndTime: new Date(2014, 04, 05, 10, 30),
                        ownerId: 2,
                        roomId: 3 
                    }],
                    resourceFields: "ownerId,roomId"
                }
            });
        });
</script>

{% endhighlight %}


### resources.resourceSettings 'object'
{:#members:resources-resourcesettings}

It holds the field names of the resources to be bound to the Schedule and also the dataSource.

### resources.resourceSettings.dataSource 'object|array'
{:#members:resources-resourcesettings-datasource}

The dataSource option accepts either JSON object collection or DataManager ([ej.DataManager](http://helpjs.syncfusion.com/js/datamanager/overview)) instance that contains the resources related data.

#### Example

To set the dataSource with array of JSON object collection,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                resources: [{
                    field: "ownerId", title: "Owner",
                    resourceSettings: {
                        dataSource: [
                         { text: "Nancy", id: 1, color: "#f8a398" },
                         { text: "Steven", id: 2, color: "#56ca85"}],
                        text: "text", id: "id", color: "color"
                    }
                }],
                appointmentSettings: {
                    dataSource: [{
                        Id: 100,
                        Subject: "Research on Sky Miracles",
                        StartTime: new Date(2014, 04, 05, 9, 00),
                        EndTime: new Date(2014, 04, 05, 10, 30),
                        ownerId: 2
                    }],
                    resourceFields: "ownerId"
                }
            });
        });

</script>

{% endhighlight %}

The following are the resourceSettings fields that maps the appropriate column names from the dataSource.

### resources.resourceSettings.text 'string'
{:#members:resources-resourcesettings-text}

Binds text field name in the dataSource to resourceSettings **text**. These text gets listed out in resources field of the appointment window.

### resources.resourceSettings.id 'string'
{:#members:resources-resourcesettings-id }

Binds id field name in the dataSource to resourceSettings **id**. 

### resources.resourceSettings.groupId 'string'
{:#members:resources-resourcesettings-groupid }

Binds groupId field name in the dataSource to resourceSettings **groupId**.

### resources.resourceSettings.color 'string'
{:#members:resources-resourcesettings-color }

Binds color field name in the dataSource to resourceSettings **color**. The color specified here gets applied to the Schedule appointments denoting to the resource it belongs. 


#### Example

To set the resources options with id, text, groupId and color fields,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                resources: [{
                    field: "ownerId", title: "Owner",
                    resourceSettings: {
                        dataSource: [
                         { OwnerText: "Nancy", id: 1, OwnerColor: "#f8a398" },
                         { OwnerText: "Steven", id: 2, OwnerColor: "#56ca95"}],
                        text: "OwnerText", id: "id", color: "OwnerColor"
                    }
                },
                {
                    field: "roomId", title: "Room(s)",
                    resourceSettings: {
                        dataSource: [
                       // groupId groups the current resources under the previous level of resource object
                         { text: "Room1", id: 1, groupId: 1, color: "#f8a398" },
                         { text: "Room2", id: 2, groupId: 2, color: "#56ca85"},
                         { text: "Room3", id: 3, groupId: 2, color: "#56ac88"}],
                        text: "text", id: "id", color: "color", groupId: "groupId"

                    }
                }],
                appointmentSettings: {
                    dataSource: [{
                        Id: 100,
                        Subject: "Research on Sky Miracles",
                        StartTime: new Date(2014, 04, 05, 9, 00),
                        EndTime: new Date(2014, 04, 05, 10, 30),
                        ownerId: 2,
                        roomId: 3 
                    }],
                    resourceFields: "ownerId,roomId"
                }
            });
        });
</script>

{% endhighlight %}


### appointmentClass 'string'
{:#members:appointmentclass}

Binds appointmentClass field name in the dataSource. It applies custom CSS classname to appointments depicting to the resorce it belongs.

#### Example

To customize the styles of the appointments based on the resources it belongs, use the appointmentClass field with other resources options,

{% highlight html %}

<div id="Schedule"></div>

<style type="text/css">
    .e-schedule .e-appointcss1
    {
	background-color: Maroon;
	color: Orange;
    	
    }
    .e-schedule .e-appointcss2
    {
  	background-color: Orange;
    	color: Maroon;
    }
</style>


<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                resources: [{
                    field: "ownerId", title: "Owner",
                    resourceSettings: {
                        dataSource: [
                         { OwnerText: "Nancy", id: 1, customClass: "e-appointcss1" },
                         { OwnerText: "Steven", id: 2, customClass: "e-appointcss2"}],
                        text: "OwnerText", id: "id", appointmentClass: "customClass"
                    }
                }],
                appointmentSettings: {
                    dataSource: [{
                        Id: 100,
                        Subject: "Research on Sky Miracles",
                        StartTime: new Date(2014, 04, 05, 9, 00),
                        EndTime: new Date(2014, 04, 05, 10, 30),
                        ownerId: 2
                    },
                    {
                        Id: 101,
                        Subject: "Discovery of exo-planets",
                        StartTime: new Date(2014, 04, 07, 6, 00),
                        EndTime: new Date(2014, 04, 07, 9, 30),
                        ownerId: 1
                    }],
                    resourceFields: "ownerId"
                }
            });
        });
</script>

{% endhighlight %}

> **Note: The custom css class names defined separately for each resources within 'style' tag are prefixed with the class name '.e-schedule', only then it gets applied to the appointments.**


### showAllDayRow 'boolean'
{:#members:showalldayrow}

#### Default Value

* true

When set to true, displays the all-day row cells on the Schedule.

#### Example 

To hide the all-day row cells,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                showAllDayRow: false,
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                }
            });
        });
</script>

{% endhighlight %}

### showCurrentTimeIndicator 'boolean'
{:#members:showcurrenttimeindicator}

#### Default Value

* true

When set to true, displays the current time indicator on the Schedule.

#### Example

To hide the current time indicator,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                showCurrentTimeIndicator: false,
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                }
            });
        });
</script>

{% endhighlight %}

### showHeaderBar 'boolean'
{:#members:showheaderbar}

#### Default Value

* true

When set to true, displays the header bar on the Schedule.

#### Example

To hide the Schedule header bar,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                showHeaderBar: false,
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                }
            });
        });
</script>

{% endhighlight %}

### showLocationField 'boolean'
{:#members:showlocationfield}

#### Default Value

* false

When set to true, displays the location field additionally on Schedule appointment window.

#### Example

To show the location field,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                showLocationField: true,
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00),
                        Location: "Chicago"
                    }],
                    location: "Location"
                }
            });
        });
</script>

{% endhighlight %}

### showQuickWindow 'boolean'
{:#members:showquickwindow}

#### Default Value

* true

When set to true, displays the quick window for every single click made on the Schedule cells or appointments.

#### Example

To hide the quick window,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                showQuickWindow: false,
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                }
            });
        });
</script>

{% endhighlight %}

### showTimeScale 'boolean'
{:#members:showtimescale}

#### Default Value

* true

When set to true, displays the timescale on the left side of the Schedule.

#### Example

To hide the timescale,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                showTimeScale: false,
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                }
            });
        });
</script>

{% endhighlight %}

### startHour 'number'
{:#members:starthour}

#### Default Value

* 0

Sets the start hour time range to be displayed on the Schedule.

#### Example

To set the start hour on the Schedule,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                startHour: 9,
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                }
            });
        });
</script>

{% endhighlight %}

### timeMode 'string/enum'
{:#members:timemode}

#### Default Value

* null

Sets either 12 or 24 hour time mode on the Schedule. It accepts either the enum Value ej.Schedule.TimeMode.Hour12 or ej.Schedule.TimeMode.Hour24.

#### Example

To set the 24 hour time mode on the Schedule,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                timeMode: ej.Schedule.TimeMode.Hour24,
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                }
            });
        });
</script>

{% endhighlight %}

### timeZone 'string'
{:#members:timezone}

#### Default Value

* null

Sets the timezone for the Schedule.

#### Example

To set the timezone in Schedule,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                timeZone: "UTC +2:00",
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                }
            });
        });
</script>

{% endhighlight %}

### timeZoneCollection 'object'
{:#members:timezonecollection}

Sets the collection of timezone items to be bound to the Schedule. Only the items bound to this property gets listed out in the timezone field of the appointment window.

### timeZoneCollection.dataSource 'object'
{:#members:timezonecollection-datasource}

Sets the collection of timezone items to the dataSource that accepts either JSON object collection or DataManager ([ej.DataManager](http://helpjs.syncfusion.com/js/datamanager/overview)) instance that contains Schedule timezones.

#### Example

To set the dataSource with array of JSON object collection,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                timeZoneCollection:{
                  dataSource: [
                    { text: "UTC -12:00", id: "1", value: "UTC -12:00" },
                    { text: "UTC -11:00", id: "2", value: "UTC -11:00" },
                    { text: "UTC -10:00", id: "3", value: "UTC -10:00" },
                    { text: "UTC -09:00", id: "4", value: "UTC -09:00" },
                    { text: "UTC -08:00", id: "5", value: "UTC -08:00" },
                    { text: "UTC -07:00", id: "6", value: "UTC -07:00" }]
                }, 
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                }
            });
        });
</script>

{% endhighlight %}

The following are the timeZoneCollection fields that maps the appropriate column names from the dataSource.

### timeZoneCollection.text 'string'
{:#members:timezonecollection-text}

Binds text field name in the dataSource to timeZoneCollection **text**. These text gets listed out in the timezone fields of the appointment window.

### timeZoneCollection.id 'string'
{:#members:timezonecollection-id }

Binds id field name in the dataSource to timeZoneCollection **id**.  

### timeZoneCollection.value 'string'
{:#members:timezonecollection-value }

Binds value field name in the dataSource to timeZoneCollection **value**.

#### Example

To define the timeZoneCollection options by using all the above specified fields,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                timeZoneCollection:{
                  dataSource: [
                    { text: "UTC -12:00", id: "1", value: "UTC -12:00" },
                    { text: "UTC -11:00", id: "2", value: "UTC -11:00" },
                    { text: "UTC -10:00", id: "3", value: "UTC -10:00" },
                    { text: "UTC -09:00", id: "4", value: "UTC -09:00" },
                    { text: "UTC -08:00", id: "5", value: "UTC -08:00" },
                    { text: "UTC -07:00", id: "6", value: "UTC -07:00" }],
                  text: "text", id: "id", value: "value"
                }, 
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                }
            });
        });
</script>

{% endhighlight %}


### views 'array'
{:#members:views }

#### Default Value

* ["Day", "Week", "WorkWeek", "Month", "Agenda"]

Defines the view collection to be displayed on the Schedule. By default, it displays all the views namely, Day, Week, WorkWeek and Month.

#### Example

To display only the day and week view on the Schedule,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                width: "100%",
                currentDate: new Date(2014, 04, 05),
                views: ["Day", "Week"],
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                }
            });
        });
</script>

{% endhighlight %}

### width 'string'
{:#members:width }

#### Default Value

* 100%

Sets the width of the Schedule. Accepts both pixel and percentage values. 

#### Example

To set the width of the Schedule in pixels,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                currentDate: new Date(2014, 04, 05),
                width: "600px",
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00)
                    }]
                }
            });
        });
</script>

{% endhighlight %}

### enableRecurrenceValidation 'boolean'
{:#members:enablerecurrencevalidation}

#### Default Value

* true

When set to true, Schedule allows the validation of recurrence pattern to take place before it is being assigned to the appointments. For example, when one of the instance of recurrence appointment is dragged beyond the next or previous instance of the same recurrence appointment, a pop-up is displayed with the validation message disallowing the drag functionality. 

#### Example

To disable the RecurrenceValidation for Schedule appointments,

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
	            currentDate:new Date(2014,4,5),
                enableRecurrenceValidation: false,
                appointmentSettings: {
                    dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 11, 00),
                        Recurrence: true,
                        RecurrenceRule: "FREQ=DAILY;INTERVAL=1;COUNT=10"

                    }]
                } 
            });
        });
</script>

{% endhighlight %}

### agendaViewSettings 'object'
{:#members:agendaviewsettings }

Sets the week to display more than one week appointment summary.

### agendaViewSettings.daysInAgenda 'number'
{:#members:agendaviewsettings-daysinagenda }

#### Default Value

* 7

You can display the summary of multiple week's appointment by setting this value.

#### Example

To set the daysInAgenda of agendaViewSettings,

{% highlight html %}

<div id="Schedule"></div>
    
<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                currentDate: new Date(2014, 4, 2),
                agendaViewSettings: {
                    daysInAgenda: 10
                }
            });
        });
</script>

{% endhighlight %}


### agendaViewSettings.dateColumnTemplateId 'string'
{:#members:agendaviewsettings-datecolumntemplateid }

#### Default Value

* null

You can customize the Date column display based on the requirement.

#### Example

To display the StartTime value in the date column of agenda View,

{% highlight html %}

<div id="Schedule"></div>

<script id="datecolumntemplate" type="text/x-jsrender">
        <div style="height:100%">           
            <div>
                <div>{{:StartTime}}</div>
            </div>
        </div>
</script>
    
<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                currentDate: new Date(2014, 4, 2),
                agendaViewSettings: {
                    daysInAgenda: 7,
                    dateColumnTemplateId: "#datecolumntemplate"
                },
            });
        });
</script>

{% endhighlight %}

### agendaViewSettings.timeColumnTemplateId 'string'
{:#members:agendaviewsettings-timecolumntemplateid }

#### Default Value

* null

You can customize the time column display based on the requirement.

#### Example

To display the StartTime value in the time column of agenda View.

{% highlight html %}

<div id="Schedule"></div>

<script id="timecolumntemplate" type="text/x-jsrender">
        <div style="height:100%">           
            <div>
                <div>{{:StartTime}}</div>
            </div>
        </div>
</script>
    
<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                currentDate: new Date(2014, 4, 2),
                agendaViewSettings: {
                    daysInAgenda: 7,
                    timeColumnTemplateId: "#timecolumntemplate"
                }
            });
        });
</script>

{% endhighlight %}


### firstDayOfWeek 'string'
{:#members:firstdayofweek}

#### Default Value

* null

You can change or set the starting day of the week.

#### Example

To set Tuesday as starting day of the week.

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                currentDate: new Date(2014, 4, 5),
                firstDayOfWeek:"Tuesday",
            });
        });
</script>

{% endhighlight %}

### workWeek 'array'
{:#members:workweek}

#### Default Value

* ["Monday", "Tuesday", "Wednesday", "Thursday", "Friday"]

You can set the workWeek days of the workWeek.

#### Example

To set Tuesday to Saturday as workWeek days of the workWeek.

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                currentDate: new Date(2014, 4, 5),
                workWeek: ["Tuesday", "Wednesday", "Thursday", "Friday","Saturday"]
            });
        });
</script>

{% endhighlight %}

### tooltipSettings 'object'
{:#members:tooltipsettings}

The tooltip allows to display appointment details in a tooltip while hovering on it.

### tooltipSettings.enable 'boolean'
{:#members:tooltipsettings-enable}

#### Default Value

* false

To enable or disable the tooltip display.

#### Example

To enable the tooltip display.

{% highlight html %}

<div id="Schedule"></div>

<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                currentDate: new Date(2014, 4, 5),
                tooltipSettings:{
                    enable:true
                }
            });
        });
</script>

{% endhighlight %}

### tooltipSettings.template 'string'
{:#members:tooltipsettings-template}

#### Default Value

* null

To customize the tooltip display based on your requirements. 

#### Example

To display the customized tooltip.

{% highlight html %}

<div id="Schedule"></div>

<script id="tooltip" type="text/x-jsrender">                 
            <div>
                <div>Subject: {{:Subject}}</div>
                <div>StartTime: {{:StartTime}}</div>
                <div>EndTime: {{:EndTime}}</div>
            </div>        
</script>
    
<script type="text/javascript">
        $(function () {
            $("#Schedule").ejSchedule({
                currentDate: new Date(2014, 4, 5),
                 tooltipSettings:{
                    enable: true,
                    template:"#tooltip"
                },
            });
        });
</script>

{% endhighlight %}



## Methods


### deleteAppointment()
{:#methods:deleteappointment}

It is used to delete the appointment. The id is based on the argument passed along with this method.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">argument.id</td>
            <td class="type">number</td>
            <td class="description">id value of the appointment</td>
        </tr>
    </tbody>
</table>


#### Example

{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$('#Schedule').ejSchedule({
    appointmentSettings: { 
           dataSource: [{
                        EventId: 105,
                        EventSubject: "Play with Pets",
                        EventStartTime: new Date(2014, 4, 5, 10, 00),
                        EventEndTime: new Date(2014, 4, 5, 12, 00),
                        EventStartTimeZone: "UTC +00:00",
                        EventEndTimeZone: "UTC +00:00"
                    }],
                    id: "EventId",
                    startTime: "EventStartTime",
                    endTime: "EventEndTime",
                    subject: "EventSubject",
                    startTimeZone: "EventStartTimeZone",
                    endTimeZone: "EventEndTimeZone"
            }                            
  });
var schObj = $("#Schedule").data("ejSchedule");
schObj.deleteAppointment(105); //Appointments id number.
</script>

{% endhighlight %}


### destroy()
{:#methods:destroy}

Destroys the Schedule widget. All the events bound using this._on are unbound automatically and the control is moved to pre-init state.


#### Example


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>

$('#Schedule').ejSchedule();
var schObj = $("#Schedule").data("ejSchedule");
schObj.destroy(); // destroy the schedule

</script>

{% endhighlight %}


### exportSchedule()
{:#methods:exportschedule}

Exports the appointments from the Schedule control.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">argument.action</td>
            <td class="type">string</td>
            <td class="description">To refer the controller action name to redirect. (For MVC)</td>
        </tr>
        <tr>
            <td class="name">argument.serverEvent</td>
            <td class="type">string</td>
            <td class="description">To refer the server event name.(For ASP)</td>
        </tr>
        <tr>
            <td class="name">argument.id</td>
            <td class="type">string</td>
            <td class="description">To pass the id of an appointment, in case of a single appointment to be exported. Otherwise, it takes the null value.</td>
        </tr>
    </tbody>
</table>


#### Example


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$('#Schedule').ejSchedule({
    appointmentSettings: { 
        dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 12, 00),
                        StartTimeZone: "UTC +00:00",
                        EndTimeZone: "UTC +00:00
                    },
                    {
                        Id: 102,
                        Subject: "Play with pets",
                        StartTime: new Date(2014, 4, 5, 05, 00),
                        EndTime: new Date(2014, 4, 5, 07, 00),
                        StartTimeZone: "UTC +00:00",
                        EndTimeZone: "UTC +00:00
                    }]
                    id: "Id",
                    startTime: "StartTime",
                    endTime: "EndTime",
                    subject: "Subject",
                    startTimeZone: "StartTimeZone",
                    endTimeZone: "EndTimeZone"
       }                            
  });
var schObj = $("#Schedule").data("ejSchedule");
schObj.exportSchedule("ActionName","ExportToICS", null); // To Export all the Appointments
schObj.exportSchedule("ActionName","ExportToICS", 101); // To Export a single appointment with an id "101"
</script>

{% endhighlight %}

### filterAppointments ()
{:#methods:filterappointments}


Searches the appointments from appointment list of Schedule control.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">argument.filterConditions</td>
            <td class="type">object</td>
            <td class="description">filterConditions value of the filter collections for appointments.</td>
        </tr>
    </tbody>
</table>


#### Example

{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$('#Schedule').ejSchedule({
    appointmentSettings: { 
        dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 12, 00),
                        StartTimeZone: "UTC +00:00",
                        EndTimeZone: "UTC +00:00
                    },
                    {
                        Id: 102,
                        Subject: "Play with pets",
                        StartTime: new Date(2014, 4, 5, 05, 00),
                        EndTime: new Date(2014, 4, 5, 07, 00),
                        StartTimeZone: "UTC +00:00",
                        EndTimeZone: "UTC +00:00
                    },
                    {
                        Id: 103,
                        Subject: "Reading books",
                        StartTime: new Date(2014, 4, 5, 08, 00),
                        EndTime: new Date(2014, 4, 5, 09, 00),
                        StartTimeZone: "UTC +00:00",
                        EndTimeZone: "UTC +00:00
                    }]
                    id: "Id",
                    startTime: "StartTime",
                    endTime: "EndTime",
                    subject: "Subject",
                    startTimeZone: "StartTimeZone",
                    endTimeZone: "EndTimeZone"
       }                            
  });
var schObj = $("#Schedule").data("ejSchedule");
var filter=[{
   field: "Subject",
   operator: "contains",
   value: "with",
   predicate: "or"
}];
var appointments=schObj.filterAppointments(filter); // Gets the appointments list of Schedule control
</script>

{% endhighlight %}

### getAppointments()
{:#methods:getappointments}


Gets the appointment list of Schedule control.

#### Example

{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$('#Schedule').ejSchedule({
    appointmentSettings: { 
        dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 12, 00),
                        StartTimeZone: "UTC +00:00",
                        EndTimeZone: "UTC +00:00
                    },
                    {
                        Id: 102,
                        Subject: "Play with pets",
                        StartTime: new Date(2014, 4, 5, 05, 00),
                        EndTime: new Date(2014, 4, 5, 07, 00),
                        StartTimeZone: "UTC +00:00",
                        EndTimeZone: "UTC +00:00
                    },
                    {
                        Id: 103,
                        Subject: "Reading books",
                        StartTime: new Date(2014, 4, 5, 08, 00),
                        EndTime: new Date(2014, 4, 5, 09, 00),
                        StartTimeZone: "UTC +00:00",
                        EndTimeZone: "UTC +00:00
                    }]
                    id: "Id",
                    startTime: "StartTime",
                    endTime: "EndTime",
                    subject: "Subject",
                    startTimeZone: "StartTimeZone",
                    endTimeZone: "EndTimeZone"
       }                            
  });
var schObj = $("#Schedule").data("ejSchedule");
var appointments=schObj.getAppointments(); // Gets the appointments list of Schedule control
</script>

{% endhighlight %}


### print()
{:#methods:print}


Prints the Schedule.

#### Example


{% highlight html %}
 
<div id="Schedule"></div> 
<script>
$('#Schedule').ejSchedule({
    appointmentSettings: { 
        dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 12, 00),
                        Recurrence:false,
                        RecurrenceRule:null,
                        StartTimeZone: "UTC +00:00",
                        EndTimeZone: "UTC +00:00
                    },
                    {
                        Id: 102,
                        Subject: "Play with pets",
                        StartTime: new Date(2014, 4, 5, 05, 00),
                        EndTime: new Date(2014, 4, 5, 07, 00),
                        Recurrence:true,
                        RecurrenceRule:"FREQ=DAILY;INTERVAL=1;COUNT=10",
                        StartTimeZone: "UTC +00:00",
                        EndTimeZone: "UTC +00:00
                    }]
                    id: "Id",
                    startTime: "StartTime",
                    endTime: "EndTime",
                    subject: "Subject",
                    recurrence:"Recurrence",
                    recurrenceRule:"RecurrenceRule",
                    startTimeZone: "StartTimeZone",
                    endTimeZone: "EndTimeZone"
       }                            
  });
var schObj = $("#Schedule").data("ejSchedule");
schObj.print();
</script>

{% endhighlight %}


### refreshScroller()
{:#methods:refreshscroller}

Refreshes the Scroller while using Schedule control in some other controls.

#### Example

{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$('#Schedule').ejSchedule();
var schObj = $("#Schedule").data("ejSchedule");
schObj.refreshScroller(); // To refresh scroller while using Schedule control in some other control
</script>

{% endhighlight %}


### saveAppointment()
{:#methods:saveappointment}

It is used to save the appointment. The appointment obj is based on the argument passed along with this method.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">argument.obj</td>
            <td class="type">object</td>
            <td class="description">obj of the appointment</td>
        </tr>
    </tbody>
</table>


#### Example

{% highlight html %}
 
<div id="Schedule"></div> 
<script>
$('#Schedule').ejSchedule({
    appointmentSettings: { 
        dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 12, 00),
                        AllDay:true,
                        Recurrence:false,
                        RecurrenceRule:null,
                        StartTimeZone: "UTC +00:00",
                        EndTimeZone: "UTC +00:00
                    }]
                    id: "Id",
                    startTime: "StartTime",
                    endTime: "EndTime",
                    subject: "Subject",
                    allday:"AllDay",
                    recurrence:"Recurrence",
                    recurrenceRule:"RecurrenceRule",
                    startTimeZone: "StartTimeZone",
                    endTimeZone: "EndTimeZone"
        }                            
  });
var schObj = $("#Schedule").data("ejSchedule");
schObj.saveAppointment(obj); //obj contains collection of appointment. 
</script>

{% endhighlight %}



### searchAppointments()
{:#methods:searchappointments}

Searches the appointments from appointment list of Schedule control.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">argument.searchString</td>
            <td class="type">string</td>
            <td class="description">searchString value of the search word in the appointments.</td>
        </tr>
        <tr>
            <td class="name">argument.fields</td>
            <td class="type">string</td>
            <td class="description">field value of fields that requires search.</td>
        </tr>
        <tr>
            <td class="name">argument.filterOperator</td>
            <td class="type">string</td>
            <td class="description">filterOperator value of the search operation.</td>
        </tr>
        <tr>
            <td class="name">argument.ignoreCase</td>
            <td class="type">boolean</td>
            <td class="description">ignoreCase value of the case.</td>
        </tr>
    </tbody>
</table>



#### Example


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$('#Schedule').ejSchedule({
    appointmentSettings: { 
        dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 12, 00),
                        StartTimeZone: "UTC +00:00",
                        EndTimeZone: "UTC +00:00
                    },
                    {
                        Id: 102,
                        Subject: "Play with pets",
                        StartTime: new Date(2014, 4, 5, 05, 00),
                        EndTime: new Date(2014, 4, 5, 07, 00),
                        StartTimeZone: "UTC +00:00",
                        EndTimeZone: "UTC +00:00
                    },
                    {
                        Id: 103,
                        Subject: "Reading books",
                        StartTime: new Date(2014, 4, 5, 08, 00),
                        EndTime: new Date(2014, 4, 5, 09, 00),
                        StartTimeZone: "UTC +00:00",
                        EndTimeZone: "UTC +00:00
                    }]
                    id: "Id",
                    startTime: "StartTime",
                    endTime: "EndTime",
                    subject: "Subject",
                    startTimeZone: "StartTimeZone",
                    endTimeZone: "EndTimeZone"
       }                            
  });
var schObj = $("#Schedule").data("ejSchedule");
var appointments=schObj.searchAppointments("with"); // Gets the appointments list of Schedule control
</script>

{% endhighlight %}

### refresh()
{:#methods:refresh}

To refresh the Schedule control.

#### Example

{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$('#Schedule').ejSchedule();
var schObj = $("#Schedule").data("ejSchedule");
schObj.refresh(); // To refresh the Schedule control within the client side event
</script>

{% endhighlight %}


### refreshAppointment()
{:#methods:refreshappointment}

To Refresh only the Schedule control appointments.

#### Example

{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$('#Schedule').ejSchedule();
var schObj = $("#Schedule").data("ejSchedule");
schObj.refreshAppointment(); // To refresh the Schedule control within the client side event
</script>

{% endhighlight %}






## Events

### actionBegin
{:#events:actionbegin}

Triggers before the action begin of the Schedule.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">argument</td>
            <td class="type">object</td>
            <td class="description">Event parameters when view change action starts:
                <table class="params">
                    <thead>
                        <tr>
                            <th>Name</th>
                            <th>Type</th>
                            <th>Description</th>
                        </tr>
                    </thead>
                <tbody>
                    <tr>
                        <td class="name">argument.data.currentDate</td>
                        <td class="type">date</td>
                        <td class="description">Returns the current date value.</td>
                    </tr>
                    <tr>
                        <td class="name">cancel</td>
                        <td class="type">boolean</td>
                        <td class="description">Returns the cancel option value.</td>
                    </tr>
                    <tr>
                        <td class="name">argument.data.currentView</td>
                        <td class="type">string</td>
                        <td class="description">Returns the current view value.</td>
                    </tr>
                    <tr>
                        <td class="name">model</td>
                        <td class="type">object</td>
                        <td class="description">Returns the Schedule model.</td>
                    </tr>
                    <tr>
                        <td class="name">requestType</td>
                        <td class="type">string</td>
                        <td class="description">Returns the action begin request type.</td>
                    </tr>
                    <tr>
                        <td class="name">target</td>
                        <td class="type">object</td>
                        <td class="description">Returns the target of the click.</td>
                    </tr>
                    <tr>
                        <td class="name">type</td>
                        <td class="type">string</td>
                        <td class="description">Returns the name of the event.</td>
                    </tr>
                </tbody>
                </table>
            </td>
        </tr>
        <tr>
            <td class="name">argument</td>
            <td class="type">object</td>
            <td class="description">Event parameters when date navigate action starts:
            <table class="params">
                <thead>
                    <tr>
                        <th>Name</th>
                        <th>Type</th>
                        <th>Description</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td class="name">cancel</td>
                        <td class="type">boolean</td>
                        <td class="description">Returns the cancel option value.</td>      
                    </tr>
                    <tr>
                        <td class="name">currentDate</td>
                        <td class="type">object</td>
                        <td class="description">Returns the current date value.</td>
                    </tr>
                    <tr>
                        <td class="name">model</td>
                        <td class="type">object</td>
                        <td class="description">Returns the Schedule model.</td>
                    </tr>
                    <tr>
                        <td class="name">requestType</td>
                        <td class="type">string</td>
                        <td class="description">Returns the action begin request type.</td>
                    </tr>
                    <tr>
                        <td class="name">target</td>
                        <td class="type">object</td>
                        <td class="description">Returns the target of the click.</td>
                    </tr>
                    <tr>
                        <td class="name">type</td>
                        <td class="type">string</td>
                        <td class="description">Returns the name of the event.</td>
                    </tr>
                </tbody>
            </table>
            </td>
        </tr>
        <tr>
            <td class="name">argument</td>
            <td class="type">object</td>
            <td class="description">Event parameters when date change by calendar action starts:
            <table class="params">
                <thead>
                    <tr>
                        <th>Name</th>
                        <th>Type</th>
                        <th>Description</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td class="name">cancel</td>
                        <td class="type">boolean</td>
                        <td class="description">Returns the cancel option value.</td>
                    </tr>
                    <tr>
                        <td class="name">currentDate</td>
                        <td class="type">object</td>
                        <td class="description">Returns the current date value.</td>
                    </tr>
                    <tr>
                        <td class="name">model</td>
                        <td class="type">object</td>
                        <td class="description">Returns the Schedule model.</td>
                    </tr>
                    <tr>
                        <td class="name">requestType</td>
                        <td class="type">string</td>
                        <td class="description">Returns the action begin request type.</td>
                    </tr>
                    <tr>
                        <td class="name">target</td>
                        <td class="type">object</td>
                        <td class="description">Returns the target of the click.</td>
                    </tr>
                    <tr>
                        <td class="name">type</td>
                        <td class="type">string</td>
                        <td class="description">Returns the name of the event.</td>
                    </tr>
                </tbody>
                </table>
            </td>
        </tr>
        <tr>
            <td class="name">argument</td>
            <td class="type">object</td>
            <td class="description">Event parameters when appointment save action starts:
                <table class="params">
                    <thead>
                        <tr>
                            <th>Name</th>
                            <th>Type</th>
                            <th class="last">Description</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td class="name">cancel</td>
                            <td class="type">boolean</td>
                            <td class="description">Returns the cancel option value.</td>
                        </tr>
                        <tr>
                            <td class="name">data</td>
                            <td class="type">object</td>                
                            <td class="description">Returns the save appointment value.</td>
                        </tr>                                                                                                                                  <tr>
                            <td class="name">model</td>                                                                                                                                                                                                               <td class="type">object</td>
                            <td class="description">Returns the Schedule model.</td>
                        </tr>
                        <tr>
                            <td class="name">requestType</td>
                            <td class="type">string</td>
                            <td class="description">Returns the action begin request type.</td>
                        </tr>
                        <tr>
                            <td class="name">type</td>
                            <td class="type">string</td>
                            <td class="description">Returns the name of the event.</td>
                        </tr>
                    </tbody>
                </table>
            </td>
        </tr>
        <tr>
            <td class="name">argument</td>
            <td class="type">object</td>
            <td class="description">Event parameters when appointment edit action starts:
            <table class="params">
                <thead>
                    <tr>
                        <th>Name</th>
                        <th>Type</th>
                        <th>Description</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td class="name">cancel</td>
                        <td class="type">boolean</td>
                        <td class="description">Returns the cancel option value.</td>
                    </tr>
                    <tr>
                        <td class="name">data</td>
                        <td class="type">object</td>
                        <td class="description">Returns the edit appointment value.</td>
                    </tr>
                    <tr>
                        <td class="name">model</td>
                        <td class="type">object</td>
                        <td class="description">Returns the Schedule model.</td>
                    </tr>
                    <tr>
                        <td class="name">requestType</td>
                        <td class="type">string</td>
                        <td class="description">Returns the action begin request type.</td>
                    </tr>
                    <tr>
                        <td class="name">type</td>
                        <td class="type">string</td>
                        <td class="description">Returns the name of the event.</td>
                    </tr>
                </tbody>
             </table>
           </td>
        </tr>
        <tr>
            <td class="name">argument</td>
            <td class="type">object</td>
            <td class="description">Event parameters when appointment delete action starts:
            <table class="params">
                <thead>
                    <tr>
                        <th>Name</th>
                        <th>Type</th>
                        <th>Description</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td class="name">cancel</td>
                        <td class="type">boolean</td>
                        <td class="description">Returns the cancel option value.</td>
                    </tr>
                    <tr>
                        <td class="name">id</td>
                        <td class="type">number</td>
                        <td class="description">Returns the id of delete appointment.</td>
                    </tr>
                    <tr>
                        <td class="name">model</td>
                        <td class="type">object</td>
                        <td class="description">Returns the Schedule model.</td>
                    </tr>
                    <tr>
                        <td class="name">requestType</td>
                        <td class="type">string</td>
                        <td class="description">Returns the action begin request type.</td>
                    </tr>
                    <tr>
                        <td class="name">type</td>
                        <td class="type">string</td>
                        <td class="description">Returns the name of the event.</td>
                    </tr>
                </tbody>
            </table>
            </td>
        </tr>
        <tr>
            <td class="name">argument</td>
            <td class="type">object</td>
            <td class="description">Event parameters when appointment drag action starts:
            <table class="params">
                <thead>
                    <tr>
                        <th>Name</th>       
                        <th>Type</th>
                        <th>Description</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td class="name">cancel</td>
                        <td class="type">boolean</td>
                        <td class="description">Returns the cancel option value.</td>
                    </tr>
                    <tr>
                        <td class="name">data</td>
                        <td class="type">object</td>
                        <td class="description">Returns the target of the appointment you drag.</td>
                    </tr>
                    <tr>
                        <td class="name">model</td>
                        <td class="type">object</td>
                        <td class="description">Returns the Schedule model.</td>
                    </tr>
                    <tr>
                        <td class="name">requestType</td>
                        <td class="type">string</td>
                        <td class="description">Returns the action begin request type.</td>
                    </tr>
                    <tr>
                        <td class="name">type</td>
                        <td class="type">string</td>
                        <td class="description">Returns the name of the event.</td>
                    </tr>
                </tbody>
            </table>
            </td>
        </tr>
        <tr>
            <td class="name">argument</td>
            <td class="type">object</td>
            <td class="description">Event parameters when appointment resize action starts:
            <table class="params">
                <thead>
                    <tr>
                        <th>Name</th>
                        <th>Type</th>
                        <th class="last">Description</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td class="name">cancel</td>
                        <td class="type">boolean</td>
                        <td class="description">Returns the cancel option value.</td>
                    </tr>
                    <tr>
                        <td class="name">data</td>
                        <td class="type">object</td>
                        <td class="description">Returns the target of the appointment you resize.</td>
                    </tr>
                    <tr>
                        <td class="name">model</td>
                        <td class="type">object</td>
                        <td class="description">Returns the Schedule model.</td>
                    </tr>
                    <tr>
                        <td class="name">requestType</td>
                        <td class="type">string</td>
                        <td class="description">Returns the action begin request type.</td>
                    </tr>
                    <tr>
                        <td class="name">type</td>
                        <td class="type">string</td>
                        <td class="description">Returns the name of the event.</td>
                    </tr>
                </tbody>
            </table>
            </td>
         </tr>
    </tbody>
</table>



#### Example

{% highlight html %}

<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
   actionBegin: function (args) {}
});
</script>

{% endhighlight %}


### actionComplete
{:#events:actioncomplete}


Triggers after the completion of action in the Schedule.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
    <tr>
        <td class="name">argument</td>
        <td class="type">object</td>
        <td class="description">Event parameters when view change action completes:
        <table class="params">
            <thead>
                <tr>
                    <th>Name</th>
                    <th>Type</th>
                    <th>Description</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td class="name">cancel</td>
                    <td class="type">boolean</td>
                    <td class="description">Returns the cancel option value.</td>
                </tr>
                <tr>
                    <td class="name">data</td>
                    <td class="type">object</td>
                    <td class="description">Returns the data about viewchange action.</td>
                </tr>
                <tr>
                    <td class="name">model</td>
                    <td class="type">object</td>
                    <td class="description">Returns the Schedule model.</td>
                </tr>
                <tr>
                    <td class="name">requestType</td>
                    <td class="type">string</td>
                    <td class="description">Returns the action complete request type.</td>
                </tr>
                <tr>
                    <td class="name">type</td>
                    <td class="type">string</td>
                    <td class="description">Returns the name of the event.</td>
                </tr>
            </tbody>
        </table>
        </td>
    </tr>
    <tr>
        <td class="name">argument</td>
        <td class="type">object</td>
        <td class="description">Event parameters when date navigate action completes:
        <table class="params">
            <thead>
                <tr>
                    <th>Name</th>
                    <th>Type</th>
                    <th>Description</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td class="name">cancel</td>
                    <td class="type">boolean</td>
                    <td class="description">Returns the cancel option value.</td>
                </tr>
                <tr>
                    <td class="name">data</td>
                    <td class="type">object</td>
                    <td class="description">Returns the data about the date navigate action.</td>
                </tr>
                <tr>
                    <td class="name">model</td>
                    <td class="type">object</td>
                    <td class="description">Returns the Schedule model.</td>
                </tr>
                <tr>
                    <td class="name">requestType</td>
                    <td class="type">string</td>
                    <td class="description">Returns the action complete request type.</td>
                </tr>
                <tr>
                    <td class="name">type</td>
                    <td class="type">string</td>
                    <td class="description">Returns the name of the event.</td>
                </tr>
            </tbody>
        </table>
        </td>
    </tr>
    <tr>
        <td class="name">argument</td>
        <td class="type">object</td>
        <td class="description">Event parameters when date change by calendar action completes:
        <table class="params">
            <thead>
                <tr>
                    <th>Name</th>
                    <th>Type</th>
                    <th>Description</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td class="name">cancel</td>
                    <td class="type">boolean</td>
                    <td class="description">Returns the cancel option value.</td>
                </tr>
                <tr>
                    <td class="name">data</td>
                    <td class="type">object</td>
                    <td class="description">Returns the data about calendar navigation action.</td>
                </tr>
                <tr>
                    <td class="name">model</td>
                    <td class="type">object</td>
                    <td class="description">Returns the Schedule model.</td>
                </tr>
                <tr>
                    <td class="name">requestType</td>
                    <td class="type">string</td>
                    <td class="description">Returns the action complete request type.</td>
                </tr>
                <tr>
                    <td class="name">type</td>
                    <td class="type">string</td>
                    <td class="description">Returns the name of the event.</td>
                </tr>
            </tbody>
        </table>
        </td>
    </tr>
    <tr>
        <td class="name">argument</td>
        <td class="type">object</td>
        <td class="description">Event parameters when appointment save action completes:
        <table class="params">
            <thead>
                <tr>
                    <th>Name</th>
                    <th>Type</th>
                    <th class="last">Description</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td class="name">cancel</td>
                    <td class="type">boolean</td>
                    <td class="description">Returns the cancel option value.</td>
                </tr>
                <tr>
                    <td class="name">data</td>
                    <td class="type">object</td>
                    <td class="description">Returns the data about appointment saved value.</td>
                </tr>
                <tr>
                    <td class="name">model</td>
                    <td class="type">object</td>
                    <td class="description">Returns the Schedule model.</td>
                </tr>
                <tr>
                    <td class="name">requestType</td>
                    <td class="type">string</td>
                    <td class="description">Returns the action complete request type.</td>
                </tr>
                <tr>
                    <td class="name">type</td>
                    <td class="type">string</td>
                    <td class="description">Returns the name of the event.</td>
                </tr>
            </tbody>
          </table>
        </td>
    </tr>
    <tr>
        <td class="name">argument</td>
        <td class="type">object</td>
        <td class="description">Event parameters when appointment edit action completes:
        <table class="params">
            <thead>
                <tr>
                    <th>Name</th>
                    <th>Type</th>
                    <th class="last">Description</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td class="name">cancel</td>
                    <td class="type">boolean</td>
                    <td class="description">Returns the cancel option value.</td>
                </tr>
                <tr>
                    <td class="name">data</td>
                    <td class="type">object</td>
                    <td class="description">Returns the data about appointment edited value.</td>
                </tr>
                <tr>
                    <td class="name">model</td>
                    <td class="type">object</td>
                    <td class="description">Returns the Schedule model.</td>
                </tr>
                <tr>
                    <td class="name">requestType</td>
                    <td class="type">string</td>
                    <td class="description">Returns the action complete request type.</td>
                </tr>
                <tr>
                    <td class="name">type</td>
                    <td class="type">string</td>
                    <td class="description">Returns the name of the event.</td>
                </tr>
              </tbody>
            </table>
        </td>
    </tr>
    <tr>
        <td class="name">argument</td>
        <td class="type">object</td>
        <td class="description">Event parameters when appointment delete action completes:
        <table class="params">
            <thead>
                <tr>
                    <th>Name</th>
                    <th>Type</th>
                    <th>Description</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td class="name">cancel</td>
                    <td class="type">boolean</td>
                    <td class="description">Returns the cancel option value.</td>
                </tr>
                <tr>
                    <td class="name">data</td>
                    <td class="type">object</td>
                    <td class="description">Returns the data about appointment deleted action.</td>
                </tr>
                <tr>
                    <td class="name">model</td>
                    <td class="type">object</td>
                    <td class="description">Returns the Schedule model.</td>
                </tr>
                <tr>
                    <td class="name">requestType</td>
                    <td class="type">string</td>
                    <td class="description">Returns the action complete request type.</td>
                </tr>
                <tr>
                    <td class="name">type</td>
                    <td class="type">string</td>
                    <td class="description">Returns the name of the event.</td>
                </tr>
            </tbody>
          </table>
        </td>
    </tr>
    <tr>
        <td class="name">argument</td>
        <td class="type">object</td>
        <td class="description">Event parameters when appointment dragging action completes:
        <table class="params">
            <thead>
                <tr>
                    <th>Name</th>
                    <th>Type</th>
                    <th>Description</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td class="name">appointment</td>
                    <td class="type">object</td>
                    <td class="description">Returns the appointment data dropped.</td>
                </tr>
                <tr>
                    <td class="name">cancel</td>
                    <td class="type">boolean</td>
                    <td class="description">Returns the cancel option value.</td>
                </tr>
                <tr>
                    <td class="name">model</td>
                    <td class="type">object</td>
                    <td class="description">Returns the Schedule model.</td>
                </tr>
                <tr>
                    <td class="name">requestType</td>
                    <td class="type">string</td>
                    <td class="description">Returns the action complete request type.</td>
                </tr>
                <tr>
                    <td class="name">type</td>
                    <td class="type">string</td>
                    <td class="description">Returns the name of the event.</td>
                </tr>
             </tbody>
        </table>
        </td>
    </tr>
    <tr>
        <td class="name">argument</td>
        <td class="type">object</td>
        <td class="description">Event parameters when appointment resizing action completes:
        <table class="params">
            <thead>
                <tr>
                    <th>Name</th>
                    <th>Type</th>
                    <th>Description</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td class="name">cancel</td>
                    <td class="type">boolean</td>
                    <td class="description">Returns the cancel option value.</td>
                </tr>
                <tr>
                    <td class="name">data</td>
                    <td class="type">object</td>
                    <td class="description">Returns the element we resized.</td>
                </tr>
                <tr>
                    <td class="name">model</td>
                    <td class="type">object</td>
                    <td class="description">Returns the Schedule model.</td>
                </tr>
                <tr>
                    <td class="name">requestType</td>
                    <td class="type">string</td>
                    <td class="description">Returns the action complete request type.</td>
                </tr>
                <tr>
                    <td class="name">type</td>
                    <td class="type">string</td>
                    <td class="description">Returns the name of the event.</td>
                </tr>
            </tbody>
        </table>
        </td>
    </tr>
    </tbody>
</table>




#### Example


{% highlight html %}

<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
   actionComplete: function (args) {}
});
</script>

{% endhighlight %}


### appointmentClick
{:#events:appointmentclick}

Triggers after the appointment is clicked.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">argument.object</td>
            <td class="type">object</td>
            <td class="description">Returns the object of appointmentClick event.</td>
        </tr>
        <tr>
            <td class="name">argument.appointment</td>
            <td class="type">object</td>
            <td class="description">Returns the clicked appointment object.</td>
        </tr>
        <tr>
            <td class="name">argument.cancel</td>
            <td class="type">boolean</td>
            <td class="description">Returns the cancel option value.</td>
        </tr>
        <tr>
            <td class="name">argument.model</td>
            <td class="type">object</td>
            <td class="description">Returns the Schedule model.</td>
        </tr>
        <tr>
            <td class="name">argument.type</td>
            <td class="type">string</td>
            <td class="description">Returns the name of the event.</td>
        </tr>
    </tbody>
</table>




#### Example


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { 
        dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 12, 00),
                        AllDay:true,
                        Recurrence:false,
                        RecurrenceRule:null,
                        StartTimeZone: "UTC +00:00",
                        EndTimeZone: "UTC +00:00
                    }]
                    id: "Id",
                    startTime: "StartTime",
                    endTime: "EndTime",
                    subject: "Subject",
                    allday:"AllDay",
                    recurrence:"Recurrence",
                    recurrenceRule:"RecurrenceRule",
                    startTimeZone: "StartTimeZone",
                    endTimeZone: "EndTimeZone"
        },   
        appointmentClick: function (args) {}
});
</script>

{% endhighlight %}

### appointmentDeleted
{:#events:appointmentdeleted}


Triggers after the appointment is deleted.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">argument.object</td>
            <td class="type">object</td>
            <td class="description">Returns the object of appointmentDeleted event.</td>
        </tr>
        <tr>
            <td class="name">argument.cancel</td>
            <td class="type">boolean</td>
            <td class="description">Returns the cancel option value.</td>
        </tr>
        <tr>
            <td class="name">argument.appointment</td>
            <td class="type">object</td>
            <td class="description">Returns the deleted appointment object.</td>
        </tr>
        <tr>
            <td class="name">argument.model</td>
            <td class="type">object</td>
            <td class="description">Returns the Schedule model.</td>
        </tr>
        <tr>
            <td class="name">argument.type</td>
            <td class="type">string</td>
            <td class="description">Returns the name of the event.</td>
        </tr>
    </tbody>
</table>




#### Example


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { 
        dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 12, 00),
                        AllDay:true,
                        Recurrence:false,
                        RecurrenceRule:null,
                        StartTimeZone: "UTC +00:00",
                        EndTimeZone: "UTC +00:00
                    },
                    {
                        Id: 102,
                        Subject: "Play with Pets",
                        StartTime: new Date(2014, 4, 6, 10, 00),
                        EndTime: new Date(2014, 4, 6, 12, 00),
                        AllDay:false,
                        Recurrence:false,
                        RecurrenceRule:null,
                        StartTimeZone: "UTC +00:00",
                        EndTimeZone: "UTC +00:00
                    }]
                    id: "Id",
                    startTime: "StartTime",
                    endTime: "EndTime",
                    subject: "Subject",
                    allday:"AllDay",
                    recurrence:"Recurrence",
                    recurrenceRule:"RecurrenceRule",
                    startTimeZone: "StartTimeZone",
                    endTimeZone: "EndTimeZone"
        },
   appointmentDeleted: function (args) {}
});
</script>

{% endhighlight %}


### appointmentEdited
{:#events:appointmentedited}


Triggers after the appointment is edited.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">argument.object</td>
            <td class="type">object</td>
            <td class="description">Returns the object of appointmentEdited event.</td>
        </tr>
        <tr>
            <td class="name">argument.appointment</td>
            <td class="type">object</td>
            <td class="description">Returns the edited appointment object.</td>
        </tr>
        <tr>
            <td class="name">argument.cancel</td>
            <td class="type">boolean</td>
            <td class="description">Returns the cancel option value.</td>
        </tr>
        <tr>
            <td class="name">argument.model</td>
            <td class="type">object</td>
            <td class="description">Returns the Schedule model.</td>
        </tr>
        <tr>
            <td class="name">argument.type</td>
            <td class="type">string</td>
            <td class="description">Returns the name of the event.</td>
        </tr>
    </tbody>
</table>




#### Example

{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { 
        dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 12, 00),
                        AllDay:true,
                        Recurrence:false,
                        RecurrenceRule:null,
                        StartTimeZone: "UTC +00:00",
                        EndTimeZone: "UTC +00:00
                    },
                    {
                        Id: 102,
                        Subject: "Play with Pets",
                        StartTime: new Date(2014, 4, 6, 10, 00),
                        EndTime: new Date(2014, 4, 6, 12, 00),
                        AllDay:false,
                        Recurrence:false,
                        RecurrenceRule:null,
                        StartTimeZone: "UTC +00:00",
                        EndTimeZone: "UTC +00:00
                    }]
                    id: "Id",
                    startTime: "StartTime",
                    endTime: "EndTime",
                    subject: "Subject",
                    allday:"AllDay",
                    recurrence:"Recurrence",
                    recurrenceRule:"RecurrenceRule",
                    startTimeZone: "StartTimeZone",
                    endTimeZone: "EndTimeZone"
        },
   appointmentEdited: function (args) {}
});
</script>

{% endhighlight %}


### appointmentHover
{:#events:appointmenthover}


Triggers after the appointment is hovered.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">argument.object</td>
            <td class="type">object</td>
            <td class="description">Returns the object of appointmentHover event.</td>
        </tr>
        <tr>
            <td class="name">argument.appointment</td>
            <td class="type">object</td>
            <td class="description">Returns the hovered appointment object.</td>
        </tr>
        <tr>
            <td class="name">argument.cancel</td>
            <td class="type">boolean</td>
            <td class="description">Returns the cancel option value.</td>
        </tr>
        <tr>
            <td class="name">argument.model</td>
            <td class="type">object</td>
            <td class="description">Returns the Schedule model.</td>
        </tr>
        <tr>
            <td class="name">argument.type</td>
            <td class="type">string</td>
            <td class="description">Returns the name of the event.</td>
        </tr>
    </tbody>
</table>




#### Example

{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { 
        dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 12, 00),
                        AllDay:true,
                        Recurrence:false,
                        RecurrenceRule:null,
                        StartTimeZone: "UTC +00:00",
                        EndTimeZone: "UTC +00:00
                    }]
                    id: "Id",
                    startTime: "StartTime",
                    endTime: "EndTime",
                    subject: "Subject",
                    allday:"AllDay",
                    recurrence:"Recurrence",
                    recurrenceRule:"RecurrenceRule",
                    startTimeZone: "StartTimeZone",
                    endTimeZone: "EndTimeZone"
        },   
   appointmentHover: function (args) {}
});
</script>

{% endhighlight %}

### appointmentSaved
{:#events:appointmentsaved}

Triggers after the appointment is saved.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">argument.object</td>
            <td class="type">object</td>
            <td class="description">Returns the object of appointmentSaved event by using appointment window.</td>
        </tr>
        <tr>
            <td class="name">argument.appointment</td>
            <td class="type">object</td>
            <td class="description">Returns the saved appointment object.</td>
        </tr>
        <tr>
            <td class="name">argument.cancel</td>
            <td class="type">boolean</td>
            <td class="description">Returns the cancel option value.</td>
        </tr>
        <tr>
            <td class="name">argument.model</td>
            <td class="type">object</td>
            <td class="description">Returns the Schedule model.</td>
        </tr>
        <tr>
            <td class="name">argument.type</td>
            <td class="type">string</td>
            <td class="description">Returns the name of the event.</td>
        </tr>
        <tr>
            <td class="name">argument.object</td>
            <td class="type">object</td>
            <td class="description">Returns the object of appointmentSaved event by using quick window.</td>
        </tr>
        <tr>
            <td class="name">argument.cancel</td>
            <td class="type">boolean</td>
            <td class="description">Returns the cancel option value.</td>
        </tr>
        <tr>
            <td class="name">argument.appointment</td>
            <td class="type">object</td>
            <td class="description">Returns the saved appointment object.</td>
        </tr>
        <tr>
            <td class="name">argument.model</td>
            <td class="type">object</td>
            <td class="description">Returns the Schedule model.</td>
        </tr>
        <tr>
            <td class="name">argument.type</td>
            <td class="type">string</td>
            <td class="description">Returns the name of the event.</td>
        </tr>
    </tbody>
</table>




#### Example

{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
   appointmentSaved: function (args) {}
});
</script>

{% endhighlight %}


### appointmentWindowOpen
{:#events:appointmentwindowopen}

Triggers before the appointment window opens.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">argument.object</td>
            <td class="type">object</td>
            <td class="description">returns the object of appointmentWindowOpen event while selecting the detail option from quick window.</td>
        </tr>
        <tr>
            <td class="name">argument.cancel</td>
            <td class="type">boolean</td>
            <td class="description">Returns the cancel option value.</td>
        </tr>
        <tr>
            <td class="name">argument.endTime</td>
            <td class="type">object</td>
            <td class="description">Returns the end time of the double clicked cell.</td>
        </tr>
        <tr>
            <td class="name">argument.model</td>
            <td class="type">object</td>
            <td class="description">Returns the Schedule model.</td>
        </tr>
        <tr>
            <td class="name">argument.originalEventType</td>
            <td class="type">string</td>
            <td class="description">Returns the action name that triggers window open.</td>
        </tr>
        <tr>
            <td class="name">argument.startTime</td>
            <td class="type">object</td>
            <td class="description">Returns the start time of the double clicked cell.</td>
        </tr>
        <tr>
            <td class="name">argument.target</td>
            <td class="type">object</td>
            <td class="description">Returns the target of the double clicked cell.</td>
        </tr>
        <tr>
            <td class="name">argument.type</td>
            <td class="type">string</td>
            <td class="description">Returns the name of the event.</td>
        </tr>
        <tr>
            <td class="name">argument.object</td>
            <td class="type">object</td>
            <td class="description">Returns the object of edit appointmentWindowOpen event while selecting the edit appointment or edit series option.</td>
        </tr>
        <tr>
            <td class="name">argument.appointment</td>
            <td class="type">object</td>
            <td class="description">Returns the edit appointment object.</td>
        </tr>
        <tr>
            <td class="name">argument.cancel</td>
            <td class="type">boolean</td>
            <td class="description">Returns the cancel option value.</td>
        </tr>
        <tr>
            <td class="name">argument.edit</td>
            <td class="type">boolean</td>
            <td class="description">Returns the edit occurrence option value.</td>
        </tr>
        <tr>
            <td class="name">argument.model</td>
            <td class="type">object</td>
            <td class="description">Returns the Schedule model.</td>
        </tr>
        <tr>
            <td class="name">argument.type</td>
            <td class="type">string</td>
            <td class="description">Returns the name of the event.</td>
        </tr>
    </tbody>
</table>




#### Example


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
   appointmentWindowOpen: function (args) {}
});
</script>

{% endhighlight %}


### beforeContextMenuOpen
{:#events:beforecontextmenuopen}


Triggers before the context menu opens.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">argument.object</td>
            <td class="type">object</td>
            <td class="description">Returns the object of beforeContextMenuOpen event.</td>
        </tr>
        <tr>
            <td class="name">argument.cancel</td>
            <td class="type">boolean</td>
            <td class="description">Returns the cancel option value.</td>
        </tr>
        <tr>
            <td class="name">argument.cellIndex</td>
            <td class="type">number</td>
            <td class="description">Returns the current cell index value.</td>
        </tr>
        <tr>
            <td class="name">argument.currentDate</td>
            <td class="type">date</td>
            <td class="description">Returns the current date value.</td>
        </tr>
        <tr>
            <td class="name">argument.resources</td>
            <td class="type">object</td>
            <td class="description">Returns the current resource details, when multiple resources are present, otherwise returns null.</td>
        </tr>
        <tr>
            <td class="name">argument.appointment</td>
            <td class="type">object</td>
            <td class="description">Returns the current appointment details while opening the menu from appointment.</td>
        </tr>
        <tr>
            <td class="name">argument.events</td>
            <td class="type">object</td>
            <td class="description">Returns the object of before opening menu target.</td>
        </tr>
        <tr>
            <td class="name">argument.model</td>
            <td class="type">object</td>
            <td class="description">Returns the Schedule model.</td>
        </tr>
        <tr>
            <td class="name">argument.type</td>
            <td class="type">string</td>
            <td class="description">Returns the name of the event.</td>
        </tr>   
    </tbody>
</table>




#### Example

{% highlight html %}

<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
   beforeContextMenuOpen: function (args) {}
});
</script>

{% endhighlight %}


### cellClick
{:#events:cellclick}

Triggers after the cell is clicked.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">argument.object</td>
            <td class="type">object</td>
            <td class="description">Returns the object of cellClick event.</td>
        </tr>
        <tr>
            <td class="name">argument.cancel</td>
            <td class="type">boolean</td>
            <td class="description">Returns the cancel option value.</td>
        </tr>
        <tr>
            <td class="name">argument.endTime</td>
            <td class="type">object</td>
            <td class="description">Returns the end time of the clicked cell.</td>
        </tr>
        <tr>
            <td class="name">argument.model</td>
            <td class="type">object</td>
            <td class="description">Returns the Schedule model.</td>
        </tr>
        <tr>
            <td class="name">argument.startTime</td>
            <td class="type">object</td>
            <td class="description">Returns the start time of the clicked cell.</td>
        </tr>
        <tr>
            <td class="name">argument.target</td>
            <td class="type">object</td>
            <td class="description">Returns the target of the clicked cell.</td>
        </tr>
        <tr>
            <td class="name">argument.type</td>
            <td class="type">string</td>
            <td class="description">Returns the name of the event.</td>
        </tr>
    </tbody>
</table>




#### Example


{% highlight html %}

<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
   cellClick: function (args) {}
});
</script>

{% endhighlight %}


### cellDoubleClick
{:#events:celldoubleclick}


Triggers after the cell is clicked twice.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">argument.object</td>
            <td class="type">object</td>
            <td class="description">Returns the object of cellDoubleClick event.</td>
        </tr>
        <tr>
            <td class="name">argument.cancel</td>
            <td class="type">boolean</td>
            <td class="description">Returns the cancel option value.</td>
        </tr>
        <tr>
            <td class="name">argument.endTime</td>
            <td class="type">object</td>
            <td class="description">Returns the end time of the double clicked cell.</td>
        </tr>
        <tr>
            <td class="name">argument.model</td>
            <td class="type">object</td>
            <td class="description">Returns the Schedule model.</td>
        </tr>
        <tr>
            <td class="name">argument.startTime</td>
            <td class="type">object</td>
            <td class="description">Returns the start time of the double clicked cell.</td>
        </tr>
        <tr>
            <td class="name">argument.target</td>
            <td class="type">object</td>
            <td class="description">Returns the target of the double clicked cell.</td>
        </tr>
        <tr>
            <td class="name">argument.type</td>
            <td class="type">string</td>
            <td class="description">Returns the name of the event.</td>
        </tr>
    </tbody>
</table>




#### Example

{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
   cellDoubleClick: function (args) {}
});
</script>

{% endhighlight %}


### cellHover
{:#events:cellhover}

Triggers after the cell is hovered.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">argument.object</td>
            <td class="type">object</td>
            <td class="description">Returns the object of cellHover event.</td>
        </tr>   
        <tr>
            <td class="name">argument.cancel</td>
            <td class="type">boolean</td>
            <td class="description">Returns the cancel option value.</td>
        </tr>
        <tr>
            <td class="name">argument.cellIndex</td>
            <td class="type">object</td>
            <td class="description">Returns the index of the hovered cell.</td>
        </tr>
        <tr>
            <td class="name">argument.currentDate</td>
            <td class="type">object</td>
            <td class="description">Returns the current date of the hovered cell.</td>
        </tr>
        <tr>
            <td class="name">argument.model</td>
            <td class="type">object</td>
            <td class="description">Returns the Schedule model.</td>
        </tr>
        <tr>
            <td class="name">argument.target</td>
            <td class="type">object</td>
            <td class="description">Returns the target of the clicked cell.</td>
        </tr>
        <tr>
            <td class="name">argument.type</td>
            <td class="type">string</td>
            <td class="description">Returns the name of the event.</td>
        </tr>
    </tbody>
</table>




#### Example

{% highlight html %}

<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
   cellHover: function (args) {}
});
</script>

{% endhighlight %}

### drag
{:#events:drag}

Triggers while the appointment is being dragged over the workcells.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Type</th>
            <th>Description</th>       
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">argument.object</td>
            <td class="type">object</td>
            <td class="description">Returns the object of dragOver event.</td>
        </tr>
        <tr>
            <td class="name">argument.cancel</td>
            <td class="type">boolean</td>
            <td class="description">Returns the cancel option value.</td>
        </tr>
        <tr>
            <td class="name">argument.model</td>
            <td class="type">object</td>
            <td class="description">Returns the Schedule model.</td>
        </tr>
        <tr>
            <td class="name">argument.target</td>
            <td class="type">object</td>
            <td class="description">Returns the target of the drag over appointment.</td>
        </tr>
        <tr>
            <td class="name">argument.type</td>
            <td class="type">string</td>
            <td class="description">Returns the name of the event.</td>
        </tr>
    </tbody>
</table>




#### Example


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { 
        dataSource: [{
                        Id: 102,
                        Subject: "Play with Pets",
                        StartTime: new Date(2014, 4, 6, 10, 00),
                        EndTime: new Date(2014, 4, 6, 12, 00),
                        AllDay:false,
                        Recurrence:false,
                        RecurrenceRule:null,
                        StartTimeZone: "UTC +00:00",
                        EndTimeZone: "UTC +00:00
                    }]
                    id: "Id",
                    startTime: "StartTime",
                    endTime: "EndTime",
                    subject: "Subject",
                    allday:"AllDay",
                    recurrence:"Recurrence",
                    recurrenceRule:"RecurrenceRule",
                    startTimeZone: "StartTimeZone",
                    endTimeZone: "EndTimeZone"
        },
   drag: function (args) {}
});
</script>

{% endhighlight %}

### dragStart
{:#events:dragstart}

Triggers when the appointment dragging begins.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">argument.object</td>
            <td class="type">object</td>
            <td class="description">Returns the object of dargStart event.</td>
        </tr>
        <tr>
            <td class="name">argument.cancel</td>
            <td class="type">boolean</td>
            <td class="description">Returns the cancel option value.</td>
        </tr>
        <tr>
            <td class="name">argument.model</td>
            <td class="type">object</td>
            <td class="description">Returns the Schedule model.</td>
        </tr>
        <tr>
            <td class="name">argument.target</td>
            <td class="type">object</td>
            <td class="description">Returns the target of the dragging appointment.</td>
        </tr>
        <tr>
            <td class="name">argument.type</td>
            <td class="type">string</td>
            <td class="description">Returns the name of the event.</td>
        </tr>
    </tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { 
        dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 12, 00),
                        AllDay:false,
                        Recurrence:false,
                        RecurrenceRule:null,
                        StartTimeZone: "UTC +00:00",
                        EndTimeZone: "UTC +00:00
                    }]
                    id: "Id",
                    startTime: "StartTime",
                    endTime: "EndTime",
                    subject: "Subject",
                    allday:"AllDay",
                    recurrence:"Recurrence",
                    recurrenceRule:"RecurrenceRule",
                    startTimeZone: "StartTimeZone",
                    endTimeZone: "EndTimeZone"
        },
   dragStart: function (args) {}
});
</script>

{% endhighlight %}

### dragStop
{:#events:dragstop}

Triggers when the appointment is dropped.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">argument.object</td>
            <td class="type">object</td>
            <td class="description">Returns the object of dragDrop event.</td>
        </tr>
        <tr>
            <td class="name">argument.appointment</td>
            <td class="type">object</td>
            <td class="description">Returns the dropped appointment object.</td>
        </tr>
        <tr>
            <td class="name">argument.cancel</td>
            <td class="type">boolean</td>
            <td class="description">Returns the cancel option value.</td>
        </tr>
        <tr>
            <td class="name">argument.model</td>
            <td class="type">object</td>
            <td class="description">Returns the Schedule model.</td>
        </tr>
        <tr>
            <td class="name">argument.type</td>
            <td class="type">string</td>
            <td class="description">Returns the name of the event.</td>
        </tr>
    </tbody>
</table>




#### Example

{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>

$("#Schedule").ejSchedule({
    appointmentSettings: { 
        dataSource: [{
                        Id: 101,
                        Subject: "Talk with Nature",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 12, 00),
                        AllDay:true,
                        Recurrence:false,
                        RecurrenceRule:null,
                        StartTimeZone: "UTC +00:00",
                        EndTimeZone: "UTC +00:00
                    },
                    {
                        Id: 102,
                        Subject: "Play with Pets",
                        StartTime: new Date(2014, 4, 6, 10, 00),
                        EndTime: new Date(2014, 4, 6, 12, 00),
                        AllDay:false,
                        Recurrence:false,
                        RecurrenceRule:null,
                        StartTimeZone: "UTC +00:00",
                        EndTimeZone: "UTC +00:00
                    }]
                    id: "Id",
                    startTime: "StartTime",
                    endTime: "EndTime",
                    subject: "Subject",
                    allday:"AllDay",
                    recurrence:"Recurrence",
                    recurrenceRule:"RecurrenceRule",
                    startTimeZone: "StartTimeZone",
                    endTimeZone: "EndTimeZone"
        },
   dragStop: function (args) {}
});
</script>

{% endhighlight %}


### menuItemClick
{:#events:menuitemclick}


Triggers after the context menu is clicked.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">argument.object</td>
            <td class="type">object</td>
            <td class="description">Returns the object of menuItemClick event.</td>
        </tr>
        <tr>
            <td class="name">argument.cancel</td>
            <td class="type">boolean</td>
            <td class="description">Returns the cancel option value.</td>
        </tr>
        <tr>
            <td class="name">argument.events</td>
            <td class="type">object</td>
            <td class="description">Returns the object of menu item event.</td>
        </tr>
        <tr>
            <td class="name">argument.model</td>
            <td class="type">object</td>
            <td class="description">Returns the Schedule model.</td>
        </tr>
        <tr>
            <td class="name">argument.type</td>
            <td class="type">string</td>
            <td class="description">Returns the name of the event.</td>
        </tr>
    </tbody>
</table>




#### Example

{% highlight html %}

<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
   menuItemClick: function (args) {}
});
</script>

{% endhighlight %}


### navigation
{:#events:navigation}

Triggers after the Schedule view or date is navigated.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">argument</td>
            <td class="type">object</td>
            <td class="description">Event parameters when view changes:
            Returns the object of Schedule view navigation event.
            <table class="params">
                <thead>
                    <tr>
                        <th>Name</th>
                        <th>Type</th>
                        <th>Description</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>    
                        <td class="name">argument.currentDate</td>
                        <td class="type">date</td>
                        <td class="description">Returns the current date object.</td>
                    </tr>
                    <tr>
                        <td class="name">argument.cancel</td>
                        <td class="type">boolean</td>
                        <td class="description">Returns the cancel option value.</td>
                    </tr>
                    <tr>
                        <td class="name">argument.model</td>
                        <td class="type">object</td>
                        <td class="description">Returns the Schedule model.</td>
                    </tr>
                    <tr>
                        <td class="name">argument.currentView</td>
                        <td class="type">string</td>
                        <td class="description">Returns the current view value.</td>
                    </tr>
                    <tr>
                        <td class="name">argument.previousView</td>
                        <td class="type">string</td>
                        <td class="description">Returns the previous view value.</td>
                    </tr>
                    <tr>
                        <td class="name">argument.target</td>
                        <td class="type">object</td>
                        <td class="description">Returns the target of the action.</td>
                    </tr>
                    <tr>
                        <td class="name">argument.type</td>
                        <td class="type">string</td>
                        <td class="description">Returns the name of the event.</td>
                    </tr>
                </tbody>
            </table>
            </td>   
        </tr>
        <tr>
            <td class="name">argument</td>
            <td class="type">object</td>
            <td class="description">Returns the object of previous or next date navigation event:
            <table class="params">
                <thead>
                    <tr>
                        <th>Name</th>
                        <th>Type</th>
                        <th>Description</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td class="name">argument.cancel</td>
                        <td class="type">boolean</td>
                        <td class="description">Returns the cancel option value.</td>
                    </tr>
                    <tr>
                        <td class="name">argument.model</td>
                        <td class="type">object</td>
                        <td class="description">Returns the Schedule model.</td>
                    </tr>
                    <tr>
                        <td class="name">argument.currentDate</td>
                        <td class="type">object</td>
                        <td class="description">Returns the new date of the Schedule.</td>
                    </tr>
                    <tr>
                        <td class="name">argument.previousDate</td>
                        <td class="type">object</td>
                        <td class="description">Returns the previous date of the Schedule.</td>
                    </tr>
                    <tr>
                        <td class="name">argument.target</td>
                        <td class="type">object</td>
                        <td class="description">Returns the target of the action.</td>
                    </tr>
                    <tr>
                        <td class="name">argument.type</td>
                        <td class="type">string</td>
                        <td class="description">Returns the name of the event.</td>
                    </tr>
                </tbody>
            </table>
            </td>
        </tr>
        <tr>
            <td class="name">argument</td>
            <td class="type">object</td>
            <td class="description">Returns the navigation event while changing the date by using calendar in Schedule.
            <table class="params">
                <thead>
                    <tr>
                        <th>Name</th>
                        <th>Type</th>
                        <th>Description</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td class="name">argument.cancel</td>
                        <td class="type">boolean</td>
                        <td class="description">Returns the cancel option value.</td>
                    </tr>
                    <tr>
                        <td class="name">argument.model</td>
                        <td class="type">object</td>
                        <td class="description">Returns the Schedule model.</td>
                    </tr>
                    <tr>
                        <td class="name">argument.currentDate</td>
                        <td class="type">object</td>
                        <td class="description">Returns the new date of the Schedule.</td>
                    </tr>
                    <tr>
                        <td class="name">argument.previousDate</td>
                        <td class="type">object</td>
                        <td class="description">Returns the previous date of the Schedule.</td>
                    </tr>
                    <tr>
                        <td class="name">argument.target</td>
                        <td class="type">object</td>
                        <td class="description">Returns the target of the action.</td>
                    </tr>
                    <tr>
                        <td class="name">argument.type</td>
                        <td class="type">string</td>
                        <td class="description">Returns the name of the event.</td> 
                    </tr>
                </tbody>
            </table>
            </td>
        </tr>
    </tbody>
</table>


#### Example

{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
   navigation: function (args) {}
});
</script>

{% endhighlight %}


### reminder
{:#events:reminder}

Triggers when the reminder is raised for an appointment.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">argument.cancel</td>
            <td class="type">boolean</td>
            <td class="description">Returns the cancel option value.</td>
        </tr>
        <tr>
            <td class="name">argument.model</td>
            <td class="type">object</td>
            <td class="description">Returns the Schedule model.</td>
        </tr>
        <tr>
            <td class="name">argument.type</td>
            <td class="type">string</td>
            <td class="description">Returns the name of the event.</td>
        </tr>
        <tr>
            <td class="name">argument.reminderAppointment</td>
            <td class="type">object</td>
            <td class="description">Returns the appointment object for which the reminder is raised.</td>
        </tr>
    </tbody>
</table>




#### Example

{% highlight html %}

<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
   reminder: function (args) {}
});
</script>

{% endhighlight %}

### resize
{:#events:resize}

Triggers while resizing the appointment.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">argument.object</td>
            <td class="type">object</td>
            <td class="description">Returns the object of resizing event.</td>
        </tr>
        <tr>
            <td class="name">argument.cancel</td>
            <td class="type">boolean</td>
            <td class="description">Returns the cancel option value.</td>
        </tr>
        <tr>
            <td class="name">argument.element</td>
            <td class="type">object</td>
            <td class="description">Returns the resize element value.</td>
        </tr>
        <tr>
            <td class="name">argument.model</td>
            <td class="type">object</td>
            <td class="description">Returns the Schedule model.</td>
        </tr>
        <tr>
            <td class="name">argument.type</td>
            <td class="type">string</td>
            <td class="description">Returns the name of the event.</td>
        </tr>
    </tbody>
</table>




#### Example

{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { 
        dataSource: [{
                        Id: 102,
                        Subject: "Play With Friends",
                        StartTime: new Date(2014, 4, 6, 10, 00),
                        EndTime: new Date(2014, 4, 6, 12, 00),
                        AllDay:false,
                        Recurrence:false,
                        RecurrenceRule:null,
                        StartTimeZone: "UTC +00:00",
                        EndTimeZone: "UTC +00:00
                    }]
                    id: "Id",
                    startTime: "StartTime",
                    endTime: "EndTime",
                    subject: "Subject",
                    allday:"AllDay",
                    recurrence:"Recurrence",
                    recurrenceRule:"RecurrenceRule",
                    startTimeZone: "StartTimeZone",
                    endTimeZone: "EndTimeZone"
        },
   resize: function (args) {}
});
</script>

{% endhighlight %}

### resizeStart
{:#events:resizestart}

Triggers when the appointment resizing begins.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">argument.object</td>
            <td class="type">object</td>
            <td class="description">Returns the object of resizeStart event.</td>
        </tr>
        <tr>
            <td class="name">argument.cancel</td>
            <td class="type">boolean</td>
            <td class="description">Returns the cancel option value.</td>
        </tr>
        <tr>
            <td class="name">argument.element</td>
            <td class="type">object</td>
            <td class="description">Returns the resize element value.</td>
        </tr>
        <tr>
            <td class="name">argument.model</td>
            <td class="type">object</td>
            <td class="description">Returns the Schedule model.</td>
        </tr>
        <tr>
            <td class="name">argument.type</td>
            <td class="type">string</td>
            <td class="description">Returns the name of the event.</td>
        </tr>
    </tbody>
</table>




#### Example

{% highlight html %}
 
<div id="Schedule"></div> 
 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { 
        dataSource: [{
                        Id: 101,
                        Subject: "Talk with Lecturers",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 12, 00),
                        AllDay:false,
                        Recurrence:false,
                        RecurrenceRule:null,
                        StartTimeZone: "UTC +00:00",
                        EndTimeZone: "UTC +00:00
                    }]
                    id: "Id",
                    startTime: "StartTime",
                    endTime: "EndTime",
                    subject: "Subject",
                    allday:"AllDay",
                    recurrence:"Recurrence",
                    recurrenceRule:"RecurrenceRule",
                    startTimeZone: "StartTimeZone",
                    endTimeZone: "EndTimeZone"
        },
        resizeStart: function (args) {}
});
</script>

{% endhighlight %}

### resizeStop
{:#events:resizestop}

Triggers when appointment resizing stops.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">argument.object</td>
            <td class="type">object</td>
            <td class="description">Returns the object of resizeStop event.</td>
        </tr>
        <tr>
            <td class="name">argument.appointment</td>
            <td class="type">object</td>
            <td class="description">Returns the resized appointment value.</td>
        </tr>
        <tr>
            <td class="name">argument.cancel</td>
            <td class="type">boolean</td>
            <td class="description">Returns the cancel option value.</td>
        </tr>
        <tr>
            <td class="name">argument.model</td>
            <td class="type">object</td>
            <td class="description">Returns the Schedule model.</td>
        </tr>
        <tr>
            <td class="name">argument.target</td>
            <td class="type">object</td>
            <td class="description">Returns the target of the resized appointment.</td>
        </tr>
        <tr>
            <td class="name">argument.type</td>
            <td class="type">string</td>
            <td class="description">Returns the name of the event.</td>
        </tr>
    </tbody>
</table>




#### Example

{% highlight html %}
 
<div id="Schedule"></div> 
<script>
$("#Schedule").ejSchedule({
    appointmentSettings: { 
        dataSource: [{
                        Id: 101,
                        Subject: "Helping to Dad",
                        StartTime: new Date(2014, 4, 5, 10, 00),
                        EndTime: new Date(2014, 4, 5, 12, 00),
                        AllDay:false,
                        Recurrence:false,
                        RecurrenceRule:null,
                        StartTimeZone: "UTC +00:00",
                        EndTimeZone: "UTC +00:00
                    }]
                    id: "Id",
                    startTime: "StartTime",
                    endTime: "EndTime",
                    subject: "Subject",
                    allday:"AllDay",
                    recurrence:"Recurrence",
                    recurrenceRule:"RecurrenceRule",
                    startTimeZone: "StartTimeZone",
                    endTimeZone: "EndTimeZone"
        },
        resizeStop: function (args) {}
});
</script>

{% endhighlight %}
