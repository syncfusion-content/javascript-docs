---
layout: post
title: Getting-Started
description: getting started 
platform: js
control: OlapClient
documentation: ug
---

# Getting Started 

This section briefly explains how you can create an **OlapClient** in your application with **Essential JavaScript**.

##Syncfusion OLAP Controls – Architecture

{% include image.html url="/js/OlapClient/Getting-Started_images/Getting-Started_img2.png" %}

As shown in the above architecture, control rendering takes place in client-side and the analytical operations on each action takes place server-side.

##Service for OLAP Controls

The primary reasons for using service in an **OLAP** processing are as follows:

1. **DataSource Connectivity:** You can establish a connection between different cube data sources such as

   * Offline Cube
   * Online Cube (XML/A)
   * Cube within SQL Server, locally or through remote, you can move the connectivity related coding to service-side as it is impossible client-side other than **Online Cube** (**XML/A**) option. Using service, you can connect any cube data source without any limitation.

2. **Cube Schema:** As the connection is moved to service-side, you can use **Microsoft ADOMD assembly** to get the entire cube schema. Only with the cube schema the following details can be achieved for control rendering.

   * Availability of cubes.
   * A complete end-to-end detail such as name, caption, unique name, parent information, child information, its properties etc. about the dimension, hierarchy, level, members are available in cube schema only.
   * Localized information is also available in cube schema.

3. **MDX Generator: You can frame the MDX query using an MDX generator in Syncfusion.Olap.Base** assembly. To execute the framed **MDX** from the cube data source, you need to send framed MDX via **Microsoft ADOMD assembly**. The executed query is returned in the form of cell set, containing values that are converted to Pivot Engine and then to JSON data to render any **OLAP** controls.

4. **OLAP Report:** The **OLAP Report** holds the complete information of each axis such as column, row and slicer. Using OLAP Report, you can maintain the dimension element, measure element, hierarchy name, level name as well as member information that is included and excluded.  

As the **OLAP Control** is the key for each and every operation, initially you need to serialize the OLAP Reports and send them client-side in the form of a string.
When you perform any operation, such as drill up or down, filtering, sorting etc., you can send OLAP Reports from client-side to the service in a de-serialized and updated format.
Further operations are carried with updated OLAP Reports only, and you can send the updated OLAP Reports back to client-side with **JSON** data in a serialized format again.
This process has the OLAP Reports always updated. You cannot operate serialized OLAP Reports client-side and hence it is carried to service to perform the update operation.
   
   1. Saving and Loading Report in Database:  You can save and load the reports available in **OlapClient** control via service only. This is not applicable in client-side. You can serialize the OLAP Report and save it to database as a stream.  Also you can load it back from database via service.
   2. Exporting: You can export **OLAP** values and information to excel sheet via service only. So this provides feasible option to save and view **OLAP** information.

##Create an application

This section illustrates how to add and configure the OlapClient component in an application with AdventureWorks Cycle cube to assess the Customer Count over different fiscal years.

{% include image.html url="/js/OlapClient/Getting-Started_images/Getting-Started_img3.png" %}

Open **Visual Studio** and create a new project by clicking **New Project**. Select the **Web** category. Select the **ASP.NET Empty Web Application** template, and then click **OK**. The following screenshot of a Project Creation Wizard is displayed:

{% include image.html url="/js/OlapClient/Getting-Started_images/Getting-Started_img4.png" %}

##Create HTML page

To create a new web form in the application, right-click on the project and select Add. The following screenshot shows the Add New Item Wizard.

{% include image.html url="/js/OlapClient/Getting-Started_images/Getting-Started_img5.png" %}

Click New Item and select HTML Page from the listed templates. Name the page as default.html and click OK.

##Add References, Scripts, Styles and Control in HTML page

###Add References

* In the Solution Explorer, right-click the References folder and then click **Add Reference**.
{% include image.html url="/js/OlapClient/Getting-Started_images/Getting-Started_img6.png" %}
* The following screenshot illustrates how to refer **Syncfusion.Olap.Base.**
{% include image.html url="/js/OlapClient/Getting-Started_images/Getting-Started_img7.png" %}
* Select the following assemblies: Microsoft.AnalysisServices.AdomdClient.dll,  Syncfusion.Compression.Base.dll, Syncfusion.Linq.Base.dll, Syncfusion.Olap.Base.dll, Syncfusion.EJ.dll, Syncfusion.EJ.Olap.dll and Syncfusion.XlsIO.Base.dll, Syncfusion.DocIO.Base.dll, Syncfusion.Pdf.Base.dll , System.Data.SqlServerCe.dll (Version: 4.0.0.0).
* Click OK.

