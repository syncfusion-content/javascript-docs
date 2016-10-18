---
layout: post
title: Properties, Methods and Events of ejPivotGrid Widget
documentation: API
platform: js
keywords: ejPivotGrid, API, Essential JS PivotGrid
metaname: 
metacontent: 
---

# PivotGrid

The PivotGrid control is easily configurable, presentation-quality business control that reads OLAP data from a Microsoft SQL Server Analysis Services database, an offline cube, XML/A or relational datasource.

#### Syntax

{% highlight javascript %}

    $(element).ejPivotGrid()
{% endhighlight %}

#### Example

{% highlight html %}
 
<div id="PivotGrid1"> </div> 
 
<script>
//Create PivotGrid
$("#PivotGrid1").ejPivotGrid(...);       
</script>

{% endhighlight %}

#### Requires

* module:jQuery-1.10.2.min.js
* module:jQuery.easing.1.3.min.js
* module:ej.core.js
* module:ej.data.js
* module:ej.touch.js
* module:ej.waitingpopup.js
* module:ej.pivotgrid.js
* module:ej.pivotpager.js


## Members

### analysisMode `enum`
{:#members:analysismode}

<ts name = "ej.Pivot.AnalysisMode"/>

Sets the mode for the PivotGrid widget for binding either OLAP or relational data source.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">OLAP</td>
            <td class="description">To bind an OLAP data source to PivotGrid.</td>
        </tr>
        <tr>
            <td class="name">Relational</td>
            <td class="description">To bind a relational data source to PivotGrid.</td>
        </tr>
    </tbody>
</table>

#### Default Value: ej.PivotGrid.AnalysisMode.Olap

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({analysisMode: ej.PivotGrid.AnalysisMode.Relational });  

{% endhighlight %}


### cssClass `string`
{:#members:cssclass}

Specifies the CSS class to PivotGrid to achieve custom theme.

#### Default Value: “”

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ cssClass: "gradient-lime" });       

{% endhighlight %}

### currentReport `string`
{:#members:currentreport}

Contains the serialized OlapReport at that instant.

#### Default Value: “”

### dataSource `object`
{:#members:datasource}

Initializes the data source for the PivotGrid widget, when it functions completely on client-side.

#### Default Value: {}

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {data:value}});

{% endhighlight %}


### dataSource.catalog `string`
{:#members:datasource-catalog}

Contains the database name as string type to fetch the data from the given connection string.

#### Default Value: “”

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {catalog: value}});

{% endhighlight %}


### dataSource.columns `array`
{:#members:datasource-columns}

Lists out the items to be arranged in column section of PivotGrid.

#### Default Value: []

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {columns: itemsArray}});

{% endhighlight %}


### dataSource.columns.fieldName `string`
{:#members:datasource-columns-fieldname}

Allows the user to bind the item by using its unique name as field name.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {columns: [{ fieldName : value}]}});

{% endhighlight %}

### dataSource.columns.fieldCaption `string`
{:#members:datasource-columns-fieldcaption}

Allows the user to set the display name for an item.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {columns: [{ fieldCaption : value}]}});

{% endhighlight %}

### dataSource.columns.advancedFilter `array`
{:#members:datasource-columns-advancedfilter}

Allows the user to filter the report by default using advanced filtering (excel-like) option for OLAP data source in client-mode.

#### Default Value: []

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {columns: [{ advancedFilter : itemArray}]}});

{% endhighlight %}

### dataSource.columns.advancedFilter.name `string`
{:#members:datasource-columns-advancedfilter-name}

Allows the user to provide level unique name to do advanced filtering (excel-like) for OLAP data source in client-mode.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {columns: [{ advancedFilter : [{name: "dimensionUniqueName"}]}]}});

{% endhighlight %}

### dataSource.columns.advancedFilter.labelFilterOperator `string`
{:#members:datasource-columns-advancedfilter-labelfilteroperator}

Allows the user to set the operator for label filtering to do advanced filtering (excel-like) for OLAP data source in client-mode.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {columns: [{ advancedFilter : [{labelFilterOperator: ej.olap.LabelFilterOptions.EndsWith}]}]}});

{% endhighlight %}

### dataSource.columns.advancedFilter.valueFilterOperator `string`
{:#members:datasource-columns-advancedfilter-valuefilteroperator}

Allows the user to set the operator for value filtering to do advanced filtering (excel-like) for OLAP data source in client-mode.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {columns: [{ advancedFilter : [{valueFilterOperator: ej.olap.ValueFilterOptions.Between}]}]}});

{% endhighlight %}

### dataSource.columns.advancedFilter.advancedFilterType `string`
{:#members:datasource-columns-advancedfilter-advancedfiltertype}

Allows the user to set the filtering type while doing advanced filtering (excel-like) for OLAP data source in client-mode.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {columns: [{ advancedFilter : [{advancedFilterType:  ej.olap.AdvancedFilterType.LabelFilter}]}]}});

{% endhighlight %}

### dataSource.columns.advancedFilter.values `string`
{:#members:datasource-columns-advancedfilter-values}

Allows the user to holds the filter value in advanced filtering (excel-like) option for OLAP data source in client-mode.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {columns: [{ advancedFilter : [{values:  ["002"]}]}]}});

{% endhighlight %}


### dataSource.columns.isNamedSets `boolean`
{:#members:datasource-columns-isnamedsets}

Allows the user to enable the usage of named set items in respective axis. This is only applicable for OLAP datasource.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {columns: [{ isNamedSets : true}]}});

{% endhighlight %}


### dataSource.cube `string`
{:#members:datasource-cube}

Contains the respective Cube name from database as string type.

#### Default Value: “”

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {cube: value}});

{% endhighlight %}


### dataSource.data `object`
{:#members:datasource-data}

Provides the raw data source for the PivotGrid.

#### Default Value: null

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {data: value}});

{% endhighlight %}


