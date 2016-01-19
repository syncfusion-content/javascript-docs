---
layout: post
title: Getting-Started
description: getting started
platform: js
control: PivotGrid
documentation: ug
---

# Getting Started

##Creating a simple application with PivotGrid and OLAP datasource

This section covers the information required to create a simple PivotGrid bound to OLAP datasource.  

N> We will be illustrating this section by creating a simple Web Application through Visual Studio IDE since PivotGrid is a server-side control with .NET dependency. The Web Application would contain a HTML page and a service that would transfer data to server-side, process and return back the data to client-side for control re-rendering. The service utilized for communication could be either WCF or WebAPI based on user requirement and we have illustrated both for user convenience.

###Project Initialization
Create a new **ASP.NET Empty Web Application** by using Visual Studio IDE and name the project as **“PivotGridDemo”**.

Next you need to add a HTML page. To add a HTML page in your Web Application, right-click on the project in Solution Explorer and select **Add > New Item.** In the **Add New Item** window, select **HTML Page** and name it as **“GettingStarted.html”**, click **Add.**

Now you need to set “GettingStarted.html” as start-up page. In-order to do so, right-click on “GettingStarted.html” page and select **“Set As Start Page”**.

###Scripts and CSS Initialization
The scripts and style sheets that are mandatorily required to render a PivotGrid widget inside a HTML page are highlighted below in an appropriate order.

1. ej.widgets.all.min.css
2. jquery-1.10.2.min.js
3. jquery.easing.1.3.min.js
4. ej.web.all.min.js

The scripts and style sheets listed above could be found in any of the following locations:

