---
layout: post
title: Getting-Started
description: getting started
platform: js
control: ReportViewer
documentation: ug
---

# Getting Started

This section explains briefly about how to create a **ReportViewer** in your web application with **JavaScript**.

## Create your first ReportViewer in JavaScript

###Control Structure

The following screenshot displays the control structure of **ReportViewer**.

{% include image.html url="/js/ReportViewer/Getting-Started_images/Getting-Started_img1.png" Caption="ReportViewer Structure"%}

###Create an Application

This section explains how to configure a **ReportViewer** component in web application. As **ReportViewer** uses **WebApi** to process the report file, you can also learn how to create **WebApi** Service to process the report for **ReportViewer**. In the following example, the **ReportViewer** component displays the Sales Dashboard Report.    

Open **Visual Studio** and create a new project by clicking **New Project**. Select the **Web** category, select the **ASP.NET****Empty Web Application** template, and then click **OK**. The following screenshot displays the **Project Creation** Wizard.

{% include image.html url="/js/ReportViewer/Getting-Started_images/Getting-Started_img2.png" Caption="Project Creation Wizard"%}

###Create HTML Page

To create a new web form in the application

1\. Right-Click on the project and select **Add**

{% include image.html url="/js/ReportViewer/Getting-Started_images/Getting-Started_img3.png" Caption="Add New Item Wizard"%}



2\. Click **New Item** and select **HTML** Page from the listed templates

{% include image.html url="/js/ReportViewer/Getting-Started_images/Getting-Started_img4.png" Caption="Adding HTML page"%}



3\. Name the page as **Default.html** and click **OK**.



###Add References, Scripts, Styles and Control in HTML Page

###Add References

1\. In the **Solution Explorer**, right-click the **References** folder and then click **Add Reference**



{% include image.html url="/js/ReportViewer/Getting-Started_images/Getting-Started_img5.png" Caption="Adding reference"%}

2\. Add the following assemblies

* System.Web.Routing,  

* System.Web.Http,

* System. Web.Http.WebHost,

* System.Net.Http,

* System.Net.Http.WebRequest,

* System.Net.Http.Formatting,

* Syncfusion.Linq.Base.dll,

* Syncfusion.EJ.ReportViewer,

* Syncfusion.ReportControls.Wpf

* Syncfusion.ReportWriter.Base

* Syncfusion.Pdf.Base,

* Syncfusion.XlsIO.Base,

* Syncfusion.DocIO.Base

* Synfusion.Shared.Wpf

* Syncfusion.Chart.Wpf

* Syncfusion.Gauge.Wpf

* Syncfusion.SfMaps.Wpf 



>**Note**_: Refer System.Web.Http, System. Web.Http.WebHost, System.Net.Http.WebRequest and System.Net.Http.Formatting dlls from ASP.NET WebApi nuget package._





3\. Click **OK**



###Add Scripts and Styles

Add the script files and CSS files in the **&lt;title&gt;** tag of the **default.html** page.





{% highlight html %}

  
<link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
<script src="http://code.jquery.com/jquery-1.10.2.min.js" type="text/javascript"> </script>
<script src="http://cdnjs.cloudflare.com/ajax/libs/jquery-easing/1.3/jquery.easing.min.js" type="text/javascript"> </script>
<script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js" type="text/javascript"></script>


{% endhighlight %}



###Add Control in HTML Page

Add the following code example in the **&lt;body&gt;** tag in the **Default.html** page. Set the desired **ReportPath** and **ReportServiceUrl** to **ReportViewer**.

{% highlight html %}


<div>
        <!-- Creating a div tag which will act as a container for ejReportViewer widget.-->
        <div  style="height: 650px;width: 950px;min-height:404px;" id="viewer"></div>

        <!-- Setting property and initializing ejReportViewer widget.-->
<script type="text/javascript">
$(function () {
$("#viewer").ejReportViewer(
                    {
                        reportServiceUrl: "/api/ReportApi",
                        reportPath: '~/App_Data/Sales Dashboard.rdl'
                    });
});
        </script>
</div>


{% endhighlight %}



>**Note**_: Add your report files to your application’s App_Data folder. You can obtain sample rdl/rdlc files from Syncfusion installed location (%userprofile%\AppData\Local\Syncfusion\EssentialStudio\XX.X.X.XX\Common\Data\ejReportTemplate). “XX.X.X.XX” is the Essential Studio Release Version._



###Add WebAPI controller for ReportViewer

The **JavaScript ReportViewer** uses **WebApi** services to process the report file and process the request from control.

{% include image.html url="/js/ReportViewer/Getting-Started_images/Getting-Started_img6.png" Caption="Adding WebApi Controller"%}

####Inherit IReportController

The **ApiController** inherits the **IReportController** and you can add the following code example to its methods definition in order to process the report file. The interface **IReportController** contains the required actions and helper methods declaration to process the report. The **ReportHelper** class contains helper methods that helps to process Post/Get request from control and return the response to control.

