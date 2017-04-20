---
layout: post
title: Defer-Update
description: defer update
platform: js
control: PivotGrid
documentation: ug
api: /api/js/ejpivotgrid
---

# Defer Update

I> This feature is applicable for OLAP datasource only at Server Mode.

Defer Update support allows you to refresh the control only on-demand and not during every UI interaction. 

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

![](Defer-Update_images/defer.png) 


