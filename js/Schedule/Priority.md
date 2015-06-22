---
layout: post
title: Priority
description: priority
platform: js
control: Schedule
documentation: ug
---

# Priority

* This feature allows you to prioritize the appointments with various priority options each differentiated with its individual icons/images. 

* You can also denote the priority of the appointments using this priority option and can specify your own user-defined priority collection.

## Priority settings

* The **prioritySettings** is an object collection that holds the priority related information. 

* For example **enable** property enables/disables the priority value to be displayed.





The following are the sub-properties used within the prioritySettings.

**enable**

* This option accepts either true or false, denoting whether to enable/disable the priority option.

**datasource** 

* It either accepts the local JSON data or remote data for binding the priority related information.

**text**

* It holds****the binding name for text field in the priority dataSource.

**id**

* It holds the binding name for id field in the priority dataSource.



**value**

* It holds the binding name for value field in the priority dataSource.

The following code example illustrates on how to render priority feature in the **Schedule** control.



{% highlight html %}

<div id="Schedule1"></div>

{% endhighlight %}

{% highlight js %}

 $(function () {
        var dManager = ej.DataManager(window.Default).executeLocal(ej.Query().take(10));
        $("#Schedule1").ejSchedule({
            width: "100%",
            height: "525px",
            currentDate: new Date(2014, 4, 5),
            prioritySettings: {
            enable: true
          },
            appointmentSettings: {
                dataSource: dManager,
                id: "Id",
                subject: "Subject",
                startTime: "StartTime",
                endTime: "EndTime",
                description:"Description",
                allDay: "AllDay",
                priority:"Priority", // To display the Priority value appointment window need to bind the property like this
                recurrence: "Recurrence",
                recurrenceRule: "RecurrenceRule"
            }
        });
    });
    // The appointment data along with priority data to be passed to the dataSource are as follows,
    window.Default = [{
        Id: 100,
        Subject: "Bering Sea Gold",
        StartTime: new Date(2014,4,2,06,00),
        EndTime:new Date(2014,4,2,08,00),
        Description: "",
        Priority:"low",  // The Priority value passed in the JSON object like this with lower cases
        AllDay: false,
        Recurrence: true,
        RecurrenceRule: "FREQ=DAILY;INTERVAL=2;COUNT=10",
        Categorize:"3"
    },
    {
        Id: 101,
        Subject: "Bering Sea Gold",
        StartTime:new Date(2014,4,5,10,00),
        EndTime: new Date(2014,4,5,11,00),
        Description: "",
        Priority: "high",
        AllDay: false,
        Recurrence: false,
        Categorize: "1,3"
    }
    ];


{% endhighlight %}


On executing the above specified code the Priority field will be added in the create appointment window as follows:

 {% include image.html url="/js/Schedule/Priority_images/Priority_img1.png" Caption="schedule with priority."%}



**template**

* The Priority option can be customized based on the user- defined datasource. 

* You need to mention the “template” value also while passing the user-defined datasource. 



The following code example illustrates on how to render priority feature with user- defined datasource in the **Schedule** control. 



{% highlight html %}

<div id="Schedule1"></div>

{% endhighlight %}

{% highlight js %}

 $(function () {
        var dManager = ej.DataManager(window.Default).executeLocal(ej.Query().take(10));
        $("#Schedule1").ejSchedule({
            width: "100%",
            height: "525px",
            currentDate: new Date(2014, 4, 5),
            prioritySettings: {
                enable: true,
                template: "<div class='${value}'></div>",  // To display the Priority option in the appointment window while passing custom datasource we need to mention the template like this
                dataSource:  // We can pass the custom datasource (priority option) for the schedule control like the following
                [
                { text: "None", id: 1, value: "none" },
                { text: "Critical", id: 2, value: "critical" },
                { text: "UltraCritical", id: 3, value: "ultracritical" }
                ],
            },
            categorizeSettings: { enable: true },
            appointmentSettings: {
                dataSource: dManager,
                id: "Id",
                subject: "Subject",
                startTime: "StartTime",
                endTime: "EndTime",
                description: "Description",
                allDay: "AllDay",
                priority: "Priority",
                recurrence: "Recurrence",
                recurrenceRule: "RecurrenceRule"
            }
        });
    });


{% endhighlight %}



And then need to define the styles to display the "priority icon/images (you can use your desired images)" with the priority options. The class name (while defining styles) should be the field name in template. For example if you define the template (ex: Template ("&lt;div class='${value}'&gt;&lt;/div&gt;")) then you need to define class with **value** field and its value should be a class name (ex: critical). 



The following code example illustrates how to define the css style while using the template.



{% highlight css %}

<!--  Her we are defining the style of the "custom priority icon" -->

    .critical,
    .ultracritical,
    .none {
        height: 16px;
        width: 17px;
        float: left;
        background-repeat: no-repeat;
        padding: 1px;
    }
    .critical {
        background-image: url('../themes/images/arrowup.png');
        background-color: orange;
        background-position: 2px;
    }
    .ultracritical {
        background-image: url('../themes/images/arrowup.png');
        background-color: red;
        background-position: 2px;
    }



{% endhighlight %}


Similarly you can use the image tag directly in the template. Following code snippets illustrates the image tag usage in the template.



{% highlight html %}

<div id="Schedule1"></div>

{% endhighlight %}

{% highlight js %}

 $(function () {
        var dManager = ej.DataManager(window.Default).executeLocal(ej.Query().take(10));
        $("#Schedule1").ejSchedule({
            width: "100%",
            height: "525px",
            currentDate: new Date(2014, 4, 5),
            prioritySettings: {
                enable: true,
                template: "<img class='eimg' src='../images/schedule/${value}.png' height='20px' width='20px'/>",  // We can use the image tag directly to display the priority icon/image
                dataSource:
                [
                { text: "None", id: 1, value: "none" },
                { text: "Critical", id: 2, value: "critical" },
                { text: "UltraCritical", id: 3, value: "ultracritical" }
                ],
            },
            categorizeSettings: { enable: true },
            appointmentSettings: {
                dataSource: dManager,
                id: "Id",
                subject: "Subject",
                startTime: "StartTime",
                endTime: "EndTime",
                description: "Description",
                allDay: "AllDay",
                priority: "Priority",
                recurrence: "Recurrence",
                recurrenceRule: "RecurrenceRule"
            }
        });
    });

{% endhighlight %}



On excuting the above mentioned codes will render the same output as follows.

 {% include image.html url="/js/Schedule/Priority_images/Priority_img2.png" Caption=""%}


{% include image.html url="/js/Schedule/Priority_images/Priority_img3.png" Caption="schedule with customised priority."%}

