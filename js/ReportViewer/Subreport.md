---
layout: post
title: Render subreport | Report Viewer | Syncfusion
description: Preview subreport with custom data collection (JSON array, IList, DataSet, and DataTable) and parameter using JavaScript Report Viewer.
platform: js
control: ReportViewer
documentation: ug
api: /api/js/ejreportviewer
---

# Preview subreport

You can display another report inside the body of a main report using the Report Viewer. The following steps helps you to customize the subreport properties such as data source, report path, and parameters.

1.Add the sub report and main reports to your application App_Data folder. In this tutorial, use the already created reports. Refer to the [Create Report](/js/reportviewer/how-to/create-report) section to create a new report.

N> Download the Side_By_SideMainReport.rdl, Side_By_SideSubReport.rdl reports from [here](http://www.syncfusion.com/downloads/support/directtrac/general/ze/Subreports-1004880284). Also, you can add the report from Syncfusion installation location. For more information, see [Samples and demos](/js/reportviewer/samples-and-demos). The reports used from installed location, requires NorthwindIO_Reports.sdf database to run, so add it to your application.

2.Set the `reportpath` and `reportServiceUrl` properties of the Report Viewer as in following code snippet..

{% highlight javascript %}
        <script type="text/javascript">
            $(function () {
                $("#viewer").ejReportViewer({
                    reportServiceUrl: "/api/ReportsApi",
                    reportPath: '~/App_Data/Side_By_SideMainReport.rdl',
                });
            });
        </script>

{% endhighlight %}

3.Build and run the application, to view the following result

![Employee comparison using subreport report item](images/getting-started/side-by-side-subreport.png)

## Change subreport path
To change the subreport file path, set the `ReportPath` property of SubReportModel in the `OnInitReportOptions` method.

{% highlight c# %}
        public void OnInitReportOptions(ReportViewerOptions reportOption)
        {
            if (reportOption.SubReportModel != null)
            {
                reportOption.SubReportModel.ReportPath = System.Web.Hosting.HostingEnvironment.MapPath(@"~/App_Data/SubReport_Detail.rdl");
            }
        }

{% endhighlight %}

## Set subreport parameter
You can change the parameter default values of a subreport in the Web API Controller `OnReportLoaded`, method as given in the following code snippet.

{% highlight c# %}
        public void OnReportLoaded(ReportViewerOptions reportOption)
        {
            if (reportOption.SubReportModel != null)
            {
                reportOption.SubReportModel.Parameters = new Syncfusion.Reports.EJ.ReportParameterInfoCollection();
                reportOption.SubReportModel.Parameters.Add(new Syncfusion.Reports.EJ.ReportParameterInfo()
                {
                    Name = "SalesPersonID",
                    Values = new List<string>() { "2" }
                });
            }
        }

{% endhighlight %}

## Modify subreport data source connection string
You can change the credential and connection information of the data sources used in the subreport using the SubReportModel in `OnInitReportOptions` method.

{% highlight c# %}
        public void OnInitReportOptions(ReportViewerOptions reportOption)
        {
            if (reportOption.SubReportModel != null)
            {
                reportOption.SubReportModel.DataSourceCredentials = new List<Syncfusion.Reports.EJ.DataSourceCredentials>();
                reportOption.SubReportModel.DataSourceCredentials.Add(new Syncfusion.Reports.EJ.DataSourceCredentials("NorthWind", "Data Source=dataplatformdemodata.syncfusion.com;Initial Catalog=Northwind;user id=demoreadonly@data-platform-demo;password=N@c)=Y8s*1&dh"));
            }
        }

{% endhighlight %}

## Set subreport data source
To specify data source of a RDLC subreport, set the `ReportDataSource` property in `OnReportLoaded` method. The data source name is case sensitive, it should be same as in the report definition.

{% highlight c# %}
        public void OnReportLoaded(ReportViewerOptions reportOption)
        {
            //Assigning the data source for 'Product List.rdlc'
            if (reportOption.SubReportModel != null)
            {
                reportOption.SubReportModel.DataSources = new Syncfusion.Reports.EJ.ReportDataSourceCollection();
                reportOption.SubReportModel.DataSources.Add(new Syncfusion.Reports.EJ.ReportDataSource { Name = "list", Value = ProductList.GetData() });
            }
        }

{% endhighlight %}

N> You can bind local business object data source collection only for RDLC reports. The RDL report has the connection information in report definition itself, so no need to bind data source.