### dataSource.rows `array`
{:#members:datasource-rows}

Lists out the items to be arranged in row section of PivotGrid.

#### Default Value: []

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {rows: itemsArray}});

{% endhighlight %}


### dataSource.rows.fieldName `string`
{:#members:datasource-rows-fieldname}

Allows the user to bind the item by using its unique name as field name.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {rows: [{ fieldName : value}]}});

{% endhighlight %}

### dataSource.rows.fieldCaption `string`
{:#members:datasource-rows-fieldcaption}

Allows the user to set the display name for an item.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {rows: [{ fieldCaption : value}]}});

{% endhighlight %}

### dataSource.rows.advancedFilter `array`
{:#members:datasource-rows-advancedfilter}

Allows the user to filter the report by default using advanced filtering (excel-like) option for OLAP data source in client-mode.

#### Default Value: []

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {rows: [{ advancedFilter : itemArray}]}});

{% endhighlight %}

### dataSource.rows.advancedFilter.name `string`
{:#members:datasource-rows-advancedfilter-name}

Allows the user to provide level unique name to do advanced filtering (excel-like) for OLAP data source in client-mode.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {rows: [{ advancedFilter : [{name: "dimensionUniqueName"}]}]}});

{% endhighlight %}

### dataSource.rows.advancedFilter.labelFilterOperator `string`
{:#members:datasource-rows-advancedfilter-labelfilteroperator}

Allows the user to set the operator for label filtering to do advanced filtering (excel-like) for OLAP data source in client-mode.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {rows: [{ advancedFilter : [{labelFilterOperator: ej.olap.LabelFilterOptions.EndsWith}]}]}});

{% endhighlight %}

### dataSource.rows.advancedFilter.valueFilterOperator `string`
{:#members:datasource-rows-advancedfilter-valuefilteroperator}

Allows the user to set the operator for value filtering to do advanced filtering (excel-like) for OLAP data source in client-mode.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {rows: [{ advancedFilter : [{valueFilterOperator: ej.olap.ValueFilterOptions.Between}]}]}});

{% endhighlight %}

### dataSource.rows.advancedFilter.advancedFilterType `string`
{:#members:datasource-rows-advancedfilter-advancedfiltertype}

Allows the user to set the filtering type while doing advanced filtering (excel-like) for OLAP data source in client-mode.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {rows: [{ advancedFilter : [{advancedFilterType:  ej.olap.AdvancedFilterType.LabelFilter}]}]}});

{% endhighlight %}

### dataSource.rows.advancedFilter.values `string`
{:#members:datasource-rows-advancedfilter-values}

Allows the user to holds the filter value in advanced filtering (excel-like) option for OLAP data source in client-mode.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {rows: [{ advancedFilter : [{values:  ["002"]}]}]}});

{% endhighlight %}

### dataSource.rows.isNamedSets `boolean`
{:#members:datasource-rows-isnamedsets}

Allows the user to enable the usage of named set items in respective axis. This is only applicable for OLAP datasource.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {rows: [{ isNamedSets : true}]}});

{% endhighlight %}


### dataSource.values `array`
{:#members:datasource-values}

Lists out the items which supports calculation in PivotGrid.

#### Default Value: []

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {values: itemsArray}});

{% endhighlight %}

### dataSource.values.measures `array`
{:#members:datasource-values[0]-measures}

This holds the measures unique name to bind them from the Cube.

#### Default Value: []

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {values: [{measures : itemsArray}]}});

{% endhighlight %}

### dataSource.values.axis `string`
{:#members:datasource-values[0]-axis}

Allows to set the axis name to place the measures items.

#### Default Value: “”

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {values: [{axis : value}]}});

{% endhighlight %}

### dataSource.values.fieldName `string`
{:#members:datasource-values[0]-fieldname}

Allows the user to bind the item by using its unique name as field name.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {values: [{ fieldName : value}]}});

{% endhighlight %}

### dataSource.values.fieldCaption `string`
{:#members:datasource-values[0]-fieldcaption}

Allows the user to set the display name for an item.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {values: [{ fieldCaption : value}]}});

{% endhighlight %}


### dataSource.values.isCalculatedField `boolean`
{:#members:datasource-values[0]-iscalculatedfield}

Allows the user to create new fields by enabling the calculated field option for relational data source at client-side.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {values: {isCalculatedField : true}}});

{% endhighlight %}

### dataSource.values.formula `string`
{:#members:datasource-values[0]-formula}

Allows the user to apply the formula as an expression in-order to create new field using calculated field option (in code-behind) for relational data source at client-side.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {values: {formula : formulaString}}});

{% endhighlight %}

### dataSource.enableAdvancedFilter `boolean`
{:#members:datasource-enableadvancedfilter}

Allows user to filter the members (by its name and values) by enable the advanced filtering (excel-like) option for OLAP data source in client-mode.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {enableAdvancedFilter: true}});

{% endhighlight %}


### dataSource.filters `array`
{:#members:datasource-filters}

Lists out the items which supports filtering of values in PivotGrid.

#### Default Value: []

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {filters: itemsArray}});

{% endhighlight %}


### dataSource.filters.fieldName `string`
{:#members:datasource-filters-fieldname}

Allows the user to bind the item by using its unique name as field name.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {filters: [{ fieldName : value}]}});

{% endhighlight %}

### dataSource.filters.fieldCaption `string`
{:#members:datasource-filters-fieldcaption}

Allows the user to set the display name for an item.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {filters: [{ fieldCaption : value}]}});

{% endhighlight %}


### dataSource.filters.isNamedSets `boolean`
{:#members:datasource-filters-isnamedsets}

Allows the user to enable the usage of named set items in respective axis. This is only applicable for OLAP datasource.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {filters: [{ isNamedSets : true}]}});

{% endhighlight %}


