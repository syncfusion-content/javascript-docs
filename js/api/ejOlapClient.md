---
layout: post
title: ejOlapClient
documentation: API
platform: js
metaname: 
metacontent: 
---

Custom Design for Html OLAP Client control.










#### $(element).ejOlapClient<span class="signature">()</span>











##### Example

<pre class="prettyprint">
<code> 
&lt;div id="OlapClient"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create OLAP Client
$("#OlapClient").ejOlapClient(...);     
&lt;/script&gt;</code>
</pre>






### Requires




* module:jquery-1.10.2.min.js


* module:jquery.easing.1.3.min.js


* module:jquery.globalize.min.js


* module:ej.core.js


* module:ej.data.js


* module:ej.touch.js


* module:ej.button.js


* module:ej.togglebutton.js


* module:ej.checkbox.js


* module:ej.radiobutton.js


* module:ej.dropdownlist.js


* module:ej.dialog.js


* module:ej.draggable.js


* module:ej.toolbar.js


* module:ej.scroller.js


* module:ej.maskedit.js


* module:ej.waitingpopup.js


* module:ej.treeview.js


* module:ej.tab.js


* module:ej.chart.js


* module:ej.olapchart.js


* module:ej.pivotgrid.js


* module:ej.olapclient.js




### Members








#### chartType<span class="type-signature type enum">enum</span>








Sets the type for OLAP Chart component inside OLAP Client.




Default Value:






* ej.olap.OlapChart.ChartTypes.Column








##### Examples

<pre class="prettyprint">
<code> 
//To set chartType API value during initialization
$("#OlapClient").ejOlapClient({ chartType: ej.olap.OlapChart.ChartTypes.Spline });</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the chartType API, after initialization:
//Gets the chartType value  
$("#OlapClient").ejOlapClient("option","chartType");
                        
//Sets the chartType value 
$("#OlapClient").ejOlapClient("option","chartType", ej.olap.OlapChart.ChartTypes.Area); </code>
</pre>






#### cssClass<span class="type-signature type string">string</span>








Sets the CSS name for custom operation.




Default Value:






* null








##### Examples

<pre class="prettyprint">
<code> 
//To set cssClass API value during initialization
$("#OlapClient").ejOlapClient({ cssClass: "Olive" });</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the cssClass API, after initialization:
//Gets the cssClass value  
$("#OlapClient").ejOlapClient("option","cssClass");
                 
//Sets the cssClass value 
$("#OlapClient").ejOlapClient("option","cssClass", "Olive" ); </code>
</pre>






#### customObject<span class="type-signature type object">Object</span>








Custom object to pass additional information between client-end and service-end.




Default Value:






* null








##### Examples

<pre class="prettyprint">
<code> 
//To set customObject API value during initialization
$("#OlapClient").ejOlapClient({ customObject: {"MyObject": "Hi Syncfusion!!"} });</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the customObject API, after initialization:
//Gets the customObject value  
$("#OlapClient").ejOlapClient("option","customObject");
                     
//Sets the customObject value 
$("#OlapClient").ejOlapClient("option","customObject", {"MyObject": "Hello World!!"} ); </code>
</pre>






#### displaySettings<span class="type-signature type object">object</span>








Allows the user to customize the control layout and appearance.




Default Value:






* null








##### Examples

<pre class="prettyprint">
<code> 
//To set displaySettings API value, in-order to customize the control layout and appearance.
 $("#OlapClient").ejOlapClient({  displaySettings: {mode: "chartandgrid"}});</code>
</pre>
<pre class="prettyprint">
<code> 
//Gets or sets the displaySettings API, to customize the control layout and appearance:
//Gets the displaySettings value  
$("#OlapClient").ejOlapClient("option", "displaySettings");
   
//Sets the displaySettings value 
$("#OlapClient").ejOlapClient("option", "displaySettings", {mode: "chartandgrid"} ); </code>
</pre>






#### displaySettings.controlPlacement<span class="type-signature type enum">enum</span>








Lets the user to customize the display of OLAP Chart and PivotGrid controls inside the OLAP Client component.




Default Value:






* ej.olap.OlapClient.ControlPlacement.Tab








##### Examples

