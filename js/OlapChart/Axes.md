---
layout: post
title: Axes
description: axes 
platform: js
control: OlapChart
documentation: ug
---

#Axes 

**OlapChart** typically have two axes that are used to measure and categorize data: a vertical Y-axis and a horizontal X-axis. By default vertical Y-axis and horizontal X-axis is added to the Chart with axis labels, gridlines, and tick lines. You can also customize this axis explicitly by adding axis title or removing gridlines, tick lines that are added to the axis by default.

{% highlight js %}
$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc",
    primaryXAxis: {
        majorTickLines: {
            visible: false
        }
    },
    primaryYAxis: {
        majorTickLines: {
            visible: false
        }
    },
    size: {
        height: "460px",
        width: "950px"
    }
});

{% endhighlight %}


##Axis Title Customization

Primary axis title [font](/js/api/ejChart#members:primaryxaxis-title-font) appearance is further customized with the help of the following code example.

{% highlight js %}

$(function() {
    $("#OlapChart1").ejOlapChart({
        url: "../wcf/OlapChartService.svc",
        legend: {
            visible: true,
            rowCount: 3
        },
        commonSeriesOptions: {
            type: ej.olap.OlapChart.ChartTypes.Column
        },
        primaryXAxis: {
            title: {
                text: "Primary X title customization",
                font: {
                    color: 'red',
                    fontFamily: 'Segoe UI',
                    fontStyle: 'Italic',
                    size: '18px',
                    opacity: 1,
                    fontWeight: 'lighter'
                }
            }
        },
        primaryYAxis: {
            title: {
                text: "Primary Y title customization",
                font: {
                    color: 'red',
                    fontFamily: 'Segoe UI',
                    fontStyle: 'Italic',
                    size: '18px',
                    opacity: 1,
                    fontWeight: 'lighter'
                }
            }
        },
        size: {
            height: "460px",
            width: "950px"
        }
    });
});


{% endhighlight %}

![]("/js/OlapChart/Chart-Axes_images/Chart-Axes_img1.png") 

##Axis Line

**Axis line** is drawn in Chart to represent the end of the axis in **ChartArea**. It can be customized as shown below.

{% highlight js %}

$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc",
    title: {
        text: "OLAP Chart in Essential Studio"
    },
    legend: {
        visible: true,
        rowCount: 3
    },
    primaryXAxis: {
        axisLine: {
            visible: true
        },
        axisLine: {
            offset: 1
        },
        axisLine: {
            width: 3.5
        },
    },
    primaryYAxis: {
        axisLine: {
            dashArray: "2,3"
        }
    },
    size: {
        height: "460px",
        width: "950px"
    }
});


{% endhighlight %}


![]("/js/OlapChart/Chart-Axes_images/Chart-Axes_img2.png") 

##Position Opposed

**Position** of the primary X and Y axis is set to the top with the help [opposedPosition](/js/api/ejChart#members:primaryxaxis-opposedposition) property.

{% highlight js %}

$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc",
    title: {
        text: "OLAP Chart in Essential Studio"
    },
    primaryXAxis: {
        opposedPosition: true
    },
    primaryYAxis: {
        opposedPosition: true
    },
    size: {
        height: "460px",
        width: "950px"
    }
});


{% endhighlight %}


![]("/js/OlapChart/Chart-Axes_images/Chart-Axes_img3.png") 

##Area Customization 

Background, border color and outer width of the Chart Area can be customized with the help of following properties.

* [Background](/js/api/ejChart#members:chartarea-background) – sets the background color for Chart Area.
* [Color](/js/api/ejChart#members:chartarea-border-color) – sets the color for the border.
* [Width](/js/api/ejChart#members:chartarea-border-width) – sets the width for the border.



{% highlight js %}

$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc",
    title: {
        text: "OLAP Chart in Essential Studio"
    },
    chartArea: {
        border: {
            color: "gray",
            width: 4
        },
        background: "aqua"
    },
    size: {
        height: "460px",
        width: "950px"
    }
});

{% endhighlight %}


![]("/js/OlapChart/Chart-Axes_images/Chart-Axes_img4.png") 

#Label

**Label** represents the text on the axis data points in the Chart. Each axis data point are represented by separate label text information in order to provide precise information about each points. **Label** text is displayed in a customizable format.

##Label font and color customization 

Font style and color of the label text is customized with the help of [font](/js/api/ejChart#members:primaryxaxis-font) and [color](/js/api/ejChart#members:primaryxaxis-font-fontstyle) properties within its respective axis.

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

![]("/js/OlapChart/Chart-Axes_images/Label_img1.png") 

##Rotating Axis Labels

You can rotate the labels to desired angle. The axis labels are rendered in the degree specified in the [labelRotation](/js/api/ejChart#members:primaryxaxis-labelrotation) property.

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


![]("/js/OlapChart/Chart-Axes_images/Label_img2.png") 

