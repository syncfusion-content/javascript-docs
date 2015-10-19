---
layout: post
title: Getting-Started
description: getting started
platform: js
control: PivotGrid
documentation: ug
---

# Getting Started

This section briefly explains how you can create a **PivotGrid** in your application with **Essential JavaScript.** The first section of the document explains about creating an application with PivotGrid using OLAP datasource and later using Relational datasource briefly.

#OLAP

##Create an application with PivotGrid using OLAP datasource

This section illustrates how to add and configure the PivotGrid component in an application with AdventureWorks Cycle cube to assess the Internet Sales Amount over a period of fiscal years across different customer geographic locations."
 

![](/js/PivotGrid/Getting-Started_images/Getting-Started_img2.png) 
                                                                                   
Open Visual Studio and create a new project by clicking **New Project**. Select the **Web category**, and then select the **ASP.NET Empty Web Application template** and then click **OK**. The following screenshot displays the **Project Creation Wizard**:

![](/js/PivotGrid/Getting-Started_images/Getting-Started_img3.png) 

##Create HTML Page

To create a new web form in the application, right-click on the project and select Add.

![](/js/PivotGrid/Getting-Started_images/Getting-Started_img4.png) 

Click **New Item** and select **HTML Page** from the listed templates. Name the page **default.html** and click **OK**.
After clicking **OK**, the referred assemblies look as follows.

![](/js/PivotGrid/Getting-Started_images/Getting-Started_img5.png) 
    
##Add References, Scripts, Styles and Control in HTML page

###Add References

* In the **Solution Explorer**, right click the References folder and then click **Add Reference**.
![](/js/PivotGrid/Getting-Started_images/Getting-Started_img6.png) 
![](/js/PivotGrid/Getting-Started_images/Getting-Started_img7.png) 
* Select the following assemblies: Microsoft.AnalysisServices.AdomdClient.dll, Syncfusion.Compression.Base.dll, Syncfusion.Linq.Base.dll, Syncfusion.EJ.dll, Syncfusion.EJ.Olap.dll,Syncfusion.PivotAnalysis.Base.dll, Syncfusion.XlsIO.Base.dll, Syncfusion.Pdf.Base.dll, Syncfusion.DocIO.Base.dll and Syncfusion.Olap.Base.dll. 
* Click OK.

###Add Scripts and Styles

Add the script files and CSS files in the **head** tag of the **default.html** page.

N>  Use the following code example when adding scripts and styles.


{% highlight html %}

<link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
<script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"> </script>
<script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js" type="text/javascript"> </script>
<script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"> </script>

{% endhighlight %}

###Add Control in HTML page

Add the following code example inside the &lt;body&gt; tag in the default.html page.

{% highlight html %}

<div>
    <!--Create a <div> tag which acts as a container for ejPivotGrid widget.-->
    <div id="PivotGrid" style="height: 350px; width: 100%; overflow: auto">
    </div>
    <script type="text/javascript">
        //Set property and initializing ejPivotGrid widget.
        $(function() {
            $("#PivotGrid").ejPivotGrid({
                url: "/wcf/PivotGridService.svc"
            });
        });
    </script>
</div>

{% endhighlight %}

##Add WCF Service for PivotGrid

###Create WCF Services

Right-click the project and select Add > New Folder. Name the folder as wcf. Let the folder name "wcf" be in lower case.

![](/js/PivotGrid/Getting-Started_images/Getting-Started_img8.png) 

Now, right-click the wcf folder created and select Add > New Item.  

![](/js/PivotGrid/Getting-Started_images/Getting-Started_img9.png) 

In the **Add New Item** window, select **WCF Service** and name it as **PivotGridService.svc**. Click **Add**.

![](/js/PivotGrid/Getting-Started_images/Getting-Started_img10.png) 

###Add service methods inside Interface

Add the following code example in the `IPivotGridService` interface available in **IPivotGridService.cs** file.

