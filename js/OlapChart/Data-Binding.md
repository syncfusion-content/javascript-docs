---
layout: post
title: Data-Binding
description: data binding
platform: js
control: OlapChart
documentation: ug
---

# DataBinding 

###Binding OlapChart to Offline Cube

To connect an OLAP Cube available in local machine, set the physical path of the Cube in the connection string. The following code example illustrates the same.

{% highlight c# %}

string connectionString = @"DataSource= system drive:\OfflineCube\Adventure_Works_Ext.cub; Provider = MSOLAP;";
OlapDataManager DataManager = new OlapDataManager(connectionString);

{% endhighlight %}

###Binding OlapChart to Cube in local SQL Server

To connect an OLAP Cube available in SQL Server Analysis Service in local machine, set the server name and database name in the connection string. When you have any credentials to connect your Cube, then set the “User ID” and “Password” attributes accordingly. The following code example illustrates the same.

{% highlight c# %}

string connectionString = "Data source=localhost; Initial Catalog=Adventure Works DW;";
OlapDataManager DataManager = new OlapDataManager(connectionString);

{% endhighlight %}

###Binding OlapChart to Cube in online SQL Server

To connect an OLAP Cube available in SQL Server Analysis Service in online server through `**XML/A**`, set the host server link and database name in the connection string. When you have any credentials to connect your Cube, then set the “User ID” and “Password” attributes accordingly. The following code example illustrates the same.


{% highlight c# %}

static string connectionString = "Data Source=http://bi.syncfusion.com/olap/msmdpump.dll; Initial Catalog=Adventure Works DW 2008 SE;";   
OlapDataManager DataManager = new OlapDataManager(connectionString);

{% endhighlight %}

###Binding OlapChart to Cube in online Mondrian Server

To connect an OLAP Cube available in Mondrian Server through `**XML/A**`, set the host server link and database name in the connection string. When you have any credentials to connect your Cube, then set the “User ID” and “Password” attributes accordingly. The following code example illustrates the same.

{% highlight c# %}

string connectionString = @"Data Source = http://localhost:8080/mondrian/xmla; Initial Catalog =FoodMart;";
OlapDataManager DataManager = new OlapDataManager(connectionString);
DataManager.DataProvider.ProviderName = Syncfusion.Olap.DataProvider.Providers.Mondrian;

{% endhighlight %}


###Binding OlapChart to Cube in online ActivePivot Server
To connect an OLAP Cube available in ActivePivot Server through `**XML/A**`, set the host server link and database name in the connection string. When you have any credentials to connect your Cube, then set the “User ID” and “Password” attributes accordingly. The following code example illustrates the same.

{% highlight c# %}

string connectionString=@"Data Source=http://localhost:8081/var_s/xmla; Initial Catalog=VaRCubes; User ID=; Password=; Transport Compression=None;";
OlapDataManager DataManager = new OlapDataManager(connectionString);
DataManager.DataProvider.ProviderName=Syncfusion.Olap.DataProvider.Providers.ActivePivot;

{% endhighlight %}



###WCF
**Adding a WCF Service**

To add a WCF service in an existing web application, right-click on project in Solution Explorer and select **Add > New Item**. In the **Add New Item** window, select WCF Service and name it as “OlapChartService.svc”, click Add.

Now, WCF service is added into your application successfully and it comprises of the following files. The utilization of these files is explained in the immediate sections.

* OlapChartService.svc
* OlapChartService.svc.cs
* IOlapChartService.svc.cs

**Configuring WCF Service Class**

Remove the “DoWork” method present inside both OlapChartService.svc.cs and IOlapChartService.cs files. Next, add “AspNetCompatibilityRequirements” attribute on top of main class present inside `**OlapChartService.svc.cs**` and set “RequirementsMode” value as “Allowed”.

{% highlight c# %}

namespace OlapChartDemo
{
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class OlapChartService: IOlapChartService
    {
    
    }
}
{% endhighlight %}

**List of Dependency Libraries**

Next, add the following dependency libraries into your Web Application. These libraries can be found in GAC (Global Assembly Cache) in your machine.
 
To add them to your Web Application, right-click on **References** in Solution Explorer and select **Add Reference**. Now, in the **Reference Manager** dialog, under **Assemblies > Extension**, the following Syncfusion libraries are found. 

>**NOTE: When you have installed any version of SQL Server Analysis Service (SSAS) or Microsoft ADOMD.NET utility, then the location of Microsoft.AnalysisServices.AdomdClient library is [system drive:\Program Files (x86)\Microsoft.NET\ADOMD.NET]**

* Microsoft.AnalysisServices.AdomdClient.dll,  
* Syncfusion.Linq.Base.dll, 
* Syncfusion.Olap.Base.dll,  
* Syncfusion.EJ.dll 
* Syncfusion.EJ.Olap.dll.
* Syncfusion.Pdf.Base.dll
* Syncfusion.XlsIO.Base.dll
* Syncfusion.DocIO.Base.dll

**List of Namespaces**

Following are the list of namespaces to be added on top of the main class inside `**OlapChartService.svc.cs**` file.

{% highlight c# %}

using System.ServiceModel.Activation;
using Syncfusion.Olap.Manager;
using Syncfusion.Olap.Reports;
using Syncfusion.JavaScript.Olap;
using System.Web.Script.Serialization;

namespace OlapChartDemo
{
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class OlapChartService: IOlapChartService
    {
    
    }
}
{% endhighlight %}

**Datasource Initialization**

Now, the connection string to connect OLAP Cube, OlapChart and JavaScriptSerializer instances are created immediately inside the main class in `**OlapChartService.svc.cs**` file.

{% highlight c# %}

namespace OlapChartDemo
{
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class OlapChartService: IOlapChartService
    {
        OlapChart htmlHelper = new OlapChart();
        string connectionString = "Data Source=http://bi.syncfusion.com/olap/msmdpump.dll; Initial Catalog=Adventure Works DW 2008 SE;";
        JavaScriptSerializer serializer = new JavaScriptSerializer();
        //Other codes
    }
}

{% endhighlight %}

**Service methods in WCF Service**

First, define the service methods inside IOlapChartService interface, found in `**IOlapChartService.cs**` file, created while adding WCF Service to your Web Application.

 {% highlight c# %}

namespace OlapChartDemo
{
    [ServiceContract]
    public interface IOlapChartService
    {
        [OperationContract]
        Dictionary < string, object > InitializeChart(string action, string customObject);
        [OperationContract]
        Dictionary < string, object > DrillChart(string action, string drilledSeries, string olapReport, string customObject);
        [OperationContract]
        void Export(System.IO.Stream stream);
    }
}

Secondly, elaborate the service methods inside the main class, found in OlapChartService.svc.cs file

namespace OlapChartDemo
{
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class OlapChartService: IOlapChartService
    {
        OlapChart htmlHelper = new OlapChart();
        string connectionString = "Data Source=http://bi.syncfusion.com/olap/msmdpump.dll; Initial Catalog=Adventure Works DW 2008 SE;";
        JavaScriptSerializer serializer = new JavaScriptSerializer();
        //This method provides the required information from server-side to initialize the OlapChart.
        public Dictionary < string, object > InitializeChart(string action, string customObject)
            {
                OlapDataManager DataManager = new OlapDataManager(connectionString);
                DataManager.SetCurrentReport(CreateOlapReport());
                return htmlHelper.GetJsonData(action, DataManager);
            }
            //This method provides the required information from server-side while the drill up or down operation is performed in OlapChart.
        public Dictionary < string, object > DrillChart(string action, string drilledSeries, string olapReport, string customObject)
            {
                OlapDataManager DataManager = new OlapDataManager(connectionString);
                DataManager.SetCurrentReport(Utils.DeserializeOlapReport(olapReport));
                dynamic customData = serializer.Deserialize < dynamic > (customObject.ToString());
                return htmlHelper.GetJsonData(action, DataManager, drilledSeries);
            }
            //This method exports the OlapChart to Excel, word and PDF.
        public void Export(System.IO.Stream stream)
            {
                System.IO.StreamReader sReader = new System.IO.StreamReader(stream);
                string args = System.Web.HttpContext.Current.Server.UrlDecode(sReader.ReadToEnd());
                OlapDataManager DataManager = new OlapDataManager(connectionString);
                string fileName = "Sample";
                htmlHelper.ExportOlapChart(DataManager, args, fileName, System.Web.HttpContext.Current.Response);
            }
            //This method carries information about the default report rendered within OlapChart initially. 
        private OlapReport CreateOlapReport()
        {
            OlapReport olapReport = new OlapReport();
            olapReport.Name = "Default Report";
            olapReport.CurrentCubeName = "Adventure Works";
            DimensionElement dimensionElementColumn = new DimensionElement();
            dimensionElementColumn.Name = "Customer";
            dimensionElementColumn.AddLevel("Customer Geography", "Country");
            MeasureElements measureElementColumn = new MeasureElements();
            measureElementColumn.Elements.Add(new MeasureElement
            {
                Name = "Customer Count"
            });
            DimensionElement dimensionElementRow = new DimensionElement();
            dimensionElementRow.Name = "Date";
            dimensionElementRow.AddLevel("Fiscal", "Fiscal Year");
            olapReport.SeriesElements.Add(dimensionElementRow);
            olapReport.CategoricalElements.Add(dimensionElementColumn);
            olapReport.CategoricalElements.Add(measureElementColumn);
            return olapReport;
        }
    }
}

{% endhighlight %}

**Configuring Web Configuration File**

You can expose services through the properties, binding, contract and address by using an endpoint.
* Contract: This property indicates that the contract of the endpoint is exposing. Here you are referring to IOlapChartService contract and hence it is `OlapChartDemo.IOlapChartService.`
* Binding: In your application, you use webHttpBinding to post and receive the requests and responses between the client-end and the service.
* behaviorConfiguration: This property contains the name of the behavior to be used in the endpoint.

The endpointBehaviors are illustrated as follows. 
 
{% highlight xml %}

<system.serviceModel> 
    <services>
        <service name="OlapChartDemo.OlapChartService">
            <endpoint address="" behaviorConfiguration="OlapChartDemo.OlapChartServiceAspNetAjaxBehavior" binding="webHttpBinding" contract="OlapChartDemo.IOlapChartService" /> </service>
    </services>
</system.serviceModel>

{% endhighlight %}

The endpointBehaviors contain all the behaviors for an endpoint. You can link each endpoint to the respective behavior only by using this name property.

{% highlight xml %}

<system.serviceModel>
    <behaviors>
        <endpointBehaviors>
            <behavior name="OlapChartDemo.OlapChartServiceAspNetAjaxBehavior">
                <enableWebScript /> </behavior>
        </endpointBehaviors>
    </behaviors> 
</system.serviceModel>
{% endhighlight %}


>** NOTE: In this example, “OlapChartDemo” indicates the name and root namespace of the Web Application created in Visual Studio IDE and “OlapChartService” indicates the name of the WCF service created.
Now, OlapChart is rendered with Customer Count over a period of fiscal years across different customer geographic locations.**

{% include image.html url="/js/OlapChart/Getting-Started_images/Getting-Started_img9.png"%}


