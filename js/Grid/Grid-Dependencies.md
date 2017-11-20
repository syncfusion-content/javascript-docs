---
layout: post
title: Dependencies for Grid widget rendered in Syncfusion Essential JS
description: What is the need for Grid rendering
platform: js
control: Grid
documentation: ug
api: /api/js/ejgrid
---
# Grid Dependencies

The `ej.web.all.js` is a bundle of all **Essential****JavaScript** controls. If you use `ej.web.all.js` in your application, you can leave this section or else you can try to render `ejgrid` in your application using **ej.grid.min.js** file. You can refer to the following frameworks and controls in your project.

_Grid Dependency_ 

<table>
<tr>
<th>
<b>File                          </b></th><th>
<b>Description/Usage</b></th></tr>
<tr>
<td>
ej.core.min.js</td><td>
Must be referred always before using all the JS controls.</td></tr>
<tr>
<td>
ej.data.min.js</td><td>
Used to handle `dataManager` operation and should be used while binding data to JS controls.</td></tr>
<tr>
<td>
ej.grid.min.js</td><td>
Should be referred when using <b>Grid</b> control.</td></tr>
<tr>
<td>
ej.pager.min.js</td><td>
Should be referred when using paging in grid.  </td></tr>
<tr>
<td>
ej.scroller.min.js</td><td>
Should be referred when using scrolling in grid.  </td></tr>
<tr>
<td>
ej.waitingpopup.min.js</td><td>
Should be referred when using the remote data binding in grid. The waiting popup will show while requesting the server for data.</td></tr>
<tr>
<td>
ej.gridresize.min.js</td><td>
Need to refer when using the resizing feature in grid.</td></tr>
<tr>
<td>
ej.dropdownlist.min.js</td><td rowspan = "8">
  These files are used while enable Editing and Filtering feature in grid.</td></tr>
<tr>
<td>
ej.dialog.min.js</td></tr>
<tr>
<td>
ej.button.min.js</td></tr>
<tr>
<td>
ej.autocomplete.min.js</td></tr>
<tr>
<td>
ej.datepicker.min.js</td></tr>
<tr>
<td>
ej.datetimepicker.min.js</td></tr>
<tr>
<td>
ej.checkbox.min.js</td></tr>
<tr>
<td>
ej.editor.min.js</td></tr>
</table>


