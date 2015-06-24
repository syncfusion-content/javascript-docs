---
layout: post
title: ejReportViewer
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html ReportViewer control.










## $(element).ejReportViewer<span class="signature">()</span>











Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="reportviewer"&gt;ReportViewer&lt;/div&gt; 
 
&lt;script&gt;
// Create ReportViewer
$('#reportviewer').ejReportViewer();    
&lt;/script&gt;</code>
</pre>






## Requires




* module:jQuery


* module:jquery.easing.1.3.js


* module:jquery.globalize.js


* module:jquery.easing.1.3.js


* module:jsrender.js


* module:ej.core.js


* module:ej.editor.js


* module:ej.dialog.js


* module:ej.treeview.js


* module:ej.dropdownlist.js


* module:ej.checkbox.js


* module:ej.waitingpopup.js


* module:ej.toolbar.js


* module:ej.radiobutton.js


* module:ej.splitter.js


* module:ej.button.js


* module:ej.chart.js


* module:ej.datepicker.js


* module:ej.map.js


* module:ej.touch.js


* module:ej.data.js


* module:ej.circulargauge.js


* module:ej.lineargauge.js


* module:ej.reportviewer.js




## Members








### dataSources<span class="type-signature type array">array</span>








Gets or sets the list of data sources for the RDLC report.




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#reportviewer").ejReportViewer({ dataSources: [{name:"Menu Items",
                        values:[{ OrderId: "21D60", FoodName: "Burger", Price: 20, Category: "Veg" },
                                { OrderId: "21D61", FoodName: "Pizza", Price: 25, Category: "Non-Veg" },
                                { OrderId: "21D63", FoodName: "Sandwiches", Price: 30, Category: "Non-Veg" },
                                { OrderId: "21D65", FoodName: "Chicken Drum Sticks", Price: 23, Category: "Non-Veg" },
                                { OrderId: "21D64", FoodName: "Fulka", Price: 15, Category: "Veg" }]}]
                                });
&lt;/script&gt;</code>
</pre>






### dataSources.name<span class="type-signature type string">string</span>








Gets or sets the name of the data source.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#reportviewer").ejReportViewer({ dataSources: [name:"Menu Items",
                        values:[{ OrderId: "21D60", FoodName: "Burger", Price: 20, Category: "Veg" },
                                { OrderId: "21D61", FoodName: "Pizza", Price: 25, Category: "Non-Veg" },
                                { OrderId: "21D63", FoodName: "Sandwiches", Price: 30, Category: "Non-Veg" },
                                { OrderId: "21D65", FoodName: "Chicken Drum Sticks", Price: 23, Category: "Non-Veg" },
                                { OrderId: "21D64", FoodName: "Fulka", Price: 15, Category: "Veg" }]]
                                });
&lt;/script&gt;</code>
</pre>






### dataSources.values<span class="type-signature type object">object</span>








Gets or sets the values of data source.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#reportviewer").ejReportViewer({ dataSources: [name:"Menu Items",
                        values:[{ OrderId: "21D60", FoodName: "Burger", Price: 20, Category: "Veg" },
                                { OrderId: "21D61", FoodName: "Pizza", Price: 25, Category: "Non-Veg" },
                                { OrderId: "21D63", FoodName: "Sandwiches", Price: 30, Category: "Non-Veg" },
                                { OrderId: "21D65", FoodName: "Chicken Drum Sticks", Price: 23, Category: "Non-Veg" },
                                { OrderId: "21D64", FoodName: "Fulka", Price: 15, Category: "Veg" }]]
                                });
&lt;/script&gt;</code>
</pre>






### exportSettings<span class="type-signature type object">object</span>








Specifies the export settings.











### exportSettings.excelFormat<span class="type-signature type enum">enum</span>








Specifies the excel export format.




Default Value:
{:.param}






* ej.ReportViewer.ExcelFormats.Excel97to2003








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;        
        $("#reportviewer").ejReportViewer(
            {
               exportSettings:{ excelFormat: ej.ReportViewer.ExcelFormats.Excel97to2003}
            });            
