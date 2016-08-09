---
layout: post
title: Getting-Started
description: getting started 
platform: js
control: OlapClient
documentation: ug
---

# Getting Started

##Creating a simple application with OlapClient

This section covers the information required to create a simple OlapClient bound to OLAP datasource.

N> We will be illustrating this section by creating a simple Web Application through Visual Studio IDE since OlapClient is a server-side control with .NET dependency. The Web Application would contain a HTML page and a service that would transfer data to server-side, process and return back the data to client-side for control re-rendering. The service utilized for communication could be either WCF or WebAPI based on user requirement and we have illustrated both for user convenience.

###Project Initialization
Create a new **ASP.NET Empty Web Application** by using Visual Studio IDE and name the project as **“OlapClientDemo”**.

Next, add a HTML page. To add a HTML page in your Web Application, right-click on the project in Solution Explorer and select **Add > New Item.** In the **Add New Item** window, select **HTML Page** and name it as “GettingStarted.html”, click **Add.**

Now, set “GettingStarted.html” as start-up page by right-clicking on “GettingStarted.html” page and select **“Set As Start Page”.**

###Scripts and CSS Initialization
The scripts and style sheets that are mandatorily required to render OlapClient widget inside a HTML page are highlighted in an appropriate order as follows,

1. ej.web.all.min.css
2. jQuery-1.10.2.min.js
3. jQuery.easing.1.3.min.js
4. jQuery.globalize.min.js
5. ej.web.all.min.js

You can find the scripts and style sheets listed above could in any of the following locations:

