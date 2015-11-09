---
layout: post
title: Hyperlink
description: hyperlink
platform: js
control: PivotGrid
documentation: ug
---

# Hyperlink

The PivotGrid control supports **Hyperlink** option to link data for any individual cell. [Hyperlinks](/js/api/ejPivotGrid#members:hyperlinksettings) are enabled individually for value, row, column, and summary cells. After enabling the property, the specified cells display Hyperlink on hovering.

The following code example demonstrates how to create a PivotGrid with hyperlink enabled cells.

{% highlight js %}
$(function() {
    $("#PivotGrid1").ejPivotGrid({
        hyperlinkSettings: {
            enableValueCellHyperlink: true,
            enableRowHeaderHyperlink: true,
            enableColumnHeaderHyperlink: true,
            enableSummaryCellHyperlink: true
        },
        valueCellHyperlinkClick: "CellClickEvent",
        rowHeaderHyperlinkClick: "CellClickEvent",
        columnHeaderHyperlinkClick: "CellClickEvent",
        summaryCellHyperlinkClick: "CellClickEvent",
        url: "../wcf/PivotGridService.svc",
        layout: ej.PivotGrid.Layout.Normal
    });
    CellClickEvent = function(evt) {
        alert("Cell Click event is fired");
    }
});
{% endhighlight %}

Output:

![](/js/PivotGrid/Hyperlink_images/Hyperlink_img1.png) 

