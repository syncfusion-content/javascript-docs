---
layout: post
title: webAPI reference for PivotGauge
description: webAPI reference for OlapGauge
documentation: ug
platform: js
keywords: PivotGauge , syncfusion, PivotGauge webapi
---

## Initialize

 [POST] [/Api/OlapGauge/Initialize](http://js.syncfusion.com/demos/ejServices/api/OlapGauge/Initialize)

It fetches the OLAP data required to render the PivotGauge control from server-end.

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
