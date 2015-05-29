---
layout: post
title: 13-concepts-and-features
description: 1.3 concepts and features
platform: js
control: ReportViewer
documentation: ug
---

## 1.3 Concepts and Features

### 1.3.1 Report Controller

The **ReportViewer** uses **Web API** services to process the report file, process the request from control, and to return the processed data to control. The **Syncfusion.EJ.ReportViewer** assembly has helper APIs to define the service actions and process the service requests. 

**IReportController**

The interface **IReportController** has the declaration of action methods that is defined in **WebApi** Controller for processing the RDL/RDLC files and for processing request from **ReportViewer** control. The **IReportController** has the following action methods declaration. 



_Report Controller methods_

<table>
<tr>
<td>
<b>Methods</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
GetResource</td><td>
Action (HttpGet) method for getting resource for report. </td></tr>
<tr>
<td>
PostReportAction</td><td>
Action (HttpPost) method for posting the request for report process. </td></tr>
<tr>
<td>
OnInitReportOptions</td><td>
Report initialization method that is triggered when report begins to be processed.</td></tr>
<tr>
<td>
OnReportLoaded</td><td>
Report loaded method that is triggered when report and sub report begin loading.</td></tr>
</table>
**ReportHelper**

The class **ReportHelper** contains helper methods that helps process Post/Get request from **ReportViewer** control and returns the response to **ReportViewer** control. The **ReportHelper** has the following methods. 

_Report Helper methods_

<table>
<tr>
<td>
<b>Methods</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
GetResource</td><td>
Returns the report resource for the requested key.</td></tr>
<tr>
<td>
ProcessReport</td><td>
Processes the report request and returns the result.</td></tr>
</table>


