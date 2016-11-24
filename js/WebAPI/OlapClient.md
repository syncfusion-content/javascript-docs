---
layout: post
title: webAPI reference for PivotClient
description: webAPI reference for PivotClient
documentation: API
platform: js-webapi
keywords: PivotClient, syncfusion, PivotClient webapi
---

## Initialize

[POST&nbsp;&nbsp;/Api/OlapClient/Initialize](http://js.syncfusion.com/demos/ejServices/api/OlapClient/Initialize)


### URL parameters

|  Parameter |  Description | 
|---|---|
|   |   |

### Response information 

Code: 

Content-Type: 

Response(JSON):

```javascript


```

### Code example 

```javascript


```

## InitializeGrid

[POST&nbsp;&nbsp;/Api/OlapClient/InitializeGrid](http://js.syncfusion.com/demos/ejServices/api/OlapClient/InitializeGrid)


### URL parameters

|  Parameter |  Description | 
|---|---|
|   |   |

### Response information 

Code: 

Content-Type: 

Response(JSON):

```javascript


```

### Code example 

```javascript


```
```csharp

public Dictionary<string, object> InitializeGrid(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    if (DataManager.ConnectionString.ToLower().Replace(" ", String.Empty).Split(';', '=').Contains("localeidentifier"))
    {
        DataManager.Culture = new System.Globalization.CultureInfo(cultureIDInfoval);
        DataManager.OverrideDefaultFormatStrings = true;
    }
    DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
    return jsonResult.ContainsKey("gridLayout") ? olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["gridLayout"].ToString()) : olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager);
}

```

## InitializeChart

[POST&nbsp;&nbsp;/Api/OlapClient/InitializeChart](http://js.syncfusion.com/demos/ejServices/api/OlapClient/InitializeChart)


### URL parameters

|  Parameter |  Description | 
|---|---|
|   |   |

### Response information 

Code: 

Content-Type: 

Response(JSON):

```javascript


```

### Code example 

```javascript



```
```csharp
public Dictionary<string, object> InitializeChart(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
    return chartHelper.GetJsonData(jsonResult["action"].ToString(), DataManager);
}
```

## InitializeTreeMap

[POST&nbsp;&nbsp;/Api/OlapClient/InitializeTreeMap](http://js.syncfusion.com/demos/ejServices/api/OlapClient/InitializeTreeMap)


### URL parameters

|  Parameter |  Description | 
|---|---|
|   |   |

### Response information 

Code: 

Content-Type: 

Response(JSON):

```javascript


```

### Code example 

```javascript


```
```csharp

public Dictionary<string, object> InitializeTreeMap(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
    return treeMapHelper.GetJsonData(jsonResult["action"].ToString(), DataManager);
}

```

## DrillChart

[POST&nbsp;&nbsp;/Api/OlapClient/DrillChart](http://js.syncfusion.com/demos/ejServices/api/OlapClient/DrillChart

### URL parameters

|  Parameter |  Description | 
|---|---|
|   |   |

### Response information 

Code: 

Content-Type: 

Response(JSON):

```javascript


```

### Code example 

```javascript

```
```csharp
public Dictionary<string, object> DrillChart(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["olapReport"].ToString()));
    DataManager.Reports = olapClientHelper.DeserializedReports(jsonResult["clientReports"].ToString());
    return chartHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["drilledSeries"].ToString());
}

```

## DrillTreeMap

[POST&nbsp;&nbsp;/Api/OlapClient/DrillTreeMap](http://js.syncfusion.com/demos/ejServices/api/OlapClient/DrillTreeMap)


### URL parameters

|  Parameter |  Description | 
|---|---|
|   |   |

### Response information 

Code: 

Content-Type: 

Response(JSON):

```javascript

```
```csharp

public Dictionary<string, object> DrillTreeMap(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["olapReport"].ToString()));
    DataManager.Reports = olapClientHelper.DeserializedReports(jsonResult["clientReports"].ToString());
    return treeMapHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["drillInfo"].ToString());
}

```

### Code example 

```javascript


```

## DrillGrid

[POST&nbsp;&nbsp;/Api/OlapClient/DrillGrid](http://js.syncfusion.com/demos/ejServices/api/OlapClient/DrillGrid)


### URL parameters

|  Parameter |  Description | 
|---|---|
|   |   |

### Response information 

Code: 

Content-Type: 

Response(JSON):

```javascript


```

### Code example 

```javascript

```
```csharp

public Dictionary<string, object> DrillGrid(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    if (DataManager.ConnectionString.ToLower().Replace(" ", String.Empty).Split(';', '=').Contains("localeidentifier"))
    {
        DataManager.Culture = new System.Globalization.CultureInfo(cultureIDInfoval);
        DataManager.OverrideDefaultFormatStrings = true;
    }
    DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
    DataManager.Reports = olapClientHelper.DeserializedReports(jsonResult["clientReports"].ToString());
    return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["cellPosition"].ToString(), jsonResult["headerInfo"].ToString(), jsonResult["layout"].ToString());
}

```

## FilterElement

[POST&nbsp;&nbsp;/Api/OlapClient/FilterElement](http://js.syncfusion.com/demos/ejServices/api/OlapClient/FilterElement)


### URL parameters

|  Parameter |  Description | 
|---|---|
|   |   |

### Response information 

Code: 

Content-Type: 

Response(JSON):

```javascript


```

### Code example 

```javascript


```
```csharp

public Dictionary<string, object> FilterElement(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["olapReport"].ToString()));
    DataManager.Reports = olapClientHelper.DeserializedReports(jsonResult["clientReports"].ToString());
    return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["clientParams"].ToString());
}

```

## RemoveSplitButton

[POST&nbsp;&nbsp;/Api/OlapClient/RemoveSplitButton](http://js.syncfusion.com/demos/ejServices/api/OlapClient/RemoveSplitButton)


### URL parameters

|  Parameter |  Description | 
|---|---|
|   |   |

### Response information 

Code: 

Content-Type: 

Response(JSON):

```javascript


```

### Code example 

```javascript


```
```csharp
public Dictionary<string, object> RemoveSplitButton(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["olapReport"].ToString()));
    DataManager.Reports = olapClientHelper.DeserializedReports(jsonResult["clientReports"].ToString());
    return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["clientParams"].ToString());
}
```

## FetchMemberTreeNodes

[POST&nbsp;&nbsp;/Api/OlapClient/FetchMemberTreeNodes](http://js.syncfusion.com/demos/ejServices/api/OlapClient/FetchMemberTreeNodes)


### URL parameters

|  Parameter |  Description | 
|---|---|
|   |   |

### Response information 

Code: 

Content-Type: 

Response(JSON):

```javascript


```

### Code example 

```javascript


```
```csharp

public Dictionary<string, object> FetchMemberTreeNodes(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["olapReport"].ToString()));
    return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["dimensionName"].ToString());
}

```

## DropNode

[POST&nbsp;&nbsp;/Api/OlapClient/DropNode](http://js.syncfusion.com/demos/ejServices/api/OlapClient/DropNode)


### URL parameters

|  Parameter |  Description | 
|---|---|
|   |   |

### Response information 

Code: 

Content-Type: 

Response(JSON):

```javascript


```

### Code example 

```javascript


```
```csharp

public Dictionary<string, object> DropNode(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["olapReport"].ToString()));
    DataManager.Reports = olapClientHelper.DeserializedReports(jsonResult["clientReports"].ToString());
    return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["dropType"].ToString(), jsonResult["nodeInfo"].ToString());
}

```

## CubeChange

[POST&nbsp;&nbsp;/Api/OlapClient/CubeChange](http://js.syncfusion.com/demos/ejServices/api/OlapClient/CubeChange)


### URL parameters

|  Parameter |  Description | 
|---|---|
|   |   |

### Response information 

Code: 

Content-Type: 

Response(JSON):

```javascript


```

### Code example 

```javascript


```
```csharp

public Dictionary<string, object> CubeChange(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    dynamic customData = serializer.Deserialize<dynamic>(jsonResult["customObject"].ToString());
    if (customData is Dictionary<string, object> && customData.ContainsKey("isPaging"))
    {
        DataManager.CurrentReport.EnablePaging = true;
        DataManager.CurrentReport.PagerOptions.SeriesPageSize = 5;
        DataManager.CurrentReport.PagerOptions.CategorialPageSize = 3;
    }
    return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["cubeName"].ToString(), jsonResult["clientParams"].ToString());
}

```

## MeasureGroup

[POST&nbsp;&nbsp;/Api/OlapClient/MeasureGroup](http://js.syncfusion.com/demos/ejServices/api/OlapClient/MeasureGroup)


### URL parameters

|  Parameter |  Description | 
|---|---|
|   |   |

### Response information 

Code: 

Content-Type: 

Response(JSON):

```javascript


```
```csharp

public Dictionary<string, object> MeasureGroup(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["measureGroupName"].ToString());
}

```

### Code example 

```javascript


```

## ToolbarOperations

[POST&nbsp;&nbsp;/Api/OlapClient/ToolbarOperations](http://js.syncfusion.com/demos/ejServices/api/OlapClient/ToolbarOperations)


### URL parameters

|  Parameter |  Description | 
|---|---|
|   |   |

### Response information 

Code: 

Content-Type: 

Response(JSON):

```javascript


```

### Code example 

```javascript


```

## ExpandMember

[POST&nbsp;&nbsp;/Api/OlapClient/ExpandMember](http://js.syncfusion.com/demos/ejServices/api/OlapClient/ExpandMember)


### URL parameters

|  Parameter |  Description | 
|---|---|
|   |   |

### Response information 

Code: 

Content-Type: 

Response(JSON):

```javascript


```
```csharp

public Dictionary<string, object> ExpandMember(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    if (!string.IsNullOrEmpty(jsonResult["olapReport"].ToString()))
        DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["olapReport"].ToString()));
    if (!string.IsNullOrEmpty(jsonResult["clientReports"].ToString()))
        DataManager.Reports = olapClientHelper.DeserializedReports(jsonResult["clientReports"].ToString());
    return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, Convert.ToBoolean(jsonResult["checkedStatus"].ToString()), jsonResult["parentNode"].ToString(), jsonResult["tag"].ToString(), jsonResult["dimensionName"].ToString(), jsonResult["cubeName"].ToString());
}

```
### Code example 

```javascript


```

## UpdateReport

[POST&nbsp;&nbsp;/Api/OlapClient/UpdateReport](http://js.syncfusion.com/demos/ejServices/api/OlapClient/UpdateReport)


### URL parameters

|  Parameter |  Description | 
|---|---|
|   |   |

### Response information 

Code: 

Content-Type: 

Response(JSON):

```javascript


```

### Code example 

```javascript


```
```csharp

public Dictionary<string, object> UpdateReport(Dictionary<string, object> jsonResult)
{
    return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), jsonResult["clientParams"].ToString(), jsonResult["olapReport"].ToString(), jsonResult["clientReports"].ToString());
}

```
## SaveReportToDB

[POST&nbsp;&nbsp;/Api/OlapClient/SaveReportToDB](http://js.syncfusion.com/demos/ejServices/api/OlapClient/SaveReportToDB)


### URL parameters

|  Parameter |  Description | 
|---|---|
|   |   |

### Response information 

Code: 

Content-Type: 

Response(JSON):

```javascript


```

### Code example 

```javascript


```

## FetchReportListFromDB

[POST&nbsp;&nbsp;/Api/OlapClient/FetchReportListFromDB](http://js.syncfusion.com/demos/ejServices/api/OlapClient/FetchReportListFromDB)


### URL parameters

|  Parameter |  Description | 
|---|---|
|   |   |

### Response information 

Code: 

Content-Type: 

Response(JSON):

```javascript


```

### Code example 

```javascript


```
## LoadReportFromDB

[POST&nbsp;&nbsp;/Api/OlapClient/LoadReportFromDB](http://js.syncfusion.com/demos/ejServices/api/OlapClient/LoadReportFromDB)


### URL parameters

|  Parameter |  Description | 
|---|---|
|   |   |

### Response information 

Code: 

Content-Type: 

Response(JSON):

```javascript


```

### Code example 

```javascript


```
```csharp

```
## Export

[POST&nbsp;&nbsp;/Api/OlapClient/Export](http://js.syncfusion.com/demos/ejServices/api/OlapClient/Export)


### URL parameters

|  Parameter |  Description | 
|---|---|
|   |   |

### Response information 

Code: 

Content-Type: 

Response(JSON):

```javascript


```

### Code example 

```javascript


```
```csharp

public void Export()
{
    PivotClientExport olapClient = new PivotClientExport();
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    olapClient.ExportPivotClient(string.Empty, args, HttpContext.Current.Response);
}

```
## ExportOlapClient

[POST&nbsp;&nbsp;/Api/OlapClient/ExportOlapClient](http://js.syncfusion.com/demos/ejServices/api/OlapClient/ExportOlapClient)


### URL parameters

|  Parameter |  Description | 
|---|---|
|   |   |

### Response information 

Code: 

Content-Type: 

Response(JSON):

```javascript


```

### Code example 

```javascript


```
```csharp

public void ExportOlapClient()
{
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    string fileName = "Sample";
    olapClientHelper.ExportPivotClient(DataManager, args, fileName, System.Web.HttpContext.Current.Response);
}

```
## GetMDXQuery

[POST&nbsp;&nbsp;/Api/OlapClient/GetMDXQuery](http://js.syncfusion.com/demos/ejServices/api/OlapClient/GetMDXQuery)


### URL parameters

|  Parameter |  Description | 
|---|---|
|   |   |

### Response information 

Code: 

Content-Type: 

Response(JSON):

```javascript


```

### Code example 

```javascript


```
```csharp

public string GetMDXQuery(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["olapReport"].ToString()));
    return DataManager.GetMDXQuery();
}

```
## ToggleAxis

[POST&nbsp;&nbsp;/Api/OlapClient/ToggleAxis](http://js.syncfusion.com/demos/ejServices/api/OlapClient/ToggleAxis)


### URL parameters

|  Parameter |  Description | 
|---|---|
|   |   |

### Response information 

Code: 

Content-Type: 

Response(JSON):

```javascript


```

### Code example 

```javascript


```
```csharp

public Dictionary<string, object> ToggleAxis(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
    DataManager.Reports = olapClientHelper.DeserializedReports(jsonResult["clientReports"].ToString());
    DataManager.ToggleAxis(DataManager.CurrentReport);
    return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["clientReports"].ToString());
}

```
## Paging

[POST&nbsp;&nbsp;/Api/OlapClient/Paging](http://js.syncfusion.com/demos/ejServices/api/OlapClient/Paging)


### URL parameters

|  Parameter |  Description | 
|---|---|
|   |   |

### Response information 

Code: 

Content-Type: 

Response(JSON):

```javascript


```

### Code example 

```javascript


```
```csharp

public Dictionary<string, object> Paging(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.SetPaging(jsonResult["currentReport"].ToString(), jsonResult["pagingInfo"].ToString()));
    return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["layout"].ToString());
}

```
