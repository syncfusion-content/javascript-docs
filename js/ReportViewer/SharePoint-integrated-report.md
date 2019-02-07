---
layout: post
title: SharePoint integrated reports | Report Viewer | Syncfusion
description: Render SharePoint integrated SSRS reports using Syncfusion JavaScript Report Viewer.
platform: js
control: ReportViewer
documentation: ug
api: /api/js/ejreportviewer
---

# Load SharePoint integrated reports

To render SharePoint integrated SSRS reports set the [`reportServerUrl`](../api/ejreportviewer#members:reportserverurl), [`reportPath`](../api/ejreportviewer#members:reportpath), `reportServiceUrl` properties as in the below code snippet.

{% highlight javascript %}
    <div style="height: 100%; width: 100%;">
        <div style="height: 600px; width: 950px; min-height: 400px;" id="viewer"></div>
        <script type="text/javascript">
            $(function () {
                $("#viewer").ejReportViewer({
                    reportServiceUrl: "/api/ReportApi",
                    reportPath: "http://mvc.syncfusion.com/dev_report/SSRSSamples/Territory Sales.rdl",
                    reportServerUrl: "http://mvc.syncfusion.com/dev_report/reportserver"
                });
            });
        </script>
    </div>

{% endhighlight %}

N> In SharePoint integrated mode reportServerUrl will be same as your site URL.
The report path is relative to your reportServerUrl with file extension.

## Forms credential for SharePoint server
The Forms credentials are required to connect with the specified SharePoint integrated SSRS Report Server using Report Viewer. Specify the `ReportServerFormsCredential` property in Web API Controller `OnInitReportOptions` method.

{% highlight c# %}
public void OnInitReportOptions(ReportViewerOptions reportOption)
{
    //Add ReportServerFormsCredential for server
    reportOption.ReportModel.ReportServerFormsCredential = new Syncfusion.Reports.EJ.ReportServerFormsCredential("ssrs", "RDLReport1");
}
{% endhighlight %}


## Data source credential for shared data sources

Add the data source credentials in `DataSourceCredentials` to connect with database, for all the report data source to use in the report that do not have credentials in the connection strings.

{% highlight c# %}
public void OnInitReportOptions(ReportViewerOptions reportOption)
{
    //Add ReportServerFormsCredential and data source credentials
    reportOption.ReportModel.ReportServerFormsCredential = new Syncfusion.Reports.EJ.ReportServerFormsCredential("ssrs", "RDLReport1");
    reportOption.ReportModel.DataSourceCredentials.Add(new Syncfusion.Reports.EJ.DataSourceCredentials("AdventureWorks", "ssrs1", "RDLReport1"));
}
{% endhighlight %}

N> DataSource credentials must be added for shared data sources that do not have credentials in the connection strings.

Build and run the application and you can see the ReportViewer on the page as displayed in the following screenshot.

![SharePoint integrated SSRS report preview in Report Viewer](images/getting-started/territory-sales-report.png)