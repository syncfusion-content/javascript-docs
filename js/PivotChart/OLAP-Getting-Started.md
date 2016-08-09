---
layout: post
title: OLAP-Getting-Started
description: olap-getting started
platform: js
control: PivotChart
documentation: ug
---

# Getting Started

## Creating a simple application with PivotChart and OLAP datasource (Client Mode)

This section covers the information required to populate a simple PivotChart with OLAP data completely on the client-side.  

### Scripts and CSS References

Create a HTML page and add scripts and style sheets that are mandatorily required to render a PivotChart widget which are highlighted below in an appropriate order.

1. ej.web.all.min.css
2. jQuery-1.10.2.min.js
3. jQuery.easing.1.3.min.js
4. ej.web.all.min.js

### Initialize PivotChart

Place a "div" tag in the HTML page which acts as a container for the PivotChart widget. Then initialize the widget using the "ejPivotChart" method.

{% highlight html %}

    <!DOCTYPE html>
    <html>
        <head>
            <title>PivotChart - Getting Started</title>
            <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" type="text/css" />
            <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js" type="text/javascript"></script>
            <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js" type="text/javascript"></script>
            <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js" type="text/javascript"></script>
        </head>
        <body>
            <!--Create a tag which acts as a container for ejPivotChart widget.-->
            <div id="PivotChart1" style="width: 800px; height: 350px"></div>
            <script type="text/javascript">
                $(function () {
                    //Set properties and initialize ejPivotChart widget.
                    $("#PivotChart1").ejPivotChart();
                });
            </script>
        </body>
    </html>
{% endhighlight %}

### Populate PivotChart with DataSource

Initialize the OLAP datasource for PivotChart widget as shown below.

{% highlight html %}

    <html>

        //....

        <body>
            <div id="PivotChart1" style="width: 800px; height: 350px"></div>
            <script type="text/javascript">
                $(function() {
                    $("#PivotChart1").ejPivotChart({
                        dataSource: {
                            data: "http://bi.syncfusion.com/olap/msmdpump.dll",
                            catalog: "Adventure Works DW 2008 SE",
                            cube: "Adventure Works",
                            rows: [{
                                fieldName: "[Date].[Fiscal]"
                            }],
                            columns: [{
                                fieldName: "[Customer].[Customer Geography]"
                            }],
                            values: [{
                                measures: [{
                                    fieldName: "[Measures].[Internet Sales Amount]",
                                }],
                                axis: "columns"
                            }]
                        },
                        size: {
                            height: "350px",
                            width: "800px"
                        }
                    });
                });
            </script>
        </body>
    </html>
{% endhighlight %}

The above code will generate a simple PivotChart showing Internet Sales Amount over a period of fiscal years across different customer geographic locations.

![](Olap-Getting-Started_images/OlapClientMode.png) 

## Creating a simple application with PivotChart and OLAP datasource (Server Mode)

This section covers the information required to create a simple PivotChart bound to OLAP datasource.  

N> We will be illustrating this section by creating a simple Web Application through Visual Studio IDE since PivotChart in ServerMode requires .NET dependency. The Web Application would contain a HTML page and a service that would transfer data to server-side, process and return back the data to client-side for control rendering. The service utilized for communication could be either WCF or WebAPI based on user requirement and we have illustrated both for user convenience.

### Project Initialization
Create a new **ASP.NET Empty Web Application** by using Visual Studio IDE and name the project as **“PivotChartDemo”**.

Next you need to add a HTML page. To add a HTML page in your Web Application, right-click on the project in Solution Explorer and select **Add > New Item.** In the **Add New Item** window, select **HTML Page** and name it as **“GettingStarted.html”**, click **Add.**

Now you need to set “GettingStarted.html” as start-up page. In-order to do so, right-click on “GettingStarted.html” page and select **“Set As Start Page”**.

### Scripts and CSS Initialization
The scripts and style sheets that are mandatorily required to render a PivotChart widget inside a HTML page are highlighted below in an appropriate order.

1. ej.widgets.all.min.css
2. jQuery-1.10.2.min.js
3. jQuery.easing.1.3.min.js
4. ej.web.all.min.js

The scripts and style sheets listed above could be found in any of the following locations:

