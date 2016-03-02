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

#### Example

{% highlight html %}

<div id="reportviewer">ReportViewer</div> 
<script>
    // Create ReportViewer
    $('#reportviewer').ejReportViewer();    
</script>

{% endhighlight %}

#### Requires

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

### dataSources `Array`
{:#members:datasources}

Gets or sets the list of data sources for the RDLC report.

#### Default Value

* []

#### Example

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

### dataSources.name `String`
{:#members:datasources-name}

Gets or sets the name of the data source.

#### Default Value

* empty

#### Example

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

### dataSources.values `Object`
{:#members:datasources-values}

Gets or sets the values of data source.

#### Default Value

* null

#### Example

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

### enablePageCache `Boolean`
{:#members:enablePageCache}

Enables or disables the page cache of report.

#### Default Value

* false

#### Example

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>        
    $("#reportviewer").ejReportViewer({ enablePageCache: false });            
</script>

{% endhighlight %}

### exportSettings `Object`
{:#members:exportsettings}

Specifies the export settings.

### exportSettings.exportOptions `enum`
{:#members:exportsettings-exportoptions}

Specifies the export formats.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">All</td>
<td class="description">Specifies the All property in ExportOptions to get all availble options.</td>
</tr>
<tr>
<td class="name">Pdf</td>
<td class="description">Specifies the Pdf property in ExportOptions to get Pdf option.</td>
</tr>
<tr>
<td class="name">Word</td>
<td class="description">Specifies the Word property in ExportOptions to get Word option.</td>
</tr>
<tr>
<td class="name">Excel</td>
<td class="description">Specifies the Excel property in ExportOptions to get Excel option.</td>
</tr>
<tr>
<td class="name">Html</td>
<td class="description">Specifies the Html property in ExportOptions to get Html option.</td>
</tr>
</tbody>
</table>

#### Default Value

* ej.ReportViewer.ExportOptions.All

#### Example

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>        
    $("#reportviewer").ejReportViewer(
        {
            exportSettings:{ exportOptions: ej.ReportViewer.ExportOptions.Html | ej.ReportViewer.ExportOptions.Pdf }
        });            
</script>

{% endhighlight %}

### exportSettings.excelFormat `enum`
{:#members:exportsettings-excelformat}

Specifies the excel export format.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Excel97to2003</td>
<td class="description">Specifies the Excel97to2003 property in ExcelFormats to get specified version of exported format.</td>
</tr>
<tr>
<td class="name">Excel2007</td>
<td class="description">Specifies the Excel2007 property in ExcelFormats to get specified version of exported format.</td>
</tr>
<tr>
<td class="name">Excel2010</td>
<td class="description">Specifies the Excel2010 property in ExcelFormats to get specified version of exported format.</td>
</tr>
<tr>
<td class="name">Excel2013</td>
<td class="description">Specifies the Excel2013 property in ExcelFormats to get specified version of exported format.</td>
</tr>
</tbody>
</table>

#### Default Value

* ej.ReportViewer.ExcelFormats.Excel97to2003

#### Example

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>        
    $("#reportviewer").ejReportViewer(
        {
            exportSettings:{ excelFormat: ej.ReportViewer.ExcelFormats.Excel97to2003}
        });            
</script>

{% endhighlight %}

### exportSettings.wordFormat `enum`
{:#members:exportsettings-wordformat}

Specifies the word export format.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Doc</td>
<td class="description">Specifies the Doc property in WordFormats to get specified version of exported format.</td>
</tr>
<tr>
<td class="name">Dot</td>
<td class="description">Specifies the Dot property in WordFormats to get specified version of exported format.</td>
</tr>
<tr>
<td class="name">Docx</td>
<td class="description">Specifies the Docx property in WordFormats to get specified version of exported format.</td>
</tr>
<tr>
<td class="name">Word2007</td>
<td class="description">Specifies the Word2007 property in WordFormats to get specified version of exported format.</td>
</tr>
<tr>
<td class="name">Word2010</td>
<td class="description">Specifies the Word2010 property in WordFormats to get specified version of exported format.</td>
</tr>
<tr>
<td class="name">Word2013</td>
<td class="description">Specifies the Word2013 property in WordFormats to get specified version of exported format.</td>
</tr>
<tr>
<td class="name">Word2007Dotx</td>
<td class="description">Specifies the Word2007Dotx property in WordFormats to get specified version of exported format.</td>
</tr>
<tr>
<td class="name">Word2010Dotx</td>
<td class="description">Specifies the Word2010Dotx property in WordFormats to get specified version of exported format.</td>
</tr>
<tr>
<td class="name">Word2013Dotx</td>
<td class="description">Specifies the Word2013Dotx property in WordFormats to get specified version of exported format.</td>
</tr>
<tr>
<td class="name">Word2007Docm</td>
<td class="description">Specifies the Word2007Docm property in WordFormats to get specified version of exported format.</td>
</tr>
<tr>
<td class="name">Word2010Docm</td>
<td class="description">Specifies the Word2010Docm property in WordFormats to get specified version of exported format.</td>
</tr>
<tr>
<td class="name">Word2013Docm</td>
<td class="description">Specifies the Word2013Docm property in WordFormats to get specified version of exported format.</td>
</tr>
<tr>
<td class="name">Word2007Dotm</td>
<td class="description">Specifies the Word2007Dotm property in WordFormats to get specified version of exported format.</td>
</tr>
<tr>
<td class="name">Word2010Dotm</td>
<td class="description">Specifies the Word2010Dotm property in WordFormats to get specified version of exported format.</td>
</tr>
<tr>
<td class="name">Word2013Dotm</td>
<td class="description">Specifies the Word2013Dotm property in WordFormats to get specified version of exported format.</td>
</tr>
<tr>
<td class="name">Rtf</td>
<td class="description">Specifies the Rtf property in WordFormats to get specified version of exported format.</td>
</tr>
<tr>
<td class="name">Txt</td>
<td class="description">Specifies the Txt property in WordFormats to get specified version of exported format.</td>
</tr>
<tr>
<td class="name">EPub</td>
<td class="description">Specifies the EPub property in WordFormats to get specified version of exported format.</td>
</tr>
<tr>
<td class="name">Html</td>
<td class="description">Specifies the Html property in WordFormats to get specified version of exported format.</td>
</tr>
<tr>
<td class="name">Xml</td>
<td class="description">Specifies the Xml property in WordFormats to get specified version of exported format.</td>
</tr>
<tr>
<td class="name">Automatic</td>
<td class="description">Specifies the Automatic property in WordFormats to get specified version of exported format.</td>
</tr>
</tbody>
</table>

#### Default Value

* ej.ReportViewer.WordFormats.Doc

#### Example

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>        
    $("#reportviewer").ejReportViewer(
        {
            exportSettings:{ wordFormat: ej.ReportViewer.WordFormats.Doc}
        });            
</script>

{% endhighlight %}

### isResponsive `Boolean`
{:#members:isResponsive}

When set to true, adapts the report layout to fit the screen size of devices on which it renders.

#### Default Value

* true

#### Example

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>        
    $("#reportviewer").ejReportViewer({ isResponsive: true });            
</script>

{% endhighlight %}

### locale `String`
{:#members:locale}

Specifies the locale for report viewer.

#### Default Value

* "en-US"

#### Example

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>          
    $("#reportviewer").ejReportViewer(
        {
            locale: "it-IT"
        });             
</script>

{% endhighlight %}

### pageSettings `Object`
{:#members:pagesettings}

Specifies the page settings.

### pageSettings.orientation `enum`
{:#members:pagesettings-orientation}

Specifies the print layout orientation.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Landscape</td>
<td class="description">Specifies the Landscape property in pageSettings.orientation to get specified layout.</td>
</tr>
<tr>
<td class="name">portrait</td>
<td class="description">Specifies the portrait property in pageSettings.orientation to get specified layout.</td>
</tr>
</tbody>
</table>

#### Default Value

* null

#### Example

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>        
    $("#reportviewer").ejReportViewer(
        {
            pageSettings:{ orientation: ej.ReportViewer.Orientation.Landscape }
        });
</script>

{% endhighlight %}

### pageSettings.paperSize `enum`
{:#members:pagesettings-papersize}

Specifies the paper size of print layout.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">A3</td>
<td class="description">Specifies the A3 as value in pageSettings.paperSize to get specified size.</td>
</tr>
<tr>
<td class="name">portrait</td>
<td class="description">Specifies the A4 as value in pageSettings.paperSize to get specified size.</td>
</tr>
<tr>
<td class="name">B4(JIS)</td>
<td class="description">Specifies the B4(JIS) as value in pageSettings.paperSize to get specified size.</td>
</tr>
<tr>
<td class="name">B5(JIS)</td>
<td class="description">Specifies the B5(JIS) as value in pageSettings.paperSize to get specified size.</td>
</tr>
<tr>
<td class="name">Envelope #10</td>
<td class="description">Specifies the Envelope #10 as value in pageSettings.paperSize to get specified size.</td>
</tr>
<tr>
<td class="name">Envelope Monarch</td>
<td class="description">Specifies the Envelope as value in pageSettings.paperSize to get specified size.</td>
</tr>
<tr>
<td class="name">Executive</td>
<td class="description">Specifies the Executive as value in pageSettings.paperSize to get specified size.</td>
</tr>
<tr>
<td class="name">Legal</td>
<td class="description">Specifies the Legal as value in pageSettings.paperSize to get specified size.</td>
</tr>
<tr>
<td class="name">Letter</td>
<td class="description">Specifies the Letter as value in pageSettings.paperSize to get specified size.</td>
</tr>
<tr>
<td class="name">Tabloid</td>
<td class="description">Specifies the Tabloid as value in pageSettings.paperSize to get specified size.</td>
</tr>
<tr>
<td class="name">Custom</td>
<td class="description">Specifies the Custom as value in pageSettings.paperSize to get specified size.</td>
</tr>
</tbody>
</table>

#### Default Value

* null

#### Example

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>        
    $("#reportviewer").ejReportViewer(
        {
            pageSettings:{ paperSize: ej.ReportViewer.PaperSize.A4 }
        });
</script>

{% endhighlight %}

### parameters `Array`
{:#members:parameters}

Gets or sets the list of parameters associated with the report.

#### Default Value

* []

#### Example

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

### parameters.labels `Array`
{:#members:parameters-labels}

Gets or sets the parameter labels.

#### Default Value

* null

#### Example

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

### parameters.name `String`
{:#members:parameters-name}

Gets or sets the name of the parameter.

#### Default Value

* empty

#### Example

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

### parameters.nullable `Boolean`
{:#members:parameters-nullable}

Gets or sets whether the parameter allows nullable value or not.

#### Default Value

* false

#### Example

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

### parameters.prompt `String`
{:#members:parameters-prompt}

Gets or sets the prompt message associated with the specified parameter.

#### Default Value

* empty

#### Example

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

### parameters.values `Array`
{:#members:parameters-values}

Gets or sets the parameter values.

#### Default Value

* null

#### Example

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

### printMode `Boolean`
{:#members:printmode}

Enables and disables the print mode.

#### Default Value

* false

#### Example

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>          
    $("#reportviewer").ejReportViewer(
        {
            printMode:true
        });             
</script>

{% endhighlight %}

### printOptions `enum`
{:#members:printOptions}

Specifies the print option of the report.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Default</td>
<td class="description">Specifies the Default property in printOptions.</td>
</tr>
<tr>
<td class="name">NewTab</td>
<td class="description">Specifies the NewTab property in printOptions.</td>
</tr>
<tr>
<td class="name">None</td>
<td class="description">Specifies the None property in printOptions.</td>
</tr>
</tbody>
</table>

#### Default Value

* ej.ReportViewer.PrintOptions.Default

#### Example

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>        
    $("#reportviewer").ejReportViewer({ printOption: ej.ReportViewer.PrintOptions.Default });            
</script>

{% endhighlight %}

### processingMode `enum`
{:#members:processingmode}

Specifies the processing mode of the report.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Remote</td>
<td class="description">Specifies the Remote property in processingMode.</td>
</tr>
<tr>
<td class="name">Local</td>
<td class="description">Specifies the Local property in processingMode.</td>
</tr>
</tbody>
</table>

#### Default Value

* ej.ReportViewer.ProcessingMode.Remote

#### Example

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>        
    $("#reportviewer").ejReportViewer({ processingMode: ej.ReportViewer.ProcessingMode.Remote });            
</script>

{% endhighlight %}

### renderMode `enum`
{:#members:rendermode}

Specifies the render layout.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Default</td>
<td class="description">Specifies the Default property in RenderMode to get default output.</td>
</tr>
<tr>
<td class="name">Mobile</td>
<td class="description">Specifies the Mobile property in RenderMode to get specified output.</td>
</tr>
<tr>
<td class="name">Desktop</td>
<td class="description">Specifies the Desktop property in RenderMode to get specified output.</td>
</tr>
</tbody>
</table>

#### Default Value

* ej.ReportViewer.RenderMode.Default

#### Example

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>        
    $("#reportviewer").ejReportViewer({ renderMode: ej.ReportViewer.RenderMode.Default });            
</script>

{% endhighlight %}

### reportPath `String`
{:#members:reportpath}

Gets or sets the path of the report file.

#### Default Value

* empty

#### Example

{% highlight html %}

<div id="reportviewer"></div> 
<script>
    $("#reportviewer").ejReportViewer({ reportPath: "~/App_Data/Sample.rdl" });            
</script>

{% endhighlight %}

### reportServerUrl `String`
{:#members:reportserverurl}

Gets or sets the reports server url.

#### Default Value

* empty

#### Example

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>
    $("#reportviewer").ejReportViewer({ reportServerUrl: "http://mvc.syncfusion.com/reportserver" });            
</script>

{% endhighlight %}

### reportServiceUrl `String`
{:#members:reportserviceurl}

Specifies the report Web API service url.

#### Default Value

* empty

#### Example

{% highlight html %}

<div id="reportviewer"></div> 
<script>
    $("#reportviewer").ejReportViewer({ reportServiceUrl: "../api/RDLReport" });            
</script>

{% endhighlight %}

### toolbarSettings `Object`
{:#members:toolbarsettings}

Specifies the toolbar settings.

### toolbarSettings.click `String`
{:#members:toolbarsettings-click}

Fires when user click on toolbar item in the toolbar.

#### Default Value

* empty

#### Example

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>          
    $("#reportviewer").ejReportViewer(
        {
            toolbarSettings:{click: "onToolbarClick"}
        });         
</script>

{% endhighlight %}

### toolbarSettings.items `enum`
{:#members:toolbarsettings-items}

Specifies the toolbar items.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Print</td>
<td class="description">Specifies the Print as value in ToolbarItems to get specified item.</td>
</tr>
<tr>
<td class="name">Refresh</td>
<td class="description">Specifies the Refresh as value in ToolbarItems to get specified item.</td>
</tr>
<tr>
<td class="name">Zoom</td>
<td class="description">Specifies the Zoom as value in ToolbarItems to get specified item.</td>
</tr>
<tr>
<td class="name">FittoPage</td>
<td class="description">Specifies the FittoPage as value in ToolbarItems to get specified item.</td>
</tr>
<tr>
<td class="name">Export</td>
<td class="description">Specifies the Export as value in ToolbarItems to get specified item.</td>
</tr>
<tr>
<td class="name">PageNavigation</td>
<td class="description">Specifies the PageNavigation as value in ToolbarItems to get specified item.</td>
</tr>
<tr>
<td class="name">Parameters</td>
<td class="description">Specifies the Parameters as value in ToolbarItems to get specified item.</td>
</tr>
<tr>
<td class="name">PrintLayout</td>
<td class="description">Specifies the PrintLayout as value in ToolbarItems to get specified item.</td>
</tr>
<tr>
<td class="name">PageSetup</td>
<td class="description">Specifies the PageSetup as value in ToolbarItems to get specified item.</td>
</tr>
</tbody>
</table>

#### Default Value

* ej.ReportViewer.ToolbarItems.All

#### Example

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>        
    $("#reportviewer").ejReportViewer(
        {
            toolbarSettings:{ exportOptions: ej.ReportViewer.ToolbarItems.All }
        });
</script>

{% endhighlight %}

### toolbarSettings.showToolbar `Boolean`
{:#members:toolbarsettings-showtoolbar}

Shows or hides the toolbar.

#### Default Value

* true

#### Example

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>          
    $("#reportviewer").ejReportViewer(
        {
            toolbarSettings:{showToolbar: true}
        });         
</script>

{% endhighlight %}

### toolbarSettings.showTooltip `Boolean`
{:#members:toolbarsettings-showtooltip}

Shows or hides the tooltip of toolbar items.

#### Default Value

* true

#### Example

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>          
    $("#reportviewer").ejReportViewer(
        {
            toolbarSettings:showTooltip: true}
        });         
</script>

{% endhighlight %}

### toolbarSettings.templateId `String`
{:#members:toolbarsettings-templateid}

Specifies the toolbar template ID.

#### Default Value

* empty

#### Example

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>          
    $("#reportviewer").ejReportViewer(
        {
            toolbarSettings:{templateId: "customtoolbarId"}
        });         
</script>

{% endhighlight %}

### zoomFactor `Number`
{:#members:zoomfactor}

Gets or sets the zoom factor for report viewer.

#### Default Value

* 1

#### Example

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>        
    $("#reportviewer").ejReportViewer({ zoomFactor:  2 });            
</script>

{% endhighlight %}

## Methods

### exportReport()
{:#methods:exportreport}

Export the report to the specified format.

#### Example

{% highlight html %}
 
<div id="reportviewer">ReportViewer</div> 
<script>
    var reportviewerObj = $("#reportviewer").data("ejReportViewer");
    reportviewerObj.exportReport(); //Exports the reports
</script>

{% endhighlight %}

### fitToPage()
{:#methods:fittopage}

Fit the report page to the container.

#### Example

{% highlight html %}
 
<div id="reportviewer">ReportViewer</div> 
<script>
    var reportviewerObj = $("#reportviewer").data("ejReportViewer");
    reportviewerObj.fitToPage(); // To fit the report page.
</script>

{% endhighlight %}

### fitToPageHeight()
{:#methods:fittopageheight}

Fit the report page height to the container.

#### Example

{% highlight html %}
 
<div id="reportviewer">ReportViewer</div> 
<script>
    var reportviewerObj = $("#reportviewer").data("ejReportViewer");
    reportviewerObj.fitToPageHeight(); // To fit the report page height.
</script>

{% endhighlight %}

### fitToPageWidth()
{:#methods:fittopagewidth}

Fit the report page width to the container.

#### Example

{% highlight html %}
 
<div id="reportviewer">ReportViewer</div> 
<script>
    var reportviewerObj = $("#reportviewer").data("ejReportViewer");
    reportviewerObj.fitToPageWidth(); // To fit the report page width.
</script>

{% endhighlight %}

### getDataSetNames()
{:#methods:getdatasetnames}

Get the available datasets name of the rdlc report.

#### Example

{% highlight html %}
 
<div id="reportviewer">ReportViewer</div> 
<script>
    var reportviewerObj = $("#reportviewer").data("ejReportViewer");
    reportviewerObj.getDataSetNames(); // To get the dataset names.
</script>

{% endhighlight %}

### getParameters()
{:#methods:getparameters}

Get the available parameters of the report.

#### Example

{% highlight html %}
 
<div id="reportviewer">ReportViewer</div> 
<script>
    var reportviewerObj = $("#reportviewer").data("ejReportViewer"); 
    reportviewerObj.getParameters(); // To get the parameters.
</script>

{% endhighlight %}

### gotoFirstPage()
{:#methods:gotofirstpage}

Navigate to first page of report.

#### Example

{% highlight html %}

<div id="reportviewer">ReportViewer</div> 
<script>
    var reportviewerObj = $("#reportviewer").data("ejReportViewer");
    reportviewerObj.gotoFirstPage(); // To navigate to first page
</script>

{% endhighlight %}

### gotoLastPage()
{:#methods:gotolastpage}

Navigate to last page of the report.

#### Example

{% highlight html %}
 
<div id="reportviewer">ReportViewer</div> 
<script>
    var reportviewerObj = $("#reportviewer").data("ejReportViewer");
    reportviewerObj.gotoLastPage(); // Navigate to the last page
</script>

{% endhighlight %}

### gotoNextPage()
{:#methods:gotonextpage}

Navigate to next page from the current page.

#### Example

{% highlight html %}
 
<div id="reportviewer">ReportViewer</div> 
<script>
    var reportviewerObj = $("#reportviewer").data("ejReportViewer");
    reportviewerObj.gotoNextPage(); //To navigate to the next page
</script>

{% endhighlight %}

### gotoPageIndex()
{:#methods:gotopageindex}

Go to specific page index of the report.

#### Example

{% highlight html %}
 
<div id="reportviewer">ReportViewer</div> 
<script>
    var reportviewerObj = $("#reportviewer").data("ejReportViewer");
    reportviewerObj.gotoPageIndex(5); // To navigate the specific page
</script>

{% endhighlight %}

### gotoPreviousPage()
{:#methods:gotopreviouspage}

Navigate to previous page from the current page.

#### Example

{% highlight html %}
 
<div id="reportviewer">ReportViewer</div> 
<script>
    var reportviewerObj = $("#reportviewer").data("ejReportViewer");
    reportviewerObj.gotoPreviousPage(); // To navigate to the previous page
</script>

{% endhighlight %}

### print()
{:#methods:print}

Print the report.

#### Example

{% highlight html %}
 
<div id="reportviewer">ReportViewer</div> 
<script>
    var reportviewerObj = $("#reportviewer").data("ejReportViewer");
    reportviewerObj.print(); //To perform print operation.
</script>

{% endhighlight %}

### printLayout()
{:#methods:printlayout}

Apply print layout to the report.

#### Example

{% highlight html %}
 
<div id="reportviewer">ReportViewer</div> 
<script>
    var reportviewerObj = $("#reportviewer").data("ejReportViewer");
    reportviewerObj.printLayout(); //Changes between print layout and normal modes.
</script>

{% endhighlight %}

### refresh()
{:#methods:refresh}

Refresh the report.

#### Example

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
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Event parameters from reportviewer.
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">true if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the report model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

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
<td class="name">argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from reportviewer.
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">true if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">actionInfo</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the actionInfo's parameters bookmarkLink, hyperLink, reportName, parameters.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the report model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

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
<td class="name">argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from reportviewer.
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">true if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the report model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

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
<td class="name">argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from reportviewer.
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">true if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the report model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">reportParameters</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the collection of parameters.</td>
</tr>
<tr>
<td class="name">reportParameters</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the collection of parameters.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

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
<td class="name">argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from reportviewer.
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">true if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">error</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the error details.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the report model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

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

### reportExport
{:#events:reportexport}

Fires when the report is being exported.If you want to perform any operation before exporting of report, you can make use of the reportExport event.

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
<td class="name">argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from reportviewer.
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">true if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the report model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
<div id="reportviewer"></div> 
<script>        
    $("#reportviewer").ejReportViewer({ 
        reportExport:  function (args) {
            // Write a code block to perform any action before exporting of report.
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
<td class="name">
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">event parameters from reportviewer.
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">true if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the report model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

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
<td class="name">argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from reportviewer.
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
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">true if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">parameters</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the parameter collection.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the report model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

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











