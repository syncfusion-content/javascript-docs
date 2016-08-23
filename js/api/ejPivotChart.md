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

The PivotChart is a lightweight control that reads OLAP information and visualizes it in graphical format with the ability to drill up and down.

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

* module:jQuery-1.10.2.min.js
* module:jQuery.easing.1.3.min.js
* module:jQuery.globalize.min.js
* module:ej.core.js
* module:ej.data.js
* module:ej.touch.js
* module:ej.dialog.js
* module:ej.draggable.js
* module:ej.waitingpopup.js
* module:ej.chart.js
* module:ej.olap.base.js
* module:ej.pivotanalysis.base.js
* module:ej.pivotchart.js


## Members

### analysisMode `object`
{:#members:analysismode}

Sets the mode for the PivotChart widget for binding either OLAP or Relational data source.

#### Default Value: ej.PivotChart.AnalysisMode.Olap

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({analysisMode: ej.PivotChart.AnalysisMode.Relational });  

{% endhighlight %}


### cssClass `string`
{:#members:cssclass}

Specifies the CSS class to PivotChart to achieve custom theme.

#### Default Value: “”

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({ cssClass : "gradient-lime" });

{% endhighlight %}

### commonSeriesOptions `object`
{:#members:commonseriesoptions}

Options available to configure the properties of entire series. You can also override the options for specific series by using series collection.

#### Default Value: {}

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({commonSeriesOptions: {type: ej.PivotChart.ChartTypes.Line}});

{% endhighlight %}

### currentReport `string`
{:#members:currentreport}

Contains the serialized OlapReport at that instant, that is, current OlapReport. 

#### Default Value: “”

### dataSource `object`
{:#members:datasource}

Initializes the data source for the PivotChart widget, when it functions completely on client-side.

#### Default Value: {}

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({dataSource: {data:value}});

{% endhighlight %}


### dataSource.catalog `string`
{:#members:datasource-catalog}

Contains the database name as string type to fetch the data from the given connection string.

#### Default Value: “”

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({dataSource: {catalog: value}});

{% endhighlight %}


### dataSource.columns `array`
{:#members:datasource-columns}

Lists out the items to be arranged in column section of PivotChart.

#### Default Value: []

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({dataSource: {columns: itemsArray}});

{% endhighlight %}


### dataSource.columns.fieldName `string`
{:#members:datasource-columns-fieldname}

Allows the user to bind the item by using its unique name as field name.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({dataSource: {columns: [{ fieldName : value}]}});

{% endhighlight %}


### dataSource.columns.fieldCaption `string`
{:#members:datasource-columns-fieldcaption}

Allows the user to set the display name for an item.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({dataSource: {columns: [{ fieldCaption : value}]}});

{% endhighlight %}


### dataSource.columns.isNamedSets `boolean`
{:#members:datasource-columns-isnamedsets}

Allows the user to enable the usage of named set items in respective axis. This is only applicable for OLAP datasource.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({dataSource: {columns: [{ isNamedSets : true}]}});

{% endhighlight %}


### dataSource.cube `string`
{:#members:datasource-cube}

Contains the respective Cube name from database as string type.

#### Default Value: “”

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({dataSource: {cube: value}});

{% endhighlight %}


### dataSource.data `object`
{:#members:datasource-data}

Provides the raw data source for the PivotChart.

#### Default Value: null

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({dataSource: {data: value}});

{% endhighlight %}


### dataSource.rows `array`
{:#members:datasource-rows}

Lists out the items to be arranged in row section of PivotChart.

#### Default Value: []

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({dataSource: {rows: itemsArray}});

{% endhighlight %}


### dataSource.rows.fieldName `string`
{:#members:datasource-rows-fieldname}

Allows the user to bind the item by using its unique name as field name.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({dataSource: {rows: [{ fieldName : value}]}});

{% endhighlight %}


### dataSource.rows.fieldCaption `string`
{:#members:datasource-rows-fieldcaption}

Allows the user to set the display name for an item.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({dataSource: {rows: [{ fieldCaption : value}]}});

{% endhighlight %}


### dataSource.rows.isNamedSets `boolean`
{:#members:datasource-rows-isnamedsets}

Allows the user to enable the usage of named set items in respective axis. This is only applicable for OLAP datasource.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({dataSource: {rows: [{ isNamedSets : true}]}});

{% endhighlight %}

### dataSource.values `array`
{:#members:datasource-values}

Lists out the items which supports calculation in PivotChart.

#### Default Value: []

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({dataSource: {values: itemsArray}});

{% endhighlight %}

### dataSource.values.measures `array`
{:#members:datasource-values[0]-measures}

This holds the measures unique name to bind them from the Cube.

#### Default Value: []

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({dataSource: {values: [{measures : itemsArray}]}});

{% endhighlight %}

### dataSource.values.axis `string`
{:#members:datasource-values[0]-axis}

Allows to set the axis name to place the measures items.

#### Default Value: “”

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({dataSource: {values: [{axis : value}]}});

{% endhighlight %}


### dataSource.values.fieldName `string`
{:#members:datasource-values[0]-fieldname}

Allows the user to bind the item by using its unique name as field name.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({dataSource: {values: [{ fieldName : value}]}});

{% endhighlight %}


### dataSource.values.fieldCaption `string`
{:#members:datasource-values[0]-fieldcaption}

Allows the user to set the display name for an item.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({dataSource: {values: [{ fieldCaption : value}]}});

{% endhighlight %}

### dataSource.filters `array`
{:#members:datasource-filters}

Lists out the items which supports filtering of values in PivotChart.

#### Default Value: []

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({dataSource: {filters: itemsArray}});

{% endhighlight %}

### dataSource.filters.fieldName `string`
{:#members:datasource-filters-fieldname}

Allows the user to bind the item by using its unique name as field name.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({dataSource: {filters: [{ fieldName : value}]}});

{% endhighlight %}


### dataSource.filters.fieldCaption `string`
{:#members:datasource-filters-fieldcaption}

Allows the user to set the display name for an item.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({dataSource: {filters: [{ fieldCaption : value}]}});

{% endhighlight %}


### dataSource.filters.isNamedSets `boolean`
{:#members:datasource-filters-isnamedsets}

Allows the user to enable the usage of named set items in respective axis. This is only applicable for OLAP datasource.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({dataSource: {filters: [{ isNamedSets : true}]}});

{% endhighlight %}


### customObject `object`
{:#members:customobject}

Object utilized to pass additional information between client-end and service-end.

#### Default Value: {}

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({ customObject: {"key":"Hello World"} });

{% endhighlight %}

### enable3D `boolean`
{:#members:enable3d}

Allows the user to enable 3D view of PivotChart.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({ enable3D: true });

{% endhighlight %}

### enableRTL `boolean`
{:#members:enablertl}

Allows the user to view PivotChart from right to left.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({ enableRTL: true });

{% endhighlight %}

### isResponsive `boolean`
{:#members:isresponsive}

Allows the user to enable PivotChart’s responsiveness in the browser layout.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({ isResponsive: true });

{% endhighlight %}

### legend `object`
{:#members:legend}

Options available to customize the legend items and its title.

#### Default Value: {}

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({legend: {visible: true}});

{% endhighlight %}

### locale `string`
{:#members:locale}

Allows the user to set the localized language for the widget.

#### Default Value: "en-US"

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({ locale: "fr-FR" }); 

{% endhighlight %}

### operationalMode `object`
{:#members:operationalmode}

Sets the mode for the PivotChart widget for binding data source either in server-side or client-side.

#### Default Value: ej.PivotChart.OperationalMode.ClientMode

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({operationalMode: ej.PivotChart.OperationalMode.ServerMode});

{% endhighlight %}

### primaryXAxis `object`
{:#members:primaryxaxis}

This is a horizontal axis that contains options to configure axis and it is the primary x axis for all the series in series array. To override x axis for particular series, create an axis object by providing unique name by using name property and add it to axes array. Then, assign the name to the series&rsquo;s xAxisName property to link both axis and series.

#### Default Value: {}

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({ primaryXAxis: { title: { text: "Fiscal Year" }, labelRotation: 0 });

{% endhighlight %}

### primaryYAxis `object`
{:#members:primaryyaxis}

This is a vertical axis that contains options to configure axis. This is the primary y axis for all the series in series array. To override y axis for particular series, create an axis object by providing unique name by using name property and add it to axes array. Then, assign the name to the series&rsquo;s yAxisName property to link both axis and series.

#### Default Value: {}

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({ title: { text: "Customer Count"} });

{% endhighlight %}

### rotation `number`
{:#members:rotation}

Allows the user to rotate the angle of PivotChart in 3D view.

#### Default Value: 0

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({ rotation: 45 }); 

{% endhighlight %}


### serviceMethodSettings `object`
{:#members:servicemethodsettings}

Allows the user to set custom name for the methods at service-end, communicated on AJAX post.

#### Default Value: {}

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({ serviceMethodSettings: {initialize: "MyMethod1", drillDown: "MyMethod2"} });

{% endhighlight %}

### serviceMethodSettings.drillDown `string`
{:#members:servicemethodsettings-drilldown}

Allows the user to set the custom name for the service method that&rsquo;s responsible for drilling up/down operation in PivotChart.

#### Default Value: "DrillChart"

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({ serviceMethodSettings: {drillDown: "DrillChartMyMethod"} });                                       

{% endhighlight %}

### serviceMethodSettings.exportPivotChart `string`
{:#members:servicemethodsettings-exportpivotchart}

Allows the user to set the custom name for the service method that’s responsible for exporting.

#### Default Value: "Export"

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({ serviceMethodSettings: { exportPivotChart: "ExportMyMethod" } })

{% endhighlight %}

### serviceMethodSettings.initialize `string`
{:#members:servicemethodsettings-initialize}

Allows the user to set the custom name for the service method that&rsquo;s responsible for initializing PivotChart.

#### Default Value: "InitializeChart"

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({ serviceMethodSettings: {initialize: "IninlizeChartMyMethod"} });

 {% endhighlight %}


### size `object`
{:#members:size}

Options to customize the Chart size.

#### Default Value: {}

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({ size: { height: "450px", width: "95%" } });

{% endhighlight %}

###  url `string`
{:#members:url}

Connects the service using the specified URL for any server updates.

#### Default Value: “”

**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({ url: "/PivotChartService.svc" });

{% endhighlight %}


## Methods

### doAjaxPost()
{:#methods:doajaxpost}

Perform an asynchronous HTTP (AJAX) request.

**Example:**

{% highlight html %}
 
<div id="PivotChart1"></div> 
 
<script>
$('#PivotChart1').ejPivotChart({
      url: "PivotChartService.svc",
                animation: true, type: ej.PivotChart.ChartTypes.Column, 
                       commonSeriesOptions: { type: ej.PivotChart.ChartTypes.Column, tooltip: { visible: true} },
                       size: { height: 460, width: 950 }, primaryXAxis: { title: { text: "Fiscal Year" }, labelRotation: 0 },
                       primaryYAxis: { title: { text: "Customer Count"} }, legend: { visible: true, rowCount: 2 },
                       load: "loadTheme"
 });
var chartObj = $("#PivotChart1").data("ejPivotChart");
chartObj.doAjaxPost("POST", "/PivotChartService.svc/Initialize", {"key", "Hello World"}, "renderControlSuccess", null);
</script>

{% endhighlight %}



### doPostBack()
{:#methods:dopostback}

Perform an asynchronous HTTP (FullPost) submit.

**Example:**

{% highlight html %}

<div id="PivotChart1"></div> 
 
<script>
$('#PivotChart1).ejPivotChart({
      url: "PivotChartService.svc",
 });
var chartObj = $("#PivotChart1").data("ejPivotChart");
chartObj.doPostBack("/PivotChartService.svc/Initialize", {"key", "Hello World"});
</script> 

{% endhighlight %}


### exportPivotChart()
{:#methods:exportpivotchart}

Exports the PivotChart to an appropriate format based on the parameter passed.
  
**Example:**

{% highlight html %}
 
<div id="PivotChart1"></div> 
 
<script>
var chartObj = $("#PivotChart1").data("ejPivotChart");
chartObj.exportPivotChart(ej.PivotChart.ExportOptions.Excel);
</script>

{% endhighlight %}


### renderChartFromJSON()
{:#methods:renderchartfromjson}

This function receives the JSON formatted datasource to render the PivotChart control.


**Example:**

{% highlight html %}
 
<div id="PivotChart1"></div> 
 
<script>
$('#PivotChart1').ejPivotChart({
      url: "PivotChartService.svc",
                animation: true, type: ej.PivotChart.ChartTypes.Column, 
                       commonSeriesOptions: { type: ej.PivotChart.ChartTypes.Column, tooltip: { visible: true} },
                       size: { height: 460, width: 950 }, primaryXAxis: { title: { text: "Fiscal Year" }, labelRotation: 0 },
                       primaryYAxis: { title: { text: "Customer Count"} }, legend: { visible: true, rowCount: 2 },
                       load: "loadTheme"
 });
var chartObj = $("#PivotChart1").data("ejPivotChart");
chartObj.renderControlFromJSON(this.getJSONRecords());
</script>

{% endhighlight %}

### renderControlSuccess()
{:#methods:rendercontrolsuccess}

This function receives the update from service-end, which would be utilized for rendering the widget.

**Example:**

{% highlight html %}
 
<div id="PivotChart1"></div> 
 
<script>
$('#PivotChart1').ejPivotChart({
      url: "PivotChartService.svc",
                animation: true, type: ej.PivotChart.ChartTypes.Column, 
                       commonSeriesOptions: { type: ej.PivotChart.ChartTypes.Column, tooltip: { visible: true} },
                       size: { height: 460, width: 950 }, primaryXAxis: { title: { text: "Fiscal Year" }, labelRotation: 0 },
                       primaryYAxis: { title: { text: "Customer Count"} }, legend: { visible: true, rowCount: 2 },
                       load: "loadTheme"
  });
var chartObj = $("#PivotChart1").data("ejPivotChart");
chartObj.renderControlSuccess({"OlapReport": this.getOlapReport(), "JsonRecords": this.getJSONRecords()});
</script>

{% endhighlight %}


## Events


### load
{:#events:load}

Triggers when PivotChart starts to render.

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
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description last">Event parameters from PivotChart
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
<td class="description last">return the current action of PivotChart control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">return the custom object bounds with PivotChart control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">return the outer HTML of PivotChart control.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.PivotChart.Model"/>object</td>
<td class="description last">returns the PivotChart model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


**Example:**

{% highlight html %}
 
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
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description last">Event parameters from PivotChart
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
<td class="description last">return the current action of PivotChart control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">return the custom object bounds with PivotChart control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">return the outer HTML of PivotChart control.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.PivotChart.Model"/>object</td>
<td class="description last">returns the PivotChart model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


**Example:**

{% highlight html %}
 
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
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description last">Event parameters from PivotChart
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
<td class="description last">return the current action of PivotChart control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">return the custom object bounds with PivotChart control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">return the outer HTML of PivotChart control.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.PivotChart.Model"/>object</td>
<td class="description last">returns the PivotChart model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({
   beforeServiceInvoke: function (args) {}
});      

{% endhighlight %}



### drillSuccess
{:#events:drillsuccess}

Triggers when drill up/down happens in PivotChart control.

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
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description last">Event parameters from PivotChart
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
<td class="type"><ts ref="ej.PivotChart.Model"/>object</td>
<td class="description last">returns the PivotChart model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


**Example:**

{% highlight html %}
 
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
<th>Name</th>
<th>Type</th>
<th >Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description last">Event parameters from PivotChart
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
<td class="description last">return the current action of PivotChart control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">return the custom object bounds with PivotChart control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">return the outer HTML of PivotChart control.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.PivotChart.Model"/>object</td>
<td class="description last">returns the PivotChart model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


**Example:**

{% highlight html %}
 
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
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description last">Event parameters from PivotChart
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
<td class="description last">return the current action of PivotChart control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">return the custom object bounds with PivotChart control.</td>
</tr>
<tr>
<td class="name">message</td>
<td class="type">object</td>
<td class="description last">return the error stack trace of the original exception.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">return the outer HTML of PivotChart control.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.PivotChart.Model"/>object</td>
<td class="description last">returns the PivotChart model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


**Example:**

{% highlight html %}
 
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
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description last">Event parameters from PivotChart
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
<td class="description last">return the current action of PivotChart control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">return the custom object bounds with PivotChart control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">return the outer HTML of PivotChart control.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.PivotChart.Model"/>object</td>
<td class="description last">returns the PivotChart model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


**Example:**

{% highlight html %}
 
$("#PivotChart1").ejPivotChart({
   renderSuccess: function (args) {}
});     

{% endhighlight %}



## Enumeration

### AnalysisMode  `enum`
{:#enum:analysismode}

<ts name = "ej.PivotChart.AnalysisMode"/>

Sets the mode for the PivotChart widget for binding either OLAP or relational data source.

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
            <td class="description">To bind an OLAP data source to PivotChart.</td>
        </tr>
        <tr>
            <td class="name">Relational</td>
            <td class="description">To bind a relational data source to PivotChart.</td>
        </tr>
    </tbody>
</table>


**Example:**

{% highlight html %}

$("#PivotChart1").ejPivotChart({analysisMode: ej.PivotChart.AnalysisMode.Olap});

{% endhighlight %}


### OperationalMode  `enum`
{:#enum:operationalmode}

<ts name = "ej.PivotChart.OperationalMode"/>

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


**Example:**

{% highlight html %}

$("#PivotChart1").ejPivotChart({operationalMode:ej.PivotChart.OperationalMode.ServerMode});

{% endhighlight %}


### SymbolShapes  `enum`
{:#enum:symbolshapes}

<ts name = "ej.PivotChart.SymbolShapes"/>

Allows the user to set shape for the marker.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">None</td>
            <td class="description">Does not set any shape for the marker.</td>
        </tr>
        <tr>
            <td class="name">LeftArrow</td>
            <td class="description">To set left arrow shape for the marker</td>
        </tr>
        <tr>
            <td class="name">RightArrow</td>
            <td class="description">To set right arrow shape for the marker.</td>
        </tr>
        <tr>
            <td class="name">Circle</td>
            <td class="description">To set circle shape for the marker.</td>
        </tr>
        <tr>
            <td class="name">Cross</td>
            <td class="description">To set cross shape for the marker.</td>
        </tr>
        <tr>
            <td class="name">HorizLine</td>
            <td class="description">To set horizontal line shape for the marker.</td>
        </tr>
        <tr>
            <td class="name">VertLine</td>
            <td class="description">To set vertical line shape for the marker.</td>
        </tr>
        <tr>
            <td class="name">Diamond</td>
            <td class="description">To set diamond shape for the marker.</td>
        </tr>
        <tr>
            <td class="name">Rectangle</td>
            <td class="description">To set rectangle shape for the marker.</td>
        </tr>
        <tr>
            <td class="name">Triangle</td>
            <td class="description">To set triangle shape for the marker.</td>
        </tr>
        <tr>
            <td class="name">InvertedTriangle</td>
            <td class="description">To set inverted triangle shape for the marker.</td>
        </tr>
        <tr>
            <td class="name">Hexagon</td>
            <td class="description">To set hexagon shape for the marker.</td>
        </tr>
        <tr>
            <td class="name">Pentagon</td>
            <td class="description">To set pentagon shape for the marker.</td>
        </tr>
        <tr>
            <td class="name">Star</td>
            <td class="description">To set star shape for the marker.</td>
        </tr>
        <tr>
            <td class="name">Ellipse</td>
            <td class="description">To set ellipse shape for the marker.</td>
        </tr>
        <tr>
            <td class="name">Wedge</td>
            <td class="description">To set wedge shape for the marker.</td>
        </tr>
        <tr>
            <td class="name">Trapezoid</td>
            <td class="description">To set trapezoid shape for the marker.</td>
        </tr>
        <tr>
            <td class="name">UpArrow</td>
            <td class="description">To set up arrow shape for the marker.</td>
        </tr>
        <tr>
            <td class="name">DownArrow</td>
            <td class="description">To set down arrow shape for the marker.</td>
        </tr>
        <tr>
            <td class="name">Image</td>
            <td class="description">To set image shape for the marker.</td>
        </tr>
    </tbody>
</table>

**Example:**

{% highlight html %}

$("#PivotChart1").ejPivotChart({commonSeriesOptions :{marker :{ shape: ej.PivotChart.SymbolShapes.LeftArrow} }});

{% endhighlight %}


### ChartTypes `enum`
{:#enum:charttypes}

<ts name = "ej.PivotChart.ChartTypes"/>

Allows the user to set the type for PivotChart.

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

{% highlight html %}

$("#PivotChart1").ejPivotChart({commonSeriesOptions :{ type: ej.PivotChart.ChartTypes.Column} });

{% endhighlight %}

### ExportOption  `enum`
{:#enum:exportoption }

<ts name = "ej.PivotChart.ExportOptions"/>

Allows the user to export PivotChart to an appropriate format based on the parameter passed.

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
            <td class="description">To export PivotChart in Excel format.</td>
        </tr>
        <tr>
            <td class="name">Word</td>
            <td class="description">To export PivotChart in Word format.</td>
        </tr>
        <tr>
            <td class="name">PDF</td>
            <td class="description">To export PivotChart in PDF format.</td>
        </tr>
        <tr>
            <td class="name">CSV</td>
            <td class="description">To export PivotChart in CSV format.</td>
        </tr>
        <tr>
            <td class="name">PNG</td>
            <td class="description">To export PivotChart in PNG format.</td>
        </tr>
        <tr>
            <td class="name">JPG</td>
            <td class="description">To export PivotChart in JPG format.</td>
        </tr>
        <tr>
            <td class="name">EMF</td>
            <td class="description">To export PivotChart in EMF format.</td>
        </tr>
        <tr>
            <td class="name">GIF</td>
            <td class="description">To export PivotChart in GIF format.</td>
        </tr>
        <tr>
            <td class="name">BMP</td>
            <td class="description">To export PivotChart in BMP format.</td>
        </tr>
    </tbody>
</table>

**Example:**

{% highlight html %}

$("#PivotChart1").ejPivotChart({commonSeriesOptions :{ exportPivotChart: ej.PivotChart.ExportOptions.Excel } });

{% endhighlight %}
