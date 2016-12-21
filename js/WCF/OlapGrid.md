---
layout: post
title: WCF reference for PivotGrid
description: WCF reference for PivotGrid
documentation: ug
platform: js
keywords: PivotGrid , syncfusion, PivotGrid WCF
---

## Initialize

 [POST] [/WCF/PivotGrid/Initialize](http://js.syncfusion.com/demos/ejServices/wcf/PivotGrid/Olap.svc/Initialize)

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

public Dictionary<string, object> Initialize(string action, string gridLayout, bool enablePivotFieldList, object customObject)
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
    DataManager.SetCurrentReport(CreateOlapReport((customData is Dictionary<string, object> && customData.ContainsKey("isPaging")) ? customData["isPaging"] : false));
    return htmlHelper.GetJsonData(action, DataManager, gridLayout, enablePivotFieldList);
}

{% endhighlight %} 

## Drill

 [POST] [/WCF/PivotGrid/Drill](http://js.syncfusion.com/demos/ejServices/wcf/PivotGrid/Olap.svc/Drill)

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

public Dictionary<string, object> Drill(string action, string cellPosition, string currentReport, string headerInfo, string layout, object customObject)
{
    dynamic customData = serializer.Deserialize<dynamic>(customObject.ToString());
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    if (customData is Dictionary<string, object> && customData.ContainsKey("Language"))
    {
        var cultureIDInfo = new System.Globalization.CultureInfo((customData["Language"])).LCID;
        connectionString = connectionString.Replace("" + cultureIDInfoval + "", "" + cultureIDInfo + "");
        cultureIDInfoval = cultureIDInfo;
        DataManager = new OlapDataManager(connectionString);
        DataManager.Culture = new System.Globalization.CultureInfo((customData["Language"]));
        DataManager.OverrideDefaultFormatStrings = true;
    }
    else
        DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(Utils.DeserializeOlapReport(currentReport));
    return htmlHelper.GetJsonData(action, connectionString, DataManager, cellPosition, headerInfo, layout);
}

{% endhighlight %} 

## DropNode

 [POST] [/WCF/PivotGrid/DropNode](http://js.syncfusion.com/demos/ejServices/wcf/PivotGrid/Olap.svc/DropNode)

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

public Dictionary<string, object> DropNode(string action, string dropType, string nodeInfo, string filterParams, string gridLayout, string currentReport)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(Utils.DeserializeOlapReport(currentReport));
    return htmlHelper.GetJsonData(action, DataManager, dropType, nodeInfo, filterParams, gridLayout, true);
}

{% endhighlight %} 

## Filtering

 [POST] [/WCF/PivotGrid/Filtering](http://js.syncfusion.com/demos/ejServices/wcf/PivotGrid/Olap.svc/Filtering)

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

public Dictionary<string, object> Filtering(string action, string filterParams, string gridLayout, string currentReport)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(Utils.DeserializeOlapReport(currentReport));
    return htmlHelper.GetJsonData(action, connectionString, DataManager, null, filterParams, gridLayout);
}

{% endhighlight %} 

## FetchMembers

 [POST] [/WCF/PivotGrid/FetchMembers](http://js.syncfusion.com/demos/ejServices/wcf/PivotGrid/Olap.svc/FetchMembers)

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

public Dictionary<string, object> FetchMembers(string action, string headerTag, string currentReport)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(Utils.DeserializeOlapReport(currentReport));
    return htmlHelper.GetJsonData(action, DataManager, null, headerTag);
}

{% endhighlight %} 


## Paging

 [POST] [/WCF/PivotGrid/Paging](http://js.syncfusion.com/demos/ejServices/wcf/PivotGrid/Olap.svc/Paging)

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

public Dictionary<string, object> Paging(string action, string pagingInfo, string currentReport, string gridLayout, object customObject)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(htmlHelper.SetPaging(currentReport, pagingInfo));
    return htmlHelper.GetJsonData(action, DataManager, gridLayout);
}

{% endhighlight %} 

## RemoveButton

 [POST] [/WCF/PivotGrid/RemoveButton](http://js.syncfusion.com/demos/ejServices/wcf/PivotGrid/Olap.svc/RemoveButton)

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

public Dictionary<string, object> RemoveButton(string action, string headerInfo, string gridLayout, string currentReport)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(Utils.DeserializeOlapReport(currentReport));
    return htmlHelper.GetJsonData(action, connectionString, DataManager, null, headerInfo, gridLayout);
}

{% endhighlight %} 

## ExpandMember

 [POST] [/WCF/PivotGrid/ExpandMember](http://js.syncfusion.com/demos/ejServices/wcf/PivotGrid/Olap.svc/ExpandMember)

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

public Dictionary<string, object> ExpandMember(string action, bool checkedStatus, string parentNode, string tag, string cubeName, string currentReport)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    if (!string.IsNullOrEmpty(currentReport))
        DataManager.SetCurrentReport(Utils.DeserializeOlapReport(currentReport));
    return htmlHelper.GetJsonData(action, DataManager, checkedStatus, parentNode, tag, cubeName);
}

{% endhighlight %} 

## Export

 [POST] [/WCF/PivotGrid/Export](http://js.syncfusion.com/demos/ejServices/wcf/PivotGrid/Olap.svc/Export)

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

public void Export(Stream stream)
{
    System.IO.StreamReader sReader = new System.IO.StreamReader(stream);
    string args = System.Web.HttpContext.Current.Server.UrlDecode(sReader.ReadToEnd()).Remove(0, 5); ;
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    string fileName = "Sample";
    htmlHelper.ExportPivotGrid(DataManager, args, fileName, System.Web.HttpContext.Current.Response);
}

{% endhighlight %} 

## SaveReport

 [POST] [/WCF/PivotGrid/SaveReport](http://js.syncfusion.com/demos/ejServices/wcf/PivotGrid/Olap.svc/SaveReport)

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

 [POST] [/WCF/PivotGrid/LoadReportFromDB](http://js.syncfusion.com/demos/ejServices/wcf/PivotGrid/Olap.svc/LoadReportFromDB)

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
public Dictionary<string, object> LoadReportFromDB(string action, string layout, bool enablePivotFieldList, object customObject, string reportName, string operationalMode, string olapReport, string clientReports)
{
    string mode = operationalMode;
    var reports = "";
    byte[] reportString = new byte[4 * 1024];
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
                    reportString = row.ItemArray[1] as byte[];
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
        OlapDataManager DataManager = new OlapDataManager(connectionString);
        dynamic customData = serializer.Deserialize<dynamic>(customObject.ToString());
        var cultureIDInfo = new System.Globalization.CultureInfo(("en-US")).LCID;
        if (customData is Dictionary<string, object> && customData.ContainsKey("Language"))
        {
            cultureIDInfo = new System.Globalization.CultureInfo((customData["Language"])).LCID;
        }
        connectionString = connectionString.Replace("" + cultureIDInfoval + "", "" + cultureIDInfo + "");
        cultureIDInfoval = cultureIDInfo;
        DataManager.Culture = new System.Globalization.CultureInfo((cultureIDInfo));
        DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(reports));
        DataManager.OverrideDefaultFormatStrings = true;
        dictionary = htmlHelper.GetJsonData(action, DataManager, layout, enablePivotFieldList);
    }
    return dictionary;
}

{% endhighlight %} 

## DeferUpdate

 [POST] [/WCF/PivotGrid/DeferUpdate](http://js.syncfusion.com/demos/ejServices/wcf/PivotGrid/Olap.svc/DeferUpdate)

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

public Dictionary<string, object> DeferUpdate(string action, string filterParams, string currentReport)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(Utils.DeserializeOlapReport(currentReport));
    return htmlHelper.GetJsonData(action, DataManager, null, filterParams);
}

{% endhighlight %} 