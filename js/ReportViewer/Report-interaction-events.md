---
layout: post
title: Report Interaction Events | Report Viewer | Syncfusion
description: Preview subreport with custom data collection (JSON array, IList, DataSet, and DataTable) and parameter using JavaScript Report Viewer.
platform: js
control: Report Viewer
documentation: ug
api: /api/js/ejreportviewer
---

# Report interaction events
You can handle the report processing actions and interact with reports using the following events.

* ReportLoaded
* ReportError
* ShowError
* Drill through
* Hyperlink

## Report loaded

The [`reportLoaded`](../api/ejreportviewer#events:reportloaded) event fires once the report loading is completed and ready to start the processing. You can handle the event and specify data source, parameters at client-side. The following sample code loads a report by assigning report data source input in the `reportLoaded` event.

N> In this tutorial, `Product List.rdlc` report is used, you can add the report from Syncfusion installation location. For more information, see [Samples and demos](/js/reportviewer/samples-and-demos).

{% highlight javascript %}
        <script type="text/javascript">
            $(function () {
                $("#viewer").ejReportViewer(
                    {
                        reportServiceUrl: "/api/ReportsApi",
                        processingMode: ej.ReportViewer.ProcessingMode.Local,
                        reportPath: '~/App_Data/Product List.rdlc',
                        reportLoaded: "onReportLoaded",
                    });
            });

            function onReportLoaded(args) {
                var dataSource = [
                    {
                        ProductName: "Baked Chicken and Cheese", OrderId: "323B60", Price: 55, Category: "Non-Veg", Ingredients: "Grilled chicken, Corn and Olives.", ProductImage: ""
                    },
                    {
                        ProductName: "Chicken Delite", OrderId: "323B61", Price: 100, Category: "Non-Veg", Ingredients: "Cheese, Chicken chunks, Onions & Pineapple chunks.", ProductImage: ""
                    },
                    {
                        ProductName: "Chicken Tikka", OrderId: "323B62", Price: 64, Category: "Non-Veg", Ingredients: "Onions, Grilled chicken, Chicken salami & Tomatoes.", ProductImage: ""
                    }];

                var reportObj = $('#viewer').data("ejReportViewer");
                reportObj.model.dataSources = [{
                    value: ej.DataManager(desc2013).executeLocal(ej.Query()),
                    name: "list"
                }];
            }
        </script>
{% endhighlight %}

## Report error
When an error occurs in the report processing, it raises the [`reportError`](../api/ejreportviewer#events:reporterror) event. You can handle the event and show the details in your custom dialog instead of component default error detail interface.

{% highlight javascript %}
        <script type="text/javascript">
            $(function () {
                $("#viewer").ejReportViewer(
                    {
                        reportServiceUrl: "/api/ReportsApi",
                        processingMode: ej.ReportViewer.ProcessingMode.Local,
                        reportPath: '~/App_Data/Product List.rdlc',
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
The [`showError`](../api/ejreportviewer#events:showerror) event invoked whenever the user clicks a report item that contains an error in processing. It provides detailed information about the cause of the error. You can hide the default dialog and show your customized dialog.

{% highlight javascript %}
        <script type="text/javascript">
            $(function () {
                $("#viewer").ejReportViewer(
                    {
                        reportServiceUrl: "/api/ReportsApi",
                        processingMode: ej.ReportViewer.ProcessingMode.Local,
                        reportPath: '~/App_Data/Product List.rdlc',
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
When a drill through item is selected in a report, it invokes the [`drillThrough`](../api/ejreportviewer#events:drillthrough) event. You can change the drill through arguments such as report parameter and data sources. The following sample code can be used to change the drill through report name and set the parameter value before the drill through report is rendered.

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
The [`hyperlink`](../api/ejreportviewer#events:hyperlink) event occurs when the user clicks a hyperlink in a report, before the hyperlink is followed. The following sample code redirects to a new custom URL and cancels the component default action.

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
