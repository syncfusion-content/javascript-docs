---
layout: post
title: Toolbar Customization | Report Viewer | Syncfusion
description: toolbar customization
platform: js
control: ReportViewer
documentation: ug
api: /api/js/ejreportviewer
---

# Toolbar Customization
You can hide the component toolbar to show customized user interface or to customize the toolbar icons and element’s appearances using the templates and Report Viewer properties.  

## Hide parameter block and toolbar items
To hide toolbar items, set the [`toolbarSettings`](../api/ejreportviewer#members:toolbarsettings) property. The following code can be used to remove the parameter option from the toolbar and hide the parameter block.

{% highlight javascript %}
        <script type="text/javascript">
            $(function () {
                $("#viewer").ejReportViewer({
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
        .....
        $(function () {
            $("#container").ejReportViewer(
                {
                    reportServiceUrl: "/api/ReportsApi",
                    reportPath: '~/App_Data/Sales Order Detail.rdl',
                    toolbarSettings:{ showToolbar: true },
                });
        });
    </script>

{% endhighlight %}

## Decide the export option
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
To add custom items to the export drop-down available in the Report Viewer toolbar, use the property [`customExportItems`](../api/ejreportviewer#members:members:exportsettings-customexportitems) and provide the JSON array of collection input with the index, cssClass name, and value properties as given in following code snippet.

{% highlight javascript %}
            $(function () {
            $("#container").ejReportViewer(
                {
                    reportServiceUrl: "/api/ReportsApi ",
                    reportPath: '~/App_Data/Sales Order Detail.rdl',
                    exportSettings: {
                        customExportItems: [{
                            index: 5,
                            cssClass: 'e-icon e-mail e-reportviewer-icon',
                            value: 'Mail Template',
                        }]
                    },
                });
        });
        function customExport(args) {
            alert("Export clicked !!!");
        }

{% endhighlight %}

## Add custom option to toolbar
The properties [`customToolBarItems`](../api/ejreportviewer#members:members:toolbarsettings-customtoolbaritems) and [`customToolBarGroups`](../api/ejreportviewer#members:members:toolbarsettings-customtoolbargroups) are used to add custom toolbar items to the Report Viewer toolbar. It takes JSON array input with index, cssClass name, tooltip, and event to fire by clicking it. following code adds an email option to the toolbar.

{% highlight javascript %}
            $(function () {
            $("#container").ejReportViewer(
                {
                    reportServiceUrl: "/api/ReportsApi",
                    reportPath: '~/App_Data/Sales Order Detail.rdl',
                    toolbarSettings:{ showToolbar: true },
                    //exportSettings: { exportOptions:ej.ReportViewer.ExportOptions.All & ~ej.ReportViewer.ExportOptions.Html },
                    toolbarSettings: { click: 'customExport' },
                    exportSettings: {
                        index: 2,
                        customExportItems: [{
                            index: 2,
                            cssClass: '',
                            value: 'Custom',
                        },
                        {
                            index: 4,
                            cssClass: '',
                            value: 'Custom2',
                        }]
                    },
                    toolbarSettings: {
                        customToolBarGroups: [{
                            items: [{
                                groupIndex: 1,
                                index: 3,
                                cssClass: "span.e-icon e-mail e-reportviewer-icon",
                                tooltip: 'CustomGroup',
                                click: 'customExport1'
                            }]
                        }],
                        customToolBarItems: [{
                            groupIndex: 2,
                            index: 2,
                            cssClass: "span.e-icon e-mail e-reportviewer-icon",
                            tooltip: 'CustomItem',
                            click: '2'
                        }]
                    }
                });
        });
        function customExport(args) {
            alert("Export clicked !!!");
            // document.getElementById(args.target.id).innerHTML = "YOU CLICKED ME!";
        }
{% endhighlight %}