---
layout: post
title: Service reference for ejChart widget
description: What are the services used in Essential JavaScript Chart.
documentation: api
platform: js
keywords: ejChart, Services, Essential JS Chart, Chart, Excel Exporting Service, Chart Exporting
metaname: 
metacontent:
control: ejChart
---

#ejChart
<ts root="datavisualization" />

Essential chart uses services to export Chart as a PDF, Word or Excel document.

##Exporting service

### Description

To export Chart as PNG, JPG, SVG, PDF document, Excel document or Word document.

### URL
[http://js.syncfusion.com/ExportingServices/api/JSChartExport/ExportChart](http://js.syncfusion.com/ExportingServices/api/JSChartExport/ExportChart)

### Parameter
<table>
<tr>
<td>type</td><td>image</td>
<td>URL</td><td>http://js.syncfusion.com/ExportingServices/api/JSChartExport/ExportChart</td>
<td>exportMultipleChart</td><td>false</td>
</tr>
</table>

### Request

{% highlight js %}
 
var chart = $(".e-datavisualization-chart").ejChart("instance");
var exportSettings = chart.model.exportSettings;
exportSettings.fileName = "Chart";
exportSettings.angle = "90";
exportSettings.type = "png";
exportSettings.mode = 'server';
exportSettings.action = 'http://js.syncfusion.com/ExportingServices/api/JSChartExport/ExportChart';
data = chart.export();

{% endhighlight %}

###Response

####Code: 200

####Content-Type: application/octet-stream

####Response (PNG, JPG, SVG, PDF, Word or Excel):

Browser will prompt a dialog box to save the file (image or document).