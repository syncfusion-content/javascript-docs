---
layout: post
title: Multi-level Labels with PivotChart widget for Syncfusion Essential JS
description: multilevellabels
platform: js
control: PivotChart
documentation: ug
---

# Multi-level labels

Multi-level labels allow you to drill down to access the detailed level of data or drill up to see the summarized data by using the expander present in the OLAP chart. You can enable this option by setting the [`enableMultiLevelLabels`](/api/js/ejpivotchart#members:enablemultilevellabels) property to **“true”.**

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart(
    {
        //..
        //Enable Multi-level Labels
        enableMultiLevelLabels: true,
        //..
    });
{% endhighlight %}


## Relational

![Multi-level labels in JavaScript pivot chart with relational mode](MultiLevelLabels_images/relational.png)

## OLAP

![Multi-level labels in JavaScript pivot chart OLAP mode](MultiLevelLabels_images/olap.png)

