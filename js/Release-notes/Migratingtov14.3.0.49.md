---
title : Essential Studio 2016 Vol3 Migration document
description : Essential Studio 2016 Migration document
platform : js
documentation: ug
keywords: migration, upgradation, upgrade-changes, vol3-changes
---

# Common Changes

* To avoid conflict between ej.web.all and ej.widgets.all JavaScript, theme and TypeScript files we are deprecating the below ej.widgets.all files and those files are no longer shipped along with our next Essential Studio release

<table class="params">
<tbody>
<tr>
<td>ej.widgets.all.min.css</td>
<td>ej.web.all.min.css</td>
</tr>
<tr>
<td> ej.widgets.all.min.js </td>
<td>ej.web.all.min.js</td>
</tr>
<tr>
<td>ej.widgets.all.d.ts</td>
<td>ej.web.all.d.ts</td>
</tr>
</tbody>
</table>

*  To optimize the loading process and reduce the package size, global files (376 culture files) present in the i18n directory has been removed from JavaScript package and it contains frequently used culture files only.

                * ej.culture.ar-AE.min.js
                * ej.culture.de-DE.min.js
                * ej.culture.en-US.min.js
                * ej.culture.es-ES.min.js
                * ej.culture.fr-FR.min.js
                * ej.culture.vi-VN.min.js
                * ej.culture.zh-CN.min.js

 However based on the application need, global culture files can be downloaded from the  [GitHuB](https://github.com/syncfusion/JavaScript-Widgets/tree/master/Scripts/ej) location.
 
 * 	localetexts directory has been renamed to l10n as per localization standard.  
 
<table class="params">
<tbody>
<tr>
<td>localetexts</td>
<td>l10n</td>
</tr>
</tbody>
</table>

 * Proper naming convention is implemented in TypeScript definition file for Syncfusion JavaScript control’s Array properties to ensure unique naming style followed throughout all the controls. 

        For example, columns: Array<Columns> renamed as columns: Array<Column>.

 * jQuery easing external dependency has been removed from our JavaScript package.
 
## ejButton
 
**Class name**

Custom font icons are not applied due to e-icon class overrides it. So e-icon class has been removed from ejButton source. Display EJ icons as prefix/suffix icon by using their corresponding class names along with e-icon class (e-icon icon_name).

<table class="params">
<tbody>
<tr>
<td>e-icon</td>
<td>e-icon icon_name</td>
</tr>
</tbody>
</table>


## ejChart
 
To have a better appearance in mobile, we have changed the font size for the chart title, axis title, axis label and data label. 

<table class="params">
<thead>
<tr>
<th>Property Name</th>
<th>Default size</th>
<th>New Default size</th>
</tr>
</thead>
<tbody>
<tr>
<td>Rounded corner rx and  ry values for  crosshair</td>
<td>0</td>
<td>3</td>
</tr>
<tr>
<td>title.font.size</td>
<td>20px</td>
<td>16px</td>
</tr>
<tr>
<td>primaryXAxis.title.font.size</td>
<td>16px</td>
<td>14px</td>
</tr>
<tr>
<td>primaryYAxis.title.font.size</td>
<td>16px</td>
<td>14px</td>
</tr>
<tr>
<td>primaryXAxis.font.size</td>
<td>13px</td>
<td>11px</td>
</tr>
<tr>
<td>primaryYAxis.font.size</td>
<td>13px</td>
<td>11px</td>
</tr>
<tr>
<td>series.marker.dataLabel.font.size</td>
<td>12px</td>
<td>11px</td>
</tr>
</tbody>
</table>

## ejFileExplorer

**select** event is triggered while unselect any items in grid/tile view issue has been fixed and now we have provided **unselect** event while unselect any items in grid/tile view.


##  ejGantt

Now the editor type of the duration column has been changed, to support displaying duration units in the project such as days, hours and minutes. Hence duration column will be displayed along with duration unit, with days as default duration unit.


**Editor type of the duration column**


<table class="params">
<tbody>
<tr>
<td>numeric </td>
<td>string </td>
</tr>
</tbody>
</table>

Now the editor type for the duration and predecessor offset fields in the add and edit dialogs has been changed from numeric to string type, to support displaying duration units in the project such as days, hours and minutes.

<table class="params">
<tbody>
<tr>
<td>numeric </td>
<td>string </td>
</tr>
</tbody>
</table>


## ejGrid

Grid height responsiveness will works only if the scrollSettings->height property is set as ‘100%’

Restore old resizing behavior, in which adjusting all the other columns while resizing a particular column

**Default column resizing mode**

<table class="params">
<tbody>
<tr>
<td>Normal </td>
<td>NextColumn </td>
</tr>
</tbody>
</table>

While referring individual files, it is essential to include ej.tooltip.min.js file in project for rendering toolbar in Grid.


## ejkanban

* Kanban card layout structure has been changed.

* To avoid multiple internal processing for handling UI related changes on the Kanban control while doing priority sorting or filtering with drag and drop, complete refresh will be taken place now, instead of updating the dropped cards alone.

**Property**

To improve the user experience, we are getting the Context Menu item as string array instead of nested properties

<table class="params">
<tbody>
<tr>
<td>menuItem property removed from contextMenuSettings.menuItems </td>
<td>menuItems(string of array) </td>
</tr>
</tbody>
</table>

**Methods**

Divided as module based structure based on features and corresponding methods are changed.

<table class="params">
<tbody>
<tr>
<td>expandAll </td>
<td>KanbanSwimlane.expandAll </td>
</tr>
<tr>
<td>collapseAll </td>
<td>KanbanSwimlane.collapseAll </td>
</tr>
<tr>
<td>toggleSwimlane </td>
<td>KanbanSwimlane.toggle</td>
</tr>
<tr>
<td>clearSelection </td>
<td>KanbanSelection.clear</td>
</tr>
<tr>
<td>clearSearch </td>
<td>KanbanFilter.clearSearch</td>
</tr>
<tr>
<td>searchCards </td>
<td>KanbanFilter.searchCards </td>
</tr>
<tr>
<td>clearFilter  </td>
<td>KanbanFilter.clearFilter</td>
</tr>
<tr>
<td>filterCards </td>
<td>KanbanFilter.filter</td>
</tr>
</tbody>
</table>

## ejPivotChart

We have started to support both OLAP and Relational data sources in a single widget and so we have renamed our controls from “Olap” to “Pivot” (prefix term). Due to this change we have renamed our assembly as well from “Syncfusion.EJ.Olap” to “Syncfusion.EJ.Pivot”. 

Note: Widget name, namespace, class name and enumeration were changed in prior release itself

**Assembly name**

<table class="params">
<tbody>
<tr>
<td>Syncfusion.EJ.Olap </td>
<td>Syncfusion.EJ.Pivot </td>
</tr>
</tbody>
</table>


## ejPivotClient

We have started to support both OLAP and Relational data sources in Client widget and so we have renamed our controls from “OlapClient” to “PivotClient”. Due to this change we have renamed our widget name, assembly name, namespace, class name and enumeration. 

**Assembly name**

<table class="params">
<tbody>
<tr>
<td>Syncfusion.EJ.Olap </td>
<td>Syncfusion.EJ.Pivot </td>
</tr>
</tbody>
</table>

**Widget name**

<table class="params">
<tbody>
<tr>
<td>ejOlapClient</td>
<td>ejPivotClient </td>
</tr>
</tbody>
</table>


**Class name**

<table class="params">
<tbody>
<tr>
<td>OlapClient</td>
<td>PivotClient </td>
</tr>
<tr>
<td>ej.olap.OlapClient.Locale</td>
<td>ej.PivotClient.Locale </td>
</tr>
</tbody>
</table>


**Namespace**

<table class="params">
<tbody>
<tr>
<td>ej.olap.OlapClient</td>
<td>ej.PivotClient </td>
</tr>
</tbody>
</table>

**Enumeration**

<table class="params">
<tbody>
<tr>
<td>ej.olap.OlapClient</td>
<td>ej.PivotClient </td>
</tr>
</tbody>
</table>

## ejPivotGauge

We have started to support both OLAP and Relational data sources in a single widget and so we have renamed our controls from “Olap” to “Pivot” (prefix term). Due to this change we have renamed our assembly as well from “Syncfusion.EJ.Olap” to “Syncfusion.EJ.Pivot”. 

Note: Widget name, namespace, class name and enumeration were changed in prior release itself. 

**Assembly name**

<table class="params">
<tbody>
<tr>
<td>Syncfusion.EJ.Olap</td>
<td>Syncfusion.EJ.Pivot</td>
</tr>
</tbody>
</table>


## ejPivotGrid

We have started to support both OLAP and Relational data sources in a single widget and so we have renamed our controls from “Olap” to “Pivot” (prefix term). Due to this change we have renamed our assembly as well from “Syncfusion.EJ.Olap” to “Syncfusion.EJ.Pivot”. 

Note: Widget name, namespace, class name and enumeration were changed in prior release itself. 


**Assembly name**

<table class="params">
<tbody>
<tr>
<td>Syncfusion.EJ.Olap</td>
<td>Syncfusion.EJ.Pivot</td>
</tr>
</tbody>
</table>

## ejPivotTreeMap

We have started to support both OLAP and Relational data sources in a single widget and so we have renamed our controls from “Olap” to “Pivot” (prefix term). Due to this change we have renamed our assembly as well from “Syncfusion.EJ.Olap” to “Syncfusion.EJ.Pivot”. 

Note: Widget name, namespace, class name and enumeration were changed in prior release itself. 


**Assembly name**

<table class="params">
<tbody>
<tr>
<td>Syncfusion.EJ.Olap</td>
<td>Syncfusion.EJ.Pivot</td>
</tr>
</tbody>
</table>

## ejPivotSchemaDesigner

We have started to support both OLAP and Relational data sources in a single widget and so we have renamed our controls from “Olap” to “Pivot” (prefix term). Due to this change we have renamed our assembly as well from “Syncfusion.EJ.Olap” to “Syncfusion.EJ.Pivot”.

Note: Widget name, namespace, class name and enumeration were changed in prior release itself. 


**Assembly name**

<table class="params">
<tbody>
<tr>
<td>Syncfusion.EJ.Olap</td>
<td>Syncfusion.EJ.Pivot</td>
</tr>
</tbody>
</table>


## ejSpreadsheet

For getting started sample code optimization, default value is changed for show header.

<table class="params">
<tbody>
<thead>
<tr>
<th>Property Name</th>
<th>Default size</th>
<th>New Default size</th>
</tr>
</thead>
<tr>
<td>showHeader  </td>
<td>false</td>
<td>true</td>
</tr>
</tbody>
</table>

**Class name**

Issue with Styles class which conflict between Syncfusion.JavaScript.Models and System.Web.Optimization. 

<table class="params">
<tbody>
<tr>
<td>Syncfusion.JavaScript.Models.Styles </td>
<td>Syncfusion.JavaScript.Models.SpreadsheetCellStyles</td>
</tr>
</tbody>
</table>

## ejTreeGrid

To group the selection related APIs and to maintain the consistency with other APIs in ejTreeGrid, we have deprecated the selectionMode and selectionType properties.

**Property name**

<table class="params">
<tbody>
<tr>
<td>selectionMode </td>
<td>selectionSettings.selectionMode</td>
</tr>
<tr>
<td>selectionType </td>
<td>selectionSettings.selectionType</td>
</tr>
</tbody>
</table>






