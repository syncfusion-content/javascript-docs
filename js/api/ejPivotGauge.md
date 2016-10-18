---
layout: post
title: Properties, Methods and Events of ejPivotGauge Widget
documentation: API
platform: js
keywords: ejPivotGauge, API, Essential JS PivotGauge
metaname: 
metacontent: 
---

# PivotGauge

The PivotGauge control is ideal for highlighting business critical Key Performance Indicator (KPI) information in executive dashboards and report cards. The PivotGauge let you present values against goals in a very intuitive manner.

#### Syntax

{% highlight javascript %}

    $(element).ejPivotGauge()
{% endhighlight %}

#### Example

{% highlight html %}
 
    <div id="PivotGauge1"></div> 
    
    <script>
    //Create PivotGauge
    $("#PivotGauge1").ejPivotGauge(...);       
    </script>

{% endhighlight %}

#### Requires

* module:jQuery-3.0.0.min.js
* module:ej.core.js
* module:ej.data.js
* module:ej.waitingpopup.js
* module:ej.circulargauge.js
* module:ej.pivot.common.js
* module:ej.olap.base.js
* module:ej.pivotanalysis.base.js
* module:ej.pivotgauge.js


## Members

### columnsCount `number`
{:#members:columnscount}

Sets the number of columns to arrange the Pivot Gauges.

#### Default Value: 0

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ columnsCount: 1 });
{% endhighlight %}

### cssClass `string`
{:#members:cssclass}

Specifies the CSS class to PivotGauge to achieve custom theme.

#### Default Value: “”

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ cssClass : "gradient-lime" });
{% endhighlight %}

### customObject `object`
{:#members:customobject}

Object utilized to pass additional information between client-end and service-end on operating in server mode.

#### Default Value: {}

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ customObject: { "key": "Hello World" } });
{% endhighlight %}

### dataSource `object`
{:#members:datasource}

Initializes the data source for the PivotGauge widget, when it functions completely on client-side.

#### Default Value: {}

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge( { dataSource: { data: value } });
{% endhighlight %}

### dataSource.cube `string`
{:#members:datasource-cube}

Contains the respective cube name from OLAP database as string type.

#### Default Value: “”

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ dataSource: { cube: "Adventure Works" } });
{% endhighlight %}

### dataSource.data `object`
{:#members:datasource-data}

Provides the raw data source for the PivotGauge in Relational mode.

#### Default Value: null

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ dataSource: { data: value } });
{% endhighlight %}

### dataSource.catalog `string`
{:#members:datasource-catalog}

In connection with an OLAP database, this property contains the database name as string to fetch the data from the given connection string.

#### Default Value: “”

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge( { dataSource: { catalog: "databaseName" } } );
{% endhighlight %}

### dataSource.columns `array`
{:#members:datasource-columns}

Lists out the items to bind in columns section.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ dataSource: { columns: itemsArray } });
{% endhighlight %}


### dataSource.columns.fieldName `string`
{:#members:datasource-columns-fieldname}

Allows the user to bind the item by using its unique name as field name.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ dataSource: { columns: [{ fieldName : "MyFieldName" }] } });
{% endhighlight %}

### dataSource.columns.filterItems `object`
{:#members:datasource-columns-filteritems}

Applies filter to the field members.

#### Default Value: null

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ dataSource: { columns: [{ fieldName: "Country", filterItems : { filterType: ej.PivotAnalysis.FilterType.Exclude, values: ["Canada", "France"] } }] } });
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
 
    $("#PivotGauge1").ejPivotGauge({ dataSource: { columns: [{ fieldName: "Country", filterItems : { filterType: ej.PivotAnalysis.FilterType.Include, values: valueArray } }] } });
{% endhighlight %}

### dataSource.columns.filterItems.values `array`
{:#members:datasource-columns-filteritems-values}

Contains the collection of items to be included/excluded among the field members.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ dataSource: { columns: [{ fieldName: "Country", filterItems : { filterType: ej.PivotAnalysis.FilterType.Exclude, values: ["Canada", "France"] } }] } });
{% endhighlight %}