<pre class="prettyprint">
<code> 
//To set controlPlacement API value during initialization
$("#OlapClient").ejOlapClient({ displaySettings: {controlPlacement: ej.olap.OlapClient.ControlPlacement.Tab} });</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the controlPlacement API, after initialization:
//Gets the controlPlacement value  
$("#OlapClient").ejOlapClient("option","displaySettings.controlPlacement");
                 
//Sets the controlPlacement value 
$("#OlapClient").ejOlapClient("option","displaySettings.controlPlacement", ej.olap.OlapClient.ControlPlacement.Tile ); </code>
</pre>






#### displaySettings.defaultView<span class="type-signature type enum">enum</span>








Lets the user to set Chart or Grid tab as default.




Default Value:






* ej.olap.OlapClient.DefaultView.Grid








##### Examples

<pre class="prettyprint">
<code> 
//To set defaultView API value during initialization
$("#OlapClient").ejOlapClient({ displaySettings: {defaultView: ej.olap.OlapClient.DefaultView.Grid} });</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the defaultView API, after initialization:
//Gets the defaultView value  
$("#OlapClient").ejOlapClient("option","displaySettings.defaultView");
                      
//Sets the defaultView value 
$("#OlapClient").ejOlapClient("option","displaySettings.defaultView", ej.olap.OlapClient.DefaultView.Chart ); </code>
</pre>






#### displaySettings.enableFullScreen<span class="type-signature type boolean">boolean</span>








Enables/ disables the full screen view of the OLAP components(OLAP Chart, PivotGrid) in OLAP Client.




Default Value:






* false








##### Examples

<pre class="prettyprint">
<code> 
//To set enableFullScreen API value during initialization
$("#OlapClient").ejOlapClient({ displaySettings.enableFullScreen: true });</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the enableFullScreen API, after initialization:
//Gets the enableFullScreen value  
$("#OlapClient").ejOlapClient("option","displaySettings.enableFullScreen");
                 
//Sets the enableFullScreen value 
$("#OlapClient").ejOlapClient("option","displaySettings.enableFullScreen", true ); </code>
</pre>






#### displaySettings.enableTogglePanel<span class="type-signature type boolean">boolean</span>








Sets the Toggle Panel visibility mode.




Default Value:






* false








##### Examples

<pre class="prettyprint">
<code> 
//To set enableTogglePanel API value during initialization
$("#OlapClient").ejOlapClient({ displaySettings.enableTogglePanel: true });</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the enableTogglePanel API, after initialization:
//Gets the enableTogglePanel value  
$("#OlapClient").ejOlapClient("option","displaySettings.enableTogglePanel");
                        
//Sets the enableTogglePanel value 
$("#OlapClient").ejOlapClient("option","displaySettings.enableTogglePanel", true ); </code>
</pre>






#### displaySettings.mode<span class="type-signature type enum">enum</span>








Sets the display mode (Only Chart/Only Grid/Both Chart And Grid) of OLAP Client.




Default Value:






* ej.olap.OlapClient.DisplayMode.ChartAndGrid








##### Examples

<pre class="prettyprint">
<code> 
//To set mode API value during initialization
$("#OlapClient").ejOlapClient({ displaySettings: { mode: ej.olap.OlapClient.DisplayMode.ChartOnly }});</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the mode API, after initialization:
//Gets the mode value  
$("#OlapClient").ejOlapClient("option","displaySettings.mode");
                     
//Sets the mode value 
$("#OlapClient").ejOlapClient("option","displaySettings.mode", ej.olap.OlapClient.DisplayMode.ChartOnly ); </code>
</pre>






#### enableMeasureGroups<span class="type-signature type boolean">boolean</span>








Enables/ disables the visibility of measure group selector drop down in Cube browser in OLAP Client.




Default Value:






* false








##### Examples

<pre class="prettyprint">
<code> 
//To set enableMeasureGroups API value during initialization
$("#OlapClient").ejOlapClient({ enableMeasureGroups : true });</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the enableMeasureGroups API, after initialization:
//Gets the enableMeasureGroups value  
$("#OlapClient").ejOlapClient("option","enableMeasureGroups");
                      
//Sets the enableMeasureGroups value 
$("#OlapClient").ejOlapClient("option","enableMeasureGroups", true ); </code>
</pre>






#### gridLayout<span class="type-signature type enum">enum</span>








Sets the layout for PivotGrid component inside OLAP Client.




