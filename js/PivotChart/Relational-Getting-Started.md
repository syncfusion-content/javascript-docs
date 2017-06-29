---
layout: post
title: Relational-Getting-Started
description: relational-getting started
platform: js
control: PivotChart
documentation: ug
api: /api/js/ejpivotchart
---

# Getting Started

## Creating a simple application with PivotChart and Relational datasource (Client Mode)

This section covers the basic information required to populate a simple PivotChart with Relational data completely on the client-side.  

### Scripts and CSS References

Create a HTML page and add scripts and style sheets that are mandatorily required to render a PivotChart widget which are highlighted below in an appropriate order.

1. ej.web.all.min.css
2. jQuery-3.0.0.min.js
4. ej.web.all.min.js

### Initialize PivotChart

Place a "div" tag in the HTML page which acts as a container for the PivotChart widget.  Then initialize the widget using the "ejPivotChart" method.

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
                //Initialize ejPivotChart widget.
                $("#PivotChart1").ejPivotChart();
            });
        </script>
    </body>
</html>

{% endhighlight %}

### Populate PivotChart With Data

Let us now see how to populate the PivotChart control using a sample JSON data as shown below. 

{% highlight html %}

var pivotData = [
    { Amount: 100, Country: "Canada", Product: "Bike" },
    { Amount: 200, Country: "Germany", Product: "Van" },
    { Amount: 300, Country: "Germany", Product: "Car" },
    { Amount: 150, Country: "United Kingdom", Product: "Bike" },
    { Amount: 200, Country: "Canada", Product: "Car" }
];
{% endhighlight %}

Now set the JSON data to the **"data"** property available inside the **"dataSource"** object.  The **"dataSource"** object allows us to set the raw data input and the fields that need to be displayed in the row, column, value and filter section of the PivotChart control. 

{% highlight html %}

