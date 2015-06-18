---
layout: post
title: Get-Grid-object
description: get grid object
platform: js
control: Grid
documentation: ug
---

### Get Grid object

After **Grid** initialization, **Grid** object is stored in a container element of **Grid**. To access **Grid** object, you can use the following code example.

{% highlight js %}

var gridObject = $("#Grid").ejGrid("instance");

                [or]

var gridObject = $("#Grid").data("ejGrid");


{% endhighlight %}