&lt;/script&gt;</code>
</pre>






### exportSettings.exportOptions<span class="type-signature type enum">enum</span>








Specifies the export formats.




Default Value:
{:.param}






* ej.ReportViewer.ExportOptions.All








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;        
        $("#reportviewer").ejReportViewer(
            {
               exportSettings:{ exportOptions: ej.ReportViewer.ExportOptions.Html | ej.ReportViewer.ExportOptions.Pdf }
            });            
&lt;/script&gt;</code>
</pre>






### exportSettings.wordFormat<span class="type-signature type enum">enum</span>








Specifies the word export format.




Default Value:
{:.param}






* ej.ReportViewer.WordFormats.Doc








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;        
        $("#reportviewer").ejReportViewer(
            {
               exportSettings:{ wordFormat: ej.ReportViewer.WordFormats.Doc}
            });            
&lt;/script&gt;</code>
</pre>






### locale<span class="type-signature type string">string</span>








Specifies the locale for report viewer.




Default Value:
{:.param}






* "en-US"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#reportviewer").ejReportViewer(
                {
                   locale: "it-IT"
                });             
&lt;/script&gt;</code>
</pre>






### pageSettings<span class="type-signature type object">object</span>








Specifies the page settings.











### pageSettings.orientation<span class="type-signature type enum">enum</span>








Specifies the print layout orientation.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;        
        $("#reportviewer").ejReportViewer(
            {
               pageSettings:{ orientation: ej.ReportViewer.Orientation.Landscape }
            });
&lt;/script&gt;</code>
</pre>






### pageSettings.paperSize<span class="type-signature type enum">enum</span>








Specifies the paper size of print layout.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;        
        $("#reportviewer").ejReportViewer(
            {
               pageSettings:{ paperSize: ej.ReportViewer.PaperSize.A4 }
            });
&lt;/script&gt;</code>
</pre>






### parameters<span class="type-signature type array">array</span>








Gets or sets the list of parameters associated with the report.




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#reportviewer").ejReportViewer({ parameters: [{
                                name:"Vehicle",
                                labels:["Motor Bikes"],
                                prompt:"Please select the color",
                                values:["Red","Green","Blue","Yellow","Black"],
                                nullable:false
                                 }]});
&lt;/script&gt;</code>
</pre>






### parameters.labels<span class="type-signature type array">array</span>








Gets or sets the parameter labels.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#reportviewer").ejReportViewer({ parameters: [{
                                name:"Vehicle",
                                labels:["Motor Bikes"],
                                prompt:"Please select the color",
                                values:["Red","Green","Blue","Yellow","Black"],
                                nullable:false
                                 }]});
&lt;/script&gt;</code>
</pre>






### parameters.name<span class="type-signature type string">string</span>








Gets or sets the name of the parameter.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#reportviewer").ejReportViewer({ parameters: [{
                                name:"Vehicle",
                                labels:["Motor Bikes"],
                                prompt:"Please select the color",
                                values:["Red","Green","Blue","Yellow","Black"],
                                nullable:false
                                 }]});
&lt;/script&gt;</code>
</pre>






### parameters.nullable<span class="type-signature type boolean">boolean</span>








Gets or sets whether the parameter allows nullable value or not.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#reportviewer").ejReportViewer({ parameters: [{
                                name:"Vehicle",
                                labels:["Motor Bikes"],
                                prompt:"Please select the color",
                                values:["Red","Green","Blue","Yellow","Black"],
                                nullable:false
                                 }]});
&lt;/script&gt;</code>
</pre>






### parameters.prompt<span class="type-signature type string">string</span>








Gets or sets the prompt message associated with the specified parameter.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#reportviewer").ejReportViewer({ parameters: [{
                                name:"Vehicle",
                                labels:["Motor Bikes"],
                                prompt:"Please select the Color",
                                values:["Red","Green","Blue","Yellow","Black"],
                                nullable:false
                                 }]});
&lt;/script&gt;</code>
</pre>






### parameters.values<span class="type-signature type array">array</span>








