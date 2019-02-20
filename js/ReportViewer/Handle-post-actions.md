---
layout: post
title: Handle Post Actions | Report Viewer | JavaScript | Syncfusion
description: Handling JavaScript Report Viewer post actions.  
platform: js
control: Report Viewer
documentation: ug
---

# Handle Post Actions
Report processing actions are sent in an Ajax request to exchange data with the Web API service. You can use the following Report Viewer events to customize the Ajax requests.

* `AjaxBeforeLoad`
* `AjaxSuccess`
* `AjaxError`

## AjaxBeforeLoad
This event can be triggered before an Ajax request is sent to the Report Viewer Web API service. It allows you to set additional headers, custom data in the Ajax request. The following code sample demonstrates adding custom authorization header and passing default parameter values to service.

### Add custom header in Ajax request
Initialize the [`ajaxBeforeLoad`](../api/ejreportviewer#events:ajaxbeforeload) event in the script and add the authorization token to the `headers` property

{% highlight javascript %}
    <script type="text/javascript">
        $(function () {
            $("#viewer").ejReportViewer({
                reportServiceUrl: "/api/ReportsApi",
                reportPath: '~/App_Data/Sales Order Detail.rdl',
                ajaxBeforeLoad: "onAjaxRequest",
            });
        });

        function onAjaxRequest(args) {
            args.headers.push({ Key: 'Authorization', Value: btoa('guest', 'demo@123') });
        }
    </script>
{% endhighlight %}

N> In this tutorial, the `Sales Order Detail.rdl` report is used, and it can be downloaded from [here](http://www.syncfusion.com/downloads/support/directtrac/general/ze/Sales_Order_Detail-1633189686).

Get the custom header value from the `HttpContext` header collection using the key name specified at client-side.

{% highlight c# %}
        string authenticationHeader;

        public object PostReportAction(Dictionary<string, object> jsonResult)
        {
            if (jsonResult != null)
            {
                //Get client side custom ajax header and store in local variable
                authenticationHeader = HttpContext.Current.Request.Headers["Authorization"];

                //Perform your custom validation here
                if (authenticationHeader == "")
                {
                    return new Exception("Authentication failed!!!");
                }
                else
                {
                    return ReportHelper.ProcessReport(jsonResult, this);
                }
            }

            return null;
        }
{% endhighlight %}

N> Perform your own action to validate the header values.

### Pass custom data in Ajax request
Use the `data` property to set custom data to the server in the Ajax request. In the following code sample, parameter values are passed to the server-side.

{% highlight javascript %}
        <script type="text/javascript">
            $(function () {
                $("#viewer").ejReportViewer({
                    reportServiceUrl: "/api/ReportsApi",
                    reportPath: '~/App_Data/Sales Order Detail.rdl',
                    ajaxBeforeLoad: "onAjaxRequest",
                });
            });

            function onAjaxRequest(args) {
                args.headers.push({ Key: 'Authorization', Value: btoa('guest', 'demo@123') });

                //Passing custom parameter data to server
                args.data = [{ name: 'SalesOrderNumber', labels: ['SO50756'], values: ['SO50756'] }];
            }
        </script>
{% endhighlight %}

The custom data values are stored in the `CustomData` header key, you can store it to the local property. The following code sample stores parameter values, then the values are set to report in the `OnReportLoaded` method.

{% highlight c# %}
        public string DefaultParameter = null;
        string authenticationHeader;

        public object PostReportAction(Dictionary<string, object> jsonResult)
        {
            if (jsonResult != null)
            {
                if (jsonResult.ContainsKey("CustomData"))
                {
                    //Get client side custom data and store in local variable. Here parameter values are sent.
                    DefaultParameter = jsonResult["CustomData"].ToString();
                }

                //Get client side custom ajax header and store in local variable
                authenticationHeader = HttpContext.Current.Request.Headers["Authorization"];

                //Perform your custom validation here
                if (authenticationHeader == "")
                {
                    return new Exception("Authentication failed!!!");
                }
                else
                {
                    return ReportHelper.ProcessReport(jsonResult, this);
                }
            }

            return null;
        }

        public void OnReportLoaded(ReportViewerOptions reportOption)
        {
            if (DefaultParameter != null)
            {
                //Set client side custom header data 
                reportOption.ReportModel.Parameters = JsonConvert.DeserializeObject<List<Syncfusion.Reports.EJ.ReportParameter>>(DefaultParameter);
            }
        }
{% endhighlight %}

## AjaxSuccess
To perform custom action or show user defined message, use the [`ajaxSuccess`](../api/ejreportviewer#events:ajaxsuccess) event on the successful Ajax request.

{% highlight javascript %}
        <script type="text/javascript">
            $(function () {
                $("#viewer").ejReportViewer({
                    reportServiceUrl: "/api/ReportsApi",
                    reportPath: '~/App_Data/Sales Order Detail.rdl',
                    ajaxBeforeLoad: "onAjaxRequest",
                    ajaxSuccess: "onAjaxSuccess",
                });
            });

            function onAjaxRequest(args) {
                args.headers.push({ Key: 'Authorization', Value: btoa('guest', 'demo@123') });

                //Passing custom parameter data to server
                args.data = [{ name: 'SalesOrderNumber', labels: ['SO50756'], values: ['SO50756'] }];
            }

            function onAjaxSuccess(args) {
                //Perform your custom success message here
                alert("Ajax request success!!!");
            }
        </script>
{% endhighlight %}

## AjaxError
The [`ajaxError`](../api/ejreportviewer#events:ajaxerror) event is called, if an error occurred with the request, you can display the customized error detail in the event method.

{% highlight javascript %}
        <script type="text/javascript">
            $(function () {
                $("#viewer").ejReportViewer({
                    reportServiceUrl: "/api/Reports",
                    reportPath: '~/App_Data/Sales Order Detail.rdl',
                    ajaxBeforeLoad: "onAjaxRequest",
                    ajaxError: "onAjaxFailure"
                });
            });

            function onAjaxRequest(args) {
                args.headers.push({ Key: 'Authorization', Value: btoa('guest', 'demo@123') });

                //Passing custom parameter data to server
                args.data = [{ name: 'SalesOrderNumber', labels: ['SO50756'], values: ['SO50756'] }];
            }

            function onAjaxFailure(args) {
                alert("Status: " + args.status + "\n" +
                    "Error: " + args.responseText);
            }
        </script>
{% endhighlight %}

N> You can never have both an error and a success callback with a request.
