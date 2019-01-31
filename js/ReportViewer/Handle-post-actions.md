---
layout: post
title: Handle Post Actions | ReportViewer | JavaScript | Syncfusion
description: Handling JavaScript Report Viewer post actions.  
platform: js
control: ReportViewer
documentation: ug
---

# Handle Post Actions
## AjaxBeforeLoad
This event triggered before an Ajax request is sent to Report Viewer Web API service. It allows you to set additional headers, custom data. Here in the following code sample demonstrates adding custom authorization header and passing default parameter value to service.

### Add custom header in ajax request
Initialize the `ajaxBeforeLoad` event in script and add the authorization token to `headers` property.

{% highlight javascript %}
    <script type="text/javascript">
            $(function () {
                $("#container").ejReportViewer({
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

Get the custom header value from HttpContext header collection using the key name specified at client side.

{% highlight c# %}
        public object PostReportAction(Dictionary<string, object> jsonResult)
        {
            if (jsonResult != null)
            {
                authenticationHeader = HttpContext.Current.Request.Headers["Authorization"];

                //Perform your custom validation here
                if (authenticationHeader == "")
                {
                    return new Exception("Authentication failed!!!");
                }
            }

            return ReportHelper.ProcessReport(jsonResult, this);
        }
{% endhighlight %}

N> Perform your own action to validate the header values.

### Pass custom data in ajax request
Use the `data` property to set custom data to server in ajax request. Here in the below code sample, parameter values are passed to server side.

{% highlight javascript %}
    <script type="text/javascript">
            .....
            function onAjaxRequest(args) {
                args.headers.push({ Key: 'Authorization', Value: btoa('guest', 'demo@123') });

                //Passing custom parameter data to server
                args.data = [{ name: 'SalesOrderNumber', labels: ['SO50756'], values: ['SO50756'] }];
            }
    </script>
{% endhighlight %}

The custom data values are stored in `CustomData` header key, you can store it to local property. The following code sample stores parameter values, then values are set to report in `OnReportLoaded` method.

{% highlight c# %}
    public class ReportsApiController : ApiController, IReportController
    {
        public string DefaultParameter = null;
        string authenticationHeader;

        public object PostReportAction(Dictionary<string, object> jsonResult)
        {

            if (jsonResult != null)
            {
                if (jsonResult.ContainsKey("CustomData"))
                {
                    DefaultParam = jsonResult["CustomData"].ToString();
                }

                authenticationHeader = HttpContext.Current.Request.Headers["Authorization"];

                //Perform your custom validation here
                if (authenticationHeader == "")
                {
                    return new Exception("Authentication failed!!!");
                }
            }

            return ReportHelper.ProcessReport(jsonResult, this);
        }

        public void OnReportLoaded(ReportViewerOptions reportOption)
        {
            if (DefaultParameter != null)
            {
                reportOption.ReportModel.Parameters = JsonConvert.DeserializeObject<List<Syncfusion.Reports.EJ.ReportParameter>>( DefaultParameter);
            }
        }
    }
{% endhighlight %}

## AjaxSucess
To perform custom action or show user defined message, when an ajax request was successful you can use the `ajaxSuccess` event.

{% highlight javascript %}
    <script type="text/javascript">
            $(function () {
                $("#container").ejReportViewer({
                    reportServiceUrl: "/api/ReportsApi",
                    reportPath: '~/App_Data/Sales Order Detail.rdl',
                    ajaxSuccess:"onAjaxSuccess",
                });
            });

            function onAjaxSuccess(args) {
                //Perform your custom success action here
                //alert("Ajax reque success!!!");
            }
    </script>
{% endhighlight %}

## AjaxError
The `ajaxError` event is called if an error occurred with the request, you can display the customized error detail in the event method.

{% highlight javascript %}
    <script type="text/javascript">
            $(function () {
                $("#container").ejReportViewer({
                    reportServiceUrl: "/api/ReportsApi",
                    reportPath: '~/App_Data/Sales Order Detail.rdl',
                    ajaxSuccess:"onAjaxSuccess",
                    ajaxError:"onAjaxFailure"
                });
            });

            function onAjaxSuccess(args) {
                //Perform your custom success action here
                //alert("Authentication success!!!");
            }

            function onAjaxFailure(args) {
                alert("Status: " + args.status + "\n" +
                    "Error: " + args.statusText);
            }
    </script>
{% endhighlight %}

N> You can never have both an error and a success callback with a request.
