---
layout: post
title: Properties, Methods and Events of ejPivotTreeMap Widget
documentation: API
platform: js
keywords: ejPivotTreeMap, API, Essential JS PivotTreeMap
metaname: 
metacontent: 
---

# ejPivotTreeMap

The PivotTreemap is a lightweight control that reads OLAP information and visualizes it in graphical format with the ability to drill up and down.

#### Syntax

{% highlight javascript %}

    $(element).ejPivotTreeMap()
{% endhighlight %}


#### Example

{% highlight html %}
 
    <div id="PivotTreeMap1"></div>

    <script>
        //Create PivotTreeMap
        $("#PivotTreeMap1").ejPivotTreeMap(...);
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
* module:ej.pivot.common.js
* module:ej.olap.base.js
* module:ej.pivotanalysis.base.js
* module:ej.treemap.js
* module:ej.pivottreemap.js

## Members

### cssClass `string`
{:#members:cssclass}

Specifies the CSS class to PivotTreeMap to achieve custom theme.

#### Default Value: “”

**Example:**

{% highlight javascript %}
 
    $("#PivotTreeMap1").ejPivotTreeMap({ cssClass : "gradient-lime" });
{% endhighlight %}

### dataSource `object`
{:#members:datasource}

Initializes the data source for the PivotTreeMap widget, when it functions completely on client-side.

#### Default Value: {}

**Example:**

{% highlight javascript %}
 
    $("#PivotTreeMap1").ejPivotTreeMap( { dataSource: { data: value } });
{% endhighlight %}

### dataSource.cube `string`
{:#members:datasource-cube}

Contains the respective cube name from OLAP database as string type.

#### Default Value: “”

**Example:**

{% highlight javascript %}
 
    $("#PivotTreeMap1").ejPivotTreeMap({ dataSource: { cube: "Adventure Works" } });
{% endhighlight %}

### dataSource.catalog `string`
{:#members:datasource-catalog}

In connection with an OLAP database, this property contains the database name as string to fetch the data from the given connection string.

#### Default Value: “”

**Example:**

{% highlight javascript %}
 
    $("#PivotTreeMap1").ejPivotTreeMap( { dataSource: { catalog: "databaseName" } } );
{% endhighlight %}

### dataSource.columns `array`
{:#members:datasource-columns}

Lists out the items to be displayed as series of PivotTreeMap.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotTreeMap1").ejPivotTreeMap({ dataSource: { columns: itemsArray } });
{% endhighlight %}


### dataSource.columns.fieldName `string`
{:#members:datasource-columns-fieldname}

Allows the user to bind the item by using its unique name as field name.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotTreeMap1").ejPivotTreeMap({ dataSource: { columns: [{ fieldName : "HierarchyUniqueName" }] } });
{% endhighlight %}

### dataSource.columns.isNamedSets `boolean`
{:#members:datasource-columns-isnamedsets}

Allows the user to indicate whether the added item is a named set or not. 

#### Default Value: false

**Example:**

{% highlight javascript %}
 
    $("#PivotTreeMap1").ejPivotTreeMap({ dataSource: { columns: [{ fieldName: "[Core Product Group]", isNamedSets : true }] } });
{% endhighlight %}

### dataSource.columns.filterItems `object`
{:#members:datasource-columns-filteritems}

Applies filter to the field members.

#### Default Value: null

**Example:**

{% highlight javascript %}
 
    $("#PivotTreeMap1").ejPivotTreeMap({ dataSource: { columns: [{ fieldName: "[Customer].[Customer Geography]", filterItems : { filterType: ej.PivotAnalysis.FilterType.Exclude, values: ["Canada", "France"] } }] } });
{% endhighlight %}

### dataSource.columns.filterItems.values `array`
{:#members:datasource-columns-filteritems-values}

Contains the collection of items to be excluded among the field members.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotTreeMap1").ejPivotTreeMap({ dataSource: { columns: [{ fieldName: "[Customer].[Customer Geography]", filterItems : { filterType: ej.PivotAnalysis.FilterType.Exclude, values: ["Canada", "France"] } }] } });
{% endhighlight %}

### dataSource.rows `array`
{:#members:datasource-rows}

Lists out the items to be displayed as segments of PivotTreeMap.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotTreeMap1").ejPivotTreeMap({ dataSource: { rows: itemsArray } });
{% endhighlight %}


### dataSource.rows.fieldName `string`
{:#members:datasource-rows-fieldname}

Allows the user to bind the item by using its unique name as field name.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotTreeMap1").ejPivotTreeMap({ dataSource: { rows: [{ fieldName : "HierarchyUniqueName" }] } });
{% endhighlight %}

### dataSource.rows.isNamedSets `boolean`
{:#members:datasource-rows-isnamedsets}

Allows the user to indicate whether the added item is a named set or not. 

#### Default Value: false

**Example:**

{% highlight javascript %}
 
    $("#PivotTreeMap1").ejPivotTreeMap({ dataSource: { rows: [{ fieldName: "[Core Product Group]", isNamedSets : true }] } });
{% endhighlight %}

### dataSource.rows.filterItems `object`
{:#members:datasource-rows-filteritems}

Applies filter to the field members.

#### Default Value: null

**Example:**

{% highlight javascript %}
 
    $("#PivotTreeMap1").ejPivotTreeMap({ dataSource: { rows: [{ fieldName: "[Customer].[Customer Geography]", filterItems : { filterType: ej.PivotAnalysis.FilterType.Exclude, values: ["Canada", "France"] } }] } });
{% endhighlight %}

### dataSource.rows.filterItems.values `array`
{:#members:datasource-rows-filteritems-values}

Contains the collection of items to be excluded among the field members.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotTreeMap1").ejPivotTreeMap({ dataSource: { rows: [{ fieldName: "[Customer].[Customer Geography]", filterItems : { filterType: ej.PivotAnalysis.FilterType.Exclude, values: ["Canada", "France"] } }] } });
{% endhighlight %}

### dataSource.values `array`
{:#members:datasource-values}

Lists out the items supports calculation in PivotTreeMap.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotTreeMap1").ejPivotTreeMap({ dataSource: { values: itemsArray } });
{% endhighlight %}

### dataSource.values.measures `array`
{:#members:datasource-values-measures}

This holds the list of unique names of measures to bind them from the OLAP cube.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotTreeMap1").ejPivotTreeMap({ dataSource: { values: [{ measures : itemsArray }] } });
{% endhighlight %}

### dataSource.values.measures.fieldName `string`
{:#members:datasource-values-measures-fieldName}

Allows the user to bind the measure from OLAP datasource by using its unique name as field name.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotTreeMap1").ejPivotTreeMap({ dataSource: { values: [{ measures : [{ fieldName: "MeasureUniqueName" }] }] } });
{% endhighlight %}

### dataSource.values.axis `string`
{:#members:datasource-values-axis}

Allows to set the axis name to place the measures items.

#### Default Value: "rows"

**Example:**

{% highlight javascript %}
 
    $("#PivotTreeMap1").ejPivotTreeMap({ dataSource: { values: [{ axis : ej.olap.AxisName.Row }] } });
{% endhighlight %}

### dataSource.filters `array`
{:#members:datasource-filters}

Lists out the items which supports filtering of values without displaying the members in UI in PivotTreeMap.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotTreeMap1").ejPivotTreeMap({ dataSource: { filters: itemsArray } });
{% endhighlight %}


### dataSource.filters.fieldName `string`
{:#members:datasource-filters-fieldname}

Allows the user to bind the item by using its unique name as field name.

#### Default Value: ""

**Example:**

{% highlight javascript %}
 
    $("#PivotTreeMap1").ejPivotTreeMap({ dataSource: { filters: [{ fieldName : "HierarchyUniqueName" }] } });
{% endhighlight %}

### dataSource.filters.filterItems `object`
{:#members:datasource-filters-filteritems}

Applies filter to the field members.

#### Default Value: null

**Example:**

{% highlight javascript %}
 
    $("#PivotTreeMap1").ejPivotTreeMap({ dataSource: { filters: [{ fieldName: "[Customer].[Customer Geography]", filterItems : { filterType: ej.PivotAnalysis.FilterType.Exclude, values: ["Canada", "France"] } }] } });
{% endhighlight %}

### dataSource.filters.filterItems.values `array`
{:#members:datasource-filters-filteritems-values}

Contains the collection of items to be excluded among the field members.

#### Default Value: []

**Example:**

{% highlight javascript %}
 
    $("#PivotTreeMap1").ejPivotTreeMap({ dataSource: { filters: [{ fieldName: "[Customer].[Customer Geography]", filterItems : { filterType: ej.PivotAnalysis.FilterType.Exclude, values: ["Canada", "France"] } }] } });
{% endhighlight %}

### customObject `object`
{:#members:customobject}

Object utilized to pass additional information between client-end and service-end.

#### Default Value: {}

**Example:**

{% highlight javascript %}
 
    $("#PivotTreeMap1").ejPivotTreeMap({ customObject: { "key": "Hello World" } });
{% endhighlight %}

### isResponsive `boolean`
{:#members:isresponsive}

Allows the user to enable PivotTreeMap’s responsiveness in the browser layout.

#### Default Value: false

**Example:**

{% highlight javascript %}
 
    $("#PivotTreeMap1").ejPivotTreeMap({ isResponsive: true });
{% endhighlight %}


### locale `string`
{:#members:locale}

Allows the user to set the localized language for the widget.

#### Default Value: "en-US"

**Example:**

{% highlight javascript %}
 
    $("#PivotTreeMap1").ejPivotTreeMap({ locale: "fr-FR" }); 
{% endhighlight %}

### operationalMode `enum`
{:#members:operationalmode}

<ts ref = "ej.Pivot.OperationalMode"/>

Sets the mode for the PivotTreeMap widget for binding data source either in server-side or client-side.

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
 
    $("#PivotTreeMap1").ejPivotTreeMap({ operationalMode: ej.Pivot.OperationalMode.ServerMode });
{% endhighlight %}


### serviceMethodSettings `object`
{:#members:servicemethodsettings}

Allows the user to set custom name for the methods at service-end, communicated on AJAX post.

#### Default Value: {}

**Example:**

{% highlight javascript %}
 
    $("#PivotTreeMap1").ejPivotTreeMap({ serviceMethodSettings: values });
{% endhighlight %}

### serviceMethodSettings.initialize `string`
{:#members:servicemethodsettings-initialize}

Allows the user to set the custom name for the service method responsible for initializing PivotTreeMap.

#### Default Value: "InitializeTreemap"

**Example:**

{% highlight javascript %}
 
    $("#PivotTreeMap1").ejPivotTreeMap({ serviceMethodSettings: { initialize: "IninlizeTreeMapMyMethod" } });
{% endhighlight %}

### serviceMethodSettings.drillDown `string`
{:#members:servicemethodsettings-drilldown}

Allows the user to set the custom name for the service method responsible for drilling up/down operation in PivotTreeMap.

#### Default Value: "DrillTreeMap"

**Example:**

{% highlight javascript %}
 
    $("#PivotTreeMap1").ejPivotTreeMap({ serviceMethodSettings: { drillDown: "DrillTreeMapMyMethod" } });
{% endhighlight %}


### url `string`
{:#members:url}

Connects the service using the specified URL for any server updates.

#### Default Value: “”

**Example:**

{% highlight javascript %}
 
    $("#PivotTreeMap1").ejPivotTreeMap({ url: "/PivotTreeMapService" });
{% endhighlight %}


## Methods

### doAjaxPost()
{:#methods:doajaxpost}

Performs an asynchronous HTTP (AJAX) request.

**Example:**

{% highlight javascript %}
 
    var treemapObj = $("#PivotTreeMap1").data("ejPivotTreeMap");
    treemapObj.doAjaxPost("POST", "/PivotTreeMapService.svc/Initialize", { "key", "Hello World" }, successEvent, null);
{% endhighlight %}

### getOlapReport()
{:#methods:getolapreport}

Returns the OlapReport string maintained along with the axis elements information.

>**Note**: This method is applicable only on operating the control in server mode.

**Example:**

{% highlight javascript %}
 
    var treeMapObj = $("#PivotTreeMap1").data("ejPivotTreeMap");
    var report = treeMapObj.getOlapReport();
{% endhighlight %}

### setOlapReport()
{:#methods:setolapreport}

Sets the OlapReport string along with the axis information and maintains it in a property.

>**Note**: This method is applicable only on operating the control in server mode.

**Example:**

{% highlight javascript %}
 
    var treeMapObj = $("#PivotTreeMap1").data("ejPivotTreeMap");
    treeMapObj.setOlapReport(olapReportObj);
{% endhighlight %}

### getJSONRecords()
{:#methods:getjsonrecords}

Returns the JSON records formed to render the control.

**Example:**

{% highlight javascript %}
 
    var treeMapObj = $("#PivotTreeMap1").data("ejPivotTreeMap");
    var jsonRecords = treeMapObj.getJSONRecords();
{% endhighlight %}

### setJSONRecords()
{:#methods:setjsonrecords}

Sets the JSON records to render the control.

**Example:**

{% highlight javascript %}
 
    var treeMapObj = $("#PivotTreeMap1").data("ejPivotTreeMap");
    treeMapObj.setJSONRecords(jsonRecords);
{% endhighlight %}

### generateJSON()
{:#methods:generatejson}

Renders the control with the pivot engine obtained from olap cube.

**Example:**

{% highlight javascript %}
 
    var treeMapObj = $("#PivotTreeMap1").data("ejPivotTreeMap");
    treeMapObj.generateJSON(baseObj, pivotEngineObj);
{% endhighlight %}

### renderTreeMapFromJSON()
{:#methods:rendertreemapfromjson}

This function receives the JSON formatted datasource to render the PivotTreeMap control.

**Example:**

{% highlight javascript %}
 
    var treeMapObj = $("#PivotTreeMap1").data("ejPivotTreeMap");
    treeMapObj.renderTreeMapFromJSON(this.getJSONRecords());
{% endhighlight %}

### renderControlSuccess()
{:#methods:rendercontrolsuccess}

This function receives the update from service-end, which would be utilized for rendering the widget.

**Example:**

{% highlight javascript %}
 
    var treeMapObj = $("#PivotTreeMap1").data("ejPivotTreeMap");
    treeMapObj.renderControlSuccess({ "OlapReport": this.getOlapReport(), "JsonRecords": this.getJSONRecords() });
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
 
    $("#PivotTreeMap1").ejPivotTreeMap({
        afterServiceInvoke: function (args) {}
    });
{% endhighlight %}


### beforeServiceInvoke
{:#events:beforeserviceinvoke}

Triggers before any AJAX request is passed from PivotTreeMap to service methods.

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
 
    $("#PivotTreeMap1").ejPivotTreeMap({
        beforeServiceInvoke: function (args) {}
    });
{% endhighlight %}

### load
{:#events:load}

Triggers when PivotTreeMap starts to render.

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
 
    $("#PivotTreeMap1").ejPivotTreeMap({
        load: function (args) {}
    });
{% endhighlight %}

### beforePivotEnginePopulate
{:#events:beforepivotenginepopulate}

Triggers before populating the pivot engine from datasource.

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
<td class="name">treeMapObject</td>
<td class="type">object</td>
<td class="description last">returns the current instance of PivotTreeMap control.</td>
</tr>
</tbody>
</table>


**Example:**

{% highlight javascript %}
 
    $("#PivotTreeMap1").ejPivotTreeMap({
        beforePivotEnginePopulate: function (args) {}
    });
{% endhighlight %}

### drillSuccess
{:#events:drillsuccess}

Triggers when drill up/down happens in PivotTreeMap control. And it returns the outer HTML of PivotTreeMap control.

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
<td class="description last">return the HTML element of PivotTreeMap control.</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight javascript %}
 
    $("#PivotTreeMap1").ejPivotTreeMap({
        drillSuccess: function (args) {}
    });
{% endhighlight %}


### renderComplete
{:#events:rendercomplete}

Triggers when PivotTreeMap widget completes all operations at client-side after any AJAX request.

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
 
    $("#PivotTreeMap1").ejPivotTreeMap({
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
<tr>
<td class="name">message</td>
<td class="type">string</td>
<td class="description last">returns the error stack trace of the original exception.</td>
</tr>
</tbody>
</table>


**Example:**

{% highlight javascript %}
 
    $("#PivotTreeMap1").ejPivotTreeMap({
        renderFailure: function (args) {}
    });
{% endhighlight %}


### renderSuccess
{:#events:rendersuccess}

Triggers when PivotTreeMap successfully reaches client-side after any AJAX request.

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
 
    $("#PivotTreeMap1").ejPivotTreeMap({
        renderSuccess: function (args) {}
    });
{% endhighlight %}