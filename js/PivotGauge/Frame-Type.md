---
layout: post
title: Frame-Type
description: frame type 
platform: js
control: PivotGauge
documentation: ug
---

# Frame Type

## Full Circle

Full Circle frame lets the PivotGauge display in circular shape. Frame type can be set using the [`frameType`](/js/api/ejcirculargauge#members:frame) property.  By default, the frame type is "fullCircle".

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({
        //....
        frame: { frameType: "fullCircle" }
    });

{% endhighlight %}

![](Frame-Type_images/FullCircle.png) 

## Half Circle

Half Circle frame lets the PivotGauge display in semi-circular shape. For this, frame type needs to be set as "halfCircle" within the [`frameType`](/js/api/ejcirculargauge#members:frame) property.

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({
        //....
        frame: { frameType: "halfCircle" }
    });

{% endhighlight %}

![](Frame-Type_images/HalfCircle.png) 

