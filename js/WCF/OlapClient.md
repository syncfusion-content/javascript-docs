---
layout: post
title: WCF reference for PivotClient
description: WCF reference for PivotClient
documentation: ug
platform: js
keywords: PivotClient, syncfusion, PivotClient WCF
---

## Initialize

 [POST] [/WCF/PivotClient/Initialize](http://js.syncfusion.com/demos/ejServices/wcf/PivotClient/Olap.svc/Initialize)

It fetches the data required to render the PivotClient control initially.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|customObject|It contains the custom object passed from client side|
|clientParams|It contains the information about the control for initial rendering|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string

### Code example 

{% highlight c# %}

public Dictionary<string, object> Initialize(string action, string customObject, string clientParams)
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
    return olapClientHelper.GetJsonData(action, DataManager, clientParams);
}

{% endhighlight %} 

## InitializeGrid

 [POST] [/WCF/PivotClient/InitializeGrid](http://js.syncfusion.com/demos/ejServices/wcf/PivotClient/Olap.svc/InitializeGrid)

It fetches the data required to render the PivotGrid control inside PivotClient.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|currentReport|It contains the current report as compressed string|
|gridLayout|It contains the layout of PivotGrid control|
|customObject|It contains the custom object passed from client side|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string

### Code example 

{% highlight c# %}

public Dictionary<string, object> InitializeGrid(string action, string currentReport, string gridLayout, string customObject)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    if (DataManager.ConnectionString.ToLower().Replace(" ", String.Empty).Split(';', '=').Contains("localeidentifier"))
    {
        DataManager.Culture = new System.Globalization.CultureInfo(cultureIDInfoval);
        DataManager.OverrideDefaultFormatStrings = true;
    }
    DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(currentReport));
    return olapClientHelper.GetJsonData(action, DataManager, gridLayout);
}

{% endhighlight %} 

## InitializeChart

 [POST] [/WCF/PivotClient/InitializeChart](http://js.syncfusion.com/demos/ejServices/wcf/PivotClient/Olap.svc/InitializeChart)

It fetches the data required to render the PivotChart control inside PivotClient.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|currentReport|It contains the current report as compressed string|
|customObject|It contains the custom object passed from client side|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string

### Code example 

{% highlight c# %}

public Dictionary<string, object> InitializeChart(string action, string currentReport, string customObject)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(currentReport));
    return chartHelper.GetJsonData(action, DataManager);
}

{% endhighlight %} 

## InitializeTreeMap

 [POST] [/WCF/PivotClient/InitializeTreeMap](http://js.syncfusion.com/demos/ejServices/wcf/PivotClient/Olap.svc/InitializeTreeMap)

It fetches the data required to render the PivotTreeMap control inside PivotClient.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|currentReport|It contains the current report as compressed string|
|customObject|It contains the custom object passed from client side|


### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string

### Code example 

{% highlight c# %}

public Dictionary<string, object> InitializeTreeMap(string action, string currentReport, string customObject)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(currentReport));
    return treemapHelper.GetJsonData(action, DataManager);
}

{% endhighlight %} 

## DrillChart

 [POST] [/WCF/PivotClient/DrillChart](http://js.syncfusion.com/demos/ejServices/wcf/PivotClient/Olap.svc/DrillChart)

It fetches the drilled data required to render the PivotChart on drilling.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|drilledSeries|It contains the name of the drilled member|
|olapReport|It contains the current report as compressed string|
|clientReports|It contains the report collection as compressed string|


### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string

### Code example 

{% highlight c# %}

public Dictionary<string, object> DrillChart(string action, string drilledSeries, string olapReport, string clientReports)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(olapReport));
    DataManager.Reports = olapClientHelper.DeserializedReports(clientReports);
    return chartHelper.GetJsonData(action, DataManager, drilledSeries);
}

{% endhighlight %} 

## DrillTreeMap

 [POST] [/WCF/PivotClient/DrillTreeMap](http://js.syncfusion.com/demos/ejServices/wcf/PivotClient/Olap.svc/DrillTreeMap)

It fetches the drilled data required to render the PivotTreeMap on drilling.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|drillInfo|It contains the drilled information|
|olapReport|It contains the current report as compressed string|
|clientReports|It contains the report collection at that instant|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string

### Code example 

{% highlight c# %}

public Dictionary<string, object> DrillTreeMap(string action, string drillInfo, string olapReport, string clientReports)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(olapReport));
    DataManager.Reports = olapClientHelper.DeserializedReports(clientReports);
    return treemapHelper.GetJsonData(action, DataManager, drillInfo);
}

{% endhighlight %} 

## DrillGrid

 [POST] [/WCF/PivotClient/DrillGrid](http://js.syncfusion.com/demos/ejServices/wcf/PivotClient/Olap.svc/DrillGrid)

It fetches the drilled data required to render the PivotGrid on drilling.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|cellPosition|It holds the position of the cell drilled|
|currentReport|It contains the current report as compressed string|
|clientReports|It contains the report collection at that instant|
|headerInfo|It contains the information about the drilled member|
|layout|It contains the layout of PivotGrid control|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string

### Code example 

{% highlight c# %}

public Dictionary<string, object> DrillGrid(string action, string cellPosition, string currentReport, string clientReports, string headerInfo, string layout)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    if (DataManager.ConnectionString.ToLower().Replace(" ", String.Empty).Split(';', '=').Contains("localeidentifier"))
    {
        DataManager.Culture = new System.Globalization.CultureInfo(cultureIDInfoval);
        DataManager.OverrideDefaultFormatStrings = true;
    }
    DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(currentReport));
    DataManager.Reports = olapClientHelper.DeserializedReports(clientReports);
    return olapClientHelper.GetJsonData(action, DataManager, cellPosition, headerInfo, layout);
}

{% endhighlight %} 

## FilterElement

 [POST] [/WCF/PivotClient/FilterElement](http://js.syncfusion.com/demos/ejServices/wcf/PivotClient/Olap.svc/FilterElement)

It fetches the filtered data required to render the control after performing filtering.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|clientParams|It contains the information about the filter action performed|
|olapReport|It contains the current report as compressed string|
|clientReports|It contains the report collection at that instant|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string

### Code example 

{% highlight c# %}

public Dictionary<string, object> FilterElement(string action, string clientParams, string olapReport, string clientReports)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(olapReport));
    DataManager.Reports = olapClientHelper.DeserializedReports(clientReports);
    return olapClientHelper.GetJsonData(action, DataManager, clientParams);
}

{% endhighlight %} 

## RemoveSplitButton

 [POST] [/WCF/PivotClient/RemoveSplitButton](http://js.syncfusion.com/demos/ejServices/wcf/PivotClient/Olap.svc/RemoveSplitButton)

It fetches the drilled data required to render the PivotChart on removing an item from report.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|clientParams|It contains the information about the removed item|
|olapReport|It contains the current report as compressed string|
|clientReports|It contains the report collection at that instant|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string

### Code example 

{% highlight c# %}

public Dictionary<string, object> RemoveSplitButton(string action, string clientParams, string olapReport, string clientReports)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(olapReport));
    DataManager.Reports = olapClientHelper.DeserializedReports(clientReports);
    return olapClientHelper.GetJsonData(action, DataManager, clientParams);
}

{% endhighlight %} 

## FetchMemberTreeNodes

 [POST] [/WCF/PivotClient/FetchMemberTreeNodes](http://js.syncfusion.com/demos/ejServices/wcf/PivotClient/Olap.svc/FetchMemberTreeNodes)

It fetches the details of the members to render the member editor dialog.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|dimensionName|It contains the hierarchy name|
|olapReport|It contains the current report as compressed string|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string

### Code example 

{% highlight c# %}

public Dictionary<string, object> FetchMemberTreeNodes(string action, string dimensionName, string olapReport)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(olapReport));
    return olapClientHelper.GetJsonData(action, DataManager, dimensionName);
}

{% endhighlight %} 

## DropNode

 [POST] [/WCF/PivotClient/DropNode](http://js.syncfusion.com/demos/ejServices/wcf/PivotClient/Olap.svc/DropNode)

It fetches the data required to render the control after drag and drop action.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|dropType|It tells whether the dropped item is a node or pivot button|
|nodeInfo|It contains the information about the dropped item|
|olapReport|It contains the current report as compressed string|
|clientReports|It contains the report collection at that instant|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string

### Code example 

{% highlight c# %}

public Dictionary<string, object> DropNode(string action, string dropType, string nodeInfo, string olapReport, string clientReports)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(olapReport));
    DataManager.Reports = olapClientHelper.DeserializedReports(clientReports);
    return olapClientHelper.GetJsonData(action, DataManager, dropType, nodeInfo);
}

{% endhighlight %} 

## CubeChange

 [POST] [/WCF/PivotClient/CubeChange](http://js.syncfusion.com/demos/ejServices/wcf/PivotClient/Olap.svc/CubeChange)

It fetches the data required to render the control on changing the cube.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|cubeName|It contains the cube name|
|clientParams|It contains the information of the cube selected|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string

### Code example 

{% highlight c# %}

public Dictionary<string, object> CubeChange(string action, string cubeName, string clientParams)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    return olapClientHelper.GetJsonData(action, DataManager, cubeName, clientParams);
}

{% endhighlight %} 

## MeasureGroup

 [POST] [/WCF/PivotClient/MeasureGroup](http://js.syncfusion.com/demos/ejServices/wcf/PivotClient/Olap.svc/MeasureGroup)

It fetches the data required to render the control on changing the measure group.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|measureGroupName|It contains the measure group selected|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string

### Code example 

{% highlight c# %}

public Dictionary<string, object> MeasureGroup(string action, string measureGroupName)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    return olapClientHelper.GetJsonData(action, DataManager, measureGroupName);
}

{% endhighlight %} 

## ToolbarOperations

 [POST] [/WCF/PivotClient/ToolbarOperations](http://js.syncfusion.com/demos/ejServices/wcf/PivotClient/Olap.svc/ToolbarOperations)

It fetches the data required to render the control on performing toolbar operations.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|toolbarOperation|It contains name of the operation performed|
|clientInfo|It contains the information about the operation performed|
|olapReport|It contains the current report as compressed string|
|clientReports|It contains the report collection at that instant|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string

### Code example 

{% highlight c# %}

public Dictionary<string, object> ToolbarOperations(string action, string toolbarOperation, string clientInfo, string olapReport, string clientReports)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    if (!string.IsNullOrEmpty(olapReport))
        DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(olapReport));
    if (!string.IsNullOrEmpty(clientReports))
        DataManager.Reports = olapClientHelper.DeserializedReports(clientReports);
    return olapClientHelper.GetJsonData(action, DataManager, toolbarOperation, clientInfo);
}

{% endhighlight %} 

## ExpandMember

 [POST] [/WCF/PivotClient/ExpandMember](http://js.syncfusion.com/demos/ejServices/wcf/PivotClient/Olap.svc/ExpandMember)

It fetches the children nodes on expanding a node in Member Editor.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|checkedStatus|It contains the checked status of the member in member editor|
|parentNode|It contains the name of member expanded|
|tag|It contains the information of the member expanded|
|dimensionName|It contains the hierarchy name|
|cubeName|It contains the cube name|
|olapReport|It contains the current report as compressed string|
|clientReports|It contains the report collection at that instant|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string

### Code example 

{% highlight c# %}

public Dictionary<string, object> ExpandMember(string action, bool checkedStatus, string parentNode, string tag, string dimensionName, string cubeName, string olapReport, string clientReports)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    if (!string.IsNullOrEmpty(olapReport))
        DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(olapReport));
    if (!string.IsNullOrEmpty(clientReports))
        DataManager.Reports = olapClientHelper.DeserializedReports(clientReports);
    return olapClientHelper.GetJsonData(action, DataManager, checkedStatus, parentNode, tag, dimensionName, cubeName);
}

{% endhighlight %} 

## UpdateReport

 [POST] [/WCF/PivotClient/UpdateReport](http://js.syncfusion.com/demos/ejServices/wcf/PivotClient/Olap.svc/UpdateReport)

It updates the report in server side.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|clientParams|It contains the information required to update the report|
|olapReport|It contains the current report as compressed string|
|clientReports|It contains the report collection at that instant|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string

### Code example 

{% highlight c# %}

public Dictionary<string, object> UpdateReport(string action, string clientParams, string olapReport, string clientReports)
{
    return olapClientHelper.GetJsonData(action, clientParams, olapReport, clientReports);
}

{% endhighlight %} 

## SaveReportToDB

 [POST] [/WCF/PivotClient/SaveReportToDB](http://js.syncfusion.com/demos/ejServices/wcf/PivotClient/Olap.svc/SaveReportToDB)

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

{% highlight c# %}

public Dictionary<string, object> SaveReportToDB(string reportName, string operationalMode, string analysisMode, string olapReport, string clientReports)
{
    reportName = reportName + "##" + operationalMode.ToLower() + "#>>#" + analysisMode.ToLower();
    bool isDuplicate = true;
    SqlCeConnection con = new SqlCeConnection() { ConnectionString = conStringforDB };
    con.Open();
    SqlCeCommand cmd1 = null;
    foreach (DataRow row in GetDataTable().Rows)
    {
        if ((row.ItemArray[0] as string).Equals(reportName))
        {
            isDuplicate = false;
            cmd1 = new SqlCeCommand("update ReportsTable set Report=@Reports where ReportName like @ReportName", con);
        }
    }
    if (isDuplicate)
    {
        cmd1 = new SqlCeCommand("insert into ReportsTable Values(@ReportName,@Reports)", con);
    }
    cmd1.Parameters.Add("@ReportName", reportName);
    if (operationalMode.ToLower() == "servermode" && analysisMode == "olap")
        cmd1.Parameters.Add("@Reports", OLAPUTILS.Utils.GetReportStream(clientReports).ToArray());
    else
        cmd1.Parameters.Add("@Reports", Encoding.UTF8.GetBytes(clientReports).ToArray());
    cmd1.ExecuteNonQuery();
    con.Close();
    return null;
}

{% endhighlight %} 

## FetchReportListFromDB

 [POST] [/WCF/PivotClient/FetchReportListFromDB](http://js.syncfusion.com/demos/ejServices/wcf/PivotClient/Olap.svc/FetchReportListFromDB)

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

{% highlight c# %}

public Dictionary<string, object> FetchReportListFromDB(string operationalMode, string analysisMode)
{
    string reportNames = string.Empty;
    string currentRptName = string.Empty;
    foreach (System.Data.DataRow row in GetDataTable().Rows)
    {
        currentRptName = (row.ItemArray[0] as string);
        if (currentRptName.IndexOf("##" + operationalMode + "#>>#" + analysisMode) >= 0)
        {
            currentRptName = currentRptName.Replace("##" + operationalMode + "#>>#" + analysisMode, "");
            reportNames = reportNames == "" ? currentRptName : reportNames + "__" + currentRptName;
        }
    }
    Dictionary<string, object> dictionary = new Dictionary<string, object>();
    dictionary.Add("ReportNameList", reportNames);
    return dictionary;
}

{% endhighlight %} 

## LoadReportFromDB

 [POST] [/WCF/PivotClient/LoadReportFromDB](http://js.syncfusion.com/demos/ejServices/wcf/PivotClient/Olap.svc/LoadReportFromDB)

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

{% highlight c# %}

public Dictionary<string, object> LoadReportFromDB(string reportName, string operationalMode, string analysisMode, string olapReport, string clientReports)
{
    PivotReport report = new PivotReport();
    Dictionary<string, object> dictionary = new Dictionary<string, object>();
    string currentRptName = string.Empty;
    foreach (DataRow row in GetDataTable().Rows)
    {
        currentRptName = (row.ItemArray[0] as string).Replace("##" + operationalMode.ToLower() + "#>>#" + analysisMode.ToLower(), "");
        if (currentRptName.Equals(reportName))
        {
            if (operationalMode.ToLower() == "servermode" && analysisMode == "olap")
            {
                var reportString = "";
                OlapDataManager DataManager = new OlapDataManager(connectionString);
                reportString = OLAPUTILS.Utils.CompressData(row.ItemArray[1] as byte[]);
                DataManager.Reports = olapClientHelper.DeserializedReports(reportString);
                DataManager.SetCurrentReport(DataManager.Reports[0]);
                return olapClientHelper.GetJsonData("toolbarOperation", DataManager, "Load Report", reportName);
            }
            else
            {
                byte[] reportString = new byte[2 * 1024];
                reportString = (row.ItemArray[1] as byte[]);
                if (analysisMode.ToLower() == "pivot" && operationalMode.ToLower() == "servermode")
                    dictionary = olapClientHelper.GetJsonData("LoadReport", ProductSales.GetSalesData(), Encoding.UTF8.GetString(reportString));
                else
                    dictionary.Add("report", Encoding.UTF8.GetString(reportString));
                break;
            }
        }
    }
    return dictionary;
}
        
{% endhighlight %} 

## GetMDXQuery

 [POST] [/WCF/PivotClient/GetMDXQuery](http://js.syncfusion.com/demos/ejServices/wcf/PivotClient/Olap.svc/GetMDXQuery)

It retrieves the MDX query formed to fetch the data at that instant.

### URL parameters

|  Parameter |  Description | 
|---|---|
|olapReport|It contains the current report as compressed string|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string

### Code example 

{% highlight c# %}

public string GetMDXQuery(string olapReport)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(olapReport));
    return DataManager.GetMDXQuery();
}

{% endhighlight %} 

## ToggleAxis

 [POST] [/WCF/PivotClient/ToggleAxis](http://js.syncfusion.com/demos/ejServices/wcf/PivotClient/Olap.svc/ToggleAxis)

It fetches the data after interchanging the elements in row and column axes.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|currentReport|It contains the current report as compressed string|
|clientReports|It contains the report collection at that instant|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string

### Code example 

{% highlight c# %}

public Dictionary<string, object> ToggleAxis(string action, string currentReport, string clientReports)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(currentReport));
    DataManager.Reports = olapClientHelper.DeserializedReports(clientReports);
    DataManager.ToggleAxis(DataManager.CurrentReport);
    return olapClientHelper.GetJsonData(action, DataManager, clientReports);
}

{% endhighlight %} 