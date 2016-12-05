---
layout: post
title: webAPI reference for PivotChart
description: webAPI reference for PivotChart
documentation: ug
platform: js
keywords: PivotChart , syncfusion, PivotChart webapi
---

## Initialize

 [POST] [/Api/OlapChart/Initialize](http://js.syncfusion.com/demos/ejServices/api/OlapChart/Initialize)

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

{% highlight c# %}
public Dictionary<string, object> Initialize(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(CreateOlapReport());
    return htmlHelper.GetJsonData(jsonResult["action"].ToString(), DataManager);
}

{% endhighlight %}

## Drill

 [POST] [/Api/OlapChart/Drill](http://js.syncfusion.com/demos/ejServices/api/OlapChart/Drill)

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

{% highlight c# %}
public Dictionary<string, object> Drill(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["olapReport"].ToString()));
    return htmlHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["drilledSeries"].ToString());
}

{% endhighlight %}

## Export

 [POST] [/Api/OlapChart/Export](http://js.syncfusion.com/demos/ejServices/api/OlapChart/Export)

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

{% highlight c# %}
public void Export()
{
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    string fileName = "Sample";
    htmlHelper.ExportPivotChart(args, fileName, System.Web.HttpContext.Current.Response);
}

{% endhighlight %}

## ExcelExport

 [POST] [/Api/OlapChart/ExcelExport](http://js.syncfusion.com/demos/ejServices/api/OlapChart/ExcelExport)

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

{% highlight c# %}
public void ExcelExport()
{
    PivotChartExcelExport pivotChartExcelExport = new PivotChartExcelExport();
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    Dictionary<string, string> chartParams = serializer.Deserialize<Dictionary<string, string>>(args);
    pivotChartExcelExport.ExportToExcel(chartParams);
}

{% endhighlight %}

## WordExport

 [POST] [/Api/OlapChart/WordExport](http://js.syncfusion.com/demos/ejServices/api/OlapChart/WordExport)

It exports the PivotChart control at the instant to a Word document.

### URL parameters

|  Parameter |  Description | 
|---|---|
|chartData |It contains the information required to export the control to a Word document|

### Response information 

Code: 200

Content-Type: application/json

Response: Word document

### Code example 

{% highlight c# %}
public void WordExport()
{
    PivotChartWordExport pivotChartWordExport = new PivotChartWordExport();
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    Dictionary<string, string> chartParams = serializer.Deserialize<Dictionary<string, string>>(args);
    pivotChartWordExport.ExportToWord(chartParams);
}

{% endhighlight %}

## PdfExport

 [POST] [/Api/OlapChart/PdfExport](http://js.syncfusion.com/demos/ejServices/api/OlapChart/PdfExport)

It exports the PivotChart control at the instant to a PDF document.

### URL parameters

|  Parameter |  Description | 
|---|---|
|chartData |It contains the information required to export the control to a PDF document|

### Response information 

Code: 200

Content-Type: application/json

Response: PDF document

### Code example 

{% highlight c# %}
public void PdfExport()
{
    PivotChartPDFExport pivotChartPDFExport = new PivotChartPDFExport();
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    Dictionary<string, string> chartParams = serializer.Deserialize<Dictionary<string, string>>(args);
    pivotChartPDFExport.ExportToPDF(chartParams);
}

{% endhighlight %}

## ImageExport

 [POST] [/Api/OlapChart/ImageExport](http://js.syncfusion.com/demos/ejServices/api/OlapChart/ImageExport)

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

{% highlight c# %}
public void ImageExport()
{
    PivotChartImageExport pivotChartImageExport = new PivotChartImageExport();
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    Dictionary<string, string> chartParams = serializer.Deserialize<Dictionary<string, string>>(args);
    pivotChartImageExport.ExportToImage(chartParams);
}

{% endhighlight %}