{% highlight c# %}

[ServiceContract(SessionMode = SessionMode.Allowed)]
public interface IPivotGridService
{
   [OperationContract]
   Dictionary<string, object> InitializeGrid(string action, string gridLayout, bool enablePivotFieldList, object customObject);

   [OperationContract]
   Dictionary<string, object> DrillGrid(string action, string cellPosition, string currentReport, string headerInfo, string gridLayout, object customObject);

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
}

{% endhighlight %}

###Add Namespaces

Add the following namespaces required to implement the service methods.

{% highlight c# %}

using System;
using System.Collections.Generic;
using System.Linq;
using System.Runtime.Serialization;
using System.ServiceModel;
using System.Text;
using System.ServiceModel.Activation;
using System.Web.Script.Serialization;
using Syncfusion.Olap.Manager;
using Syncfusion.Olap.Reports;
using Syncfusion.JavaScript;
using OLAPUTILS = Syncfusion.JavaScript.Olap;

{% endhighlight %}

###Create Class in Service file

You can create the `PivotGridService class` to implement the service methods. You can inherit the class from the `IPivotGridService interface` that is created automatically when adding any new service.

{% highlight c# %}

namespace WebApplication2.wcf
{
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class PivotGridService : IPivotGridService
    {        
    }
}

{% endhighlight %}

###Implement Service Methods

You can add the following methods to the service that are invoked for any server-side operations to be performed in `PivotGrid`.

Initialize the PivotGrid helper class. 

{% highlight c# %}

PivotGrid htmlHelper = new PivotGrid();        
static string connectionString = "Data Source=http://bi.syncfusion.com/olap/msmdpump.dll; Initial Catalog=Adventure Works DW 2008 SE;";   
JavaScriptSerializer serializer = new JavaScriptSerializer();

{% endhighlight %}

Add the following relevant service methods.

{% highlight c# %}

//This method provides the required information from server-side when initializing the PivotGrid.
public Dictionary<string, object> InitializeGrid(string action, string gridLayout, bool enablePivotFieldList, object customObject)
{
   OlapDataManager DataManager = null;
   dynamic customData = serializer.Deserialize<dynamic>(customObject.ToString());
   DataManager = new OlapDataManager(connectionString);
   DataManager.SetCurrentReport(CreateOlapReport());
   return htmlHelper.GetJsonData(action, DataManager, gridLayout, enablePivotFieldList);
}

//This method provides the required information from server-side when drill up or down operation is performed in PivotGrid.
public Dictionary<string, object> DrillGrid(string action, string cellPosition, string currentReport, string headerInfo, string layout, object customObject)
{
   dynamic customData = serializer.Deserialize<dynamic>(customObject.ToString());
   OlapDataManager DataManager = new OlapDataManager(connectionString);
   DataManager = new OlapDataManager(connectionString);
   DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(currentReport));
   return htmlHelper.GetJsonData(action, connectionString, DataManager, cellPosition, headerInfo, layout);
}

//This method provides the required information from server-side when tree node is dropped in PivotTable Field List.
public Dictionary<string, object> NodeDropped(string action, string dropType, string nodeInfo, string filterParams, string currentReport)
{
   OlapDataManager DataManager = new OlapDataManager(connectionString);
   DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(currentReport));
   return htmlHelper.GetJsonData(action, DataManager, dropType, nodeInfo, filterParams, true);
}

//This method provides the required information from server-side when filtering values in PivotTable Field List.
public Dictionary<string, object> Filtering(string action, string filterParams, string currentReport)
{
   OlapDataManager DataManager = new OlapDataManager(connectionString);
   DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(currentReport));
   return htmlHelper.GetJsonData(action, DataManager, null, filterParams);
}

//This method provides the required information from server-side when opening the editor in PivotTable Field List.
public Dictionary<string, object> FetchMembers(string action, string headerTag, string currentReport)
{
   OlapDataManager DataManager = new OlapDataManager(connectionString);
   DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(currentReport));
   return htmlHelper.GetJsonData(action, DataManager, null, headerTag);
}

//This method provides the required information from server-side when paging is done in PivotGrid.
public Dictionary<string, object> Paging(string action, string pagingInfo, string currentReport, string gridLayout, object customObject)
{
   OlapDataManager DataManager = new OlapDataManager(connectionString);
   DataManager.SetCurrentReport(htmlHelper.SetPaging(currentReport, pagingInfo));
   return htmlHelper.GetJsonData(action, DataManager, gridLayout);
}

//This method provides the required information from server-side when removing the split button from PivotTable Field List.
public Dictionary<string, object> RemoveButton(string action, string headerInfo, string currentReport)
{
   OlapDataManager DataManager = new OlapDataManager(connectionString);
   DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(currentReport));
   return htmlHelper.GetJsonData(action, DataManager, null, headerInfo);
}