Default Value:






* ej.PivotGrid.Layout.Normal








##### Examples

<pre class="prettyprint">
<code> 
//To set gridLayout API value during initialization
$("#OlapClient").ejOlapClient({ gridLayout: ej.PivotGrid.Layout.NoSummaries });</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the gridLayout API, after initialization:
//Gets the gridLayout value  
$("#OlapClient").ejOlapClient("option","gridLayout");
                       
//Sets the gridLayout value 
$("#OlapClient").ejOlapClient("option","gridLayout", ej.PivotGrid.Layout.NormalTopSummary); </code>
</pre>






#### isResponsive<span class="type-signature type boolean">Boolean</span>








Allows the user to enable Responsive layout support.




Default Value:






* false








##### Examples

<pre class="prettyprint">
<code> 
//To set the isResponsive option during initialization  
$("#OlapClient1").ejOlapClient({isResponsive: true});</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the isResponsive, after initialization:
//Gets the isResponsive values state
$("#OlapClient").ejOlapClient("option", "isResponsive");
                    
//Sets the reponsive layout
$("#OlapClient").ejOlapClient("option", "isResponsive","true");                                </code>
</pre>






#### locale<span class="type-signature type string">string</span>








Sets the localized language for the control.




Default Value:






* "en-US"








##### Examples

<pre class="prettyprint">
<code> 
//To set locale API value during initialization
$("#OlapClient").ejOlapClient({ locale: "en-US" });</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the locale API, after initialization:
//Gets the locale value  
$("#OlapClient").ejOlapClient("option","locale");
                   
//Sets the locale value 
$("#OlapClient").ejOlapClient("option","locale", "fr-FR" ); </code>
</pre>






#### serviceMethodSettings<span class="type-signature type object">object</span>








Allows the user to set custom name for the methods at service-end invoked on AJAX post.




Default Value:






* null








##### Examples

<pre class="prettyprint">
<code> 
//To set serviceMethodSettings API value, to invoke the appropriate service method on UI operation.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {initialize: "MyMethod"}});</code>
</pre>
<pre class="prettyprint">
<code> 
//Gets or sets the serviceMethodSettings API, to invoke the appropriate service method on UI operation:
//Gets the serviceMethodSettings value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the serviceMethodSettings value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings",  {initialize: "MyMethod"} ); </code>
</pre>






#### serviceMethodSettings.cubeChanged<span class="type-signature type string">string</span>








Allows the user to set the custom name for the service method that&rsquo;s responsible for updating entire report and control while changing the Cube.




Default Value:






* "CubeChanged"








##### Examples

<pre class="prettyprint">
<code> 
//To set cubeChanged API value, to invoke the corresponding service method for updating entire report and control while changing the Cube.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {cubeChanged: "CubeChangedMyMethod"}});</code>
</pre>
<pre class="prettyprint">
<code> 
//Gets or sets the cubeChanged API, to invoke the corresponding service method for updating entire report and control while changing the Cube:
//Gets the cubeChanged value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the cubeChanged value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.cubeChanged","CubeChangedMyMethod" ); </code>
</pre>






#### serviceMethodSettings.fetchMemberTreeNodes<span class="type-signature type string">string</span>








Allows the user to set the custom name for the service method that&rsquo;s responsible to get members for the tree-view inside member-editor dialog.




Default Value:






* "FetchMemberTreeNodes"








##### Examples

<pre class="prettyprint">
<code> 
//To set fetchMemberTreeNodes API value, to invoke the corresponding service method to get members for the tree-view inside member-editor dialog.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {fetchMemberTreeNodes: "FetchMemberTreeNodesMyMethod"}});</code>
</pre>
<pre class="prettyprint">
<code> 
//Gets or sets the fetchMemberTreeNodes API, to invoke the corresponding service method to get members for the tree-view inside member-editor dialog:
//Gets the fetchMemberTreeNodes value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the fetchMemberTreeNodes value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.fetchMemberTreeNodes", "FetchMemberTreeNodesMyMethod" ); </code>
</pre>






#### serviceMethodSettings.fetchReportList<span class="type-signature type string">string</span>








Allows the user to set the custom name for the service method that&rsquo;s responsible for fetching the report names from the database.




Default Value:






* "FetchReportListFromDB"








