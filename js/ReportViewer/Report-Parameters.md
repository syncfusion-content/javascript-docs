---
layout: post
title: Report Parameters | Report Viewer | Syncfusion
description: report parameters
platform: js
control: ReportViewer
documentation: ug
api: /api/js/ejreportviewer
---

# Report Parameters

Report Viewer allows to pass or set report parameters default values at runtime. It provides [`parameters`](../api/ejreportviewer#members:parameters) property to set values of report parameters. You can set report parameters while creating ReportViewer control in script or in Web API Controller.

## Set parameter at client
The [`parameters`](../api/ejreportviewer#members:parameters) property takes JSON array values with parameter details such as name, prompt, labels, values, and nullable. 
1.Set the default value to the [`values`](../api/ejreportviewer#members:parameters-values) property and name of the report parameter to [`name`](../api/ejreportviewer#members:parameters-name) property.

N> The parameter name is case sensitive, it should be same as available in the report definition.

2.The following code example illustrates how to set ReportParameter in script.

{% highlight javascript %}
    <script type="text/javascript">
            $(function () {
                $("#viewer").ejReportViewer({
                    reportServiceUrl: "/api/ReportsApi",
                    reportPath: '~/App_Data/Sales Order Detail.rdl',
                    parameters: [{ name: 'SalesOrderNumber', labels: ['SO50751'], values: ['SO50751'] }]
                });
            });
    </script>

{% endhighlight %}

3.Run the application and the result shown as in below screenshot.

![Sales order detail report preview](images/report-parameter/set-paramerter-at-client.png)

## Set parameters in Web API Controller
To set parameter default value in Web API Controller, use the following code in `OnReportLoaded` method.

{% highlight c# %}
public void OnReportLoaded(ReportViewerOptions reportOption)
{
    List<Syncfusion.Reports.EJ.ReportParameter> userParameters = new List<Syncfusion.Reports.EJ.ReportParameter>();
    userParameters.Add(new Syncfusion.Reports.EJ.ReportParameter()
    {
        Name = "SalesOrderNumber",
        Values = new List<string>() { "SO50756" }
    });
    reportOption.ReportModel.Parameters = userParameters;
}
{% endhighlight %}

## Get report parameter
The `ReportHelper` class provides methods that helps to get the report parameters used in report. The following helper methods used to get parameter with or without values.

<table>
<tr>
<th>
Methods</th><th>
Description</th></tr>
<tr>
<td>
GetParameters</td><td>
Returns the parameters that are used in the current report without the processed values.</td></tr>
<tr>
<td>
GetParametersWithValues</td><td>
Returns the report parameters with processed data values that are used in the current report.</td></tr>
</table>

You can use the below code sample to get parameter names and set parameter default values.

{% highlight c# %}
    public class ReportsApiController : ApiController, IReportController
    {
        Dictionary<string, object> jsonArray = null;
        public object PostReportAction(Dictionary<string, object> jsonResult)
        {
            jsonArray = jsonResult;
            return ReportHelper.ProcessReport(jsonResult, this);
        }

        public void OnReportLoaded(ReportViewerOptions reportOption)
        {
            var reportParameters = ReportHelper.GetParameters(jsonArray, this);
            List<Syncfusion.Reports.EJ.ReportParameter> setParameters = new List<Syncfusion.Reports.EJ.ReportParameter>();

            if (reportParameters != null)
            {
                foreach (var rptParameter in reportParameters)
                {
                    setParameters.Add(new Syncfusion.Reports.EJ.ReportParameter()
                    {
                        Name = rptParameter.Name,
                        Values = new List<string>() { "SO50756" }
                    });
                }

                reportOption.ReportModel.Parameters = setParameters;
            }
        }
    }
{% endhighlight %}