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

Report Viewer has support to displays another report inside the body of a main report. The following guides you to customize the subreport properties such as data source, report path, and parameters. 

1.Add the sub report and main reports to your application, in this tutorial we are using the already created reports. Refer the [Create Report](/js/reportviewer/how-to/create-report) section to create a new report.

N> You can obtain Side_By_SideMainReport.rdl, Side_By_SideSubReport.rdl files from Syncfusion installed location (%userprofile%\AppData\Local\Syncfusion\EssentialStudio\{{ site.releaseversion }}\Common\Data\ejReportTemplate) or you can download from [here](http://www.syncfusion.com/downloads/support/directtrac/general/ze/Subreports-1004880284).

N> If the reports used from installed location it requires NorthwindIO_Reports.sdf database to run, so add it to your application.

2.Set `reportPath` and `reportServiceUrl` properties of Report Viewer as in below code snippet.

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

3.Build and run the application, to view the below result.

![Employee comparison using subreport report item](images/getting-started/side-by-side-subreport.png)

## Change subreport path
To change the subreport file path, set ReportPath property of SubReportModel in `OnInitReportOptions` method.

{% highlight c# %}
        public void OnInitReportOptions(ReportViewerOptions reportOption)
        {
            if (reportOption.SubReportModel != null)
            {
                reportOption.SubReportModel.ReportPath = @" D:\Tutorial\ReportViewerWebAPIService\ReportViewerWebAPIService\App_Data \SubReport_Detail.rdl";
                reportOption.ReportModel.DataSourceCredentials.Add(new Syncfusion.Reports.EJ.DataSourceCredentials("NorthWind", "Data Source=dataplatformdemodata.syncfusion.com;Initial Catalog=Northwind;user id=demoreadonly@data-platform-demo;password=N@c)=Y8s*1&dh"));
            }
        }

{% endhighlight %}

## Set subreport parameter
You can change the parameter default values of a subreport in Web API Controller `OnReportLoaded`, method as given in below code snippet.

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

## Set or modify subreport data source
To change the data source of a RDLC subreport, set the `ReportDataSource` collection in `OnReportLoaded` method. The data source name is case sensitive, it should be same as in the report definition.

{% highlight c# %}
        public void OnReportLoaded(ReportViewerOptions reportOption)
        {
            //Assigning the data source for 'Product List.rdlc'
            if (reportOption.SubReportModel != null)
            {
                reportOption.ReportModel.DataSources.Add(new Syncfusion.Reports.EJ.ReportDataSource { Name = "list", Value = ProductList.GetData() });
            }
        }

{% endhighlight %}

N> You can bind data source only for RDLC reports. The RDL report has the connection information in report definition itself, so no need to bind data source.

## Modify subreport data source connection string
You can change the credential and connection information of the data sources used in the subreport using the SubReportModel in `OnInitReportOptions` method.

{% highlight c# %}
        public void OnInitReportOptions(ReportViewerOptions reportOption)
        {
            if (reportOption.SubReportModel != null)
            {
                reportOption.ReportModel.DataSourceCredentials.Add(new Syncfusion.Reports.EJ.DataSourceCredentials("NorthWind", "Data Source=dataplatformdemodata.syncfusion.com;Initial Catalog=Northwind;user id=demoreadonly@data-platform-demo;password=N@c)=Y8s*1&dh"));
            }
        }

{% endhighlight %}