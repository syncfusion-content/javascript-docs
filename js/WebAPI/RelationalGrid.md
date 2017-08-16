---
layout: post
title: webAPI reference for RelationalGrid
description: webAPI reference for RelationalGrid
documentation: ug
platform: js
keywords: RelationalGrid, syncfusion, RelationalGrid webapi
---

## Initialize

 [POST] [/Api/RelationalGrid/Initialize](http://js.syncfusion.com/demos/ejServices/api/RelationalGrid/Initialize)

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

public Dictionary<string, object> Initialize(Dictionary<string, object> jsonResult)
{
    htmlHelper.PivotReport = BindDefaultData(); 
    return htmlHelper.GetJsonData(jsonResult["action"].ToString(), ProductSales.GetSalesData());
}

{% endhighlight %}

## FetchMembers

 [POST] [/Api/RelationalGrid/FetchMembers](http://js.syncfusion.com/demos/ejServices/api/RelationalGrid/FetchMembers)

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

public Dictionary<string, object> FetchMembers(Dictionary<string, object> jsonResult)
{
    htmlHelper.PopulateData(jsonResult["currentReport"].ToString());
    return htmlHelper.GetJsonData(jsonResult["action"].ToString(), ProductSales.GetSalesData(), jsonResult["headerTag"].ToString(), jsonResult["sortedHeaders"].ToString());
}

{% endhighlight %}

## Filtering

 [POST] [/Api/RelationalGrid/Filtering](http://js.syncfusion.com/demos/ejServices/api/RelationalGrid/Filtering)

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

public Dictionary<string, object> Filtering(Dictionary<string, object> jsonResult)
{
    htmlHelper.PopulateData(jsonResult["currentReport"].ToString());
    return htmlHelper.GetJsonData(jsonResult["action"].ToString(), ProductSales.GetSalesData(), jsonResult["filterParams"].ToString(), jsonResult["sortedHeaders"].ToString());
}

{% endhighlight %}

## ModifyNodeState

 [POST] [/Api/RelationalGrid/ModifyNodeState](http://js.syncfusion.com/demos/ejServices/api/RelationalGrid/ModifyNodeState)

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

public Dictionary<string, object> ModifyNodeState(Dictionary<string, object> jsonResult)
{
    htmlHelper.PopulateData(jsonResult["currentReport"].ToString());
    return htmlHelper.GetJsonData(jsonResult["action"].ToString(), ProductSales.GetSalesData(), jsonResult["headerTag"].ToString(), jsonResult["dropAxis"].ToString(), jsonResult["filterParams"].ToString(), jsonResult["sortedHeaders"].ToString());
}

{% endhighlight %}

## DropNode

 [POST] [/Api/RelationalGrid/DropNode](http://js.syncfusion.com/demos/ejServices/api/RelationalGrid/DropNode)

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

public Dictionary<string, object> DropNode(Dictionary<string, object> jsonResult)
{
    htmlHelper.PopulateData(jsonResult["currentReport"].ToString());
    return htmlHelper.GetJsonData(jsonResult["action"].ToString(), ProductSales.GetSalesData(), jsonResult["dropAxis"].ToString(), jsonResult["headerTag"].ToString(), jsonResult.ContainsKey("filterParams") ? jsonResult["filterParams"].ToString() : null, jsonResult["sortedHeaders"].ToString());
}

{% endhighlight %}

## Sorting

 [POST] [/Api/RelationalGrid/Sorting](http://js.syncfusion.com/demos/ejServices/api/RelationalGrid/Sorting)

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
public Dictionary<string, object> Sorting(Dictionary<string, object> jsonResult)
{
    htmlHelper.PopulateData(jsonResult["currentReport"].ToString());
    return htmlHelper.GetJsonData(jsonResult["action"].ToString(), ProductSales.GetSalesData(), jsonResult["sortedHeaders"].ToString());
}

{% endhighlight %}

## CalculatedField

 [POST] [/Api/RelationalGrid/CalculatedField](http://js.syncfusion.com/demos/ejServices/api/RelationalGrid/CalculatedField)

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

public Dictionary<string, object> CalculatedField(Dictionary<string, object> jsonResult)
{
    htmlHelper.PopulateData(jsonResult["currentReport"].ToString());
    return htmlHelper.GetJsonData(jsonResult["action"].ToString(), ProductSales.GetSalesData(), null, jsonResult["headerTag"].ToString());
}

{% endhighlight %}

## Export

 [POST] [/Api/RelationalGrid/Export](http://js.syncfusion.com/demos/ejServices/api/RelationalGrid/Export)

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

public void Export()
{
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    Dictionary<string, string> gridParams = serializer.Deserialize<Dictionary<string, string>>(args);
    htmlHelper.PopulateData(gridParams["currentReport"]);
    string fileName = "Sample";
    htmlHelper.ExportPivotGrid(ProductSales.GetSalesData(), args, fileName, System.Web.HttpContext.Current.Response);
}

{% endhighlight %}

## SaveReport

 [POST] [/Api/RelationalGrid/SaveReport](http://js.syncfusion.com/demos/ejServices/api/RelationalGrid/SaveReport)

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

public Dictionary<string, object> SaveReport(Dictionary<string, object> jsonResult)
{
    string mode = jsonResult["operationalMode"].ToString();
    bool isDuplicate = true;
    SqlCeConnection con = new SqlCeConnection() { ConnectionString = conStringforDB };
    con.Open();
    SqlCeCommand cmd1 = null;
    foreach (DataRow row in GetDataTable().Rows)
    {
        if ((row.ItemArray[0] as string).Equals(jsonResult["reportName"].ToString()))
        {
            isDuplicate = false;
            cmd1 = new SqlCeCommand("update ReportsTable set Report=@Reports where ReportName like @ReportName", con);
        }
    }
    if (isDuplicate)
    {
        cmd1 = new SqlCeCommand("insert into ReportsTable Values(@ReportName,@Reports)", con);
    }
    cmd1.Parameters.Add("@ReportName", jsonResult["reportName"].ToString());
    if (mode == "serverMode")
        cmd1.Parameters.Add("@Reports", Syncfusion.JavaScript.Olap.Utils.GetReportStream(jsonResult["clientReports"].ToString()).ToArray());
    else if (mode == "clientMode")
        cmd1.Parameters.Add("@Reports", Encoding.UTF8.GetBytes(jsonResult["clientReports"].ToString()).ToArray());
    cmd1.ExecuteNonQuery();
    con.Close();
    return null;
}

{% endhighlight %}

## LoadReportFromDB

 [POST] [/Api/RelationalGrid/LoadReportFromDB](http://js.syncfusion.com/demos/ejServices/api/RelationalGrid/LoadReportFromDB)

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

public Dictionary<string, object> LoadReportFromDB(Dictionary<string, object> jsonResult)
{
    byte[] reportString = new byte[2 * 1024];
    PivotReport report = new PivotReport();
    var reports = "";
    string mode = jsonResult["operationalMode"].ToString();
    Dictionary<string, object> dictionary = new Dictionary<string, object>();
    foreach (DataRow row in GetDataTable().Rows)
    {
        if ((row.ItemArray[0] as string).Equals(jsonResult["reportName"].ToString()))
        {
            if (mode == "clientMode")
            {
                reportString = (row.ItemArray[1] as byte[]);
                dictionary.Add("report", Encoding.UTF8.GetString(reportString));
                break;
            }
            else if (mode == "serverMode")
            {
                reports = Syncfusion.JavaScript.Olap.Utils.CompressData(row.ItemArray[1] as byte[]);
                report = htmlHelper.DeserializedReports(reports);
                htmlHelper.PivotReport = report;
                dictionary = htmlHelper.GetJsonData("loadOperation", ProductSales.GetSalesData(), "Load Report", jsonResult["reportName"].ToString());
                break;
            }
        }
    }
    return dictionary;
}


{% endhighlight %}

## DeferUpdate

 [POST] [/Api/RelationalGrid/DeferUpdate](http://js.syncfusion.com/demos/ejServices/api/RelationalGrid/DeferUpdate)

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

public Dictionary<string, object> DeferUpdate(Dictionary<string, object> jsonResult)
{
    htmlHelper.PopulateData(jsonResult["currentReport"].ToString());
    return htmlHelper.GetJsonData(jsonResult["action"].ToString(), ProductSales.GetSalesData(), null, null, null, jsonResult["sortedHeaders"].ToString(), jsonResult["filterParams"].ToString());
}

{% endhighlight %}

## CellEditing

 [POST] [/Api/RelationalGrid/CellEditing](http://js.syncfusion.com/demos/ejServices/api/RelationalGrid/CellEditing)

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

public Dictionary<string, object> CellEditing(Dictionary<string, object> jsonResult)
{
    htmlHelper.PopulateData(jsonResult["currentReport"].ToString());
    return htmlHelper.GetJsonData(jsonResult["action"].ToString(), ProductSales.GetSalesData(), jsonResult["index"].ToString(), jsonResult["summaryValues"].ToString(), jsonResult["valueHeaders"].ToString());
}

{% endhighlight %}
