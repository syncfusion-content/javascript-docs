---
layout: post
title: webAPI reference for PivotChart
description: webAPI reference for PivotChart
documentation: API
platform: js-webapi
keywords: PivotChart , syncfusion, PivotChart webapi
---

## Initialize

[POST&nbsp;&nbsp;/Api/OlapChart/Initialize](http://js.syncfusion.com/demos/ejServices/api/OlapChart/Initialize)

It fetches the OLAP data required to initialize the PivotChart from server-end.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|customObject|It contains the custom object passed from client side|

### Response information 

Code: 200

Content-Type: application/json;

Response: serialized JSON string

### Code example 

```javascript


```

## Drill

[POST&nbsp;&nbsp;/Api/OlapChart/Drill](http://js.syncfusion.com/demos/ejServices/api/OlapChart/Drill)

It fetches the drilled OLAP data required to render the PivotChart control from server-end.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|drilledSeries|It contains the name of the drilled member|
|olapReport|It contains the current report as compressed string|
|customObject|It contains the custom object passed from client side|

### Response information 

Code: 200

Content-Type: application/json;

Response: serialized JSON string

### Code example 

```javascript


```

## Export

[POST&nbsp;&nbsp;/Api/OlapChart/Export](http://js.syncfusion.com/demos/ejServices/api/OlapChart/Export)

It exports the PivotChart control at the instant to the specified format.

### URL parameters

|  Parameter |  Description | 
|---|---|
|chartData |It contains the information required to export the control|

### Response information 

Code: 200

Content-Type: application/json	

Response: file

### Code example 

```javascript


```

```csharp

public void Export()
{
	string args = HttpContext.Current.Request.Form.GetValues(0)[0];
	string fileName = "Sample";
	htmlHelper.ExportPivotChart(args, fileName, System.Web.HttpContext.Current.Response);
}

```
## ExcelExport

[POST&nbsp;&nbsp;/Api/OlapChart/ExcelExport](http://js.syncfusion.com/demos/ejServices/api/OlapChart/ExcelExport)

It exports the PivotChart control at the instant to an Excel document.

### URL parameters

|  Parameter |  Description | 
|---|---|
|chartData |It contains the information required to export the control to an Excel sheet|

### Response information 

Code: 200

Content-Type: application/json

Response: Excel document

### Code example 

```javascript


```
```csharp

public void ExcelExport()
{
	PivotChartExcelExport pivotChartExcelExport = new PivotChartExcelExport();
	string args = HttpContext.Current.Request.Form.GetValues(0)[0];
	Dictionary<string, string> chartParams = serializer.Deserialize<Dictionary<string, string>>(args);
	pivotChartExcelExport.ExportToExcel(chartParams);
}

```
## WordExport

[POST&nbsp;&nbsp;/Api/OlapChart/WordExport](http://js.syncfusion.com/demos/ejServices/api/OlapChart/WordExport)

It exports the PivotChart control at the instant to an Word document.

### URL parameters

|  Parameter |  Description | 
|---|---|
|chartData |It contains the information required to export the control to a Word document|

### Response information 

Code: 200

Content-Type: application/json

Response: Word document

### Code example 

```javascript


```
```csharp

public void WordExport()
{
	PivotChartWordExport pivotChartWordExport = new PivotChartWordExport();
	string args = HttpContext.Current.Request.Form.GetValues(0)[0];
	Dictionary<string, string> chartParams = serializer.Deserialize<Dictionary<string, string>>(args);
	pivotChartWordExport.ExportToWord(chartParams);
}

```
## PdfExport

[POST&nbsp;&nbsp;/Api/OlapChart/PdfExport](http://js.syncfusion.com/demos/ejServices/api/OlapChart/PdfExport)

It exports the PivotChart control at the instant to an PDF document.

### URL parameters

|  Parameter |  Description | 
|---|---|
|chartData |It contains the information required to export the control to a PDF document|

### Response information 

Code: 200

Content-Type: application/json

Response: PDF document

### Code example 

```javascript


```
```csharp

public void PdfExport()
{
	PivotChartPDFExport pivotChartPDFExport = new PivotChartPDFExport();
	string args = HttpContext.Current.Request.Form.GetValues(0)[0];
	Dictionary<string, string> chartParams = serializer.Deserialize<Dictionary<string, string>>(args);
	pivotChartPDFExport.ExportToPDF(chartParams);
}

```
## ImageExport

[POST&nbsp;&nbsp;/Api/OlapChart/ImageExport](http://js.syncfusion.com/demos/ejServices/api/OlapChart/ImageExport)

It exports the PivotChart control at the instant as an Image in specified format.

### URL parameters

|  Parameter |  Description | 
|---|---|
|chartData |It contains the information required to export the control to an image file|

### Response information 

Code: 200

Content-Type: application/json

Response: Image file

### Code example 

```javascript


```
```csharp

public void ImageExport()
{
	PivotChartImageExport pivotChartImageExport = new PivotChartImageExport();
	string args = HttpContext.Current.Request.Form.GetValues(0)[0];
	Dictionary<string, string> chartParams = serializer.Deserialize<Dictionary<string, string>>(args);
	pivotChartImageExport.ExportToImage(chartParams);
}  

```