{% highlight c# %}


using Syncfusion.EJ.ReportViewer;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Net;
using System.Net.Http;
using System.Web.Http;

namespace ReportViewerDemo.Api
{
    public class ReportApiController : ApiController, IReportController
    {
        //Post action for processing the rdl/rdlc report 
        public object PostReportAction(Dictionary<string, object> jsonResult
        {
            return ReportHelper.ProcessReport(jsonResult, this);
        }

        //Get action for getting resources from the report
        [System.Web.Http.ActionName("GetResource")]
        [AcceptVerbs("GET")]
        public object GetResource(string key, string resourcetype, bool isPrint)
        {
            return ReportHelper.GetResource(key, resourcetype, isPrint);
        }

        //Method will be called when initialize the report options before start processing the report        public void OnInitReportOptions(ReportViewerOptions reportOption)
        {
           //You can update report options here
        }

        //Method will be called when reported is loaded
        public void OnReportLoaded(ReportViewerOptions reportOption)
        {
           //You can update report options here
        }   
    }
}


{% endhighlight %}



###WebAPI Routing

1\. Right-Click the **Project**, select **Add >** and select **Global.asax** file from the listed templates.

{% include image.html url="/js/ReportViewer/Getting-Started_images/Getting-Started_img7.png" Caption="Adding Global.asax"%}

2\. You can route the **WebAPI** in **Application_Start** event into **Global.asax** file as follows.

{% highlight c# %}


using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.Security;
using System.Web.SessionState;
using System.Web.Http;

namespace ReportViewerDemo
{
    public class Global : System.Web.HttpApplication
    {
        protected void Application_Start(object sender, EventArgs e)
        {
          System.Web.Http.GlobalConfiguration.Configuration.Routes.MapHttpRoute(
          name: "DefaultApi",
          routeTemplate: "api/{controller}/{action}/{id}",
          defaults: new { id = RouteParameter.Optional });
        }
    }
}


{% endhighlight %}



###Run the Application

Run the sample application and you can see the **ReportViewer** on the page as displayed in the following screenshot.

{% include image.html url="/js/ReportViewer/Getting-Started_images/Getting-Started_img8.png" Caption="ReportViewer with Sales Dashboard Report"%}

###Load SSRS Server Reports

**ReportViewer** supports to load RDL/RDLC files from SSRS Server. The following steps help you to load reports from SSRS Server.

1\. Set the **reportPath** from SSRS and SSRS **reportServerUrl** in the **ReportViewer** properties.

{% highlight html %}


<div>
        <!-- Creating a div tag which will act as a container for ejReportViewer widget.-->
        <div  style="height: 650px;width: 950px;min-height:404px;" id="viewer"></div>

        <!-- Setting property and initializing ejReportViewer widget.-->
<script type="text/javascript">
$(function () {
$("#viewer").ejReportViewer(
                    {
                      reportServiceUrl: "/api/ReportApi",
                      reportPath: "/SSRSSamples2/Territory Sales",
                      reportServerUrl: "http://76.74.153.81/ReportServer"
                    });
});
        </script>
</div>


{% endhighlight %}

2\. Add the credential information in **ReportApiController’s****OnInitReportOptions** method which is available in **IReportController**.

{% highlight c# %}


        public void OnInitReportOptions(ReportViewerOptions reportOption)
        {
            //Add SSRS Server and database credentials here
            reportOption.ReportModel.ReportServerCredential = new System.Net.NetworkCredential("ssrs", "RDLReport1");
            reportOption.ReportModel.DataSourceCredentials.Add(new DataSourceCredentials("AdventureWorks", "ssrs1", "RDLReport1"));
        }


{% endhighlight %}



3\. Run the application and you can see the **ReportViewer** on the page as displayed in the following screenshot.

{% include image.html url="/js/ReportViewer/Getting-Started_images/Getting-Started_img9.png" Caption="Report from SSRS"%}

###Load RDLC Reports

The **ReportViewer** has data binding support to visualize the **RDLC** reports. The following code example helps you to bind data to **ReportViewer**.

1\. Assign the **RDLC** report path to **ReportViewer’s****ReportPath** property and set the data sources to the **ReportViewer’s****dataSources** property.

{% highlight html %}


<div>
        <!-- Creating a div tag which will act as a container for ejReportViewer widget.-->
        <div  style="height: 650px;width: 950px;min-height:404px;" id="viewer"></div>

        <!-- Setting property and initializing ejReportViewer widget.-->
<script type="text/javascript">
$(function () {
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
});
        </script>
</div>


{% endhighlight %}

2\. Run the application and you can see the **ReportViewer** on the page as displayed in the following screenshot.

{% include image.html url="/js/ReportViewer/Getting-Started_images/Getting-Started_img10.png" Caption="Product List RDLC Report"%}

