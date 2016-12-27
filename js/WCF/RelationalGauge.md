---
layout: post
title: WCF reference for RelationalGauge
description: WCF reference for RelationalGauge
documentation: ug
platform: js
keywords: RelationalGauge, syncfusion, RelationalGauge WCF
---

## Initialize

 [POST] [/WCF/PivotGauge/Initialize](http://js.syncfusion.com/demos/ejServices/wcf/PivotGauge/Relational.svc/Initialize)

It fetches the Relational data required to render the PivotGauge control from server-end.

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

public Dictionary<string, object> Initialize(string action, string customObject)
{
    htmlHelper.PivotReport = BindDefaultData();
    return htmlHelper.GetJsonData(action, ProductSales.GetSalesData());
}

{% endhighlight %} 
