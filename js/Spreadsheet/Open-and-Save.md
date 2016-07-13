---
title: Open and Save with Spreadsheet widget for Syncfusion Essential JS
description: How to perform Open and Save and configure its functionalities like server mapper, import URL etc.
platform: js
control: Spreadsheet
documentation: ug
---

# Open and Save

The native data format for spreadsheet is JSON. You can load and store JSON data with spreadsheet. In Spreadsheet we have saveAsJSON and loadFromJSON method which is used to save spreadsheet as JSON and same JSON used to render spreadsheet.
{% highlight javascript %}
function SaveAsJSON() {
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
window.xlData = xlObj.saveAsJSON();
}
function loadFromJSON() {
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.loadFromJSON(window.xlData);
}
{% endhighlight %}


When you open excel, the excel file need to be read and converted to client side spreadsheet model. The converted client side spreadsheet model is sent as JSON which is used to render spreadsheet. Similarly, when you save the spreadsheet, the client spreadsheet model is sent to the server as JSON for processing and saved. Server configuration is used for this process.

## Open 

The Spreadsheet can open excel documents as like excel application with its data, style, format. To enable open option in Spreadsheet set [`allowImport`](http://help.syncfusion.com/js/api/ejspreadsheet#members:allowimport "allowImport") option to true. Since Spreadsheet uses a server side helper to open document, set [`importMapper`](http://help.syncfusion.com/js/api/ejspreadsheet#members:importsettings-importmapper "importMapper") in importSettings to map server action.

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
$(function () {
$("#Spreadsheet").ejSpreadsheet({
allowImport: true,
importSettings: {
importMapper: "http://js.syncfusion.com/demos/ejservices/api/JSXLExport/Import"
}
});
});
</script>
{% endhighlight %}

Following file types can be opened in Spreadsheet

* XLS

* XLSX

* CSV


[`Click`](http://js.syncfusion.com/demos/web/#!/azure/spreadsheet/importexport "Click") here to view online demo sample.
You can open excel documents in following ways

1. Initial settings

2. Methods

3. User Interface


### Initial settings

The spreadsheet can load excel documents initially. The document can be specified either from client side or in server side.
To load excel documents initially from client side, set [`importUrl`](http://help.syncfusion.com/js/api/ejspreadsheet#members:importsettings-importurl "importUrl") in importSettings. The code snippets for document initial load on client side are as follows,

{% highlight javascript %}

$("#Spreadsheet").ejSpreadsheet({
importSettings: {
importMapper: "http://js.syncfusion.com/demos/ejservices/api/JSXLExport/Import",
importUrl: "http://mvc.syncfusion.com/Spreadsheet/LargeData.xlsx"
}         
});

{% endhighlight %}

To load excel documents initially from server side, set [`importOnLoad`](http://help.syncfusion.com/js/api/ejspreadsheet#members:importonload "importOnLoad") as true and assign document stream or URL in the server. The code snippets for document initial load from server side are as follows,
{% highlight html %}
<div id="Spreadsheet"></div>
<script>
$(function () {
$("#Spreadsheet").ejSpreadsheet({
importOnLoad: true,
importSettings:
{
importMapper: "http://js.syncfusion.com/demos/ejservices/api/JSXLExport/Import",
}           
});
});    
</script>


{% endhighlight %}

{% highlight c# %}
public class JSXLExportController : ApiController
{
[OperationContract]
[WebGet(BodyStyle = WebMessageBodyStyle.Bare)]
[System.Web.Http.ActionName("Import")]
[AcceptVerbs("Post")]
public HttpResponseMessage Import()
{
ImportRequest importRequest = new ImportRequest();
importRequest.Url = "http://mvc.syncfusion.com/Spreadsheet/LargeData.xlsx";           
string str = Spreadsheet.Open(importRequest);
return new HttpResponseMessage() { Content = new StringContent(str, Encoding.UTF8, "text/plain") };
}
}


{% endhighlight %}

![](Open-and-Save_images/Open-and-Save_img1.png)

### Methods

To open an excel document, import method should be called with import options as a parameter. The spreadsheet can open excel document as a stream. The document stream was either from the client side or it can be specified in server side.
The code snippets to open excel document as a stream from client side are as follows,
{% highlight javascript %}
function fileOpen(args) {
var xlObj = $("#Spreadsheet").data("ejSpreadsheet"),
stream = args.files[0]; // file stream from ejUploadbox
xlObj["import"]({ file: stream });
}


{% endhighlight %}

The Code snippets to specify excel document as stream in server side are as follows,
{% highlight c# %}
[OperationContract]
[WebGet(BodyStyle = WebMessageBodyStyle.Bare)]
[System.Web.Http.ActionName("Import")]
[AcceptVerbs("Post")]
public HttpResponseMessage Import()
{            
ImportRequest importRequest = new ImportRequest();
importRequest.FileStream = getFileStream(); // assign file stream            
string str = Spreadsheet.Open(importRequest);
return new HttpResponseMessage() { Content = new StringContent(str, Encoding.UTF8, "text/plain") };
}


{% endhighlight %}

Spreadsheet can open excel document from specified URL. The URL can be specified either from client side or in server side.
The code snippets to open excel document as URL from client side are as follows,
{% highlight javascript %}
function fileOpen() {
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj["import"]({Url: "http://mvc.syncfusion.com/Spreadsheet/LargeData.xlsx"});
}


{% endhighlight %}

The Code snippets to specify excel document as URL in server side are as follows,
{% highlight c# %}
[OperationContract]
[WebGet(BodyStyle = WebMessageBodyStyle.Bare)]
[System.Web.Http.ActionName("Import")]
[AcceptVerbs("Post")]
public HttpResponseMessage Import()
{
ImportRequest importRequest = new ImportRequest();
importRequest.Url = "http://mvc.syncfusion.com/Spreadsheet/LargeData.xlsx";
string str = Spreadsheet.Open(importRequest);
return new HttpResponseMessage() { Content = new StringContent(str, Encoding.UTF8, "text/plain") };
}


{% endhighlight %}

### User Interface

You can dynamically open excel document by clicking the file menu in ribbon and choose Open to upload excel file.

## Save

The Spreadsheet can save its data, style, format into an excel file. To enable save option in Spreadsheet set [`allowExporting`](http://help.syncfusion.com/js/api/ejspreadsheet#members:exportsettings-allowexporting "allowExporting") option in exportSettings to true. Since Spreadsheet uses server side helper to save documents set [`excelUrl`](http://help.syncfusion.com/js/api/ejspreadsheet#members:exportsettings-excelurl "excelUrl") in exportSettings option.
{% highlight html %}
<div id="Spreadsheet"></div>
<script>
$(function () {
$("#Spreadsheet").ejSpreadsheet({
exportSettings:
{
allowExporting: true,
excelUrl: "http://js.syncfusion.com/demos/ejservices/api/JSXLExport/ExportToExcel",
}           
});
});
</script>


{% endhighlight %}

You can save Spreadsheet contents with following file types

* XLS

* XLSX

* CSV

* PDF


[`Click`](http://js.syncfusion.com/demos/web/#!/azure/spreadsheet/importexport "Click") here to view online demo sample.
You can save excel documents in following ways

1. Methods

2. User Interface

### Methods


To save Spreadsheet document as excel file, export method should be called with file type as parameter. The code snippets to save Spreadsheet document are as follows,
{% highlight javascript %}
function saveAsFile() {
var xlObj = $("#spreadsheet").data("ejSpreadsheet");
xlObj.XLExport["export"](ej.Spreadsheet.exportType.Excel);
}


{% endhighlight %}

### User Interface

You can dynamically save spreadsheet by clicking file menu in ribbon and choose SaveAs option.

## Server Configuration 

The import from excel and export to excel is processed in server-side only, through Syncfusion.EJ.Export helper functions provided for .NET Framework. So, to use importing and exporting in your projects, it is required to create a server with any of the following web services.

* WebAPI

* WCF Service

* ASP.NET MVC Controller Action


Following code snippet demonstrate open option using WebAPI controller.
{% highlight c# %}
public class JSXLExportController : ApiController
{
[OperationContract]
[WebGet(BodyStyle = WebMessageBodyStyle.Bare)]
[System.Web.Http.ActionName("Import")]
[AcceptVerbs("Post")]
public HttpResponseMessage Import()
{
ImportRequest importRequest = new ImportRequest();
importRequest.FileStream = HttpContext.Current.Request.Files[0].InputStream;            
string str = Spreadsheet.Open(importRequest);
return new HttpResponseMessage() { Content = new StringContent(str, Encoding.UTF8, "text/plain") };
}
[System.Web.Http.ActionName("ExportToExcel")]
[AcceptVerbs("POST")]
public void ExportToExcel()
{
string sheetModel = HttpContext.Current.Request.Params["sheetModel"], sheetData = HttpContext.Current.Request.Params["sheetData"];
Spreadsheet.Save(sheetModel, sheetData, "sample", ExportFormat.XLSX, ExcelVersion.Excel2013);
}
}


{% endhighlight %}

### Server dependencies

Import and Export Helper functions are available in the Assembly Syncfusion.EJ.Export, which is available in Essential Studio and Essential JavaScript builds. The full list of assemblies needed for Spreadsheet import and export is follows.

1. Syncfusion.EJ

2. Syncfusion.EJ.Export

3. Syncfusion.Linq.Base

4. Syncfusion.Compression.Base

5. Syncfusion.DocIO.Base

6. Syncfusion.XlsIO.Base

7. Syncfusion.PDF.Base



N> 1. The above mentioned assemblies will be available in below location after Essential Studio build installation.
N> 2. C:\Program Files (x86)\Syncfusion\Essential Studio\x.x.x.x\precompiledassemblies\x.x.x.x\y.y.
N> 3. x.x.x.x defines build version of Essential Studio and y.y defines .NET Framework version.
