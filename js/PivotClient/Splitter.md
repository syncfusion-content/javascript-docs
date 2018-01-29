---
layout: post
title: Splitter
description: splitter
platform: js
control: PivotClient
documentation: ug
api: /api/js/ejpivotclient
---

# Splitter

I> This feature is not applicable for OLAP datasource bound from server-side. 

You can resize Cube Dimension Browser and Axis Element Builder by setting [`enableSplitter`](/api/js/ejpivotclient#members:enableSplitter) property to true.This property is disabled by default.

{% highlight javascript %}

            $("#PivotClient1").ejPivotClient({
                //...
                enableSplitter: true,
            });

{% endhighlight %}

![](Splitter_images/Splitter1.png)

![](Splitter_images/Splitter2.png)

![](Splitter_images/Splitter3.png)

![](Splitter_images/Splitter4.png)
