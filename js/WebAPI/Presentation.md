---
layout: post
title: webAPI reference for Presentation
description: webAPI reference for Presentation
documentation: ug
platform: js
keywords: Presentation, syncfusion, Presentation webapi
---

## CreatePresentation

[POST] [/Api/Presentation/CreatePresentation](http://js.syncfusion.com/demos/ejservices/api/Presentation/CreatePresentation)

It is used to create simple PowerPoint presentation with texts, images and tables.

### Response information 

Code: 200

Content-Type: data:attachment/pptx

### Code example 

{% highlight js %}

URL: http://js.syncfusion.com/demos/ejServices/api/Presentation/CreatePresentation

  $(function () {
        $('#slidespresentation').click(function () {
		var formData = new FormData();
		var req = new XMLHttpRequest();
		req.open("POST", window.baseurl + "/api/Presentation/CreatePresentation", true);
		req.send(formData);
		req.responseType = "blob";
		
		req.onload = function (event) {
		if (req.response != null && navigator.msSaveBlob)
			return navigator.msSaveBlob(new Blob([req.response], { type: "data:attachment/powerpoint" }), "Sample.pptx");
		var a = document.createElement('a');
		var url = window.URL.createObjectURL(new Blob([req.response], {type: "data:attachment/powerpoint"}));
		a.href = url;
		a.download = "Sample.pptx";
		document.body.appendChild(a);
		a.click();
		window.URL.revokeObjectURL(url);
		a.remove();};
       });
   });

{% endhighlight %}

> The above sample demonstrates adding slides to a PowerPoint presentation and adding contents to the PowerPoint slide.

## ManipulateSmartArt

[POST] [/Api/Presentation/ManipulateSmartArt](http://js.syncfusion.com/demos/ejservices/api/Presentation/ManipulateSmartArt)

It is used to manipulate SmartArt in PowerPoint slides.

### Response information 

Code: 200

Content-Type: data:attachment/pptx

### Code example 

{% highlight js %}

URL: http://js.syncfusion.com/demos/ejServices/api/Presentation/ManipulateSmartArt

  $(function () {
        $('#SmartPresentation').click(function () {
		var formData = new FormData();
		var req = new XMLHttpRequest();
		req.open("POST", window.baseurl + "/api/Presentation/ManipulateSmartArt", true);
		req.send(formData);
		req.responseType = "blob";
		
		req.onload = function (event) {
		if (req.response != null && navigator.msSaveBlob)
			return navigator.msSaveBlob(new Blob([req.response], { type: "data:attachment/powerpoint" }), "Sample.pptx");
		var a = document.createElement('a');
		var url = window.URL.createObjectURL(new Blob([req.response], {type: "data:attachment/powerpoint"}));
		a.href = url;
		a.download = "Sample.pptx";
		document.body.appendChild(a);
		a.click();
		window.URL.revokeObjectURL(url);
		a.remove();};
       });
   });

{% endhighlight %}

> The above sample demonstrates adding and removing the nodes in a SmartArt diagram.

## MergePresentations

[POST] [/Api/Presentation/MergePresentations](http://js.syncfusion.com/demos/ejservices/api/Presentation/MergePresentations)

It is used to merge two PowerPoint presentations.

| Parameter | Data Type | Description |
|---|---|---|
|MergingType|String|It specifies the paste option for merging presentations.|

### Response information 

Code: 200

Content-Type: data:attachment/pptx

### Code example 

{% highlight js %}

URL: http://js.syncfusion.com/demos/ejServices/api/Presentation/MergePresentations

  $(function () {
        $('#mergingpresentation').click(function () {
		var formData = new FormData();
		var destinationtheme = document.getElementById("destinationtheme").checked;
        var sourceformatting = document.getElementById("sourceformatting").checked;
		var contentType = "data:attachment/powerpoint";
        var filename = "Sample.pptx";
        if (sourceformatting) {
            formData.append("MergingType", "SourceFormatting");
        }
        else if(destinationtheme)
        {
            formData.append("MergingType", "DestinationTheme");
        }
		var req = new XMLHttpRequest();
		req.open("POST", window.baseurl + "/api/Presentation/MergePresentations", true);
		req.send(formData);
		req.responseType = "blob";
		
		req.onload = function (event) {
		if (req.response != null && navigator.msSaveBlob)
			return navigator.msSaveBlob(new Blob([req.response], { type: contentType }), filename);
		var a = document.createElement('a');
		var url = window.URL.createObjectURL(new Blob([req.response], {type: contentType}));
		a.href = url;
		a.download = filename;
		document.body.appendChild(a);
		a.click();
		window.URL.revokeObjectURL(url);
		a.remove();};
	 });
   });

{% endhighlight %}

> The above sample demonstrates merging two PowerPoint documents with paste options - use destination theme and source formatting using Essential Presentation. 

## CreateNotes

[POST] [/Api/Presentation/CreateNotes](http://js.syncfusion.com/demos/ejservices/api/Presentation/CreateNotes)

It is used to add notes page in PowerPoint slides and converts the notes page to PDF document. 

### URL parameters

| Parameter | Data Type | Description |
|---|---|---|
|FormatType|String|It contains format type to save.|

### Response information

Code: 200

Content-Type: data:attachment/pptx

### Code example 

{% highlight js %}

URL: http://js.syncfusion.com/demos/ejServices/api/Presentation/CreateNotes

  $(function () {
        $('#NotesPresentation').click(function () {
		var formData = new FormData();
		var rdButtonPPTX = document.getElementById("rdButtonPPTX").checked;
        var rdButtonPDF = document.getElementById("rdButtonPDF").checked;
		var contentType;
        var filename;
        if (rdButtonPPTX) {
            formData.append("FormatType", "PPTX");
            contentType = "data:attachment/powerpoint";
            filename = "Sample.pptx";
        }
        else if(rdButtonPDF)
        {
            formData.append("FormatType", "PDF");
            contentType = "data:attachment/pdf";
            filename = "Sample.pdf";
        }
		var req = new XMLHttpRequest();
		req.open("POST", window.baseurl + "/api/Presentation/CreateNotes", true);
		req.send(formData);
		req.responseType = "blob";
		
		req.onload = function (event) {
		if (req.response != null && navigator.msSaveBlob)
			return navigator.msSaveBlob(new Blob([req.response], { type: contentType }), filename);
		var a = document.createElement('a');
		var url = window.URL.createObjectURL(new Blob([req.response], {type: contentType}));
		a.href = url;
		a.download = filename;
		document.body.appendChild(a);
		a.click();
		window.URL.revokeObjectURL(url);
		a.remove();};
     });
   });

{% endhighlight %}

> The above sample demonstrates adding the Notes pages to a Presentation slide and how to convert the Notes pages in the PowerPoint Presentation as PDF document. 

## ConvertToPDF

[POST] [/Api/Presentation/ConvertToPDF](http://js.syncfusion.com/demos/ejservices/api/Presentation/ConvertToPDF)

It is used to convert the PowerPoint presentation to PDF document

### URL parameters

| Parameter | Data Type | Description |
|---|---|---|
|UploadedFile|File|It contains uploaded file to oonvert as PDF.|

### Response information 

Code: 200

Content-Type: data:attachment/pdf

### Code example 

{% highlight js %}

URL: http://js.syncfusion.com/demos/ejServices/api/Presentation/ConvertToPDF

  $(function () {
        $('#pptxtopdfpresentation').click(function () {
		var formData = new FormData();
		var req = new XMLHttpRequest();
		req.open("POST", window.baseurl + "/api/Presentation/ConvertToPDF", true);
		req.send(formData);
		req.responseType = "blob";
		
		req.onload = function (event) {
		if (req.response != null && navigator.msSaveBlob)
			return navigator.msSaveBlob(new Blob([req.response], { type: "data:attachment/pdf" }), "Sample.pdf");
		var a = document.createElement('a');
		var url = window.URL.createObjectURL(new Blob([req.response], {type: "data:attachment/pdf"}));
		a.href = url;
		a.download = "Sample.pdf";
		document.body.appendChild(a);
		a.click();
		window.URL.revokeObjectURL(url);
		a.remove();};
    });
   });

{% endhighlight %}

> The above sample demonstrates converting a PowerPoint presentation to PDF document. 
