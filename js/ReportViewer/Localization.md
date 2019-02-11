---
layout: post
title: Localization | JavaScript ReportViewer | Syncfusion
description: Localize Report Viewer static text based on a specific culture.
platform: js
control: ReportViewer
documentation: ug
---

# Localization

You can localize the Report Viewer static text and tooltip. To render the static text with specific culture, refer to the corresponding culture script and set culture name to the [`locale`](../api/ejreportviewer#members:locale) property of the Report Viewer.

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

N> Refer to the [Localization](../localization) document to get the culture specific script files.

![Renders Report Viewer in French localization](images/localization.png)

View the online Report Viewer localization demo [here](https://js.syncfusion.com/demos/web/#!/bootstrap/reportviewer/localization).
