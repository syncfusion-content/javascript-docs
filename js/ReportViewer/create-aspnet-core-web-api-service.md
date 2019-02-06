---
layout: post
title: Create ASP.NET Core Web API Service | Report Viewer | Syncfusion
description: Create ASP.NET Core Web API Service for Syncfusion HTML5 JavaScript Report Viewer to process and render reports.
platform: js
control: ReportViewer
documentation: ug
api: /api/js/ejreportviewer
---

# Create ASP.NET Core Web API Service
In this section, you will learn how to create a ASP.NET Core Web API for Report Viewer using the new ASP.NET Core Web Application template.

1.	Open Visual Studio 2017, from the File menu, select New Project. 
2.	Select the ASP.NET Core Web Application template. Name the project “ReportViewerWebAPIService” and click OK.
3.	Choose the ASP.NET Core version. Select the Empty template and click OK. Do not select Enable Docker Support.

    ![Creating a new ASP.NET Core Application Project](/images/report-service/aspnet-core-web-application.png)

## List of dependency libraries
The Web API service configuration requires the following reporting server-side packages. In the Solution Explore, right-click on Dependencies, select Manage NuGet Packages then search the below packages and install to the application.


I> Starting with v16.2.0.x, if you refer to Syncfusion assemblies from trial setup or from the NuGet feed, include a license key in your projects. Refer to this link to learn about registering Syncfusion license key in your ASP.NET Core application to use our components.

## Add a controller
1.	Right-click the Controllers folder.
2.	Select Add > New Item.
3.	In the Add New Item dialog, select the API Controller Class template.
4.	Name the class ReportsApiController and select Add.

    ![Add ASP.NET Core api controller](/images/report-service/add-core-api-controller.png)

## Inherit IReportController
The ‘IReportController’ interface contains the required actions and helper methods declaration to process the report. The `ReportHelper` class contains methods that helps to process Post/Get request from control and return the response. Open the ReportsApiController, inherit the IReportController interface and implement its methods (you can use the following codes).

{% highlight c# %}
public class HomeController : Controller, IReportController
    {
        // Report viewer requires a memory cache to store the information of consecutive client request and
        // have the rendered report viewer information in server.
        private Microsoft.Extensions.Caching.Memory.IMemoryCache _cache;

        // IHostingEnvironment used with sample to get the application data from wwwroot.
        private Microsoft.AspNetCore.Hosting.IHostingEnvironment _hostingEnvironment;

        // Post action to process the report from server based json parameters and send the result back to the client.
        public HomeController(Microsoft.Extensions.Caching.Memory.IMemoryCache memoryCache,
            Microsoft.AspNetCore.Hosting.IHostingEnvironment hostingEnvironment)
        {
            _cache = memoryCache;
            _hostingEnvironment = hostingEnvironment;
        }

        // Post action to process the report from server based json parameters and send the result back to the client.
        [HttpPost]
        public object PostReportAction([FromBody] Dictionary<string, object> jsonArray)
        {
            return Syncfusion.EJ.ReportViewer.ReportHelper.ProcessReport(jsonArray, this, this._cache);
        }

        // Method will be called to initialize the report information to load the report with ReportHelper for processing.
        public void OnInitReportOptions(Syncfusion.EJ.ReportViewer.ReportViewerOptions reportOption)
        {
            string basePath = _hostingEnvironment.WebRootPath;
            // Here, we have loaded the sample report report from application the folder wwwroot. Sample.rdl should be there in wwwroot application folder.
            FileStream reportStream = new FileStream(basePath + @"\invoice.rdl", FileMode.Open, FileAccess.Read);
            reportOption.ReportModel.Stream = reportStream;
        }

        // Method will be called when reported is loaded with internally to start to layout process with ReportHelper.
        public void OnReportLoaded(Syncfusion.EJ.ReportViewer.ReportViewerOptions reportOption)
        {
        }

        //Get action for getting resources from the report
        [ActionName("GetResource")]
        [AcceptVerbs("GET")]
        // Method will be called from Report Viewer client to get the image src for Image report item.
        public object GetResource(Syncfusion.EJ.ReportViewer.ReportResource resource)
        {
            return Syncfusion.EJ.ReportViewer.ReportHelper.GetResource(resource, this, _cache);
        }

        [HttpPost]
        public object PostFormReportAction()
        {
            return Syncfusion.EJ.ReportViewer.ReportHelper.ProcessReport(null, this, _cache);
        }
    }

{% endhighlight %}

N> You cannot load the application report with path information in ASP.NET Core. So, you should load the report as Stream like an example provided above in OnInitReportOptions. If you need to get the invoice sample report then you can obtain it from the Syncfusion ASP.NET Core sample browser installed location (wwwroot\reports\invoice.rdl).

Compile and run the Web API service application.