###Add Scripts and Styles 

Add the script files and CSS files in the &lt;head&gt; tag of the default.html page.

N>  Use the following code example while adding scripts and styles.

{% highlight html %}

<link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
<script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js" type="text/javascript">
</script>
<script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js" type="text/javascript">
</script>
<script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"></script>
<script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js">
</script>

{% endhighlight %}

###Add Control in HTML page

Add the following code example in the **&lt;body&gt;** tag in the **default.html** page.

{% highlight html %}

<div>
    <!--Creating a div tag, that acts as a container for ejOlapClient widget.-->
    <div id="OlapClient" style="height: 350px; width: 100%; overflow: auto">
    </div>
    <script type="text/javascript">
        //Setting property and initializing ejOlapClient widget.
        $(function() {
            $("#OlapClient").ejOlapClient({
                url: "../wcf/OlapClientService.svc”
            });
        });
    </script>
</div>

{% endhighlight %}

##Add WCF Service for OlapClient

###Create WCF Service

Right-click the project and select **Add > New Folder**.  Name the folder as **wcf.** Let the folder name "wcf" be in lower case.

{% include image.html url="/js/OlapClient/Getting-Started_images/Getting-Started_img8.png" %}

Now right-click the **wcf** folder created and select **Add > New Item.**

{% include image.html url="/js/OlapClient/Getting-Started_images/Getting-Started_img9.png" %}

In the Add New Item window, select **WCF Service** and name it **OlapClientService.svc.** Click **Add.**

{% include image.html url="/js/OlapClient/Getting-Started_images/Getting-Started_img10.png" %}

###Add service methods inside Interface

Add the following code inside the `IOlapClientService` interface available in an **IOlapClientService.cs** file.