##### Examples

<pre class="prettyprint">
<code>                     
//To set fetchReportList API value, to invoke the corresponding service method that&rsquo;s responsible for fetching the report names from the database.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {fetchReportList: "FetchReportListFromDBMyMethod"}});</code>
</pre>
<pre class="prettyprint">
<code> 
//Gets or sets the fetchReportList API, to invoke the corresponding service method that&rsquo;s responsible for fetching the report names from the database:
//Gets the fetchReportList value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the fetchReportList value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.fetchReportList", "FetchReportListFromDBMyMethod" ); </code>
</pre>






#### serviceMethodSettings.filterElement<span class="type-signature type string">string</span>








Allows the user to set the custom name for the service method that&rsquo;s responsible for updating reports while filtering members.




Default Value:






* "FilterElement"








##### Examples

<pre class="prettyprint">
<code> 
//To set filterElement API value, to invoke the corresponding service method for performing server-side operation while filtering members.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {filterElement: "filterElementMyMethod"}});</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the filterElement API, to invoke the corresponding service method for performing server-side operation while filtering members:
//Gets the filterElement value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the filterElement value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.filterElement", "FilterElementMyMethod" ); </code>
</pre>






#### serviceMethodSettings.initialize<span class="type-signature type string">string</span>








Allows the user to set the custom name for the service method that&rsquo;s responsible for initializing OLAP Client.




Default Value:






* "InitializeClient"








##### Examples

<pre class="prettyprint">
<code> 
//To set initialize API value, to invoke the corresponding service method for OLAP Client initialization.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {initialize: "InitializeClientMyMethod"});</code>
</pre>
<pre class="prettyprint">
<code> 
//Gets or sets the initialize API, to invoke the corresponding service method for OLAP Client initialization:
//Gets the initialize value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the initialize value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.initialize", "InitializeClientMyMethod" ); </code>
</pre>






#### serviceMethodSettings.loadReport<span class="type-signature type string">string</span>








Allows the user to set the custom name for the service method that&rsquo;s responsible for loading the report collection from database.




Default Value:






* "LoadReportFromDB"








##### Examples

<pre class="prettyprint">
<code> 
//To set loadReport API value, to invoke the corresponding service method that&rsquo;s responsible for loading the report collection from database.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {loadReport: "LoadReportFromDBMyMethod"}});</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the loadReport API, to invoke the corresponding service method that&rsquo;s responsible for loading the report from the database:
//Gets the loadReport value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the loadReport value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.loadReport", "LoadReportFromDBMyMethod"} ); </code>
</pre>






#### serviceMethodSettings.measureGroupChanged<span class="type-signature type string">string</span>








Allows the user to set the custom name for the service method that&rsquo;s responsible for updating cube browser tree while changing the measure group.




Default Value:






* "MeasureGroupChanged"








##### Examples

<pre class="prettyprint">
<code> 
//To set measureGroupChanged API value, to invoke the corresponding service method for updating the cube browser tree while changing the measure group.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {measureGroupChanged: "MeasureGroupChangedMyMethod"}});</code>
</pre>
<pre class="prettyprint">
<code> 
//Gets or sets the measureGroupChanged API, to invoke the corresponding service method for updating the cube browser tree while changing the Measure group:
//Gets the measureGroupChanged value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the measureGroupChanged value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.measureGroupChanged","MeasureGroupChangedMyMethod" ); </code>
</pre>






#### serviceMethodSettings.memberExpand<span class="type-signature type string">string</span>








Allows the user to set the custom name for the service method that&rsquo;s responsible to get the child members on node expand.




Default Value:






* "MemberExpanded"








##### Examples

<pre class="prettyprint">
<code> 
//To set memberExpand API value, to invoke the corresponding service method which would get the child members on node expand.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {memberExpand: "MemberExpandedMyMethod"}});</code>
</pre>
<pre class="prettyprint">
<code> 
//Gets or sets the memberExpand API, to invoke the corresponding service method which would get the child members on node expand:
//Gets the memberExpand value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the memberExpand value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.memberExpand", "MemberExpandedMyMethod" ); </code>
</pre>






#### serviceMethodSettings.nodeDropped<span class="type-signature type string">string</span>








Allows the user to set the custom name for the service method that&rsquo;s responsible for updating report while dropping a Node/SplitButton inside AxisElementBuilder.




