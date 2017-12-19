---
title: Getting started with Schedule component	
description: Rendering a basic Scheduler with remote data
platform: js
control: schedule
documentation: ug
keywords: ejschedule, schedule, schedule widget, js schedule
api: /api/js/ejschedule 
---
# Getting Started

To render the Schedule control, the following list of external dependencies are needed, 

* [jQuery](http://jquery.com) - 1.7.1 and later versions
* [jsRender](https://github.com/borismoore/jsrender) - to render the templates
* [jQuery.easing](http://gsgd.co.uk/sandbox/jquery/easing) - to support animation effects in the components

The other required internal dependencies are tabulated below,

<table>
<tr>
<th>
File<br/><br/></th><th>
Description/Usage<br/><br/></th></tr>
<tr>
<td>
ej.core.min.js<br/><br/></td><td>
Must be referred always first before using all the JS controls.<br/><br/></td></tr>
<tr>
<td>
ej.data.min.js<br/><br/></td><td>
Used to handle data operation and should be used while binding data to JS controls.<br/><br/></td></tr>
<tr>
<td>
ej.globalize.min.js<br/><br/></td><td>
Must be referred to localize any of the JS control's text and content.<br/><br/></td></tr>
<tr>
<td>
ej.schedule.min.js<br/><br/></td><td>
Schedule core script file which includes schedule related scripts files such as <i>ej.schedule.render.js</i>, <i>ej.schedule.resources.js</i> and <i>ej.schedule.horizontal.js</i><br/><br/></td></tr>
<tr>
<td>
ej.scroller.js<br/><br/>ej.touch.js<br/><br/>ej.draggable.js<br/><br/>ej.navigationdrawerbase.js<br/><br/>ej.listviewbase.js<br/><br/>ej.listview.js<br/><br/>ej.recurrenceeditor.js<br/><br/>ej.dropdownlist.js<br/><br/>ej.radiobutton.js<br/><br/>ej.dialog.js<br/><br/>ej.button.js<br/><br/>ej.autocomplete.js<br/><br/>ej.datepicker.js<br/><br/>ej.timepicker.js<br/><br/>ej.checkbox.js<br/><br/>ej.editor.js<br/><br/>ej.menu.js<br/><br/>ej.navigationdrawer.js<br/><br/>ej.tooltip.js<br/><br/></td><td>
These files are referred for proper working of the sub-controls used within Scheduler.<br/><br/></td></tr>
</table>

N> Scheduler uses one or more sub-controls, therefore refer the `ej.web.all.min.js` (which encapsulates all the `ej` controls and frameworks in a single file) in the application instead of referring all the above specified internal dependencies. 

To get the real appearance of the Scheduler, the dependent CSS file `ej.web.all.min.css` (which includes styles of all the widgets) should also needs to be referred.


## Script/CSS Reference

Create a new HTML file and include the below initial code.

{% highlight html %}

<!DOCTYPE html>
<html lang="en" xmlns="http://www.w3.org/1999/xhtml">
    <head>
        <meta charset="utf-8" />
        <title> </title>
    </head>
    <body>
    </body>
</html>

{% endhighlight %}

Refer the CSS file from the specific theme folder to your HTML file within the head section. Refer the built-in available themes from [here](/js/theming-in-essential-javascript-components).

{% highlight html %}

<head>
    <meta charset="utf-8" />
    <title>Getting Started - Schedule</title>
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
</head>

{% endhighlight %}

Add links to the [CDN](/js/cdn) Script files with other required external dependencies.

{% highlight html %}

<head>
    <meta charset="utf-8" />
    <title>Getting Started - Schedule</title>
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jsrender.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
</head>

{% endhighlight %}

N> Uncompressed version of library files are also available which is used for development or debugging purpose and can be generated from the custom script [here](http://csg.syncfusion.com).


## Control Initialization

Create a Div element within the body section of the HTML document, where the Scheduler needs to be rendered.

{% highlight html %}

<body>
	<div id="schedule"></div>
</body>

{% endhighlight %}

Initialize the Schedule control by adding the following script code to the body section of the HTML document.

{% highlight html %}

<body>
    <!-- div for Scheduler creation -->    
    <div id="schedule"></div>
	
    <script type="text/javascript">
        // To initialize Scheduler
        $(function () {
            $("#schedule").ejSchedule();
        });
    </script>
</body>

{% endhighlight %}


## Data Binding

Scheduler uses [ejDataManager](/js/datamanager/overview) which supports both RESTful JSON data services binding and local JSON array binding. The **dataSource** property of the Scheduler can be assigned either with the instance of `ejDataManger` or JSON data array collection. 

For demo purpose, remote data URL is used here and the code example is as follows.

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="schedule"></div>

<script type="text/javascript">
$(function() { // document ready function.
    //DataManager with remote URL
    var dataManager = new ej.DataManager("http://js.syncfusion.com/demos/ejServices/api/Schedule/LoadData");
    $("#schedule").ejSchedule({
        width: "100%",
        height: "600px",
        currentDate: new Date(2014, 4, 5),
        appointmentSettings: {
            dataSource: dataManager
        }
    });
});
</script>

{% endhighlight %}

N> While binding Scheduler dataSource to other web services, proper [data adaptor](/js/datamanager/data-adaptors) needs to be set for `adaptor` option of DataManager.


## Mapper Fields

The appointment fields are needed to be mapped with the appropriate column names from the dataSource as shown below.

{% highlight html %}

<!--Container for ejScheduler widget-->
<div id="schedule"></div>

<script type="text/javascript">
$(function() { // Document is ready
    //DataManager with remote URL
    var dataManager = new ej.DataManager("http://js.syncfusion.com/demos/ejServices/api/Schedule/LoadData");
    $("#schedule").ejSchedule({
        width: "100%",
        height: "600px",
        currentDate: new Date(2014, 4, 5),
        appointmentSettings: {
            dataSource: dataManager,
            id: "Id",
            subject: "Subject",
            startTime: "StartTime",
            endTime: "EndTime",
            allDay: "AllDay",
            recurrence: "Recurrence",
            recurrenceRule: "RecurrenceRule"
        }
    });
});	
</script>

{% endhighlight %}

![](Getting-Started_images/Getting-Started_img1.png)


