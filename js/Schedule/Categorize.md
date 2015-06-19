---
layout: post
title: Categorize
description: categorize	
platform: js
control: Schedule
documentation: ug
---

# Categorize	

* This feature allows you to differentiate the appointments with various categorize options and individual colors. You can also denote the status of the appointments using this categorize option and can specify your own user-defined category collection.

You can use the following code example to include the categorize option.

{% highlight html %}

<div id="Schedule1"></div>

{% endhighlight %}

{% highlight js %}

$(function () {
        $("#Schedule1").ejSchedule({
            categorizeSettings: {
                enable: true,
                allowMultiple: true,
                dataSource: [
                { text: "Blue Category", id: 1, color: "#7499e1", fontColor: "red" },
                { text: "Green Category", id: 2, color: "#7cce6e", fontColor: "white" },
                { text: "Orange Category", id: 3, color: "#ffaa00", fontColor: "green" }
                ],
                text: "text", id: "id", color: "color", fontColor: "fontColor"
            },
        });
    });

{% endhighlight %}


**Categorize Settings**

* The **categorizeSettings** is an object collection that holds the categorize related information such as the dataSource. It provides the collection of categorize values that are to be used in appointments, allowMultiple that enables/disables the multiple selection of categorize values and other mapper field names to bind the fields of the dataSource. 

The following are the sub-properties used within the categorizeSettings.

**enable**

* This option accepts either true or false, denoting whether to enable/disable the categorize option.

**allowMultiple**

* This property enables or disables the multiple selection of categories in the appointment window. 

**dataSource**

* It either accepts the local JSON data or remote data for binding the category related information. 

**text**

* It holds****the binding name for text field in the categorize dataSource.

**id**

* It holds the binding name for id field in the categorize dataSource.

**color**

* It holds the binding name for color field in the categorize dataSource.

**fontColor**

* It holds the binding name for fontcolor field in the categorize dataSource.

The following code example illustrates on how to render categorize feature in the **Schedule** control.


{% highlight html %}

<div id="Schedule1"></div>

{% endhighlight %}

{% highlight js %}
  $(function () {
        var dManager = ej.DataManager(window.Default).executeLocal(ej.Query().take(2));
        $("#Schedule1").ejSchedule({
            // categorize data collection
            categorizeSettings: {
                enable: true,
                dataSource: [
                { text: "Blue Category", id: 1, color: "#7499e1", fontColor: "red" },
                { text: "Green Category", id: 2, color: "#7cce6e", fontColor: "white" },
                { text: "Orange Category", id: 3, color: "#ffaa00", fontColor: "green" }
                ],
                text: "text", id: "id", color: "color", fontColor: "fontColor"
            },
            appointmentSettings: {
                dataSource: dManager,
                id: "Id",
                subject: "Subject",
                startTime: "StartTime",
                endTime: "EndTime",
                allDay: "AllDay",
                recurrence: "Recurrence",
                recurrenceRule: "RecurrenceRule",
                // bind the resource id fields collection of each level
                categorize: "Categorize"
            }
        });
    });
    // The appointment data along with categorize data to be passed to the dataSource are as follows,
    window.Default = [{
        Id: 100,
        Subject: "Bering Sea Gold",
        StartTime: new Date(new Date().setMinutes(new Date().getMinutes() + 6)),
        EndTime: new Date(new Date().setHours(new Date().getHours() + 2)),
        AllDay: false,
        Recurrence: true,
        RecurrenceRule: "FREQ=DAILY;INTERVAL=2;COUNT=10",
        // single value for the categorize
        Categorize: "3"
    }, {
        Id: 101,
        Subject: "Bering Sea Gold",
        StartTime: new Date().setHours(4, 0),
        EndTime: new Date().setHours(5, 0),
        AllDay: false,
        Recurrence: false,
        // two values to separate using the comma separate.
        Categorize: "1,3"
    }
    ];



{% endhighlight %}



The output of the above code is illustrated as follows.

{% include image.html url="/js/Schedule/Categorize_images/Categorize_img1.png" Caption="Schedule for the categorize option."%}
