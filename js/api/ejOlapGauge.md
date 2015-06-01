---
layout: post
title: ejOlapGauge
documentation: API
platform: js
metaname: 
metacontent: 
---

Custom Design for Html OLAP Gauge control.





#### $(element).ejOlapGauge<span class="signature">()</span>






##### Example
<pre class="prettyprint"><code> &lt;div id="OlapGauge"&gt;&lt;/div&gt; 
 &lt;script&gt;// Create OLAP Gauge$("#OlapGauge").ejOlapGauge(...);       &lt;/script&gt;</code></pre>



### Requires


* module:jquery-1.10.2.min.js

* module:jquery.easing.1.3.min.js

* module:jquery.globalize.min.js

* module:ej.core.js

* module:ej.data.js

* module:ej.waitingpopup.js

* module:ej.circulargauge.js

* module:ej.olapgauge.js


### Members




#### columnsCount<span class="type-signature type number">number</span>




Sets the number of colunsCount in OLAP Gauges for its arrangement.


Default Value:



* 0




##### Examples
<pre class="prettyprint"><code> //To set columnsCount API value during initialization          $("#OlapGauge").ejOlapGauge({  columnsCount: 1});                                       * </code></pre><pre class="prettyprint"><code> //Get or set the columnsCount API, after initialization:
        //Gets the columnsCount value          $("#OlapGauge").ejOlapGauge("option", "columnsCount");
                              //Sets the columnsCount value         $("#OlapGauge").ejOlapGauge("option", "columnsCount", 2 ); </code></pre>



#### cssClass<span class="type-signature type string">string</span>




Specify the CSS class to OLAP Gauge to achieve custom theme.


Default Value:



* ""




##### Examples
<pre class="prettyprint"><code> // Set the CSS class during initialization.                             $("#OlapGauge").ejOlapGauge({  cssClass : "gradient-lime" });                   * </code></pre><pre class="prettyprint"><code> //Get or set the CSS class after initialization:
        // Gets the CSS class value.                    $("#OlapGauge").ejOlapGauge("option", "cssClass");                              // Sets the CSS class to OLAP Gauge        $("#OlapGauge").ejOlapGauge("option", "cssClass",  "gradient-lime" );</code></pre>



#### customObject<span class="type-signature type object">object</span>




Custom object to pass additional information between client-end and service-end.


Default Value:



* null




##### Examples
<pre class="prettyprint"><code> //To set customObject API value during initialization          $("#OlapGauge").ejOlapGauge({  customObject: {"key":"Hello World"}});                                   * </code></pre><pre class="prettyprint"><code> //Get or set the customObject API, after initialization:
        //Gets the customObject value          $("#OlapGauge").ejOlapGauge("option", "customObject");
                              //Sets the customObject value         $("#OlapGauge").ejOlapGauge("option", "customObject",  {"key":"Hi Syncfusion!"} ); </code></pre>



#### enableTooltip<span class="type-signature type boolean">boolean</span>




Enables/disables tooltip in OLAP Gauge.


Default Value:



* false




##### Examples
<pre class="prettyprint"><code> //To set enableTooltip API value during initialization          $("#OlapGauge").ejOlapGauge({  enableTooltip: true});                                   * </code></pre><pre class="prettyprint"><code> //Get or set the enableTooltip API, after initialization:
        //Gets the enableTooltip value          $("#OlapGauge").ejOlapGauge("option", "enableTooltip");
                             //Sets the enableTooltip value         $("#OlapGauge").ejOlapGauge("option", "enableTooltip", false ); </code></pre>



#### isResponsive<span class="type-signature type boolean">Boolean</span>




Allows the user to enable Responsive layout support.


Default Value:



* false




##### Examples
<pre class="prettyprint"><code> //To set the isResponsive option during initialization  $("#OlapGauge").ejOlapGauge({isResponsive: true});</code></pre><pre class="prettyprint"><code> //Get or set the isResponsive, after initialization:
        //Gets the isResponsive values state        $("#OlapGauge").ejOlapGauge("option", "isResponsive");
                              //Sets the reponsive layout        $("#OlapGauge").ejOlapGauge("option", "isResponsive","true");                   *               </code></pre>



