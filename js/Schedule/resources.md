---
title: Schedule - Resource handling with multiple option
description: Handling multiple resources in Scheduler
platform: js
control: schedule
documentation: ug
keywords: resource, resources, multiple resources, grouping 
---
# Resources

The Scheduler provides **Resources** support, with which the single Scheduler is shared by multiple resources simultaneously. Each resource in the Scheduler is arranged in a column/row wise with individual spacing to display all its respective appointments on a single page. It also supports the grouping of resources, thus enabling the categorization of resources in a hierarchical structure and shows it either in expandable groups (**Horizontal** **view**) or else vertical hierarchy one after the other (**Vertical** **view**).

One or more resources can be assigned to the Scheduler appointments by making selection of the resource options available in the appointment window.

## Fields of Resources

The default options available within the [resources](/js/api/ejschedule#members:resources) collection are as follows,

### name (**String**)

A unique resource name which is used for differentiating various resource objects while grouping it in various levels.

### title (**String**)

It holds the title name of the resource field to be displayed on the Scheduler appointment window.

### field (**String**)

It holds the name of the resource field to be bound to the Scheduler appointments which contains the resource Id.

### allowMultiple (**Boolean**)

When set to true, allows multiple selection of resource names, thus creating multiple instances of same appointment for the selected resources.

### resourceSettings (**Object**)

It holds the field names of the resources to be bound to the Scheduler and also includes the dataSource.

The following are the resource fields which must be defined within the **resourceSettings** that holds the appropriate column names from the dataSource.

<table>
<tr>
<th>
Field name<br/><br/></th><th>
Description<br/><br/></th></tr>
<tr>
<td>
text<br/><br/></td><td>
Binds the text field name in the dataSource to the resourceSettings <b>text</b>. These text gets listed out in the resources field of the appointment window. It’s mandatory.<br/><br/><br/><br/></td></tr>
<tr>
<td>
id<br/><br/></td><td>
Binds the id field name in the dataSource to the resourceSettings <b>id</b>. It’s mandatory.<br/><br/><br/><br/></td></tr>
<tr>
<td>
groupId<br/><br/></td><td>
Binds the groupId field name in the dataSource to the resourceSettings <b>groupId</b>. This field is not necessary for a resource object (resource data) defined as first level within the resources collection.<br/><br/><br/><br/></td></tr>
<tr>
<td>
color<br/><br/></td><td>
Binds the color field name in the dataSource to the resourceSettings <b>color</b>. It is optional.<br/><br/><br/><br/></td></tr>
<tr>
<td>
appointmentClass<br/><br/></td><td>
Binds the appointmentClass field name in the dataSource. It applies the custom css class name to the appointments based on the resources.<br/><br/><br/><br/></td></tr>
</table>

**Example**: To set the resources options using all the above specified fields,

{% highlight html %}


<div id="Schedule1"></div>

<script type="text/javascript">

$(function () {

$("#Schedule1").ejSchedule({

width: "100%",

currentDate: new Date(2015, 04, 05),

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

// groupId maps the current resources to the previous level of resource object (current groupId maps with previous level id field)

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

StartTime: new Date(2015, 04, 05, 9, 00),

EndTime: new Date(2015, 04, 05, 10, 30),

ownerId: 2,

roomId: 3 

}],

resourceFields: "ownerId,roomId"

}

});

});

</script>





{% endhighlight %}

**Note**: The resource object defined at **first level** within the **resources** collection doesn’t make use of the **groupId** field, as there is no previous levels applicable to map.

## Data Binding

The resource data can be bound to the Schedule control through the **resourceSettings** options available within the **resources** property. The data-binding can be done either using JSON object collection or DataManager ([ej.DataManager](/js/datamanager/overview)) instance which contains the resources related data.

### JSON Data

**Example**: To set the resource data with array of **JSON** object collection

{% highlight html %}


<div id="Schedule1"></div>

<script type="text/javascript">

$(function () {

$("#Schedule1").ejSchedule({

width: "100%",

currentDate: new Date(2015, 04, 05),

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

StartTime: new Date(2015, 04, 05, 9, 00),

EndTime: new Date(2015, 04, 05, 10, 30),

ownerId: 2

},

{

Id: 101,

Subject: "Research on Clouds",

StartTime: new Date(2015, 04, 07, 7, 00),

EndTime: new Date(2015, 04, 07, 10, 30),

ownerId: 1

}],

resourceFields: "ownerId"

}

});

});

</script>





{% endhighlight %}

### Remote Data

**Example**: To set the resource data through the instance of **ejDataManager**

{% highlight html %}


<div id="Schedule1"></div>

<script type="text/javascript">

$(function () {

var dataManager = ej.DataManager({

// referring data from remote service (url binding)

url: "http://mvc.syncfusion.com/OdataServices/Northwnd.svc"

});

// query to fetch the records from the specified table “Events”

var queryResource = ej.Query().select("CategoryID","CategoryName").from("Categories").take(3);

$("#Schedule1").ejSchedule({

width: "60%", height: "550px",

currentDate: new Date(2015, 04, 05),

resources: [{

field: "ownerId", title: "Owner",

resourceSettings: {

dataSource: dataManager,

text: "CategoryName", id: "CategoryID", query: queryResource

}

}],

appointmentSettings: {

dataSource: [{

Id: 100,

Subject: "Research on Sky Miracles",

StartTime: new Date(2015, 04, 05, 9, 00),

EndTime: new Date(2015, 04, 05, 10, 30),

ownerId: 2

},

{

Id: 101,

Subject: "Research on Clouds",

StartTime: new Date(2015, 04, 07, 7, 00),

EndTime: new Date(2015, 04, 07, 10, 30),

ownerId: 1

}],

resourceFields: "ownerId"

}

});

});

