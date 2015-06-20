---
layout: post
title: ejPivotGrid
documentation: API
platform: js
metaname: 
metacontent: 
---

Custom Design for Pivot Grid control.










#### $(element).ejPivotGrid<span class="signature">()</span>











##### Example

<pre class="prettyprint">
<code> 
&lt;div id="PivotGrid"&gt; &lt;/div&gt; 
 
&lt;script&gt;
// Create Pivot Grid
$("#PivotGrid").ejPivotGrid(...);       
&lt;/script&gt;</code>
</pre>






### Requires




* module:jquery-1.10.2.min.js


* module:jquery.easing.1.3.min.js


* module:ej.core.js


* module:ej.data.js


* module:ej.touch.js


* module:ej.waitingpopup.js


* module:ej.pivotgrid.js


* module:ej.pivotpager.js




### Members








#### cssClass<span class="type-signature type string">String</span>








Sets the CSS name for custom operation.




Default Value:






* ""








##### Examples

<pre class="prettyprint">
<code> 
//To set the CSS name during initialization  
$("#PivotGrid").ejPivotGrid({cssClass: "gradient-lime"});       </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set css class for initialization:
        // Gets the css name.           
        $("#PivotGrid").ejPivotGrid("option", "cssClass");                      
        // Sets the rounded corner to button
        $("#PivotGrid").ejPivotGrid("option", "cssClass",  "gradient-lime" );           </code>
</pre>






#### currentReport<span class="type-signature type string">String</span>








Contains the serialized OlapReport at the instant.




Default Value:






* ""














#### customObject<span class="type-signature type object">Object</span>








Custom object to pass additional information between client-end and service-end.




Default Value:






* null








##### Examples

<pre class="prettyprint">
<code> 
// To pass additional information between client-end and service-end   
 $("#PivotGrid").ejPivotGrid({customObject: { Language: "en-US" }}); </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the custom object API, after initialization:
        //Gets the custom object value  
        $("#PivotGrid").ejPivotGrid("option","customObject");
                       
        //Sets the custom object value 
        $("#PivotGrid").ejPivotGrid("option","customObject", {Language: "en-US"} );             </code>
</pre>






#### enableCellContext<span class="type-signature type boolean">Boolean</span>








Allows the user to access/operate each cell through a custom design on right click.




Default Value:






* false








##### Examples

<pre class="prettyprint">
<code> 
//To set the cell context option during initialization  
$("#PivotGrid").ejPivotGrid({enableCellContext: true});</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the cell context, after initialization:
        //Gets the cell context state
        $("#PivotGrid").ejPivotGrid("option", "enableCellContext");
                 
        //Sets the cell context value
        $("#PivotGrid").ejPivotGrid("option", "enableCellContext","true");                      *               </code>
</pre>






#### enableJSONRendering<span class="type-signature type boolean">Boolean</span>








Allows the user to load PivotGrid using JSON data.




Default Value:






* false








##### Examples

<pre class="prettyprint">
<code> 
//To enable the direct JSONRendering during initialization  
$("#PivotGrid").ejPivotGrid({enableJSONRendering: true});</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the JSON Rendering, after initialization:
        //Gets the JSON rendering state
        $("#PivotGrid").ejPivotGrid("option", "enableJSONRendering");
               
        //Sets the JSON rendering 
        $("#PivotGrid").ejPivotGrid("option", "enableJSONRendering","true");                    *               </code>
</pre>






#### enableRTL<span class="type-signature type boolean">Boolean</span>








Allows the user to enable RTL support.




Default Value:






* false








##### Examples

<pre class="prettyprint">
<code> 
//To set the enableRTL option during initialization  
$("#PivotGrid").ejPivotGrid({enableRTL: true});</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the enableRTL, after initialization:
        //Gets the enableRTL values state
        $("#PivotGrid").ejPivotGrid("option", "enableRTL");
                 
        //Sets the cell context value
        $("#PivotGrid").ejPivotGrid("option", "enableRTL","true");                      *               </code>
</pre>






#### enableToolTip<span class="type-signature type boolean">Boolean</span>