#### labelFormatSettings<span class="type-signature type enum">enum</span>




Number format allows you to change the format of label values in OLAP Gauge.


Default Value:



* Default




##### Examples
<pre class="prettyprint"><code> //To set numberFormat API value during initialization  $("#OlapGauge").ejOlapGauge({  numberFormat: ej.olap.OlapGauge.numberFormat.Default});                                  * </code></pre><pre class="prettyprint"><code> //Get or set the numberFormat API, after initialization:
        //Gets the showHeaderLabel value          $("#OlapGauge").ejOlapGauge("option", "numberFormat");
                              //Sets the numberFormat value         $("#OlapGauge").ejOlapGauge("option", "numberFormat", ej.olap.OlapGauge.numberFormat.Default); </code></pre>



#### locale<span class="type-signature type string">string</span>




Sets the localized language for the control.


Default Value:



* "en-US"




##### Examples
<pre class="prettyprint"><code> //To set localization API value during initialization          $("#OlapGauge").ejOlapGauge({  locale: "fr-FR"});                                       * </code></pre><pre class="prettyprint"><code> //Get or set the localization API, after initialization:
        //Gets the localization value          $("#OlapGauge").ejOlapGauge("option", "locale");
                            //Sets the localization value         $("#OlapGauge").ejOlapGauge("option", "locale",  "fr-FR" ); </code></pre>



#### rowsCount<span class="type-signature type number">number</span>




Sets the number of rows in OLAP Gauges for its arrangement.


Default Value:



* 0




##### Examples
<pre class="prettyprint"><code> //To set rowsCount API value during initialization          $("#OlapGauge").ejOlapGauge({  rowsCount: 1});                                  * </code></pre><pre class="prettyprint"><code> //Get or set the rowsCOunt API, after initialization:
        //Gets the rowsCount value          $("#OlapGauge").ejOlapGauge("option", "rowsCount");
                         //Sets the rowsCount value         $("#OlapGauge").ejOlapGauge("option", "rowsCount", 2); </code></pre>



#### scales<span class="type-signature type object">object</span>




Sets the scale values such as pointers, indicators, etc... for OLAP Gauge.


Default Value:



* null




##### Examples
<pre class="prettyprint"><code> //To set scales API value during initialization          $("#OlapGauge").ejOlapGauge({  scales: {showRanges: true, showIndicators: true}});                                      * </code></pre><pre class="prettyprint"><code> //Get or set the scales API, after initialization:
        //Gets the scales value          $("#OlapGauge").ejOlapGauge("option", "scales");
                            //Sets the scales value         $("#OlapGauge").ejOlapGauge("option", "scales", {showRanges: true, showIndicators: true}); </code></pre>



#### serviceMethodSettings<span class="type-signature type object">object</span>




Allows the user to set custom name for the methods at service-end invoked on AJAX post.


Default Value:



* null




