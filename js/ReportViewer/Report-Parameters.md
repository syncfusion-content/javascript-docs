---
layout: post
title: Report Parameters
description: report parameters
platform: js
control: ReportViewer
documentation: ug
api: /api/js/ejreportviewer
---

# Report Parameters

The ReportViewer has support to add report Parameters to ReportViewer at runtime. The ReportViewer has `parameters` property that is the list of ReportParameter type to add collection of report parameters to it. You can add report parameters either through ReportViewer model when creating ReportViewer control or through Web API.

The following code example illustrates how to add ReportParameter at control creation.

{% highlight javascript %}

$("#viewer").ejReportViewer({
    reportServiceUrl: "/api/SSRSReport",
    processingMode: ej.ReportViewer.ProcessingMode.Remote,
    reportPath: "~/InvoiceTemplate",
    parameters: [{
        name: 'InvoiceID',
        labels: ['InvoiceID'],
        values: [10250],
        nullable: false
    }]
});

{% endhighlight %}

The following code example illustrates how to add ReportParameter in Web API.

{% highlight c# %}

public class ReportsController : ApiController, IReportController
{
    /// <summary>
    /// Report Initialization method that is triggered when report begins to be processed.
    /// </summary>
    /// <param name="reportOptions">The ReportViewer options.</param>
    public void OnInitReportOptions(ReportViewerOptions reportOptions)
    {
        List<ReportParameter> parameters = new List<ReportParameter>();
        parameters.Add(new ReportParameter() { Name = "InvoiceID", Labels = new List<string>() { "InvoiceID" }, Values = new List<string>() { "10250" } });
        reportOptions.ReportModel.Parameters = parameters;
    }        
}

{% endhighlight %}



