---
layout: post
title: Measure-Groups
description: measure groups 
platform: js
control: PivotClient
documentation: ug
api: /api/js/ejpivotclient
---

# Measure groups

I> This feature is applicable only for the OLAP data source bound from the server-side.

In cube dimension browser, the tree view can be viewed in a filtered manner through the measure groups option. This feature allows you to view the list of measures and dimensions associated with the selected measure group from the cube. For enabling this, the [`enableMeasureGroups`](/api/js/ejpivotclient#members:enablemeasuregroups) property is set to true. By default, its value is set to false.

{% highlight javascript %}

    $("#PivotClient1").ejPivotClient({
        url: "/OlapClient",
        title: "OLAP Browser",
        enableMeasureGroups: true
    });

{% endhighlight %}

When you select a measure group from the drop-down list, the tree view of the cube dimension browser will display the related measures and dimensions as follows:

![](Measure-Groups_images/beforemeasure.png)

![](Measure-Groups_images/aftermeasure.png)

