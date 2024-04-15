---
layout: post
title: Defer-update in JavaScript PivotGrid Control | Syncfusion
description: Learn here all about how to enable defer update at server mode in Syncfusion JavaScript PivotGrid control, it's elements and more.
platform: js
control: PivotGrid
documentation: ug
api: /api/js/ejpivotgrid
---

# Defer update in JavaScript PivotGrid

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



