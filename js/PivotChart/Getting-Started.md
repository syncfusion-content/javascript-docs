---
layout: post
title: Getting-Started
description: getting started
platform: js
control: PivotChart
documentation: ug
---

# Getting Started

##Creating a simple application with PivotChart

This section covers the information required to create a simple PivotChart bound to OLAP datasource.

N> We will be illustrating this section by creating a simple Web Application through Visual Studio IDE since PivotChart is a server-side control with .NET dependency. The Web Application would contain a HTML page and a service that would transfer data to server-side, process and return back the data to client-side for control re-rendering. The service utilized for communication could be either WCF or WebAPI based on user requirement and we have illustrated both for user convenience. 

###Project Initialization
Create a new **ASP.NET Empty Web Application** by using Visual Studio IDE and name the project as **“PivotChartDemo”**.

Next, add a HTML page. To add a HTML page in your Web Application, right-click on the project in Solution Explorer and select **Add > New Item.** In the **Add New Item** window, select **HTML Page** and name it as **GettingStarted.html**, click **Add.**

Now, set “GettingStarted.html” as start-up page by right clicking on “GettingStarted.html” page and select **“Set As Start Page”.**

###Scripts and CSS Initialization
The scripts and style sheets that are mandatorily required to render a PivotChart widget inside a HTML page are highlighted in an appropriate order as follows,

1. ej.widgets.all.min.css
2. jQuery-1.10.2.min.js
3. jQuery.easing.1.3.min.js
4. jQuery.globalize.min.js
5. ej.web.all.min.js

You can find the scripts and style sheets listed above in any of the following locations:

