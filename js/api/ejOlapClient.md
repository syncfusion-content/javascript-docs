---
layout: post
title: ejOlapClient
documentation: API
platform: js
keywords: ejOlapClient, API, Essential JS OlapClient
metaname: 
metacontent: 
---

# OlapClient

Custom Design for Html OLAP Client control.


#### Syntax

{% highlight js %}

$(element).ejOlapClient()

{% endhighlight %}


#### Example

{% highlight html %}
 
<div id="OlapClient"></div> 
 
<script>
// Create OLAP Client
$("#OlapClient").ejOlapClient(...);     
</script>

{% endhighlight %}


#### Requires

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

### chartType `enum`
{:#members:charttype}

Sets the type for OLAP Chart component inside OLAP Client.


#### Default Value

* ej.olap.OlapChart.ChartTypes.Column


#### Example

{% highlight html %}
 
//To set chartType API value during initialization
$("#OlapClient").ejOlapClient({ chartType: ej.olap.OlapChart.ChartTypes.Spline });

{% endhighlight %}


{% highlight html %}
 
//Get or set the chartType API, after initialization:
//Gets the chartType value  
$("#OlapClient").ejOlapClient("option","chartType");
                        
//Sets the chartType value 
$("#OlapClient").ejOlapClient("option","chartType", ej.olap.OlapChart.ChartTypes.Area);

 {% endhighlight %}



### cssClass `string`
{:#members:cssclass}

Sets the CSS name for custom operation.


#### Default Value

* null


#### Example

{% highlight html %}
 
//To set cssClass API value during initialization
$("#OlapClient").ejOlapClient({ cssClass: "Olive" });

{% endhighlight %}


{% highlight html %}
 
//Get or set the cssClass API, after initialization:
//Gets the cssClass value  
$("#OlapClient").ejOlapClient("option","cssClass");
                 
//Sets the cssClass value 
$("#OlapClient").ejOlapClient("option","cssClass", "Olive" ); 

{% endhighlight %}

### customObject `object`
{:#members:customobject}

Custom object to pass additional information between client-end and service-end.

#### Default Value

* {}


#### Example

{% highlight html %}
 
//To set customObject API value during initialization
$("#OlapClient").ejOlapClient({ customObject: {"MyObject": "Hi Syncfusion!!"} });

{% endhighlight %}


{% highlight html %}
 
//Get or set the customObject API, after initialization:
//Gets the customObject value  
$("#OlapClient").ejOlapClient("option","customObject");
                     
//Sets the customObject value 
$("#OlapClient").ejOlapClient("option","customObject", {"MyObject": "Hello World!!"} );

 {% endhighlight %}


### displaySettings `object`
{:#members:displaysettings}

Allows the user to customize the control layout and appearance.


#### Default Value

* null


#### Example

{% highlight html %}
 
//To set displaySettings API value, in-order to customize the control layout and appearance.
 $("#OlapClient").ejOlapClient({  displaySettings: {mode: "chartandgrid"}});
 
 {% endhighlight %}


{% highlight html %}
 
//Gets or sets the displaySettings API, to customize the control layout and appearance:
//Gets the displaySettings value  
$("#OlapClient").ejOlapClient("option", "displaySettings");
   
//Sets the displaySettings value 
$("#OlapClient").ejOlapClient("option", "displaySettings", {mode: "chartandgrid"} ); 

{% endhighlight %}



### displaySettings.controlPlacement `enum`
{:#members:displaysettings-controlplacement}

Lets the user to customize the display of OLAP Chart and OLAP Grid controls inside the OLAP Client component.


#### Default Value

* ej.olap.OlapClient.ControlPlacement.Tab


#### Example

{% highlight html %}
 
//To set controlPlacement API value during initialization
$("#OlapClient").ejOlapClient({ displaySettings: {controlPlacement: ej.olap.OlapClient.ControlPlacement.Tab} });

{% endhighlight %}


{% highlight html %}
 
//Get or set the controlPlacement API, after initialization:
//Gets the controlPlacement value  
$("#OlapClient").ejOlapClient("option","displaySettings.controlPlacement");
                 
//Sets the controlPlacement value 
$("#OlapClient").ejOlapClient("option","displaySettings.controlPlacement", ej.olap.OlapClient.ControlPlacement.Tile ); 

{% endhighlight %}



### displaySettings.defaultView `enum`
{:#members:displaysettings-defaultview}

Lets the user to set Chart or Grid tab as default.


#### Default Value

* ej.olap.OlapClient.DefaultView.Grid


#### Example

{% highlight html %}
 
//To set defaultView API value during initialization
$("#OlapClient").ejOlapClient({ displaySettings: {defaultView: ej.olap.OlapClient.DefaultView.Grid} });

{% endhighlight %}


{% highlight html %}
 
//Get or set the defaultView API, after initialization:
//Gets the defaultView value  
$("#OlapClient").ejOlapClient("option","displaySettings.defaultView");
                      
//Sets the defaultView value 
$("#OlapClient").ejOlapClient("option","displaySettings.defaultView", ej.olap.OlapClient.DefaultView.Chart ); 

{% endhighlight %}



### displaySettings.enableFullScreen `boolean`
{:#members:displaysettings-enablefullscreen}

Enables/ disables the full screen view of the OLAP components(OLAP Chart, OLAP Grid) in OLAP Client.


#### Default Value

* false


#### Example

{% highlight html %}
 
//To set enableFullScreen API value during initialization
$("#OlapClient").ejOlapClient({ displaySettings.enableFullScreen: true });

{% endhighlight %}


{% highlight html %}
 
//Get or set the enableFullScreen API, after initialization:
//Gets the enableFullScreen value  
$("#OlapClient").ejOlapClient("option","displaySettings.enableFullScreen");
                 
//Sets the enableFullScreen value 
$("#OlapClient").ejOlapClient("option","displaySettings.enableFullScreen", true ); 

{% endhighlight %}


### displaySettings.enableTogglePanel `boolean`
{:#members:displaysettings-enabletogglepanel}

Sets the Toggle Panel visibility mode.


#### Default Value

* false


#### Example

{% highlight html %}
 
//To set enableTogglePanel API value during initialization
$("#OlapClient").ejOlapClient({ displaySettings.enableTogglePanel: true });

{% endhighlight %}


{% highlight html %}
 
//Get or set the enableTogglePanel API, after initialization:
//Gets the enableTogglePanel value  
$("#OlapClient").ejOlapClient("option","displaySettings.enableTogglePanel");
                        
//Sets the enableTogglePanel value 
$("#OlapClient").ejOlapClient("option","displaySettings.enableTogglePanel", true ); 

{% endhighlight %}



### displaySettings.isResponsive `boolean`
{:#members:displaysettings-isresponsive}

Allows the user to enable Responsive layout support.

#### Default Value

* false

#### Example

{% highlight html %}
 
//To set the isResponsive option during initialization  
$("#OlapClient1").ejOlapClient({isResponsive: true});

{% endhighlight %}


{% highlight html %}
 
//Get or set the isResponsive, after initialization:
//Gets the isResponsive values state
$("#OlapClient").ejOlapClient("option", "isResponsive");
                    
//Sets the reponsive layout
$("#OlapClient").ejOlapClient("option", "isResponsive","true"); 

{% endhighlight %}



### displaySettings.mode `enum`
{:#members:displaysettings-mode}

Sets the display mode (Only Chart/Only Grid/Both Chart And Grid) of OLAP Client.


#### Default Value

* ej.olap.OlapClient.DisplayMode.ChartAndGrid


#### Example

{% highlight html %}
 
//To set mode API value during initialization
$("#OlapClient").ejOlapClient({ displaySettings: { mode: ej.olap.OlapClient.DisplayMode.ChartOnly }});

{% endhighlight %}


{% highlight html %}
 
//Get or set the mode API, after initialization:
//Gets the mode value  
$("#OlapClient").ejOlapClient("option","displaySettings.mode");
                     
//Sets the mode value 
$("#OlapClient").ejOlapClient("option","displaySettings.mode", ej.olap.OlapClient.DisplayMode.ChartOnly ); 

{% endhighlight %}



### enableMeasureGroups `boolean`
{:#members:enablemeasuregroups}

Enables/ disables the visibility of measure group selector drop down in Cube browser in OLAP Client.


#### Default Value

* false


#### Example

{% highlight html %}
 
//To set enableMeasureGroups API value during initialization
$("#OlapClient").ejOlapClient({ enableMeasureGroups : true });

{% endhighlight %}


{% highlight html %}
 
//Get or set the enableMeasureGroups API, after initialization:
//Gets the enableMeasureGroups value  
$("#OlapClient").ejOlapClient("option","enableMeasureGroups");
                      
//Sets the enableMeasureGroups value 
$("#OlapClient").ejOlapClient("option","enableMeasureGroups", true ); 

{% endhighlight %}



### gridLayout `enum`
{:#members:gridlayout}

Sets the layout for OLAP Grid component inside OLAP Client.


#### Default Value

* ej.PivotGrid.Layout.Normal


#### Example

{% highlight html %}
 
//To set gridLayout API value during initialization
$("#OlapClient").ejOlapClient({ gridLayout: ej.PivotGrid.Layout.NoSummaries });

{% endhighlight %}


{% highlight html %}
 
//Get or set the gridLayout API, after initialization:
//Gets the gridLayout value  
$("#OlapClient").ejOlapClient("option","gridLayout");
                       
//Sets the gridLayout value 
$("#OlapClient").ejOlapClient("option","gridLayout", ej.PivotGrid.Layout.NormalTopSummary); 

{% endhighlight %}





### locale `string`
{:#members:locale}

Sets the localized language for the control.


#### Default Value

* "en-US"


#### Example

{% highlight html %}
 
//To set locale API value during initialization
$("#OlapClient").ejOlapClient({ locale: "en-US" });

{% endhighlight %}


{% highlight html %}
 
//Get or set the locale API, after initialization:
//Gets the locale value  
$("#OlapClient").ejOlapClient("option","locale");
                   
//Sets the locale value 
$("#OlapClient").ejOlapClient("option","locale", "fr-FR" ); 

{% endhighlight %}


### serviceMethodSettings `object`
{:#members:servicemethodsettings}

Allows the user to set custom name for the methods at service-end invoked on AJAX post.


#### Default Value

* null



#### Example

{% highlight html %}
 
//To set serviceMethodSettings API value, to invoke the appropriate service method on UI operation.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {initialize: "MyMethod"}});
 
 {% endhighlight %}


{% highlight html %}
 
//Gets or sets the serviceMethodSettings API, to invoke the appropriate service method on UI operation:
//Gets the serviceMethodSettings value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the serviceMethodSettings value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings",  {initialize: "MyMethod"} ); 

{% endhighlight %}



### serviceMethodSettings.cubeChanged `string`
{:#members:servicemethodsettings-cubechanged}

Allows the user to set the custom name for the service method that&rsquo;s responsible for updating entire report and control while changing the Cube.



#### Default Value

* "CubeChanged"


#### Example

{% highlight html %}
 
//To set cubeChanged API value, to invoke the corresponding service method for updating entire report and control while changing the Cube.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {cubeChanged: "CubeChangedMyMethod"}});
 
 {% endhighlight %}


{% highlight html %}
 
//Gets or sets the cubeChanged API, to invoke the corresponding service method for updating entire report and control while changing the Cube:
//Gets the cubeChanged value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the cubeChanged value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.cubeChanged","CubeChangedMyMethod" ); 

{% endhighlight %}




### serviceMethodSettings.exportOlapClient `string`
{:#members:servicemethodsettings-exportolapclient}

Allows the user to set the custom name for the service method that’s responsible for exporting operation.

#### Default Value

* "Export"

#### Example

{% highlight html %}
 
To set exportOlapClient API value to invoke the corresponding service method for exporting operation.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: { exportOlapClient: "Export"}});
 
{% endhighlight %}


{% highlight html %}
 
//Gets or sets the exportOlapClient API, to invoke the corresponding service method for exporting operation.

//Gets the exportOlapClient value
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the exportOlapClient value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings. exportOlapClient", "Export" );
 
{% endhighlight %}



### serviceMethodSettings.fetchMemberTreeNodes `string`
{:#members:servicemethodsettings-fetchmembertreenodes}

Allows the user to set the custom name for the service method that&rsquo;s responsible to get members for the tree-view inside member-editor dialog.



#### Default Value

* "FetchMemberTreeNodes"



#### Example

{% highlight html %}
 
//To set fetchMemberTreeNodes API value, to invoke the corresponding service method to get members for the tree-view inside member-editor dialog.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {fetchMemberTreeNodes: "FetchMemberTreeNodesMyMethod"}});
 
 {% endhighlight %}


{% highlight html %}
 
//Gets or sets the fetchMemberTreeNodes API, to invoke the corresponding service method to get members for the tree-view inside member-editor dialog:
//Gets the fetchMemberTreeNodes value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the fetchMemberTreeNodes value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.fetchMemberTreeNodes", "FetchMemberTreeNodesMyMethod" ); 

{% endhighlight %}


### serviceMethodSettings.fetchReportList `string`
{:#members:servicemethodsettings-fetchreportlist}

Allows the user to set the custom name for the service method that&rsquo;s responsible for fetching the report names from the database.


#### Default Value

* "FetchReportListFromDB"


#### Example

{% highlight html %}
                     
//To set fetchReportList API value, to invoke the corresponding service method that&rsquo;s responsible for fetching the report names from the database.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {fetchReportList: "FetchReportListFromDBMyMethod"}});
 
 {% endhighlight %}


{% highlight html %}
 
//Gets or sets the fetchReportList API, to invoke the corresponding service method that&rsquo;s responsible for fetching the report names from the database:
//Gets the fetchReportList value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the fetchReportList value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.fetchReportList", "FetchReportListFromDBMyMethod" );

 {% endhighlight %}



### serviceMethodSettings.filterElement `string`
{:#members:servicemethodsettings-filterelement}

Allows the user to set the custom name for the service method that&rsquo;s responsible for updating reports while filtering members.


#### Default Value

* "FilterElement"


#### Example

{% highlight html %}
 
//To set filterElement API value, to invoke the corresponding service method for performing server-side operation while filtering members.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {filterElement: "filterElementMyMethod"}});
 
 {% endhighlight %}


{% highlight html %}
 
//Get or set the filterElement API, to invoke the corresponding service method for performing server-side operation while filtering members:
//Gets the filterElement value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the filterElement value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.filterElement", "FilterElementMyMethod" ); 

{% endhighlight %}


### serviceMethodSettings.initialize `string`
{:#members:servicemethodsettings-initialize}

Allows the user to set the custom name for the service method that&rsquo;s responsible for initializing OLAP Client.

#### Default Value

* "InitializeClient"



#### Example

{% highlight html %}
 
//To set initialize API value, to invoke the corresponding service method for OLAP Client initialization.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {initialize: "InitializeClientMyMethod"});
 
 {% endhighlight %}


{% highlight html %}
 
//Gets or sets the initialize API, to invoke the corresponding service method for OLAP Client initialization:
//Gets the initialize value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the initialize value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.initialize", "InitializeClientMyMethod" );

 {% endhighlight %}


### serviceMethodSettings.loadReport `string`
{:#members:servicemethodsettings-loadreport}

Allows the user to set the custom name for the service method that&rsquo;s responsible for loading the report collection from database.



#### Default Value

* "LoadReportFromDB"


#### Example

{% highlight html %}
 
//To set loadReport API value, to invoke the corresponding service method that&rsquo;s responsible for loading the report collection from database.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {loadReport: "LoadReportFromDBMyMethod"}});
 
 {% endhighlight %}


{% highlight html %}
 
//Get or set the loadReport API, to invoke the corresponding service method that&rsquo;s responsible for loading the report from the database:
//Gets the loadReport value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the loadReport value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.loadReport", "LoadReportFromDBMyMethod"} ); 

{% endhighlight %}


### serviceMethodSettings.mdxQuery `string`
{:#members:servicemethodsettings-mdxquery}

Allows the user to set the custom name for the service method that’s responsible for retrieving the MDX query for the current report.

#### Default Value

* "GetMDXQuery"


#### Example

{% highlight html %}
 
//To set mdxQuery API value to invoke the corresponding service method for retrieving the MDX query for the current report.

$("#OlapClient").ejOlapClient({  serviceMethodSettings: {mdxQuery: "GetMDXQuery"}});

{% endhighlight %}

{% highlight html %}
 
//Gets or sets the mdxQuery API, to invoke the corresponding service method for retrieving the MDX query for the current report.
//Gets the mdxQuery value
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the mdxQuery value
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.mdxQuery", "GetMDXQuery"} ); 
 
{% endhighlight %}




### serviceMethodSettings.measureGroupChanged `string`
{:#members:servicemethodsettings-measuregroupchanged}

Allows the user to set the custom name for the service method that&rsquo;s responsible for updating cube browser tree while changing the measure group.


#### Default Value

* "MeasureGroupChanged"


#### Example

{% highlight html %}
 
//To set measureGroupChanged API value, to invoke the corresponding service method for updating the cube browser tree while changing the measure group.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {measureGroupChanged: "MeasureGroupChangedMyMethod"}});
 
 {% endhighlight %}


{% highlight html %}
 
//Gets or sets the measureGroupChanged API, to invoke the corresponding service method for updating the cube browser tree while changing the Measure group:
//Gets the measureGroupChanged value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the measureGroupChanged value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.measureGroupChanged","MeasureGroupChangedMyMethod" ); 

{% endhighlight %}


### serviceMethodSettings.memberExpand `string`
{:#members:servicemethodsettings-memberexpand}

Allows the user to set the custom name for the service method that&rsquo;s responsible to get the child members on node expand.


#### Default Value

* "MemberExpanded"


#### Example

{% highlight html %}
 
//To set memberExpand API value, to invoke the corresponding service method which would get the child members on node expand.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {memberExpand: "MemberExpandedMyMethod"}});
 
 {% endhighlight %}


{% highlight html %}
 
//Gets or sets the memberExpand API, to invoke the corresponding service method which would get the child members on node expand:
//Gets the memberExpand value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the memberExpand value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.memberExpand", "MemberExpandedMyMethod" ); 

{% endhighlight %}



### serviceMethodSettings.nodeDropped `string`
{:#members:servicemethodsettings-nodedropped}

Allows the user to set the custom name for the service method that&rsquo;s responsible for updating report while dropping a Node/SplitButton inside AxisElementBuilder.


#### Default Value

* "NodeDropped"



#### Example

{% highlight html %}
 
//To set nodeDropped API value, to invoke the corresponding service method for performing server-side operation while dropping a Node/SplitButton inside AxisElementBuilder.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {nodeDropped: "NodeDroppedMyMethod"}});
 
 {% endhighlight %}


{% highlight html %}
 
//Gets or sets the nodeDropped API, to invoke the corresponding service method for performing server-side operation while dropping a Node/SplitButton inside AxisElementBuilder:
//Gets the nodeDropped value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the nodeDropped value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.nodeDropped","NodeDroppedMyMethod"); 

{% endhighlight %}


### serviceMethodSettings.removeSplitButton `string`
{:#members:servicemethodsettings-removesplitbutton}

Allows the user to set the custom name for the service method that&rsquo;s responsible for updating report while removing SplitButton from AxisElementBuilder.



#### Default Value

* "RemoveSplitButton"


#### Example

{% highlight html %}
 
//To set removeSplitButton API value, to invoke the corresponding service method for performing server-side operation while removing SplitButton from the AxisElementBuilder.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {removeSplitButton: "RemoveSplitButtonMyMethod"}});
 
 {% endhighlight %}


{% highlight html %}
 
//Gets or sets the removeSplitButton API, to invoke the corresponding service method for performing server-side operation while removing SplitButton from the AxisElementBuilder:
//Gets the removeSplitButton value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the removeSplitButton value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.removeSplitButton", "RemoveSplitButtonMyMethod" );

 {% endhighlight %}


### serviceMethodSettings.saveReport `string`
{:#members:servicemethodsettings-savereport}

Allows the user to set the custom name for the service method that&rsquo;s responsible for saving the report collection to database.



#### Default Value

* "SaveReportToDB"


#### Example

{% highlight html %}
 
//To set saveReport API value, to invoke the corresponding service method which would save the report collection to database.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {saveReport: "SaveReportToDBMyMethod"}});
 
 {% endhighlight %}


{% highlight html %}
 
//Gets or sets the saveReport API, to invoke the corresponding service method which would save the report collection to database:
//Gets the saveReport value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the saveReport value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.saveReport", "SaveReportToDBMyMethod" ); 

{% endhighlight %}



### serviceMethodSettings.toggleAxis `string`
{:#members:servicemethodsettings-toggleaxis}

Allows the user to set the custom name for the service method that’s responsible for toggling the elements in row and column axes.

#### Default Value

* "ToggleAxis"


{% highlight html %}
 
//To set toggleAxis API value, inorder to invoke the corresponding service method for toggling row and column axes.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {toggleAxis: "ToggleAxis"}});

{% endhighlight %}


{% highlight html %}
 
//Gets or sets the toggleAxis API, to invoke the corresponding service method to toggle row and column axes.
//Gets the toggleAxis value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the toggleAxis value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.toggleAxis", "ToggleAxis"); 

{% endhighlight %}


### serviceMethodSettings.toolbarServices `string`
{:#members:servicemethodsettings-toolbarservices}

Allows the user to set the custom name for the service method that&rsquo;s responsible for any toolbar operation.


#### Default Value

* "ToolbarOperations"


#### Example

{% highlight html %}
 
//To set the toolbarServices API value, to invoke the corresponding service method responsible for any toolbar operation.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {toolbarServices: "ToolbarOperationsMyMethod"}});
 
 {% endhighlight %}


{% highlight html %}
 
//Gets or sets the toolbarServices API value, to invoke the corresponding service method responsible for any toolbar operation:
//Gets the toolbarServices value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the toolbarServices value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.toolbarServices", "ToolbarOperationsMyMethod"} ); 

{% endhighlight %}




### serviceMethodSettings.updateReport `string`
{:#members:servicemethodsettings-updatereport}

Allows the user to set the custom name for the service method that&rsquo;s responsible for updating report collection.


#### Default Value

* "UpdateReport"


#### Example

{% highlight html %}
 
//To set updateReport API value, to invoke the corresponding service method that&rsquo;s responsible for updating the report collection and current report.
 $("#OlapClient").ejOlapClient({  serviceMethodSettings: {updateReport: "UpdateReportFromMyMethod"}});
 
 {% endhighlight %}


{% highlight html %}
 
//Get or set the updateReport API, to invoke the corresponding service method that&rsquo;s responsible for updating the current report and report collection:
//Gets the updateReport value  
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings");
   
//Sets the updateReport value 
$("#OlapClient").ejOlapClient("option", "serviceMethodSettings.updateReport", "UpdateReportFromMyMethod"} ); 

{% endhighlight %}



### title `string`
{:#members:title}

Sets the title for OLAP Client.


#### Default Value

* null


#### Example

{% highlight html %}
 
//To set title API value during initialization
$("#OlapClient").ejOlapClient({ title: "Olap Browser" });

{% endhighlight %}


{% highlight html %}
 
//Get or set the title API, after initialization:
//Gets the title value  
$("#OlapClient").ejOlapClient("option","title");
                    
//Sets the title value 
$("#OlapClient").ejOlapClient("option","title", "Olap Browser" );

 {% endhighlight %}


### url `string`
{:#members:url}

Connects the service using the specified URL for any server updates.



#### Default Value

* null


#### Example

{% highlight html %}
 
//To set url value during initialization
$("#OlapClient").ejOlapClient({ url: "/wcf/OlapClientService.svc" });

{% endhighlight %}


{% highlight html %}
 
//Get or set the url, after initialization:
//Gets the url value  
$("#OlapClient").ejOlapClient("option","url");
                      
//Sets the url value 
$("#OlapClient").ejOlapClient("option","url", "/wcf/OlapClientService.svc" ); 

{% endhighlight %}



## Methods


### chartDrillSuccess()
{:#methods:chartdrillsuccess}

This function is used to drill down the OLAP Grid widget once OLAP Chart drill down.


#### Example

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
</script>

{% endhighlight %}



### cubeChanged()
{:#methods:cubechanged}

This function is raised while changing the cube.


#### Example

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
</script>

{% endhighlight %}



### doAjaxPost()
{:#methods:doajaxpost}

Perform an asynchronous HTTP (Ajax) request.


#### Example

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
</script>

{% endhighlight %}


### doPostBack(url, params)
{:#methods:dopostback}

Perform an asynchronous HTTP (FullPost) submit.

#### Example

{% highlight html %}

<div id="OlapClient"></div> 
 
<script>
// Create OLAP Client
$('#OlapClient').ejOlapClient({
      url: "OlapClientService.svc"
  });
var clientObj = $("#OlapClient").data("ejOlapClient");//Initiates the instance
clientObj.doPostBack("/OlapClientService.svc/Initialize", {"key", "Hello World"});
</script>

{% endhighlight %}




### getAxisPosition()
{:#methods:getaxisposition}

This function is used to get the position of the axis element builders.

#### Example

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
</script>

{% endhighlight %}



### gridDrillSuccess()
{:#methods:griddrillsuccess}

This function is used to drill down the OLAP Chart widget once OLAP Grid component drill down.



#### Example

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
</script>

{% endhighlight %}




### nodeDropped()
{:#methods:nodedropped}

This function is used to perform required action after dropping a tree node in Axis Element builder.



#### Example

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
</script>

{% endhighlight %}



### onDropped()
{:#methods:ondropped}

This function is raised after dropping the element in Axis Element Builder.



#### Example

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
</script>

{% endhighlight %}



### onTabClick()
{:#methods:ontabclick}

This function is raised while tab changes.


#### Example

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
</script>

{% endhighlight %}




### reportChanged()
{:#methods:reportchanged}

This function is raised while changing the report.



#### Example

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
</script>

{% endhighlight %}



### setSplitBtnTargetPos()
{:#methods:setsplitbtntargetpos}

This function is used to set the position to currently dropped split button in respective axes.


#### Example

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
</script>

{% endhighlight %}




## Events


### afterServiceInvoke
{:#events:afterserviceinvoke}

Fires after the service is invoked.

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
<td class="description">Event parameters from OLAP Client component.
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
<td class="description">return the current action of OLAP Client control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">return the custom object bounds with OLAP Client control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">return the outer HTML of OLAP Client control.</td>
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
<td class="description">returns the OLAP Client model.</td>
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
 
//afterServiceInvoke event
$("#OlapClient").ejOlapClient({
    afterServiceInvoke: function(args) {}
});

{% endhighlight %}



### beforeServiceInvoke
{:#events:beforeserviceinvoke}

Fires when the summary cell is clicked.

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
<td class="description">Event parameters from OLAP Client component.
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
<td class="description">return the current action of OLAP Client control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">return the custom object bounds with OLAP Client control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">return the outer HTML of OLAP Client control.</td>
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
<td class="description">returns the OLAP Client model.</td>
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
 
//beforeServiceInvoke event
$("#OlapClient").ejOlapClient({
    beforeServiceInvoke: function(args) {}
});

{% endhighlight %}



### chartLoad
{:#events:chartload}


Fires before rendering the chart

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
<td class="description">Event parameters from OLAP Chart component.
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
<td class="description">return the current action of OLAP Chart control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">return the custom object bounds with OLAP Chart control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">return the outer HTML of OLAP Chart control.</td>
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
<td class="description">returns the OLAP Chart model.</td>
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
 
//event triggered when OLAP Chart begins rendering.
$("#OlapClient").ejOlapClient({
   chartLoad: function (args) {}
});      

{% endhighlight %}



### load
{:#events:load}


Fires on loading the control

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
<td class="description">Event parameters from OLAP Client component.
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
<td class="description">returns the outer HTML of OLAP Client component.</td>
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
<td class="description">returns the OLAP Client model.</td>
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
 
//event triggered on loading the control
$("#OlapClient").ejOlapClient({
   load: function (args) {}
});     

{% endhighlight %}



### renderComplete
{:#events:rendercomplete}


Fires on completion of rendering control

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
<td class="description">Event parameters from OLAP Client component
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
customObject{% endhighlight %}</td>
<td class="type">Object</td>
<td class="description">returns the custom object bounded with the control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the outer HTML of OLAP Client control.</td>
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
<td class="description">returns the OLAP Client model.</td>
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
 
//event triggered after completing rendering the control
$("#OlapClient").ejOlapClient({
   renderComplete: function (args) {}
});     

{% endhighlight %}



### renderFailure
{:#events:renderfailure}

Fires when error occured in rendering the control

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
<td class="description">Event parameters from OLAP Client component
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
customObject{% endhighlight %}</td>
<td class="type">Object</td>
<td class="description">returns the custom object bounded with the control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the outer HTML of OLAP Client control.</td>
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
<td class="description">returns the OLAP Client model.</td>
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
 
//event triggered when error occurs in rendering the control
$("#OlapClient").ejOlapClient({
   renderFailure: function (args) {}
});     

{% endhighlight %}



### renderSuccess
{:#events:rendersuccess}

Fires when the control is rendered success

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
<td class="description">Event parameters from OLAP Client component.
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
customObject{% endhighlight %}</td>
<td class="type">Object</td>
<td class="description">returns the custom object bounded with the control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the outer HTML of OLAP Client control.</td>
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
<td class="description">returns the OLAP Client model.</td>
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
 
//success event for rendering the control
$("#OlapClient").ejOlapClient({
   renderSuccess: function (args) {}
});      

{% endhighlight %}




