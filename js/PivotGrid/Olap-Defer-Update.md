---
layout: post
title: Defer-Update with PivotGrid widget for Syncfusion Essential JS
description: defer update
platform: js
control: PivotGrid
documentation: ug
api: /api/js/ejpivotgrid
---

# Defer Update

I> This feature is applicable for the OLAP datasource only at server mode.

Defer update support allows you to refresh the control only on-demand and not during every UI interaction.

{% highlight js %}

$(function() {
    $("#PivotGrid1").ejPivotGrid({
        url: "/OLAPService",
        afterServiceInvoke: "onServiceInvokes"
    });
});

function onServiceInvokes(args) {
    if (args.action == "initialize") $("#PivotSchemaDesigner").ejPivotSchemaDesigner({
        pivotControl: this,
        layout: ej.PivotSchemaDesigner.Layouts.Excel
    });
}

{% endhighlight %}

![Defer update in JavaScript pivot grid OLAP server mode](Defer-Update_images/defer.png)