### dataSource.rows `array`
{:#members:datasource-rows}

Lists out the items to bind in rows section.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ dataSource: { rows: itemsArray } });
{% endhighlight %}

### dataSource.rows.fieldName `string`
{:#members:datasource-rows-fieldname}

Allows the user to bind the item by using its unique name as field name.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ dataSource: { rows: [{ fieldName : "MyFieldName" }] } });
{% endhighlight %}

### dataSource.rows.filterItems `object`
{:#members:datasource-rows-filteritems}

Applies filter to the field members.

#### Default Value: null

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ dataSource: { rows: [{ fieldName: "Country", filterItems : { filterType: ej.PivotAnalysis.FilterType.Exclude, values: ["Canada", "France"] } }] } });
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
 
    $("#PivotGauge1").ejPivotGauge({ dataSource: { rows: [{ fieldName: "Country", filterItems : { filterType: ej.PivotAnalysis.FilterType.Include, values: valueArray } }] } });
{% endhighlight %}

### dataSource.rows.filterItems.values `array`
{:#members:datasource-rows-filteritems-values}

Contains the collection of items to be included/excluded among the field members.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ dataSource: { rows: [{ fieldName: "Country", filterItems : { filterType: ej.PivotAnalysis.FilterType.Exclude, values: ["Canada", "France"] } }] } });
{% endhighlight %}

### dataSource.values `array`
{:#members:datasource-values}

Lists out the items supports calculation in PivotGauge.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ dataSource: { values: itemsArray } });
{% endhighlight %}

### dataSource.values.fieldName `string`
{:#members:datasource-values-fieldname}

Allows the user to bind the item by using its unique name as field name for Relational datasource.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ dataSource: { values: [{ fieldName : "MyFieldName" }] } });
{% endhighlight %}

### dataSource.values.fieldCaption `string`
{:#members:datasource-values-fieldcaption}

Allows the user to set the display caption for an item for Relational datasource.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ dataSource: { values: [{ fieldCaption : "MyFieldCaption" }] } });
{% endhighlight %}

### dataSource.values.measures `array`
{:#members:datasource-values-measures}

This holds the list of unique names of measures to bind them from the OLAP cube.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ dataSource: { values: [{ measures : itemsArray }] } });
{% endhighlight %}

### dataSource.values.measures.fieldName `string`
{:#members:datasource-values-measures-fieldName}

Allows the user to bind the measure from OLAP datasource by using its unique name as field name.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ dataSource: { values: [{ measures : [{ fieldName: "MeasureUniqueName" }] }] } });
{% endhighlight %}

### dataSource.values.axis `string`
{:#members:datasource-values-axis}

Allows to set the axis name to place the measures items.

>**Note**: This is applicable for OLAP datasource only.

#### Default Value: "rows"

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ dataSource: { values: [{ axis : ej.olap.AxisName.Row }] } });
{% endhighlight %}

### dataSource.values.isCalculatedField `boolean`
{:#members:datasource-values-iscalculatedfield}

Indicates whether the field is a calculated field or not with Relational datasource.

#### Default Value: false

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ dataSource: { values: [{ isCalculatedField : true }] } });
{% endhighlight %}

### dataSource.values.formula `string`
{:#members:datasource-values-formula}

Allows to set the formula for calculation of values for calculated members in Relational datasource.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ dataSource: { values: [{ formula : "Quantity*10" }] } });
{% endhighlight %}

### dataSource.filters `array`
{:#members:datasource-filters}

Lists out the items which supports filtering of values without displaying the members in UI in PivotGauge.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ dataSource: { filters: itemsArray } });
{% endhighlight %}


### dataSource.filters.fieldName `string`
{:#members:datasource-filters-fieldname}

Allows the user to bind the item by using its unique name as field name.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ dataSource: { filters: [{ fieldName : "MyFieldName" }] } });
{% endhighlight %}