Local Disk: [Click here](http://helpjs.syncfusion.com/js/installation-and-deployment) to know more about script and style sheets installed in local machine.

CDN Link: [Click here](http://helpjs.syncfusion.com/js/cdn) to know more about script and style sheets available online.

NuGet Package: [Click here](http://helpjs.syncfusion.com/js/installation-and-deployment#configuring-syncfusion-nuget-packages) to know more about script and style sheets available in NuGet package. 

###Control Initialization
In-order to initialize a PivotGrid widget, first you need to define a “div” tag with an appropriate “id” attribute which acts as a container for PivotGrid widget. Then you need to initialize the widget using `ejPivotGrid` method.
    
{% highlight html %}
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title>PivotGrid - Getting Started</title>
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" type="text/css" />
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js" type="text/javascript"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js" type="text/javascript"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js" type="text/javascript"></script>
</head>

<body>
    <form id="form1" runat="server">
        <div>
            <!--Create a tag which acts as a container for ejPivotGrid widget.-->
            <div id="PivotGrid1" style="height: 350px; width: 100%; overflow: auto"> </div>
            <script type="text/javascript">
                //Set properties and initialize ejPivotGrid widget.
                $(function()
                {
                    $("#PivotGrid1").ejPivotGrid(
                    {
                        url: "../OLAPService"
                    });
                });
            </script>
        </div>
    </form>
</body>

</html>

{% endhighlight %}

The “url” property in PivotGrid widget points the service endpoint, where data are processed and fetched in the form of JSON. The service used for the PivotGrid widget as endpoint are WCF and WebAPI.

N> The above "GettingStarted.html" contains WebAPI Url, which is **“../OLAPService”**. Suppose if you are using WCF service then the Url would look like **"../OLAPService.svc"**. 

###WebAPI

**Adding a WebAPI Controller**

To add a WebAPI controller in your existing Web Application, right-click on the project in Solution Explorer and select **Add > New Item.** In the **Add New Item** window, select **WebAPI Controller Class** and name it as “OLAPServiceController.cs”, click **Add.**

Now WebAPI controller is added into your application successfully which in-turn comprise of the following file. The utilization of this file will be explained in the following sections.
 
* OLAPServiceController.cs

N> While adding WebAPI Controller Class, name it with the suffix “Controller” that is mandatory. For example, in demo the controller is named as “OLAPServiceController”.

Next, remove all the existing methods such as “Get”, “Post”, “Put” and “Delete” present inside `OLAPServiceController.cs` file. 

{% highlight c# %}

namespace PivotGridDemo
{
    public class OLAPServiceController : ApiController
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

Following are the list of namespaces to be added on top of the main class inside `OLAPServiceController.cs` file.

{% highlight c# %}

using System.Web;
using System.Web.Script.Serialization;
using System.ServiceModel.Activation;
using Syncfusion.Olap.Manager;
using Syncfusion.Olap.Reports;
using Syncfusion.JavaScript;
using Syncfusion.JavaScript.Olap;
using OLAPUTILS = Syncfusion.JavaScript.Olap;

namespace PivotGridDemo
{
    public class OLAPServiceController : ApiController
    {

    }
}

{% endhighlight %}

**Datasource Initialization**

Now, the connection string to connect OLAP Cube, PivotGrid and JavaScriptSerializer instances are created immediately inside the main class in `OLAPServiceController.cs` file.

{% highlight c# %}

namespace PivotGridDemo
{
    public class OLAPServiceController : ApiController
    {
        PivotGrid htmlHelper = new PivotGrid();
        string connectionString = "Data Source=http://bi.syncfusion.com/olap/msmdpump.dll; Initial Catalog=Adventure Works DW 2008 SE;";
        JavaScriptSerializer serializer = new JavaScriptSerializer();
        //Other codes

    }
}

{% endhighlight %}

**Service methods in WebAPI Controller**

Now you need to define the service methods inside OLAPServiceController class, found inside `OLAPServiceController.cs` file, created while adding WebAPI Controller Class to your Web Application.
 
{% highlight c# %}

namespace PivotGridDemo
{
    public class OLAPServiceController : ApiController
    {
        PivotGrid htmlHelper = new PivotGrid();
        string connectionString = "Data Source=http://bi.syncfusion.com/olap/msmdpump.dll; Initial Catalog=Adventure Works DW 2008 SE;";
        JavaScriptSerializer serializer = new JavaScriptSerializer();

        [System.Web.Http.ActionName("InitializeGrid")]
        [System.Web.Http.HttpPost]
        public Dictionary<string, object> InitializeGrid(Dictionary<string, object> jsonResult)
        {
            Dictionary<string, object> customDict = new Dictionary<string, object>();
            OlapDataManager DataManager = new OlapDataManager(connectionString);
            DataManager.SetCurrentReport(CreateOlapReport());
            customDict = htmlHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["gridLayout"].ToString(), Convert.ToBoolean(jsonResult
["enablePivotFieldList"].ToString()));
            return customDict;
        }

        [System.Web.Http.ActionName("DrillGrid")]
        [System.Web.Http.HttpPost]
        public Dictionary<string, object> DrillGrid(Dictionary<string, object> jsonResult)
        {
            dynamic customData = serializer.Deserialize<dynamic>(jsonResult["customObject"].ToString());
            OlapDataManager DataManager = new OlapDataManager(connectionString);
            DataManager = new OlapDataManager(connectionString);
            if ((customData.ContainsKey("Language")))
            {
                DataManager.Culture = new System.Globalization.CultureInfo((customData["Language"]));
                DataManager.OverrideDefaultFormatStrings = true;
            }
            DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
            return htmlHelper.GetJsonData(jsonResult["action"].ToString(), connectionString, DataManager, jsonResult["cellPosition"].ToString(), jsonResult
["headerInfo"].ToString(), jsonResult["layout"].ToString());
        }

        [System.Web.Http.ActionName("NodeDropped")]
        [System.Web.Http.HttpPost]
        public Dictionary<string, object> NodeDropped(Dictionary<string, object> jsonResult)
        {
            OlapDataManager DataManager = new OlapDataManager(connectionString);
            DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
            return htmlHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["dropType"].ToString(), jsonResult["nodeInfo"].ToString(), null,
true);
        }

        [System.Web.Http.ActionName("Filtering")]
        [System.Web.Http.HttpPost]
        public Dictionary<string, object> Filtering(Dictionary<string, object> jsonResult)
        {
            OlapDataManager DataManager = new OlapDataManager(connectionString);
            DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
            return htmlHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, null, jsonResult["filterParams"].ToString());
        }

        [System.Web.Http.ActionName("FetchMembers")]
        [System.Web.Http.HttpPost]
        public Dictionary<string, object> FetchMembers(Dictionary<string, object> jsonResult)
        {
            OlapDataManager DataManager = new OlapDataManager(connectionString);
            DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
            return htmlHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, null, jsonResult["headerTag"].ToString());
        }

        [System.Web.Http.ActionName("Paging")]
        [System.Web.Http.HttpPost]
        public Dictionary<string, object> Paging(Dictionary<string, object> jsonResult)
        {
            OlapDataManager DataManager = new OlapDataManager(connectionString);
            DataManager.SetCurrentReport(htmlHelper.SetPaging(jsonResult["currentReport"].ToString(), jsonResult["pagingInfo"].ToString()));
            return htmlHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, jsonResult["gridLayout"].ToString());
        }

        [System.Web.Http.ActionName("RemoveButton")]
        [System.Web.Http.HttpPost]
        public Dictionary<string, object> RemoveButton(Dictionary<string, object> jsonResult)
        {
            OlapDataManager DataManager = new OlapDataManager(connectionString);
            DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
            return htmlHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, null, jsonResult["headerInfo"].ToString());
        }

        [System.Web.Http.ActionName("MemberExpanded")]
        [System.Web.Http.HttpPost]
        public Dictionary<string, object> MemberExpanded(Dictionary<string, object> jsonResult)
        {
            OlapDataManager DataManager = new OlapDataManager(connectionString);
            if (!string.IsNullOrEmpty(jsonResult["currentReport"].ToString()))
                DataManager.SetCurrentReport(Syncfusion.JavaScript.Olap.Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
            return htmlHelper.GetJsonData(jsonResult["actiion"].ToString(), DataManager, jsonResult["checkedStatus"].ToString(), jsonResult["parentNode"].ToString(),
jsonResult["tag"].ToString(), jsonResult["cubeName"].ToString());
        }

        [System.Web.Http.ActionName("Export")]
        [System.Web.Http.HttpPost]
        public void Export(System.IO.Stream stream)
        {
            System.IO.StreamReader sReader = new System.IO.StreamReader(stream);
            string args = System.Web.HttpContext.Current.Server.UrlDecode(sReader.ReadToEnd());
            OlapDataManager DataManager = new OlapDataManager(connectionString);
            string fileName = "Sample";
            htmlHelper.ExportPivotGrid(DataManager, args, fileName, System.Web.HttpContext.Current.Response);
        }
        
         [System.Web.Http.ActionName("DeferUpdate")]
        [System.Web.Http.HttpPost]
        public Dictionary<string, object> DeferUpdate(Dictionary<string, object> jsonResult)
        {
            OlapDataManager DataManager = new OlapDataManager(connectionString);
            DataManager.SetCurrentReport(Utils.DeserializeOlapReport(jsonResult["currentReport"].ToString()));
            return htmlHelper.GetJsonData(jsonResult["action"].ToString(), DataManager, null, jsonResult["filterParams"].ToString());
        }

        private OlapReport CreateOlapReport()
        {
            OlapReport olapReport = new OlapReport();
            olapReport.CurrentCubeName = "Adventure Works";

            MeasureElements measureElement = new MeasureElements();
            measureElement.Elements.Add(new MeasureElement { UniqueName = "[Measures].[Internet Sales Amount]" });

            DimensionElement dimensionElementRow = new DimensionElement();
            dimensionElementRow.Name = "Date";
            dimensionElementRow.AddLevel("Fiscal", "Fiscal Year");

            DimensionElement dimensionElementColumn = new DimensionElement();
            dimensionElementColumn.Name = "Customer";
            dimensionElementColumn.AddLevel("Customer Geography", "Country");

            olapReport.SeriesElements.Add(dimensionElementRow);
            olapReport.CategoricalElements.Add(dimensionElementColumn);
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

public class Global : System.Web.HttpApplication
    {
        protected void Application_Start(object sender, EventArgs e)
        {
            System.Web.Http.GlobalConfiguration.Configuration.Routes.MapHttpRoute(
                name: "DefaultApi",
                routeTemplate: "{controller}/{action}/{id}",
                defaults: new { id = RouteParameter.Optional });
            AppDomain.CurrentDomain.SetData("SQLServerCompactEditionUnderWebHosting", true);
        }
}

{% endhighlight %}

Now, PivotGrid will be rendered with Internet Sales Amount over a period of fiscal years across different customer geographic locations.

{% include image.html url="/js/PivotGrid/Getting-Started_images/olapwebapi.png" %}

###WCF
This section demonstrates the utilization of WCF service as endpoint binding OLAP datasource to a simple PivotGrid. For more details on this topic, [click here](http://help.syncfusion.com/js/pivotgrid/olap-connectivity#wcf).

##Creating a simple application with PivotGrid and Relational datasource

This section covers the information required to create a simple PivotGrid bound to Relational datasource. 

N> We will be illustrating this section by creating a simple Web Application through Visual Studio IDE since PivotGrid is a server-side control with .NET dependency. The Web Application would contain a HTML page and a service that would transfer data to server-side, process and return back the data to client-side for control re-rendering. The service utilized for communicate could be either WCF or WebAPI based on user requirement and we have also illustrated both for user convenience.

###Project Initialization

Create a new **ASP.NET Empty Web Application** by using Visual Studio IDE and name the project as **“PivotGridDemo”.**

Next you need to add a HTML page. To add a HTML page in your Web Application, right-click on the project in Solution Explorer and select **Add > New Item**. In the **Add New Item** window, select **HTML Page** and name it as “GettingStarted.html”, click **Add.**
 
Now you need to set “GettingStarted.html” as start-up page. In-order to do so, right-click on “GettingStarted.html” page and select **“Set As Start Page”**.

###Scripts and CSS Initialization
The scripts and style sheets that are mandatorily required to render a PivotGrid widget inside a HTML page are highlighted below in an appropriate order.

1. ej.widgets.all.min.css
2. jquery-1.10.2.min.js
3. jquery.easing.1.3.min.js
4. ej.web.all.min.js

The scripts and style sheets listed above could be found in any of the following locations:

Local Disk: [Click here](http://helpjs.syncfusion.com/js/installation-and-deployment) to know more about script and style sheets installed in local machine.
 
CDN Link: [Click here](http://helpjs.syncfusion.com/js/cdn) to know more about script and style sheets available online.

NuGet Package: [Click here](http://helpjs.syncfusion.com/js/installation-and-deployment#configuring-syncfusion-nuget-packages) to know more about script and style sheets available in NuGet package.

###Control Initialization

In-order to initialize a PivotGrid widget, first you need to define a “div” tag with an appropriate “id” attribute which acts as a container for PivotGrid widget. Then you need to initialize the widget using `ejPivotGrid` method.

{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">

<head>
    <title>PivotGrid - Getting Started</title>
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" type="text/css" />
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js" type="text/javascript"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js" type="text/javascript"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js" type="text/javascript"></script>
</head>

<body>
    <form id="form1" runat="server">
        <div>
            <!--Create a tag which acts as a container for ejPivotGrid widget.-->
            <div id="PivotGrid1" style="height: 350px; width: 100%; overflow: auto"> </div>
            <script type="text/javascript">
                //Set properties and initialize ejPivotGrid widget.
                $(function()
                {
                    $("#PivotGrid1").ejPivotGrid(
                    {
                        url: "/RelationalService"
                    });
                });
            </script>
        </div>
    </form>
</body>
</html>

{% endhighlight %}

The “url” property in PivotGrid widget points the service endpoint, where data are processed and fetched in the form of JSON. The service used for the PivotGrid widget as endpoint are WCF and WebAPI. 

###WebAPI

**Adding a WebAPI Controller**

To add a WebAPI controller in your existing Web Application, right-click on the project in Solution Explorer and select **Add > New Item**. In the **Add New Item** window, select **WebAPI Controller Class** and name it as “RelationalServiceController.cs”, click **Add**.
 
Now WebAPI controller is added into your application successfully which in-turn comprise of the following file. The utilization of this file will be explained in the immediate sections. 

* RelationalServiceController.cs

N> While adding WebAPI Controller Class, name it with the suffix “Controller” that is mandatory. For example, in demo the controller is named as “RelationalServiceController”.

Next, remove all the existing methods such as “Get”, “Post”, “Put” and “Delete” present inside `RelationalServiceController.cs` file.

{% highlight c# %}

namespace PivotGridDemo
{
    public class RelationalServiceController: ApiController
    {
        
    }
}

{% endhighlight %}

**List of Dependency Libraries**

Next you need to add the below mentioned dependency libraries into your Web Application. These libraries could be found in GAC (Global Assembly Cache) as well.

To add them to your Web Application, right-click on **References** in Solution Explorer and select **Add Reference.** Now in the **Reference Manager** dialog, under **Assemblies > Extension**, the following Syncfusion libraries are found. 

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

Following are the list of namespaces to be added on top of the main class inside `RelationalServiceController.cs` file.
 
{% highlight c# %}

using System.Web.Script.Serialization;
using Syncfusion.JavaScript;
using Syncfusion.PivotAnalysis.Base; 

namespace PivotGridDemo
{
    public class RelationalServiceController : ApiController
    {

    }
}

{% endhighlight %}

**Datasource Initialization**

A simple collection is provided as a datasource for the PivotGrid in this demo section. This datasource is placed inside a separate class “ProductSales” in `RelationalServiceController.cs` file. Refer to the following code example.

{% highlight c# %}

namespace PivotGridDemo
{
………
………
………
internal class ProductSales
    {
        public string Product { get; set; }

        public string Date { get; set; }

        public string Country { get; set; }

        public string State { get; set; }

        public int Quantity { get; set; }

        public double Amount { get; set; }

        public static ProductSalesCollection GetSalesData()
        {
            /// Geography
            string[] countries = new string[] { "Australia", "Canada", "France", "Germany", "United Kingdom", "United States" };
            string[] ausStates = new string[] { "New South Wales", "Queensland", "South Australia", "Tasmania", "Victoria" };
            string[] canadaStates = new string[] { "Alberta", "British Columbia", "Brunswick", "Manitoba", "Ontario", "Quebec" };
            string[] franceStates = new string[] { "Charente-Maritime", "Essonne", "Garonne (Haute)", "Gers", };
            string[] germanyStates = new string[] { "Bayern", "Brandenburg", "Hamburg", "Hessen", "Nordrhein-Westfalen", "Saarland" };
            string[] ukStates = new string[] { "England" };
            string[] ussStates = new string[] { "New York", "North Carolina", "Alabama", "California", "Colorado", "New Mexico", "South Carolina" };

            /// Time
            string[] dates = new string[] { "FY 2005", "FY 2006", "FY 2007", "FY 2008", "FY 2009" };

            /// Products
            string[] products = new string[] { "Bike", "Van", "Car" };
            Random r = new Random(123345345);

            int numberOfRecords = 2000;
            ProductSalesCollection listOfProductSales = new ProductSalesCollection();
            for (int i = 0; i < numberOfRecords; i++)
            {
                ProductSales sales = new ProductSales();
                sales.Country = countries[r.Next(1, countries.GetLength(0))];
                sales.Quantity = r.Next(1, 12);
                /// 1 percent discount for 1 quantity
                double discount = (30000 * sales.Quantity) * (double.Parse(sales.Quantity.ToString()) / 100);
                sales.Amount = (30000 * sales.Quantity) - discount;
                sales.Date = dates[r.Next(r.Next(dates.GetLength(0) + 1))];
                sales.Product = products[r.Next(r.Next(products.GetLength(0) + 1))];
                switch (sales.Product)
                {
                    case "Car":
                        {
                            sales.Date = "FY 2005";
                            break;
                        }
                }
                switch (sales.Country)
                {
                    case "Australia":
                        {
                            sales.State = ausStates[r.Next(ausStates.GetLength(0))];
                            break;
                        }
                    case "Canada":
                        {
                            sales.State = canadaStates[r.Next(canadaStates.GetLength(0))];
                            break;
                        }
                    case "France":
                        {
                            sales.State = franceStates[r.Next(franceStates.GetLength(0))];
                            break;
                        }
                    case "Germany":
                        {
                            sales.State = germanyStates[r.Next(germanyStates.GetLength(0))];
                            break;
                        }
                    case "United Kingdom":
                        {
                            sales.State = ukStates[r.Next(ukStates.GetLength(0))];
                            break;
                        }
                    case "United States":
                        {
                            sales.State = ussStates[r.Next(ussStates.GetLength(0))];
                            break;
                        }
                }
                listOfProductSales.Add(sales);
            }

            return listOfProductSales;
        }

        public override string ToString()
        {
            return string.Format("{0}-{1}-{2}", this.Country, this.State, this.Product);
        }

        public class ProductSalesCollection : List<ProductSales>
        {
        }
    }
}

{% endhighlight %}

**Service methods in WebAPI Controller**

Now you need to define the service methods inside RelationalServiceController class, found inside `RelationalServiceController.cs` file, created while adding WebAPI Controller Class to your Web Application.
 
{% highlight c# %}

namespace PivotGridDemo
{
    public class RelationalServiceController : ApiController
    {
        PivotGrid htmlHelper = new PivotGrid();
        JavaScriptSerializer serializer = new JavaScriptSerializer();
        Dictionary<string, object> dict = new Dictionary<string, object>();

        [System.Web.Http.ActionName("InitializeGrid")]
        [System.Web.Http.HttpPost]
        public Dictionary<string, object> InitializeGrid(Dictionary<string, object> jsonResult)
        {
                htmlHelper.PivotReport = BindDefaultData();
                dict = htmlHelper.GetJsonData(jsonResult["action"].ToString(), ProductSales.GetSalesData());
            return dict;
        }

        [System.Web.Http.ActionName("FetchMembers")]
        [System.Web.Http.HttpPost]
        public Dictionary<string, object> FetchMembers(Dictionary<string, object> jsonResult)
        {
            htmlHelper.PopulateData(jsonResult["currentReport"].ToString());
            dict = htmlHelper.GetJsonData(jsonResult["action"].ToString(), ProductSales.GetSalesData(), jsonResult["headerTag"].ToString(), jsonResult["sortedHeaders"].ToString());
            return dict;
        }

        [System.Web.Http.ActionName("Filtering")]
        [System.Web.Http.HttpPost]
        public Dictionary<string, object> Filtering(Dictionary<string, object> jsonResult)
        {
            htmlHelper.PopulateData(jsonResult["currentReport"].ToString());
            dict = htmlHelper.GetJsonData(jsonResult["action"].ToString(), ProductSales.GetSalesData(), jsonResult["filterParams"].ToString(), jsonResult["sortedHeaders"].ToString());
            return dict;
        }

        [System.Web.Http.ActionName("NodeStateModified")]
        [System.Web.Http.HttpPost]
        public Dictionary<string, object> NodeStateModified(Dictionary<string, object> jsonResult)
        {
            htmlHelper.PopulateData(jsonResult["currentReport"].ToString());
            dict = htmlHelper.GetJsonData(jsonResult["action"].ToString(), ProductSales.GetSalesData(), jsonResult["headerTag"].ToString(), jsonResult["dropAxis"].ToString(), jsonResult["filterParams"].ToString(), jsonResult["sortedHeaders"].ToString());
            return dict;
        }

        [System.Web.Http.ActionName("NodeDropped")]
        [System.Web.Http.HttpPost]
        public Dictionary<string, object> NodeDropped(Dictionary<string, object> jsonResult)
        {
            htmlHelper.PopulateData(jsonResult["currentReport"].ToString());
            dict = htmlHelper.GetJsonData(jsonResult["action"].ToString(), ProductSales.GetSalesData(), jsonResult["dropAxis"].ToString(), jsonResult["headerTag"].ToString(), jsonResult["filterParams"].ToString(), jsonResult["sortedHeaders"].ToString());
            return dict;
        }

        [System.Web.Http.ActionName("Sorting")]
        [System.Web.Http.HttpPost]
        public Dictionary<string, object> Sorting(Dictionary<string, object> jsonResult)
        {
            htmlHelper.PopulateData(jsonResult["currentReport"].ToString());
            dict = htmlHelper.GetJsonData(jsonResult["action"].ToString(), ProductSales.GetSalesData(), jsonResult["sortedHeaders"].ToString());
            return dict;
        }

        private PivotReport BindDefaultData()
        {
            PivotReport pivotSetting = new PivotReport();
            pivotSetting.PivotRows.Add(new PivotItem { FieldMappingName = "Product", FieldHeader = "Product", TotalHeader = "Total", ShowSubTotal = false });
            pivotSetting.PivotColumns.Add(new PivotItem { FieldMappingName = "Country", FieldHeader = "Country", TotalHeader = "Total", ShowSubTotal = false });
            pivotSetting.PivotCalculations.Add(new PivotComputationInfo { CalculationName = "Amount", Description = "Amount", FieldHeader = "Amount", FieldName = "Amount", Format = "C", SummaryType = Syncfusion.PivotAnalysis.Base.SummaryType.DoubleTotalSum });
            return pivotSetting;
        }
    }
}

{% endhighlight %}

**Configure routing in Global Application Class**

To add a Global.asax in your existing Web Application, right-click on the project in Solution Explorer and select **Add > New** Item. In the **Add New Item** window, select **Global Application** Class and name it as **“Global.asax”**, click **Add.**
 
Once you finish adding the **Global.asax** file, immediately add the namespace **“using System.Web.Http;”** and then you can configure routing like in the following code example.

{% highlight c# %}

public class Global : System.Web.HttpApplication
    {
        protected void Application_Start(object sender, EventArgs e)
        {
            System.Web.Http.GlobalConfiguration.Configuration.Routes.MapHttpRoute(
                name: "DefaultApi",
                routeTemplate: "{controller}/{action}/{id}",
                defaults: new { id = RouteParameter.Optional });
            AppDomain.CurrentDomain.SetData("SQLServerCompactEditionUnderWebHosting", true);
        }
}

{% endhighlight %}

Now, PivotGrid is rendered with Sales Amount over a set of products across different customer geographic locations. 
 
{% include image.html url="/js/PivotGrid/Getting-Started_images/relaionalwebapi.png" %}

###WCF

This section demonstrates the utilization of WCF service as endpoint binding Relational datasource to a simple PivotGrid. For more details on this topic, [click here](http://help.syncfusion.com/js/pivotgrid/olap-connectivity#wcf-1).
  
##Creating a simple application with PivotGrid and Relational datasource (Client-Side)

This section covers the information that you need to know to populate a simple PivotGrid with Relational data completely on the client-side.  

### Scripts and CSS References

Create a HTML page and add scripts and style sheets that are mandatorily required to render a PivotGrid widget which are highlighted below in an appropriate order.

1. ej.widgets.all.min.css
2. jquery-1.10.2.min.js
3. jquery.easing.1.3.min.js
4. jquery.linq.js
5. ej.web.all.min.js

### Initialize PivotGrid

Place a "div" tag in the HTML page which acts as a container for the PivotGrid widget. Then initialize the widget using the "ejPivotGrid" method.

{% highlight html %}

<!DOCTYPE html>
<html>
<head>

    <title>PivotGrid - Getting Started</title>

    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" type="text/css" />
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js" type="text/javascript"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js" type="text/javascript"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/linq.js/2.2.0.2/jquery.linq.js" type="text/javascript"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js" type="text/javascript"></script>

</head>
<body>
     <!--Create a tag which acts as a container for ejPivotGrid widget.-->
     <div id="PivotGrid1" style="height: 350px; width: 100%; overflow: auto">
     </div>

     <script type="text/javascript">
         $(function () {
              //Set properties and initialize ejPivotGrid widget.
              $("#PivotGrid1").ejPivotGrid();
         });
     </script>
</body>
</html>

{% endhighlight %}

### Populate PivotGrid With Data

Let us now see how to populate the PivotGrid control using a sample JSON data as shown below. 

{% highlight html %}

var pivotData = [
    { Amount: 100, Country: "Canada", Product: "Bike" },
    { Amount: 200, Country: "Germany", Product: "Van" },
    { Amount: 300, Country: "Germany", Product: "Car" },
    { Amount: 150, Country: "United Kingdom", Product: "Bike" },
    { Amount: 200, Country: "Canada", Product: "Car" }
]

{% endhighlight %}

Now set the JSON data to the **"data"** property present inside the **"dataSource"** object. **"dataSource"** object allows us to set both datasource as well as the fields that needs to be displayed in the row, column, value and filter section of the PivotGrid control. 

{% highlight html %}

<!DOCTYPE html>
<html>

//……

<body>
    <div id="PivotGrid1" style="height: 350px; width: 100%; overflow: auto">
    </div>
    <script type="text/javascript">

        //Datasource
        var pivotData = [
            { Amount: 100, Country: "Canada", Product: "Bike" },
            { Amount: 200, Country: "Germany", Product: "Van" },
            { Amount: 300, Country: "Germany", Product: "Car" },
            { Amount: 150, Country: "United Kingdom", Product: "Bike" },
            { Amount: 200, Country: "Canada", Product: "Car" }
        ]

        $(function () {
            $("#PivotGrid1").ejPivotGrid({
                dataSource: {
                    //Datasource bound to PivotGrid control.
                    data: pivotData,
                    //Required fields in row, column, value and filter areas of PivotGrid control.
                    rows: [
                        {
                            fieldName: "Country",
                            fieldCaption: "Country"
                        }
                    ],
                    columns: [
                        {
                            fieldName: "Product",
                            fieldCaption: "Product"
                        }
                    ],
                    values: [
                        {
                           fieldName: "Amount",
                           fieldCaption: "Amount"
                        }
                    ],
                },
            });
        });
    </script>
</body>
</html>


{% endhighlight %}

The above code will generate a simple PivotGrid with "Country" field in Row, "Product" field in Column and "Amount" field in Value section. 

{% include image.html url="/js/PivotGrid/Getting-Started_images/purejs.png" %}

### Apply Sorting

You can sort a field either to ascending or descending order using the **"sortOrder"** property. Sorting is applicable only for Row and Column fields. By default, fields are arranged in ascending order.

{% highlight html %}

$(function () {
    $("#PivotGrid1").ejPivotGrid({
        dataSource: {
            data: pivotData,
            rows: [{
                fieldName: "Country",
                fieldCaption: "Country",
                sortOrder: ej.PivotAnalysis.SortOrder.Descending
            }
            ],
            //……
        },
    });
});



{% endhighlight %}


{% include image.html url="/js/PivotGrid/Getting-Started_images/purejssorting.png" %}


### Apply Filtering

Filtering option allows you to specify a set of values that either need to be displayed or hided. Also filtering option is applicable only for Row, Column and Filter areas.

**"filterItems"** object allow us to apply filtering to the fields using the following properties:

* filterType -  indicates whether the values should be included or excluded.
* values -  specify an array of values that needs to be included or excluded within the particular field.


{% highlight html %}

$(function () {
    $("#PivotGrid1").ejPivotGrid({
        dataSource: {
            data: pivotData,
            rows: [{
                fieldName: "Country",
                fieldCaption: "Country",
                filterItems: {
                    filterType: ej.PivotAnalysis.FilterType.Exclude,
                    values: ["United Kingdom"]
                }
            }
            ],
            columns: [{
                fieldName: "Product",
                fieldCaption: "Product",
                filterItems: {
                    filterType: ej.PivotAnalysis.FilterType.Include,
                    values: ["Bike", "Car"]
                 }
            }
            ],
           //……
        },
    });
});

{% endhighlight %}

{% include image.html url="/js/PivotGrid/Getting-Started_images/purejsfiltering.png" %}

### Apply Summary Types

Allow us to specify the required summary type that PivotGrid should use in its summary cells. **"totalsum"** is the default summary type. Following are the summary types that are supported:

* totalsum
* average
* count
* minimum
* maximum

{% highlight html %}

$(function () {
    $("#PivotGrid1").ejPivotGrid({
        dataSource: {
            data: pivotData,
            //……
            values: [{
                fieldName: "Amount",
                fieldCaption: "Amount",
                summaryType: ej.PivotAnalysis.SummaryType.Average
            },
            {
                fieldName: "Quantity",
                fieldCaption: "Quantity",
                summaryType: ej.PivotAnalysis.SummaryType.TotalSum
            }
            ],
            //……
        },
    });
});


{% endhighlight %}

{% include image.html url="/js/PivotGrid/Getting-Started_images/purejssummarytype.png" %}



