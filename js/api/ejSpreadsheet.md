---
layout: post
title: Properties, Methods and Events of ejSpreadsheet Widget
description: Methods,members and events avaliable in ejSpreadsheet
documentation: API
platform: js
keywords: ejSpreadsheet, API, Essential JS Spreadsheet
---

#ejSpreadsheet

The Spreadsheet can be easily configured to the DOM element, such as div. you can create a Spreadsheet with a highly customizable look and feel.

#### Syntax

{% highlight javascript %}

$(element).ejSpreadsheet(options)

{% endhighlight %}

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
{% highlight html %} 
options
{% endhighlight %}
</td>
<td class="type"><ts ref= "ej.Spreadsheet.Model"/><span class="param-type">object</span></td>
<td class="description">Settings for Spreadsheet.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// Create Spreadsheet
$('#Spreadsheet').ejSpreadsheet();
</script>

{% endhighlight %}

#### Requires

* jQuery.js
* jsrender.js
* jQuery.easing.min.js
* jQuery.validate.js
* ej.globalize.js
* ej.core.js
* ej.data.js
* ej.scroller.js
* ej.ribbon.js
* ej.chart.js
* ej.listbox.js
* ej.menu.js
* ej.colorpicker.js
* ej.slider.js
* ej.excelfilter.js
* ej.treeview.js
* ej.button.js
* ej.checkbox.js
* ej.draggable.js
* ej.waitingpopup.js
* ej.radiobutton.js
* ej.autocomplete.js
* ej.dropdownlist.js
* ej.datepicker.js
* ej.dialog.js
* ej.editor.js
* ej.pager.js
* ej.ribbon.js
* ej.uploadbox.js
* ej.togglebutton.js
* ej.calculate.js
* ej.tab.js
* ej.toolbar.js

## Members

