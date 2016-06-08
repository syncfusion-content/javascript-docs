---
layout: post
title: Getting-Started
description: getting started 
platform: js
control: PivotGauge
documentation: ug
---

# Getting Started 

##Creating a simple application with PivotGauge

This section covers the information required to create a simple PivotGauge bound to OLAP datasource.

N> We will be illustrating this section by creating a simple Web Application through Visual Studio IDE since PivotGauge is a server-side control with .NET dependency. The Web Application would contain a HTML page and a service that would transfer data to server-side, process and return back the data to client-side for control re-rendering. The service utilized for communication could be either WCF or WebAPI based on user requirement and we have illustrated both for user convenience.

###Project Initialization
Create a new **ASP.NET Empty Web Application** by using Visual Studio IDE and name the project as **“PivotGaugeDemo”**.

Next add a HTML page. To add a HTML page in your Web Application, right-click on the project in Solution Explorer and select **Add > New Item.** In the **Add New Item** window, select **HTML Page** and name it as “GettingStarted.html”, click **Add.**

Now, set “GettingStarted.html” as start-up page by right-clicking on “GettingStarted.html” page and select **“Set As Start Page”.**

###Scripts and CSS Initialization
The scripts and style sheets that are mandatorily required to render a PivotGauge widget inside a HTML page are highlighted in an appropriate order as follows,

1. ej.widgets.all.min.css
2. jQuery-1.10.2.min.js
3. jQuery.easing.1.3.min.js
4. ej.web.all.min.js

You can find the scripts and style sheets listed above in any of the following locations:

