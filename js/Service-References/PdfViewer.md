---
title: Service reference for ejPdfViewer widget
description: Services used in Essential JavaScript PDF Viewer.
platform: js
control: ejPdfViewer
documentation: api
keywords: ejPdfViewer, Services, Essential JS PDF Viewer, PDF Viewer
---
### URL: http://js.syncfusion.com/demos/ejservices/api/PdfViewer/PostViewerAction 
### Parameter
<table>
<thead>
<tr>
<th>
{{'**Parameter name **'| markdownify }}
</th>
<th>
{{'**Datatype**'| markdownify }}
</th>
<th>
{{'**Description**'| markdownify }}
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
data
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format
</td>
</tr>
<tr>
<td class="parameter name">
viewerAction
</td>
<td class="datatype">
String
</td>
<td class="description">
Specified the action of the ajax request
</td>
</tr>
<tr>
<td class="parameter name">
controlId
</td>
<td class="datatype">
String 
</td>
<td class="description">
Control ID of the widget 
</td>
</tr>
<tr>
<td class="parameter name">
pageindex
</td>
<td class="datatype">
String
</td>
<td class="description">
Current page index of the PDF document which display the content in PDF Viewer
</td>
</tr>
<tr>
<td class="parameter name">
isInitialLoading
</td>
<td class="datatype">
String
</td>
<td class="description">
Specify the ajax request whether the request is initial loading or consecutive loading.  
</td>
</tr>
</tbody>
</table>
### Request
<table>
<thead>
<tr>
<th>
$.ajax({
    type: 'POST',
    contentType: 'application/json: charset=utf-8',
    url: 'http://js.syncfusion.com/demos/ejservices/api/PdfViewer/PostViewerAction',
    dataType: "json",
    data: JSON.stringify([{
        "viewerAction": "GetPageModel",
        "controlId": this._id,
        "isInitialLoading": "true"
        "pageindex": "1"
    }])
});
</th>
</tr>
</thead>
<tbody>
</tbody>
</table>
### Response
#### Code:  200
#### Content-Type:”application/json:charset=utf-8”;
#### Response Text:
<table>
<thead>
<tr>
<th>
imagestream
</th>
<th>
Current page content stream 
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="imagestream">
pagesize
</td>
<td class="current page content stream">
Collection of page size for total page
</td>
</tr>
<tr>
<td class="imagestream">
currentpage
</td>
<td class="current page content stream">
Current page number
</td>
</tr>
<tr>
<td class="imagestream">
filename 
</td>
<td class="current page content stream">
Current file name
</td>
</tr>
<tr>
<td class="imagestream">
pagecount
</td>
<td class="current page content stream">
Total page count of the PDF document
</td>
</tr>
<tr>
<td class="imagestream">
pageheight 
</td>
<td class="current page content stream">
Current page height
</td>
</tr>
<tr>
<td class="imagestream">
pagewidth
</td>
<td class="current page content stream">
Current page width
</td>
</tr>
<tr>
<td class="imagestream">
linkannotation
</td>
<td class="current page content stream">
Collection of link annotation in the PDF document
</td>
</tr>
<tr>
<td class="imagestream">
annotpagenum
</td>
<td class="current page content stream">
Collection of page number which contain annotation
</td>
</tr>
</tbody>
</table>
### URL: http://js.syncfusion.com/demos/ejservices/api/PdfViewer/FileUploadPostAction  
### Parameter
<table>
<thead>
<tr>
<th>
{{'**Parameter name **'| markdownify }}
</th>
<th>
{{'**Datatype**'| markdownify }}
</th>
<th>
{{'**Description**'| markdownify }}
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
data
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format
</td>
</tr>
<tr>
<td class="parameter name">
viewerAction
</td>
<td class="datatype">
String
</td>
<td class="description">
Specified the action of the ajax request
</td>
</tr>
<tr>
<td class="parameter name">
controlId
</td>
<td class="datatype">
String 
</td>
<td class="description">
Control ID of the widget 
</td>
</tr>
<tr>
<td class="parameter name">
pageindex
</td>
<td class="datatype">
String
</td>
<td class="description">
Current page index of the PDF document which display the content in PDF Viewer
</td>
</tr>
<tr>
<td class="parameter name">
isInitialLoading
</td>
<td class="datatype">
String
</td>
<td class="description">
Specify the ajax request whether the request is initial loading or consecutive loading.  
</td>
</tr>
<tr>
<td class="parameter name">
newFileName
</td>
<td class="datatype">
String
</td>
<td class="description">
New file name to be loaded into the PDF Viewer
</td>
</tr>
</tbody>
</table>
### Request
<table>
<thead>
<tr>
<th>
$.ajax({
    type: 'POST',
    contentType: 'application/json: charset=utf-8',
    url: 'http://js.syncfusion.com/demos/ejservices/api/PdfViewer/ FileUploadPostAction',
    dataType: "json",
    data: JSON.stringify([{
        "viewerAction": "GetPageModel",
        "controlId": this._id,
        "isInitialLoading": "true"
        "pageindex": "1"
    }])
});
</th>
</tr>
</thead>
<tbody>
</tbody>
</table>
### Response
#### Code:  200
#### Content-Type:”application/json:charset=utf-8”;
#### Response Text:
<table>
<thead>
<tr>
<th>
imagestream
</th>
<th>
Current page content stream 
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="imagestream">
pagesize
</td>
<td class="current page content stream">
Collection of page size for total page
</td>
</tr>
<tr>
<td class="imagestream">
currentpage
</td>
<td class="current page content stream">
Current page number
</td>
</tr>
<tr>
<td class="imagestream">
filename 
</td>
<td class="current page content stream">
Current file name
</td>
</tr>
<tr>
<td class="imagestream">
pagecount
</td>
<td class="current page content stream">
Total page count of the PDF document
</td>
</tr>
<tr>
<td class="imagestream">
pageheight 
</td>
<td class="current page content stream">
Current page height
</td>
</tr>
<tr>
<td class="imagestream">
pagewidth
</td>
<td class="current page content stream">
Current page width
</td>
</tr>
<tr>
<td class="imagestream">
linkannotation
</td>
<td class="current page content stream">
Collection of link annotation in the PDF document
</td>
</tr>
<tr>
<td class="imagestream">
annotpagenum
</td>
<td class="current page content stream">
Collection of page number which contain annotation
</td>
</tr>
</tbody>
</table>
### URL: http://js.syncfusion.com/demos/ejservices/api/PdfViewer/DocumentDownloadAction 
### Parameter
<table>
<thead>
<tr>
<th>
{{'**Parameter name **'| markdownify }}
</th>
<th>
{{'**Datatype**'| markdownify }}
</th>
<th>
{{'**Description**'| markdownify }}
</th>
</tr>
</thead>
<tbody>
<tr>
<td class="parameter name">
data
</td>
<td class="datatype">
JSON
</td>
<td class="description">
Input data in the JSON format
</td>
</tr>
<tr>
<td class="parameter name">
Download
</td>
<td class="datatype">
String
</td>
<td class="description">
PDF document name to be download
</td>
</tr>
</tbody>
</table>
### Request
<table>
<thead>
<tr>
<th>
$.ajax({
    type: 'POST',
    contentType: 'application/json: charset=utf-8',
    url: 'http://js.syncfusion.com/demos/ejservices/api/PdfViewer/ DocumentDownloadAction',
    dataType: "json",
    data: JSON.stringify([{
        "DocumentName: this.fileName
    }])
});
</th>
</tr>
</thead>
<tbody>
</tbody>
</table>
### Response
#### Code:  200
#### Content-Type:”application/json:charset=utf-8”;
#### Response Text:
<table>
<thead>
<tr>
<th>
DocumentStream
</th>
<th>
PDF document stream for downloading 
</th>
</tr>
</thead>
<tbody>
</tbody>
</table>
### PdfViewerHelper
PdfViewerHelper class used to process the PDF document in server side.
### Methods:
### Load(string filename)
Loads a PDF document in the PDF viewer from the specified file path.
Code snippet:
PdfViewerHelper helper = new PdfViewerHelper();
helper.Load(filepath/filename.pdf);
### Load(string filename, string password)
Loads the encrypted PDF document.
Code snippet:
PdfViewerHelper helper = new PdfViewerHelper();
helper.Load(filepath/filename.pdf, password);
### Load(Stream documentStream)
Loads the PDF document from the specified stream.
Code snippet:
PdfViewerHelper helper = new PdfViewerHelper();
helper.Load(documentStream);
### Load(Stream documentStream, string password)
Loads the encrypted PDF document from the specified stream.
Code snippet:
PdfViewerHelper helper = new PdfViewerHelper();
helper.Load(documentStream,password);
### Load(PdfLoadedDocument ldoc)
Loads the PDF document from the PdfLoadedDocument object.
Code snippet:
PdfViewerHelper helper = new PdfViewerHelper();
helper.Load(pdfloadeddocument);
### Load(byte[] byteArray)
Loads the PDF document from the byte array.
Code snippet:
PdfViewerHelper helper = new PdfViewerHelper();
helper.Load(byteArray);
### Load(byte[] byteArray, string password)
Loads the encrypted PDF document from the byte array.
Code snippet:
PdfViewerHelper helper = new PdfViewerHelper();
helper.Load(byteArray,password);
### ProcessPdf(Dictionary&lt;string,string&gt; jsonResult)
Process the PDF document and convert them to json data.
Code snippet:
PdfViewerHelper helper = new PdfViewerHelper();
helper.Load(filepath/filename.pdf);
helper.ProcessPdf(jsonResult)
