---
layout: post
title: ejReportViewer
documentation: API
platform: js
metaname: 
metacontent: 
---


# ejReportViewer

The ReportViewer is a visualization control to view Microsoft SSRS RDL/RDLC files on a web page and it is powered by HTML5/JavaScript. It has support to bind DataSources/Parameters to the Reports and also supports exporting, paging, zooming and printing the report.

$(element).ejReportViewer<span class="signature">()</span>

Example
{:.example}

{% highlight html %}

<div id="reportviewer">ReportViewer</div> 
<script>
    // Create ReportViewer
    $('#reportviewer').ejReportViewer();    
</script>

{% endhighlight %}

Requires
{:.require}

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
{:#members:datasources}

Gets or sets the list of data sources for the RDLC report.

Default Value:
{:.param}

* []

Example
{:.example}

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>
    $("#reportviewer").ejReportViewer({ dataSources: [{name:"Menu Items",
    values:[{ OrderId: "21D60", FoodName: "Burger", Price: 20, Category: "Veg" },
            { OrderId: "21D61", FoodName: "Pizza", Price: 25, Category: "Non-Veg" },
            { OrderId: "21D63", FoodName: "Sandwiches", Price: 30, Category: "Non-Veg" },
            { OrderId: "21D65", FoodName: "Chicken Drum Sticks", Price: 23, Category: "Non-Veg" },
            { OrderId: "21D64", FoodName: "Fulka", Price: 15, Category: "Veg" }]}]
    });
</script>

{% endhighlight %}

### dataSources.name<span class="type-signature type string">string</span>
{:#members:datasources-name}

Gets or sets the name of the data source.

Default Value:
{:.param}

* empty

Example
{:.example}

{% highlight html %}

<div id="reportviewer"></div> 
<script>
    $("#reportviewer").ejReportViewer({ dataSources: [name:"Menu Items",
    values:[{ OrderId: "21D60", FoodName: "Burger", Price: 20, Category: "Veg" },
            { OrderId: "21D61", FoodName: "Pizza", Price: 25, Category: "Non-Veg" },
            { OrderId: "21D63", FoodName: "Sandwiches", Price: 30, Category: "Non-Veg" },
            { OrderId: "21D65", FoodName: "Chicken Drum Sticks", Price: 23, Category: "Non-Veg" },
            { OrderId: "21D64", FoodName: "Fulka", Price: 15, Category: "Veg" }]]
    });
</script>

{% endhighlight %}

### dataSources.values<span class="type-signature type object">object</span>
{:#members:datasources-values}

Gets or sets the values of data source.

Default Value:
{:.param}

* null

Example
{:.example}

{% highlight html %}

<div id="reportviewer"></div> 
<script>
    $("#reportviewer").ejReportViewer({ dataSources: [name:"Menu Items",
    values:[{ OrderId: "21D60", FoodName: "Burger", Price: 20, Category: "Veg" },
            { OrderId: "21D61", FoodName: "Pizza", Price: 25, Category: "Non-Veg" },
            { OrderId: "21D63", FoodName: "Sandwiches", Price: 30, Category: "Non-Veg" },
            { OrderId: "21D65", FoodName: "Chicken Drum Sticks", Price: 23, Category: "Non-Veg" },
            { OrderId: "21D64", FoodName: "Fulka", Price: 15, Category: "Veg" }]]
    });
</script>

{% endhighlight %}

### exportSettings<span class="type-signature type object">object</span>
{:#members:exportsettings}

Specifies the export settings.

### exportSettings.excelFormat<span class="type-signature type enum">enum</span>
{:#members:exportsettings-excelformat}

Specifies the excel export format.

Default Value:
{:.param}

* ej.ReportViewer.ExcelFormats.Excel97to2003

Example
{:.example}

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>        
    $("#reportviewer").ejReportViewer(
        {
            exportSettings:{ excelFormat: ej.ReportViewer.ExcelFormats.Excel97to2003}
        });            
</script>

{% endhighlight %}

### exportSettings.exportOptions<span class="type-signature type enum">enum</span>
{:#members:exportsettings-exportoptions}

Specifies the export formats.

Default Value:
{:.param}

* ej.ReportViewer.ExportOptions.All

Example
{:.example}

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>        
    $("#reportviewer").ejReportViewer(
        {
            exportSettings:{ exportOptions: ej.ReportViewer.ExportOptions.Html | ej.ReportViewer.ExportOptions.Pdf }
        });            
</script>

{% endhighlight %}


### exportSettings.wordFormat<span class="type-signature type enum">enum</span>
{:#members:exportsettings-wordformat}

Specifies the word export format.

Default Value:
{:.param}

* ej.ReportViewer.WordFormats.Doc

Example
{:.example}

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>        
    $("#reportviewer").ejReportViewer(
        {
            exportSettings:{ wordFormat: ej.ReportViewer.WordFormats.Doc}
        });            
</script>

{% endhighlight %}

### locale<span class="type-signature type string">string</span>
{:#members:locale}

Specifies the locale for report viewer.

Default Value:
{:.param}

* "en-US"

Example
{:.example}

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>          
    $("#reportviewer").ejReportViewer(
        {
            locale: "it-IT"
        });             
</script>

{% endhighlight %}

### pageSettings<span class="type-signature type object">object</span>
{:#members:pagesettings}

Specifies the page settings.

### pageSettings.orientation<span class="type-signature type enum">enum</span>
{:#members:pagesettings-orientation}

Specifies the print layout orientation.

Default Value:
{:.param}

* null

Example
{:.example}

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>        
    $("#reportviewer").ejReportViewer(
        {
            pageSettings:{ orientation: ej.ReportViewer.Orientation.Landscape }
        });
</script>

{% endhighlight %}

### pageSettings.paperSize<span class="type-signature type enum">enum</span>
{:#members:pagesettings-papersize}

Specifies the paper size of print layout.

Default Value:
{:.param}

* null

Example
{:.example}

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>        
    $("#reportviewer").ejReportViewer(
        {
            pageSettings:{ paperSize: ej.ReportViewer.PaperSize.A4 }
        });
</script>

{% endhighlight %}


### parameters<span class="type-signature type array">array</span>
{:#members:parameters}

Gets or sets the list of parameters associated with the report.

Default Value:
{:.param}

* []

Example
{:.example}

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>
    $("#reportviewer").ejReportViewer({ 
        parameters: [{
            name:"Vehicle",
            labels:["Motor Bikes"],
            prompt:"Please select the color",
            values:["Red","Green","Blue","Yellow","Black"],
            nullable:false
        }]       
    });
</script>

{% endhighlight %}

### parameters.labels<span class="type-signature type array">array</span>
{:#members:parameters-labels}

Gets or sets the parameter labels.

Default Value:
{:.param}

* null

Example
{:.example}

{% highlight html %}

<div id="reportviewer"></div> 
<script>
    $("#reportviewer").ejReportViewer({ 
        parameters: [{
            name:"Vehicle",
            labels:["Motor Bikes"],
            prompt:"Please select the color",
            values:["Red","Green","Blue","Yellow","Black"],
            nullable:false
        }]
    });
</script>

{% endhighlight %}

### parameters.name<span class="type-signature type string">string</span>
{:#members:parameters-name}

Gets or sets the name of the parameter.

Default Value:
{:.param}

* empty

Example
{:.example}

{% highlight html %}

<div id="reportviewer"></div> 
<script>
    $("#reportviewer").ejReportViewer({
        parameters: [{
            name:"Vehicle",
            labels:["Motor Bikes"],
            prompt:"Please select the color",
            values:["Red","Green","Blue","Yellow","Black"],
            nullable:false
        }]
    });
</script>

{% endhighlight %}

### parameters.nullable<span class="type-signature type boolean">boolean</span>
{:#members:parameters-nullable}

Gets or sets whether the parameter allows nullable value or not.

Default Value:
{:.param}

* false

Example
{:.example}

{% highlight html %}

<div id="reportviewer"></div> 
<script>
    $("#reportviewer").ejReportViewer({
        parameters: [{
            name:"Vehicle",
            labels:["Motor Bikes"],
            prompt:"Please select the color",
            values:["Red","Green","Blue","Yellow","Black"],
            nullable:false
        }]
    });
</script>

{% endhighlight %}

### parameters.prompt<span class="type-signature type string">string</span>
{:#members:parameters-prompt}

Gets or sets the prompt message associated with the specified parameter.

Default Value:
{:.param}

* empty

Example
{:.example}

{% highlight html %}

<div id="reportviewer"></div> 
<script>
    $("#reportviewer").ejReportViewer({ 
        parameters: [{
            name:"Vehicle",
            labels:["Motor Bikes"],
            prompt:"Please select the Color",
            values:["Red","Green","Blue","Yellow","Black"],
            nullable:false
        }]
    });
</script>

{% endhighlight %}

### parameters.values<span class="type-signature type array">array</span>
{:#members:parameters-values}

Gets or sets the parameter values.

Default Value:
{:.param}

* null

Example
{:.example}

{% highlight html %}

<div id="reportviewer"></div> 
<script>
    $("#reportviewer").ejReportViewer({ 
        parameters: [{
            name:"Vehicle",
            labels:["Motor Bikes"],
            prompt:"Please select the color",
            values:["Red","Green","Blue","Yellow","Black"],
            nullable:false
        }]
    });
</script>

{% endhighlight %}

### printMode<span class="type-signature type boolean">boolean</span>
{:#members:printmode}

Enables and disables the print mode.

Default Value:
{:.param}

* false

Example
{:.example}

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>          
    $("#reportviewer").ejReportViewer(
        {
            printMode:true
        });             
</script>

{% endhighlight %}

### processingMode<span class="type-signature type enum">enum</span>
{:#members:processingmode}

Specifies the processing mode of the report.

Default Value:
{:.param}

* ej.ReportViewer.ProcessingMode.Remote

Example
{:.example}

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>        
    $("#reportviewer").ejReportViewer({ processingMode: ej.ReportViewer.ProcessingMode.Remote });            
</script>

{% endhighlight %}

### renderMode<span class="type-signature type enum">enum</span>
{:#members:rendermode}

Specifies the render layout.

Default Value:
{:.param}

* ej.ReportViewer.RenderMode.Default

Example
{:.example}

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>        
    $("#reportviewer").ejReportViewer({ renderMode: ej.ReportViewer.RenderMode.Default });            
</script>

{% endhighlight %}

### reportPath<span class="type-signature type string">string</span>
{:#members:reportpath}

Gets or sets the path of the report file.

Default Value:
{:.param}

* empty

Example
{:.example}

{% highlight html %}

<div id="reportviewer"></div> 
<script>
    $("#reportviewer").ejReportViewer({ reportPath: "~/App_Data/Sample.rdl" });            
</script>

{% endhighlight %}

### reportServerUrl<span class="type-signature type string">string</span>
{:#members:reportserverurl}

Gets or sets the reports server url.

Default Value:
{:.param}

* empty

Example
{:.example}

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>
    $("#reportviewer").ejReportViewer({ reportServerUrl:  "http://172.16.7.164/ReportServer/SampleReport.rdl" });            
</script>

{% endhighlight %}

### reportServiceUrl<span class="type-signature type string">string</span>
{:#members:reportserviceurl}

Specifies the report Web API service url.

Default Value:
{:.param}

* empty

Example
{:.example}

{% highlight html %}

<div id="reportviewer"></div> 
<script>
    $("#reportviewer").ejReportViewer({ reportServiceUrl:  "../api/RDLReport" });            
</script>

{% endhighlight %}

### toolbarSettings<span class="type-signature type object">object</span>
{:#members:toolbarsettings}

Specifies the toolbar settings.

### toolbarSettings.click<span class="type-signature type string">string</span>
{:#members:toolbarsettings-click}

Fires when user click on toolbar item in the toolbar.

Default Value:
{:.param}

* empty

Example
{:.example}

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>          
    $("#reportviewer").ejReportViewer(
        {
            toolbarSettings:{click: "onToolbarClick"}
        });         
</script>

{% endhighlight %}

### toolbarSettings.items<span class="type-signature type enum">enum</span>
{:#members:toolbarsettings-items}

Specifies the toolbar items.

Default Value:
{:.param}

* ej.ReportViewer.ToolbarItems.All

Example
{:.example}

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>        
    $("#reportviewer").ejReportViewer(
        {
            toolbarSettings:{ exportOptions: ej.ReportViewer.ToolbarItems.All }
        });
</script>

{% endhighlight %}

### toolbarSettings.showToolbar<span class="type-signature type boolean">boolean</span>
{:#members:toolbarsettings-showtoolbar}

Shows or hides the toolbar.

Default Value:
{:.param}

* true

Example
{:.example}

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>          
    $("#reportviewer").ejReportViewer(
        {
            toolbarSettings:{showToolbar: true}
        });         
</script>

{% endhighlight %}

### toolbarSettings.showTooltip<span class="type-signature type boolean">boolean</span>
{:#members:toolbarsettings-showtooltip}

Shows or hides the tooltip of toolbar items.

Default Value:
{:.param}

* true

Example
{:.example}

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>          
    $("#reportviewer").ejReportViewer(
        {
            toolbarSettings:showTooltip: true}
        });         
</script>

{% endhighlight %}

### toolbarSettings.templateId<span class="type-signature type string">string</span>
{:#members:toolbarsettings-templateid}

Specifies the toolbar template ID.

Default Value:
{:.param}

* empty

Example
{:.example}

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>          
    $("#reportviewer").ejReportViewer(
        {
            toolbarSettings:{templateId: "customtoolbarId"}
        });         
</script>

{% endhighlight %}

### zoomFactor<span class="type-signature type number">number</span>
{:#members:zoomfactor}

Gets or sets the zoom factor for report viewer.

Default Value:
{:.param}

* 1

Example
{:.example}

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>        
    $("#reportviewer").ejReportViewer({ zoomFactor:  2 });            
</script>

{% endhighlight %}

### isResponsive<span class="type-signature type boolean">boolean</span>
{:#members:isResponsive}

Enables or disables the responsive of report viewer when window resized.

Default Value:
{:.param}

* true

Example
{:.example}

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>        
    $("#reportviewer").ejReportViewer({ isResponsive: true });            
</script>

{% endhighlight %}

### enablePageCache<span class="type-signature type boolean">boolean</span>
{:#members:enablePageCache}

Enables or disables the cache in page of report viewer.

Default Value:
{:.param}

* false

Example
{:.example}

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>        
    $("#reportviewer").ejReportViewer({ enablePageCache: false });            
</script>

{% endhighlight %}

## Methods

### exportReport<span class="signature">()</span>
{:#methods:exportreport}

Export the report to the specified format.

Example
{:.example}

{% highlight html %}
 
<div id="reportviewer">ReportViewer</div> 
<script>
    var reportviewerObj = $("#reportviewer").data("ejReportViewer");
    reportviewerObj.exportReport(); //Exports the reports
</script>

{% endhighlight %}

### fitToPage<span class="signature">()</span>
{:#methods:fittopage}

Fit the report page to the container.

Example
{:.example}

{% highlight html %}
 
<div id="reportviewer">ReportViewer</div> 
<script>
    var reportviewerObj = $("#reportviewer").data("ejReportViewer");
    reportviewerObj.fitToPage(); // To fit the report page.
</script>

{% endhighlight %}

### fitToPageHeight<span class="signature">()</span>
{:#methods:fittopageheight}

Fit the report page height to the container.

Example
{:.example}

{% highlight html %}
 
<div id="reportviewer">ReportViewer</div> 
<script>
    var reportviewerObj = $("#reportviewer").data("ejReportViewer");
    reportviewerObj.fitToPageHeight(); // To fit the report page height.
</script>

{% endhighlight %}

### fitToPageWidth<span class="signature">()</span>
{:#methods:fittopagewidth}

Fit the report page width to the container.

Example
{:.example}

{% highlight html %}
 
<div id="reportviewer">ReportViewer</div> 
<script>
    var reportviewerObj = $("#reportviewer").data("ejReportViewer");
    reportviewerObj.fitToPageWidth(); // To fit the report page width.
</script>

{% endhighlight %}

### getDataSetNames<span class="signature">()</span>
{:#methods:getdatasetnames}

Get the available datasets name of the rdlc report.

Example
{:.example}

{% highlight html %}
 
<div id="reportviewer">ReportViewer</div> 
<script>
    var reportviewerObj = $("#reportviewer").data("ejReportViewer");
    reportviewerObj.getDataSetNames(); // To get the dataset names.
</script>

{% endhighlight %}

### getParameters<span class="signature">()</span>
{:#methods:getparameters}

Get the available parameters of the report.

Example
{:.example}

{% highlight html %}
 
<div id="reportviewer">ReportViewer</div> 
<script>
    var reportviewerObj = $("#reportviewer").data("ejReportViewer"); 
    reportviewerObj.getParameters(); // To get the parameters.
</script>

{% endhighlight %}

### gotoFirstPage<span class="signature">()</span>
{:#methods:gotofirstpage}

Navigate to first page of report.

Example
{:.example}

{% highlight html %}

<div id="reportviewer">ReportViewer</div> 
<script>
    var reportviewerObj = $("#reportviewer").data("ejReportViewer");
    reportviewerObj.gotoFirstPage(); // To navigate to first page
</script>

{% endhighlight %}

### gotoLastPage<span class="signature">()</span>
{:#methods:gotolastpage}

Navigate to last page of the report.

Example
{:.example}

{% highlight html %}
 
<div id="reportviewer">ReportViewer</div> 
<script>
    var reportviewerObj = $("#reportviewer").data("ejReportViewer");
    reportviewerObj.gotoLastPage(); // Navigate to the last page
</script>

{% endhighlight %}

### gotoNextPage<span class="signature">()</span>
{:#methods:gotonextpage}

Navigate to next page from the current page.

Example
{:.example}

{% highlight html %}
 
<div id="reportviewer">ReportViewer</div> 
<script>
    var reportviewerObj = $("#reportviewer").data("ejReportViewer");
    reportviewerObj.gotoNextPage(); //To navigate to the next page
</script>

{% endhighlight %}


### gotoPageIndex<span class="signature">()</span>
{:#methods:gotopageindex}

Go to specific page index of the report.

Example
{:.example}

{% highlight html %}
 
<div id="reportviewer">ReportViewer</div> 
<script>
    var reportviewerObj = $("#reportviewer").data("ejReportViewer");
    reportviewerObj.gotoPageIndex(5); // To navigate the specific page
</script>

{% endhighlight %}

### gotoPreviousPage<span class="signature">()</span>
{:#methods:gotopreviouspage}

Navigate to previous page from the current page.

Example
{:.example}

{% highlight html %}
 
<div id="reportviewer">ReportViewer</div> 
<script>
    var reportviewerObj = $("#reportviewer").data("ejReportViewer");
    reportviewerObj.gotoPreviousPage(); // To navigate to the previous page
</script>

{% endhighlight %}

### print<span class="signature">()</span>
{:#methods:print}

Print the report.

Example
{:.example}

{% highlight html %}
 
<div id="reportviewer">ReportViewer</div> 
<script>
    var reportviewerObj = $("#reportviewer").data("ejReportViewer");
    reportviewerObj.print(); //To perform print operation.
</script>

{% endhighlight %}

### printLayout<span class="signature">()</span>
{:#methods:printlayout}

Apply print layout to the report.

Example
{:.example}

{% highlight html %}
 
<div id="reportviewer">ReportViewer</div> 
<script>
    var reportviewerObj = $("#reportviewer").data("ejReportViewer");
    reportviewerObj.printLayout(); //Changes between print layout and normal modes.
</script>

{% endhighlight %}

### refresh<span class="signature">()</span>
{:#methods:refresh}

Refresh the report.

Example
{:.example}

{% highlight html %}
 
<div id="reportviewer">ReportViewer</div> 
<script>
    var reportviewerObj = $("#reportviewer").data("ejReportViewer");
    reportviewerObj.refresh(); // To refresh the report.
</script>

{% endhighlight %}

## Events

### destroy
{:#events:destroy}

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">true if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the report model</td>
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
 
<div id="reportviewer"></div>
<script>
    $("#reportviewer").ejReportViewer({
        destroy: function (args) {
            // Write a code block to perform any operation after destroy of reportviewer.
        }
    });
</script>

{% endhighlight %}

### drillThrough
{:#events:drillthrough}

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">true if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
actionInfo{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the actionInfo's parameters bookmarkLink,hyperLink,reportName,parameters.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the report model</td>
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
 
<div id="reportviewer"></div> 
<script>        
    $("#reportviewer").ejReportViewer({ 
        drillThrough: function (args) {
            // Write a code block to perform any operation when drill through action occurs in report.
        }
    });                   
</script>

{% endhighlight %}

### renderingBegin
{:#events:renderingbegin}

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">true if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the report model</td>
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
 
<div id="reportviewer"></div> 
<script>  
    //rendering begin event for report.               
    $("#reportviewer").ejReportViewer({
        renderingBegin:function(args) {
            // Write a code block to perform any operation before rendering.
        }
    });                 
</script>

{% endhighlight %}

### renderingComplete
{:#events:renderingcomplete}

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">true if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the report model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
reportParameters{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the collection of parameters</td>
</tr>
<tr>
<td class="name">{% highlight html %}
reportParameters{% endhighlight %}</td>
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

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>        
    //rendering complete event for reportviewer control.
    $("#reportviewer").ejReportViewer({ 
        renderingComplete:function(args) {
            // Write a code block to perform any operation after rendering completed.
        }
    });            
</script>

{% endhighlight %}

### reportError
{:#events:reporterror}

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">true if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
error{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the error details</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the report model</td>
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
 
<div id="reportviewer"></div> 
<script>        
    $("#reportviewer").ejReportViewer({
        reportError: function (args) {
            // Write a code block to perform any operation when report error occurs.
        }
    });                         
</script>

{% endhighlight %}

### reportLoaded
{:#events:reportloaded}

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">true if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the report model</td>
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
 
<div id="reportviewer"></div> 
<script>        
    $("#reportviewer").ejReportViewer({
        reportLoaded: function(args) {
            // Write a code block to perform any action when the report is loaded successfully.
        }
    });             
</script>

{% endhighlight %}

### viewReportClick
{:#events:viewreportclick}

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">true if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
parameters{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the parameter collection.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the report model</td>
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
 
<div id="reportviewer"></div> 
<script>        
    $("#reportviewer").ejReportViewer({ 
        viewReportClick:  function (args) {
            // Write a code block to perform any operation after destroy of reportviewer.
        }
    });           
</script>

{% endhighlight %}

### ReportPrint
{:#events:reportprint}

Fires when the report is printed.If you want to perform any operation after the successful printing of report, you can make use of the ReportPrint event.

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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">true if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the report model</td>
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
 
<div id="reportviewer"></div> 
<script>        
    $("#reportviewer").ejReportViewer({ 
        reportPrint:  function (args) {
            // Write a code block to perform any action when the report is printed successfully.
        }
    });           
</script>

{% endhighlight %}

### ReportExport
{:#events:reportexport}

Fires when the report is exported.If you want to perform any operation after the successful exporting of report, you can make use of the ReportExport event.

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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">true if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the report model</td>
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
 
<div id="reportviewer"></div> 
<script>        
    $("#reportviewer").ejReportViewer({ 
        reportExport:  function (args) {
            // Write a code block to perform any action when the report is exported successfully.
        }
    });           
</script>

{% endhighlight %}