{% highlight c# %}

[ServiceContract]

public interface IOlapClientService
{
   [OperationContract]
   Dictionary<string, object> InitializeClient(string action, string customObject, string clientParams);
        
   [OperationContract]
   Dictionary<string, object> FetchMemberTreeNodes(string action, string dimensionName, string olapReport);
        
   [OperationContract]
   Dictionary<string, object> InitializeChart(string action, string currentReport, string customObject);
        
   [OperationContract]
   Dictionary<string, object> DrillChart(string action, string drilledSeries, string olapReport, string clientReports);
        
   [OperationContract]
   Dictionary<string, object> InitializeGrid(string action, string currentReport, string gridLayout, string customObject);
        
   [OperationContract]
   Dictionary<string, object> DrillGrid(string action, string cellPosition, string currentReport, string clientReports, string headerInfo, string layout);
        
   [OperationContract]
   Dictionary<string, object> FilterElement(string action, string clientParams, string olapReport, string clientReports);
        
   [OperationContract]
   Dictionary<string, object> RemoveSplitButton(string action, string clientParams, string olapReport, string clientReports);
        
   [OperationContract]
   Dictionary<string, object> NodeDropped(string action, string dropType, string nodeInfo, string olapReport, string clientReports);
        
   [OperationContract]
   Dictionary<string, object> CubeChanged(string action, string cubeName, string clientParams);
        
   [OperationContract]
   Dictionary<string, object> MeasureGroupChanged(string action, string measureGroupName);
        
   [OperationContract]
   Dictionary<string, object> ToolbarOperations(string action, string toolbarOperation, string clientInfo, string olapReport, string clientReports);
        
   [OperationContract]
   Dictionary<string, object> UpdateReport(string action, string clientParams, string olapReport, string clientReports);
        
   [OperationContract]
   Dictionary<string, object> SaveReportToDB(string reportName, string olapReport, string clientReports);
        
   [OperationContract]
   Dictionary<string, object> LoadReportFromDB(string reportName, string olapReport, string clientReports);
        
   [OperationContract]
   Dictionary<string, object> FetchReportListFromDB();
        
   [OperationContract]
   Dictionary<string, object> MemberExpanded(string action, bool checkedStatus, string parentNode, string tag, string dimensionName, string cubeName, string olapReport, string clientReports);
        
   [OperationContract]
   void Export(System.IO.Stream stream);

}


{% endhighlight %}

###Add Namespaces

Add the following namespaces required to implement the **service** methods.

{% highlight c# %}

using System;
using System.Collections.Generic;
using System.Linq;
using System.Runtime.Serialization;
using System.ServiceModel;
using System.Text;
using System.ServiceModel.Activation;
using Syncfusion.Olap.DataProvider;
using Syncfusion.Olap.Manager;
using Syncfusion.Olap.Common;
using Syncfusion.Olap.Reports;
using System.IO;
using System.Data.SqlServerCe;
using System.Xml.Serialization;
using System.Data;
using System.Web;
using OLAPUTILS = Syncfusion.JavaScript.Olap;
using System.Web.Script.Serialization;
using Syncfusion.JavaScript;
using Syncfusion.JavaScript.Olap;

{% endhighlight %}

###Create Class in Service file

You can create the `OlapClientService` class to implement the **service** methods. You can inherit the class from the `IOlapClientService` interface that is created automatically while adding any new service.

{% highlight c# %}

namespace WebApplication2.wcf
{
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    
    public class OlapClientService : IOlapClientService
    
    {
    
    }
}


{% endhighlight %}

###Implement Service Methods

You can add the following methods to the service that are invoked for any server-side operations performed in OlapClient.

Initialize the OlapClient helper class.

{% highlight c# %}

OlapClient olapClientHelper = new OlapClient();
OlapChart htmlHelper = new OlapChart();
JavaScriptSerializer serializer = new JavaScriptSerializer();
string connectionString = "Data Source=http://bi.syncfusion.com/olap/msmdpump.dll; Initial Catalog=Adventure Works DW 2008 SE;";
string conStringforDB = "DataSource=" + HttpContext.Current.Server.MapPath(".").Split(new string[] { "\\wcf" }, StringSplitOptions.None)[0] + "\\database\\ReportsTable.sdf; Persist Security Info=False", reportTableName = "ReportsTable";

{% endhighlight %}

Add the following relevant service methods.

{% highlight c# %}

//This method provides the required information from the server side for initializing the OlapClient.
public Dictionary<string, object> InitializeClient(string action, string customObject, string clientParams)
{   
   OlapDataManager DataManager = null;
   DataManager = new OlapDataManager(connectionString);
   DataManager.SetCurrentReport(CreateOlapReport());
   return olapClientHelper.GetJsonData(action, DataManager, clientParams);
}

//This method provides the required information from the server side for initializing the PivotGrid.
public Dictionary<string, object> InitializeGrid(string action, string currentReport, string gridLayout, string customObject)
{
   OlapDataManager DataManager = new OlapDataManager(connectionString);
   DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(currentReport));
   return olapClientHelper.GetJsonData(action, DataManager, gridLayout);
}

//This method provides the required information from the server side for initializing the OlapChart.
public Dictionary<string, object> InitializeChart(string action, string currentReport, string customObject)
{
   OlapDataManager DataManager = new OlapDataManager(connectionString);
   DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(currentReport));
   return htmlHelper.GetJsonData(action, DataManager);
}

//This method provides the required information from the server side while drill up/down operation is performed in OlapChart.
public Dictionary<string, object> DrillChart(string action, string drilledSeries, string olapReport, string clientReports)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(olapReport));
    DataManager.Reports = olapClientHelper.DeserializedReports(clientReports);
    return htmlHelper.GetJsonData(action, DataManager, drilledSeries);
}

//This method provides the required information from server-side while the filtering operation is performed with the members inside respective dimension.
public Dictionary<string, object> FilterElement(string action, string clientParams, string olapReport, string clientReports)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(olapReport));
    DataManager.Reports = olapClientHelper.DeserializedReports(clientReports);
    return olapClientHelper.GetJsonData(action, DataManager, clientParams);
}

//This method provides the required information from server-side while a split button is removed from any axis.
public Dictionary<string, object> RemoveSplitButton(string action, string clientParams, string olapReport, string clientReports)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(olapReport));
    DataManager.Reports = olapClientHelper.DeserializedReports(clientReports);
    return olapClientHelper.GetJsonData(action, DataManager, clientParams);
}

