---
layout: post
title: ejPivotGrid
documentation: API
platform: js
keywords: ejPivotGrid, API, Essential JS PivotGrid
metaname: 
metacontent: 
---

# PivotGrid

Custom Design for Pivot Grid control.


#### Syntax

{% highlight js %}

$(element).ejPivotGrid()

{% endhighlight %}


#### Example

{% highlight html %}
 
<div id="PivotGrid"> </div> 
 
<script>
// Create Pivot Grid
$("#PivotGrid").ejPivotGrid(...);       
</script>

{% endhighlight %}


#### Requires

* module:jquery-1.10.2.min.js
* module:jquery.easing.1.3.min.js
* module:ej.core.js
* module:ej.data.js
* module:ej.touch.js
* module:ej.waitingpopup.js
* module:ej.pivotgrid.js
* module:ej.pivotpager.js


## Members


### cssClass `string`
{:#members:cssclass}

Sets the CSS name for custom operation.


#### Default Value

* ""


#### Example

{% highlight html %}
 
//To set the CSS name during initialization  
$("#PivotGrid").ejPivotGrid({cssClass: "gradient-lime"});       

{% endhighlight %}


{% highlight html %}
 
//Get or set css class for initialization:
// Gets the css name.           
$("#PivotGrid").ejPivotGrid("option", "cssClass");                      
// Sets the rounded corner to button
$("#PivotGrid").ejPivotGrid("option", "cssClass",  "gradient-lime" );           

{% endhighlight %}

### currentReport `string`
{:#members:currentreport}

Contains the serialized OlapReport at the instant.



#### Default Value

* ""


### customObject `object`
{:#members:customobject}

Custom object to pass additional information between client-end and service-end.



#### Default Value

* null


#### Example

{% highlight html %}
 
// To pass additional information between client-end and service-end   
$("#PivotGrid").ejPivotGrid({customObject: { Language: "en-US" }}); 

{% endhighlight %}


{% highlight html %}
 
//Get or set the custom object API, after initialization:
//Gets the custom object value  
$("#PivotGrid").ejPivotGrid("option","customObject");
                       
//Sets the custom object value 
$("#PivotGrid").ejPivotGrid("option","customObject", {Language: "en-US"} );             

{% endhighlight %}


### enableCellContext `boolean`
{:#members:enablecellcontext}

Allows the user to access/operate each cell through a custom design on right click.



#### Default Value

* false



#### Example

{% highlight html %}
 
//To set the cell context option during initialization  
$("#PivotGrid").ejPivotGrid({enableCellContext: true});

{% endhighlight %}


{% highlight html %}
 
//Get or set the cell context, after initialization:
//Gets the cell context state
$("#PivotGrid").ejPivotGrid("option", "enableCellContext");
                 
//Sets the cell context value
$("#PivotGrid").ejPivotGrid("option", "enableCellContext","true"); 

{% endhighlight %}



### enableJSONRendering `boolean`
{:#members:enablejsonrendering}

Allows the user to load PivotGrid using JSON data.


#### Default Value

* false



#### Example

{% highlight html %}
 
//To enable the direct JSONRendering during initialization  
$("#PivotGrid").ejPivotGrid({enableJSONRendering: true});

{% endhighlight %}


{% highlight html %}
 
//Get or set the JSON Rendering, after initialization:
//Gets the JSON rendering state
$("#PivotGrid").ejPivotGrid("option", "enableJSONRendering");
               
//Sets the JSON rendering 
$("#PivotGrid").ejPivotGrid("option", "enableJSONRendering","true"); 

{% endhighlight %}



### enableRTL `boolean`
{:#members:enablertl}

Allows the user to enable RTL support.


#### Default Value

* false



#### Example


{% highlight html %}
 
//To set the enableRTL option during initialization  
$("#PivotGrid").ejPivotGrid({enableRTL: true});

{% endhighlight %}


{% highlight html %}
 
//Get or set the enableRTL, after initialization:
//Gets the enableRTL values state
$("#PivotGrid").ejPivotGrid("option", "enableRTL");
                 
//Sets the cell context value
$("#PivotGrid").ejPivotGrid("option", "enableRTL","true"); 

{% endhighlight %}



### enableToolTip `boolean`
{:#members:enabletooltip}

Allows the user to enable ToolTip support.


#### Default Value

* false



#### Example

{% highlight html %}
 
//To set the enableToolTip option during initialization  
$("#PivotGrid").ejPivotGrid({enableToolTip: true});

{% endhighlight %}


{% highlight html %}
 
//Get or set the enableToolTip, after initialization:
//Gets the enableToolTip values state
$("#PivotGrid").ejPivotGrid("option", "enableToolTip");
                     
//Sets the cell context value
$("#PivotGrid").ejPivotGrid("option", "enableToolTip","true"); 

{% endhighlight %}



### enableVirtualScrolling `boolean`
{:#members:enablevirtualscrolling}

Allows the user to load large amount of data into pages.


#### Default Value

* false


#### Example

{% highlight html %}
 
//To set the virtual scrolling during initialization  
$("#PivotGrid").ejPivotGrid({enableVirtualScrolling: true});

{% endhighlight %}


{% highlight html %}
 
//Get or set the virtual scrolling, after initialization:
//Gets the virtual calling state
$("#PivotGrid").ejPivotGrid("option", "enableVirtualScrolling");
            
//Sets the virtual scrolling 
$("#PivotGrid").ejPivotGrid("option", "enableVirtualScrolling","true");
{% endhighlight %}




### hyperlinkSettings `object`
{:#members:hyperlinksettings}

Allows the user to configure hyperlink settings to Pivot Grid control.



#### Default Value

* null


#### Example

{% highlight html %}
 
//To configure the hyperlink settings to Pivot Grid during initialization  
$("#PivotGrid").ejPivotGrid({hyperlinkSettings:{enableValueCellHyperlink: true, enableRowHeaderHyperlink: true}});

{% endhighlight %}


{% highlight html %}
 
//Get or set the hyperlink settings, after initialization:
//Gets the hyperlink settings
$("#PivotGrid").ejPivotGrid("option", "hyperlinkSettings");
                 
//Sets the hyperlink settings to Pivot Grid
$("#PivotGrid").ejPivotGrid("option", "hyperlinkSettings", {enableValueCellHyperlink: true, enableRowHeaderHyperlink: true}); 

{% endhighlight %}



### hyperlinkSettings.enableColumnHeaderHyperlink `boolean`
{:#members:hyperlinksettings-enablecolumnheaderhyperlink}

Allows the user to enable/diable hyperlink for column header.


#### Default Value

* false


#### Example

{% highlight html %}
 
//To set the Hyperlink option for column header during initialization  
$("#PivotGrid").ejPivotGrid({hyperlinkSettings:{enableColumnHeaderHyperlink: true}});

{% endhighlight %}


{% highlight html %}
 
//Get or set the hyper link for column header, after initialization:
//Gets the hyper link state
$("#PivotGrid").ejPivotGrid("option", "hyperlinkSettings");
                                 
//Sets the column header hyper link state
$("#PivotGrid").ejPivotGrid("option", "hyperlinkSettings.enableColumnHeaderHyperlink","true"); 

{% endhighlight %}



### hyperlinkSettings.enableRowHeaderHyperlink `boolean`
{:#members:hyperlinksettings-enablerowheaderhyperlink}

Allows the user to enable/diable hyperlink for row header.



#### Default Value

* false


#### Example

{% highlight html %}
 
//To set the Hyperlink option for row header during initialization  
$("#PivotGrid").ejPivotGrid({hyperlinkSettings:{enableRowHeaderHyperlink: true}});

{% endhighlight %}


{% highlight html %}
 
//Get or set the hyper link for row header, after initialization:
//Gets the row header hyperlink state
$("#PivotGrid").ejPivotGrid("option", "hyperlinkSettings");
         
//Sets the row header hyperlink
$("#PivotGrid").ejPivotGrid("option", "hyperlinkSettings.enableRowHeaderHyperlink","true");

 {% endhighlight %}



### hyperlinkSettings.enableSummaryCellHyperlink `boolean`
{:#members:hyperlinksettings-enablesummarycellhyperlink}

Allows the user to enable/diable hyperlink for summary cells.



#### Default Value

* false


#### Example

{% highlight html %}
 
//To set the Hyperlink option for summary cell during initialization  
$("#PivotGrid").ejPivotGrid({hyperlinkSettings:{enableSummaryCellHyperlink: true}});

{% endhighlight %}


{% highlight html %}
 
//Get or set the hyper link for summary cell, after initialization:
//Gets the summary cell hyperlink state
$("#PivotGrid").ejPivotGrid("option", "hyperlinkSettings");
               
//Sets the summary cell hyperlink 
$("#PivotGrid").ejPivotGrid("option", "hyperlinkSettings.enableSummaryCellHyperlink","true");

{% endhighlight %}




### hyperlinkSettings.enableValueCellHyperlink `boolean`
{:#members:hyperlinksettings-enablevaluecellhyperlink}

Allows the user to enable/diable hyperlink for value cells.



#### Default Value

* false


#### Example

{% highlight html %}
 
//To set the Hyperlink option for value cell during initialization  
$("#PivotGrid").ejPivotGrid({hyperlinkSettings:{enableValueCellHyperlink: true}});

{% endhighlight %}


{% highlight html %}
 
//Get or set the hyper link for cell, after initialization:
//Gets the hyper link state
$("#PivotGrid").ejPivotGrid("option", "hyperlinkSettings");
                 
//Sets the cell hyperlink value
$("#PivotGrid").ejPivotGrid("option", "hyperlinkSettings.enableValueCellHyperlink","true");

{% endhighlight %}


### isResponsive `boolean`
{:#members:isresponsive}

Allows the user to enable Responsive layout support.



#### Default Value

* false


#### Example

{% highlight html %}
 
//To set the isResponsive option during initialization  
$("#PivotGrid").ejPivotGrid({isResponsive: true});

{% endhighlight %}


{% highlight html %}
 
//Get or set the isResponsive, after initialization:
//Gets the isResponsive values state
$("#PivotGrid").ejPivotGrid("option", "isResponsive");
                      
//Sets the reponsive layout
$("#PivotGrid").ejPivotGrid("option", "isResponsive","true"); 

{% endhighlight %}



### jsonRecords `string`
{:#members:jsonrecords}

Contains the serialized JSON string which renders PivotGrid.


#### Default Value

* ""



### layout `enum`
{:#members:layout}

Allows the user access the different layouts for Pivot Grid.


#### Default Value

* ej.PivotGrid.Layout.Normal


#### Example

{% highlight html %}
 
//To set the layout during initialization  
$("#PivotGrid").ejPivotGrid({layout: ej.PivotGrid.Layout.NoSummaries});

{% endhighlight %}


{% highlight html %}
 
//Get or set the grid layout, after initialization:
//Gets the layout value
$("#PivotGrid").ejPivotGrid("option", "layout");
                    
//Sets the grid layout
$("#PivotGrid").ejPivotGrid("option", "layout",ej.PivotGrid.Layout.Normal); 

{% endhighlight %}



### locale `string`
{:#members:locale}

Sets the localized language for the control.


#### Default Value

* "en-US"


#### Example

{% highlight html %}
 
//Sets the localized language    
$("#PivotGrid").ejPivotGrid({locale: "en-US"}}); 

{% endhighlight %}


{% highlight html %}
 
//Get or set the size API, after initialization:
//Gets the localization value  
$("#PivotGrid").ejPivotGrid("option","locale");
                     
//Sets the localization value 
$("#PivotGrid").ejPivotGrid("option","locale", "en-US" );

{% endhighlight %}



### serviceMethodSettings `object`
{:#members:servicemethodsettings}

Allows the user to set custom name for the methods at service-end invoked on AJAX post.


#### Default Value

* {}


#### Example

{% highlight html %}
 
//To set serviceMethodSettings API value, to invoke the appropriate service method on UI operation.
$("#PivotGrid").ejPivotGrid({ servieMethods.initialize: "InitializeGrid" });

{% endhighlight %}


{% highlight html %}
 
//Gets or sets the serviceMethodSettings API, to invoke the appropriate service method on UI operation:
//Gets the serviceMethodSettings value   
$("#PivotGrid").ejPivotGrid("option", "serviceMethodSettings");
                                             
//Sets the serviceMethodSettings value                          
$("#PivotGrid").ejPivotGrid("option", "serviceMethodSettings",  {initialize: "InitializeGrid"} ); 

{% endhighlight %}




### serviceMethodSettings.drillDown `string`
{:#members:servicemethodsettings-drilldown}

Allows the user to set the custom name for the service method that&#39;s responsible for drilling up/down operation in Pivot Grid.



#### Default Value

* "DrillGrid"


#### Example

{% highlight html %}
 
//To set drillDown API value, to invoke the corresponding service method for performing server-side operation while drilling up/down in Pivot Grid.   
$("#PivotGrid").ejPivotGrid({ serviceMethodSettings: { drillDown: "DrillGridMyMethod" } });

{% endhighlight %}


{% highlight html %}
 
//Get or set the drillDown API, to invoke the corresponding service method for performing server-side operation while drilling up/down in Pivot Grid:
//Gets the drillDown value   
$("#PivotGrid").ejPivotGrid("option", "serviceMethodSettings");
                                             
//Sets the drillDown value                      
$("#PivotGrid").ejPivotGrid("option", "serviceMethodSettings.drillDown", "DrillGridMyMethod"} );

 {% endhighlight %}



### serviceMethodSettings.exportOptions `string`
{:#members:servicemethodsettings-exportoptions}

Allows the user to set the custom name for the service method that&#39;s responsible for performing exporting operation in Pivot Grid.


#### Default Value

* "ExportOptions"


#### Example

{% highlight html %}
 
//To set exportOptions API value, to invoke the corresponding service method for performing server-side operation while exporting.  
$("#PivotGrid").ejPivotGrid({ serviceMethodSettings: { exportOptions: "ExportOptionsMyMethod" } });

{% endhighlight %}


{% highlight html %}
 
//Gets or sets the exportOptions API, to invoke the corresponding service method for performing server-side operation while exporting.:
//Gets the exportOptions value   
$("#PivotGrid").ejPivotGrid("option", "serviceMethodSettings");
                                             
//Sets the exportOptions value                          
$("#PivotGrid").ejPivotGrid("option", "serviceMethodSettings.exportOptions", "ExportOptionsMyMethod");

 {% endhighlight %}




### serviceMethodSettings.initialize `string`
{:#members:servicemethodsettings-initialize}

Allows the user to set the custom name for the service method that&#39;s responsible for initializing Pivot Grid.


#### Default Value

* "InitializeGrid"


#### Example

{% highlight html %}
 
//To set initialize API value, to invoke the corresponding service method for Pivot Grid initialization.
$("#PivotGrid").ejPivotGrid({ servieMethods",  {initialize: "InitializeGrid"} );

 {% endhighlight %}


{% highlight html %}
 
//Gets or sets the initialize API, to invoke the corresponding service method for Pivot Grid initialization:
//Gets the initialize value   
$("#PivotGrid").ejPivotGrid("option", "serviceMethodSettings");
                                             
//Sets the initialize value                     
$("#PivotGrid").ejPivotGrid("option", "serviceMethodSettings.initialize", "InitializeGrid" ); 

{% endhighlight %}




### serviceMethodSettings.paging `string`
{:#members:servicemethodsettings-paging}

Allows the user to set the custom name for the service method that&#39;s responsible for performing paging operation in Pivot Grid.


#### Default Value

* "Paging"


#### Example

{% highlight html %}
 
//To set paging API value, to invoke the corresponding service method for performing server-side operation during paging in Pivot Grid.  
$("#PivotGrid").ejPivotGrid({ serviceMethodSettings: { paging: "PagingMyMethod" } });

{% endhighlight %}


{% highlight html %}
 
//Gets or sets the paging API, to invoke the corresponding service method for performing server-side operation during paging in Pivot Grid:
//Gets the paging value   
$("#PivotGrid").ejPivotGrid("option", "serviceMethodSettings");
                                             
//Sets the paging value                         
$("#PivotGrid").ejPivotGrid("option", "serviceMethodSettings.paging",  "PagingMyMethod"); 

{% endhighlight %}



### url `string`
{:#members:url}

Connects the service using the specified URL for any server updates. See url


#### Default Value

* ""


#### Example

{% highlight html %}
 
//To set service url during initialization  
$("#PivotGrid").ejPivotGrid({url: "/wcf/PivotGridService.svc"});

{% endhighlight %}


{% highlight html %}
 
//Get or set the size API, after initialization:
//Gets the url value  
$("#PivotGrid").ejPivotGrid("option","url");
   
//Sets the url value 
$("#PivotGrid").ejPivotGrid("option","url", "/wcf/PivotGridService.svc" ); 

{% endhighlight %}


## Methods


### doAjaxPost()
{:#methods:doajaxpost}

Perform an asynchronous HTTP (Ajax) request.


#### Example

{% highlight html %}
 
<div id="PivotGrid"></div> 
 
<script>
// Create Pivot Grid
$('#PivotGrid').ejPivotGrid({
      url: "PivotGridService.svc",
  });
var gridObj = $("#PivotGrid").data("ejPivotGrid");
gridObj.doAjaxPost("POST", "/PivotGridService.svc/Initialize", {"key", "Hello World"}, "_renderControlSuccess", null);
// Initiate an Ajax request.
</script>

{% endhighlight %}



### doPostBack()
{:#methods:dopostback}

Perform an asynchronous HTTP (FullPost) submit.


#### Example

{% highlight html %}
 
<div id="PivotGrid"></div> 
 
<script>
// Submitting required informatin to the service.
$('#PivotGrid').ejPivotGrid({
      url: "PivotGridService.svc",
  });
var gridObj = $("#PivotGrid").data("ejPivotGrid");
gridObj.doPostBack("/PivotGridService.svc/Initialize", {"key", "Hello World"});
// Initiate an submit.
</script>

{% endhighlight %}


### refreshPagedPivotGrid()
{:#methods:refreshpagedpivotgrid}

This function re-renders the Pivot Grid on clicking the navigating buttons on Pivot Pager.


#### Example

{% highlight html %}
 
<div id="PivotGrid"></div> 
 
<script>
// Refreshing Pivot Grid while perform paging.
$('#PivotGrid').ejPivotGrid({
      url: "PivotGridService.svc",
  });
var gridObj = $("#PivotGrid").data("ejPivotGrid");
gridObj.refreshPagedPivotGrid("series", 2);
// Initiate an Ajax request.
</script>

{% endhighlight %}

### renderControlFromJSON()
{:#methods:rendercontrolfromjson}

This function receives the JSON formatted datasource to render the Pivot Grid control.

#### Example

{% highlight html %}
 
<div id="PivotGrid"></div> 
 
<script>
// Rendering Pivot Grid from given JSON formatted data.
$('#PivotGrid').ejPivotGrid({
      url: "PivotGridService.svc",
  });
var gridObj = $("#PivotGrid").data("ejPivotGrid");
gridObj.renderControlFromJSON({this.getJSONRecords()});
// Rendering Pivot Grid.
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
<td class="description">Event parameters from Pivot Grid
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
<td class="description">return the current action of Pivot Grid control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">return the custom object bounds with Pivot Grid control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">return the outer HTML of Pivot Grid control.</td>
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
<td class="description">returns the Pivot Grid model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
//afterServiceInvoke event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   afterServiceInvoke: function (args) {}
});     

{% endhighlight %}


### beforeServiceInvoke
{:#events:beforeserviceinvoke}

Fires before service invoked.

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
<td class="description">Event parameters from Pivot Grid
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
<td class="description">return the current action of Pivot Grid control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">return the custom object bounds with Pivot Grid control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">return the outer HTML of Pivot Grid control.</td>
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
<td class="description">returns the Pivot Grid model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
//beforeServiceInvoke event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   beforeServiceInvoke: function (args) {}
});      

{% endhighlight %}



### cellContext
{:#events:cellcontext}

Fires when the cell is right clicked.

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
<td class="description">Event parameters from Pivot Grid.
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
args{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">returns the original event args.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellPosition{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the cell position (row index and column index) in table.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellType{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the type of the cell.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
rowData{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the seriealized data of the header cells.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
uniqueName{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the unique name of levels/members.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
//cellContext event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   cellContext: function (args) {}
});      

{% endhighlight %}


### columnHeaderHyperlinkClick
{:#events:columnheaderhyperlinkclick}

Fires when the column header cell is clicked once if Pivot Grid enabled with hyperlink.

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
<td class="description">Event parameters from Pivot Grid.
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
args{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">returns the original event args.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellPosition{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the cell position (row index and column index) in table.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellType{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the type of the cell.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
rowData{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the seriealized data of the header cells.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
uniqueName{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the unique name of levels/members.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
//columnHeaderHyperlinkClick event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   columnHeaderHyperlinkClick: function (args) {}
});      

{% endhighlight %}


### drillSuccess
{:#events:drillsuccess}

Fires after drill down of Pivot Grid.

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
<td class="description">Event parameters from Pivot Grid
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
<td class="description">returns the Pivot Grid model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



#### Example

{% highlight html %}
 
//drillSuccess event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   drillSuccess: function (args) {}
});      

{% endhighlight %}



### load
{:#events:load}

Fires when Pivot Grid Start loading.

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
<td class="description">Event parameters from Pivot Grid.
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
args{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">returns the original event args.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
action{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the current action of Pivot Grid control.</td>
</tr>
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
<td class="description">returns the HTML of Pivot Grid control.</td>
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
<td class="description">returns the Pivot Grid model.</td>
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
 
//load event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   load: function (args) {}
});      

{% endhighlight %}



### renderComplete
{:#events:rendercomplete}

Fires when Pivot Grid completely finished its rendering.

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
<td class="description">Event parameters from Pivot Grid.
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
args{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">returns the original event args.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
action{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the current action of Pivot Grid control.</td>
</tr>
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
<td class="description">returns the HTML of Pivot Grid control.</td>
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
<td class="description">returns the Pivot Grid model.</td>
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
 
//renderComplete event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   renderComplete: function (args) {}
});      

{% endhighlight %}




### renderFailure
{:#events:renderfailure}

Fires while any discrepancies occurs during the rendering time.

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
<td class="description">Event parameters from Pivot Grid.
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
args{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">returns the original event args.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
action{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the current action of Pivot Grid control.</td>
</tr>
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
<td class="description">returns the HTML of Pivot Grid control.</td>
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
<td class="description">returns the Pivot Grid model.</td>
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
 
//renderFailure event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   renderFailure: function (args) {}
});      

{% endhighlight %}




### renderSuccess
{:#events:rendersuccess}

Fires when Pivot Grid successfully finished its rendering.

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
<td class="description">Event parameters from Pivot Grid.
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
args{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">returns the original event args.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
action{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the current action of Pivot Grid control.</td>
</tr>
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
<td class="description">returns the HTML of Pivot Grid control.</td>
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
<td class="description">returns the Pivot Grid model.</td>
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
 
//renderSuccess event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   renderSuccess: function (args) {}
});      

{% endhighlight %}




### rowHeaderHyperlinkClick
{:#events:rowheaderhyperlinkclick}

Fires when the row header cell is clicked once if Pivot Grid enabled with hyperlink.

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
<td class="description">Event parameters from Pivot Grid.
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
args{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">returns the original event args.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellPosition{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the cell position (row index and column index) in table.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellType{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the type of the cell.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
rowData{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the seriealized data of the header cells.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
uniqueName{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the unique name of levels/members.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



#### Example

{% highlight html %}
 
//rowHeaderHyperlinkClick event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   rowHeaderHyperlinkClick: function (args) {}
});      

{% endhighlight %}




### summaryCellHyperlinkClick
{:#events:summarycellhyperlinkclick}

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
<td class="description">Event parameters from Pivot Grid.
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
args{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">returns the original event args.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellPosition{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the cell position (row index and column index) in table.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellType{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the type of the cell.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
rowData{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the seriealized data of the header cells.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
uniqueName{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the unique name of levels/members.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



#### Example

{% highlight html %}
 
//summaryCellHyperlinkClick event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   summaryCellHyperlinkClick: function (args) {}
});      

{% endhighlight %}



### valueCellHyperlinkClick
{:#events:valuecellhyperlinkclick}

Fires when the value cell is clicked once if Pivot Grid enabled with hyperlink.

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
<td class="description">Event parameters from Pivot Grid.
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
args{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">returns the original event args.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellPosition{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the cell position (row index and column index) in table.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellType{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the type of the cell.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
rowData{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the seriealized data of the header cells.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
uniqueName{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the unique name of levels/members.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
//valueCellHyperlinkClick event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   valueCellHyperlinkClick: function (args) {}
});      

{% endhighlight %}