//This method provides the required information from server-side when expanding member in member editor.
public Dictionary<string, object> MemberExpanded(string action, bool checkedStatus, string parentNode, string tag, string cubeName, string currentReport)
{
   OlapDataManager DataManager = new OlapDataManager(connectionString);
   if (!string.IsNullOrEmpty(currentReport))
      DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(currentReport));
   return htmlHelper.GetJsonData(action, DataManager, checkedStatus, parentNode, tag, cubeName);
}

//This method export PivotGrid to Excel, Word, CSV and PDF.
 public void Export(System.IO.Stream stream)
 {
    System.IO.StreamReader sReader = new System.IO.StreamReader(stream);
    string args = System.Web.HttpContext.Current.Server.UrlDecode(sReader.ReadToEnd());
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    string fileName = "Sample";
    htmlHelper.ExportPivotGrid(DataManager, args, fileName, System.Web.HttpContext.Current.Response);
 }
 
//This method carries the information about the default report that is rendered within PivotGrid initially.
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

{% endhighlight %}

###Configure Web.Config

* You can expose services through the properties such as binding, contract and address using an endpoint.  

   1. **Contract:** This property indicates that the contract of the endpoint is exposed. Here you must refer **IPivotGridService** contract, hence it is `WebApplication2.wcf.IPivotGridService`.
   2. **Binding:** In your application, you use `webHttpBinding` to post and receive the requests and responses between the client-end and the service.
   3. **behaviorConfiguration:** This property contains the name of the behavior to be used in the endpoint. **endpointBehaviors** are illustrated as follows.
   
{% highlight xml %}

<services>
   <service name="WebApplication2.wcf.PivotGridService">
      <endpoint address="" behaviorConfiguration="WebApplication2.wcf.PivotGridServiceAspNetAjaxBehavior"
      binding="webHttpBinding" contract="WebApplication2.wcf.IPivotGridService" />
   </service>
</services>

{% endhighlight %}

* The `endpointBehaviors` contains all the behaviors for an endpoint. You can link each endpoint to the respective behavior only by using the name property. In the following code example, `WebApplication2.wcf.PivotGridServiceAspNetAjaxBehavior` refers to the PivotGridService class under the namespace WebApplication2.wcf in PivotGridService.svc.cs file which is the appropriate behavior for the endpoint. 

{% highlight xml %}

<endpointBehaviors>
   <behavior name="WebApplication2.PivotGridServiceAspNetAjaxBehavior">
      <enableWebScript />
   </behavior>
</endpointBehaviors>

{% endhighlight %} 

N>  In this example, “WebApplication2.wcf” indicates the namespace in the WCF Service and “PivotGridService” indicates the class name in the WCF Service.

#Relational

##Create an application with PivotGrid using Relational datasource

This section explains how you can configure the **PivotGrid** component in an application. You can also pass the required data to **PivotGrid** and customize it according to your requirements.

This example illustrates how the **PivotGrid** component tabulates the sales or revenue amount over a period of fiscal years across different locations. 

![](/js/PivotGrid/Getting-Started_images/Getting-Started_img12.png) 

Open **Visual Studio** and create a new project by clicking **New Project**. Select the **Web category**, and then select the **ASP.NET Empty Web Application template** and then click **OK**.  The following screenshot displays the **Project Creation Wizard**:

![](/js/PivotGrid/Getting-Started_images/Getting-Started_img13.png) 

##Create HTML Page

To create new web form in the application, right-click on the project and select Add.

![](/js/PivotGrid/Getting-Started_images/Getting-Started_img14.png) 

Click New Item and select HTML Page from the listed templates. Name the page default.html and click OK.
After clicking OK, the referred assemblies appear as follows.

![](/js/PivotGrid/Getting-Started_images/Getting-Started_img15.png) 

##Add References, Scripts, Styles and Control in HTML page

###Add References