Allows the user to enable ToolTip support.




Default Value:






* false








##### Examples

<pre class="prettyprint">
<code> 
//To set the enableToolTip option during initialization  
$("#PivotGrid").ejPivotGrid({enableToolTip: true});</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the enableToolTip, after initialization:
        //Gets the enableToolTip values state
        $("#PivotGrid").ejPivotGrid("option", "enableToolTip");
                     
        //Sets the cell context value
        $("#PivotGrid").ejPivotGrid("option", "enableToolTip","true");                  *               </code>
</pre>






#### enableVirtualScrolling<span class="type-signature type boolean">Boolean</span>








Allows the user to load large amount of data into pages.




Default Value:






* false








##### Examples

<pre class="prettyprint">
<code> 
//To set the virtual scrolling during initialization  
$("#PivotGrid").ejPivotGrid({enableVirtualScrolling: true});</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the virtual scrolling, after initialization:
        //Gets the virtual calling state
        $("#PivotGrid").ejPivotGrid("option", "enableVirtualScrolling");
            
        //Sets the virtual scrolling 
        $("#PivotGrid").ejPivotGrid("option", "enableVirtualScrolling","true");                 *               </code>
</pre>






#### hyperlinkSettings<span class="type-signature type object">Object</span>








Allows the user to configure hyperlink settings to Pivot Grid control.




Default Value:






* false








##### Examples

<pre class="prettyprint">
<code> 
//To configure the hyperlink settings to Pivot Grid during initialization  
$("#PivotGrid").ejPivotGrid({hyperlinkSettings:{enableValueCellHyperlink: true, enableRowHeaderHyperlink: true}});</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the hyperlink settings, after initialization:
        //Gets the hyperlink settings
        $("#PivotGrid").ejPivotGrid("option", "hyperlinkSettings");
                 
        //Sets the hyperlink settings to Pivot Grid
        $("#PivotGrid").ejPivotGrid("option", "hyperlinkSettings", {enableValueCellHyperlink: true, enableRowHeaderHyperlink: true});                   *               </code>
</pre>






#### hyperlinkSettings.enableColumnHeaderHyperlink<span class="type-signature type boolean">Boolean</span>








Allows the user to enable/diable hyperlink for column header.




Default Value:






* false








##### Examples

<pre class="prettyprint">
<code> 
//To set the Hyperlink option for column header during initialization  
$("#PivotGrid").ejPivotGrid({hyperlinkSettings:{enableColumnHeaderHyperlink: true}});</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the hyper link for column header, after initialization:
        //Gets the hyper link state
        $("#PivotGrid").ejPivotGrid("option", "hyperlinkSettings");
                                 
        //Sets the column header hyper link state
        $("#PivotGrid").ejPivotGrid("option", "hyperlinkSettings.enableColumnHeaderHyperlink","true");                  *               </code>
</pre>






#### hyperlinkSettings.enableRowHeaderHyperlink<span class="type-signature type boolean">Boolean</span>








Allows the user to enable/diable hyperlink for row header.




Default Value:






* false








##### Examples

<pre class="prettyprint">
<code> 
//To set the Hyperlink option for row header during initialization  
$("#PivotGrid").ejPivotGrid({hyperlinkSettings:{enableRowHeaderHyperlink: true}});</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the hyper link for row header, after initialization:
        //Gets the row header hyperlink state
        $("#PivotGrid").ejPivotGrid("option", "hyperlinkSettings");
         
        //Sets the row header hyperlink
        $("#PivotGrid").ejPivotGrid("option", "hyperlinkSettings.enableRowHeaderHyperlink","true");                     *               </code>
</pre>






#### hyperlinkSettings.enableSummaryCellHyperlink<span class="type-signature type boolean">Boolean</span>








Allows the user to enable/diable hyperlink for summary cells.




Default Value:






* false








##### Examples

