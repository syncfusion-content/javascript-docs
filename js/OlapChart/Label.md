---
layout: post
title: Label
description: label
platform: js
control: OlapChart
documentation: ug
---

#Label

**Label** represents the text on the axis data points in the Chart. Each axis data point are represented by separate label text information in order to provide precise information about each points. **Label** text is displayed in a customizable format.

##Label font and color customization 

Font style and color of the label text is customized with the help of **font** and **color** properties within its respective axis.

{% highlight js %}

$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc",
    primaryXAxis: {
        font: {
            fontFamily: "Algerian",
            fontWeight: "lighter",
            fontStyle: "Italic",
            size: "14px",
            color: "red"
        }
    },
    primaryYAxis: {
        font: {
            fontFamily: "Algerian",
            fontWeight: "lighter",
            fontStyle: "Italic",
            size: "14px",
            color: "red"
        },
    },
    size: {
        height: "460px",
        width: "950px"
    }
});


{% endhighlight %}

{% include image.html url="/js/OlapChart/Label_images/Label_img1.png" %}

##Rotating Axis Labels

You can rotate the labels to desired angle. The axis labels are rendered in the degree specified in the **labelRotation** property.

{% highlight js %}

$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc",
    primaryXAxis: {
        labelRotation: 45
    },
    size: {
        height: "460px",
        width: "950px"
    }
});


{% endhighlight %}


{% include image.html url="/js/OlapChart/Label_images/Label_img2.png" %}

