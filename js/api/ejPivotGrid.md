---
layout: post
title: ejPivotGrid
documentation: API
platform: js
keywords: ejPivotGrid, API, Essential JS PivotGrid
metaname: 
metacontent: 
---

# PivotGrid

The PivotGrid control is easily configurable, presentation-quality business control that reads OLAP data from a Microsoft SQL Server Analysis Services database, an offline cube, XML/A or relational datasource.

#### Syntax

{% highlight js %}

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

* module:jquery-1.10.2.min.js
* module:jquery.easing.1.3.min.js
* module:ej.core.js
* module:ej.data.js
* module:ej.touch.js
* module:ej.waitingpopup.js
* module:ej.pivotgrid.js
* module:ej.pivotpager.js


## Members

### analysisMode `object`
{:#members:analysismode}

Sets the mode for the PivotGrid widget for binding either OLAP or relational data source.

**Default Value:** ej.PivotGrid.AnalysisMode.Olap

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({analysisMode: ej.PivotGrid.AnalysisMode.Relational });  

{% endhighlight %}


### cssClass `string`
{:#members:cssclass}

Specifies the CSS class to PivotGrid to achieve custom theme.

**Default Value:** “”

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ cssClass: "gradient-lime" });       

{% endhighlight %}

### currentReport `string`
{:#members:currentreport}

Contains the serialized OlapReport at that instant.

**Default Value:** “”

### dataSource `object`
{:#members:datasource}

Initializes the data source for the PivotGrid widget, when it functions completely on client-side.

**Default Value:** {}

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {data:value}});

{% endhighlight %}


### dataSource.data `object`
{:#members:dataSource-data}

Provides the raw data source for the PivotGrid.

**Default Value:** null

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {data: value}});

{% endhighlight %}


### dataSource.columns `object`
{:#members:datasource-columns}

Lists out the items to be arranged in column section of PivotGrid.

**Default Value:** []

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {columns: itemsArray}});

{% endhighlight %}

### dataSource.rows `object`
{:#members:datasource-rows}

Lists out the items to be arranged in row section of PivotGrid.

**Default Value:** []

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {rows: itemsArray}});

{% endhighlight %}


### dataSource.values `object`
{:#members:datasource-values}

Lists out the items which supports calculation in PivotGrid.

**Default Value:** []

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {values: itemsArray}});

{% endhighlight %}


### dataSource.filters `object`
{:#members:datasource-filters}

Lists out the items which supports filtering of values in PivotGrid.

**Default Value:** []

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {filters: itemsArray}});

{% endhighlight %}


### customObject `object`
{:#members:customobject}

Object utilized to pass additional information between client-end and service-end.

**Default Value:** null

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ customObject: { Language: "en-US" }}); 

{% endhighlight %}

### enableCellContext `boolean`
{:#members:enablecellcontext}

Allows the user to access each cell on right-click.

**Default Value:** false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ enableCellContext: true });

{% endhighlight %}

### enableCellSelection `boolean`
{:#members:enablecellselection}

Enables the cell selection for a specified range of value cells.

**Default Value:** false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ enableCellSelection:true });

{% endhighlight %}