Default Value:






* "NodeDropped"








##### Examples

<pre class="prettyprint">
<code> 
//To set nodeDropped API value, to invoke the corresponding service method for performing server-side operation while dropping a Node/SplitButton inside AxisElementBuilder.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {nodeDropped: "NodeDroppedMyMethod"}});</code>
</pre>
<pre class="prettyprint">
<code> 
//Gets or sets the nodeDropped API, to invoke the corresponding service method for performing server-side operation while dropping a Node/SplitButton inside AxisElementBuilder:
//Gets the nodeDropped value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the nodeDropped value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.nodeDropped","NodeDroppedMyMethod"); </code>
</pre>






#### serviceMethodSettings.removeSplitButton<span class="type-signature type string">string</span>








Allows the user to set the custom name for the service method that&rsquo;s responsible for updating report while removing SplitButton from AxisElementBuilder.




Default Value:






* "RemoveSplitButton"








##### Examples

<pre class="prettyprint">
<code> 
//To set removeSplitButton API value, to invoke the corresponding service method for performing server-side operation while removing SplitButton from the AxisElementBuilder.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {removeSplitButton: "RemoveSplitButtonMyMethod"}});</code>
</pre>
<pre class="prettyprint">
<code> 
//Gets or sets the removeSplitButton API, to invoke the corresponding service method for performing server-side operation while removing SplitButton from the AxisElementBuilder:
//Gets the removeSplitButton value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the removeSplitButton value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.removeSplitButton", "RemoveSplitButtonMyMethod" ); </code>
</pre>






#### serviceMethodSettings.saveReport<span class="type-signature type string">string</span>








Allows the user to set the custom name for the service method that&rsquo;s responsible for saving the report collection to database.




Default Value:






* "SaveReportToDB"








##### Examples

<pre class="prettyprint">
<code> 
//To set saveReport API value, to invoke the corresponding service method which would save the report collection to database.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {saveReport: "SaveReportToDBMyMethod"}});</code>
</pre>
<pre class="prettyprint">
<code> 
//Gets or sets the saveReport API, to invoke the corresponding service method which would save the report collection to database:
//Gets the saveReport value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the saveReport value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.saveReport", "SaveReportToDBMyMethod" ); </code>
</pre>






#### serviceMethodSettings.toolbarServices<span class="type-signature type string">string</span>








Allows the user to set the custom name for the service method that&rsquo;s responsible for any toolbar operation.




Default Value:






* "ToolbarOperations"








##### Examples

<pre class="prettyprint">
<code> 
//To set the toolbarServices API value, to invoke the corresponding service method responsible for any toolbar operation.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {toolbarServices: "ToolbarOperationsMyMethod"}});</code>
</pre>
<pre class="prettyprint">
<code> 
//Gets or sets the toolbarServices API value, to invoke the corresponding service method responsible for any toolbar operation:
//Gets the toolbarServices value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the toolbarServices value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.toolbarServices", "ToolbarOperationsMyMethod"} ); </code>
</pre>






#### serviceMethodSettings.updateReport<span class="type-signature type string">string</span>








Allows the user to set the custom name for the service method that&rsquo;s responsible for updating report collection.




Default Value:






* "UpdateReport"








##### Examples

<pre class="prettyprint">
<code> 
//To set updateReport API value, to invoke the corresponding service method that&rsquo;s responsible for updating the report collection and current report.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {updateReport: "UpdateReportFromMyMethod"}});</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the updateReport API, to invoke the corresponding service method that&rsquo;s responsible for updating the current report and report collection:
//Gets the updateReport value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the updateReport value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.updateReport", "UpdateReportFromMyMethod"} ); </code>
</pre>






#### title<span class="type-signature type string">string</span>








Sets the title for OLAP Client.




Default Value:






* null








##### Examples

<pre class="prettyprint">
<code> 
//To set title API value during initialization
$("#OlapClient").ejOlapClient({ title: "Olap Browser" });</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the title API, after initialization:
//Gets the title value  
$("#OlapClient").ejOlapClient("option","title");
                    
//Sets the title value 
$("#OlapClient").ejOlapClient("option","title", "Olap Browser" ); </code>
</pre>






#### url<span class="type-signature type string">string</span>








