---
layout: post
title: WCF reference for PivotClient
description: WCF reference for PivotClient
documentation: ug
platform: js
keywords: PivotClient, syncfusion, PivotClient WCF
---

## Initialize

 [POST] [/WCF/PivotClient/Initialize](http://js.syncfusion.com/demos/ejServices/wcf/PivotClient/Relational.svc/Initialize)

It fetches the data required to render the PivotClient control initially.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string

### Code example 

{% highlight c# %}

public Dictionary<string, object> Initialize(string action)
{
    BindData();
    return pivotClient.GetJsonData(action, ProductSales.GetSalesData(), null);
}


{% endhighlight %} 

## DrillChart

 [POST] [/WCF/PivotClient/DrillChart](http://js.syncfusion.com/demos/ejServices/wcf/PivotClient/Relational.svc/DrillChart)

It fetches the drilled data required to render the PivotChart on drilling.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|drilledSeries|It contains the name of the drilled member|
|currentReport|It contains the current report as compressed string|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string

### Code example 

{% highlight c# %}

public Dictionary<string, object> DrillChart(string action, string drilledSeries, string currentReport)
{
    pivotClient.PopulateData(currentReport);
    pivotChart.PivotEngine.PivotRows = this.pivotClient.PivotReport.PivotRows;
    pivotChart.PivotEngine.PivotColumns = this.pivotClient.PivotReport.PivotColumns;
    pivotChart.PivotEngine.PivotCalculations = this.pivotClient.PivotReport.PivotCalculations;
    pivotChart.PivotEngine.Filters = this.pivotClient.PivotReport.Filters;
    return pivotChart.GetJsonData(action, ProductSales.GetSalesData(), drilledSeries);
}

{% endhighlight %} 

## Filtering

 [POST] [/WCF/PivotClient/Filtering](http://js.syncfusion.com/demos/ejServices/wcf/PivotClient/Relational.svc/Filtering)

It fetches the filtered data required to render the control after performing filtering.

### URL parameters

|  Parameter |  Description | 
|---|---|
|action|It holds the current action name as string|
|filterParams|It contains the information about the filter action performed|
|currentReport|It contains the current report as compressed string|
|customObject|It contains the custom object passed from client side|

### Response information 

Code: 200

Content-Type: application/json

Response: serialized JSON string

### Code example 

{% highlight c# %}

public Dictionary<string, object> Filtering(string action, string filterParams, string currentReport, string customObject)
{
    pivotClient.PopulateData(currentReport);
    return pivotClient.GetJsonData(action, ProductSales.GetSalesData(), filterParams);
}

{% endhighlight %} 

## FetchMembers

 [POST] [/WCF/PivotClient/FetchMembers](http://js.syncfusion.com/demos/ejServices/wcf/PivotClient/Relational.svc/FetchMembers)

It fetches the details of the members to render the member editor dialog.

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

{% highlight c# %}

public Dictionary<string, object> FetchMembers(string action, string currentReport, string customObject, string headerTag)
{
    pivotClient.PopulateData(currentReport);
    return pivotClient.GetJsonData(action, ProductSales.GetSalesData(), headerTag);
}

{% endhighlight %} 

## DropNode

 [POST] [/WCF/PivotClient/DropNode](http://js.syncfusion.com/demos/ejServices/wcf/PivotClient/Relational.svc/DropNode)

It fetches the data required to render the control after drag and drop action.

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

{% highlight c# %}

public Dictionary<string, object> DropNode(string action, string args)
{
    return pivotClient.GetJsonData(action, ProductSales.GetSalesData(), args);
}

{% endhighlight %} 

## ToolbarOperations

 [POST] [/WCF/PivotClient/ToolbarOperations](http://js.syncfusion.com/demos/ejServices/wcf/PivotClient/Relational.svc/ToolbarOperations)

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

{% highlight c# %}

public Dictionary<string, object> ToolbarOperations(string action, string args)
{
    return pivotClient.GetJsonData(action, ProductSales.GetSalesData(), args);
}

{% endhighlight %} 

## SaveReportToDB

 [POST] [/WCF/PivotClient/SaveReportToDB](http://js.syncfusion.com/demos/ejServices/wcf/PivotClient/Relational.svc/SaveReportToDB)

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
    cmd1.Parameters.Add("@Reports", Encoding.UTF8.GetBytes(clientReports).ToArray());
    cmd1.ExecuteNonQuery();
    con.Close();
    return null;
}

{% endhighlight %} 

## Export

 [POST] [/WCF/PivotClient/Export](http://js.syncfusion.com/demos/ejServices/wcf/PivotClient/Relational.svc/Export)

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

{% highlight c# %}

public void Export(Stream stream)
{
    System.IO.StreamReader sReader = new System.IO.StreamReader(stream);
    string args = System.Web.HttpContext.Current.Server.UrlDecode(sReader.ReadToEnd()).Remove(0, 5);
    Dictionary<string, string> gridParams = serializer.Deserialize<Dictionary<string, string>>(args);
    pivotClient.PopulateData(gridParams["currentReport"]);
    string fileName = "Sample";
    pivotClient.ExportPivotClient(ProductSales.GetSalesData(), args, fileName, System.Web.HttpContext.Current.Response);
}

{% endhighlight %} 

## FetchReportListFromDB

 [POST] [/WCF/PivotClient/FetchReportListFromDB](http://js.syncfusion.com/demos/ejServices/wcf/PivotClient/Relational.svc/FetchReportListFromDB)

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

 [POST] [/WCF/PivotClient/LoadReportFromDB](http://js.syncfusion.com/demos/ejServices/wcf/PivotClient/Relational.svc/LoadReportFromDB)

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
                OlapDataManager DataManager = new OlapDataManager();
                reportString = OLAPUTILS.Utils.CompressData(row.ItemArray[1] as byte[]);
                DataManager.Reports = pivotClient.DeserializedReports(reportString);
                DataManager.SetCurrentReport(DataManager.Reports[0]);
                return pivotClient.GetJsonData("toolbarOperation", DataManager, "Load Report", reportName);
            }
            else
            {
                byte[] reportString = new byte[2 * 1024];
                reportString = (row.ItemArray[1] as byte[]);
                if (analysisMode.ToLower() == "pivot" && operationalMode.ToLower() == "servermode")
                    dictionary = pivotClient.GetJsonData("LoadReport", ProductSales.GetSalesData(), Encoding.UTF8.GetString(reportString));
                else
                    dictionary.Add("report", Encoding.UTF8.GetString(reportString));
                break;
            }

        }
    }
    return dictionary;
}

{% endhighlight %} 