* In the Solution Explorer, right click the References folder and then click Add Reference.
![](/js/PivotGrid/Getting-Started_images/Getting-Started_img16.png) 
![](/js/PivotGrid/Getting-Started_images/Getting-Started_img17.png) 
* Select the following assemblies: Microsoft.AnalysisServices.AdomdClient.dll, Syncfusion.Compression.Base.dll, Syncfusion.Linq.Base.dll, Syncfusion.EJ.dll, Syncfusion.EJ.Olap.dll,Syncfusion.PivotAnalysis.Base and Syncfusion.Olap.Base.dll 
* Click OK.    

###Add Scripts and Styles

Add the script files and CSS files in the **title** tag of the **default.html** page.

N>  Use the following code example while adding scripts and styles.

{% highlight html %}
<link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
<script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js">
</script>
<script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js" type="text/javascript">
</script>
<script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js">
</script>
{% endhighlight %}

###Add Control in HTML page

Add the following code example inside the **&lt;body&gt;** tag in the **default.html** page.

{% highlight html %}

<div>
    <!--Create a <div> tag which acts as a container for ejPivotGrid widget.-->
    <div id="PivotGrid" style="height: 350px; width: 100%; overflow: auto">
    </div>
    <script type="text/javascript">
        //Set property and initializing ejPivotGrid widget.
        $(function() {
            $("#PivotGrid").ejPivotGrid({
                url: "/wcf/PivotGridService.svc"
            });
        });
    </script>
</div>

{% endhighlight %}

##Add WCF Service for PivotGrid

###Create WCF Services

Right-click the project and select Add > New Folder. Name the folder as wcf. Let the folder name "wcf" be in lower case.

![](/js/PivotGrid/Getting-Started_images/Getting-Started_img18.png) 

Now, right-click the wcf folder created and select Add > New Item.  

![](/js/PivotGrid/Getting-Started_images/Getting-Started_img19.png) 

In the Add New Item window, select WCF Service and name it as PivotGridService.svc. Click Add.

![](/js/PivotGrid/Getting-Started_images/Getting-Started_img20.png) 

###Add service methods inside Interface

Add the following code example inside the **IPivotGridService** interface available in **IPivotGridService.cs** file.

{% highlight c# %}

[ServiceContract]
public interface IPivotGridService
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
   Dictionary < string, object > Sorting(string action, string sortedHeaders, string currentReport);       
}

{% endhighlight %}

###Add Namespaces

Add the following necessary namespaces required to implement the **service** methods.