Connects the service using the specified URL for any server updates.




Default Value:






* null








##### Examples

<pre class="prettyprint">
<code> 
//To set url value during initialization
$("#OlapClient").ejOlapClient({ url: "/wcf/OlapClientService.svc" });</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the url, after initialization:
//Gets the url value  
$("#OlapClient").ejOlapClient("option","url");
                      
//Sets the url value 
$("#OlapClient").ejOlapClient("option","url", "/wcf/OlapClientService.svc" ); </code>
</pre>




### Methods








#### chartDrillSuccess<span class="signature">()</span>








This function is used to drill down the PivotGrid widget once OLAP Chart drill down.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="OlapClient"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create OLAP Client
$('#OlapClient').ejOlapClient({
      url: "OlapClientService.svc"
  });
var clientObj = $("#OlapClient").data("ejOlapClient");
clientObj.gridDrillSuccess(ej.proxy(function(){}, this));
// raised after OLAP Chart drill down
&lt;/script&gt;</code>
</pre>






#### cubeChanged<span class="signature">()</span>








This function is raised while changing the cube.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="OlapClient"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create OLAP Client
$('#OlapClient').ejOlapClient({
      url: "OlapClientService.svc"
  });
var clientObj = $("#OlapClient").data("ejOlapClient");
clientObj.cubeChanged(ej.proxy(function(){}, this));
// raised while changing cubes
&lt;/script&gt;</code>
</pre>






#### doAjaxPost<span class="signature">()</span>








Perform an asynchronous HTTP (Ajax) request.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="OlapClient"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create OLAP Client
$('#OlapClient').ejOlapClient({
      url: "OlapClientService.svc"
  });
var clientObj = $("#OlapClient").data("ejOlapClient");
clientObj.doAjaxPost("POST", "/OlapClientService.svc/Initialize", {"key", "Hello World"}, "renderControlSuccess", null);
// initiate an Ajax request
&lt;/script&gt;</code>
</pre>






#### getAxisPosition<span class="signature">()</span>








This function is used to get the position of the axis element builders.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="OlapClient"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create OLAP Client
$('#OlapClient').ejOlapClient({
      url: "OlapClientService.svc"
  });
var clientObj = $("#OlapClient").data("ejOlapClient");
clientObj.getAxisPosition(eve);
// used to get the position of the axis element builders
&lt;/script&gt;</code>
</pre>






#### gridDrillSuccess<span class="signature">()</span>








This function is used to drill down the OLAP Chart widget once PivotGrid component drill down.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="OlapClient"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create OLAP Client
$('#OlapClient').ejOlapClient({
      url: "OlapClientService.svc"
  });
var clientObj = $("#OlapClient").data("ejOlapClient");
clientObj.gridDrillSuccess(ej.proxy(function(){}, this));
// raised after PivotGrid drill down
&lt;/script&gt;</code>
</pre>






#### nodeDropped<span class="signature">()</span>








This function is used to perform required action after dropping a tree node in Axis Element builder.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="OlapClient"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create OLAP Client
$('#OlapClient').ejOlapClient({
      url: "OlapClientService.svc"
  });
var clientObj = $("#OlapClient").data("ejOlapClient");
clientObj.nodeDropped(ej.proxy(function(){}, this));
// raised while dropping tree nodes
&lt;/script&gt;</code>
</pre>






#### onDropped<span class="signature">()</span>








This function is raised after dropping the element in Axis Element Builder.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="OlapClient"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create OLAP Client
$('#OlapClient').ejOlapClient({
      url: "OlapClientService.svc"
  });
var clientObj = $("#OlapClient").data("ejOlapClient");
clientObj.onDropped(ej.proxy(function(){}, this));
// raised while dropping tree nodes
&lt;/script&gt;</code>
</pre>






#### onTabClick<span class="signature">()</span>








This function is raised while tab changes.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="OlapClient"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create OLAP Client
$('#OlapClient').ejOlapClient({
      url: "OlapClientService.svc"
  });
var clientObj = $("#OlapClient").data("ejOlapClient");
clientObj.onTabClick(ej.proxy(function(){}, this));
// raised while changing tabs
&lt;/script&gt;</code>
</pre>






#### reportChanged<span class="signature">()</span>