Gets or sets the parameter values.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#reportviewer").ejReportViewer({ parameters: [{
                                name:"Vehicle",
                                labels:["Motor Bikes"],
                                prompt:"Please select the color",
                                values:["Red","Green","Blue","Yellow","Black"],
                                nullable:false
                                 }]});
&lt;/script&gt;</code>
</pre>






### printMode<span class="type-signature type boolean">boolean</span>








Enables and disables the print mode.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#reportviewer").ejReportViewer(
                {
                   printMode:true
                });             
&lt;/script&gt;</code>
</pre>






### processingMode<span class="type-signature type enum">enum</span>








Specifies the processing mode of the report.




Default Value:
{:.param}






* ej.ReportViewer.ProcessingMode.Remote








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;        
        $("#reportviewer").ejReportViewer({ processingMode: ej.ReportViewer.ProcessingMode.Remote });            
&lt;/script&gt;</code>
</pre>






### renderMode<span class="type-signature type enum">enum</span>








Specifies the render layout.




Default Value:
{:.param}






* ej.ReportViewer.RenderMode.Default








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;        
        $("#reportviewer").ejReportViewer({ renderMode: ej.ReportViewer.RenderMode.Default });            
&lt;/script&gt;</code>
</pre>






### reportPath<span class="type-signature type string">string</span>








Gets or sets the path of the report file.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#reportviewer").ejReportViewer({ reportPath: "~/App_Data/Sample.rdl" });            
&lt;/script&gt;</code>
</pre>






### reportServerUrl<span class="type-signature type string">string</span>








Gets or sets the reports server url.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#reportviewer").ejReportViewer({ reportServerUrl:  "http://172.16.7.164/ReportServer/SampleReport.rdl" });            
&lt;/script&gt;</code>
</pre>






### reportServiceUrl<span class="type-signature type string">string</span>








Specifies the report Web API service url.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;
        $("#reportviewer").ejReportViewer({ reportServiceUrl:  "../api/RDLReport" });            
&lt;/script&gt;</code>
</pre>






### toolbarSettings<span class="type-signature type object">object</span>








Specifies the toolbar settings.











### toolbarSettings.click<span class="type-signature type string">string</span>








Fires when user click on toolbar item in the toolbar.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#reportviewer").ejReportViewer(
            {
               toolbarSettings:{click: "onToolbarClick"}
            });         
&lt;/script&gt;</code>
</pre>






### toolbarSettings.items<span class="type-signature type enum">enum</span>








Specifies the toolbar items.




Default Value:
{:.param}






* ej.ReportViewer.ToolbarItems.All








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;        
        $("#reportviewer").ejReportViewer(
            {
               toolbarSettings:{ exportOptions: ej.ReportViewer.ToolbarItems.All }
            });
&lt;/script&gt;</code>
</pre>






### toolbarSettings.showToolbar<span class="type-signature type boolean">boolean</span>








Shows or hides the toolbar.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#reportviewer").ejReportViewer(
            {
               toolbarSettings:{showToolbar: true}
            });         
&lt;/script&gt;</code>
</pre>






### toolbarSettings.showTooltip<span class="type-signature type boolean">boolean</span>








Shows or hides the tooltip of toolbar items.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#reportviewer").ejReportViewer(
            {
               toolbarSettings:showTooltip: true}
            });         
&lt;/script&gt;</code>
</pre>






### toolbarSettings.templateId<span class="type-signature type string">string</span>








Specifies the toolbar template ID..




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;          
        $("#reportviewer").ejReportViewer(
            {
               toolbarSettings:{templateId: ""}
            });         
&lt;/script&gt;</code>
</pre>






### zoomFactor<span class="type-signature type number">number</span>








Gets or sets the zoom factor for report viewer.




Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;        
        $("#reportviewer").ejReportViewer({ zoomFactor:  2 });            
&lt;/script&gt;</code>
</pre>




## Methods








### exportReport<span class="signature">()</span>








Export the report to the specified format.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;ReportViewer&lt;/div&gt; 
 
&lt;script&gt;
var reportviewerObj = $("#reportviewer").data("ejReportViewer");
reportviewerObj.exportReport(); //Exports the reports
&lt;/script&gt;</code>
</pre>






