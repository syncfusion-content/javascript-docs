---
layout: post
title: Legend
description: legend
platform: js
control: OLAP Chart
documentation: ug
---

#Legend

**Legend** is a color code that helps to differentiate between chart items. Legend also has labels beside each color to indicate that it applies to information from Series 1, Series 2, and so on.

##Legend Symbol

In **OlapChart**, you can customize the legend symbol with different shapes like rectangle, circle, cross, diamond, pentagon, hexagon, star, ellipse, triangle etc. Default value of legend **shape** is “Rectangle”.

{% highlight js %}

$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc",
    title: {
        text: "OLAP Chart in Essential Studio"
    },
    legend: {
        visible: true,
        rowCount: 3,
        shape: "Star"
    },
});


{% endhighlight %}

{% include image.html url="/js/OlapChart/Legend_images/Legend_img1.png" Caption="Legend Symbol"%}

##Legend Position

You can customize the legend position in top, bottom, left and right position of the Chart. Default value of legend **position** is “bottom”. 

{% highlight js %}

$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc",
    title: {
        text: "OLAP Chart in Essential Studio"
    },
    legend: {
        visible: true,
        rowCount: 3,
        shape: "Star",
        position: "top"
    },
});

{% endhighlight %}

{% include image.html url="/js/OlapChart/Legend_images/Legend_img2.png" Caption="Legend Position"%}

##Legend Arrangement

You can align the legend using **alignment** property of legend. This allows you to align the legend in center, far and near position of Chart Area. The Default value of legend **alignment** is “Center”.

{% highlight js %}

$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc",
    title: {
        text: "OLAP Chart in Essential Studio"
    },
    legend: {
        visible: true,
        rowCount: 3,
        alignment: "Near"
    }
});


{% endhighlight %}

{% include image.html url="/js/OlapChart/Legend_images/Legend_img3.png" Caption="Legend Arrangement"%}

##Legend Style

You can draw and customize the outline of Chart legend using **border** property of legend. Default value of legend border color is “**Transparent**”.

{% highlight js %}

$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc",
    title: {
        text: "OLAP Chart in Essential Studio"
    },
    legend: {
        visible: true,
        rowCount: 3,
        border: {
            color: 'red',
            width: 2
        }
    }
});

{% endhighlight %}


{% include image.html url="/js/OlapChart/Legend_images/Legend_img4.png" Caption="Legend Style Customization"%}

##Legend Item

**Legend item** is represented by an icon or image and a text. This gets rendered automatically corresponding to each Series in the **OlapChart**. You can customize the **Legend item**.

{% highlight js %}

$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc",
    title: {
        text: "OLAP Chart in Essential Studio"
    },
    legend: {
        visible: true,
        rowCount: 3,
        itemSize: {
            border: {
                color: "green",
                width: 0.5
            }
        }
    }
});

{% endhighlight %}

{% include image.html url="/js/OlapChart/Legend_images/Legend_img5.png" Caption="Legend Item Customization"%}

##Legend Text

You can customize the **legend text** - font family, font style, font weight and size using **font** property of **legend**. The following code illustrates this.

{% highlight js %}

$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc",
    title: {
        text: "OLAP Chart in Essential Studio"
    },
    legend: {
        visible: true,
        rowCount: 3,
        font: {
            fontFamily: 'Segoe UI',
            fontStyle: 'italic',
            fontWeight: 'bold',
            size: '13px'
        }
    },
});


{% endhighlight %}


{% include image.html url="/js/OlapChart/Legend_images/Legend_img6.png" Caption="Legend Text Customization "%}

