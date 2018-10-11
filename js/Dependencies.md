---
layout: post
title: Dependent scripts and .NET libraries for Essential JS widgets
description: Common scripts and .NET libraries for Syncfusion components are listed.
platform: js
control: Introduction
documentation: ug
---

# Dependencies

## Common Libraries

**Essential JavaScript** components mainly relies on the following 2 common libraries –

* jQuery (from the version 1.7.1 to 3.1.0)
* JsRender - to render the templates.

N> jQuery.easing external dependency has been removed from version 14.3.0.49 onwards. Kindly include this jQuery.easing dependency for versions lesser than 14.3.0.49. 

The following table provides jQuery compatibility information.

<table class="props">
<thead>
<tr>
<th colspan="2">EJ Versions</th>
<th colspan="2">Compatible jQuery Versions</th>
</tr>
<tr>
<th>From</th>
<th>To</th>
<th>From</th>
<th>To</th>
</tr>
</thead>

<tbody>
<tr>
<td class="fromejversion">14.3.0.49</td>
<td class="toejversion">14.3.0.52</td>
<td class="fromjqueryversion">1.7.1</td>
<td class="tojqueryversion">3.1.0</td>
</tr>

<tr>
<td class="fromejversion">13.2.0.29</td>
<td class="toejversion">14.2.0.32</td>
<td class="fromjqueryversion">1.7.1</td>
<td class="tojqueryversion">2.2.4</td>
</tr>

<tr>
<td class="fromejversion">lower version</td>
<td class="toejversion">13.1.0.30</td>
<td class="fromjqueryversion">1.7.1</td>
<td class="tojqueryversion">2.1.3</td>
</tr>
</tbody>
</table>

> jQuery-2.1.4, jQuery-3.0.0 support has been given from ejVersion 13.2.0.29, 14.3.0.49 onwards respectively.

## Server-side Libraries

Some JavaScript UI web widgets like Grid and Schedule requires the below assemblies to support export functionality. 

* Syncfusion.Compression.Base
* Syncfusion.Linq.Base
* Syncfusion.EJ.Export
* Syncfusion.XlsIO.Base
* Syncfusion.Pdf.Base
* Syncfusion.DocIO.Base
* Syncfusion.EJ

**Reporting** controls (ReportViewer) requires the following assemblies listed below are to be referred mandatorily in the application. 

* System.Web.Routing  
* System.Web.Http
* System. Web.Http.WebHost
* System.Net.Http
* System.Net.Http.WebRequest
* System.Net.Http.Formatting
* Syncfusion.Compression.Base
* Syncfusion.Linq.Base
* Syncfusion.EJ.ReportViewer
* Syncfusion.Pdf.Base
* Syncfusion.XlsIO.Base
* Syncfusion.DocIO.Base
* Syncfusion.Shared.Wpf
* Syncfusion.Chart.Wpf
* Syncfusion.Gauge.Wpf
* Syncfusion.SfMaps.Wpf 

**Business Intelligence** components (Pivot Grid, OLAP Client, OLAP Chart and OLAP Gauge) require the below listed assemblies -  

* Syncfusion.Compression.Base
* Syncfusion.Linq.Base
* Syncfusion.EJ
* Syncfusion.EJ.Olap
* Syncfusion.Olap.Base
* Syncfusion.PivotAnalysis.Base
* Syncfusion.XlsIO.Base
* Syncfusion.Pdf.Base
* Syncfusion.DocIO.Base
* Microsoft.AnalysisServices.AdomdClient
* System.Data.SqlServerCe (Version: 4.0.0.0).

**File Format** products (XlsIO, DocIO, PDF and Presentation) require the below listed assemblies -  

* Syncfusion.Compression.Base
* Syncfusion.XlsIO.Base
* Syncfusion.ExcelToPDFConverter.Base
* Syncfusion.ExcelChartToImageConverter.WPF
* Syncfusion.OfficeChart.Base
* Syncfusion.DocIO.Base
* Syncfusion.DocToPDFConverter.Base
* Syncfusion.Pdf.Base
* Syncfusion.HtmlConverter.Base
* Syncfusion.GeckoHtmlRenderer.Base
* Syncfusion.OCRProcessor.Base
* Syncfusion.Presentation.Base
* Syncfusion.PresentationToPdfConverter.Base
* Syncfusion.OfficeChartToImageConverter.WPF
* Syncfusion.SfChart.WPF
* Syncfusion.Shared.WPF

All the above specified Syncfusion assemblies are available separately for the .NET Frameworks **4.0**, **4.5** and **4.5.1**.

