---
layout: post
title: Collapse by default
description: Collapse by default
platform: js
control: PivotGrid
documentation: ug
api: /api/js/ejpivotgrid
---

# Collapse by default

I> This feature is applicable only for the relational datasource.

Allows you to collapse all members displayed in the grid. You can enable collapsing all members by default in the PivotGrid by setting the [`enableCollapseByDefault`](/api/js/ejpivotgrid#members:enablecollapsebydefault) property to true.

{% highlight js %}
   
    $(function() {
        $("#PivotGrid1").ejPivotGrid({
            //..
            enableCollapseByDefault:true
        });
    });

{% endhighlight %}

![](Collapsed-By-Default_images/Collapse-members.png)

