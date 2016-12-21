---
layout: post
title: WCF reference for PivotChart
description: WCF reference for PivotChart
documentation: ug
platform: js
keywords: PivotChart , syncfusion, PivotChart WCF
---

## Initialize

 [POST] [/WCF/PivotChart/Initialize](http://js.syncfusion.com/demos/ejServices/wcf/PivotChart/Relational.svc/Initialize)

It fetches the OLAP data which is required to initialize the PivotChart from server-end.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|customObject|It contains the custom object passed from client side|
|CurrentReport|It contains the current report as compressed string|

### Response information 

Code: 200

Content-Type: application/json;

Response: serialized JSON string

### Code example 

{% highlight c# %}

public Dictionary<string, object> Initialize(string action, string currentReport, string customObject)
{
    BindData();
    return PivotChart.GetJsonData(action, ProductSales.GetSalesData());
}

{% endhighlight %} 

## Drill

 [POST] [/WCF/PivotChart/Drill](http://js.syncfusion.com/demos/ejServices/wcf/PivotChart/Relational.svc/Drill)

It fetches the drilled OLAP data which is required to render the PivotChart control from server-end.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|drilledSeries|It contains the name of the drilled member|

### Response information 

Code: 200

Content-Type: application/json;

Response: serialized JSON string

### Code example 

{% highlight c# %}

public Dictionary<string, object> Drill(string action, string drilledSeries)
{
    BindData();
    return PivotChart.GetJsonData(action, ProductSales.GetSalesData(), drilledSeries);
}

{% endhighlight %} 