### activeSheetIndex `Number`
{:#members:activesheetindex}


Gets or sets an active sheet index in the Spreadsheet. By defining this value, you can specify which sheet should be active in workbook.

#### Default Value
* 1


#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
$('#Spreadsheet').ejSpreadsheet({
sheetCount: 5,
activeSheetIndex: 3
});         
</script>

{% endhighlight %}

### allowAutoCellType `Boolean`
{:#members:allowautocelltype}

Gets or sets a value that indicates whether to enable or disable auto rendering of cell type in the Spreadsheet. 

#### Default Value
* false


Note: allowCellType must be true while using the allowAutoCellType.

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({   
allowCellType: true,
allowAutoCellType:true
});        
</script>

{% endhighlight %}

### allowAutoFill `Boolean`
{:#members:allowautofill}

Gets or sets a value that indicates whether to enable or disable auto fill feature in the Spreadsheet. 

#### Default Value
* true

#### Example
{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({   
allowAutoFill: true
});        
</script>


{% endhighlight %}

### allowAutoSum `Boolean`
{:#members:allowautosum}

Gets or sets a value that indicates whether to enable or disable auto sum feature in the Spreadsheet.

#### Default Value
* true


#### Example
{% highlight html %}
<div id="Spreadsheet"></div>
<script>
$('#Spreadsheet').ejSpreadsheet({ 
allowAutoSum: true
});         
</script>


{% endhighlight %}

### allowCellFormatting `Boolean`
{:#members:allowcellformatting}

Gets or sets a value that indicates whether to enable or disable cell format feature in the Spreadsheet. By enabling this, you can customize styles and number formats.

#### Default Value
* true


#### Example
{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({ 
allowCellFormatting : true
});                     
</script>

{% endhighlight %}

### allowCellType `Boolean`
{:#members:allowcelltype}

Gets or sets a value that indicates whether to enable or disable cell type feature in the Spreadsheet.

#### Default Value
* false

#### Example
{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({ 
allowCellType : true
});                     
</script>

{% endhighlight %}

### allowCharts `Boolean`
{:#members:allowcharts}

Gets or sets a value that indicates whether to enable or disable chart feature in the Spreadsheet. By enabling this feature, you can create and customize charts in Spreadsheet.

#### Default Value
* true


#### Example
{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({ 
allowCharts: true
}); 
</script>


{% endhighlight %}

### allowClipboard `Boolean`
{:#members:allowclipboard}

Gets or sets a value that indicates whether to enable or disable clipboard feature in the Spreadsheet. By enabling this feature, you can perform cut/copy and paste operations in Spreadsheet.

#### Default Value
* true


#### Example
{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({ 
allowClipboard : true                    
});
</script>


{% endhighlight %}

### allowComments `Boolean`
{:#members:allowcomments}

Gets or sets a value that indicates whether to enable or disable comment feature in the Spreadsheet. By enabling this, you can add/delete/modify comments in Spreadsheet.

#### Default Value
* true

#### Example
{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({ 
allowComments: true
});         
</script>


{% endhighlight %}

### allowConditionalFormats `Boolean`
{:#members:allowconditionalformats}

Gets or sets a value that indicates whether to enable or disable Conditional Format feature in the Spreadsheet. By enabling this, you can apply formatting to the selected range of cells based on the provided conditions (Greater than, Less than, Equal, Between, Contains, etc.).
Note: allowCellFormatting must be true while using conditional formatting.

#### Default Value
* true


#### Example
{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
allowCellFormatting : true,
allowConditionalFormats : true         
});
</script>


{% endhighlight %}

### allowDataValidation `Boolean`
{:#members:allowdatavalidation}

Gets or sets a value that indicates whether to enable or disable data validation feature in the Spreadsheet.

#### Default Value
* true


#### Example
{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({ 
allowDataValidation: true                   
});
</script>


{% endhighlight %}

### allowDelete `Boolean`
{:#members:allowdelete}

Gets or sets a value that indicates whether to enable or disable the delete action in the Spreadsheet. By enabling this feature, you can delete existing rows, columns, cells and sheet.
 
#### Default Value
* true


#### Example
{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({ 
allowDelete: true
});         
</script>


{% endhighlight %}

### allowDragAndDrop `Boolean`
{:#members:allowdraganddrop}

Gets or sets a value that indicates whether to enable or disable drag and drop feature in the Spreadsheet.

#### Default Value
* true


#### Example
{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({ 
allowDragAndDrop: true
});         
</script>


{% endhighlight %}

### allowEditing `Boolean`
{:#members:allowediting}

Gets or sets a value that indicates whether to enable or disable the edit action in the Spreadsheet.

#### Default Value
* true


#### Example
{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({ 
allowEditing: true
});         
</script>


{% endhighlight %}

### allowFiltering `Boolean`
{:#members:allowfiltering}

Gets or sets a value that indicates whether to enable or disable filtering feature in the Spreadsheet. Filtering can be used to limit the data displayed using required criteria.

#### Default Value
* true


#### Example
{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({ 
allowFiltering: true
});         
</script>


{% endhighlight %}

### allowFormatAsTable `Boolean`
{:#members:allowformatastable}

Gets or sets a value that indicates whether to enable or disable table feature in the Spreadsheet. By enabling this, you can render table in selected range.

Note: allowCellFormatting and allowFiltering must be true while using format as table.

#### Default Value
* true


#### Example
{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({ 
allowCellFormatting  :true,
allowFiltering:true,
allowFormatAsTable: true
});         
</script>


{% endhighlight %}

### allowFormatPainter `Boolean`
{:#members:allowformatpainter}

Get or sets a value that indicates whether to enable or disable format painter feature in the Spreadsheet. By enabling this feature, you can copy the format from the selected range and apply it to another range.

Note: allowCellFormatting must be true while enable this feature.

#### Default Value
* true


#### Example
{% highlight html %}
<div id="Spreadsheet"></div>  
<script>
$('#Spreadsheet').ejSpreadsheet({ 
allowCellFormatting: true,
allowFormatPainter: true
});         
</script>


{% endhighlight %}

### allowFormulaBar `Boolean`
{:#members:allowformulabar}

Gets or sets a value that indicates whether to enable or disable formula bar in the Spreadsheet.

#### Default Value
* true


#### Example
{% highlight html %}
<div id="Spreadsheet"></div>  
<script>
$('#Spreadsheet').ejSpreadsheet({ 
allowFormulaBar: false
});         
</script>


{% endhighlight %}

### allowFreezing `Boolean`
{:#members:allowfreezing}

Gets or sets a value that indicates whether to enable or disable freeze pane support in Spreadsheet. After enabling this feature, you can use freeze top row, freeze first column and freeze panes options.

#### Default Value
* true


#### Example
{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
allowFreezing : true
});
</script>


{% endhighlight %}

### allowHyperlink `Boolean`
{:#members:allowhyperlink}

Gets or sets a value that indicates whether to enable or disable hyperlink feature in the Spreadsheet. By enabling this feature, you can add hyperlink which is used to easily navigate to the cell reference from one sheet to another or a web page.

#### Default Value
* true


#### Example
{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({ 
allowHyperlink: true
});         
</script>


{% endhighlight %}

### allowImport `Boolean`
{:#members:allowimport}

Gets or sets a value that indicates whether to enable or disable import feature in the Spreadsheet. By enabling this feature, you can open existing Spreadsheet documents. 

Note: Need to specify importMapper while enabling this feature. Import feature supports XLS, XLSX file formats.

#### Default Value
* true


#### Example
{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({ 
allowImport: true,
importSettings:
{
importMapper: "http://js.syncfusion.com/ExportingServices/api/JSXLExport/Import"
}
});         
</script>


{% endhighlight %}

### allowInsert `Boolean`
{:#members:allowinsert}

Gets or sets a value that indicates whether to enable or disable the insert action in the Spreadsheet. By enabling this feature, you can insert new rows, columns, cells and sheet.

#### Default Value
* true


#### Example
{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
allowInsert: true
});         
</script>


{% endhighlight %}

### allowKeyboardNavigation `Boolean`
{:#members:allowkeyboardnavigation}

Gets or sets a value that indicates whether to enable or disable keyboard navigation feature in the Spreadsheet.

#### Default Value
* true


#### Example
{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
allowKeyboardNavigation: true
});         
</script>


{% endhighlight %}

### allowLockCell `Boolean`
{:#members:allowlockcell}

Gets or sets a value that indicates whether to enable or disable lock cell feature in the Spreadsheet. 

#### Default Value
* true

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({ 
allowLockCell: true                     
});
</script>
{% endhighlight %}

### allowMerging `Boolean`
{:#members:allowmerging}

Gets or sets a value that indicates whether to enable or disable merge feature in the Spreadsheet.

#### Default Value
* true

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
allowMerging: true
});         
</script>

{% endhighlight %}

### allowResizing `Boolean`
{:#members:allowresizing}

Gets or sets a value that indicates whether to enable or disable resizing feature in the Spreadsheet. By enabling this feature, you can change the column width and row height by dragging its header boundaries.

#### Default Value
* true

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
allowResizing: true
});         
</script>

{% endhighlight %}

### allowSearching `Boolean`
{:#members:allowsearching}

Gets or sets a value that indicates whether to enable or disable find and replace feature in the Spreadsheet. By enabling this, you can easily find and replace a specific value in the sheet or workbook. By using goto behavior, you can select and highlight all cells that contains specific data or data types.

#### Default Value
* true

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
allowSearching : true
});        
</script>

{% endhighlight %}

### allowSelection `Boolean`
{:#members:allowselection}

Gets or sets a value that indicates whether to enable or disable selection in the Spreadsheet. By enabling this feature, selected items will be highlighted.

#### Default Value
* true

#### Example
{% highlight html %}
<div id="Spreadsheet"></div>
 
<script>
$('#Spreadsheet').ejSpreadsheet({ 
    allowSelection: true
});         
</script>

{% endhighlight %}

### allowSorting `Boolean`
{:#members:allowsorting}

Gets or sets a value that indicates whether to enable the sorting feature in the Spreadsheet. 

#### Default Value
* true

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({ 
allowSorting: true
});         
</script>

{% endhighlight %}

### allowUndoRedo `Boolean`
{:#members:allowundoredo}

Gets or sets a value that indicates whether to enable or disable undo and redo feature in the Spreadsheet.

#### Default Value
* true

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({ 
allowUndoRedo: true                    
});
</script>

{% endhighlight %}

### allowWrap `Boolean`
{:#members:allowwrap}

Gets or sets a value that indicates whether to enable or disable wrap text feature in the Spreadsheet. By enabling this, cell content can wrap to the next line, if the cell content exceeds the boundary of the cell.

#### Default Value
* true

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({ 
allowWrap: true                     
});
</script>

{% endhighlight %}

### apWidth `Number`
{:#members:apwidth}

Gets or sets a value that indicates to define the width of the activation panel in Spreadsheet.

#### Default Value
* 200

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
$('#Spreadsheet').ejSpreadsheet({ 
apWidth: 100
});         
</script>

{% endhighlight %}

### autoFillSettings `Object`
{:#members:autofillsettings}

Gets or sets an object that indicates to customize the auto fill behavior in the Spreadsheet.

### autoFillSettings.fillType `Enum` 
{:#members:autofillsettings-filltype}

<ts name="ej.Spreadsheet.AutoFillOptions"/>

This property is used to set fillType unit in Spreadsheet. It has five types which are CopyCells, FillSeries, FillFormattingOnly, FillWithoutFormatting and FlashFill.

Note: allowAutoFill must be true while setting fillType. 

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">CopyCells</td>
<td class="description">Specifies the CopyCells property in AutoFillOptions.</td>
</tr>
<tr>
<td class="name">FillSeries</td>
<td class="description">Specifies the FillSeries property in AutoFillOptions.</td>
</tr>
<tr>
<td class="name">FillFormattingOnly</td>
<td class="description">Specifies the FillFormattingOnly property in AutoFillOptions.</td>
</tr>
<tr>
<td class="name">FillWithoutFormatting</td>
<td class="description">Specifies the FillWithoutFormatting property in AutoFillOptions.</td>
</tr>
<tr>
<td class="name">FlashFill</td>
<td class="description">Specifies the FlashFill property in AutoFillOptions.</td>
</tr>
</tbody>
</table>

#### Default Value
* ej.Spreadsheet.AutoFillOptions.FillSeries



#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
allowAutoFill: true,
autoFillSettings({
fillType: ej.Spreadsheet.AutoFillOptions.CopyCells
})
});  
</script>

{% endhighlight %}

### autoFillSettings.showFillOptions `Boolean`
{:#members:autofillsettings-showfilloptions}

Gets or sets a value that indicates to enable or disable auto fill options in the Spreadsheet.

Note: allowAutoFill must be true while enabling this property.

#### Default Value
* true

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
allowAutoFille: true,
autoFillSettings({
showFillOptions: true
})
});  
</script>

{% endhighlight %}

### chartSettings `Object`
{:#members:chartsettings}

Gets or sets an object that indicates to customize the chart behavior in the Spreadsheet.

### chartSettings.height `Number`
{:#members:chartsettings-height}

Gets or sets a value that defines the chart height in Spreadsheet.

#### Default Value
* 220

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({ 
allowCharts: true,
chartSettings: {
height : 300
}
}); 
</script>

{% endhighlight %}

### chartSettings.width `Number`
{:#members:chartsettings-width}

Gets or sets a value that defines the chart width in the Spreadsheet.

#### Default Value
* 440

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({ 
allowCharts: true,
chartSettings: {
width : 500
}
}); 
</script>

{% endhighlight %}

### columnCount `Number`
{:#members:columncount}

Gets or sets a value that defines the number of columns displayed in the sheet.

#### Default Value
* 21


#### Example
{% highlight html %}
<div id="Spreadsheet"></div>
<script>
$('#Spreadsheet').ejSpreadsheet({ 
columnCount: 30
});         
</script>

{% endhighlight %}

### columnWidth `Number`
{:#members:columnwidth}

Gets or sets a value that indicates to define the common width for each column in the Spreadsheet.

#### Default Value
* 64

#### Example
{% highlight html %}
<div id="Spreadsheet"></div>
<script>
$('#Spreadsheet').ejSpreadsheet({ 
columnWidth: 100
});         
</script>

{% endhighlight %}

### cssClass `String`
{:#members:cssclass}

Gets or sets a value that indicates to render the spreadsheet with custom theme.

#### Default Value
* ""

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
// Set the CSS class during initialization. 
$('#Spreadsheet').ejSpreadsheet({
cssClass: "gradient-lime"
});        
</script>

{% endhighlight %}

### customFormulas `Object`
{:#members:customformulas}

Gets or sets a value that indicates custom formulas in Spreadsheet.

#### Default Value
* []

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
// Set the custom formula
$('#Spreadsheet').ejSpreadsheet({
customFormulas: [{
	formulaName:"CUSTOMTOTAL",
	functionName:"customTotal"
}]
});   
function customTotal(args){}//args-It uses the value given by the user while using custom formula in Spreadsheet.
</script>

{% endhighlight %}

### enableContextMenu `Boolean`
{:#members:enablecontextmenu}

Gets or sets a value that indicates whether to enable or disable context menu in the Spreadsheet.

#### Default Value
* true

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({ 
enableContextMenu: true
});                   
</script>

{% endhighlight %}

### enablePivotTable `Boolean`
{:#members:enablepivottable}

Gets or sets a value that indicates whether to enable or disable pivot table in the Spreadsheet.

#### Default Value
* false

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({ 
enablePivotTable: false
});                   
</script>

{% endhighlight %}

### exportSettings `Object`
{:#members:exportsettings}

Gets or sets an object that indicates to customize the exporting behavior in Spreadsheet.

### exportSettings.allowExporting `Boolean`
{:#members:exportsettings-allowexporting}

Gets or sets a value that indicates whether to enable or disable save feature in Spreadsheet. By enabling this feature, you can save existing Spreadsheet.

N> User must specify excelUrl or csvUrl while enabling this feature

#### Default Value
* true

#### Example
{% highlight html %}

<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
exportSettings({
allowExporting: true,
csvUrl: "http://js.syncfusion.com/ExportingServices/api/JSXLExport/ExportToCsv", // It is used to set the url of the csv export.
excelUrl: "http://js.syncfusion.com/ExportingServices/api/JSXLExport/ExportToExcel", //It is used to set the url of the excel export.
})
});        
</script>

{% endhighlight %}

### exportSettings.csvUrl `String`
{:#members:exportsettings-csvurl}

Gets or sets a value that indicates to define csvUrl for export to CSV format.

Note: User must specify allowExporting true while use this property.

#### Default Value
* null

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
exportSettings({
allowExporting: true,
csvUrl: "http://js.syncfusion.com/ExportingServices/api/JSXLExport/ExportToCsv", // It is used to set the url of the csv export.
})
});        
</script>

{% endhighlight %}

### exportSettings.excelUrl `String`
{:#members:exportsettings-excelurl}

Gets or sets a value that indicates to define excelUrl for export to excel format.
Note: User must specify allowExporting true while use this property.

#### Default Value
* null

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
exportSettings({
allowExporting: true,
excelUrl: "http://js.syncfusion.com/ExportingServices/api/JSXLExport/ExportToExcel", //It is used to set the url of the excel export.
})
});        
</script>

{% endhighlight %}

### exportSettings.password `String`
{:#members:exportsettings-password}

Gets or sets a value that indicates to define password while export to excel format.

Note: User must specify allowExporting true while use this property.

#### Default Value
* null

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
exportSettings({
allowExporting: true,
excelUrl: "http://js.syncfusion.com/ExportingServices/api/JSXLExport/ExportToExcel", //It is used to set the url of the excel export
password :"Spreadsheet"
})
});        
</script>

{% endhighlight %}

### formatSettings `Object`
{:#members:formatsettings}

Gets or sets an object that indicates to customize the format behavior in the Spreadsheet.

### formatSettings.allowCellBorder `Boolean`
{:#members:formatsettings-allowcellborder}

Gets or sets a value that indicates whether to enable or disable cell border feature in the Spreadsheet.

Note: allowCellFormatting must be true while using this property.

#### Default Value
* true

#### Example
{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
allowCellFormatting: true,
formatSettings({
allowCellBorder: true
})
});  
</script>

{% endhighlight %}

### formatSettings.allowDecimalPlaces `Boolean`
{:#members:formatsettings-allowdecimalplaces}

Gets or sets a value that indicates whether to enable or disable decimal places in the Spreadsheet.

Note: allowCellFormatting must be true while using this property.

#### Default Value
* true

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
allowCellFormatting: true,
formatSettings({
allowDecimalPlaces: true
})
});  
</script>

{% endhighlight %}

### formatSettings.allowFontFamily `Boolean`
{:#members:formatsettings-allowfontfamily}

Gets or sets a value that indicates whether to enable or disable font family feature in Spreadsheet.

Note: allowCellFormatting must be true while using this property. 

#### Default Value
* true

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
allowCellFormatting : true,
formatSettings({
allowFontFamily: true
})
});  
</script>

{% endhighlight %}

### importOnLoad `Boolean`
{:#members:importonload}

Gets or sets a value that indicates whether to enable or disable import while initial loading.

#### Default Value
* false

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({ 
importOnLoad: false
});                   
</script>

{% endhighlight %}

### importSettings `Object`
{:#members:importsettings}

Gets or sets an object that indicates to customize the import behavior in the Spreadsheet.

### importSettings.importMapper `String`
{:#members:importsettings-importmapper}

Sets import mapper to perform import feature in Spreadsheet.

Note: allowImport must be true while using this property.

#### Default Value
* ""

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
allowImport: true,
importSettings({
importMapper: "http://js.syncfusion.com/ExportingServices/api/JSXLExport/Import",
})
});        
</script>

{% endhighlight %}

### importSettings.importUrl `String`
{:#members:importsettings-importurl}

Sets import URL to access the online files in the Spreadsheet.

Note: allowImport must be true while using this property.

#### Default Value
* ""

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
allowImport: true,
importSettings({
importUrl: "http://mvc.syncfusion.com/beta/JSSpreadSheet/SpreadSheet.xlsx", //It is used to access the online files in Spreadsheet.
})
});        
</script>

{% endhighlight %}

### importSettings.password `String`
{:#members:importsettings-password}

Gets or sets a value that indicates to define password while importing in the Spreadsheet.

Note: allowImport must be true while using this property.

#### Default Value
* ""

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
allowImport: true,
importSettings({
importMapper: "http://js.syncfusion.com/ExportingServices/api/JSXLExport/Import",
password: "Spreadsheet" //It is used to set password for sheet.
})
});        
</script>

{% endhighlight %}

### locale `String`
{:#members:locale}

Gets or sets a value that indicates whether to customizing the user interface (UI) as locale-specific in order to display regional data (i.e.) in a language and culture specific to a particular country or region.

#### Default Value
* "en-US"

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
ej.Spreadsheet.locale["es-ES"] = {
Sheet: "Hoja"
};             
$('#Spreadsheet').ejSpreadsheet({ 
locale: "es-ES"
});         
</script>

{% endhighlight %}

### pictureSettings `Object`
{:#members:picturesettings}

Gets or sets an object that indicates to customize the picture behavior in the Spreadsheet.

### pictureSettings.allowPictures `Boolean`
{:#members:picturesettings-allowpictures}

Gets or sets a value that indicates whether to enable or disable picture feature in Spreadsheet. By enabling this, you can add pictures in Spreadsheet.

#### Default Value
* true

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
pictureSettings({
allowPictures: true,
})
});    
</script>

{% endhighlight %}

### pictureSettings.height `Number`
{:#members:picturesettings-height}

Gets or sets a value that indicates to define height to picture in the Spreadsheet.

#### Default Value
* 220

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
pictureSettings({
allowPictures: true,
height: 300
})
});    
</script>

{% endhighlight %}

### pictureSettings.width `Number`
{:#members:picturesettings-width}

Gets or sets a value that indicates to define width to picture in the Spreadsheet.

#### Default Value
* 440

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
pictureSettings({
allowPictures: true,
width: 500
})
});    
</script>

{% endhighlight %}

### printSettings `Object`
{:#members:printsettings}

Gets or sets an object that indicates to customize the print option in Spreadsheet.

### printSettings.allowPageSetup `Boolean`
{:#members:printsettings-allowpagesetup}

Gets or sets a value that indicates whether to enable or disable page setup support for printing in Spreadsheet. 

Note: allowPrinting must be true while enabling allowPageSetup.

#### Default Value
* true

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
allowPrinting: true,
printSettings({
allowPageSetup: true
})
});   
</script>

{% endhighlight %}

### printSettings.allowPageSize `Boolean`
{:#members:printsettings-allowpagesize}

Gets or sets a value that indicates whether to enable or disable page size support for printing in Spreadsheet.

Note: allowPrinting must be true while enabling allowPageSetup.

#### Default Value
* false

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
allowPrinting: true,
printSettings({
allowPageSize: true
})
});   
</script>

{% endhighlight %}

### printSettings.allowPrinting `Boolean`
{:#members:printsettings-allowprinting}

Gets or sets a value that indicates whether to enable or disable print feature in the Spreadsheet.

#### Default Value
* true

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
printSettings({
allowPrinting: true
})
});   
</script>

{% endhighlight %}

### rowCount `Number`
{:#members:rowcount}

Gets or sets a value that indicates whether to define the number of rows to be displayed in the sheet.

#### Default Value
* 20

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({ 
rowCount: 30
});         
</script>

{% endhighlight %}

### rowHeight `Number`
{:#members:rowheight}

Gets or sets a value that indicates to define the common height for each row in the sheet.

#### Default Value
* 20

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({ 
rowHeight: 30
});         
</script>

{% endhighlight %}

### scrollSettings `Object`
{:#members:scrollsettings}

Gets or sets an object that indicates to customize the scroll options in the Spreadsheet.

### scrollSettings.allowScrolling `Boolean`
{:#members:scrollsettings-allowscrolling}

Gets or sets a value that indicates whether to enable or disable scrolling in Spreadsheet.

#### Default Value
* true

#### Example
{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
scrollSettings({
allowScrolling: true,
})
});    
</script>

{% endhighlight %}

### scrollSettings.allowSheetOnDemand `Boolean`
{:#members:scrollsettings-allowsheetondemand}

Gets or sets a value that indicates whether to enable or disable sheet on demand. By enabling this, it render only the active sheet element while paging remaining sheets are created one by one.

#### Default Value
* false

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
scrollSettings({
allowScrolling: true,
allowSheetOnDemand: true,
})
});    
</script>

{% endhighlight %}

### scrollSettings.allowVirtualScrolling `Boolean`
{:#members:scrollsettings-allowvirtualscrolling}

Gets or sets a value that indicates whether to enable or disable virtual scrolling feature in the Spreadsheet.

Note: allowScrolling must be true while enabling allowVirtualScrolling.

#### Default Value
* true

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
scrollSettings({
allowScrolling: true,
allowVirtualScrolling: true
})
});    
</script>

{% endhighlight %}

### scrollSettings.height  `Number|String`
{:#members:scrollsettings-height}

Gets or sets the value that indicates to define the height of spreadsheet.

#### Default Value
* 550

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
scrollSettings({
allowScrolling: true,
height: 600
})
});    
</script>

{% endhighlight %}

### scrollSettings.isResponsive `Boolean`
{:#members:scrollsettings-isresponsive}

Gets or sets the value that indicates whether to enable or disable responsive mode in the Spreadsheet.

#### Default Value
* false

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
scrollSettings({
allowScrolling: true,
width: "100%",
height: "100%",
isResponsive: true
})
});    
</script>

{% endhighlight %}

### scrollSettings.scrollMode `Enum`
{:#members:scrollsettings-scrollmode}

<ts name="ej.Spreadsheet.scrollMode"/>

Gets or sets a value that indicates to set scroll mode in Spreadsheet. It has two scroll modes, Normal and Infinite.

Note: allowScrolling must be true while enabling this property.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Infinite</td>
<td class="description">To enable Infinite scroll mode for Spreadsheet.</td>
</tr>
<tr>
<td class="name">Normal</td>
<td class="description">To enable Normal scroll mode for Spreadsheet.</td>
</tr>
</tbody>
</table>

#### Default Value
* ej.Spreadsheet.scrollMode.Infinite



#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
scrollSettings({
allowScrolling: true,
height: "100%",
width: "100%",
scrollmode: ej.Spreadsheet.scrollMode.Infinite,
})
});    
</script>

{% endhighlight %}

### scrollSettings.width `Number|String`
{:#members:scrollsettings-width}

Gets or sets the value that indicates to define the height off spreadsheet.

#### Default Value
* 1300

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
scrollSettings({
allowScrolling: true,
width: 1300,
scrollmode: ej.Spreadsheet.scrollMode.Infinite
})
});    
</script>

{% endhighlight %}

### selectionSettings `Object`
{:#members:selectionsettings}

Gets or sets an object that indicates to customize the selection options in the Spreadsheet.

### selectionSettings.activeCell `String`
{:#members:selectionsettings-activecell}

Gets or sets a value that indicates to define active cell in spreadsheet.

Note: allowSelection must be true while using this property.

#### Default Value
* ""

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
allowSelection: true,
selectionSettings({
activeCell: "A1"
})
});
</script>

{% endhighlight %}

### selectionSettings.animationTime `Number`
{:#members:selectionsettings-animationtime}

Gets or sets a value that indicates to define animation time while selection in the Spreadsheet.

Note: allowSelection and enableAnimation must be true while using this property.

#### Default Value
* 0.001

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
allowSelection: true,
selectionSettings({
enableAnimation: true,
animationTime: 0.002
})
});
</script>

{% endhighlight %}

### selectionSettings.enableAnimation `Boolean`
{:#members:selectionsettings-enableanimation}

Gets or sets a value that indicates to enable or disable animation while selection.
Note: allowSelection must be true while using this property.

#### Default Value
* false

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
allowSelection: true,
selectionSettings({
enableAnimation: true
})
});
</script>

{% endhighlight %}

### selectionSettings.selectionType `Enum`
{:#members:selectionsettings-selectiontype}

<ts name="ej.Spreadsheet.SelectionType"/>

Gets or sets a value that indicates to set selection type in Spreadsheet. It has three types which are Column, Row and Default.

N> [`allowSelection`](http://help.syncfusion.com/js/api/ejspreadsheet#members:allowselection "allowSelection") must be `true` while using this property

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Column</td>
<td class="description">To select only Column in Spreadsheet.</td>
</tr>
<tr>
<td class="name">Row</td>
<td class="description">To select only Row in Spreadsheet.</td>
</tr>
<tr>
<td class="name">Default</td>
<td class="description">To select both Column/Row in Spreadsheet.</td>
</tr>
</tbody>
</table>

#### Default Value
* ej.Spreadsheet.SelectionType.Default

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>

<script>
$('#Spreadsheet').ejSpreadsheet({
    allowSelection: true,
    selectionSettings({
        selectionType: ej.Spreadsheet.SelectionType.Default,
        animationTime: 0.001,
        enableAnimation: true
    })
});
</script>
{% endhighlight %}

### selectionSettings.selectionUnit `Enum`
{:#members:selectionsettings-selectionunit}

<ts name="ej.Spreadsheet.SelectionUnit"/>

Gets or sets a value that indicates to set selection unit in Spreadsheet. It has three types which are Single, Range and MultiRange.

N> [`allowSelection`](http://help.syncfusion.com/js/api/ejspreadsheet#members:allowselection "allowSelection") must be `true` while using this property
	
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Single</td>
<td class="description">To enable Single selection in Spreadsheet</td>
</tr>
<tr>
<td class="name">Range</td>
<td class="description">To enable Range selection in Spreadsheet</td>
</tr>
<tr>
<td class="name">MultiRange</td>
<td class="description">To enable MultiRange selection in Spreadsheet</td>
</tr>
</tbody>
</table>

#### Default Value
* ej.Spreadsheet.SelectionUnit.MultiRange

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>

<script>
$('#Spreadsheet').ejSpreadsheet({
    allowSelection: true,
    selectionSettings({
        selectionUnit: ej.Spreadsheet.SelectionUnit.Single
    })
});  
</script>

{% endhighlight %}

### sheetCount `Number`
{:#members:sheetcount}

Gets or sets a value that indicates to define the number of sheets to be created at the initial load.

#### Default Value
* 1

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({ 
sheetCount: 5
});         
</script>

{% endhighlight %}

### sheets `Array`
{:#members:sheets}

Gets or sets an object that indicates to customize the sheet behavior in Spreadsheet.

### sheets.colCount `Number`
{:#members:sheets-colcount}

Gets or sets a value that indicates to define column count in the Spreadsheet.

#### Default Value:

* 21

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
sheets:[{
rangeSettings: [{dataSource: window.defaultData, startCell: "A1"}],
colCount: 25
}]
});    
</script>

{% endhighlight %}

### sheets.columnWidth `Number`
{:#members:sheets-columnwidth}

Gets or sets a value that indicates to define column width in the Spreadsheet.

#### Default Value:

* 64 

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
sheets:[{
        columnWidth: 100
    }]
});    
</script>

{% endhighlight %}

### sheets.dataSource `Object`
{:#members:sheets-datasource}

Gets or sets the data to render the Spreadsheet.

#### Default Value:

* -

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>

<script>
$('#Spreadsheet').ejSpreadsheet({
    sheets:[{
        // the datasource "window.defaultData" is referred from 'http://js.syncfusion.com/demos/web/scripts/xljsondata.js'
        dataSource: window.defaultData;
    }]
});    
</script>
{% endhighlight %}

### sheets.fieldAsColumnHeader `Boolean`
{:#members:sheets-fieldascolumnheader}

Gets or sets a value that indicates whether to enable or disable field as column header in the Spreadsheet.

#### Default Value:

* false

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
var dataManager = ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Orders/");
$('#Spreadsheet').ejSpreadsheet({
sheets:[{
dataSource: dataManager,
query: ej.Query().take(50).select(["OrderID", "CustomerID", "EmployeeID", "ShipName", "ShipAddress", "ShipCity", "ShipCountry"]),
fieldAsColumnHeader: true,
primaryKey: "OrderID"
}]
});    
</script>

{% endhighlight %}

### sheets.headerStyles `Object`
{:#members:sheets-headerstyles}

Specifies the header styles for the datasource range in Spreadsheet.

#### Default Value:

* null

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
sheets:[{
dataSource: window.defaultData, showHeader: true, headerStyles: { "font-weight": "bold", "vertical-align": "middle", "text-align": "center", "background-color": "#559ad9", "color": "#FFFFFF" }}]
});    
</script>

{% endhighlight %}

### sheets.primaryKey `String`
{:#members:sheets-primarykey}

Specifies the primary key for the datasource in Spreadsheet.

#### Default Value:

* ""

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
var dataManager = ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Orders/");
$('#Spreadsheet').ejSpreadsheet({
sheets:[{
dataSource: dataManager,
query: ej.Query().take(50).select(["OrderID", "CustomerID", "EmployeeID", "ShipName", "ShipAddress", "ShipCity", "ShipCountry"]),
primaryKey: "OrderID"
}]
});    
</script>

{% endhighlight %}

### sheets.query `Object`
{:#members:sheets-query}

Specifies the query for the [`dataSource`](http://help.syncfusion.com/js/api/ejspreadsheet#members:sheets-datasource "dataSource") in Spreadsheet.

#### Default Value:

* null

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 

<script>
var dataManager = ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Orders/");
$('#Spreadsheet').ejSpreadsheet({
    sheets:[{
        dataSource: dataManager,
        query: ej.Query().take(50).select(["OrderID", "CustomerID", "EmployeeID", "ShipName", "ShipAddress", "ShipCity", "ShipCountry"])
    }]
});    
</script>
{% endhighlight %}

### sheets.rangeSettings `Array`
{:#members:sheets-rangesettings}

Specifies single range or multiple range settings for a sheet in Spreadsheet.

#### Default Value:

* -

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
sheets:[
{rangeSettings: [{dataSource: window.defaultData, showHeader: true, startCell: "A1"}]},
{rangeSettings: [{dataSource: window.personList, showHeader: true, startCell: "D1"}]}
]
});    
</script>

{% endhighlight %}

### sheets.rangeSettings.dataSource `Object`
{:#members:sheets-rangesettings-datasource}

Gets or sets the data to render the Spreadsheet.

#### Default Value:

* -

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
sheets:[{
rangeSettings: [{dataSource: window.defaultData, showHeader: true, startCell: "A1"}]}]
});    
</script>

{% endhighlight %}

### sheets.rangeSettings.headerStyles `Object`
{:#members:sheets-rangesettings-headerstyles}

Specifies the header styles for the datasource range in Spreadsheet.

#### Default Value:

* null

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
sheets:[{
rangeSettings: [{dataSource: window.defaultData, showHeader: true, headerStyles: { "font-weight": "bold", "vertical-align": "middle", "text-align": "center", "background-color": "#559ad9", "color": "#FFFFFF" }}]}]
});    
</script>

{% endhighlight %}

### sheets.rangeSettings.primaryKey `String`
{:#members:sheets-rangesettings-primarykey}

Specifies the primary key for the datasource in Spreadsheet.

#### Default Value:

* ""

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
var dataManager = ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Orders/");
$('#Spreadsheet').ejSpreadsheet({
sheets:[{
dataSource: dataManager,
sheets:[{
        query: ej.Query().take(50).select(["OrderID", "CustomerID", "EmployeeID", "ShipName", "ShipAddress", "ShipCity", "ShipCountry"]),
        primaryKey: "OrderID"
    }]
}]
});    
</script>

{% endhighlight %}

### sheets.rangeSettings.query `Object`
{:#members:sheets-rangesettings-query}

Specifies the query for the datasource in Spreadsheet.

#### Default Value:

* null

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
var dataManager = ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Orders/");
$('#Spreadsheet').ejSpreadsheet({
sheets:[{
dataSource: dataManager,
rangeSettings:[{
    query: ej.Query().take(50).select(["OrderID", "CustomerID", "EmployeeID", "ShipName", "ShipAddress", "ShipCity", "ShipCountry"])
    }]
}]
});    
</script>

{% endhighlight %}

### sheets.rangeSettings.showHeader `Boolean`
{:#members:sheets-rangesettings-showheader}

Gets or sets a value that indicates whether to enable or disable the datasource header in Spreadsheet.

#### Default Value:

* false

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
sheets:[{
rangeSettings: [{dataSource: window.defaultData, showHeader: true}]}]
});    
</script>

{% endhighlight %}

### sheets.rangeSettings.startCell `String`
{:#members:sheets-rangesettings-startcell}

Specifies the start cell for the datasource range in Spreadsheet.

#### Default Value:

* "A1"

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
sheets:[{
rangeSettings: [{dataSource: window.defaultData, startCell: "A1"}]}]
});    
</script>

{% endhighlight %}

### sheets.rowCount `Number`
{:#members:sheets-rowcount}

Gets or sets a value that indicates to define row count in the Spreadsheet.

#### Default Value:

* 20

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
sheets:[{
rangeSettings: [{dataSource: window.defaultData, startCell: "A1"}],
rowCount: 30
}]
});    
</script>

{% endhighlight %}

### sheets.showGridlines `Boolean`
{:#members:sheets-showgridlines}

Gets or sets a value that indicates whether to show or hide grid lines in the Spreadsheet.

#### Default Value
* true

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
	sheets:[{
		showGridlines: true
	}]
});   
</script>

{% endhighlight %}


### sheets.showHeader `Boolean`
{:#members:sheets-showheader}

Gets or sets a value that indicates whether to enable or disable the datasource header in Spreadsheet.

#### Default Value:

* false

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
sheets:[{
dataSource: window.defaultData, showHeader: true}]
});    
</script>

{% endhighlight %}

### sheets.showHeadings `Boolean`
{:#members:sheets-showheadings}

Gets or sets a value that indicates whether to show or hide headings in the Spreadsheet.

#### Default Value
* true

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
	sheets:[{
		showHeadings: true
	}]
});   
</script>

{% endhighlight %}

### sheets.startCell `String`
{:#members:sheets-startcell}

Specifies the start cell for the datasource range in Spreadsheet.

#### Default Value:

* "A1"

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({
sheets:[{
dataSource: window.defaultData, startCell: "A1"}]
});    
</script>

{% endhighlight %}

### showRibbon `Boolean`
{:#members:showribbon}

Gets or sets a value that indicates whether to show or hide ribbon in the Spreadsheet.

#### Default Value
* true

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
$('#Spreadsheet').ejSpreadsheet({ 
showRibbon: true
});         
</script>

{% endhighlight %}

### undoRedoStep `Number`
{:#members:undoredostep}

This is used to set the number of undo-redo steps in the Spreadsheet.

#### Default Value
* 20

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
$('#Spreadsheet').ejSpreadsheet({ 
undoRedoStep: 15
});         
</script>

{% endhighlight %}

### userName `String`
{:#members:username}

Define the username for the Spreadsheet which is displayed in comment.

#### Default Value
* User Name

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
$('#Spreadsheet').ejSpreadsheet({ 
userName: "User Name"
});         
</script>

{% endhighlight %}

## Methods

### addCustomFormula(formulaName, functionName)
{:#methods:addcustomformula}

This method is used to add custom formulas in Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">formulaName</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description">Pass the name of the formula.</td>
</tr>
<tr>
<td class="name">functionName</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description">Pass the name of the function.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.addCustomFormula("CUSTOMTOTAL","customTotal"); // Sends a add custom formula request to the Spreadsheet.
function customTotal(args){}//args-It uses the value given by the user while using custom formula in Spreadsheet.
</script>

{% endhighlight %}

{% highlight html %}
<script>
// Sends a add custom formula request to the Spreadsheet.
$("#Spreadsheet").ejSpreadsheet("addCustomFormula","CUSTOMTOTAL","customTotal" );     
function customTotal(args){}//args-It uses the value given by the user while using custom formula in Spreadsheet.  
</script>

{% endhighlight %}

### addNewSheet()
{:#methods:addnewsheet}

This method is used to add a new sheet in the last position of the sheet container.

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.addNewSheet(); // Sends a add new sheet request to the Spreadsheet.
</script>

{% endhighlight %}

{% highlight html %}
<script>
// Sends a add new sheet request to the Spreadsheet
$("#Spreadsheet").ejSpreadsheet("addNewSheet");        
</script>

{% endhighlight %}


### clearAll(\[range\])
{:#methods:clearall}

It is used to clear all the data and format in the specified range of cells in Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description"><span class="optional">Optional. </span> If range is specified, then it will clear all content in the specified range else it will use the current selected range. </td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.clearAll("A2:A6"); // Sends a clear all request to the Spreadsheet.
</script>
{% endhighlight %}

{% highlight html %}
<script>
// Sends a clear all request to the Spreadsheet.
$("#Spreadsheet").ejSpreadsheet("clearAll", "A2:A6");        
</script>

{% endhighlight %}


### clearAllFormat(\[range\])
{:#methods:clearallformat}

This property is used to clear all the formats applied in the specified range in Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description"><span class="optional">Optional. </span> If range is specified, then it will clear all format in the specified range else it will use the current selected range. </td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.clearAllFormat("A2:A6"); // Sends a clear all format request to the Spreadsheet.
</script>
{% endhighlight %}

{% highlight html %}
<script>
// Sends a clear all format request to the Spreadsheet
$("#Spreadsheet").ejSpreadsheet("clearAllFormat", "A2:A6");        
</script>

{% endhighlight %}

### clearBorder(\[range\])
{:#methods:clearborder}

Used to clear the applied border in the specified range in Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description"><span class="optional">Optional. </span> If range is specified, then it will clear border in the specified range else it will use the current selected range.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.clearBorder("A2:A6"); // Sends a clear border request to the Spreadsheet.
</script>
{% endhighlight %}

{% highlight html %}
<script>
// Sends a clear border request to the Spreadsheet.
$("#Spreadsheet").ejSpreadsheet("clearBorder", "A2:A6");        
</script>

{% endhighlight %}

### clearContents(\[range\])
{:#methods:clearcontents}

This property is used to clear the contents in the specified range in Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description"><span class="optional">Optional. </span> If the range is specified, then it will clear the content in the specified <br/>range else it will use the current selected range. </td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Create Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.clearContents("A2:A6"); // Sends a clear content request to the Spreadsheet.
</script>

{% endhighlight %}

{% highlight html %}
<script>
// Sends a clear content request to the Spreadsheet
$("#Spreadsheet").ejSpreadsheet("clearContents", "A2:A6");        
</script>

{% endhighlight %}

### clearRange(rangeName)
{:#methods:clearrange}

This method is used to remove only the data in the range denoted by the specified range name.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">rangeName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Pass the defined rangeSettings property name.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.clearRange("updateTable"); // Sends a clear range request to the Spreadsheet.
</script>

{% endhighlight %}

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// Sends a clear range request to the Spreadsheet.
$("#Spreadsheet").ejSpreadsheet("clearRange","updateTable");        
</script>

{% endhighlight %}

### clearRangeData(\[range\], \[property\],\[cells\],\[skipHiddenRow\],\[status\],\[skipCell\])
{:#methods:clearrangedata}

It is used to remove data in the specified range of cells based on the defined property.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">array|string</span></td>
<td class="description"><span class="optional">Optional. </span> If range is specified, it will clear data for the specified range else it will use the current selected range. </td>
</tr>
<tr>
<td class="name">property</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description"><span class="optional">Optional. </span> If property is specified, it will remove the specified property in the range else it will remove default properties </td>
</tr>
<tr>
<td class="name">cells</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description"><span class="optional">Optional. </span></td>
</tr>
<tr>
<td class="name">skipHiddenRow</td>
<td class="type"><span class="param-type">boolean</span> </td>
<td class="description"><span class="optional">Optional. </span> If pass true, if you want to skip the hidden rows </td>
</tr>
<tr>
<td class="name">status</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description"><span class="optional">Optional. </span>Pass the status to perform undo and redo operation.</td>
</tr>
<tr>
<td class="name">skipCell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description"><span class="optional">Optional. </span>It specifies whether to skip element processing or not.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.clearRangeData("A1:A5", ["value", "value2"], xlObj.getRange("A1:A5"), true);
</script>

{% endhighlight %}

{% highlight html %}
<script>
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Sends a clear range data request to the Spreadsheet.
$("#Spreadsheet").ejSpreadsheet("clearRangeData", "A1:A5", ["value", "value2"], xlObj.getRange("A1:A5"), false);        
</script>

{% endhighlight %}

### copySheet(fromIdx, toIdx, isCopySheet)
{:#methods:copysheet}

This method is used to copy or move the sheets in Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">fromIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the sheet index that you want to copy or move.</td>
</tr>
<tr>
<td class="name">toIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the position index where you want to copy or move.</td>
</tr>
<tr>
<td class="name">isCopySheet</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Pass true,If you want to copy sheet or else it will move sheet.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.copySheet(2, 1, true); // Sends a copy sheet request to the Spreadsheet.
//xlObj.copySheet(2, 1, false); // Sends a move sheet request to the Spreadsheet.
</script>

{% endhighlight %}

{% highlight html %}
<script>
// Sends a copy sheet request to the Spreadsheet.
$("#Spreadsheet").ejSpreadsheet("copySheet", 2, 1, true);        
</script>

{% endhighlight %}


### deleteEntireColumn(startCol, endCol)
{:#methods:deleteentirecolumn}

This method is used to delete the entire column which is selected.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">startCol</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the start column index.</td>
</tr>
<tr>
<td class="name">endCol</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the end column index.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Delete a column in the sheet.
xlObj.deleteEntireColumn(2, 3);
</script>

{% endhighlight %}

{% highlight html %}
<script>
// Delete a column in the sheet.
$("#Spreadsheet").ejSpreadsheet("deleteEntireColumn",2,3);
</script> 

{% endhighlight %}

### deleteEntireRow(startRow, endRow)
{:#methods:deleteentirerow}

This method is used to delete the entire row which is selected.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">startRow</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the start row index.</td>
</tr>
<tr>
<td class="name">endRow</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the end row index.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Delete a row in the sheet.
xlObj.deleteEntireRow(2,3);
</script>

{% endhighlight %}

{% highlight html %}
<script>
// Delete a row in the sheet.
$("#Spreadsheet").ejSpreadsheet("deleteEntireRow", 2, 3);
</script> 

{% endhighlight %}

### deleteSheet(idx)
{:#methods:deletesheet}

This method is used to delete a particular sheet in the Spreadsheet.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">idx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the sheet index to perform delete action.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.deleteSheet(3); // Sends a sheet delete request to the Spreadsheet
</script>

{% endhighlight %}

{% highlight html %}
<script>
// Sends a sheet delete request to the Spreadsheet
$("#Spreadsheet").ejSpreadsheet("deleteSheet", 3);        
</script>

{% endhighlight %}


### deleteShiftLeft(startCell, endCell)
{:#methods:deleteshiftleft}

This method is used to delete the selected cells and shift the remaining cells to left.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">startCell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Row index and column index of the starting cell.</td>
</tr>
<tr>
<td class="name">endCell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Row index and column index of the ending cell.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
var startCell= {rowIdx: 1, colIdx: 2}, endCell= {rowIdx: 1, colIdx: 2};
// Initialize the Spreadsheet object
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
//Delete a cell and shift cells left in the sheet.
xlObj.deleteShiftLeft(startCell, endCell);
</script>

{% endhighlight %}

{% highlight html %}
<script>
var startCell= {rowIdx: 1, colIdx: 2}, endCell= {rowIdx: 1, colIdx: 2};
// Delete a cell and shift cells left in the sheet.
$("#Spreadsheet").ejSpreadsheet("deleteShiftLeft", startCell, endCell);
</script> 

{% endhighlight %}

### deleteShiftUp(startCell, endCell)
{:#methods:deleteshiftup}

This method is used to delete the selected cells and shift the remaining cells up.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">startCell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Row index and column index of the start cell.</td>
</tr>
<tr>
<td class="name">endCell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Row index and column index of the end cell.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
var startCell= {rowIdx: 1, colIdx: 2}, endCell= {rowIdx: 1, colIdx: 2};
// Initialize the Spreadsheet object
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Delete a cell and shift cells up in the sheet.
xlObj.deleteShiftUp(startCell, endCell);
</script>

{% endhighlight %}

{% highlight html %}
<script>
var startCell= {rowIdx: 1, colIdx: 2}, endCell= {rowIdx: 1, colIdx: 2};
// Delete a cell and shift cells up in the sheet.
$("#Spreadsheet").ejSpreadsheet("deleteShiftUp", startCell, endCell);
</script> 

{% endhighlight %}

### editRange(rangeName, fn)
{:#methods:editrange}

This method is used to edit data in the specified range of cells based on its corresponding rangeSettings.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">rangeName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Pass the defined rangeSettings property name.</td>
</tr>
<tr>
<td class="name">fn</td>
<td class="type"><span class="param-type">function</span></td>
<td class="description">Pass the function that you want to perform range edit.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
var updateFn = function(cell, cellIdx) {
if (cellIdx % 2 == 0)
return "SpreadSheet";
else
return "Grid";
};
var rangeSettings = {
range: "B1:C2",
name: "updateTable",
cssClass: "readOnly1",
readOnly: true,
contextTab: {},
contextMenuSettings: {
dataSource: [{
id: 1,
text: "Copy",
parentId: null,
sprite: "e-icon e-copy"
}, {
id: 2,
text: "Refresh",
parentId: null,
}]
},
showPanel: true
};
//Update new rangeSettings property before invoking edit range
xlObj.model.sheets[1].rangeSettings["updateTable"] = rangeSettings;
//Sends a edit range request to the Spreadsheet
xlObj.editRange("updateTable", updateFn); 
</script>

{% endhighlight %}

{% highlight html %}
<script>
//Sends a edit range request to the Spreadsheet after updating new rangeSettings.
$("#Spreadsheet").ejSpreadsheet("editRange", "updateTable", updateFn);        
</script>

{% endhighlight %}

### getActivationPanel()
{:#methods:getactivationpanel}

This method is used to get the activation panel in the Spreadsheet.

####Returns:
Element

#### Example
{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.getActivationPanel(); // Gets sheet  ActivationPanel element in Spreadsheet.
</script>
{% endhighlight %}

{% highlight html %}
<script>
// Gets sheet ActivationPanel element in Spreadsheet.
$("#Spreadsheet").ejSpreadsheet("getActivationPanel");        
</script>

{% endhighlight %}


### getActiveCell(\[sheetIdx\])
{:#methods:getactivecell}

This method is used to get the active cell object in Spreadsheet. It will returns object which contains rowIndex and colIndex of the active cell.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description"><span class="optional">Optional. </span> If sheetIdx is specified, it will return the active cell object in specified sheet index else it will use the current sheet index</td>
</tr>
</tbody>
</table>

####Returns:
Object

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.getActiveCell(1); // Gets the activecell  object in specified sheet index.
</script>

{% endhighlight %}

{% highlight html %}
<script>
// Gets the activecell element in specified sheetindex
$("#Spreadsheet").ejSpreadsheet("getActiveCell", 1);        
</script>

{% endhighlight %}

### getActiveCellElem(\[sheetIdx\])
{:#methods:getactivecellelem}

This method is used to get the active cell element based on the given sheet index in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description"><span class="optional">Optional. </span> If sheetIndex is specified, it will return the active cell element in specified <br/>sheet index else it will use the current active sheet index.</td>
</tr>
</tbody>
</table>

####Returns:
Element

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.getActiveCellElem(1); // Gets activecell element in Spreadsheet.
</script>

{% endhighlight %}

{% highlight html %}
<script>
// Gets activecell element in Spreadsheet.
$("#Spreadsheet").ejSpreadsheet("getActiveCellElem", 1);        
</script>

{% endhighlight %}

### getActiveSheetIndex()
{:#methods:getactivesheetindex}

This method is used to get the current active sheet index in Spreadsheet.

####Returns:
Number
 
#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.getActiveSheetIndex(); // Gets activesheet index in Spreadsheet.
</script>

{% endhighlight %}

{% highlight html %}
<script>
// Gets activesheet index in Spreadsheet
$("#Spreadsheet").ejSpreadsheet("getActiveSheetIndex");        
</script>

{% endhighlight %}

### getAutoFillElem()
{:#methods:getautofillelem}

This method is used to get the auto fill element in Spreadsheet.

####Returns:
Element

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.getAutoFillElem(); // Gets autofill element in Spreadsheet.
</script>

{% endhighlight %}

{% highlight html %}
<script>
// Gets autofill element in Spreadsheet.
$("#Spreadsheet").ejSpreadsheet("getAutoFillElem");        
</script>

{% endhighlight %}

### getCell(rowIdx, colIdx, \[sheetIdx\])
{:#methods:getcell}

This method is used to get the cell element based on specified row and column index in the Spreadsheet.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">rowIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the row index.</td>
</tr>
<tr>
<td class="name">colIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the column index.</td>
</tr>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description"><span class="optional">Optional. </span> Pass the sheet index that you want to get cell.</td>
</tr>
</tbody>
</table>

####Returns:
Element

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.getCell(2, 3, 1); // Get the cell based on rowIndex and colIndex.
</script>

{% endhighlight %}

{% highlight html %}
<script>
// Get the cell based on row and column index
$("#Spreadsheet").ejSpreadsheet("getCell", 2, 3, 1);        
</script>

{% endhighlight %}

### getDataSettings(sheetIdx)
{:#methods:getdatasettings}

This method is used to get the data settings in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the sheet index.</td>
</tr>
</tbody>
</table>

####Returns:
Number

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
// Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.getDataSettings(1); // Gets the data settings in Spreadsheet
</script>

{% endhighlight %}

{% highlight html %}
<script>
// Gets the data settings in Spreadsheet
$("#Spreadsheet").ejSpreadsheet("getDataSettings", 1);        
</script>

{% endhighlight %}

### getFrozenColumns(sheetIdx)
{:#methods:getfrozencolumns}

This method is used to get the frozen columns index in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the sheet index.</td>
</tr>
</tbody>
</table>

####Returns:
Number

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
// Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.getFrozenColumns(1); // Gets the freezed column index in Spreadsheet
</script>

{% endhighlight %}

{% highlight html %}
<script>
// Gets the freezed column index in Spreadsheet
$("#Spreadsheet").ejSpreadsheet("getFrozenColumns", 1);        
</script>

{% endhighlight %}

### getFrozenRows(sheetIdx)
{:#methods:getfrozenrows}

This method is used to get the frozen row’s index in Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the sheet index.</td>
</tr>
</tbody>
</table>

####Returns:
Number

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
// Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.getFrozenRows(1); // Gets the freezed row index in Spreadsheet.
</script>

{% endhighlight %}

{% highlight html %}
<script>
// Gets the freezed row index in Spreadsheet
$("#Spreadsheet").ejSpreadsheet("getFrozenRows", 1);        
</script>

{% endhighlight %}

### getHyperlink(cell)
{:#methods:gethyperlink}

This method is used to get the hyperlink data as object from the specified cell in Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cell</td>
<td class="type"><span class="param-type">Element</span></td>
<td class="description">Pass the DOM element to get hyperlink</td>
</tr>
</tbody>
</table>

####Returns:
Object

#### Example

{% highlight html %}
<script>
// Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.getHyperlink(xlObj.getCell(1, 1)); // To get the hyperlink data of specified cell.
</script>

{% endhighlight %}

{% highlight html %}
<script>
// To get the hyperlink data of specified cell.
$("#Spreadsheet").ejSpreadsheet("getHyperlink", xlObj.getCell(1, 1, 1));        
</script>

{% endhighlight %}

### getRange(startRIndex, startCIndex, endRIndex, endCIndex, sheetIdx)
{:#methods:getrange}

This method is used to get all cell elements in the specified range.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">startRIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the row index of the start cell.</td>
</tr>
<tr>
<td class="name">startCIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the column index of the start cell.</td>
</tr>
<tr>
<td class="name">endRIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the row index of the end cell.</td>
</tr>
<tr>
<td class="name">endCIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the column index of the end cell.</td>
</tr>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the index of the sheet.</td>
</tr>
</tbody>
</table>

####Returns:
Element

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.getRange(1, 2, 4, 5, 1); // Get the range cells based on startcell and endcell index
</script>

{% endhighlight %}

{% highlight html %}
<script>
// Get the range cells based on startcell and endcell index
$("#Spreadsheet").ejSpreadsheet("getRange", 1, 2, 4, 5, 1);        
</script>

{% endhighlight %}

### getRangeData(\[options\])
{:#methods:getrangedata}

This method is used to get the data in specified range in Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">options</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description"><span class="optional">Optional. </span> Pass the range, property, sheetIdx, valueOnly in options. </td>
</tr>
</tbody>
</table>

####Returns:
Array

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.getRangeData({range: [2, 6, 2, 6], property: ["value", "value2", "format"], sheetIdx: 1}); // To get the cells data of specified range
</script>

{% endhighlight %}

{% highlight html %}
<script>
// To get the cells data of specified range
$("#Spreadsheet").ejSpreadsheet("getRangeData", {range: [2, 6, 2, 6], property: ["value", "value2", "format"], sheetIdx: 1});        
</script>

{% endhighlight %}

### getRangeIndices(range)
{:#methods:getrangeindices}

This method is used to get the range indices array based on the specified alpha range in Spreadsheet.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Pass the alpha range that you want to get range indices.</td>
</tr>
</tbody>
</table>

####Returns:
Array
 
#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.getRangeIndices("A1:A9"); // Get range indicesbased on specified alpha range.
</script>

{% endhighlight %}

{% highlight html %}
<script>
// Get cells based on specified range indices
$("#Spreadsheet").ejSpreadsheet("getRangeIndices", "A1:A9");        
</script>
{% endhighlight %}

### getSheet(sheetIdx)
{:#methods:getsheet}

This method is used to get the sheet details based on the given sheet index in Spreadsheet.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the sheet index to get the sheet object.</td>
</tr>
</tbody>
</table>

####Returns:
Object

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.getSheet(1); // Gets sheet details of Spreadsheet.
</script>

{% endhighlight %}

{% highlight html %}
<script>
// Gets sheet details of Spreadsheet
$("#Spreadsheet").ejSpreadsheet("getSheet", 1);        
</script>

{% endhighlight %}

### getSheetElement(sheetIdx)
{:#methods:getsheetelement}

This method is used to get the sheet content div element of Spreadsheet.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the sheet index to get the sheet content.</td>
</tr>
</tbody>
</table>

####Returns:
Element

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.getSheetElement(1); // Gets sheet content of Spreadsheet.
</script>

{% endhighlight %}

{% highlight html %}
<script>
// Gets sheet content of Spreadsheet.
$("#Spreadsheet").ejSpreadsheet("getSheetElement", 1);        
</script>

{% endhighlight %}

### gotoPage(sheetIdx, newSheet)
{:#methods:gotopage}

This method is used to send a paging request to the specified sheet Index in the Spreadsheet.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the sheet index to perform paging at specified sheet index</td>
</tr>
<tr>
<td class="name">newSheet</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Pass 'true' to create a new sheet. If the specified sheet index is already exist,<br/> it navigate to that sheet else it create a new sheet.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.gotoPage(1, false); // Sends a paging request to the Spreadsheet with specified sheet index
</script>

{% endhighlight %}

{% highlight html %}
<script>
// Sends a paging request to the Spreadsheet with specified sheet index.
$("#Spreadsheet").ejSpreadsheet("gotoPage", 3, true);        
</script>

{% endhighlight %}

### hideColumn(startCol, endCol)
{:#methods:hidecolumn}

This method is used to hide the entire columns from the specified range (startCol, endCol) in Spreadsheet.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">startCol</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Index of the start column.</td>
</tr>
<tr>
<td class="name">endCol</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Optional. Index of the end column.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
// Initialize the Spreadsheet object
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Hide the column by passing column index in the active sheet.
xlObj.hideColumn(1);
// Hide the columns from startCol to endCol in the active sheet.
xlObj.hideColumn(1, 4);
</script>

{% endhighlight %}

{% highlight html %}
<script>
// Hide the column by passing column index in the active sheet.
$("#Spreadsheet").ejSpreadsheet("hideColumn", 1);
// Hide the columns from startCol to endCol in the active sheet.
$("#Spreadsheet").ejSpreadsheet("hideColumn", 1, 4);
</script>

{% endhighlight %}

### hideFormulaBar()
{:#methods:hideformulabar}

This method is used to hide the formula bar in Spreadsheet.

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
//To hide formula bar in Spreadsheet.
xlObj.hideFormulaBar();
</script>

{% endhighlight %}

### hideRow(startRow, endRow)
{:#methods:hiderow}

This method is used to hide the rows, based on the specified row index in Spreadsheet.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">startRow</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Index of the start row.</td>
</tr>
<tr>
<td class="name">endRow</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description"> Optional. Index of the end row.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
// Initialize the Spreadsheet object
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Hide the row by passing row index in the active sheet.
xlObj.hideRow(1);
// Hide a rows from startRow to endRow in the active sheet.
xlObj.hideRow(1, 4);
</script>


{% endhighlight %}

{% highlight html %}
<script>
// Hide the row by passing row index in the active sheet.
$("#Spreadsheet").ejSpreadsheet("hideRow", 1);
// Hide a rows from startRow to endRow in the active sheet.
$("#Spreadsheet").ejSpreadsheet("hideRow", 1, 4);
</script>

{% endhighlight %}

### hideSheet(sheetIdx)
{:#methods:hidesheet}

This method is used to hide the sheet based on the specified sheetIndex or sheet name in the Spreadsheet.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">string|number</span></td>
<td class="description">Pass the sheet name or index that you want to hide.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
//Sends a hide sheet request to the Spreadsheet.
xlObj.hideSheet("Sheet2");
</script>

{% endhighlight %}

{% highlight html %}
<script>
//Sends a hide sheet request to the Spreadsheet.
$("#Spreadsheet").ejSpreadsheet("hideSheet", 2);
</script>

{% endhighlight %}

### hideWaitingPopUp()
{:#methods:hidewaitingpopup}

This method is used to hide the displayed waiting pop-up in Spreadsheet.

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// hide waiting popup in the Spreadsheet.
xlObj.hideWaitingPopUp();
</script>

{% endhighlight %}

{% highlight html %}
<script>
// hide waiting popup in the Spreadsheet.
$("#Spreadsheet").ejSpreadsheet("hideWaitingPopUp");
</script>

{% endhighlight %}

### insertEntireColumn(startCol, endCol)
{:#methods:insertentirecolumn}

This method is used to insert a column before the active cell's column in the Spreadsheet.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">startCol</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass start column.</td>
</tr>
<tr>
<td class="name">endCol</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass end column.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
//initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Insert a column in the sheet.
xlObj.insertEntireColumn(1, 2);
</script>

{% endhighlight %}

{% highlight html %}
<script>
// Insert a column in the sheet.
$("#Spreadsheet").ejSpreadsheet("insertEntireColumn", 1, 2);
</script>

{% endhighlight %}

### insertEntireRow(startRow, endRow)
{:#methods:insertentirerow}

This method is used to insert a row before the active cell's row in the Spreadsheet.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">startRow</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass start row.</td>
</tr>
<tr>
<td class="name">endRow</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass end row.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
//initialize the Spreadsheet object
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Insert a row in the sheet.
xlObj.insertEntireRow(1, 2);
</script>

{% endhighlight %}

{% highlight html %}
<script>
// Insert a row in the sheet.
$("#Spreadsheet").ejSpreadsheet("insertEntireRow", 1, 2);
</script>

{% endhighlight %}

### insertSheet()
{:#methods:insertsheet}

This method is used to insert a new sheet to the left of the current active sheet.

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.insertSheet(); // Sends a insert new sheet request to the Spreadsheet.
</script>

{% endhighlight %}

{% highlight html %}
<script>
// Sends an insert new sheet request to the Spreadsheet.
$("#Spreadsheet").ejSpreadsheet("insertSheet");        
</script>

{% endhighlight %}

### insertShiftBottom(startCell, endCell)
{:#methods:insertshiftbottom}

This method is used to insert cells in the selected or specified range and shift remaining cells to bottom.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">startCell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Row index and column index of the start cell.</td>
</tr>
<tr>
<td class="name">endCell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Row index and column index of the end cell.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
var startCell= {rowIndex: 1, colIndex: 2}, endCell= {rowIndex: 1, colIndex: 2};
//initialize the Spreadsheet object
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Insert a cells and shift cells bottom in the sheet.
xlObj.insertShiftBottom(startCell, endCell);
</script>

{% endhighlight %}

{% highlight html %}
<script>
var startCell= {rowIndex: 1, colIndex: 2}, endCell= {rowIndex: 1, colIndex: 2};
// Insert a cell and shift cells bottom in the sheet.
$("#Spreadsheet").ejSpreadsheet("insertShiftBottom", startCell, endCell);
</script>

{% endhighlight %}

### insertShiftRight(startCell, endCell)
{:#methods:insertshiftright}

This method is used to insert cells in the selected or specified range and shift remaining cells to right.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">startCell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Row index and column index of the start cell.</td>
</tr>
<tr>
<td class="name">endCell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Row index and column index of the end cell.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
var startCell= {rowIndex: 1, colIndex: 2}, endCell= {rowIndex: 1, colIndex: 2};
//initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Insert a cells and shift cells right in the sheet.
xlObj.insertShiftRight(startCell, endCell);
</script>

{% endhighlight %}

{% highlight html %}
<script>
var startCell= {rowIndex: 1, colIndex: 2}, endCell= {rowIndex: 1, colIndex: 2};
// Insert a cell and shift cells right in the sheet.
$("#Spreadsheet").ejSpreadsheet("insertShiftRight", startCell, endCell);
</script> 

{% endhighlight %}

### import(importRequest)
{:#methods:import}

This method is used to import excel file manually by using form data.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">importRequest</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Pass the form data object to import files manually.</td>
</tr>
</tbody>
</table>

The Objects are File, Password, URL, FileStream, FileType. 

#### Example

{% highlight html %}

<div id="Spreadsheet"></div> 
<script>
var xlObj = $("#Spreadsheet").data("ejSpreadsheet"); // Initialize the Spreadsheet object.
var importRequest = {Url:"http://staging.syncfusion.com:7777/ejSpreadsheet/Spreadsheet.xlsx";
xlObj.import(importRequest); 
</script>

{% endhighlight %}

### lockCells(range, \[isLocked\])
{:#methods:lockcells}

This method is used to lock/unlock the range of cells in active sheet. Lock cells are activated only after the sheet is protected. Once the sheet is protected it is unable to lock/unlock cells.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">string|array</span></td>
<td class="description">Pass the alpha range cells or array range of cells.</td>
</tr>
<tr>
<td class="name">isLocked</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description"><span class="optional">Optional. </span> By default is true. If it is false locked cells are unlocked.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.lockCells("A3:B5", true); // To lock cells in the Spreadsheet.
</script>

{% endhighlight %}

{% highlight html %}
<script>
// To lock cells in the Spreadsheet.
$("#Spreadsheet").ejSpreadsheet("lockCells","A3:B5", true);        
</script>

{% endhighlight %}

### mergeAcrossCells(\[range\], \[alertStatus\])
{:#methods:mergeacrosscells}

This method is used to merge cells by across in the Spreadsheet.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description"><span class="optional">Optional. </span> To pass the cell range or selected cells are process.</td>
</tr>
<tr>
<td class="name">alertStatus</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description"><span class="optional">Optional. </span> If pass true it does not show alert.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Create Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.mergeAcrossCells("A3:B5", true); // To merge cells across in the Spreadsheet.
</script>

{% endhighlight %}

{% highlight html %}
<script>
// To merge cells across in the Spreadsheet.
$("#Spreadsheet").ejSpreadsheet("mergeAcrossCells","A3:B5");        
</script>

{% endhighlight %}

### mergeCells(\[range\], \[alertStatus\])
{:#methods:mergecells}

This method is used to merge the selected cells in the Spreadsheet.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description"><span class="optional">Optional. </span> To pass the cell range or selected cells are process.</td>
</tr>
<tr>
<td class="name">alertStatus</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description"><span class="optional">Optional. </span> If pass true it does not show alert.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.mergeCells("A3:B5", true); // To merge the selecetd cell in Spreadsheet.
</script>

{% endhighlight %}

{% highlight html %}
<script>
// To merge the selecetd cell in Spreadsheet
$("#Spreadsheet").ejSpreadsheet("mergeCells","A3:B5");        
</script>

{% endhighlight %}

### protectSheet(\[isProtected\])
{:#methods:protectsheet}

This method is used to protect or unprotect active sheet.

<table class="params">
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
<tr>
<td class="name">isProtected</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description"><span class="optional">Optional. </span>  By default is true. If it is false active sheet is unprotected.</td>
</tr>
</table>

#### Example

{% highlight html %}
<script>
//initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// To protect sheet in Spreadsheet.
xlObj.protectSheet(false);
</script>
{% endhighlight %}

{% highlight html %}
<script>
// To defined refresh selection in Spreadsheet.
$("#Spreadsheet").ejSpreadsheet("protectSheet", false);
</script>

{% endhighlight %}

### refreshContent(sheetIdx)
{:#methods:refreshcontent}
This method is used to refresh the content in Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the index of the sheet.</td>
</tr>
</tbody>
</table>

#### Example
{% highlight html %}
<script>
//initialize the Spreadsheet object
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.refreshContent(1);
</script>
{% endhighlight %}

{% highlight html %}
<script>
$("#Spreadsheet").ejSpreadsheet("refreshContent",1);
</script>
{% endhighlight %}


### refreshSpreadsheet()
{:#methods:refreshspreadsheet}
This method is used to refresh the Spreadsheet.

#### Example
{% highlight html %}
<script>
//initialize the Spreadsheet object
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.refreshSpreadsheet();
</script>
{% endhighlight %}

{% highlight html %}
<script>
$("#Spreadsheet").ejSpreadsheet("refreshSpreadsheet");
</script>
{% endhighlight %}

### removeCustomFormula(formulaName, functionName)
{:#methods:removecustomformula}

This method is used to remove custom formulae in Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">formulaName</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description">Pass the name of the formula.</td>
</tr>
<tr>
<td class="name">functionName</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description">Pass the name of the function.</td>
</tr>
</tbody>
</table>

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.removeCustomFormula("CUSTOMTOTAL","customTotal"); // Sends a remove custom formula request to the Spreadsheet.
function customTotal(args){}//args-It uses the value given by the user while using custom formula in Spreadsheet.
</script>
{% endhighlight %}

{% highlight html %}
<script>
// Sends a remove custom formula request to the Spreadsheet.
$("#Spreadsheet").ejSpreadsheet("removeCustomFormula","CUSTOMTOTAL","customTotal" ); 
function customTotal(args){}//args-It uses the value given by the user while using custom formula in Spreadsheet .      
</script>
{% endhighlight %}

### removeHyperlink(range, \[isClearHLink\], \[status\], \[cells\], \[skipHiddenRow\])
{:#methods:removehyperlink}

This method is used to remove the hyperlink from selected cells of current sheet.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Hyperlink remove from the specified range.</td>
</tr>
<tr>
<td class="name">isClearHLink</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description"><span class="optional">Optional. </span> If it is true, It will clear link only not format.</td>
</tr>
<tr>
<td class="name">status</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description"><span class="optional">Optional. </span> Pass the status to perform undo and redo operations.</td>
</tr>
<tr>
<td class="name">cells</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description"><span class="optional">Optional. </span> Pass the cells that you want to remove hyperlink.</td>
</tr>
<tr>
<td class="name">skipHiddenRow</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description"><span class="optional">Optional. </span> Pass true, if you want to skip the hidden rows.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.removeHyperlink("A2:A3", false); // To remove the hyperlink  of specified range
</script>
{% endhighlight %}

{% highlight html %}
<script>
// To remove the hyperlink  of specified range
$("#Spreadsheet").ejSpreadsheet("removeHyperlink", "A2:A3", false);        
</script>

{% endhighlight %}

### removeRange(rangeName)
{:#methods:removerange}

This method is used to remove the range data and its defined rangeSettings property based on the specified range name.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">rangeName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Pass the defined rangeSetting property name.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Sends a remove range request to the Spreadsheet.
xlObj.removeRange("updateTable"); 
</script>

{% endhighlight %}

{% highlight html %}
<script>
// Sends a remove range request to the Spreadsheet.
$("#Spreadsheet").ejSpreadsheet("removeRange", "updateTable");
</script>

{% endhighlight %}

### saveAsJSON()
{:#methods:saveasjson}

This method is used to save JSON data in Spreadsheet.

#### Example

{% highlight html %}
<script>
//initialize the Spreadsheet object
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.saveAsJSON();
</script>
{% endhighlight %}

{% highlight html %}
<script>
$("#Spreadsheet").ejSpreadsheet("saveAsJSON");
</script>

{% endhighlight %}

### saveBatchChanges(sheetIdx)
{:#methods:savebatchchanges}

This method is used to save batch changes in Spreadsheet.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the sheet index for Spreadsheet.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
//initialize the Spreadsheet object
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
//Set sheet index for Spreadsheet. 
xlObj.saveBatchChanges(1);
</script>

{% endhighlight %}

{% highlight html %}
<script>
//Set sheet index for Spreadsheet.
$("#Spreadsheet").ejSpreadsheet("saveBatchChanges", 1);
</script>

{% endhighlight %}

### setActiveCell(rowIdx, colIdx, sheetIdx)
{:#methods:setactivecell}

This method is used to set the active cell in the Spreadsheet.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">rowIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the row index.</td>
</tr>
<tr>
<td class="name">colIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the column index.</td>
</tr>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the index of the sheet.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.setActiveCell(1, 0, 1); // Sets activecell in Spreadsheet.
</script>

{% endhighlight %}

{% highlight html %}
<script>
// Sets activecell in Spreadsheet.
$("#Spreadsheet").ejSpreadsheet("setActiveCell", 1, 0, 1);
</script>

{% endhighlight %}

### setActiveSheetIndex(sheetIdx)
{:#methods:setactivesheetindex}

This method is used to set active sheet index for the Spreadsheet.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the active sheet index for Spreadsheet.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
var sheetIndex= 1;
//initialize the Spreadsheet object
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
//Set active sheet index for Spreadsheet. 
xlObj.setActiveSheetIndex(sheetIndex);
</script>

{% endhighlight %}

{% highlight html %}
<script>
//Set active sheet index for Spreadsheet.
$("#Spreadsheet").ejSpreadsheet("setActiveSheetIndex", sheetIndex);
</script>

{% endhighlight %}

### setBorder(property, \[range\])
{:#methods:setborder}

This method is used to set border for the specified range of cells in the Spreadsheet.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">property</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Pass the border properties that you want to set.</td>
</tr>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description"><span class="optional">Optional. </span> If range is specified, it will set border for the specified range else it will use the selected range.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.setBorder({ borderStyle: "solid", ID: "outside", hexaCode: "#000000"}, "B2:B6"); // To set borders in Spreadsheet
</script>

{% endhighlight %}

{% highlight html %}
<script>
// To set borders in Spreadsheet.
$("#Spreadsheet").ejSpreadsheet("setBorder", { borderStyle: "solid", ID: "outside", hexaCode: "#000000"}, "B2:B6");        
</script>

{% endhighlight %}

### setHyperlink(range, link, sheetIdx)
{:#methods:sethyperlink}

This method is used to set the hyperlink in selected cells of the current sheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">If range is specified, it will set the hyperlink in range of the cells.</td>
</tr>
<tr>
<td class="name">link</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Pass cellAddress or webAddress</td>
</tr>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">If we pass cellAddress then which sheet to be navigate in the applied link.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}

<script>
// Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.setHyperlink("A2:A3",{"cellAddr":"A2:A8"}, 3); // To set the hyperlink  of specified range.
</script>

{% endhighlight %}

{% highlight html %}
<script>
// To set the hyperlink  of specified range
$("#Spreadsheet").ejSpreadsheet("setHyperlink", "A2:A3",{"cellAddr":"A2:A8"},3);        
</script>

{% endhighlight %}

### setSheetFocus()
{:#methods:setsheetfocus}

This method is used to set the focus to the Spreadsheet.

#### Example

{% highlight html %}
<script>
//initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Set focus on Spreadsheet.
xlObj.setSheetFocus();
</script>

{% endhighlight %}

{% highlight html %}
<script>
// Set focus on Spreadsheet.
$("#Spreadsheet").ejSpreadsheet("setSheetFocus");
</script>

{% endhighlight %}

### setWidthToColumns(widthColl)
{:#methods:setwidthtocolumns}

This method is used to set the width for the columns in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">widthColl</td>
<td class="type"><span class="param-type">array|object</span></td>
<td class="description">Pass the column index and width of the columns.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
var widthCollObj= [{colIndex: 2, width: 40}, {colIndex: 3, width: 50}], widthCollArr = [80, 90];
//initialize the Spreadsheet object
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Set width for specified columns in active sheet
xlObj.setWidthToColumns(widthCollObj);
// Set width for columns starting from the '0'th index in active sheet.
xlObj.setWidthToColumns(widthCollArr);
</script>

{% endhighlight %}

{% highlight html %}
<script>
// Set width for specified columns in active sheet.
$("#Spreadsheet").ejSpreadsheet("setWidthToColumns", widthCollObj);
// Set width for columns starting from the '0'th index in active sheet.
$("#Spreadsheet").ejSpreadsheet("setWidthToColumns", widthCollArr);

</script>

{% endhighlight %}

### sheetRename(sheetName)
{:#methods:sheetrename}

This method is used to rename the active sheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">sheetName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Pass the sheet name that you want to change the current active sheet name.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.sheetRename("Sep-Billing"); // Sends a sheet rename request to the Spreadsheet
</script>

{% endhighlight %}

{% highlight html %}
<script>
// To rename a sheet in Spreadsheet
$("#Spreadsheet").ejSpreadsheet("sheetRename", "Sep-Billing");        
</script>

{% endhighlight %}

### showActivationPanel(rangeName)
{:#methods:showactivationpanel}

This method is used to display the activationPanel for the specified range name.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">rangeName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Pass the range name that you want to display the activation panel.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.showActivationPanel("upTable"); // To display the activationPanel in Spreadsheet
</script>

{% endhighlight %}

{% highlight html %}
<script>
// To display the activationPanel in Spreadsheet
$("#Spreadsheet").ejSpreadsheet("showActivationPanel", "upTable");        
</script>

{% endhighlight %}

### showColumn(startCol, endCol)
{:#methods:showcolumn}

This method is used to show the hidden columns within the specified range in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">startColIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Index of the start column.</td>
</tr>
<tr>
<td class="name">endColIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Optional. Index of the end column.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
//initialize the Spreadsheet object
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// show the hidden column by passing column index in the active sheet.
xlObj.showColumn(1);
// show the hidden columns from startColIdx to startColIdx in the active sheet.
xlObj.showColumn(3, 6);

</script>

{% endhighlight %}

{% highlight html %}
<script>
// show the hidden column by passing column index in the active sheet.
$("#Spreadsheet").ejSpreadsheet("showColumn", 1);
// show the hidden columns from startColIdx to startColIdx in the active sheet.
$("#Spreadsheet").ejSpreadsheet("showColumn", 3, 6);
</script>

{% endhighlight %}

### showFormulaBar()
{:#methods:showformulabar}

This method is used to show the formula bar in Spreadsheet.

#### Example

{% highlight html %}
<script>
//initialize the Spreadsheet object
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
//To show the formula bar in Spreadsheet
xlObj.showFormulaBar();
</script>

{% endhighlight %}

{% highlight html %}
<script>
// To show the formula bar in Spreadsheet.
$("#Spreadsheet").ejSpreadsheet("showFormulaBar ");
</script>

{% endhighlight %}

### showGridlines(status)
{:#methods:showgridlines}

This method is used to show/hide gridlines in active sheet in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">status</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Pass true to show the gridlines</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// To hide the gridlines in the sheet.
xlObj.showGridlines(false);
</script>

{% endhighlight %}

{% highlight html %}
<script>
// hide the gridlines in the sheet.
$("#Spreadsheet").ejSpreadsheet("showGridlines", false);
</script>

{% endhighlight %}

### showHeadings(status)
{:#methods:showheadings}

This method is used to show/hide the headers in active sheet in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">startRow</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Pass true to show the sheet headers.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// To hide the headers in the sheet.
xlObj.showHeadings(false);
</script>
{% endhighlight %}

{% highlight html %}
<script>
// To hide the headers in the sheet.
$("#Spreadsheet").ejSpreadsheet("showHeadings", false);
</script>

{% endhighlight %}

### showRow(startRow, endRow)
{:#methods:showrow}

This method is used to show the hidden rows in the specified range in the Spreadsheet. 
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">startRow</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Index of the start row.</td>
</tr>
<tr>
<td class="name">endRow</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Optional. Index of the end row.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// show the hidden row by passing row index in the active sheet.
xlObj.showRow(1);
// To show the hidden rows for startRow to endRow in the active sheet.
xlObj.showRow(3, 6);
</script>

{% endhighlight %}

{% highlight html %}
<script>
// show the hidden row by passing row index in the active sheet.
$("#Spreadsheet").ejSpreadsheet("showRow", 1);
// To show the hidden rows for startRow to endRow in the active sheet.
$("#Spreadsheet").ejSpreadsheet("showRow", 3, 6);
</script>

{% endhighlight %}

### showWaitingPopUp()
{:#methods:showwaitingpopup}

This method is used to show waiting pop-up in Spreadsheet.

#### Example

{% highlight html %}
<script>
//initialize the Spreadsheet object
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// To show waiting popup in Spreadsheet
xlObj.showWaitingPopUp();
</script>

{% endhighlight %}

{% highlight html %}
<script>
// show waiting popup in the Spreadsheet
$("#Spreadsheet").ejSpreadsheet("showWaitingPopUp");
</script>

{% endhighlight %}

### unfreezePanes()
{:#methods:unfreezepanes}

This method is used to unfreeze the frozen rows and columns in the Spreadsheet.

#### Example

{% highlight html %}
<script>
//Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// To unfreeze the freezed rows and columns in the sheet.
xlObj.XLFreeze.unfreezePanes();
</script>

{% endhighlight %}

### unhideSheet(sheetInfo)
{:#methods:unhidesheet}

This method is used to unhide the sheet based on specified sheet name or sheet index.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">sheetInfo</td>
<td class="type"><span class="param-type">string|number</span></td>
<td class="description">Pass the sheet name or index that you want to unhide.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
//Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
//To unhide a sheet in Spreadsheet.
xlObj.unhideSheet("Sheet2");
</script>

{% endhighlight %}

{% highlight html %}
<script>
//To unhide a sheet in Spreadsheet.
$("#Spreadsheet").ejSpreadsheet("unhideSheet", "Sheet2");
</script>

{% endhighlight %}

### unmergeCells(\[range\])
{:#methods:unmergecells}

This method is used to unmerge the selected range of cells in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description"><span class="optional">Optional. </span> If the range is specified, then it will un merge the specified range else it will use the current selected range.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// To unmerge the selected cells in Spreadsheet.
xlObj.unmergeCells("A3:B5"); 
</script>

{% endhighlight %}

{% highlight html %}
<script>
// To unmerge the selected cells in Spreadsheet.
$("#Spreadsheet").ejSpreadsheet("unmergeCells","A3:B5");        
</script>

{% endhighlight %}

### unWrapText(\[range\])
{:#methods:unwraptext}

This method is used to unwrap the selected range of cells in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">array|string</span></td>
<td class="description"><span class="optional">Optional. </span> If the range is specified, then it will update unwrap in the specified <br/>range else it will use the current selected range.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
//Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// To unwrap the cell text.
xlObj.unWrapText("A1:B3");
</script>

{% endhighlight %}

{% highlight html %}
<script>
// To unwrap the cell text.
$("#Spreadsheet").ejSpreadsheet("unWrapText","A1:B3")
</script>

{% endhighlight %}

### updateData(data, \[range\])
{:#methods:updatedata}

This method is used to update the data for the specified range of cells in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Pass the cells data that you want to update.</td>
</tr>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description"><span class="optional">Optional. </span> If range is specified, it will update data for the specified range <br/> else it will use the current selected range. </td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// To update data in the specified range of the cells in Spreadsheet.
xlObj.updateData([{ value: 10, value2: 10, type: "general"}, { value: 25000, value2: 25000, type: "general"}], [1, 0, 3, 0]); 
</script>

{% endhighlight %}

{% highlight html %}
<script>
// To update a data in the specified range of cells in Spreadsheet.
$("#Spreadsheet").ejSpreadsheet("updateData", [{ value: 10, value2: 10, type: "general"}, { value: 25000, value2: 25000, type: "general"}], [1, 0, 2, 0]);        
</script>

{% endhighlight %}

### updateFormulaBar()
{:#methods:updateformulabar}

This method is used to update the formula bar in the Spreadsheet.

#### Example

{% highlight html %}
<script>
//initialize the Spreadsheet object
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
//To update the formula bar in Spreadsheet
xlObj.updateFormulaBar();
</script>

{% endhighlight %}

### updateRange(sheetIdx, settings)
{:#methods:updaterange}

This method is used to update the range of cells based on the specified settings which we want to update in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the sheet index that you want to update.</td>
</tr>
<tr>
<td class="name">settings</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Pass the dataSource, startCell and showHeader values as settings.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
var settings = { dataSource: [{ Product: "XYZ", Price: "2000" }], showHeader: "true", startCell: "F1" };
// To update range of cells with the specified settings
xlObj.updateRange(1, settings); 
</script>

{% endhighlight %}

{% highlight html %}
<script>
var settings = { dataSource: [{ Product: "XYZ", Price: "2000" }], showHeader: "true", startCell: "F1" };
// To update cells range of cells with the specified settings
$("#Spreadsheet").ejSpreadsheet("updateRange", 1, settings);        
</script>

{% endhighlight %}

### updateUniqueData(data, \[range\])
{:#methods:updateuniquedata}

This method is used to update the unique data for the specified range of cells in Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Pass the  data that you want to update in the particular range</td>
</tr>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">array|string</span></td>
<td class="description"><span class="optional">Optional. </span> If range is specified, it will update data for the specified range else it will use the current selected range.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// To update unique data in Spreadsheet.
xlObj.updateUniqueData([{ value: 10, value2: 10, type: "general"}], [1, 0, 5, 0]); 
</script>

{% endhighlight %}

{% highlight html %}
<script>
// To update unique data in Spreadsheet.
$("#Spreadsheet").ejSpreadsheet("updateUniqueData", [{ value: 10, value2: 10, type: "general"}], [1, 0, 5, 0]);        
</script>

{% endhighlight %}

### wrapText(\[range\])
{:#methods:wraptext}

This method is used to wrap the selected range of cells in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">array|string</span></td>
<td class="description"><span class="optional">Optional. </span> If the range is specified, then it will update wrap in the specified <br/> range else it will use the current selected range.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
//Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// To wrap the cell Text.
xlObj.wrapText("A1:B3");
</script>

{% endhighlight %}

{% highlight html %}
<script>
// To wrap the cell Text.
$("#Spreadsheet").ejSpreadsheet("wrapText","A1:B3")
</script>

{% endhighlight %}

### XLCellType
{:#methods:xlcelltype}

### XLCellType.addCellTypes(range, settings, \[sheetIdx\])
{:#methods:xlcelltype-addcelltypes}

This method is used to set a cell type from the specified range of cells in the spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Pass the range where you want apply cell type.</td>
</tr>
<tr>
<td class="name">settings</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Pass type of cell type and its settings.</td>
</tr>
<tr>
<td class="name">sheetIdx</td>
<td  class="type"><span class="param-type">number</span></td>
<td  class="description">Optional. Pass sheet index.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// To add cell types in Spreadsheet.
xlObj.XLCellType.addCellTypes("A1 : B3", {"type" : ej.Spreadsheet.CustomCellType.Button, "text" : "Button1", "background-color" : "green" },  1);
</script>

{% endhighlight %}

### XLCellType.removeCellTypes(range, \[sheetIdx\])
{:#methods:xlcelltype-removecelltypes}

This method is used to remove cell type from the specified range of cells in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Pass the range where you want remove cell type.</td>
</tr>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description"><span class="optional">Optional. </span> Pass sheet index.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// To remove cell types in Spreadsheet.
xlObj.XLCellType.removeCellTypes("A1:B2", 1);
</script>

{% endhighlight %}

### XLCFormat
{:#methods:xlcformat}

### XLCFormat.clearCF(isSelected, \[range\])
{:#methods:xlcformat-clearcf}

This method is used to clear the applied conditional formatting rules in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">isSelected</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Pass true if you want to clear rules from selected cells else it will clear rules from entire sheet.</td>
</tr>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">array|string</span></td>
<td class="description"><span class="optional">Optional. </span>  If range is specified, it will clear rules for the specified range else it will use the current selected range.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// To clear conditional formatting rules in Spreadsheet.
xlObj.XLCFormat.clearCF(true, [1, 0, 7, 0]);
</script>

{% endhighlight %}

### XLCFormat.getCFRule(rowIdx, colIdx)
{:#methods:xlcformat-getcfrule}

This method is used to get the applied conditional formatting rules as array of objects based on the specified row Index and column Index in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">rowIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the row index.</td>
</tr>
<tr>
<td class="name">colIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the column index.</td>
</tr>
</tbody>
</table>

####Returns:
Array

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Gets the conditional formatting rules in Spreadsheet.
xlObj.XLCFormat.getCFRule(2, 0);
</script>

{% endhighlight %}

### XLCFormat.setCFRule(rule)
{:#methods:xlcformat-setcfrule}

This method is used to set the conditional formatting rule in the Spreadsheet.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">rule</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Pass the rule to set.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
//initialize the Spreadsheet object
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Sets the conditional formatting rules in Spreadsheet
xlObj.XLCFormat.setCFRule({ "action": "lessthan", "input1": "30", "color": "yellowft", "addr": "H3:H7" });
</script>

{% endhighlight %}

### XLChart
{:#methods:xlchart}

### XLChart.createChart(\[range\], \[options\])
{:#methods:xlchart-createchart}

This method is used to create a chart for specified range in Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description"><span class="optional">Optional. </span> If range is specified, it will create chart for the specified range else it will use the current selected range.</td>
</tr>
<tr>
<td class="name">options</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description"><span class="optional">Optional. </span> To pass the type of chart and chart name.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.XLChart.createChart("A3:A7",{"type":"stackingcolumn100","enable3D":"true","marker":{"visible":false}}); // To create chart in Spreadsheet.
</script>

{% endhighlight %}

### XLChart.refreshChart(id, options)
{:#methods:xlchart-refreshchart}

This method is used to refresh the chart in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">id</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">To pass the chart Id.</td>
</tr>
<tr>
<td class="name">options</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">To pass the type of chart and chart name.</td>
</tr>
</tbody>
</table>

#### Example 

{% highlight html %}
<script>
// Create Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.XLChart.refreshChart(id,{"type":"stackingcolumn100","enable3D":"true","marker":{"visible":false}}); // To refresh the chart in Spreadsheet
</script>
{% endhighlight %}

### XLChart.resizeChart(id, height, width)
{:#methods:xlchart-resizechart}

This method is used to resize the chart of specified id in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">id</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">To pass the chart id.</td>
</tr>
<tr>
<td class="name">height</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">To pass height value.</td>
</tr>
<tr>
<td class="name">width</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">To pass the width value.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Create Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.XLChart.resizeChart("Spreadsheet_Chart1", 200, 300); // It is used to resize the chart in Spreadsheet.
</script>

{% endhighlight %}

### XLClipboard
{:#methods:xlclipboard}

### XLClipboard.copy()
{:#methods:xlclipboard-copy}

This method is used to copy the selected cells in the Spreadsheet.

#### Example
{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// To copy cells in a Spreadsheet.
xlObj.XLClipboard.copy();
</script>

{% endhighlight %}

### XLClipboard.cut()
{:#methods:xlclipboard-cut}

This method is used to cut the selected cells in the Spreadsheet.

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// To cut cells in a Spreadsheet
xlObj.XLClipboard.cut();
</script>

{% endhighlight %}

### XLClipboard.paste()
{:#methods:xlclipboard-paste}

This method is used to paste the cut or copied cells data in the Spreadsheet.

#### Example

{% highlight html %}
<script>
//initialize the Spreadsheet object
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// To paste data in Spreadsheet
xlObj.XLClipboard.paste();
</script>

{% endhighlight %}

### XLComment
{:#methods:xlcomment}

### XLComment.deleteComment(\[range\], \[sheetIdx\], \[skipHiddenRow\])
{:#methods:xlcomment-deletecomment}

This method is used to delete the comment in the specified range in Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">array|string</span></td>
<td class="description"><span class="optional">Optional. </span> If range is specified, it will delete comments for the specified range else it will use the current selected range. </td>
</tr>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description"><span class="optional">Optional. </span> If sheetIdx is specified, it will delete comment in specified sheet else it will use active sheet.</td>
</tr>
<tr>
<td class="name">skipHiddenRow</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description"><span class="optional">Optional. </span> Pass true, if you want to skip the hidden rows data.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
//Sends a delete comment request to the Spreadsheet.
xlObj.XLComment.deleteComment("A1:D3", 1, true);
</script>

{% endhighlight %}

### XLComment.editComment(\[targetCell\])
{:#methods:xlcomment-editcomment}

This method is used to edit the comment in the target Cell in Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">targetCell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description"><span class="optional">Optional. </span> Pass the row index and column index of the cell which contains comment. </td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
//Sends an edit comment request to the Spreadsheet.
xlObj.XLComment.editComment({rowIdx: 1, colIdx: 1});
</script>

{% endhighlight %}

### XLComment.findNextComment()
{:#methods:xlcomment-findnextcomment}

This method is used to find the next comment from the active cell in Spreadsheet.

####Returns:
Boolean

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
//Sends a find next comment request to the Spreadsheet.
xlObj.XLComment.findNextComment();
</script>

{% endhighlight %}

### XLComment.findPrevComment()
{:#methods:xlcomment-findprevcomment}

This method is used to find the previous comment from the active cell in Spreadsheet.

####Returns:
Boolean

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
//Sends a find previous comment request to the Spreadsheet.
xlObj.XLComment.findPrevComment();
</script>

{% endhighlight %}

### XLComment.getComment(cell)
{:#methods:xlcomment-getcomment}

This method is used to get comment data for the specified cell.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cell</td>
<td class="type"><span class="param-type">Element</span></td>
<td class="description">Pass the DOM element to get comment data as object.</td>
</tr>
</tbody>
</table>

####Returns:
Object

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// Create Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.getComment(xlObj.getCell(1, 5)); // Get the specified cell comment data.
</script>

{% endhighlight %}

{% highlight html %}
<script>
// Get the specified cell comment data
$("#Spreadsheet").ejSpreadsheet("getComment", xlObj.getCell(1, 5));        
</script>

{% endhighlight %}

### XLComment.setComment(\[range\], \[data\], \[showEditPanel\])
{:#methods:xlcomment-setcomment}

This method is used to set new comment in Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">string|array</span> </td>
<td class="description"><span class="optional">Optional. </span> If we pass the range comment will set in the range otherwise it will set with selected cells. </td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description"><span class="optional">Optional. </span> Pass the comment data.</td>
</tr>
<tr>
<td class="name">showEditPanel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description"><span class="optional">Optional. </span> Pass true to show comment in edit mode </td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
//To set comment in Spreadsheet.
xlObj.XLComment.setComment(spreadsheetObj.getCell(1, 5), "Spreadsheet Comment!");
</script>

{% endhighlight %}

### XLComment.showAllComments()
{:#methods:xlcomment-showallcomments}

This method is used to show all the comments in the Spreadsheet.

#### Example

{% highlight html %}
<script>
// Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
//Sends a show all comment request to the Spreadsheet.
xlObj.XLComment.showAllComments();
</script>

{% endhighlight %}

### XLComment.showHideComment(\[targetCell\])
{:#methods:xlcomment-showhidecomment}

This method is used to show or hide the specific comment in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">targetCell</td>
<td class="type"><span class="param-type">Element</span></td>
<td class="description"><span class="optional">Optional. </span> Pass the cell DOM element to show or hide its comment. If pass empty argument active cell will processed.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
//To show/hide comment request in Spreadsheet.
xlObj.XLComment.showHideComment(spreadsheetObj.getCell(1, 5));
</script>

{% endhighlight %}

### XLDragDrop
{:#methods:xldragdrop}

### XLDragDrop.moveRangeTo(sourceRange, destinationRange)
{:#methods:xldragdrop-moverangeto}

This method is used to drag and drop the selected range of cells to destination range in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">sourceRange</td>
<td class="type"><span class="param-type">object|array</span></td>
<td class="description">Pass the source range to perform drag and drop.</td>
</tr>
<tr>
<td class="name">destinationRange</td>
<td class="type"><span class="param-type">object|array</span></td>
<td class="description">Pass the destination range to drop the dragged cells.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Create Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
var options = {sourcerange: [1,2,1,2], destinationrange: [1,3,1,6]}
xlObj.XLDragDrop.moveRangeTo(options.sourcerange, options.destinationrange); // To perform drag and drop in Spreadsheet.
</script>

{% endhighlight %}

### XLDragFill
{:#methods:xldragfill}

### XLDragFill.autoFill(options)
{:#methods:xldragfill-autofill}

This method is used to perform auto fill in Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">options</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Pass the options to perform auto fill in Spreadsheet.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
var options = {dataRange: "A1:B1", direction: "right", fillRange:"A1:B2"}
xlObj.XLDragFill.autoFill(options); // To perform autofill in Spreadsheet.
</script>

{% endhighlight %}

### XLDragFill.hideAutoFillElement()
{:#methods:xldragfill-hideautofillelement}

This method is used to hide the auto fill element in the Spreadsheet.

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
// Initialize the Spreadsheet object
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// To hide auto fill element in Spreadsheet
xlObj.XLDragFill.hideAutoFillElement();
</script>

{% endhighlight %}

### XLDragFill.hideAutoFillOptions()
{:#methods:xldragfill-hideautofilloptions}

This method is used to hide the auto fill options in the Spreadsheet.

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
// Initialize the Spreadsheet object
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// To hide auto fill element in Spreadsheet
xlObj.XLDragFill.hideAutoFillOptions();
</script>

{% endhighlight %}


### XLDragFill.positionAutoFillElement(isDragFill)
{:#methods:xldragfill-positionautofillelement}

This method is used to set position of the auto fill element in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">isDragFill</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Pass the drag fill status as boolean value for show auto fill options in Spreadsheet.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Create Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.XLDragFill.positionAutoFillElement(false); // set position of the autofill element in Spreadsheet.
</script>

{% endhighlight %}

### XLEdit
{:#methods:xledit}

### XLEdit.calcNow(\[sheetIdx\])
{:#methods:xledit-calcnow}

This method is used to calculate formulas in the specified sheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description"><span class="optional">Optional. </span> If sheet index is specified, then it will calculate formulas in the specified sheet only else it will calculate formulas in all sheets.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.XLEdit.calcNow(1); // To calculate formulas in specified sheet in Spreadsheet.
</script>

{% endhighlight %}

### XLEdit.editCell(rowIdx, colIdx, oldData)
{:#methods:xledit-editcell}

This method is used to edit a particular cell based on the row index and column index in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">rowIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the row index to edit particular cell.</td>
</tr>
<tr>
<td class="name">colIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the column index to edit particular cell.</td>
</tr>
<tr>
<td class="name">oldData</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Pass true, if you want to maintain previous cell value.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
//initialize the Spreadsheet object.
var spreadsheetObj = $("#Spreadsheet").data("ejSpreadsheet");
// Edit particular cell based on row index and column index.
spreadsheetObj.XLEdit.editCell(1, 1, true);
</script>

{% endhighlight %}

{% highlight html %}
<script>
// Edit particular cell based on row index and column index.
$("#Spreadsheet").ejSpreadsheet("XLEdit").editCell(1, 1, true);
</script> 

{% endhighlight %}

### XLEdit.getPropertyValue(rowIdx, colIdx, \[prop\], \[sheetIdx\])
{:#methods:xledit-getpropertyvalue}

This method is used to get the property value of particular cell, based on the row and column index in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">rowIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the row index to get the property value.</td>
</tr>
<tr>
<td class="name">colIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the column index to get the property value.</td>
</tr>
<tr>
<td class="name">prop</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description"><p><span class="optional">Optional. </span>Pass the property name that you want("value", "value2", "type",<br/> "cFormatRule", "range", "thousandSeparator", "rule", "format", "border",<br/> "picture", "chart", "calcValue", "align", "hyperlink", "formats", "borders",<br/> "tformats", "tborders", "isFilterHeader",  "filterState", "tableName",<br/> "comment", "formatStr", "decimalPlaces", "cellType").</p></td>
</tr>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description"><span class="optional">Optional. </span> Pass the index of the sheet.</td>
</tr>
</tbody>
</table>

####Returns:
Object|String|Array

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
// Initialize the Spreadsheet object.
var ssObj = $("#Spreadsheet").data("ejSpreadsheet");
// Get the cell property value.
xlObj.XLEdit.getPropertyValue(1, 1, "value", 1);
</script>

{% endhighlight %}

### XLEdit.getPropertyValueByElem(elem, property, sheetIdx)
{:#methods:xledit-getpropertyvaluebyelem}

This method is used to get the property value in specified cell in Spreadsheet.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">elem</td>
<td class="type"><span class="param-type">Element</span></td>
<td class="description">Pass the cell element to get property value.</td>
</tr>
<tr>
<td class="name">property</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description"><p>Pass the property name that you want ("value", "value2", "type",<br/> "cFormatRule", "range", "thousandSeparator", "rule", "format", "border",<br/> "picture", "chart", "calcValue", "align", "hyperlink", "formats", "borders",<br/> "tformats", "tborders", "isFilterHeader", "filterState", "tableName", <br/>"comment", "formatStr", "decimalPlaces", "cellType").</p></td>
</tr>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the index of sheet.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Get the cell property value based on tag element.
xlObj.XLEdit.getPropertyValueByElem(xlObj.getCell(1, 1), "value", 1);
</script>

{% endhighlight %}

### XLEdit.saveCell()
{:#methods:xledit-savecell}

This method is used to save the edited cell value in the Spreadsheet.

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Save the edited cell value
xlObj.XLEdit.saveCell();
</script>

{% endhighlight %}

### XLEdit.updateCell(cell, value)
{:#methods:xledit-updatecell}

This method is used to update a particular cell value in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Pass row index and column index of the cell.</td>
</tr>
<tr>
<td class="name">value</td>
<td class="type"><span class="param-type">string|number</span></td>
<td class="description">Pass the cell value.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Update the specified values to a particular cell.
xlObj.XLEdit.updateCell({rowIndex: 1, colIndex: 1}, "product");
</script>

{% endhighlight %}

### XLEdit.updateCellValue(cellIdx, val, formatClass, sheetIdx)
{:#methods:xledit-updatecellvalue}

This method is used to update a particular cell value and its format in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cellIdx</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Pass row index and column index of the cell.</td>
</tr>
<tr>
<td class="name">val</td>
<td class="type"><span class="param-type">string|number</span></td>
<td class="description">Pass the cell value.</td>
</tr>
<tr>
<td class="name">formatClass</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Pass the class name to update format. </td>
</tr>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass sheet index.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object
var xlObj = $("#Spreadsheet").data("ejSpreadsheet"), className;
className = xlObj.XLFormat.getFormatHashCode({ color: "red" });
// To update the specified values in a particular cell.
xlObj.XLEdit.updateCellValue({rowIndex: 1, colIndex: 1}, "product", className,1);
</script>

{% endhighlight %}

### XLExport
{:#methods:xlexport}

### XLExport.export(type)
{:#methods:xlexport-export}

This method is used to save the sheet data as Excel or CSV document (.xls, .xlsx and .csv) in Spreadsheet.

N> Using export, user must be provided the excelUrl and csvUrl property under exportSettings

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Pass the export type that you want. </td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// To save the worksheet on Excel format.
xlObj.XLExport.export("Excel");
</script>

{% endhighlight %}

### XLFilter
{:#methods:xlfilter}

### XLFilter.clearFilter()
{:#methods:xlfilter-clearfilter}

This method is used to clear the filter in filtered columns in the Spreadsheet.

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Clear filter for columns in the sheet.
xlObj.XLFilter.clearFilter();
</script>

{% endhighlight %}

### XLFilter.filter(range)
{:#methods:xlfilter-filter}

This method is used to apply filter for the selected range of cells in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Pass the range of the selected cells.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// To apply filter for specified range of cells.
xlObj.XLFilter.filter("A3:C8");
</script>

{% endhighlight %}

### XLFilter.filterByActiveCell()
{:#methods:xlfilter-filterbyactivecell}

This method is used to apply filter for the column by active cell's value in the Spreadsheet.

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Apply filter for columns with active cell in the sheet.
xlObj.XLFilter.filterByActiveCell();
</script>

{% endhighlight %}

### XLFormat
{:#methods:xlformat}

### XLFormat.createTable( tableObject, \[range\])
{:#methods:xlformat-createtable}

This method is used to create a table for the selected range of cells in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">tableObject</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Pass the table object.</td>
</tr>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description"><span class="optional">Optional. </span>  If the range is specified, then it will create table in the specified range else it will use the current selected range. </td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object
var xlObj = $("#Spreadsheet").data("ejSpreadsheet"), tableObj;
tableObj = { header: true, name: "Table 0", formatName: "TableStyleLight1"};
// Sends a create table request to the Spreadsheet
xlObj.XLFormat.createTable(tableObj, "A1:C6");
</script>

{% endhighlight %}

### XLFormat.format(formatObj, range)
{:#methods:xlformat-format}

This method is used to set format style and values in a cell or range of cells.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">formatObj</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Pass the formatObject which contains style, type, format, groupSeparator and decimalPlaces.</td>
</tr>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Pass the range indices to format cells.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Sends a format request to the Spreadsheet.
xlObj.XLFormat.format({style:{ "background-color": "#C0C0C0"}}, "A1:C10");
</script>

{% endhighlight %}

### XLFormat.removeStyle(range,options)
{:#methods:xlformat-removestyle}

This method is used to remove the style in the specified range.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">array|string</span></td>
<td class="description">Pass the cell range .</td>
</tr>
<tr>
<td class="name">options</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description"><span class="optional">Optional. </span>Pass the options for which the style gets removed.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Sends a remove style request to the Spreadsheet.
xlObj.XLFormat.removeStyle("E4:F13",{ cellStyle: true, tableStyle: true, format: true, border: true }); 
</script>

{% endhighlight %}

### XLFormat.removeTable(tableId)
{:#methods:xlformat-removetable}

This method is used to remove table with specified tableId in the Spreadsheet.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">tableId</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the tableId that you want to remove.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Sends a remove table request to the Spreadsheet.
xlObj.XLFormat.removeTable(1);
</script>

{% endhighlight %}

### XLFormat.updateDecimalPlaces(type, range)
{:#methods:xlformat-updatedecimalplaces}

This method is used to update the decimal places for numeric value for the selected range of cells in the Spreadsheet.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Pass the decimal places type in increment/decrement.</td>
</tr>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Pass the range indices.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// To update decimal place value in the range of cells in the Spreadsheet.
xlObj.XLFormat.updateDecimalPlaces("increment", "A1:C3");
</script>

{% endhighlight %}

### XLFormat.updateFormat(formatObj, \[range\])
{:#methods:xlformat-updateformat}

This method is used to update the format for the selected range of cells in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">formatObj</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Pass the format object that you want to update.</td>
</tr>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description"><span class="optional">Optional. </span> If the range is specified, then it will update format in the specified range else it will use the current selected range. </td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object
var xlObj = $("#Spreadsheet").data("ejSpreadsheet"), formatObj;
formatObj = { format: ["e-formatFFFF006N2N2N1N1N1N1N2N1N", "", "e-formatFFFF006N2N2N1N1N1N1N2N1N"], leftborder: ["","",""], topborder: ["e-border1N1N6N1N1N6NS1N1N6N11000000"]};
// To update a format in the specified range of cells.
xlObj.XLFormat.updateFormat(formatObj, [1, 0, 3, 0]);
</script>

{% endhighlight %}

### XLFormat.updateUniqueFormat(formatClass, \[range\])
{:#methods:xlformat-updateuniqueformat}

This method is used to update the unique format for selected range of cells in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">formatClass</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Pass the unique format class.</td>
</tr>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description"><span class="optional">Optional. </span> If the range is specified, then it will update format in the specified range else it will use the current selected range.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// To update the unique format.
xlObj.XLFormat.updateUniqueFormat("e-formatFFFF006N2N2N1N1N1N1N2N1N", [1, 0, 4, 0]);
</script>

{% endhighlight %}

### XLFreeze
{:#methods:xlfreeze}

### XLFreeze.freezeColumns(colIdx)
{:#methods:xlfreeze-freezecolumns}

This method is used to freeze columns upto the specified column index in the Spreadsheet.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">colIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Index of the column to be freeze.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
//initialize the Spreadsheet object
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Freeze a column in the sheet.
xlObj.XLFreeze.freezeColumns(2);
</script>

{% endhighlight %}

### XLFreeze.freezeLeftColumn()
{:#methods:xlfreeze-freezeleftcolumn}

This method is used to freeze the first column in the Spreadsheet.

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Freeze the first column in the sheet.
xlObj.XLFreeze.freezeLeftColumn();
</script>

{% endhighlight %}

### XLFreeze.freezePanes(cell)
{:#methods:xlfreeze-freezepanes}

This method is used to freeze rows and columns before the specified cell in the Spreadsheet.

<table>
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Row index and column index of the cell which you want to freeze.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// Initialize the Spreadsheet object
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Freeze some rows and columns in the sheet.
xlObj.XLFreeze.freezePane({ rowIndex: 2, colIndex: 3});
</script>

{% endhighlight %}

### XLFreeze.freezeRows(rowIdx)
{:#methods:xlfreeze-freezerows}

This method is used to freeze rows upto the specified row index in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">rowIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Index of the row to be freeze.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
//initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Freeze a row in the sheet.
xlObj.XLFreeze.freezeRows(2);
</script>

{% endhighlight %}

### XLFreeze.freezeTopRow()
{:#methods:xlfreeze-freezetoprow}

This method is used to freeze the top row in the Spreadsheet.

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
//initialize the Spreadsheet object
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Freeze the top row in the sheet.
xlObj.XLFreeze.freezeTopRow();
</script>

{% endhighlight %}

### XLPivot
{:#methods:xlpivot}

### XLPivot.clearPivotFieldList(pivotName)
{:#methods:xlpivot-clearpivotfieldlist}

This property is used to clear the pivot table list in Spreadsheet.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">pivotName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Pass the name of the pivot table. </td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Create Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.XLPivot.clearPivotFieldList("name"); // Sends a clear pivot field list request to the Spreadsheet.
</script>

{% endhighlight %}


### XLPivot.createPivotTable(range,location,name,settings,pvt)
{:#methods:xlpivot-createpivottable}

This method is used to create pivot table.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">It specifies the range for which the pivot table is created.</td>
</tr>
<tr>
<td class="name">location</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">It specifies the location in which the pivot table is created.</td>
</tr>
<tr>
<td class="name">name</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">It specifies the name of the pivot table.</td>
</tr>
<tr>
<td class="name">settings</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Pass the pivot table settings.</td>
</tr>
<tr>
<td class="name">pvt</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Pass the pivot range, sheet index, address and data source .</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// create a pivot table in the sheet.
var settings = {
                 rows: [ {fieldName: "Country",},{fieldName: "State",}],
                 columns: [{fieldName: "Product",}],
                 values: [{fieldName: "Amount", },{fieldName: "Quantity", } ],
                 filters: [ {fieldName: "Date", }] };
xlObj.XLPivot.createPivotTable("Sheet1!$A$1:$F$25","Sheet1!$A$1", null, settings);
</script>

{% endhighlight %}

### XLPivot.deletePivotTable(pivotName)
{:#methods:xlpivot-deletepivottable}

This method is used to delete the pivot table which is selected.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">pivotName</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description">Pass the name of the pivot table.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Delete pivot table in the sheet.
xlObj.XLPivot.deletePivotTable("name");
</script>

{% endhighlight %}

### XLPivot.refreshDataSource(name, sheetIdx)
{:#methods:xlpivot-refreshdatasource}

This method is used to refresh data in pivot table.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">name</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description"><span class="optional">Optional. </span>Pass the name of the pivot table.</td>
</tr>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description"><span class="optional">Optional. </span>Pass the index of the sheet.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.XLPivot.refreshDataSource(); // Sends a refresh data source request to the Spreadsheet.
</script>

{% endhighlight %}

### XLPrint
{:#methods:xlprint}

### XLPrint.printSelection()
{:#methods:xlprint-printselection}

This method is used to print the selected contents in the Spreadsheet.

#### Example

{% highlight html %}
<script>
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Print the selected area in the sheet.
xlObj.XLPrint.printSelection();
</script>

{% endhighlight %}

### XLPrint.printSheet()
{:#methods:xlprint-printsheet}

This method is used to print the entire contents in the active sheet.

#### Example

{% highlight html %}
<script>
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
//Sends a print entire sheet request to the Spreadsheet.
xlObj.XLPrint.printSheet();
</script>

{% endhighlight %}

### XLResize
{:#methods:xlresize}

### XLResize.getColWidth(colIdx)
{:#methods:xlresize-getcolwidth}

This method is used to get the column width of the specified column index in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">colIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the column index.</td>
</tr>
</tbody>
</table>

####Returns:
Number

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
//initialize the Spreadsheet object
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Gets the particular column width in Spreadsheet.
xlObj.XLResize.getColWidth(2);
</script>

{% endhighlight %}

### XLResize.getRowHeight(rowIdx)
{:#methods:xlresize-getrowheight}

This method is used to get the row height of the specified row index in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">rowIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the row index which you want to find its height.</td>
</tr>
</tbody>
</table>

####Returns:
Number

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Gets the particular row height in Spreadsheet.
xlObj.XLResize.getRowHeight(2);
</script>

{% endhighlight %}

{% highlight html %}
<script>
// Gets the particular row height in Spreadsheet.
$("#Spreadsheet").ejSpreadsheet("XLResize.getRowHeight",2);
</script>

{% endhighlight %}

### XLResize.setColWidth(colIdx, size)
{:#methods:xlresize-setcolwidth}

This method is used to set the column width of the specified column index in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">colIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the column index.</td>
</tr>
<tr>
<td class="name">size</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the width value that you want to set.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Sets the column width in the Spreadsheet.
xlObj.XLResize.setColWidth(2, 100);
</script>

{% endhighlight %}

### XLResize.setRowHeight(rowIdx, size)
{:#methods:xlresize-setrowheight}

This method is used to set the row height of the specified row index in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">rowIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the row index.</td>
</tr>
<tr>
<td class="name">size</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the height value that you want to set.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
//initialize the Spreadsheet object
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// Sets the row height in Spreadsheet.
xlObj.XLResize.setRowHeight(2, 100);
</script>

{% endhighlight %}


### XLRibbon
{:#methods:xlribbon}

### XLRibbon.addNamedRange(name, refersTo, \[comment\], \[sheetIdx\])
{:#methods:xlribbon-addnamedrange}

This method is used to add a new name in the Spreadsheet name manager.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">name</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Pass the name that you want to define in name manager.</td>
</tr>
<tr>
<td class="name">refersTo</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Pass the cell reference.</td>
</tr>
<tr>
<td class="name">comment</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description"><span class="optional">Optional. </span> Pass comment, if you want.</td>
</tr>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description"><span class="optional">Optional. </span>  Pass the sheet index.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// To define new name in the Spreadsheet.
xlObj.XLRibbon.addNamedRange("PRICE_LIST", "=Sheet1!$A$2:$A$7", "Month_Wise");
</script>

{% endhighlight %}

### XLRibbon.autoSum(type, range)
{:#methods:xlribbon-autosum}

This method is used to insert the few type (SUM, MAX, MIN, AVG, COUNT) of formulas in the selected range of cells in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">To pass the type("SUM","MAX","MIN","AVG","COUNT").</td>
</tr>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">If range is specified, it will apply auto sum for the specified range else it will use the current selected range.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.XLRibbon.autoSum("SUM", "A2:A6"); // To insert the formula after selected range of cells in Spreadsheet.
</script>

{% endhighlight %}

### XLRibbon.removeNamedRange(name)
{:#methods:xlribbon-removenamedrange}

This method is used to delete the defined name in the Spreadsheet name manager.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">name</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Pass the defined name that you want to remove from name manager.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
//initialize the Spreadsheet object
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// To remove the define name in Spreadsheet name manager.
xlObj.XLRibbon.removeNamedRange("PRICE_LIST");
</script>

{% endhighlight %}

### XLSearch
{:#methods:xlsearch}

### XLSearch.replaceAllByBook(findData, replaceData, isCSen, isEMatch)
{:#methods:xlsearch-replaceallbybook}

This method is used to find and replace all data by workbook in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">findData</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Pass the search data.</td>
</tr>
<tr>
<td class="name">replaceData</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Pass the replace data.</td>
</tr>
<tr>
<td class="name">isCSen</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Pass true, if you want to match with case-sensitive.</td>
</tr>
<tr>
<td class="name">isEMatch</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Pass true, if you want to match with entire cell contents.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.XLSearch.replaceAllByBook("Sheet", "Spreadsheet", true, false); // Sends a replace all by workbook request to the Spreadsheet.
</script>

{% endhighlight %}

### XLSearch.replaceAllBySheet(findData, replaceData, isCSen, isEMatch)
{:#methods:xlsearch-replaceallbysheet}

This method is used to find and replace all data by sheet in Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">findData</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Pass the search data.</td>
</tr>
<tr>
<td class="name">replaceData</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Pass the replace data.</td>
</tr>
<tr>
<td class="name">isCSen</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Pass true, if you want to match with case-sensitive.</td>
</tr>
<tr>
<td class="name">isEMatch</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Pass true, if you want to match with entire cell contents.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.XLSearch.replaceAllBySheet("Sheet", "Spreadsheet", true, false); // Sends a replace all by sheet request to Spreadsheet
</script>

{% endhighlight %}

### XLSelection
{:#methods:xlselection}

### XLSelection.getSelectedCells(sheetIdx)
{:#methods:xlselection-getselectedcells}

This method is used to get the selected cells element based on specified sheet index in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the sheet index to get the cells element.</td>
</tr>
</tbody>
</table>

####Returns:
Element

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
// Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.XLSelection.getSelectedCells(1); //Gets the selected cells element.
</script>

{% endhighlight %}

### XLSelection.refreshSelection(\[range\])
{:#methods:xlselection-refreshselection}

This method is used to refresh the selection in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description"><span class="optional">Optional. </span> Pass range to refresh selection.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
//initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// To defined refresh selection in Spreadsheet.
xlObj.XLSelection.refreshSelection([1,2,3,4]);
</script>

{% endhighlight %}

### XLSelection.selectColumn(colIdx)
{:#methods:xlselection-selectcolumn}

This method is used to select a single column in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">colIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the column index value.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.XLSelection.selectColumn(1); //To select a single column in the active sheet.
</script>

{% endhighlight %}

### XLSelection.selectColumns(startIdx, endIdx)
{:#methods:xlselection-selectcolumns}

This method is used to select entire columns in a specified range (start index and end index) in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">startIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the column start index.</td>
</tr>
<tr>
<td class="name">endIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the column end index.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.XLSelection.selectColumns(2, 4); //To select entire columns in the specified range.
</script>

{% endhighlight %}

### XLSelection.selectRange(range)
{:#methods:xlselection-selectrange}

This method is used to select the specified range of cells in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Pass range which want to select.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.XLSelection.selectRange("A1:B2"); //To select range of cells in Spreadsheet.
</script>
{% endhighlight %}

### XLSelection.selectRow(rowIdx)
{:#methods:xlselection-selectrow}

This method is used to select a single row in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">rowIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the row index value.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.XLSelection.selectRow(1); //To select a single row in the specified sheet index in Spreadsheet.
</script>

{% endhighlight %}

### XLSelection.selectRows(startIdx, endIdx)
{:#methods:xlselection-selectrows}

This method is used to select entire rows in a specified range (start index and end index) in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">startIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the start row index.</td>
</tr>
<tr>
<td class="name">endIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Pass the end row index.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
xlObj.XLSelection.selectRows(2, 4); //To select entire rows in the specified range.
</script>

{% endhighlight %}

### XLSelection.selectSheet()
{:#methods:xlselection-selectsheet}

This method is used to select all cells in active sheet.

#### Example

{% highlight html %}
<script>
// Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
spreadsheetObj.XLSelection.selectSheet(); //To select all cells in Spreadsheet.
</script>

{% endhighlight %}

### XLSort
{:#methods:xlsort}

### XLSort.sortByColor(operation, color, range)
{:#methods:xlsort-sortbycolor}

This method is used to sort a particular range of cells based on its cell or font color in the Spreadsheet.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">operation</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Pass 'PutCellColor' to sort by cell color or 'PutFontColor' for by font color.</td>
</tr>
<tr>
<td class="name">color</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Pass the HEX color code to sort.</td>
</tr>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Pass the range</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
//To sort range based on cell color in the Spreadsheet.
xlObj.XLSort.sortByColor("PutCellColor", {"background-color" : "#EC2024", color:  "#6N2N2N"}, "D2:D8"); </script>

{% endhighlight %}

### XLSort.sortByRange(range, columnName, direction)
{:#methods:xlsort-sortbyrange}

This method is used to sort a particular range of cells based on its values in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">array|string</span></td>
<td class="description">Pass the range to sort.</td>
</tr>
<tr>
<td class="name">columnName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Pass the column name.</td>
</tr>
<tr>
<td class="name">direction</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Pass the direction to sort (ascending or descending).</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
//To sort the cell value in a specified range in the Spreadsheet.
xlObj.XLSort.sortByRange("A1:D3", "B",  "ascending"); 
</script>

{% endhighlight %}

### XLValidate
{:#methods:xlvalidate}

### XLValidate.applyDVRules(range, values, type, required, showErrorAlert)
{:#methods:xlvalidate-applydvrules}

This method is used to apply data validation rules in a selected range of cells based on the defined condition in the Spreadsheet.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">If range is specified, it will apply rules for the specified range else it will use the current selected range. </td>
</tr>
<tr>
<td class="name">values</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description">Pass the validation condition, value1 and value2.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Pass the data type.</td>
</tr>
<tr>
<td class="name">required</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Pass 'true' if you ignore blank values.</td>
</tr>
<tr>
<td class="name">showErrorAlert</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Pass 'true' if you want to show an error alert.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
//Initialize the Spreadsheet object.
var xlObj = $("#Spreadsheet").data("ejSpreadsheet");
// To apply validation rule to allow whole number between 15 and 20.
xlObj.XLValidate.applyDVRules("A1:D3", ["Between", "15", "20"], "number" ,true, true);
</script>

{% endhighlight %}

### XLValidate.clearDV(\[range\])
{:#methods:xlvalidate-cleardv}

This method is used to clear the applied validation rules in a specified range of cells in the Spreadsheet.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description"><span class="optional">Optional. </span> If range is specified, it will clear rules for the specified range else it will use the current selected range. </td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<script>
// Initialize the Spreadsheet object.
var spreadsheetObj = $("#Spreadsheet").data("ejSpreadsheet");
// To clear validation rules in selected cells.
spreadsheetObj.XLValidate.clearDV("A2:A7");
</script>

{% endhighlight %}

### XLValidate.highlightInvalidData(\[range\])
{:#methods:xlvalidate-highlightinvaliddata}

This method is used to highlight invalid data in a specified range of cells in the Spreadsheet.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description"><span class="optional">Optional. </span> If range is specified, it will clear rules for the specified range else it will use the current selected range.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
//initialize the Spreadsheet object
var spreadsheetObj = $("#Spreadsheet").data("ejSpreadsheet");
// To highlight invalid cell data
spreadsheetObj.XLValidate.highlightInvalidData("A2:A7");
</script>

{% endhighlight %}

## Events

### actionBegin
{:#events:actionbegin}

Triggered for every action before its starts.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Arguments when actionBegin event is triggered. 
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">afterFormat</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the applied style format object.</td>
</tr>
<tr>
<td class="name">beforeFormat</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the applied style format object.</td>
</tr>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Returns the sheet index.</td>
</tr>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description">Returns the cell range.</td>
</tr>
<tr>
<td class="name">reqType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the action format.</td>
</tr>
<tr>
<td class="name">gotoIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Returns goto index while paging.</td>
</tr>
<tr>
<td class="name">newSheet</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns boolean value. If create new sheet it returns true.</td>
</tr>
<tr>
<td class="name">columnName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Return column name while sorting.</td>
</tr>
<tr>
<td class="name">colSelected</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Returns selected columns while sorting or filtering begins.</td>
</tr>
<tr>
<td class="name">sortDirection</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns sort direction while sort action begins.</td>
</tr>
</tbody>
</table>
</td></tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
//actionBegin event for Spreadsheet
$("#Spreadsheet").ejSpreadsheet({
actionBegin: function (args){}
});
</script>

{% endhighlight %}

### actionComplete
{:#events:actioncomplete}

Triggered for every action complete.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Arguments when actionComplete event is triggered. 
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.Spreadsheet.Model"/><span class="param-type">object</span></td>
<td class="description">Returns Spreadsheet model.</td>
</tr>
<tr>
<td class="name">selectedCell</td>
<td class="type"><span class="param-type">array|object</span></td>
<td class="description">Returns the applied cell format object.</td>
</tr>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Returns the sheet index.</td>
</tr>
<tr>
<td class="name">reqType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the request type.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td></tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
//actionComplete event for Spreadsheet
$("#Spreadsheet").ejSpreadsheet({
actionComplete: function (args){}
});
</script>

{% endhighlight %}

### autoFillBegin
{:#events:autofillbegin}

Triggered when the auto fill operation begins.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Arguments when autoFillBegin event is triggered. 
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">dataRange</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description">Returns auto fill begin cell range.</td>
</tr>
<tr>
<td class="name">direction</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns which direction drag the auto fill.</td>
</tr>
<tr>
<td class="name">fillRange</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description">Returns fill cells range.</td>
</tr>
<tr>
<td class="name">fillType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the auto fill type.</td>
</tr>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Returns the sheet index.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.Spreadsheet.Model"/><span class="param-type">object</span></td>
<td class="description">Returns the Spreadsheet model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event.</td>
</tr><tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns the cancel option value.</td>
</tr>
</tbody>
</table>
</td></tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
//autoFillBegin event for Spreadsheet
$("#Spreadsheet").ejSpreadsheet({
autoFillBegin: function (args){}
});
</script>

{% endhighlight %}

### autoFillComplete
{:#events:autofillcomplete}

Triggered when the auto fill operation completes.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Arguments when autoFillComplete event is triggered. 
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">dataRange</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description">Returns auto fill begin cell range.</td>
</tr>
<tr>
<td class="name">direction</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns which direction to drag the auto fill.</td>
</tr>
<tr>
<td class="name">fillRange</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description">Returns fill cells range.</td>
</tr>
<tr>
<td class="name">fillType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the auto fill type.</td>
</tr>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Returns the sheet index.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.Spreadsheet.Model"/><span class="param-type">object</span></td>
<td class="description">Returns the Spreadsheet model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns the cancel option value.</td>
</tr>
</tbody>
</table>
</td></tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
//autoFillComplete event for Spreadsheet
$("#Spreadsheet").ejSpreadsheet({
autoFillComplete: function (args){}
});
</script>

{% endhighlight %}

### beforeBatchSave
{:#events:beforebatchsave}

Triggered before the batch save.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Arguments when beforeBatchSave event is triggered. 
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">Number</span></td>
<td class="description">Returns the sheet index.</td>
</tr><tr>
<td class="name">dataSetting</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Returns the query, primary key,batch changes for the data Source.</td>
</tr>
<tr>
<td class="name">batchChanges</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Returns the changed record object.</td>
</tr>
</tbody>
</table>
</td></tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
//beforeBatchSave event for Spreadsheet
$("#Spreadsheet").ejSpreadsheet({
beforeBatchSave: function (args){}
});
</script>

{% endhighlight %}

### beforeCellFormat
{:#events:beforecellformat}

Triggered before the cells to be formatted.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Arguments when beforeCellFormat event is triggered. 
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Returns the sheet index.</td>
</tr><tr>
<td class="name">format</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the applied style format object.</td>
</tr>
<tr>
<td class="name">cells</td>
<td class="type"><span class="param-type">array|object</span></td>
<td class="description">Returns the selected cells.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.Spreadsheet.Model"/><span class="param-type">object</span></td>
<td class="description">Returns the Spreadsheet model.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td></tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
//beforeCellFormat event for Spreadsheet
$("#Spreadsheet").ejSpreadsheet({
beforeCellFormat: function (args){}
});
</script>

{% endhighlight %}


### beforeCellSelect
{:#events:beforecellselect}

Triggered before the cell selection.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Arguments when beforeCellSelect event is triggered. 
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">prevRange</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description">Returns the previous cell range.</td>
</tr>
<tr>
<td class="name">currRange</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description">Returns the current cell range.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.Spreadsheet.Model"/><span class="param-type">object</span></td>
<td class="description">Returns the Spreadsheet model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns the cancel option value.</td>
</tr>
</tbody>
</table>
</td></tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// beforeCellSelect event for Spreadsheet
$('#Spreadsheet').ejSpreadsheet({ 
beforeCellSelect: function (args){}
});
</script>

{% endhighlight %}

### beforeDrop
{:#events:beforedrop}

Triggered before the selected cells are dropped.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Arguments when beforeDrop event is triggered. 
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Returns the sheet index.</td>
</tr>
<tr>
<td class="name">currentCell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the current cell row and column index.</td>
</tr>
<tr>
<td class="name">dragAndDropRange</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the drag cells range object.</td>
</tr>
<tr>
<td class="name">preventAlert</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns the cell Overwriting alert option value.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.Spreadsheet.Model"/><span class="param-type">object</span></td>
<td class="description">Returns the Spreadsheet model.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">Element</span></td>
<td class="description">Returns the target item.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns the cancel option value.</td>
</tr>
</tbody>
</table>
</td></tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
//beforeDrop event for Spreadsheet.
$("#Spreadsheet").ejSpreadsheet({
beforeDrop: function (args){}
});
</script>

{% endhighlight %}

### beforeOpen
{:#events:beforeopen}

Triggered before the contextmenu is open.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Arguments when beforeOpen event is triggered. 
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">Element</span></td>
<td class="description">Returns the target element.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.Spreadsheet.Model"/><span class="param-type">object</span></td>
<td class="description">Returns the Spreadsheet model.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns the cancel option value.</td>
</tr>
</tbody>
</table>
</td></tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
//beforeOpen event for Spreadsheet
$('#Spreadsheet').ejSpreadsheet({ 
beforeOpen: function (args){}
});
</script>

{% endhighlight %}

### beforePanelOpen
{:#events:beforepanelopen}

Triggered before the activation panel is open.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Arguments when beforePanelOpen event is triggered. 
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Returns the sheet index.</td>
</tr>
<tr>
<td class="name">activationPanel</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the activation panel element.</td>
</tr>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the range option value.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.Spreadsheet.Model"/><span class="param-type">object</span></td>
<td class="description">Returns the Spreadsheet model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns the cancel option value.</td>
</tr>
</tbody>
</table>
</td></tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// beforePanelOpen event for Spreadsheet
$('#Spreadsheet').ejSpreadsheet({ 
beforePanelOpen: function (args){}
});
</script>

{% endhighlight %}

### cellClick
{:#events:cellclick}

Triggered when click on sheet cell.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Arguments when cellClick event is triggered. 
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cell</td>
<td class="type"><span class="param-type">Element</span></td>
<td class="description">Returns the click cell element.</td>
</tr>
<tr>
<td class="name">columnIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Returns the column index of clicked cell.</td>
</tr>
<tr>
<td class="name">rowIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Returns the row index of clicked cell.</td>
</tr>
<tr>
<td class="name">columnName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the column name of clicked cell.</td>
</tr>
<tr>
<td class="name">columnObject</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the column information.</td>
</tr>
</tbody>
</table>
</td></tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
//cellClick event for Spreadsheet
$('#Spreadsheet').ejSpreadsheet({ 
cellClick: function (args){}
});
</script>

{% endhighlight %}

### cellEdit
{:#events:celledit}

Triggered when the cell is edited.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Arguments when cellEdit event is triggered. 
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cell</td>
<td class="type"><span class="param-type">Element</span></td>
<td class="description">Returns the click cell element.</td>
</tr>
<tr>
<td class="name">columnName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the columnName of clicked cell.</td>
</tr>
<tr>
<td class="name">columnObject</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the column field information.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.Spreadsheet.Model"/><span class="param-type">object</span></td>
<td class="description">Returns the Spreadsheet model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns the cancel option value.</td>
</tr>
</tbody>
</table>
</td></tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
//cellEdit event for Spreadsheet
$('#Spreadsheet').ejSpreadsheet({ 
cellEdit: function (args){}
});
</script>

{% endhighlight %}

### cellFormatting
{:#events:cellformatting}

Triggered while cell is formatting.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Arguments when cellFormatting event is triggered. 
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">SheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Returns the sheet index</td>
</tr>
<tr>
<td class="name">Format</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the applied style format object</td>
</tr>
<tr>
<td class="name">Cell</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Returns the cell index.</td>
</tr>
</tbody>
</table>
</td></tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
//cellFormatting event for Spreadsheet
$('#Spreadsheet').ejSpreadsheet({ 
cellFormatting: function (args){}
});
</script>

{% endhighlight %}

### cellHover
{:#events:cellhover}

Triggered when mouse hover on cell in sheets.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Arguments when cellHover event is triggered. 
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">Element</span></td>
<td class="description">Returns the target element.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.Spreadsheet.Model"/><span class="param-type">object</span></td>
<td class="description">Returns the Spreadsheet model.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns the cancel option value.</td>
</tr>
</tbody>
</table>
</td></tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// cellHover event for Spreadsheet
$('#Spreadsheet').ejSpreadsheet({ 
cellHover: function (args){}
});
</script>

{% endhighlight %}

### cellSave
{:#events:cellsave}

Triggered when save the edited cell.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Arguments when cellSave event is triggered. 
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cell</td>
<td class="type"><span class="param-type">Element</span></td>
<td class="description">Returns the save cell element.</td>
</tr>
<tr>
<td class="name">columnName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the columnName of clicked cell.</td>
</tr>
<tr>
<td class="name">columnObject</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the column field information.</td>
</tr>
<tr>
<td class="name">rowIndex</td>
<td class="type"><span class="param-type">Number</span></td>
<td class="description">Returns the index of the row.</td>
</tr>
<tr>
<td class="name">colIndex</td>
<td class="type"><span class="param-type">Number</span></td>
<td class="description">Returns the index of the column.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.Spreadsheet.Model"/><span class="param-type">object</span></td>
<td class="description">Returns the Spreadsheet model.</td>
</tr>
<tr>
<td class="name">pValue</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the cell previous value.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">value</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the cell value.</td>
</tr>
</tbody>
</table>
</td></tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
//cellSave event for Spreadsheet
$('#Spreadsheet').ejSpreadsheet({ 
cellSave: function (args){}
});
</script>

{% endhighlight %}

### contextMenuClick
{:#events:contextmenuclick}

Triggered when click the contextmenu items.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Arguments when contextMenuClick event is triggered. 
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Id</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns target element Id.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type"><span class="param-type">Element</span></td>
<td class="description">Returns the target element.</td>
</tr>
<tr>
<td class="name">event</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns event information.</td>
</tr>
<tr>
<td class="name">events</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns target element and event information.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.Spreadsheet.Model"/><span class="param-type">object</span></td>
<td class="description">Returns the Spreadsheet model.</td>
</tr>
<tr>
<td class="name">parentId</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns target element parent Id.</td>
</tr>
<tr>
<td class="name">parentText</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns target element parent text.</td>
</tr>
<tr>
<td class="name">text</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns target element text.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns the cancel option value.</td>
</tr>
</tbody>
</table>
</td></tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// contextMenuClick event for Spreadsheet.
$('#Spreadsheet').ejSpreadsheet({ 
contextMenuClick: function (args){}
});
</script>

{% endhighlight %}

### drag
{:#events:drag}

Triggered when the selected cells are being dragged.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Arguments when drag event is triggered. 
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Returns the sheet index.</td>
</tr>
<tr>
<td class="name">currentCell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the current cell row and column index.</td>
</tr>
<tr>
<td class="name">dragAndDropRange</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the drag cells range object.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.Spreadsheet.Model"/><span class="param-type">object</span></td>
<td class="description">Returns the Spreadsheet model.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">Element</span></td>
<td class="description">Returns the target item.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns the cancel option value.</td>
</tr>
</tbody>
</table>
</td></tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
//drag event for Spreadsheet
$("#Spreadsheet").ejSpreadsheet({
drag: function (args){}
});
</script>

{% endhighlight %}

### dragStart
{:#events:dragstart}

Triggered when the selected cells are initiated to drag.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Arguments when dragStart event is triggered. 
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Returns the sheet index.</td>
</tr>
<tr>
<td class="name">currentCell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the current cell row and column index.</td>
</tr>
<tr>
<td class="name">dragAndDropRange</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the drag cells range object.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.Spreadsheet.Model"/><span class="param-type">object</span></td>
<td class="description">Returns the Spreadsheet model.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">Element</span></td>
<td class="description">Returns the target item.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns the cancel option value.</td>
</tr>
</tbody>
</table>
</td></tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
//dragStart event for Spreadsheet
$("#Spreadsheet").ejSpreadsheet({
dragStart: function (args){}
});
</script>

{% endhighlight %}

### drop
{:#events:drop}

Triggered when the selected cells are dropped.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Arguments when drop event is triggered. 
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Returns the sheet index.</td>
</tr>
<tr>
<td class="name">currentCell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the current cell row and column index.</td>
</tr>
<tr>
<td class="name">dragAndDropRange</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the drag cells range object.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.Spreadsheet.Model"/><span class="param-type">object</span></td>
<td class="description">Returns the Spreadsheet model.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">Element</span></td>
<td class="description">Returns the target item.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns the cancel option value.</td>
</tr>
</tbody>
</table>
</td></tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
//drop event for Spreadsheet
$("#Spreadsheet").ejSpreadsheet({
drop: function (args){}
});
</script>

{% endhighlight %}

### editRangeBegin
{:#events:editrangebegin}

Triggered before the range editing starts.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Arguments when editRangeBegin event is triggered. 
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Returns the sheet index.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.Spreadsheet.Model"/><span class="param-type">object</span></td>
<td class="description">Returns the Spreadsheet model.</td>
</tr>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the range option value.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns the cancel option value.</td>
</tr>
</tbody>
</table>
</td></tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// editRangeBegin event for Spreadsheet.
$('#Spreadsheet').ejSpreadsheet({ 
editRangeBegin: function (args){}
});
</script>

{% endhighlight %}

### editRangeComplete
{:#events:editrangecomplete}

Triggered after range editing completes.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Arguments when editRangeComplete event is triggered. 
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">sheetIdx</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Returns the sheet index.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.Spreadsheet.Model"/><span class="param-type">object</span></td>
<td class="description">Returns the Spreadsheet model.</td>
</tr>
<tr>
<td class="name">range</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the range option value.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns the cancel option value.</td>
</tr>
</tbody>
</table>
</td></tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// editRangeComplete event for Spreadsheet
$('#Spreadsheet').ejSpreadsheet({ 
editRangeComplete: function (args){}
});
</script>

{% endhighlight %}

### load
{:#events:load}

Triggered before the sheet is loaded.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Arguments when load event is triggered. 
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.Spreadsheet.Model"/><span class="param-type">object</span></td>
<td class="description">Returns the Spreadsheet model.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">sheetIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Returns the active sheet index.</td>
</tr>
</tbody>
</table>
</td></tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
//load event for Spreadsheet
$('#Spreadsheet').ejSpreadsheet({ 
load: function (args){}
});
</script>

{% endhighlight %}

### loadComplete
{:#events:loadcomplete}

Triggered after the sheet is loaded.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Arguments when loadComplete event is triggered. 
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.Spreadsheet.Model"/><span class="param-type">object</span></td>
<td class="description">Returns the Spreadsheet model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns the cancel option value.</td>
</tr>
</tbody>
</table>
</td></tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// loadComplete event for Spreadsheet
$('#Spreadsheet').ejSpreadsheet({ 
loadComplete: function (args){}
});
</script>

{% endhighlight %}

### menuClick
{:#events:menuclick}

Triggered every click of the menu item.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Arguments when menuClick event is triggered. 
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">element</td>
<td class="type"><span class="param-type">Element</span></td>
<td class="description">Returns menu click element.</td>
</tr>
<tr>
<td class="name">event</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns the event information.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.Spreadsheet.Model"/><span class="param-type">object</span></td>
<td class="description">Returns the Spreadsheet model.</td>
</tr>
<tr>
<td class="name">parentId</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns target element parent Id.</td>
</tr>
<tr>
<td class="name">parentText</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns target element parent text.</td>
</tr>
<tr>
<td class="name">text</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns target element text.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns the cancel option value.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// menuClick event for Spreadsheet.
$('#Spreadsheet').ejSpreadsheet({ 
menuClick: function (args){}
});
</script>

{% endhighlight %}

### openFailure
{:#events:openfailure}

Triggered when import sheet is failed to open.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type">object</td>
<td class="description">Arguments when openFailure event is triggered. 
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">failureType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the failure type.</td>
</tr>
<tr>
<td class="name">status</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Returns the status index.</td>
</tr>
<tr>
<td class="name">statusText</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the status in text.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.Spreadsheet.Model"/><span class="param-type">object</span></td>
<td class="description">Returns the Spreadsheet model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns the cancel option value.</td>
</tr>
</tbody>
</table>
</td></tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
//openFailure event for Spreadsheet
$("#Spreadsheet").ejSpreadsheet({
openFailure: function (args){}
});
</script>

{% endhighlight %}

### pagerClick
{:#events:pagerclick}

Triggered when pager item is clicked in the Spreadsheet.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Arguments when pagerClick event is triggered. 
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">activeSheet</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Returns the active sheet index.</td>
</tr>
<tr>
<td class="name">gotoSheet</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Returns the new sheet index.</td>
</tr>
<tr>
<td class="name">newSheet</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns whether new sheet icon is clicked.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.Spreadsheet.Model"/><span class="param-type">object</span></td>
<td class="description">Returns the Spreadsheet model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns the cancel option value.</td>
</tr>
</tbody>
</table>
</td></tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// pagerClick event for Spreadsheet
$('#Spreadsheet').ejSpreadsheet({ 
pagerClick: function (args){}
});
</script>

{% endhighlight %}

### ribbonClick
{:#events:ribbonclick}

Triggered when click on the ribbon.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Arguments when ribbonClick event is triggered. 
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Id</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns element Id.</td>
</tr>
<tr>
<td class="name">prop</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns target information.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.Spreadsheet.Model"/><span class="param-type">object</span></td>
<td class="description">Returns the Spreadsheet model.</td>
</tr>
<tr>
<td class="name">status</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns status.</td>
</tr>
<tr>
<td class="name">isChecked</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns isChecked in boolean.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns the cancel option value.</td>
</tr>
</tbody>
</table>
</td></tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// ribbonClick event for Spreadsheet
$('#Spreadsheet').ejSpreadsheet({ 
ribbonClick: function (args){}
});
</script>

{% endhighlight %}

### seriesRendering
{:#events:seriesrendering}

Triggered when the chart series rendering.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Arguments when seriesRendering event is triggered. 
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns chart data and chart information.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.Spreadsheet.Model"/><span class="param-type">object</span></td>
<td class="description">Returns the chart model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns the cancel option value.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div>
<script>
//seriesRendering event for Spreadsheet
$("#Spreadsheet").ejSpreadsheet({
seriesRendering: function (args){}
});
</script>

{% endhighlight %}

### tabClick
{:#events:tabclick}

Triggered when click the ribbon tab.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Arguments when tabClick event is triggered. 
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">activeIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Returns the active tab index.</td>
</tr>
<tr>
<td class="name">activeHeader</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns active tab header element.</td>
</tr>
<tr>
<td class="name">prevActiveHeader</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns previous active tab header element.</td>
</tr>
<tr>
<td class="name">prevActiveIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Returns previous active tab index.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.Spreadsheet.Model"/><span class="param-type">object</span></td>
<td class="description">Returns the Spreadsheet model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns the cancel option value.</td>
</tr>
</tbody>
</table>
</td></tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// tabClick event for Spreadsheet.
$('#Spreadsheet').ejSpreadsheet({ 
tabClick: function (args){}
});
</script>

{% endhighlight %}

### tabSelect
{:#events:tabselect}

Triggered when select the ribbon tab.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Arguments when tabSelect event is triggered. 
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">activeIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Returns the active tab index.</td>
</tr>
<tr>
<td class="name">activeHeader</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns active tab header element.</td>
</tr>
<tr>
<td class="name">prevActiveHeader</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Returns previous active tab header element.</td>
</tr>
<tr>
<td class="name">prevActiveIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Returns previous active tab index.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.Spreadsheet.Model"/><span class="param-type">object</span></td>
<td class="description">Returns the Spreadsheet model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Returns the cancel option value.</td>
</tr>
</tbody>
</table>
</td></tr>
</tbody>
</table>

#### Example

{% highlight html %}
<div id="Spreadsheet"></div> 
<script>
// tabSelect event for Spreadsheet.
$('#Spreadsheet').ejSpreadsheet({ 
tabSelect: function (args){}
});
</script>

{% endhighlight %}