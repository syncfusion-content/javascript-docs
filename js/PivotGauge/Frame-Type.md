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

<<<<<<< HEAD
Full circle frame allows the pivot gauge to display in a circular shape. The frame type can be set by using the [`frameType`](/api/js/ejcirculargauge#members:frame) property. By default, the frame type is "fullCircle".
=======
Full circle frame allows the pivot gauge to display in a circular shape. The frame type can be set by using the [`frameType`](/api/js/ejcirculargauge#members:frame) property.  By default, the frame type is "fullCircle".
>>>>>>> hotfix/hotfix-v15.4.0.20

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({
        //....
        frame: { frameType: "fullCircle" }
    });

{% endhighlight %}

![](Frame-Type_images/FullCircle.png) 

## Half circle

<<<<<<< HEAD
Half circle frame allows the pivot gauge to display in a semi-circular shape. For this, the frame type should be set as "halfcircle" within the [`frameType`](/api/js/ejcirculargauge#members:frame) property and need to set `startAngle` and `sweepAngle` for the pivot gauge in the  [`scales`](/api/js/ejcirculargauge#members:scales) property.
=======
The half circle frame allows the pivot gauge to display in a semi-circular shape. For this, the frame type should be set as "halfCircle" within the [`frameType`](/api/js/ejcirculargauge#members:frame) property and should set the `startAngle` and `sweepAngle` for the pivot gauge in the  [`scales`](/api/js/ejcirculargauge#members:scales) property.
>>>>>>> hotfix/hotfix-v15.4.0.20

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

