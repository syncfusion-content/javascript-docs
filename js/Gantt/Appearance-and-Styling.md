---
layout: post
title: Appearance-and-Styling
description: appearance and styling
platform: js
control: Gantt
documentation: ug
api: /api/js/ejgantt
---

# Appearance and Styling

The look and feel of the Gantt control can be customized by applying themes and formatting the schedule header.

## Schedule Header Customization

You can change the format of schedule headers in various timescale modes by using [`dayHeaderFormat`](/api/js/ejgantt#members:scheduleheadersettings-dayheaderformat "scheduleHeaderSettings.dayHeaderFormat"), [`hourHeaderFormat`](/api/js/ejgantt#members:scheduleheadersettings-hourheaderformat "scheduleHeaderSettings.hourHeaderFormat"), [`weekHeaderFormat`](/api/js/ejgantt#members:scheduleheadersettings-weekheaderformat "scheduleHeaderSettings.weekHeaderFormat"), [`monthHeaderFormat`](/api/js/ejgantt#members:scheduleheadersettings-monthheaderformat "scheduleHeaderSettings.monthHeaderFormat") and [`yearHeaderFormat`](/api/js/ejgantt#members:scheduleheadersettings-yearheaderformat "scheduleHeaderSettings.yearHeaderFormat") properties available in [`scheduleHeaderSettings`](/api/js/ejgantt#members:scheduleheadersettings) property.
And you can change the background of weekends available in timescale by using [`weekendBackground`](/api/js/ejgantt#members:scheduleheadersettings-weekendbackground "scheduleHeaderSettings.weekendBackground") property, please refer the following code example.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        scheduleHeaderSettings: {
            weekHeaderFormat: "MMM yyyy",
            dayHeaderFormat: "d",
            hourHeaderFormat: "HH",
            monthHeaderFormat: "MMM",
            yearHeaderFormat : "yyyy", 
            weekendBackground: '#F2F2F2'
        }
    });

{% endhighlight %}

The following screenshot shows the customized format schedule header in Gantt control.

![](/js/Gantt/Appearance-and-Styling_images/Appearance-and-Styling_img1.png)

## Taskbar Customization

 The Taskbar can be customized based on the task information in Gantt control by using [queryTaskbarInfo](/api/js/ejgantt#events:querytaskbarinfo) event. The following code example shows how to customize the Taskbar in Gantt control.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        queryTaskbarInfo: function(args) {
            //queryTaskbarInfo will be triggered when a taskbar is rendered

            if (args.data.level === 0) {
                args.parentTaskbarBackground = "pink";
                args.parentProgressbarBackground = "cyan";
            } else {
                if (args.data.status == "60") {
                    args.progressbarBackground = "red";
                } else if (args.data.status == "70") {
                    args.progressbarBackground = "yellow";
                } else if (args.data.status == "80") {
                    args.progressbarBackground = "green";
                }
            }
        }

    });

{% endhighlight %}

The following screenshot shows the customized taskbar in Gantt control.

![](/js/Gantt/Appearance-and-Styling_images/Appearance-and-Styling_img2.png)

## Themes

 The following are the types of themes available in Gantt control.

1.Flat Azure                           
2.Flat Azure Dark                  
3.Flat Lime                             
4.Flat Lime Dark                   
5.Flat Saffron                        
6.Flat Saffron Dark
7.Gradient Azure
8.Gradient Azure Dark
9.Gradient Lime
10.Gradient Lime Dark
11.Gradient Saffron
12.Gradient Saffron Dark
13.Bootstrap

The theme (Gradient lime) can be applied to the Gantt control by using the style sheet from the online link as follows.

{% highlight html %}

    <!DOCTYPE html>

    <html xmlns="http://www.w3.org/1999/xhtml">
        <head>
        <title>Getting Started with Gantt Control for JavaScript</title>
        <!-- style sheet for default theme(gradient lime) -->
        <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" /> 
        //...
    </html>

{% endhighlight %}

The following screenshot shows the Gantt control with `Gradient-lime` theme.

![](/js/Gantt/Appearance-and-Styling_images/Appearance-and-Styling_img3.png)