{% highlight c# %}

using System;
using System.Collections.Generic;
using System.Linq;
using System.Runtime.Serialization;
using System.ServiceModel;
using System.Text;
using System.ServiceModel.Activation;
using System.Web.Script.Serialization;
using Syncfusion.Olap.Manager;
using Syncfusion.Olap.Reports;
using Syncfusion.JavaScript;
using Syncfusion.PivotAnalysis.Base;

{% endhighlight %}

###Create Class in Service file

You can create the `PivotGridService` class to implement the **service** methods. You can inherit the class from the `IPivotGridService` interface that is created automatically when adding any new service.

{% highlight c# %}

namespace WebApplication2.wcf
{
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class PivotGridService : IPivotGridService
    {        
    }
}

{% endhighlight %}

###Implement Service Methods

You can add the following methods to the service that are invoked for any server-side operations to be performed in PivotGrid.

Initialize the PivotGrid helper class. 

{% highlight c# %}

PivotGrid htmlHelper = new PivotGrid();
JavaScriptSerializer serializer = new JavaScriptSerializer();
Dictionary<string, object> dict = new Dictionary<string, object>()>;

{% endhighlight %}

Add the following relevant **service** methods.

{% highlight c# %}

//This method provides the required information from server-side when initializing the PivotGrid.
public Dictionary<string, object> InitializeGrid(string action)
{
   htmlHelper.PivotReport = BindDefaultData();
   dict = htmlHelper.GetJsonData(action, ProductSales.GetSalesData());
   return dict;
}

//This method provides the required information from server-side when node state is modified in PivotTable Field List.
public Dictionary<string, object> NodeStateModified(string action, string headerTag, string dropAxis, string sortedHeaders, string filterParams, string currentReport)
{
   htmlHelper.PopulateData(currentReport);
   dict = htmlHelper.GetJsonData(action, ProductSales.GetSalesData(), headerTag, dropAxis, filterParams, sortedHeaders);
   return dict;
}

//This method provides the required information from server-side when tree node is dropped in PivotTable Field List.
public Dictionary<string, object> NodeDropped(string action, string dropAxis, string headerTag, string sortedHeaders, string filterParams, string currentReport)
{
   htmlHelper.PopulateData(currentReport);
   dict = htmlHelper.GetJsonData(action, ProductSales.GetSalesData(), dropAxis, headerTag, filterParams, sortedHeaders);
   return dict;
}

//This method provides the required information from server-side when filtering values in PivotTable Field List.
public Dictionary<string, object> Filtering(string action, string filterParams, string sortedHeaders, string currentReport)
{
   htmlHelper.PopulateData(currentReport);
   dict = htmlHelper.GetJsonData(action, ProductSales.GetSalesData(), filterParams, sortedHeaders);
   return dict;
}

//This method provides the required information from server-side when opening the editor in PivotTable Field List.
public Dictionary<string, object> FetchMembers(string action, string headerTag, string sortedHeaders, string currentReport)
{
   htmlHelper.PopulateData(currentReport);
   dict = htmlHelper.GetJsonData(action, ProductSales.GetSalesData(), headerTag, sortedHeaders);
   return dict;
}

//This method provides the required information from server-side when sorting values in PivotTable Field List.
public Dictionary < string, object> Sorting(string action, string sortedHeaders, string currentReport) 
{
	htmlHelper.PopulateData(currentReport);
	dict = htmlHelper.GetJsonData(action, ProductSales.GetSalesData(), sortedHeaders);
	return dict;
}

//This method carries the information about the default report that is rendered within PivotGrid initially.
private PivotReport BindDefaultData()
{
    PivotReport pivotSetting = new PivotReport();
    pivotSetting.PivotRows.Add(new PivotItem { FieldMappingName = "Date", FieldHeader = "Date", TotalHeader = "Total" });
    pivotSetting.PivotColumns.Add(new PivotItem { FieldMappingName = "Country", FieldHeader = "Country", TotalHeader = "Total", ShowSubTotal = false });
    pivotSetting.PivotCalculations.Add(new PivotComputationInfo { CalculationName = "Amount", Description = "Amount", FieldHeader = "Amount", FieldName = "Amount", Format = "C", SummaryType = Syncfusion.PivotAnalysis.Base.SummaryType.DoubleTotalSum });
    return pivotSetting;
}

{% endhighlight %}


{% highlight c# %}

namespace WebApplication2.wcf
{
   //This collection is bound with PivotGrid control.
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

###Configure Web.Config 

* You can expose services through the properties such as binding, contract and address using an endpoint.

   1. **Contract:** This property indicates that the contract of the endpoint is exposed. Here you are referring to the **IPivotGridService** contract hence it is `WebApplication2.wcf.IPivotGridService`.
   2. **Binding:** In your application, use `webHttpBinding` to post and receive the requests and responses between the client-end and the service.
   3. **behaviorConfiguration:** This property contains the name of the behavior to be used in the endpoint. **endpointBehaviors** are illustrated as follows.
   
{% highlight xml %}   

<services>
   <service name="WebApplication2.wcf.PivotGridService">
      <endpoint address="" behaviorConfiguration="WebApplication2.wcf.PivotGridServiceAspNetAjaxBehavior"
      binding="webHttpBinding" contract="WebApplication2.wcf.IPivotGridService" />
   </service>
</services>

{% endhighlight %}

* The `endpointBehaviors` contain all the behaviors for an endpoint. You can link each endpoint to the respective behavior only using this `name` property. In the following code example, `WebApplication2.wcf.PivotGridServiceAspNetAjaxBehavior` refers to the PivotGridService class under the namespace WebApplication2.wcf in PivotGridService.svc.cs file which is the appropriate behavior for the endpoint. 

{% highlight xml %}  

<endpointBehaviors>
   <behavior name="WebApplication2.wcf.PivotGridServiceAspNetAjaxBehavior">
      <enableWebScript />
   </behavior>
</endpointBehaviors>

{% endhighlight %}

N>  In this example, “WebApplication2.wcf” indicates the namespace in the WCF Service and “PivotGridService” indicates the class name in the WCF Service.
