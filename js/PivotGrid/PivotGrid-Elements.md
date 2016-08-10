---
layout: post
title: PivotGrid-Elements
description: pivotGrid elements
platform: js
control: PivotGrid
documentation: ug
---

# PivotGrid: Elements

## Hyperlink
The PivotGrid control supports hyperlink option to link data for each individual cells. Hyperlink can be enabled separately for row, column, value and summary cells. Following are the respective properties:

* [`enableColumnHeaderHyperlink`](/js/api/ejpivotgrid#members:hyperlinksettings-enablerowheaderhyperlink) - Enables hyperlink for column header.
* [`enableRowHeaderHyperlink`](/js/api/ejpivotgrid#members:hyperlinksettings-enablerowheaderhyperlink) - Enables hyperlink for row header.
* [`enableSummaryCellHyperlink`](/js/api/ejpivotgrid#members:hyperlinksettings-enablesummarycellhyperlink) - Enables hyperlink for summary cell.
* [`enableValueCellHyperlink`](/js/api/ejpivotgrid#members:hyperlinksettings-enablevaluecellhyperlink) - Enables hyperlink for value cell.

Also hyperlink option provides separate event for row, column, value and summary cells as mentioned below.
 
* [`columnHeaderHyperlinkClick`](/js/api/ejpivotgrid#events:columnheaderhyperlinkclick) - Returns column header information through event on hyperlink click.
* [`rowHeaderHyperlinkClick`](/js/api/ejpivotgrid#events:rowheaderhyperlinkclick) - Returns row header information through event on hyperlink click.
* [`summaryCellHyperlinkClick`](/js/api/ejpivotgrid#events:summarycellhyperlinkclick) - Returns column header information through event on hyperlink click.
* [`valueCellHyperlinkClick`](/js/api/ejpivotgrid#events:valuecellhyperlinkclick) - Returns value cell information through event on hyperlink click.

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
       url: "/OLAPService",
        layout: ej.PivotGrid.Layout.Normal
    });

    CellClickEvent = function(evt) {
        alert("Cell click event is fired.");
    }
});

{% endhighlight %}

![](PivotGrid-Elements_images/hyperlink.png)

## Selection
You can select a particular range of value cells from PivotGrid and manipulate/display them. Cell selection is applicable only for values cells and you can enable this functionality by setting `enableCellSelection` property to true.

The **"cellSelection"** event would be triggered as soon as the selection process is over, that is, when the mouse left click is released. The event argument contains a collection of JSON records and header values, which contains information about the selected cells.

{% highlight js %}

$(function() {
    $("#PivotGrid1").ejPivotGrid({
        url: "/OLAPService",
        enableCellSelection: true,
        cellSelection: "valueCellClick"
    });

    valueCellClick = function(evt) {
        //This event lets you to perform required operation with the selected range of cells.
        cellvalue = evt.JSONRecords;
        rowheaders = evt.rowHeader;
        colheaders = evt.columnHeader;
    }
});

{% endhighlight %}

![](PivotGrid-Elements_images/cellselection.png)

## Cell Context
Cell context allows user to perform any custom operation on cell right-click. For example, you can create and display content menu on cell right-click.

Cell context is enabled by setting the [`enableCellContext`](/js/api/ejpivotgrid#members:enablecellcontext) property to true. The **"cellContext"** event would be raised as soon as right-click is done providing cell information through event argument.

{% highlight js %}

$(function() {
    $("#PivotGrid1").ejPivotGrid({
       url: "/OLAPService",
        enableCellContext: true,
        cellContext: "cell_RightClick"
    });
});

cell_RightClick = function(evt) {
    //You can write your code here
}

{% endhighlight %}

## Conditional Formatting
Conditional formatting in PivotGrid allows user to highlight particular cells with certain color, font-style, font-family etc. Based on the condition it has met.
  
Conditional formatting is enabled by setting `enableConditionalFormatting` property to true and the formatting dialog is launched when **"createConditionalDialog"** method is invoked.

{% highlight html %}

<html>
//...

<body>
    <div id="PivotGrid1" style="height: 350px; width: 100%; overflow: auto"> </div>
    <button id="Button1">Apply formatting</button>

    <script type="text/javascript">
        $(function() {
            $("#PivotGrid1").ejPivotGrid({
                url: "/OLAPService",
                enableConditionalFormatting: true
            });
            $("#Button1").ejButton({
                size: "normal",
                roundedCorner: true,
                click: "btnClick"
            });
        });

        function btnClick(e) {
            var pivotGridObj = $('#PivotGrid1').data("ejPivotGrid");
            if (pivotGridObj.model.enableConditionalFormatting) {
                pivotGridObj.createConditionalDialog();
            }
        }
    </script>
</body>

</html>

{% endhighlight %}

![](PivotGrid-Elements_images/conditional.png)


