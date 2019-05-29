---
layout: post
title: Defer-Update with PivotGrid widget for Syncfusion Essential JS
description: This document illustrates that how to enable defer-update in server mode of JavaScript PivotGrid control
platform: js
control: PivotGrid
documentation: ug
api: /api/js/ejpivotgrid
---

# Defer Update

I> This feature is applicable for the relational datasource only at server mode.

Defer update support allows you to refresh the control only on-demand and not during every UI interaction.

{% highlight js %}

  $(function() {
      $("#PivotGrid1").ejPivotGrid({
          url: "/RelationalService",
          afterServiceInvoke: "onServiceInvokes"
      });
  });

  function onServiceInvokes(args) {
      if (args.action == "initialize")
          $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({
              pivotControl: this,
              layout: ej.PivotSchemaDesigner.Layouts.Excel
          });
  }

{% endhighlight %}

![Defer update support in JavaScript pivot grid control](Defer-Update_images/relationaldeferupdate.png)