Local Disk: [Click here](http://helpjs.syncfusion.com/js/installation-and-deployment) to know more about script and style sheets installed in local machine.

CDN Link: [Click here](http://helpjs.syncfusion.com/js/cdn) to know more about script and style sheets available online.

NuGet Package: [Click here](http://helpjs.syncfusion.com/js/installation-and-deployment#configuring-syncfusion-nuget-packages) to know more about script and style sheets available in NuGet package. 

###Control Initialization
In-order to initialize a OlapClient widget, first you need to define a “div” tag with an appropriate “id” attribute which acts as a container for OlapClient widget. Then you need to initialize the widget using ejOlapClient method.

{% highlight html %}
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">

<head>
    <title>OlapClient - Getting Started</title>
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" type="text/css" />
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js" type="text/javascript"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js" type="text/javascript"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"></script>  
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js" type="text/javascript"></script>
</head>

<body>
    <form id="form1" runat="server">
        <div>
            <!--Creating a div tag, that acts as a container for ejOlapClient widget.-->
            <div id="OlapClient" style="height: 900px; width: 100%; overflow: auto"> </div>
            <script type="text/javascript">
                //Setting property and initializing ejOlapClient widget.
                $(function()
                {
                    $("#OlapClient").ejOlapClient(
                    {
                        url: "/OlapClientService",title: "OLAP Browser"
                    });
                });
            </script>
        </div>
    </form>
</body>
</html>

{% endhighlight %}

The “url” property in OlapClient widget points the service endpoint, where data are processed and fetched in the form of JSON. The service used for the OlapClient widget as endpoint are WCF and WebAPI.

N> The above "GettingStarted.html" contains WebAPI URL, which is **“/OlapClientService”**. Suppose if you are using WCF service, then the URL would look like **“/OlapClientService.svc”**. 

###WebAPI

**Adding a WebAPI Controller**

To add a WebAPI controller in your existing Web Application, right-click on the project in Solution Explorer and select **Add > New Item.** In the **Add New Item** window, select **WebAPI Controller Class** and name it as **“OlapClientServiceController.cs”**, click **Add.**

Now, WebAPI controller is added into your application successfully with the following file. The utilization of this file will be explained in the following sections.
 
* OlapClientServiceController.cs

N> While adding WebAPI Controller Class, name it with the suffix “Controller” which is mandatory. For example, in demo the controller is named “OlapClientServiceController”.

Next, remove all the existing methods such as “Get”, “Post”, “Put” and “Delete” present inside `OlapClientServiceController.cs` file. 

{% highlight c# %}

namespace OlapClientDemo
{
    public class OlapClientServiceController: ApiController
    {
    
    }
}

{% endhighlight %}

**List of Dependency Libraries**

Next, add the following dependency libraries into your Web Application. You can find these libraries in GAC (Global Assembly Cache) in your machine.

To add them to your Web Application, right-click on **References** in Solution Explorer and select **Add Reference.** Now in the **Reference Manager** dialog, under **Assemblies > Extension**, the following Syncfusion libraries are found. 

>**NOTE: If you have installed any version of SQL Server Analysis Service (SSAS) or Microsoft ADOMD.NET utility, then the location of Microsoft.AnalysisServices.AdomdClient library is [system drive:\Program Files (x86)\Microsoft.NET\ADOMD.NET]**

* Microsoft.AnalysisServices.AdomdClient.dll
* Syncfusion.Compression.Base.dll
* Syncfusion.Linq.Base.dll
* Syncfusion.Olap.Base.dll
* Syncfusion.EJ.dll
* Syncfusion.EJ.Olap.dll 
* Syncfusion.XlsIO.Base.dll
* Syncfusion.DocIO.Base.dll
* Syncfusion.Pdf.Base.dll
* System.Data.SqlServerCe.dll (Version: 4.0.0.0).


**List of Namespaces**

The following are the list of namespaces to be added on top of the main class inside `OlapClientServiceController.cs` file.

{% highlight c# %}

using System.Data.SqlServerCe;
using System.Data;
using System.Web;
using System.Web.Http;
using Syncfusion.JavaScript.Olap;
using Syncfusion.Olap.Manager;
using Syncfusion.Olap.Reports;
using System.Web.Script.Serialization;
using OLAPUTILS = Syncfusion.JavaScript.Olap;

namespace OlapClientDemo
{
    public class OlapClientServiceController: ApiController
    {
    
    }
}
{% endhighlight %}

**Datasource Initialization**

Now, the connection string to connect OLAP Cube, OlapClient and JavaScriptSerializer instances are created immediately inside the main class in `OlapClientServiceController.cs` file. Also, the database connection for saving and loading reports is provided appropriately. 

{% highlight c# %}

namespace OlapClientDemo
{
    public class OlapClientServiceController: ApiController
    {
        OlapClient olapClientHelper = new OlapClient();
        string connectionString = "Data Source=http://bi.syncfusion.com/olap/msmdpump.dll; Initial Catalog=Adventure Works DW 2008 SE;";
        string conStringforDB = "DataSource=" + HttpContext.Current.Server.MapPath(".").Split(new string[] { "\\api" }, StringSplitOptions.None)[0] + "\\database\\ReportsTable.sdf; Persist Security Info=False", reportTableName = "ReportsTable";
        OlapChart htmlHelper = new OlapChart();
        PivotTreeMap treemapHelper = new PivotTreeMap();
        JavaScriptSerializer serializer = new JavaScriptSerializer();
        //Other codes
    }
}

{% endhighlight %}

**Service methods in WebAPI Controller**

Now you need to define the service methods inside OlapClientServiceController class, found inside `OlapClientServiceController.cs` file, created while adding WebAPI Controller Class to your Web Application.
 
{% highlight c# %}

namespace OlapClientDemo
{
    public class OlapClientServiceController: ApiController
    {
        OlapClient olapClientHelper = new OlapClient();
        string connectionString = "Data Source=http://bi.syncfusion.com/olap/msmdpump.dll; Initial Catalog=Adventure Works DW 2008 SE;";
        string conStringforDB = "DataSource=" + HttpContext.Current.Server.MapPath(".").Split(new string[] { "\\api" }, StringSplitOptions.None)[0] + "\\database\\ReportsTable.sdf; Persist Security Info=False", reportTableName = "ReportsTable";
        OlapChart htmlHelper = new OlapChart();
        PivotTreeMap treemapHelper = new PivotTreeMap();
        JavaScriptSerializer serializer = new JavaScriptSerializer();
        [System.Web.Http.ActionName("InitializeClient")]
        [System.Web.Http.HttpPost]
        public Dictionary < string, object > InitializeClient(Dictionary < string, object > jsonResult)
            {
                OlapDataManager DataManager = new OlapDataManager(connectionString);
                DataManager.SetCurrentReport(CreateOlapReport());
                return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["clientParams"].ToString());
            }
            [System.Web.Http.ActionName("InitializeGrid")]
            [System.Web.Http.HttpPost]
        public Dictionary < string, object > InitializeGrid(Dictionary < string, object > jsonResult)
            {
                OlapDataManager DataManager = new OlapDataManager(connectionString);
                DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
                return jsonResult.ContainsKey("gridLayout") ? olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["gridLayout"].ToString()) : olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager);
            }
            [System.Web.Http.ActionName("InitializeChart")]
            [System.Web.Http.HttpPost]
        public Dictionary < string, object > InitializeChart(Dictionary < string, object > jsonResult)
            {
                OlapDataManager DataManager = new OlapDataManager(connectionString);
                DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
                return htmlHelper.GetJsonData(jsonResult["action"].ToString(), DataManager);
            }
            [System.Web.Http.ActionName("InitializeTreeMap")]
            [System.Web.Http.HttpPost]
        public Dictionary < string, object > InitializeTreeMap(Dictionary< string, object > jsonResult)
            {
                OlapDataManager DataManager = new OlapDataManager(connectionString);
                DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
                return treemapHelper.GetJsonData(jsonResult["action"].ToString(), DataManager);
            }
            [System.Web.Http.ActionName("DrillChart")]
            [System.Web.Http.HttpPost]
        public Dictionary < string, object > DrillChart(Dictionary < string, object > jsonResult)
            {
                OlapDataManager DataManager = new OlapDataManager(connectionString);
                DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(jsonResult["olapReport"].ToString()));
                DataManager.Reports = olapClientHelper.DeserializedReports(jsonResult["clientReports"].ToString());
                return htmlHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["drilledSeries"].ToString());
            }
            [System.Web.Http.ActionName("DrillTreeMap")]
            [System.Web.Http.HttpPost]
        public Dictionary< string, object > DrillTreeMap(Dictionary< string, object > jsonResult)
            {
                OlapDataManager DataManager = new OlapDataManager(connectionString);
                DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(jsonResult["olapReport"].ToString()));
                DataManager.Reports = olapClientHelper.DeserializedReports(jsonResult["clientReports"].ToString());
                return treemapHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["drillInfo"].ToString());
            }   
            [System.Web.Http.ActionName("FilterElement")]
            [System.Web.Http.HttpPost]
        public Dictionary < string, object > FilterElement(Dictionary < string, object > jsonResult)
            {
                OlapDataManager DataManager = new OlapDataManager(connectionString);
                DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(jsonResult["olapReport"].ToString()));
                DataManager.Reports = olapClientHelper.DeserializedReports(jsonResult["clientReports"].ToString());
                return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["clientParams"].ToString());
            }
            [System.Web.Http.ActionName("RemoveSplitButton")]
            [System.Web.Http.HttpPost]
        public Dictionary < string, object > RemoveSplitButton(Dictionary < string, object > jsonResult)
            {
                OlapDataManager DataManager = new OlapDataManager(connectionString);
                DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(jsonResult["olapReport"].ToString()));
                DataManager.Reports = olapClientHelper.DeserializedReports(jsonResult["clientReports"].ToString());
                return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["clientParams"].ToString());
            }
            [System.Web.Http.ActionName("FetchMemberTreeNodes")]
            [System.Web.Http.HttpPost]
        public Dictionary < string, object > FetchMemberTreeNodes(Dictionary < string, object > jsonResult)
            {
                OlapDataManager DataManager = new OlapDataManager(connectionString);
                DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(jsonResult["olapReport"].ToString()));
                return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["dimensionName"].ToString());
            }
            [System.Web.Http.ActionName("DrillGrid")]
            [System.Web.Http.HttpPost]
         public Dictionary< string, object > DrillGrid(Dictionary< string, object > jsonResult)
        {
            OlapDataManager DataManager = new OlapDataManager(connectionString);
            DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
            DataManager.Reports = olapClientHelper.DeserializedReports(jsonResult["clientReports"].ToString());
            return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["cellPosition"].ToString(), jsonResult["headerInfo"].ToString(), jsonResult["layout"].ToString());
        }
            [System.Web.Http.ActionName("NodeDropped")]
            [System.Web.Http.HttpPost]
        public Dictionary < string, object > NodeDropped(Dictionary < string, object > jsonResult)
            {
                OlapDataManager DataManager = new OlapDataManager(connectionString);
                DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(jsonResult["olapReport"].ToString()));
                DataManager.Reports = olapClientHelper.DeserializedReports(jsonResult["clientReports"].ToString());
                return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["dropType"].ToString(), jsonResult["nodeInfo"].ToString());
            }
            [System.Web.Http.ActionName("CubeChanged")]
            [System.Web.Http.HttpPost]
        public Dictionary < string, object > CubeChanged(Dictionary < string, object > jsonResult)
            {
                OlapDataManager DataManager = new OlapDataManager(connectionString);
                return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["cubeName"].ToString(), jsonResult["clientParams"].ToString());
            }
            [System.Web.Http.ActionName("MeasureGroupChanged")]
            [System.Web.Http.HttpPost]
        public Dictionary < string, object > MeasureGroupChanged(Dictionary < string, object > jsonResult)
            {
                OlapDataManager DataManager = new OlapDataManager(connectionString);
                return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["measureGroupName"].ToString());
            }
            [System.Web.Http.ActionName("ToolbarOperations")]
            [System.Web.Http.HttpPost]
        public Dictionary < string, object > ToolbarOperations(Dictionary < string, object > jsonResult)
            {
                var toolbarOperation = "";
                OlapDataManager DataManager = new OlapDataManager(connectionString);
                if (jsonResult["olapReport"] != null && (!string.IsNullOrEmpty(jsonResult["olapReport"].ToString()))) DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(jsonResult["olapReport"].ToString()));
                if (!string.IsNullOrEmpty(jsonResult["clientReports"].ToString())) DataManager.Reports = olapClientHelper.DeserializedReports(jsonResult["clientReports"].ToString());
                toolbarOperation = jsonResult["toolbarOperation"] == null ? null : jsonResult["toolbarOperation"].ToString();
                return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, toolbarOperation, jsonResult["clientInfo"].ToString());
            }
            [System.Web.Http.ActionName("MemberExpanded")]
            [System.Web.Http.HttpPost]
        public Dictionary < string, object > MemberExpanded(Dictionary < string, object > jsonResult)
            {
                OlapDataManager DataManager = new OlapDataManager(connectionString);
                if (!string.IsNullOrEmpty(jsonResult["olapReport"].ToString())) DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(jsonResult["olapReport"].ToString()));
                if (!string.IsNullOrEmpty(jsonResult["clientReports"].ToString())) DataManager.Reports = olapClientHelper.DeserializedReports(jsonResult["clientReports"].ToString());
                return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, Convert.ToBoolean(jsonResult["checkedStatus"].ToString()), jsonResult["parentNode"].ToString(), jsonResult["tag"].ToString(), jsonResult["dimensionName"].ToString(), jsonResult["cubeName"].ToString());
            }
            [System.Web.Http.ActionName("UpdateReport")]
            [System.Web.Http.HttpPost]
        public Dictionary < string, object > UpdateReport(Dictionary < string, object > jsonResult)
            {
                return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), jsonResult["clientParams"].ToString(), jsonResult["olapReport"].ToString(), jsonResult["clientReports"].ToString());
            }
            [System.Web.Http.ActionName("SaveReportToDB")]
            [System.Web.Http.HttpPost]
        public Dictionary < string, object > SaveReportToDB(Dictionary < string, object > jsonResult)
            {
                SqlCeConnection con = new SqlCeConnection()
                {
                    ConnectionString = conStringforDB
                };
                con.Open();
                SqlCeCommand cmd1 = new SqlCeCommand("insert into ReportsTable Values(@ReportName,@Reports)", con);
                cmd1.Parameters.Add("@ReportName", jsonResult["reportName"].ToString());
                cmd1.Parameters.Add("@Reports", OLAPUTILS.Utils.GetReportStream(jsonResult["clientReports"].ToString()).ToArray());
                cmd1.ExecuteNonQuery();
                con.Close();
                return null;
            }
            [System.Web.Http.ActionName("FetchReportListFromDB")]
            [System.Web.Http.HttpPost]
        public Dictionary < string, object > FetchReportListFromDB()
            {
                string reportNames = string.Empty;
                foreach(System.Data.DataRow row in GetDataTable().Rows)
                reportNames = reportNames == "" ? (row.ItemArray[0] as string) : reportNames + "__" + (row.ItemArray[0] as string);
                Dictionary < string, object > dictionary = new Dictionary < string, object > ();
                dictionary.Add("ReportNameList", reportNames);
                return dictionary;
            }
            [System.Web.Http.ActionName("LoadReportFromDB")]
            [System.Web.Http.HttpPost]
        public Dictionary < string, object > LoadReportFromDB(Dictionary < string, object > jsonResult)
        {
            OlapDataManager DataManager = new OlapDataManager(connectionString);
            var reportString = "";
            foreach(DataRow row in GetDataTable().Rows)
            {
                if ((row.ItemArray[0] as string).Equals(jsonResult["reportName"].ToString()))
                {
                    reportString = OLAPUTILS.Utils.CompressData(row.ItemArray[1] as byte[]);
                    break;
                }
            }
            DataManager.Reports = olapClientHelper.DeserializedReports(reportString);
            DataManager.SetCurrentReport(DataManager.Reports[0]);
            return olapClientHelper.GetJsonData("toolbarOperation", DataManager, "Load Report", jsonResult["reportName"].ToString());
        }
        private DataTable GetDataTable()
            {
                SqlCeConnection con = new SqlCeConnection()
                {
                    ConnectionString = conStringforDB
                };
                con.Open();
                DataSet dSet = new DataSet();
                new SqlCeDataAdapter("Select * from ReportsTable", con).Fill(dSet);
                con.Close();
                return dSet.Tables[0];
            }
            [System.Web.Http.ActionName("Export")]
            [System.Web.Http.HttpPost]
        public void Export()
            {
                string args = HttpContext.Current.Request.Form.GetValues(0)[0];
                OlapDataManager DataManager = new OlapDataManager(connectionString);
                string fileName = "Sample";
                olapClientHelper.ExportOlapClient(DataManager, args, fileName, System.Web.HttpContext.Current.Response);
            }
            [System.Web.Http.ActionName("GetMDXQuery")]
            [System.Web.Http.HttpPost]
        public string GetMDXQuery(Dictionary < string, object > jsonResult)
            {
                OlapDataManager DataManager = new OlapDataManager(connectionString);
                DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(jsonResult["olapReport"].ToString()));
                return DataManager.GetMDXQuery();
            }
            [System.Web.Http.ActionName("ToggleAxis")]
            [System.Web.Http.HttpPost]
        public Dictionary < string, object > ToggleAxis(Dictionary < string, object > jsonResult)
        {
            OlapDataManager DataManager = new OlapDataManager(connectionString);
            DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
            DataManager.Reports = olapClientHelper.DeserializedReports(jsonResult["clientReports"].ToString());
            DataManager.ToggleAxis(DataManager.CurrentReport);
            return olapClientHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["clientReports"].ToString());
        }
        private OlapReport CreateOlapReport()
        {
            OlapReport olapReport = new OlapReport()
            {
                Name = "Default Report"
            };
            olapReport.CurrentCubeName = "Adventure Works";
            MeasureElements measureElement = new MeasureElements();
            measureElement.Elements.Add(new MeasureElement
            {
                UniqueName = "[Measures].[Customer Count]"
            });
            DimensionElement dimensionElementRow = new DimensionElement();
            dimensionElementRow.Name = "Date";
            dimensionElementRow.AddLevel("Fiscal", "Fiscal Year");
            olapReport.SeriesElements.Add(dimensionElementRow);
            olapReport.CategoricalElements.Add(measureElement);
            return olapReport;
        }
    }
}
{% endhighlight %}

