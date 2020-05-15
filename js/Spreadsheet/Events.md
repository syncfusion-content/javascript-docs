---
layout: post
title: Events with Spreadsheet widget for Syncfusion Essential JS.
description: How to customize the action events available in the Syncfusion Essential Javascript Spreadsheet widget.
platform: js
control: Spreadsheet
documentation: ug
api: /api/js/ejspreadsheet
---

# Javascript Spreadsheet Events

### Action Begin

The [`actionBegin`](../api/ejspreadsheet#events:actionbegin) event is triggered before every action starts.

List of actions that triggered for actionBegin event.

<table>
    <colgroup><col width="30px" /><col width="250px" /></colgroup>
    <tr><th>S.NO</th><th>Actions</th></tr>
    <tr><td>1</td><td>Cell Formatting.</td></tr>
     <tr><td>2</td><td>Clipboard Actions.</td></tr>
    <tr><td>3</td><td>Merge Cells</td></tr>
    <tr><td>4</td><td>Wrap text.</td></tr>
    <tr><td>5</td><td>Number formatting.</td></tr>
    <tr><td>6</td><td>Conditional Formatting.</td></tr>
    <tr><td>7</td><td>Cell Styles.</td></tr>
    <tr><td>8</td><td>Clear Functionalities</td></tr>
    <tr><td>9</td><td>Chart</td></tr>
     <tr><td>10</td><td>Picture.</td></tr>
    <tr><td>11</td><td>Sorting.</td></tr>
    <tr><td>12</td><td>Comments.</td></tr>
    <tr><td>13</td><td>Goto Actions.</td></tr>
    <tr><td>14</td><td>Sheet Updation.</td></tr>
    <tr><td>15</td><td>Hyperlinks.</td></tr>
    <tr><td>16</td><td>Lock cells and Protect sheet.</td></tr>
    <tr><td>17</td><td>Filtering.</td></tr>
    <tr><td>18</td><td>Format as Table.</td></tr>
    <tr><td>19</td><td>Find and Replace Actions.</td></tr>
    <tr><td>20</td><td>Named Range Actions.</td></tr>
    <tr><td>21</td><td>Data validation.</td></tr> 
</table>

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$("#Spreadsheet").ejSpreadsheet({
            // action begin event triggers before paste action
            actionBegin: function(args){
              if (args.reqType === "paste") {
                 args.cancel = true;  // if we set args.cancel value as true, paste action is prevented
             }
          },
        });
</script>

{% endhighlight %}

### Action Complete

The [`actionComplete`](../api/ejspreadsheet#events:actioncomplete) event is triggered after every action completes. 

List of actions that triggered for actionComplete event.

<table>
    <colgroup><col width="30px" /><col width="250px" /></colgroup>
    <tr><th>S.NO</th><th>Actions</th></tr>
    <tr><td>1</td><td>Cell Formatting.</td></tr>
     <tr><td>2</td><td>Clipboard Actions.</td></tr>
    <tr><td>3</td><td>Merge Cells</td></tr>
    <tr><td>4</td><td>Wrap text.</td></tr>
    <tr><td>5</td><td>Number formatting.</td></tr>
    <tr><td>6</td><td>Conditional Formatting.</td></tr>
    <tr><td>7</td><td>Cell Styles.</td></tr>
    <tr><td>8</td><td>Clear Functionalities</td></tr>
    <tr><td>9</td><td>Chart</td></tr>
     <tr><td>10</td><td>Picture.</td></tr>
    <tr><td>11</td><td>Sorting.</td></tr>
    <tr><td>12</td><td>Comments.</td></tr>
    <tr><td>13</td><td>Goto Actions.</td></tr>
    <tr><td>14</td><td>Sheet Updation.</td></tr>
    <tr><td>15</td><td>Hyperlinks.</td></tr>
    <tr><td>16</td><td>Lock cells and Protect sheet.</td></tr>
    <tr><td>17</td><td>Filtering.</td></tr>
    <tr><td>18</td><td>Format as Table.</td></tr>
    <tr><td>19</td><td>Find and Replace Actions.</td></tr>
    <tr><td>20</td><td>Named Range Actions.</td></tr>
    <tr><td>21</td><td>Data validation.</td></tr> 
</table>

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$("#Spreadsheet").ejSpreadsheet({
            // action complete event triggers after copy paste action
            actionComplete: function(args){
              if (args.reqType === "copy-paste") {
                 var sheetIndex = args.pasteSheetIndex  // if we want to know the pasted sheet index.
             }
          },
        });
</script>

{% endhighlight %}

### Before Batch Save

The [`beforeBatchSave`](../api/ejspreadsheet#events:beforebatchsave) event is triggered  before the batch save.

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$("#Spreadsheet").ejSpreadsheet({
            // beforeBatchSave event triggered  before the batch save.
            beforeBatchSave: function(args){
             var dataSettings = args.dataSettings // if we want to know the dataSettings of batch save event.
          },
        });
</script>

{% endhighlight %}

### Before Cell Format

The [`beforeCellFormat`](../api/ejspreadsheet#events:beforecellformat) event is triggered before the cells to be formatted.

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$("#Spreadsheet").ejSpreadsheet({
            // before cell format event triggers before apply background color to cell.
            beforeCellFormat: function(args){
                 args.format.style["background-color"] = "#000000"  // if we want to change the color before applied to the cell.
          },
        });
</script>

{% endhighlight %}

### Before Open

The [`beforeOpen`](../api/ejspreadsheet#events:beforeopen) event is triggered before the contextmenu is open.

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$("#Spreadsheet").ejSpreadsheet({
            // before open event triggers before opening the spreadsheet context menu.
            beforeOpen: function(args){
                 args.cancel = true;  // if we want to close the menu before open
            },
        });
</script>

{% endhighlight %}

### Cell Click

The [`cellClick`](../api/ejspreadsheet#events:cellclick) event is triggered when click on sheet cell.

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$("#Spreadsheet").ejSpreadsheet({
            // while clicking the spreadsheet cell.
            cellClick: function(args){
                 var rowIndex = args.rowIndex;
                 var colIndex = args.columnIndex;
                 var value = args.value; // if we want to know the clicked cell rowIndex and columnIndex and value
            },
        });
</script>

{% endhighlight %}

### Cell Formatting

The [`cellFormatting`](../api/ejspreadsheet#events:cellformatting) event is triggered while formatting the cell.

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$("#Spreadsheet").ejSpreadsheet({
            // while formatting the spreadsheet cell.
            cellFormatting: function(args){
                 var format = args.format.style; //to know the styles applied while cell formatting.
            },
        });
</script>

{% endhighlight %}

### Cell Selected

The [`cellSelected`](../api/ejspreadsheet#events:cellselected) event is triggered when the cell is selected.

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$("#Spreadsheet").ejSpreadsheet({
            // when the cell is selected.
            cellSelected: function(args){
                 var range = args.selectedRange; //to know the range of the cells to be selected.
            },
        });
</script>

{% endhighlight %}

### Context Menu Click

The [`contextMenuClick`](../api/ejspreadsheet#events:contextmenuclick) event is triggered when click the contextmenu items.

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$("#Spreadsheet").ejSpreadsheet({
            // when  click the contextmenu items.
            contextMenuClick: function(args){
                 args.cancel = true; //to prevent the clicked item's action in spreadsheet context menu.
            },
        });
</script>

{% endhighlight %}

### Drag

The [`drag`](../api/ejspreadsheet#events:drag) event is triggered when the selected cells are being dragged.

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$("#Spreadsheet").ejSpreadsheet({
            // when the selected cells are being dragged.
            drag: function(args){
                 range = args.dragAndDropRange; //to know the range.
            },
        });
</script>

{% endhighlight %}

### Drag Start

The [`dragStart`](../api/ejspreadsheet#events:dragstart) event is triggered when the selected cells are initiated to drag.

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$("#Spreadsheet").ejSpreadsheet({
            // when the selected cells are initiated to drag.
            dragStart: function(args){
                 range = args.dragAndDropRange; //to know the range.
            },
        });
</script>

{% endhighlight %}

### Drop

The [`drop`](../api/ejspreadsheet#events:drop) event is triggered when the selected cells are dropped.

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$("#Spreadsheet").ejSpreadsheet({
            // when the selected cells are dropped
            drop: function(args){
                 range = args.dragAndDropRange; //to know the range.
            },
        });
</script>

{% endhighlight %}

### editRangeBegin

The [`editRangeBegin`](../api/ejspreadsheet#events:editrangebegin) event is triggered when the range editing starts.

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$("#Spreadsheet").ejSpreadsheet({
            // when the range editing starts.
            editRangeBegin: function(args){
                var range = args.range;
                var sheetIndex = args.sheetIndex//to know the range and sheet index to be edited.
            },
        });
</script>

{% endhighlight %}

### Edit Range Complete

The [`editRangeComplete`](../api/ejspreadsheet#events:editrangecomplete) event is triggered when the range editing completes.

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$("#Spreadsheet").ejSpreadsheet({
            // when the range editing completes.
            editRangeComplete: function(args){
                var range = args.range;
                var sheetIndex = args.sheetIndex//to know the range and sheet index to be edited.
            },
        });
</script>

{% endhighlight %}

### Key Down

The [`keyDown`](../api/ejspreadsheet#events:keydown) event is triggered when the  key is pressed down.

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$("#Spreadsheet").ejSpreadsheet({
            // when the  key is pressed down.
            keyDown: function(args){
                args.cancel = true; //to prevent the spreadsheet in edit mode.
            },
        });
</script>

{% endhighlight %}

### Key Up

The [`keyUp`](../api/ejspreadsheet#events:keyup) event is triggered when the key is released.

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$("#Spreadsheet").ejSpreadsheet({
            // when the key is released.
            keyUp: function(args){
                var commentEdit = args.isCommentEdit //to know whether we edited the comment cell.
            },
        });
</script>

{% endhighlight %}

### load

The [`load`](../api/ejspreadsheet#events:load) event is triggered before the sheet is loaded.

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$("#Spreadsheet").ejSpreadsheet({
            // before the sheet is loaded.
            load: function(args){
               this.sheetRename("Sep-Billing");//to rename the sheet before it is loaded.
            },
        });
</script>

{% endhighlight %}

### Load Complete

The [`loadComplete`](../api/ejspreadsheet#events:loadcomplete) event is triggered after the sheet is loaded.

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$("#Spreadsheet").ejSpreadsheet({
            // after the sheet is loaded
            loadComplete: function(args){
               this.setBorder({ "type": "left", "color": "#FF5668", "style": "solid" }, "A1"); //it sets the border to cell A1 after the sheet is loaded
            },
        });
</script>

{% endhighlight %}

### Menu Click

The [`menuClick`](../api/ejspreadsheet#events:menuclick) event is triggered when click the menu item.

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$("#Spreadsheet").ejSpreadsheet({
            // when click the menu item.
            menuClick: function(args){
               args.cancel = true; //to prevent the clicked item's action in the menu.
            },
        });
</script>

{% endhighlight %}

### Menu Click

The [`menuClick`](../api/ejspreadsheet#events:menuclick) event is triggered when click the menu item.

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$("#Spreadsheet").ejSpreadsheet({
            // when click the menu item.
            menuClick: function(args){
               args.cancel = true; //to prevent the clicked item's action in the menu.
            },
        });
</script>

{% endhighlight %}

### On Import

The [`onImport`](../api/ejspreadsheet#events:onimport) event is triggered when a file is imported.

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$("#Spreadsheet").ejSpreadsheet({
            // when a file is imported.
            onImport: function(args){
              var importedData = args.importData //to get the data to be imported
            },
        });
</script>

{% endhighlight %}

### Open Failure

The [`openFailure`](../api/ejspreadsheet#events:openfailure) event is triggered when import sheet is failed to open.

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$("#Spreadsheet").ejSpreadsheet({
            // when import sheet is failed to open.
            openFailure: function(args){
              var status = args.statusText //to get the status
            },
        });
</script>

{% endhighlight %}

### Resize Start

The [`resizeStart`](../api/ejspreadsheet#events:resizestart) event is triggered when start resizing the chart, picture, row and column.

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$("#Spreadsheet").ejSpreadsheet({
            // when start resizing column.
            resizeStart: function(args){
              var oldWidth = args.oldWidth;
              var colIndex = args.colIndex; //to get the resized column index and old width
            },
        });
</script>

{% endhighlight %}

### Resize End

The [`resizeEnd`](../api/ejspreadsheet#events:resizeend) event is triggered after end of resizing the chart, picture, row and column.

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$("#Spreadsheet").ejSpreadsheet({
            // when completes the column resizing
            resizeEnd: function(args){
              var newWidth = args.newWidth;
              var oldWidth = args.oldWidth;
              var colIndex = args.colIndex; //to get the resized column index and old width and new width.
            },
        });
</script>

{% endhighlight %}

### Ribbon Click

The [`ribbonClick`](../api/ejspreadsheet#events:ribbonclick) event is triggered when click on the ribbon.

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$("#Spreadsheet").ejSpreadsheet({
            // when completes the column resizing
            ribbonClick: function(args){
              var id = args.Id; // to get the Id of the clicked ribbon item.
            },
        });
</script>

{% endhighlight %}

### Tab Click

The [`tabClick`](../api/ejspreadsheet#events:tabclick) event is triggered when click the ribbon tab.

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$("#Spreadsheet").ejSpreadsheet({
            // when click the ribbon tab.
            tabClick: function(args){
              var activeIndex = args.activeIndex;
              var prevActiveIndex = args.prevActiveIndex; // to get the current and previous active index.
            },
        });
</script>

{% endhighlight %}

### tabSelect

The [`tabSelect`](../api/ejspreadsheet#events:tabselect) event is triggered when select the ribbon tab.

{% highlight html %}

<div id="Spreadsheet"></div>

<script>
$("#Spreadsheet").ejSpreadsheet({
            // when select the ribbon tab.
            tabClick: function(args){
              var activeIndex = args.activeIndex;
              var prevActiveIndex = args.prevActiveIndex; // to get the current and previous active index.
            },
        });
</script>

{% endhighlight %}