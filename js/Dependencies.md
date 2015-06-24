---
layout: post
title: Dependencies
description: dependencies
platform: js
control: Introduction
documentation: ug
---

# Dependencies

## Common Libraries

**Essential JavaScript** components mainly relies on the following 4 common libraries –

* jQuery 1.7.1 and later versions
* jsRender - to render the templates.
* jQuery.easing - to support the animation effects in the components.
* jQuery.Globalize - to support the globalization.

Current version of Syncfusion components supports the latest version of jQuery (**jQuery 2.1.4**).

## Server-side Libraries

Some JavaScript UI web widgets like Grid and Schedule that supports **Exporting** functionality. This requires the below assemblies to be referred in the application. 

* Syncfusion.Compression.Base
* Syncfusion.Linq.Base
* Syncfusion.EJ.Export
* Syncfusion.XlsIO.Base
* Syncfusion.Pdf.Base
* Syncfusion.DocIO.Base
* Syncfusion.EJ

If the user wants to use the **Reporting** controls (ReportViewer), then the following `System` and other Syncfusion assemblies listed below are needed to be referred mandatorily in the application. 

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
* Synfusion.Shared.Wpf
* Syncfusion.Chart.Wpf
* Syncfusion.Gauge.Wpf
* Syncfusion.SfMaps.Wpf 

The dependency files required for making use of **Business Intelligence Components** (PivotGrid, Olap Client, Olap Chart and Olap Gauge) in JavaScript platform are listed below -  

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

The dependent assemblies required to use the **File Format** products (XlsIO, DocIO, PDF and Presentation) are as follows -  

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

All the above specified Syncfusion assemblies are available separately for the .NET framerworks **4.0**, **4.5** and **4.5.1**.

