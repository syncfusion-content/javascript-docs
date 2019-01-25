---
layout: post
title: Localization | JavaScript ReportViewer | Syncfusion
description: Localize Report Viewer static text based on a specific culture.
platform: js
control: ReportViewer
documentation: ug
---

# Localization

Report Viewer supports to localize its static text and tooltip. To render the static with specific culture, refer the corresponding culture script and set culture name in [`locale`](../api/ejreportviewer#members:locale) property of Report Viewer.

{% highlight html %}

<head>
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <script src="http://code.jquery.com/jquery-1.10.2.min.js" type="text/javascript"></script>
    <script src="http://cdnjs.cloudflare.com/ajax/libs/jquery-easing/1.3/jquery.easing.min.js" type="text/javascript"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js" type="text/javascript"></script>
    <script src="Scripts/l10n/ej.localetexts.fr-FR.min.js"></script>
    <script src="Scripts/i18n/ej.culture.fr-FR.min.js"></script>
</head>
<body style="overflow: hidden; position: static; height: 100%; width: 100%;">
    <div id="container" style="position: absolute; height: 100%; width: 100%;"></div>
    <script type="text/javascript">
        $(function () {
            $("#container").ejReportViewer(
                {
                    reportServiceUrl: '/api/ReportsApi',
                    processingMode: ej.ReportViewer.ProcessingMode.Remote,
                    reportPath: '~/App_Data/Sales Order Detail.rdl',
                    //Render Report Viewer in French locale
                    locale: "fr-FR"
                });
        });
    </script>
</body>

{% endhighlight %}

![Renders Report Viewer in French localization](Localization_images\report-viewer-localization.png)

You can view the online Report Viewer localization demo [here](https://js.syncfusion.com/demos/web/#!/bootstrap/reportviewer/localization).

