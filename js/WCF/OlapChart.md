---
layout: post
title: WCF reference for PivotChart
description: WCF reference for PivotChart
documentation: ug
platform: js
keywords: PivotChart , syncfusion, PivotChart wcf
---

## Initialize

 [POST] [/WCF/PivotChart/Initialize](http://js.syncfusion.com/demos/ejServices/wcf/PivotChart/Olap.svc/Initialize)

It fetches the OLAP data which is required to initialize the PivotChart from server-end.

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
    var cultureIDInfo = new System.Globalization.CultureInfo(("en-US")).LCID;
    if (customData is Dictionary<string, object> && customData.ContainsKey("Language"))
    {
        cultureIDInfo = new System.Globalization.CultureInfo((customData["Language"])).LCID;
    }
    connectionString = connectionString.Replace("" + cultureIDInfovalval + "", "" + cultureIDInfo + "");
    cultureIDInfovalval = cultureIDInfo;
    DataManager = new OlapDataManager(connectionString);
    DataManager.Culture = new System.Globalization.CultureInfo((cultureIDInfo));
    DataManager.SetCurrentReport(CreateOlapReport());
    return htmlHelper.GetJsonData(action, DataManager);
}

{% endhighlight %} 

## Drill

 [POST] [/WCF/PivotChart/Drill](http://js.syncfusion.com/demos/ejServices/wcf/PivotChart/Olap.svc/Drill)

It fetches the drilled OLAP data which is required to render the PivotChart control from server-end.

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

public Dictionary<string, object> Drill(string action, string drilledSeries, string olapReport, string customObject)
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
    DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(olapReport));
    return htmlHelper.GetJsonData(action, DataManager, drilledSeries);
}

{% endhighlight %} 

## Export

 [POST] [/WCF/PivotChart/Export](http://js.syncfusion.com/demos/ejServices/wcf/PivotChart/Olap.svc/Export)

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

public void Export(Stream stream)
{
    System.IO.StreamReader sReader = new System.IO.StreamReader(stream);
    string args = System.Web.HttpContext.Current.Server.UrlDecode(sReader.ReadToEnd()).Remove(0, 5);
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    string fileName = "Sample";
    htmlHelper.ExportPivotChart(args, fileName, System.Web.HttpContext.Current.Response);
}

{% endhighlight %} 