### dataSource.filters.filterItems `object`
{:#members:datasource-filters-filteritems}

Applies filter to the field members.

#### Default Value: null

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ dataSource: { filters: [{ fieldName: "Country", filterItems : { filterType: ej.PivotAnalysis.FilterType.Exclude, values: ["Canada", "France"] } }] } });
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
 
    $("#PivotGauge1").ejPivotGauge({ dataSource: { filters: [{ fieldName: "Country", filterItems : { filterType: ej.PivotAnalysis.FilterType.Include, values: valueArray } }] } });
{% endhighlight %}

### dataSource.filters.filterItems.values `array`
{:#members:datasource-filters-filteritems-values}

Contains the collection of items to be included/excluded among the field members.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ dataSource: { filters: [{ fieldName: "Country", filterItems : { filterType: ej.PivotAnalysis.FilterType.Exclude, values: ["Canada", "France"] } }] } });
{% endhighlight %}

### enableAnimation `boolean`
{:#members:enableanimation}

Enables/disables the animation of pointer in PivotGauge.

#### Default Value: false

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ enableAnimation: true });
{% endhighlight %}

### enableTooltip `boolean`
{:#members:enabletooltip}

Enables/disables tooltip visibility in PivotGauge.

#### Default Value: false

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ enableTooltip: true }); 
{% endhighlight %}

### enableRTL `boolean`
{:#members:enablertl}

Allows the user to view PivotGauge from right to left.

#### Default Value: false

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ enableRTL: true });
{% endhighlight %}


### isResponsive `boolean`
{:#members:isresponsive}

Allows the user to enable PivotGauge’s responsiveness in the browser layout.

#### Default Value: false

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ isResponsive: true });
{% endhighlight %}

### labelFormatSettings `object`
{:#members:labelformatsettings}

Allows the user to change the format of the label values in PivotGauge.

#### Default Value: null

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ labelFormatSettings: value  });
{% endhighlight %}

### labelFormatSettings.numberFormat `enum`
{:#members:labelformatsettings-numberformat}

<ts name = "ej.PivotGauge.NumberFormat"/>

Allows the user to change the number format of the label values in PivotGauge.

#### Default Value: ej.PivotGauge.NumberFormat.Default

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">Default</td>
            <td class="description">To set default format for label values.</td>
        </tr>
        <tr>
            <td class="name">Currency</td>
            <td class="description">To set currency format for label values.</td>
        </tr>
        <tr>
            <td class="name">Percentage</td>
            <td class="description">To set percentage format for label values.</td>
        </tr>
        <tr>
            <td class="name">Fraction</td>
            <td class="description">To set fraction format for label values.</td>
        </tr>
        <tr>
            <td class="name">Scientific</td>
            <td class="description">To set scientific format for label values.</td>
        </tr>
        <tr>
            <td class="name">Text</td>
            <td class="description">To set text format for label values.</td>
        </tr>
        <tr>
            <td class="name">Notation</td>
            <td class="description">To set notation format for label values.</td>
        </tr>
    </tbody>
</table>


**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ labelFormatSettings: { numberFormat: ej.PivotGauge.NumberFormat.Default } });
{% endhighlight %}


### labelFormatSettings.decimalPlaces `number`
{:#members:labelformatsettings-decimalplaces}

Allows you to set the number of digits displayed after decimal point.

#### Default Value: 5

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ labelFormatSettings: { decimalPlaces: 3 } });
{% endhighlight %}


### labelFormatSettings.prefixText  `string`
{:#members:labelformatsettings-prefixtext}

Allows you to add a text at the beginning of the label.

#### Default Value: " "

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ labelFormatSettings: { prefixText: "prefixTextValue" } });
{% endhighlight %}


### labelFormatSettings.suffixText `string`
{:#members:labelformatsettings-suffixtext }

Allows you to add text at the end of the label.

#### Default Value: " "

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ labelFormatSettings: { suffixText: "suffixTextValue" } });
{% endhighlight %}


