---
layout: post
title: ejOlapChart
documentation: API
platform: js
keywords: ejOlapChart, API, Essential JS OlapChart
metaname: 
metacontent: 
---

# ejOlapChart

The OlapChart is a lightweight control that reads OLAP information and visualizes it in graphical format with the ability to drill up and down.

#### Syntax

{% highlight js %}

$(element).ejOlapChart()

{% endhighlight %}


#### Example

{% highlight html %}
 
<div id="OlapChart1"></div>

<script>
    //Create OlapChart
    $("#OlapChart1").ejOlapChart(...);
</script>

{% endhighlight %}

#### Requires

* module:jquery-1.10.2.min.js
* module:jquery.easing.1.3.min.js
* module:jquery.globalize.min.js
* module:ej.core.js
* module:ej.data.js
* module:ej.touch.js
* module:ej.dialog.js
* module:ej.draggable.js
* module:ej.waitingpopup.js
* module:ej.chart.js
* module:ej.olapchart.js


## Members


### cssClass `string`
{:#members:cssclass}

Specifies the CSS class to OlapChart to achieve custom theme.

**Default Value:** “”

**Example:**

{% highlight html %}
 
$("#OlapChart1").ejOlapChart({ cssClass : "gradient-lime" });

{% endhighlight %}

### currentReport `string`
{:#members:currentreport}

Contains the serialized OlapReport at that instant, that is, current OlapReport. 

**Default Value:** “”

### customObject `object`
{:#members:customobject}

Object utilized to pass additional information between client-end and service-end.

**Default Value:** {}

**Example:**

{% highlight html %}
 
$("#OlapChart1").ejOlapChart({ customObject: {"key":"Hello World"} });

{% endhighlight %}

### enable3D `boolean`
{:#members:enable3d}

Allows the user to enable 3D view of OlapChart.

**Default Value:** false

**Example:**

{% highlight html %}
 
$("#OlapChart1").ejOlapChart({ enable3D: true });

{% endhighlight %}

### isResponsive `boolean`
{:#members:isresponsive}

Allows the user to enable OlapChart’s responsiveness in the browser layout.

**Default Value:** false

**Example:**

{% highlight html %}
 
$("#OlapChart1").ejOlapChart({ isResponsive: true });

{% endhighlight %}

### locale `string`
{:#members:locale}

Allows the user to set the localized language for the widget.

**Default Value:** "en-US"

**Example:**

{% highlight html %}
 
$("#OlapChart1").ejOlapChart({ locale: "fr-FR" }); 

{% endhighlight %}

### rotation `number`
{:#members:rotation}

Allows the user to rotate the angle of OlapChart in 3D view.

**Default Value:** 0

**Example:**

{% highlight html %}
 
$("#OlapChart1").ejOlapChart({ rotation: 45 }); 

{% endhighlight %}

### serviceMethodSettings `object`
{:#members:servicemethodsettings}

Allows the user to set custom name for the methods at service-end, communicated on AJAX post.

**Default Value:** {}

**Example:**

{% highlight html %}
 
$("#OlapChart1").ejOlapChart({ serviceMethodSettings: {initialize: "MyMethod1", drillDown: "MyMethod2"} });

{% endhighlight %}

### serviceMethodSettings.exportOlapChart `string`
{:#members:servicemethodsettings-exportolapchart}

Allows the user to set the custom name for the service method that’s responsible for exporting.

**Default Value:** "Export"

**Example:**

{% highlight html %}
 
$("# OlapChart1").ejOlapChart({ serviceMethodSettings: { exportOlapChart: "Export"} });                                  

{% endhighlight %}


### serviceMethodSettings.drillDown `string`
{:#members:servicemethodsettings-drilldown}

Allows the user to set the custom name for the service method that&rsquo;s responsible for drilling up/down operation in OlapChart.

**Default Value:** "DrillChart"

**Example:**

{% highlight html %}
 
$("#OlapChart1").ejOlapChart({ serviceMethodSettings: {drillDown: "DrillChartMyMethod"} });                                       

{% endhighlight %}

###  serviceMethodSettings.initialize `string`
{:#members:servicemethodsettings-initialize}

Allows the user to set the custom name for the service method that&rsquo;s responsible for initializing OlapChart.

**Default Value:** "InitializeChart"

**Example:**

{% highlight html %}
 
$("#OlapChart1").ejOlapChart({ serviceMethodSettings: {initialize: "IninlizeChartMyMethod"} });

 {% endhighlight %}

###  url `string`
{:#members:url}

Connects the service using the specified URL for any server updates.

**Default Value:** “”

**Example:**

{% highlight html %}
 
$("#OlapChart1").ejOlapChart({ url: "/OlapChartService.svc" });

{% endhighlight %}


## Methods

### doAjaxPost()
{:#methods:doajaxpost}

Perform an asynchronous HTTP (AJAX) request.


**Example:**

{% highlight html %}
 
<div id="OlapChart1"></div> 
 
<script>
$('#OlapChart1').ejOlapChart({
      url: "OlapChartService.svc",
                animation: true, type: ej.olap.OlapChart.ChartTypes.Column, 
                       commonSeriesOptions: { type: ej.olap.OlapChart.ChartTypes.Column, tooltip: { visible: true} },
                       size: { height: 460, width: 950 }, primaryXAxis: { title: { text: "Fiscal Year" }, labelRotation: 0 },
                       primaryYAxis: { title: { text: "Customer Count"} }, legend: { visible: true, rowCount: 2 },
                       load: "loadTheme"
 });
var chartObj = $("#OlapChart1").data("ejOlapChart");
chartObj.doAjaxPost("POST", "/OlapChartService.svc/Initialize", {"key", "Hello World"}, "renderControlSuccess", null);
</script>

{% endhighlight %}



### doPostBack()
{:#methods:dopostback}

Perform an asynchronous HTTP (FullPost) submit.

**Example:**

{% highlight html %}

<div id="OlapChart1"></div> 
 
<script>
$('#OlapChart1).ejOlapChart({
      url: "OlapChartService.svc",
 });
var chartObj = $("#OlapChart1").data("ejOlapChart");
chartObj.doPostBack("/OlapChartService.svc/Initialize", {"key", "Hello World"});
</script> 

{% endhighlight %}


### exportOlapChart()
{:#methods:exportolapchart}

Exports the OlapChart to an appropriate format based on the parameter passed.
  
**Example:**

{% highlight html %}
 
<div id="OlapChart1"></div> 
 
<script>
var chartObj = $("#OlapChart1").data("ejOlapChart");
chartObj.exportOlapChart(ej.olap.OlapChart.ExportOptions.Excel);
</script>

{% endhighlight %}



### renderChartFromJSON()
{:#methods:renderchartfromjson}

This function receives the JSON formatted datasource to render the OlapChart control.


**Example:**

{% highlight html %}
 
<div id="OlapChart1"></div> 
 
<script>
$('#OlapChart1').ejOlapChart({
      url: "OlapChartService.svc",
                animation: true, type: ej.olap.OlapChart.ChartTypes.Column, 
                       commonSeriesOptions: { type: ej.olap.OlapChart.ChartTypes.Column, tooltip: { visible: true} },
                       size: { height: 460, width: 950 }, primaryXAxis: { title: { text: "Fiscal Year" }, labelRotation: 0 },
                       primaryYAxis: { title: { text: "Customer Count"} }, legend: { visible: true, rowCount: 2 },
                       load: "loadTheme"
 });
var chartObj = $("#OlapChart1").data("ejOlapChart");
chartObj.renderControlFromJSON(this.getJSONRecords());
</script>

{% endhighlight %}

### renderControlSuccess()
{:#methods:rendercontrolsuccess}

This function receives the update from service-end, which would be utilized for rendering the widget.

**Example:**

{% highlight html %}
 
<div id="OlapChart1"></div> 
 
<script>
$('#OlapChart1').ejOlapChart({
      url: "OlapChartService.svc",
                animation: true, type: ej.olap.OlapChart.ChartTypes.Column, 
                       commonSeriesOptions: { type: ej.olap.OlapChart.ChartTypes.Column, tooltip: { visible: true} },
                       size: { height: 460, width: 950 }, primaryXAxis: { title: { text: "Fiscal Year" }, labelRotation: 0 },
                       primaryYAxis: { title: { text: "Customer Count"} }, legend: { visible: true, rowCount: 2 },
                       load: "loadTheme"
  });
var chartObj = $("#OlapChart1").data("ejOlapChart");
chartObj.renderControlSuccess({"OlapReport": this.getOlapReport(), "JsonRecords": this.getJSONRecords()});
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
<td class="description">Event parameters from OlapChart
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
<td class="description">return the current action of OlapChart control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">return the custom object bounds with OlapChart control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">return the outer HTML of OlapChart control.</td>
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
<td class="description">returns the OlapChart model.</td>
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
 
$("#OlapChart1").ejOlapChart({
   afterServiceInvoke: function (args) {}
});

{% endhighlight %}


### beforeServiceInvoke
{:#events:beforeserviceinvoke}

Triggers before any AJAX request is passed from OlapChart to service methods.

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
<td class="description">Event parameters from OlapChart
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
<td class="description">return the current action of OlapChart control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">return the custom object bounds with OlapChart control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">return the outer HTML of OlapChart control.</td>
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
<td class="description">returns the OlapChart model.</td>
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
 
$("#OlapChart1").ejOlapChart({
   beforeServiceInvoke: function (args) {}
});      

{% endhighlight %}



### drillSuccess
{:#events:drillsuccess}

Triggers when drill up/down happens in OlapChart control.

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
<td class="description">Event parameters from OlapChart
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
<td class="type">object</span></td>
<td class="description">returns the OlapChart model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type">string</span></td>
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
 
$("#OlapChart1").ejOlapChart({
   drillSuccess: function (args) {}
});

{% endhighlight %}




### renderComplete
{:#events:rendercomplete}

Triggers when OlapChart widget completes all operations at client-side after any AJAX request.

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type">Object</td>
<td class="description">Event parameters from OlapChart
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
<td class="description">return the current action of OlapChart control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">return the custom object bounds with OlapChart control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">return the outer HTML of OlapChart control.</td>
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
<td class="description">returns the OlapChart model.</td>
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
 
$("#OlapChart1").ejOlapChart({
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
<td class="description">Event parameters from OlapChart
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
<td class="description">return the current action of OlapChart control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">return the custom object bounds with OlapChart control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
message{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">return the error stacke tace of the original exception.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">return the outer HTML of OlapChart control.</td>
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
<td class="description">returns the OlapChart model.</td>
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
 
$("#OlapChart1").ejOlapChart({
   renderFailure: function (args) {}
});      

{% endhighlight %}


### renderSuccess
{:#events:rendersuccess}

Triggers when OlapChart successfully reaches client-side after any AJAX request.

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
<td class="description">Event parameters from OlapChart
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
<td class="description">return the current action of OlapChart control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">return the custom object bounds with OlapChart control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">return the outer HTML of OlapChart control.</td>
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
<td class="description">returns the OlapChart model.</td>
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
 
$("#OlapChart1").ejOlapChart({
   renderSuccess: function (args) {}
});     

{% endhighlight %}



## Enumeration

### SymbolShapes  `enum`
{:#enum:symbolshapes}

Allows the user to set shape for the marker.

**Example:**

{% highlight html %}

$("#OlapChart1").ejOlapChart({commonSeriesOptions :{marker :{ shape: ej.olap.OlapChart.SymbolShapes.LeftArrow} }});

{% endhighlight %}


### ChartTypes `enum`
{:#enum:charttypes}

Allows the user to set the type for OlapChart.

**Example:**

{% highlight html %}

$("#OlapChart1").ejOlapChart({commonSeriesOptions :{ type: ej.olap.OlapChart.ChartTypes.Column} });

{% endhighlight %}

### ExportOption  `enum`
{:#enum:exportoption }

Allows the user to export OlapChart to an appropriate format based on the parameter passed.

**Example:**

{% highlight html %}

$("#OlapChart1").ejOlapChart({commonSeriesOptions :{ exportOlapChart: ej.olap.OlapChart.ExportOptions.Excel } });

{% endhighlight %}