### drilledItems `array`
{:#members:drilleditems}

Used to bind the drilled members by default through report.

#### Default Value: []

### frozenHeaderSettings `object`
{:#members:frozenheadersettings}

Object that holds the settings of frozen headers.

#### Default Value: {}

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ frozenHeaderSettings: { enableFrozenHeaders: true }}); 

{% endhighlight %}

### frozenHeaderSettings.enableFrozenRowHeaders `boolean`
{:#members:frozenheadersettings-enablefrozenrowheaders}

Allows the user to freeze the row headers alone on scrolling the horizontal scroll bar.

#### Default Value: false

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ frozenHeaderSettings: { enableFrozenRowHeaders: true }}); 

{% endhighlight %}
### frozenHeaderSettings.enableFrozenColumnHeaders `boolean`
{:#members:frozenheadersettings-enablefrozencolumnheaders}

Allows the user to freeze the column headers alone on scrolling the vertical scroll bar.

#### Default Value: false

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ frozenHeaderSettings: { enableFrozenColumnHeaders: true }}); 

{% endhighlight %}

### frozenHeaderSettings.enableFrozenHeaders `boolean`
{:#members:frozenheadersettings-enablefrozenheaders}

Allows the user to freeze both the row headers and column headers on scrolling.

#### Default Value: false

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ frozenHeaderSettings: { enableFrozenHeaders: true }});

{% endhighlight %}

### customObject `object`
{:#members:customobject}

Object utilized to pass additional information between client-end and service-end.

#### Default Value: null

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ customObject: { Language: "en-US" }}); 

{% endhighlight %}

### collapsedMembers `object`
{:#members:collapsedmembers}

Contains the list of members in field-wise manner which are collapsed.

#### Default Value: null

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ collapsedMembers: { Country: ["Canada", "France"] } }); 

{% endhighlight %}

### enableCellContext `boolean`
{:#members:enablecellcontext}

Allows the user to access each cell on mouse right-click.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ enableCellContext: true });

{% endhighlight %}

### enableCellSelection `boolean`
{:#members:enablecellselection}

Enables the cell selection for a specified range of value cells. And, the individual row/column cells can be selected by clicking its headers.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ enableCellSelection:true });

{% endhighlight %}

### enableDrillThrough `boolean`
{:#members:enabledrillthrough}

Enables the Drill-Through feature which retrieves the raw items that are used to create a specified cell in PivotGrid. This is only applicable in server mode component.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ enableDrillThrough:true});

{% endhighlight %}

### enableCellDoubleClick `boolean`
{:#members:enablecelldoubleclick}

Allows user to get the cell details in JSON format when double clicking the cell.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ enableCellDoubleClick:true});

{% endhighlight %}

### enableCellEditing `boolean`
{:#members:enablecellediting}

Allows user to edit the value cells for write-back support in PivotGrid. This is applicable only for server-mode. 

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ enableCellEditing:true });

{% endhighlight %}


### enableCollapseByDefault `boolean`
{:#members:enablecollapsebydefault}

Collapses the Pivot Items along rows and columns by default.  It works only for relational data source.

#### Default Value: false

**Example:**

{% highlight html %}

$("#PivotGrid1").ejPivotGrid({enableCollapseByDefault: true});

{% endhighlight %}

### enableColumnGrandTotal `boolean`
{:#members:enablecolumngrandtotal}

Enables the display of grand total for all the columns.

#### Default Value: true

**Example:**

{% highlight html %}

$("#PivotGrid1").ejPivotGrid({enableColumnGrandTotal: true});

{% endhighlight %}

### enableConditionalFormatting `boolean`
{:#members:enableconditionalformatting}

Allows the user to format a specific set of cells based on the condition. 

#### Default Value: false

**Example:**

{% highlight html %}

$("#PivotGrid1").ejPivotGrid({ enableConditionalFormatting:true });

{% endhighlight %}


### enableDeferUpdate `boolean`
{:#members:enabledeferupdate}

Allows the user to refresh the control on-demand and not during every UI operation.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({enableDeferUpdate: true});

{% endhighlight %}


### enableGroupingBar `boolean`
{:#members:enablegroupingbar}

Enables the display of GroupingBar allowing you to filter, sort and remove fields obtained from relational datasource.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ enableGroupingBar:true });

{% endhighlight %}


### enableGrandTotal `boolean`
{:#members:enablegrandtotal}

Enables the display of grand total for rows and columns.

#### Default Value: true

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({enableGrandTotal: true});

{% endhighlight %}


### enableJSONRendering `boolean`
{:#members:enablejsonrendering}

Allows the user to load PivotGrid using JSON data.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ enableJSONRendering: true });

{% endhighlight %}

### enablePivotFieldList `boolean`
{:#members:enablepivotfieldlist}

Enables rendering of PivotGrid widget along with the PivotTable Field List, which allows UI operation.

#### Default Value: true

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({enablePivotFieldList: true});

{% endhighlight %}

### enableRowGrandTotal `boolean`
{:#members:enablerowgrandtotal}

Enables the display of grand total for all the rows.

#### Default Value: true

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({enableRowGrandTotal: true});

{% endhighlight %}

### enableRTL `boolean`
{:#members:enablertl}

Allows the user to view layout of the PivotGrid from right to left.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ enableRTL: true });

{% endhighlight %}

### enableToolTip `boolean`
{:#members:enabletooltip}

Allows the user to enable ToolTip option.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ enableToolTip: true });

{% endhighlight %}

### enableToolTipAnimation `boolean`
{:#members:enabletooltipanimation}

Allows the user to enable the animation effects in tooltip.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ enableToolTipAnimation: true });

{% endhighlight %}

### enableColumnResizing `boolean`
{:#members:enablecolumnresizing}

Allows the user to adjust the width of the columns dynamically.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ enableColumnResizing: true });

{% endhighlight %}

### enableVirtualScrolling `boolean`
{:#members:enablevirtualscrolling}

Allows the user to view large amount of data through virtual scrolling.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ enableVirtualScrolling: true });

