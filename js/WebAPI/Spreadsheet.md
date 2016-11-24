---
layout: post
title: webAPI reference for ejSpreadsheet
description: webAPI reference for ejSpreadsheet
documentation: API
platform: js-webapi
keywords: Spreadsheet,ejSpreadsheet , syncfusion, ejSpreadsheet webapi
---

## ExcelExport

[POST&nbsp;&nbsp;/Api/Spreadsheet/ExcelExport](http://js.syncfusion.com/demos/ejServices/api/Spreadsheet/ExcelExport)

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

```javascript


```
```csharp
public void ExcelExport()
{
	string sheetModel = HttpContext.Current.Request.Params["sheetModel"], sheetData = HttpContext.Current.Request.Params["sheetData"], password = HttpContext.Current.Request.Params["password"];
	if (!string.IsNullOrEmpty(password))
		Spreadsheet.Save(sheetModel, sheetData, "sample", ExportFormat.XLSX, ExcelVersion.Excel2013, password);
	else
		Spreadsheet.Save(sheetModel, sheetData, "sample", ExportFormat.XLSX, ExcelVersion.Excel2013);
}
```
>The above example will export the Spreadsheet as an Excel file.

## CsvExport

[POST&nbsp;&nbsp;/Api/Spreadsheet/CsvExport](http://js.syncfusion.com/demos/ejServices/api/Spreadsheet/CsvExport)

It is used to export the Spreadsheet data to Csv file.

### URL parameters

|  Parameter |  Description | 
|---|---|
|sheetModel|It contains the model of the Spreadsheet.|
|sheetData|DataURL of the Spreadsheet to be exported.|

### Response information 

Code: 200

Content-Type: application/octet-stream	

### Code example 

```javascript



```
```csharp

public void CsvExport()
{
	string sheetModel = HttpContext.Current.Request.Params["sheetModel"], sheetData = HttpContext.Current.Request.Params["sheetData"];
	Spreadsheet.Save(sheetModel, sheetData, "sample", ExportFormat.CSV);
}

```

>The above example will export the Spreadsheet as Csv file.

## PdfExport

[POST&nbsp;&nbsp;/Api/Spreadsheet/PdfExport](http://js.syncfusion.com/demos/ejServices/api/Spreadsheet/PdfExport)

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

```javascript


```

```csharp

public void PdfExport()
{
	string sheetModel = HttpContext.Current.Request.Params["sheetModel"], sheetData = HttpContext.Current.Request.Params["sheetData"];
	Spreadsheet.Save(sheetModel, sheetData, "sample", ExportFormat.PDF);
}

```
>The above example will export the Spreadsheet as PDF file.

## Import

[POST&nbsp;&nbsp;/Api/Spreadsheet/Import](http://js.syncfusion.com/demos/ejServices/api/Spreadsheet/Import)

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

```javascript

```