This function is raised while changing the report.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="OlapClient"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create OLAP Client
$('#OlapClient').ejOlapClient({
      url: "OlapClientService.svc"
  });
var clientObj = $("#OlapClient").data("ejOlapClient");
clientObj.reportChanged(ej.proxy(function(){}, this));
// raised while changing reports
&lt;/script&gt;</code>
</pre>






#### setSplitBtnTargetPos<span class="signature">()</span>








This function is used to set the position to currently dropped split button in respective axes.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="OlapClient"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create OLAP Client
$('#OlapClient').ejOlapClient({
      url: "OlapClientService.svc"
  });
var clientObj = $("#OlapClient").data("ejOlapClient");
clientObj.setSplitBtnTargetPos(eve);
// used to set the position to the dropped split button
&lt;/script&gt;</code>
</pre>




### Events








#### afterServiceInvoke








Fires after the service is invoked.

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
<td class="description last">Event parameters from OLAP Client component.
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
<td class="description last">return the current action of OLAP Client control.</td>
</tr>
<tr>
<td class="name"><code>customObject</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">return the custom object bounds with OLAP Client control.</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the outer HTML of OLAP Client control.</td>
</tr>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the OLAP Client model.</td>
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




##### Example

<pre class="prettyprint">
<code> 
//afterServiceInvoke event
$("#OlapClient").ejOlapClient({
                afterServiceInvoke: function (args) {}
});</code>
</pre>






#### beforeServiceInvoke








Fires when the summary cell is clicked.

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
<td class="description last">Event parameters from OLAP Client component.
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
<td class="description last">return the current action of OLAP Client control.</td>
</tr>
<tr>
<td class="name"><code>customObject</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">return the custom object bounds with OLAP Client control.</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the outer HTML of OLAP Client control.</td>
</tr>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the OLAP Client model.</td>
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




##### Example

<pre class="prettyprint">
<code> 
//beforeServiceInvoke event
$("#OlapClient").ejOlapClient({
                beforeServiceInvoke: function (args) {}
});</code>
</pre>






#### chartLoad








Fires before rendering the chart

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
<td class="description last">Event parameters from OLAP Chart component.
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
<td class="description last">if the event should be cancelled; otherwise, false.</td>
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




##### Example

<pre class="prettyprint">
<code> 
//event triggered when OLAP Chart begins rendering.
$("#OlapClient").ejOlapClient({
   chartLoad: function (args) {}
});      </code>
</pre>






#### load








Fires on loading the control

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
<td class="description last">Event parameters from OLAP Client component.
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
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the outer HTML of OLAP Client component.</td>
</tr>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the OLAP Client model.</td>
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




##### Example

<pre class="prettyprint">
<code> 
//event triggered on loading the control
$("#OlapClient").ejOlapClient({
   load: function (args) {}
});      </code>
</pre>






#### renderComplete








Fires on completion of rendering control

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
<td class="description last">Event parameters from OLAP Client component
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
<td class="name"><code>customObject</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the custom object bounded with the control.</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the outer HTML of OLAP Client control.</td>
</tr>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the OLAP Client model.</td>
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




##### Example

<pre class="prettyprint">
<code> 
//event triggered after completing rendering the control
$("#OlapClient").ejOlapClient({
   renderComplete: function (args) {}
});      </code>
</pre>






#### renderFailure








Fires when error occured in rendering the control

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
<td class="description last">Event parameters from OLAP Client component
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
<td class="name"><code>customObject</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the custom object bounded with the control.</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the outer HTML of OLAP Client control.</td>
</tr>
<tr>
<td class="name"><code>message</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the error message with error code.</td>
</tr>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the OLAP Client model.</td>
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




##### Example

<pre class="prettyprint">
<code> 
//event triggered when error occurs in rendering the control
$("#OlapClient").ejOlapClient({
   renderFailure: function (args) {}
});      </code>
</pre>






#### renderSuccess








Fires when the control is rendered success

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
<td class="description last">Event parameters from OLAP Client component.
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
<td class="name"><code>customObject</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the custom object bounded with the control.</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the outer HTML of OLAP Client control.</td>
</tr>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the OLAP Client model.</td>
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




##### Example

<pre class="prettyprint">
<code> 
//success event for rendering the control
$("#OlapClient").ejOlapClient({
   renderSuccess: function (args) {}
});      </code>
</pre>



