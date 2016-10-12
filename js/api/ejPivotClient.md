---
layout: post
title: Properties, Methods and Events of ejPivotClient Widget
documentation: API
platform: js
keywords: ejPivotClient, API, Essential JS PivotClient
metaname: 
metacontent: 
---

# PivotClient

PivotClient is an ad hoc analysis tool that can be easily bound to any OLAP and Relational datasource to provide a visual presentation of the information retrieved from the database.

#### Syntax

{% highlight javascript %}

    $(element).ejPivotClient()
{% endhighlight %}

#### Example

{% highlight html %}
 
    <div id="PivotClient1"></div> 
 
    <script>
        //Create PivotClient
        $("#PivotClient1").ejPivotClient(...);     
    </script>
{% endhighlight %}

#### Requires

* module: jQuery-3.0.0.min.js
* module: ej.core.js
* module: ej.data.js
* module: ej.globalize.js
* module: ej.touch.js
* module: ej.draggable.js
* module: ej.scroller.js
* module: ej.chart.js
* module: ej.synchart.js
* module: ej.rangescrollbar.js
* module: ej.tooltip.js
* module: ej.button.js
* module: ej.checkbox.js
* module: ej.dropdownlist.js
* module: ej.dialog.js
* module: ej.togglebutton.js
* module: ej.toolbar.js
* module: ej.maskedit.js
* module: ej.waitingpopup.js
* module: ej.menu.js
* module: ej.treeview.js
* module: ej.tab.js
* module: ej.pivot.common.js
* module: ej.pivotanalysis.base.js
* module: ej.olap.base.js
* module: ej.pivotchart.js
* module: ej.pivottreemap.js
* module: ej.pivotpager.js
* module: ej.pivotgrid.js
* module: ej.pivotschemadesigner.js
* module: ej.pivotclient.js

## Members

### analysisMode `enum`
{:#members:analysisMode}

<ts name = "ej.Pivot.AnalysisMode"/>

Sets the mode for the PivotClient widget for binding either OLAP or Relational data source.

#### Default Value: ej.Pivot.AnalysisMode.Pivot

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">Pivot</td>
            <td class="description">To bind Relational datasource to PivotClient widget</td>
        </tr>
        <tr>
            <td class="name">Olap</td>
            <td class="description">To bind OLAP datasource to PivotClient widget</td>
        </tr>
    </tbody>
</table>

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ analysisMode: ej.Pivot.AnalysisMode.Olap });
{% endhighlight %}

### chartType `enum`
{:#members:charttype}

<ts name = "ej.PivotChart.ChartTypes"/>

Allows the user to set the specific chart type for PivotChart inside PivotClient widget.

#### Default Value: ej.PivotChart.ChartTypes.Column

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">Line</td>
            <td class="description">To render a Line type for PivotChart.</td>
        </tr>
        <tr>
            <td class="name">Spline</td>
            <td class="description">To render a Spline type for PivotChart.</td>
        </tr>
        <tr>
            <td class="name">Column</td>
            <td class="description">To render a Column type for PivotChart.</td>
        </tr>
        <tr>
            <td class="name">Area</td>
            <td class="description">To render an Area type for PivotChart.</td>
        </tr>
        <tr>
            <td class="name">SplineArea</td>
            <td class="description">To render a SplineArea type for PivotChart.</td>
        </tr>
        <tr>
            <td class="name">StepLine</td>
            <td class="description">To render a StepLine type for PivotChart.</td>
        </tr>
        <tr>
            <td class="name">StepArea</td>
            <td class="description">To render a StepArea type for PivotChart.</td>
        </tr>
        <tr>
            <td class="name">Pie</td>
            <td class="description">To render a Pie type for PivotChart.</td>
        </tr>
        <tr>
            <td class="name">Bar</td>
            <td class="description">To render a Bar type for PivotChart.</td>
        </tr>
        <tr>
            <td class="name">StackingArea</td>
            <td class="description">To render a StackingArea type for PivotChart.</td>
        </tr>
        <tr>
            <td class="name">StackingColumn</td>
            <td class="description">To render a StackingColumn type for PivotChart.</td>
        </tr>
        <tr>
            <td class="name">StackingBar</td>
            <td class="description">To render a StackingBar type for PivotChart.</td>
        </tr>
        <tr>
            <td class="name">Pyramid</td>
            <td class="description">To render a Pyramid type for PivotChart.</td>
        </tr>
        <tr>
            <td class="name">Funnel</td>
            <td class="description">To render a Funnel type for PivotChart.</td>
        </tr>
        <tr>
            <td class="name">Doughnut</td>
            <td class="description">To render a Doughnut type for PivotChart.</td>
        </tr>
        <tr>
            <td class="name">Scatter</td>
            <td class="description">To render a Scatter type for PivotChart.</td>
        </tr>
        <tr>
            <td class="name">Bubble</td>
            <td class="description">To render a Bubble type for PivotChart.</td>
        </tr>
    </tbody>
</table>


**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ chartType: ej.PivotChart.ChartTypes.Spline });
{% endhighlight %}

### operationalMode `enum`
{:#members:operationalmode}

<ts name = "ej.Pivot.OperationalMode"/>

Sets the mode for the PivotClient widget for binding data source either in server-side or client-side.

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

#### Default Value: ej.Pivot.OperationalMode.ClientMode

**Example:**

{% highlight html %}
 
    $("#PivotClient1").ejPivotClient({ operationalMode: ej.Pivot.OperationalMode.ServerMode });

{% endhighlight %}

### clientExportMode `enum`
{:#members:clientExportMode}

<ts name = "ej.PivotClient.ClientExportMode"/>

Allows the user to set the content on exporting the PivotClient widget.

#### Default Value: ej.PivotClient.ClientExportMode.ChartAndGrid

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">ChartAndGrid</td>
            <td class="description">Exports both the PivotChart and PivotGrid on exporting.</td>
        </tr>
        <tr>
            <td class="name">ChartOnly</td>
            <td class="description">Exports the PivotChart control alone on exporting.</td>
        </tr>
        <tr>
            <td class="name">GridOnly</td>
            <td class="description">Exports the PivotGrid control alone on exporting.</td>
        </tr>
    </tbody>
</table>


**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ clientExportMode: ej.PivotClient.ClientExportMode.ChartOnly });
{% endhighlight %}

