---
layout: post
title: ejOlapClient
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html OLAP Client control.










$(element).ejOlapClient<span class="signature">()</span>











Example
{:.example}


{% highlight html %}
 
<div id="OlapClient"></div> 
 
<script>
// Create OLAP Client
$("#OlapClient").ejOlapClient(...);     
</script>{% endhighlight %}







Requires
{:.require}




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




## Members








### chartType<span class="type-signature type enum">enum</span>
{:#members:charttype}








Sets the type for OLAP Chart component inside OLAP Client.




Default Value:
{:.param}






* ej.olap.OlapChart.ChartTypes.Column








Example
{:.example}


{% highlight html %}
 
//To set chartType API value during initialization
$("#OlapClient").ejOlapClient({ chartType: ej.olap.OlapChart.ChartTypes.Spline });{% endhighlight %}


{% highlight html %}
 
//Get or set the chartType API, after initialization:
//Gets the chartType value  
$("#OlapClient").ejOlapClient("option","chartType");
                        
//Sets the chartType value 
$("#OlapClient").ejOlapClient("option","chartType", ej.olap.OlapChart.ChartTypes.Area); {% endhighlight %}







### cssClass<span class="type-signature type string">string</span>
{:#members:cssclass}








Sets the CSS name for custom operation.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
//To set cssClass API value during initialization
$("#OlapClient").ejOlapClient({ cssClass: "Olive" });{% endhighlight %}


{% highlight html %}
 
//Get or set the cssClass API, after initialization:
//Gets the cssClass value  
$("#OlapClient").ejOlapClient("option","cssClass");
                 
//Sets the cssClass value 
$("#OlapClient").ejOlapClient("option","cssClass", "Olive" ); {% endhighlight %}







### customObject<span class="type-signature type object">Object</span>
{:#members:customobject}








Custom object to pass additional information between client-end and service-end.




Default Value:
{:.param}






* {}








Example
{:.example}


{% highlight html %}
 
//To set customObject API value during initialization
$("#OlapClient").ejOlapClient({ customObject: {"MyObject": "Hi Syncfusion!!"} });{% endhighlight %}


{% highlight html %}
 
//Get or set the customObject API, after initialization:
//Gets the customObject value  
$("#OlapClient").ejOlapClient("option","customObject");
                     
//Sets the customObject value 
$("#OlapClient").ejOlapClient("option","customObject", {"MyObject": "Hello World!!"} ); {% endhighlight %}







### displaySettings<span class="type-signature type object">object</span>
{:#members:displaysettings}








Allows the user to customize the control layout and appearance.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
//To set displaySettings API value, in-order to customize the control layout and appearance.
 $("#OlapClient").ejOlapClient({  displaySettings: {mode: "chartandgrid"}});{% endhighlight %}


{% highlight html %}
 
//Gets or sets the displaySettings API, to customize the control layout and appearance:
//Gets the displaySettings value  
$("#OlapClient").ejOlapClient("option", "displaySettings");
   
//Sets the displaySettings value 
$("#OlapClient").ejOlapClient("option", "displaySettings", {mode: "chartandgrid"} ); {% endhighlight %}







### displaySettings.controlPlacement<span class="type-signature type enum">enum</span>
{:#members:displaysettings-controlplacement}








Lets the user to customize the display of OLAP Chart and OLAP Grid controls inside the OLAP Client component.




Default Value:
{:.param}






* ej.olap.OlapClient.ControlPlacement.Tab








Example
{:.example}


{% highlight html %}
 
//To set controlPlacement API value during initialization
$("#OlapClient").ejOlapClient({ displaySettings: {controlPlacement: ej.olap.OlapClient.ControlPlacement.Tab} });{% endhighlight %}


{% highlight html %}
 
//Get or set the controlPlacement API, after initialization:
//Gets the controlPlacement value  
$("#OlapClient").ejOlapClient("option","displaySettings.controlPlacement");
                 
//Sets the controlPlacement value 
$("#OlapClient").ejOlapClient("option","displaySettings.controlPlacement", ej.olap.OlapClient.ControlPlacement.Tile ); {% endhighlight %}







### displaySettings.defaultView<span class="type-signature type enum">enum</span>
{:#members:displaysettings-defaultview}








Lets the user to set Chart or Grid tab as default.




Default Value:
{:.param}






* ej.olap.OlapClient.DefaultView.Grid








Example
{:.example}


{% highlight html %}
 
//To set defaultView API value during initialization
$("#OlapClient").ejOlapClient({ displaySettings: {defaultView: ej.olap.OlapClient.DefaultView.Grid} });{% endhighlight %}


{% highlight html %}
 
//Get or set the defaultView API, after initialization:
//Gets the defaultView value  
$("#OlapClient").ejOlapClient("option","displaySettings.defaultView");
                      
//Sets the defaultView value 
$("#OlapClient").ejOlapClient("option","displaySettings.defaultView", ej.olap.OlapClient.DefaultView.Chart ); {% endhighlight %}







### displaySettings.enableFullScreen<span class="type-signature type boolean">boolean</span>
{:#members:displaysettings-enablefullscreen}








Enables/ disables the full screen view of the OLAP components(OLAP Chart, OLAP Grid) in OLAP Client.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
//To set enableFullScreen API value during initialization
$("#OlapClient").ejOlapClient({ displaySettings.enableFullScreen: true });{% endhighlight %}


{% highlight html %}
 
//Get or set the enableFullScreen API, after initialization:
//Gets the enableFullScreen value  
$("#OlapClient").ejOlapClient("option","displaySettings.enableFullScreen");
                 
//Sets the enableFullScreen value 
$("#OlapClient").ejOlapClient("option","displaySettings.enableFullScreen", true ); {% endhighlight %}







### displaySettings.enableTogglePanel<span class="type-signature type boolean">boolean</span>
{:#members:displaysettings-enabletogglepanel}








Sets the Toggle Panel visibility mode.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
//To set enableTogglePanel API value during initialization
$("#OlapClient").ejOlapClient({ displaySettings.enableTogglePanel: true });{% endhighlight %}


{% highlight html %}
 
//Get or set the enableTogglePanel API, after initialization:
//Gets the enableTogglePanel value  
$("#OlapClient").ejOlapClient("option","displaySettings.enableTogglePanel");
                        
//Sets the enableTogglePanel value 
$("#OlapClient").ejOlapClient("option","displaySettings.enableTogglePanel", true ); {% endhighlight %}







### displaySettings.mode<span class="type-signature type enum">enum</span>
{:#members:displaysettings-mode}








Sets the display mode (Only Chart/Only Grid/Both Chart And Grid) of OLAP Client.




Default Value:
{:.param}






* ej.olap.OlapClient.DisplayMode.ChartAndGrid








Example
{:.example}


{% highlight html %}
 
//To set mode API value during initialization
$("#OlapClient").ejOlapClient({ displaySettings: { mode: ej.olap.OlapClient.DisplayMode.ChartOnly }});{% endhighlight %}


{% highlight html %}
 
//Get or set the mode API, after initialization:
//Gets the mode value  
$("#OlapClient").ejOlapClient("option","displaySettings.mode");
                     
//Sets the mode value 
$("#OlapClient").ejOlapClient("option","displaySettings.mode", ej.olap.OlapClient.DisplayMode.ChartOnly ); {% endhighlight %}







### enableMeasureGroups<span class="type-signature type boolean">boolean</span>
{:#members:enablemeasuregroups}








Enables/ disables the visibility of measure group selector drop down in Cube browser in OLAP Client.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
//To set enableMeasureGroups API value during initialization
$("#OlapClient").ejOlapClient({ enableMeasureGroups : true });{% endhighlight %}


{% highlight html %}
 
//Get or set the enableMeasureGroups API, after initialization:
//Gets the enableMeasureGroups value  
$("#OlapClient").ejOlapClient("option","enableMeasureGroups");
                      
//Sets the enableMeasureGroups value 
$("#OlapClient").ejOlapClient("option","enableMeasureGroups", true ); {% endhighlight %}







### gridLayout<span class="type-signature type enum">enum</span>
{:#members:gridlayout}








Sets the layout for OLAP Grid component inside OLAP Client.




Default Value:
{:.param}






* ej.PivotGrid.Layout.Normal








Example
{:.example}


{% highlight html %}
 
//To set gridLayout API value during initialization
$("#OlapClient").ejOlapClient({ gridLayout: ej.PivotGrid.Layout.NoSummaries });{% endhighlight %}


{% highlight html %}
 
//Get or set the gridLayout API, after initialization:
//Gets the gridLayout value  
$("#OlapClient").ejOlapClient("option","gridLayout");
                       
//Sets the gridLayout value 
$("#OlapClient").ejOlapClient("option","gridLayout", ej.PivotGrid.Layout.NormalTopSummary); {% endhighlight %}







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
$("#OlapClient1").ejOlapClient({isResponsive: true});{% endhighlight %}


{% highlight html %}
 
//Get or set the isResponsive, after initialization:
//Gets the isResponsive values state
$("#OlapClient").ejOlapClient("option", "isResponsive");
                    
//Sets the reponsive layout
$("#OlapClient").ejOlapClient("option", "isResponsive","true"); {% endhighlight %}







### locale<span class="type-signature type string">string</span>
{:#members:locale}








Sets the localized language for the control.




Default Value:
{:.param}






* "en-US"








Example
{:.example}


{% highlight html %}
 
//To set locale API value during initialization
$("#OlapClient").ejOlapClient({ locale: "en-US" });{% endhighlight %}


{% highlight html %}
 
//Get or set the locale API, after initialization:
//Gets the locale value  
$("#OlapClient").ejOlapClient("option","locale");
                   
//Sets the locale value 
$("#OlapClient").ejOlapClient("option","locale", "fr-FR" ); {% endhighlight %}







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
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {initialize: "MyMethod"}});{% endhighlight %}


{% highlight html %}
 
//Gets or sets the serviceMethodSettings API, to invoke the appropriate service method on UI operation:
//Gets the serviceMethodSettings value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the serviceMethodSettings value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings",  {initialize: "MyMethod"} ); {% endhighlight %}







### serviceMethodSettings.cubeChanged<span class="type-signature type string">string</span>
{:#members:servicemethodsettings-cubechanged}








Allows the user to set the custom name for the service method that&rsquo;s responsible for updating entire report and control while changing the Cube.




Default Value:
{:.param}






* "CubeChanged"








Example
{:.example}


{% highlight html %}
 
//To set cubeChanged API value, to invoke the corresponding service method for updating entire report and control while changing the Cube.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {cubeChanged: "CubeChangedMyMethod"}});{% endhighlight %}


{% highlight html %}
 
//Gets or sets the cubeChanged API, to invoke the corresponding service method for updating entire report and control while changing the Cube:
//Gets the cubeChanged value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the cubeChanged value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.cubeChanged","CubeChangedMyMethod" ); {% endhighlight %}







### serviceMethodSettings.fetchMemberTreeNodes<span class="type-signature type string">string</span>
{:#members:servicemethodsettings-fetchmembertreenodes}








Allows the user to set the custom name for the service method that&rsquo;s responsible to get members for the tree-view inside member-editor dialog.




Default Value:
{:.param}






* "FetchMemberTreeNodes"








Example
{:.example}


{% highlight html %}
 
//To set fetchMemberTreeNodes API value, to invoke the corresponding service method to get members for the tree-view inside member-editor dialog.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {fetchMemberTreeNodes: "FetchMemberTreeNodesMyMethod"}});{% endhighlight %}


{% highlight html %}
 
//Gets or sets the fetchMemberTreeNodes API, to invoke the corresponding service method to get members for the tree-view inside member-editor dialog:
//Gets the fetchMemberTreeNodes value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the fetchMemberTreeNodes value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.fetchMemberTreeNodes", "FetchMemberTreeNodesMyMethod" ); {% endhighlight %}







### serviceMethodSettings.fetchReportList<span class="type-signature type string">string</span>
{:#members:servicemethodsettings-fetchreportlist}








Allows the user to set the custom name for the service method that&rsquo;s responsible for fetching the report names from the database.




Default Value:
{:.param}






* "FetchReportListFromDB"








Example
{:.example}


{% highlight html %}
                     
//To set fetchReportList API value, to invoke the corresponding service method that&rsquo;s responsible for fetching the report names from the database.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {fetchReportList: "FetchReportListFromDBMyMethod"}});{% endhighlight %}


{% highlight html %}
 
//Gets or sets the fetchReportList API, to invoke the corresponding service method that&rsquo;s responsible for fetching the report names from the database:
//Gets the fetchReportList value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the fetchReportList value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.fetchReportList", "FetchReportListFromDBMyMethod" ); {% endhighlight %}







### serviceMethodSettings.filterElement<span class="type-signature type string">string</span>
{:#members:servicemethodsettings-filterelement}








Allows the user to set the custom name for the service method that&rsquo;s responsible for updating reports while filtering members.




Default Value:
{:.param}






* "FilterElement"








Example
{:.example}


{% highlight html %}
 
//To set filterElement API value, to invoke the corresponding service method for performing server-side operation while filtering members.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {filterElement: "filterElementMyMethod"}});{% endhighlight %}


{% highlight html %}
 
//Get or set the filterElement API, to invoke the corresponding service method for performing server-side operation while filtering members:
//Gets the filterElement value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the filterElement value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.filterElement", "FilterElementMyMethod" ); {% endhighlight %}







### serviceMethodSettings.initialize<span class="type-signature type string">string</span>
{:#members:servicemethodsettings-initialize}








Allows the user to set the custom name for the service method that&rsquo;s responsible for initializing OLAP Client.




Default Value:
{:.param}






* "InitializeClient"








Example
{:.example}


{% highlight html %}
 
//To set initialize API value, to invoke the corresponding service method for OLAP Client initialization.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {initialize: "InitializeClientMyMethod"});{% endhighlight %}


{% highlight html %}
 
//Gets or sets the initialize API, to invoke the corresponding service method for OLAP Client initialization:
//Gets the initialize value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the initialize value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.initialize", "InitializeClientMyMethod" ); {% endhighlight %}







### serviceMethodSettings.loadReport<span class="type-signature type string">string</span>
{:#members:servicemethodsettings-loadreport}








Allows the user to set the custom name for the service method that&rsquo;s responsible for loading the report collection from database.




Default Value:
{:.param}






* "LoadReportFromDB"








Example
{:.example}


{% highlight html %}
 
//To set loadReport API value, to invoke the corresponding service method that&rsquo;s responsible for loading the report collection from database.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {loadReport: "LoadReportFromDBMyMethod"}});{% endhighlight %}


{% highlight html %}
 
//Get or set the loadReport API, to invoke the corresponding service method that&rsquo;s responsible for loading the report from the database:
//Gets the loadReport value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the loadReport value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.loadReport", "LoadReportFromDBMyMethod"} ); {% endhighlight %}







### serviceMethodSettings.measureGroupChanged<span class="type-signature type string">string</span>
{:#members:servicemethodsettings-measuregroupchanged}








Allows the user to set the custom name for the service method that&rsquo;s responsible for updating cube browser tree while changing the measure group.




Default Value:
{:.param}






* "MeasureGroupChanged"








Example
{:.example}


{% highlight html %}
 
//To set measureGroupChanged API value, to invoke the corresponding service method for updating the cube browser tree while changing the measure group.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {measureGroupChanged: "MeasureGroupChangedMyMethod"}});{% endhighlight %}


{% highlight html %}
 
//Gets or sets the measureGroupChanged API, to invoke the corresponding service method for updating the cube browser tree while changing the Measure group:
//Gets the measureGroupChanged value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the measureGroupChanged value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.measureGroupChanged","MeasureGroupChangedMyMethod" ); {% endhighlight %}







### serviceMethodSettings.memberExpand<span class="type-signature type string">string</span>
{:#members:servicemethodsettings-memberexpand}








Allows the user to set the custom name for the service method that&rsquo;s responsible to get the child members on node expand.




Default Value:
{:.param}






* "MemberExpanded"








Example
{:.example}


{% highlight html %}
 
//To set memberExpand API value, to invoke the corresponding service method which would get the child members on node expand.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {memberExpand: "MemberExpandedMyMethod"}});{% endhighlight %}


{% highlight html %}
 
//Gets or sets the memberExpand API, to invoke the corresponding service method which would get the child members on node expand:
//Gets the memberExpand value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the memberExpand value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.memberExpand", "MemberExpandedMyMethod" ); {% endhighlight %}







### serviceMethodSettings.nodeDropped<span class="type-signature type string">string</span>
{:#members:servicemethodsettings-nodedropped}








Allows the user to set the custom name for the service method that&rsquo;s responsible for updating report while dropping a Node/SplitButton inside AxisElementBuilder.




Default Value:
{:.param}






* "NodeDropped"








Example
{:.example}


{% highlight html %}
 
//To set nodeDropped API value, to invoke the corresponding service method for performing server-side operation while dropping a Node/SplitButton inside AxisElementBuilder.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {nodeDropped: "NodeDroppedMyMethod"}});{% endhighlight %}


{% highlight html %}
 
//Gets or sets the nodeDropped API, to invoke the corresponding service method for performing server-side operation while dropping a Node/SplitButton inside AxisElementBuilder:
//Gets the nodeDropped value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the nodeDropped value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.nodeDropped","NodeDroppedMyMethod"); {% endhighlight %}







### serviceMethodSettings.removeSplitButton<span class="type-signature type string">string</span>
{:#members:servicemethodsettings-removesplitbutton}








Allows the user to set the custom name for the service method that&rsquo;s responsible for updating report while removing SplitButton from AxisElementBuilder.




Default Value:
{:.param}






* "RemoveSplitButton"








Example
{:.example}


{% highlight html %}
 
//To set removeSplitButton API value, to invoke the corresponding service method for performing server-side operation while removing SplitButton from the AxisElementBuilder.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {removeSplitButton: "RemoveSplitButtonMyMethod"}});{% endhighlight %}


{% highlight html %}
 
//Gets or sets the removeSplitButton API, to invoke the corresponding service method for performing server-side operation while removing SplitButton from the AxisElementBuilder:
//Gets the removeSplitButton value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the removeSplitButton value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.removeSplitButton", "RemoveSplitButtonMyMethod" ); {% endhighlight %}







### serviceMethodSettings.saveReport<span class="type-signature type string">string</span>
{:#members:servicemethodsettings-savereport}








Allows the user to set the custom name for the service method that&rsquo;s responsible for saving the report collection to database.




Default Value:
{:.param}






* "SaveReportToDB"








Example
{:.example}


{% highlight html %}
 
//To set saveReport API value, to invoke the corresponding service method which would save the report collection to database.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {saveReport: "SaveReportToDBMyMethod"}});{% endhighlight %}


{% highlight html %}
 
//Gets or sets the saveReport API, to invoke the corresponding service method which would save the report collection to database:
//Gets the saveReport value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the saveReport value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.saveReport", "SaveReportToDBMyMethod" ); {% endhighlight %}







### serviceMethodSettings.toolbarServices<span class="type-signature type string">string</span>
{:#members:servicemethodsettings-toolbarservices}








Allows the user to set the custom name for the service method that&rsquo;s responsible for any toolbar operation.




Default Value:
{:.param}






* "ToolbarOperations"








Example
{:.example}


{% highlight html %}
 
//To set the toolbarServices API value, to invoke the corresponding service method responsible for any toolbar operation.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {toolbarServices: "ToolbarOperationsMyMethod"}});{% endhighlight %}


{% highlight html %}
 
//Gets or sets the toolbarServices API value, to invoke the corresponding service method responsible for any toolbar operation:
//Gets the toolbarServices value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the toolbarServices value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.toolbarServices", "ToolbarOperationsMyMethod"} ); {% endhighlight %}







### serviceMethodSettings.updateReport<span class="type-signature type string">string</span>
{:#members:servicemethodsettings-updatereport}








Allows the user to set the custom name for the service method that&rsquo;s responsible for updating report collection.




Default Value:
{:.param}






* "UpdateReport"








Example
{:.example}


{% highlight html %}
 
//To set updateReport API value, to invoke the corresponding service method that&rsquo;s responsible for updating the report collection and current report.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {updateReport: "UpdateReportFromMyMethod"}});{% endhighlight %}


{% highlight html %}
 
//Get or set the updateReport API, to invoke the corresponding service method that&rsquo;s responsible for updating the current report and report collection:
//Gets the updateReport value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the updateReport value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.updateReport", "UpdateReportFromMyMethod"} ); {% endhighlight %}







### title<span class="type-signature type string">string</span>
{:#members:title}








Sets the title for OLAP Client.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
//To set title API value during initialization
$("#OlapClient").ejOlapClient({ title: "Olap Browser" });{% endhighlight %}


{% highlight html %}
 
//Get or set the title API, after initialization:
//Gets the title value  
$("#OlapClient").ejOlapClient("option","title");
                    
//Sets the title value 
$("#OlapClient").ejOlapClient("option","title", "Olap Browser" ); {% endhighlight %}







### url<span class="type-signature type string">string</span>
{:#members:url}








Connects the service using the specified URL for any server updates.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
//To set url value during initialization
$("#OlapClient").ejOlapClient({ url: "/wcf/OlapClientService.svc" });{% endhighlight %}


{% highlight html %}
 
//Get or set the url, after initialization:
//Gets the url value  
$("#OlapClient").ejOlapClient("option","url");
                      
//Sets the url value 
$("#OlapClient").ejOlapClient("option","url", "/wcf/OlapClientService.svc" ); {% endhighlight %}





## Methods








### chartDrillSuccess<span class="signature">()</span>
{:#methods:chartdrillsuccess}








This function is used to drill down the OLAP Grid widget once OLAP Chart drill down.





Example
{:.example}


{% highlight html %}
 
<div id="OlapClient"></div> 
 
<script>
// Create OLAP Client
$('#OlapClient').ejOlapClient({
      url: "OlapClientService.svc"
  });
var clientObj = $("#OlapClient").data("ejOlapClient");
clientObj.gridDrillSuccess(ej.proxy(function(){}, this));
// raised after OLAP Chart drill down
</script>{% endhighlight %}







### cubeChanged<span class="signature">()</span>
{:#methods:cubechanged}








This function is raised while changing the cube.





Example
{:.example}


{% highlight html %}
 
<div id="OlapClient"></div> 
 
<script>
// Create OLAP Client
$('#OlapClient').ejOlapClient({
      url: "OlapClientService.svc"
  });
var clientObj = $("#OlapClient").data("ejOlapClient");
clientObj.cubeChanged(ej.proxy(function(){}, this));
// raised while changing cubes
</script>{% endhighlight %}







### doAjaxPost<span class="signature">()</span>
{:#methods:doajaxpost}








Perform an asynchronous HTTP (Ajax) request.





Example
{:.example}


{% highlight html %}
 
<div id="OlapClient"></div> 
 
<script>
// Create OLAP Client
$('#OlapClient').ejOlapClient({
      url: "OlapClientService.svc"
  });
var clientObj = $("#OlapClient").data("ejOlapClient");
clientObj.doAjaxPost("POST", "/OlapClientService.svc/Initialize", {"key", "Hello World"}, "renderControlSuccess", null);
// initiate an Ajax request
</script>{% endhighlight %}







### getAxisPosition<span class="signature">()</span>
{:#methods:getaxisposition}








This function is used to get the position of the axis element builders.





Example
{:.example}


{% highlight html %}
 
<div id="OlapClient"></div> 
 
<script>
// Create OLAP Client
$('#OlapClient').ejOlapClient({
      url: "OlapClientService.svc"
  });
var clientObj = $("#OlapClient").data("ejOlapClient");
clientObj.getAxisPosition(eve);
// used to get the position of the axis element builders
</script>{% endhighlight %}







### gridDrillSuccess<span class="signature">()</span>
{:#methods:griddrillsuccess}








This function is used to drill down the OLAP Chart widget once OLAP Grid component drill down.





Example
{:.example}


{% highlight html %}
 
<div id="OlapClient"></div> 
 
<script>
// Create OLAP Client
$('#OlapClient').ejOlapClient({
      url: "OlapClientService.svc"
  });
var clientObj = $("#OlapClient").data("ejOlapClient");
clientObj.gridDrillSuccess(ej.proxy(function(){}, this));
// raised after OLAP Grid drill down
</script>{% endhighlight %}







### nodeDropped<span class="signature">()</span>
{:#methods:nodedropped}








This function is used to perform required action after dropping a tree node in Axis Element builder.





Example
{:.example}


{% highlight html %}
 
<div id="OlapClient"></div> 
 
<script>
// Create OLAP Client
$('#OlapClient').ejOlapClient({
      url: "OlapClientService.svc"
  });
var clientObj = $("#OlapClient").data("ejOlapClient");
clientObj.nodeDropped(ej.proxy(function(){}, this));
// raised while dropping tree nodes
</script>{% endhighlight %}







### onDropped<span class="signature">()</span>
{:#methods:ondropped}








This function is raised after dropping the element in Axis Element Builder.





Example
{:.example}


{% highlight html %}
 
<div id="OlapClient"></div> 
 
<script>
// Create OLAP Client
$('#OlapClient').ejOlapClient({
      url: "OlapClientService.svc"
  });
var clientObj = $("#OlapClient").data("ejOlapClient");
clientObj.onDropped(ej.proxy(function(){}, this));
// raised while dropping tree nodes
</script>{% endhighlight %}







### onTabClick<span class="signature">()</span>
{:#methods:ontabclick}








This function is raised while tab changes.





Example
{:.example}


{% highlight html %}
 
<div id="OlapClient"></div> 
 
<script>
// Create OLAP Client
$('#OlapClient').ejOlapClient({
      url: "OlapClientService.svc"
  });
var clientObj = $("#OlapClient").data("ejOlapClient");
clientObj.onTabClick(ej.proxy(function(){}, this));
// raised while changing tabs
</script>{% endhighlight %}







### reportChanged<span class="signature">()</span>
{:#methods:reportchanged}








This function is raised while changing the report.





Example
{:.example}


{% highlight html %}
 
<div id="OlapClient"></div> 
 
<script>
// Create OLAP Client
$('#OlapClient').ejOlapClient({
      url: "OlapClientService.svc"
  });
var clientObj = $("#OlapClient").data("ejOlapClient");
clientObj.reportChanged(ej.proxy(function(){}, this));
// raised while changing reports
</script>{% endhighlight %}







### setSplitBtnTargetPos<span class="signature">()</span>
{:#methods:setsplitbtntargetpos}








This function is used to set the position to currently dropped split button in respective axes.





Example
{:.example}


{% highlight html %}
 
<div id="OlapClient"></div> 
 
<script>
// Create OLAP Client
$('#OlapClient').ejOlapClient({
      url: "OlapClientService.svc"
  });
var clientObj = $("#OlapClient").data("ejOlapClient");
clientObj.setSplitBtnTargetPos(eve);
// used to set the position to the dropped split button
</script>{% endhighlight %}





## Events








### afterServiceInvoke
{:#events:afterserviceinvoke}








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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
action{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the current action of OLAP Client control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">return the custom object bounds with OLAP Client control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the outer HTML of OLAP Client control.</td>
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
<td class="description last">returns the OLAP Client model.</td>
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
 
//afterServiceInvoke event
$("#OlapClient").ejOlapClient({
    afterServiceInvoke: function(args) {}
});{% endhighlight %}







### beforeServiceInvoke
{:#events:beforeserviceinvoke}








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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
action{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the current action of OLAP Client control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">return the custom object bounds with OLAP Client control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the outer HTML of OLAP Client control.</td>
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
<td class="description last">returns the OLAP Client model.</td>
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
 
//beforeServiceInvoke event
$("#OlapClient").ejOlapClient({
    beforeServiceInvoke: function(args) {}
});{% endhighlight %}







### chartLoad
{:#events:chartload}








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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
 
//event triggered when OLAP Chart begins rendering.
$("#OlapClient").ejOlapClient({
   chartLoad: function (args) {}
});      {% endhighlight %}







### load
{:#events:load}








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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the outer HTML of OLAP Client component.</td>
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
<td class="description last">returns the OLAP Client model.</td>
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
 
//event triggered on loading the control
$("#OlapClient").ejOlapClient({
   load: function (args) {}
});      {% endhighlight %}







### renderComplete
{:#events:rendercomplete}








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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the custom object bounded with the control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the outer HTML of OLAP Client control.</td>
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
<td class="description last">returns the OLAP Client model.</td>
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
 
//event triggered after completing rendering the control
$("#OlapClient").ejOlapClient({
   renderComplete: function (args) {}
});      {% endhighlight %}







### renderFailure
{:#events:renderfailure}








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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the custom object bounded with the control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the outer HTML of OLAP Client control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
message{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the error message with error code.</td>
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
<td class="description last">returns the OLAP Client model.</td>
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
 
//event triggered when error occurs in rendering the control
$("#OlapClient").ejOlapClient({
   renderFailure: function (args) {}
});      {% endhighlight %}







### renderSuccess
{:#events:rendersuccess}








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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the custom object bounded with the control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the outer HTML of OLAP Client control.</td>
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
<td class="description last">returns the OLAP Client model.</td>
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
 
//success event for rendering the control
$("#OlapClient").ejOlapClient({
   renderSuccess: function (args) {}
});      {% endhighlight %}




