---
layout: post
title: Title with PivotChart widget for Syncfusion Essential JS
description: This document illustrates that how to enable title and its customization in JavaScript PivotChart control
platform: js
control: PivotChart
documentation: ug
api: /api/js/ejpivotchart
---

# Title

## Title text
By using the [`title.text`](/api/js/ejpivotchart#members:title-text) property, you can add the title text for the pivot chart.


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

![Title text in JavaScript pivot chart control](Title_images/Title_img1.png)

## Title alignment

By using the [`title.textAlignment`](/api/js/ejchart#members:title-textalignment) property, you can align the title text of the pivot chart control to center, far, or near.

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

![Title alignment in JavaScript pivot chart control](Title_images/Title_img2.png)

## Title customization
By using the [`title`](/api/js/ejpivotchart#members:title) property, you can add the title text for X-axis and Y-axis. The title text can be customized by using the [`text`](/api/js/ejchart#members:title-text) and [`font`](/api/js/ejchart#members:title-font) properties. By setting the [`enableTrim`](/api/js/ejchart#members:primaryyaxis-enabletrim) to true, the title text can be trimmed based on its length.

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

![Title customization in JavaScript pivot chart control](Title_images/Title_img3.png)
