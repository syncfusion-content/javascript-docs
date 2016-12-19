---
layout: post
title: webAPI reference for PivotTreeMAp
description: webAPI reference for OlapTreeMap
documentation: ug
platform: js
keywords: PivotTreeMAp , syncfusion, PivotTreeMAp webapi
---

## Initialize

 [POST] [/Api/OlapTreeMap/Initialize](http://js.syncfusion.com/demos/ejServices/api/OlapTreeMap/Initialize)

It fetches the OLAP data required to render the PivotTreeMap control from server-end.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string.|
|customObject|It contains the custom object passed from client side.|
|currentReport|It contains the current report as compressed string.|

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

 [POST] [/Api/OlapTreeMap/Drill](http://js.syncfusion.com/demos/ejServices/api/OlapTreeMap/Drill)

It fetches the OLAP data required to render the drilled PivotTreeMap.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|drillInfo|It contains the information about the drilled member|
|olapReport|It contains the current report as serialized string|
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
    return htmlHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["drillInfo"].ToString());
}

{% endhighlight %}