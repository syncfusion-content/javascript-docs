---
layout: post
title: webAPI reference for ejUploadbox
description: webAPI reference for ejUploadbox
documentation: API
platform: js-webapi
keywords: uploadbox, ejUploadbox, syncfusion, uploadbox webapi
---

## Save

[POST&nbsp;&nbsp;/Api/UploadBox/Save](http://js.syncfusion.com/demos/ejservices/api/UploadBox/Save)

It is used for storing the uploaded file.

### URL parameters

|  Parameter |  Description | 
|---|---|
|FileName|Name of the files to be stored.| 


### Response information 

Code: 204 No Content

Content-Type: multipart/form-data;

### Code example 

```javascript

$(function () {
	$("#UploadDefault").ejUploadbox({
		saveUrl: "http://js.syncfusion.com/demos/ejservices/api/UploadBox/Save"
	});
});

```
>In the above example we have used webAPI named as Save in order to save the uploaded file.

## Remove

[POST&nbsp;&nbsp;/Api/UploadBox/Remove](http://js.syncfusion.com/demos/ejservices/api/UploadBox/Remove)

It is used for removing the stored files from server.

### URL parameters

|  Parameter |  Description | 
|---|---|
|FileName|Name of the files to be removed from the server.| 

### Response information 

Code: 204 No Content

Content-Type: application/x-www-form-urlencoded; charset=UTF-8

### Code example 

```javascript

$(function () {
	$("#UploadDefault").ejUploadbox({
		saveUrl: "http://js.syncfusion.com/demos/ejservices/api/UploadBox/Save",
		removeUrl: "http://js.syncfusion.com/demos/ejservices/api/UploadBox/Remove",
	});
});

```

>In the above example we have used webAPI named as Remove in order to remove the saved file.