### fitToPage<span class="signature">()</span>








Fit the report page to the container.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;ReportViewer&lt;/div&gt; 
 
&lt;script&gt;
var reportviewerObj = $("#reportviewer").data("ejReportViewer");
reportviewerObj.fitToPage(); // To fit the report page.
&lt;/script&gt;</code>
</pre>






### fitToPageHeight<span class="signature">()</span>








Fit the report page height to the container.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;ReportViewer&lt;/div&gt; 
 
&lt;script&gt;
var reportviewerObj = $("#reportviewer").data("ejReportViewer");
reportviewerObj.fitToPageHeight(); // To fit the report page height.
&lt;/script&gt;</code>
</pre>






### fitToPageWidth<span class="signature">()</span>








Fit the report page width to the container.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;ReportViewer&lt;/div&gt; 
 
&lt;script&gt;
var reportviewerObj = $("#reportviewer").data("ejReportViewer");
reportviewerObj.fitToPageWidth(); // To fit the report page width.
&lt;/script&gt;</code>
</pre>






### getDataSetNames<span class="signature">()</span>








Get the available datasets name of the rdlc report.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;ReportViewer&lt;/div&gt; 
 
&lt;script&gt;
var reportviewerObj = $("#reportviewer").data("ejReportViewer");
reportviewerObj.getDataSetNames(); // To get the dataset names.
&lt;/script&gt;</code>
</pre>






### getParameters<span class="signature">()</span>








Get the available parameters of the report.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;ReportViewer&lt;/div&gt; 
 
&lt;script&gt;
var reportviewerObj = $("#reportviewer").data("ejReportViewer");
reportviewerObj.getParameters(); // To get the parameters.
&lt;/script&gt;</code>
</pre>






### gotoFirstPage<span class="signature">()</span>








Navigate to first page of report.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;ReportViewer&lt;/div&gt; 
 
&lt;script&gt;
var reportviewerObj = $("#reportviewer").data("ejReportViewer");
reportviewerObj.gotoFirstPage(); // To navigate to first page
&lt;/script&gt;</code>
</pre>






### gotoLastPage<span class="signature">()</span>








Navigate to last page of the report.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;ReportViewer&lt;/div&gt; 
 
&lt;script&gt;
var reportviewerObj = $("#reportviewer").data("ejReportViewer");
reportviewerObj.gotoLastPage(); // Navigate to the last page
&lt;/script&gt;</code>
</pre>






### gotoNextPage<span class="signature">()</span>








Navigate to next page from the current page.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;ReportViewer&lt;/div&gt; 
 
&lt;script&gt;
var reportviewerObj = $("#reportviewer").data("ejReportViewer");
reportviewerObj.gotoNextPage(); //To navigate to the next page
&lt;/script&gt;</code>
</pre>






### gotoPageIndex<span class="signature">()</span>








Go to specific page index of the report.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;ReportViewer&lt;/div&gt; 
 
&lt;script&gt;
var reportviewerObj = $("#reportviewer").data("ejReportViewer");
reportviewerObj.gotoPageIndex(5); // To navigate the specific page
&lt;/script&gt;</code>
</pre>






### gotoPreviousPage<span class="signature">()</span>








Navigate to previous page from the current page.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;ReportViewer&lt;/div&gt; 
 
&lt;script&gt;
var reportviewerObj = $("#reportviewer").data("ejReportViewer");
reportviewerObj.gotoPreviousPage(); // To navigate to the previous page
&lt;/script&gt;</code>
</pre>






### print<span class="signature">()</span>








Print the report.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;ReportViewer&lt;/div&gt; 
 
&lt;script&gt;
var reportviewerObj = $("#reportviewer").data("ejReportViewer");
reportviewerObj.print(); //To perform print operation.
&lt;/script&gt;</code>
</pre>






### printLayout<span class="signature">()</span>








Apply print layout to the report.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;ReportViewer&lt;/div&gt; 
 
