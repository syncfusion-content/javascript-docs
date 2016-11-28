---
layout: post
title: webAPI reference for PivotGrid
description: webAPI reference for PivotGrid
documentation: API
platform: js-webapi
keywords: PivotGrid , syncfusion, PivotGrid webapi
---

## Initialize

[POST&nbsp;&nbsp;/Api/OlapGrid/Initialize](http://js.syncfusion.com/demos/ejServices/api/OlapGrid/Initialize)

It fetches the OLAP data required to render the PivotGrid initially from server-end.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|gridLayout|It contains the layout of PivotGrid control|
|enablePivotFieldList|Boolean property tells whether the field list is enabled or not|
|customObject|It contains the custom object passed from client side|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string

### Code example 

```javascript


```

## Drill

[POST&nbsp;&nbsp;/Api/OlapGrid/Drill](http://js.syncfusion.com/demos/ejServices/api/OlapGrid/Drill)

It fetches the OLAP data required to render the PivotGrid control after drilling it.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string.|
|cellPosition|It contains the cell position of the drilled cell.|
|currentReport|It contains the current report as compressed string.|
|headerInfo|It contains the information about the drilled member.|
|layout|It contains the layout of PivotGrid control.|
|customObject|It contains the custom object passed from client side.|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string

### Code example 

```javascript


```

## DropNode

[POST&nbsp;&nbsp;/Api/OlapGrid/DropNode](http://js.syncfusion.com/demos/ejServices/api/OlapGrid/DropNode)

It fetches the data required to render the control after performing node drop operation.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string.|
|dropType|It tells whether the dropped item is a node or pivot button.|
|nodeInfo|It contains the information about the hierarchy dropped.|
|filterParams|It contains the filter information applied to the hierarchy.|
|gridLayout|It contains the layout of PivotGrid control.|
|currentReport|It contains the current report as compressed string.|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string

### Code example 

```javascript


```

```csharp

public Dictionary<string, object> DropNode(Dictionary<string, object> jsonResult)
{
	OlapDataManager DataManager = new OlapDataManager(connectionString);
	DataManager.SetCurrentReport(Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
	return htmlHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["dropType"].ToString(), jsonResult["nodeInfo"].ToString(), jsonResult.ContainsKey("filterParams") ? jsonResult["filterParams"].ToString() : null, jsonResult["gridLayout"].ToString(), true);
}

```
## Filtering

[POST&nbsp;&nbsp;/Api/OlapGrid/Filtering](http://js.syncfusion.com/demos/ejServices/api/OlapGrid/Filtering)

It fetches the OLAP data required to render the control after performing filtering.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string.|
|filterParams |It contains the filter information applied to the hierarchy.|
|currentReport|It contains the current report as compressed string.|
|gridLayout|It contains the layout of PivotGrid control.|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string

### Code example 

```javascript


```
```csharp

public Dictionary<string, object> Filtering(Dictionary<string, object> jsonResult)
{
	OlapDataManager DataManager = new OlapDataManager(connectionString);
	DataManager.SetCurrentReport(Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
	return htmlHelper.GetJsonData(jsonResult["action"].ToString(), connectionString, DataManager, null, jsonResult["filterParams"].ToString(), jsonResult["gridLayout"].ToString());
}

```

## FetchMembers

[POST&nbsp;&nbsp;/Api/OlapGrid/FetchMembers](http://js.syncfusion.com/demos/ejServices/api/OlapGrid/FetchMembers)

It fetches the members of the selected hierarchy to render the member editor.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string.|
|headerTag|It contains the information about the selected hierarchy.|
|currentReport|It contains the current report as compressed string.|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string

### Code example 

```javascript


```
```csharp

public Dictionary<string, object> FetchMembers(Dictionary<string, object> jsonResult)
{
	OlapDataManager DataManager = new OlapDataManager(connectionString);
	DataManager.SetCurrentReport(Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
	return htmlHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, null, jsonResult["headerTag"].ToString());
}

```


## Paging

[POST&nbsp;&nbsp;/Api/OlapGrid/Paging](http://js.syncfusion.com/demos/ejServices/api/OlapGrid/Paging)

It fetches the OLAP data required to render the specific page of PivotGrid with paging enabled.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string.|
|pagingInfo|It contains the pagination parameters.|
|currentReport|It contains the current report as compressed string.|
|gridLayout|It contains the layout of PivotGrid control.|
|customObject|It contains the custom object passed from client side.|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string

### Code example 

```javascript


```
```csharp

public Dictionary<string, object> Paging(Dictionary<string, object> jsonResult)
{
	OlapDataManager DataManager = new OlapDataManager(connectionString);
	DataManager.SetCurrentReport(htmlHelper.SetPaging(jsonResult["currentReport"].ToString(), jsonResult["pagingInfo"].ToString()));
	return htmlHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["layout"].ToString());
}

```

## RemoveButton

[POST&nbsp;&nbsp;/Api/OlapGrid/RemoveButton](http://js.syncfusion.com/demos/ejServices/api/OlapGrid/RemoveButton)

It fetches the data required to render the control after removing a button.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string.|
|headerInfo |It contains the information about the drilled member.|
|gridLayout|It contains the layout of PivotGrid control.|
|currentReport|It contains the current report as compressed string.|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string

### Code example 

```javascript


```
```csharp

public Dictionary<string, object> RemoveButton(Dictionary<string, object> jsonResult)
{
	OlapDataManager DataManager = new OlapDataManager(connectionString);
	DataManager.SetCurrentReport(Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
	return htmlHelper.GetJsonData(jsonResult["action"].ToString(), connectionString, DataManager, null, jsonResult["headerInfo"].ToString(), jsonResult["gridLayout"].ToString());
}

```

## ExpandMember

[POST&nbsp;&nbsp;/Api/OlapGrid/ExpandMember](http://js.syncfusion.com/demos/ejServices/api/OlapGrid/ExpandMember)

It fetches the data to render children nodes of a member in Member Editor Tree.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string.|
|checkedStatus|It contains checked status of the member in member editor tree.|
|parentNode|It contains the information about the expanded member.|
|tag|It contains the unique name of the expanded member.|
|cubeName|It contains the current cube name.|
|currentReport|It contains the current report as compressed string.|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string

### Code example 

```javascript


```
```csharp

public Dictionary<string, object> ExpandMember(Dictionary<string, object> jsonResult)
{
	OlapDataManager DataManager = new OlapDataManager(connectionString);
	if (!string.IsNullOrEmpty(jsonResult["currentReport"].ToString()))
		DataManager.SetCurrentReport(Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
	return htmlHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, Convert.ToBoolean(jsonResult["checkedStatus"].ToString()), jsonResult["parentNode"].ToString(), jsonResult["tag"].ToString(), jsonResult["cubeName"].ToString());
}

```

## Export

[POST&nbsp;&nbsp;/Api/OlapGrid/Export](http://js.syncfusion.com/demos/ejServices/api/OlapGrid/Export)

It is used to export the PivotGrid data to specified format.

### URL parameters

|  Parameter |  Description | 
|---|---|
|args|It holds the current report as compressed string|

### Response information 

Code: 200

Content-Type: application/json

Response: file

### Code example 

```javascript


```

```csharp

public void Export()
{
	string args = HttpContext.Current.Request.Form.GetValues(0)[0];
	OlapDataManager DataManager = new OlapDataManager(connectionString);
	string fileName = "Sample";
	htmlHelper.ExportPivotGrid(DataManager, args, fileName, System.Web.HttpContext.Current.Response);
}

```

## SaveReport

[POST&nbsp;&nbsp;/Api/OlapGrid/SaveReport](http://js.syncfusion.com/demos/ejServices/api/OlapGrid/SaveReport)

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

[POST&nbsp;&nbsp;/Api/OlapGrid/LoadReportFromDB](http://js.syncfusion.com/demos/ejServices/api/OlapGrid/LoadReportFromDB)

It loads a report from the database and refreshes the control with it.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string.|
|layout|It contains the layout of PivotGrid control.|
|enablePivotFieldList|Boolean property tells whether the field list is enabled or not.|
|customObject|It contains the custom object passed from client side.|
|reportName|It holds the name of the report to be loaded.|
|operationalMode|It contains the mode of operation of control whether from client side or server side.|
|olapReport|It contains the current report as compressed string.|
|clientReports|It contains the report collection as compressed string.|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string

### Code example 

```javascript


```
## DeferUpdate

[POST&nbsp;&nbsp;/Api/OlapGrid/DeferUpdate](http://js.syncfusion.com/demos/ejServices/api/OlapGrid/DeferUpdate)

It fetches the data with respect to the report available at that instant (i.e) updates the control with current report.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string.|
|filterParams|It contains the filter information applied to the hierarchy.|
|currentReport|It contains the current report as compressed string.|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string

### Code example 

```javascript


```

## ExcelExport

[POST&nbsp;&nbsp;/Api/OlapGrid/ExcelExport](http://js.syncfusion.com/demos/ejServices/api/OlapGrid/ExcelExport)

It exports the PivotGrid control at that instant to the Excel format.

### URL parameters

|  Parameter |  Description | 
|---|---|
|currentReport|It contains the current report as compressed string.|

### Response information 

Code: 200

Content-Type: application/json

Response: Excel document

### Code example 

```javascript


```
```csharp

public void ExcelExport()
{
	PivotGridExcelExport pGrid = new PivotGridExcelExport();
	string args = HttpContext.Current.Request.Form.GetValues(0)[0];
	pGrid.ExportToExcel(string.Empty, args, HttpContext.Current.Response);
}

```
>The above example will export the PivotGrid as an Excel file.


## PdfExport

[POST&nbsp;&nbsp;/Api/OlapGrid/PdfExport](http://js.syncfusion.com/demos/ejServices/api/OlapGrid/PdfExport)

It exports the PivotGrid control at the instant to PDF document.

### URL parameters

|  Parameter |  Description | 
|---|---|
|currentReport|It contains the current report as compressed string.|

### Response information 

Code: 200

Content-Type: application/json

Response: PDF document

### Code example 

```javascript


```

```csharp

public void PdfExport()
{
	PivotGridPDFExport pGrid = new PivotGridPDFExport();
	string args = HttpContext.Current.Request.Form.GetValues(0)[0];
	pGrid.ExportToPDF(string.Empty, args, HttpContext.Current.Response);
}
```
>The above example will export the PivotGrid as PDF file.

## WordExport

[POST&nbsp;&nbsp;/Api/OlapGrid/WordExport](http://js.syncfusion.com/demos/ejServices/api/OlapGrid/WordExport)

It exports the PivotGrid control at the instant to Word document.

### URL parameters

|  Parameter |  Description | 
|---|---|
|currentReport|It contains the current report as compressed string.|

### Response information 

Code: 200

Content-Type: application/json

Response: Word document

### Code example 

```javascript


```

```csharp

public void WordExport()
{
	PivotGridWordExport pGrid = new PivotGridWordExport();
	string args = HttpContext.Current.Request.Form.GetValues(0)[0];
	pGrid.ExportToWord(string.Empty, args, HttpContext.Current.Response);
}

```
>The above example will export the PivotGrid as Word file.

## CsvExport

[POST&nbsp;&nbsp;/Api/OlapGrid/CsvExport](http://js.syncfusion.com/demos/ejServices/api/OlapGrid/CsvExport)

It exports the PivotGrid control at the instant to CSV document.

### URL parameters

|  Parameter |  Description | 
|---|---|
|currentReport|It contains the current report as compressed string.|

### Response information 

Code: 200

Content-Type: application/json

Response: CSV document

### Code example 

```javascript



```
```csharp

public void CsvExport()
{
	PivotGridCSVExport pGrid = new PivotGridCSVExport();
	string args = HttpContext.Current.Request.Form.GetValues(0)[0];
	pGrid.ExportToCSV(string.Empty, args, HttpContext.Current.Response);
}

```

>The above example will export the PivotGrid as Csv file.
