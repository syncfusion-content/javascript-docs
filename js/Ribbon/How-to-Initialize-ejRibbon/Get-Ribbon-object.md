---
layout: post
title: Get-Ribbon-object
description: get ribbon object
platform: js
control: Ribbon
documentation: ug
---

### Get Ribbon object

After **Ribbon** initialization, **Ribbon** object is stored in a container element of Ribbon. To access Ribbon object, you can use the following code example.

{% highlight js %}

var ribbonObject = $("#Ribbon").ejRibbon("instance");

[or]

var ribbonObject = $("#Ribbon").data("ejRibbon");


{% endhighlight %}



