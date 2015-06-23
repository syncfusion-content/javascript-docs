---
layout: post
title: Getting-Started
description: getting started
platform: js
control: PivotGrid
documentation: ug
---

# Getting Started

This section explains briefly about how to create a **PivotGrid** in your application with **JavaScript.** First section of the document covers on creating an application with PivotGrid using OLAP datasource and later using Relational datasource briefly.

#OLAP

##Create an application with PivotGrid using OLAP datasource

This section encompasses how to configure the **PivotGrid** component in an application. You can also pass the required data to **PivotGrid** and customize it according to your requirements.

This example illustrates how the **PivotGrid** component tabulates the Internet Sales Amount over a period of fiscal years across different customer geographic locations. 

{% include image.html url="/js/PivotGrid/Getting-Started_images/Getting-Started_img2.png" Caption="PivotGrid"%}
                                                                                   
Open Visual Studio and create a new project by clicking **New Project**. Select the **Web category**, and then select the **ASP.NET Empty Web Application template** and then click **OK**. The following screenshot displays the **Project Creation Wizard**:

{% include image.html url="/js/PivotGrid/Getting-Started_images/Getting-Started_img3.png" Caption="Project Creation Wizard"%}

##Create HTML Page

To create new web form in the application, right-click on the project and select Add.

{% include image.html url="/js/PivotGrid/Getting-Started_images/Getting-Started_img4.png" Caption="Creating New Web Form"%}

Click **New Item** and select **HTML Page** from the listed templates. Name the page **default.html** and click **OK**.
After clicking **OK**, the referred assemblies look as follows.

{% include image.html url="/js/PivotGrid/Getting-Started_images/Getting-Started_img5.png" Caption="References"%}
    
##Add References, Scripts, Styles and Control in HTML page

###Add References

* In the **Solution Explorer**, right click the References folder and then click **Add Reference**.

{% include image.html url="/js/PivotGrid/Getting-Started_images/Getting-Started_img6.png" Caption="Adding References"%}

{% include image.html url="/js/PivotGrid/Getting-Started_images/Getting-Started_img7.png" Caption="Reference Manager Dialog"%}

* Select the following assemblies: Microsoft.AnalysisServices.AdomdClient.dll, Syncfusion.Core.dll, Syncfusion.Compression.Base.dll, Syncfusion.Linq.Base.dll, Syncfusion.EJ.dll, Syncfusion.EJ.Olap.dll, Syncfusion.XlsIO.Base.dll, Syncfusion.PivotAnalysis.Base.dll and Syncfusion.Olap.Base.dll.

* Click OK.

###Add Scripts and Styles

Add the script files and CSS files in the **title** tag of the **default.html** page.

> _**Note:** Use the following code example when adding scripts and styles._


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
    //Create a <div> tag which acts as a container for ejPivotGrid widget.
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

Right-click the project and select Add > New Folder. Name the folder as WCF.

{% include image.html url="/js/PivotGrid/Getting-Started_images/Getting-Started_img8.png" Caption="Adding and Naming the WCF Folder"%}

Now, right-click the WCF folder created and select Add > New Item.  

{% include image.html url="/js/PivotGrid/Getting-Started_images/Getting-Started_img9.png" Caption="Adding New Item to Folder"%}

In the **Add New Item** window, select **WCF Service** and name it as **PivotGridService.svc**. Click **Add**.

{% include image.html url="/js/PivotGrid/Getting-Started_images/Getting-Started_img10.png" Caption="Add New Item Dialog"%}

###Add service methods inside Interface

Add the following code example in the **IPivotGridService** interface available in **IPivotGridService.cs** file.

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
    }


{% endhighlight %}

###Add Namespaces

Add the following necessary namespaces required to implement the service methods.

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

You can create the **PivotGridService class** to implement the service methods. You can inherit the class from the **IPivotGridService interface** that is created automatically when adding any new service.

