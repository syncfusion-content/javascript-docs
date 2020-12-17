---
layout: post
title: Syncfusion webAPI reference for ejChart 
description: Know more about the webAPI references available for the Syncfusion Essential Studio ejChart control to export the Chart control to specified formats.
documentation: ug
platform: js
keywords: Chart, ejChart, syncfusion, ejChart webapi
---

# Various Chart Export using WebAPI

## Export

[POST] [/Api/Chart/Export](http://js.syncfusion.com/demos/ejServices/api/Chart/Export)

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

{% highlight js %}

$("#chartContainer").ejChart(
	 { exportSettings: { angle: 180, action: "http://js.syncfusion.com/demos/ejServices/api/Chart/Export" },
});

{% endhighlight %}

>The above example will export the Chart into specified file format.

## SvgExport

[POST] [/Api/Chart/SvgExport](http://js.syncfusion.com/demos/ejServices/api/Chart/SvgExport)

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

{% highlight js %}

$("#chartContainer").ejChart(
	 {exportSettings: { type: "svg", angle: 180, action: "http://js.syncfusion.com/demos/ejServices/api/Chart/SvgExport" },
});

{% endhighlight %}

>The above example will export the Chart as an SVG image.

## ExcelExport

 [POST][/Api/Chart/ExcelExport](http://js.syncfusion.com/demos/ejServices/api/Chart/ExcelExport)

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

{% highlight js %}

$("#chartContainer").ejChart(
	 {exportSettings: { type: "xlsx", angle: 180, action: "http://js.syncfusion.com/demos/ejServices/api/Chart/ExcelExport" },
});

{% endhighlight %}

>The above example will export the Chart as an Excel file.

## WordExport

[POST] [/Api/Chart/WordExport](http://js.syncfusion.com/demos/ejServices/api/Chart/WordExport)

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

{% highlight js %}

$("#chartContainer").ejChart(
	 {exportSettings: { type: "docx", angle: 180, action: "http://js.syncfusion.com/demos/ejServices/api/Chart/WordExport" },
});

{% endhighlight %}

>The above example will export the Chart as an Word file.

## PdfExport

[POST] [/Api/Chart/PdfExport](http://js.syncfusion.com/demos/ejServices/api/Chart/PdfExport)

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

{% highlight js %}

$("#chartContainer").ejChart(
	 {exportSettings: { type: "pdf", angle: 180, action: "http://js.syncfusion.com/demos/ejServices/api/Chart/PdfExport" },
});

{% endhighlight %}

>The above example will export the Chart as PDF file.

## ImageExport

[POST] [/Api/Chart/ImageExport](http://js.syncfusion.com/demos/ejServices/api/Chart/ImageExport)

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

{% highlight js %}

$("#chartContainer").ejChart(
	 {exportSettings: { type: "jpg", angle: 180, action: "http://js.syncfusion.com/demos/ejServices/api/Chart/ImageExport" },
});

{% endhighlight %}

>The above example will export the Chart as JPG Image.