//This method provides the required information from server-side while creating a member tree-view inside the editor dialog.
public Dictionary<string, object> FetchMemberTreeNodes(string action, string dimensionName, string olapReport)
{
   OlapDataManager DataManager = new OlapDataManager(connectionString);
   DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(olapReport));
   return olapClientHelper.GetJsonData(action, DataManager, dimensionName);
}

//This method provides the required information from server-side while the drill up or down operation is performed in PivotGrid.
public Dictionary<string, object> DrillGrid(string action, string cellPosition, string currentReport, string clientReports, string headerInfo, string layout)
{
   OlapDataManager DataManager = new OlapDataManager(connectionString);
   DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(currentReport));
   DataManager.Reports = olapClientHelper.DeserializedReports(clientReports);
   return olapClientHelper.GetJsonData(action, DataManager, cellPosition, headerInfo, layout);
}

//This method provides the required information from server-side while a node is dropped to any of the axes. 
public Dictionary<string, object> NodeDropped(string action, string dropType, string nodeInfo, string olapReport, string clientReports)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(olapReport));
    DataManager.Reports = olapClientHelper.DeserializedReports(clientReports);
    return olapClientHelper.GetJsonData(action, DataManager, dropType, nodeInfo);
}

//This method provides the required information from server-side while a cube is changed.
public Dictionary<string, object> CubeChanged(string action, string cubeName, string clientParams)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    return olapClientHelper.GetJsonData(action, DataManager, cubeName, clientParams);
}

//This method provides the required information from server-side while measure group name is changed.
public Dictionary<string, object> MeasureGroupChanged(string action, string measureGroupName)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    return olapClientHelper.GetJsonData(action, DataManager, measureGroupName);
}

//This method provides the required information from server-side while any toolbar operations are performed.
public Dictionary<string, object> ToolbarOperations(string action, string toolbarOperation, string clientInfo, string olapReport, string clientReports)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    if (!string.IsNullOrEmpty(olapReport))
    DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(olapReport));
    if (!string.IsNullOrEmpty(clientReports))
    DataManager.Reports = olapClientHelper.DeserializedReports(clientReports);
    return olapClientHelper.GetJsonData(action, DataManager, toolbarOperation, clientInfo);
}
//This method fetches the required information from server-side while expanding a member inside member editor dialog.
public Dictionary<string, object> MemberExpanded(string action, bool checkedStatus, string parentNode, string tag, string dimensionName, string cubeName, string olapReport, string clientReports)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    if (!string.IsNullOrEmpty(olapReport))
        DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(olapReport));
    if (!string.IsNullOrEmpty(clientReports))
        DataManager.Reports = olapClientHelper.DeserializedReports(clientReports);
    return olapClientHelper.GetJsonData(action, DataManager, checkedStatus, parentNode, tag, dimensionName, cubeName);
}

//This method fetches the required information from server-side while updating reports using measure group.
public Dictionary<string, object> UpdateReport(string action, string clientParams, string olapReport, string clientReports)
{
    return olapClientHelper.GetJsonData(action, clientParams, olapReport, clientReports);
}

//This method saves the OlapReports with the specific or entered name into the database.
public Dictionary<string, object> SaveReportToDB(string reportName, string olapReport, string clientReports)
{
    SqlCeConnection con = new SqlCeConnection() { ConnectionString = conStringforDB };
    con.Open();
    SqlCeCommand cmd1 = new SqlCeCommand("insert into ReportsTable Values(@ReportName,@Reports)", con);
    cmd1.Parameters.Add("@ReportName", reportName);
    cmd1.Parameters.Add("@Reports", OLAPUTILS.Utils.GetReportStream(clientReports).ToArray());
    cmd1.ExecuteNonQuery();
    con.Close();
    return null;
}

//This method fetches the list of OlapReports stored in the database.
public Dictionary<string, object> FetchReportListFromDB()
{
    string reportNames = string.Empty;
    foreach (System.Data.DataRow row in GetDataTable().Rows)
        reportNames = reportNames == "" ? (row.ItemArray[0] as string) : reportNames + "__" + (row.ItemArray[0] as string);
    Dictionary<string, object> dictionary = new Dictionary<string, object>();
    dictionary.Add("ReportNameList", reportNames);
    return dictionary;
}

