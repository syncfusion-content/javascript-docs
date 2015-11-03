---
layout: post
title: Globalization and localization
description: Globalization and localization
platform: js
control: Grid
documentation: ug
---
# Globalization and localization

## Localization

All text in Grid can be localized using `ej.Grid.locale` object. Please find the table with list of properties and its value in locale object.

<table>
<tr>
<td>
Locale key words <br/><br/></td><td>
Text<br/><br/></td></tr>
<tr>
<td>
EmptyRecord<br/><br/></td><td>
No records to display<br/><br/></td></tr>
<tr>
<td>
GroupDropArea<br/><br/></td><td>
Drag a column header here to group its column<br/><br/></td></tr>
<tr>
<td>
DeleteOperationAlert<br/><br/></td><td>
No records selected for delete operation<br/><br/></td></tr>
<tr>
<td>
EditOperationAlert<br/><br/></td><td>
No records selected for edit operation<br/><br/></td></tr>
<tr>
<td>
SaveButton<br/><br/></td><td>
Save<br/><br/></td></tr>
<tr>
<td>
OkButton<br/><br/></td><td>
OK<br/><br/></td></tr>
<tr>
<td>
CancelButton<br/><br/></td><td>
Cancel<br/><br/></td></tr>
<tr>
<td>
EditFormTitle<br/><br/></td><td>
Details of<br/><br/></td></tr>
<tr>
<td>
AddFormTitle<br/><br/></td><td>
Add New Record<br/><br/></td></tr>
<tr>
<td>
Notactionkeyalert<br/><br/></td><td>
This Key-Combination is not available <br/><br/></td></tr>
<tr>
<td>
Keyconfigalerttext<br/><br/></td><td>
This Key-Combination has already been assigned to<br/><br/></td></tr>
<tr>
<td>
GroupCaptionFormat<br/><br/></td><td>
{{:headerText}}: {{:key}} - {{:count}} {{if count == 1 }} item {{else}} items {{/if}}<br/><br/></td></tr>
<tr>
<td>
BatchSaveConfirm<br/><br/></td><td>
Are you sure you want to save changes?<br/><br/></td></tr>
<tr>
<td>
BatchSaveLostChanges<br/><br/></td><td>
Unsaved changes will be lost. Are you sure you want to continue?<br/><br/></td></tr>
<tr>
<td>
ConfirmDelete<br/><br/></td><td>
Are you sure you want to Delete Record?<br/><br/></td></tr>
<tr>
<td>
PagerInfo<br/><br/></td><td>
{0} of {1} pages ({2} items)<br/><br/></td></tr>
<tr>
<td>
FrozenColumnsViewAlert<br/><br/></td><td>
Frozen columns should be in grid view area<br/><br/></td></tr>
<tr>
<td>
FrozenColumnsScrollAlert<br/><br/></td><td>
Enable allowScrolling while using frozen Columns<br/><br/></td></tr>
<tr>
<td>
FrozenNotSupportedException<br/><br/></td><td>
Frozen Columns and Rows are not supported for Grouping, Row Template, Detail Template, Hierarchy Grid and Batch Editing<br/><br/></td></tr>
<tr>
<td>
Add<br/><br/></td><td>
Add<br/><br/></td></tr>
<tr>
<td>
Edit<br/><br/></td><td>
Edit<br/><br/></td></tr>
<tr>
<td>
Delete<br/><br/></td><td>
Delete<br/><br/></td></tr>
<tr>
<td>
Update<br/><br/></td><td>
Update<br/><br/></td></tr>
<tr>
<td>
Cancel<br/><br/></td><td>
Cancel<br/><br/></td></tr>
<tr>
<td>
Done<br/><br/></td><td>
Done<br/><br/></td></tr>
<tr>
<td>
Columns<br/><br/></td><td>
Columns<br/><br/></td></tr>
<tr>
<td>
PrintGrid<br/><br/></td><td>
Print<br/><br/></td></tr>
<tr>
<td>
ExcelExport<br/><br/></td><td>
Excel Export<br/><br/></td></tr>
<tr>
<td>
WordExport<br/><br/></td><td>
Word Export<br/><br/></td></tr>
<tr>
<td>
PdfExport<br/><br/></td><td>
PDF Export<br/><br/></td></tr>
<tr>
<td>
StringMenuOptions<br/><br/></td><td>
[<br/><br/>{text: "StartsWith",value: "StartsWith"},<br/><br/>{text: "EndsWith",value: "EndsWith"},<br/><br/>{text: "Contains",value: "Contains"},<br/><br/>{text: "Equal",value: "Equal"},<br/><br/>{text: "NotEqual",value: "NotEqual"}<br/><br/>]<br/><br/></td></tr>
<tr>
<td>
NumberMenuOptions<br/><br/></td><td>
[<br/><br/>{text: "LessThan",value: "LessThan"},<br/><br/>{text: "GreaterThan",value: "GreaterThan"},<br/><br/>{text: "LessThanOrEqual",value: "LessThanOrEqual"},<br/><br/>{text: "GreaterThanOrEqual",value: "GreaterThanOrEqual"},<br/><br/>{text: "Equal",value: "Equal"},<br/><br/>{text: "NotEqual",value: "NotEqual"}]<br/><br/></td></tr>
<tr>
<td>
PredicateAnd<br/><br/></td><td>
AND<br/><br/></td></tr>
<tr>
<td>
PredicateOr<br/><br/></td><td>
OR<br/><br/></td></tr>
<tr>
<td>
Filter<br/><br/></td><td>
Filter<br/><br/></td></tr>
<tr>
<td>
FilterMenuCaption<br/><br/></td><td>
Filter Value<br/><br/></td></tr>
<tr>
<td>
FilterbarTitle<br/><br/></td><td>
's filter bar cell<br/><br/></td></tr>
<tr>
<td>
MatchCase<br/><br/></td><td>
Match Case<br/><br/></td></tr>
<tr>
<td>
Clear<br/><br/></td><td>
Clear<br/><br/></td></tr>
<tr>
<td>
ResponsiveFilter<br/><br/></td><td>
Filter<br/><br/></td></tr>
<tr>
<td>
ResponsiveSorting<br/><br/></td><td>
Sort<br/><br/></td></tr>
<tr>
<td>
Search<br/><br/></td><td>
Search<br/><br/></td></tr>
<tr>
<td>
DatePickerWaterMark<br/><br/></td><td>
Select date<br/><br/></td></tr>
<tr>
<td>
EmptyDataSource<br/><br/></td><td>
DataSource must not be empty at initial load since columns are generated from dataSource in AutoGenerate Column Grid<br/><br/></td></tr>
<tr>
<td>
True<br/><br/></td><td>
True<br/><br/></td></tr>
<tr>
<td>
False<br/><br/></td><td>
False<br/><br/></td></tr>
<tr>
<td>
UnGroup<br/><br/></td><td>
Click here to ungroup<br/><br/></td></tr>
<tr>
<td>
AddRecord<br/><br/></td><td>
Add Record<br/><br/></td></tr>
<tr>
<td>
EditRecord<br/><br/></td><td>
Edit Record<br/><br/></td></tr>
<tr>
<td>
DeleteRecord<br/><br/></td><td>
Delete Record<br/><br/></td></tr>
<tr>
<td>
Save<br/><br/></td><td>
Save<br/><br/></td></tr>
<tr>
<td>
Grouping<br/><br/></td><td>
Grouping<br/><br/></td></tr>
<tr>
<td>
Ungrouping<br/><br/></td><td>
Ungrouping<br/><br/></td></tr>
<tr>
<td>
SortInAscendingOrder<br/><br/></td><td>
Sort In Ascending Order<br/><br/></td></tr>
<tr>
<td>
SortInDescendingOrder<br/><br/></td><td>
Sort In Descending Order<br/><br/></td></tr>
<tr>
<td>
NextPage<br/><br/></td><td>
Next Page<br/><br/></td></tr>
<tr>
<td>
PreviousPage<br/><br/></td><td>
Previous Page<br/><br/></td></tr>
<tr>
<td>
FirstPage<br/><br/></td><td>
First Page<br/><br/></td></tr>
<tr>
<td>
LastPage<br/><br/></td><td>
Last Page<br/><br/></td></tr>
</table>