### enableCollapseByDefault `boolean`
{:#members:enablecollapsebydefault}

Collapses the Pivot Items along rows and columns by default.  It works only for relational data source.

**Default Value:** false

**Example:**

{% highlight html %}

$("#PivotGrid1").ejPivotGrid({enableCollapseByDefault: true});

{% endhighlight %}

### enableColumnGrandTotal `boolean`
{:#members:enablecolumngrandtotal}

Enables the display of grand total for all the columns.

**Default Value:** true

**Example:**

{% highlight html %}

$("#PivotGrid1").ejPivotGrid({enableColumnGrandTotal: true});

{% endhighlight %}

### enableConditionalFormatting `boolean`
{:#members:enableconditionalformatting}

Allows the user to format a specific set of cells based on the condition. 

**Default Value:** false

**Example:**

{% highlight html %}

$("#PivotGrid1").ejPivotGrid({ enableConditionalFormatting:true });

{% endhighlight %}


### enableDeferUpdate `boolean`
{:#members:enabledeferupdate}

Allows the user to refresh the control on-demand and not during every UI operation.

**Default Value:** false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({enableDeferUpdate: true});

{% endhighlight %}


### enableGroupingBar `boolean`
{:#members:enablegroupingbar}

Enables the display of GroupingBar allowing you to filter, sort and remove fields obtained from relational datasource.

**Default Value:** false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ enableGroupingBar:true });

{% endhighlight %}


### enableGrandTotal `boolean`
{:#members:enablegrandtotal}

Enables the display of grand total for rows and columns.

**Default Value:** true

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({enableGrandTotal: true});

{% endhighlight %}


### enableJSONRendering `boolean`
{:#members:enablejsonrendering}

Allows the user to load PivotGrid using JSON data.

**Default Value:** false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ enableJSONRendering: true });

{% endhighlight %}

### enablePivotFieldList `boolean`
{:#members:enablepivotfieldlist}

Enables rendering of PivotGrid widget along with the PivotTable Field List, which allows UI operation.

**Default Value:** true

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({enablePivotFieldList: true});

{% endhighlight %}

### enableRowGrandTotal `boolean`
{:#members:enablerowgrandtotal}

Enables the display of grand total for all the rows.

**Default Value:** true

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({enableRowGrandTotal: true});

{% endhighlight %}

### enableRTL `boolean`
{:#members:enablertl}

Allows the user to view PivotGrid from right to left.

**Default Value:** false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ enableRTL: true });

{% endhighlight %}

### enableToolTip `boolean`
{:#members:enabletooltip}

Allows the user to enable ToolTip option.

**Default Value:** false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ enableToolTip: true });

{% endhighlight %}

### enableVirtualScrolling `boolean`
{:#members:enablevirtualscrolling}

Allows the user to view large amount of data through virtual scrolling.

**Default Value:** false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ enableVirtualScrolling: true });

{% endhighlight %}

### hyperlinkSettings `object`
{:#members:hyperlinksettings}

Allows the user to configure hyperlink settings of PivotGrid control.

**Default Value:** {}

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ hyperlinkSettings: {enableValueCellHyperlink: true, enableRowHeaderHyperlink: true} });

{% endhighlight %}

### hyperlinkSettings.enableColumnHeaderHyperlink `boolean`
{:#members:hyperlinksettings-enablecolumnheaderhyperlink}

Allows the user to enable/diable hyperlink for column header.

**Default Value:** false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ hyperlinkSettings: { enableColumnHeaderHyperlink: true } });

{% endhighlight %}

### hyperlinkSettings.enableRowHeaderHyperlink `boolean`
{:#members:hyperlinksettings-enablerowheaderhyperlink}

Allows the user to enable/diable hyperlink for row header.

**Default Value:** false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ hyperlinkSettings: { enableRowHeaderHyperlink: true } });

{% endhighlight %}

### hyperlinkSettings.enableSummaryCellHyperlink `boolean`
{:#members:hyperlinksettings-enablesummarycellhyperlink}

Allows the user to enable/diable hyperlink for summary cells.

**Default Value:** false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ hyperlinkSettings: { enableSummaryCellHyperlink: true } });

{% endhighlight %}

### hyperlinkSettings.enableValueCellHyperlink `boolean`
{:#members:hyperlinksettings-enablevaluecellhyperlink}

Allows the user to enable/diable hyperlink for value cells.

**Default Value:** false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ hyperlinkSettings: { enableValueCellHyperlink: true } });

{% endhighlight %}

### isResponsive `boolean`
{:#members:isresponsive}

Allows the user to enable PivotGrid’s responsiveness in the browser layout.

**Default Value:** false

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ isResponsive: true });

{% endhighlight %}

### jsonRecords `string`
{:#members:jsonrecords}

Contains the serialized JSON string which renders PivotGrid.

**Default Value:** “”

### layout `enum`
{:#members:layout}

Sets the summary layout for PivotGrid. Following are the ways in which summary can be positioned: normal summary (bottom), top summary, no summary and excel-like summary.

**Default Value:** ej.PivotGrid.Layout.Normal

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

**Default Value:** "en-US"

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ locale: "en-US" }}); 

{% endhighlight %}


### operationalMode `object`
{:#members:operationalmode}

Sets the mode for the PivotGrid widget for binding data source either in server-side or client-side.

**Default Value:** ej.PivotGrid.OperationalMode.ClientMode

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({operationalMode: ej.PivotGrid.OperationalMode.ServerMode});

{% endhighlight %}

### serviceMethodSettings `object`
{:#members:servicemethodsettings}

Allows the user to set custom name for the methods at service-end, communicated during AJAX post.

**Default Value:** {}

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ serviceMethodSettings: { initialize: "InitializeGrid"} });

{% endhighlight %}

### serviceMethodSettings.drillDown `string`
{:#members:servicemethodsettings-drilldown}

Allows the user to set the custom name for the service method that&#39;s responsible for drill up/down operation in PivotGrid.

**Default Value:** "DrillGrid"

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ serviceMethodSettings: { drillDown: "DrillGridMyMethod" } });

{% endhighlight %}

### serviceMethodSettings.exportPivotGrid `string`
{:#members:servicemethodsettings-exportpivotgrid}

Allows the user to set the custom name for the service method that’s responsible for exporting.

**Default Value:** "Export"

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ serviceMethodSettings: { exportPivotGrid: "ExportMyMethod" } })

