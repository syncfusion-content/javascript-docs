---
layout: post
title: OLAP-Getting-Started
description: olap-getting started
platform: js
control: PivotGauge
documentation: ug
api: /api/js/ejpivotgauge
---

# Getting started

## Creating a simple application with pivot gauge and OLAP data sources (client mode)

This section covers the information required to populate a simple pivot gauge with the [`OLAP`](/api/js/ejpivotgauge#members:analysisMode) data completely on the [`client-side`](/api/js/ejpivotgauge#members:operationalmode).

### Scripts and CSS references

Create an HTML page and add scripts and style sheets that are required to render a pivot gauge widget which are highlighted below in an appropriate order:

1. ej.web.all.min.css
2. jQuery-3.0.0.min.js
3. ej.web.all.min.js

### Initialize pivot gauge

Place a "div" tag in the HTML page which acts as a container for the pivot gauge widget. Then, initialize the widget by using the "ejPivotGauge" method.

{% highlight html %}

<!DOCTYPE html>
<html>
    <head>
        <title>PivotGauge - Getting Started</title>
        <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" type="text/css" />
        <script src="http://cdn.syncfusion.com/js/assets/external/jquery-3.0.0.min.js" type="text/javascript"></script>
        <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js" type="text/javascript"></script>
    </head>
    <body>
        <!--Create a tag which acts as a container for ejPivotGauge widget.-->
        <div id="PivotGauge1"></div>
        <script type="text/javascript">
            $(function () {
                //Set properties and initialize ejPivotGauge widget.
                $("#PivotGauge1").ejPivotGauge();
            });
        </script>
    </body>
</html>
{% endhighlight %}

### Populate pivot gauge with data source

Initialize the [`OLAP`](/api/js/ejpivotgauge#members:analysisMode) data source for the pivot gauge widget by using the **dataSource** property.

{% highlight html %}

<html>

    //....
    <body>
        <div id="PivotGauge1"></div>
        <script type="text/javascript">
            $(function() {
                $("#PivotGauge1").ejPivotGauge({
                    dataSource: {
                        data: "http://bi.syncfusion.com/olap/msmdpump.dll",
                        catalog: "Adventure Works DW 2008 SE",
                        cube: "Adventure Works",
                        rows: [
                            {
                                fieldName: "[Date].[Fiscal]"
                            },
                        ],
                        columns: [
                            {
                                fieldName: "[Customer].[Customer Geography]"
                            }
                        ],
                        values: [
                            {
                                measures: [
                                    {
                                        fieldName: "[Measures].[Internet Sales Amount]"
                                    },
                                    {
                                        fieldName: "[Measures].[Internet Revenue Status]"
                                    },
                                    {
                                        fieldName: "[Measures].[Internet Revenue Trend]"
                                    },
                                    {
                                        fieldName: "[Measures].[Internet Revenue Goal]"
                                    },
                                ],
                                axis: ej.PivotGauge.AxisName.Columns
                            }
                        ]
                    },
                    scales: [
                        {
                            showRanges: true,
                            radius: 150, showScaleBar: true, size: 1,
                            border: {
                                width: 0.5
                            },
                            showIndicators: true, showLabels: true,
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
                                }
                            ],
                            ticks: [
                                {
                                    type: "major",
                                    distanceFromScale: 2,
                                    height: 16,
                                    width: 1, color: "#8c8c8c"
                                },
                                {
                                    type: "minor",
                                    height: 6,
                                    width: 1,
                                    distanceFromScale: 2,
                                    color: "#8c8c8c"
                                }
                            ],
                            labels: [
                                {
                                    color: "#8c8c8c"
                                }
                            ],
                            ranges: [
                                {
                                    distanceFromScale: -5,
                                    backgroundColor: "#fc0606",
                                    border: { color: "#fc0606" }
                                },
                                {
                                    distanceFromScale: -5
                                }
                            ],
                            customLabels: [
                                {
                                    position: { x: 180, y: 290 },
                                    font: { size: "10px", fontFamily: "Segoe UI", fontStyle: "Normal" }, color: "#666666"
                                }, 
                                {
                                    position: { x: 180, y: 320 },
                                    font: { size: "10px", fontFamily: "Segoe UI", fontStyle: "Normal" }, color: "#666666"
                                }, 
                                {
                                    position: { x: 180, y: 150 },
                                    font: { size: "12px", fontFamily: "Segoe UI", fontStyle: "Normal" }, color: "#666666"
                                }
                            ]
                        }
                    ]
                });
            });
        </script>
    </body>
</html>
{% endhighlight %}

The above code will generate a series of gauges for all countries as shown below:

![](OLAP-Getting-Started_images/ClientMode.png)