### cssClass `string`
{:#members:cssclass}

Specifies the CSS class to PivotClient to achieve custom theme.

#### Default Value: “”

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ cssClass: "Olive" });
{% endhighlight %}

### customObject `object`
{:#members:customobject}

Object utilized to pass additional information between client-end and service-end when the control functions in server-mode.

#### Default Value: {}

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ customObject: { "MyMessage": "Hi Syncfusion!!" } });
{% endhighlight %}

### dataSource `object`
{:#members:datasource}

Initializes the data source for the PivotClient widget, when it functions completely on client-side.

#### Default Value: {}

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient( { dataSource: { data: value } });
{% endhighlight %}

### dataSource.cube `string`
{:#members:datasource-cube}

Contains the respective Cube name from OLAP database as string type.

#### Default Value: “”

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { cube: "Adventure Works" } });
{% endhighlight %}


### dataSource.data `object`
{:#members:datasource-data}

Provides the raw data source for the PivotClient.

#### Default Value: null

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { data: value } });
{% endhighlight %}

### dataSource.catalog `string`
{:#members:datasource-catalog}

In connection with an OLAP database, this property contains the database name as string to fetch the data from the given connection string.

#### Default Value: “”

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient( { dataSource: { catalog: "databaseName" } } );
{% endhighlight %}


### dataSource.columns `array`
{:#members:datasource-columns}

Lists out the items to be arranged in column section of PivotClient.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { columns: itemsArray } });
{% endhighlight %}


### dataSource.columns.fieldName `string`
{:#members:datasource-columns-fieldname}

Allows the user to bind the item by using its unique name as field name.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { columns: [{ fieldName : "MyFieldName" }] } });
{% endhighlight %}

### dataSource.columns.fieldCaption `string`
{:#members:datasource-columns-fieldcaption}

Allows the user to set the display caption for an item.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { columns: [{ fieldCaption : "MyFieldCaption" }] } });
{% endhighlight %}

### dataSource.columns.advancedFilter `array`
{:#members:datasource-columns-advancedfilter}

Allows the user to filter the report by default using advanced filtering (excel-like) option for OLAP data source in client-mode.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { columns: [{ advancedFilter : itemArray }] } });
{% endhighlight %}

### dataSource.columns.advancedFilter.name `string`
{:#members:datasource-columns-advancedfilter-name}

Allows the user to provide level unique name to perform advanced filtering.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { columns: [{ advancedFilter : [{ name: "dimensionUniqueName" }] }] } });
{% endhighlight %}

### dataSource.columns.advancedFilter.labelFilterOperator `string`
{:#members:datasource-columns-advancedfilter-labelfilteroperator}

Allows the user to set the operator to perform Label filtering.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { columns: [{ advancedFilter : [{ labelFilterOperator: ej.olap.LabelFilterOptions.EndsWith }] }] } });
{% endhighlight %}

### dataSource.columns.advancedFilter.valueFilterOperator `string`
{:#members:datasource-columns-advancedfilter-valuefilteroperator}

Allows the user to set the operator to perform Value filtering.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { columns: [{ advancedFilter : [{ valueFilterOperator: ej.olap.ValueFilterOptions.Between }] }] } });
{% endhighlight %}

### dataSource.columns.advancedFilter.advancedFilterType `string`
{:#members:datasource-columns-advancedfilter-advancedfiltertype}

Allows the user to set the filtering type while performing advanced filtering.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { columns: [{ advancedFilter : [{ advancedFilterType:  ej.olap.AdvancedFilterType.LabelFilter}] }] } });
{% endhighlight %}

### dataSource.columns.advancedFilter.measure `string`
{:#members:datasource-columns-advancedfilter-measure}

In case of value filtering, this property contains the measure name to which the filter is applied.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { columns: [{ advancedFilter : [{ measure: "measureUniqueName", advancedFilterType: ej.olap.AdvancedFilterType.ValueFilter }] }] } });
{% endhighlight %}

### dataSource.columns.advancedFilter.values `string`
{:#members:datasource-columns-advancedfilter-values}

Allows the user to hold the filter operand values in advanced filtering.

#### Default Value: ""

**Example:**

{% highlight javascript %}
    
    //For Label Filters
    $("#PivotClient1").ejPivotClient({ dataSource: { columns: [{ advancedFilter : [{ labelFilterOperator: ej.olap.LabelFilterOptions.EndsWith, values:  ["002"] }] }] } });
{% endhighlight %}

{% highlight javascript %}
    
    //For Value Filters
    $("#PivotClient1").ejPivotClient({ dataSource: { columns: [{ advancedFilter : [{ valueFilterOperator: ej.olap.ValueFilterOptions.GreaterThan, values:  ["200"] }] }] } });
{% endhighlight %}


### dataSource.columns.isNamedSets `boolean`
{:#members:datasource-columns-isnamedsets}

Allows the user to indicate whether the added item is a named set or not. 

> **Note**: This is only applicable for OLAP datasource.

#### Default Value: false

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { columns: [{ fieldName: "[Core Product Group]", isNamedSets : true }] } });
{% endhighlight %}

### dataSource.columns.showSubTotal `boolean`
{:#members:datasource-columns-showsubtotal}

Shows/Hides the sub-total of the field. 

#### Default Value: true

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { columns: [{ fieldName: "Country", showSubTotal : false }] } });
{% endhighlight %}

### dataSource.columns.sortOrder `enum`
{:#members:datasource-columns-sortorder}

<ts name = "ej.PivotAnalysis.SortOrder"/>

Allows the user to set the sorting order of the members of the field.

#### Default Value: ej.PivotAnalysis.SortOrder.Ascending

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">Ascending</td>
            <td class="description">Sorts the members of the field in ascending order.</td>
        </tr>
        <tr>
            <td class="name">Descending</td>
            <td class="description">Sorts the members of the field in descending order.</td>
        </tr>
        <tr>
            <td class="name">None</td>
            <td class="description">Displays the members without sorting in any order.</td>
        </tr>
    </tbody>
</table>

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { columns: [{ fieldName: "Country", sortOrder : ej.PivotAnalysis.SortOrder.Descending }] } });
{% endhighlight %}