<pre class="prettyprint">
<code> 
//To set the Hyperlink option for summary cell during initialization  
$("#PivotGrid").ejPivotGrid({hyperlinkSettings:{enableSummaryCellHyperlink: true}});</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the hyper link for summary cell, after initialization:
        //Gets the summary cell hyperlink state
  $("#PivotGrid").ejPivotGrid("option", "hyperlinkSettings");
               
        //Sets the summary cell hyperlink 
  $("#PivotGrid").ejPivotGrid("option", "hyperlinkSettings.enableSummaryCellHyperlink","true");                 *               </code>
</pre>






#### hyperlinkSettings.enableValueCellHyperlink<span class="type-signature type boolean">Boolean</span>








Allows the user to enable/diable hyperlink for value cells.




Default Value:






* false








##### Examples

<pre class="prettyprint">
<code> 
//To set the Hyperlink option for value cell during initialization  
$("#PivotGrid").ejPivotGrid({hyperlinkSettings:{enableValueCellHyperlink: true}});</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the hyper link for cell, after initialization:
        //Gets the hyper link state
        $("#PivotGrid").ejPivotGrid("option", "hyperlinkSettings");
                 
        //Sets the cell hyperlink value
        $("#PivotGrid").ejPivotGrid("option", "hyperlinkSettings.enableValueCellHyperlink","true");                     *               </code>
</pre>






#### isResponsive<span class="type-signature type boolean">Boolean</span>








Allows the user to enable Responsive layout support.




Default Value:






* false








##### Examples

<pre class="prettyprint">
<code> 
//To set the isResponsive option during initialization  
$("#PivotGrid").ejPivotGrid({isResponsive: true});</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the isResponsive, after initialization:
        //Gets the isResponsive values state
        $("#PivotGrid").ejPivotGrid("option", "isResponsive");
                      
        //Sets the reponsive layout
        $("#PivotGrid").ejPivotGrid("option", "isResponsive","true");                   *               </code>
</pre>






#### jsonRecords<span class="type-signature type string">String</span>








Contains the serialized JSON string which renders PivotGrid.




Default Value:






* ""














#### layout<span class="type-signature type enum">enum</span>








Allows the user access the different layouts for Pivot Grid.




Default Value:






* ej.PivotGrid.Layout.Normal








##### Examples

<pre class="prettyprint">
<code> 
//To set the layout during initialization  
$("#PivotGrid").ejPivotGrid({layout: ej.PivotGrid.Layout.NoSummaries});</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the grid layout, after initialization:
        //Gets the layout value
        $("#PivotGrid").ejPivotGrid("option", "layout");
                    
        //Sets the grid layout
        $("#PivotGrid").ejPivotGrid("option", "layout",ej.PivotGrid.Layout.Normal);                     *               </code>
</pre>






#### locale<span class="type-signature type string">String</span>








Sets the localized language for the control.




Default Value:






* "en-US"








##### Examples

<pre class="prettyprint">
<code> 
//Sets the localized language    
 $("#PivotGrid").ejPivotGrid({locale: "en-US"}}); </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the size API, after initialization:
        //Gets the localization value  
        $("#PivotGrid").ejPivotGrid("option","locale");
                     
        //Sets the localization value 
        $("#PivotGrid").ejPivotGrid("option","locale", "en-US" );               </code>
</pre>






#### serviceMethodSettings<span class="type-signature type object">Object</span>








Allows the user to set custom name for the methods at service-end invoked on AJAX post.




Default Value:






* {}








##### Examples

<pre class="prettyprint">
<code> 
//To set serviceMethodSettings API value, to invoke the appropriate service method on UI operation.
$("#PivotGrid").ejPivotGrid({ servieMethods.initialize: "InitializeGrid" });</code>
</pre>
<pre class="prettyprint">
<code> 
//Gets or sets the serviceMethodSettings API, to invoke the appropriate service method on UI operation:
//Gets the serviceMethodSettings value   
$("#PivotGrid").ejPivotGrid("option", "serviceMethodSettings");
                                             
//Sets the serviceMethodSettings value                          
$("#PivotGrid").ejPivotGrid("option", "serviceMethodSettings",  {initialize: "InitializeGrid"} ); </code>
</pre>






#### serviceMethodSettings.drillDown<span class="type-signature type string">string</span>








