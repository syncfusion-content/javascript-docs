---
layout: post
title: webAPI reference for PdfViewer
description: webAPI reference for PdfViewer
documentation: API
platform: js-webapi
keywords: pdfviewer,ejpdfviewer, syncfusion, pdfviewer webapi
---

## Load

[POST&nbsp;&nbsp;/Api/PdfViewer/Load](http://js.syncfusion.com/demos/ejServices/api/PdfViewer/Load)

It loads the PDF document in the PDF viewer control and process the PDF document for each request.

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

```javascript
{
  imagestream,
  pagesize,
  currentpage,
  filename,
  pagecount,
  pageheight,
  pagewidth,
  linkannotation,
  annotpagenum,
  selection,
  pageContents,
  restrictionSummary
}
```


### Code example 

```javascript

URL: http://js.syncfusion.com/demos/ejServices/api/PdfViewer/Load

$.ajax({
		type: “POST”,
		url: “http://js.syncfusion.com/demos/ejServices/api/PdfViewer/Load”,
		crossDomain: true,
		contentType: “application/json; charset=utf-8”,
		dataType: “json”,
		traditional: true
})


```
>The above example is used to load the PDF document in the PdfViewer.

## FileUpload

[POST&nbsp;&nbsp;/Api/PdfViewer/FileUpload](http://js.syncfusion.com/demos/ejServices/api/PdfViewer/FileUpload)

It uploads and loads the PDF document to the PDF viewer control.

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

```javascript
{
  imagestream,
  pagesize,
  currentpage,
  filename,
  pagecount,
  pageheight,
  pagewidth,
  linkannotation,
  annotpagenum,
  selection,
  pageContents,
  restrictionSummary
}
```
### Code example 

```javascript

URL: http://js.syncfusion.com/demos/ejServices/api/PdfViewer/FileUpload

$.ajax({
		type: “POST”,
		url: “http://js.syncfusion.com/demos/ejServices/api/PdfViewer/FileUpload”,
		crossDomain: true,
		contentType: “application/json; charset=utf-8”,
		dataType: “json”,
		traditional: true
})

```
>The above code example is used to upload the PDF file.


## Download

[POST&nbsp;&nbsp;/Api/PdfViewer/Download](http://js.syncfusion.com/demos/ejServices/api/PdfViewer/Download)

It downloads the PDF document that is in view of the PDF viewer control.

### Response information 

Code: 200

Access-Control-Allow-Origin: *

Content-Type:  application/json; charset=utf-8

Response: DocumentStream

### Code example 

```javascript

http://js.syncfusion.com/demos/ejServices/api/PdfViewer/Download

$.ajax({
        type: "POST",
        url: “http://js.syncfusion.com/demos/ejServices/api/PdfViewer/Download”,
        crossDomain: true,
        contentType: “application/json; charset=utf-8”,
        dataType:”json”,
        traditional: true,
        aync: false
})

```
>The above example shows that it will download the PDF doccument.