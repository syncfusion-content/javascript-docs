---
layout: post
title: Print Report | Report Viewer | JavaScript | Syncfusion
description: Control and customize the report printing using properties and events. 
platform: js
control: Report Viewer
documentation: ug
---

# Printing 
The Report Viewer provides print option in the toolbar to print a copy of the report. The page setup dialog allows you to set the paper size or other page setup properties. To see print margins, click Print Layout on the toolbar.

N> The values allow you to set in the Page Setup dialog box for current session only. When you close the report and reopen it, it will have the default values again. The default values for the page setup dialog come from the report properties, which are set in the design view.

## View report in print mode
Print margins are displayed in the Print Layout only, to view report in print mode by default, set the [`printMode`](../api/ejreportviewer#members:printmode) property to true. 

{% highlight javascript %}
        <script type="text/javascript">
            $(function () {
                $("#viewer").ejReportViewer({
                    reportServiceUrl: "/api/ReportsApi",
                    reportPath: '~/App_Data/Sales Order Detail.rdl',
                    printMode: true
                });
            });
        </script>
{% endhighlight %}

N> By default, the Report Viewer renders report in normal layout in which the print margins are not displayed.

## Print in new page
To open the print in a new tab of the current browser, set the property [`printOption`](../api/ejreportviewer#members:printOption) to `NewTab`. By default, it shows the print dialog in the same page.

{% highlight javascript %}
        <script type="text/javascript">
            $(function () {
                $("#viewer").ejReportViewer({
                    reportServiceUrl: "/api/ReportsApi",
                    reportPath: '~/App_Data/Sales Order Detail.rdl',
                    printMode: true,
                    printOption: ej.ReportViewer.PrintOptions.NewTab
                });
            });
        </script>
{% endhighlight %}

N> The pop-up blocker must be enabled for the page to open the print view in new tab.

## Set page orientation and paper size
You can specify the print page paper size, orientation at client-side to change page setup properties by setting the [`pageSettings`](../api/ejreportviewer#members:pagesettings) property.

{% highlight javascript %}
        <script type="text/javascript">
            $(function () {
                $("#viewer").ejReportViewer({
                    reportServiceUrl: "/api/ReportsApi",
                    reportPath: '~/App_Data/Sales Order Detail.rdl',
                    printMode: true,
                    pageSettings: {
                        orientation: ej.ReportViewer.Orientation.Landscape,
                        paperSize: ej.ReportViewer.PaperSize.Letter
                    }
                });
            });
        </script>
{% endhighlight %}

## Set report margin
To set margin values to the report page setup, use the property [`margins`](../api/ejreportviewer#members:pagesettings-margins) and specify the value to top, right, bottom, and left.

{% highlight javascript %}
        <script type="text/javascript">
            $(function () {
                $("#viewer").ejReportViewer({
                    reportServiceUrl: "/api/ReportsApi",
                    reportPath: '~/App_Data/Sales Order Detail.rdl',
                    printMode: true,
                    pageSettings: {
                        margins: {
                            top: 0.5,
                            right: 0.25,
                            bottom: 0.25,
                            left: 0.25
                        }
                    }
                });
            });
        </script>
{% endhighlight %}

N> The values set in the margin property is considered as inches input.


## Set page height and width
To set height and width values to the report page setup, use the [`height`](../api/ejreportviewer#members:pagesettings-height), and [`width`](../api/ejreportviewer#members:pagesettings-width) properties.

{% highlight javascript %}
        <script type="text/javascript">
            $(function () {
                $("#viewer").ejReportViewer({
                    reportServiceUrl: "/api/ReportsApi",
                    reportPath: '~/App_Data/Sales Order Detail.rdl',
                    printMode: true,
                    pageSettings: {
                        height: 11.69,
                        width: 8.27
                    }
                });
            });
        </script>
{% endhighlight %}

N> The values set in the height and width property is considered as inches input.

## Print report with images
When the report has more images, the browser will send the report stream to the print dialog before the images are completely loaded. To load the print report stream with complete images, you should set the `EmbedImageData` property to true in `OnInitReportOptions` as shown in the following code.

{% highlight c# %}
    public void OnInitReportOptions(ReportViewerOptions reportOption)
    {
        reportOption.ReportModel.EmbedImageData = true;
    }
{% endhighlight %}

Replace the following code sample in client side html file.

{% highlight javascript %}
        <script type="text/javascript">
            $(function () {
                $("#viewer").ejReportViewer(
                    {
                        reportServiceUrl: "/api/ReportsApi",
                        reportPath: '~/App_Data/Product Details.rdl'
                    });
            });
        </script>
{% endhighlight %}

N> In this tutorial, the `Product Details.rdl` report is used, and it can be downloaded from [here](http://www.syncfusion.com/downloads/support/directtrac/general/ze/Product_Details-1522024720).

## External styles in report printing
While printing report, the external styles are used in the application overrides printable page style and prints output with incorrect alignments. To avoid the external script overriding, set the `isStyleLoad` property to false, which will print the page using only the Report Viewer styles.

{% highlight javascript %}
        <script type="text/javascript">
            $(function () {
                $("#viewer").ejReportViewer(
                    {
                        reportServiceUrl: "/api/ReportsApi",
                        reportPath: '~/App_Data/Product Details.rdl',
                        reportPrint: "onReportPrint"
                    });
            });

            function onReportPrint(args) {
                args.isStyleLoad = false;
            }
        </script>
{% endhighlight %}

## Show print progress
Report Viewer provides events that help you to show the progress information when the printing takes a long time to complete.

1.Set the [`printProgressChanged`](../api/ejreportviewer#events:printprogresschanged) in Report Viewer initialization.
2.Implement the function and add code samples to show a custom message based on the print progress status as shown in the following code snippet. 

{% highlight javascript %}
        <script type="text/javascript">
            $(function () {
                $("#viewer").ejReportViewer({
                    reportServiceUrl: "/api/ReportsApi",
                    reportPath: '~/App_Data/Product Details.rdl',
                    printProgressChanged: "onPrintProgressChanged",
                });
            });

            function onPrintProgressChanged(args) {
                if (args.stage == "beginPrint") {
                    $('#viewer').ejWaitingPopup({ showOnInit: true, cssClass: "customStyle", text: "Preparing print data.. Please wait..." });
                }
                if (args.stage == "printStarted") {
                    var popupObj = $('#viewer').data('ejWaitingPopup');
                    popupObj.hide();
                }
                else if (args.stage == "preparation") {
                    console.log(args.stage);
                    if (args.preparationStage == "dataPreparation") {
                        console.log(args.preparationStage);
                        console.log(args.totalPages);
                        console.log(args.currentPage);
                        if (args.totalPages > 1 && args.currentPage > 1) {
                            var progressPercentage = Math.floor((args.currentPage / args.totalPages) * 100);
                            if (progressPercentage > 0) {
                                var popupObj = $('#viewer').data('ejWaitingPopup');
                                popupObj.setModel({ text: "Preparing print data.." + progressPercentage + " % completed.. Please wait..." });
                            }
                        }
                    }
                }

                args.handled = true;
            }
        </script>
{% endhighlight %}

## Remove empty spaces in printing
The extra blank page is created when the Body of your report is too wide for your page. If you want the report to appear on a single page, all the content within the report body must fit on the physical page and the body width should be lesser or equal to the following formula:

**Body Width <= Page Width - (Left Margin + Right Margin)**

For more details on designing a report to remove the empty pages in the report, refer to the knowledge base article of [report page sizing](https://www.syncfusion.com/kb/8622/how-to-avoid-the-extra-blank-pages-in-print-and-print-preview).