{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
ej.Grid.locale["de-DE"] = {
EmptyRecord: "Keine Aufzeichnungen angezeigt",
GroupDropArea: "Ziehen Sie eine Spaltenüberschrift hier",
DeleteOperationAlert: "Keine Einträge für Löschvorgang ausgewählt",
EditOperationAlert: "Keine Einträge für Bearbeiten Betrieb ausgewählt",
SaveButton: "Speichern",
CancelButton: "stornieren",
EditFormTitle: "Korrektur von",
GroupCaptionFormat: "{{:field}}: {{:key}} - {{:count}} {{if count == 1}}Beiträge{{else}}Beiträges{{/if}}",
UnGroup: "Klicken Sie hier, um die Gruppierung aufheben"
};
ej.Pager.locale["de-DE"] = {
pagerInfo: "{0} von {1} Seiten ({2} Beiträge)",
firstPageTooltip: "Zur ersten Seite",
lastPageTooltip: "Zur letzten Seite",
nextPageTooltip: "Zur nächsten Seite",
previousPageTooltip: "Zurück zur letzten Seite",
nextPagerTooltip: "Zum nächsten Pager",
previousPagerTooltip: "Zum vorherigen Pager"
};
$("#Grid").ejGrid({
// the datasource "window.gridData" is referred from jsondata.min.js
dataSource: window.gridData,
locale: "de-DE",
allowPaging: true,
allowGrouping: true,
groupSettings: {
enableDropAreaAnimation: false
},
columns:
	[
		{ field: "OrderID", headerText: "Order ID", isPrimaryKey: true, textAlign: ej.TextAlign.Right, width: 75 },
		{ field: "CustomerID", headerText: "Customer ID", width: 95 },
		{ field: "EmployeeID", headerText: "Employee ID", textAlign: ej.TextAlign.Right, width: 95 },
		{ field: "Freight", headerText: "Freight", textAlign: ej.TextAlign.Right, width: 75, format: "{0:C}" },
		{ field: "ShipCity", headerText: "Ship City", width: 80 }
	]
});

</script>



{% endhighlight %}

![](Globalizationandlocalization._images/Globalizationandlocalization._img1.png)


I> You need to change pager locale in `ej.Pager.locale` object.


## Excel-Filter Localization


All text in Grid can be localized using `ej.ExcelFilter.locale` object. Please find the table with list of properties and its value in locale object.

<table>
<tr>
<td>
Locale key words <br/><br/></td><td>
Text<br/><br/></td></tr>
<tr>
<td>
SortNoSmaller<br/><br/></td><td>
Sort Smallest to Largest<br/><br/></td></tr>
<tr>
<td>
SortNoLarger<br/><br/></td><td>
Sort Largest to smallest<br/><br/></td></tr>
<tr>
<td>
SortTextAscending<br/><br/></td><td>
Sort A to Z<br/><br/></td></tr>
<tr>
<td>
SortTextDescending<br/><br/></td><td>
Sort Z to A<br/><br/></td></tr>
<tr>
<td>
SortDateOldest<br/><br/></td><td>
Sort By Oldest<br/><br/></td></tr>
<tr>
<td>
SortDateNewest<br/><br/></td><td>
Sort By Newest<br/><br/></td></tr>
<tr>
<td>
SortByColor<br/><br/></td><td>
Sort By Color<br/><br/></td></tr>
<tr>
<td>
SortByCellColor<br/><br/></td><td>
Sort By Cell Color<br/><br/></td></tr>
<tr>
<td>
SortByFontColor:<br/><br/></td><td>
Sort By Font Color:<br/><br/></td></tr>
<tr>
<td>
FilterByColor<br/><br/></td><td>
Filter By Color<br/><br/></td></tr>
<tr>
<td>
SortColorOptions:<br/><br/></td><td>
[{ id: 1, background:"#FFFFFF"}, {id: 2, background:"#5EABDA"}],<br/><br/></td></tr>
<tr>
<td>
CustomSort<br/><br/></td><td>
Custom Sort<br/><br/></td></tr>
<tr>
<td>
FilterColorOptions<br/><br/></td><td>
{ id: 1, background:"#FFFFFF"}, {id: 2, background:"#5EABDA"}],<br/><br/></td></tr>
<tr>
<td>
FilterByCellColor<br/><br/></td><td>
Filter By Cell Color<br/><br/></td></tr>
<tr>
<td>
FilterByFontColor<br/><br/></td><td>
Filter By Font Color<br/><br/></td></tr>
<tr>
<td>
ClearFilter<br/><br/></td><td>
Clear Filter<br/><br/></td></tr>
<tr>
<td>
NumberFilter<br/><br/></td><td>
Number Filter<br/><br/></td></tr>
<tr>
<td>
TextFilter<br/><br/></td><td>
Text Filter<br/><br/></td></tr>
<tr>
<td>
DateFilter<br/><br/></td><td>
Date Filter<br/><br/></td></tr>
<tr>
<td>
StringMenuOptions<br/><br/></td><td>
[<br/><br/>{ text:"Equal",value:"equal"},<br/><br/>{ text:"Not Equal", value:"notequal"},<br/><br/>{ text:"Starts With",value:"startswith"}, <br/><br/>{ text:"Ends With",value:"endswith"},<br/><br/>{ text:"Contains",value:"contains"}, <br/><br/>{text:"Custom Filter", value:"customfilter"}],<br/><br/></td></tr>
<tr>
<td>
NumberMenuOptions<br/><br/></td><td>
[<br/><br/>{text:"Equal",value:"equal"}, <br/><br/>{text:"Not Equal",value:"notequal"}, <br/><br/>{ text:"Less Than",value:"lessthan"}, <br/><br/>{text:"Less Than Or Equal", value:"lessthanorequal"}, <br/><br/>{text:"Greater Than",value:"greaterthan"},<br/><br/>{ text:"Greater Than Or Equal", value:"greaterthanorequal"}, <br/><br/>{ text:"Between",value:"between"},<br/><br/>{ text:"Custom Filter", value:"customfilter"}]<br/><br/></td></tr>
<tr>
<td>
DateMenuOptions<br/><br/></td><td>
[<br/><br/>{ text:"Equal", value:"equal"}<br/><br/>, {text:"Not Equal",value:"notequal"},<br/><br/>{text:"Less Than",>value:"lessthan"}, <br/><br/>{text:"Less Than Or Equal",value:"lessthanorequal"}, <br/><br/>{text:"Greater Than",value:"greaterthan"},<br/><br/>{text:"Greater Than Or Equal", value:"greaterthanorequal"}, <br/><br/>{ text:"Between",value:"between"},<br/><br/>{ text:"Custom Filter", value:"customfilter"}]<br/><br/></td></tr>
<tr>
<td>
Top10MenuOptions<br/><br/></td><td>
[{ <br/><br/>text:"Top", <br/><br/>value:"top"<br/><br/>},<br/><br/>{<br/><br/>text:"Bottom", <br/><br/>value:"bottom"<br/><br/>}]<br/><br/></td></tr>
<tr>
<td>
title<br/><br/></td><td>
Custom Filter<br/><br/></td></tr>
<tr>
<td>
PredicateOr<br/><br/></td><td>
OR<br/><br/></td></tr>
<tr>
<td>
Ok<br/><br/></td><td>
Ok<br/><br/></td></tr>
<tr>
<td>
MathCase<br/><br/></td><td>
Match Case<br/><br/></td></tr>
<tr>
<td>
Cancel<br/><br/></td><td>
Cancel<br/><br/></td></tr>
<tr>
<td>
NoResult<br/><br/></td><td>
No Match Found<br/><br/></td></tr>
<tr>
<td>
CheckBoxStatusMsg<br/><br/></td><td>
Not all items showing<br/><br/></td></tr>
<tr>
<td>
DatePickerWaterMark<br/><br/></td><td>
Select date<br/><br/></td></tr>
<tr>
<td>
True<br/><br/></td><td>
True<br/><br/></td></tr>
<tr>
<td>
False<br/><br/></td><td>
False<br/><br/></td></tr>
<tr>
<td>
Search<br/><br/></td><td>
Search<br/><br/></td></tr>
<tr>
<td>
DatePickerWaterMark<br/><br/></td><td>
Select date<br/><br/></td></tr>
<tr>
<td>
EmptyDataSource<br/><br/></td><td>
DataSource must not be empty at initial load since columns are generated from dataSource in AutoGenerate Column Grid<br/><br/></td></tr>
<tr>
<td>
True<br/><br/></td><td>
True<br/><br/></td></tr>
<tr>
<td>
False<br/><br/></td><td>
False<br/><br/></td></tr>
</table>
Please find the code

