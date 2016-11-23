---
layout: post
title: webAPI reference for ejChart
description: webAPI reference for ejChart
documentation: API
platform: js-webapi
keywords: Chart,ejChart , syncfusion, ejChart webapi
---

## Export

<a>POST&nbsp;&nbsp;/Api/Chart/Export</a>

It is used to export the Chart control to the specified format.

### URL parameters

|  Parameter |  Description | 
|---|---|
|ChartModel|It contains the model of the chart.|
|Data|DataURL of the chart to be exported.|

### Response information 

Code: 200

Content-Type: application/octet-stream	

### Code example 

```javascript

$("#chartcontainer").ejChart(
	 { exportSettings: { angle: 180, action: "http://js.syncfusion.com/demos/api/Chart/Export" },
});

```

>The above example will export the Chart into specified file format.

## SvgExport

<a>POST&nbsp;&nbsp;/Api/Chart/SvgExport</a>

It is used to export the Chart control as an SVG image.

### URL parameters

|  Parameter |  Description | 
|---|---|
|ChartModel|It contains the model of the chart.|
|Data|DataURL of the chart to be exported.|

### Response information 

Code: 200

Content-Type: application/octet-stream	

### Code example 

```javascript

$("#chartcontainer").ejChart(
	 {exportSettings: { type: "svg", angle: 180, action: "http://js.syncfusion.com/demos/api/Chart/SvgExport" },
});

```
>The above example will export the Chart as an SVG image.

## ExcelExport

<a>POST&nbsp;&nbsp;/Api/Chart/ExcelExport</a>

It is used to export the Chart control as an Excel document.

### URL parameters

|  Parameter |  Description | 
|---|---|
|ChartModel|It contains the model of the chart.|
|Data|DataURL of the chart to be exported.|

### Response information 

Code: 200

Content-Type: application/octet-stream	

### Code example 

```javascript

$("#chartcontainer").ejChart(
	 {exportSettings: { type: "xlsx", angle: 180, action: "http://js.syncfusion.com/demos/api/Chart/ExcelExport" },
});

```
>The above example will export the Chart as an Excel file.

## WordExport

<a>POST&nbsp;&nbsp;/Api/Chart/WordExport</a>

It is used to export the Chart control as a Word document.

### URL parameters

|  Parameter |  Description | 
|---|---|
|ChartModel|It contains the model of the chart.|
|Data|DataURL of the chart to be exported.|

### Response information 

Code: 200

Content-Type: application/octet-stream	

### Code example 

```javascript

$("#chartcontainer").ejChart(
	 {exportSettings: { type: "docx", angle: 180, action: "http://js.syncfusion.com/demos/api/Chart/WordExport" },
});

```
>The above example will export the Chart as an Word file.

## PdfExport

<a>POST&nbsp;&nbsp;/Api/Chart/PdfExport</a>

It is used to export the Chart control as a PDF document.

### URL parameters

|  Parameter |  Description | 
|---|---|
|ChartModel|It contains the model of the chart.|
|Data|DataURL of the chart to be exported.|

### Response information 

Code: 200

Content-Type: application/octet-stream	

### Code example 

```javascript

$("#chartcontainer").ejChart(
	 {exportSettings: { type: "pdf", angle: 180, action: "http://js.syncfusion.com/demos/api/Chart/PdfExport" },
});

```
>The above example will export the Chart as PDF file.

## ImageExport

<a>POST&nbsp;&nbsp;/Api/Chart/ImageExport</a>

It is used to export the chart control as an image (PNG/JPG).

### URL parameters

|  Parameter |  Description | 
|---|---|
|ChartModel|It contains the model of the chart.|
|Data|DataURL of the chart to be exported.|

### Response information 

Code: 200

Content-Type: application/octet-stream	

### Code example 

```javascript

$("#chartcontainer").ejChart(
	 {exportSettings: { type: "jpg", angle: 180, action: "http://js.syncfusion.com/demos/api/Chart/ImageExport" },
});

```
>The above example will export the Chart as JPG Image.