### dataSource.columns.drilledItems `array`
{:#members:datasource-drilleditems}

Contains the list of members which are drilled in the field.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { columns: [{ fieldName: "Country", drilledItems : ["Canada", "France"] }] } });
{% endhighlight %}

### dataSource.columns.filterItems `object`
{:#members:datasource-filteritems}

Applies filter to the field members.

#### Default Value: null

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { columns: [{ fieldName: "Country", filterItems : { filterType: ej.PivotAnalysis.FilterType.Exclude, values: ["Canada", "France"] } }] } });
{% endhighlight %}

### dataSource.columns.filterItems.filterType `enum`
{:#members:datasource-columns-filteritems-filtertype}

<ts name = "ej.PivotAnalysis.FilterType"/>

Sets the type of filter whether to include/exclude the mentioned values.

#### Default Value: ej.PivotAnalysis.FilterType.Exclude

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">Exclude</td>
            <td class="description">Excludes the specified values among the members of the field.</td>
        </tr>
        <tr>
            <td class="name">Include</td>
            <td class="description">Includes the specified values alone among the members of the field.</td>
        </tr>
    </tbody>
</table>

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { columns: [{ fieldName: "Country", filterItems : { filterType: ej.PivotAnalysis.FilterType.Include, values: valueArray } }] } });
{% endhighlight %}

### dataSource.columns.filterItems.values `array`
{:#members:datasource-filteritems}

Contains the collection of items to be included/excluded among the field members.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { columns: [{ fieldName: "Country", filterItems : { filterType: ej.PivotAnalysis.FilterType.Exclude, values: ["Canada", "France"] } }] } });
{% endhighlight %}

### dataSource.rows `array`
{:#members:datasource-rows}

Lists out the items to be arranged in row section of PivotClient.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { rows: itemsArray } });
{% endhighlight %}

### dataSource.rows.fieldName `string`
{:#members:datasource-rows-fieldname}

Allows the user to bind the item by using its unique name as field name.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { rows: [{ fieldName : "MyFieldName" }] } });
{% endhighlight %}

### dataSource.rows.fieldCaption `string`
{:#members:datasource-rows-fieldcaption}

Allows the user to set the display caption for an item.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { rows: [{ fieldCaption : "MyFieldCaption" }] } });
{% endhighlight %}

### dataSource.rows.advancedFilter `array`
{:#members:datasource-rows-advancedfilter}

Allows the user to filter the report by default using advanced filtering (excel-like) option for OLAP data source in client-mode.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { columns: [{ advancedFilter : itemArray }] } });
{% endhighlight %}

### dataSource.columns.advancedFilter.name `string`
{:#members:datasource-columns-advancedfilter-name}

Allows the user to provide level unique name to perform advanced filtering.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { columns: [{ advancedFilter : [{ name: "dimensionUniqueName" }] }] } });
{% endhighlight %}

### dataSource.columns.advancedFilter.labelFilterOperator `string`
{:#members:datasource-columns-advancedfilter-labelfilteroperator}

Allows the user to set the operator to perform Label filtering.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { columns: [{ advancedFilter : [{ labelFilterOperator: ej.olap.LabelFilterOptions.EndsWith }] }] } });
{% endhighlight %}

### dataSource.columns.advancedFilter.valueFilterOperator `string`
{:#members:datasource-columns-advancedfilter-valuefilteroperator}

Allows the user to set the operator to perform Value filtering.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { columns: [{ advancedFilter : [{ valueFilterOperator: ej.olap.ValueFilterOptions.Between }] }] } });
{% endhighlight %}

### dataSource.rows.advancedFilter `array`
{:#members:datasource-rows-advancedfilter}

Allows the user to filter the report by default using advanced filtering (excel-like) option for OLAP data source in client-mode.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { rows: [{ advancedFilter : itemArray }] } });
{% endhighlight %}

### dataSource.rows.advancedFilter.name `string`
{:#members:datasource-rows-advancedfilter-name}

Allows the user to provide level unique name to do advanced filtering (excel-like) for OLAP data source in client-mode.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { rows: [{ advancedFilter : [{ name: "dimensionUniqueName" }] }] } });
{% endhighlight %}

### dataSource.rows.advancedFilter.labelFilterOperator `string`
{:#members:datasource-rows-advancedfilter-labelfilteroperator}

Allows the user to set the operator for label filtering to do advanced filtering (excel-like) for OLAP data source in client-mode.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { rows: [{ advancedFilter : [{ labelFilterOperator: ej.olap.LabelFilterOptions.EndsWith }] }] } });
{% endhighlight %}

### dataSource.rows.advancedFilter.valueFilterOperator `string`
{:#members:datasource-rows-advancedfilter-valuefilteroperator}

Allows the user to set the operator for value filtering to do advanced filtering (excel-like) for OLAP data source in client-mode.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { rows: [{ advancedFilter : [{ valueFilterOperator: ej.olap.ValueFilterOptions.Between }] }] } });
{% endhighlight %}

### dataSource.rows.advancedFilter.advancedFilterType `string`
{:#members:datasource-rows-advancedfilter-advancedfiltertype}

Allows the user to set the filtering type while doing advanced filtering (excel-like) for OLAP data source in client-mode.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: {rows: [{ advancedFilter : [{ advancedFilterType:  ej.olap.AdvancedFilterType.LabelFilter }] }] } });
{% endhighlight %}

### dataSource.rows.advancedFilter.values `string`
{:#members:datasource-rows-advancedfilter-values}

Allows the user to holds the filter value in advanced filtering (excel-like) option for OLAP data source in client-mode.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { rows: [{ advancedFilter : [{ values:  ["002"] }] }] } });
{% endhighlight %}