{% endhighlight %}

### enablePaging `boolean`
{:#members:enablepaging}

Allows the user to view large amount of data by applying paging.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ enablePaging: true });

{% endhighlight %}

### hyperlinkSettings `object`
{:#members:hyperlinksettings}

Allows the user to configure hyperlink settings of PivotGrid control.

#### Default Value: {}

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ hyperlinkSettings: {enableValueCellHyperlink: true, enableRowHeaderHyperlink: true} });

{% endhighlight %}

### hyperlinkSettings.enableColumnHeaderHyperlink `boolean`
{:#members:hyperlinksettings-enablecolumnheaderhyperlink}

Allows the user to enable/disable hyperlink for column header.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ hyperlinkSettings: { enableColumnHeaderHyperlink: true } });

{% endhighlight %}

### hyperlinkSettings.enableRowHeaderHyperlink `boolean`
{:#members:hyperlinksettings-enablerowheaderhyperlink}

Allows the user to enable/disable hyperlink for row header.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ hyperlinkSettings: { enableRowHeaderHyperlink: true } });

{% endhighlight %}

### hyperlinkSettings.enableSummaryCellHyperlink `boolean`
{:#members:hyperlinksettings-enablesummarycellhyperlink}

Allows the user to enable/disable hyperlink for summary cells.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ hyperlinkSettings: { enableSummaryCellHyperlink: true } });

{% endhighlight %}

### hyperlinkSettings.enableValueCellHyperlink `boolean`
{:#members:hyperlinksettings-enablevaluecellhyperlink}

Allows the user to enable/disable hyperlink for value cells.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ hyperlinkSettings: { enableValueCellHyperlink: true } });

{% endhighlight %}


### isNamedSets `boolean`
{:#members:isnamedsets}

This is used for identifying whether the member is Named Set or not.

#### Default Value: false


### isResponsive `boolean`
{:#members:isresponsive}

Allows the user to enable PivotGrid’s responsiveness in the browser layout.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ isResponsive: true });

{% endhighlight %}

### jsonRecords `string`
{:#members:jsonrecords}

Contains the serialized JSON string which renders PivotGrid.

#### Default Value: “”

### layout `enum`
{:#members:layout}

<ts name = "ej.PivotGrid.Layout"/>

Sets the summary layout for PivotGrid. Following are the ways in which summary can be positioned: normal summary (bottom), top summary, no summary and excel-like summary.

#### Default Value: ej.PivotGrid.Layout.Normal

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">Normal</td>
            <td class="description">To set normal summary layout in PivotGrid.</td>
        </tr>
        <tr>
            <td class="name">NormalTopSummary</td>
            <td class="description">To set layout with summaries at the top in PivotGrid.</td>
        </tr>
        <tr>
            <td class="name">NoSummaries</td>
            <td class="description">To set layout without summaries in PivotGrid.</td>
        </tr>
        <tr>
            <td class="name">ExcelLikeLayout</td>
            <td class="description">To set excel-like layout in PivotGrid.</td>
        </tr>
    </tbody>
</table>

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ layout: ej.PivotGrid.Layout.NoSummaries });

{% endhighlight %}

### locale `string`
{:#members:locale}

Allows the user to set the localized language for the widget.

#### Default Value: "en-US"

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ locale: "en-US" }}); 

{% endhighlight %}


### operationalMode `enum`
{:#members:operationalmode}

<ts name = "ej.PivotGrid.OperationalMode"/>

Sets the mode for the PivotGrid widget for binding data source either in server-side or client-side.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">ClientMode</td>
            <td class="description">To bind data source completely from client-side.</td>
        </tr>
        <tr>
            <td class="name">ServerMode</td>
            <td class="description">To bind data source completely from server-side.</td>
        </tr>
    </tbody>
</table>

#### Default Value: ej.PivotGrid.OperationalMode.ClientMode

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({operationalMode: ej.PivotGrid.OperationalMode.ServerMode});

{% endhighlight %}

### serviceMethodSettings `object`
{:#members:servicemethodsettings}

Allows the user to set custom name for the methods at service-end, communicated during AJAX post.

#### Default Value: {}

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ serviceMethodSettings: { initialize: "InitializeGrid"} });

{% endhighlight %}

### serviceMethodSettings.drillDown `string`
{:#members:servicemethodsettings-drilldown}

Allows the user to set the custom name for the service method that&#39;s responsible for drill up/down operation in PivotGrid.

#### Default Value: "DrillGrid"

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ serviceMethodSettings: { drillDown: "DrillGridMyMethod" } });

{% endhighlight %}

### serviceMethodSettings.exportPivotGrid `string`
{:#members:servicemethodsettings-exportpivotgrid}

Allows the user to set the custom name for the service method that’s responsible for exporting.

#### Default Value: "Export"

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ serviceMethodSettings: { exportPivotGrid: "ExportMyMethod" } })

{% endhighlight %}

### serviceMethodSettings.deferUpdate `string`
{:#members:servicemethodsettings-deferupdate}

Allows the user to set the custom name for the service method that’s responsible for performing server-side actions on defer update.

#### Default Value: "DeferUpdate"

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ serviceMethodSettings: { deferUpdate: "DeferUpdateMethod" } });

{% endhighlight %}

### serviceMethodSettings.fetchMembers `string`
{:#members:servicemethodsettings-fetchmembers}

Allows the user to set the custom name for the service method that’s responsible to getting the values for the tree-view inside filter dialog.

#### Default Value: "FetchMembers"

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ serviceMethodSettings:  { fetchMembers: "FetchMembersMethod" } });

{% endhighlight %}
 
### serviceMethodSettings.filtering `string`
{:#members:servicemethodsettings-filtering}

Allows the user to set the custom name for the service method that's responsible for filtering operation in PivotGrid.

#### Default Value: "Filtering"

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ serviceMethodSettings:  { filtering : "FilteringMethod" } });