Allows the user to set the custom name for the service method that&#65533;s responsible for drilling up/down operation in Pivot Grid.




Default Value:






* "DrillGrid"








##### Examples

<pre class="prettyprint">
<code> 
//To set drillDown API value, to invoke the corresponding service method for performing server-side operation while drilling up/down in Pivot Grid.   
$("#PivotGrid").ejPivotGrid({ serviceMethodSettings: { drillDown: "DrillGridMyMethod" } });</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the drillDown API, to invoke the corresponding service method for performing server-side operation while drilling up/down in Pivot Grid:
//Gets the drillDown value   
$("#PivotGrid").ejPivotGrid("option", "serviceMethodSettings");
                                             
//Sets the drillDown value                      
$("#PivotGrid").ejPivotGrid("option", "serviceMethodSettings.drillDown", "DrillGridMyMethod"} ); </code>
</pre>






#### serviceMethodSettings.exportOptions<span class="type-signature type string">string</span>








Allows the user to set the custom name for the service method that&#65533;s responsible for performing exporting operation in Pivot Grid.




Default Value:






* "ExportOptions"








##### Examples

<pre class="prettyprint">
<code> 
//To set exportOptions API value, to invoke the corresponding service method for performing server-side operation while exporting.  
$("#PivotGrid").ejPivotGrid({ serviceMethodSettings: { exportOptions: "ExportOptionsMyMethod" } });</code>
</pre>
<pre class="prettyprint">
<code> 
//Gets or sets the exportOptions API, to invoke the corresponding service method for performing server-side operation while exporting.:
//Gets the exportOptions value   
$("#PivotGrid").ejPivotGrid("option", "serviceMethodSettings");
                                             
//Sets the exportOptions value                          
$("#PivotGrid").ejPivotGrid("option", "serviceMethodSettings.exportOptions", "ExportOptionsMyMethod"); </code>
</pre>






#### serviceMethodSettings.initialize<span class="type-signature type string">string</span>








Allows the user to set the custom name for the service method that&#65533;s responsible for initializing Pivot Grid.




Default Value:






* "InitializeGrid"








##### Examples