### dataSource.rows.isNamedSets `boolean`
{:#members:datasource-rows-isnamedsets}

Allows the user to enable the usage of named set items in respective axis. This is only applicable for OLAP datasource.

#### Default Value: false

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { rows: [{ isNamedSets : true}]}});
{% endhighlight %}


### dataSource.values `array`
{:#members:datasource-values}

Lists out the items which supports calculation in PivotClient.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { values: itemsArray } });
{% endhighlight %}

### dataSource.values.measures `array`
{:#members:datasource-values[0]-measures}

This holds the list of unique names of measures to bind them from the cube.

> **Note**: This is applicable only for OLAP data source.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { values: [{ measures : itemsArray }] } });
{% endhighlight %}

### dataSource.values.axis `string`
{:#members:datasource-values[0]-axis}

Allows to set the axis name to place the measures items.

#### Default Value: “”

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { values: [{ axis : ej.olap.AxisName.Row }] } });
{% endhighlight %}

### dataSource.values.fieldName `string`
{:#members:datasource-values[0]-fieldname}

Allows the user to bind the item by its unique name as field name.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { values: [{ fieldName : value }] } });
{% endhighlight %}

### dataSource.values.fieldCaption `string`
{:#members:datasource-values[0]-fieldcaption}

Allows the user to set the display name for an item.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { values: [{ fieldCaption : value}] } });
{% endhighlight %}

### dataSource.enableAdvancedFilter `boolean`
{:#members:datasource-enableadvancedfilter}

Allows user to filter the members (by its name and values) through advanced filtering (excel-like) option for OLAP data source in client-mode.

#### Default Value: false

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { enableAdvancedFilter: true } });
{% endhighlight %}


### dataSource.filters `array`
{:#members:datasource-filters}

Lists out the items which supports filtering of values without displaying the members in UI in PivotClient.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { filters: itemsArray } });
{% endhighlight %}


### dataSource.filters.fieldName `string`
{:#members:datasource-filters-fieldname}

Allows the user to bind the item by using its unique name as field name.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { filters: [{ fieldName : value }] } });
{% endhighlight %}

### dataSource.filters.fieldCaption `string`
{:#members:datasource-filters-fieldcaption}

Allows the user to set the display name for an item.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { filters: [{ fieldCaption : value }] } });
{% endhighlight %}

### dataSource.reportName `string`
{:#members:datasource-reportName}

Sets a name to the report bound to the control.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { reportName: "Default Report" } });
{% endhighlight %}

### dataSource.pagerOptions `object`
{:#members:datasource-pageroptions}

Allows the set the page size and current page number for each axis on applying paging.

> **Note**: This is applicable only for binding OLAP data from client-side.

#### Default Value: {}

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { pagerOptions: value } }); 
{% endhighlight %}

### dataSource.pagerOptions.categoricalPageSize `number`
{:#members:datasource-pageroptions-categoricalpagesize}

Allows to set the number of categorical columns to be displayed in each page on applying paging.

> **Note**: This is applicable only for binding OLAP data from client-side.

#### Default Value: {}

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { pagerOptions: { categoricalPageSize: 10 } } }); 
{% endhighlight %}

### dataSource.pagerOptions.seriesPageSize `number`
{:#members:datasource-pageroptions-seriespagesize}

Allows to set the number of series rows to be displayed in each page on applying paging.

> **Note**: This is applicable only for binding OLAP data from client-side.

#### Default Value: {}

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { pagerOptions: { seriesPageSize: 5 } } }); 
{% endhighlight %}

### dataSource.pagerOptions.categoricalCurrentPage `number`
{:#members:datasource-pageroptions-categoricalcurrentpage}

Allows to set the page number in categorical axis to be loaded by default.

> **Note**: This is applicable only for binding OLAP data from client-side.

#### Default Value: {}

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { pagerOptions: { categoricalCurrentPage: 3 } } }); 
{% endhighlight %}

### dataSource.pagerOptions.seriesCurrentPage `number`
{:#members:datasource-pageroptions-seriescurrentpage}

Allows to set the page number in series axis to be loaded by default.

> **Note**: This is applicable only for binding OLAP data from client-side.

#### Default Value: {}

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ dataSource: { pagerOptions: { seriesCurrentPage: 7 } } }); 
{% endhighlight %}

### displaySettings `object`
{:#members:displaysettings}

Allows the user to customize the widget's layout and appearance.

#### Default Value: {}

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ displaySettings: settingsObject });
{% endhighlight %}

### displaySettings.controlPlacement `enum`
{:#members:displaysettings-controlplacement}

<ts name = "ej.PivotClient.ControlPlacement"/>

Lets the user to customize the display of PivotChart and PivotGrid widgets, either in tabs or tiles.

#### Default Value: ej.PivotClient.ControlPlacement.Tab

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">Tab</td>
            <td class="description">Displays PivotChart and PivotGrid widgets in separate tabs.</td>
        </tr>
        <tr>
            <td class="name">Tile</td>
            <td class="description">Displays PivotChart and PivotGrid widgets one above the other.</td>
        </tr>
    </tbody>
</table>


**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ displaySettings: { controlPlacement: ej.PivotClient.ControlPlacement.Tile } });
{% endhighlight %}

### displaySettings.defaultView `enum`
{:#members:displaysettings-defaultview}

<ts name = "ej.PivotClient.DefaultView"/>

Lets the user to set either Chart or Grid as the start-up widget.

#### Default Value: ej.PivotClient.DefaultView.Grid

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">Chart</td>
            <td class="description">To set PivotChart as a default control in view.</td>
        </tr>
        <tr>
            <td class="name">Grid</td>
            <td class="description">To set PivotGrid as a default control in view.</td>
        </tr>
    </tbody>
</table>


**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ displaySettings: { defaultView: ej.PivotClient.DefaultView.Chart } });
{% endhighlight %}

### displaySettings.enableFullScreen `boolean`
{:#members:displaysettings-enablefullscreen}

Lets the user to have an option for switching to full screen view of PivotChart and PivotGrid from default view in PivotClient.

#### Default Value: false

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ displaySettings: { enableFullScreen: true } });
{% endhighlight %}

