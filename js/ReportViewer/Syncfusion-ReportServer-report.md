---
layout: post
title: Report Server reports | Report Viewer | Syncfusion
description: Render Syncfusion Report Server deployed RDL reports using JavaScript Report Viewer.
platform: js
control: Report Viewer
documentation: ug
api: /api/js/ejreportviewer
---

# Load Syncfusion Report Server reports

You can render the Syncfusion Report Server hosted reports in the Report Viewer easily without creating a Web API service. Syncfusion Report Server provides the built-in Web API service that helps you to display the server reports.

1.The Report Viewer requires the [`serviceAuthorizationToken`](../api/ejreportviewer#members:members:serviceauthorizationtoken) to connect and download the items from the Syncfusion Report Server. Create a token for the user by using the server RESTful API, the following code is used to generate the token.

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

2.Set the Syncfusion Report Server built-in service URL to the `reportServiceUrl` property. Assign the created token to [`serviceAuthorizationToken`](../api/ejreportviewer#members:members:serviceauthorizationtoken) and `reportPath` to a report deployed on the server. You can use the following complete code in your HTML page.

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

T> You can also load the report using Guid instead of report location. Set the Guid of the report in `reportPath` as like as `reportPath: ‘91f24bf1-e537-4488-b19f-b37f77481d00’`.

3.View the HTML file in a web browser and the report result shows as in the following screenshot.
![Renders company sales report from Syncfusion Report Server](images/getting-started/company-sales-report.png)