<pre class="prettyprint">
<code> 
//To set initialize API value, to invoke the corresponding service method for Pivot Grid initialization.
$("#PivotGrid").ejPivotGrid({ servieMethods",  {initialize: "InitializeGrid"} ); </code>
</pre>
<pre class="prettyprint">
<code> 
//Gets or sets the initialize API, to invoke the corresponding service method for Pivot Grid initialization:
//Gets the initialize value   
$("#PivotGrid").ejPivotGrid("option", "serviceMethodSettings");
                                             
//Sets the initialize value                     
$("#PivotGrid").ejPivotGrid("option", "serviceMethodSettings.initialize", "InitializeGrid" ); </code>
</pre>






#### serviceMethodSettings.paging<span class="type-signature type string">string</span>








Allows the user to set the custom name for the service method that&#65533;s responsible for performing paging operation in Pivot Grid.




Default Value:






* "Paging"








##### Examples

<pre class="prettyprint">
<code> 
//To set paging API value, to invoke the corresponding service method for performing server-side operation during paging in Pivot Grid.  
$("#PivotGrid").ejPivotGrid({ serviceMethodSettings: { paging: "PagingMyMethod" } });</code>
</pre>
<pre class="prettyprint">
<code> 
//Gets or sets the paging API, to invoke the corresponding service method for performing server-side operation during paging in Pivot Grid:
//Gets the paging value   
$("#PivotGrid").ejPivotGrid("option", "serviceMethodSettings");
                                             
//Sets the paging value                         
$("#PivotGrid").ejPivotGrid("option", "serviceMethodSettings.paging",  "PagingMyMethod"); </code>
</pre>






#### url<span class="type-signature type string">String</span>








Connects the service using the specified URL for any server updates. See url




Default Value:






* ""








##### Examples

<pre class="prettyprint">
<code> 
//To set service url during initialization  
$("#PivotGrid").ejPivotGrid({url: "/wcf/PivotGridService.svc"});</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the size API, after initialization:
//Gets the url value  
$("#PivotGrid").ejPivotGrid("option","url");
   
//Sets the url value 
$("#PivotGrid").ejPivotGrid("option","url", "/wcf/PivotGridService.svc" ); </code>
</pre>




### Methods








#### doAjaxPost<span class="signature">()</span>








Perform an asynchronous HTTP (Ajax) request.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="PivotGrid"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create Pivot Grid
$('#PivotGrid').ejPivotGrid({
      url: "PivotGridService.svc",
  });
var gridObj = $("#PivotGrid").data("ejPivotGrid");
gridObj.doAjaxPost("POST", "/PivotGridService.svc/Initialize", {"key", "Hello World"}, "_renderControlSuccess", null);
// Initiate an Ajax request.
&lt;/script&gt;</code>
</pre>






#### doPostBack<span class="signature">()</span>








Perform an asynchronous HTTP (FullPost) submit.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="PivotGrid"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Submitting required informatin to the service.
$('#PivotGrid').ejPivotGrid({
      url: "PivotGridService.svc",
  });
var gridObj = $("#PivotGrid").data("ejPivotGrid");
gridObj.doPostBack("/PivotGridService.svc/Initialize", {"key", "Hello World"});
// Initiate an submit.
&lt;/script&gt;</code>
</pre>






#### refreshPagedPivotGrid<span class="signature">()</span>








This function re-renders the Pivot Grid on clicking the navigating buttons on Pivot Pager.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="PivotGrid"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Refreshing Pivot Grid while perform paging.
$('#PivotGrid').ejPivotGrid({
      url: "PivotGridService.svc",
  });
var gridObj = $("#PivotGrid").data("ejPivotGrid");
gridObj.refreshPagedPivotGrid("series", 2);
// Initiate an Ajax request.
&lt;/script&gt;</code>
</pre>






#### renderControlFromJSON<span class="signature">()</span>








This function receives the JSON formatted datasource to render the Pivot Grid control.





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="PivotGrid"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Rendering Pivot Grid from given JSON formatted data.
$('#PivotGrid').ejPivotGrid({
      url: "PivotGridService.svc",
  });
var gridObj = $("#PivotGrid").data("ejPivotGrid");
gridObj.renderControlFromJSON({this.getJSONRecords()});
// Rendering Pivot Grid.
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
<td class="name"><code>action</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the current action of Pivot Grid control.</td>
</tr>
<tr>
<td class="name"><code>customObject</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">return the custom object bounds with Pivot Grid control.</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the outer HTML of Pivot Grid control.</td>
</tr>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the Pivot Grid model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
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
//afterServiceInvoke event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   afterServiceInvoke: function (args) {}
});      </code>
</pre>






#### beforeServiceInvoke








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>action</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the current action of Pivot Grid control.</td>
</tr>
<tr>
<td class="name"><code>customObject</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">return the custom object bounds with Pivot Grid control.</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the outer HTML of Pivot Grid control.</td>
</tr>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the Pivot Grid model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
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
//beforeServiceInvoke event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   beforeServiceInvoke: function (args) {}
});      </code>
</pre>






#### cellContext








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>args</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the original event args.</td>
</tr>
<tr>
<td class="name"><code>cellPosition</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the cell position (row index and column index) in table.</td>
</tr>
<tr>
<td class="name"><code>cellType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the type of the cell.</td>
</tr>
<tr>
<td class="name"><code>rowData</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the seriealized data of the header cells.</td>
</tr>
<tr>
<td class="name"><code>uniqueName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the unique name of levels/members.</td>
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
//cellContext event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   cellContext: function (args) {}
});      </code>
</pre>






#### columnHeaderHyperlinkClick








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>args</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the original event args.</td>
</tr>
<tr>
<td class="name"><code>cellPosition</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the cell position (row index and column index) in table.</td>
</tr>
<tr>
<td class="name"><code>cellType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the type of the cell.</td>
</tr>
<tr>
<td class="name"><code>rowData</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the seriealized data of the header cells.</td>
</tr>
<tr>
<td class="name"><code>uniqueName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the unique name of levels/members.</td>
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
//columnHeaderHyperlinkClick event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   columnHeaderHyperlinkClick: function (args) {}
});      </code>
</pre>






