---
layout: post
title: Frame-Type
description: frame type 
platform: js
control: OlapGauge
documentation: ug
---

# Frame Type

## Full Circle

Full Circle frame lets the OlapGauge display in circular shape. Frame type can be set using the [`frameType`](/js/api/ejcirculargauge#members:frame) property.  By default, the frame type is "fullCircle".

{% highlight js %}

$("#OlapGauge1").ejOlapGauge({
    url: "../OlapGauge",
    frameType: "fullCircle",
    //...
});

{% endhighlight %}

![](Frame-Type_images/fullCircle.png) 

## Half Circle

Half Circle frame lets the OlapGauge display in semi-circular shape. For this, frame type needs to be set as "halfCircle" within the [`frameType`](/js/api/ejcirculargauge#members:frame) property.

{% highlight js %}

$("#OlapGauge1").ejOlapGauge({
    url: "../OlapGauge",
    frameType: "halfCircle",
    //...
});

{% endhighlight %}

![](Frame-Type_images/halfCircle.png) 

