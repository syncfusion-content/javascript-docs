---
layout: post
title: Report Interaction Events | Report Viewer | Syncfusion
description: Preview subreport with custom data collection (JSON array, IList, DataSet, and DataTable) and parameter using JavaScript Report Viewer.
platform: js
control: ReportViewer
documentation: ug
api: /api/js/ejreportviewer
---

# Report interaction events

## Report loaded
The ‘reportLoaded` event fires once the report loading is completed and ready to start the processing and evaluation. You can override the event and specify data source, parameters at client side The following sample code loads a report by assigning report data source input in reportLoaded event.

N> Here in this sample, used the IndicatorReport.rdlc and you can find the report from Syncfusion installed location (%userprofile%\AppData\Local\Syncfusion\EssentialStudio\{{ site.releaseversion }}\Common\Data\ejReportTemplate).

{% highlight javascript %}
    <script type="text/javascript">

        $(function () {
            $("#container").ejReportViewer(
                {
                    reportServiceUrl: "/api/ReportsApi",
                    reportPath: '~/App_Data/IndicatorReport.rdlc',
                    reportLoaded: "onReportLoaded",
                    reportError: "onReportError",
                    showError: "onShowError",
                    hyperlink: "onHyperlink",
                    drillThrough: "onDrillThrough",
                });
        });
        function onReportLoaded(args) {

            var desc2013 = [
                {
                    No: 1, Name: "Carlos Slim", NetWorth: 73.0, Age: 73, CitizenShip: "Mexico", Source: "Telmex,America Movil, Grupo Carso", RankingStatus: 50, ProfitStatus: 75
                },
                {
                    No: 2, Name: "Bill Gates", NetWorth: 67.0, Age: 57, CitizenShip: "United States", Source: "Microsoft", RankingStatus: 50, ProfitStatus: 75
                },
                {
                    No: 3, Name: "Amancio Ortega", NetWorth: 57.0, Age: 57, CitizenShip: "Spain", Source: "Inditex Group", RankingStatus: 75, ProfitStatus: 75
                },
                {
                    No: 4, Name: "Warren Buffett", NetWorth: 53.0, Age: 82, CitizenShip: "United States", Source: "Berkshire Hathaway", RankingStatus: 25, ProfitStatus: 75
                },
                {
                    No: 5, Name: "Larry Ellison", NetWorth: 43.0, Age: 68, CitizenShip: "United States", Source: "Oracle Corporation", RankingStatus: 75, ProfitStatus: 75
                },
                {
                    No: 6, Name: "Charles Koch", NetWorth: 34.0, Age: 77, CitizenShip: "United States", Source: "Koch Industries", RankingStatus: 75, ProfitStatus: 75
                },
                {
                    No: 7, Name: "David Koch", NetWorth: 34.0, Age: 72, CitizenShip: "United States", Source: "Koch Industries", RankingStatus: 75, ProfitStatus: 75
                },
                {
                    No: 8, Name: "Li Ka-shing", NetWorth: 32.0, Age: 84, CitizenShip: "Hong Kong/ Canada", Source: "Cheung Kong Holdings", RankingStatus: 75, ProfitStatus: 75
                },
                {
                    No: 9, Name: "Liliane Bettencourt", NetWorth: 30.0, Age: 90, CitizenShip: "France", Source: "L'Oreal", RankingStatus: 75, ProfitStatus: 75
                },
                {
                    No: 10, Name: "Bernard Arnault", NetWorth: 29.0, Age: 63, CitizenShip: "France", Source: "LVMH Moet Hennessy Louis Vuitton", RankingStatus: 25, ProfitStatus: 25
                }];

            var desc2012 = [
                {
                    No: 1, Name: "Carlos Slim", NetWorth: 69.0, Age: 72, CitizenShip: "Mexico", Source: "Telmex,America Movil, Grupo Carso", RankingStatus: 50, ProfitStatus: 25
                },
                {
                    No: 2, Name: "Bill Gates", NetWorth: 61.0, Age: 56, CitizenShip: "United States", Source: "Microsoft", RankingStatus: 50, ProfitStatus: 75
                },
                {
                    No: 3, Name: "Warren Buffett", NetWorth: 44.0, Age: 81, CitizenShip: "United States", Source: "Berkshire Hathaway", RankingStatus: 50, ProfitStatus: 25
                },
                {
                    No: 4, Name: "Bernard Arnault", NetWorth: 41.0, Age: 63, CitizenShip: "France", Source: "LVMH Moet Hennessy Louis Vuitton", RankingStatus: 50, ProfitStatus: 75
                },
                {
                    No: 5, Name: "Amancio Ortega", NetWorth: 37.5, Age: 75, CitizenShip: "Spain", Source: "Inditex Group", RankingStatus: 75, ProfitStatus: 75
                },
                {
                    No: 6, Name: "Larry Ellison", NetWorth: 36.0, Age: 67, CitizenShip: "United States", Source: "Oracle Corporation", RankingStatus: 25, ProfitStatus: 75
                },
                {
                    No: 7, Name: "Eike Batista", NetWorth: 30.0, Age: 55, CitizenShip: "Brazil", Source: "EBX Group", RankingStatus: 75, ProfitStatus: 75
                },
                {
                    No: 8, Name: "Stefan Persson", NetWorth: 26.5, Age: 64, CitizenShip: "Sweden", Source: "H&M", RankingStatus: 75, ProfitStatus: 75
                },
                {
                    No: 9, Name: "Li Ka-shing", NetWorth: 25.0, Age: 83, CitizenShip: "Hong Kong/ Canada", Source: "Cheung Kong Holdings", RankingStatus: 75, ProfitStatus: 75
                },
                {
                    No: 10, Name: "Karl Albrecht", NetWorth: 25.4, Age: 92, CitizenShip: "Germany", Source: "Aldi", RankingStatus: 75, ProfitStatus: 25
                }];

            var description = [
                {
                    Status: 25, Description: "Has not changed from the previous ranking."
                },
                {
                    Status: 50, Description: "Has increased from the previous ranking."
                },
                {
                    Status: 75, Description: "Has decreased from the previous ranking."
                }];

            var reportObj = $('#container').data("ejReportViewer");
            reportObj.model.dataSources = [{
                value: ej.DataManager(desc2013).executeLocal(ej.Query()),
                name: "DataSet1"
            }, {
                value: ej.DataManager(desc2012).executeLocal(ej.Query()),
                name: "DataSet2"
            }, {
                value: ej.DataManager(description).executeLocal(ej.Query()),
                name: "DataSet3"
            }];
        }
    </script>
{% endhighlight %}

## Report error
When an error occurs in the report it raises the [`reportError`](../api/ejreportviewer#events:reporterror) event and you can handle and show the details in your custom dialog instead of component default error detail interface.

{% highlight javascript %}
    <script type="text/javascript">
        $(function () {
            $("#container").ejReportViewer(
                {
                    reportServiceUrl: "/api/ReportsApi",
                    reportPath: '~/App_Data/IndicatorReport.rdlc',
                    reportError: "onReportError",
                });
        });
        function onReportError(args) {
            alert(args.errmsg);

            args.cancel = true;
        }
    </script>
{% endhighlight %}

N> To suppress the default error dialog, set the cancel argument to true.

## Show error
The [`showError`](../api/ejreportviewer#events:showerror) event invoked whenever click on a report item that contains error processing errors. It provides detailed information about the cause of error. You can override it and show your customized dialog.

{% highlight javascript %}
    <script type="text/javascript">

        $(function () {
            $("#container").ejReportViewer(
                {
                    reportServiceUrl: "/api/ReportsApi",
                    reportPath: '~/App_Data/IndicatorReport.rdlc',
                    showError: "onShowError",
                });
        });

        function onShowError(args) {
            alert("Error code : " + args.errorCode + "\n" +
                "Error Detail : " + args.errorDetail + "\n" +
                "Error Message : " + args.errorMessage);

            args.cancel = true;
        }
    </script>
{% endhighlight %}

## Drill through
When a drill through item is selected in a report, it invokes the [`drillThrough`](../api/ejreportviewer#events:drillthrough) event, you can change the drill through arguments such as drill through report parameter, datasources. The following sample code loads drill through report and adds data source to the report before the drillthrough report is rendered.

{% highlight c# %}
    <script type="text/javascript">

        $(function () {
            $("#container").ejReportViewer(
                {
                    reportServiceUrl: "/api/ReportsApi",
                    reportPath: '~/App_Data/SubReport_Detail.rdl',
                    drillThrough: "onDrillThrough",
                });
        });

        function onDrillThrough(args) {
            args.actionInfo.ReportName = "Sales Order Detail";
            args.actionInfo.Parameters = [{ name: 'SalesOrderNumber', labels: ['SO50751'], values: ['SO50751'] }];
        }
    </script>
{% endhighlight %}

## Hyperlink
The [`hyperlink`](../api/ejreportviewer#events:hyperlink) event occurs when a user clicks a hyperlink in a report, before the hyperlink is followed. The following sample code redirects to new custom URL and cancels the component default action.

{% highlight c# %}
    <script type="text/javascript">
        $(function () {
            $("#container").ejReportViewer(
                {
                    reportServiceUrl: "/api/ReportsApi",
                    reportPath: '~/App_Data/SubReport_Detail.rdl',
                    hyperlink: "onHyperlink",
                });
        });
        function onHyperlink(args) {
            args.cancel = true;
            window.open(args.actionInfo.Hyperlink + "/Report Parameter");
        }
    </script>
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