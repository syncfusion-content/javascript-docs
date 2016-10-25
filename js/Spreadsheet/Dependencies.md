---
title: Essential JavaScript Spreadsheet dependencies
description: Listed Spreadsheet internal and external dependencies
platform: JS
control: Spreadsheet
documentation: ug
---
# Dependencies

The Spreadsheet have the following list of external dependencies.

* [`jQuery`](http://jquery.com "jQuery") 1.7.1 and later versions.

* [`jsRender`](https://github.com/borismoore/jsrender "jsRender") - to render the templates.

* [`jQuery.validate`](https://github.com/jzaefferer/jquery-validation "jQuery.validate") - to support validation in editing and dialog inputs.


And the internal dependencies are tabulated below.

<table>
    <tr>
        <th>
            File
        </th>
        <th>
            Description/Usage
        </th>
    </tr>
    <tr>
        <td>
            ej.core.min.js
        </td>
        <td>
            Must be referred always before using all the JS controls
        </td>
    </tr>
    <tr>
        <td>
            ej.data.min.js
        </td>
        <td>
            Used to handle data operation and should be used while binding data to JS controls
        </td>
    </tr>
    <tr>
        <td>
            ej.scroller.min.js
        </td>
        <td>
            Used to handle scrolling operation in all JS controls
        </td>
    </tr>
    <tr>
        <td>
            ej.spreadsheet.common.min.js
        </td>
        <td>
            Spreadsheet's main file
        </td>
    </tr>
    <tr>
        <td>
            ej.spreadsheet.selection.min.js
        </td>
        <td>
            Should be referred when using selection in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.spreadsheet.filter.min.js
        </td>
        <td>
            Should be referred when using filtering in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.spreadsheet.ribbon.min.js
        </td>
        <td>
            Should be referred when ribbon is enabled in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.spreadsheet.freezepane.min.js
        </td>
        <td>
            Should be referred when using freeze pane options in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.spreadsheet.math.min.js
        </td>
        <td>
            Must be referred and used for Spreadsheet common calculation
        </td>
    </tr>
    <tr>
        <td>
            ej.spreadsheet.resizing.min.js
        </td>
        <td>
            Should be referred when using resizing in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.spreadsheet.editing.min.js
        </td>
        <td>
            Should be referred when using editing in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.spreadsheet.validation.min.js
        </td>
        <td>
            Should be referred when using data validation in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.spreadsheet.comments.min.js
        </td>
        <td>
            Should be referred when using comments in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.spreadsheet.dragFill.min.js
        </td>
        <td>
            Should be referred when using auto fill in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.spreadsheet.cellNavigation.min.js
        </td>
        <td>
            Should be referred when using keyboard navigation in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.spreadsheet.cellFormatting.min.js
        </td>
        <td>
            Should be referred when using cell formatting in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.spreadsheet.cFormat.min.js
        </td>
        <td>
            Should be referred when using conditional formatting in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.spreadsheet.clipboard.min.js
        </td>
        <td>
            Should be referred when using clipboard options in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.spreadsheet.contextmenu.min.js
        </td>
        <td>
            Should be referred when using context menu in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.spreadsheet.sorting.min.js
        </td>
        <td>
            Should be referred when using sorting in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.spreadsheet.dragAndDrop.min.js
        </td>
        <td>
            Should be referred when using drag and drop in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.spreadsheet.findnreplace.min.js
        </td>
        <td>
            Should be referred when using find and replace option in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.spreadsheet.exporting.min.js
        </td>
        <td>
            Should be referred when using exporting in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.spreadsheet.shape.min.js
        </td>
        <td>
            Should be referred when using picture and chart in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.spreadsheet.chart.min.js
        </td>
        <td>
            Should be referred when using chart in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.spreadsheet.print.min.js
        </td>
        <td>
            Should be referred when using print option in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.spreadsheet.scroller.min.js
        </td>
        <td>
            Should be referred when using scrolling in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.spreadsheet.pivot.min.js
        </td>
        <td>
            Should be referred when using pivot table in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.spreadsheet.formatCellDlg.min.js
        </td>
        <td>
            Should be referred when using format cell dialog in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.spreadsheet.cellType.min.js
        </td>
        <td>
            Should be referred when using cell type in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.grid.min.js
        </td>
        <td>
            Used this control for Name Manager option in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.pager.min.js
        </td>
        <td>
            Must be referred and used for paging option in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.waitingpopup.min.js
        </td>
        <td>
            Should be referred while importing files in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.autocomplete.min.js
        </td>
        <td>
            Should be referred when editing is enabled in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.chart.min.js
        </td>
        <td>
            Used this control for chart option is enabled in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.ribbon.min.js
        </td>
        <td>
            These files are used when ribbon option is enabled in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.button.min.js
        </td>
        <td rowspan="17">
            These files are used while enable the cellFormatting, import and drag and drop feature in the Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.checkbox.min.js
        </td>
    </tr>
    <tr>
        <td>
            ej.radiobutton.min.js
        </td>
    </tr>
    <tr>
        <td>
            ej.dropdownlist.min.js
        </td>
    </tr>
    <tr>
        <td>
            ej.listbox.min.js
        </td>
    </tr>
    <tr>
        <td>
            ej.editor.min.js
        </td>
    </tr>
    <tr>
        <td>
            ej.menu.min.js
        </td>
    </tr>
    <tr>
        <td>
            ej.colorpicker.min.js
        </td>
    </tr>
    <tr>
        <td>
            ej.slider.min.js
        </td>
    </tr>
    <tr>
        <td>
            ej.splitbutton.min.js
        </td>
    </tr>
    <tr>
        <td>
            ej.togglebutton.min.js
        </td>
    </tr>
    <tr>
        <td>
            ej.toolbar.min.js
        </td>
    </tr>
    <tr>
        <td>
            ej.tab.min.js
        </td>
    </tr>
    <tr>
        <td>
            ej.uploadbox.min.js
        </td>
    </tr>
    <tr>
        <td>
            ej.draggable.min.js
        </td>
    </tr>
    <tr>
        <td>
            ej.datepicker.min.js
        </td>
    </tr>
    <tr>
        <td>
            ej.tooltip.min.js
        </td>
        <td>
        </td>
    </tr>
    <tr>
        <td>
            ej.calculate.min.js
        </td>
        <td>
            Must be referred and used for formula in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.dialog.min.js
        </td>
        <td>
            Must be referred since dialog is used in various features in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.treeview.min.js
        </td>
        <td>
            Should be referred when Hyperlink options is enabled in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.excelfilter.min.js
        </td>
        <td>
            Should be referred when filtering is enabled in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.pivotgrid.min.js
        </td>
        <td rowspan="2">
            Should be referred when pivot table is enabled in Spreadsheet
        </td>
    </tr>
    <tr>
        <td>
            ej.pivotschemadesigner.min.js
        </td>              
    </tr>
    <tr>
        <td>
            ej.globalize.min.js
        </td>
        <td>
            It is referred when using localization in Spreadsheet
        </td>        
    </tr>
</table>
