---
layout: post
title: Getting started | Spreadsheet | JavaScript | Syncfusion
description: getting started
platform: JS
control: Spreadsheet
documentation: ug
---
# Getting started

## Preparing HTML document

The Spreadsheet have the following list of external dependencies. 

* [jQuery](http://jquery.com/) 1.7.1 and later versions.
* [jsRender](https://github.com/borismoore/jsrender) - to render the templates.
* [jQuery.easing](http://gsgd.co.uk/sandbox/jquery/easing/) - to support the animation effects in the components.
* [jQuery.validate](https://github.com/jzaefferer/jquery-validation) - to support validation in editing and dialog inputs.

And the internal dependencies are tabulated below. 

<table>
<tr>
<th>
File                              </th><th>
Description/Usage</th></tr>
<tr>
<td>
ej.core.min.js</td><td>
Must be referred always before using all the JS controls.  </td></tr>
<tr>
<td>
ej.data.min.js</td><td>
Used to handle data operation and should be used while binding data to JS controls.  </td></tr>
<tr>
<td>
ej.scroller.min.js</td><td>
Used to handle scrolling operation in all JS controls.  </td></tr>
<tr>
<td>
ej.spreadsheet.common.min.js</td><td>
Spreadsheet's main file.  </td></tr>
<tr>
<td>
ej.spreadsheet.selection.min.js</td><td>
Should be referred when using selection in Spreadsheet.  </td></tr>
<tr>
<td>
ej.spreadsheet.filter.min.js</td><td>
Should be referred when using filtering in Spreadsheet.  </td></tr>
<tr>
<td>
ej.spreadsheet.ribbon.min.js</td><td>
Should be referred when ribbon is enabled in Spreadsheet.  </td></tr>
<tr>
<td>
ej.spreadsheet.freezepane.min.js</td><td>
Should be referred when using freeze pane options in Spreadsheet.  </td></tr>
<tr>
<td>
ej.spreadsheet.math.min.js</td><td>
Must be referred and used for Spreadsheet common calculation.  </td></tr>
<tr>
<td>
ej.spreadsheet.resizing.min.js</td><td>
Should be referred when using resizing in Spreadsheet.  </td></tr>
<tr>
<td>
ej.spreadsheet.editing.min.js</td><td>
Should be referred when using editing in Spreadsheet.  </td></tr>
<tr>
<td>
ej.spreadsheet.validation.min.js</td><td>
Should be referred when using data validation in Spreadsheet.  </td></tr>
<tr>
<td>
ej.spreadsheet.comments.min.js</td><td>
Should be referred when using comments in Spreadsheet.  </td></tr>
<tr>
<td>
ej.spreadsheet.dragFill.min.js</td><td>
Should be referred when using auto fill in Spreadsheet.  </td></tr>
<tr>
<td>
ej.spreadsheet.cellNavigation.min.js</td><td>
Should be referred when using keyboard navigation in Spreadsheet.  </td></tr>
<tr>
<td>
ej.spreadsheet.cellFormatting.min.js</td><td>
Should be referred when using cell formatting in Spreadsheet.  </td></tr>
<tr>
<td>
ej.spreadsheet.cFormat.min.js</td><td>
Should be referred when using conditional formatting in Spreadsheet.  </td></tr>
<tr>
<td>
ej.spreadsheet.clipboard.min.js</td><td>
Should be referred when using clipboard options in Spreadsheet.  </td></tr>
<tr>
<td>
ej.spreadsheet.contextmenu.min.js</td><td>
Should be referred when using context menu in Spreadsheet.  </td></tr>
<tr>
<td>
ej.spreadsheet.sorting.min.js</td><td>
Should be referred when using sorting in Spreadsheet.  </td></tr>
<tr>
<td>
ej.spreadsheet.dragAndDrop.min.js</td><td>
Should be referred when using drag and drop in Spreadsheet.  </td></tr>
<tr>
<td>
ej.spreadsheet.findnreplace.min.js</td><td>
Should be referred when using find and replace option in Spreadsheet.  </td></tr>
<tr>
<td>
ej.spreadsheet.exporting.min.js</td><td>
Should be referred when using exporting in Spreadsheet.  </td></tr>
<tr>
<td>
ej.spreadsheet.shape.min.js</td><td>
Should be referred when using picture and chart in Spreadsheet.  </td></tr>
<tr>
<td>
ej.spreadsheet.chart.min.js</td><td>
Should be referred when using chart in Spreadsheet.  </td></tr>
<tr>
<td>
ej.spreadsheet.print.min.js</td><td>
Should be referred when using print option in Spreadsheet.  </td></tr>
<tr>
<td>
ej.spreadsheet.scroller.min.js</td><td>
Should be referred when using scrolling in Spreadsheet.  </td></tr>
<tr>
<td>
ej.grid.min.js</td><td>
Used this control for Name Manager option in Spreadsheet.  </td></tr>
<tr>
<td>
ej.pager.min.js</td><td>
Must be referred and used for paging option in Spreadsheet.  </td></tr>
<tr>
<td>
ej.waitingpopup.min.js</td><td>
Should be referred while importing files in Spreadsheet.  </td></tr>
<tr>
<td>
ej.autocomplete.min.js</td><td>
Should be referred when editing is enabled in Spreadsheet.  </td></tr>
<tr>
<td>
ej.chart.min.js</td><td>
Used this control for chart option is enabled in Spreadsheet.  </td></tr>
<tr>
<td>
ej.ribbon.min.js</td><td>
These files are used when ribbon option is enabled in Spreadsheet.  </td></tr>
<tr>
<td>
ej.button.min.js</td><td rowspan = "16">
These files are used while enable the cellFormatting , import and drag and drop feature in the Spreadsheet.</td></tr>
<tr>
<td>
ej.checkbox.min.js</td></tr>
<tr>
<td>
ej.radiobutton.min.js</td></tr>
<tr>
<td>
ej.dropdownlist.min.js</td></tr>
<tr>
<td>
ej.listbox.min.js</td></tr>
<tr>
<td>
ej.editor.min.js</td></tr>
<tr>
<td>
ej.menu.min.js</td></tr>
<tr>
<td>
ej.colorpicker.min.js</td></tr>
<tr>
<td>
ej.slider.min.js</td></tr>
<tr>
<td>
ej.splitbutton.min.js</td></tr>
<tr>
<td>
ej.togglebutton.min.js</td></tr>
<tr>
<td>
ej.toolbar.min.js</td></tr>
<tr>
<td>
ej.tab.min.js</td></tr>
<tr>
<td>
ej.uploadbox.min.js</td></tr>
<tr>
<td>
ej.draggable.min.js</td></tr>
<tr>
<td>
ej.datepicker.min.js</td></tr>
<tr>
<td>
ej.calculate.min.js</td><td>
Must be referred and used for formula in Spreadsheet.  </td></tr>
<tr>
<td>
ej.dialog.min.js</td><td>
Must be referred since dialog is used in various features in Spreadsheet.  </td></tr>
<tr>
<td>
ej.treeview.min.js</td><td>
Should be referred when Hyperlink options is enabled in Spreadsheet.  </td></tr>
<tr>
<td>
ej.excelfilter.min.js</td><td>
Should be referred when filtering is enabled in Spreadsheet.  </td></tr>
<tr>
<td>
ej.globalize.min.js</td><td>
It is referred when using localization in Spreadsheet.  </td></tr>
</table>
For getting started, you can use the `ej.web.all.min.js` file, which encapsulates all the `ej` controls and frameworks in one single file. For themes, you can use the `ej.web.all.min.css` or Use CDN links for scripts and CSS from the snippet given.To add the themes in your application, please refer to [this link](http://help.syncfusion.com/js/theming-in-essential-javascript-components). 

{% highlight html %}
<!DOCTYPE html>
<html>
    <head>
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
            <meta name="description" content="Essential Studio for JavaScript">
                <meta name="author" content="Syncfusion">
                    <title>Untitled</title>
                    <!-- Essential Studio for JavaScript  theme reference -->
                    <link rel="stylesheet" href="http://cdn.syncfusion.com/13.3.0.7/js/web/flat-azure/ej.web.all.min.css" />
                    <!-- Essential Studio for JavaScript  script references -->
                    <script src="https://code.jquery.com/jquery-1.10.2.min.js"></script>
                    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>
                    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"></script>
                    <script src="http://cdn.syncfusion.com/js/assets/external/jsrender.min.js"></script>
                    <script src="http://ajax.aspnetcdn.com/ajax/jquery.validate/1.14.0/jquery.validate.min.js"></script>
                    <script src="http://cdn.syncfusion.com/13.3.0.7/js/web/ej.web.all.min.js"></script>
                    <!--Add custom scripts here -->
                </head>
                <body></body>
            </html>
			{% endhighlight %}
			
N> In production, we highly recommend you to use our [custom script generator](http://helpjs.syncfusion.com/js/include-only-the-needed-widgets) to create custom script file with required controls and its dependencies only. Also to reduce the file size further please use [GZip compression](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer?hl=en) in your server.

## Creating ejSpreadsheet

The Spreadsheet control can be created from an HTML `DIV` element with `id` attribute.  To create the Spreadsheet, you should call the `ejSpreadsheet` jQuery plug-in function with the options as parameter.  The basic options to create Spreadsheet are `rowCount`, `colCount`, `activeSheetIndex`, `sheetCount` , `scrollSettings.width` and `scrollSettings.height`. Code snippet for loading `ejSpreadsheet` with minimal settings and to initialize with default data.

{% highlight html %}
<div id='Spreadsheet'></div>
<script>
        $(function () {
            $('#Spreadsheet').ejSpreadsheet({
                sheetCount: 3,
                activeSheetIndex: 1,
                scrollSettings: { height: 550, width: 1200 },
// JSON data can be loaded into Spreadsheet using rangeSettings.dataSource for particular sheet. This is optional
                sheets: [{
                    rangeSettings: { dataSource: window.defaultData, startCell: "A1", showHeader: true, }
                }],
                // the datasource "window.defaultData" is defaultData from 'http://js.syncfusion.com/demos/web/scripts/xljsondata.js'
            });
        });
    </script>
{% endhighlight %}

![](Getting-Started_images/Getting-Started_img1.png)


## Initialize from Excel File

The Spreadsheet control can be initialized from an Excel file by defining `importSettings.importUrl` with server endpoint. The server endpoint requires to be a .NET Web service or MVC controller/action, where excel file can be serialized in to JSON format, that the Spreadsheet can understand. The required .NET helper libraries are provided in Essential Studio build, please refer [this link](http://help.syncfusion.com/js/spreadsheet/server-configuration)  for configuring server.

{% highlight html %}
<div id='Spreadsheet'></div>
<script>
        $(function () {
            $('#Spreadsheet').ejSpreadsheet({
                sheetCount: 3,
                activeSheetIndex: 1,
                scrollSettings: { height: 550, width: 1200 },
                importSettings: {
                    importMapper: "http://js.syncfusion.com/ExportingServices/api/JSXLExport/Import",
                    importUrl: "http://mvc.syncfusion.com/beta/JSSpreadSheet/SpreadSheet.xlsx"
                },
            });
        });
    </script>
{% endhighlight %}

![](Getting-Started_images/Getting-Started_img2.png)


## Cell Navigation and Drag Fill

The Spreadsheet provides built-in support for cell navigation as in Microsoft Excel. The supported Key combinations are tabulated in the following table.

<table>
<tr>
<th>
Keys                     </th><th>
Description</th></tr>
<tr>
<td>
Tab</td><td>
Navigate to next cell in the row.  </td></tr>
<tr>
<td>
Shift + tab</td><td>
Navigate to previous cell in the row.  </td></tr>
<tr>
<td>
Enter</td><td>
Navigate to next cell in the column.  </td></tr>
<tr>
<td>
Shift + Enter </td><td>
Navigate to previous cell in the column.  </td></tr>
<tr>
<td>
Up</td><td>
Navigate to previous cell in the column.  </td></tr>
<tr>
<td>
Down</td><td>
Navigate to next cell in the column.  </td></tr>
<tr>
<td>
Left</td><td>
Navigate to previous cell in the row.  </td></tr>
<tr>
<td>
Right</td><td>
Navigate to next cell in the row.  </td></tr>
<tr>
<td>
Ctrl  + Up</td><td>
Navigate  to first cell in the column.  </td></tr>
<tr>
<td>
Ctrl + Down</td><td>
Navigate  to last cell in the column.  </td></tr>
<tr>
<td>
Ctrl + Left</td><td>
Navigate  to first cell in the row.  </td></tr>
<tr>
<td>
Ctrl + Right</td><td>
Navigate  to last cell in the row.  </td></tr>
<tr>
<td>
Shift  + Up</td><td>
Extend the selection Upward.  </td></tr>
<tr>
<td>
Shift + Down</td><td>
Extend the selection downwards.  </td></tr>
<tr>
<td>
Shift + Left</td><td>
Extend the selection in left.  </td></tr>
<tr>
<td>
Shift + Right</td><td>
Extend the selection in right.  </td></tr>
</table>
The Spreadsheet control also has support for excel like drag fill, which can be used to fill the adjacent cells data using a dragging fill handle of a selected cells. With drag fill, the following list of Auto fill options are also provided in Spreadsheet. 

1. Copy - repeat values (Text).
2. Series - fill data based on series (Number, Month, Day).
3. Formula Series - fill formula based on cell reference.
4. Formatting - repeat cell formats.

For auto filling, editing and auto fill should be enabled using `allowEditing` and `allowAutoFill`.

{% highlight html %}
<div id='Spreadsheet'></div>
<script>
        $(function () {
            $('#Spreadsheet').ejSpreadsheet({
                sheetCount: 3,
                activeSheetIndex: 1,
                scrollSettings: { height: 550, width: 1200 },
                importSettings: {
                    importMapper: "http://js.syncfusion.com/ExportingServices/api/JSXLExport/Import",
                    importUrl: "http://mvc.syncfusion.com/beta/JSSpreadSheet/SpreadSheet.xlsx"
                },
                allowEditing: true,
                allowAutofill: true

            });
        });
    </script>
{% endhighlight %}


![](Getting-Started_images/Getting-Started_img3.png)


## Creating Chart

The Spreadsheet control provides options to create chart through API and Ribbon. The chart can be created using ribbon similar to excel and to create using API, `XLChart.createChart()` should be called with the following parameters.

1. Range - Chart data from the range.
2. Chart options - for setting its width, height, type e.t.c.

{% highlight html %}
<div id='Spreadsheet'></div>
<script>
        $(function () {
            $('#Spreadsheet').ejSpreadsheet({
                sheetCount: 3,
                activeSheetIndex: 1,
                scrollSettings: { height: 550, width: 1200 },
                importSettings: {
                    importMapper: "http://js.syncfusion.com/ExportingServices/api/JSXLExport/Import",
                    importUrl: "http://mvc.syncfusion.com/beta/JSSpreadSheet/SpreadSheet.xlsx"
                },
                allowEditing: true,
                allowAutofill: true,
                allowDataValidation: true,
                loadComplete: function (args) {
                    this.XLChart.createChart("A1:B8", { type: "column", enable3D: false, marker: false, top: 40, left: 260, width: 400, height: 250 });
                }

            });
        });
    </script>
			{% endhighlight %}
			
![](Getting-Started_images/Getting-Started_img4.png)



