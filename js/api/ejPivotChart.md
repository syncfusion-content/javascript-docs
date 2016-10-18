---
layout: post
title: Properties, Methods and Events of ejPivotChart Widget
documentation: API
platform: js
keywords: ejPivotChart, API, Essential JS PivotChart
metaname: 
metacontent: 
---

# ejPivotChart

The PivotChart is a lightweight control that reads OLAP and Relational information and visualizes it in graphical format with the ability to drill up and down.

#### Syntax

{% highlight javascript %}

    $(element).ejPivotChart()
{% endhighlight %}


#### Example

{% highlight html %}
 
    <div id="PivotChart1"></div>

    <script>
        //Create PivotChart
        $("#PivotChart1").ejPivotChart(...);
    </script>

{% endhighlight %}

#### Requires

* module:jQuery-3.0.0.min.js
* module:ej.core.js
* module:ej.data.js
* module:ej.touch.js
* module:ej.dialog.js
* module:ej.draggable.js
* module:ej.waitingpopup.js
* module:ej.chart.js
* module:ej.pivot.common.js
* module:ej.olap.base.js
* module:ej.pivotanalysis.base.js
* module:ej.pivotchart.js


## Members

### analysisMode `enum`
{:#members:analysismode}

<ts ref = "ej.Pivot.AnalysisMode"/>

Sets the mode for the PivotChart widget for binding either OLAP or Relational data source.

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
            <td class="description">To bind Relational datasource to PivotChart widget</td>
        </tr>
        <tr>
            <td class="name">Olap</td>
            <td class="description">To bind OLAP datasource to PivotChart widget</td>
        </tr>
    </tbody>
</table>

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ analysisMode: ej.Pivot.AnalysisMode.Olap });
{% endhighlight %}


### cssClass `string`
{:#members:cssclass}

Specifies the CSS class to PivotChart to achieve custom theme.

#### Default Value: “”

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ cssClass : "olive" });
{% endhighlight %}

### commonSeriesOptions `object`
{:#members:commonseriesoptions}

Options available to configure the properties of entire series. You can also override the options for specific series by using series collection.

#### Default Value: {}

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ commonSeriesOptions: { type: ej.PivotChart.ChartTypes.Line } });
{% endhighlight %}

### commonSeriesOptions.type `enum`
{:#members:commonseriesoptions-type}

<ts name = "ej.PivotChart.ChartTypes"/>

Allows the user to set the specific chart type for PivotChart widget.

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
            <td class="description">To render a Line type PivotChart.</td>
        </tr>
        <tr>
            <td class="name">Spline</td>
            <td class="description">To render a Spline type PivotChart.</td>
        </tr>
        <tr>
            <td class="name">Column</td>
            <td class="description">To render a Column type PivotChart.</td>
        </tr>
        <tr>
            <td class="name">Area</td>
            <td class="description">To render an Area type PivotChart.</td>
        </tr>
        <tr>
            <td class="name">SplineArea</td>
            <td class="description">To render a SplineArea type PivotChart.</td>
        </tr>
        <tr>
            <td class="name">StepLine</td>
            <td class="description">To render a StepLine type PivotChart.</td>
        </tr>
        <tr>
            <td class="name">StepArea</td>
            <td class="description">To render a StepArea type PivotChart.</td>
        </tr>
        <tr>
            <td class="name">Pie</td>
            <td class="description">To render a Pie type PivotChart.</td>
        </tr>
        <tr>
            <td class="name">Bar</td>
            <td class="description">To render a Bar type PivotChart.</td>
        </tr>
        <tr>
            <td class="name">StackingArea</td>
            <td class="description">To render a StackingArea type PivotChart.</td>
        </tr>
        <tr>
            <td class="name">StackingColumn</td>
            <td class="description">To render a StackingColumn type PivotChart.</td>
        </tr>
        <tr>
            <td class="name">StackingBar</td>
            <td class="description">To render a StackingBar type PivotChart.</td>
        </tr>
        <tr>
            <td class="name">Pyramid</td>
            <td class="description">To render a Pyramid type PivotChart.</td>
        </tr>
        <tr>
            <td class="name">Funnel</td>
            <td class="description">To render a Funnel type PivotChart.</td>
        </tr>
        <tr>
            <td class="name">Doughnut</td>
            <td class="description">To render a Doughnut type PivotChart.</td>
        </tr>
        <tr>
            <td class="name">Scatter</td>
            <td class="description">To render a Scatter type PivotChart.</td>
        </tr>
        <tr>
            <td class="name">Bubble</td>
            <td class="description">To render a Bubble type PivotChart.</td>
        </tr>
    </tbody>
</table>


**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ commonSeriesOptions: { type: ej.PivotChart.ChartTypes.Spline } });
{% endhighlight %}

