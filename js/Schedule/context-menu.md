---
title: Schedule - Context Menu	
description: How to display context menu on appointment and cell with customization
platform: js
control: schedule
documentation: ug
keywords: context-menu
---
## Context Menu

Scheduler provides default context menu options for both appointments as well as work cells. It also allows to define additional custom context menu options.

The options that are available under **[contextMenuSettings](http://help.syncfusion.com/js/api/ejschedule#members:contextmenusettings "")** are as follows,

* **enable** - Enables/disables the context menu option in Scheduler.
* **menuItems** - Contains the sub-menu collections related to both the appointment and cells.

### Default Menu Options


The menu items contains two separate collection based on the appointment and cells. 

**Appointment**

The appointment collection includes the following options. 

<table>
<tr>
<td>
Open Appointment (default)<br/><br/></td></tr>
<tr>
<td>
Delete Appointment (default)<br/><br/></td></tr>
<tr>
<td>
Print Appointment<br/><br/></td></tr>
<tr>
<td>
Categorize<br/><br/></td></tr>
</table>
**Cells**

The default options available within the cell collection includes - 

<table>
<tr>
<td>
New Appointment<br/><br/></td></tr>
<tr>
<td>
New Recurring Appointment<br/><br/></td></tr>
<tr>
<td>
Today<br/><br/></td></tr>
<tr>
<td>
Go to date<br/><br/></td></tr>
<tr>
<td>
Settings<br/><br/>**View**<br/><br/>Day<br/><br/>Week<br/><br/>Work Week<br/><br/>Month<br/><br/>Agenda<br/><br/>**TimeMode**<br/><br/>12 Hours<br/><br/>24 Hours<br/><br/>**Work Hours**<br/><br/></td></tr>
</table>
The following code snippet shows how to enable the context menu settings in Scheduler and to make use of it with default available options. 

{% highlight html %}


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

Id: 100,

Subject: "Research on Sky Miracles",

StartTime: new Date(2015, 11, 2, 9, 00),

EndTime: new Date(2015, 11, 2, 10, 30)

}]

}

});

});

</script>



{% endhighlight %}

**Note**:

* In agenda view, only the appointment menu items shows up in the context menu options.

* For default menu items, the id must be defined the same as mentioned in the above code example – as we processed the menus based on this id within our source.
### Custom Menu Options


Apart from the default available options, it is also possible to add custom menu options to the context-menu in both the appointment and cell collection.

The following code example depicts how **to add the custom menu items** to the appointment and cells collection of the context menu settings.

{% highlight html %}


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

{ id: "delete", text: "Delete Appointment" }

{ id: "option1", text: "User Option 1" }],

cells: [

{ id: "celloption1", text: "Custom Option 1" }]

}

},

appointmentSettings: {

dataSource: [{

Id: 100,

Subject: "Research on Sky Miracles",

StartTime: new Date(2015, 11, 2, 9, 00),

EndTime: new Date(2015, 11, 2, 10, 30)

}]

}

});

});

</script>



{% endhighlight %}

**Note**: The **id’s** given for the custom menu items **must be unique** in both the appointment and cells collection. 

### Handling Menu Actions

To define specific actions for a click made on the custom menu items, the client-side event **[menuItemClick](http://help.syncfusion.com/js/api/ejschedule#events:menuitemclick "")** can be used as depicted in the below code example.

{% highlight html %}


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

{ id: "option1", text: "User Option 1" }]

}

},

appointmentSettings: {

dataSource: [{

Id: 100,

Subject: "Research on Sky Miracles",

StartTime: new Date(2015, 11, 2, 9, 00),

EndTime: new Date(2015, 11, 2, 10, 30)

}]

},

menuItemClick: function (args) {

//args.events contains information of the clicked menu item.

if (args.events.ID == "option1")

alert("Custom menu clicked");

}

});

});

</script>



{% endhighlight %}



Also, it is possible to predict the target on which the right click is made either on the cells or appointments with the use of the event **[beforeContextMenuOpen](http://help.syncfusion.com/js/api/ejschedule#events:beforecontextmenuopen "")**. The below code example shows how to block the display of context menu when right clicked on the cells by setting **args.cancel** as **true**.

{% highlight html %}


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

{ id: "option1", text: "User Option 1" }]

}

},

appointmentSettings: {

dataSource: [{

Id: 100,

Subject: "Research on Sky Miracles",

StartTime: new Date(2015, 11, 2, 9, 00),

EndTime: new Date(2015, 11, 2, 10, 30)

}]

},

beforeContextMenuOpen: function (args) {

//args.target –target information to depict either cell/appointment

if ($(args.target.target).hasClass("e-workcells,e-monthcells"))

args.cancel = true;

}

});

});

</script>



{% endhighlight %}

### Adding Categorize Option

To include the default categorize options within the context menu, it is necessary to enable the **[categorizeSettings](http://help.syncfusion.com/js/api/ejschedule#members:categorizesettings "")** property as shown in the below code example.

{% highlight html %}


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

{ id: "categorize", text: "Categorize" }],

}

},

categorizeSettings: { enable: true },

appointmentSettings: {

dataSource: [{

Id: 100,

Subject: "Research on Sky Miracles",

StartTime: new Date(2015, 11, 2, 9, 00),

EndTime: new Date(2015, 11, 2, 10, 30)

}]

}

});

});

</script>



{% endhighlight %}

**Note**: The **categorize** option must be added only to the **appointment** collection, which displays on right clicking over the appointments.

