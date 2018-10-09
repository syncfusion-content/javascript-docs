---
layout: post
title: Frame-Type
description: frame type
platform: js
control: PivotGauge
documentation: ug
api: /api/js/ejpivotgauge
---

# Frame type

## Full circle

Full circle frame allows the pivot gauge to display in a circular shape. The frame type can be set by using the [`frameType`](/api/js/ejcirculargauge#members:frame) property. By default, the frame type is "fullCircle".

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({
        //....
        frame: { frameType: "fullCircle" }
    });

{% endhighlight %}

![](Frame-Type_images/FullCircle.png)

## Half circle

The half circle frame allows the pivot gauge to display in a semi-circular shape. For this, the frame type should be set as "halfCircle" within the [`frameType`](/api/js/ejpivotgauge#members:frame-frametype) property and should set the [`startAngle`](/api/js/ejpivotgauge#members:frame) and [`sweepAngle`](/api/js/ejpivotgauge#members:frame) for the pivot gauge in the  [`scales`](/api/js/ejpivotgauge#members:scales) property.

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