Local Disk: [Click here](http://helpjs.syncfusion.com/js/installation-and-deployment) to know more about script and style sheets installed in local machine.

CDN Link: [Click here](http://helpjs.syncfusion.com/js/cdn) to know more about script and style sheets available online.

NuGet Package: [Click here](http://helpjs.syncfusion.com/js/installation-and-deployment#configuring-syncfusion-nuget-packages) to know more about script and style sheets available in NuGet package. 

### Control Initialization
In-order to initialize a PivotChart widget, first you need to define a “div” tag with an appropriate “id” attribute which acts as a container for PivotChart widget. Then you need to initialize the widget using `ejPivotChart` method.
    
{% highlight html %}

    <!DOCTYPE html>
    <html xmlns="http://www.w3.org/1999/xhtml">
        <head>
            <title>PivotChart - Getting Started</title>
            <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" type="text/css" />
            <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js" type="text/javascript"></script>
            <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js" type="text/javascript"></script>
            <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js" type="text/javascript"></script>
        </head>

        <body>
            <!--Create a tag which acts as a container for ejPivotChart widget.-->
            <div id="PivotChart1" style="width: 800px; height: 350px"> </div>
            <script type="text/javascript">
                //Set properties and initialize ejPivotChart widget.
                $(function() {
                    $("#PivotChart1").ejPivotChart({
                        url: "/OlapChart",
                        size: {
                            height: "350px",
                            width: "800px"
                        }
                    });
                });
            </script>
        </body>
    </html>

{% endhighlight %}

The “url” property in PivotChart widget points the service endpoint, where data are processed and fetched in the form of JSON. The services used for the PivotChart widget as endpoint are WCF and WebAPI.

N> The above "GettingStarted.html" contains WebAPI URL, which is **“/OlapChart”**. Suppose if you are using WCF service then the URL would look like **"/OlapChartService.svc"**. 

Register the referenced assemblies in Web.config file available at the root of the application.

{% highlight xml %}

<compilation debug="true" targetFramework="4.5.1">
    <assemblies> 
        …… 
        ……
        <add assembly="Syncfusion.EJ, Version= {{ site.45esreleaseversion }}, Culture=neutral, PublicKeyToken=3d67ed1f87d44c89" />
        <add assembly="Syncfusion.EJ.Olap, Version= {{ site.45esreleaseversion }}, Culture=neutral, PublicKeyToken=3d67ed1f87d44c89" />
        <add assembly="Syncfusion.Linq.Base, Version= {{ site.45esreleaseversion }}, Culture=neutral, PublicKeyToken=3d67ed1f87d44c89" />
        <add assembly="Syncfusion.Olap.Base, Version= {{ site.45esreleaseversion }}, Culture=neutral, PublicKeyToken=3d67ed1f87d44c89" />
        <add assembly="Syncfusion.Compression.Base, Version= {{ site.45esreleaseversion }}, Culture=neutral, PublicKeyToken=3d67ed1f87d44c89" /> 
        <add assembly="Syncfusion.PivotAnalysis.Base, Version= {{ site.45esreleaseversion }}, Culture=neutral, PublicKeyToken=3d67ed1f87d44c89" /> 
        <add assembly="Syncfusion.Pdf.Base, Version= {{ site.45esreleaseversion }}, Culture=neutral, PublicKeyToken=3d67ed1f87d44c89" />
        <add assembly="Syncfusion.XlsIO.Base, Version= {{ site.45esreleaseversion }}, Culture=neutral, PublicKeyToken=3d67ed1f87d44c89" />
        <add assembly="Syncfusion.DocIO.Base, Version= {{ site.45esreleaseversion }}, Culture=neutral, PublicKeyToken=3d67ed1f87d44c89" /> 
    </assemblies>
</compilation>

{% endhighlight %}

### WebAPI

**Adding a WebAPI Controller**

To add a WebAPI controller in your existing Web Application, right-click on the project in Solution Explorer and select **Add > New Item.** In the **Add New Item** window, select **WebAPI Controller Class** and name it as “OlapChartController.cs”, click **Add.**

Now WebAPI controller is added into your application successfully which in-turn comprise of the following file. The utilization of this file will be explained in the following sections.
 
* OlapChartController.cs

N> While adding WebAPI Controller Class, name it with the suffix “Controller” that is mandatory. For example, in demo the controller is named as “OlapChartController”.

Next, remove all the existing methods such as “Get”, “Post”, “Put” and “Delete” present inside `OlapChartController.cs` file. 

{% highlight c# %}

    namespace PivotChartDemo
    {
        public class OlapChartController : ApiController
        {
        
        }
    }

{% endhighlight %}

**List of Dependency Libraries**

Next you need to add the below mentioned dependency libraries into your Web Application. These libraries could be found in GAC (Global Assembly Cache) as well.

To add them to your Web Application, right-click on **References** in Solution Explorer and select **Add Reference.** Now, in the **Reference Manager** dialog, under **Assemblies > Extension**, the following Syncfusion libraries are found. 

N> When you have installed any version of SQL Server Analysis Service (SSAS) or Microsoft ADOMD.NET utility, then the location of Microsoft.AnalysisServices.AdomdClient library is [system drive:\Program Files (x86)\Microsoft.NET\ADOMD.NET]

* Microsoft.AnalysisServices.AdomdClient
* Syncfusion.Compression.Base
* Syncfusion.Linq.Base
* Syncfusion.Olap.Base
* Syncfusion.PivotAnalysis.Base
* Syncfusion.XlsIO.Base
* Syncfusion.Pdf.Base
* Syncfusion.DocIO.Base
* Syncfusion.EJ
* Syncfusion.EJ.Olap

**List of Namespaces**

Following are the list of namespaces to be added on top of the main class inside `OlapChartController.cs` file.

{% highlight c# %}

    using Syncfusion.Olap.Manager;
    using Syncfusion.Olap.Reports;
    using Syncfusion.JavaScript;

    namespace PivotChartDemo
    {
        public class OlapChartController : ApiController
        {

        }
    }

{% endhighlight %}

**Datasource Initialization**

Now, the connection string to connect OLAP Cube and PivotChart instances are created immediately inside the main class in `OlapChartController.cs` file.

{% highlight c# %}

    namespace PivotChartDemo
    {
        public class OlapChartController : ApiController
        {
            string connectionString = "Data Source=http://bi.syncfusion.com/olap/msmdpump.dll; Initial Catalog=Adventure Works DW 2008 SE;";
            PivotChart pivotChart = new PivotChart();
            //Other codes
        }
    }

{% endhighlight %}

**Service methods in WebAPI Controller**

Now you need to define the service methods inside OlapChartController class, found inside `OlapChartController.cs` file, created while adding WebAPI Controller Class to your Web Application.
 
{% highlight c# %}

    namespace PivotChartDemo
    {
        public class OlapChartController : ApiController
        {
            string connectionString = "Data Source=http://bi.syncfusion.com/olap/msmdpump.dll; Initial Catalog=Adventure Works DW 2008 SE;";
            PivotChart pivotChart = new PivotChart();
            
            [System.Web.Http.ActionName("InitializeChart")]
            [System.Web.Http.HttpPost]
            public Dictionary<string, object> InitializeChart(Dictionary<string, object> jsonResult)
            {
                OlapDataManager DataManager = new OlapDataManager(connectionString);
                DataManager.SetCurrentReport(CreateOlapReport());
                return pivotChart.GetJsonData(jsonResult["action"].ToString(), DataManager);
            }

            [System.Web.Http.ActionName("DrillChart")]
            [System.Web.Http.HttpPost]
            public Dictionary<string, object> DrillChart(Dictionary<string, object> jsonResult)
            {
                OlapDataManager DataManager = new OlapDataManager(connectionString);
                DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["olapReport"].ToString()));
                return pivotChart.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["drilledSeries"].ToString());
            }

            private OlapReport CreateOlapReport()
            {
                OlapReport olapReport = new OlapReport();
                olapReport.Name = "Default Report";
                olapReport.CurrentCubeName = "Adventure Works";

                DimensionElement dimensionElementColumn = new DimensionElement();
                //Specifying the Name for the Dimension Element
                dimensionElementColumn.Name = "Customer";
                dimensionElementColumn.AddLevel("Customer Geography", "Country");

                MeasureElements measureElementColumn = new MeasureElements();
                //Specifying the Name for the Measure Element
                measureElementColumn.Elements.Add(new MeasureElement { Name = "Customer Count" });

                DimensionElement dimensionElementRow = new DimensionElement();
                //Specifying the Dimension Name
                dimensionElementRow.Name = "Date";
                dimensionElementRow.AddLevel("Fiscal", "Fiscal Year");

                ///Adding Row Members
                olapReport.SeriesElements.Add(dimensionElementRow);
                ///Adding Column Members
                olapReport.CategoricalElements.Add(dimensionElementColumn);
                ///Adding Measure Element
                olapReport.CategoricalElements.Add(measureElementColumn);
                return olapReport;
            }
        }
    }

{% endhighlight %}

**Configure routing in Global Application Class**

To add a Global.asax in your existing Web Application, right-click on the project in Solution Explorer and select **Add > New Item.** In the **Add New Item** window, select **Global Application Class** and name it as “Global.asax”, click **Add.**

Once you finish adding the **Global.asax** file, immediately add the namespace **“using System.Web.Http;”** and then you can configure routing like in the following code example.

{% highlight c# %}

    public class Global : System.Web.HttpApplication
    {
        protected void Application_Start(object sender, EventArgs e)
        {
            GlobalConfiguration.Configuration.Routes.MapHttpRoute(
                name: "DefaultApi",
                routeTemplate: "{controller}/{action}/{id}",
                defaults: new { id = RouteParameter.Optional });
            AppDomain.CurrentDomain.SetData("SQLServerCompactEditionUnderWebHosting", true);
        }
    }

{% endhighlight %}

Now, PivotChart will be rendered with Customer Count over a period of fiscal years across different customer geographic locations.

![](Olap-Getting-Started_images/ServerMode.png)

### WCF
This section demonstrates the utilization of WCF service as endpoint binding OLAP datasource to a simple PivotChart. For more details on this topic, [click here](http://help.syncfusion.com/js/pivotchart/olap-connectivity#wcf).





