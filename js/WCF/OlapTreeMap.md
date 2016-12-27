---
layout: post
title: WCF reference for PivotTreeMAp
description: WCF reference for OlapTreeMap
documentation: ug
platform: js
keywords: PivotTreeMAp , syncfusion, PivotTreeMAp WCF
---

## Initialize

 [POST] [/WCF/PivotTreeMAp/Initialize](http://js.syncfusion.com/demos/ejServices/wcf/PivotTreeMAp/Olap.svc/Initialize)

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

public Dictionary<string, object> Initialize(string action, string currentReport, string customObject)
{
    OlapDataManager DataManager = null;
    dynamic customData = serializer.Deserialize<dynamic>(customObject.ToString());
    var cultureIDInfo = new System.Globalization.CultureInfo(("en-US")).LCID;
    if (customData is Dictionary<string, object> && customData.ContainsKey("Language"))
        cultureIDInfo = new System.Globalization.CultureInfo((customData["Language"])).LCID;
    connectionString = connectionString.Replace("" + cultureIDInfovalval + "", "" + cultureIDInfo + "");
    cultureIDInfovalval = cultureIDInfo;
    DataManager = new OlapDataManager(connectionString);
    DataManager.Culture = new System.Globalization.CultureInfo((cultureIDInfo));
    DataManager.SetCurrentReport(CreateOlapReport());
    return htmlHelper.GetJsonData(action, DataManager);
}

{% endhighlight %} 

## Drill

 [POST] [/WCF/PivotTreeMAp/Drill](http://js.syncfusion.com/demos/ejServices/wcf/PivotTreeMAp/Olap.svc/Drill)

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

public Dictionary<string, object> Drill(string action, string drillInfo, string olapReport, string customObject)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    dynamic customData = serializer.Deserialize<dynamic>(customObject.ToString());
    if (customData is Dictionary<string, object> && customData.ContainsKey("Language"))
    {
        var cultureIDInfo = new System.Globalization.CultureInfo((customData["Language"])).LCID;
        connectionString = connectionString.Replace("" + cultureIDInfovalval + "", "" + cultureIDInfo + "");
        cultureIDInfovalval = cultureIDInfo;
        DataManager = new OlapDataManager(connectionString);
        DataManager.Culture = new System.Globalization.CultureInfo((customData["Language"]));
    }
    else
        DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(olapReport));
    return htmlHelper.GetJsonData(action, DataManager, drillInfo);
}

{% endhighlight %} 