---
layout: post
title: webAPI reference for PivotClient
description: webAPI reference for PivotClient
documentation: ug
platform: js
keywords: PivotClient, syncfusion, PivotClient webapi
---

## Initialize

 [POST] [/Api/OlapClient/Initialize](http://js.syncfusion.com/demos/ejServices/api/OlapClient/Initialize)

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
public Dictionary<string, object> Initialize(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(CreateOlapReport());
    return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["clientParams"].ToString())
}

{% endhighlight %}

## InitializeGrid

 [POST] [/Api/OlapClient/InitializeGrid](http://js.syncfusion.com/demos/ejServices/api/OlapClient/InitializeGrid)

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
public Dictionary<string, object> InitializeGrid(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
    return jsonResult.ContainsKey("gridLayout") ? olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["gridLayout"].ToString()) : olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager);
}

{% endhighlight %}

## InitializeChart

 [POST] [/Api/OlapClient/InitializeChart](http://js.syncfusion.com/demos/ejServices/api/OlapClient/InitializeChart)

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
public Dictionary<string, object> InitializeChart(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
    return chartHelper.GetJsonData(jsonResult["action"].ToString(), DataManager);
}
{% endhighlight %}

## InitializeTreeMap

 [POST] [/Api/OlapClient/InitializeTreeMap](http://js.syncfusion.com/demos/ejServices/api/OlapClient/InitializeTreeMap)

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
public Dictionary<string, object> InitializeTreeMap(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
    return treeMapHelper.GetJsonData(jsonResult["action"].ToString(), DataManager);
}

{% endhighlight %}

## DrillChart

 [POST] [/Api/OlapClient/DrillChart](http://js.syncfusion.com/demos/ejServices/api/OlapClient/DrillChart

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
public Dictionary<string, object> DrillChart(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["olapReport"].ToString()));
    DataManager.Reports = olapClientHelper.DeserializedReports(jsonResult["clientReports"].ToString());
    return chartHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["drilledSeries"].ToString());
}

{% endhighlight %}

## DrillTreeMap

 [POST] [/Api/OlapClient/DrillTreeMap](http://js.syncfusion.com/demos/ejServices/api/OlapClient/DrillTreeMap)

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
public Dictionary<string, object> DrillTreeMap(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["olapReport"].ToString()));
    DataManager.Reports = olapClientHelper.DeserializedReports(jsonResult["clientReports"].ToString());
    return treeMapHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["drillInfo"].ToString());
}

{% endhighlight %}

## DrillGrid

 [POST] [/Api/OlapClient/DrillGrid](http://js.syncfusion.com/demos/ejServices/api/OlapClient/DrillGrid)

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
public Dictionary<string, object> DrillGrid(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
    DataManager.Reports = olapClientHelper.DeserializedReports(jsonResult["clientReports"].ToString());
    return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["cellPosition"].ToString(), jsonResult["headerInfo"].ToString(), jsonResult["layout"].ToString());
}

{% endhighlight %}

## FilterElement

 [POST] [/Api/OlapClient/FilterElement](http://js.syncfusion.com/demos/ejServices/api/OlapClient/FilterElement)

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
public Dictionary<string, object> FilterElement(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["olapReport"].ToString()));
    DataManager.Reports = olapClientHelper.DeserializedReports(jsonResult["clientReports"].ToString());
    return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["clientParams"].ToString());
}

{% endhighlight %}

## RemoveSplitButton

 [POST] [/Api/OlapClient/RemoveSplitButton](http://js.syncfusion.com/demos/ejServices/api/OlapClient/RemoveSplitButton)

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
public Dictionary<string, object> RemoveSplitButton(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["olapReport"].ToString()));
    DataManager.Reports = olapClientHelper.DeserializedReports(jsonResult["clientReports"].ToString());
    return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["clientParams"].ToString());
}

{% endhighlight %}

## FetchMemberTreeNodes

 [POST] [/Api/OlapClient/FetchMemberTreeNodes](http://js.syncfusion.com/demos/ejServices/api/OlapClient/FetchMemberTreeNodes)

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
public Dictionary<string, object> FetchMemberTreeNodes(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["olapReport"].ToString()));
    return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["dimensionName"].ToString());
}

{% endhighlight %}

## DropNode

 [POST] [/Api/OlapClient/DropNode](http://js.syncfusion.com/demos/ejServices/api/OlapClient/DropNode)

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
public Dictionary<string, object> DropNode(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["olapReport"].ToString()));
    DataManager.Reports = olapClientHelper.DeserializedReports(jsonResult["clientReports"].ToString());
    return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["dropType"].ToString(), jsonResult["nodeInfo"].ToString());
}

