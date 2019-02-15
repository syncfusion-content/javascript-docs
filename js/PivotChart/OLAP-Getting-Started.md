---
layout: post
title: OLAP-Getting-Started with PivotChart for Syncfusion JavaScript
description: olap-getting started
platform: js
control: PivotChart
documentation: ug
api: /api/js/ejpivotchart
---

# Getting started

## Creating a simple application with pivot chart and OLAP data sources (client mode)

This section covers the information required to populate a simple pivot chart with the [`OLAP`](/api/js/ejpivotchart#members:analysismode) data completely on the [`client-side`](/api/js/ejpivotchart#members:operationalmode).

### Scripts and CSS references

Create an HTML page and add scripts and style sheets that are required to render a pivot chart widget which are highlighted below in an appropriate order:

1. ej.web.all.min.css
2. jQuery-3.0.0.min.js
3. ej.web.all.min.js

### Initialize pivot chart

Place a "div" tag in the HTML page which acts as a container for the pivot chart widget. Then, initialize the widget by using the "ejPivotChart" method.

{% highlight html %}

<!DOCTYPE html>
<html>
    <head>
        <title>PivotChart - Getting Started</title>
        <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" type="text/css" />
        <script src="http://cdn.syncfusion.com/js/assets/external/jquery-3.0.0.min.js" type="text/javascript"></script>
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

### Populate pivot chart with data source

Initialize the [`OLAP`](/api/js/ejpivotchart#members:analysismode) data source for pivot chart widget as shown below:

{% highlight html %}

<html>

    //....

   <body>
        <div id="PivotChart1" style="width: 800px; height: 350px"></div>
        <script type="text/javascript">
            $(function() {
                $("#PivotChart1").ejPivotChart({
                    dataSource: {
                        data: "https://bi.syncfusion.com/olap/msmdpump.dll",
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

The above code will generate a simple pivot chart showing internet sales amount over a period of fiscal years across different customer geographic locations.

![JavaScript pivot chart control with OLAP client mode](Olap-Getting-Started_images/OlapClientMode.png)

The following table will explain the [`OLAP`](/api/js/ejpivotchart#members:analysismode) [`datasource`](/api/js/ejpivotchart#members:datasource) properties at [`client-side`](/api/js/ejpivotchart#members:operationalmode) in detail:

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
        {{'[`cube`](https://help.syncfusion.com/api/js/ejpivotchart#members:datasource-cube "cube")'| markdownify }}
    </td>
    <td>
        Contains the respective cube name as string type in the OLAP database.
    </td>
    </tr>
    <tr>
    <td>
        {{'[`sourceInfo`](https://help.syncfusion.com/api/js/ejpivotchart#members:datasource-sourceinfo "sourceInfo")'| markdownify }}
    </td>
    <td>
        To set the data source name to fetch the data.
    </td>
    </tr>
    <tr>
    <td>
        {{'[`providerName`](https://help.syncfusion.com/api/js/ejpivotchart#members:datasource-providername "providerName")'| markdownify }}
    </td>
    <td>
        Sets the provider name for PivotGrid to identify whether the provider is SSAS or Mondrian.
    </td>
    </tr>
    <tr>
    <td>
        {{'[`data`](https://help.syncfusion.com/api/js/ejpivotchart#members:datasource-data "data")'| markdownify }}
    </td>
    <td>
        Provides the raw data source for the PivotGrid.
    </td>
    </tr>
    <tr>
    <td>
        {{'[`catalog`](https://help.syncfusion.com/api/js/ejpivotchart#members:datasource-catalog "catalog")'| markdownify }}
    </td>
    <td>
        In connection with an OLAP database, this property contains the database name as string to fetch the data from the given connection string.
    </td>
    </tr>
    <tr>
        <td>
            {{'[`columns`](https://help.syncfusion.com/api/js/ejpivotchart#members:datasource-columns "columns")'| markdownify }}
        </td>
        <td>
            Lists out the items to be arranged in the columns section of the PivotGrid.
             <table class="params">
            <thead>
            <tr>
            <th>Properties</th>
            <th>Description</th>
            </tr>
            </thead>
            <tbody>
            <tr>
            <td>{{'[`fieldName`](https://help.syncfusion.com/api/js/ejpivotchart#members:datasource-columns-fieldname "fieldName")'| markdownify }} </td>
            <td>Allows you to bind the item by using its unique name as field name.</td>
            </tr>
            <tr>
            <td>{{'[`fieldCaption`](https://help.syncfusion.com/api/js/ejpivotchart#members:datasource-columns-fieldcaption "fieldCaption")'| markdownify }}</td>
            <td>Allows you to set the display caption for an item.</td>
            </tr>
            <tr>
            <td>{{'[`isNamedSets`](https://help.syncfusion.com/api/js/ejpivotchart#members:datasource-columns-isnamedsets "isNamedSets")'| markdownify }}</td>
            <td>Allows you to indicate whether the added item is a named set or not.</td>
            </tr>
            </tbody>
            </table>
        </td>
    </tr>
    <tr>
        <td>
            {{'[`rows`](https://help.syncfusion.com/api/js/ejpivotchart#members:datasource-rows "rows")'| markdownify }}
        </td>
        <td>
            Lists out the items to be arranged in the rows section of PivotGrid.
             <table class="params">
            <thead>
            <tr>
            <th>Properties</th>
            <th>Description</th>
            </tr>
            </thead>
            <tbody>
            <tr>
            <td>{{'[`fieldName`](https://help.syncfusion.com/api/js/ejpivotchart#members:datasource-rows-fieldname "fieldName")'| markdownify }} </td>
            <td>Allows you to bind the item by using its unique name as field name.</td>
            </tr>
            <tr>
            <td>{{'[`fieldCaption`](https://help.syncfusion.com/api/js/ejpivotchart#members:datasource-rows-fieldcaption "fieldCaption")'| markdownify }}</td>
            <td>Allows you to set the display caption for an item.</td>
            </tr>
            <tr>
            <td>{{'[`isNamedSets`](https://help.syncfusion.com/api/js/ejpivotchart#members:datasource-rows-isnamedsets "isNamedSets")'| markdownify }}</td>
            <td>Allows you to indicate whether the added item is a named set or not.</td>
            </tr>
            </tbody>
            </table>
        </td>
    </tr>
    <tr>
        <td>
            {{'[`values`](https://help.syncfusion.com/api/js/ejpivotchart#members:datasource-values "values")'| markdownify }}
        </td>
        <td>
            Lists out the items to be arranged in the rows section of PivotGrid.
            <table class="params">
            <thead>
            <tr>
            <th>Properties</th>
            <th>Description</th>
            </tr>
            </thead>
            <tbody>
            <tr>
            <td>{{'[`axis`](https://help.syncfusion.com/api/js/ejpivotchart#members:datasource-values-axis "axis")'| markdownify }} </td>
            <td>Allows you to set the axis name to place measures items.</td>
            </tr>
            <tr>
            <td>{{'[`measures`](https://help.syncfusion.com/api/js/ejpivotchart#members:datasource-values-measures "measures")'| markdownify }}</td>
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
                {{'[`fieldName`](https://help.syncfusion.com/api/js/ejpivotchart#members:datasource-values-measures-fieldName "fieldName")'| markdownify }} </td>
            <td>Allows you to bind the measure from the OLAP datasource by using its unique name as field name.</td>
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

## Creating a simple application with pivot chart and OLAP data source (server mode)

This section covers the information required to create a simple pivot chart bound to the [`OLAP`](/api/js/ejpivotchart#members:analysismode) data source.

N> This section is illustrated by creating a simple web application through the Visual Studio IDE since the pivot chart in server mode requires .NET dependency. The web application contains an HTML page and a service that will transfer the data to [`server-side`](/api/js/ejpivotchart#members:operationalmode), process it, and return it to the [`client-side`](/api/js/ejpivotchart#members:operationalmode) for control rendering. The service utilized for communication can be either WCF or WebAPI based on user requirement. Here, both are illustrated for user convenience.

### Project initialization
Create a new **ASP.NET Empty Web Application** by using the Visual Studio IDE and name the project **“PivotChartDemo”**.

Next, you can add an HTML page. To add an HTML page in your web application, right-click the project in the solution explorer and select **Add > New Item.** In the **Add New Item** window, select **HTML Page** and name it **“GettingStarted.html,”** and then click **Add.**

Now, you can set the “GettingStarted.html” as start-up page. To do so, right-click the “GettingStarted.html” page and select **“Set As Start Page”**.

### Scripts and CSS initialization
The scripts and style sheets that are required to render a pivot chart widget in the HTML page are highlighted below in an appropriate order:

This section covers the information required to create a simple pivot chart bound to the OLAP data source.

N> This section is illustrated by creating a simple web application through the Visual Studio IDE since the pivot chart in server mode requires .NET dependency. The web application contains an HTML page and a service that will transfer data to server-side, process it, and return it client-side for control rendering. The service utilized for communication can be either WCF or WebAPI based on user requirement. Both are illustrated here for user convenience.

### Project initialization
Create a new **ASP.NET Empty Web Application** by using the Visual Studio IDE and name the project **“PivotChartDemo.”**

Next, you should add an HTML page. To add an HTML page in your web application, right-click the project in the solution explorer and select **Add > New Item.** In the **Add New Item** window, select **HTML Page** and name it **“GettingStarted.html,”** and then click **Add.**

Now, you can set the “GettingStarted.html” page as start-up page. To do so, right-click “GettingStarted.html” page and select **“Set As Start Page.”**

### Scripts and CSS initialization
The scripts and style sheets that are required to render a pivot chart widget in an HTML page are highlighted below in an appropriate order:

1. ej.web.all.min.css
2. jQuery-3.0.0.min.js
3. ej.web.all.min.js

The scripts and style sheets listed above can be found in any of the following locations:

Local disk: [Click here](https://help.syncfusion.com/js/installation-and-deployment) to know more about script and style sheets installed on the local machine.

CDN link: [Click here](https://help.syncfusion.com/js/cdn) to know more about script and style sheets available in online.

NuGet package: [Click here](https://help.syncfusion.com/js/installation-and-deployment#configuring-syncfusion-nuget-packages) to know more about script and style sheets available in the NuGet package.

### Control initialization
To initialize a pivot chart widget, first you can define a “div” tag with an appropriate “id” attribute which acts as a container for the pivot chart widget. Then, you can initialize the widget by using the `ejPivotChart` method.

{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
    <head>
        <title>PivotChart - Getting Started</title>
        <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" type="text/css" />
        <script src="http://cdn.syncfusion.com/js/assets/external/jquery-3.0.0.min.js" type="text/javascript"></script>
        <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js" type="text/javascript"></script>
    </head>

    <body>
        <!--Create a tag which acts as a container for ejPivotChart widget.-->
        <div id="PivotChart1" style="width: 800px; height: 350px"> </div>
        <script type="text/javascript">
            //Set properties and initialize ejPivotChart widget.
            $(function() {
                $("#PivotChart1").ejPivotChart({
                    url: "/Olap",
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

The [`url`](/api/js/ejpivotchart#members:url) property in the pivot chart widget points the service endpoint, where the data is processed and fetched in the form of JSON. The services used for the pivot chart widget as endpoint are WCF and WebAPI.

N> The above "GettingStarted.html" contains WebAPI URL, which is **“/Olap”**. If you are using the WCF service, then the URL will look like **"/OlapService.svc"**.

Register the referenced assemblies in "Web.config" file available at the root of the application.

{% highlight xml %}

<compilation debug="true" targetFramework="4.5.1">
    <assemblies>
        ……
        ……
        <add assembly="Syncfusion.EJ, Version= {{ site.45esreleaseversion }}, Culture=neutral, PublicKeyToken=3d67ed1f87d44c89" />
        <add assembly="Syncfusion.EJ.Pivot, Version= {{ site.45esreleaseversion }}, Culture=neutral, PublicKeyToken=3d67ed1f87d44c89" />
        <add assembly="Syncfusion.EJ.Export, Version= {{ site.45esreleaseversion }}, Culture=neutral, PublicKeyToken=3d67ed1f87d44c89" />
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

**Adding a WebAPI controller**

To add a WebAPI controller in your existing web application, right-click the project in the solution explorer and select **Add > New Item.** In the **Add New Item** window, select **WebAPI Controller Class** and name it “OlapController.cs,” and then click **Add.**

The WebAPI controller is added to your application, which, in-turn, comprises the following file. The utilization of this file will be explained in the following sections.

* OlapController.cs

N> While adding the WebAPI controller class, add the mandatory suffix “Controller.” For example, in the demo, the controller is named “OlapController”.

Next, remove all existing methods such as “Get”, “Post”, “Put”, and “Delete” present in the `OlapController.cs` file.

{% highlight c# %}

namespace PivotChartDemo
{
    public class OlapController : ApiController
    {

    }
}

{% endhighlight %}

**List of dependency libraries**

Next, you can add the below mentioned dependency libraries to your web application. These libraries can be found in the GAC (Global Assembly Cache).

To add them to your web application, right-click **References** in the solution explorer and select **Add Reference.** In the **Reference Manager** dialog, under **Assemblies > Extension**, the following Syncfusion libraries are found.

N> If you have installed any version of SQL Server Analysis Service (SSAS) or Microsoft ADOMD.NET utility, then the location of Microsoft.AnalysisServices.AdomdClient library is [system drive:\Program Files (x86)\Microsoft.NET\ADOMD.NET]. If you have installed any version of Essential Studio, then the location of Syncfusion libraries is [system drive:\Program Files (x86)\Syncfusion\Essential Studio\{{ site.releaseversion }}\Assemblies].

* Microsoft.AnalysisServices.AdomdClient
* Syncfusion.Compression.Base
* Syncfusion.Linq.Base
* Syncfusion.Olap.Base
* Syncfusion.PivotAnalysis.Base
* Syncfusion.XlsIO.Base
* Syncfusion.Pdf.Base
* Syncfusion.DocIO.Base
* Syncfusion.EJ
* Syncfusion.EJ.Pivot
* Syncfusion.EJ.Export

**List of namespaces**

Following are the list of namespaces to be added on top of the main class in the `OlapController.cs` file:

{% highlight c# %}

using Syncfusion.Olap.Manager;
using Syncfusion.Olap.Reports;
using Syncfusion.JavaScript;

namespace PivotChartDemo
{
    public class OlapController : ApiController
    {

    }
}

{% endhighlight %}

**Data source initialization**

Now, the connection string to connect [`OLAP`](/api/js/ejpivotchart#members:analysismode) cube and pivot chart instances is created immediately in the main class of the `OlapController.cs` file.

{% highlight c# %}

namespace PivotChartDemo
{
    public class OlapController : ApiController
    {
        string connectionString = "Data Source=https://bi.syncfusion.com/olap/msmdpump.dll; Initial Catalog=Adventure Works DW 2008 SE;";
        PivotChart pivotChart = new PivotChart();
        //Other codes
    }
}

{% endhighlight %}

**Service methods in WebAPI controller**

Now, you can define the service methods in the OlapController class. To do this, find the `OlapController.cs` file which was created while adding the WebAPI controller class to your web application.

{% highlight c# %}

namespace PivotChartDemo
{
    public class OlapController : ApiController
    {
        string connectionString = "Data Source=https://bi.syncfusion.com/olap/msmdpump.dll; Initial Catalog=Adventure Works DW 2008 SE;";
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

The pivot chart will be rendered with customer count over a period of fiscal years across different customer geographic locations.

![JavaScript pivot chart control with OLAP server mode](Olap-Getting-Started_images/ServerMode.png)

### WCF
This section demonstrates the utilization of the WCF service as an endpoint binding the OLAP data source to the simple pivot chart. For more details on this topic, [click here](https://help.syncfusion.com/js/pivotchart/olap-connectivity#wcf).





