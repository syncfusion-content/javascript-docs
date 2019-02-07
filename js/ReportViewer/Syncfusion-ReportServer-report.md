---
layout: post
title: Report Server reports | Report Viewer | Syncfusion
description: Render Syncfusion Report Server deployed RDL reports using JavaScript Report Viewer.
platform: js
control: ReportViewer
documentation: ug
api: /api/js/ejreportviewer
---

# Load Syncfusion Report Server reports

You can render the Syncfusion Report Server reports in Report Viewer easily without creating a Web API service. It provides the built-in Web API service that helps to render the server reports.

1.Report Viewer requires the [`serviceAuthorizationToken`](../api/ejreportviewer#members:members:serviceauthorizationtoken) to connect and download the items from Syncfusion Report Server. Create token for the user by using server RESTful API, the following code used to generate the token.

{% highlight javascript %}
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
                        // Report Viewer initialization.
                    }
                });
            });
    </script>

{% endhighlight %}

2.Set the Syncfusion ReportServer built-in service URL to `reportServiceUrl` property. Assign the created token to [`serviceAuthorizationToken`](../api/ejreportviewer#members:members:serviceauthorizationtoken) and `reportPath` to a report deployed on server. You can use the following complete code in your HTML page.

{% highlight javascript %}
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
                                reportPath: '/Sample Reports/Company Sales'
                            });
                    }
                });
            });
    </script>
{% endhighlight %}

N> You can also load the report using guid instead of report location. Set the guid of the report in reportPath as like as “reportPath: ‘91f24bf1-e537-4488-b19f-b37f77481d00’”.

3.View the HTML file in web browser and the report result shows as in the following screenshot.

![Renders company sales report from Syncfusion Report Server](images/getting-started/company-sales-report.png)