### displaySettings.enableTogglePanel `boolean`
{:#members:displaysettings-enabletogglepanel}

Enables an option to enhance the space for PivotGrid and PivotChart by hiding Cube Browser and Axis Element Builder.

#### Default Value: false

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ displaySettings: { enableTogglePanel: true } });
{% endhighlight %}

### displaySettings.isResponsive `boolean`
{:#members:displaysettings-isresponsive}

Allows the user to enable PivotClient’s responsiveness in the browser layout.

#### Default Value: false

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ displaySettings: { isResponsive: true } });
{% endhighlight %}

### displaySettings.mode `enum`
{:#members:displaysettings-mode}

<ts name = "ej.PivotClient.DisplayMode"/>

Sets the display mode (Only Chart/Only Grid/Both) in PivotClient.

#### Default Value: ej.PivotClient.DisplayMode.ChartAndGrid

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">ChartOnly</td>
            <td class="description">To display only PivotChart widget.</td>
        </tr>
        <tr>
            <td class="name">GridOnly</td>
            <td class="description">To display only PivotGrid widget.</td>
        </tr>
        <tr>
            <td class="name">ChartAndGrid</td>
            <td class="description">To display both PivotChart and PivotGrid widgets.</td>
        </tr>
    </tbody>
</table>


**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ displaySettings: { mode: ej.PivotClient.DisplayMode.ChartOnly } });
{% endhighlight %}

### enableAdvancedFilter `boolean`
{:#members:enableadvancedfilter}

Enables the advanced filtering options Value Filtering, Label Filtering and Sorting for each dimensions on binding OLAP data.

#### Default Value: false

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ enableAdvancedFilter: true });
{% endhighlight %}

### enableDeferUpdate `boolean`
{:#members:enabledeferupdate}

Allows the user to refresh the control on-demand and not during every UI operation. 

> **Note**: This property is applicable for OLAP data bound from server-side alone.

#### Default Value: false

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ enableDeferUpdate: true });
{% endhighlight %}

### enableLocalStorage `boolean`
{:#members:enablelocalstorage}

Lets the user to save and load reports in a customized way with the help of events. 

#### Default Value: false

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ enableLocalStorage: true });
{% endhighlight %}

### enablePaging `boolean`
{:#members:enablepaging}

Allows the user to enable paging for both the PivotChart and PivotGrid components for the ease of viewing large data.

> **Note**: This property is applicable OLAP data bound from client-side alone.

#### Default Value: false

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ enablePaging: true });
{% endhighlight %}

### enablePivotTreeMap `boolean`
{:#members:enablepivottreemap}

Allows the user to include the PivotTreeMap component as one of the chart types.

> **Note**: This property is applicable for OLAP data bound from server-side alone.

#### Default Value: false

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ enablePivotTreeMap: true });
{% endhighlight %}

### enableRTL `boolean`
{:#members:enablertl}

Allows the user to view the layout of PivotClient from right to left.

#### Default Value: false

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ enableRTL: true });
{% endhighlight %}

### enableMeasureGroups `boolean`
{:#members:enablemeasuregroups}

Enables/disables the visibility of measure group selector drop-down in Cube Browser.

> **Note**: This property is applicable only for OLAP data source bound from server-side.

#### Default Value: false

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ enableMeasureGroups : true });
{% endhighlight %}

### enableVirtualScrolling `boolean`
{:#members:enablevirtualscrolling}

Allows the user to enable virtual scrolling for both the PivotChart and PivotGrid components for the ease of viewing large data. 

> **Note**: This is applicable only for OLAP data.

#### Default Value: false

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ enableVirtualScrolling: true });
{% endhighlight %}

### enableMemberEditorPaging `boolean`
{:#members:enablemembereditorpaging}

Enables/Disables paging in Member Editor for viewing the large count of members in pages. 

> **Note**: This property is applicable only for OLAP data.

#### Default Value: false

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ enableMemberEditorPaging: true });
{% endhighlight %}

### memberEditorPageSize `number`
{:#members:memberEditorPageSize}

Allows the user to set the number of members to be displayed in each page of Member Editor on applying paging in it. 

> **Note**: This property is applicable only for OLAP data.

#### Default Value: 100

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ memberEditorPageSize: 50 });
{% endhighlight %}

### gridLayout `enum`
{:#members:gridlayout}

<ts ref = "ej.PivotGrid.Layout"/>

Sets the summary layout for PivotGrid. Following are the ways in which summary can be positioned: normal summary (bottom), top summary, no summary and excel-like summary.

> **Note**: This property is applicable only for OLAP data bound from server-side.

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

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ gridLayout: ej.PivotGrid.Layout.NoSummaries });
{% endhighlight %}

### locale `string`
{:#members:locale}

Allows the user to set the localized language for the widget.

#### Default Value: "en-US"

**Example:** 

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ locale: "fr-FR" });
{% endhighlight %}

### operationalMode `enum`
{:#members:operationalmode}

<ts name = "ej.Pivot.OperationalMode"/>

Sets the mode for the PivotClient widget for binding data source either in server-side or client-side.

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

#### Default Value: ej.Pivot.OperationalMode.ClientMode

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ operationalMode: ej.Pivot.OperationalMode.ServerMode });
{% endhighlight %}

### serviceMethodSettings `object`
{:#members:servicemethodsettings}

Allows the user to set custom name for the methods at service-end, communicated during AJAX post.

> **Note**: This property is applicable only on operating the control from server-side.

#### Default Value: {}

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ serviceMethodSettings: value });
{% endhighlight %}

### serviceMethodSettings.cubeChanged `string`
{:#members:servicemethodsettings-cubechanged}

Allows the user to set the custom name for the service method responsible for updating the entire report and widget, while changing the Cube.

#### Default Value: "CubeChanged"

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ serviceMethodSettings: { cubeChanged: "CubeChangedMyMethod" } });
{% endhighlight %}

