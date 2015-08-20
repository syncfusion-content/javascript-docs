---
layout: post
title: ejPivotGrid
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Pivot Grid control.










$(element).ejPivotGrid<span class="signature">()</span>











Example
{:.example}


{% highlight html %}
 
<div id="PivotGrid"> </div> 
 
<script>
// Create Pivot Grid
$("#PivotGrid").ejPivotGrid(...);       
</script>{% endhighlight %}







Requires
{:.require}




* module:jquery-1.10.2.min.js


* module:jquery.easing.1.3.min.js


* module:ej.core.js


* module:ej.data.js


* module:ej.touch.js


* module:ej.waitingpopup.js


* module:ej.pivotgrid.js


* module:ej.pivotpager.js




## Members








### cssClass<span class="type-signature type string">String</span>
{:#members:cssclass}








Sets the CSS name for custom operation.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
//To set the CSS name during initialization  
$("#PivotGrid").ejPivotGrid({cssClass: "gradient-lime"});       {% endhighlight %}


{% highlight html %}
 
//Get or set css class for initialization:
// Gets the css name.           
$("#PivotGrid").ejPivotGrid("option", "cssClass");                      
// Sets the rounded corner to button
$("#PivotGrid").ejPivotGrid("option", "cssClass",  "gradient-lime" );           {% endhighlight %}







### currentReport<span class="type-signature type string">String</span>
{:#members:currentreport}








Contains the serialized OlapReport at the instant.




Default Value:
{:.param}






* ""














### customObject<span class="type-signature type object">Object</span>
{:#members:customobject}








Custom object to pass additional information between client-end and service-end.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
// To pass additional information between client-end and service-end   
$("#PivotGrid").ejPivotGrid({customObject: { Language: "en-US" }}); {% endhighlight %}


{% highlight html %}
 
//Get or set the custom object API, after initialization:
//Gets the custom object value  
$("#PivotGrid").ejPivotGrid("option","customObject");
                       
//Sets the custom object value 
$("#PivotGrid").ejPivotGrid("option","customObject", {Language: "en-US"} );             {% endhighlight %}







### enableCellContext<span class="type-signature type boolean">Boolean</span>
{:#members:enablecellcontext}








Allows the user to access/operate each cell through a custom design on right click.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
//To set the cell context option during initialization  
$("#PivotGrid").ejPivotGrid({enableCellContext: true});{% endhighlight %}


{% highlight html %}
 
//Get or set the cell context, after initialization:
//Gets the cell context state
$("#PivotGrid").ejPivotGrid("option", "enableCellContext");
                 
//Sets the cell context value
$("#PivotGrid").ejPivotGrid("option", "enableCellContext","true"); {% endhighlight %}







### enableJSONRendering<span class="type-signature type boolean">Boolean</span>
{:#members:enablejsonrendering}








Allows the user to load PivotGrid using JSON data.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
//To enable the direct JSONRendering during initialization  
$("#PivotGrid").ejPivotGrid({enableJSONRendering: true});{% endhighlight %}


{% highlight html %}
 
//Get or set the JSON Rendering, after initialization:
//Gets the JSON rendering state
$("#PivotGrid").ejPivotGrid("option", "enableJSONRendering");
               
//Sets the JSON rendering 
$("#PivotGrid").ejPivotGrid("option", "enableJSONRendering","true"); {% endhighlight %}







### enableRTL<span class="type-signature type boolean">Boolean</span>
{:#members:enablertl}








Allows the user to enable RTL support.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
//To set the enableRTL option during initialization  
$("#PivotGrid").ejPivotGrid({enableRTL: true});{% endhighlight %}


{% highlight html %}
 
//Get or set the enableRTL, after initialization:
//Gets the enableRTL values state
$("#PivotGrid").ejPivotGrid("option", "enableRTL");
                 
//Sets the cell context value
$("#PivotGrid").ejPivotGrid("option", "enableRTL","true"); {% endhighlight %}







### enableToolTip<span class="type-signature type boolean">Boolean</span>
{:#members:enabletooltip}








Allows the user to enable ToolTip support.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
//To set the enableToolTip option during initialization  
$("#PivotGrid").ejPivotGrid({enableToolTip: true});{% endhighlight %}


{% highlight html %}
 
//Get or set the enableToolTip, after initialization:
//Gets the enableToolTip values state
$("#PivotGrid").ejPivotGrid("option", "enableToolTip");
                     
//Sets the cell context value
$("#PivotGrid").ejPivotGrid("option", "enableToolTip","true"); {% endhighlight %}







### enableVirtualScrolling<span class="type-signature type boolean">Boolean</span>
{:#members:enablevirtualscrolling}








Allows the user to load large amount of data into pages.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
//To set the virtual scrolling during initialization  
$("#PivotGrid").ejPivotGrid({enableVirtualScrolling: true});{% endhighlight %}


{% highlight html %}
 
//Get or set the virtual scrolling, after initialization:
//Gets the virtual calling state
$("#PivotGrid").ejPivotGrid("option", "enableVirtualScrolling");
            
//Sets the virtual scrolling 
$("#PivotGrid").ejPivotGrid("option", "enableVirtualScrolling","true");{% endhighlight %}







### hyperlinkSettings<span class="type-signature type object">Object</span>
{:#members:hyperlinksettings}








Allows the user to configure hyperlink settings to Pivot Grid control.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
//To configure the hyperlink settings to Pivot Grid during initialization  
$("#PivotGrid").ejPivotGrid({hyperlinkSettings:{enableValueCellHyperlink: true, enableRowHeaderHyperlink: true}});{% endhighlight %}


{% highlight html %}
 
//Get or set the hyperlink settings, after initialization:
//Gets the hyperlink settings
$("#PivotGrid").ejPivotGrid("option", "hyperlinkSettings");
                 
//Sets the hyperlink settings to Pivot Grid
$("#PivotGrid").ejPivotGrid("option", "hyperlinkSettings", {enableValueCellHyperlink: true, enableRowHeaderHyperlink: true}); {% endhighlight %}







### hyperlinkSettings.enableColumnHeaderHyperlink<span class="type-signature type boolean">Boolean</span>
{:#members:hyperlinksettings-enablecolumnheaderhyperlink}








Allows the user to enable/diable hyperlink for column header.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
//To set the Hyperlink option for column header during initialization  
$("#PivotGrid").ejPivotGrid({hyperlinkSettings:{enableColumnHeaderHyperlink: true}});{% endhighlight %}


{% highlight html %}
 
//Get or set the hyper link for column header, after initialization:
//Gets the hyper link state
$("#PivotGrid").ejPivotGrid("option", "hyperlinkSettings");
                                 
//Sets the column header hyper link state
$("#PivotGrid").ejPivotGrid("option", "hyperlinkSettings.enableColumnHeaderHyperlink","true"); {% endhighlight %}







### hyperlinkSettings.enableRowHeaderHyperlink<span class="type-signature type boolean">Boolean</span>
{:#members:hyperlinksettings-enablerowheaderhyperlink}








Allows the user to enable/diable hyperlink for row header.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
//To set the Hyperlink option for row header during initialization  
$("#PivotGrid").ejPivotGrid({hyperlinkSettings:{enableRowHeaderHyperlink: true}});{% endhighlight %}


{% highlight html %}
 
//Get or set the hyper link for row header, after initialization:
//Gets the row header hyperlink state
$("#PivotGrid").ejPivotGrid("option", "hyperlinkSettings");
         
//Sets the row header hyperlink
$("#PivotGrid").ejPivotGrid("option", "hyperlinkSettings.enableRowHeaderHyperlink","true"); {% endhighlight %}







### hyperlinkSettings.enableSummaryCellHyperlink<span class="type-signature type boolean">Boolean</span>
{:#members:hyperlinksettings-enablesummarycellhyperlink}








Allows the user to enable/diable hyperlink for summary cells.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
//To set the Hyperlink option for summary cell during initialization  
$("#PivotGrid").ejPivotGrid({hyperlinkSettings:{enableSummaryCellHyperlink: true}});{% endhighlight %}


{% highlight html %}
 
//Get or set the hyper link for summary cell, after initialization:
//Gets the summary cell hyperlink state
$("#PivotGrid").ejPivotGrid("option", "hyperlinkSettings");
               
//Sets the summary cell hyperlink 
$("#PivotGrid").ejPivotGrid("option", "hyperlinkSettings.enableSummaryCellHyperlink","true");{% endhighlight %}







### hyperlinkSettings.enableValueCellHyperlink<span class="type-signature type boolean">Boolean</span>
{:#members:hyperlinksettings-enablevaluecellhyperlink}








Allows the user to enable/diable hyperlink for value cells.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
//To set the Hyperlink option for value cell during initialization  
$("#PivotGrid").ejPivotGrid({hyperlinkSettings:{enableValueCellHyperlink: true}});{% endhighlight %}


{% highlight html %}
 
//Get or set the hyper link for cell, after initialization:
//Gets the hyper link state
$("#PivotGrid").ejPivotGrid("option", "hyperlinkSettings");
                 
//Sets the cell hyperlink value
$("#PivotGrid").ejPivotGrid("option", "hyperlinkSettings.enableValueCellHyperlink","true");{% endhighlight %}







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
$("#PivotGrid").ejPivotGrid({isResponsive: true});{% endhighlight %}


{% highlight html %}
 
//Get or set the isResponsive, after initialization:
//Gets the isResponsive values state
$("#PivotGrid").ejPivotGrid("option", "isResponsive");
                      
//Sets the reponsive layout
$("#PivotGrid").ejPivotGrid("option", "isResponsive","true"); {% endhighlight %}







### jsonRecords<span class="type-signature type string">String</span>
{:#members:jsonrecords}








Contains the serialized JSON string which renders PivotGrid.




Default Value:
{:.param}






* ""














### layout<span class="type-signature type enum">enum</span>
{:#members:layout}








Allows the user access the different layouts for Pivot Grid.




Default Value:
{:.param}






* ej.PivotGrid.Layout.Normal








Example
{:.example}


{% highlight html %}
 
//To set the layout during initialization  
$("#PivotGrid").ejPivotGrid({layout: ej.PivotGrid.Layout.NoSummaries});{% endhighlight %}


{% highlight html %}
 
//Get or set the grid layout, after initialization:
//Gets the layout value
$("#PivotGrid").ejPivotGrid("option", "layout");
                    
//Sets the grid layout
$("#PivotGrid").ejPivotGrid("option", "layout",ej.PivotGrid.Layout.Normal); {% endhighlight %}







### locale<span class="type-signature type string">String</span>
{:#members:locale}








Sets the localized language for the control.




Default Value:
{:.param}






* "en-US"








Example
{:.example}


{% highlight html %}
 
//Sets the localized language    
$("#PivotGrid").ejPivotGrid({locale: "en-US"}}); {% endhighlight %}


{% highlight html %}
 
//Get or set the size API, after initialization:
//Gets the localization value  
$("#PivotGrid").ejPivotGrid("option","locale");
                     
//Sets the localization value 
$("#PivotGrid").ejPivotGrid("option","locale", "en-US" );{% endhighlight %}







### serviceMethodSettings<span class="type-signature type object">Object</span>
{:#members:servicemethodsettings}








Allows the user to set custom name for the methods at service-end invoked on AJAX post.




Default Value:
{:.param}






* {}








Example
{:.example}


{% highlight html %}
 
//To set serviceMethodSettings API value, to invoke the appropriate service method on UI operation.
$("#PivotGrid").ejPivotGrid({ servieMethods.initialize: "InitializeGrid" });{% endhighlight %}


{% highlight html %}
 
//Gets or sets the serviceMethodSettings API, to invoke the appropriate service method on UI operation:
//Gets the serviceMethodSettings value   
$("#PivotGrid").ejPivotGrid("option", "serviceMethodSettings");
                                             
//Sets the serviceMethodSettings value                          
$("#PivotGrid").ejPivotGrid("option", "serviceMethodSettings",  {initialize: "InitializeGrid"} ); {% endhighlight %}







### serviceMethodSettings.drillDown<span class="type-signature type string">string</span>
{:#members:servicemethodsettings-drilldown}








Allows the user to set the custom name for the service method that&#39;s responsible for drilling up/down operation in Pivot Grid.




Default Value:
{:.param}






* "DrillGrid"








Example
{:.example}


{% highlight html %}
 
//To set drillDown API value, to invoke the corresponding service method for performing server-side operation while drilling up/down in Pivot Grid.   
$("#PivotGrid").ejPivotGrid({ serviceMethodSettings: { drillDown: "DrillGridMyMethod" } });{% endhighlight %}


{% highlight html %}
 
//Get or set the drillDown API, to invoke the corresponding service method for performing server-side operation while drilling up/down in Pivot Grid:
//Gets the drillDown value   
$("#PivotGrid").ejPivotGrid("option", "serviceMethodSettings");
                                             
//Sets the drillDown value                      
$("#PivotGrid").ejPivotGrid("option", "serviceMethodSettings.drillDown", "DrillGridMyMethod"} ); {% endhighlight %}







### serviceMethodSettings.exportOptions<span class="type-signature type string">string</span>
{:#members:servicemethodsettings-exportoptions}








Allows the user to set the custom name for the service method that&#39;s responsible for performing exporting operation in Pivot Grid.




Default Value:
{:.param}






* "ExportOptions"








Example
{:.example}


{% highlight html %}
 
//To set exportOptions API value, to invoke the corresponding service method for performing server-side operation while exporting.  
$("#PivotGrid").ejPivotGrid({ serviceMethodSettings: { exportOptions: "ExportOptionsMyMethod" } });{% endhighlight %}


{% highlight html %}
 
//Gets or sets the exportOptions API, to invoke the corresponding service method for performing server-side operation while exporting.:
//Gets the exportOptions value   
$("#PivotGrid").ejPivotGrid("option", "serviceMethodSettings");
                                             
//Sets the exportOptions value                          
$("#PivotGrid").ejPivotGrid("option", "serviceMethodSettings.exportOptions", "ExportOptionsMyMethod"); {% endhighlight %}







### serviceMethodSettings.initialize<span class="type-signature type string">string</span>
{:#members:servicemethodsettings-initialize}








Allows the user to set the custom name for the service method that&#39;s responsible for initializing Pivot Grid.




Default Value:
{:.param}






* "InitializeGrid"








Example
{:.example}


{% highlight html %}
 
//To set initialize API value, to invoke the corresponding service method for Pivot Grid initialization.
$("#PivotGrid").ejPivotGrid({ servieMethods",  {initialize: "InitializeGrid"} ); {% endhighlight %}


{% highlight html %}
 
//Gets or sets the initialize API, to invoke the corresponding service method for Pivot Grid initialization:
//Gets the initialize value   
$("#PivotGrid").ejPivotGrid("option", "serviceMethodSettings");
                                             
//Sets the initialize value                     
$("#PivotGrid").ejPivotGrid("option", "serviceMethodSettings.initialize", "InitializeGrid" ); {% endhighlight %}







### serviceMethodSettings.paging<span class="type-signature type string">string</span>
{:#members:servicemethodsettings-paging}








Allows the user to set the custom name for the service method that&#39;s responsible for performing paging operation in Pivot Grid.




Default Value:
{:.param}






* "Paging"








Example
{:.example}


{% highlight html %}
 
//To set paging API value, to invoke the corresponding service method for performing server-side operation during paging in Pivot Grid.  
$("#PivotGrid").ejPivotGrid({ serviceMethodSettings: { paging: "PagingMyMethod" } });{% endhighlight %}


{% highlight html %}
 
//Gets or sets the paging API, to invoke the corresponding service method for performing server-side operation during paging in Pivot Grid:
//Gets the paging value   
$("#PivotGrid").ejPivotGrid("option", "serviceMethodSettings");
                                             
//Sets the paging value                         
$("#PivotGrid").ejPivotGrid("option", "serviceMethodSettings.paging",  "PagingMyMethod"); {% endhighlight %}







### url<span class="type-signature type string">String</span>
{:#members:url}








Connects the service using the specified URL for any server updates. See url




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
//To set service url during initialization  
$("#PivotGrid").ejPivotGrid({url: "/wcf/PivotGridService.svc"});{% endhighlight %}


{% highlight html %}
 
//Get or set the size API, after initialization:
//Gets the url value  
$("#PivotGrid").ejPivotGrid("option","url");
   
//Sets the url value 
$("#PivotGrid").ejPivotGrid("option","url", "/wcf/PivotGridService.svc" ); {% endhighlight %}





## Methods








### doAjaxPost<span class="signature">()</span>
{:#methods:doajaxpost}








Perform an asynchronous HTTP (Ajax) request.





Example
{:.example}


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
</script>{% endhighlight %}







### doPostBack<span class="signature">()</span>
{:#methods:dopostback}








Perform an asynchronous HTTP (FullPost) submit.





Example
{:.example}


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
</script>{% endhighlight %}







### refreshPagedPivotGrid<span class="signature">()</span>
{:#methods:refreshpagedpivotgrid}








This function re-renders the Pivot Grid on clicking the navigating buttons on Pivot Pager.





Example
{:.example}


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
</script>{% endhighlight %}







### renderControlFromJSON<span class="signature">()</span>
{:#methods:rendercontrolfromjson}








This function receives the JSON formatted datasource to render the Pivot Grid control.





Example
{:.example}


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
<td class="description last">Event parameters from Pivot Grid
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
<td class="description last">return the current action of Pivot Grid control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">return the custom object bounds with Pivot Grid control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the outer HTML of Pivot Grid control.</td>
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
<td class="description last">returns the Pivot Grid model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
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
 
//afterServiceInvoke event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   afterServiceInvoke: function (args) {}
});      {% endhighlight %}







### beforeServiceInvoke
{:#events:beforeserviceinvoke}








Fires before service invoked.

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
<td class="description last">Event parameters from Pivot Grid
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
<td class="description last">return the current action of Pivot Grid control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">return the custom object bounds with Pivot Grid control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the outer HTML of Pivot Grid control.</td>
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
<td class="description last">returns the Pivot Grid model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
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
 
//beforeServiceInvoke event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   beforeServiceInvoke: function (args) {}
});      {% endhighlight %}







### cellContext
{:#events:cellcontext}








Fires when the cell is right clicked.

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
<td class="description last">Event parameters from Pivot Grid.
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
args{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the original event args.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellPosition{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the cell position (row index and column index) in table.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the type of the cell.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
rowData{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the seriealized data of the header cells.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
uniqueName{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the unique name of levels/members.</td>
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
 
//cellContext event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   cellContext: function (args) {}
});      {% endhighlight %}







### columnHeaderHyperlinkClick
{:#events:columnheaderhyperlinkclick}








Fires when the column header cell is clicked once if Pivot Grid enabled with hyperlink.

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
<td class="description last">Event parameters from Pivot Grid.
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
args{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the original event args.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellPosition{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the cell position (row index and column index) in table.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the type of the cell.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
rowData{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the seriealized data of the header cells.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
uniqueName{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the unique name of levels/members.</td>
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
 
//columnHeaderHyperlinkClick event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   columnHeaderHyperlinkClick: function (args) {}
});      {% endhighlight %}







### drillSuccess
{:#events:drillsuccess}








Fires after drill down of Pivot Grid.

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
<td class="description last">Event parameters from Pivot Grid
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
<td class="description last">returns the Pivot Grid model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
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
 
//drillSuccess event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   drillSuccess: function (args) {}
});      {% endhighlight %}







### load
{:#events:load}








Fires when Pivot Grid Start loading.

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
<td class="description last">Event parameters from Pivot Grid.
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
args{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the original event args.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
action{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current action of Pivot Grid control.</td>
</tr>
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
<td class="description last">returns the HTML of Pivot Grid control.</td>
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
<td class="description last">returns the Pivot Grid model.</td>
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
 
//load event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   load: function (args) {}
});      {% endhighlight %}







### renderComplete
{:#events:rendercomplete}








Fires when Pivot Grid completely finished its rendering.

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
<td class="description last">Event parameters from Pivot Grid.
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
args{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the original event args.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
action{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current action of Pivot Grid control.</td>
</tr>
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
<td class="description last">returns the HTML of Pivot Grid control.</td>
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
<td class="description last">returns the Pivot Grid model.</td>
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
 
//renderComplete event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
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
<td class="description last">Event parameters from Pivot Grid.
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
args{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the original event args.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
action{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current action of Pivot Grid control.</td>
</tr>
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
<td class="description last">returns the HTML of Pivot Grid control.</td>
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
<td class="description last">returns the Pivot Grid model.</td>
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
 
//renderFailure event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   renderFailure: function (args) {}
});      {% endhighlight %}







### renderSuccess
{:#events:rendersuccess}








Fires when Pivot Grid successfully finished its rendering.

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
<td class="description last">Event parameters from Pivot Grid.
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
args{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the original event args.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
action{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current action of Pivot Grid control.</td>
</tr>
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
<td class="description last">returns the HTML of Pivot Grid control.</td>
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
<td class="description last">returns the Pivot Grid model.</td>
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
 
//renderSuccess event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   renderSuccess: function (args) {}
});      {% endhighlight %}







### rowHeaderHyperlinkClick
{:#events:rowheaderhyperlinkclick}








Fires when the row header cell is clicked once if Pivot Grid enabled with hyperlink.

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
<td class="description last">Event parameters from Pivot Grid.
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
args{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the original event args.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellPosition{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the cell position (row index and column index) in table.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the type of the cell.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
rowData{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the seriealized data of the header cells.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
uniqueName{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the unique name of levels/members.</td>
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
 
//rowHeaderHyperlinkClick event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   rowHeaderHyperlinkClick: function (args) {}
});      {% endhighlight %}







### summaryCellHyperlinkClick
{:#events:summarycellhyperlinkclick}








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
<td class="description last">Event parameters from Pivot Grid.
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
args{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the original event args.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellPosition{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the cell position (row index and column index) in table.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the type of the cell.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
rowData{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the seriealized data of the header cells.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
uniqueName{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the unique name of levels/members.</td>
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
 
//summaryCellHyperlinkClick event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   summaryCellHyperlinkClick: function (args) {}
});      {% endhighlight %}







### valueCellHyperlinkClick
{:#events:valuecellhyperlinkclick}








Fires when the value cell is clicked once if Pivot Grid enabled with hyperlink.

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
<td class="description last">Event parameters from Pivot Grid.
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
args{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the original event args.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellPosition{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the cell position (row index and column index) in table.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cellType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the type of the cell.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
rowData{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the seriealized data of the header cells.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
uniqueName{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the unique name of levels/members.</td>
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
 
//valueCellHyperlinkClick event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   valueCellHyperlinkClick: function (args) {}
});      {% endhighlight %}