### locale `string`
{:#members:locale}

Allows the user to set the localized language for the widget.

#### Default Value: "en-US"

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ locale: "fr-FR" });
{% endhighlight %}

### rowsCount `number`
{:#members:rowscount}

Sets the number of rows to arrange the Pivot Gauges.

#### Default Value: 0

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ rowsCount: 1 });
{% endhighlight %}

### scales `object`
{:#members:scales}

Sets the scale values such as pointers, indicators, etc... for PivotGauge.

#### Default Value: {}

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ scales: { showRanges: true, showIndicators: true } });
{% endhighlight %}

### serviceMethodSettings `object`
{:#members:servicemethodsettings}

Allows the user to set the custom name for the methods at service-end, communicated during AJAX post.

>**Note**: This is applicable only for server mode operation.

#### Default Value: {}

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ serviceMethodSettings: { initialize: "MyMethod" } });
{% endhighlight %}

### serviceMethodSettings.initialize `string`
{:#members:servicemethodsettings-initialize}

Allows the user to set the custom name for the service method responsible for initializing PivotGauge.

#### Default Value: "InitializeGauge"

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ serviceMethodSettings: { initialize: "InitializeGaugeMyMethod" } }); 
{% endhighlight %}

### showHeaderLabel `boolean`
{:#members:showheaderlabel}

Enables/disables the header labels in PivotGauge.

#### Default Value: true

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ showHeaderLabel: false });
{% endhighlight %}

### url `string`
{:#members:url}

Connects the service using the specified URL for any server updates on server mode operation.

#### Default Value: “”

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ url: "/PivotGaugeService" });
{% endhighlight %}