{% endhighlight %}

## CubeChange

 [POST] [/Api/OlapClient/CubeChange](http://js.syncfusion.com/demos/ejServices/api/OlapClient/CubeChange)

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
public Dictionary<string, object> CubeChange(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["cubeName"].ToString(), jsonResult["clientParams"].ToString());
}

{% endhighlight %}

## MeasureGroup

 [POST] [/Api/OlapClient/MeasureGroup](http://js.syncfusion.com/demos/ejServices/api/OlapClient/MeasureGroup)

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
public Dictionary<string, object> MeasureGroup(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["measureGroupName"].ToString());
}

{% endhighlight %}

## ToolbarOperations

 [POST] [/Api/OlapClient/ToolbarOperations](http://js.syncfusion.com/demos/ejServices/api/OlapClient/ToolbarOperations)

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
public Dictionary<string, object> ToolbarOperations(Dictionary<string, object> jsonResult)
{
    var toolbarOperation = "";
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    if ((jsonResult["olapReport"]) != null && !string.IsNullOrEmpty(jsonResult["olapReport"].ToString()))
        DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["olapReport"].ToString()));
    if ((jsonResult["clientReports"]) != null && !string.IsNullOrEmpty(jsonResult["clientReports"].ToString()))
        DataManager.Reports = olapClientHelper.DeserializedReports(jsonResult["clientReports"].ToString());
    toolbarOperation = jsonResult["toolbarOperation"] == null ? null : jsonResult["toolbarOperation"].ToString();
    return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, toolbarOperation, jsonResult["clientInfo"].ToString());
}

{% endhighlight %}

## ExpandMember

 [POST] [/Api/OlapClient/ExpandMember](http://js.syncfusion.com/demos/ejServices/api/OlapClient/ExpandMember)

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
public Dictionary<string, object> ExpandMember(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    if (!string.IsNullOrEmpty(jsonResult["olapReport"].ToString()))
        DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["olapReport"].ToString()));
    if (!string.IsNullOrEmpty(jsonResult["clientReports"].ToString()))
        DataManager.Reports = olapClientHelper.DeserializedReports(jsonResult["clientReports"].ToString());
    return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, Convert.ToBoolean(jsonResult["checkedStatus"].ToString()), jsonResult["parentNode"].ToString(), jsonResult["tag"].ToString(), jsonResult["dimensionName"].ToString(), jsonResult["cubeName"].ToString());
}

{% endhighlight %}

## UpdateReport

 [POST] [/Api/OlapClient/UpdateReport](http://js.syncfusion.com/demos/ejServices/api/OlapClient/UpdateReport)

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
public Dictionary<string, object> UpdateReport(Dictionary<string, object> jsonResult)
{
    return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), jsonResult["clientParams"].ToString(), jsonResult["olapReport"].ToString(), jsonResult["clientReports"].ToString());
}

{% endhighlight %}