### dataSource `object`
{:#members:datasource}

Initializes the data source for the PivotChart widget, when it functions completely on client-side.

#### Default Value: {}

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart( { dataSource: { data: value } });
{% endhighlight %}

### dataSource.cube `string`
{:#members:datasource-cube}

Contains the respective cube name from OLAP database as string type.

#### Default Value: “”

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ dataSource: { cube: "Adventure Works" } });
{% endhighlight %}

### dataSource.data `object`
{:#members:datasource-data}

Provides the raw data source for the PivotChart in Relational mode.

#### Default Value: null

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ dataSource: { data: value } });
{% endhighlight %}

### dataSource.catalog `string`
{:#members:datasource-catalog}

In connection with an OLAP database, this property contains the database name as string to fetch the data from the given connection string.

#### Default Value: “”

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart( { dataSource: { catalog: "databaseName" } } );
{% endhighlight %}

### dataSource.columns `array`
{:#members:datasource-columns}

Lists out the items to be displayed as series of PivotChart.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ dataSource: { columns: itemsArray } });
{% endhighlight %}


### dataSource.columns.fieldName `string`
{:#members:datasource-columns-fieldname}

Allows the user to bind the item by using its unique name as field name.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ dataSource: { columns: [{ fieldName : "MyFieldName" }] } });
{% endhighlight %}

### dataSource.columns.fieldCaption `string`
{:#members:datasource-columns-fieldcaption}

Allows the user to set the display caption for an item.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ dataSource: { columns: [{ fieldCaption : "MyFieldCaption" }] } });
{% endhighlight %}

### dataSource.columns.isNamedSets `boolean`
{:#members:datasource-columns-isnamedsets}

Allows the user to indicate whether the added item is a named set or not. 

> **Note**: This is only applicable for OLAP datasource.

#### Default Value: false

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ dataSource: { columns: [{ fieldName: "[Core Product Group]", isNamedSets : true }] } });
{% endhighlight %}

### dataSource.columns.sortOrder `enum`
{:#members:datasource-columns-sortorder}

<ts ref = "ej.PivotAnalysis.SortOrder"/>

Allows the user to set the sorting order of the members of the field.

>**Note**: This is applicable for Relational datasource only.

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
 
    $("#PivotChart1").ejPivotChart({ dataSource: { columns: [{ fieldName: "Country", sortOrder : ej.PivotAnalysis.SortOrder.Descending }] } });
{% endhighlight %}

### dataSource.columns.filterItems `object`
{:#members:datasource-columns-filteritems}

Applies filter to the field members.

#### Default Value: null

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ dataSource: { columns: [{ fieldName: "Country", filterItems : { filterType: ej.PivotAnalysis.FilterType.Exclude, values: ["Canada", "France"] } }] } });
{% endhighlight %}

