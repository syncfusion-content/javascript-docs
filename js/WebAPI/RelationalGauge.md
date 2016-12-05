---
layout: post
title: webAPI reference for RelationalGauge
description: webAPI reference for RelationalGauge
documentation: ug
platform: js
keywords: RelationalGauge, syncfusion, RelationalGauge webapi
---

## Initialize

 [POST] [/Api/RelationalGauge/Initialize](http://js.syncfusion.com/demos/ejServices/api/RelationalGauge/Initialize)

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

public Dictionary<string, object> Initialize(Dictionary<string, object> jsonResult)
{
    htmlHelper.PivotReport = BindDefaultData();
    return htmlHelper.GetJsonData(jsonResult["action"].ToString(), ProductSales.GetSalesData());
}

{% endhighlight %}