The following table will explain the [`OLAP`](/api/js/ejpivotgauge#members:analysisMode) [`datasource`](/api/js/ejpivotgauge#members:datasource) properties at [`client-side`](/api/js/ejpivotgauge#members:operationalmode) in detail:

<table>
    <tr>
        <th>
            Properties
        </th>
        <th>
            Description
        </th>
    </tr>
    <tr>
    <td>
        {{'[`cube`](https://help.syncfusion.com/api/js/ejpivotgauge#members:datasource-cube "cube")'| markdownify }}
    </td>
    <td>
        Contains the respective cube name as string type in the OLAP database.
    </td>
    </tr>
    <tr>
    <td>
        {{'[`sourceInfo`](https://help.syncfusion.com/api/js/ejpivotgauge#members:datasource-sourceinfo "sourceInfo")'| markdownify }}
    </td>
    <td>
        To set the data source name to fetch the data.
    </td>
    </tr>
    <tr>
    <td>
        {{'[`providerName`](https://help.syncfusion.com/api/js/ejpivotgauge#members:datasource-providername "providerName")'| markdownify }}
    </td>
    <td>
        Set the provider name for pivot gauge to identify whether the provider is SSAS or Mondrian.
    </td>
    </tr>
    <tr>
    <td>
        {{'[`data`](https://help.syncfusion.com/api/js/ejpivotgauge#members:datasource-data "data")'| markdownify }}
    </td>
    <td>
        Provides the raw data source for the pivot gauge.
    </td>
    </tr>
    <tr>
    <td>
        {{'[`catalog`](https://help.syncfusion.com/api/js/ejpivotgauge#members:datasource-catalog "catalog")'| markdownify }}
    </td>
    <td>
        In connection with an OLAP database, this property contains the database name as string to fetch the data from the given connection string.
    </td>
    </tr>
    <tr>
        <td>
            {{'[`columns`](https://help.syncfusion.com/api/js/ejpivotgauge#members:datasource-columns "columns")'| markdownify }}
        </td>
        <td>
            Lists out the items to bind in columns section.
             <table class="params">
            <thead>
            <tr>
            <th>Properties</th>
            <th>Description</th>
            </tr>
            </thead>
            <tbody>
            <tr>
            <td>{{'[`fieldName`](https://help.syncfusion.com/api/js/ejpivotgauge#members:datasource-columns-fieldname "fieldName")'| markdownify }} </td>
            <td>Allows the user to bind the item by using its unique name as field name.</td>
            </tr>
            </tbody>
            </table>
        </td>
    </tr>
    <tr>
        <td>
            {{'[`rows`](https://help.syncfusion.com/api/js/ejpivotgauge#members:datasource-rows "rows")'| markdownify }}
        </td>
        <td>
            Lists out the items to bind in rows section.
             <table class="params">
            <thead>
            <tr>
            <th>Properties</th>
            <th>Description</th>
            </tr>
            </thead>
            <tbody>
            <tr>
            <td>{{'[`fieldName`](https://help.syncfusion.com/api/js/ejpivotgauge#members:datasource-rows-fieldname "fieldName")'| markdownify }} </td>
            <td>Allows the user to bind the item by using its unique name as field name.</td>
            </tr>
            </tbody>
            </table>
        </td>
    </tr>
    <tr>
        <td>
            {{'[`values`](https://help.syncfusion.com/api/js/ejpivotgauge#members:datasource-values "values")'| markdownify }}
        </td>
        <td>
            Lists out the items supports calculation in pivot gauge.
            <table class="params">
            <thead>
            <tr>
            <th>Properties</th>
            <th>Description</th>
            </tr>
            </thead>
            <tbody>
            <tr>
            <td>{{'[`axis`](https://help.syncfusion.com/api/js/ejpivotgauge#members:datasource-values-axis "axis")'| markdownify }} </td>
            <td>Allows to set the axis name to place the measures items.</td>
            </tr>
            <tr>
            <td>{{'[`measures`](https://help.syncfusion.com/api/js/ejpivotgauge#members:datasource-values-measures "measures")'| markdownify }}</td>
            <td>This holds the list of unique names of measures to bind them from the OLAP cube.
            <table class="params">
            <thead>
            <tr>
            <th>Property</th>
            <th>Description</th>
            </tr>
            </thead>
            <tbody>
            <tr>
            <td>
                {{'[`fieldName`](https://help.syncfusion.com/api/js/ejpivotgauge#members:datasource-values-measures-fieldName "fieldName")'| markdownify }} </td>
            <td>Allows the user to bind the measure from OLAP datasource by using its unique name as field name.</td>
            </tr>
            </td>
            </tr>
            </tbody>
            </table>
            </td>
            </tr>
            </tbody>
            </table>
        </td>
        </tr>

</table>

## Creating a simple application with pivot gauge and OLAP data source (server mode)

This section covers the information required to create a simple pivot gauge that is bound to the [`OLAP`](/api/js/ejpivotgauge#members:analysisMode) data source from the [`server-side`](/api/js/ejpivotgauge#members:operationalmode).

N> This section is illustrated by creating a simple web application through the Visual Studio IDE since the pivot gauge in the server mode requires .NET dependency. The web application contain an HTML page and a service that will transfer the data to the [`server-side`](/api/js/ejpivotgauge#members:operationalmode), process it, and return it to the [`client-side`](/api/js/ejpivotgauge#members:operationalmode) for control rendering. The service utilized for communication can be WCF or WebAPI based on user requirement. Here, both are illustrated for user convenience.

### Project initialization
Create a new **ASP.NET Empty Web Application** by using the Visual Studio IDE and name the project **“PivotGaugeDemo”**.

Next, you should add an HTML page. To add an HTML page in your web application, right-click the project in the solution explorer and select **Add > New Item.** In the **Add New Item** window, select **HTML Page** and name it **“GettingStarted.html”** page, and then click **Add.**

Now, you can set “GettingStarted.html” as start-up page. To do so, right-click the “GettingStarted.html” page and select **“Set As Start Page”**.

### Scripts and CSS initialization
The scripts and style sheets that are required to render a pivot gauge widget in an HTML page are highlighted below in an appropriate order:

1. ej.web.all.min.css
2. jQuery-3.0.0.min.js
3. ej.web.all.min.js

The scripts and style sheets listed above can be found in any of the following locations:

Local disk: [Click here](https://help.syncfusion.com/js/installation-and-deployment) to know more about script and style sheets installed on the local machine.

CDN link: [Click here](https://help.syncfusion.com/js/cdn) to know more about script and style sheets available in online.

NuGet package: [Click here](https://help.syncfusion.com/js/installation-and-deployment#configuring-syncfusion-nuget-packages) to know more about script and style sheets available in the NuGet package. 

### Control initialization
To initialize a pivot gauge widget, first you can define a “div” tag with an appropriate “id” attribute which acts as a container for the pivot gauge widget. Then, you can initialize the widget by using the `ejPivotGauge` method.
    
{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
    <head>
        <title>PivotGauge - Getting Started</title>
        <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" type="text/css" />
        <script src="http://cdn.syncfusion.com/js/assets/external/jquery-3.0.0.min.js" type="text/javascript"></script>
        <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js" type="text/javascript"></script>
    </head>

    <body>
        <!--Create a tag which acts as a container for ejPivotGauge widget.-->
        <div id="PivotGauge1"> </div>
        <script type="text/javascript">
            //Set properties and initialize ejPivotGauge widget.
            $(function() {
                $("#PivotGauge1").ejPivotGauge({
                    url: "/Olap",
                    scales: [
                        {
                            showRanges: true,
                            radius: 150, showScaleBar: true, size: 1,
                            border: {
                                width: 0.5
                            },
                            showIndicators: true, showLabels: true,
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
                                }
                            ],
                            ticks: [
                                {
                                    type: "major",
                                    distanceFromScale: 2,
                                    height: 16,
                                    width: 1, color: "#8c8c8c"
                                },
                                {
                                    type: "minor",
                                    height: 6,
                                    width: 1,
                                    distanceFromScale: 2,
                                    color: "#8c8c8c"
                                }
                            ],
                            labels: [
                                {
                                    color: "#8c8c8c"
                                }
                            ],
                            ranges: [
                                {
                                    distanceFromScale: -5,
                                    backgroundColor: "#fc0606",
                                    border: { color: "#fc0606" }
                                },
                                {
                                    distanceFromScale: -5
                                }
                            ],
                            customLabels: [
                                {
                                    position: { x: 180, y: 290 },
                                    font: { size: "10px", fontFamily: "Segoe UI", fontStyle: "Normal" }, color: "#666666"
                                }, 
                                {
                                    position: { x: 180, y: 320 },
                                    font: { size: "10px", fontFamily: "Segoe UI", fontStyle: "Normal" }, color: "#666666"
                                }, 
                                {
                                    position: { x: 180, y: 150 },
                                    font: { size: "12px", fontFamily: "Segoe UI", fontStyle: "Normal" }, color: "#666666"
                                }
                            ]
                        }
                    ]
                });
            });
        </script>
    </body>
</html>

{% endhighlight %}

The [`url`](../api/ejpivotgauge#members:url) property in the pivot gauge widget points the service endpoint, where the data is processed and fetched in the form of JSON. The services used for the pivot gauge widget as endpoint are WCF and WebAPI.

N> The above "GettingStarted.html" contains WebAPI [`url`](../api/ejpivotgauge#members:url), which is **“/Olap”**. If you are using the WCF service, then the [`url`](../api/ejpivotgauge#members:url) will look like **"/OlapService.svc"**.

### WebAPI

**Adding a WebAPI controller**

To add a WebAPI controller in your existing web application, right-click the project in the solution explorer and select **Add > New Item.** In the **Add New Item** window, select **WebAPI Controller Class** and name it “OlapController.cs,” and then click **Add.**

The WebAPI controller is added to your application, which, in-turn, comprises the following file. The utilization of this file will be explained in the following sections:
 
* OlapController.cs

N> While adding the WebAPI controller class, add the mandatory suffix “Controller”. For example, in the demo, the controller is named “OlapController”.

Next, remove all existing methods such as “Get”, “Post”, “Put”, and “Delete” present in the `OlapController.cs` file.

{% highlight c# %}

namespace PivotGaugeDemo
{
    public class OlapController : ApiController
    {
    
    }
}

{% endhighlight %}

**List of dependency libraries**

Next, you can add the below-mentioned dependency libraries to your web application. These libraries can be found in the GAC (Global Assembly Cache).

To add them to your web application, right-click **References** in the solution explorer and select **Add Reference.** In the **Reference Manager** dialog, under **Assemblies > Extension**, the following Syncfusion libraries are found. 

N> If you have installed any version of SQL Server Analysis Service (SSAS) or Microsoft ADOMD.NET utility, then the location of Microsoft.AnalysisServices.AdomdClient library is [system drive:\Program Files (x86)\Microsoft.NET\ADOMD.NET]. If you have installed any version of Essential Studio, then the location of Syncfusion libraries is [system drive:\Program Files (x86)\Syncfusion\Essential Studio\{{ site.releaseversion }}\Assemblies].

* Microsoft.AnalysisServices.AdomdClient
* Syncfusion.Compression.Base
* Syncfusion.Linq.Base
* Syncfusion.Olap.Base
* Syncfusion.PivotAnalysis.Base
* Syncfusion.EJ
* Syncfusion.EJ.Export
* Syncfusion.EJ.Pivot

**List of namespaces**

Following are the list of namespaces to be added on top of the main class in the `OlapController.cs` file:

{% highlight c# %}

using Syncfusion.Olap.Manager;
using Syncfusion.Olap.Reports;
using Syncfusion.JavaScript;

namespace PivotGaugeDemo
{
    public class OlapController : ApiController
    {
        
    }
}

{% endhighlight %}

**Data source initialization**

Now, the connection string to connect the OLAP cube and the pivot gauge instances is created immediately in the main class of the `OlapController.cs` file.

{% highlight c# %}

namespace PivotGaugeDemo
{
    public class OlapController : ApiController
    {
        string connectionString = "Data Source=http://bi.syncfusion.com/olap/msmdpump.dll; Initial Catalog=Adventure Works DW 2008 SE;";
        PivotGauge pivotGauge = new PivotGauge();
        //Other codes
    }
}

{% endhighlight %}

**Service methods in WebAPI controller**

Now, you can define the service methods in the OlapController class, find in the `OlapController.cs` file which was created while adding the WebAPI controller class to your web application.
 
{% highlight c# %}

namespace PivotGaugeDemo
{
    public class OlapController : ApiController
    {
        string connectionString = "Data Source=http://bi.syncfusion.com/olap/msmdpump.dll; Initial Catalog=Adventure Works DW 2008 SE;";
        PivotGauge pivotGauge = new PivotGauge();
        
        [System.Web.Http.ActionName("InitializeGauge")]
        [System.Web.Http.HttpPost]
        public Dictionary<string, object> InitializeGauge(Dictionary<string, object> jsonResult)
        {
            OlapDataManager DataManager = new OlapDataManager(connectionString);
            DataManager.SetCurrentReport(CreateOlapReport());
            return pivotGauge.GetJsonData(jsonResult["action"].ToString(), DataManager);
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

**Configure routing in global application class**

To add a Global.asax in your existing web application, right-click the project in the solution explorer and select **Add > New Item.** In the **Add New Item** window, select **Global Application Class** and name it “Global.asax”, and then click **Add.**

After adding the **Global.asax** file, immediately add the namespace **“using System.Web.Http;”**, and then configure the routing as shown in the following code example:

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

Now, the pivot gauge will be rendered with the provided data as shown below:

![](Olap-Getting-Started_images/ServerMode.png)

### WCF
This section demonstrates the utilization of the WCF service as endpoint binding the [`OLAP`](/api/js/ejpivotgauge#members:analysisMode) data source to a simple pivot gauge. For more details on this topic, [click here](https://help.syncfusion.com/js/pivotgauge/olap-connectivity#wcf).





