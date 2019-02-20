---
layout: post
title: Toolbar Customization | Report Viewer | Syncfusion
description: toolbar customization
platform: js
control: Report Viewer
documentation: ug
api: /api/js/ejreportviewer
---

# Toolbar Customization
You can hide the component toolbar to show customized user interface or to customize the toolbar icons and element’s appearances using the templates and Report Viewer properties.  

N> In this tutorial, the `Sales Order Detail.rdl` report is used, and it can be downloaded from [here](http://www.syncfusion.com/downloads/support/directtrac/general/ze/Sales_Order_Detail-1633189686). You can add the reports from Syncfusion installation location. For more information, see [Samples and demos](/js/reportviewer/samples-and-demos).

## Hide parameter block and toolbar items
To hide toolbar items, set the [`toolbarSettings`](../api/ejreportviewer#members:toolbarsettings) property. The following code can be used to remove the parameter option from the toolbar and hide the parameter block.

{% highlight javascript %}
        <script type="text/javascript">
            $(function () {
                $("#viewer").ejReportViewer({
                    reportServiceUrl: "/api/ReportsApi",
                    reportPath: '~/App_Data/Sales Order Detail.rdl',
                    toolbarSettings: {
                        items: ej.ReportViewer.ToolbarItems.All & ~ej.ReportViewer.ToolbarItems.Parameters
                    }
                });
            });
        </script>
{% endhighlight %}

The following code sample hides the print options from the toolbar items.

{% highlight javascript %}
        <script type="text/javascript">
            $(function () {
                $("#viewer").ejReportViewer({
                    reportServiceUrl: "/api/ReportsApi",
                    reportPath: '~/App_Data/Sales Order Detail.rdl',
                    toolbarSettings: {
                        items: ej.ReportViewer.ToolbarItems.All & ~ej.ReportViewer.ToolbarItems.Print
                    }
                });
            });
        </script>
{% endhighlight %}


Similarly, you can show or hide all other toolbar options with the help of [`toolbarSettings.items`](../api/ejreportviewer#members:toolbarsettings-items) enum.

## Hide toolbar
To hide the Report Viewer toolbar set the [`showToolbar`](../api/ejreportviewer#members:members:toolbarsettings-showtoolbar) property to false.

{% highlight javascript %}
        <script type="text/javascript">
            $(function () {
                $("#viewer").ejReportViewer({
                    reportServiceUrl: "/api/ReportsApi",
                    reportPath: '~/App_Data/Sales Order Detail.rdl',
                    toolbarSettings: { showToolbar: false }
                });
            });
        </script>
{% endhighlight %}


## Decide or hide the export option
The Report Viewer provides the [`exportOptions`](../api/ejreportviewer#members:members:exportsettings-exportoptions) property to show or hide the default export types available in the component. The following code hides the HTML export type from the default export options. 

{% highlight javascript %}
    <script type="text/javascript">
        ....
        $(function () {
            $("#container").ejReportViewer(
                {
                    reportServiceUrl: "/api/ReportsApi ",
                    reportPath: '~/App_Data/Sales Order Detail.rdl',
                    exportSettings: { exportOptions:ej.ReportViewer.ExportOptions.All & ~ej.ReportViewer.ExportOptions.Html }
                });
        });
    </script>
{% endhighlight %}


## Add custom items to the export drop-down
To add custom items to the export drop-down available in the Report Viewer toolbar, use the property [`customItems`](../api/ejreportviewer#members:members:exportsettings-customitems) and provide the JSON array of collection input with the `index`, `cssClass` name, and `value` properties. Register the `exportItemClick` event to handle the custom item actions as given in following code snippet..

{% highlight javascript %}
        <script type="text/javascript">
            $(function () {
                $("#viewer").ejReportViewer({
                    reportServiceUrl: "/api/ReportsApi",
                    reportPath: '~/App_Data/Sales Order Detail.rdl',
                    exportSettings: {
                        excelFormat: ej.ReportViewer.ExcelFormats.Excel2013,
                        wordFormat: ej.ReportViewer.WordFormats.Word2013,
                        exportOptions: ej.ReportViewer.ExportOptions.All & ~ej.ReportViewer.ExportOptions.Html,
                        customItems: [{
                            index: 2,
                            cssClass: '',
                            value: 'Text File',
                        },
                        {
                            index: 4,
                            cssClass: '',
                            value: 'DOT',
                        }]
                    },
                    exportItemClick: 'onExportItemClick'
                });
            });

            //Export click event handler
            function onExportItemClick(args) {
                if (args.value == "Text File") {
                    //Implement the code to export report as Text
                } else if (args.value == "DOT") {
                    //Implement the code to export report as DOT
                }
            }
        </script>
{% endhighlight %}


## Add custom toolbar item
You can add custom items to Report Viewer toolbar using the [`toolbarSettings`](../api/ejreportviewer#members:members:toolbarsettings) property. You must register the `toolBarItemClick` event to handle the newly added custom items action. 

### Add custom item to exiting toolbar group
To add a custom item to existing toolbar group use the property [`customItems`](../api/ejreportviewer#members:members:toolbarsettings-customitems) in `toolbarSettings` and provide the JSON array of collection input with the `groupIndex`, `index`, `itemType`, `cssClass` name, and `tooltip` properties as given in following code snippet. 

{% highlight javascript %}
        <script type="text/javascript">
            $(function () {
                $("#viewer").ejReportViewer({
                    reportServiceUrl: "/api/ReportsApi",
                    reportPath: '~/App_Data/Sales Order Detail.rdl',
                    toolbarSettings: {
                        showToolbar: true,
                        items: ej.ReportViewer.ToolbarItems.All & ~ej.ReportViewer.ToolbarItems.Print,
                        customItems: [{
                            groupIndex: 1,
                            index: 1,
                            itemType: 'Default',
                            cssClass: "e-icon e-mail e-reportviewer-icon CustomItem",
                            tooltip: { header: 'CustomItem', content: 'toolbaritems', value: 'CustomItem' },
                        }]

                    },
                    toolBarItemClick: 'ontoolBarItemClick',
                });
            });

            //Toolbar click event handler
            function ontoolBarItemClick(args) {
                if (args.value == "CustomItem") {
                    //Implement the code to CustomItem toolbar option
                }
            }
        </script>
{% endhighlight %}

### Add new toolbar group
To add new toolbar group and custom items to it, use the property [`customGroups`](../api/ejreportviewer#members:members:toolbarsettings-customgroups) in `toolbarSettings` and provide the JSON array of collection input with the `groupIndex`, `items` properties. The `items` must have the properties `itemType`, `cssClass` and `tooltip` as given in following code snippet. 

{% highlight javascript %}
        <script type="text/javascript">
            $(function () {
                $("#viewer").ejReportViewer({
                    reportServiceUrl: "/api/ReportsApi",
                    reportPath: '~/App_Data/Sales Order Detail.rdl',
                    toolbarSettings: {
                        customGroups: [{
                            items: [{
                                itemType: 'Default',
                                cssClass: "e-icon e-mail e-reportviewer-icon CustomGroup",
                                tooltip: { header: 'CustomGroup', content: 'toolbargroups', value: 'CustomGroup' },
                            },
                            {
                                itemType: 'Default',
                                cssClass: "e-icon e-mail e-reportviewer-icon subCustomGroup",
                                tooltip: { header: 'subCustomGroup', content: 'subtoolbargroups', value: 'subCustomGroup' },
                            }],
                            groupIndex: 3
                        }],
                    },
                    toolBarItemClick: 'ontoolBarItemClick',
                });
            });

            //Toolbar click event handler
            function ontoolBarItemClick(args) {
                if (args.value == "CustomGroup") {
                    //Implement the code to CustomGroup toolbar option
                }
                if (args.value == "subCustomGroup") {
                    //Implement the code to subCustomGroup toolbar option
                }
            }
        </script>
{% endhighlight %}