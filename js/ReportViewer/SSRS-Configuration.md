---
layout: post
title: SSRS Configuration
description: ssrs configuration
platform: js
control: ReportViewer
documentation: ug
api: /api/js/ejreportviewer
---

# SSRS Configuration

The ReportViewer has support to load RDL/RDLC reports from SSRS server. You have to set your SSRS server URL to ReportViewer’s `reportServerUrl` property and set the relative path of RDL/RDLC file in SSRS to ReportViewer’s `reportPath` property. 

{% highlight javascript %}
$("#viewer").ejReportViewer({
    reportServiceUrl: "/api/SSRSReport",
    processingMode: ej.ReportViewer.ProcessingMode.Remote,
    reportPath: "/SSRSSamples2/Territory Sales new",
    reportServerUrl: "http://mvc.syncfusion.com/reportserver"
});
{% endhighlight %}

## Network Credentials for SSRS

The Network credentials can be given at Web API Controller to connect the SSRS server.

{% highlight c# %}
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

N> DataSource credentials must be added to the ReportViewer for Shared DataSources that do not have credentials in the connection string and used in the SSRS Reports.



