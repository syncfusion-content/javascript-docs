---
layout: post
title: SSRS Report | Report Viewer | Syncfusion
description: Render SSRS Report Server reports using Syncfusion JavaScript Report Viewer.
platform: js
control: Report Viewer
documentation: ug
api: /api/js/ejreportviewer
---

# Load SSRS RDL reports
Report Viewer has support to load RDL reports from SSRS Report Server. To render SSRS Reports set the [`reportServerUrl`](../api/ejreportviewer#members:reportserverurl), [`reportPath`](../api/ejreportviewer#members:reportpath), and `reportServiceUrl` properties as in the following code snippet.

{% highlight javascript %}
    <div style="height: 100%; width: 100%;">
        <div style="height: 600px; width: 950px; min-height: 400px;" id="viewer"></div>
        <script type="text/javascript">
            $(function () {
                $("#viewer").ejReportViewer({
                    reportServiceUrl: "/api/ReportsApi",
                    reportPath: "/SSRSSamples/Territory Sales",
                    reportServerUrl: "http://mvc.syncfusion.com/reportserver"
                });
            });
        </script>
    </div>
{% endhighlight %}

N> Report Server URL should be in the format of `http://<servername>/reportserver$instanceName`
The report path should be in the format of "/folder name/report name".

## Network credentials for SSRS
The network credentials are required to connect with the specified SSRS Report Server using Report Viewer. Specify the `ReportServerCredential` property in the Web API Controller `OnInitReportOptions` method.

{% highlight c# %}
public void OnInitReportOptions(ReportViewerOptions reportOption)
{
    //Add SSRS Report Server credential
    reportOption.ReportModel.ReportServerCredential = new System.Net.NetworkCredential("ssrs", "RDLReport1");
}
{% endhighlight %}


## Set data source credential for shared data sources
The SSRS Report Server does not provide options to get credential information of the report data source deployed on the SSRS server. If the report has any data source that uses credentials to connect with the database, then you must specify the `DataSourceCredentials` for each report data source to establish database connection.

{% highlight c# %}
public void OnInitReportOptions(ReportViewerOptions reportOption)
{
    //Add SSRS Report Server and data source credentials
    reportOption.ReportModel.ReportServerCredential = new System.Net.NetworkCredential("ssrs", "RDLReport1");

    reportOption.ReportModel.DataSourceCredentials.Add(new Syncfusion.Reports.EJ.DataSourceCredentials("AdventureWorks", "ssrs1", "RDLReport1"));
}
{% endhighlight %}

I> Data source credentials must be added for shared data sources that do not have credentials in the connection strings.

Build and run the application and you can see the Report Viewer on the page as displayed in the following screenshot.

![Territory Sales SSRS Report Server report preview in Report Viewer](images/getting-started/territory-sales-report.png)

## Render linked reports
You can render a linked report that point to an existing report, which is published in the SSRS Report Server. Also, it is possible to set the parameter, data source, credential, and other properties as like normal SSRS reports using the Report Viewer.

{% highlight javascript %}
    <div style="height: 100%; width: 100%;">
        <div style="height: 600px; width: 950px; min-height: 400px;" id="viewer"></div>
        <script type="text/javascript">
            $(function () {
                $("#viewer").ejReportViewer({
                    reportServiceUrl: "/api/ReportApi",
                    reportPath: "/SSRSSamples/Territory Sales_Link",
                    reportServerUrl: "http://mvc.syncfusion.com/reportserver"
                });
            });
        </script>
    </div>
{% endhighlight %}

N> The `Territory Sales_Link` is a linked report created for `Territory Sales` report that is already available on the SSRS Report Server.
