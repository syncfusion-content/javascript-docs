---
layout: post
title: Frame-Type
description: frame type 
platform: js
control: PivotGauge
documentation: ug
api: /api/js/ejpivotgauge
---

# Frame Type

## Full Circle

Full Circle frame lets the PivotGauge display in circular shape. Frame type can be set using the [`frameType`](/api/js/ejcirculargauge#members:frame) property.  By default, the frame type is "fullCircle".

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({
        //....
        frame: { frameType: "fullCircle" }
    });

{% endhighlight %}

![](Frame-Type_images/FullCircle.png) 

## Half Circle

Half Circle frame lets the PivotGauge to display in semi-circular shape. For this, frame type needs to be set as "halfCircle" within the [`frameType`](/api/js/ejcirculargauge#members:frame) property and need to set `startAngle` and `sweepAngle` for the PivotGauge in the  [`scales`](/api/js/ejcirculargauge#members:scales) property.

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({
        //....
        frame: {
               frameType: 'halfcircle',
               halfCircleFrameStartAngle: 180, halfCircleFrameEndAngle: 360
        },
        scales: [{
                    //..
                    startAngle: 180, sweepAngle: 180
                    //..
                }]
    });

{% endhighlight %}

![](Frame-Type_images/HalfCircle.png) 

