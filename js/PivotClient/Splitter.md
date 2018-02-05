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

I> This feature is not applicable for the OLAP data source bound from the server-side. 

You can resize the cube dimension browser and the axis element builder by setting the [`enableSplitter`](/api/js/ejpivotclient#members:enableSplitter) property to true. This property is disabled by default.

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
