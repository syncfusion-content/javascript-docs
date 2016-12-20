---
layout: post
title: WCF reference for RelationalGrid
description: WCF reference for RelationalGrid
documentation: ug
platform: js
keywords: RelationalGrid, syncfusion, RelationalGrid WCF
---

## Initialize

 [POST] [/WCF/PivotGrid/Initialize](http://js.syncfusion.com/demos/ejServices/wcf/PivotGrid/Relational.svc/Initialize)

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

{% highlight c# %}

public Dictionary<string, object> Initialize(string action)
{
    htmlHelper.PivotReport = BindDefaultData();
    dict = htmlHelper.GetJsonData(action, ProductSales.GetSalesData());
    return dict;
}

{% endhighlight %} 

## FetchMembers

 [POST] [/WCF/PivotGrid/FetchMembers](http://js.syncfusion.com/demos/ejServices/wcf/PivotGrid/Relational.svc/FetchMembers)

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

{% highlight c# %}

public Dictionary<string, object> FetchMembers(string action, string headerTag, string sortedHeaders, string currentReport)
{
    htmlHelper.PopulateData(currentReport);
    dict = htmlHelper.GetJsonData(action, ProductSales.GetSalesData(), headerTag, sortedHeaders);
    return dict;
}

{% endhighlight %} 

## Filtering

 [POST] [/WCF/PivotGrid/Filtering](http://js.syncfusion.com/demos/ejServices/wcf/PivotGrid/Relational.svc/Filtering)

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

{% highlight c# %}

public Dictionary<string, object> Filtering(string action, string filterParams, string sortedHeaders, string currentReport)
{
    htmlHelper.PopulateData(currentReport);
    dict = htmlHelper.GetJsonData(action, ProductSales.GetSalesData(), filterParams, sortedHeaders);
    return dict;
}

{% endhighlight %} 

## ModifyNodeState

 [POST] [/WCF/PivotGrid/ModifyNodeState](http://js.syncfusion.com/demos/ejServices/wcf/PivotGrid/Relational.svc/ModifyNodeState)

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

{% highlight c# %}

public Dictionary<string, object> ModifyNodeState(string action, string headerTag, string dropAxis, string sortedHeaders, string filterParams, string currentReport)
{
    htmlHelper.PopulateData(currentReport);
    dict = htmlHelper.GetJsonData(action, ProductSales.GetSalesData(), headerTag, dropAxis, filterParams, sortedHeaders);
    return dict;
}

{% endhighlight %} 

## DropNode

 [POST] [/WCF/PivotGrid/DropNode](http://js.syncfusion.com/demos/ejServices/wcf/PivotGrid/Relational.svc/DropNode)

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

{% highlight c# %}

public Dictionary<string, object> DropNode(string action, string dropAxis, string headerTag, string sortedHeaders, string filterParams, string currentReport)
{
    htmlHelper.PopulateData(currentReport);
    dict = htmlHelper.GetJsonData(action, ProductSales.GetSalesData(), dropAxis, headerTag, filterParams, sortedHeaders);
    return dict;
}

{% endhighlight %} 

## Sorting

 [POST] [/WCF/PivotGrid/Sorting](http://js.syncfusion.com/demos/ejServices/wcf/PivotGrid/Relational.svc/Sorting)

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

{% highlight c# %}

public Dictionary<string, object> Sorting(string action, string sortedHeaders, string currentReport)
{
    htmlHelper.PopulateData(currentReport);
    dict = htmlHelper.GetJsonData(action, ProductSales.GetSalesData(), sortedHeaders);
    return dict;
}

{% endhighlight %} 

## CalculatedField

 [POST] [/WCF/PivotGrid/CalculatedField](http://js.syncfusion.com/demos/ejServices/wcf/PivotGrid/Relational.svc/CalculatedField)

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

{% highlight c# %}

public Dictionary<string, object> CalculatedField(string action, string headerTag, string currentReport)
{
    htmlHelper.PopulateData(currentReport);
    dict = htmlHelper.GetJsonData(action, ProductSales.GetSalesData(), null, headerTag);
    return dict;
}

{% endhighlight %} 

## Export

 [POST] [/WCF/PivotGrid/Export](http://js.syncfusion.com/demos/ejServices/wcf/PivotGrid/Relational.svc/Export)

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

{% highlight c# %}

public void Export(Stream stream)
{
    System.IO.StreamReader sReader = new System.IO.StreamReader(stream);
    string args = System.Web.HttpContext.Current.Server.UrlDecode(sReader.ReadToEnd()).Remove(0, 5);
    Dictionary<string, string> gridParams = serializer.Deserialize<Dictionary<string, string>>(args);
    htmlHelper.PopulateData(gridParams["currentReport"]);
    string fileName = "Sample";
    htmlHelper.ExportPivotGrid(ProductSales.GetSalesData(), args, fileName, System.Web.HttpContext.Current.Response);
}

{% endhighlight %} 

## SaveReport

 [POST] [/WCF/PivotGrid/SaveReport](http://js.syncfusion.com/demos/ejServices/wcf/PivotGrid/Relational.svc/SaveReport)

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

{% highlight c# %}

public Dictionary<string, object> SaveReport(string reportName, string operationalMode, string olapReport, string clientReports)
{
    string mode = operationalMode;
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
    //cmd1.Parameters.Add("@Reports", OLAPUTILS.Utils.GetReportStream(clientReports).ToArray());
    if (mode == "serverMode")
        cmd1.Parameters.Add("@Reports", OLAPUTILS.Utils.GetReportStream(clientReports).ToArray());
    else if (mode == "clientMode")
        cmd1.Parameters.Add("@Reports", Encoding.UTF8.GetBytes(clientReports).ToArray());
    cmd1.ExecuteNonQuery();
    con.Close();
    return null;
}

{% endhighlight %} 

## LoadReportFromDB

 [POST] [/WCF/PivotGrid/LoadReportFromDB](http://js.syncfusion.com/demos/ejServices/wcf/PivotGrid/Relational.svc/LoadReportFromDB)

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

{% highlight c# %}

public Dictionary<string, object> LoadReportFromDB(string reportName, string operationalMode, string olapReport, string clientReports)
{
    byte[] reportString = new byte[2 * 1024];
    PivotReport report = new PivotReport();
    var reports = "";
    string mode = operationalMode;
    Dictionary<string, object> dictionary = new Dictionary<string, object>();
    if (mode == "serverMode" && !string.IsNullOrEmpty(clientReports))
    {
        reports = clientReports;
    }
    else
    {
        foreach (DataRow row in GetDataTable().Rows)
        {
            if ((row.ItemArray[0] as string).Equals(reportName))
            {
                if (mode == "clientMode")
                {
                    reportString = (row.ItemArray[1] as byte[]);
                    dictionary.Add("report", Encoding.UTF8.GetString(reportString));
                    break;
                }
                else if (mode == "serverMode")
                {
                    reports = OLAPUTILS.Utils.CompressData(row.ItemArray[1] as byte[]);
                    break;
                }
            }
        }
    }
    if (reports != "")
    {
        report = htmlHelper.DeserializedReports(reports);
        htmlHelper.PivotReport = report;
        dictionary = htmlHelper.GetJsonData("loadOperation", ProductSales.GetSalesData(), "Load Report", reportName);
    }
    return dictionary;
}

{% endhighlight %} 

## DeferUpdate

 [POST] [/WCF/PivotGrid/DeferUpdate](http://js.syncfusion.com/demos/ejServices/wcf/PivotGrid/Relational.svc/DeferUpdate)

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

{% highlight c# %}

public Dictionary<string, object> DeferUpdate(string action, string filterParams, string sortedHeaders, string currentReport)
{
    htmlHelper.PopulateData(currentReport);
    dict = htmlHelper.GetJsonData(action, ProductSales.GetSalesData(), null, null, null, sortedHeaders, filterParams);
    return dict;
}

{% endhighlight %} 

## CellEditing

 [POST] [/WCF/PivotGrid/CellEditing](http://js.syncfusion.com/demos/ejServices/wcf/PivotGrid/Relational.svc/CellEditing)

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

{% highlight c# %}

public Dictionary<string, object> CellEditing(string action, string index, string valueHeaders, string summaryValues, string currentReport)
{
    htmlHelper.PopulateData(currentReport);
    dict = htmlHelper.GetJsonData(action, ProductSales.GetSalesData(), index, summaryValues, valueHeaders);
    return dict;
}

{% endhighlight %} 
