---
layout: post
title: OLAP-Connection-Types
description: OLAP Connection Types
platform: js
control: PivotGrid
documentation: ug
---

# DataBinding 

##OLAP

###Binding PivotGrid to Offline Cube
To connect an OLAP Cube available in local machine, set the physical path of the Cube in the connection string. The following code example illustrates the same.

{% highlight c# %}

string connectionString = @"DataSource = system drive:\OfflineCube\Adventure_Works_Ext.cub; Provider = MSOLAP;";
OlapDataManager DataManager = new OlapDataManager(connectionString);

{% endhighlight %}

###Binding PivotGrid to Cube in local SQL Server
To connect an OLAP Cube available in SQL Server Analysis Service in local machine, set the server name and database name in the connection string. When you have any credentials to connect your Cube, then set the “User ID” and “Password” attributes accordingly. The following code example illustrates the same.

{% highlight c# %}

string connectionString = "Data source=localhost; Initial Catalog=Adventure Works DW;"; 
OlapDataManager DataManager = new OlapDataManager(connectionString);

{% endhighlight %}

###Binding PivotGrid to Cube in online SQL Server
To connect an OLAP Cube available in SQL Server Analysis Service in online server through **XML/A**, set the host server link and database name in the connection string. When you have any credentials to connect your Cube, then set the “User ID” and “Password” attributes accordingly. The following code example illustrates the same.

{% highlight c# %}

string connectionString = "Data Source=http://bi.syncfusion.com/olap/msmdpump.dll; Initial Catalog=Adventure Works DW 2008 SE;"; 
OlapDataManager DataManager = new OlapDataManager(connectionString);

{% endhighlight %}

###Binding PivotGrid to Cube in online Mondrian Server
To connect an OLAP Cube available in Mondrian Server through **XML/A**, set the host server link and database name in the connection string. When you have any credentials to connect your Cube, then set the “User ID” and “Password” attributes accordingly. The following code example illustrates the same.

{% highlight c# %}

string connectionString = @"Data Source = http://localhost:8080/mondrian/xmla; Initial Catalog =FoodMart;";
OlapDataManager DataManager = new OlapDataManager(connectionString);
DataManager.DataProvider.ProviderName = Syncfusion.Olap.DataProvider.Providers.Mondrian;

{% endhighlight %}

###Binding PivotGrid to Cube in online ActivePivot Server
To connect an OLAP Cube available in ActivePivot Server through **XML/A**, set the host server link and database name in the connection string. When you have any credentials to connect your Cube, then set the “User ID” and “Password” attributes accordingly. The following code example illustrates the same.

{% highlight c# %}

string connectionString = @"Data Source = http://localhost:8080/cva_s/xmla; Initial Catalog = CVAS;";
OlapDataManager DataManager = new OlapDataManager(connectionString);
DataManager.DataProvider.ProviderName=Syncfusion.Olap.DataProvider.Providers.ActivePivot;

{% endhighlight %}

###WCF
**Adding a WCF Service**

To add a WCF service in an existing web application, right-click on the project in Solution Explorer and select **Add > New Item**. In the **Add New Item** window, select WCF Service and name it as **“OLAPService.svc”**, click **Add**.
 
Now WCF service is added into your application successfully which in-turn comprise of the following files. The utilization of these files will be explained in the immediate sections. 

* OLAPService.svc
* OLAPService.svc.cs
* IOLAPService.cs

**Configuring WCF Service Class**

Remove the “DoWork” method present inside both `OLAPService.svc.cs` and `IOLAPService.cs files`. Next, add “AspNetCompatibilityRequirements” attribute on top of main class present inside `OLAPService.svc.cs` and set “RequirementsMode” value to “Allowed”.

{% highlight c# %}

namespace PivotGridDemo
{
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class OLAPService : IOLAPService
    {

    }
}


{% endhighlight %}

**List of Dependency Libraries**

Next you need to add the below mentioned dependency libraries into your Web Application. These libraries could be found in GAC (Global Assembly Cache) as well.
 
To add them to your Web Application, right-click on **References** in Solution Explorer and select **Add Reference**. Now in the **Reference Manager** dialog, under **Assemblies > Extension**, the following Syncfusion libraries are found. 

N> If you have installed any version of SQL Server Analysis Service (SSAS) or Microsoft ADOMD.NET utility, then the location of Microsoft.AnalysisServices.AdomdClient library is [system drive:\Program Files (x86)\Microsoft.NET\ADOMD.NET]

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

Following are the list of namespaces to be added on top of the main class inside `OLAPService.svc.cs` file.

{% highlight c# %}

using System.Web.Script.Serialization;
using System.ServiceModel.Activation;
using Syncfusion.Olap.Manager;
using Syncfusion.Olap.Reports;
using Syncfusion.JavaScript;
using OLAPUTILS = Syncfusion.JavaScript.Olap;

namespace PivotGridDemo
{
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class OLAPService : IOLAPService
    {

    }
}

{% endhighlight %}

**Datasource Initialization**

Now the connection string to connect OLAP Cube, PivotGrid and JavaScriptSerializer instances are created immediately inside the main class in `OLAPService.svc.cs` file.

{% highlight c# %}

namespace PivotGridDemo
{
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class OLAPService : IOLAPService
    {
        PivotGrid htmlHelper = new PivotGrid();
        string connectionString = "Data Source=http://bi.syncfusion.com/olap/msmdpump.dll; Initial Catalog=Adventure Works DW 2008 SE;";
        JavaScriptSerializer serializer = new JavaScriptSerializer();
        //Other codes

    }
}

{% endhighlight %}

**Service methods in WCF Service**

First, you need to define the service methods inside IOLAPService interface, found in `IOLAPService.cs` file, created while adding WCF Service to your Web Application.

 {% highlight c# %}

namespace PivotGridDemo
{
    [ServiceContract]
    public interface IOLAPService
    {
        [OperationContract]
        Dictionary<string, object> InitializeGrid(string action, string gridLayout, bool enablePivotFieldList, object customObject);

        [OperationContract]
        Dictionary<string, object> DrillGrid(string action, string cellPosition, string currentReport, string headerInfo, string layout, object customObject);

        [OperationContract]
        Dictionary<string, object> Paging(string action, string pagingInfo, string currentReport, string gridLayout, object customObject);

        [OperationContract]
        Dictionary<string, object> NodeDropped(string action, string dropType, string nodeInfo, string filterParams, string currentReport);

        [OperationContract]
        Dictionary<string, object> RemoveButton(string action, string headerInfo, string currentReport);

        [OperationContract]
        Dictionary<string, object> FetchMembers(string action, string headerTag, string currentReport);

        [OperationContract]
        Dictionary<string, object> Filtering(string action, string filterParams, string currentReport);

        [OperationContract]
        Dictionary<string, object> MemberExpanded(string action, bool checkedStatus, string parentNode, string tag, string cubeName, string currentReport);

        [OperationContract]
        void Export(System.IO.Stream stream);
        
        [OperationContract]
        Dictionary<string, object> DeferUpdate(string action, string filterParams, string currentReport);
    }
}

{% endhighlight %}

Secondly, you need to elaborate the service methods inside the main class, found in `OLAPService.svc.cs` file 

{% highlight c# %}

namespace PivotGridDemo
{
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class OLAPService : IOLAPService
    {
        PivotGrid htmlHelper = new PivotGrid();
        string connectionString = "Data Source=http://bi.syncfusion.com/olap/msmdpump.dll; Initial Catalog=Adventure Works DW 2008 SE;";
        JavaScriptSerializer serializer = new JavaScriptSerializer();

        //This method provides the required information from the server side when initializing the PivotGrid.
        public Dictionary<string, object> InitializeGrid(string action, string gridLayout, bool enablePivotFieldList, object customObject)
        {
            OlapDataManager DataManager = null;
            dynamic customData = serializer.Deserialize<dynamic>(customObject.ToString());
            DataManager = new OlapDataManager(connectionString);
            DataManager.SetCurrentReport(CreateOlapReport());
            return htmlHelper.GetJsonData(action, DataManager, gridLayout, enablePivotFieldList);
        }

        //This method provides the required information from the server side when drill up/down operation is performed in PivotGrid.
        public Dictionary<string, object> DrillGrid(string action, string cellPosition, string currentReport, string headerInfo, string layout, object customObject)
        {
            dynamic customData = serializer.Deserialize<dynamic>(customObject.ToString());
            OlapDataManager DataManager = new OlapDataManager(connectionString);
            DataManager = new OlapDataManager(connectionString);
            DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(currentReport));
            return htmlHelper.GetJsonData(action, connectionString, DataManager, cellPosition, headerInfo, layout);
        }

        //This method provides the required information from the server side when tree node is dropped in PivotTable Field List.
        public Dictionary<string, object> NodeDropped(string action, string dropType, string nodeInfo, string filterParams, string currentReport)
        {
            OlapDataManager DataManager = new OlapDataManager(connectionString);
            DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(currentReport));
            return htmlHelper.GetJsonData(action, DataManager, dropType, nodeInfo, filterParams, true);
        }

        //This method provides the required information from the server side when filtering values in PivotTable Field List.
        public Dictionary<string, object> Filtering(string action, string filterParams, string currentReport)
        {
            OlapDataManager DataManager = new OlapDataManager(connectionString);
            DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(currentReport));
            return htmlHelper.GetJsonData(action, DataManager, null, filterParams);
        }

        //This method provides the required information from the server side when opening the editor in PivotTable Field List.
        public Dictionary<string, object> FetchMembers(string action, string headerTag, string currentReport)
        {
            OlapDataManager DataManager = new OlapDataManager(connectionString);
            DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(currentReport));
            return htmlHelper.GetJsonData(action, DataManager, null, headerTag);
        }

        //This method provides the required information from the server side when paging is done in PivotGrid.
        public Dictionary<string, object> Paging(string action, string pagingInfo, string currentReport, string gridLayout, object customObject)
        {
            OlapDataManager DataManager = new OlapDataManager(connectionString);
            DataManager.SetCurrentReport(htmlHelper.SetPaging(currentReport, pagingInfo));
            return htmlHelper.GetJsonData(action, DataManager, gridLayout);
        }

        //This method provides the required information from the server side when removing the split button from PivotTable Field List.
        public Dictionary<string, object> RemoveButton(string action, string headerInfo, string currentReport)
        {
            OlapDataManager DataManager = new OlapDataManager(connectionString);
            DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(currentReport));
            return htmlHelper.GetJsonData(action, DataManager, null, headerInfo);
        }

        //This method provides the required information from the server side when expanding member in member editor.
        public Dictionary<string, object> MemberExpanded(string action, bool checkedStatus, string parentNode, string tag, string cubeName, string currentReport)
        {
            OlapDataManager DataManager = new OlapDataManager(connectionString);
            if (!string.IsNullOrEmpty(currentReport))
                DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(currentReport));
            return htmlHelper.GetJsonData(action, DataManager, checkedStatus, parentNode, tag, cubeName);
        }

        //This method export PivotGrid to Excel, CSV, Word and PDF.
        public void Export(System.IO.Stream stream)
        {
            System.IO.StreamReader sReader = new System.IO.StreamReader(stream);
            string args = System.Web.HttpContext.Current.Server.UrlDecode(sReader.ReadToEnd());
            OlapDataManager DataManager = new OlapDataManager(connectionString);
            string fileName = "Sample";
            htmlHelper.ExportPivotGrid(DataManager, args, fileName, System.Web.HttpContext.Current.Response);
        }
        
        //This method Defer Update the Rows and Columns
         public Dictionary<string, object> DeferUpdate(string action, string filterParams, string currentReport)
        {
            OlapDataManager DataManager = new OlapDataManager(connectionString);
            DataManager.SetCurrentReport(Utils.DeserializeOlapReport(currentReport));
            return htmlHelper.GetJsonData(action, DataManager, null, filterParams);
        }

        //This method carries the information about the default report which when be rendered within PivotGrid initially.
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

**Configuring Web Configuration File**

You can expose services through the properties such as binding, contract and address by using an endpoint.

* Contract: This property indicates that the contract of the endpoint is exposing. Here you are referring to **IOLAPService** contract and hence it is **PivotGridDemo.IOLAPService**.
* Binding: In your application, you use **webHttpBinding** to post and receive the requests and responses between the client-end and the service.
* behaviorConfiguration: This property contains the name of the behavior to be used in the endpoint.

The endpointBehaviors are illustrated as follows. 
 
{% highlight xaml %}

<system.serviceModel>
……
……
    <services>
      <service name="PivotGridDemo.OLAPService">
        <endpoint address="" behaviorConfiguration="PivotGridDemo.OLAPServiceAspNetAjaxBehavior"
        binding="webHttpBinding" contract="PivotGridDemo.IOLAPService" />
      </service>
    </services>
</system.serviceModel>

{% endhighlight %}

The endpointBehaviors contain all the behaviors for an endpoint. You can link each endpoint to the respective behavior only by using this name property.

{% highlight xaml %}

<system.serviceModel>
    <behaviors>
      <endpointBehaviors>
        <behavior name="PivotGridDemo.OLAPServiceAspNetAjaxBehavior">
          <enableWebScript />
        </behavior>
      </endpointBehaviors>
    </behaviors>
……
……
</system.serviceModel>

{% endhighlight %}

N> In this example, “PivotGridDemo” indicates the name and root namespace of the Web Application created in Visual Studio IDE and “OLAPService” indicates the name of the WCF service created.
Now, PivotGrid is rendered with Internet Sales Amount over a period of fiscal years across different customer geographic locations.

{% include image.html url="/js/PivotGrid/OLAP-Connectivity_images/olapwebapi.png" %}

##Relational

###Binding PivotGrid to Collection
This section demonstrates binding of a collection to the PivotGrid control as datasource. For more information on this datasource refer to the following links.

When you are using WebAPI controller, refer to the “Datasource Initialization” section under the following [link](http://help.syncfusion.com/js/pivotgrid/getting-started). 

Or, when you use WCF service, refer to the “Datasource Initialization” section under the following [link](http://help.syncfusion.com/js/pivotgrid/olap-connectivity).

###WCF
**Adding a WCF Service**

To add a WCF service in an existing web application, right-click on the project in Solution Explorer and select **Add > New Item**. In the **Add New Item** window, select **WCF Service** and name it as **“RelationalService.svc”** and click **Add**. 

Now WCF service is added into your application successfully which in-turn comprise of the following files. The utilization of these files will be explained in the immediate sections. 

* RelationalService.svc
* RelationalService.svc.cs
* IRelationalService.cs

**Configuring WCF Service Class**

Remove the “DoWork” method present inside both `RelationalService.svc.cs` and `IRelationalService.cs` files. Next, add “AspNetCompatibilityRequirements” attribute on top of main class present inside `RelationalService.svc.cs` and set **“RequirementsMode”** value to **“Allowed”**.

{% highlight c# %}

namespace PivotGridDemo
{
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class RelationalService : IRelationalService
    {

    }
}

{% endhighlight %}
**List of Dependency Libraries**

Next you need to add the below mentioned dependency libraries into your Web Application. These libraries could be found in GAC (Global Assembly Cache) as well.
 
To add them to your Web Application, right-click on **References** in Solution Explorer and select **Add Reference**. Now in the **Reference Manager** dialog, under **Assemblies > Extension**, the following Syncfusion libraries are found. 

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

Following are the list of namespaces to be added on top of the main class inside `RelationalService.svc.cs` file.

{% highlight c# %}

using System.Web.Script.Serialization;
using System.ServiceModel.Activation;
using Syncfusion.JavaScript;
using Syncfusion.PivotAnalysis.Base; 

namespace PivotGridDemo
{
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class RelationalService : IRelationalService
    {

    }
}

{% endhighlight %}

**Datasource Initialization**

A simple collection is provided as a datasource for our PivotGrid in this demo section. This datasource is placed inside a separate class named “ProductSales” in `RelationalService.svc.cs` file. Refer to the following code example.

{% highlight c# %}

namespace PivotGridDemo
{
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class RelationalService : IRelationalService
    {
     ……
     …… 
    }

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

**Service methods in WCF Service**

First, you need to define the service methods inside IRelationalService interface, found in `IRelationalService.cs` file, created while adding WCF service to your Web Application.

{% highlight c# %}

namespace PivotGridDemo
{
    [ServiceContract]
    public interface IRelationalService
    {
        [OperationContract]
        Dictionary<string, object> InitializeGrid(string action);

        [OperationContract]
        Dictionary<string, object> FetchMembers(string action, string headerTag, string sortedHeaders, string currentReport);

        [OperationContract]
        Dictionary<string, object> Filtering(string action, string filterParams, string sortedHeaders, string currentReport);

        [OperationContract]
        Dictionary<string, object> NodeStateModified(string action, string headerTag, string dropAxis, string sortedHeaders, string filterParams, string currentReport);
        
        [OperationContract]
        Dictionary<string, object> NodeDropped(string action, string dropAxis, string headerTag, string sortedHeaders, string filterParams, string currentReport);
        
        [OperationContract]
        Dictionary<string, object> Sorting(string action, string sortedHeaders, string currentReport);
            
        [OperationContract]
        void Export(System.IO.Stream stream);
        [OperationContract]
        Dictionary<string, object> DeferUpdate(string action, string filterParams, string sortedHeaders, string currentReport);
    }
}

{% endhighlight %}

Secondly, you need to elaborate the service methods inside the main class, found in `RelationalService.svc.cs` file.

 {% highlight c# %}

namespace PivotGridDemo
{
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class RelationalService : IRelationalService
    {
        PivotGrid htmlHelper = new PivotGrid();
        JavaScriptSerializer serializer = new JavaScriptSerializer();
        Dictionary<string, object> dict = new Dictionary<string, object>();

        public Dictionary<string, object> InitializeGrid(string action)
        {
            htmlHelper.PivotReport = BindDefaultData();
            dict = htmlHelper.GetJsonData(action, ProductSales.GetSalesData());
            return dict;
        }

        public Dictionary<string, object> FetchMembers(string action, string headerTag, string sortedHeaders, string currentReport)
        {
            htmlHelper.PopulateData(currentReport);
            dict = htmlHelper.GetJsonData(action, ProductSales.GetSalesData(), headerTag, sortedHeaders);
            return dict;
        }

        public Dictionary<string, object> Filtering(string action, string filterParams, string sortedHeaders, string currentReport)
        {
            htmlHelper.PopulateData(currentReport);
            dict = htmlHelper.GetJsonData(action, ProductSales.GetSalesData(), filterParams, sortedHeaders);
            return dict;
        }

        public Dictionary<string, object> NodeStateModified(string action, string headerTag, string dropAxis, string sortedHeaders, string filterParams, string currentReport)
        {
            htmlHelper.PopulateData(currentReport);
            dict = htmlHelper.GetJsonData(action, ProductSales.GetSalesData(), headerTag, dropAxis, filterParams, sortedHeaders);
            return dict;
        }

        public Dictionary<string, object> NodeDropped(string action, string dropAxis, string headerTag, string sortedHeaders, string filterParams, string currentReport)
        {
            htmlHelper.PopulateData(currentReport);
            dict = htmlHelper.GetJsonData(action, ProductSales.GetSalesData(), dropAxis, headerTag, filterParams, sortedHeaders);
            return dict;
        }

        public Dictionary<string, object> Sorting(string action, string sortedHeaders, string currentReport)
        {
            htmlHelper.PopulateData(currentReport);
            dict = htmlHelper.GetJsonData(action, ProductSales.GetSalesData(), sortedHeaders);
            return dict;
        }
        
         public void Export(System.IO.Stream stream)
        {
            System.IO.StreamReader sReader = new System.IO.StreamReader(stream);
            string args = System.Web.HttpContext.Current.Server.UrlDecode(sReader.ReadToEnd()).Remove(0, 5);
            Dictionary<string, string> gridParams = serializer.Deserialize<Dictionary<string, string>>(args);
            htmlHelper.PopulateData(gridParams["currentReport"]);
            string fileName = "Sample";
            htmlHelper.ExportPivotGrid(ProductSales.GetSalesData(), args, fileName, System.Web.HttpContext.Current.Response);
        }
        
        public Dictionary<string, object> DeferUpdate(string action, string filterParams, string sortedHeaders, string currentReport)
        {
            htmlHelper.PopulateData(currentReport);
            dict = htmlHelper.GetJsonData(action, ProductSales.GetSalesData(), null, null, null, sortedHeaders, filterParams);
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

**Configuring Web Configuration File**

You can expose services through the properties such as binding, contract and address by using an endpoint.

1. Contract: This property indicates that the contract of the endpoint is exposing. Here you are referring to `IRelationalService` contract and hence it is `PivotGridDemo.IRelationalService`.
2. Binding: In your application, you use `webHttpBinding` to post and receive the requests and responses between the client-end and the service.
3. behaviorConfiguration: This property contains the name of the behavior to be used in the endpoint.
 
The endpointBehaviors are illustrated as follows.
 
{% highlight xaml %}

<system.serviceModel>
……
……

    <services>
      <service name="PivotGridDemo.RelationalService">
        <endpoint address="" behaviorConfiguration="PivotGridDemo.RelationalServiceAspNetAjaxBehavior"
        binding="webHttpBinding" contract="PivotGridDemo.IRelationalService" />
      </service>
    </services>
</system.serviceModel>

{% endhighlight %}
 
The endpointBehaviors contain all the behaviors for an endpoint. You can link each endpoint to the respective behavior only by using this name property.

{% highlight xaml %}

<system.serviceModel>
    <behaviors>
      <endpointBehaviors>
        <behavior name="PivotGridDemo.RelationalServiceAspNetAjaxBehavior">
          <enableWebScript />
        </behavior>
      </endpointBehaviors>
    </behaviors>
……
……
</system.serviceModel>

{% endhighlight %}

N> In this example, **“PivotGridDemo”** indicates the name and root namespace of the Web Application created in Visual Studio IDE and **“RelationalService”** indicates the name of the WCF service created.

Now, PivotGrid will be rendered with Sales Amount over a set of products across different customer geographic locations.

{% include image.html url="/js/PivotGrid/OLAP-Connectivity_images/relaionalwebapi.png" %}