#### drillSuccess








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the Pivot Grid model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
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
//drillSuccess event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   drillSuccess: function (args) {}
});      </code>
</pre>






#### load








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>args</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the original event args.</td>
</tr>
<tr>
<td class="name"><code>action</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current action of Pivot Grid control.</td>
</tr>
<tr>
<td class="name"><code>customObject</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the custom object bounded with the control.</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the HTML of Pivot Grid control.</td>
</tr>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the Pivot Grid model.</td>
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
//load event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   load: function (args) {}
});      </code>
</pre>






#### renderComplete








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>args</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the original event args.</td>
</tr>
<tr>
<td class="name"><code>action</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current action of Pivot Grid control.</td>
</tr>
<tr>
<td class="name"><code>customObject</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the custom object bounded with the control.</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the HTML of Pivot Grid control.</td>
</tr>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the Pivot Grid model.</td>
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
//renderComplete event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   renderComplete: function (args) {}
});      </code>
</pre>






#### renderFailure








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
<td class="name"><code>args</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the original event args.</td>
</tr>
<tr>
<td class="name"><code>action</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current action of Pivot Grid control.</td>
</tr>
<tr>
<td class="name"><code>customObject</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the custom object bounded with the control.</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the HTML of Pivot Grid control.</td>
</tr>
<tr>
<td class="name"><code>message</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the error message with error code.</td>
</tr>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the Pivot Grid model.</td>
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
//renderFailure event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   renderFailure: function (args) {}
});      </code>
</pre>






#### renderSuccess








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>args</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the original event args.</td>
</tr>
<tr>
<td class="name"><code>action</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current action of Pivot Grid control.</td>
</tr>
<tr>
<td class="name"><code>customObject</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the custom object bounded with the control.</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the HTML of Pivot Grid control.</td>
</tr>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the Pivot Grid model.</td>
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
//renderSuccess event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   renderSuccess: function (args) {}
});      </code>
</pre>






#### rowHeaderHyperlinkClick








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>args</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the original event args.</td>
</tr>
<tr>
<td class="name"><code>cellPosition</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the cell position (row index and column index) in table.</td>
</tr>
<tr>
<td class="name"><code>cellType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the type of the cell.</td>
</tr>
<tr>
<td class="name"><code>rowData</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the seriealized data of the header cells.</td>
</tr>
<tr>
<td class="name"><code>uniqueName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the unique name of levels/members.</td>
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
//rowHeaderHyperlinkClick event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   rowHeaderHyperlinkClick: function (args) {}
});      </code>
</pre>






#### summaryCellHyperlinkClick








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
<td class="name"><code>args</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the original event args.</td>
</tr>
<tr>
<td class="name"><code>cellPosition</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the cell position (row index and column index) in table.</td>
</tr>
<tr>
<td class="name"><code>cellType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the type of the cell.</td>
</tr>
<tr>
<td class="name"><code>rowData</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the seriealized data of the header cells.</td>
</tr>
<tr>
<td class="name"><code>uniqueName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the unique name of levels/members.</td>
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
//summaryCellHyperlinkClick event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   summaryCellHyperlinkClick: function (args) {}
});      </code>
</pre>






#### valueCellHyperlinkClick








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>args</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the original event args.</td>
</tr>
<tr>
<td class="name"><code>cellPosition</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the cell position (row index and column index) in table.</td>
</tr>
<tr>
<td class="name"><code>cellType</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the type of the cell.</td>
</tr>
<tr>
<td class="name"><code>rowData</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the seriealized data of the header cells.</td>
</tr>
<tr>
<td class="name"><code>uniqueName</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the unique name of levels/members.</td>
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
//valueCellHyperlinkClick event for Pivot Grid
$("#PivotGrid").ejPivotGrid({
   valueCellHyperlinkClick: function (args) {}
});      </code>
</pre>



