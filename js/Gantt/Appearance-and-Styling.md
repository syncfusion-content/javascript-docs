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

### Schedule Header Unit Format
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

### Schedule Header Unit Width

Schedule header units width value can be customized by using [`scheduleHeaderSettings.timescaleUnitSize`](/api/js/ejgantt#members:scheduleheadersettings-timescaleunitsize "scheduleHeaderSettings.timescaleUnitSize") property. The default value of this property was `100%`, we can set value for this property from `50%` to `500%`.
The following code example shows how to use this properties.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        scheduleHeaderSettings: {
            timescaleUnitSize: "70%",
        }
    });

{% endhighlight %}

The following screenshot shows the output of above code example.
![](/js/Gantt/Appearance-and-Styling_images/Appearance-and-Styling_img8.png)

Schedule header units with `300%` width value
{:.caption}

![](/js/Gantt/Appearance-and-Styling_images/Appearance-and-Styling_img9.png)

Schedule header units with `70%` width value
{:.caption}

You can find the JS playground sample for this properties [here](http://jsplayground.syncfusion.com/Sync_5ltkoq4b "Demo Link").

## Taskbar Customization

### Taskbar Background

Background color of child taskbars and parent taskbars can be customized by using [`taskbarBackground`](/api/js/ejgantt#members:taskbarbackground) and [`parentTaskbarBackground`](/api/js/ejgantt#members:parenttaskbarbackground) properties. The following code example shows how to use this properties.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        taskbarBackground: "#1764d7",
        parentTaskbarBackground: "#91dc88",
    });

{% endhighlight %}

The following screenshot shows the customized parent and child taskbars in Gantt.
![](/js/Gantt/Appearance-and-Styling_images/Appearance-and-Styling_img5.png)

You can find the JS playground sample for this properties [here](http://jsplayground.syncfusion.com/Sync_wd4b4xrw "Demo Link").

### Taskbar Height

Height of child taskbars and parent taskbars can be customized by using [`taskbarHeight`](/api/js/ejgantt#members:taskbarheight) property. The following code example shows how to use the property.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        taskbarHeight: 30,
        rowHeight: 40
    });

{% endhighlight %}

The following screenshot shows the output of above code example.
![](/js/Gantt/Appearance-and-Styling_images/Appearance-and-Styling_img6.png)

You can find the JS playground sample for this properties [here](http://jsplayground.syncfusion.com/Sync_skkep23a "Demo Link").

N> [`taskbarHeight`](/api/js/ejgantt#members:taskbarheight) value should be lower than [`rowHeight`](/api/js/ejgantt#members:rowheight) property value.

### Progressbar Customization

Background color of child task's progress bar and parent task's progress bar can be customized by using [`progressbarBackground `](/api/js/ejgantt#members:progressbarbackground) and [`parentProgressbarBackground`](/api/js/ejgantt#members:parentprogressbarbackground) properties. Progress bars height can be changed by using [`progressbarHeight`](/api/js/ejgantt#members:progressbarheight) property. The visibility of progress status label inside the taskbars can be changed by using [`showProgressStatus`](/api/js/ejgantt#members:showprogressstatus) property.
 The following code example shows how to use this properties.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        progressbarBackground: "#8c83b1",
        parentProgressbarBackground: "#af2f2f",
        progressbarHeight: 80,
        showProgressStatus: true,
    });

{% endhighlight %}

The following screenshot shows the customized progress bar of parent and child tasks in Gantt.
![](/js/Gantt/Appearance-and-Styling_images/Appearance-and-Styling_img7.png)

You can find the JS playground sample for this properties [here](http://jsplayground.syncfusion.com/Sync_ca3bj03o "Demo Link").

N> [`progressbarHeight`](/api/js/ejgantt#members:progressbarheight) property value should be in 0 to 100, because this value was considered as percentage value of taskbar height value.

### Conditional Formatting

The Taskbar can be customized based on the task information in Gantt control by using [`queryTaskbarInfo`](/api/js/ejgantt#events:querytaskbarinfo) event. The following code example shows how to customize the Taskbar in Gantt control.

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

## Dependency line customization

Width and background color of dependency line in Gantt can be customized by using [`connectorlineWidth`](/api/js/ejgantt#members:connectorlinewidth) and [`connectorLineBackground`](/api/js/ejgantt#members:connectorlinebackground) properties. The following code example shows how to use this properties.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        connectorlineWidth :2,
        connectorLineBackground: "#0aecb8",
    });

{% endhighlight %}

The following screenshot shows the customized dependency lines in Gantt.
![](/js/Gantt/Appearance-and-Styling_images/Appearance-and-Styling_img4.png)

You can find the JS playground sample for this properties [here](http://jsplayground.syncfusion.com/Sync_ecvgphrl "Demo Link").

## Weekend background

Background color of weekends in Gantt can be changed by using [`weekendBackground`](/api/js/ejgantt#members:weekendbackground) property. The following code example shows how to use this properties.

{% highlight javascript %}

    $("#GanttContainer").ejGantt({
        //...
        weekendBackground: "rgba(116, 195, 231, 0.26)",
    });

{% endhighlight %}

The following screenshot shows the customized dependency lines in Gantt.
![](/js/Gantt/Appearance-and-Styling_images/Appearance-and-Styling_img10.png)

You can find the JS playground sample for this properties [here](http://jsplayground.syncfusion.com/Sync_rkk1fzd5 "Demo Link").

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
14.High Contrast 01
15.High Contrast 02
16.Material
17.Office-365

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

## Configuring CSS Class

In Gantt [`cssClass`](/api/js/ejgantt#members:cssclass) property was used to apply different customized styles to multiple Gantt controls available in same page. The following code example shows how to apply different background color for each Gantt control's toolbar element.

{% highlight html %}
    <style>
        .c-class1.e-gantt .e-toolbar {
            background-color: rgba(169, 45, 45, 0.31);
        }
        .c-class2.e-gantt .e-toolbar {
            background-color: rgba(0, 128, 0, 0.2);
        }
    </style>
    <div>
        <div id="GanttContainer"></div>
    </div>

    <div>
        <div id="GanttContainer1"></div>
    </div>
    <script>
    $("#GanttContainer").ejGantt({
        //...
        cssClass: "c-class1",
    });

     $("#GanttContainer1").ejGantt({
        //...
        cssClass: "c-class2",
    });
    </script>

{% endhighlight %}

The below screenshot shows the output of above code example.

![](/js/Gantt/Appearance-and-Styling_images/Appearance-and-Styling_img11.png)

## Customize rows and cells

While rendering the rows in Grid part of Gantt [`rowDataBound`](/api/js/ejgantt#events:rowdatabound) event and [`queryCellInfo`](/api/js/ejgantt#events:querycellinfo) event will be triggered for each rows and cells. Using this event we can customize the rows and cells. The below code example shows how to customize the cell and row element using this events.

{% highlight javascript %}

$("#GanttContainer").ejGantt({
    //...
    queryCellInfo: function (args) {
        if (args.column.mappingName == "progress") {
            if (args.data.item["progress"] < 80)
                $(args.cellElement).css("background-color", "rgba(255, 0, 0, 0.12)");
            else
                $(args.cellElement).css("background-color", "rgba(86, 226, 86, 0.25)");
        } 
    },
    rowDataBound: function (args) {
        if (args.data.item["taskID"] == 5)
            $(args.rowElement).css("background-color", "rgba(251, 255, 0, 0.24)");
    },
});

{% endhighlight %}

The below screenshot shows the output of above code example.
![](/js/Gantt/Appearance-and-Styling_images/Appearance-and-Styling_img12.png)
