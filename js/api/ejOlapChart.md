---
layout: post
title: ejOlapChart
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html OLAP Chart control.





$(element).ejOlapChart<span class="signature">()</span>






Example
{:.example}


{% highlight html %}
 
<div id="OlapChart"></div> 
 
<script>
// Create OLAP Chart
$("#OlapChart").ejOlapChart(...);       
</script>{% endhighlight %}




Requires
{:.require}


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




### cssClass<span class="type-signature type string">string</span>
{:#members:cssclass}




Specify the CSS class to OLAP Chart to achieve custom theme.


Default Value:
{:.param}



* ""




Example
{:.example}


{% highlight html %}
 
// Set the CSS class during initialization.                     
$("#OlapChart").ejOlapChart({  cssClass : "gradient-lime" });{% endhighlight %}


{% highlight html %}
 
//Get or set the CSS class after initialization:
// Gets the CSS class value.            
$("#OlapChart").ejOlapChart("option", "cssClass");                      
// Sets the CSS class to OLAP Chart
$("#OlapChart").ejOlapChart("option", "cssClass",  "gradient-lime" );{% endhighlight %}




### currentReport<span class="type-signature type string">String</span>
{:#members:currentreport}




Contains the serialized OlapReport at the instant.


Default Value:
{:.param}



* ""







### customObject<span class="type-signature type object">object</span>
{:#members:customobject}




Custom object to pass additional information between client-end and service-end.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
//To set customObject API value during initialization  
$("#OlapChart").ejOlapChart({  customObject: {"key":"Hello World"}});{% endhighlight %}


{% highlight html %}
 
//Get or set the customObject API, after initialization:
//Gets the customObject value  
$("#OlapChart").ejOlapChart("option", "customObject");
                      
//Sets the customObject value 
$("#OlapChart").ejOlapChart("option", "customObject",  {"key":"Hi Syncfusion!"} ); {% endhighlight %}




### isResponsive<span class="type-signature type boolean">Boolean</span>
{:#members:isresponsive}




Allows the user to enable Responsive layout support.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
//To set the isResponsive option during initialization  
$("#OlapChart").ejOlapChart({isResponsive: true});{% endhighlight %}


{% highlight html %}
 
//Get or set the isResponsive, after initialization:
//Gets the isResponsive values state
$("#OlapChart").ejOlapChart("option", "isResponsive");
                      
//Sets the reponsive layout
$("#OlapChart").ejOlapChart("option", "isResponsive","true"); {% endhighlight %}




### locale<span class="type-signature type string">string</span>
{:#members:locale}




Sets the localized language for the control.


Default Value:
{:.param}



* "en-US"




Example
{:.example}


{% highlight html %}
 
//To set localization API value during initialization  
$("#OlapChart").ejOlapChart({  locale: "fr-FR"}); {% endhighlight %}


{% highlight html %}
 
//Get or set the localization API, after initialization:
//Gets the localization value  
$("#OlapChart").ejOlapChart("option", "locale");
                    
//Sets the localization value 
$("#OlapChart").ejOlapChart("option", "locale",  "fr-FR" ); {% endhighlight %}




### serviceMethodSettings<span class="type-signature type object">object</span>
{:#members:servicemethodsettings}




Allows the user to set custom name for the methods at service-end invoked on AJAX post.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
//To set serviceMethodSettings API value, to invoke the appropriate service method on UI operation.
$("#OlapChart").ejOlapChart({  serviceMethodSettings: {initialize: "MyMethod", drillDown: "DrillChart"});{% endhighlight %}


{% highlight html %}
 
//Gets or sets the serviceMethodSettings API, to invoke the appropriate service method on UI operation:
//Gets the serviceMethodSettings value  
$("#OlapChart").ejOlapChart("option", "serviceMethodSettings");
                     
//Sets the serviceMethodSettings value 
$("#OlapChart").ejOlapChart("option", "serviceMethodSettings",  {initialize: "MyMethod", drillDown: "DrillChart"} ); {% endhighlight %}




### serviceMethodSettings.drillDown<span class="type-signature type string">string</span>
{:#members:servicemethodsettings-drilldown}




Allows the user to set the custom name for the service method that&rsquo;s responsible for drilling up/down operation in OLAP Chart.


Default Value:
{:.param}



* "DrillChart"




Example
{:.example}


{% highlight html %}
 
//To set drillDown API value, to invoke the corresponding service method for performing server-side operation while drilling up/down in OLAP Chart. 
$("#OlapChart").ejOlapChart({  serviceMethodSettings: {drillDown: "DrillChartMyMethod"});                                       {% endhighlight %}


{% highlight html %}
 
//Get or set the drillDown API, to invoke the corresponding service method for performing server-side operation while drilling up/down in OLAP Chart:
//Gets the drillDown value  
$("#OlapChart").ejOlapChart("option", "serviceMethodSettings");
                     
//Sets the drillDown value 
$("#OlapChart").ejOlapChart("option", "serviceMethodSettings.drillDown", "DrillChartMyMethod"} ); {% endhighlight %}




### serviceMethodSettings.initialize<span class="type-signature type string">string</span>
{:#members:servicemethodsettings-initialize}




Allows the user to set the custom name for the service method that&rsquo;s responsible for initializing OLAP Chart.


Default Value:
{:.param}



* "InitializeChart"




Example
{:.example}


{% highlight html %}
 
//To set initialize API value, to invoke the corresponding service method for OLAP Chart initialization. 
$("#OlapChart").ejOlapChart({  serviceMethodSettings: {initialize: "IninlizeChartMyMethod"}); {% endhighlight %}


{% highlight html %}
 
//Gets or sets the initialize API, to invoke the corresponding service method for OLAP Chart initialization:
//Gets the initialize value  
$("#OlapChart").ejOlapChart("option", "serviceMethodSettings");
                     
//Sets the initialize value 
$("#OlapChart").ejOlapChart("option", "serviceMethodSettings.initialize", "IninlizeChartMyMethod"} ); {% endhighlight %}




### url<span class="type-signature type string">string</span>
{:#members:url}




Connects the service using the specified URL for any server updates.


Default Value:
{:.param}



* ""




Example
{:.example}


{% highlight html %}
 
//To set url API value during initialization  
$("#OlapChart").ejOlapChart({  url: "/OlapChartService.svc"});{% endhighlight %}


{% highlight html %}
 
//Get or set the url API, after initialization:
//Gets the url value  
$("#OlapChart").ejOlapChart("option", "url");
                       
//Sets the url value 
$("#OlapChart").ejOlapChart("option", "url",  "/OlapChartService.svc" ); {% endhighlight %}



## Methods




### destroy<span class="signature">()</span>
{:#methods:destroy}




Destroy the OLAP Chart widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.



Example
{:.example}


{% highlight html %}
 
<div id="OlapChart"></div> 
 
<script>
// Create OLAP Chart
var chartObj = $("#OlapChart").data("ejOlapChart");
chartObj.destroy(); // destroy the OLAP Chart
</script>{% endhighlight %}


{% highlight html %}
 
<div id="OlapChart"></div> 
 
<script>
// enable the OLAP Chart
$("#OlapChart").ejOlapChart("destroy"); 
</script>{% endhighlight %}




### doAjaxPost<span class="signature">()</span>
{:#methods:doajaxpost}




Perform an asynchronous HTTP (Ajax) request.



Example
{:.example}


{% highlight html %}
 
<div id="OlapChart"></div> 
 
<script>
// Create OLAP Chart
$('#OlapChart').ejOlapChart({
      url: "OlapChartService.svc",
                animation: true, type: ej.olap.OlapChart.ChartTypes.Column, 
                       commonSeriesOptions: { type: ej.olap.OlapChart.ChartTypes.Column, tooltip: { visible: true} },
                       size: { height: 460, width: 950 }, primaryXAxis: { title: { text: "Fiscal Year" }, labelRotation: 0 },
                       primaryYAxis: { title: { text: "Customer Count"} }, legend: { visible: true, rowCount: 2 },
                       load: "loadTheme"
  });
var chartObj = $("#OlapChart").data("ejOlapChart");
chartObj.doAjaxPost("POST", "/OlapChartService.svc/Initialize", {"key", "Hello World"}, "renderControlSuccess", null);
// initiate an Ajax request
</script>{% endhighlight %}




### renderChartFromJSON<span class="signature">()</span>
{:#methods:renderchartfromjson}




This function receives the JSON formatted datasource to render the OLAP Chart control.



Example
{:.example}


{% highlight html %}
 
<div id="OlapChart"></div> 
 
<script>
// Create OLAP Chart
$('#OlapChart').ejOlapChart({
      url: "OlapChartService.svc",
                animation: true, type: ej.olap.OlapChart.ChartTypes.Column, 
                       commonSeriesOptions: { type: ej.olap.OlapChart.ChartTypes.Column, tooltip: { visible: true} },
                       size: { height: 460, width: 950 }, primaryXAxis: { title: { text: "Fiscal Year" }, labelRotation: 0 },
                       primaryYAxis: { title: { text: "Customer Count"} }, legend: { visible: true, rowCount: 2 },
                       load: "loadTheme"
  });
var chartObj = $("#OlapChart").data("ejOlapChart");
chartObj.renderControlFromJSON(this.getJSONRecords());
// render the OLAP Chart from JSON formatted data.
</script>{% endhighlight %}




### renderControlSuccess<span class="signature">()</span>
{:#methods:rendercontrolsuccess}




This function receives the controls update from service-end which would be utilized for rendering the widget.



Example
{:.example}


{% highlight html %}
 
<div id="OlapChart"></div> 
 
<script>
// Create OLAP Chart
$('#OlapChart').ejOlapChart({
      url: "OlapChartService.svc",
                animation: true, type: ej.olap.OlapChart.ChartTypes.Column, 
                       commonSeriesOptions: { type: ej.olap.OlapChart.ChartTypes.Column, tooltip: { visible: true} },
                       size: { height: 460, width: 950 }, primaryXAxis: { title: { text: "Fiscal Year" }, labelRotation: 0 },
                       primaryYAxis: { title: { text: "Customer Count"} }, legend: { visible: true, rowCount: 2 },
                       load: "loadTheme"
  });
var chartObj = $("#OlapChart").data("ejOlapChart");
chartObj.renderControlSuccess({"OlapReport": this.getOlapReport(), "JsonRecords": this.getJSONRecords()});
// creating OLAP Chart after Ajax request
</script>{% endhighlight %}



## Events




### afterServiceInvoke
{:#events:afterserviceinvoke}




Fires when it reaches client script after any Ajax request.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from OLAP Chart
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
action{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the current action of OLAP Chart control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">return the custom object bounds with OLAP Chart control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the outer HTML of OLAP Chart control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the OLAP Chart model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
//afterServiceInvoke event for OLAP Chart
$("#OlapChart").ejOlapChart({
   afterServiceInvoke: function (args) {}
});      {% endhighlight %}




### beforeServiceInvoke
{:#events:beforeserviceinvoke}




Fires before any Ajax request passed from OLAP Chart to service methods.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from OLAP Chart
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
action{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the current action of OLAP Chart control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">return the custom object bounds with OLAP Chart control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the outer HTML of OLAP Chart control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the OLAP Chart model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
//beforeServiceInvoke event for OLAP Chart
$("#OlapChart").ejOlapChart({
   beforeServiceInvoke: function (args) {}
});      {% endhighlight %}




### drillSuccess
{:#events:drillsuccess}




Fires when drilldown happens in OLAP Chart control.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from OLAP Chart
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the OLAP Chart model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
//drillSuccess event for OLAP Chart
$("#OlapChart").ejOlapChart({
   drillSuccess: function (args) {}
});{% endhighlight %}




### renderComplete
{:#events:rendercomplete}




Fires when OLAP Chart completely finishes its rendering.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from OLAP Chart
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
action{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the current action of OLAP Chart control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">return the custom object bounds with OLAP Chart control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the outer HTML of OLAP Chart control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the OLAP Chart model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
//renderComplete event for OLAP Chart
$("#OlapChart").ejOlapChart({
   renderComplete: function (args) {}
});      {% endhighlight %}




### renderFailure
{:#events:renderfailure}




Fires while any discrepancies occurs during the rendering time.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from OLAP Chart
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
action{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the current action of OLAP Chart control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">return the custom object bounds with OLAP Chart control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
message{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">return the error stacke tace of the original exception.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the outer HTML of OLAP Chart control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the OLAP Chart model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
//renderFailure event for OLAP Chart
$("#OlapChart").ejOlapChart({
   renderFailure: function (args) {}
});      {% endhighlight %}




### renderSuccess
{:#events:rendersuccess}




Fires when OLAP Chart successfully finished its rendering.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from OLAP Chart
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
action{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the current action of OLAP Chart control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">return the custom object bounds with OLAP Chart control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the outer HTML of OLAP Chart control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the OLAP Chart model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
//renderSuccess event for OLAP Chart
$("#OlapChart").ejOlapChart({
   renderSuccess: function (args) {}
});      {% endhighlight %}