Local Disk: [Click here](http://helpjs.syncfusion.com/js/installation-and-deployment) to know more about script and style sheets installed in local machine.

CDN Link: [Click here](http://helpjs.syncfusion.com/js/cdn) to know more about script and style sheets available online.

NuGet Package: [Click here](http://helpjs.syncfusion.com/js/installation-and-deployment#configuring-syncfusion-nuget-packages) to know more about script and style sheets available in NuGet package. 

###Control Initialization
In-order to initialize a PivotChart widget, first you need to define a “div” tag with an appropriate “id” attribute which acts as a container for PivotChart widget. Then you need to initialize the widget using ejPivotChart method.

{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">

<head>
    <title>PivotChart - Getting Started</title>
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" type="text/css" />
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js" type="text/javascript"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js" type="text/javascript"></script>
     <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js" type="text/javascript"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js" type="text/javascript"></script>
</head>

<body>
    <form id="form1" runat="server">
        <div>
            <!--Creating a div tag that acts as a container for ejPivotChart widget.-->
            <div id="PivotChart" style="height: 350px; width: 100%; overflow: auto"> </div>
            <script type="text/javascript">
                //Setting property and initializing ejPivotChart widget.
                $(function()
                {
                    $("#PivotChart").ejPivotChart(
                    {
                        url: "../PivotChartService",
                        size:
                        {
                            height: "350px",
                            width: "540px"
                        }
                    });
                });
            </script>
        </div>
    </form>
</body>

</html>

{% endhighlight %}

The “url” property in PivotChart widget points the service endpoint, where data are processed and fetched in the form of JSON. The service used for the PivotChart widget as endpoint are WCF and WebAPI.

N> The above "GettingStarted.html" contains WebAPI URL, which is **“../PivotChartService”**. Suppose if you are using WCF service, then the URL would look like **“../PivotChartService.svc”**.

###WebAPI

**Adding a WebAPI Controller**

To add a WebAPI controller in your existing Web Application, right-click on the project in Solution Explorer and select **Add > New Item.** In the **Add New Item** window, select **WebAPI Controller Class** and name it as **PivotChartServiceController.cs**. Finally, click **Add.**

Now, WebAPI controller is added into your application successfully with the following file. The utilization of this file will be explained in the following sections.
 
* PivotChartServiceController.cs

N> While adding WebAPI Controller Class, name it with the suffix “Controller” which is mandatory. For example, in the demo the controller is named as “PivotChartServiceController”.

Next, remove all the existing methods such as “Get”, “Post”, “Put” and “Delete” present inside `PivotChartServiceController.cs` file.

{% highlight c# %}

namespace PivotChartDemo
{
    public class PivotChartServiceController: ApiController
    {
    
    }
}
{% endhighlight %} 

**List of Dependency Libraries**

Add the following mentioned dependency libraries into your Web Application. You can find these libraries in GAC (Global Assembly Cache) in your machine.

To add them to your Web Application, right-click on **References** in Solution Explorer and select **Add Reference.** Now, in the **Reference Manager** dialog, under **Assemblies > Extension**, the following Syncfusion libraries are found. 

>**NOTE: If you have installed any version of SQL Server Analysis Service (SSAS) or Microsoft ADOMD.NET utility, then the location of Microsoft.AnalysisServices.AdomdClient library is [system drive:\Program Files (x86)\Microsoft.NET\ADOMD.NET]**

* Microsoft.AnalysisServices.AdomdClient.dll
* Syncfusion.Compression.Base.dll
* Syncfusion.Linq.Base.dll
* Syncfusion.Olap.Base.dll  
* Syncfusion.EJ.dll 
* Syncfusion.EJ.Olap.dll
* Syncfusion.Pdf.Base.dll
* Syncfusion.XlsIO.Base.dll
* Syncfusion.DocIO.Base.dll

**List of Namespaces**

The following are the list of namespaces to be added on top of the main class inside `PivotChartServiceController.cs` file.

{% highlight c# %}

using System.Web;
using System.Web.Script.Serialization;
using Syncfusion.Olap.Manager;
using Syncfusion.Olap.Reports;
using Syncfusion.JavaScript;
using Syncfusion.JavaScript.Olap;

namespace PivotChartDemo
{
    public class PivotChartServiceController : ApiController
    {

    }
}

{% endhighlight %}

**Datasource Initialization**

Now, the connection string to connect OLAP Cube, PivotChart and JavaScriptSerializer instances are created immediately inside the main class in `PivotChartServiceController.cs` file.

{% highlight c# %}

namespace PivotChartDemo
{
    public class PivotChartServiceController: ApiController
    {
        PivotChart htmlHelper = new PivotChart();
        string connectionString = "Data Source=http://bi.syncfusion.com/olap/msmdpump.dll; Initial Catalog=Adventure Works DW 2008 SE;";
        JavaScriptSerializer serializer = new JavaScriptSerializer();
        //Other codes
    }
}

{% endhighlight %}

**Service methods in WebAPI Controller**

Now you need to define the service methods inside PivotChartServiceController class, found inside `PivotChartServiceController.cs` file, created while adding WebAPI Controller Class to your Web Application.

{% highlight c# %}

namespace PivotChartDemo
{
    public class PivotChartServiceController: ApiController
    {
        PivotChart htmlHelper = new PivotChart();
        string connectionString = "Data Source=http://bi.syncfusion.com/olap/msmdpump.dll; Initial Catalog=Adventure Works DW 2008 SE;";
        JavaScriptSerializer serializer = new JavaScriptSerializer();
        [System.Web.Http.ActionName("InitializeChart")]
        [System.Web.Http.HttpPost]
       public Dictionary<string, object> InitializeChart(Dictionary<string, object> jsonResult)
        {
            OlapDataManager DataManager = null;
            DataManager = new OlapDataManager(connectionString);
            DataManager.SetCurrentReport(CreateOlapReport());
            return htmlHelper.GetJsonData(jsonResult["action"].ToString(), DataManager);
        }
            [System.Web.Http.ActionName("DrillChart")]
            [System.Web.Http.HttpPost]
           public Dictionary<string, object> DrillChart(Dictionary<string, object> jsonResult)
            {
                OlapDataManager DataManager = new OlapDataManager(connectionString);
                DataManager = new OlapDataManager(connectionString);
                DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["olapReport"].ToString()));
                return htmlHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["drilledSeries"].ToString());
     
            }
            [System.Web.Http.ActionName("Export")]
            [System.Web.Http.HttpPost]
        public void Export()
        {
            string args = HttpContext.Current.Request.Form.GetValues(0)[0];
            OlapDataManager DataManager = new OlapDataManager(connectionString);
            string fileName = "Sample";
            htmlHelper.ExportPivotChart(DataManager, args, fileName, System.Web.HttpContext.Current.Response);
        }
        private OlapReport CreateOlapReport()
        {
            OlapReport olapReport = new OlapReport();
            olapReport.Name = "Default Report";
            olapReport.CurrentCubeName = "Adventure Works";
            DimensionElement dimensionElementColumn = new DimensionElement();
            dimensionElementColumn.Name = "Customer";
            dimensionElementColumn.AddLevel("Customer Geography", "Country");
            MeasureElements measureElementColumn = new MeasureElements();
            measureElementColumn.Elements.Add(new MeasureElement{Name = "Customer Count"});
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

**Configure routing in Global Application Class**

To add a Global.asax in your existing Web Application, right-click on the project in Solution Explorer and select **Add > New Item.** In the **Add New Item** window, select **Global Application Class** and name it as “Global.asax”. Finally, click **Add.**
Once you finish adding the **Global.asax** file, immediately add the namespace **“using System.Web.Http;”** and then you can configure routing like in the following code example.

{% highlight c# %}

public class Global: System.Web.HttpApplication
{
    protected void Application_Start(object sender, EventArgs e)
    {
        GlobalConfiguration.Configuration.Routes.MapHttpRoute(name: "DefaultApi", routeTemplate: "{controller}/{action}/{id}", defaults: new
        {
            id = RouteParameter.Optional
        });
        AppDomain.CurrentDomain.SetData("SQLServerCompactEditionUnderWebHosting", true);
    }
}

{% endhighlight %}

Now, PivotChart is rendered with Customer Count over a period of fiscal years across different customer geographic locations.

{% include image.html url="/js/PivotChart/Getting-Started_images/Getting-Started_img9.png"%}

###WCF
This section demonstrates the utilization of WCF service as endpoint binding OLAP datasource to a simple PivotChart. For more details on this topic, [click here](http://help.syncfusion.com/js/PivotChart/data-binding#wcf).


