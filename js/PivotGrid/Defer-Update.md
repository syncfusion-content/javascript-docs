---
layout: post
title: Defer-Update
description: defer update
platform: js
control: PivotGrid
documentation: ug
---

# Defer Update

Defer Update support will allow user to refresh the control only on-demand and not during every UI interaction. To enable this functionality, we need to set `enableDeferUpdate` property to "true".

The following code example explains on how to enable Defer Update in the PivotGrid control.

{% highlight js %}

$(function()
{
    $("#PivotGrid").ejPivotGrid(
    {
        url: "../wcf/OLAPService.svc",
        analysisMode: ej.PivotGrid.AnalysisMode.OlapAnalysis,
        enableDeferUpdate: true,
        afterServiceInvoke: "onServiceInvokes"
    });
});

function onServiceInvokes(args)
{
    if (args.action == "initialize") $("#PivotSchemaDesigner").ejPivotSchemaDesigner(
    {
        pivotControl: this,
        layout: ej.PivotSchemaDesigner.Layouts.Excel
    });
}

{% endhighlight %}

{% include image.html url="/js/PivotGrid/Defer-Update_images/Defer-Update_images1.png" %}