##### Examples
<pre class="prettyprint"><code> /To set serviceMethodSettings API value, to invoke the appropriate service method on UI operation.  $("#OlapGauge").ejOlapGauge({  serviceMethodSettings: {initialize: "MyMethod"});</code></pre><pre class="prettyprint"><code> //Gets or sets the serviceMethodSettings API, to invoke the appropriate service method on UI operation:
//Gets the serviceMethodSettings value  $("#OlapGauge").ejOlapGauge("option", "serviceMethodSettings");
                     //Sets the serviceMethodSettings value $("#OlapGauge").ejOlapGauge("option", "serviceMethodSettings",  {initialize: "MyMethod"} ); </code></pre>



#### serviceMethodSettings.initialize<span class="type-signature type string">string</span>




Allows the user to set the custom name for the service method that&rsquo;s responsible for initializing OLAP Guage.


Default Value:



* "InitializeGuage"




##### Examples
<pre class="prettyprint"><code> //To set initialize API value, to invoke the corresponding service method for OLAP Gauge initialization. $("#OlapGauge").ejOlapGauge({  serviceMethodSettings: {initialize: "InitializeGuageMyMethod"});</code></pre><pre class="prettyprint"><code> //Gets or sets the initialize API, to invoke the corresponding service method for OLAP Gauge initialization:
//Gets the initialize value  $("#OlapGauge").ejOlapGauge("option", "serviceMethodSettings");
   //Sets the initialize value $("#OlapGauge").ejOlapGauge("option", "serviceMethodSettings.initialize", "InitializeGuageMyMethod" ); </code></pre>



#### showHeaderLabel<span class="type-signature type boolean">boolean</span>




Enables/disables the header labels in OLAP Gauge.


Default Value:



* true




##### Examples
<pre class="prettyprint"><code> //To set showHeaderLabel API value during initialization          $("#OlapGauge").ejOlapGauge({  showHeaderLabel: false});                                        * </code></pre><pre class="prettyprint"><code> //Get or set the showHeaderLabel API, after initialization:
        //Gets the showHeaderLabel value          $("#OlapGauge").ejOlapGauge("option", "showHeaderLabel");
                           //Sets the showHeaderLabel value         $("#OlapGauge").ejOlapGauge("option", "showHeaderLabel", true); </code></pre>



#### url<span class="type-signature type string">string</span>




Connects the service using the specified URL for any server updates.


Default Value:



* ""




##### Examples
<pre class="prettyprint"><code> //To set url API value during initialization          $("#OlapGauge").ejOlapGauge({  url: "/OlapGaugeService.svc"});                                  * </code></pre><pre class="prettyprint"><code> //Get or set the url API, after initialization:
        //Gets the url value          $("#OlapGauge").ejOlapGauge("option", "url");
                               //Sets the url value         $("#OlapGauge").ejOlapGauge("option", "url",  "/OlapGaugeService" ); </code></pre>


### Methods




#### destroy<span class="signature">()</span>




Destroy the OLAP Gauge widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.



##### Examples
<pre class="prettyprint"><code> &lt;div id="OlapGauge1"&gt;&lt;/div&gt; 
 &lt;script&gt;// Create OLAP Gaugevar gaugeObj = $("#OlapGauge").data("ejOlapGauge");gaugeObj.destroy(); // destroy the OLAP Gauge&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="OlapGauge"&gt;&lt;/div&gt; 
 &lt;script&gt;// enable the OLAP Gauge$("#OlapGauge").ejOlapGauge("destroy"); &lt;/script&gt;</code></pre>



#### doAjaxPost<span class="signature">()</span>




Perform an asynchronous HTTP (Ajax) request.



##### Example
<pre class="prettyprint"><code> &lt;div id="OlapGauge"&gt;&lt;/div&gt; 
 &lt;script&gt;// Create OLAP Gauge$('#OlapGauge').ejOlapGauge({      url: "OlapGaugeService.svc",                enableTooltip: true,                scales: [{                pointers: [{                           showBackNeedle: true,                           backNeedleLength: 20,                           length: 120,                           width: 7                       },               {                   type: "marker",                   markerType: "diamond",                   distanceFromScale: 5,                   placement: "center",                   backgroundColor: "#29A4D9",                   length: 25,                   width: 15               }]                                }]  });var gaugeObj = $("#OlapGauge").data("ejOlapGauge");gaugeObj.doAjaxPost("POST", "/OlapGaugeService.svc/Initialize", {"key", "Hello World"}, "renderControlSuccess", null);// initiate an Ajax request&lt;/script&gt;</code></pre>



#### progressStatus<span class="signature">()</span>




This function receives JSON data and prepares for rendering the widget after service request.



##### Example
<pre class="prettyprint"><code> &lt;div id="OlapGauge"&gt;&lt;/div&gt; 
 &lt;script&gt;// Create OLAP Gauge$('#OlapGauge').ejOlapGauge({      url: "OlapGaugeService.svc",                enableTooltip: true,                scales: [{                pointers: [{                           showBackNeedle: true,                           backNeedleLength: 20,                           length: 120,                           width: 7                       },               {                   type: "marker",                   markerType: "diamond",                   distanceFromScale: 5,                   placement: "center",                   backgroundColor: "#29A4D9",                   length: 25,                   width: 15               }]                                }]  });var gaugeObj = $("#OlapGauge").data("ejOlapGauge");gaugeObj.progressStatus({"OlapReport": this.getOlapReport(), "JsonRecords": this.getJSONRecords()});// creating OLAP Gauge after Ajax request&lt;/script&gt;</code></pre>



#### refresh<span class="signature">()</span>




This function is used to refresh the OLAP Gauge at client side.



##### Example
<pre class="prettyprint"><code> &lt;div id="OlapGauge"&gt;&lt;/div&gt; 
 &lt;script&gt;// Create OLAP Gauge$('#OlapGauge').ejOlapGauge({      url: "OlapGaugeService.svc",                enableTooltip: true,                scales: [{                pointers: [{                           showBackNeedle: true,                           backNeedleLength: 20,                           length: 120,                           width: 7                       },               {                   pointerType: "marker",                   markerType: "diamond",                   distanceFromScale: 5,                   placement: "center",                   backgroundColor: "#29A4D9",                   length: 25,                   width: 15               }]                                }]  });var gaugeObj = $("#OlapGauge").data("ejOlapGauge");gaugeObj.refresh();// refresh the OLAP Gauge in client-side.&lt;/script&gt;</code></pre>



#### removeImg<span class="signature">()</span>




This function removes the KPI image tags in OLAP Gauge control.



##### Example
<pre class="prettyprint"><code> &lt;div id="OlapGauge"&gt;&lt;/div&gt; 
 &lt;script&gt;// Create OLAP Gauge$('#OlapGauge').ejOlapGauge({      url: "OlapGaugeService.svc",                enableTooltip: true,                scales: [{                pointers: [{                           showBackNeedle: true,                           backNeedleLength: 20,                           length: 120,                           width: 7                       },               {                   type: "marker",                   markerType: "diamond",                   distanceFromScale: 5,                   placement: "center",                   backgroundColor: "#29A4D9",                   length: 25,                   width: 15               }]                                }]  });var gaugeObj = $("#OlapGauge").data("ejOlapGauge");gaugeObj.removeImg();// removes HTML image tags inside of OLAP Gauge.&lt;/script&gt;</code></pre>



#### renderControlFromJSON<span class="signature">()</span>




This function receives the JSON formatted datasource to render the OLAP Gauge control.



##### Example
<pre class="prettyprint"><code> &lt;div id="OlapGauge"&gt;&lt;/div&gt; 
 &lt;script&gt;// Create OLAP Gauge$('#OlapGauge').ejOlapGauge({      url: "OlapGaugeService.svc",                enableTooltip: true,                scales: [{                pointers: [{                           showBackNeedle: true,                           backNeedleLength: 20,                           length: 120,                           width: 7                       },               {                   type: "marker",                   markerType: "diamond",                   distanceFromScale: 5,                   placement: "center",                   backgroundColor: "#29A4D9",                   length: 25,                   width: 15               }]                                }]  });var gaugeObj = $("#OlapGauge").data("ejOlapGauge");gaugeObj.renderControlFromJSON(this.getJSONRecords());// render the OLAP Gauge from JSON formatted data.&lt;/script&gt;</code></pre>


### Events




#### afterServiceInvoke




Fires when it reaches client script after any Ajax request.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from OLAP Gauge.<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>action</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">return the current action of OLAP Gauge control.</td></tr><tr><td class="name"><code>customObject</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">return the custom object bounds with OLAP Gauge control.</td></tr><tr><td class="name"><code>element</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">return the outer HTML of OLAP Gauge control.</td></tr><tr><td class="name"><code>cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">if the event should be canceled; otherwise, false.</td></tr><tr><td class="name"><code>model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the OLAP Gauge model.</td></tr><tr><td class="name"><code>type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event.</td></tr></tbody></table></td></tr></tbody></table>


##### Example
<pre class="prettyprint"><code> //afterServiceInvoke event for OLAP Gauge$("#OlapGauge").ejOlapGauge({   afterServiceInvoke: function (args) {}});      </code></pre>



#### beforeServiceInvoke




Fires before any Ajax request passed from OLAP Gauge to service methods.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from OLAP Gauge.<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>action</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">return the current action of OLAP Gauge control.</td></tr><tr><td class="name"><code>customObject</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">return the custom object bounds with OLAP Gauge control.</td></tr><tr><td class="name"><code>element</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">return the outer HTML of OLAP Gauge control.</td></tr><tr><td class="name"><code>cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">if the event should be canceled; otherwise, false.</td></tr><tr><td class="name"><code>model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the OLAP Gauge model.</td></tr><tr><td class="name"><code>type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event.</td></tr></tbody></table></td></tr></tbody></table>


##### Example
<pre class="prettyprint"><code> //beforeServiceInvoke event for OLAP Gauge$("#OlapGauge").ejOlapGauge({   beforeServiceInvoke: function (args) {}});      </code></pre>



#### load




Fires when gauge started loading at client-side.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from OLAP Gauge.<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">if the event should be canceled; otherwise, false.</td></tr><tr><td class="name"><code>model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the OLAP Gauge model.</td></tr><tr><td class="name"><code>type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event.</td></tr></tbody></table></td></tr></tbody></table>


##### Example
<pre class="prettyprint"><code> //load event for OLAP Gauge$("#OlapGauge").ejOlapGauge({   load: function (args) {}});      </code></pre>



#### renderComplete




Fires when OLAP Gauge control completes all operations at client script after any Ajax request.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from OLAP Gauge.<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>element</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the outer HTML of OLAP Gauge control.</td></tr><tr><td class="name"><code>customObject</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">returns the custom object bounded with the control.</td></tr><tr><td class="name"><code>cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">if the event should be canceled; otherwise, false.</td></tr><tr><td class="name"><code>model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the OLAP Gauge model.</td></tr><tr><td class="name"><code>type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event.</td></tr></tbody></table></td></tr></tbody></table>


##### Example
<pre class="prettyprint"><code> //renderCompleteevent for OLAP Gauge$("#OlapGauge").ejOlapGauge({   renderComplete: function (args) {}});      </code></pre>



#### renderFailure




Fires when error occurs during Ajax request.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from OLAP Gauge.<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>element</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the outer HTML of OLAP Gauge control.</td></tr><tr><td class="name"><code>customObject</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">returns the custom object bounded with the control.</td></tr><tr><td class="name"><code>message</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">returns the error message with error code.</td></tr><tr><td class="name"><code>cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">if the event should be canceled; otherwise, false.</td></tr><tr><td class="name"><code>model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the OLAP Gauge model.</td></tr><tr><td class="name"><code>type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event.</td></tr><tr><td class="name"><code>responseJSON</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the JSON formatted response while error occurs.</td></tr></tbody></table></td></tr></tbody></table>


##### Example
<pre class="prettyprint"><code> //renderFailure event for OLAP Gauge$("#OlapGauge").ejOlapGauge({   renderFailure: function (args) {}});      </code></pre>



#### renderSuccess




Fires when OLAP Gauge control successfully reaches client script after any Ajax request.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from OLAP Gauge.<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>element</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the outer HTML of OLAP Gauge control.</td></tr><tr><td class="name"><code>customObject</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">returns the custom object bounded with the control.</td></tr><tr><td class="name"><code>cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">if the event should be canceled; otherwise, false.</td></tr><tr><td class="name"><code>model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the OLAP Gauge model.</td></tr><tr><td class="name"><code>type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event.</td></tr></tbody></table></td></tr></tbody></table>


##### Example
<pre class="prettyprint"><code> //renderSuccess event for OLAP Gauge.$("#OlapGauge").ejOlapGauge({   renderSuccess: function (args) {}});      </code></pre>


