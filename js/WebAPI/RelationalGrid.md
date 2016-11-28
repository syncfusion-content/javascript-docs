---
layout: post
title: webAPI reference for RelationalGrid
description: webAPI reference for RelationalGrid
documentation: API
platform: js-webapi
keywords: RelationalGrid, syncfusion, RelationalGrid webapi
---

## Initialize

[POST&nbsp;&nbsp;/Api/RelationalGrid/Initialize](http://js.syncfusion.com/demos/ejServices/api/RelationalGrid/Initialize)

It fetches the data required to render the PivotGrid initially.

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

[POST&nbsp;&nbsp;/Api/RelationalGrid/FetchMembers](http://js.syncfusion.com/demos/ejServices/api/RelationalGrid/FetchMembers)

It fetches the members of the selected field to render the member editor tree.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|headerTag|It contains the information about the dropped item|
|sortedHeaders|It contains the information about the sorting applied|
|currentReport|It contains the current report as compressed string|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string	

### Code example 

```javascript



```

## Filtering

[POST&nbsp;&nbsp;/Api/RelationalGrid/Filtering](http://js.syncfusion.com/demos/ejServices/api/RelationalGrid/Filtering)

It fetches the data required to render the PivotGrid control on performing filtering action.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|filterParams|It contains the filter information applied to the hierarchy|
|sortedHeaders|It contains the information about the sorting applied|
|currentReport|It contains the current report as compressed string|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string	

### Code example 

```javascript



```

## ModifyNodeState

[POST&nbsp;&nbsp;/Api/RelationalGrid/ModifyNodeState](http://js.syncfusion.com/demos/ejServices/api/RelationalGrid/ModifyNodeState)

It fetches the relational data required to render the PivotGrid control on selecting/unselecting nodes in Field list.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|headerTag|It contains the information about the dropped item|
|dropAxis|It contains the dropped axis|
|sortedHeaders|It contains the information about the sorting applied|
|filterParams|It contains the filter information applied to the hierarchy|
|currentReport|It contains the current report as compressed string|


### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string	

### Code example 

```javascript



```

## DropNode

[POST&nbsp;&nbsp;/Api/RelationalGrid/DropNode](http://js.syncfusion.com/demos/ejServices/api/RelationalGrid/DropNode)

It fetches the relational data required to render the PivotGrid control on node drop action.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|dropAxis|It tells the dropped axis|
|headerTag|It contains the information about the dropped item|
|sortedHeaders|It contains the information about the sorting applied|
|filterParams|It contains the filter information applied to the hierarchy|
|currentReport|It contains the current report as compressed string|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string	

### Code example 

```javascript



```

## Sorting

[POST&nbsp;&nbsp;/Api/RelationalGrid/Sorting](http://js.syncfusion.com/demos/ejServices/api/RelationalGrid/Sorting)

It fetches the sorted data to render the PivotGrid control on performing sorting.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|sortedHeaders|It contains the information about the sorting applied|
|currentReport|It contains the current report as compressed string|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string	

### Code example 

```javascript



```

## CalculatedField

[POST&nbsp;&nbsp;/Api/RelationalGrid/CalculatedField](http://js.syncfusion.com/demos/ejServices/api/RelationalGrid/CalculatedField)

It forms a calculated field in values area and fetches the data along with it to render the PivotGrid control.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|headerTag|It contains the calculation parameters|
|currentReport|It contains the current report as compressed string|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string	

### Code example 

```javascript



```

## Export

[POST&nbsp;&nbsp;/Api/RelationalGrid/Export](http://js.syncfusion.com/demos/ejServices/api/RelationalGrid/Export)

It is used to export the PivotGrid data to specified format.

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

## SaveReport

[POST&nbsp;&nbsp;/Api/RelationalGrid/SaveReport](http://js.syncfusion.com/demos/ejServices/api/RelationalGrid/SaveReport)

It saves the current report to database with the specified name.

### URL parameters

|  Parameter |  Description | 
|---|---|
|reportName|It holds the name with which the report to be saved|
|operationalMode|It contains the mode of operation of control whether from client side or server side|
|olapReport|It contains the current report as compressed string|
|clientReports|It contains the report collection as compressed string|

### Response information 

Code: 200

Content-Type: application/json

Response: None	

### Code example 

```javascript



```

## LoadReportFromDB

[POST&nbsp;&nbsp;/Api/RelationalGrid/LoadReportFromDB](http://js.syncfusion.com/demos/ejServices/api/RelationalGrid/LoadReportFromDB)

It loads a report from the database and refreshes the control with it.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|layout|It contains the layout of PivotGrid control|
|enablePivotFieldList|Boolean property tells whether the field list is enabled or not|
|customObject|It contains the custom object passed from client side|
|reportName|It holds the name of the report to be loaded|
|operationalMode|It contains the mode of operation of control whether from client side or server side|
|olapReport|It contains the current report as compressed string|
|clientReports|It contains the report collection as compressed string|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string	

### Code example 

```javascript



```

## DeferUpdate

[POST&nbsp;&nbsp;/Api/RelationalGrid/DeferUpdate](http://js.syncfusion.com/demos/ejServices/api/RelationalGrid/DeferUpdate)

It fetches the data with respect to the report available at that instant (i.e) updates the control with current report.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|filterParams|It contains the filter information applied to the hierarchy|
|currentReport|It contains the current report as compressed string|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string	

### Code example 

```javascript



```

## CellEditing

[POST&nbsp;&nbsp;/Api/RelationalGrid/CellEditing](http://js.syncfusion.com/demos/ejServices/api/RelationalGrid/CellEditing)

It rewrites the content of database on editing a cell.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|index|It contains the position of the cell edited|
|valueHeaders|It contains the value information related to the edited cell|
|summaryValues|It contains the summaries associated with the selected cells|
|currentReport|It contains the current report as compressed string|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string	

### Code example 

```javascript



```