&lt;script&gt;
var reportviewerObj = $("#reportviewer").data("ejReportViewer");
reportviewerObj.printLayout(); //Changes between print layout and normal modes.
&lt;/script&gt;</code>
</pre>






### refresh<span class="signature">()</span>








Refresh the report.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;ReportViewer&lt;/div&gt; 
 
&lt;script&gt;
var reportviewerObj = $("#reportviewer").data("ejReportViewer");
reportviewerObj.refresh(); // To refresh the report.
&lt;/script&gt;</code>
</pre>




## Events








### destroy








Fires when the report viewer is destroyed successfully.If you want to perform any operation after destroying the reportviewer control,you can make use of the destroy event.

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
<td class="description last">Event parameters from reportviewer
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
<td class="description last">true if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the report model</td>
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




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;        
        $("#reportviewer").ejReportViewer({ 
     destroy:  function (args) {
      // Write a code block to perform any operation after destroy of reportviewer.
      }
    });           
&lt;/script&gt;</code>
</pre>






### drillThrough








Fires during drill through action done in report.If you want to perform any operation when a drill through action is performed, you can make use of the drillThrough event.

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
<td class="description last">Event parameters from reportviewer
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
<td class="description last">true if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>actionInfo</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the actionInfo's parameters bookmarkLink,hyperLink,reportName,parameters.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the report model</td>
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




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;        
        $("#reportviewer").ejReportViewer({ 
         drillThrough: function (args) {
      // Write a code block to perform any operation when drill through action occurs in report.
      }
    });                   
&lt;/script&gt;</code>
</pre>






### renderingBegin








Fires before report rendering is completed.If you want to perform any operation before the rendering of report,you can make use of the renderingBegin event.

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
<td class="description last">Event parameters from reportviewer
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
<td class="description last">true if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the report model</td>
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




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;  
//rendering begin event for report.               
        $("#reportviewer").ejReportViewer({
       renderingBegin:function(args)
            {
                 // Write a code block to perform any operation before rendering.
            }
    });                 
&lt;/script&gt;</code>
</pre>






### renderingComplete








Fires after report rendering completed.If you want to perform any operation after the rendering of report,you can make use of this renderingComplete event.

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
<td class="description last">Event parameters from reportviewer
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
<td class="description last">true if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the report model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>reportParameters</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the collection of parameters</td>
</tr>
<tr>
<td class="name"><code>reportParameters</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the collection of parameters</td>
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
&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;        
//rendering complete event for reportviewer control.
        $("#reportviewer").ejReportViewer({ 
      renderingComplete:function(args)
            {
                 // Write a code block to perform any operation after rendering completed.
            }
    });            
&lt;/script&gt;</code>
</pre>






### reportError








Fires when any error occurred while rendering the report.If you want to perform any operation when an error occurs in the report, you can make use of the reportError event.

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
<td class="description last">Event parameters from reportviewer
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
<td class="description last">true if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>error</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the error details</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the report model</td>
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




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;        
        $("#reportviewer").ejReportViewer({
                  reportError: function (args) {
      // Write a code block to perform any operation when report error occurs.
      }
    });                         
&lt;/script&gt;</code>
</pre>






### reportLoaded








Fires when the report is loaded.If you want to perform any operation after the successful loading of report, you can make use of the reportLoaded event.

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
<td class="description last">event parameters from reportviewer
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
<td class="description last">true if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the report model</td>
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




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;        
        $("#reportviewer").ejReportViewer({
          reportLoaded: function(args)
            {
                 // Write a code block to perform any action when the report is loaded successfully.
            }
    });             
&lt;/script&gt;</code>
</pre>






### viewReportClick








Fires when click the View Report Button.

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
<td class="description last">Event parameters from reportviewer
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
<td class="description last">true if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>parameters</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the parameter collection.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the report model</td>
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




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="reportviewer"&gt;&lt;/div&gt; 
&lt;script&gt;        
        $("#reportviewer").ejReportViewer({ 
     viewReportClick:  function (args) {
      // Write a code block to perform any operation after destroy of reportviewer.
      }
    });           
&lt;/script&gt;</code>
</pre>



