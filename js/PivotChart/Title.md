---
layout: post
title: Title
description: title
platform: js
control: PivotChart
documentation: ug
api: /api/js/ejpivotchart
---

# Title

## Title Text
By using the [`title.text`](/api/js/ejchart#members:title-text) property, you can add the title text for PivotChart.
 

{% highlight javascript %}

$(function () {
    $("#PivotChart1").ejPivotChart(
       ....
       //Adding Chart title
       title: {
          text: "PivotChart"
       },
       //....
    });
});

{% endhighlight %}

![](Title_images/Title_img1.png) 

## Title Alignment

By using the [`title.textAlignment`](/api/js/ejchart#members:title-textalignment) property, you can align the PivotChart controls title text to center, far or near.

{% highlight javascript %}

$(function () {
    $("#PivotChart1").ejPivotChart(
       ....
       title: {
            text: "PivotChart", 
            //Change title text alignment
            textAlignment: "near"
       },
       //....
    });
});

{% endhighlight %}

![](Title_images/Title_img2.png) 

## Title Customization
By using the [`title`](/api/js/ejchart#members:title) property, you can add the title text for X-axis and Y-axis. Also title text can be customized by using the [`text`](/api/js/ejchart#members:title-text) and [`font`](/api/js/ejchart#members:title-font) properties. On setting [`enableTrim`](/api/js/ejchart#members:primaryyaxis-enabletrim) to true, title text could be trimmed based on its length.

{% highlight javascript %}

$(function () {
       $("#PivotChart1").ejPivotChart(
            //...
          primaryXAxis: {
              //Customizing X-axis title
              title: {
                 text: "Country",
                 font: {
                    fontFamily: 'Segoe UI',
                    size: '16px',
                    fontWeight: 'bold',
                    color: 'grey',
                 },
                 enableTrim: true
              }
          }
     });
 });

{% endhighlight %}

![](Title_images/Title_img3.png) 