<!DOCTYPE html>
<html>

    //....
    <body>
        <div id="PivotChart1" style="width: 800px; height: 350px"></div>
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
                $("#PivotChart1").ejPivotChart({
                    dataSource: {
                        //Datasource bound to PivotChart control.
                        data: pivotData,
                        //Required fields in row, column, value and filter areas of PivotChart control.
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

The above code will generate a simple PivotChart with sales amount over a range of products across different locations. 

![](Relational-Getting-Started_images/PopulatePivotChartWithData.png)

### Apply Sorting

You can sort a field either in ascending or descending order using the **"sortOrder"** property. Sorting is applicable only for the fields in rows and columns.

N> By default, the values in all fields are arranged in ascending order.

{% highlight html %}

$(function () {
    $("#PivotChart1").ejPivotChart({
        dataSource: {
            //....
            rows: [
                {
                    fieldName: "Country",
                    fieldCaption: "Country",
                    sortOrder: ej.PivotAnalysis.SortOrder.Descending
                }
            ],
            //....
        },
    });
});
{% endhighlight %}


![](Relational-Getting-Started_images/ApplySorting.png)


### Apply Filtering

Filtering option allows you to specify a set of values that need to be made either visible or hidden. Also filtering option is applicable only for Row, Column and Filter areas.

**"filterItems"** object allows us to apply filtering to the fields using the following properties:

* filterType -  indicates whether the values should be included or excluded.
* values -  specify an array of values that needs to be included or excluded within the particular field.


{% highlight html %}

$(function () {
    $("#PivotChart1").ejPivotChart({
        dataSource: {
            data: pivotData,
            rows: [
                {
                    fieldName: "Country",
                    fieldCaption: "Country",
                    filterItems: {
                        filterType: ej.PivotAnalysis.FilterType.Exclude,
                        values: ["United Kingdom"]
                    }
                }
            ],
            columns: [
                {
                    fieldName: "Product",
                    fieldCaption: "Product",
                    filterItems: {
                        filterType: ej.PivotAnalysis.FilterType.Include,
                        values: ["Bike", "Car"]
                    }
                }
            ],
            //....
        },
    });
});
{% endhighlight %}

![](Relational-Getting-Started_images/ApplyFiltering.png)

## Creating a simple application with PivotChart and Relational datasource (Server Mode)

This section covers the information required to create a simple PivotChart bound with Relational datasource from server-side. 

N>The illustration is done by creating a simple Web Application through Visual Studio IDE since PivotChart in ServerMode requires .NET dependency. The Web Application would contain a HTML page and a service which transfers data to server-side, processes and returns back the data to client-side for control rendering. The service utilized for communication could be either a WebAPI Controller Class or a WCF Service based on user requirement.  We have illustrated both for user convenience.

### Project Initialization

Create a new **ASP.NET Empty Web Application** by using Visual Studio IDE and name the project as **“PivotChartDemo”.**

Next you need to add a HTML page. To add a HTML page in your Web Application, right-click on the project in Solution Explorer and select **Add > New Item**. In the **Add New Item** window, select **HTML Page** and name it as “GettingStarted.html”, click **Add.**
 
Now you need to set “GettingStarted.html” as start-up page. In-order to do so, right-click on “GettingStarted.html” page and select **“Set As Start Page”**.

### Scripts and CSS Initialization
The scripts and style sheets that are mandatorily required to render a PivotChart widget inside a HTML page are highlighted below in an appropriate order.

1. ej.web.all.min.css
2. jQuery-3.0.0.min.js
3. ej.web.all.min.js

The scripts and style sheets listed above could be found in any of the following locations:

Local Disk: [Click here](https://help.syncfusion.com/js/installation-and-deployment) to know more about script and style sheets installed in local machine.
 
CDN Link: [Click here](https://help.syncfusion.com/js/cdn) to know more about script and style sheets available online.

NuGet Package: [Click here](https://help.syncfusion.com/js/installation-and-deployment#configuring-syncfusion-nuget-packages) to know more about script and style sheets available in NuGet package.

### Control Initialization

In-order to initialize a PivotChart widget, first you need to define a “div” tag with an appropriate “id” attribute which acts as a container for PivotChart widget. Then you need to initialize the widget using `ejPivotChart` method.

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
                    url: "/Relational",
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

The “url” property in PivotChart widget points the service endpoint, where the data gets processed and fetched in the form of JSON. The services used for the PivotChart widget as endpoint are WebAPI and WCF.

N> The above "GettingStarted.html" contains WebAPI URL, which is **“/Relational”**. Suppose if you are using WCF service then the URL would look like **"/RelationalService.svc"**. 

### WebAPI

**Adding a WebAPI Controller**

To add a WebAPI controller in your existing Web Application, right-click on the project in Solution Explorer and select **Add > New Item**. In the **Add New Item** window, select **WebAPI Controller Class** and name it as “RelationalController.cs”, click **Add**.
 
Now WebAPI controller is added to your application successfully which in-turn comprise of the following file. The utilization of this file will be explained in the immediate sections. 

* RelationalController.cs

N> While adding WebAPI Controller Class, name it with the suffix “Controller” that is mandatory. For example, in demo the controller is named as “RelationalController”.

Next, remove all the existing methods such as “Get”, “Post”, “Put” and “Delete” present inside `RelationalController.cs` file.

{% highlight c# %}

namespace PivotChartDemo
{
    public class RelationalController: ApiController
    {
    
    }
}

{% endhighlight %}

**List of Dependency Libraries**

Next you need to add the below mentioned dependency libraries into your Web Application. These libraries could be found in GAC (Global Assembly Cache) as well.

To add them to your Web Application, right-click on **References** in Solution Explorer and select **Add Reference.** Now in the **Reference Manager** dialog, under **Assemblies > Extension**, the following Syncfusion libraries are found. 

N> If you have installed any version of Essential Studio, then the location of Syncfusion libraries is [system drive:\Program Files (x86)\Syncfusion\Essential Studio\{{ site.releaseversion }}\Assemblies].

* Syncfusion.Compression.Base
* Syncfusion.Linq.Base
* Syncfusion.Olap.Base
* Syncfusion.PivotAnalysis.Base
* Syncfusion.XlsIO.Base
* Syncfusion.Pdf.Base
* Syncfusion.DocIO.Base
* Syncfusion.EJ
* Syncfusion.EJ.Web
* Syncfusion.EJ.Pivot

**List of Namespaces**

Following are the list of namespaces to be added on top of the main class inside `RelationalController.cs` file.
 
{% highlight c# %}

using System.Web.Script.Serialization;
using Syncfusion.JavaScript;
using Syncfusion.PivotAnalysis.Base; 

namespace PivotChartDemo
{
    public class RelationalController : ApiController
    {

    }
}
{% endhighlight %}

**Datasource Initialization**

A simple collection is provided as a datasource for the PivotChart in this demo section. This datasource is placed inside a separate class “ProductSales” in `RelationalController.cs` file. Refer to the following code example.

{% highlight c# %}

namespace PivotChartDemo
{
    //....
    //....
    
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

Now you need to define the service methods inside RelationalController class, found inside `RelationalController.cs` file, created while adding WebAPI Controller Class to your Web Application.
 
{% highlight c# %}

namespace PivotChartDemo
{
    public class RelationalController : ApiController
    {
        PivotChart pivotChart = new PivotChart();
        JavaScriptSerializer serializer = new JavaScriptSerializer();

        [System.Web.Http.ActionName("InitializeChart")]
        [System.Web.Http.HttpPost]
        public Dictionary<string, object> InitializeChart(Dictionary<string, object> jsonResult)
        {
            this.BindData();
            return pivotChart.GetJsonData(jsonResult["action"].ToString(), ProductSales.GetSalesData());
        }

        [System.Web.Http.ActionName("DrillChart")]
        [System.Web.Http.HttpPost]
        public Dictionary<string, object> DrillChart(Dictionary<string, object> jsonResult)
        {
            this.BindData();
            return pivotChart.GetJsonData(jsonResult["action"].ToString(), ProductSales.GetSalesData(), jsonResult["drilledSeries"].ToString());
        }

        private void BindData()
        {
            this.pivotChart.PivotEngine.PivotRows.Add(new PivotItem { FieldMappingName = "Country", FieldHeader = "Country", TotalHeader = "Total" });
            this.pivotChart.PivotEngine.PivotRows.Add(new PivotItem { FieldMappingName = "State", FieldHeader = "State", TotalHeader = "Total" });
            this.pivotChart.PivotEngine.PivotRows.Add(new PivotItem { FieldMappingName = "Date", FieldHeader = "Date", TotalHeader = "Total" });
            this.pivotChart.PivotEngine.PivotColumns.Add(new PivotItem { FieldMappingName = "Product", FieldHeader = "Product", TotalHeader = "Total" });
            this.pivotChart.PivotEngine.PivotCalculations.Add(new PivotComputationInfo { CalculationName = "Amount", Description = "Amount", FieldHeader = "Amount", FieldName = "Amount", Format = "C", SummaryType = Syncfusion.PivotAnalysis.Base.SummaryType.DoubleTotalSum });
        }
    }
    .....
    ..... // Datasource initialization
    .....
}
{% endhighlight %}

**Configure routing in Global Application Class**

To add a Global.asax in your existing Web Application, right-click on the project in Solution Explorer and select **Add > New** Item. In the **Add New Item** window, select **Global Application** Class and name it as **“Global.asax”**, click **Add.**
 
Once you finish adding the **Global.asax** file, delete all the methods inside the **Global** class and add the namespace **“using System.Web.Http;”** and then you can configure routing like in the following code example.

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

Now, PivotChart is rendered with sales amount details over a set of products across different countries. 
 
![](Relational-Getting-Started_images/ServerMode.png)

### WCF

This section demonstrates the utilization of WCF service as endpoint binding Relational datasource to a simple PivotChart. For more details on this topic, [click here](https://help.syncfusion.com/js/pivotchart/relational-connectivity#wcf-1).
  


