---
title: Schedule - Views
description: View options available in Scheduler
platform: js
control: schedule
documentation: ug
keywords: day, week, workweek, month, timeline, horizontal, custom
api: /api/js/ejschedule  
---
# Views

The number of days and its associated appointments are usually grouped together in Scheduler to organize different views. The available view options in Scheduler are as follows,

* Day
* Week
* Workweek
* Month
* Custom View
* Agenda
* Timeline View

Usually these view options are displayed as a toolbar in the date-header section of the Schedule control. The items within the views toolbar can be added/removed based on the value passed to the [views](/api/js/ejschedule#members:views) property. 

By default, the Schedule control’s active view is **Week** view. Also, it is possible to change the active view of the Scheduler by setting [currentView](/api/js/ejschedule#members:currentview) option with the required view name as depicted below.

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="schedule"></div>

<script>
$(function() {
    $("#schedule").ejSchedule({
        //Required views display the control
        views: ["Day", "WorkWeek"],
        // Set the Active view
        currentView: ej.Schedule.CurrentView.Workweek
    });
})	
</script>

{% endhighlight %}

N> The **currentView** property accepts both the `string` and `ej.Schedule.CurrentView` enum value.

## Day 

It represents a single day Scheduler view (single date display) with all its related appointments.

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="schedule"></div>

<script>
$(function() {
    $("#schedule").ejSchedule({
        // Set the Active view
        currentView: ej.Schedule.CurrentView.Day,
        currentDate: new Date(2015, 11, 7),
        appointmentSettings: {
            //Array of JSON data configure in dataSource
            dataSource: [{
                Id: 1,
                Subject: "Music Class",
                StartTime: new Date("2015/11/7 06:00 AM"),
                EndTime: new Date("2015/11/7 07:00 AM")
            }, {
                Id: 2,
                Subject: "School",
                StartTime: new Date("2015/11/7 9:00 AM"),
                EndTime: new Date("2015/11/7 02:30 PM")
            }]
        }
    });
});	
</script>

{% endhighlight %}

## Week

It’s a view displaying a count of 7 days (from Sunday to Saturday) with all its related appointments. The first day of the week can be changed using the [firstDayOfWeek](/api/js/ejschedule#members:firstdayofweek) API which accepts either the `integer` (Sunday=0, Monday=1, Tuesday=2, etc) or `string` (“Sunday”, “Monday”, etc) or `ej.Schedule.DayOfWeek` enum type value. The default value of this **firstDayOfWeek** depends on the current culture (language) used in the Scheduler.

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="schedule"></div>

<script>
$(function() {
    $("#schedule").ejSchedule({
        // Set the Active view
        currentView: ej.Schedule.CurrentView.Week,
        // Configure the week start day(First day of week)
        firstDayOfWeek: ej.Schedule.FirstDayOfWeek.Monday,
        currentDate: new Date(2015, 11, 7),
        appointmentSettings: {
            //Array of JSON data configure in dataSource
            dataSource: [{
                Id: 1,
                Subject: "Music Class",
                StartTime: new Date("2015/11/7 06:00 AM"),
                EndTime: new Date("2015/11/7 07:00 AM")
            }, {
                Id: 2,
                Subject: "School",
                StartTime: new Date("2015/11/7 9:00 AM"),
                EndTime: new Date("2015/11/7 02:30 PM")
            }]
        }
    });
});	
</script>

{% endhighlight %}

## Work Week 

Work week view displays the working days of the week (count of 5 days) and its associated appointments. It is also possible to customize the days to be displayed in the work week view using [workWeek](/api/js/ejschedule#members:workweek) API which accepts the string array such as ["Monday", "Tuesday", "Wednesday", "Thursday" and "Friday"]. By default, it renders from Monday to Friday (5 days).

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="schedule"></div>

<script>
$(function() {
    $("#schedule").ejSchedule({
        // Set the Active view
        currentView: ej.Schedule.CurrentView.Workweek,
        // configure the work week days
        workWeek: ["Monday", "Tuesday", "Thursday", "Friday", "Saturday"],
        currentDate: new Date(2015, 11, 7),
        appointmentSettings: {
            //Array of JSON data configure in dataSource
            dataSource: [{
                Id: 1,
                Subject: "Music Class",
                StartTime: new Date("2015/11/7 06:00 AM"),
                EndTime: new Date("2015/11/7 07:00 AM")
            }, {
                Id: 2,
                Subject: "School",
                StartTime: new Date("2015/11/7 9:00 AM"),
                EndTime: new Date("2015/11/7 02:30 PM")
            }]
        }
    });
});	
</script>

{% endhighlight %}

## Month

Month view displays the entire days of a particular month and all its related appointments. An alternative way to navigate to a particular date in a day view directly from Month view, clicking on the appropriate month cell date header will do so. If the week date range column is clicked, it will navigate to the corresponding week view.

The next and previous month date cells in the Month view can be shown/hidden on the Scheduler using [showNextPrevMonth](/api/js/ejschedule#members:shownextprevmonth) property by setting it to *false*.

For example – To set the Month view as current view in Scheduler and to hide the other month days in it, refer the below code example.

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="schedule"></div>

<script>
$(function() {
    $("#schedule").ejSchedule({
        // Set the Active view as Month
        currentView: ej.Schedule.CurrentView.Month,
        showNextPrevMonth: false,
        currentDate: new Date(2015, 11, 7),
        appointmentSettings: {
            //Array of JSON data configure in dataSource
            dataSource: [{
                Id: 1,
                Subject: "Music Class",
                StartTime: new Date("2015/11/7 06:00 AM"),
                EndTime: new Date("2015/11/7 07:00 AM")
            }, {
                Id: 2,
                Subject: "School",
                StartTime: new Date("2015/11/7 9:00 AM"),
                EndTime: new Date("2015/11/7 02:30 PM")
            }]
        }
    });
});	
</script>

{% endhighlight %}

N> An appointment directly created in Month view will be considered as an all-day appointment.

## Custom

### Customizing Number of Days

The Scheduler can be displayed with the user-specified date ranges, such as 4 days or any specific date ranges instead of default view options, by making use of the [renderDates](/api/js/ejschedule#members:renderdates) property. This property includes two sub properties namely **start** and **end**, which accepts the date object or date value in string format to specify the date range. 

To display the custom view option in the toolbar-like view options in the scheduler header area, add the `CustomView` value to the views property array collection as shown below. 

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="schedule"></div>

<script>
$(function() {
    $("#schedule").ejSchedule({
        // We can add the "CustomView" in views collection
        views: ["Day", "Week", "WorkWeek", "Month", "CustomView"],
        currentDate: new Date(2015, 11, 6),
        // Configure the custom date
        renderDates: {
            // Render start date 
            start: new Date(2015, 11, 6),
            // Render end date 
            end: new Date(2015, 11, 9)
        },
        // Set the Active view
        currentView: ej.Schedule.CurrentView.CustomView,
        appointmentSettings: {
            //Array of JSON data configure in dataSource
            dataSource: [{
                Id: 1,
                Subject: "Music Class",
                StartTime: new Date("2015/11/7 06:00 AM"),
                EndTime: new Date("2015/11/7 07:00 AM")
            }, {
                Id: 2,
                Subject: "School",
                StartTime: new Date("2015/11/7 9:00 AM"),
                EndTime: new Date("2015/11/7 02:30 PM")
            }]
        }
    });
});	
</script>

{% endhighlight %}

When the date difference between the provided start and end date is greater than 7, then the month-like view will get displayed in Vertical Scheduler mode - whereas with the date difference less than 7 days displays the Scheduler with exact count of the specified days.

N> When the `currentDate` property of Scheduler is set with a date, that lies beyond the specified custom date range - then the Scheduler navigates to the current date with the mentioned date differences.  

## Customizing Number of Dates

The Scheduler can be displayed with the user-provided custom dates, such as 4 dates or any specific collection of dates, by making use of the [renderDates](/api/js/ejschedule#members:renderdates) property.This property accepts both the object and array values. You need to pass the array (array of strings/array of date/array of objects) value to utilize this feature. To render the custom dates based Scheduler, need to set the "customView" as the Scheduler active view.

The following code example renders the Scheduler with the user-provided custom dates.

a. Passing array of string values

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="Schedule1"></div>

<script type="text/javascript">
$(function() {
    $("#Schedule1").ejSchedule({
        width: "100%",
        renderDates: [
            "5/2/2017", "5/4/2017", "5/6/2017", "5/9/2017", "5/10/2017",
            "5/11/2017", "5/28/2017", "5/30/2017", "6/3/2017", "6/5/2017"
        ],
        views: ["CustomView"],
        currentView: ej.Schedule.CurrentView.CustomView,
        appointmentSettings: {
            dataSource: [{
                Id: 101,
                Subject: "Talk with Nature",
                StartTime: new Date(2017, 11, 5, 10, 00),
                EndTime: new Date(2017, 11, 5, 11, 00)
            }]
        }
    });
});
</script>

{% endhighlight %}

b. Passing array of date values

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="Schedule1"></div>

<script type="text/javascript">
$(function() {
    $("#Schedule1").ejSchedule({
        width: "100%",
        renderDates: [                        
            new Date(2017,5,2), new Date(2017,5,4), new Date(2017,5,6), new Date(2017,5,8), 
            new Date(2017,5,10), new Date(2017,5,12), new Date(2017,5,14), new Date(2017,5,16), 
            new Date(2017,5,20), new Date(2017,5,22), new Date(2017,5,24), new Date(2017,5,28)
        ],
        views: ["CustomView"],
        currentView: ej.Schedule.CurrentView.CustomView,
        appointmentSettings: {
            dataSource: [{
                Id: 101,
                Subject: "Talk with Nature",
                StartTime: new Date(2017, 11, 5, 10, 00),
                EndTime: new Date(2017, 11, 5, 11, 00)
            }]
        }
    });
});
</script>

{% endhighlight %}

c. Passing array of object values

You can use sub properties namely **start** and **end** while passing array of object values, which accepts the date object or date value in string format to specify the custom date range.

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="Schedule1"></div>

<script type="text/javascript">
$(function() {
    $("#Schedule1").ejSchedule({
        width: "100%",
        renderDates: [                        
            { start: new Date(2015, 1, 6), end: new Date(2015, 1, 10) },
            { start: new Date(2016, 6, 11), end: new Date(2016, 6, 20) },
            { start: new Date(2017, 10, 26), end: new Date(2017, 10, 30) }
        ],
        views: ["CustomView"],
        currentView: ej.Schedule.CurrentView.CustomView,
        appointmentSettings: {
            dataSource: [{
                Id: 101,
                Subject: "Talk with Nature",
                StartTime: new Date(2017, 11, 5, 10, 00),
                EndTime: new Date(2017, 11, 5, 11, 00)
            }]
        }
    });
});
</script>

{% endhighlight %}

N> When the passed custom dates length is greater than 7, then the month-like view will get displayed in Horizontal Scheduler mode - whereas with the dates length less than 7 days displays the Scheduler with its specified orientation.

The following restrictions will be applied while using this feature.

* firstDayOfWeek, currentDate, minDate, maxDate and showAppointmentNavigator property values does not reflect in Scheduler.

## Agenda

This View option lists out the appointments in a grid-like view for the next 7 days by default from the current date. The count of the number of appointments to be listed in this view can be customized using the [agendaViewSettings.daysInAgenda](/api/js/ejschedule#members:agendaviewsettings-daysinagenda).

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="schedule"></div>

<script>
$(function() {
    $("#schedule").ejSchedule({
        // Set the Active view
        currentView: ej.Schedule.CurrentView.Agenda,
        currentDate: new Date(2015, 11, 7),
        //configure the agenda view 
        agendaViewSettings: {
            //Next 5 days Appointments lists out from current date
            daysInAgenda: 5
        },
        appointmentSettings: {
            //Array of JSON data configure in dataSource
            dataSource: [{
                Id: 1,
                Subject: "Music Class",
                StartTime: new Date("2015/11/7 06:00 AM"),
                EndTime: new Date("2015/11/7 07:00 AM")
            }, {
                Id: 2,
                Subject: "School",
                StartTime: new Date("2015/11/7 9:00 AM"),
                EndTime: new Date("2015/11/7 02:30 PM")
            }]
        }
    });
});	
</script>

{% endhighlight %}

N> In Agenda view, the templates can be applied for the date and time columns which can be referred [here](/api/js/ejschedule#members:agendaviewsettings). Also, the template passed through the [appointmentTemplateID](/api/js/ejschedule#members:appointmenttemplateid) will gets applied to the event column in Agenda view.

## Restriction on View Navigation

It is possible to restrict the users to display only the specific list of views in the Schedule header section and also not to navigate to other views that are not listed. 

**For example**, if the views property is set only with `Month` view – then the Schedule header section displays only the Month option in the view toolbar and also other additional available actions like navigating to day/week view on clicking the month header dates and week date-range is stopped.

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="schedule"></div>

<script>
$(function() {
    $("#schedule").ejSchedule({
        // Add only the "Month" in views collection
        views: ["Month"],
        currentDate: new Date(2015, 11, 7),
        appointmentSettings: {
            //Array of JSON data configure in dataSource
            dataSource: [{
                Id: 1,
                Subject: "Music Class",
                StartTime: new Date("2015/11/7 06:00 AM"),
                EndTime: new Date("2015/11/7 07:00 AM")
            }, {
                Id: 2,
                Subject: "School",
                StartTime: new Date("2015/11/7 9:00 AM"),
                EndTime: new Date("2015/11/7 02:30 PM")
            }]
        }
    });
});	
</script>

{% endhighlight %}

N> Even though Week view is the active view in Scheduler by default, if it is not listed in the views collection – then the first listed option in the views collection will be taken as current view of the Scheduler.

## Timeline View

Timeline view displays the day, time and its associated events horizontally arranged from left to right. By default, Scheduler renders in vertical mode and it can be changed to the timeline mode using [orientation](/api/js/ejschedule#members:orientation) property which accepts both the `string` and `ej.Schedule.Orientation` enum value.

All the applicable features in Vertical mode works similar with Timeline mode (Horizontal) and only the visualization of the layout changes based on the orientation.

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="schedule"></div>

<script>
$(function() {
    $("#schedule").ejSchedule({
        currentDate: new Date(2015, 11, 7),
        //set the timeline (horizontal) view
        orientation: ej.Schedule.Orientation.Horizontal,
        appointmentSettings: {
            //Array of JSON data configure in dataSource
            dataSource: [{
                Id: 1,
                Subject: "Music Class",
                StartTime: new Date("2015/11/7 09:00 AM"),
                EndTime: new Date("2015/11/7 10:00 AM")
            }, {
                Id: 2,
                Subject: "School",
                StartTime: new Date("2015/11/7 02:00 PM"),
                EndTime: new Date("2015/11/7 06:30 PM")
            }]
        }
    });
});	
</script>

{% endhighlight %}
