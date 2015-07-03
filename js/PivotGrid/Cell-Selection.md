---
layout: post
title: Cell-Selection
description: cell selection
platform: js
control: PivotGrid
documentation: ug
---

#Cell Selection

The PivotGrid control provides support to select specific range of value cells and display them in a format based on your requirements. Selection can be done through simple mouse down and drag operation. By default, this functionality is not available.To enable this functionality, set `enableCellSelection` property to "true".

The following code example explains on how to enable cell selection in the PivotGrid control.

{% highlight js %}

$(function() {
   $("#PivotGrid").ejPivotGrid({
      url: "../wcf/OLAPService.svc",
      enableCellSelection: true,
      cellSelection: "valueCellClick"
   });
   valueCellClick = function(evt) {
      // The event lets you to perform required operation with the selected set of cells. The details of the selected range can be obtained in the parameter of the event.
      cellvalue = evt.JSONRecords;
      rowheaders = evt.rowHeader;
      colheaders = evt.columnHeader;
   }
});

{% endhighlight %}

{% include image.html url="/js/PivotGrid/Cell-Selection_images/Cell-Selection_img1.png" Caption="Cell Selection in the PivotGrid Control" %}

{% include image.html url="/js/PivotGrid/Cell-Selection_images/Cell-Selection_img2.png" Caption="Chart Series Based on Selected Cells" %}


