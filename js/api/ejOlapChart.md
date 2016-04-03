---
layout: post
title: Properties, Methods and Events of ejOlapChart Widget
documentation: API
platform: js
keywords: ejOlapChart, API, Essential JS OlapChart
metaname: 
metacontent: 
---

# ejOlapChart

The OlapChart is a lightweight control that reads OLAP information and visualizes it in graphical format with the ability to drill up and down.

#### Syntax

{% highlight javascript %}

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

#### Default Value: “”

**Example:**

{% highlight html %}
 
$("#OlapChart1").ejOlapChart({ cssClass : "gradient-lime" });

{% endhighlight %}

### currentReport `string`
{:#members:currentreport}

Contains the serialized OlapReport at that instant, that is, current OlapReport. 

#### Default Value: “”

### customObject `object`
{:#members:customobject}

Object utilized to pass additional information between client-end and service-end.

#### Default Value: {}

**Example:**

{% highlight html %}
 
$("#OlapChart1").ejOlapChart({ customObject: {"key":"Hello World"} });

{% endhighlight %}

### enable3D `boolean`
{:#members:enable3d}

Allows the user to enable 3D view of OlapChart.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#OlapChart1").ejOlapChart({ enable3D: true });

{% endhighlight %}

### isResponsive `boolean`
{:#members:isresponsive}

Allows the user to enable OlapChart’s responsiveness in the browser layout.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#OlapChart1").ejOlapChart({ isResponsive: true });

{% endhighlight %}

### locale `string`
{:#members:locale}

Allows the user to set the localized language for the widget.

#### Default Value: "en-US"

**Example:**

{% highlight html %}
 
$("#OlapChart1").ejOlapChart({ locale: "fr-FR" }); 

{% endhighlight %}

### rotation `number`
{:#members:rotation}

Allows the user to rotate the angle of OlapChart in 3D view.

#### Default Value: 0

**Example:**

{% highlight html %}
 
$("#OlapChart1").ejOlapChart({ rotation: 45 }); 

{% endhighlight %}

### serviceMethodSettings `object`
{:#members:servicemethodsettings}

Allows the user to set custom name for the methods at service-end, communicated on AJAX post.

#### Default Value: {}

**Example:**

{% highlight html %}
 
$("#OlapChart1").ejOlapChart({ serviceMethodSettings: {initialize: "MyMethod1", drillDown: "MyMethod2"} });

{% endhighlight %}

### serviceMethodSettings.exportOlapChart `string`
{:#members:servicemethodsettings-exportolapchart}

Allows the user to set the custom name for the service method that’s responsible for exporting.

#### Default Value: "Export"

**Example:**

{% highlight html %}
 
$("# OlapChart1").ejOlapChart({ serviceMethodSettings: { exportOlapChart: "Export"} });                                  

{% endhighlight %}


### serviceMethodSettings.drillDown `string`
{:#members:servicemethodsettings-drilldown}

Allows the user to set the custom name for the service method that&rsquo;s responsible for drilling up/down operation in OlapChart.

#### Default Value: "DrillChart"

**Example:**

{% highlight html %}
 
$("#OlapChart1").ejOlapChart({ serviceMethodSettings: {drillDown: "DrillChartMyMethod"} });                                       

{% endhighlight %}

### serviceMethodSettings.initialize `string`
{:#members:servicemethodsettings-initialize}

Allows the user to set the custom name for the service method that&rsquo;s responsible for initializing OlapChart.

#### Default Value: "InitializeChart"

**Example:**

{% highlight html %}
 
$("#OlapChart1").ejOlapChart({ serviceMethodSettings: {initialize: "IninlizeChartMyMethod"} });

 {% endhighlight %}

###  url `string`
{:#members:url}

Connects the service using the specified URL for any server updates.

#### Default Value: “”

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
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description last">Event parameters from OlapChart
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
<td class="description last">return the current action of OlapChart control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">return the custom object bounds with OlapChart control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">return the outer HTML of OlapChart control.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.olap.OlapChart.Model"/>object</td>
<td class="description last">returns the OlapChart model.</td>
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
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description last">Event parameters from OlapChart
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
<td class="description last">return the current action of OlapChart control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">return the custom object bounds with OlapChart control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">return the outer HTML of OlapChart control.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.olap.OlapChart.Model"/>object</td>
<td class="description last">returns the OlapChart model.</td>
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
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description last">Event parameters from OlapChart
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
<td class="type"><ts ref="ej.olap.OlapChart.Model"/>object</td>
<td class="description last">returns the OlapChart model.</td>
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
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description last">Event parameters from OlapChart
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
<td class="description last">return the current action of OlapChart control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">return the custom object bounds with OlapChart control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">return the outer HTML of OlapChart control.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.olap.OlapChart.Model"/>object</td>
<td class="description last">returns the OlapChart model.</td>
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
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description last">Event parameters from OlapChart
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
<td class="description last">return the current action of OlapChart control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">return the custom object bounds with OlapChart control.</td>
</tr>
<tr>
<td class="name">message</td>
<td class="type">object</td>
<td class="description last">return the error stack trace of the original exception.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">return the outer HTML of OlapChart control.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.olap.OlapChart.Model"/>object</td>
<td class="description last">returns the OlapChart model.</td>
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
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description last">Event parameters from OlapChart
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
<td class="description last">return the current action of OlapChart control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">return the custom object bounds with OlapChart control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">return the outer HTML of OlapChart control.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.olap.OlapChart.Model"/>object</td>
<td class="description last">returns the OlapChart model.</td>
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
 
$("#OlapChart1").ejOlapChart({
   renderSuccess: function (args) {}
});     

{% endhighlight %}



## Enumeration

### SymbolShapes  `enum`
{:#enum:symbolshapes}

<ts name = "ej.olap.OlapChart.SymbolShapes"/>

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

$("#OlapChart1").ejOlapChart({commonSeriesOptions :{marker :{ shape: ej.olap.OlapChart.SymbolShapes.LeftArrow} }});

{% endhighlight %}


### ChartTypes `enum`
{:#enum:charttypes}

<ts name = "ej.olap.OlapChart.ChartTypes"/>

Allows the user to set the type for OlapChart.

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
            <td class="description">To render a Line type OlapChart.</td>
        </tr>
        <tr>
            <td class="name">Spline</td>
            <td class="description">To render a Spline type OlapChart.</td>
        </tr>
        <tr>
            <td class="name">Column</td>
            <td class="description">To render a Column type OlapChart.</td>
        </tr>
        <tr>
            <td class="name">Area</td>
            <td class="description">To render an Area type OlapChart.</td>
        </tr>
        <tr>
            <td class="name">SplineArea</td>
            <td class="description">To render a SplineArea type OlapChart.</td>
        </tr>
        <tr>
            <td class="name">StepLine</td>
            <td class="description">To render a StepLine type OlapChart.</td>
        </tr>
        <tr>
            <td class="name">StepArea</td>
            <td class="description">To render a StepArea type OlapChart.</td>
        </tr>
        <tr>
            <td class="name">Pie</td>
            <td class="description">To render a Pie type OlapChart.</td>
        </tr>
        <tr>
            <td class="name">Bar</td>
            <td class="description">To render a Bar type OlapChart.</td>
        </tr>
        <tr>
            <td class="name">StackingArea</td>
            <td class="description">To render a StackingArea type OlapChart.</td>
        </tr>
        <tr>
            <td class="name">StackingColumn</td>
            <td class="description">To render a StackingColumn type OlapChart.</td>
        </tr>
        <tr>
            <td class="name">StackingBar</td>
            <td class="description">To render a StackingBar type OlapChart.</td>
        </tr>
        <tr>
            <td class="name">Pyramid</td>
            <td class="description">To render a Pyramid type OlapChart.</td>
        </tr>
        <tr>
            <td class="name">Funnel</td>
            <td class="description">To render a Funnel type OlapChart.</td>
        </tr>
        <tr>
            <td class="name">Doughnut</td>
            <td class="description">To render a Doughnut type OlapChart.</td>
        </tr>
        <tr>
            <td class="name">Scatter</td>
            <td class="description">To render a Scatter type OlapChart.</td>
        </tr>
        <tr>
            <td class="name">Bubble</td>
            <td class="description">To render a Bubble type OlapChart.</td>
        </tr>
    </tbody>
</table>

**Example:**

{% highlight html %}

$("#OlapChart1").ejOlapChart({commonSeriesOptions :{ type: ej.olap.OlapChart.ChartTypes.Column} });

{% endhighlight %}

### ExportOption  `enum`
{:#enum:exportoption }

<ts name = "ej.olap.OlapChart.ExportOptions"/>

Allows the user to export OlapChart to an appropriate format based on the parameter passed.

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
            <td class="description">To export OlapChart in Excel format.</td>
        </tr>
        <tr>
            <td class="name">Word</td>
            <td class="description">To export OlapChart in Word format.</td>
        </tr>
        <tr>
            <td class="name">PDF</td>
            <td class="description">To export OlapChart in PDF format.</td>
        </tr>
        <tr>
            <td class="name">CSV</td>
            <td class="description">To export OlapChart in CSV format.</td>
        </tr>
        <tr>
            <td class="name">PNG</td>
            <td class="description">To export OlapChart in PNG format.</td>
        </tr>
        <tr>
            <td class="name">JPG</td>
            <td class="description">To export OlapChart in JPG format.</td>
        </tr>
        <tr>
            <td class="name">EMF</td>
            <td class="description">To export OlapChart in EMF format.</td>
        </tr>
        <tr>
            <td class="name">GIF</td>
            <td class="description">To export OlapChart in GIF format.</td>
        </tr>
        <tr>
            <td class="name">BMP</td>
            <td class="description">To export OlapChart in BMP format.</td>
        </tr>
    </tbody>
</table>

**Example:**

{% highlight html %}

$("#OlapChart1").ejOlapChart({commonSeriesOptions :{ exportOlapChart: ej.olap.OlapChart.ExportOptions.Excel } });

{% endhighlight %}
