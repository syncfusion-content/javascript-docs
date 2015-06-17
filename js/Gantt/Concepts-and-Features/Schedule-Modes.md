---
layout: post
title: Schedule-Modes
description: schedule modes
platform: js
control: Gantt
documentation: ug
---

# Schedule Modes

**Gantt** contains built-in support to switch over to various schedule mode. You can achieve this by defining a **schedule header type** for the **Gantt**.

**Schedule Header Types**

**Gantt** contains the following built-in schedule header types:

* Day – Hour

* Week – Day

* Month – Week

* Year – Month

The following code example illustrates you on how to change the schedule mode.

## Week Schedule Mode

In the Week schedule mode, the upper part of the schedule header displays the **weeks** whereas the bottom half of the header displays the d**ays.** Refer the following code example.

{% highlight js %}


        $("#GanttContainer").ejGantt({
                //...
                scheduleHeaderSettings: {
                  scheduleHeaderType: ej.Gantt.ScheduleHeaderType.Week,                                                            
                  weekHeaderFormat: "MMM dd , yyyy",
                  dayHeaderFormat: "ddd",
                },             
       });


{% endhighlight %}



The following screenshot illustrates the **Week Schedule** in **Gantt** control.

{% include image.html url="/js/Gantt/Concepts-and-Features/Schedule-Modes_images/Schedule-Modes_img1.png" Caption="Week Schedule in Gantt control"%}

## Month Schedule Mode

In the Week schedule mode, the upper part of the schedule header displays the **Months** whereas the bottom header of the schedule displays its corresponding **Weeks.** Refer the following code example.

{% highlight js %}


      $("#GanttContainer").ejGantt({
                //... 
               scheduleHeaderSettings: {
                  scheduleHeaderType: ej.Gantt.ScheduleHeaderType.Month,                                                            
                  monthHeaderFormat: "MMM yyyy",
                  weekHeaderFormat: "M/dd",
                },             
     });


{% endhighlight %}



The following screenshot illustrates the **Month Schedule** in **Gantt** control.

{% include image.html url="/js/Gantt/Concepts-and-Features/Schedule-Modes_images/Schedule-Modes_img2.png" Caption="Month Schedule in Gantt control"%}

## Year Schedule Mode

In the Week schedule mode, the upper schedule header displays the **Years** whereas the bottom header displays its corresponding **Months**. Refer the following code example.

{% highlight js %}


        $("#GanttContainer").ejGantt({
                //...
                scheduleHeaderSettings: {
                  scheduleHeaderType: ej.Gantt.ScheduleHeaderType.Year,                                                            
                  yearHeaderFormat: "yyyy",
                  monthHeaderFormat: "MMM",
                },             
       });


{% endhighlight %}


The following screen shot shows the **Year Schedule** in **Gantt** control.

{% include image.html url="/js/Gantt/Concepts-and-Features/Schedule-Modes_images/Schedule-Modes_img3.png" Caption="Year Schedule in Gantt control"%}

## Day Schedule Mode

In the Week schedule mode, the upper part of the header displays the **Days** whereas the bottom schedule header displays its corresponding **Hours.** Refer the following code example.

{% highlight js %}


        $("#GanttContainer").ejGantt({
                //...
                scheduleHeaderSettings: {
                  scheduleHeaderType: ej.Gantt.ScheduleHeaderType.Day,                                                            
                  dayHeaderFormat: " dd,MM,yy ",
                  hourHeaderFormat: "HH",
                },             
       });


{% endhighlight %}



The following screenshot illustrates the **Day Schedule** in **Gantt** control.

{% include image.html url="/js/Gantt/Concepts-and-Features/Schedule-Modes_images/Schedule-Modes_img4.png" Caption="Day Schedule in Gantt control"%}

## Hour Schedule Mode

An **Hour-Minute Schedule Mode** tracks the tasks in minutes scale. In this mode, upper schedule header displays **hour scale** and the lower schedule header displays its corresponding **Minutes.** The minute split-up in the lower schedule header can be defined by using the **minutesPerInterval****Enum** property. The enumeration values of the **minutesPerInterval** are,

* auto

* oneMinute

* fiveMinutes

* fifteenMinutes

* thirtyMinutes



The value, **auto,** automatically calculates the interval depending upon the **scheduleStartDate** and 

**scheduleEndDate**, whereas the other enumeration values splits up accordingly.

The **Hour Schedule Mode** supports both the **minute** and h**our** duration units.

{% highlight js %}


       $("#GanttContainer").ejGantt({
               // ... 
               dateFormat: "M/d/yyyy hh:mm:ss tt",
               durationUnit: ej.Gantt.DurationUnit.Minute,
               scheduleHeaderSettings: {
                 scheduleHeaderType: ej.Gantt.ScheduleHeaderType.Hour, 
                 minutesPerInterval: ej.Gantt.minutesPerInterval.FiveMinutes,
               },
               // ...
      });



{% endhighlight %}



{% include image.html url="/js/Gantt/Concepts-and-Features/Schedule-Modes_images/Schedule-Modes_img5.png" Caption="Hour-Minute schedule mode in Gantt control"%}

