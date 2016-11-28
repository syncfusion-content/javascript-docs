---
layout: post
title: webAPI reference for RelationalClient
description: webAPI reference for RelationalClient
documentation: API
platform: js-webapi
keywords: RelationalClient, syncfusion, RelationalClient webapi
---

## Initialize

[POST&nbsp;&nbsp;/Api/RelationalClient/Initialize](http://js.syncfusion.com/demos/ejServices/api/RelationalClient/Initialize)

It fetches the data required to initialize the control.

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

```javascript



```

## FetchMembers

[POST&nbsp;&nbsp;/Api/RelationalClient/FetchMembers](http://js.syncfusion.com/demos/ejServices/api/RelationalClient/FetchMembers)

It fetches the details of the members in the selected field on opening member editor.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|currentReport|It contains the current report as compressed string|
|customObject|It contains the custom object passed from client side|
|headerTag|It contains the information about the selected field|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string	

### Code example 

```javascript



```

## DrillChart

[POST&nbsp;&nbsp;/Api/RelationalClient/DrillChart](http://js.syncfusion.com/demos/ejServices/api/RelationalClient/DrillChart)

It fetches the drilled data required to render the control on performing drilldown in PivotChart.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|drilledSeries|It contains the name of the drilled member|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string	

### Code example 

```javascript



```

## Filtering

[POST&nbsp;&nbsp;/Api/RelationalClient/Filtering](http://js.syncfusion.com/demos/ejServices/api/RelationalClient/Filtering)

It fetches the data required to render the control on performing filtering.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|filterParams|It contains the filter information applied to the field|
|currentReport|It contains the current report as compressed string|
|customObject|It contains the custom object passed from client side|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string	

### Code example 

```javascript



```

## DropNode

[POST&nbsp;&nbsp;/Api/RelationalClient/DropNode](http://js.syncfusion.com/demos/ejServices/api/RelationalClient/DropNode)

It fetches the data required to render the control on performing node drop action.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|args|It contains the information about the dropped item|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string	

### Code example 

```javascript



```

## ToolbarOperations

[POST&nbsp;&nbsp;/Api/RelationalClient/ToolbarOperations](http://js.syncfusion.com/demos/ejServices/api/RelationalClient/ToolbarOperations)

It fetches the data required to render the control on performing toolbar operations.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|args|It contains the details about the operation performed|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string	

### Code example 

```javascript



```

## SaveReportToDB

[POST&nbsp;&nbsp;/Api/RelationalClient/SaveReportToDB](http://js.syncfusion.com/demos/ejServices/api/RelationalClient/SaveReportToDB)

It saves the current report to database with the specified name.

### URL parameters

|  Parameter |  Description | 
|---|---|
|reportName|It contains the name with which the report to be stored|
|operationalMode|It contains the mode of operation of control whether from client side or server side|
|analysisMode|It contains the analysis mode to indicate whether the bound data source is OLAP or Relational|
|olapReport|It contains the current report as compressed string|
|clientReports|It contains the report collection at that instant|

### Response information 

Code: 200

Content-Type: application/json

Response: None	

### Code example 

```javascript



```

## Export

[POST&nbsp;&nbsp;/Api/RelationalClient/Export](http://js.syncfusion.com/demos/ejServices/api/RelationalClient/Export)

It exports the PivotGrid or PivotChart or both to the selected format.

### URL parameters

|  Parameter |  Description | 
|---|---|
|args|It contains the current report as serialized string|

### Response information 

Code: 200

Content-Type: application/json

Response: file	

### Code example 

```javascript



```

## FetchReportListFromDB

[POST&nbsp;&nbsp;/Api/RelationalClient/FetchReportListFromDB](http://js.syncfusion.com/demos/ejServices/api/RelationalClient/FetchReportListFromDB)

It fetches the list of names of reports stored in database.

### URL parameters

|  Parameter |  Description | 
|---|---|
|operationalMode|It contains the mode of operation of control whether from client side or server side|
|analysisMode|It contains the analysis mode to indicate whether the bound data source is OLAP or Relational|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string	

### Code example 

```javascript



```

## LoadReportFromDB

[POST&nbsp;&nbsp;/Api/RelationalClient/LoadReportFromDB](http://js.syncfusion.com/demos/ejServices/api/RelationalClient/LoadReportFromDB)

It loads the report with specified name from the database to the control.

### URL parameters

|  Parameter |  Description | 
|---|---|
|reportName|It contains the name of the report to be loaded|
|operationalMode|It contains the mode of operation of control whether from client side or server side|
|analysisMode|It contains the analysis mode to indicate whether the bound data source is OLAP or Relational|
|olapReport|It contains the current report as compressed string|
|clientReports|It contains the report collection at that instant|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string	

### Code example 

```javascript



```
