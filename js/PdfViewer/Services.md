---
layout: post
title: Service reference for ejPdfViewer widget
description: Services used in Essential JavaScript PDF Viewer.
platform: js
control: ejPdfViewer
documentation: api
keywords: ejPdfViewer, Services, Essential JS PDF Viewer, PDF Viewer
---
## PDF Viewer services
PDF Viewer services loads the PDF document on server side and parse the PDF document content, then return the necessary details for rendering PDF document content to the client side as JSON data.

## PostViewerAction

### Description

PostViewerAction loads the PDF document into the PDF Viewer control and parse the PDF document content on the server side, then return the necessary details for rendering PDF document content to the client side as JSON data.

### URL

[http://js.syncfusion.com/ejservices/api/PdfViewer/PostViewerAction](http://js.syncfusion.com/ejservices/api/PdfViewer/PostViewerAction) 

### Parameter

<table>
<thead>
<tr>
<th>
{{'Parameter name '| markdownify }}
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
Specified the action of the AJAX request
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
Specify the AJAX request whether the request is initial loading or consecutive loading.  
</td>
</tr>
</tbody>
</table>

### Request

{% highlight javascript %}
$.ajax({
    type: 'POST',
    contentType: 'application/json; charset=utf-8',
    url: 'http://js.syncfusion.com/ejservices/api/PdfViewer/PostViewerAction',
    dataType: "json",
    data: JSON.stringify([{
        "viewerAction": "GetPageModel",
        "controlId": this._id,
        "isInitialLoading": "true",
        "pageindex": "1"
    }])
});
{% endhighlight %}

#### PostViewerAction invoked in C# 

{% highlight c# %}

        [System.Web.Http.HttpPost]
        [System.Web.Http.ActionName("PostViewerAction")]
		public object PostViewerAction(Dictionary<string, string> jsonResult)
        {
            PdfViewerHelper helper = new PdfViewerHelper();
            //load the multiple document from client side 
            if (jsonResult.ContainsKey("newFileName"))
            {
                var name = jsonResult["newFileName"];
                var pdfName = name.ToString() + ".pdf";
                helper.Load(Helper.GetFilePath("" + pdfName));
            }
            else
            {
                if (jsonResult.ContainsKey("isInitialLoading"))
                    helper.Load(Helper.GetFilePath(documentname));
            }
            return JsonConvert.SerializeObject(helper.ProcessPdf(jsonResult));
        }

{% endhighlight %}

### Response

#### Code:  200

#### Content-Type:”application/json;charset=utf-8”;

#### Response Text:

<table>
<tr>
<td>
imagestream
</td>
<td>
Current page content stream 
</td>
</tr>
<tr>
<td>
pagesize
</td>
<td>
Collection of page size for total page
</td>
</tr>
<tr>
<td>
currentpage
</td>
<td>
Current page number
</td>
</tr>
<tr>
<td>
filename 
</td>
<td>
Current file name
</td>
</tr>
<tr>
<td>
pagecount
</td>
<td>
Total page count of the PDF document
</td>
</tr>
<tr>
<td>
pageheight 
</td>
<td>
Current page height
</td>
</tr>
<tr>
<td>
pagewidth
</td>
<td>
Current page width
</td>
</tr>
<tr>
<td>
linkannotation
</td>
<td>
Collection of link annotation in the PDF document
</td>
</tr>
<tr>
<td>
annotpagenum
</td>
<td>
Collection of page number which contain annotation
</td>
</tr>
</table>

## FileUploadPostAction

### Description

FileUploadPostAction loads the PDF document using fileuploader into the PDF Viewer control.

### URL

[http://js.syncfusion.com/ejservices/api/PdfViewer/FileUploadPostAction](http://js.syncfusion.com/ejservices/api/PdfViewer/FileUploadPostAction)  

### Parameter

<table>
<thead>
<tr>
<th>
{{'Parameter name'| markdownify }}
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
Specified the action of the AJAX request
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
Specify the AJAX request whether the request is initial loading or consecutive loading.  
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

{% highlight javascript %}
$.ajax({
    type: 'POST',
    contentType: 'application/json; charset=utf-8',
    url: 'http://js.syncfusion.com/ejservices/api/PdfViewer/FileUploadPostAction',
    dataType: "json",
    data: JSON.stringify([{
        "viewerAction": "GetPageModel",
        "controlId": this._id,
        "isInitialLoading": "true",
        "pageindex": "1"
    }])
});
{% endhighlight %}

#### FileUploadPostAction invoked in C# 

{% highlight c# %}

        [System.Web.Http.HttpPost]
        [System.Web.Http.ActionName("FileUploadPostAction")]
        public object FileUploadPostAction(Dictionary<string, string> jsonResult)
        {
            PdfViewerHelper helper = new PdfViewerHelper();
            //load the PDF document from client side by using upload button 
            if (jsonResult.ContainsKey("uploadedFile"))
            {
                var fileurl = jsonResult["uploadedFile"];
                byte[] byteArray = Convert.FromBase64String(fileurl);
                MemoryStream stream = new MemoryStream(byteArray);
                helper.Load(stream);
            }
            return JsonConvert.SerializeObject(helper.ProcessPdf(jsonResult));
        }      

{% endhighlight %}

### Response

#### Code:  200

#### Content-Type:”application/json;charset=utf-8”;

#### Response Text:

<table>
<tr>
<td>
imagestream
</td>
<td>
Current page content stream 
</td>
</tr>
<tr>
<td>
pagesize
</td>
<td>
Collection of page size for total page
</td>
</tr>
<tr>
<td>
currentpage
</td>
<td>
Current page number
</td>
</tr>
<tr>
<td>
filename 
</td>
<td>
Current file name
</td>
</tr>
<tr>
<td>
pagecount
</td>
<td>
Total page count of the PDF document
</td>
</tr>
<tr>
<td>
pageheight 
</td>
<td>
Current page height
</td>
</tr>
<tr>
<td>
pagewidth
</td>
<td>
Current page width
</td>
</tr>
<tr>
<td>
linkannotation
</td>
<td>
Collection of link annotation in the PDF document
</td>
</tr>
<tr>
<td>
annotpagenum
</td>
<td>
Collection of page number which contain annotation
</td>
</tr>
</table>

## DocumentDownloadAction

### Description

DocumentDownloadAction return the PDF document being displaying in the PDF Viewer control as base64 string to the client side for downloading the same.

### URL

[http://js.syncfusion.com/ejservices/api/PdfViewer/DocumentDownloadAction](http://js.syncfusion.com/ejservices/api/PdfViewer/DocumentDownloadAction) 

### Parameter

<table>
<thead>
<tr>
<th>
{{'Parameter name'| markdownify }}
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

{% highlight javascript %}
$.ajax({
    type: 'POST',
    contentType: 'application/json; charset=utf-8',
    url: 'http://js.syncfusion.com/ejservices/api/PdfViewer/DocumentDownloadAction',
    dataType: "json",
    data: JSON.stringify([{
        "DocumentName": this.fileName
    }])
});
{% endhighlight %}

#### DocumentDownloadAction invoked in C# 

{% highlight c# %}

     	[System.Web.Http.HttpPost]
        [System.Web.Http.ActionName("DocumentDownloadAction")]
        public object DocumentDownloadAction(Dictionary<string, string> jsonResult)
        {
            PdfViewerHelper helper = new PdfViewerHelper();
            return new { DocumentStream = Convert.ToBase64String(helper.DocumentStream.ToArray()) };
        }		

{% endhighlight %}

### Response

#### Code:  200

#### Content-Type:”application/json;charset=utf-8”;

#### Response Text:

<table>
<tr>
<td>
DocumentStream
</td>
<td>
PDF document stream for downloading 
</td>
</tr>
</table>