### dataSource.columns.filterItems.filterType `enum`
{:#members:datasource-columns-filteritems-filtertype}

<ts ref = "ej.PivotAnalysis.FilterType"/>

Sets the type of filter whether to include/exclude the mentioned values.

>**Note**: This is applicable for Relational datasource only.

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
 
    $("#PivotChart1").ejPivotChart({ dataSource: { columns: [{ fieldName: "Country", filterItems : { filterType: ej.PivotAnalysis.FilterType.Include, values: valueArray } }] } });
{% endhighlight %}

### dataSource.columns.filterItems.values `array`
{:#members:datasource-columns-filteritems-values}

Contains the collection of items to be included/excluded among the field members.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ dataSource: { columns: [{ fieldName: "Country", filterItems : { filterType: ej.PivotAnalysis.FilterType.Exclude, values: ["Canada", "France"] } }] } });
{% endhighlight %}

### dataSource.rows `array`
{:#members:datasource-rows}

Lists out the items to be displayed as segments of PivotChart.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ dataSource: { rows: itemsArray } });
{% endhighlight %}


### dataSource.rows.fieldName `string`
{:#members:datasource-rows-fieldname}

Allows the user to bind the item by using its unique name as field name.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ dataSource: { rows: [{ fieldName : "MyFieldName" }] } });
{% endhighlight %}

### dataSource.rows.fieldCaption `string`
{:#members:datasource-rows-fieldcaption}

Allows the user to set the display caption for an item.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ dataSource: { rows: [{ fieldCaption : "MyFieldCaption" }] } });
{% endhighlight %}

### dataSource.rows.isNamedSets `boolean`
{:#members:datasource-rows-isnamedsets}

Allows the user to indicate whether the added item is a named set or not. 

> **Note**: This is only applicable for OLAP datasource.

#### Default Value: false

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ dataSource: { rows: [{ fieldName: "[Core Product Group]", isNamedSets : true }] } });
{% endhighlight %}

### dataSource.rows.sortOrder `enum`
{:#members:datasource-rows-sortorder}

<ts ref = "ej.PivotAnalysis.SortOrder"/>

Allows the user to set the sorting order of the members of the field.

>**Note**: This is applicable for Relational datasource only.

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
 
    $("#PivotChart1").ejPivotChart({ dataSource: { rows: [{ fieldName: "Country", sortOrder : ej.PivotAnalysis.SortOrder.Descending }] } });
{% endhighlight %}

### dataSource.rows.filterItems `object`
{:#members:datasource-rows-filteritems}

Applies filter to the field members.

#### Default Value: null

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ dataSource: { rows: [{ fieldName: "Country", filterItems : { filterType: ej.PivotAnalysis.FilterType.Exclude, values: ["Canada", "France"] } }] } });
{% endhighlight %}

### dataSource.rows.filterItems.filterType `enum`
{:#members:datasource-rows-filteritems-filtertype}

<ts ref = "ej.PivotAnalysis.FilterType"/>

Sets the type of filter whether to include/exclude the mentioned values.

>**Note**: This is applicable for Relational datasource only.

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
 
    $("#PivotChart1").ejPivotChart({ dataSource: { rows: [{ fieldName: "Country", filterItems : { filterType: ej.PivotAnalysis.FilterType.Include, values: valueArray } }] } });
{% endhighlight %}

### dataSource.rows.filterItems.values `array`
{:#members:datasource-rows-filteritems-values}

Contains the collection of items to be included/excluded among the field members.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ dataSource: { rows: [{ fieldName: "Country", filterItems : { filterType: ej.PivotAnalysis.FilterType.Exclude, values: ["Canada", "France"] } }] } });
{% endhighlight %}

### dataSource.values `array`
{:#members:datasource-values}

Lists out the items supports calculation in PivotChart.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ dataSource: { values: itemsArray } });
{% endhighlight %}

### dataSource.values.fieldName `string`
{:#members:datasource-values-fieldname}

Allows the user to bind the item by using its unique name as field name for Relational datasource.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ dataSource: { values: [{ fieldName : "MyFieldName" }] } });
{% endhighlight %}

