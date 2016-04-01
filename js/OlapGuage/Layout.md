---
layout: post
title: Layout
description: layout 
platform: js
control: OlapGauge
documentation: ug
---

# Layout

##Row-wise Layout 

Gauges can be arranged in specified number of rows by using the [`rowsCount`](/js/api/ejolapgauge#members:rowscount) property.

{% highlight javascript %}

$("#OlapGauge1").ejOlapGauge({
    url: "../OlapGauge",
    rowsCount: 2,
    //...
});

{% endhighlight %}

![](Layout_images/row based.png) 

##Column-wise Layout

Gauges can be arranged in specified number of columns by using the [`columnsCount`](/js/api/ejolapgauge#members:columnscount) property.

{% highlight javascript %}

$("#OlapGauge1").ejOlapGauge({
    url: "../OlapGauge",
    columnsCount: 2,
    //...
});

{% endhighlight %}

![](Layout_images/column based.png) 

