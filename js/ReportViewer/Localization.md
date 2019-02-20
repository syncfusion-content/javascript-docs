---
layout: post
title: Localization | JavaScript Report Viewer | Syncfusion
description: Localize Report Viewer static text based on a specific culture.
platform: js
control: Report Viewer
documentation: ug
---

# Localization
You can localize the Report Viewer static text and tooltip. To render the static text with specific culture, refer to the corresponding culture script and set culture name to the [`locale`](../api/ejreportviewer#members:locale) property of the Report Viewer.

{% highlight html %}
<head>
    <title>Render Report Viewer in French localization</title>
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <script src="http://code.jquery.com/jquery-1.10.2.min.js" type="text/javascript"></script>
    <script src="http://cdnjs.cloudflare.com/ajax/libs/jquery-easing/1.3/jquery.easing.min.js" type="text/javascript"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js" type="text/javascript"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/l10n/ej.localetexts.fr-FR.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/i18n/ej.culture.fr-FR.min.js"></script>
</head>
<body>
    <div style="height: 600px; width: 950px;">
        <!-- Creating a div tag which will act as a container for ejReportViewer widget.-->
        <div style="height: 600px; width: 950px; min-height: 400px;" id="viewer"></div>
        <!-- Setting property and initializing ejReportViewer widget.-->
        <script type="text/javascript">
            $(function () {
                var dataValue = "";
                var apiRequest = new Object();
                apiRequest.password = "demo";
                apiRequest.userid = "guest";
                $.ajax({
                    type: "POST",
                    url: "https://reportserver.syncfusion.com/api/get-user-key",
                    data: apiRequest,
                    success: function (data) {
                        dataValue = data.Token;
                        var token = JSON.parse(dataValue);

                        $("#viewer").ejReportViewer(
                            {
                                reportServiceUrl: "https://reportserver.syncfusion.com/ReportService/api/Viewer",
                                serviceAuthorizationToken: token["token_type"] + " " + token["access_token"],
                                reportPath: '/Sample Reports/Sales Order Detail',
                                //Render Report Viewer in French locale
                                locale: "fr-FR"
                            });
                    }
                });
            });
        </script>
    </div>
</body>
{% endhighlight %}

N> Refer to the [Localization](../localization) document to get the culture specific script files.

![Renders Report Viewer in French localization](images/localization.png)

View the online Report Viewer localization demo [here](https://js.syncfusion.com/demos/web/#!/bootstrap/reportviewer/localization).
