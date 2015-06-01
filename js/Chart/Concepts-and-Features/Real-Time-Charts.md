---
layout: post
title: Real-Time-Charts
description: real-time charts
platform: js
control: Chart
documentation: ug
---

# Real-Time Charts

**Essential Chart** allows you to create dynamic Charts that update at given interval. They are highly useful in network monitoring applications, stock/finance monitoring applications and manufacturing process indicators where the most up-to-date data are displayed. Dynamic updates are supported by all Chart types including line, area, column, spline, spline area, polar and radar series.

{% highlight js %}

**[JS]**

$("#chartcontainer").ejChart(
               {   
                   // ...             
         load: 'onchartload',
           });
        });

   function onchartload(sender) {
            for (var i = 0; i < 20; i = i + 0.1) {
                AddPoint(sender.model.series[0], 0);
            }
            chartobj = this;
            intervalId = window.setInterval(OnRefresh, 80);
        }



   function OnRefresh() {

            if (chartobj.model.series[0].points.length > 200) {
                chartobj.model.series[0].points.splice(0, 2);
                count += 2;
            }
            AddPoint(chartobj.model.series[0], count);
            $("#livechart").ejChart("redraw");
        }
  function AddPoint(series, count) {
            if (series.points == undefined)
                series.points = [];
            series.points[series.points.length] =
                         { x: series.points.length + count, y: getRandomNum(30, 40) };
        }

   function getRandomNum(lbound, ubound) {
            return (Math.floor(Math.random() * (ubound - lbound)) + lbound);
        }



{% endhighlight %}



{% include image.html url="/js/Chart/Concepts-and-Features/Real-Time-Charts_images/Real-Time-Charts_img1.png" Caption="Real-Time Chart"%}

