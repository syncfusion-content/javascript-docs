---
layout: post
title: Save and Load Report
description: save and load report
platform: js
control: PivotGrid
documentation: ug
api: /api/js/ejpivotgrid
---

# Save and Load Report

Allows you to save the current report of PivotGrid and render the control with the saved report later. You can save and load the report in two ways:

* Database
* Local storage

## Save report to database

By using the current report name, storage option, and url, you can save the current report of the PivotGrid to the database.

{% highlight html %}

<div id="PivotGrid1"> </div>
<button id="btnSave">save To DB</button>
<script>
    $("#PivotGrid1").ejPivotGrid({
        //...
    });
    $("#btnSave").ejButton({click:"saveToDB"});
    function saveToDB(){
        url = "/RelationalService",
        name = "report",
        storage = "db",
        pGridObj.saveReport(name, storage, url);
    }
</script>

{% endhighlight %}

Service method can be added in the WCF/WebAPI for storing the current report of PivotGrid to the database.

For WebAPI controller, the below method needs to be added.

{% highlight c# %}

[System.Web.Http.ActionName("SaveReport")]
[System.Web.Http.HttpPost]
public Dictionary<string, object> SaveReport(Dictionary<string, object> jsonResult)
{
    string mode = jsonResult["operationalMode"].ToString();
    bool isDuplicate = true;
    SqlCeConnection con = new SqlCeConnection() { ConnectionString = "Enter appropriate connection string to connect with database" };
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
        cmd1.Parameters.Add("@Reports", OLAPUTILS.Utils.GetReportStream(jsonResult["clientReports"].ToString()).ToArray());
    cmd1.ExecuteNonQuery();
    con.Close();
    return null;
}

{% endhighlight %}

For WCF service, the below method needs to be added.

{% highlight c# %}

public Dictionary<string, object> SaveReport(string reportName, string operationalMode, string olapReport, string clientReports)
{
    string mode = operationalMode;
    bool isDuplicate = true;
    SqlCeConnection con = new SqlCeConnection() { ConnectionString = "Enter appropriate connection string to connect with database" };
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

## Save report to local storage

To save the current report of PivotGrid to the local storage, you should call the [`saveReport`](/api/js/ejpivotgrid#members:saveReport) method in the PivotGrid.

{% highlight html %}

<div id="PivotGrid1"> </div>
<button id="btnSave">save</button>
<script>
    $("#PivotGrid1").ejPivotGrid({
        //...
        saveReport: "saveToLocal"
    });
    $("#btnSave").ejButton({click:"saveLocal"});
    function saveLocal(){
        url = "",
        name = "report",
        storage = "local",
        pGridObj.saveReport(name, storage, url);
    }        
    function saveToLocal(args){
        localStorage.setItem("report", JSON.stringify(args.report));
    }
</script>

{% endhighlight %}

## Load report from database

By using the stored report name, database name, and url, you can load the saved report of PivotGrid from the database.

{% highlight html %}

<div id="PivotGrid1"> </div>
<button id="btnLoad">Load</button>
<script>
    $("#PivotGrid1").ejPivotGrid({
        //...
    });
    $("#btnLoad").ejButton({click:"loadDB"});
    function loadDB(){
        url = "/RelationalService",
        name = "report",
        storage = "db",
        pGridObj.loadReport(name, storage, url);
    }
</script>

{% endhighlight %}

Service methods should be added in the WCF/WebAPI for loading the stored report in the database.

### Relational

For WebAPI controller, the below methods need to be added:

{% highlight c# %}

[System.Web.Http.ActionName("LoadReportFromDB")]
[System.Web.Http.HttpPost]
public Dictionary<string, object> LoadReportFromDB(Dictionary<string, object> jsonResult)
{
    byte[] reportString = new byte[2 * 1024];
    PivotReport report = new PivotReport();
    var reports = "";
    string mode = jsonResult["operationalMode"].ToString();
    Dictionary<string, object> dictionary = new Dictionary<string, object>();
    if (mode == "serverMode" && jsonResult.ContainsKey("clientReports"))
    {
        reports = jsonResult["clientReports"].ToString();
    }
    else
    {
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
        dictionary = htmlHelper.GetJsonData("loadOperation", ProductSales.GetSalesData(), "Load Report", jsonResult["reportName"].ToString());
    }
    return dictionary;
}


private DataTable GetDataTable()
{
    SqlCeConnection con = new SqlCeConnection() { ConnectionString = "Enter appropriate connection string to connect with database" };
    con.Open();
    DataSet dSet = new DataSet();
    new SqlCeDataAdapter("Select * from ReportsTable", con).Fill(dSet);
    con.Close();
    return dSet.Tables[0];
}

{% endhighlight %}

For WCF service, the below methods need to be added:

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

private DataTable GetDataTable()
{
    SqlCeConnection con = new SqlCeConnection() { ConnectionString = "Enter appropriate connection string to connect with database" };
    con.Open();
    DataSet dSet = new DataSet();
    new SqlCeDataAdapter("Select * from ReportsTable", con).Fill(dSet);
    con.Close();
    return dSet.Tables[0];
}

{% endhighlight %}

### OLAP

For WebAPI controller, the below methods need to be added.

{% highlight c# %}

[System.Web.Http.ActionName("LoadReportFromDB")]
[System.Web.Http.HttpPost]
public Dictionary<string, object> LoadReportFromDB(Dictionary<string, object> jsonResult)
{
    string mode = jsonResult["operationalMode"].ToString();
    byte[] reportString = new byte[4 * 1024];
    var reports = "";
    Dictionary<string, object> dictionary = new Dictionary<string, object>();
    if (mode == "serverMode" && jsonResult.ContainsKey("clientReports"))
    {
        reports = jsonResult["clientReports"].ToString();
    }
    else
    {
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
                    reports = OLAPUTILS.Utils.CompressData(row.ItemArray[1] as byte[]);
                    break;
                }
            }
        }
    }
    if (reports != "")
    {
        OlapDataManager DataManager = new OlapDataManager(connectionString);
        dynamic customData = serializer.Deserialize<dynamic>(jsonResult["customObject"].ToString());
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
        dictionary = htmlHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["gridLayout"].ToString(), Convert.ToBoolean(jsonResult["enablePivotFieldList"].ToString()));
    }
    return dictionary;
}

private DataTable GetDataTable()
{
    SqlCeConnection con = new SqlCeConnection() { ConnectionString = "Enter appropriate connection string to connect with database" };
    con.Open();
    DataSet dSet = new DataSet();
    new SqlCeDataAdapter("Select * from ReportsTable", con).Fill(dSet);
    con.Close();
    return dSet.Tables[0];
}

{% endhighlight %}

For WCF service, the below methods need to be added.

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

private DataTable GetDataTable()
{
    SqlCeConnection con = new SqlCeConnection() { ConnectionString = "Enter appropriate connection string to connect with database" };
    con.Open();
    DataSet dSet = new DataSet();
    new SqlCeDataAdapter("Select * from ReportsTable", con).Fill(dSet);
    con.Close();
    return dSet.Tables[0];
}

{% endhighlight %}

## Load report from local storage

To load the stored report of PivotGrid from the local storage, you should call the ['loadReport'](/api/js/ejpivotgrid#members:loadReport) method in the PivotGrid.

{% highlight html %}

<div id="PivotGrid1"> </div>
<button id="btnLoad">load</button>
<script>
    $("#PivotGrid1").ejPivotGrid({
        //...
        loadReport: "loadFromLocal"
    });
    $("#btnLoad").ejButton({click:"loadReport"});
    function loadReport(){
        url = "",
        name = "report",
        storage = "local",
        pGridObj.loadReport(name, storage, url);
    }        
    function loadFromLocal(args){
        args.targetControl.model.dataSource = JSON.parse(localStorage.getItem("report"));
    }
</script>

{% endhighlight %}