### dataSource.values.fieldCaption `string`
{:#members:datasource-values-fieldcaption}

Allows the user to set the display caption for an item for Relational datasource.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ dataSource: { values: [{ fieldCaption : "MyFieldCaption" }] } });
{% endhighlight %}

### dataSource.values.measures `array`
{:#members:datasource-values-measures}

This holds the list of unique names of measures to bind them from the OLAP cube.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ dataSource: { values: [{ measures : itemsArray }] } });
{% endhighlight %}

### dataSource.values.measures.fieldName `string`
{:#members:datasource-values-measures-fieldName}

Allows the user to bind the measure from OLAP datasource by using its unique name as field name.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ dataSource: { values: [{ measures : [{ fieldName: "MeasureUniqueName" }] }] } });
{% endhighlight %}

### dataSource.values.axis `string`
{:#members:datasource-values-axis}

Allows to set the axis name to place the measures items.

>**Note**: This is applicable for OLAP datasource only.

#### Default Value: "rows"

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ dataSource: { values: [{ axis : ej.olap.AxisName.Row }] } });
{% endhighlight %}

### dataSource.values.isCalculatedField `boolean`
{:#members:datasource-values-iscalculatedfield}

Indicates whether the field is a calculated field or not with Relational datasource.

#### Default Value: false

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ dataSource: { values: [{ isCalculatedField : true }] } });
{% endhighlight %}

### dataSource.values.formula `string`
{:#members:datasource-values-formula}

Allows to set the formula for calculation of values for calculated members in Relational datasource.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ dataSource: { values: [{ formula : "Quantity*10" }] } });
{% endhighlight %}

### dataSource.filters `array`
{:#members:datasource-filters}

Lists out the items which supports filtering of values without displaying the members in UI in PivotChart.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ dataSource: { filters: itemsArray } });
{% endhighlight %}


### dataSource.filters.fieldName `string`
{:#members:datasource-filters-fieldname}

Allows the user to bind the item by using its unique name as field name.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ dataSource: { filters: [{ fieldName : "MyFieldName" }] } });
{% endhighlight %}

### dataSource.filters.filterItems `object`
{:#members:datasource-filters-filteritems}

Applies filter to the field members.

#### Default Value: null

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ dataSource: { filters: [{ fieldName: "Country", filterItems : { filterType: ej.PivotAnalysis.FilterType.Exclude, values: ["Canada", "France"] } }] } });
{% endhighlight %}

### dataSource.filters.filterItems.filterType `enum`
{:#members:datasource-filters-filteritems-filtertype}

<ts ref = "ej.PivotAnalysis.FilterType"/>

Sets the type of filter whether to include/exclude the mentioned values.

>**Note**: This is applicable for Relational datasource only.

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
 
    $("#PivotChart1").ejPivotChart({ dataSource: { filters: [{ fieldName: "Country", filterItems : { filterType: ej.PivotAnalysis.FilterType.Include, values: valueArray } }] } });
{% endhighlight %}

### dataSource.filters.filterItems.values `array`
{:#members:datasource-filters-filteritems-values}

Contains the collection of items to be included/excluded among the field members.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ dataSource: { filters: [{ fieldName: "Country", filterItems : { filterType: ej.PivotAnalysis.FilterType.Exclude, values: ["Canada", "France"] } }] } });
{% endhighlight %}

### customObject `object`
{:#members:customobject}

Object utilized to pass additional information between client-end and service-end on operating the control in server mode.

#### Default Value: {}

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ customObject: { "key": "Hello World" } });
{% endhighlight %}

### enable3D `boolean`
{:#members:enable3d}

Allows the user to enable 3D view of PivotChart.

#### Default Value: false

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ enable3D: true });
{% endhighlight %}

### enableRTL `boolean`
{:#members:enablertl}

Allows the user to view PivotChart from right to left.

#### Default Value: false

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ enableRTL: true });
{% endhighlight %}

### isResponsive `boolean`
{:#members:isresponsive}

Allows the user to enable PivotChart’s responsiveness in the browser layout.

#### Default Value: false

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ isResponsive: true });
{% endhighlight %}

