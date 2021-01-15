---
layout: post
title: WebAPI reference for JQuery PDF Viewer | Syncfusion
description: Learn about WebAPI reference for JQuery PDF Viewer and more details. This document explains the features such as load, file upload and download
documentation: ug
platform: js
keywords: pdfviewer,ejpdfviewer, syncfusion, pdfviewer webapi
---

# WebAPI reference for JQuery PDF Viewer

## Load

 [POST] [/Api/PdfViewer/Load](http://js.syncfusion.com/demos/ejServices/api/PdfViewer/Load)

Loads the PDF document into the PDF viewer control and parse the PDF document content on the server side, then return the necessary details for rendering PDF document content to the client side as JSON data.

### URL parameters

|  Parameter |Data Type| Description | 
|---|---|---|
|viewerAction |String|Specifies the action of the AJAX request.|
|controlId|String|Control ID of the widget.|
|pageindex|String|Current page index of the PDF document which display the content in PDF Viewer.|
|isInitialLoading|String|Specifies the AJAX request whether the request is initial loading or consecutive loading.| 

### Response information 

Code: 200

Access-Control-Allow-Origin: *

Content-Encoding: gzip

Content-Type:  application/json; charset=utf-8

Response (JSON):   

{% highlight js %}
{
  imageStream,
  pageSize,
  currentPage,
  fileName,
  pageCount,
  pageHeight,
  pageWidth,
  linkAnnotation,
  annotationPageNumber,
  selection,
  pageContents,
  restrictionSummary
}
{% endhighlight %}


### Code example 

{% highlight js %}

URL: http://js.syncfusion.com/demos/ejServices/api/PdfViewer/Load

$.ajax({
		type: "POST",
		url: "http://js.syncfusion.com/demos/ejServices/api/PdfViewer/Load",
		crossDomain: true,
		contentType: "application/json; charset=utf-8",
		dataType: "json",
		traditional: true
})

{% endhighlight %}

>The above example is used to load the PDF document in the PdfViewer.

## FileUpload

 [POST] [/Api/PdfViewer/FileUpload](http://js.syncfusion.com/demos/ejServices/api/PdfViewer/FileUpload)

Uploads and loads the PDF document into the PDF viewer control.

### URL parameters

|  Parameter |Data Type|Description | 
|---|---|---|
|viewerAction |String|Specifies the action of the AJAX request.|
|controlId |String|Control ID of the widget.|
|pageindex |String|Current page index of the PDF document which display the content in PDF Viewer.| 
|isInitialLoading|String|Specifies the AJAX request whether the request is initial loading or consecutive loading.|
|newFileName|String|New file name to be loaded into the PDF Viewer.|

### Response information 

Code: 200

Access-Control-Allow-Origin: *

Content-Encoding: gzip

Content-Type:  application/json; charset=utf-8

Response (JSON):   

{% highlight js %}
{
  imageStream,
  pageSize,
  currentPage,
  fileName,
  pageCount,
  pageHeight,
  pageWidth,
  linkAnnotation,
  annotationPageNumber,
  selection,
  pageContents,
  restrictionSummary
}
{% endhighlight %}


### Code example 

{% highlight js %}

URL: http://js.syncfusion.com/demos/ejServices/api/PdfViewer/FileUpload
$.ajax({
    type: "POST",
    url: "http://js.syncfusion.com/demos/ejServices/api/PdfViewer/FileUpload",
    crossDomain: true,
    contentType: "application/json; charset=utf-8",
    dataType: "json",
    traditional: true
})

{% endhighlight %}

>The above code example is used to upload the PDF file.


## Download

 [POST] [/Api/PdfViewer/Download](http://js.syncfusion.com/demos/ejServices/api/PdfViewer/Download)

Downloads the PDF document being displayed in the PDF viewer control.

### Response information 

Code: 200

Access-Control-Allow-Origin: *

Content-Type:  application/json; charset=utf-8

Response: DocumentStream

### Code example 

{% highlight js %}

http://js.syncfusion.com/demos/ejServices/api/PdfViewer/Download

$.ajax({
    type: "POST",
    url: "http://js.syncfusion.com/demos/ejServices/api/PdfViewer/Download",
    crossDomain: true,
    contentType: "application/json; charset=utf-8",
    dataType: "json",
    traditional: true,
    async: false
})

{% endhighlight %}
>The above example shows that it will download the PDF document.