{% endhighlight %}
 
### serviceMethodSettings.initialize `string`
{:#members:servicemethodsettings-initialize}

Allows the user to set the custom name for the service method that&#39;s responsible for initializing PivotGrid.

#### Default Value: "InitializeGrid"

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ serviceMethodSettings: { initialize: "InitializeGrid" } });

{% endhighlight %}

### serviceMethodSettings.nodeDropped `string`
{:#members:servicemethodsettings-nodedropped}

Allows the user to set the custom name for the service method that's responsible for the server-side action, on dropping a node into Field List.

#### Default Value: "NodeDropped"

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ serviceMethodSettings: { nodeDropped: "nodedroppedMethod" } });

{% endhighlight %}

### serviceMethodSettings.nodeStateModified `string`
{:#members:servicemethodsettings-nodestatemodified}

Allows the user to set the custom name for the service method that’s responsible for the server-side action on changing the checked state of a node in Field List.

#### Default Value: "NodeStateModified"

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ serviceMethodSettings: { nodeStateModified: "NodeStateModifiedMethod" } });

{% endhighlight %}

### serviceMethodSettings.paging `string`
{:#members:servicemethodsettings-paging}

Allows the user to set the custom name for the service method that&#39;s responsible for performing paging operation in PivotGrid.

#### Default Value: "Paging"

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ serviceMethodSettings: { paging: "PagingMyMethod" } });

{% endhighlight %}

### serviceMethodSettings.sorting `string`
{:#members:servicemethodsettings-sorting}

Allows the user to set the custom name for the service method that's responsible for sorting operation in PivotGrid.

#### Default Value: "Sorting"

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ serviceMethodSettings: { sorting: "SortingMethod" } });

{% endhighlight %}

### serviceMethodSettings.memberExpand `string`
{:#members:servicemethodsettings-memberexpand}

Allows the user to set the custom name for the service method that’s responsible for expanding members inside member editor.

#### Default Value: "MemberExpanded"

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ serviceMethodSettings: { memberExpand: "MemberExpandedMethod" } });

{% endhighlight %}

### serviceMethodSettings.cellEditing `string`
{:#members:servicemethodsettings-cellediting}

Allows the user to set the custom name for the service method responsible for editing the cells.

#### Default Value: "CellEditing"

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ serviceMethodSettings: { cellEditing: "MyCellEditingMethod" } });

{% endhighlight %}

### serviceMethodSettings.saveReport `string`
{:#members:servicemethodsettings-savereport}

Allows the user to set the custom name for the service method responsible for saving the current report to database.

#### Default Value: "SaveReport"

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ serviceMethodSettings: { saveReport: "MySaveReportMethod" } });

{% endhighlight %}

### serviceMethodSettings.loadReport `string`
{:#members:servicemethodsettings-loadreport}

Allows the user to set the custom name for the service method responsible for loading a report from database.

#### Default Value: "LoadReportFromDB"

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ serviceMethodSettings: { loadReport: "MyLoadReportMethod" } });

{% endhighlight %}

### serviceMethodSettings.calculatedField `string`
{:#members:servicemethodsettings-calculatedfield}

Allows the user to set the custom name for the service method responsible for adding a calculated field to the report.

#### Default Value: "CalculatedField"

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ serviceMethodSettings: { calculatedField: "MyCalculatedFieldMethod" } });

{% endhighlight %}

### serviceMethodSettings.drillThroughHierarchies `string`
{:#members:servicemethodsettings-drillthroughhierarchies}

Allows the user to set the custom name for the service method responsible for performing drill through operation.

#### Default Value: "DrillThroughHierarchies"

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ serviceMethodSettings: { drillThroughHierarchies: "MyDrillThroughHierarchiesMethod" } });

{% endhighlight %}

### serviceMethodSettings.drillThroughDataTable `string`
{:#members:servicemethodsettings-drillthroughdatatable}

Allows the user to set the custom name for the service method responsible for performing drill through operation in data table.

#### Default Value: "DrillThroughDataTable"

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ serviceMethodSettings: { drillThroughDataTable: "MyDrillThroughDataTableMethod" } });

{% endhighlight %}

### serviceMethodSettings.writeBack `string`
{:#members:servicemethodsettings-writeback}

Allows the user to set the custom name for the service method that’s responsible for write-back operation in OLAP Cube. This is only applicable in server-side component.

#### Default Value: "WriteBack"

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ serviceMethodSettings: { writeBack: "WriteBackMethod" } });

{% endhighlight %}


### url `string`
{:#members:url}

Connects the service using the specified URL for any server updates.

#### Default Value: “”

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ url: "/wcf/PivotGridService.svc" });

{% endhighlight %}

## Methods

