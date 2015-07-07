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

<pre class="prettyprint">
<code> 
&lt;div id="OlapChart"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create OLAP Chart
$("#OlapChart").ejOlapChart(...);       
&lt;/script&gt;</code>
</pre>



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
{:#cssClass}




Specify the CSS class to OLAP Chart to achieve custom theme.


Default Value:
{:.param}



* ""




Example
{:.example}

<pre class="prettyprint">
<code> 
// Set the CSS class during initialization.                     
        $("#OlapChart").ejOlapChart({  cssClass : "gradient-lime" });                   * </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the CSS class after initialization:
        // Gets the CSS class value.            
        $("#OlapChart").ejOlapChart("option", "cssClass");                      
        // Sets the CSS class to OLAP Chart
        $("#OlapChart").ejOlapChart("option", "cssClass",  "gradient-lime" );</code>
</pre>



### currentReport<span class="type-signature type string">String</span>
{:#currentReport}




Contains the serialized OlapReport at the instant.


Default Value:
{:.param}



* ""







### customObject<span class="type-signature type object">object</span>
{:#customObject}




Custom object to pass additional information between client-end and service-end.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
//To set customObject API value during initialization  
        $("#OlapChart").ejOlapChart({  customObject: {"key":"Hello World"}});                                   * </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the customObject API, after initialization:
        //Gets the customObject value  
        $("#OlapChart").ejOlapChart("option", "customObject");
                      
        //Sets the customObject value 
        $("#OlapChart").ejOlapChart("option", "customObject",  {"key":"Hi Syncfusion!"} ); </code>
</pre>



### isResponsive<span class="type-signature type boolean">Boolean</span>
{:#isResponsive}




Allows the user to enable Responsive layout support.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
//To set the isResponsive option during initialization  
$("#OlapChart").ejOlapChart({isResponsive: true});</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the isResponsive, after initialization:
        //Gets the isResponsive values state
        $("#OlapChart").ejOlapChart("option", "isResponsive");
                      
        //Sets the reponsive layout
        $("#OlapChart").ejOlapChart("option", "isResponsive","true");                   *               </code>
</pre>



### locale<span class="type-signature type string">string</span>
{:#locale}




Sets the localized language for the control.


Default Value:
{:.param}



* "en-US"




Example
{:.example}

<pre class="prettyprint">
<code> 
//To set localization API value during initialization  
        $("#OlapChart").ejOlapChart({  locale: "fr-FR"});                                       * </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the localization API, after initialization:
        //Gets the localization value  
        $("#OlapChart").ejOlapChart("option", "locale");
                    
        //Sets the localization value 
        $("#OlapChart").ejOlapChart("option", "locale",  "fr-FR" ); </code>
</pre>



### serviceMethodSettings<span class="type-signature type object">object</span>
{:#serviceMethodSettings}




Allows the user to set custom name for the methods at service-end invoked on AJAX post.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
//To set serviceMethodSettings API value, to invoke the appropriate service method on UI operation.
        $("#OlapChart").ejOlapChart({  serviceMethodSettings: {initialize: "MyMethod", drillDown: "DrillChart"});</code>
</pre>
<pre class="prettyprint">
<code> 
//Gets or sets the serviceMethodSettings API, to invoke the appropriate service method on UI operation:
//Gets the serviceMethodSettings value  
$("#OlapChart").ejOlapChart("option", "serviceMethodSettings");
                     
//Sets the serviceMethodSettings value 
$("#OlapChart").ejOlapChart("option", "serviceMethodSettings",  {initialize: "MyMethod", drillDown: "DrillChart"} ); </code>
</pre>



### serviceMethodSettings.drillDown<span class="type-signature type string">string</span>
{:#serviceMethodSettings-drillDown}




Allows the user to set the custom name for the service method that&rsquo;s responsible for drilling up/down operation in OLAP Chart.


Default Value:
{:.param}



* "DrillChart"




Example
{:.example}

<pre class="prettyprint">
<code> 
//To set drillDown API value, to invoke the corresponding service method for performing server-side operation while drilling up/down in OLAP Chart. 
$("#OlapChart").ejOlapChart({  serviceMethodSettings: {drillDown: "DrillChartMyMethod"});                                       </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the drillDown API, to invoke the corresponding service method for performing server-side operation while drilling up/down in OLAP Chart:
//Gets the drillDown value  
$("#OlapChart").ejOlapChart("option", "serviceMethodSettings");
                     
//Sets the drillDown value 
$("#OlapChart").ejOlapChart("option", "serviceMethodSettings.drillDown", "DrillChartMyMethod"} ); </code>
</pre>



### serviceMethodSettings.initialize<span class="type-signature type string">string</span>
{:#serviceMethodSettings-initialize}




Allows the user to set the custom name for the service method that&rsquo;s responsible for initializing OLAP Chart.


Default Value:
{:.param}



* "InitializeChart"




Example
{:.example}

<pre class="prettyprint">
<code> 
//To set initialize API value, to invoke the corresponding service method for OLAP Chart initialization. 
$("#OlapChart").ejOlapChart({  serviceMethodSettings: {initialize: "IninlizeChartMyMethod"}); </code>
</pre>
<pre class="prettyprint">
<code> 
//Gets or sets the initialize API, to invoke the corresponding service method for OLAP Chart initialization:
//Gets the initialize value  
$("#OlapChart").ejOlapChart("option", "serviceMethodSettings");
                     
//Sets the initialize value 
$("#OlapChart").ejOlapChart("option", "serviceMethodSettings.initialize", "IninlizeChartMyMethod"} ); </code>
</pre>



### url<span class="type-signature type string">string</span>
{:#url}




Connects the service using the specified URL for any server updates.


Default Value:
{:.param}



* ""




Example
{:.example}

<pre class="prettyprint">
<code> 
//To set url API value during initialization  
        $("#OlapChart").ejOlapChart({  url: "/OlapChartService.svc"});                                  * </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the url API, after initialization:
        //Gets the url value  
        $("#OlapChart").ejOlapChart("option", "url");
                       
        //Sets the url value 
        $("#OlapChart").ejOlapChart("option", "url",  "/OlapChartService.svc" ); </code>
</pre>


## Methods




### destroy<span class="signature">()</span>
{:#destroy}




Destroy the OLAP Chart widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="OlapChart"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create OLAP Chart
var chartObj = $("#OlapChart").data("ejOlapChart");
chartObj.destroy(); // destroy the OLAP Chart
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="OlapChart"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// enable the OLAP Chart
$("#OlapChart").ejOlapChart("destroy"); 
&lt;/script&gt;</code>
</pre>



### doAjaxPost<span class="signature">()</span>
{:#doAjaxPost}




Perform an asynchronous HTTP (Ajax) request.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="OlapChart"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>



### renderChartFromJSON<span class="signature">()</span>
{:#renderChartFromJSON}




This function receives the JSON formatted datasource to render the OLAP Chart control.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="OlapChart"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>



### renderControlSuccess<span class="signature">()</span>
{:#renderControlSuccess}




This function receives the controls update from service-end which would be utilized for rendering the widget.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="OlapChart"&gt;&lt;/div&gt; 
 
&lt;script&gt;
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
&lt;/script&gt;</code>
</pre>


## Events




### afterServiceInvoke
{:#afterServiceInvoke}




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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>action</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the current action of OLAP Chart control.</td>
</tr>
<tr>
<td class="name"><code>customObject</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">return the custom object bounds with OLAP Chart control.</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the outer HTML of OLAP Chart control.</td>
</tr>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the OLAP Chart model.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
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

<pre class="prettyprint">
<code> 
//afterServiceInvoke event for OLAP Chart
$("#OlapChart").ejOlapChart({
   afterServiceInvoke: function (args) {}
});      </code>
</pre>



### beforeServiceInvoke
{:#beforeServiceInvoke}




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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>action</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the current action of OLAP Chart control.</td>
</tr>
<tr>
<td class="name"><code>customObject</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">return the custom object bounds with OLAP Chart control.</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the outer HTML of OLAP Chart control.</td>
</tr>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the OLAP Chart model.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
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

<pre class="prettyprint">
<code> 
//beforeServiceInvoke event for OLAP Chart
$("#OlapChart").ejOlapChart({
   beforeServiceInvoke: function (args) {}
});      </code>
</pre>



### drillSuccess
{:#drillSuccess}




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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the OLAP Chart model.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
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

<pre class="prettyprint">
<code> 
//drillSuccess event for OLAP Chart
$("#OlapChart").ejOlapChart({
   drillSuccess: function (args) {}
});      </code>
</pre>



### renderComplete
{:#renderComplete}




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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>action</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the current action of OLAP Chart control.</td>
</tr>
<tr>
<td class="name"><code>customObject</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">return the custom object bounds with OLAP Chart control.</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the outer HTML of OLAP Chart control.</td>
</tr>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the OLAP Chart model.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
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

<pre class="prettyprint">
<code> 
//renderComplete event for OLAP Chart
$("#OlapChart").ejOlapChart({
   renderComplete: function (args) {}
});      </code>
</pre>



### renderFailure
{:#renderFailure}




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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>action</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the current action of OLAP Chart control.</td>
</tr>
<tr>
<td class="name"><code>customObject</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">return the custom object bounds with OLAP Chart control.</td>
</tr>
<tr>
<td class="name"><code>message</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">return the error stacke tace of the original exception.</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the outer HTML of OLAP Chart control.</td>
</tr>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the OLAP Chart model.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
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

<pre class="prettyprint">
<code> 
//renderFailure event for OLAP Chart
$("#OlapChart").ejOlapChart({
   renderFailure: function (args) {}
});      </code>
</pre>



### renderSuccess
{:#renderSuccess}




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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>action</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the current action of OLAP Chart control.</td>
</tr>
<tr>
<td class="name"><code>customObject</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">return the custom object bounds with OLAP Chart control.</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the outer HTML of OLAP Chart control.</td>
</tr>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the OLAP Chart model.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
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

<pre class="prettyprint">
<code> 
//renderSuccess event for OLAP Chart
$("#OlapChart").ejOlapChart({
   renderSuccess: function (args) {}
});      </code>
</pre>