//This method loads the selected OlapReports from the database based on the name with which it has been stored. 
public Dictionary<string, object> LoadReportFromDB(string reportName, string olapReport, string clientReports)
{
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    var reportString = "";
    foreach (DataRow row in GetDataTable().Rows)
    {
        if ((row.ItemArray[0] as string).Equals(reportName))
        {
            reportString = OLAPUTILS.Utils.CompressData(row.ItemArray[1] as byte[]);
            break;
        }
    }
    DataManager.Reports = olapClientHelper.DeserializedReports(reportString);
    DataManager.SetCurrentReport(DataManager.Reports[0]);
    return olapClientHelper.GetJsonData("toolbarOperation", DataManager, "Load Report", reportName);
}

//This method returns the table containing the reports from the database.
private DataTable GetDataTable()
{
    SqlCeConnection con = new SqlCeConnection() { ConnectionString = conStringforDB };
    con.Open();
    DataSet dSet = new DataSet();
    new SqlCeDataAdapter("Select * from ReportsTable", con).Fill(dSet);
    con.Close();
    return dSet.Tables[0];
}

//This method exports the PivotGrid content to an excel sheet.
public void Export(Stream stream) 
{
    System.IO.StreamReader sReader = new System.IO.StreamReader(stream);
    string args = System.Web.HttpContext.Current.Server.UrlDecode(sReader.ReadToEnd());
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    string fileName = "Sample";
    olapClientHelper.ExportOlapClient(DataManager, args, fileName, System.Web.HttpContext.Current.Response);
}

//This method carries the information about the default report that is rendered within OlapClient initially.
private OlapReport CreateOlapReport()
{
   OlapReport olapReport = new OlapReport() { Name = "Default Report" };
   olapReport.CurrentCubeName = "Adventure Works";
   MeasureElements measureElement = new MeasureElements();
   measureElement.Elements.Add(new MeasureElement { UniqueName = "[Measures].[Customer Count]" });

   DimensionElement dimensionElementRow = new DimensionElement();
   dimensionElementRow.Name = "Date";
   dimensionElementRow.AddLevel("Fiscal", "Fiscal Year");

   olapReport.SeriesElements.Add(dimensionElementRow);
   olapReport.CategoricalElements.Add(measureElement);

   return olapReport;
}

{% endhighlight %}

###Configure Web.Config

* You can expose services through the properties such as binding, contract and address etc. using an endpoint. In your application the service name is `WebApplication2.wcf.OlapClientService` where `OlapClientService` is the service class name and `WebApplication2.wcf` is the namespace name where the service class appears. The following are the properties that meet the appropriate endpoint.

   1. **Contract:** This property indicates the contract of the endpoint is exposed. Here you are referring to the **IOlapClientService** contract hence it is `WebApplication2.wcf.IOlapClientService`.
   2. **Binding:** In your application, you can use `webHttpBinding` to post and receive the requests and responses between client-end and service-end.
   3. **BehaviorConfiguration:** This property contains the name of the behavior used in the endpoint. **endpointBehaviors** are illustrated as follows**.**


{% highlight xml %}

<services>
   <service name="WebApplication2.wcf.OlapClientService">
      <endpoint address="" behaviorConfiguration="WebApplication2.wcf.OlapClientServiceAspNetAjaxBehavior"
      binding="webHttpBinding" contract="WebApplication2.wcf.IOlapClientService" />
   </service>
</services>


{% endhighlight %}

* The `endpointBehaviors` contains all the behaviors for an endpoint. You can link each endpoint to the respective behavior only by using the `name` property. In the following code example, `WebApplication2.wcf.OlapClientServiceAspNetAjaxBehavior` refers to the **OlapClientService** class under the namespace **WebApplication2.wcf** in **OlapClientService.svc.cs** file. That is the appropriate behavior for the endpoint.

{% highlight xml %}

<endpointBehaviors>
   <behavior name="WebApplication2.wcf.OlapClientServiceAspNetAjaxBehavior">
      <enableWebScript />
   </behavior>
</endpointBehaviors>

{% endhighlight %}

N>  In this example, “WebApplication2.wcf” indicates the namespace in the WCF Service and “OlapClientService” indicates the class name in the WCF Service.



