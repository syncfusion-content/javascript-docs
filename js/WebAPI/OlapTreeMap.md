---
layout: post
title: webAPI reference for PivotTreeMAp
description: webAPI reference for OlapTreeMap
documentation: API
platform: js-webapi
keywords: PivotTreeMAp , syncfusion, PivotTreeMAp webapi
---

## Initialize

[POST&nbsp;&nbsp;/Api/OlapTreeMap/Initialize](http://js.syncfusion.com/demos/ejServices/api/OlapTreeMap/Initialize)

It fetches the OLAP data required to render the PivotTreeMap control from server-end.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string.|
|customObject|It contains the custom object passed from client side.|
|currentReport|It contains the current report as compressed string.|

### Response information 

Code: 

Content-Type: application/json;

Response(JSON):

```javascript


```

### Code example 

```javascript


```

## Drill

[POST&nbsp;&nbsp;/Api/OlapTreeMap/Drill](http://js.syncfusion.com/demos/ejServices/api/OlapTreeMap/Drill)

It fetches the OLAP data required to render the drilled PivotTreeMap.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string.|
|drillInfo|It contains the information about the drilled member.|
|olapReport|It contains the current report as compressed string.|
|customObject|It contains the custom object passed from client side.|

### Response information 

Code: 

Content-Type: application/json;

Response(JSON):

```javascript


```

### Code example 

```javascript


```