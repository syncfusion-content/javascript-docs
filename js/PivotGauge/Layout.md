---
layout: post
title: Layout in JavaScript PivotGauge Control | Syncfusion
description: Learn here all about how to define layouts and its functionalities in Syncfusion JavaScript PivotGauge control, it's elements and more.
platform: js
control: PivotGauge
documentation: ug
api: /api/js/ejpivotgauge
---

# Layout in JavaScript PivotGauge

## Row-wise layout
Gauges can be arranged in the specified number of rows by using the [`rowsCount`](/api/js/ejpivotgauge#members:rowscount) property.

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({
        //....
        rowsCount: 2
    });

{% endhighlight %}

![Row-wise layout in JavaScript pivot gauge control](Layout_images/Row-wiseLayout.png) 

## Column-wise layout

Gauges can be arranged in the specified number of columns by using the [`columnsCount`](/api/js/ejpivotgauge#members:columnscount) property.

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({
        //....
        columnsCount: 2,
    });

{% endhighlight %}

![Column-wise layout in JavaScript pivot gauge control](Layout_images/Column-wiseLayout.png)

