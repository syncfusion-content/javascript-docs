---
layout: post
title: Dependencies
description: dependencies
platform: js
control: Introduction
documentation: ug
---

## Dependencies

**Essential JavaScript** components mainly relies on the following 4 common libraries –

* jQuery 1.7.1 and later versions

* jsRender

* jQuery.easing

* jQuery.Globalize

As of now, all our Syncfusion components supports the latest version of jQuery (**jQuery 2.1.4**) - which supports almost all the old and modern browsers.

**jsRender** script file is required to render the templates.

**jQuery.easing** script file is required, so as to support the animation effects in the components.

**jQuery.Globalize** script file is to support the globalization concept.

Apart from the above specified common JavaScript libraries, there are some other JavaScript UI web widgets like Grid and Schedule that supports **Export** functionality, which requires the additional assemblies to be referred in the application. If you have installed **Essential Studio package** in your machine, then the following assemblies are available by default in your machine which needs to be referred in the application to avail with the **Exporting** support,

* Syncfusion.Core

* Syncfusion.Compression.Base

* Syncfusion.Linq.Base

* Syncfusion.EJ.Export

* Syncfusion.XlsIO.Base

* Syncfusion.Pdf.Base

* Syncfusion.DocIO.Base

* Syncfusion.EJ

If the user wants to use the **Reporting** controls, then the following System assemblies and other Syncfusion assemblies listed below are needed to be referred mandatorily in the application. 

* System.Web.Routing  

* System.Web.Http

* System. Web.Http.WebHost

* System.Net.Http

* System.Net.Http.WebRequest

* System.Net.Http.Formatting

* Syncfusion.Core

* Syncfusion.Linq.Base

* Syncfusion.EJ.ReportViewer

* Syncfusion.ReportControls.Wpf

* Syncfusion.ReportWriter.Base

* Syncfusion.Pdf.Base

* Syncfusion.XlsIO.Base

* Syncfusion.DocIO.Base

* Synfusion.Shared.Wpf

* Syncfusion.Chart.Wpf

* Syncfusion.Gauge.Wpf

* Syncfusion.SfMaps.Wpf 

The dependency files required for making use of **Business Intelligence Components** (PivotGrid, Olap Client, Olap Chart and Olap Gauge) in **JavaScript** platform is listed below -  

* Syncfusion.Core 

* Syncfusion.Compression.Base

* Syncfusion.Linq.Base

* Syncfusion.EJ

* Syncfusion.EJ.Olap

* Syncfusion.Olap.Base

* Syncfusion.PivotAnalysis.Base

* Syncfusion.XlsIO.Base

* Microsoft.AnalysisServices.AdomdClient

* System.Data.SqlServerCe.dll (Version: 4.0.0.0).



All the above specified Syncfusion assemblies are available separately for the .NET framerworks 4.0, 4.5 and 4.5.1.

