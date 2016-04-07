---
layout: post
title: Defer-Update
description: defer update
platform: js
control: PivotGrid
documentation: ug
---

# Defer Update

I> This feature is applicable for Relational datasource only at Server Mode.

Defer Update support allows you to refresh the control only on-demand and not during every UI interaction.

{% highlight js %}

  $(function() {
      $("#PivotGrid1").ejPivotGrid({
          url: "../RelationalService",
          afterServiceInvoke: "onServiceInvokes"
      });
  });

  function onServiceInvokes(args) {
      if (args.action == "initialize")
          $("#PivotSchemaDesigner").ejPivotSchemaDesigner({
              pivotControl: this,
              layout: ej.PivotSchemaDesigner.Layouts.Excel
          });
  }
  
{% endhighlight %}

![](/Defer-Update_images/relationaldeferupdate.png) 



