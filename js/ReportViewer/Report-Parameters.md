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

The ReportViewer has support to add report Parameters to ReportViewer at runtime. The ReportViewer has `parameters` property that is the list of ReportParameter type to add collection of report parameters to it. You can add report parameters when creating ReportViewer control in JavaScript platform.

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