Local Disk: [Click here](http://helpjs.syncfusion.com/js/installation-and-deployment) to know more about script and style sheets installed in local machine.

CDN Link: [Click here](http://helpjs.syncfusion.com/js/cdn) to know more about script and style sheets available online.

NuGet Package: [Click here](http://helpjs.syncfusion.com/js/installation-and-deployment#configuring-syncfusion-nuget-packages) to know more about script and style sheets available in NuGet package. 

###Control Initialization
In-order to initialize a PivotGauge widget, first you need to define a “div” tag with an appropriate “id” attribute which acts as a container for PivotGauge widget. Then you need to initialize the widget using ejPivotGauge method.
    
{% highlight html %}
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">

<head>
    <title>PivotGauge - Getting Started</title>
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" type="text/css" />
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js" type="text/javascript"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js" type="text/javascript"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js" type="text/javascript"></script>
</head>

<body>
    <form id="form1" runat="server">
        <div>
            <!--Creating a div tag, that acts as a container for ejPivotGauge widget.-->
            <div id="PivotGauge" style="height: 350px; width: 100%; position:relative"> </div> //Setting properties and initializing ejPivotGauge widget.
            <script type="text/javascript">
                $(function()
                {
                    $("#PivotGauge").ejPivotGauge(
                    {
                        url: "../PivotGauge",
                        enableTooltip: true,
                        load: "loadGaugeTheme",
                        backgroundColor: "transparent",
                        scales: [
                        {
                            showRanges: true,
                            radius: 150,
                            showScaleBar: true,
                            size: 1,
                            border:
                            {
                                width: 0.5
                            },
                            showIndicators: true,
                            showLabels: true,
                            pointers: [
                            {
                                showBackNeedle: true,
                                backNeedleLength: 20,
                                length: 120,
                                width: 7
                            },
                            {
                                type: "marker",
                                markerType: "diamond",
                                distanceFromScale: 5,
                                placement: "center",
                                backgroundColor: "#29A4D9",
                                length: 25,
                                width: 15
                            }],
                            ticks: [
                            {
                                type: "major",
                                distanceFromScale: 2,
                                height: 16,
                                width: 1,
                                color: "#8c8c8c"
                            },
                            {
                                type: "minor",
                                height: 6,
                                width: 1,
                                distanceFromScale: 2,
                                color: "#8c8c8c"
                            }],
                            labels: [
                            {
                                color: "#8c8c8c"
                            }],
                            ranges: [
                            {
                                distanceFromScale: -5,
                                backgroundColor: "#fc0606",
                                border:
                                {
                                    color: "#fc0606"
                                }
                            },
                            {
                                distanceFromScale: -5
                            }],
                            customLabels: [
                            {
                                position:
                                {
                                    x: 180,
                                    y: 290
                                },
                                font:
                                {
                                    size: "10px",
                                    fontFamily: "Segoe UI",
                                    fontStyle: "Normal"
                                },
                                color: "#666666"
                            },
                            {
                                position:
                                {
                                    x: 180,
                                    y: 320
                                },
                                font:
                                {
                                    size: "10px",
                                    fontFamily: "Segoe UI",
                                    fontStyle: "Normal"
                                },
                                color: "#666666"
                            },
                            {
                                position:
                                {
                                    x: 180,
                                    y: 150
                                },
                                font:
                                {
                                    size: "12px",
                                    fontFamily: "Segoe UI",
                                    fontStyle: "Normal"
                                },
                                color: "#666666"
                            }]
                        }]
                    });
                });
            </script>
    </form>
</body>
</html>

{% endhighlight %}

The “url” property in PivotGauge widget points the service endpoint, where data are processed and fetched in the form of JSON. The service used for the PivotGauge widget as endpoint are WCF and WebAPI.

N> The above "GettingStarted.html" contains WebAPI URL, which is “../PivotGaugeService”. Suppose if you are using WCF service, then the URL would look like "../PivotGaugeService.svc". 

###WebAPI

**Adding a WebAPI Controller**

To add a WebAPI controller in your existing Web Application, right-click on the project in Solution Explorer and select **Add > New Item.** In the **Add New Item** window, select **WebAPI Controller Class** and name it as “PivotGaugeController.cs”, click **Add.**

Now, WebAPI controller is added into your application successfully with the following file. The utilization of this file will be explained in the following sections.
 
* PivotGaugeController.cs

N> While adding WebAPI Controller Class, name it with the suffix “Controller” which is mandatory. For example, in demo the controller is named as “PivotGaugeController”.

Next, remove all the existing methods such as “Get”, “Post”, “Put” and “Delete” present inside `PivotGaugeController.cs` file.

{% highlight c# %}

namespace PivotGaugeDemo
{
    public class PivotGaugeController: ApiController
    {
    
    }
}
{% endhighlight %}

**List of Dependency Libraries**

Add the following dependency libraries into your Web Application. You can find these libraries in GAC (Global Assembly Cache) in your machine.

To add them to your Web Application, right-click on **References** in Solution Explorer and select **Add Reference.** Now in the **Reference Manager** dialog, under **Assemblies > Extension**, the following Syncfusion libraries are found. 

>**NOTE: When you have installed any version of SQL Server Analysis Service (SSAS) or Microsoft ADOMD.NET utility, then the location of Microsoft.AnalysisServices.AdomdClient library is [system drive:\Program Files (x86)\Microsoft.NET\ADOMD.NET]**

* Microsoft.AnalysisServices.AdomdClient.dll
* Syncfusion.Linq.Base.dll 
* Syncfusion.Olap.Base.dll 
* Syncfusion.EJ.dll  
* Syncfusion.EJ.Olap.dll

**List of Namespaces**

Following are the list of namespaces to be added on top of the main class inside `PivotGaugeController.cs` file. 

{% highlight c# %}

using System.Web.Script.Serialization;
using Syncfusion.Olap.Manager;
using Syncfusion.Olap.Reports;
using Syncfusion.JavaScript;
using Syncfusion.JavaScript.Olap;

namespace PivotGaugeDemo
{
    public class PivotGaugeController: ApiController
    {
    
    }
}
{% endhighlight %}

**Datasource Initialization**

Now, the connection string to connect OLAP Cube, PivotGauge and JavaScriptSerializer instances are created immediately inside the main class in `PivotGaugeController.cs` file.

{% highlight c# %}

namespace PivotGaugeDemo
{
    public class PivotGaugeController: ApiController
    {
        PivotGauge htmlHelper = new PivotGauge();
        string connectionString = "Data Source=http://bi.syncfusion.com/olap/msmdpump.dll; Initial Catalog=Adventure Works DW 2008 SE;";
        JavaScriptSerializer serializer = new JavaScriptSerializer();
        //Other codes
    }
}

{% endhighlight %}

**Service methods in WebAPI Controller**

Now you need to define the service methods inside PivotGaugeController class, found inside `PivotGaugeController.cs` file, created while adding WebAPI Controller Class to your Web Application.

{% highlight c# %}

namespace PivotGaugeDemo
{
    public class PivotGaugeController: ApiController
    {
        PivotGauge htmlHelper = new PivotGauge();
        string connectionString = "Data Source=http://bi.syncfusion.com/olap/msmdpump.dll; Initial Catalog=Adventure Works DW 2008 SE;";
        JavaScriptSerializer serializer = new JavaScriptSerializer();
        [System.Web.Http.ActionName("InitializeGauge")]
        [System.Web.Http.HttpPost]
        public Dictionary < string, object > InitializeGauge(Dictionary < string, object > jsonResult)
        {
            OlapDataManager DataManager = new OlapDataManager(connectionString);
            DataManager.SetCurrentReport(CreateOlapReport());
            return htmlHelper.GetJsonData(jsonResult["action"].ToString(), DataManager);
        }
        private OlapReport CreateOlapReport()
        {
            OlapReport report = new OlapReport();
            report.CurrentCubeName = "Adventure Works";
            KpiElements kpiElement = new KpiElements();
            kpiElement.Elements.Add(new KpiElement
            {
                Name = "Internet Revenue", ShowKPIGoal = true, ShowKPIStatus = true, ShowKPIValue = true, ShowKPITrend = true
            });
            DimensionElement dimensionElementColumn = new DimensionElement();
            dimensionElementColumn.Name = "Customer";
            dimensionElementColumn.AddLevel("Customer Geography", "Country");
            MeasureElements measureElementColumn = new MeasureElements();
            measureElementColumn.Elements.Add(new MeasureElement
            {
                Name = "Internet Sales Amount"
            });
            DimensionElement dimensionElementRow = new DimensionElement();
            dimensionElementRow.Name = "Date";
            dimensionElementRow.AddLevel("Fiscal", "Fiscal Year");
            dimensionElementRow.Hierarchy.LevelElements["Fiscal Year"].Add("FY 2004");
            dimensionElementRow.Hierarchy.LevelElements["Fiscal Year"].IncludeAvailableMembers = true;
            report.CategoricalElements.Add(dimensionElementColumn);
            report.CategoricalElements.Add(kpiElement);
            report.CategoricalElements.Add(measureElementColumn);
            report.SeriesElements.Add(dimensionElementRow);
            return report;
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

Now, PivotGauge is rendered with Internet Revenue for Internet Sales Amount over a Fiscal Year 2004 across different customer geographic locations.

{% include image.html url="/js/PivotGauge/Getting-Started_images/OlapGauge.png" %}

###WCF
This section demonstrates the utilization of WCF service as endpoint binding OLAP datasource to a simple PivotGauge. For more details on this topic, [click here](http://help.syncfusion.com/js/olapgauge/data-binding#wcf).
  