</script>





{% endhighlight %}

## Multiple Resources (Without Grouping)

It is possible to display the Scheduler in default look without showcasing all the resources on it, but it allow the user to assign the required resources to the appointments through the appointment window resource options.

The appointments belonging to all the resources will be displayed on the Scheduler which will be differentiated based on the resource color assigned in the **resourceSettings** (depicting to which resource that particular appointment belongs). 

**Example**: To display default Scheduler with multiple resource options in the appointment window,

{% highlight html %}


<div id="Schedule1"></div>

<script type="text/javascript">

$(function () {

$("#Schedule1").ejSchedule({

width: "100%",

currentDate: new Date(2015, 04, 05),

resources: [{

field: "ownerId", title: "Owner", allowMultiple: true,

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

StartTime: new Date(2015, 04, 05, 9, 00),

EndTime: new Date(2015, 04, 05, 10, 30),

ownerId: 2

},

{

Id: 101,

Subject: "Research on Clouds",

StartTime: new Date(2015, 04, 07, 6, 00),

EndTime: new Date(2015, 04, 07, 9, 30),

ownerId: 1

}],

resourceFields: "ownerId"

}

});

});

</script>





{% endhighlight %}

**Note**: Setting **allowMultiple** to **true** in the above code snippet allows the user to select multiple resources in the appointment window and also creates multiple copies of the same appointment in the Scheduler for each resources while saving.

## Grouping

Scheduler supports both single and multiple levels of resource grouping that can be customized in both horizontal and vertical Scheduler views. In Vertical view - the levels are displayed in a tree structure one after the other, but in horizontal view – the levels are grouped in a vertically expandable/collapsible structure.

### Single-Level

This type of grouping allows the Scheduler to display all the resources at a single level simultaneously. The appointments will make use of the **color** defined for the first resource instance as its background color. 

**Example**: To display the Scheduler with single level resource grouping options,

{% highlight html %}


<div id="Schedule1"></div>

<script type="text/javascript">

$(function () {

$("#Schedule1").ejSchedule({

width: "100%",

currentDate: new Date(2015, 04, 05),

group: {

resources: [ "Owners" ]

},

resources: [{

field: "ownerId", title: "Owner", name: "Owners",

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

StartTime: new Date(2015, 04, 05, 9, 00),

EndTime: new Date(2015, 04, 05, 10, 30),

ownerId: 2

},

{

Id: 101,

Subject: "Discovery of exo-planets",

StartTime: new Date(2015, 04, 07, 6, 00),

EndTime: new Date(2015, 04, 07, 9, 30),

ownerId: 1

}],

resourceFields: "ownerId"

}

});

});

</script>





{% endhighlight %}

**Note**: The **name** field mentioned in the **resource** object needs to be specified within the **group** property in order to enable the grouping option in Scheduler.

### Multi-Level

This type of grouping displays the resources in the Scheduler at multiple levels with a set of resources grouped under each parent level. The appointments will make use of the **color** defined for the first/top level resource instance as its background color. 

**Example**: To display the Scheduler with multiple level resource grouping options,

{% highlight html %}


<div id="Schedule1"></div>

<script type="text/javascript">

$(function () {

$("#Schedule1").ejSchedule({

width: "100%",

currentDate: new Date(2015, 04, 05),

group: {

resources: [ "Owners", "Rooms" ]

},

resources: [{

field: "ownerId", title: "Owner", name: "Owners",

resourceSettings: {

dataSource: [

{ OwnerText: "Nancy", id: 1, OwnerColor: "#f8a398" },

{ OwnerText: "Steven", id: 2, OwnerColor: "#56ca95"}],

text: "OwnerText", id: "id", color: "OwnerColor"

}

},

{

field: "roomId", title: "Room(s)", name: "Rooms",

resourceSettings: {

dataSource: [

// groupId maps the current resources to the previous level of resource object (current groupId maps with previous level id field)

{text: "Room1", id: 1, groupId: 1, color: "#f8a398" },

{ text: "Room2", id: 2, groupId: 2, color: "#56ca85" },

{ text: "Room3", id: 3, groupId: 2, color: "#56ac88"}],

text: "text", id: "id", color: "color", groupId: "groupId"

}

}],

appointmentSettings: {

dataSource: [{

Id: 100,

Subject: "Research on Sky Miracles",

StartTime: new Date(2015, 04, 05, 9, 00),

EndTime: new Date(2015, 04, 05, 10, 30),

ownerId: 2,

roomId: 3

}],

resourceFields: "ownerId,roomId"

}

});

});

</script>





{% endhighlight %}

**Note**: Here, the appointments will make use of the **color** defined for the Owners resource instance as its background color.