{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
  ej.ExcelFilter.locale["de-DE"] = {
      SortNoSmaller: "Art Anzahl kleiner",
      SortNoLarger: "Art Anzahl größer",
      SortTextAscending: "Sortieren aufsteigend Text",
      SortTextDescending: "Sortieren absteigend Text",
      SortDateOldest: "Sortieren Datum Älteste",
      SortDateNewest: "Datum sortieren Neueste",
      ClearFilter: "Filter löschen",
      DateFilter: "Datum Filter"
  }
  $("#Grid").ejGrid({
      // the datasource "window.gridData" is referred from jsondata.min.js
      dataSource: window.gridData,
      locale: "de-DE",
      allowPaging: true,
      allowFiltering: true,
       filterSettings: { filterType: "excel"},
      columns:
          [
              { field: "OrderID", headerText: "Order ID", isPrimaryKey: true, textAlign: ej.TextAlign.Right, width: 75 },
              { field: "CustomerID", headerText: "Customer ID", width: 95 },
              {field:"OrderDate", headerText:"Order Date", width:100,format:"{0:MM/dd/yyyy}"},
              { field: "EmployeeID", headerText: "Employee ID", textAlign: ej.TextAlign.Right, width: 95 },
              { field: "Freight", headerText: "Freight", textAlign: ej.TextAlign.Right, width: 75, format: "{0:C}" },
              { field: "ShipCity", headerText: "Ship City", width: 80 }
          ]
  });
</script>



{% endhighlight %}

![](Globalizationandlocalization._images/Globalizationandlocalization._img2.png)


## Globalization

[`jQuery.globalize`](https://github.com/jquery/globalize/tree/v0.1.1) library is used to globalize numeric values in Grid control using [`format`](http://help.syncfusion.com/js/api/ejgrid#members:columns-format "format") property in [`columns`](http://help.syncfusion.com/js/api/ejgrid#members:columns "columns"). Globalize values will be automatically used when [`locale`](http://help.syncfusion.com/js/api/ejgrid#members:locale "locale") property is set with locale string value for example `en-US`.

{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
  $("#Grid").ejGrid({
      // the datasource "window.gridData" is referred from jsondata.min.js
      dataSource: window.gridData,
      locale: "de-DE",
      columns:
          [
              { field: "OrderID", headerText: "Order ID", textAlign: ej.TextAlign.Right, width: 75 },
              { field: "CustomerID", headerText: "Customer ID", width: 95 },
              { field: "EmployeeID", headerText: "Employee ID", textAlign: ej.TextAlign.Right, width: 95 },
              { field: "Freight", headerText: "Freight", textAlign: ej.TextAlign.Right, width: 75, format: "{0:C}" },
              { field: "ShipCity", headerText: "Ship City", width: 80 }
          ]
  });
</script>



{% endhighlight %}

![](Globalizationandlocalization._images/Globalizationandlocalization._img3.png)

I> In the above example, you need to use `globalize.culture.de-DE` script file to globalize values. 

{% seealso %} [localization](http://helpjs.syncfusion.com/js/localization) {% endseealso %}

## Right to Left – RTL

By default, Grid render its text and layout from left to right. To customize Grid’s direction, you can change direction from LTR to RTL by using [`enableRTL`](http://help.syncfusion.com/js/api/ejgrid#members:enablertl "enableRTL") as true.

{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
  $("#Grid").ejGrid({
      // the datasource "window.gridData" is referred from jsondata.min.js
      dataSource: window.gridData,
      enableRTL: true,
      allowPaging: true,
      columns:
          [
              { field: "OrderID", headerText: "Order ID", textAlign: ej.TextAlign.Right, width: 120 },
              { field: "CustomerID", headerText: 'Customer ID', width: 120 },
              { field: "EmployeeID", headerText: 'Employee ID', textAlign: ej.TextAlign.Right, width: 120 },
              { field: "Freight", headerText: 'Freight', textAlign: ej.TextAlign.Right, width: 120, format: "{0:C2}", },
              { field: "ShipCity", headerText: 'Ship City', textAlign: ej.TextAlign.Right, width: 120 }
          ]
  });
</script>



{% endhighlight %}

![](Globalizationandlocalization._images/Globalizationandlocalization._img4.png)


