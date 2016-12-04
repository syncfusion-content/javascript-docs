---
layout: post
title: webAPI reference for RelationalClient
description: webAPI reference for RelationalClient
documentation: ug
platform: js
keywords: RelationalClient, syncfusion, RelationalClient webapi
---

## Initialize

 [POST] [/Api/RelationalClient/Initialize](http://js.syncfusion.com/demos/ejServices/api/RelationalClient/Initialize)

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

{% highlight c# %}
public Dictionary<string, object> Initialize(Dictionary<string, object> jsonResult)
{
    this.BindData();
    return pivotClient.GetJsonData(jsonResult["action"].ToString(), ProductSales.GetSalesData(), null);
}

{% endhighlight %}

## FetchMembers

 [POST] [/Api/RelationalClient/FetchMembers](http://js.syncfusion.com/demos/ejServices/api/RelationalClient/FetchMembers)

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

{% highlight c# %}
public Dictionary<string, object> FetchMembers(Dictionary<string, object> jsonResult)
{
    pivotClient.PopulateData(jsonResult["currentReport"].ToString());
    return pivotClient.GetJsonData(jsonResult["action"].ToString(), ProductSales.GetSalesData(), jsonResult["headerTag"].ToString());
}

{% endhighlight %}

## DrillChart

 [POST] [/Api/RelationalClient/DrillChart](http://js.syncfusion.com/demos/ejServices/api/RelationalClient/DrillChart)

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

{% highlight c# %}

public Dictionary<string, object> DrillChart(Dictionary<string, object> jsonResult)
{
    pivotClient.PopulateData(jsonResult["currentReport"].ToString());
    this.pivotChart.PivotEngine.PivotRows = this.pivotClient.PivotReport.PivotRows;
    this.pivotChart.PivotEngine.PivotColumns = this.pivotClient.PivotReport.PivotColumns;
    this.pivotChart.PivotEngine.PivotCalculations = this.pivotClient.PivotReport.PivotCalculations;
    this.pivotChart.PivotEngine.Filters = this.pivotClient.PivotReport.Filters;
    return pivotChart.GetJsonData(jsonResult["action"].ToString(), ProductSales.GetSalesData(), jsonResult["drilledSeries"].ToString());
}

{% endhighlight %}

## Filtering

 [POST] [/Api/RelationalClient/Filtering](http://js.syncfusion.com/demos/ejServices/api/RelationalClient/Filtering)

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

{% highlight c# %}

public Dictionary<string, object> Filtering(Dictionary<string, object> jsonResult)
{
    pivotClient.PopulateData(jsonResult["currentReport"].ToString());
    return pivotClient.GetJsonData(jsonResult["action"].ToString(), ProductSales.GetSalesData(), jsonResult["filterParams"].ToString());
}

{% endhighlight %}

## DropNode

 [POST] [/Api/RelationalClient/DropNode](http://js.syncfusion.com/demos/ejServices/api/RelationalClient/DropNode)

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

{% highlight c# %}

public Dictionary<string, object> DropNode(Dictionary<string, object> jsonResult)
{
    Dictionary<string, object> dict = pivotClient.GetJsonData(jsonResult["action"].ToString(), ProductSales.GetSalesData(), jsonResult["args"].ToString());
    return dict;
}

{% endhighlight %}

## ToolbarOperations

 [POST] [/Api/RelationalClient/ToolbarOperations](http://js.syncfusion.com/demos/ejServices/api/RelationalClient/ToolbarOperations)

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

public Dictionary<string, object> ToolbarOperations(Dictionary<string, object> jsonResult)
{
    Dictionary<string, object> dict = pivotClient.GetJsonData(jsonResult["action"].ToString(), ProductSales.GetSalesData(), jsonResult["args"].ToString());
    return dict;
}

{% endhighlight %}

## SaveReportToDB

 [POST] [/Api/RelationalClient/SaveReportToDB](http://js.syncfusion.com/demos/ejServices/api/RelationalClient/SaveReportToDB)

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
    cmd1.Parameters.Add("@Reports", Encoding.UTF8.GetBytes(jsonResult["clientReports"].ToString()).ToArray());
    cmd1.ExecuteNonQuery();
    con.Close();
    return null;
}

{% endhighlight %}

## Export

 [POST] [/Api/RelationalClient/Export](http://js.syncfusion.com/demos/ejServices/api/RelationalClient/Export)

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
public void Export()
{
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    Dictionary<string, string> gridParams = serializer.Deserialize<Dictionary<string, string>>(args);
    pivotClient.PopulateData(gridParams["currentReport"]);
    string fileName = "Sample";
    pivotClient.ExportPivotClient(ProductSales.GetSalesData(), args, fileName, System.Web.HttpContext.Current.Response);
}

{% endhighlight %}

## FetchReportListFromDB

 [POST] [/Api/RelationalClient/FetchReportListFromDB](http://js.syncfusion.com/demos/ejServices/api/RelationalClient/FetchReportListFromDB)

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

 [POST] [/Api/RelationalClient/LoadReportFromDB](http://js.syncfusion.com/demos/ejServices/api/RelationalClient/LoadReportFromDB)

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
            byte[] reportString = new byte[2 * 1024];
            reportString = (row.ItemArray[1] as byte[]);
            if (analysisMode.ToLower() == "pivot" && operationalMode.ToLower() == "servermode")
                dictionary = pivotClient.GetJsonData("LoadReport", ProductSales.GetSalesData(), Encoding.UTF8.GetString(reportString));
            else
                dictionary.Add("report", Encoding.UTF8.GetString(reportString));
            break;
        }
    }
    return dictionary;
}

{% endhighlight %}