**Configure routing in Global Application Class**

To add a Global.asax in your existing Web Application, right-click on the project in Solution Explorer and select **Add > New Item.** In the **Add New Item** window, select **Global Application Class** and name it as “Global.asax”, click **Add.**
Once you finish adding the **Global.asax** file, immediately add the namespace **“using System.Web.Http;”** and then you can configure routing like in the following code example.

{% highlight c# %}

public class Global: System.Web.HttpApplication
{
    protected void Application_Start(object sender, EventArgs e)
    {
        System.Web.Http.GlobalConfiguration.Configuration.Routes.MapHttpRoute(name: "DefaultApi", routeTemplate: "{controller}/{action}/{id}", defaults: new
        {
            id = RouteParameter.Optional
        });
        AppDomain.CurrentDomain.SetData("SQLServerCompactEditionUnderWebHosting", true);
    }
}
{% endhighlight %}

Now, OlapClient is rendered with OlapChart and PivotGird showing Customer Count over a period of fiscal years.

{% include image.html url="/js/OlapClient/Getting-Started_images/OlapClient.png" %}

###WCF
This section demonstrates the utilization of WCF service as endpoint binding OLAP datasource to a simple OlapClient. For more details on this topic, [click here](http://help.syncfusion.com/js/olapclient/data-binding#wcf).