{% highlight c# %}

namespace WebApplication2
{
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class PivotGridService : IPivotGridService
    {        
    }
}

{% endhighlight %}

###Implement Service Methods

You can add the following methods to the service that are invoked for any server-side operations to be performed in **PivotGrid**.

Initialize the **PivotGrid helper class**. 

{% highlight c# %}

        PivotGrid htmlHelper = new PivotGrid();        
        static string connectionString = "Data Source=http://bi.syncfusion.com/olap/msmdpump.dll; Initial Catalog=Adventure Works DW 2008 SE;";   
        JavaScriptSerializer serializer = new JavaScriptSerializer();

{% endhighlight %}

Add the following relevant **service** methods.

{% highlight c# %}

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

        public Dictionary<string, object> MemberExpanded(string action, bool     checkedStatus, string parentNode, string tag, string cubeName, string currentReport)
        {
            OlapDataManager DataManager = new OlapDataManager(connectionString);
            if (!string.IsNullOrEmpty(currentReport))
                DataManager.SetCurrentReport(OLAPUTILS.Utils.DeserializeOlapReport(currentReport));
            return htmlHelper.GetJsonData(action, DataManager, checkedStatus, parentNode, tag, cubeName);
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

{% endhighlight %}

###Configure Web.Config

* You can expose services through the properties such as binding, contract and address etc. using an endpoint. In your application the service name is "WebApplication2.PivotGridService" where "PivotGridService" is the service class name and “WebApplication2" is the namespace name where service     class appears. The following are the properties that meet the appropriate endpoint.  

   1. **Contract:** This property indicates that the contract of the endpoint is exposing. Here you are referring **IPivotGridService** contract and hence it is "**WebApplication2.IPivotGridService**".

   2. **Binding:** In your application, you use **webHttpBinding** to post and receive the requests and responses between the client-end and the service.

   3. **behaviorConfiguration:** This property contains the name of the behavior to be used in the endpoint. **endpointBehaviors** are illustrated as follows.
   
{% highlight xml %}

<services>

      <service name="WebApplication2.PivotGridService">

        <endpoint address="" behaviorConfiguration="WebApplication2.PivotGridServiceAspNetAjaxBehavior"

          binding="webHttpBinding" contract="WebApplication2.IPivotGridService" />

      </service>

</services>

{% endhighlight %}

* The endpointBehaviors contain all the behaviors for an endpoint. You can link each endpoint to the respective behavior only using this name property. In the following code example, "WebApplication2.PivotGridServiceAspNetAjaxBehavior" refers to the PivotGridService class under the namespace WebApplication2 in PivotGridService.svc.cs file that is the appropriate behavior for the endpoint. 

{% highlight xml %}

  <endpointBehaviors>

       <behavior name="WebApplication2.PivotGridServiceAspNetAjaxBehavior">

          <enableWebScript />

        </behavior>

</endpointBehaviors>

{% endhighlight %} 

> _**Note:** In this example, “WebApplication2” indicates the name of the project and “PivotGridService” indicates the name of the WCF service created._

#Relational

##Create an application with PivotGrid using Relational datasource

This section encompasses how to configure the **PivotGrid** component in an application. You can also pass the required data to **PivotGrid** and customize it according to your requirements.

This example illustrates how the **PivotGrid** component tabulates the sales/revenue amount over a period of fiscal years across different geographic locations. 

{% include image.html url="/js/PivotGrid/Getting-Started_images/Getting-Started_img12.png" Caption="PivotGrid"%}

Open **Visual Studio** and create a new project by clicking **New Project**. Select the **Web category**, and then select the **ASP.NET Empty Web Application template** and then click **OK**.  The following screen shot displays the **Project Creation Wizard**:

{% include image.html url="/js/PivotGrid/Getting-Started_images/Getting-Started_img13.png" Caption="Project Creation Wizard"%}

##Create HTML Page

To create new web form in the application, right-click on the project and select Add.

{% include image.html url="/js/PivotGrid/Getting-Started_images/Getting-Started_img14.png" Caption="Creating New Web Form"%}

Click New Item and select HTML Page from the listed templates. Name the page default.html and click OK.
After clicking OK, the referred assemblies look as follows.

{% include image.html url="/js/PivotGrid/Getting-Started_images/Getting-Started_img15.png" Caption="References"%}

##Add References, Scripts, Styles and Control in HTML page

###Add References

* In the Solution Explorer, right click the References folder and then click Add Reference.

{% include image.html url="/js/PivotGrid/Getting-Started_images/Getting-Started_img16.png" Caption="Adding References"%}

{% include image.html url="/js/PivotGrid/Getting-Started_images/Getting-Started_img17.png" Caption="Reference Manager Dialog"%}

* Select the following assemblies: Microsoft.AnalysisServices.AdomdClient.dll, Syncfusion.Core.dll, Syncfusion.Linq.Base.dll, Syncfusion.EJ.dll, Syncfusion.EJ.Olap.dll, Syncfusion.XlsIO.Base.dll, Syncfusion.PivotAnalysis.Base.dll and Syncfusion.Olap.Base.dll.

* Click OK.    

###Add Scripts and Styles

Add the script files and CSS files in the **title** tag of the **default.html** page.

> _**Note:** Use the following code sample when adding scripts and styles._

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

Add the following code sample inside the **&lt;body&gt;** tag in the **default.html** page.

{% highlight html %}

<div>
    //Create a <div> tag which acts as a container for ejPivotGrid widget.
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

Right-click the project and select Add > New Folder. Name the folder as WCF.

{% include image.html url="/js/PivotGrid/Getting-Started_images/Getting-Started_img18.png" Caption="Adding and Naming the WCF Folder"%}

Now, right-click the WCF folder created and select Add > New Item.  

{% include image.html url="/js/PivotGrid/Getting-Started_images/Getting-Started_img19.png" Caption="Adding New Item to Folder"%}

In the Add New Item window, select WCF Service and name it as PivotGridService.svc. Click Add.

{% include image.html url="/js/PivotGrid/Getting-Started_images/Getting-Started_img20.png" Caption="Add New Item Dialog"%}

###Add service methods inside Interface

Add the following code sample inside the **IPivotGridService** interface available in **IPivotGridService.cs** file.

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

You can create the **PivotGridService** class to implement the **service** methods. You can inherit the class from the **IPivotGridService** interface that is created automatically when adding any new service.

{% highlight c# %}

namespace WebApplication2
{
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class PivotGridService : IPivotGridService
    {        
    }
}

{% endhighlight %}

###Implement Service Methods

You can add the following methods to the service that are invoked for any server-side operations to be performed in PivotGrid.

Initialize the **PivotGrid helper class**. 

{% highlight c# %}

PivotGrid htmlHelper = new PivotGrid();

JavaScriptSerializer serializer = new JavaScriptSerializer();
  
Dictionary<string, object> dict = new Dictionary<string, object>()>;

{% endhighlight %}

Add the following relevant **service** methods.

{% highlight c# %}

       //This method provides the required information from the server side when initializing the PivotGrid.
 
        public Dictionary<string, object> InitializeGrid(string action)
        {
            htmlHelper.PivotReport = BindDefaultData();
            dict = htmlHelper.GetJsonData(action, ProductSales.GetSalesData());
            return dict;
        }
        
        //This method provides the required information from the server side when node state is modified in PivotTable Field List.
        
        public Dictionary<string, object> NodeStateModified(string action, string headerTag, string dropAxis, string sortedHeaders, string filterParams, string currentReport)
        {
            htmlHelper.PopulateData(currentReport);
            dict = htmlHelper.GetJsonData(action, ProductSales.GetSalesData(), headerTag, dropAxis, filterParams, sortedHeaders);
            return dict;
        }
        
        //This method provides the required information from the server side when tree node is dropped in PivotTable Field List.

        public Dictionary<string, object> NodeDropped(string action, string dropAxis, string headerTag, string sortedHeaders, string filterParams, string currentReport)
        {
            htmlHelper.PopulateData(currentReport);
            dict = htmlHelper.GetJsonData(action, ProductSales.GetSalesData(), dropAxis, headerTag, filterParams, sortedHeaders);
            return dict;
        }
         
        //This method provides the required information from the server side when filtering values in PivotTable Field List.

        public Dictionary<string, object> Filtering(string action, string filterParams, string sortedHeaders, string currentReport)
        {
            htmlHelper.PopulateData(currentReport);
            dict = htmlHelper.GetJsonData(action, ProductSales.GetSalesData(), filterParams, sortedHeaders);
            return dict;
        }
        
       //This method provides the required information from the server side when opening the editor in PivotTable Field List.

        public Dictionary<string, object> FetchMembers(string action, string headerTag, string sortedHeaders, string currentReport)
        {
            htmlHelper.PopulateData(currentReport);
            dict = htmlHelper.GetJsonData(action, ProductSales.GetSalesData(), headerTag, sortedHeaders);
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

namespace WebApplication2
{
   //This collection is bounded with PivotGrid control.
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

* You can expose services through the properties such as binding, contract and address etc. using an endpoint. In your application the service name is "WebApplication2.PivotGridService" where "PivotGridService" is the service class name and “WebApplication2" is the namespace name where service class appears.The following are the properties that meet the appropriate endpoint.  

   1. **Contract:** This property indicates that the contract of the endpoint is exposing. Here you are referring **IPivotGridService** contract and hence it is "**WebApplication2.IPivotGridService**".

   2. **Binding:** In your application, use **webHttpBinding** to post and receive the requests and responses between the client-end and the service.

   3. **behaviorConfiguration:** This property contains the name of the behavior to be used in the endpoint. **endpointBehaviors** are illustrated as follows.
   
{% highlight xml %}   

<services>

<service name="WebApplication2.PivotGridService">

<endpoint address="" behaviorConfiguration="WebApplication2.PivotGridServiceAspNetAjaxBehavior"

binding="webHttpBinding" contract="WebApplication2.IPivotGridService" />

</service>

</services>

{% endhighlight %}

* The endpointBehaviors contain all the behaviors for an endpoint. You can link each endpoint to the respective behavior only using this name property. In the following code sample, "WebApplication2.PivotGridServiceAspNetAjaxBehavior" refers to the PivotGridService class under the namespace WebApplication2 in PivotGridService.svc.cs file that is the appropriate behavior for the endpoint. 

{% highlight xml %}  

<endpointBehaviors>
        
<behavior name="WebApplication2.PivotGridServiceAspNetAjaxBehavior">

<enableWebScript />

</behavior>

</endpointBehaviors>

{% endhighlight %}

> _**Note:** In this example, “WebApplication2” indicates the name of the project and “PivotGridService” indicates the name of the WCF service created._