### serviceMethodSettings.exportPivotClient `string`
{:#members:servicemethodsettings-exportpivotclient}

Allows the user to set the custom name for the service method responsible for exporting.

#### Default Value: "Export"

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ serviceMethodSettings: { exportPivotClient: "ExportMyMethod" } }); 
{% endhighlight %}

### serviceMethodSettings.fetchMemberTreeNodes `string`
{:#members:servicemethodsettings-fetchmembertreenodes}

Allows the user to set the custom name for the service method responsible to get the members for the tree-view, inside member-editor dialog.

#### Default Value: "FetchMemberTreeNodes"

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ serviceMethodSettings: { fetchMemberTreeNodes: "FetchMemberTreeNodesMyMethod" } }); 
{% endhighlight %}

### serviceMethodSettings.fetchReportList `string`
{:#members:servicemethodsettings-fetchreportlist}

Allows the user to set the custom name for the service method responsible for fetching the report names from the database.

#### Default Value: "FetchReportListFromDB"

**Example:**

{% highlight javascript %}
                     
    $("#PivotClient1").ejPivotClient({ serviceMethodSettings: { fetchReportList: "FetchReportListFromDBMyMethod" } }); 
{% endhighlight %}

### serviceMethodSettings.filterElement `string`
{:#members:servicemethodsettings-filterelement}

Allows the user to set the custom name for the service method responsible for updating report while filtering members.

#### Default Value: "FilterElement"

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ serviceMethodSettings: { filterElement: "filterElementMyMethod" } }); 
{% endhighlight %}

### serviceMethodSettings.initialize `string`
{:#members:servicemethodsettings-initialize}

Allows the user to set the custom name for the service method responsible for initializing PivotClient.

#### Default Value: "InitializeClient"

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ serviceMethodSettings: { initialize: "InitializeClientMyMethod" } }); 
{% endhighlight %}

### serviceMethodSettings.loadReport `string`
{:#members:servicemethodsettings-loadreport}

Allows the user to set the custom name for the service method responsible for loading a report collection from the database.

#### Default Value: "LoadReportFromDB"

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ serviceMethodSettings: { loadReport: "LoadReportFromDBMyMethod" } }); 
{% endhighlight %}

### serviceMethodSettings.mdxQuery `string`
{:#members:servicemethodsettings-mdxquery}

Allows the user to set the custom name for the service method responsible for retrieving the MDX query for the current report.

#### Default Value: "GetMDXQuery"

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ serviceMethodSettings: { mdxQuery: "GetMDXQueryMyMethod" } });
{% endhighlight %}

### serviceMethodSettings.measureGroupChanged `string`
{:#members:servicemethodsettings-measuregroupchanged}

Allows the user to set the custom name for the service method responsible for updating the tree-view inside Cube Browser, while changing the measure group.

#### Default Value: "MeasureGroupChanged"

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ serviceMethodSettings: { measureGroupChanged: "MeasureGroupChangedMyMethod" } }); 
{% endhighlight %}

### serviceMethodSettings.memberExpand `string`
{:#members:servicemethodsettings-memberexpand}

Allows the user to set the custom name for the service method responsible to get the child members, on tree-view node expansion.

#### Default Value: "MemberExpanded"

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ serviceMethodSettings: { memberExpand: "MemberExpandedMyMethod" } });
{% endhighlight %}

### serviceMethodSettings.nodeDropped `string`
{:#members:servicemethodsettings-nodedropped}

Allows the user to set the custom name for the service method responsible for updating report while dropping a node/SplitButton inside Axis Element Builder.

#### Default Value: "NodeDropped"

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ serviceMethodSettings: { nodeDropped: "NodeDroppedMyMethod" } }); 
{% endhighlight %}

### serviceMethodSettings.removeSplitButton `string`
{:#members:servicemethodsettings-removesplitbutton}

Allows the user to set the custom name for the service method responsible for updating report while removing SplitButton from Axis Element Builder.

#### Default Value: "RemoveSplitButton"

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ serviceMethodSettings: { removeSplitButton: "RemoveSplitButtonMyMethod" } }); 
{% endhighlight %}

### serviceMethodSettings.saveReport `string`
{:#members:servicemethodsettings-savereport}

Allows the user to set the custom name for the service method responsible for saving the report collection to database.

#### Default Value: "SaveReportToDB"

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ serviceMethodSettings: { saveReport: "SaveReportToDBMyMethod" } }); 
{% endhighlight %}

### serviceMethodSettings.toggleAxis `string`
{:#members:servicemethodsettings-toggleaxis}

Allows the user to set the custom name for the service method responsible for toggling the elements in row and column axes.

#### Default Value: "ToggleAxis"

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ serviceMethodSettings: { toggleAxis: "ToggleAxisMyMethod" } });
{% endhighlight %}

### serviceMethodSettings.toolbarServices `string`
{:#members:servicemethodsettings-toolbarservices}

Allows the user to set the custom name for the service method responsible for all the toolbar operations.

#### Default Value: "ToolbarOperations"

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ serviceMethodSettings: { toolbarServices: "ToolbarOperationsMyMethod" } }); 
{% endhighlight %}

