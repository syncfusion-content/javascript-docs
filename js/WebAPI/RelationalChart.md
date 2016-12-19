---
layout: post
title: webAPI reference for RelationalChart
description: webAPI reference for RelationalChart
documentation: ug
platform: js
keywords: RelationalChart, syncfusion, RelationalChart webapi
---

## Initialize

 [POST] [/Api/RelationalChart/Initialize](http://js.syncfusion.com/demos/ejServices/api/RelationalChart/Initialize)

It fetches the Relational data required to initialize the PivotChart from server-end.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|customObject|It contains the custom object passed from client side|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string	

### Code example 

{% highlight c# %}
public Dictionary<string, object> Initialize(Dictionary<string, object> jsonResult)
{
    BindData();
    return pivotChart.GetJsonData(jsonResult["action"].ToString(), ProductSales.GetSalesData());
}

{% endhighlight %}

## Drill

 [POST] [/Api/RelationalChart/Drill](http://js.syncfusion.com/demos/ejServices/api/RelationalChart/Drill)

It fetches the drilled Relational data required to render the PivotChart control from server-end.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|drilledSeries|It contains the name of the drilled member|
|olapReport|It contains the current report as compressed string|
|customObject|It contains the custom object passed from client side|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string

### Code example 

{% highlight c# %}
public Dictionary<string, object> Drill(Dictionary<string, object> jsonResult)
{
    BindData();
    return pivotChart.GetJsonData(jsonResult["action"].ToString(), ProductSales.GetSalesData(), jsonResult["drilledSeries"].ToString());
}

{% endhighlight %}

## Export

 [POST] [/Api/RelationalChart/Export](http://js.syncfusion.com/demos/ejServices/api/RelationalChart/Export)

It exports the PivotChart control at the instant to the specified format.

### URL parameters

|  Parameter |  Description | 
|---|---|
|chartData|It contains the information required to export the control|

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
    pivotChart.ExportPivotChart(args, fileName, System.Web.HttpContext.Current.Response);
}
        
{% endhighlight %}
