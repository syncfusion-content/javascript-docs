---
layout: post
title: PivotGrid-Elements
description: pivotGrid elements
platform: js
control: PivotGrid
documentation: ug
api: /api/js/ejpivotgrid
---

# PivotGrid: Elements

## Hyperlink
The PivotGrid control supports the hyperlink option to link data for each individual cell. Hyperlink can be enabled separately for row header, column header, value, and summary cells. Following are the respective properties:

* [`enableColumnHeaderHyperlink`](/api/js/ejpivotgrid#members:hyperlinksettings-enablerowheaderhyperlink) - Enables hyperlink for column headers.
* [`enableRowHeaderHyperlink`](/api/js/ejpivotgrid#members:hyperlinksettings-enablerowheaderhyperlink) - Enables hyperlink for row headers.
* [`enableSummaryCellHyperlink`](/api/js/ejpivotgrid#members:hyperlinksettings-enablesummarycellhyperlink) - Enables hyperlink for the summary cell.
* [`enableValueCellHyperlink`](/api/js/ejpivotgrid#members:hyperlinksettings-enablevaluecellhyperlink) - Enables hyperlink for the value cell.

Also hyperlink option provides separate events for row header, column header, value, and summary cells as mentioned below:
 
* [`columnHeaderHyperlinkClick`](/api/js/ejpivotgrid#events:columnheaderhyperlinkclick) - Returns column header information through event when clicking the hyperlink.
* [`rowHeaderHyperlinkClick`](/api/js/ejpivotgrid#events:rowheaderhyperlinkclick) - Returns row header information through event when clicking the hyperlink.
* [`summaryCellHyperlinkClick`](/api/js/ejpivotgrid#events:summarycellhyperlinkclick) - Returns summary cell information through event when clicking the hyperlink.
* [`valueCellHyperlinkClick`](/api/js/ejpivotgrid#events:valuecellhyperlinkclick) - Returns value cell information through event when clicking the hyperlink.

{% highlight html %}

$(function() {

    $("#PivotGrid1").ejPivotGrid({
        //...
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
    });

    CellClickEvent = function(evt) {
        alert("Cell click event is fired.");
    }

});

{% endhighlight %}

![](PivotGrid-Elements_images/hyperlink.png)

## Selection
You can select a particular range of value cells from the PivotGrid and manipulate/display them. Cell selection is applicable only for value cells, and you can enable this functionality by setting the [`enableCellSelection`](/api/js/ejpivotgrid#members:enablecellselection) property to true.

The [`cellSelection`](/api/js/ejpivotgrid#events:cellselection) event will be triggered after the selection process, that is, when the mouse left click is released. The event argument contains a collection of JSON records and header values, which contains information about selected cells.

{% highlight html %}

$(function() {

    $("#PivotGrid1").ejPivotGrid({
        //...
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

## Cell context
Cell context allows you to perform any custom operation by right-clicking the cell. For example, you can create and display the context menu by right-clicking the cell.

Cell context is enabled by setting the [`enableCellContext`](/api/js/ejpivotgrid#members:enablecellcontext) property to true. The [`cellContext`](/api/js/ejpivotgrid#events:cellcontext) event will be enabled by right-clicking for provided cell information through the event argument.

{% highlight html %}

$(function() {

    $("#PivotGrid1").ejPivotGrid({
    	//...
        enableCellContext: true,
        cellContext: "cell_RightClick"
    });
});

cell_RightClick = function(evt) {
    //You can write your code here
}

{% endhighlight %}

## Conditional formatting
Conditional formatting in the PivotGrid allows you to highlight particular cells with certain color, font-style, font-family, etc., based on the applied condition.  Also the condition can be applied for certain measure alone.
  
Conditional formatting is enabled by setting the [`enableConditionalFormatting`](/api/js/ejpivotgrid#members:enableConditionalFormatting) property to true and the formatting dialog is launched when the **"createConditionalDialog"** method is invoked.

{% highlight html %}

<html>
//...

<body>
    <div id="PivotGrid1"> </div>
    <button id="Button1">Apply formatting</button>

    <script type="text/javascript">
        $(function() {
            $("#PivotGrid1").ejPivotGrid({
                //...
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

![](PivotGrid-Elements_images/FormatDialog.png)

![](PivotGrid-Elements_images/FormattedGrid.png)

### Export

You can export the PivotGrid with highlighted particular cells along with its formatting styles.

Limitations for Word:

The following border styles are not supported:

* Solid
* Groove
* Ridge

Limitations for PDF:

Border styles are not applicable.

Limitations for Excel:

The following border styles are alone supported:

* Dashed
* Dotted
* Double

Also border size is not supported.

![](PivotGrid-Elements_images/conditional_export.png)