### analysisMode `enum`
{:#members:analysisMode}

<ts ref = "ej.Pivot.AnalysisMode"/>

Sets the mode for the PivotGauge widget for binding either OLAP or Relational data source.

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
            <td class="description">To bind Relational datasource to PivotGauge widget</td>
        </tr>
        <tr>
            <td class="name">Olap</td>
            <td class="description">To bind OLAP datasource to PivotGauge widget</td>
        </tr>
    </tbody>
</table>

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({ analysisMode: ej.Pivot.AnalysisMode.Olap });
{% endhighlight %}

### operationalMode `enum`
{:#members:operationalmode}

<ts ref = "ej.Pivot.OperationalMode"/>

Sets the mode for the PivotGauge widget for binding data source either in server-side or client-side.

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
 
    $("#PivotGauge1").ejPivotGauge({ operationalMode: ej.Pivot.OperationalMode.ServerMode });
{% endhighlight %}

## Methods

### doAjaxPost()
{:#methods:doajaxpost}

Performs an asynchronous HTTP (AJAX) request.

**Example:**

{% highlight javascript %}
    
    var gaugeObj = $("#PivotGauge1").data("ejPivotGauge");
    gaugeObj.doAjaxPost("POST", "/PivotService/Initialize", { "key", "Hello World" }, "renderControlSuccess", null);
{% endhighlight %}

### refresh()
{:#methods:refresh}

This function is used to refresh the PivotGauge at client-side itself.

**Example:**

{% highlight javascript %}

    var gaugeObj = $("#PivotGauge1").data("ejPivotGauge");
    gaugeObj.refresh();
{% endhighlight %}

### removeImg()
{:#methods:removeimg}

This function removes the KPI related images from PivotGauge on binding OLAP datasource.

**Example:**

{% highlight javascript %}

    var gaugeObj = $("#PivotGauge1").data("ejPivotGauge");
    gaugeObj.removeImg();
{% endhighlight %}

### renderControlFromJSON()
{:#methods:rendercontrolfromjson}

This function receives the JSON formatted datasource and renders the PivotGauge control.

**Example:**

{% highlight javascript %}

    var gaugeObj = $("#PivotGauge1").data("ejPivotGauge");
    gaugeObj.renderControlFromJSON(this.getJSONRecords());
{% endhighlight %}

### getOlapReport()
{:#methods:getolapreport}

Returns the OlapReport string maintained along with the axis elements information.

>**Note**: This method is applicable only on operating the control in server mode.

**Example:**

{% highlight javascript %}
 
    var gaugeObj = $("#PivotGauge1").data("ejPivotGauge");
    var report = gaugeObj.getOlapReport();
{% endhighlight %}

### setOlapReport()
{:#methods:setolapreport}

Sets the OlapReport string along with the axis information and maintains it in a property.

>**Note**: This method is applicable only on operating the control in server mode.

**Example:**

{% highlight javascript %}
 
    var gaugeObj = $("#PivotGauge1").data("ejPivotGauge");
    gaugeObj.setOlapReport(olapReportObj);
{% endhighlight %}

### getJSONRecords()
{:#methods:getjsonrecords}

Returns the JSON records formed to render the control.

**Example:**

{% highlight javascript %}
 
    var gaugeObj = $("#PivotGauge1").data("ejPivotGauge");
    var jsonRecords = gaugeObj.getJSONRecords();
{% endhighlight %}

### setJSONRecords()
{:#methods:setjsonrecords}

Sets the JSON records to render the control.

**Example:**

{% highlight javascript %}
 
    var gaugeObj = $("#PivotGauge1").data("ejPivotGauge");
    gaugeObj.setJSONRecords(jsonRecords);
{% endhighlight %}

### getJSONData()
{:#methods:getjsondata}

Returns the JSON records required to render the PivotGauge on performing any action with OLAP data source.

**Example:**

{% highlight javascript %}

    var gaugeObj = $("#PivotGauge1").data("ejPivotGauge");
    var args = { action : "initialize", activeObject : gaugeObj };
    var jsonData = gaugeObj.getJSONData(args, dataSource);
{% endhighlight %}

## Events

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
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">returns the custom object bound with PivotGauge control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">object</td>
<td class="description last">returns the HTML element of PivotGauge control.</td>
</tr>
</tbody>
</table>


**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({
        afterServiceInvoke: function (args) {}
    });
{% endhighlight %}


### beforeServiceInvoke
{:#events:beforeserviceinvoke}

Triggers before any AJAX request is passed from PivotGauge to service methods.

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
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">returns the custom object bound with PivotGauge control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">object</td>
<td class="description last">returns the HTML element of PivotGauge control.</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({
        beforeServiceInvoke: function (args) {}
    });
{% endhighlight %}


### load
{:#events:load}

Triggers when PivotGauge started loading at client-side.

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
<td class="description last">returns the current action of PivotGauge control.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type">object</td>
<td class="description last">returns the model of PivotGauge control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">object</td>
<td class="description last">returns the HTML element of the widget.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">returns the custom object bound to the control.</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({
        load: function (args) {}
    });
{% endhighlight %}

### renderComplete
{:#events:rendercomplete}

Triggers when PivotGauge widget completes all operations at client-side after any AJAX request.

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
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">returns the custom object bound with PivotGauge control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">object</td>
<td class="description last">returns the HTML element of PivotGauge control.</td>
</tr>
</tbody>
</table>


**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({
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
<td class="name">element</td>
<td class="type">object</td>
<td class="description last">returns the HTML element of PivotGauge control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">returns the custom object bound with the control.</td>
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
 
    $("#PivotGauge1").ejPivotGauge({
        renderFailure: function (args) {}
    });
{% endhighlight %}


### renderSuccess
{:#events:rendersuccess}

Triggers when PivotGauge successfully reaches client-side after any AJAX request.

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
<td class="name">element</td>
<td class="type">object</td>
<td class="description last">returns the HTML element of PivotGauge control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">returns the custom object bound with the control.</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight javascript %}
 
    $("#PivotGauge1").ejPivotGauge({
        renderSuccess: function (args) {}
    });
{% endhighlight %}