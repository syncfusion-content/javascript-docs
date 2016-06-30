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

The PivotTreemap is a lightweight control that reads OLAP and Relational information and visualizes it in graphical format with the ability to drill up and down.

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

* module:jQuery-1.10.2.min.js
* module:jQuery.easing.1.3.min.js
* module:jQuery.globalize.min.js
* module:ej.core.js
* module:ej.data.js
* module:ej.touch.js
* module:ej.dialog.js
* module:ej.draggable.js
* module:ej.waitingpopup.js
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

{% highlight html %}
 
$("#PivotTreeMap1").ejPivotTreeMap({ cssClass : "gradient-lime" });

{% endhighlight %}


### currentReport `string`
{:#members:currentreport}

Contains the serialized Report at that instant, that is, current Report. 

#### Default Value: “”

### dataSource `object`
{:#members:datasource}

Initializes the data source for the PivotTreeMap widget, when it functions completely on client-side.

#### Default Value: {}

**Example:**

{% highlight html %}
 
$("#PivotTreeMap1").ejPivotTreeMap({dataSource: {data:value}});

{% endhighlight %}


### dataSource.catalog `string`
{:#members:datasource-catalog}

Contains the database name as string type to fetch the data from the given connection string.

#### Default Value: “”

**Example:**

{% highlight html %}
 
$("#PivotTreeMap1").ejPivotTreeMap({dataSource: {catalog: value}});

{% endhighlight %}


### dataSource.columns `array`
{:#members:datasource-columns}

Lists out the items to be arranged in column section of PivotTreeMap.

#### Default Value: []

**Example:**

{% highlight html %}
 
$("#PivotTreeMap1").ejPivotTreeMap({dataSource: {columns: itemsArray}});

{% endhighlight %}

### dataSource.columns.fieldName `string`
{:#members:datasource-columns-fieldname}

Allows the user to bind the item by using its uniquename as field name.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotTreeMap1").ejPivotTreeMap({dataSource: {columns: [{ fieldName : value}]}});

{% endhighlight %}


### dataSource.columns.fieldCaption `string`
{:#members:datasource-columns-fieldcaption}

Allows the user to set the display name for an item.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotTreeMap1").ejPivotTreeMap({dataSource: {columns: [{ fieldCaption : value}]}});

{% endhighlight %}


### dataSource.columns.isNamedSets `boolean`
{:#members:datasource-columns-isnamedsets}

Allows the user to enable the usage of namedset items in respective axis. This is only applicable for OLAP datasource.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotTreeMap1").ejPivotTreeMap({dataSource: {columns: [{ isNamedSets : true}]}});

{% endhighlight %}


### dataSource.cube `string`
{:#members:datasource-cube}

Contains the respective Cube name from database as string type.

#### Default Value: “”

**Example:**

{% highlight html %}
 
$("#PivotTreeMap1").ejPivotTreeMap({dataSource: {cube: value}});

{% endhighlight %}


### dataSource.data `object`
{:#members:datasource-data}

Provides the raw data source for the PivotTreeMap.

#### Default Value: null

**Example:**

{% highlight html %}
 
$("#PivotTreeMap1").ejPivotTreeMap({dataSource: {data: value}});

{% endhighlight %}


### dataSource.rows `array`
{:#members:datasource-rows}

Lists out the items to be arranged in row section of PivotTreeMap.

#### Default Value: []

**Example:**

{% highlight html %}
 
$("#PivotTreeMap1").ejPivotTreeMap({dataSource: {rows: itemsArray}});

{% endhighlight %}

### dataSource.rows.fieldName `string`
{:#members:datasource-rows-fieldname}

Allows the user to bind the item by using its uniquename as field name.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotTreeMap1").ejPivotTreeMap({dataSource: {rows: [{ fieldName : value}]}});

{% endhighlight %}


### dataSource.rows.fieldCaption `string`
{:#members:datasource-rows-fieldcaption}

Allows the user to set the display name for an item.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotTreeMap1").ejPivotTreeMap({dataSource: {rows: [{ fieldCaption : value}]}});

{% endhighlight %}


### dataSource.rows.isNamedSets `boolean`
{:#members:datasource-rows-isnamedsets}

Allows the user to enable the usage of namedset items in respective axis. This is only applicable for OLAP datasource.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotTreeMap1").ejPivotTreeMap({dataSource: {rows: [{ isNamedSets : true}]}});

{% endhighlight %}


### dataSource.values `array`
{:#members:datasource-values}

Lists out the items which supports calculation in PivotTreeMap.

#### Default Value: []

**Example:**

{% highlight html %}
 
$("#PivotTreeMap1").ejPivotTreeMap({dataSource: {values: itemsArray}});

{% endhighlight %}

### dataSource.values.measures `array`
{:#members:datasource-values[0]-measures}

This holds the measures unique name to bind them from the Cube.

#### Default Value: []

**Example:**

{% highlight html %}
 
$("#PivotTreeMap1").ejPivotTreeMap({dataSource: {values: [{measures : itemsArray}]}});

{% endhighlight %}

### dataSource.values.axis `string`
{:#members:datasource-values[0]-axis}

Allows to set the axis name to place the measures items.

#### Default Value: “”

**Example:**

{% highlight html %}
 
$("#PivotTreeMap1").ejPivotTreeMap({dataSource: {values: [{axis : value}]}});

{% endhighlight %}

### dataSource.values.fieldName `string`
{:#members:datasource-values[0]-fieldname}

Allows the user to bind the item by using its uniquename as field name.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotTreeMap1").ejPivotTreeMap({dataSource: {values: [{ fieldName : value}]}});

{% endhighlight %}


### dataSource.values.fieldCaption `string`
{:#members:datasource-values[0]-fieldcaption}

Allows the user to set the display name for an item.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotTreeMap1").ejPivotTreeMap({dataSource: {values: [{ fieldCaption : value}]}});

{% endhighlight %}


### dataSource.filters `array`
{:#members:datasource-filters}

Lists out the items which supports filtering of values in PivotTreeMap.

#### Default Value: []

**Example:**

{% highlight html %}
 
$("#PivotTreeMap1").ejPivotTreeMap({dataSource: {filters: itemsArray}});

{% endhighlight %}

### dataSource.filters.fieldName `string`
{:#members:datasource-filters-fieldname}

Allows the user to bind the item by using its uniquename as field name.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotTreeMap1").ejPivotTreeMap({dataSource: {filters: [{ fieldName : value}]}});

{% endhighlight %}


### dataSource.filters.fieldCaption `string`
{:#members:datasource-filters-fieldcaption}

Allows the user to set the display name for an item.

#### Default Value: ""

**Example:**

{% highlight html %}
 
$("#PivotTreeMap1").ejPivotTreeMap({dataSource: {filters: [{ fieldCaption : value}]}});

{% endhighlight %}


### dataSource.filters.isNamedSets `boolean`
{:#members:datasource-filters-isnamedsets}

Allows the user to enable the usage of namedset items in respective axis. This is only applicable for OLAP datasource.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotTreeMap1").ejPivotTreeMap({dataSource: {filters: [{ isNamedSets : true}]}});

{% endhighlight %}


### customObject `object`
{:#members:customobject}

Object utilized to pass additional information between client-end and service-end.

#### Default Value: {}

**Example:**

{% highlight html %}
 
$("#PivotTreeMap1").ejPivotTreeMap({ customObject: {"key":"Hello World"} });

{% endhighlight %}


### enableRTL `boolean`
{:#members:enablertl}

Allows the user to view the layout of PivotTreeMap from right to left.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotTreeMap1").ejPivotTreeMap({ enableRTL: true });

{% endhighlight %}

### isResponsive `boolean`
{:#members:isresponsive}

Allows the user to enable PivotTreeMap’s responsiveness in the browser layout.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotTreeMap1").ejPivotTreeMap({ isResponsive: true });

{% endhighlight %}


### locale `string`
{:#members:locale}

Allows the user to set the localized language for the widget.

#### Default Value: "en-US"

**Example:**

{% highlight html %}
 
$("#PivotTreeMap1").ejPivotTreeMap({ locale: "fr-FR" }); 

{% endhighlight %}

### operationalMode `object`
{:#members:operationalmode}

Sets the mode for the PivotTreeMap widget for binding data source either in server-side or client-side.

#### Default Value: ej.PivotTreeMap.OperationalMode.ClientMode

**Example:**

{% highlight html %}
 
$("#PivotTreeMap1").ejPivotTreeMap({operationalMode: ej.PivotTreemap.OperationalMode.ServerMode});

{% endhighlight %}


### serviceMethodSettings `object`
{:#members:servicemethodsettings}

Allows the user to set custom name for the methods at service-end, communicated on AJAX post.

#### Default Value: {}

**Example:**

{% highlight html %}
 
$("#PivotTreeMap1").ejPivotTreeMap({ serviceMethodSettings: values });

{% endhighlight %}

### serviceMethodSettings.initialize `string`
{:#members:servicemethodsettings-initialize}

Allows the user to set the custom name for the service method that&rsquo;s responsible for initializing PivotTreeMap.

#### Default Value: "InitializeTreemap"

**Example:**

{% highlight html %}
 
$("#PivotTreeMap1").ejPivotTreeMap({ serviceMethodSettings: {initialize: "IninlizeTreeMapMyMethod"} });

 {% endhighlight %}

### serviceMethodSettings.drillDown `string`
{:#members:servicemethodsettings-drilldown}

Allows the user to set the custom name for the service method that&rsquo;s responsible for drilling up/down operation in PivotTreeMap.

#### Default Value: "DrillTreeMap"

**Example:**

{% highlight html %}
 
$("#PivotTreeMap1").ejPivotTreeMap({ serviceMethodSettings: {drillDown: "DrillTreeMapMyMethod"} });                                       

{% endhighlight %}


###  url `string`
{:#members:url}

Connects the service using the specified URL for any server updates.

#### Default Value: “”

**Example:**

{% highlight html %}
 
$("#PivotTreeMap1").ejPivotTreeMap({ url: "/PivotTreeMapService.svc" });

{% endhighlight %}


## Methods

### doAjaxPost()
{:#methods:doajaxpost}

Perform an asynchronous HTTP (AJAX) request.

**Example:**

{% highlight html %}
 
<div id="PivotTreeMap1"></div> 
 
<script>
$('#PivotTreeMap1').ejPivotTreeMap({
      url: "PivotTreeMapService.svc"
 });
var treemapObj = $("#PivotTreeMap1").data("ejPivotTreeMap");
treemapObj.doAjaxPost("POST", "/PivotTreeMapService.svc/Initialize", {"key", "Hello World"}, "renderControlSuccess", null);
</script>

{% endhighlight %}



### doPostBack()
{:#methods:dopostback}

Perform an asynchronous HTTP (FullPost) submit.

**Example:**

{% highlight html %}

<div id="PivotTreeMap1"></div> 
 
<script>
$('#PivotTreeMap1).ejPivotTreeMap({
      url: "PivotTreeMapService.svc",
 });
var treemapObj = $("#PivotTreeMap1").data("ejPivotTreeMap");
treemapObj.doPostBack("/PivotTreeMapService.svc/Initialize", {"key", "Hello World"});
</script> 

{% endhighlight %}


### renderTreeMapFromJSON()
{:#methods:rendertreemapfromjson}

This function receives the JSON formatted datasource to render the PivotTreeMap control.


**Example:**

{% highlight html %}
 
<div id="PivotTreeMap1"></div> 
 
<script>
$('#PivotTreeMap1').ejPivotTreeMap({
      url: "PivotTreeMap.svc"
 });
var treeMapObj = $("#PivotTreeMap1").data("ejPivotTreeMap");
treeMapObj.renderTreeMapFromJSON(this.getJSONRecords());
</script>

{% endhighlight %}

### renderControlSuccess()
{:#methods:rendercontrolsuccess}

This function receives the update from service-end, which would be utilized for rendering the widget.

**Example:**

{% highlight html %}
 
<div id="PivotTreeMap1"></div> 
 
<script>
$('#PivotTreeMap1').ejPivotTreeMap({
      url: "PivotTreeMapService.svc"
  });
var treeMapObj = $("#PivotTreeMap1").data("ejPivotTreeMap");
treeMapObj.renderControlSuccess({"OlapReport": this.getOlapReport(), "JsonRecords": this.getJSONRecords()});
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
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description last">Event parameters from PivotTreeMap
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
<td class="description last">return the current action of PivotTreeMap control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">return the custom object bounds with PivotTreeMap control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">return the outer HTML of PivotTreeMap control.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.PivotTreeMap.Model"/>object</td>
<td class="description last">returns the PivotTreeMap model.</td>
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
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description last">Event parameters from PivotTreeMap
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
<td class="description last">return the current action of PivotTreeMap control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">return the custom object bounds with PivotTreeMap control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">return the outer HTML of PivotTreeMap control.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.PivotTreeMap.Model"/>object</td>
<td class="description last">returns the PivotTreeMap model.</td>
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
 
$("#PivotTreeMap1").ejPivotTreeMap({
   beforeServiceInvoke: function (args) {}
});      

{% endhighlight %}



### drillSuccess
{:#events:drillsuccess}

Triggers when drill up/down happens in PivotTreeMap control. And it returns the outer HTML of PivotTreeMap control.

**Example:**

{% highlight html %}
 
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
<th>Name</th>
<th>Type</th>
<th >Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description last">Event parameters from PivotTreeMap
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
<td class="description last">return the current action of PivotTreeMap control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">return the custom object bounds with PivotTreeMap control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">return the outer HTML of PivotTreeMap control.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.PivotTreeMap.Model"/>object</td>
<td class="description last">returns the PivotTreeMap model.</td>
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
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description last">Event parameters from PivotTreeMap
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
<td class="description last">return the current action of PivotTreeMap control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">return the custom object bounds with PivotTreeMap control.</td>
</tr>
<tr>
<td class="name">message</td>
<td class="type">object</td>
<td class="description last">return the error stack trace of the original exception.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">return the outer HTML of PivotTreeMap control.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.PivotTreeMap.Model"/>object</td>
<td class="description last">returns the PivotTreeMap model.</td>
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
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description last">Event parameters from PivotTreeMap
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
<td class="description last">return the current action of PivotTreeMap control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">return the custom object bounds with PivotTreeMap control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">return the outer HTML of PivotTreeMap control.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.PivotTreeMap.Model"/>object</td>
<td class="description last">returns the PivotTreeMap model.</td>
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
 
$("#PivotTreeMap1").ejPivotTreeMap({
   renderSuccess: function (args) {}
});     

{% endhighlight %}



## Enumeration


### OperationalMode  `enum`
{:#enum:operationalmode}

<ts name = "ej.PivotTreeMap.OperationalMode"/>

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


**Example:**

{% highlight html %}

$("#PivotTreeMap1").ejPivotTreeMap({operationalMode:ej.PivotTreeMap.OperationalMode.ServerMode});

{% endhighlight %}


