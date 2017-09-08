---
layout: post
title: webAPI reference for ejSchedule
description: webAPI reference for ejSchedule
documentation: ug
platform: js
keywords: Schedule, ejSchedule, syncfusion, ejSchedule webapi
---

## LoadData

 [POST] [/Api/Schedule/LoadData](http://js.syncfusion.com/demos/ejservices/api/Schedule/LoadData)

It fetches the records from Default Schedule table and binding it to the Scheduler.

### URL parameters

|  Parameter |  Description | 
|---|---|
|CurrentAction|It is used to load the data|
|CurrentView|It contains the current week|
|CurrentDate|It contains the current date|

### Response information 

Code: 200

Content-Type: application/json; charset=utf-8

Response (JSON):   

{% highlight js %}

{
"Id":100,"Subject":"Bering Sea Gold","Location":"chn","StartTime":"2014-05-02T09:00:00","EndTime":"2014-05-02T10 :30:00","Description":null,"Owner":1,"Priority":null,"Recurrence":1,"RecurrenceType":null,"RecurrenceTypeCount" :null,"Reminder":null,"Categorize":"1,2","CustomStyle":null,"AllDay":false,"RecurrenceStartDate":null ,"RecurrenceEndDate":null,"RecurrenceRule":"FREQ=DAILY;INTERVAL=2;COUNT=10","StartTimeZone":null,"EndTimeZone" :null}, {"Id":101,"Subject":"Bering Sea Gold","Location":"mum","StartTime":"2014-05-02T04:00:00","EndTime" :"2014-05-02T05:00:00","Description":null,"Owner":1,"Priority":null,"Recurrence":0,"RecurrenceType":null ,"RecurrenceTypeCount":null,"Reminder":null,"Categorize":"2","CustomStyle":null,"AllDay":false,"RecurrenceStartDate" :null,"RecurrenceEndDate":null,"RecurrenceRule":null,"StartTimeZone":null,"EndTimeZone":null
}, //... 14 more records 

{% endhighlight %}

### Code example 

{% highlight js %}

$(function() {
    var dataManager = ej.DataManager({
        url: "http://js.syncfusion.com/demos/ejservices/api/Schedule/LoadData",
        adaptor: new ej.ODataV4Adaptor()
    });

    $("#schedule").ejSchedule({
        currentDate: new Date(1997, 2, 23),
        appointmentSettings: {
            dataSource: dataManager,
            subject: "ShipName",
            startTime: "OrderDate",
            endTime: "RequiredDate",
            description: "ShipAddress"
        }
    });
});	

{% endhighlight %}

## PdfExport

 [POST] [/Api/Schedule/PdfExport](http://js.syncfusion.com/demos/ejservices/api/Schedule/PDFExport)

It exports the entire Scheduler content into a PDF file format.

### URL parameters

|  Parameter |  Description | 
|---|---|
|ScheduleApps|It is the appointment field which holds the appropriate column names from the schedule dataSource.|
|ScheduleProcessedApps|It contains appointment collection of the schedule.|
|ScheduleModel|It has the model values of schedule.|
|ScheduleProcessedIntervalsApps|Block intervals collection of schedule.| 
|ScheduleBlockedApps|Block intervals fields which holds the appropriate column names from the block intervals dataSource.| 

### Response information 

Code: 200

Content-Type: application/pdf

### Code example 

{% highlight js %}

$("#btnExport").ejButton({
    width: "80px",
    height: "30px",
    click: "onExportClick"
});
function onExportClick(e) {
    var obj = $("#Schedule1").data("ejSchedule");
    obj.exportSchedule("http://js.syncfusion.com/demos/ejservices/api/Schedule/PDFExport", null, null);
    e.cancel = true;
}

{% endhighlight %}

>Add the above code along with the load data sample and the result of this code is used to save the Scheduler in a PDF file format.

## IcsExport

 [POST] [/Api/Schedule/IcsExport](http://js.syncfusion.com/demos/ejservices/api/Schedule/ICSExport)

It exports the complete appointment data from Scheduler into an ICS file format.

### URL parameters

|  Parameter |  Description | 
|---|---|
|ScheduleApps|It is the appointment field which holds the appropriate column names from the schedule dataSource.|
|ScheduleProcessedApps|It contains appointments collection of the schedule.|
|ScheduleModel|It has the model values of schedule.|
|ScheduleProcessedIntervalsApps|Block intervals collection of schedule.| 
|ScheduleBlockedApps|Block intervals fields which holds the appropriate column names from the block intervals dataSource.| 

### Response information 

Code: 200

Content-Type: text/Calendar

### Code example 


{% highlight js %}

$("#btnExport").ejButton({
    width: "80px",
    height: "30px",
    click: "onExportClick"
});
function onExportClick(e) {
    var obj = $("#Schedule1").data("ejSchedule");
    obj.exportSchedule("http://js.syncfusion.com/demos/ejservices/api/Schedule/ICSExport", null, null);
    e.cancel = true;
}

{% endhighlight %}

>Add the above code along with the load data sample and the result of this code is used to save the Scheduler in a ICS file format.


## Save

 [POST] [/Api/Schedule/Save](http://js.syncfusion.com/demos/ejservices/api/Schedule/Save)

It imports the appointment data generated from external calendar into Scheduler.

### Response information 

Code: 200

Content-Type: application/xml; charset=utf-8

Response (JSON):   

{% highlight js %}

{
"Id":100,"Subject":"Bering Sea Gold","Location":"chn","StartTime":"2014-05-02T09:00:00",
"EndTime":"2014-05-02T10 :30:00","Description":null,"Owner":1,
"Priority":null,"Recurrence":1,"RecurrenceType":null,
"RecurrenceTypeCount" :null,"Reminder":null,"Categorize":"1,2","CustomStyle":null,
"AllDay":false,"RecurrenceStartDate":null ,"RecurrenceEndDate":null,
"RecurrenceRule":"FREQ=DAILY;INTERVAL=2;COUNT=10","StartTimeZone":null,
"EndTimeZone" :null}, {"Id":101,"Subject":"Bering Sea Gold",
"Location":"mum","StartTime":"2014-05-02T04:00:00","EndTime" :"2014-05-02T05:00:00","Description":null,"Owner":1,"Priority":null,
"Recurrence":0,"RecurrenceType":null ,"RecurrenceTypeCount":null,"Reminder":null,
"Categorize":"2","CustomStyle":null,"AllDay":false,
"RecurrenceStartDate" :null,"RecurrenceEndDate":null,"RecurrenceRule":null,
"StartTimeZone":null,"EndTimeZone":null
}, //... 29 more records 

{% endhighlight %}

### Code example 

{% highlight js %}

  $("#UploadDefault").ejUploadbox({
		saveUrl: "http://js.syncfusion.com/demos/ejservices/api/Schedule/Save",
		extensionsAllow: ".ics",
		height: "31px", autoUpload: true,
		width: "80px",
		buttonText: {
			browse: "Import",
		},
		showFileDetails: false,
		success: "onComplete",
		dialogAction: {
			closeOnComplete: true,
		},
    });

{% endhighlight %}

>Add the above code along with the load data sample and the result of this code is used to import the appointment data generated from external calendar into Scheduler.