### doAjaxPost()
{:#methods:doajaxpost}

Perform an asynchronous HTTP (AJAX) request.

**Example:**

{% highlight html %}
 
<div id="PivotGrid1"></div> 
 
<script>
$('#PivotGrid1').ejPivotGrid({
      url: "PivotGridService.svc",
  });
var gridObj = $("#PivotGrid1").data("ejPivotGrid");
gridObj.doAjaxPost("POST", "/PivotGridService.svc/Initialize", {"key", "Hello World"}, "_renderControlSuccess", null);
</script>

{% endhighlight %}

### doPostBack()
{:#methods:dopostback}

Perform an asynchronous HTTP (FullPost) submit.

**Example:**

{% highlight html %}
 
<div id="PivotGrid1"></div> 
 
<script>
$('#PivotGrid1').ejPivotGrid({
      url: "PivotGridService.svc",
  });
var gridObj = $("#PivotGrid1").data("ejPivotGrid");
gridObj.doPostBack("/PivotGridService.svc/Initialize", {"key", "Hello World"});
</script>

{% endhighlight %}


### exportPivotGrid()
{:#methods:exportpivotgrid}

Exports the PivotGrid to an appropriate format based on the parameter passed.

**Example:**

{% highlight html %}
 
var gridObj = $("# PivotGrid1").data("ejPivotGrid");
gridObj.exportPivotGrid(ej.PivotGrid.ExportOptions.Excel);

{% endhighlight %}


### refreshPagedPivotGrid()
{:#methods:refreshpagedpivotgrid}

This function re-renders the PivotGrid on clicking the navigation buttons on PivotPager.

**Example:**

{% highlight html %}
 
<div id="PivotGrid1"></div> 
 
<script>
$('#PivotGrid1').ejPivotGrid({
      url: "PivotGridService.svc",
  });
var gridObj = $("#PivotGrid1").data("ejPivotGrid");
gridObj.refreshPagedPivotGrid("series", 2);
</script>

{% endhighlight %}

### refreshPivotGrid()
{:#methods:refreshpivotgrid}

This function is helps to update or refresh the PivotGrid with modified data source in client-mode.

**Example:**

{% highlight html %}

var gridObj = $("#PivotGrid1").data("ejPivotGrid");
gridObj.refreshPivotGrid();

{% endhighlight %}

### refreshControl()
{:#methods:refreshcontrol}

This function re-renders the control with the report available at that instant.

**Example:**

{% highlight html %}

var gridObj = $("#PivotGrid1").data("ejPivotGrid");
gridObj.refreshControl();

{% endhighlight %}

### calculateCellWidths()
{:#methods:calculatecellwidths}

This function returns the height of all rows and width each and every column.

**Example:**

{% highlight html %}

var gridObj = $("#PivotGrid1").data("ejPivotGrid");
var gridDimensions = gridObj.calculateCellWidths();

{% endhighlight %}

### createConditionalDialog()
{:#methods:createconditionaldialog}

This function creates the conditional formatting dialog to apply conditional formatting for PivotGrid control.

**Example:**

{% highlight html %}

var gridObj = $("#PivotGrid1").data("ejPivotGrid");
gridObj.createConditionalDialog();

{% endhighlight %}

### saveReport()
{:#methods:savereport}

This function saves the current report to the database/local storage.

**Example:**

{% highlight html %}

var gridObj = $("#PivotGrid1").data("ejPivotGrid");
var storageOption = "local"; //it takes the string value "local" for local storage and "database" for storing to database.
var url = "";//it takes the service url for storing to database. For local it is not required.
gridObj.saveReport("reportName", storageOption, url);

{% endhighlight %}

### loadReport()
{:#methods:loadreport}

This function loads the specified report from the database/local storage.

**Example:**

{% highlight html %}

var gridObj = $("#PivotGrid1").data("ejPivotGrid");
var storageOption = "local"; //it takes the string value "local" for loading a report from local storage and "database" for loading from database.
var url = "";//it takes the service method url for loading report from database. For local it is not required.
gridObj.loadReport("reportName", storageOption, url);

{% endhighlight %}

### excelLikeLayout()
{:#methods:excellikelayout}

This function reconstructs the JSON data formed for rendering PivotGrid in excel-like layout format.

**Example:**

{% highlight html %}

var gridObj = $("#PivotGrid1").data("ejPivotGrid");
gridObj.excelLikeLayout(JSONObjectArray);

{% endhighlight %}

### getOlapReport()
{:#methods:getolapreport}

Returns the OlapReport string maintained along with the axis elements information.

**Example:**

{% highlight html %}
 
    var gridObj = $("#PivotGrid1").data("ejPivotGrid");
    var report = gridObj.getOlapReport();
{% endhighlight %}

### setOlapReport()
{:#methods:setolapreport}

Sets the OlapReport string along with the axis information and maintains it in a property.

**Example:**

{% highlight html %}
 
    var gridObj = $("#PivotGrid1").data("ejPivotGrid");
    gridObj.setOlapReport(olapReportObj);
{% endhighlight %}

### getJSONRecords()
{:#methods:getjsonrecords}

Returns the JSON records formed to render the control.

**Example:**

{% highlight html %}
 
    var gridObj = $("#PivotGrid1").data("ejPivotGrid");
    var jsonRecords = gridObj.getJSONRecords();
{% endhighlight %}

### setJSONRecords()
{:#methods:setjsonrecords}

Sets the JSON records formed to render the control to a property.

**Example:**

{% highlight html %}
 
    var gridObj = $("#PivotGrid1").data("ejPivotGrid");
    gridObj.setJSONRecords(jsonRecords);
{% endhighlight %}

### refreshFieldCaption()
{:#methods:refreshfieldcaption}

This function allows user to change the caption of the Pivot Item (name displayed in UI) on-demand for relational datasource in client-mode.

**Example:**

{% highlight html %}

var gridObj = $("#PivotGrid1").data("ejPivotGrid");
gridObj.refreshFieldCaption("name","caption","axisClassName");

{% endhighlight %}


### renderControlFromJSON()
{:#methods:rendercontrolfromjson}

This function receives the JSON formatted datasource to render the PivotGrid control.

**Example:**

{% highlight html %}
 
<div id="PivotGrid1"></div> 
 
<script>
$('#PivotGrid1').ejPivotGrid({
      url: "PivotGridService.svc",
  });
var gridObj = $("#PivotGrid1").data("ejPivotGrid");
gridObj.renderControlFromJSON({this.getJSONRecords()});
</script>

{% endhighlight %}



## Events

### afterServiceInvoke
{:#events:afterserviceinvoke}

Triggers when it reaches client-side after any AJAX request.

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
<td class="name">action</td>
<td class="type">string</td>
<td class="description last">return the current action of PivotGrid control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">return the custom object bounds with PivotGrid control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">return the outer HTML of PivotGrid control.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.PivotGrid.Model"/>object</td>
<td class="description last">returns the PivotGrid model</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({
   afterServiceInvoke: function (args) {}
});     

{% endhighlight %}


### beforeServiceInvoke
{:#events:beforeserviceinvoke}

Triggers before any AJAX request is passed from PivotGrid to service methods.

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
<td class="name">action</td>
<td class="type">string</td>
<td class="description last">return the current action of PivotGrid control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">return the custom object bounds with PivotGrid control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">return the outer HTML of PivotGrid control.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.PivotGrid.Model"/>object</td>
<td class="description last">returns the PivotGrid model</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({
   beforeServiceInvoke: function (args) {}
});      

{% endhighlight %}

### beforePivotEnginePopulate
{:#events:beforepivotenginepopulate}

Triggers before Pivot Engine starts to populate.

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
<td class="name">pivotObject</td>
<td class="type">object</td>
<td class="description last">returns the PivotGrid object</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.PivotGrid.Model"/>object</td>
<td class="description last">returns the PivotGrid model</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({
   beforePivotEnginePopulate: function (args) {}
});      

{% endhighlight %}


### cellDoubleClick
{:#events:celldoubleclick}

Triggers when double click action is performed over a cell. 

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
<td class="name">selectedData</td>
<td class="type">object</td>
<td class="description last">return the JSON details of the double clicked cell.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">return the custom object bounds with PivotGrid widget.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">return the outer HTML of PivotGrid control.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.PivotGrid.Model"/>object</td>
<td class="description last">returns the PivotGrid model</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({
   cellDoubleClick: function (args) {}
});      

{% endhighlight %}


### cellContext
{:#events:cellcontext}

Triggers when right-click action is performed on a cell.

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
<td class="name">args</td>
<td class="type">object</td>
<td class="description last">returns the original event args.</td>
</tr>
<tr>
<td class="name">cellPosition</td>
<td class="type">string</td>
<td class="description last">returns the cell position (row index and column index) in table.</td>
</tr>
<tr>
<td class="name">cellType</td>
<td class="type">string</td>
<td class="description last">returns the type of the cell.</td>
</tr>
<tr>
<td class="name">rowData</td>
<td class="type">string</td>
<td class="description last">returns the serialized data of the header cells.</td>
</tr>
<tr>
<td class="name">uniqueName</td>
<td class="type">string</td>
<td class="description last">returns the unique name of levels/members.</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({
   cellContext: function (args) {}
});      

{% endhighlight %}


### cellSelection
{:#events:cellselection}

Triggers when a specific range of value cells are selected.

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
<td class="name">args</td>
<td class="type">object</td>
<td class="description last">returns the original event args.</td>
</tr>
<tr>
<td class="name">cellvalue</td>
<td class="type">object</td>
<td class="description last">Returns the selected cell values.</td>
</tr>
<tr>
<td class="name">rowheaders</td>
<td class="type">object</td>
<td class="description last">Returns the selected value cells row headers.</td>
</tr>
<tr>
<td class="name">colheaders</td>
<td class="type">object</td>
<td class="description last">Returns the selected value cells column headers.</td>
</tr>
<tr>
<td class="name">measure</td>
<td class="type">object</td>
<td class="description last">Returns the selected value cells measure.</td>
</tr>
<tr>
<td class="name">measureValue</td>
<td class="type">object</td>
<td class="description last">Return the row and column measure count.</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({
   cellSelection: function (args) {}
});      

{% endhighlight %}

### columnHeaderHyperlinkClick
{:#events:columnheaderhyperlinkclick}

Triggers when the hyperlink of column header is clicked.

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
<td class="name">args</td>
<td class="type">object</td>
<td class="description last">returns the original event args.</td>
</tr>
<tr>
<td class="name">cellPosition</td>
<td class="type">string</td>
<td class="description last">returns the cell position (row index and column index) in table.</td>
</tr>
<tr>
<td class="name">cellType</td>
<td class="type">string</td>
<td class="description last">returns the type of the cell.</td>
</tr>
<tr>
<td class="name">rowData</td>
<td class="type">string</td>
<td class="description last">returns the serialized data of the header cells.</td>
</tr>
<tr>
<td class="name">uniqueName</td>
<td class="type">string</td>
<td class="description last">returns the unique name of levels/members.</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({
   columnHeaderHyperlinkClick: function (args) {}
});      

{% endhighlight %}


### drillSuccess
{:#events:drillsuccess}

Triggers after performing drill operation in PivotGrid.

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
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.PivotGrid.Model"/>object</td>
<td class="description last">returns the PivotGrid model</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({
   drillSuccess: function (args) {}
});      

{% endhighlight %}


### drillThrough
{:#events:drillthrough}

Triggers while clicking "OK" button in the drill-through dialog. 

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
<td class="type">object</td>
<td class="description last">return the JSON records of the generated cells on drill-through operation.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">return the outer HTML of PivotGrid control.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.PivotGrid.Model"/>object</td>
<td class="description last">returns the PivotGrid model</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({
   drillThrough: function (args) {}
});      

{% endhighlight %}


### load
{:#events:load}

Triggers when PivotGrid loading is initiated.

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
<td class="name">args</td>
<td class="type">object</td>
<td class="description last">returns the original event args.</td>
</tr>
<tr>
<td class="name">action</td>
<td class="type">string</td>
<td class="description last">returns the current action of PivotGrid control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">Object</td>
<td class="description last">returns the custom object bounded with the control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">returns the HTML of PivotGrid control.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.PivotGrid.Model"/>object</td>
<td class="description last">returns the PivotGrid model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({
   load: function (args) {}
});      

{% endhighlight %}

### renderComplete
{:#events:rendercomplete}

Triggers when PivotGrid widget completes all operations at client-side after any AJAX request.

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
<td class="name">args</td>
<td class="type">object</td>
<td class="description last">returns the original event args.</td>
</tr>
<tr>
<td class="name">action</td>
<td class="type">string</td>
<td class="description last">returns the current action of PivotGrid control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">Object</td>
<td class="description last">returns the custom object bounded with the control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">returns the HTML of PivotGrid control.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.PivotGrid.Model"/>object</td>
<td class="description last">returns the PivotGrid model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({
   renderComplete: function (args) {}
});      

{% endhighlight %}

### renderFailure
{:#events:renderfailure}

Triggers when any error occurred during AJAX request.

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
<td class="name">args</td>
<td class="type">object</td>
<td class="description last">returns the original event args.</td>
</tr>
<tr>
<td class="name">action</td>
<td class="type">string</td>
<td class="description last">returns the current action of PivotGrid control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">Object</td>
<td class="description last">returns the custom object bounded with the control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">returns the HTML of PivotGrid control.</td>
</tr>
<tr>
<td class="name">message</td>
<td class="type">Object</td>
<td class="description last">returns the error message with error code.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.PivotGrid.Model"/>object</td>
<td class="description last">returns the PivotGrid model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({
   renderFailure: function (args) {}
});      

{% endhighlight %}


### renderSuccess
{:#events:rendersuccess}

Triggers when PivotGrid successfully reaches client-side after any AJAX request. 

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
<td class="name">args</td>
<td class="type">object</td>
<td class="description last">returns the original event args.</td>
</tr>
<tr>
<td class="name">action</td>
<td class="type">string</td>
<td class="description last">returns the current action of PivotGrid control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">Object</td>
<td class="description last">returns the custom object bounded with the control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">returns the HTML of PivotGrid control.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.PivotGrid.Model"/>object</td>
<td class="description last">returns the PivotGrid model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({
   renderSuccess: function (args) {}
});      

{% endhighlight %}


### rowHeaderHyperlinkClick
{:#events:rowheaderhyperlinkclick}

Triggers when the hyperlink of row header is clicked.

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
<td class="name">args</td>
<td class="type">object</td>
<td class="description last">returns the original event args.</td>
</tr>
<tr>
<td class="name">cellPosition</td>
<td class="type">string</td>
<td class="description last">returns the cell position (row index and column index) in table.</td>
</tr>
<tr>
<td class="name">cellType</td>
<td class="type">string</td>
<td class="description last">returns the type of the cell.</td>
</tr>
<tr>
<td class="name">rowData</td>
<td class="type">string</td>
<td class="description last">returns the serialized data of the header cells.</td>
</tr>
<tr>
<td class="name">uniqueName</td>
<td class="type">string</td>
<td class="description last">returns the unique name of levels/members.</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({
   rowHeaderHyperlinkClick: function (args) {}
});      

{% endhighlight %}

### summaryCellHyperlinkClick
{:#events:summarycellhyperlinkclick}

Triggers when the hyperlink of summary cell is clicked.

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
<td class="name">args</td>
<td class="type">object</td>
<td class="description last">returns the original event args.</td>
</tr>
<tr>
<td class="name">cellPosition</td>
<td class="type">string</td>
<td class="description last">returns the cell position (row index and column index) in table.</td>
</tr>
<tr>
<td class="name">cellType</td>
<td class="type">string</td>
<td class="description last">returns the type of the cell.</td>
</tr>
<tr>
<td class="name">rowData</td>
<td class="type">string</td>
<td class="description last">returns the serialized data of the header cells.</td>
</tr>
<tr>
<td class="name">uniqueName</td>
<td class="type">string</td>
<td class="description last">returns the unique name of levels/members.</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({
   summaryCellHyperlinkClick: function (args) {}
});      

{% endhighlight %}

### valueCellHyperlinkClick
{:#events:valuecellhyperlinkclick}

Triggers when the hyperlink of value cell is clicked.

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
<td class="name">args</td>
<td class="type">object</td>
<td class="description last">returns the original event args.</td>
</tr>
<tr>
<td class="name">cellPosition</td>
<td class="type">string</td>
<td class="description last">returns the cell position (row index and column index) in table.</td>
</tr>
<tr>
<td class="name">cellType</td>
<td class="type">string</td>
<td class="description last">returns the type of the cell.</td>
</tr>
<tr>
<td class="name">rowData</td>
<td class="type">string</td>
<td class="description last">returns the serialized data of the header cells.</td>
</tr>
<tr>
<td class="name">uniqueName</td>
<td class="type">string</td>
<td class="description last">returns the unique name of levels/members.</td>
</tr>
</tbody>
</table>

### saveReport
{:#events:saveReport}

Triggers before saving the current report to database.

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
<td class="name">args</td>
<td class="type">object</td>
<td class="description last">returns the original event args.</td>
</tr>
<tr>
<td class="name">report</td>
<td class="type">object</td>
<td class="description last">returns the report to be stored in database.</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({
   saveReport: function (args) {}
});

{% endhighlight %}

### loadReport
{:#events:loadReport}

Triggers before loading a report from database.

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
<td class="name">targetControl</td>
<td class="type">object</td>
<td class="description last">returns the PivotGrid object.</td>
</tr>
<tr>
<td class="name">dataModel</td>
<td class="type">string</td>
<td class="description last">returns whether the control is bound with OLAP or Relational data source.</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({
   loadReport: function (args) {}
});

{% endhighlight %}

### beforeExport
{:#events:beforeExport}

Triggers before performing exporting in pivot grid.

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
<td class="name">url</td>
<td class="type">string</td>
<td class="description last">contains the url of the service responsible for exporting.</td>
</tr>
<tr>
<td class="name">fileName</td>
<td class="type">string</td>
<td class="description last">contains the name of the exporting file.</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({
   beforeExport: function (args) {}
});

{% endhighlight %}

### cellEdit
{:#events:celledit}

Triggers before editing the cells.

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
<td class="name">editCellsInfo</td>
<td class="type">array</td>
<td class="description last">contains the array of cells selected for editing.</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({
   cellEdit: function (args) {}
});

{% endhighlight %}