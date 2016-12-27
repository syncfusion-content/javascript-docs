---
layout: post
title: WCF reference for PivotGauge
description: WCF reference for OlapGauge
documentation: ug
platform: js
keywords: PivotGauge , syncfusion, PivotGauge WCF
---

## Initialize

 [POST] [/WCF/PivotGauge/Initialize](http://js.syncfusion.com/demos/ejServices/wcf/PivotGauge/Olap.svc/Initialize)

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

public Dictionary<string, object> Initialize(string action, string customObject)
{
    OlapDataManager DataManager = null;
    dynamic customData = serializer.Deserialize<dynamic>(customObject.ToString());
    var cultureIDInfo = new System.Globalization.CultureInfo("en-US").LCID;
    if (customData is Dictionary<string, object> && customData.ContainsKey("Language"))
    {
        cultureIDInfo = new System.Globalization.CultureInfo((customData["Language"])).LCID;
    }
    connectionString = connectionString.Replace("" + cultureIDInfoval + "", "" + cultureIDInfo + "");
    cultureIDInfoval = cultureIDInfo;
    DataManager = new OlapDataManager(connectionString);
    DataManager.Culture = new System.Globalization.CultureInfo(cultureIDInfo);
    DataManager.SetCurrentReport(CreateOlapReport());
    return htmlHelper.GetJsonData(action, DataManager);
}

{% endhighlight %} 
