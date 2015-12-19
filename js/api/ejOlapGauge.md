---
layout: post
title: ejOlapGauge
documentation: API
platform: js
keywords: ejOlapGauge, API, Essential JS OlapGauge
metaname: 
metacontent: 
---

# OlapGauge

Custom Design for Html OLAP Gauge control.

#### Syntax

{% highlight js %}

$(element).ejOlapGauge()

{% endhighlight %}


#### Example

{% highlight html %}
 
<div id="OlapGauge"></div> 
 
<script>
// Create OLAP Gauge
$("#OlapGauge").ejOlapGauge(...);       
</script>

{% endhighlight %}


#### Requires

* module:jquery-1.10.2.min.js
* module:jquery.easing.1.3.min.js
* module:jquery.globalize.min.js
* module:ej.core.js
* module:ej.data.js
* module:ej.waitingpopup.js
* module:ej.circulargauge.js
* module:ej.olapgauge.js



## Members


### columnsCount `number`
{:#members:columnscount}

Sets the number of colunsCount in OLAP Gauges for its arrangement.


#### Default Value

* 0

#### Example

{% highlight html %}
 
//To set columnsCount API value during initialization  
$("#OlapGauge").ejOlapGauge({  columnsCount: 1}); 

{% endhighlight %}


{% highlight html %}
 
//Get or set the columnsCount API, after initialization:
//Gets the columnsCount value  
$("#OlapGauge").ejOlapGauge("option", "columnsCount");
                      
//Sets the columnsCount value 
$("#OlapGauge").ejOlapGauge("option", "columnsCount", 2 ); 

{% endhighlight %}




### cssClass `string`
{:#members:cssclass}

Specify the CSS class to OLAP Gauge to achieve custom theme.


#### Default Value

* ""


#### Example

{% highlight html %}
 
// Set the CSS class during initialization.                     
$("#OlapGauge").ejOlapGauge({  cssClass : "gradient-lime" });

 {% endhighlight %}


{% highlight html %}
 
//Get or set the CSS class after initialization:
// Gets the CSS class value.            
$("#OlapGauge").ejOlapGauge("option", "cssClass");                      
// Sets the CSS class to OLAP Gauge
$("#OlapGauge").ejOlapGauge("option", "cssClass",  "gradient-lime" );

{% endhighlight %}



### customObject `object`
{:#members:customobject}

Custom object to pass additional information between client-end and service-end.


#### Default Value

* null


#### Example

{% highlight html %}
 
//To set customObject API value during initialization  
$("#OlapGauge").ejOlapGauge({  customObject: {"key":"Hello World"}}); 

{% endhighlight %}


{% highlight html %}
 
//Get or set the customObject API, after initialization:
//Gets the customObject value  
$("#OlapGauge").ejOlapGauge("option", "customObject");
                      
//Sets the customObject value 
$("#OlapGauge").ejOlapGauge("option", "customObject",  {"key":"Hi Syncfusion!"} ); 

{% endhighlight %}



### enableTooltip `boolean`
{:#members:enabletooltip}

Enables/disables tooltip in OLAP Gauge.


#### Default Value

* false


#### Example

{% highlight html %}
 
//To set enableTooltip API value during initialization  
$("#OlapGauge").ejOlapGauge({  enableTooltip: true}); 

{% endhighlight %}


{% highlight html %}
 
//Get or set the enableTooltip API, after initialization:
//Gets the enableTooltip value  
$("#OlapGauge").ejOlapGauge("option", "enableTooltip");
                     
//Sets the enableTooltip value 
$("#OlapGauge").ejOlapGauge("option", "enableTooltip", false ); 

{% endhighlight %}



### isResponsive `boolean`
{:#members:isresponsive}

Allows the user to enable Responsive layout support.


#### Default Value

* false


#### Example

{% highlight html %}
 
//To set the isResponsive option during initialization  
$("#OlapGauge").ejOlapGauge({isResponsive: true});

{% endhighlight %}


{% highlight html %}
 
//Get or set the isResponsive, after initialization:
//Gets the isResponsive values state
$("#OlapGauge").ejOlapGauge("option", "isResponsive");
                      
//Sets the reponsive layout
$("#OlapGauge").ejOlapGauge("option", "isResponsive","true");

{% endhighlight %}



### labelFormatSettings `enum`
{:#members:labelformatsettings}

Number format allows you to change the format of label values in OLAP Gauge.


#### Default Value

* Default


#### Example

{% highlight html %}
 
//To set numberFormat API value during initialization  
$("#OlapGauge").ejOlapGauge({  numberFormat: ej.olap.OlapGauge.numberFormat.Default});

 {% endhighlight %}


{% highlight html %}
 
//Get or set the numberFormat API, after initialization:
//Gets the showHeaderLabel value  
$("#OlapGauge").ejOlapGauge("option", "numberFormat");
                      
//Sets the numberFormat value 
$("#OlapGauge").ejOlapGauge("option", "numberFormat", ej.olap.OlapGauge.numberFormat.Default); 

{% endhighlight %}




### locale `string`
{:#members:locale}

Sets the localized language for the control.


#### Default Value

* "en-US"



#### Example

{% highlight html %}
 
//To set localization API value during initialization  
$("#OlapGauge").ejOlapGauge({  locale: "fr-FR"}); 

{% endhighlight %}


{% highlight html %}
 
//Get or set the localization API, after initialization:
//Gets the localization value  
$("#OlapGauge").ejOlapGauge("option", "locale");
                    
//Sets the localization value 
$("#OlapGauge").ejOlapGauge("option", "locale",  "fr-FR" );

 {% endhighlight %}



### rowsCount `number`
{:#members:rowscount}

Sets the number of rows in OLAP Gauges for its arrangement.


#### Default Value

* 0


#### Example

{% highlight html %}
 
//To set rowsCount API value during initialization  
$("#OlapGauge").ejOlapGauge({  rowsCount: 1});

 {% endhighlight %}


{% highlight html %}
 
//Get or set the rowsCOunt API, after initialization:
//Gets the rowsCount value  
$("#OlapGauge").ejOlapGauge("option", "rowsCount");
                 
//Sets the rowsCount value 
$("#OlapGauge").ejOlapGauge("option", "rowsCount", 2); 

{% endhighlight %}



### scales `object`
{:#members:scales}

Sets the scale values such as pointers, indicators, etc... for OLAP Gauge.


#### Default Value

* null


#### Example

{% highlight html %}
 
//To set scales API value during initialization  
$("#OlapGauge").ejOlapGauge({  scales: {showRanges: true, showIndicators: true}});

 {% endhighlight %}


{% highlight html %}
 
//Get or set the scales API, after initialization:
//Gets the scales value  
$("#OlapGauge").ejOlapGauge("option", "scales");
                    
//Sets the scales value 
$("#OlapGauge").ejOlapGauge("option", "scales", {showRanges: true, showIndicators: true});

{% endhighlight %}



### serviceMethodSettings `object`
{:#members:servicemethodsettings}

Allows the user to set custom name for the methods at service-end invoked on AJAX post.



#### Default Value

* null


#### Example

{% highlight html %}
 
//To set serviceMethodSettings API value, to invoke the appropriate service method on UI operation.  
$("#OlapGauge").ejOlapGauge({  serviceMethodSettings: {initialize: "MyMethod"});

{% endhighlight %}


{% highlight html %}
 
//Gets or sets the serviceMethodSettings API, to invoke the appropriate service method on UI operation:
//Gets the serviceMethodSettings value  
$("#OlapGauge").ejOlapGauge("option", "serviceMethodSettings");
                     
//Sets the serviceMethodSettings value 
$("#OlapGauge").ejOlapGauge("option", "serviceMethodSettings",  {initialize: "MyMethod"} ); 

{% endhighlight %}


### serviceMethodSettings.initialize `string`
{:#members:servicemethodsettings-initialize}

Allows the user to set the custom name for the service method that&rsquo;s responsible for initializing OLAP Guage.


#### Default Value

* "InitializeGuage"


#### Example

{% highlight html %}
 
//To set initialize API value, to invoke the corresponding service method for OLAP Gauge initialization.
 $("#OlapGauge").ejOlapGauge({  serviceMethodSettings: {initialize: "InitializeGuageMyMethod"});
 
{% endhighlight %}


{% highlight html %}
 
//Gets or sets the initialize API, to invoke the corresponding service method for OLAP Gauge initialization:
//Gets the initialize value  
$("#OlapGauge").ejOlapGauge("option", "serviceMethodSettings");
   
//Sets the initialize value 
$("#OlapGauge").ejOlapGauge("option", "serviceMethodSettings.initialize", "InitializeGuageMyMethod" ); 

{% endhighlight %}


### showHeaderLabel `boolean`
{:#members:showheaderlabel}

Enables/disables the header labels in OLAP Gauge.


#### Default Value

* true


#### Example

{% highlight html %}
 
//To set showHeaderLabel API value during initialization  
$("#OlapGauge").ejOlapGauge({  showHeaderLabel: false}); 

{% endhighlight %}


{% highlight html %}
 
//Get or set the showHeaderLabel API, after initialization:
//Gets the showHeaderLabel value  
$("#OlapGauge").ejOlapGauge("option", "showHeaderLabel");
                   
//Sets the showHeaderLabel value 
$("#OlapGauge").ejOlapGauge("option", "showHeaderLabel", true); 

{% endhighlight %}




### url `string`
{:#members:url}

Connects the service using the specified URL for any server updates.


#### Default Value

* ""

#### Example

{% highlight html %}
 
//To set url API value during initialization  
$("#OlapGauge").ejOlapGauge({  url: "/OlapGaugeService.svc"}); 

{% endhighlight %}


{% highlight html %}
 
//Get or set the url API, after initialization:
//Gets the url value  
$("#OlapGauge").ejOlapGauge("option", "url");
                       
//Sets the url value 
$("#OlapGauge").ejOlapGauge("option", "url",  "/OlapGaugeService" ); 

{% endhighlight %}



## Methods

### destroy()
{:#methods:destroy}

Destroy the OLAP Gauge widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.

#### Example

{% highlight html %}
 
<div id="OlapGauge1"></div> 
 
<script>
// Create OLAP Gauge
var gaugeObj = $("#OlapGauge").data("ejOlapGauge");
gaugeObj.destroy(); // destroy the OLAP Gauge
</script>

{% endhighlight %}


{% highlight html %}
 
<div id="OlapGauge"></div> 
 
<script>
// enable the OLAP Gauge
$("#OlapGauge").ejOlapGauge("destroy"); 
</script>

{% endhighlight %}



### doAjaxPost()
{:#methods:doajaxpost}

Perform an asynchronous HTTP (Ajax) request.


#### Example

{% highlight html %}
 
<div id="OlapGauge"></div> 
 
<script>
// Create OLAP Gauge
$('#OlapGauge').ejOlapGauge({
      url: "OlapGaugeService.svc",
                enableTooltip: true,
                scales: [{
                pointers: [{
                           showBackNeedle: true,
                           backNeedleLength: 20,
                           length: 120,
                           width: 7
                       },
               {
                   type: "marker",
                   markerType: "diamond",
                   distanceFromScale: 5,
                   placement: "center",
                   backgroundColor: "#29A4D9",
                   length: 25,
                   width: 15
               }]
        }]
  });
var gaugeObj = $("#OlapGauge").data("ejOlapGauge");
gaugeObj.doAjaxPost("POST", "/OlapGaugeService.svc/Initialize", {"key", "Hello World"}, "renderControlSuccess", null);
// initiate an Ajax request
</script>

{% endhighlight %}




### progressStatus()
{:#methods:progressstatus}

This function receives JSON data and prepares for rendering the widget after service request.


#### Example

{% highlight html %}
 
<div id="OlapGauge"></div> 
 
<script>
// Create OLAP Gauge
$('#OlapGauge').ejOlapGauge({url: "OlapGaugeService.svc"});
      
var gaugeObj = $("#OlapGauge").data("ejOlapGauge");
gaugeObj.progressStatus({"OlapReport": this.getOlapReport(), "JsonRecords": this.getJSONRecords()});
// creating OLAP Gauge after Ajax request
</script>

{% endhighlight %}


### refresh()
{:#methods:refresh}

This function is used to refresh the OLAP Gauge at client side.

#### Example

{% highlight html %}
 
<div id="OlapGauge"></div> 
 
<script>
// Create OLAP Gauge
$('#OlapGauge').ejOlapGauge({
      url: "OlapGaugeService.svc",
                enableTooltip: true,
                scales: [{
                pointers: [{
                           showBackNeedle: true,
                           backNeedleLength: 20,
                           length: 120,
                           width: 7
                       },
               {
                   pointerType: "marker",
                   markerType: "diamond",
                   distanceFromScale: 5,
                   placement: "center",
                   backgroundColor: "#29A4D9",
                   length: 25,
                   width: 15
               }]
        }]
  });
var gaugeObj = $("#OlapGauge").data("ejOlapGauge");
gaugeObj.refresh();
// refresh the OLAP Gauge in client-side.
</script>

{% endhighlight %}


### removeImg()
{:#methods:removeimg}

This function removes the KPI image tags in OLAP Gauge control.


#### Example

{% highlight html %}
 
<div id="OlapGauge"></div> 
 
<script>
// Create OLAP Gauge
$('#OlapGauge').ejOlapGauge({
      url: "OlapGaugeService.svc",
                enableTooltip: true,
                scales: [{
                pointers: [{
                           showBackNeedle: true,
                           backNeedleLength: 20,
                           length: 120,
                           width: 7
                       },
               {
                   type: "marker",
                   markerType: "diamond",
                   distanceFromScale: 5,
                   placement: "center",
                   backgroundColor: "#29A4D9",
                   length: 25,
                   width: 15
               }]
        }]
  });
var gaugeObj = $("#OlapGauge").data("ejOlapGauge");
gaugeObj.removeImg();
// removes HTML image tags inside of OLAP Gauge.
</script>

{% endhighlight %}


### renderControlFromJSON()
{:#methods:rendercontrolfromjson}

This function receives the JSON formatted datasource to render the OLAP Gauge control.

#### Example

{% highlight html %}
 
<div id="OlapGauge"></div> 
 
<script>
// Create OLAP Gauge
$('#OlapGauge').ejOlapGauge({
      url: "OlapGaugeService.svc",
                enableTooltip: true,
                scales: [{
                pointers: [{
                           showBackNeedle: true,
                           backNeedleLength: 20,
                           length: 120,
                           width: 7
                       },
               {
                   type: "marker",
                   markerType: "diamond",
                   distanceFromScale: 5,
                   placement: "center",
                   backgroundColor: "#29A4D9",
                   length: 25,
                   width: 15
               }]
        }]
  });
var gaugeObj = $("#OlapGauge").data("ejOlapGauge");
gaugeObj.renderControlFromJSON(this.getJSONRecords());
// render the OLAP Gauge from JSON formatted data.
</script>

{% endhighlight %}



## Events

### afterServiceInvoke
{:#events:afterserviceinvoke}

Fires when it reaches client script after any Ajax request.

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
<td class="description">Event parameters from OLAP Gauge.
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
<td class="description">return the current action of OLAP Gauge control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">return the custom object bounds with OLAP Gauge control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">return the outer HTML of OLAP Gauge control.</td>
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
<td class="description">returns the OLAP Gauge model.</td>
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


#### Example

{% highlight html %}
 
//afterServiceInvoke event for OLAP Gauge
$("#OlapGauge").ejOlapGauge({
   afterServiceInvoke: function (args) {}
});      

{% endhighlight %}


### beforeServiceInvoke
{:#events:beforeserviceinvoke}

Fires before any Ajax request passed from OLAP Gauge to service methods.

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
<td class="description">Event parameters from OLAP Gauge.
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
<td class="description">return the current action of OLAP Gauge control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">return the custom object bounds with OLAP Gauge control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">return the outer HTML of OLAP Gauge control.</td>
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
<td class="description">returns the OLAP Gauge model.</td>
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


#### Example

{% highlight html %}
 
//beforeServiceInvoke event for OLAP Gauge
$("#OlapGauge").ejOlapGauge({
   beforeServiceInvoke: function (args) {}
});      

{% endhighlight %}


### load
{:#events:load}

Fires when gauge started loading at client-side.

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
<td class="description">Event parameters from OLAP Gauge.
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
<td class="type">object</td>
<td class="description">returns the OLAP Gauge model.</td>
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


#### Example

{% highlight html %}
 
//load event for OLAP Gauge
$("#OlapGauge").ejOlapGauge({
   load: function (args) {}
});      

{% endhighlight %}

### renderComplete
{:#events:rendercomplete}

Fires when OLAP Gauge control completes all operations at client script after any Ajax request.

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
<td class="description">Event parameters from OLAP Gauge.
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
element{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the outer HTML of OLAP Gauge control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type">Object</td>
<td class="description">returns the custom object bounded with the control.</td>
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
<td class="description">returns the OLAP Gauge model.</td>
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


#### Example

{% highlight html %}
 
//renderCompleteevent for OLAP Gauge
$("#OlapGauge").ejOlapGauge({
   renderComplete: function (args) {}
});      

{% endhighlight %}



### renderFailure
{:#events:renderfailure}

Fires when error occurs during Ajax request.

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
<td class="description">Event parameters from OLAP Gauge.
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
element{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the outer HTML of OLAP Gauge control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type">Object</td>
<td class="description">returns the custom object bounded with the control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
message{% endhighlight %}</td>
<td class="type">Object</td>
<td class="description">returns the error message with error code.</td>
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
<td class="description">returns the OLAP Gauge model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
responseJSON{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">returns the JSON formatted response while error occurs.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
//renderFailure event for OLAP Gauge
$("#OlapGauge").ejOlapGauge({
   renderFailure: function (args) {}
}); 

{% endhighlight %}


### renderSuccess
{:#events:rendersuccess}

Fires when OLAP Gauge control successfully reaches client script after any Ajax request.

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
<td class="description">Event parameters from OLAP Gauge.
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
element{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the outer HTML of OLAP Gauge control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type">Object</td>
<td class="description">returns the custom object bounded with the control.</td>
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
<td class="description">returns the OLAP Gauge model.</td>
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


#### Example

{% highlight html %}
 
//renderSuccess event for OLAP Gauge.
$("#OlapGauge").ejOlapGauge({
   renderSuccess: function (args) {}
});      

{% endhighlight %}



