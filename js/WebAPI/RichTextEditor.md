---
layout: post
title: webAPI reference for ejRTE
description: webAPI reference for ejRTE
documentation: ug
platform: js
keywords: RTE, ejRTE, syncfusion, RTE webapi
---

## Import

 [POST] [/Api/RTE/Import](http://js.syncfusion.com/demos/ejservices/api/RTE/Import)

It is used to Import a Word document into RTE 

### URL parameters

|  Parameter |  Description | 
|---|---|
|RTEId|RTE ID will send to server as query string and it is used in server side to extract fileName.| 


### Response information 

Code: 200

Content-Type: application/json; charset=utf-8

Response:  Returns the string containing the contents of the imported document.


### Code example 

{% highlight js %}

$(function () {
$("#rteExport").ejRTE({
    width:"100%",
    minWidth:"150px",
    importSettings: { url: "http://js.syncfusion.com/demos/ejservices/api/RTE/Import" },
    tools: {
        importExport: ["import"]
    }
});
});

{% endhighlight %}

>In the above example we have used the import option to import the Word document into RTE.

## WordExport

 [POST] [/Api/RTE/WordExport](http://js.syncfusion.com/demos/ejservices/api/RTE/WordExport)

It is used for exporting the contents of RTE into a Word document.

### URL parameters

|  Parameter |  Description | 
|---|---|
|RTEId|RTE ID will send to server as query string and it is used in server side to extract fileName and contents of RTE. | 


### Response information 

Code: 200

Content-Type: application/json; charset=utf-8

### Code example 

{% highlight js %}

$(function () {
$("#rteExport").ejRTE({
    width:"100%",
    minWidth:"150px",
    exportToWordSettings: { url:"http://js.syncfusion.com/demos/ejservices/api/RTE/WordExport", fileName: "WordSample"},
    tools: {
        importExport: ["wordExport"]
    }
});
});

{% endhighlight %}

>The above example shows that the RTE content has been exported in Word file.

## PdfExport

 [POST] [/Api/RTE/PdfExport](http://js.syncfusion.com/demos/ejservices/api/RTE/PdfExport)

It is used for exporting the contents of RTE into a PDF document.

### URL parameters

|  Parameter |  Description | 
|---|---|
|RTEId|RTE ID will send to server as query string and it is used in server side to extract fileName and contents of RTE. | 

### Response information 

Code: 200

Content-Type: application/json; charset=utf-8

### Code example 

{% highlight js %}

$(function () {
$("#rteExport").ejRTE({
    width:"100%",
    minWidth:"150px",
    exportToWordSettings: { url:"http://js.syncfusion.com/demos/ejservices/api/RTE/PdfExport", fileName: "WordSample"},
    tools: {
        importExport: ["pdfExport"]
    }
});
});

{% endhighlight %}

>The above example shows that the RTE content has been exported in PDF file.