### serviceMethodSettings.updateReport `string`
{:#members:servicemethodsettings-updatereport}

Allows the user to set the custom name for the service method responsible for updating report collection.

#### Default Value: "UpdateReport"

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({  serviceMethodSettings: { updateReport: "UpdateReportFromMyMethod" } }); 
{% endhighlight %}

### serviceMethodSettings.paging `string`
{:#members:servicemethodsettings-paging}

Allows the user to set the custom name for the service method responsible on navigating between pages in paged PivotClient.

#### Default Value: "Paging"

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({  serviceMethodSettings: { paging: "PagingMyMethod" } }); 
{% endhighlight %}

### title `string`
{:#members:title}

Sets the title for PivotClient widget.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ title: "OLAP Browser" });
{% endhighlight %}

### url `string`
{:#members:url}

Connects the service using the specified URL for any server updates.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({ url: "/wcf/OlapClientService.svc" });
{% endhighlight %}

## Methods

### doAjaxPost()
{:#methods:doajaxpost}

Performs an asynchronous HTTP (AJAX) request.

**Example:**

{% highlight html %}
 
    <div id="PivotClient1"></div> 
    
    <script>
        $('#PivotClient1').ejPivotClient({
            //...
        });
        var clientObj = $("#PivotClient1").data("ejPivotClient");
        clientObj.doAjaxPost("POST", "/OlapClientService.svc/Initialize", {"key", "Hello World"}, "renderControlSuccess", null);
    </script>

{% endhighlight %}

### doPostBack()
{:#methods:dopostback}

Performs an asynchronous HTTP (FullPost) submit.

**Example:**

{% highlight html %}

    <div id="PivotClient1"></div> 
    
    <script>
        $('#PivotClient1').ejPivotClient({
            //...
        });
        var clientObj = $("#PivotClient1").data("ejPivotClient");
        clientObj.doPostBack("/OlapClientService.svc/Initialize", {"key", "Hello World"});
    </script>
{% endhighlight %}

### refreshPagedPivotClient()
{:#methods:refreshpagedpivotclient}

Navigates to the specified page in specified axis.

**Example:**

{% highlight html %}
 
    <div id="PivotClient1"></div> 
    
    <script>
        $('#PivotClient1').ejPivotClient({
            //...
        });
        var clientObj = $("#PivotClient1").data("ejPivotClient");
        clientObj.refreshPagedPivotClient("series", 24);//Loads the 24th page in series axis
    </script>
{% endhighlight %}

### refreshPagedPivotClientSuccess()
{:#methods:refreshpagedpivotclientsuccess}

Updates the PivotClient component with the JSON data fetched from the service on navigating between pages.

**Example:**

{% highlight html %}
 
    <div id="PivotClient1"></div> 
    
    <script>
        $('#PivotClient1').ejPivotClient({
            //...
        });
        var clientObj = $("#PivotClient1").data("ejPivotClient");
        clientObj.refreshPagedPivotClientSuccess(jsonData); //jsonData object holds the JSON data required to render a specific page of the control
    </script>
{% endhighlight %}

### generateJSON()
{:#methods:generatejson}

Renders the PivotChart and PivotGrid with the JSON data provided.

**Example:**

{% highlight html %}
 
    <div id="PivotClient1"></div> 
    
    <script>
        $('#PivotClient1').ejPivotClient({
            //...
        });
        var clientObj = $("#PivotClient1").data("ejPivotClient");
        clientObj.generateJSON(jsonData);//jsonData object holds the data in JSON format required to render the control
    </script>
{% endhighlight %}

### refreshControl()
{:#methods:refreshcontrol}

Re-renders the control with the report at that instant.

> **Note**: This method could be used only for client-side operation.

**Example:**

{% highlight html %}
 
    <div id="PivotClient1"></div> 
    
    <script>
        $('#PivotClient1').ejPivotClient({
            //...
        });
        var clientObj = $("#PivotClient1").data("ejPivotClient");
        clientObj.refreshControl();
    </script>
{% endhighlight %}

### getOlapReport()
{:#methods:getolapreport}

Returns the OlapReport string maintained along with the axis elements information.

**Example:**

{% highlight html %}
 
    <div id="PivotClient1"></div> 
    
    <script>
        $('#PivotClient1').ejPivotClient({
            //...
        });
        var clientObj = $("#PivotClient1").data("ejPivotClient");
        var report = clientObj.getOlapReport();
    </script>
{% endhighlight %}

### setOlapReport()
{:#methods:setolapreport}

Sets the OlapReport string along with the axis information and maintains it in a property.

**Example:**

{% highlight html %}
 
    <div id="PivotClient1"></div> 
    
    <script>
        $('#PivotClient1').ejPivotClient({
            //...
        });
        var clientObj = $("#PivotClient1").data("ejPivotClient");
        clientObj.setOlapReport(olapReportObj);
    </script>
{% endhighlight %}

### getJSONRecords()
{:#methods:getjsonrecords}

Returns the JSON records formed to render the control.

**Example:**

{% highlight html %}
 
    <div id="PivotClient1"></div> 
    
    <script>
        $('#PivotClient1').ejPivotClient({
            //...
        });
        var clientObj = $("#PivotClient1").data("ejPivotClient");
        var jsonRecords = clientObj.getJSONRecords();
    </script>
{% endhighlight %}

### setJSONRecords()
{:#methods:setjsonrecords}

Sets the JSON records formed to render the control to a property.

**Example:**

{% highlight html %}
 
    <div id="PivotClient1"></div> 
    
    <script>
        $('#PivotClient1').ejPivotClient({
            //...
        });
        var clientObj = $("#PivotClient1").data("ejPivotClient");
        clientObj.setJSONRecords(jsonRecords);
    </script>
{% endhighlight %}

## Events

### afterServiceInvoke
{:#events:afterserviceinvoke}

Triggers when it reaches client-side after any AJAX request.

Below are the event parameters from PivotClient component.

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
<td class="description last">returns the current action of PivotClient control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">returns the custom object bounds with PivotClient control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">object</td>
<td class="description last">returns the HTML element of PivotClient control.</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({
        afterServiceInvoke: function(args) { }
    });
{% endhighlight %}



### beforeServiceInvoke
{:#events:beforeserviceinvoke}

Triggers before any AJAX request is passed from client-side to service methods.

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
<td class="description last">returns the current action of PivotClient control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">returns the custom object bounds with PivotClient control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">object</td>
<td class="description last">returns the HTML element of PivotClient control.</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({
        beforeServiceInvoke: function(args) { }
    });
{% endhighlight %}

### saveReport
{:#events:savereport}

Triggers before saving the current collection of reports.

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
<td class="description last">returns the current instance of PivotClient control.</td>
</tr>
<tr>
<td class="name">saveReportSetting</td>
<td class="type">object</td>
<td class="description last">returns the object which holds the necessary parameteres required for saving the report collection.</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({
        saveReport: function(args) { }
    });
{% endhighlight %}

### loadReport
{:#events:loadreport}

Triggers before loading a saved collection of reports.

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
<td class="description last">returns the current instance of PivotClient control.</td>
</tr>
<tr>
<td class="name">loadReportSetting</td>
<td class="type">object</td>
<td class="description last">returns the object which holds the necessary parameteres required for loading a report collection from database.</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({
        loadReport: function(args) { }
    });

{% endhighlight %}

### fetchReport
{:#events:fetchreport}

Triggers before fetching the report collection from storage.

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
<td class="description last">returns the current instance of PivotClient control.</td>
</tr>
<tr>
<td class="name">fetchReportSetting</td>
<td class="type">object</td>
<td class="description last">returns the object which holds the necessary parameteres required for fetching the report names stored in database.</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({
        fetchReport: function(args) { }
    });

{% endhighlight %}

### beforeExport
{:#events:beforeexport}

Triggers before exporting the control.

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
<td class="description last">holds the url of the service method responsible for exporting the PivotClient control.</td>
</tr>
<tr>
<td class="name">fileName</td>
<td class="type">string</td>
<td class="description last">holds the name of the file to be exported.</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({
        beforeExport: function(args) { }
    });
{% endhighlight %}

### chartLoad
{:#events:chartload}

Triggers before rendering the PivotChart.

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
<td class="description last">returns the current action of PivotChart control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">returns the custom object bound with PivotChart control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">object</td>
<td class="description last">returns the HTML element of PivotChart control.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({
        chartLoad: function (args) { }
    });      

{% endhighlight %}

### treeMapLoad
{:#events:treemapload}

Triggers before rendering the PivotTreeMap.

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
<td class="description last">returns the current action of PivotTreeMap control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">returns the custom object bound with PivotTreeMap control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">object</td>
<td class="description last">returns the HTML element of PivotTreeMap control.</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({
        treeMapLoad: function (args) { }
    });
{% endhighlight %}

### load
{:#events:load}

Triggers while we initiate loading of the widget.

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
<td class="type">object</td>
<td class="description last">returns the HTML tag of PivotClient component.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">returns the custom object bound with PivotTreeMap control.</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({
        load: function (args) { }
    });
{% endhighlight %}


### renderComplete
{:#events:rendercomplete}

Triggers when PivotClient widget completes all operations at client-end after any AJAX request. 

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
<td class="type">object</td>
<td class="description last">returns the HTML tag of PivotClient component.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">returns the custom object bound with PivotTreeMap control.</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({
        renderComplete: function (args) { }
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
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">returns the custom object bound with the control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">object</td>
<td class="description last">returns the HTML element of PivotClient control.</td>
</tr>
<tr>
<td class="name">message</td>
<td class="type">string</td>
<td class="description last">returns the error message with error code.</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({
        renderFailure: function (args) { }
    });     

{% endhighlight %}

### renderSuccess
{:#events:rendersuccess}

Triggers when PivotClient successfully completes rendering.

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
<td class="description last">returns the object of PivotClient control at that instant.</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight javascript %}
 
    $("#PivotClient1").ejPivotClient({
        renderSuccess: function (args) { }
    });      

{% endhighlight %}


## Enumeration

### ClientExportMode `enum`
{:#enum:clientexportmode}

<ts name = "ej.PivotClient.ClientExportMode"/>

Sets the mode to export the OLAP visualization components such as PivotChart and PivotGrid in PivotClient. Based on the option, either Chart or Grid or both gets exported.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">ChartAndGrid</td>
            <td class="description">To export both PivotGrid and PivotChart contents.</td>
        </tr>
        <tr>
            <td class="name">ChartOnly</td>
            <td class="description">To export only PivotChart contents.</td>
        </tr>
        <tr>
            <td class="name">GridOnly</td>
            <td class="description">To export only PivotGrid contents.</td>
        </tr>
    </tbody>
</table>

**Example:**

{% highlight javascript %}

    $("#PivotClient1").ejPivotClient({ clientExportMode: ej.PivotClient.ClientExportMode.ChartAndGrid });
{% endhighlight %}

### ControlPlacement `enum`
{:#enum:controlplacement}

<ts name = "ej.PivotClient.ControlPlacement" />

Sets the display of the PivotChart and PivotGrid either in separate tabs or one above another (in tiles).

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">Tab</td>
            <td class="description">Displays PivotGrid and PivotChart in separate tabs.</td>
        </tr>
        <tr>
            <td class="name">Tile</td>
            <td class="description">Displays PivotGrid and PivotChart one above another.</td>
        </tr>
    </tbody>
</table>

**Example:**

{% highlight javascript %}

    $("#PivotClient1").ejPivotClient({ displaySettings: { controlPlacement: ej.PivotClient.ControlPlacement.Tile } });
{% endhighlight %}

### DisplayMode `enum`
{:#enum:displaymode}

<ts name = "ej.PivotClient.DisplayMode" />

Sets the option to render PivotClient widget either with both PivotChart and PivotGrid or with any one of them.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">ChartOnly</td>
            <td class="description">Renders PivotChart only within PivotClient.</td>
        </tr>
        <tr>
            <td class="name">GridOnly</td>
            <td class="description">Renders PivotGrid only within PivotClient.</td>
        </tr>
        <tr>
            <td class="name">ChartAndGrid</td>
            <td class="description">Renders both PivotChart and PivotGrid within PivotClient.</td>
        </tr>
    </tbody>
</table>

**Example:**

{% highlight javascript %}

    $("#PivotClient1").ejPivotClient({ displaySettings: { mode: ej.PivotClient.DisplayMode.ChartOnly } });
{% endhighlight %}

### DefaultView `enum`
{:#enum:defaultview}

<ts name = "ej.PivotClient.DefaultView" />

Sets either PivotChart or PivotGrid as default component in initial loading view.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">Chart</td>
            <td class="description">Sets PivotChart as the default control.</td>
        </tr>
        <tr>
            <td class="name">Grid</td>
            <td class="description">Sets PivotGrid as the default control.</td>
        </tr>
    </tbody>
</table>

**Example:**

{% highlight javascript %}

    $("#PivotClient1").ejPivotClient({ displaySettings: { defaultView: ej.PivotClient.DefaultView.Chart } });
{% endhighlight %}