### legend `object`
{:#members:legend}

Lets the user to customize the legend items and their labels.

#### Default Value: {}

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ legend: { visible: true } });
{% endhighlight %}

### locale `string`
{:#members:locale}

Allows the user to set the localized language for the widget.

#### Default Value: "en-US"

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ locale: "fr-FR" });
{% endhighlight %}

### operationalMode `enum`
{:#members:operationalmode}

<ts ref = "ej.Pivot.OperationalMode"/>

Sets the mode for the PivotChart widget for binding data source either in server-side or client-side.

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
 
    $("#PivotChart1").ejPivotChart({ operationalMode: ej.Pivot.OperationalMode.ServerMode });
{% endhighlight %}

### primaryXAxis `object`
{:#members:primaryxaxis}

This is a horizontal axis that contains options to configure axis and it is the primary x axis for all the series in series array. To override x axis for particular series, create an axis object by providing unique name by using name property and add it to axes array. Then, assign the name to the series&rsquo;s xAxisName property to link both axis and series.

#### Default Value: {}

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ primaryXAxis: { title: { text: "Fiscal Year" }, labelRotation: 0 });
{% endhighlight %}

### primaryYAxis `object`
{:#members:primaryyaxis}

This is a vertical axis that contains options to configure axis. This is the primary y axis for all the series in series array. To override y axis for particular series, create an axis object by providing unique name by using name property and add it to axes array. Then, assign the name to the series&rsquo;s yAxisName property to link both axis and series.

#### Default Value: {}

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ title: { text: "Customer Count"} });
{% endhighlight %}

### rotation `number`
{:#members:rotation}

Allows the user to rotate the angle of PivotChart in 3D view.

#### Default Value: 0

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ rotation: 45 });
{% endhighlight %}


### serviceMethodSettings `object`
{:#members:servicemethodsettings}

Allows the user to set custom name for the methods at service-end, communicated on AJAX post.

>**Note**: This is applicable only on operating the control in server mode.

#### Default Value: {}

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ serviceMethodSettings: { initialize: "MyMethod1", drillDown: "MyMethod2" } });
{% endhighlight %}

### serviceMethodSettings.drillDown `string`
{:#members:servicemethodsettings-drilldown}

Allows the user to set the custom name for the service method responsible for drilling up/down operation in PivotChart.

#### Default Value: "DrillChart"

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ serviceMethodSettings: { drillDown: "DrillChartMyMethod" } });
{% endhighlight %}

### serviceMethodSettings.exportPivotChart `string`
{:#members:servicemethodsettings-exportpivotchart}

Allows the user to set the custom name for the service method responsible for exporting.

#### Default Value: "Export"

**Example:**

{% highlight javascript %}

    $("#PivotChart1").ejPivotChart({ serviceMethodSettings: { exportPivotChart: "ExportMyMethod" } })
{% endhighlight %}

### serviceMethodSettings.initialize `string`
{:#members:servicemethodsettings-initialize}

Allows the user to set the custom name for the service method responsible for initializing PivotChart.

#### Default Value: "InitializeChart"

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ serviceMethodSettings: { initialize: "IninlizeChartMyMethod" } });
{% endhighlight %}
 
 ### serviceMethodSettings.paging `string`
{:#members:servicemethodsettings-paging}

Allows the user to set the custom name for the service method responsible for navigating between pages in paged PivotChart.

#### Default Value: "Paging"

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ serviceMethodSettings: { paging: "PagingMyMethod" } });
{% endhighlight %}


### size `object`
{:#members:size}

Options to customize the size of the PivotChart control.

#### Default Value: {}

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ size: { height: "450px", width: "95%" } });
{% endhighlight %}

