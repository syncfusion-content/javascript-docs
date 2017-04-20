---
layout: post
title: Layout
description: layout 
platform: js
control: PivotGauge
documentation: ug
api: /api/js/ejpivotgauge
---

# Layout

## Row-wise Layout 

Gauges can be arranged in specified number of rows by using the [`rowsCount`](/api/js/ejpivotgauge#members:rowscount) property.

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({
        //....
        rowsCount: 2
    });

{% endhighlight %}

![](Layout_images/Row-wiseLayout.png) 

## Column-wise Layout

Gauges can be arranged in specified number of columns by using the [`columnsCount`](/api/js/ejpivotgauge#members:columnscount) property.

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({
        //....
        columnsCount: 2,
    });

{% endhighlight %}

![](Layout_images/Column-wiseLayout.png)

