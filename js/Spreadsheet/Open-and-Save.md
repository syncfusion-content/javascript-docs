---
title: Open and Save in JavaScript Spreadsheet widget | Syncfusion
description: You can learn here about open and save support in Syncfusion JavaScript Spreadsheet control and more details.
platform: js
control: Spreadsheet
documentation: ug
api: /api/js/ejspreadsheet
---

# Open and Save in JavaScript Spreadsheet

The native data format for Spreadsheet is JSON. You can load and store JSON data with Spreadsheet. In Spreadsheet we have [`saveAsJSON`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:saveasjson "saveAsJSON") and [`loadFromJSON`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:loadfromjson "loadFromJSON") method which is used to save Spreadsheet as JSON and same JSON used to render Spreadsheet.

{% highlight javascript %}

function SaveAsJSON() {
    var excelObj = $("#Spreadsheet").data("ejSpreadsheet");
    window.excelData = excelObj.saveAsJSON();
}

function loadFromJSON() {
    var excelObj = $("#Spreadsheet").data("ejSpreadsheet");
    excelObj.loadFromJSON(window.excelData);
}

{% endhighlight %}


When you open an excel file, it needs to be read and converted to client side Spreadsheet model. The converted client side Spreadsheet model is sent as JSON which is used to render Spreadsheet. Similarly, when you save the Spreadsheet, the client Spreadsheet model is sent to the server as JSON for processing and saved. [`Server configuration`](https://help.syncfusion.com/js/spreadsheet/open-and-save#server-configuration "Server configuration") is used for this process.

## Open 

The Spreadsheet can open excel documents as like excel application with its data, style, format. To enable open option in Spreadsheet set [`allowImport`](https://help.syncfusion.com/api/js/ejspreadsheet#members:allowimport "allowImport") option as `true`. Since Spreadsheet uses a server side helper to open document, set [`importMapper`](https://help.syncfusion.com/api/js/ejspreadsheet#members:importsettings-importmapper "importMapper") in [`importSettings`](https://help.syncfusion.com/api/js/ejspreadsheet#members:importsettings "importSettings") to map server action.

The method [`blankWorkbook`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:blankworkbook "blankworkbook") is used to create the new workbook in Spreadsheet.

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$(function () {
    $("#Spreadsheet").ejSpreadsheet({
        allowImport: true,
        importSettings: {
            importMapper: "http://js.syncfusion.com/demos/ejservices/api/Spreadsheet/Import"
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

* Using [`getExportProps`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlexport-getexportprops "getExportProps") method to get the export properties in the Spreadsheet.
You can open excel documents in following ways,

1. Initial settings
2. Methods
3. User Interface

### Initial settings

The Spreadsheet can load excel documents initially. The document can be specified either from client side or in server side.
To load excel documents initially from client side, set [`importUrl`](https://help.syncfusion.com/api/js/ejspreadsheet#members:importsettings-importurl "importUrl") as excel file URL in [`importSettings`](https://help.syncfusion.com/api/js/ejspreadsheet#members:importsettings "importSettings"). The code snippets for document initial load on client side are as follows,

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$(function () {
    $("#Spreadsheet").ejSpreadsheet({
        allowImport: true,
        importSettings: {
            importMapper: "http://js.syncfusion.com/demos/ejservices/api/Spreadsheet/Import",
            importUrl: "http://mvc.syncfusion.com/Spreadsheet/LargeData.xlsx"
        }
    });
});
</script>

{% endhighlight %}

To load excel documents initially from server side, set [`importOnLoad`](https://help.syncfusion.com/api/js/ejspreadsheet#members:importsettings-importonload "importOnLoad") as `true` and assign document stream or URL in the server, and also you can define password while importing in the spreadsheet by using [`password`](https://help.syncfusion.com/api/js/ejspreadsheet#members:importsettings-password "password") API.
The code snippets for document initial load from server side are as follows,

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$(function () {
    $("#Spreadsheet").ejSpreadsheet({        
        importSettings: {
            importOnLoad: true,
            password: "Spreadsheet" //It opens the excel file using this password.
            importMapper: "http://js.syncfusion.com/demos/ejservices/api/Spreadsheet/Import"
        }           
    });
});    
</script>

{% endhighlight %}

{% highlight c# %}

public class SpreadSheetController : ApiController
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

![open and save](Open-and-Save_images/Open-and-Save_img1.png)

### Methods

To open an excel document, [`import`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:import "import") method should be called with import options as a parameter. The Spreadsheet can open excel document as a stream or file URL.

#### Stream
Spreadsheet can open excel document as a stream and the document stream was either from the client side or it can be specified in server side. The code snippets to open excel document as a stream from client side are as follows,

{% highlight javascript %}

function fileOpen(args) {
    var excelObj = $("#Spreadsheet").data("ejSpreadsheet"),
    stream = args.files[0]; // file stream from ejUploadbox
    excelObj["import"]({ file: stream });
}

{% endhighlight %}

The code snippets to specify excel document as stream in server side are as follows,

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

#### File URL
Spreadsheet can open excel document from specified file URL. The file URL can be specified either from client side or in server side.
The code snippets to open excel document as URL from client side are as follows,

{% highlight javascript %}

function fileOpen() {
    var excelObj = $("#Spreadsheet").data("ejSpreadsheet");
    excelObj["import"]({Url: "http://mvc.syncfusion.com/Spreadsheet/LargeData.xlsx"});
}

{% endhighlight %}

The code snippets to specify excel document as URL in server side are as follows,

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

N> [`isImport`](https://help.syncfusion.com/api/js/ejspreadsheet#members:isImport "isImport") API gets a value, that indicates whether importing or not while loading the sheets in spreadsheet. 

## Save

The Spreadsheet can save its data, style, format into an excel file. To enable save option in Spreadsheet set [`allowExporting`](https://help.syncfusion.com/api/js/ejspreadsheet#members:exportsettings-allowexporting "allowExporting") option in [`exportSettings`](https://help.syncfusion.com/api/js/ejspreadsheet#members:exportsettings "exportSettings") as `true`. Since Spreadsheet uses server side helper to save documents set [`excelUrl`](https://help.syncfusion.com/api/js/ejspreadsheet#members:exportsettings-excelurl "excelUrl"),[`csvUrl`](https://help.syncfusion.com/api/js/ejspreadsheet#members:exportsettings-csvurl "csvUrl"),[`pdfUrl`](https://help.syncfusion.com/api/js/ejspreadsheet#members:exportsettings-pdfurl "pdfUrl") in [`exportSettings`](https://help.syncfusion.com/api/js/ejspreadsheet#members:exportsettings "exportSettings") option and also you can define password while exporting the spreadsheet by using [`password`](https://help.syncfusion.com/api/js/ejspreadsheet#members:exportsettings-password "password") API.

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$(function () {
    $("#Spreadsheet").ejSpreadsheet({
        exportSettings:
        {
            allowExporting: true,
            excelUrl: "http://js.syncfusion.com/demos/ejservices/api/Spreadsheet/ExcelExport",
            csvUrl: "http://js.syncfusion.com/demos/ejservices/api/Spreadsheet/CsvExport",
            pdfUrl: "http://js.syncfusion.com/demos/ejservices/api/Spreadsheet/PdfExport"
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

To save Spreadsheet document as excel file, [`export`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlexport-export "export") method should be called with file type as parameter. The code snippets to save Spreadsheet document are as follows,

{% highlight javascript %}

function saveAsFile() {
    var excelObj = $("#spreadsheet").data("ejSpreadsheet");
    excelObj.XLExport["export"](ej.Spreadsheet.exportType.Excel);
}

{% endhighlight %}

N> Import / Export operations can be processed in server side only.

### User Interface

You can dynamically save spreadsheet by clicking file menu in ribbon and choose SaveAs option.

## Server Configuration 

The import from excel and export to excel is processed in server-side only, through `Syncfusion.EJ.Export` helper functions provided for .NET Framework. So, to use importing and exporting in your projects, it is required to create a server with any of the following web services.

* WebAPI
* WCF Service
* ASP.NET MVC Controller Action

Following code snippets demonstrate open option using WebAPI controller.

{% highlight c# %}

public class SpreadSheetController : ApiController
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

    [AcceptVerbs("POST")]
    public void ExcelExport()
    {
        string sheetModel = HttpContext.Current.Request.Params["sheetModel"], sheetData = HttpContext.Current.Request.Params["sheetData"], password = HttpContext.Current.Request.Params["password"], fileName = HttpContext.Current.Request.Params["fileName"];
            if (!string.IsNullOrEmpty(password))
                Spreadsheet.Save(sheetModel, sheetData, fileName, ExportFormat.XLSX, ExcelVersion.Excel2013, password);
            else
                Spreadsheet.Save(sheetModel, sheetData, fileName, ExportFormat.XLSX, ExcelVersion.Excel2013);
    }

    [AcceptVerbs("Post")]
    public void CsvExport()
    {
        string sheetModel = HttpContext.Current.Request.Params["sheetModel"], sheetData = HttpContext.Current.Request.Params["sheetData"], fileName = HttpContext.Current.Request.Params["fileName"];
        Spreadsheet.Save(sheetModel, sheetData, fileName, ExportFormat.CSV);
    }

    [AcceptVerbs("Post")]
    public void PdfExport()
    {
        string sheetModel = HttpContext.Current.Request.Params["sheetModel"], sheetData = HttpContext.Current.Request.Params["sheetData"], fileName = HttpContext.Current.Request.Params["fileName"];
        Spreadsheet.Save(sheetModel, sheetData, fileName, ExportFormat.PDF);
    }
}

{% endhighlight %}

N> To export as `Stream` skip file name parameter in `Save` method. For more details refer below code snippets,<br>
   Stream stream = Spreadsheet.Save(sheetModel, sheetData, ExportFormat.XLSX, ExcelVersion.Excel2013);

### Server dependencies

Import and Export Helper functions are available in the assembly `Syncfusion.EJ.Export`, which is available in Essential Studio and Essential JavaScript builds. The full list of assemblies needed for Spreadsheet import and export are as follows.

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
