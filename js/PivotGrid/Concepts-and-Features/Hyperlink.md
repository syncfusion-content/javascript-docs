---
layout: post
title: Hyperlink
description: hyperlink
platform: js
control: PivotGrid
documentation: ug
---

# Hyperlink

The **PivotGrid** control supports **Hyperlink** option to link data for any individual cell. **Hyperlinks** are enabled individually for value, row, column, and summary cells by setting the **corresponding** property to **‘True’.** After enabling the property, the specified cells display **Hyperlink** on hovering. The name of the event to be triggered is passed to the **corresponding****event** property. On clicking the cells, the passed event is triggered and the information of the cell is carried through a parameter.

The following code example demonstrates how to create the **PivotGrid** control using **Hyperlink** support.


{% highlight javascript %}

**[JS]**
<body>
<div id="PivotGrid1" style="height: 380px; width: 72%; display:block; float:left; overflow: auto" />
  <script type="text/javascript">
       $(function () {
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
                        CellClickEvent = function (evt) {
                            alert("Cell Click event is fired");
                        }
                   });
</script>
</body>


{% endhighlight %}



The output of the above code creates a **PivotGrid** with the **Hyperlink** option as shown in the following screenshot:



{% include image.html url="/js/PivotGrid/Concepts-and-Features/Hyperlink_images/Hyperlink_img1.png" Caption="Hyperlink Cell"%}

