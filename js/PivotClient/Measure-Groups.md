---
layout: post
title: Measure-Groups
description: measure groups 
platform: js
control: PivotClient
documentation: ug
---

# Measure Groups 

I> This feature is applicable only for OLAP data source bound from server-side.

In Cube Dimension Browser, treeview can be viewed in a filtered manner through the Measure Groups option. This feature allows you to view the list of measures and dimensions associated with the selected measure group from the cube. For enabling this, the [`enableMeasureGroups`](/js/api/ejpivotclient#members:enablemeasuregroups) property is set to true. By default, its value is set to false.

{% highlight javascript %}

    $("#PivotClient1").ejPivotClient({
        url: "/OlapClient",
        title: "OLAP Browser",
        enableMeasureGroups: true
    });

{% endhighlight %}

On selecting a measure group from the drop-down list, the Cube Dimension Browser treeview displays the related measures and dimensions alone as follows.

![](Measure-Groups_images/beforemeasure.png)

![](Measure-Groups_images/aftermeasure.png)

