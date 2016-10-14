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

{% highlight html %}
 
$("#PivotGauge1").ejPivotGauge({dataSource: {data:value}});

{% endhighlight %}


### dataSource.catalog `string`
{:#members:datasource-catalog}

Contains the database name as string type to fetch the data from the given connection string.

#### Default Value: “”

**Example:**

{% highlight html %}
 
$("#PivotGauge1").ejPivotGauge({dataSource: {catalog: value}});

{% endhighlight %}


### dataSource.columns `array`
{:#members:datasource-columns}

Lists out the items to be arranged in column section of PivotGauge.

#### Default Value: []

**Example:**

{% highlight html %}
 
$("#PivotGauge1").ejPivotGauge({dataSource: {columns: itemsArray}});

{% endhighlight %}

### dataSource.columns.fieldName `string`
{:#members:datasource-columns-fieldname}

Allows the user to bind the item by using its unique name as field name.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotGauge1").ejPivotGauge({dataSource: {columns: [{ fieldName : value}]}});

{% endhighlight %}

### dataSource.columns.fieldCaption `string`
{:#members:datasource-columns-fieldcaption}

Allows the user to set the display name for an item.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotGauge1").ejPivotGauge({dataSource: {columns: [{ fieldCaption : value}]}});

{% endhighlight %}

### dataSource.columns.isNamedSets `boolean`
{:#members:datasource-columns-isnamedsets}

Allows the user to enable the usage of named set items in respective axis. This is only applicable for OLAP datasource.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotGauge1").ejPivotGauge({dataSource: {columns: [{ isNamedSets : true}]}});

{% endhighlight %}


### dataSource.cube `string`
{:#members:datasource-cube}

Contains the respective Cube name from database as string type.

#### Default Value: “”

**Example:**

{% highlight html %}
 
$("#PivotGauge1").ejPivotGauge({dataSource: {cube: value}});

{% endhighlight %}


### dataSource.data `object`
{:#members:datasource-data}

Provides the raw data source for the PivotGauge.

#### Default Value: null

**Example:**

{% highlight html %}
 
$("#PivotGauge1").ejPivotGauge({dataSource: {data: value}});

{% endhighlight %}


### dataSource.rows `array`
{:#members:datasource-rows}

Lists out the items to be arranged in row section of PivotGauge.

#### Default Value: []

**Example:**

{% highlight html %}
 
$("#PivotGauge1").ejPivotGauge({dataSource: {rows: itemsArray}});

{% endhighlight %}

### dataSource.rows.fieldName `string`
{:#members:datasource-rows-fieldname}

Allows the user to bind the item by using its unique name as field name.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotGauge1").ejPivotGauge({dataSource: {rows: [{ fieldName : value}]}});

{% endhighlight %}

### dataSource.rows.fieldCaption `string`
{:#members:datasource-rows-fieldcaption}

Allows the user to set the display name for an item.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotGauge1").ejPivotGauge({dataSource: {rows: [{ fieldCaption : value}]}});

{% endhighlight %}

### dataSource.rows.filterItems `object`
{:#members:datasource-rows-filterItems}

Allows the user to set the filtering values name for an item.

#### Default Value: null

**Example:**

{% highlight html %}
 
$("#PivotGauge1").ejPivotGauge({dataSource: {rows: [{ filterItems : value}]}});

{% endhighlight %}

### dataSource.rows.filterItems.filterType `string`
{:#members:datasource-rows-filterItems-filterType}

Allows the user to set the type of filtering for an item.

#### Default Value: "exclude"

**Example:**

{% highlight html %}
 
$("#PivotGauge1").ejPivotGauge({dataSource: {rows: [{ filterItems : {filterType: "include"}}]}});

{% endhighlight %}

### dataSource.rows.filterItems.values `array`
{:#members:datasource-rows-filterItems-values}

Allows the user to set the values for filtering an item.

#### Default Value: []

**Example:**

{% highlight html %}
 
$("#PivotGauge1").ejPivotGauge({dataSource: {rows: [{ filterItems : {values: itemsArray}}]}});

{% endhighlight %}

### dataSource.rows.isNamedSets `boolean`
{:#members:datasource-rows-isnamedsets}

Allows the user to enable the usage of named set items in respective axis. This is only applicable for OLAP datasource.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotGauge1").ejPivotGauge({dataSource: {rows: [{ isNamedSets : true}]}});

{% endhighlight %}

### dataSource.values `array`
{:#members:datasource-values}

Lists out the items which supports calculation in PivotGauge.

#### Default Value: []

**Example:**

{% highlight html %}
 
$("#PivotGauge1").ejPivotGauge({dataSource: {values: itemsArray}});

{% endhighlight %}

### dataSource.values.measures `array`
{:#members:datasource-values[0]-measures}

This holds the measures unique name to bind them from the Cube.

#### Default Value: []

**Example:**

{% highlight html %}
 
$("#PivotGauge1").ejPivotGauge({dataSource: {values: [{measures : itemsArray}]}});

{% endhighlight %}

### dataSource.values.axis `string`
{:#members:datasource-values[0]-axis}

Allows to set the axis name to place the measures items.

#### Default Value: “”

**Example:**

{% highlight html %}
 
$("#PivotGauge1").ejPivotGauge({dataSource: {values: [{axis : value}]}});

{% endhighlight %}

### dataSource.values.fieldName `string`
{:#members:datasource-values[0]-fieldname}

Allows the user to bind the item by using its unique name as field name.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotGauge1").ejPivotGauge({dataSource: {values: [{ fieldName : value}]}});

{% endhighlight %}

### dataSource.values.fieldCaption `string`
{:#members:datasource-values[0]-fieldcaption}

Allows the user to set the display name for an item.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotGauge1").ejPivotGauge({dataSource: {values: [{ fieldCaption : value}]}});

{% endhighlight %}


### dataSource.filters `array`
{:#members:datasource-filters}

Lists out the items which supports filtering of values in PivotGauge.

#### Default Value: []

**Example:**

{% highlight html %}
 
$("#PivotGauge1").ejPivotGauge({dataSource: {filters: itemsArray}});

{% endhighlight %}

### dataSource.filters.fieldName `string`
{:#members:datasource-filters-fieldname}

Allows the user to bind the item by using its unique name as field name.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotGauge1").ejPivotGauge({dataSource: {filters: [{ fieldName : value}]}});

{% endhighlight %}

### dataSource.filters.fieldCaption `string`
{:#members:datasource-filters-fieldcaption}

Allows the user to set the display name for an item.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotGauge1").ejPivotGauge({dataSource: {filters: [{ fieldCaption : value}]}});

{% endhighlight %}

### dataSource.filters.isNamedSets `boolean`
{:#members:datasource-filters-isnamedsets}

Allows the user to enable the usage of named set items in respective axis. This is only applicable for OLAP datasource.

#### Default Value: false

**Example:**

{% highlight html %}
 
    $("#PivotGauge1").ejPivotGauge({dataSource: {filters: [{ isNamedSets : true}]}});
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

<ts name = "ej.Pivot.AnalysisMode"/>

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

<ts name = "ej.Pivot.OperationalMode"/>

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
 
    $("#PivotGauge1").ejPivotGauge({ operationalMode: ej.PivotGrid.OperationalMode.ServerMode });
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