{% highlight c# %}

**[C#]**

public class ReportsController : ApiController, IReportController
    {
        /// <summary>
        /// Action (HttpGet) method for getting resource for report.
        /// </summary>
        /// <param name="key">The unique key to get the required resource.</param>
        /// <param name="resourceType">The type of the requested resource.</param>
        /// <param name="isPrinting">If set to <see langword="true"/>, then the resource is generated for printing.</param>
        /// <returns>The object data.</returns>
        public object GetResource(string key, string resourceType, bool isPrinting)
        {
            //Returns the report resource for the requested key.
            return ReportHelper.GetResource(key, resourceType, isPrinting);
        }

        /// <summary>
        /// Report Initialization method that is triggered when report begin processed.
        /// </summary>
        /// <param name="reportOptions">The ReportViewer options.</param>
        public void OnInitReportOptions(ReportViewerOptions reportOptions)
        {
            throw new NotImplementedException();
        }

        /// <summary>
        /// Report loaded method that is triggered when report and sub report begins to be loaded.
        /// </summary>
        /// <param name="reportOptions">The ReportViewer options.</param>
        public void OnReportLoaded(ReportViewerOptions reportOptions)
        {
            throw new NotImplementedException();
        }

        /// <summary>
        /// Action (HttpPost) method for posting the request for report process. 
        /// </summary>
        /// <param name="jsonData">The JSON data posted for processing report.</param>
        /// <returns>The object data.</returns>
        public object PostReportAction(Dictionary<string, object> jsonData)
        {
            //Processes the report request and returns the result.
            return ReportHelper.ProcessReport(jsonData, this);
        }
    }


{% endhighlight %}



### SSRS Configuration

The **ReportViewer** has support to load RDL/RDLC reports from SSRS server. You have to set your SSRS server URL to **ReportViewer’s****reportServerUrl** property and set the relative path of RDL/RDLC file in SSRS to **ReportViewer’s****reportPath** property. 

{% highlight javascript %}

**[JS]**

$("#viewer").ejReportViewer(
                {
                    reportServiceUrl: "/api/SSRSReport",
                    processingMode: ej.ReportViewer.ProcessingMode.Remote,
                    reportPath: "/SSRSSamples2/Territory Sales New",
                    reportServerUrl: "http://76.74.153.81/ReportServer"                    
                });


{% endhighlight %}



**Network Credentials for SSRS**

The **Network credentials** can be given at **Web****API** Controller to connect the SSRS server.

{% highlight c# %}

**[CS]**

                   /// <summary>
        /// Report Initialization method that is triggered when report begins to process.
        /// </summary>
        /// <param name="reportOptions">The ReportViewer options.</param>
        public void OnInitReportOptions(ReportViewerOptions reportOptions)
        {
           //Adds SSRS Server and Database Credentials here.
            reportOptions.ReportModel.ReportServerCredential = new System.Net.NetworkCredential("ssrs", "RDLReport1");
            reportOptions.ReportModel.DataSourceCredentials.Add(new DataSourceCredentials("AdventureWorks", "ssrs1", "RDLReport1"));
        }


{% endhighlight %}



_**Note: DataSource credentials must be added to the ReportViewer for Shared DataSources that do not have credentials in the connection string and used in the SSRS Reports.**_

### Report DataSources

The **ReportViewer** has support to add data sources to **ReportViewer** for RDLC reports at runtime. You can add SQL Server, Oracle, MS Azure, XML, Business Object, and SQL Server Compact DataSources to **ReportViewer**. The **ReportViewer** has **DataSources** property that is the list of **ReportDataSource** type to add collection of **DataSources** to it. You can add **DataSources** either through **ReportViewer** model when creating **ReportViewer** control or through **Web API**.

The following code example illustrates how to add **DataSource** at control creation.

{% highlight javascript %}

**[JS]**

$("#viewer").ejReportViewer(
                    {
                      reportServiceUrl: "/api/ReportApi",
                      processingMode: ej.ReportViewer.ProcessingMode.Local,
                      reportPath: 'Product List.rdlc',
                           dataSources: [{
                value: [
                           {
                               ProductName: "Baked Chicken and Cheese", OrderId: "323B60", Price: 55, Category: "Non-Veg", Ingredients: "Grilled chicken, Corn and Olives.", ProductImage: ""
                           },
                           {
                               ProductName: "Chicken Delite", OrderId: "323B61", Price: 100, Category: "Non-Veg", Ingredients: "Cheese, Chicken chunks, Onions & Pineapple chunks.", ProductImage: ""
                           },
                           {
                               ProductName: "Chicken Tikka", OrderId: "323B62", Price: 64, Category: "Non-Veg", Ingredients: "Onions, Grilled chicken, Chicken salami & Tomatoes.", ProductImage: ""
                           }
               ],
                name: "list"
            }]
                    });		        


{% endhighlight %}

 The following code example illustrates how to add **DataSource** in **Web API**.

{% highlight c# %}

**[C#]**

public class ReportsController : ApiController, IReportController
    {
        /// <summary>
        /// Report loaded method that is triggered when report and sub report are loaded.
        /// </summary>
        /// <param name="reportOptions">The ReportViewer options.</param>
        public void OnReportLoaded(ReportViewerOptions reportOptions)
        {
            //Adds data sources to report model.
            reportOptions.ReportModel.DataSources.Clear();
            ProductList productList = new ProductList();
            reportOptions.ReportModel.DataSources.Add(new ReportDataSource { Name = "list", Value = productList.GetData() });            
        }


    }

public class ProductList
    {
        public string ProductName { get; set; }
        public string OrderId { get; set; }
        public double Price { get; set; }
        public string Category { get; set; }
        public string Ingredients { get; set; }
        public string ProductImage { get; set; }

        public IList GetData()
        {
            List<ProductList> dataList = new List<ProductList>();
            ProductList data = null;
            data = new ProductList() { ProductName = "Baked Chicken and Cheese", OrderId = "323B60", Price = 55, Category = "Non-Veg", Ingredients = "grilled chicken, corn and olives.", ProductImage = "" };
            dataList.Add(data);
            data = new ProductList() { ProductName = "Chicken Delite", OrderId = "323B61", Price = 100, Category = "Non-Veg", Ingredients = "cheese, chicken chunks, onions & pineapple chunks.", ProductImage = "" };
            dataList.Add(data);
            data = new ProductList() { ProductName = "Chicken Tikka", OrderId = "323B62", Price = 64, Category = "Non-Veg", Ingredients = "onions, grilled chicken, chicken salami & tomatoes.", ProductImage = "" };
            dataList.Add(data);
            return dataList;
        }
    }


{% endhighlight %}

**DataSource Credentials**

The **DataSource** credentials can be given at **Web API** Controller to connect data source.

{% highlight c# %}

**[CS]**

                   /// <summary>
        /// Report Initialization method that is triggered when report begins to process.
        /// </summary>
        /// <param name="reportOptions">The ReportViewer options.</param>
        public void OnInitReportOptions(ReportViewerOptions reportOptions)
        {
           //Adds SSRS Server and Database Credentials here.
            reportOptions.ReportModel.ReportServerCredential = new System.Net.NetworkCredential("ssrs", "RDLReport1");
            reportOptions.ReportModel.DataSourceCredentials.Add(new DataSourceCredentials("AdventureWorks", "ssrs1", "RDLReport1"));
        }


{% endhighlight %}



### Report Parameters

The **ReportViewer** has support to add report parameters to **ReportViewer** at runtime. The **ReportViewer** has **Parameters** property that is the list of **ReportParameter** type to add collection of report parameters to it. You can add report parameters either through **ReportViewer** model when creating **ReportViewer** control or through **Web API**.

The following code example illustrates how to add **ReportParameter** at control creation.



{% highlight javascript %}

**[JS]**

$("#viewer").ejReportViewer(
                {
                    reportServiceUrl: "/api/SSRSReport",
                    processingMode: ej.ReportViewer.ProcessingMode.Remote,
                    reportPath: "~/InvoiceTemplate",                    parameters: [{ name: 'InvoiceID', labels: ['InvoiceID'], values: [10250], nullable: false }]
                });


{% endhighlight %}

The following code example illustrates how to add **ReportParameter** in **Web API.**

{% highlight c# %}

**[C#]**

public class ReportsController : ApiController, IReportController
    {
        /// <summary>
        /// Report Initialization method that is triggered when report begins to be processed.
        /// </summary>
        /// <param name="reportOptions">The ReportViewer options.</param>
        public void OnInitReportOptions(ReportViewerOptions reportOptions)
        {
            List<ReportParameter> parameters = new List<ReportParameter>();
            parameters.Add(new ReportParameter() { Name = "InvoiceID", Labels = new List<string>() { "InvoiceID" }, Values = new List<string>() { "10250" } });
            reportOptions.ReportModel.Parameters = parameters;
            throw new NotImplementedException();
        }        
    }


{% endhighlight %}



### Toolbar Customization

The **ReportViewer** has an option to show or hide items in the **toolbar**. To customize the **toolbar** items, use the **ReportViewer’s****ToolbarSettings** property. The **toolbar** template can also be customized by specifying custom template to **ReportViewer****toolbar**.

{% highlight javascript %}

**[JS]**

$("#viewer").ejReportViewer(
                {
                    toolbarSettings: {
                        items: ej.ReportViewer.ToolbarItems.All & ~ej.ReportViewer.ToolbarItems.Parameters
                    }                });


{% endhighlight %}



### Events

The **ReportViewer** has the following client-side events support to listen to the control action.

_Client-Side events_

<table>
<tr>
<td>
<b>Events</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
Destroy</td><td>
Fires when the <b>ReportViewer</b> is destroyed.</td></tr>
<tr>
<td>
drillThrough</td><td>
Fires during drill through action done in report and event can be cancelled.</td></tr>
<tr>
<td>
renderingBegin</td><td>
Fires before report rendering is completed.</td></tr>
<tr>
<td>
renderingComplete</td><td>
Report loaded method that is triggered when report and sub report begin loading.</td></tr>
<tr>
<td>
reportError</td><td>
Fires when any error occurs while rendering the report and event can be cancelled.</td></tr>
<tr>
<td>
reportLoaded</td><td>
Fires when the report is loaded.</td></tr>
</table>


{% highlight javascript %}

**[JS]**

$("#viewer").ejReportViewer(
                        {
                            reportServiceUrl: '/api/RDLCReport',
                            processingMode: ej.ReportViewer.ProcessingMode.Local,
                            reportPath: 'DatabindingRemote.rdlc'                          
                            reportLoaded:   'reportLoaded'                          
                        });
        function reportLoaded(senderObj) {
            $.ajax({
                type: "POST",
                contentType: "application/json; charset=utf-8",
                url: '../wcf/Reportservice.svc/GetOrderDetails',
                dataType: "json",
                processData: false,
                crossDomain: true,
                async: false,
                timeout: 5000,
                success: function (result) {
                    reportdata = result.d;
                    var dataManger = ej.DataManager(reportdata);
                    var query = ej.Query().select("OrderID", "CustomerID", "EmployeeID", "Freight", "ShipCity", "ShipCountry");
                    reportResult = dataManger.executeLocal(query);
                    var reportModel = $("#viewer").data('ejReportViewer');
                    reportModel.model.dataSources = [{ value: reportResult, name: "remote" }];
                },
                error: function (result) {
                    alert(result);
                }
            });
        }


{% endhighlight %}