## SaveReportToDB

 [POST] [/Api/OlapClient/SaveReportToDB](http://js.syncfusion.com/demos/ejServices/api/OlapClient/SaveReportToDB)

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
public Dictionary<string, object> SaveReportToDB(Dictionary<string, object> jsonResult)
{
    string operationalMode = jsonResult["operationalMode"].ToString(), analysisMode = jsonResult["analysisMode"].ToString(), reportName = string.Empty;
    bool isDuplicate = true;
    SqlCeConnection con = new SqlCeConnection() { ConnectionString = conStringforDB };
    con.Open();
    reportName = jsonResult["reportName"].ToString() + "##" + operationalMode.ToLower() + "#>>#" + analysisMode.ToLower();
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
        cmd1.Parameters.Add("@Reports", Syncfusion.JavaScript.Olap.Utils.GetReportStream(jsonResult["clientReports"].ToString()).ToArray());
    else
        cmd1.Parameters.Add("@Reports", Encoding.UTF8.GetBytes(jsonResult["clientReports"].ToString()).ToArray());
    cmd1.ExecuteNonQuery();
    con.Close();
    return null;
}

{% endhighlight %}

## FetchReportListFromDB

 [POST] [/Api/OlapClient/FetchReportListFromDB](http://js.syncfusion.com/demos/ejServices/api/OlapClient/FetchReportListFromDB)

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
public Dictionary<string, object> FetchReportListFromDB(Dictionary<string, object> jsonResult)
{
    string reportNames = string.Empty, currentRptName = string.Empty, operationalMode = jsonResult["operationalMode"].ToString(), analysisMode = jsonResult["analysisMode"].ToString();
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

 [POST] [/Api/OlapClient/LoadReportFromDB](http://js.syncfusion.com/demos/ejServices/api/OlapClient/LoadReportFromDB)

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
public Dictionary<string, object> LoadReportFromDB(Dictionary<string, object> jsonResult)
{
    PivotReport report = new PivotReport();
    string operationalMode = jsonResult["operationalMode"].ToString(), analysisMode = jsonResult["analysisMode"].ToString();
    Dictionary<string, object> dictionary = new Dictionary<string, object>();
    string currentRptName = string.Empty;
    foreach (DataRow row in GetDataTable().Rows)
    {
        currentRptName = (row.ItemArray[0] as string).Replace("##" + operationalMode.ToLower() + "#>>#" + analysisMode.ToLower(), "");
        if (currentRptName.Equals(jsonResult["reportName"].ToString()))
        {
            if (operationalMode.ToLower() == "servermode" && analysisMode == "olap")
            {
                var reportString = "";
                OlapDataManager DataManager = new OlapDataManager(connectionString);
                reportString = Syncfusion.JavaScript.Olap.Utils.CompressData(row.ItemArray[1] as byte[]);
                DataManager.Reports = olapClientHelper.DeserializedReports(reportString);
                DataManager.SetCurrentReport(DataManager.Reports[0]);
                return olapClientHelper.GetJsonData("toolbarOperation", DataManager, "Load Report", jsonResult["reportName"].ToString());
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

## Export

 [POST] [/Api/OlapClient/Export](http://js.syncfusion.com/demos/ejServices/api/OlapClient/Export)

It exports the PivotGrid or PivotChart or both to the selected format.

### URL parameters

|  Parameter |  Description | 
|---|---|
|args|It contains necessary information to export the PivotClient control to the specified format|

### Response information 

Code: 200

Content-Type: application/json

Response: file

### Code example 

{% highlight c# %}

public void Export()
{
    PivotClientExport olapClient = new PivotClientExport();
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    olapClient.ExportPivotClient(string.Empty, args, HttpContext.Current.Response);
}

{% endhighlight %}

## ExportOlapClient

 [POST] [/Api/OlapClient/ExportOlapClient](http://js.syncfusion.com/demos/ejServices/api/OlapClient/ExportOlapClient)

It exports the PivotGrid or PivotChart or both with OLAP data to the selected format.

### URL parameters

|  Parameter |  Description | 
|---|---|
|args|It contains the current report as serialized string for exporting process|

### Response information 

Code: 200

Content-Type: application/json

Response: file

### Code example 

{% highlight c# %}
public void ExportOlapClient()
{
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    string fileName = "Sample";
    olapClientHelper.ExportPivotClient(DataManager, args, fileName, System.Web.HttpContext.Current.Response);
}

{% endhighlight %}

## GetMDXQuery

 [POST] [/Api/OlapClient/GetMDXQuery](http://js.syncfusion.com/demos/ejServices/api/OlapClient/GetMDXQuery)

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
public string GetMDXQuery(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["olapReport"].ToString()));
    return DataManager.GetMDXQuery();
}

{% endhighlight %}

## ToggleAxis

 [POST] [/Api/OlapClient/ToggleAxis](http://js.syncfusion.com/demos/ejServices/api/OlapClient/ToggleAxis)

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
public Dictionary<string, object> ToggleAxis(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
    DataManager.Reports = olapClientHelper.DeserializedReports(jsonResult["clientReports"].ToString());
    DataManager.ToggleAxis(DataManager.CurrentReport);
    return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["clientReports"].ToString());
}

{% endhighlight %}

## Paging

 [POST] [/Api/OlapClient/Paging](http://js.syncfusion.com/demos/ejServices/api/OlapClient/Paging)

It fetches the data on navigating between pages in PivotClient with OLAP data.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It contains the current action as string|
|currentReport|It contains the report at that instant as serialized string|
|layout|It holds the layout of the PivotGrid control|
|pagingInfo|It contains the page number to which the control needs to be moved|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string

### Code example 

{% highlight c# %}
public Dictionary<string, object> Paging(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.SetPaging(jsonResult["currentReport"].ToString(), jsonResult["pagingInfo"].ToString()));
    return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["layout"].ToString());
}

{% endhighlight %}
