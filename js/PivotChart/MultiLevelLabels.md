---
layout: post
title: Multi-level Labels
description: multilevellabels
platform: js
control: PivotChart
documentation: ug
---

# Multi-level labels

<<<<<<< HEAD
Multi-level labels allows you to drill down to access the detailed level of the data or drill up to see the summarized data by using the expander present in the OLAP chart. You can enable the option by setting the property [`enableMultiLevelLabels`](/api/js/ejchart#members:enablemultilevellabels) as **“true”.**
=======
Multi-level labels allow you to drill down to access the detailed level of data or drill up to see the summarized data by using the expander present in the OLAP chart. You can enable this option by setting the [`enableMultiLevelLabels`](/api/js/ejchart#members:enableMultiLevelLabels) property to **“true”.**
>>>>>>> hotfix/hotfix-v15.4.0.20

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

![](MultiLevelLabels_images/relational.png)

## OLAP

![](MultiLevelLabels_images/olap.png)