{% endhighlight %}

### serviceMethodSettings.deferUpdate `string`
{:#members:servicemethodsettings-deferupdate}

Allows the user to set the custom name for the service method that’s responsible for performing server-side actions on defer update.

**Default Value:** "DeferUpdate"

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ serviceMethodSettings: { deferUpdate: "DeferUpdateMethod" } });

{% endhighlight %}

### serviceMethodSettings.fetchMembers `string`
{:#members:servicemethodsettings-fetchmembers}

Allows the user to set the custom name for the service method that’s responsible to getting the values for the tree-view inside filter dialog.

**Default Value:** "FetchMembers"

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ serviceMethodSettings:  { fetchMembers: "FetchMembersMethod" } });

{% endhighlight %}
 
### serviceMethodSettings.filtering `string`
{:#members:servicemethodsettings-filtering}

Allows the user to set the custom name for the service method that's responsible for filtering operation in PivotGrid.

**Default Value:** "Filtering"

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ serviceMethodSettings:  { filtering : "FilteringMethod" } });

{% endhighlight %}
 
### serviceMethodSettings.initialize `string`
{:#members:servicemethodsettings-initialize}

Allows the user to set the custom name for the service method that&#39;s responsible for initializing PivotGrid.

**Default Value:** "InitializeGrid"

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ serviceMethodSettings: { initialize: "InitializeGrid" } });

{% endhighlight %}

### serviceMethodSettings.nodeDropped `string`
{:#members:servicemethodsettings-nodedropped}

Allows the user to set the custom name for the service method that's responsible for the server-side action, on dropping a node into Field List.

**Default Value:** "NodeDropped"

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ serviceMethodSettings: { nodeDropped: "nodedroppedMethod" } });

{% endhighlight %}

### serviceMethodSettings.nodeStateModified `string`
{:#members:servicemethodsettings-nodestatemodified}

Allows the user to set the custom name for the service method that’s responsible for the server-side action on changing the checked state of a node in Field List.

**Default Value:** "NodeStateModified"

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ serviceMethodSettings: { nodeStateModified: "NodeStateModifiedMethod" } });

{% endhighlight %}

### serviceMethodSettings.paging `string`
{:#members:servicemethodsettings-paging}

Allows the user to set the custom name for the service method that&#39;s responsible for performing paging operation in PivotGrid.

**Default Value:** "Paging"

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ serviceMethodSettings: { paging: "PagingMyMethod" } });

{% endhighlight %}