###  url `string`
{:#members:url}

Connects the service using the specified URL for any server updates on operating the control in server mode.

#### Default Value: “”

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({ url: "/PivotService" });
{% endhighlight %}

## Methods

### doAjaxPost()
{:#methods:doajaxpost}

Performs an asynchronous HTTP (AJAX) request.

**Example:**

{% highlight javascript %}
 
    var chartObj = $("#PivotChart1").data("ejPivotChart");
    chartObj.doAjaxPost("POST", "/PivotService/Initialize", { "key", "Hello World" }, successEvent, null);
{% endhighlight %}

### doPostBack()
{:#methods:dopostback}

Perform an asynchronous HTTP (FullPost) submit.

**Example:**

{% highlight javascript %}

    var chartObj = $("#PivotChart1").data("ejPivotChart");
    chartObj.doPostBack("/PivotService/Initialize", { "key", "Hello World" });
{% endhighlight %}

### exportPivotChart()
{:#methods:exportpivotchart}

Exports the PivotChart to the format specified in the parameter.
  
**Example:**

{% highlight javascript %}
 
    var chartObj = $("#PivotChart1").data("ejPivotChart");
    chartObj.exportPivotChart(ej.PivotChart.ExportOptions.Excel);
{% endhighlight %}


### renderChartFromJSON()
{:#methods:renderchartfromjson}

This function renders the PivotChart control with the JSON formatted datasource.

**Example:**

{% highlight javascript %}
 
    var chartObj = $("#PivotChart1").data("ejPivotChart");
    chartObj.renderControlFromJSON(chartObj.getJSONRecords());
{% endhighlight %}

### renderControlSuccess()
{:#methods:rendercontrolsuccess}

This function receives the update from service-end, which would be utilized for rendering the widget.

**Example:**

{% highlight javascript %}
 
    var chartObj = $("#PivotChart1").data("ejPivotChart");
    chartObj.renderControlSuccess({ "OlapReport": chartObj.getOlapReport(), "JsonRecords": chartObj.getJSONRecords() });
{% endhighlight %}

### getOlapReport()
{:#methods:getolapreport}

Returns the OlapReport string maintained along with the axis elements information.

>**Note**: This method is applicable only on operating the control in server mode.

**Example:**

{% highlight javascript %}
 
    var chartObj = $("#PivotChart1").data("ejPivotChart");
    var report = chartObj.getOlapReport();
{% endhighlight %}

### setOlapReport()
{:#methods:setolapreport}

Sets the OlapReport string along with the axis information and maintains it in a property.

>**Note**: This method is applicable only on operating the control in server mode.

**Example:**

{% highlight javascript %}
 
    var chartObj = $("#PivotChart1").data("ejPivotChart");
    chartObj.setOlapReport(olapReportObj);
{% endhighlight %}

### getJSONRecords()
{:#methods:getjsonrecords}

Returns the JSON records formed to render the control.

**Example:**

{% highlight javascript %}
 
    var chartObj = $("#PivotChart1").data("ejPivotChart");
    var jsonRecords = chartObj.getJSONRecords();
{% endhighlight %}

### setJSONRecords()
{:#methods:setjsonrecords}

Sets the JSON records to render the control.

**Example:**

{% highlight javascript %}
 
    var chartObj = $("#PivotChart1").data("ejPivotChart");
    chartObj.setJSONRecords(jsonRecords);
{% endhighlight %}

### getPivotEngine()
{:#methods:getpivotengine}

Returns the PivotEngine formed to render the control.

**Example:**

{% highlight javascript %}
 
    var chartObj = $("#PivotChart1").data("ejPivotChart");
    var jsonRecords = chartObj.getPivotEngine();
{% endhighlight %}

### setPivotEngine()
{:#methods:setpivotengine}

Sets the PivotEngine required to render the control.

**Example:**

{% highlight javascript %}
 
    var chartObj = $("#PivotChart1").data("ejPivotChart");
    chartObj.setPivotEngine(jsonRecords);
{% endhighlight %}

### refreshControl()
{:#methods:refreshControl}

Re-renders the control with the data source at the instant.

>**Note**: This is only applicable on operating in client mode.

**Example:**

{% highlight javascript %}
 
    var chartObj = $("#PivotChart1").data("ejPivotChart");
    chartObj.model.dataSource = newDataSource;
    chartObj.refreshControl();
{% endhighlight %}

### generateJSON()
{:#methods:generatejson}

Renders the control with the pivot engine obtained from olap cube.

**Example:**

{% highlight javascript %}
 
    var chartObj = $("#PivotChart1").data("ejPivotChart");
    chartObj.generateJSON(baseObj, pivotEngineObj);
{% endhighlight %}

### refreshPagedPivotChart()
{:#methods:refreshpagedpivotchart}

Navigates to the specified page number in specified axis.

**Example:**

{% highlight javascript %}
 
    var chartObj = $("#PivotChart1").data("ejPivotChart");
    chartObj.refreshPagedPivotChart("series", 4);
{% endhighlight %}

## Events


### load
{:#events:load}

Triggers when PivotChart starts to render.

<table class="params">
<thead>
<tr>
<th colspan="3">Event Parameters</th>
</tr>
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


**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({
        load: function (args) {}
    });

{% endhighlight %}


### afterServiceInvoke
{:#events:afterserviceinvoke}

Triggers when it reaches client-side after any AJAX request.

<table class="params">
<thead>
<tr>
<th colspan="3">Event Parameters</th>
</tr>
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


**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({
        afterServiceInvoke: function (args) {}
    });
{% endhighlight %}


### beforeServiceInvoke
{:#events:beforeserviceinvoke}

Triggers before any AJAX request is passed from PivotChart to service methods.

<table class="params">
<thead>
<tr>
<th colspan="3">Event Parameters</th>
</tr>
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


**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({
        beforeServiceInvoke: function (args) {}
    });      

{% endhighlight %}



### drillSuccess
{:#events:drillsuccess}

Triggers on performing drill up/down in PivotChart control.

<table class="params">
<thead>
<tr>
<th colspan="3">Event Parameters</th>
</tr>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">chartObj</td>
<td class="type">object</td>
<td class="description last">returns the current instance of PivotChart.</td>
</tr>
<tr>
<td class="name">drillAction</td>
<td class="type">string</td>
<td class="description last">returns the drill action of PivotChart.</td>
</tr>
<tr>
<td class="name">drilledMember</td>
<td class="type">string</td>
<td class="description last">contains the name of the member drilled.</td>
</tr>
<tr>
<td class="name">event</td>
<td class="type">object</td>
<td class="description last">returns the event object.</td>
</tr>
</tbody>
</table>


**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({
        drillSuccess: function (args) {}
    });

{% endhighlight %}

### renderComplete
{:#events:rendercomplete}

Triggers when PivotChart widget completes all operations at client-side after any AJAX request.

<table class="params">
<thead>
<tr>
<th colspan="3">Event Parameters</th>
</tr>
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


**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({
        renderComplete: function (args) {}
    });

{% endhighlight %}




### renderFailure
{:#events:renderfailure}

Triggers when any error occurred during AJAX request.

<table class="params">
<thead>
<tr>
<th colspan="3">Event Parameters</th>
</tr>
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
<tr>
<td class="name">message</td>
<td class="type">string</td>
<td class="description last">returns the error stack trace of the original exception.</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({
        renderFailure: function (args) {}
    });      

{% endhighlight %}


### renderSuccess
{:#events:rendersuccess}

Triggers when PivotChart successfully reaches client-side after any AJAX request.

<table class="params">
<thead>
<tr>
<th colspan="3">Event Parameters</th>
</tr>
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
<td class="description last">returns the current instance of PivotChart.</td>
</tr>
</tbody>
</table>


**Example:**

{% highlight javascript %}
 
    $("#PivotChart1").ejPivotChart({
        renderSuccess: function (args) {}
    });
{% endhighlight %}