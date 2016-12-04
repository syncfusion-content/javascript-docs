---
layout: post
title: webAPI reference for PivotGrid
description: webAPI reference for PivotGrid
documentation: ug
platform: js
keywords: PivotGrid , syncfusion, PivotGrid webapi
---

## Initialize

 [POST] [/Api/OlapGrid/Initialize](http://js.syncfusion.com/demos/ejServices/api/OlapGrid/Initialize)

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

{% highlight c# %}
public Dictionary<string, object> Initialize(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(CreateOlapReport());
    return htmlHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult.ContainsKey("gridLayout") ? jsonResult["gridLayout"].ToString() : null, Convert.ToBoolean(jsonResult["enablePivotFieldList"].ToString()));
}

{% endhighlight %}

## Drill

 [POST] [/Api/OlapGrid/Drill](http://js.syncfusion.com/demos/ejServices/api/OlapGrid/Drill)

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

{% highlight c# %}
public Dictionary<string, object> Drill(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
    return htmlHelper.GetJsonData(jsonResult["action"].ToString(), connectionString, DataManager, jsonResult["cellPosition"].ToString(), jsonResult["headerInfo"].ToString(), jsonResult["layout"].ToString());
}

{% endhighlight %}

## DropNode

 [POST] [/Api/OlapGrid/DropNode](http://js.syncfusion.com/demos/ejServices/api/OlapGrid/DropNode)

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

{% highlight c# %}
public Dictionary<string, object> DropNode(Dictionary<string, object> jsonResult)
{
	OlapDataManager DataManager = new OlapDataManager(connectionString);
	DataManager.SetCurrentReport(Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
	return htmlHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["dropType"].ToString(), jsonResult["nodeInfo"].ToString(), jsonResult.ContainsKey("filterParams") ? jsonResult["filterParams"].ToString() : null, jsonResult["gridLayout"].ToString(), true);
}

{% endhighlight %}

## Filtering

 [POST] [/Api/OlapGrid/Filtering](http://js.syncfusion.com/demos/ejServices/api/OlapGrid/Filtering)

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

{% highlight c# %}
public Dictionary<string, object> Filtering(Dictionary<string, object> jsonResult)
{
	OlapDataManager DataManager = new OlapDataManager(connectionString);
	DataManager.SetCurrentReport(Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
	return htmlHelper.GetJsonData(jsonResult["action"].ToString(), connectionString, DataManager, null, jsonResult["filterParams"].ToString(), jsonResult["gridLayout"].ToString());
}

{% endhighlight %}

## FetchMembers

 [POST] [/Api/OlapGrid/FetchMembers](http://js.syncfusion.com/demos/ejServices/api/OlapGrid/FetchMembers)

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

{% highlight c# %}
public Dictionary<string, object> FetchMembers(Dictionary<string, object> jsonResult)
{
	OlapDataManager DataManager = new OlapDataManager(connectionString);
	DataManager.SetCurrentReport(Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
	return htmlHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, null, jsonResult["headerTag"].ToString());
}

{% endhighlight %}


## Paging

 [POST] [/Api/OlapGrid/Paging](http://js.syncfusion.com/demos/ejServices/api/OlapGrid/Paging)

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

{% highlight c# %}
public Dictionary<string, object> Paging(Dictionary<string, object> jsonResult)
{
	OlapDataManager DataManager = new OlapDataManager(connectionString);
	DataManager.SetCurrentReport(htmlHelper.SetPaging(jsonResult["currentReport"].ToString(), jsonResult["pagingInfo"].ToString()));
	return htmlHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["layout"].ToString());
}

{% endhighlight %}

## RemoveButton

 [POST] [/Api/OlapGrid/RemoveButton](http://js.syncfusion.com/demos/ejServices/api/OlapGrid/RemoveButton)

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

{% highlight c# %}
public Dictionary<string, object> RemoveButton(Dictionary<string, object> jsonResult)
{
	OlapDataManager DataManager = new OlapDataManager(connectionString);
	DataManager.SetCurrentReport(Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
	return htmlHelper.GetJsonData(jsonResult["action"].ToString(), connectionString, DataManager, null, jsonResult["headerInfo"].ToString(), jsonResult["gridLayout"].ToString());
}

{% endhighlight %}

## ExpandMember

 [POST] [/Api/OlapGrid/ExpandMember](http://js.syncfusion.com/demos/ejServices/api/OlapGrid/ExpandMember)

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

{% highlight c# %}
public Dictionary<string, object> ExpandMember(Dictionary<string, object> jsonResult)
{
	OlapDataManager DataManager = new OlapDataManager(connectionString);
	DataManager.SetCurrentReport(Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
	return htmlHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, Convert.ToBoolean(jsonResult["checkedStatus"].ToString()), jsonResult["parentNode"].ToString(), jsonResult["tag"].ToString(), jsonResult["cubeName"].ToString());
}

{% endhighlight %}

## Export

 [POST] [/Api/OlapGrid/Export](http://js.syncfusion.com/demos/ejServices/api/OlapGrid/Export)

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

{% highlight c# %}

public void Export()
{
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    string fileName = "Sample";
    htmlHelper.ExportPivotGrid(DataManager, args, fileName, System.Web.HttpContext.Current.Response);
}

{% endhighlight %}

## SaveReport

 [POST] [/Api/OlapGrid/SaveReport](http://js.syncfusion.com/demos/ejServices/api/OlapGrid/SaveReport)

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
    if (mode == "clientMode")
        cmd1.Parameters.Add("@Reports", Encoding.UTF8.GetBytes(jsonResult["clientReports"].ToString()).ToArray());
    else if (mode == "serverMode")
        cmd1.Parameters.Add("@Reports", Utils.GetReportStream(jsonResult["clientReports"].ToString()).ToArray());
    cmd1.ExecuteNonQuery();
    con.Close();
    return null;
}

{% endhighlight %}

## LoadReportFromDB

 [POST] [/Api/OlapGrid/LoadReportFromDB](http://js.syncfusion.com/demos/ejServices/api/OlapGrid/LoadReportFromDB)

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

{% highlight c# %}

public Dictionary<string, object> LoadReportFromDB(Dictionary<string, object> jsonResult)
{
    string mode = jsonResult["operationalMode"].ToString();
    byte[] reportString = new byte[4 * 1024];
    Dictionary<string, object> dictionary = new Dictionary<string, object>();
    foreach (DataRow row in GetDataTable().Rows)
    {
        if ((row.ItemArray[0] as string).Equals(jsonResult["reportName"].ToString()))
        {
            if (mode == "clientMode")
            {
                reportString = row.ItemArray[1] as byte[];
                dictionary.Add("report", Encoding.UTF8.GetString(reportString));
                break;
            }
            else if (mode == "serverMode")
            {
                OlapDataManager DataManager = new OlapDataManager(connectionString);
                var reports = "";
                dynamic customData = serializer.Deserialize<dynamic>(jsonResult["customObject"].ToString());
                var cultureIDInfo = new System.Globalization.CultureInfo(("en-US")).LCID;
                if (customData is Dictionary<string, object> && customData.ContainsKey("Language"))
                {
                    cultureIDInfo = new System.Globalization.CultureInfo((customData["Language"])).LCID;
                }
                connectionString = connectionString.Replace("" + cultureIDInfoval + "", "" + cultureIDInfo + "");
                cultureIDInfoval = cultureIDInfo;
                if ((row.ItemArray[0] as string).Equals(jsonResult["reportName"].ToString()))
                {
                    reports = Utils.CompressData(row.ItemArray[1] as byte[]);
                }
                DataManager.Culture = new System.Globalization.CultureInfo((cultureIDInfo));
                DataManager.SetCurrentReport(Utils.DeserializeOlapReport(reports));
                DataManager.OverrideDefaultFormatStrings = true;
                dictionary = htmlHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["gridLayout"].ToString(), Convert.ToBoolean(jsonResult["enablePivotFieldList"].ToString()));
            }
        }
    }
    return dictionary;
}

{% endhighlight %}

## DeferUpdate

 [POST] [/Api/OlapGrid/DeferUpdate](http://js.syncfusion.com/demos/ejServices/api/OlapGrid/DeferUpdate)

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

{% highlight c# %}
public Dictionary<string, object> DeferUpdate(Dictionary<string, object> jsonResult)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
    return htmlHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, null, jsonResult["filterParams"].ToString());
}

{% endhighlight %}

## ExcelExport

 [POST] [/Api/OlapGrid/ExcelExport](http://js.syncfusion.com/demos/ejServices/api/OlapGrid/ExcelExport)

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

{% highlight c# %}
public void ExcelExport()
{
	PivotGridExcelExport pGrid = new PivotGridExcelExport();
	string args = HttpContext.Current.Request.Form.GetValues(0)[0];
	pGrid.ExportToExcel(string.Empty, args, HttpContext.Current.Response);
}
{% endhighlight %}

## PdfExport

 [POST] [/Api/OlapGrid/PdfExport](http://js.syncfusion.com/demos/ejServices/api/OlapGrid/PdfExport)

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

{% highlight c# %}
public void PdfExport()
{
	PivotGridPDFExport pGrid = new PivotGridPDFExport();
	string args = HttpContext.Current.Request.Form.GetValues(0)[0];
	pGrid.ExportToPDF(string.Empty, args, HttpContext.Current.Response);
}
{% endhighlight %}

## WordExport

 [POST] [/Api/OlapGrid/WordExport](http://js.syncfusion.com/demos/ejServices/api/OlapGrid/WordExport)

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

{% highlight c# %}
public void WordExport()
{
	PivotGridWordExport pGrid = new PivotGridWordExport();
	string args = HttpContext.Current.Request.Form.GetValues(0)[0];
	pGrid.ExportToWord(string.Empty, args, HttpContext.Current.Response);
}

{% endhighlight %}

## CsvExport

 [POST] [/Api/OlapGrid/CsvExport](http://js.syncfusion.com/demos/ejServices/api/OlapGrid/CsvExport)

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

{% highlight c# %}
public void CsvExport()
{
	PivotGridCSVExport pGrid = new PivotGridCSVExport();
	string args = HttpContext.Current.Request.Form.GetValues(0)[0];
	pGrid.ExportToCSV(string.Empty, args, HttpContext.Current.Response);
}

{% endhighlight %}