### serviceMethodSettings.sorting `string`
{:#members:servicemethodsettings-sorting}

Allows the user to set the custom name for the service method that's responsible for sorting operation in PivotGrid.

**Default Value:** "Sorting"

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({ serviceMethodSettings: { sorting: "SortingMethod" } });

{% endhighlight %}

### url `string`
{:#members:url}

Connects the service using the specified URL for any server updates.

**Default Value:** “”

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type">Object</td>
<td class="description">Event parameters from PivotGrid
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
<td class="name">{% highlight html %}
action{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">return the current action of PivotGrid control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">return the custom object bounds with PivotGrid control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">return the outer HTML of PivotGrid control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type">boolean</td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">returns the PivotGrid model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type">Object</td>
<td class="description">Event parameters from PivotGrid
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
<td class="name">{% highlight html %}
action{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">return the current action of PivotGrid control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">return the custom object bounds with PivotGrid control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">return the outer HTML of PivotGrid control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type">boolean</td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">returns the PivotGrid model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({
   beforeServiceInvoke: function (args) {}
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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type">Object</td>
<td class="description">Event parameters from PivotGrid.
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
<td class="name">{% highlight html %}
args{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">returns the original event args.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellPosition{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the cell position (row index and column index) in table.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellType{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the type of the cell.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
rowData{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the seriealized data of the header cells.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
uniqueName{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the unique name of levels/members.</td>
</tr>
</tbody>
</table>
</td>
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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type">Object</td>
<td class="description">Event parameters from PivotGrid.
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
<td class="name">{% highlight html %}
args{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">returns the original event args.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellvalue{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">Returns the selected cell values.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
rowheaders{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">Returns the selected value cells row headers.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
colheaders{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">Returns the selected value cells column headers.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
measure{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">Returns the selected value cells measure.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
measureValue{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">Return the row and column measure count.</td>
</tr>
</tbody>
</table>
</td>
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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type">Object</td>
<td class="description">Event parameters from Pivotgrid.
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
<td class="name">{% highlight html %}
args{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">returns the original event args.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellPosition{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the cell position (row index and column index) in table.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellType{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the type of the cell.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
rowData{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the seriealized data of the header cells.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
uniqueName{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the unique name of levels/members.</td>
</tr>
</tbody>
</table>
</td>
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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type">Object</td>
<td class="description">Event parameters from Pivotgrid
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type">boolean</td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">returns the Pivotgrid model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({
   drillSuccess: function (args) {}
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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type">Object</td>
<td class="description">Event parameters from Pivotgrid.
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
<td class="name">{% highlight html %}
args{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">returns the original event args.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
action{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the current action of Pivotgrid control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type">Object</td>
<td class="description">returns the custom object bounded with the control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the HTML of Pivotgrid control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type">boolean</td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">returns the Pivotgrid model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type">Object</td>
<td class="description">Event parameters from Pivotgrid.
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
<td class="name">{% highlight html %}
args{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">returns the original event args.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
action{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the current action of Pivotgrid control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type">Object</td>
<td class="description">returns the custom object bounded with the control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the HTML of Pivotgrid control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type">boolean</td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">returns the Pivotgrid model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type">Object</td>
<td class="description">Event parameters from Pivotgrid.
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
<td class="name">{% highlight html %}
args{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">returns the original event args.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
action{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the current action of Pivotgrid control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type">Object</td>
<td class="description">returns the custom object bounded with the control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the HTML of Pivotgrid control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
message{% endhighlight %}</td>
<td class="type">Object</td>
<td class="description">returns the error message with error code.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type">boolean</td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">returns the Pivotgrid model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type">Object</td>
<td class="description">Event parameters from Pivotgrid.
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
<td class="name">{% highlight html %}
args{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">returns the original event args.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
action{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the current action of Pivotgrid control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type">Object</td>
<td class="description">returns the custom object bounded with the control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the HTML of Pivotgrid control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type">boolean</td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">returns the Pivotgrid model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type">Object</td>
<td class="description">Event parameters from Pivotgrid.
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
<td class="name">{% highlight html %}
args{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">returns the original event args.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellPosition{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the cell position (row index and column index) in table.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellType{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the type of the cell.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
rowData{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the seriealized data of the header cells.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
uniqueName{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the unique name of levels/members.</td>
</tr>
</tbody>
</table>
</td>
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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type">Object</td>
<td class="description">Event parameters from Pivotgrid.
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
<td class="name">{% highlight html %}
args{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">returns the original event args.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellPosition{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the cell position (row index and column index) in table.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellType{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the type of the cell.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
rowData{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the seriealized data of the header cells.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
uniqueName{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the unique name of levels/members.</td>
</tr>
</tbody>
</table>
</td>
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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type">Object</td>
<td class="description">Event parameters from Pivotgrid.
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
<td class="name">{% highlight html %}
args{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">returns the original event args.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellPosition{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the cell position (row index and column index) in table.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellType{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the type of the cell.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
rowData{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the seriealized data of the header cells.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
uniqueName{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the unique name of levels/members.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({
   valueCellHyperlinkClick: function (args) {}
});      

{% endhighlight %}


## Enumeration

### AnalysisMode  `enum`
{:#enum:analysismode}

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
            <td class="name">Olap</td>
            <td class="description">To bind an OLAP data source to PivotGrid.</td>
        </tr>
        <tr>
            <td class="name">Relational</td>
            <td class="description">To bind a relational data source to PivotGrid.</td>
        </tr>
    </tbody>
</table>


**Example:**

{% highlight html %}

$("#PivotGrid1").ejPivotGrid({analysisMode: ej.PivotGrid.AnalysisMode.Olap});

{% endhighlight %}


### ExportOptions  `enum`
{:#enum:exportoptions}

Allows the user to set the exporting options for PivotGrid widget.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">Excel</td>
            <td class="description">To export PivotGrid in Excel format.</td>
        </tr>
        <tr>
            <td class="name">Word</td>
            <td class="description">To export PivotGrid in Word format.</td>
        </tr>
         <tr>
            <td class="name">PDF</td>
            <td class="description">To export PivotGrid in PDF format.</td>
        </tr>
         <tr>
            <td class="name">CSV</td>
            <td class="description">To export PivotGrid in CSV format.</td>
        </tr>
    </tbody>
</table> 

**Example:**

{% highlight html %}

$("#PivotGrid1").ejPivotGrid({ exportOptions: ej.PivotGrid.ExportOptions.Excel});

{% endhighlight %}

### Layout  `enum`
{:#enum:layout}

Allows the user to set the layout for PivotGrid.

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

$("#PivotGrid1").ejPivotGrid({ layout: ej.PivotGrid.Layout.Normal });

{% endhighlight %}


### OperationalMode  `enum`
{:#enum:operationalmode}

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


**Example:**

{% highlight html %}

$("#PivotGrid1").ejPivotGrid({operationalMode:ej.PivotGrid.OperationalMode.ServerMode});

{% endhighlight %}



