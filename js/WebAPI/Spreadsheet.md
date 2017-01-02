---
layout: post
title: webAPI reference for ejSpreadsheet
description: webAPI reference for ejSpreadsheet
documentation: ug
platform: js
keywords: Spreadsheet,ejSpreadsheet , syncfusion, ejSpreadsheet webapi
---

## ExcelExport

 [POST] [/Api/Spreadsheet/ExcelExport](http://js.syncfusion.com/demos/ejServices/api/Spreadsheet/ExcelExport)

It is used to export the Spreadsheet data as an Excel document.

### URL parameters

|  Parameter |  Description | 
|---|---|
|sheetModel|It contains the model of the Spreadsheet.|
|sheetData|DataURL of the Spreadsheet to be exported.|
|password|It contains the password information.|

### Response information 

Code: 200

Content-Type: application/octet-stream	

### Code example 

{% highlight js %}


{% endhighlight %}

{% highlight c# %}

public void ExcelExport()
{
string sheetModel = HttpContext.Current.Request.Params["sheetModel"], sheetData = HttpContext.Current.Request.Params["sheetData"], password = HttpContext.Current.Request.Params["password"];
if (!string.IsNullOrEmpty(password))
	Spreadsheet.Save(sheetModel, sheetData, "sample", ExportFormat.XLSX, ExcelVersion.Excel2013, password);
else
	Spreadsheet.Save(sheetModel, sheetData, "sample", ExportFormat.XLSX, ExcelVersion.Excel2013);
}

{% endhighlight %}

>The above example will export the Spreadsheet as an Excel file.

## CsvExport

 [POST] [/Api/Spreadsheet/CsvExport](http://js.syncfusion.com/demos/ejServices/api/Spreadsheet/CsvExport)

It is used to export the Spreadsheet data to CSV file.

### URL parameters

|  Parameter |  Description | 
|---|---|
|sheetModel|It contains the model of the Spreadsheet.|
|sheetData|DataURL of the Spreadsheet to be exported.|

### Response information 

Code: 200

Content-Type: application/octet-stream	

### Code example 

{% highlight js %}



{% endhighlight %}

{% highlight c# %}

public void CsvExport()
{
string sheetModel = HttpContext.Current.Request.Params["sheetModel"], sheetData = HttpContext.Current.Request.Params["sheetData"];
Spreadsheet.Save(sheetModel, sheetData, "sample", ExportFormat.CSV);
}

{% endhighlight %}

>The above example will export the Spreadsheet as CSV file.

## PdfExport

 [POST] [/Api/Spreadsheet/PdfExport](http://js.syncfusion.com/demos/ejServices/api/Spreadsheet/PdfExport)

It is used to export the Spreadsheet data as a PDF document.

### URL parameters

|  Parameter |  Description | 
|---|---|
|sheetModel|It contains the model of the Spreadsheet.|
|sheetData|DataURL of the Spreadsheet to be exported.|

### Response information 

Code: 200

Content-Type: application/octet-stream	

### Code example 

{% highlight js %}


{% endhighlight %}

{% highlight c# %}

public void PdfExport()
{
string sheetModel = HttpContext.Current.Request.Params["sheetModel"], sheetData = HttpContext.Current.Request.Params["sheetData"];
Spreadsheet.Save(sheetModel, sheetData, "sample", ExportFormat.PDF);
}

{% endhighlight %}

>The above example will export the Spreadsheet as PDF file.

## Import

 [POST] [/Api/Spreadsheet/Import](http://js.syncfusion.com/demos/ejServices/api/Spreadsheet/Import)

It loads the document from specified path in Spreadsheet.

### URL parameters

|  Parameter |  Description | 
|---|---|
|sheetIndex|It denotes the index of the page in Spreadsheet.|
|dataContainer|It has the data for the Spreadsheet.|
|allowSheetOnDemand|It is used for load on demand in Spreadsheet.|
|password|It holds the password information.|

### Response information 

Code: 200

Content-Type:  application/json; charset=utf-8

### Code example 

{% highlight js %}

{% endhighlight %}




