---
layout: post
title: Responsive-Layout
description: responsive layout
platform: js
control: OLAP Chart
documentation: ug
---

#Responsive Layout

**Responsive layout** is aimed at crafting sites to provide an optimal viewing experience - easy reading. It also provides navigation with a minimum of resizing, panning, and scrolling across a wide range of devices from tablet to desktop. To get responsive layout for **OLAP Chart,** enable **IsResponsive** API to **true**. By using this feature, you can achieve an effective view of the **OLAP Chart** control in all devices including desktops, tablets, mobiles, etc. 

{% highlight js %}

$(function() {
            $("#OlapChart").ejOlapChart({
                url: "../wcf/OlapChartService.svc",
                animation: true,
                isResponsive: true,
                type: ej.olap.OlapChart.ChartTypes.Column,
                commonSeriesOptions: {
                    tooltip: {
                        visible: true
                    }
                },
                size: {
                    height: "460px",
                    width: "100%"
                },
                load: "loadTheme"
            });

{% endhighlight %}

{% include image.html url="/js/OlapChart/Responsive-Layout_images/Responsive-Layout_img1.png" Caption="Normal View"%}

<br/>

{% include image.html url="/js/OlapChart/Responsive-Layout_images/Responsive-Layout_img2.png" Caption="Responsive View"%}







