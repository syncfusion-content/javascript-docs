---
layout: post
title: webAPI reference for DocIO
description: webAPI reference for DocIO
documentation: ug
platform: js
keywords: DocIO, syncfusion, DocIO webapi
---

## GenerateWordDocument

[POST] [/Api/DocIO/GenerateWordDocument](http://js.syncfusion.com/demos/ejServices/api/DocIO/GenerateWordDocument)

It is used to create a simple Word document with text, image and tables.

### URL parameters

| Parameter | Data Type | Description |
|---|---|---|
|FormatType|String|It contains format type to save.|

### Response information

Code: 200

Access-Control-Allow-Origin: *

Content-Type: data:attachment/filetype

### Code example

{% highlight js %}

URL: http://js.syncfusion.com/demos/ejServices/api/DocIO/GenerateWordDocument

<script>
$('#generatedocument').click(function () {
    var formdata = new FormData();
    var rdButtonDoc = document.getElementById("rdButtonDoc").checked;
    var rdButtonDocx = document.getElementById("rdButtonDocx").checked;
    var rdButtonWordML = document.getElementById("rdButtonWordML").checked;
    var rdButtonPdf = document.getElementById("rdButtonPdf").checked;
    var contenttype;
    var filename;
    if (rdButtonDoc) {
        formdata.append("FormatType", "WordDoc");
        contenttype = "data:attachment/doc";
        filename = "Sample.doc";
    }
    else if(rdButtonDocx)
    {
        formdata.append("FormatType", "WordDocx");
        contenttype = "data:attachment/docx";
        filename = "Sample.docx";
    }
    else if(rdButtonWordML)
    {
        formdata.append("FormatType", "WordML");
        contenttype = "data:attachment/xml";
        filename = "Sample.xml";
    }
    else if(rdButtonPdf)
    {
        formdata.append("FormatType", "Pdf");
        contenttype = "data:attachment/pdf";
        filename = "Sample.pdf";
    }
    var req = new XMLHttpRequest();
    req.open("POST", window.baseurl + "api/DocIO/GenerateWordDocument", true);
    req.send(formdata);
    req.responseType = "blob";
    req.onload = function (event) {
    if (req.response != null && navigator.msSaveBlob)
        return navigator.msSaveBlob(new Blob([req.response], { type: contenttype}), filename);
    var a = document.createElement('a');
    var url = window.URL.createObjectURL(new Blob([req.response], {type: contenttype}));
    a.href = url;
    a.download = filename;
    document.body.appendChild(a);
    a.click();
    window.URL.revokeObjectURL(url);
    a.remove();
    };
});
</script>

{% endhighlight %}

>The above example will generate Word document or PDF.

## ConvertToPDF

[POST] [/Api/DocIO/ConvertToPDF](http://js.syncfusion.com/demos/ejServices/api/DocIO/ConvertToPDF)

It is used to convert Word document to PDF.

### URL parameters

| Parameter | Data Type | Data Type | Description |
|---|---|---|
|UploadedFile|File|It contains uploaded file to oonvert as PDF.|

### Response information

Code: 200

Access-Control-Allow-Origin: *

Content-Type: data:attachment/pdf

### Code example

{% highlight js %}

URL: http://js.syncfusion.com/demos/ejServices/api/DocIO/ConvertToPDF

<script>
$('#converttopdf').click(function () {
    var formdata = new FormData();
    var files = $("#inputfile").get(0).files;
    // Add the uploaded image content to the form data collection
    if (files.length > 0) {
        formdata.append("UploadedFile", files[0]);
    }
    var req = new XMLHttpRequest();
    req.open("POST", window.baseurl + "api/DocIO/ConvertToPDF", true);
    req.send(formdata);
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
    a.remove();
    };
});
</script>

{% endhighlight %}

>The above example will result PDF document being converted from Word document.

## ApplyTextFormat

[POST] [P/Api/DocIO/ApplyTextFormat](http://js.syncfusion.com/demos/ejServices/api/DocIO/ApplyTextFormat)

It is used to generate Word Document with various text formats such as character/text level formatting, paragraph level formatting and list level formatting.

### URL parameters

| Parameter | Data Type | Description |
|---|---|---|
|FormatType|String|It contains format type to save.|

### Response information

Code: 200

Access-Control-Allow-Origin: *

Content-Type: data:attachment/filetype

### Code example

{% highlight js %}

URL: http://js.syncfusion.com/demos/ejServices/api/DocIO/ApplyTextFormat

<script>
$('#generatedocument').click(function () {
    var formdata = new FormData();
    var rdButtonDoc = document.getElementById("rdButtonDoc").checked;
    var rdButtonDocx = document.getElementById("rdButtonDocx").checked;
    var rdButtonWordML = document.getElementById("rdButtonWordML").checked;
    var rdButtonPdf = document.getElementById("rdButtonPdf").checked;
    var contenttype;
    var filename;
    if (rdButtonDoc) {
        formdata.append("FormatType", "WordDoc");
        contenttype = "data:attachment/doc";
        filename = "Sample.doc";
    }
    else if(rdButtonDocx)
    {
        formdata.append("FormatType", "WordDocx");
        contenttype = "data:attachment/docx";
        filename = "Sample.docx";
    }
    else if(rdButtonWordML)
    {
        formdata.append("FormatType", "WordML");
        contenttype = "data:attachment/xml";
        filename = "Sample.xml";
    }
    else if(rdButtonPdf)
    {
        formdata.append("FormatType", "Pdf");
        contenttype = "data:attachment/pdf";
        filename = "Sample.pdf";
    }
    var req = new XMLHttpRequest();
    req.open("POST", window.baseurl + "api/DocIO/ApplyTextFormat", true);
    req.send(formdata);
    req.responseType = "blob";
    req.onload = function (event) {
    if (req.response != null && navigator.msSaveBlob)
        return navigator.msSaveBlob(new Blob([req.response], { type: contenttype}), filename);
    var a = document.createElement('a');
    var url = window.URL.createObjectURL(new Blob([req.response], {type: contenttype}));
    a.href = url;
    a.download = filename;
    document.body.appendChild(a);
    a.click();
    window.URL.revokeObjectURL(url);
    a.remove();
    };
});
</script>

{% endhighlight %}

>The above example will generate Word document or PDF.

## GetInvoiceTemplate

[POST] [/Api/DocIO/GetInvoiceTemplate](http://js.syncfusion.com/demos/ejServices/api/DocIO/GetInvoiceTemplate)

It is used to get invoice template Word document.

### Response information

Code: 200

Access-Control-Allow-Origin: *

Content-Type: data:attachment/doc

### Code example

{% highlight js %}

URL: http://js.syncfusion.com/demos/ejServices/api/DocIO/GetInvoiceTemplate

<script>
$('#viewtemplate').click(function () {
    var req = new XMLHttpRequest();
    req.open("POST", window.baseurl + "api/DocIO/GetInvoiceTemplate", true);
    req.responseType = "blob";
    req.send();
    req.onload = function (event) {
    if (req.response != null && navigator.msSaveBlob)
        return navigator.msSaveBlob(new Blob([req.response], { type: "data:attachment/doc"}), "SalesInvoiceTemplate.doc");
    var a = document.createElement('a');
    var url = window.URL.createObjectURL(new Blob([req.response], {type: "data:attachment/doc"}));
    a.href = url;
    a.download = "SalesInvoiceTemplate.doc";
    document.body.appendChild(a);
    a.click();
    window.URL.revokeObjectURL(url);
    a.remove();
    };
});
</script>

{% endhighlight %}

>The above example will generate invoice template Word document.

## GenerateInvoice

[POST] [Api/DocIO/GenerateInvoice](http://js.syncfusion.com/demos/ejServices/api/DocIO/GenerateInvoice)

It is used to generate sales invoice report using Mail merge functionality.

### URL parameters

| Parameter | Data Type | Description |
|---|---|---|
|FormatType|String|It contains format type to save.|

### Response information

Code: 200

Access-Control-Allow-Origin: *

Content-Type: data:attachment/filetype

### Code example

{% highlight js %}

URL: http://js.syncfusion.com/demos/ejServices/api/DocIO/GenerateInvoice

<script>
$('#generate').click(function () {
    var formdata = new FormData();
    var id = document.getElementById('order');
    formdata.append("Id", id.options[id.selectedIndex].value);
    var rdButtonDoc = document.getElementById("rdButtonDoc").checked;
    var rdButtonDocx = document.getElementById("rdButtonDocx").checked;
    var rdButtonWordML = document.getElementById("rdButtonWordML").checked;
    var rdButtonPdf = document.getElementById("rdButtonPdf").checked;
    var contenttype;
    var filename;
    if (rdButtonDoc) {
        formdata.append("FormatType", "WordDoc");
        contenttype = "data:attachment/doc";
        filename = "Sample.doc";
    }
    else if(rdButtonDocx)
    {
        formdata.append("FormatType", "WordDocx");
        contenttype = "data:attachment/docx";
        filename = "Sample.docx";
    }
    else if(rdButtonWordML)
    {
        formdata.append("FormatType", "WordML");
        contenttype = "data:attachment/xml";
        filename = "Sample.xml";
    }
    else
    {
        formdata.append("FormatType", "Pdf");
        contenttype = "data:attachment/pdf";
        filename = "Sample.pdf";
    }
    var req = new XMLHttpRequest();
    req.open("POST", window.baseurl + "api/DocIO/GenerateInvoice", true);
    req.responseType = "blob";
    req.send(formdata);
    req.onload = function (event) {
    if (req.response != null && navigator.msSaveBlob)
        return navigator.msSaveBlob(new Blob([req.response], { type: contenttype }), filename);
    var a = document.createElement('a');
    var url = window.URL.createObjectURL(new Blob([req.response], {type: contenttype}));
    a.href = url;
    a.download = filename;
    document.body.appendChild(a);
    a.click();
    window.URL.revokeObjectURL(url);
    a.remove();
    };
});
</script>

{% endhighlight %}

>The above example will generate Word document or PDF.

## GetMailmergeTemplate

[POST] [/Api/DocIO/GetMailmergeTemplate](http://js.syncfusion.com/demos/ejServices/api/DocIO/GetMailmergeTemplate)

It is used to get Mail merge template Word Document.

### URL parameters

| Parameter | Data Type | Description | 
|---|---|---|
|Template|String|It contains type of Template document.|

### Response information

Code: 200

Access-Control-Allow-Origin: *

Content-Type: data:attachment/doc

### Code example

{% highlight js %}

URL: http://js.syncfusion.com/demos/ejServices/api/DocIO/GetMailmergeTemplate

<script>
var formdata;
$('#viewtemplate').click(function () {
    formdata = new FormData();
    var rdButtonReport = document.getElementById("rdButtonReport").checked;
    var rdButtonLetter = document.getElementById("rdButtonLetter").checked;
    var template;
    if(rdButtonReport)
        template = "Report";
    else
        template = "Letter";
    formdata.append("Template", template);
    var req = new XMLHttpRequest();
    req.open("POST", window.baseurl + "api/DocIO/GetMailmergeTemplate", true);
    req.send(formdata);
    req.responseType = "blob";
    req.onload = function (event) {
    if (req.response != null && navigator.msSaveBlob)
        return navigator.msSaveBlob(new Blob([req.response], { type: "data:attachment/doc"}), "Template.doc");
    var a = document.createElement('a');
    var url = window.URL.createObjectURL(new Blob([req.response], {type: "data:attachment/doc"}));
    a.href = url;
    a.download = "Template.doc";
    document.body.appendChild(a);
    a.click();
    window.URL.revokeObjectURL(url);
    a.remove();
    };
});
</script>

{% endhighlight %}

>The above example will generate Mail merge template Word document.

## ExecuteNestedMailmerge

[[POST] /Api/DocIO/ExecuteNestedMailmerge](http://js.syncfusion.com/demos/ejServices/api/DocIO/ExecuteNestedMailmerge)

It is used to perform Mail merge for nested groups in Word Document.

### URL parameters

| Parameter | Data Type | Description | 
|---|---|---|
|Template|String|It contains type of Template document.|
|Data|String|It contatins type of Data.|
|FormatType|String|It contains format type to save.|

### Response information

Code: 200

Access-Control-Allow-Origin: *

Content-Type: data:attachment/doc

### Code example

{% highlight js %}

URL: http://js.syncfusion.com/demos/ejServices/api/DocIO/ExecuteNestedMailmerge

<script>
var formdata;
$('#generate').click(function () {
    formdata = new FormData();
    var rdButtonReport = document.getElementById("rdButtonReport").checked;
    var rdButtonLetter = document.getElementById("rdButtonLetter").checked;
    var template;
    if(rdButtonReport)
        template = "Report";
    else
        template = "Letter";
    formdata.append("Template", template);
    var rdImplicit = document.getElementById("rdImplicit").checked;
    var rdExplict = document.getElementById("rdExplict").checked;
    if(rdImplicit)
        formdata.append("Data", "Implicit");
    else if(rdExplict)
        formdata.append("Data", "Explict");
    var rdButtonDoc = document.getElementById("rdButtonDoc").checked;
    var rdButtonDocx = document.getElementById("rdButtonDocx").checked;
    var rdButtonWordML = document.getElementById("rdButtonWordML").checked;
    var rdButtonPdf = document.getElementById("rdButtonPdf").checked;
    var contenttype;
    var filename;
    if (rdButtonDoc) {
        formdata.append("FormatType", "WordDoc");
        contenttype = "data:attachment/doc";
        filename = "Sample.doc";
    }
    else if(rdButtonDocx)
    {
        formdata.append("FormatType", "WordDocx");
        contenttype = "data:attachment/docx";
        filename = "Sample.docx";
    }
    else if(rdButtonWordML)
    {
        formdata.append("FormatType", "WordML");
        contenttype = "data:attachment/xml";
        filename = "Sample.xml";
    }
    else
    {
        formdata.append("FormatType", "Pdf");
        contenttype = "data:attachment/pdf";
        filename = "Sample.pdf";
    }
    var req = new XMLHttpRequest();
    req.open("POST", window.baseurl + "api/DocIO/ExecuteNestedMailmerge", true);
    req.send(formdata);
    req.responseType = "blob";
    req.onload = function (event) {
    if (req.response != null && navigator.msSaveBlob)
        return navigator.msSaveBlob(new Blob([req.response], { type: contenttype}), filename);
    var a = document.createElement('a');
    var url = window.URL.createObjectURL(new Blob([req.response], {type: contenttype}));
    a.href = url;
    a.download = filename;
    document.body.appendChild(a);
    a.click();
    window.URL.revokeObjectURL(url);
    a.remove();
    };
});
</script>

{% endhighlight %}

>The above example will generate Word document or PDF.