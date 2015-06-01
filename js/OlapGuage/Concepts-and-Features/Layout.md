---
layout: post
title: Layout
description: layout 
platform: js
control: OLAP Gauge
documentation: ug
---

# Layout 

The **OLAP Gauge** control provides support to display multiple gauges in a structured layout. You can customize the layout using the **ColumnsCount** and **RowsCount** properties. These properties are used to specify the number of columns and rows for displaying controls.

## Supported Layouts

* **Wrap Layout**: Based on the available space, gauges are aligned and displayed automatically.

* **Row count**: Specifies the number of gauge controls to be displayed row-wise.

* **Column count**: Specifies the number of gauge controls to be displayed column-wise.

## Layout Customization 

You can customize/limit the number of gauges to be displayed in the table with the help of the **rowsCount** and **columnsCount** properties.

## Row Count

You can set the number of gauges to be displayed in row using **rowsCount** property. By default the value is **0**.



{% highlight js %}

**[JS]**

$(function () {
     $("#OlapGauge1").ejOlapGauge({ url: "../wcf/OlapGaugeService.svc", enableTooltip: true,
         backgroundColor: "transparent",**rowsCount: 2,**
         scales: [{
             showRanges: true,
             radius: 150, showScaleBar: true, size: 1,
             border: {
                 width: 0.5
             },
             showIndicators: true, showLabels: true,
             pointers: [{
                 showBackNeedle: true,
                 backNeedleLength: 20,
                 length: 120,
                 width: 7
             },
     {
         type: "marker",
         markerType: "diamond",
         distanceFromScale: 5,
         placement: "center",
         backgroundColor: "#29A4D9",
         length: 25,
         width: 15
     }],
             ticks: [{
                 type: "major",
                 distanceFromScale: 2,
                 height: 16,
                 width: 1, color: "#8c8c8c"
             },
             {
                 type: "minor",
                 height: 6,
                 width: 1,
                 distanceFromScale: 2,
                 color: "#8c8c8c"
             }],
             labels: [{
                 color: "#8c8c8c"
             }],
             ranges: [{
                 distanceFromScale: -5,
                 backgroundColor: "#fc0606",
                 border: { color: "#fc0606" }
             }, {
                 distanceFromScale: -5
             }],
             customLabels: [{
                 position: { x: 180, y: 290 },
                 font: { size: "10px", fontFamily: "Segoe UI", fontStyle: "Normal" }, color: "#666666"
             }, {
                 position: { x: 180, y: 320 },
                 font: { size: "10px", fontFamily: "Segoe UI", fontStyle: "Normal" }, color: "#666666"
             }, {
                 position: { x: 180, y: 150 },
                 font: { size: "12px", fontFamily: "Segoe UI", fontStyle: "Normal" }, color: "#666666"
             }]
         }]
     });
 });


{% endhighlight %}







{% include image.html url="/js/OlapGuage/Concepts-and-Features/Layout_images/Layout_img1.png" Caption="Figure : Row Count"%}

## Column Count

You can set the number of gauges to be displayed in column using **columnsCount** property. By default the value is **0**.



{% highlight js %}

**[JS]**
$(function () {
     $("#OlapGauge1").ejOlapGauge({ url: "../wcf/OlapGaugeService.svc", enableTooltip: true,
         backgroundColor: "transparent", columnsCount: 2,
         scales: [{
             showRanges: true,
             radius: 150, showScaleBar: true, size: 1,
             border: {
                 width: 0.5
             },
             showIndicators: true, showLabels: true,
             pointers: [{
                 showBackNeedle: true,
                 backNeedleLength: 20,
                 length: 120,
                 width: 7
             },
     {
         type: "marker",
         markerType: "diamond",
         distanceFromScale: 5,
         placement: "center",
         backgroundColor: "#29A4D9",
         length: 25,
         width: 15
     }],
             ticks: [{
                 type: "major",
                 distanceFromScale: 2,
                 height: 16,
                 width: 1, color: "#8c8c8c"
             },
             {
                 type: "minor",
                 height: 6,
                 width: 1,
                 distanceFromScale: 2,
                 color: "#8c8c8c"
             }],
             labels: [{
                 color: "#8c8c8c"
             }],
             ranges: [{
                 distanceFromScale: -5,
                 backgroundColor: "#fc0606",
                 border: { color: "#fc0606" }
             }, {
                 distanceFromScale: -5
             }],
             customLabels: [{
                 position: { x: 180, y: 290 },
                 font: { size: "10px", fontFamily: "Segoe UI", fontStyle: "Normal" }, color: "#666666"
             }, {
                 position: { x: 180, y: 320 },
                 font: { size: "10px", fontFamily: "Segoe UI", fontStyle: "Normal" }, color: "#666666"
             }, {
                 position: { x: 180, y: 150 },
                 font: { size: "12px", fontFamily: "Segoe UI", fontStyle: "Normal" }, color: "#666666"
             }]
         }]
     });
 });


{% endhighlight %}



{% include image.html url="/js/OlapGuage/Concepts-and-Features/Layout_images/Layout_img2.png" Caption="Figure: Column Count"%}

