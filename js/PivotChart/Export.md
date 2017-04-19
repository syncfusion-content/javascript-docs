---
layout: post
title: Export
description: export
platform: js
control: PivotChart
documentation: ug
api: /api/js/ejpivotchart
---

# Exporting

The PivotChart control can be exported to the following file formats.

* Excel
* Word
* PDF
* Image

The PivotChart control can be exported by invoking **“exportPivotChart”** method, with an appropriate export option as parameter.

{% highlight html %}

<html> 
    //...
<body> 
    //...
    <div id="PivotChart1" style="min-height: 275px; min-width: 525px; height: 460px; width: 720px"></div>
    <button id="btnExport">Export</button>
    <script type="text/javascript">
        $(function()
        {
            $("#PivotChart1").ejPivotChart(
            {
               //...
            });
            $("#btnExport").ejButton(
            {
                click: "exportBtnClick"
            });
        });

        function exportBtnClick(args)
        {
            var chartObj = $('#PivotChart1').data("ejPivotChart");
            
            //If you render PivotChart in Client Mode, set the export option like below.
            chartObj.exportPivotChart("http://js.syncfusion.com/ejservices/api/PivotChart/Olap/ExcelExport","fileName");
            
            //If you render PivotChart in Server Mode, set the export option like below.
            chartObj.exportPivotChart(ej.PivotChart.ExportOptions.Excel);
        }
    </script>
</body>
</html>                                           

{% endhighlight %}

When PivotChart is rendered in Server Mode, a service method needs to be added in WCF/WebAPI for server side operations.

For WebAPI controller, the below method needs to be added.

{% highlight c# %}

[System.Web.Http.ActionName("Export")]
[System.Web.Http.HttpPost]
public void Export() {
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    string fileName = "Sample";
    htmlHelper.ExportPivotChart(args, fileName, System.Web.HttpContext.Current.Response);
}

{% endhighlight %}

For WCF service, the below method needs to be added.

{% highlight c# %}

public void Export(System.IO.Stream stream) {
    System.IO.StreamReader sReader = new System.IO.StreamReader(stream);
    string args = System.Web.HttpContext.Current.Server.UrlDecode(sReader.ReadToEnd()).Remove(0, 5);
    string fileName = "Sample";
    htmlHelper.ExportPivotChart(args, fileName, System.Web.HttpContext.Current.Response);
}

{% endhighlight %}

## Excel Export

User can export contents of the PivotChart to Excel document for future archival, references and analysis purposes.

### Client Mode

To achieve Excel export, service URL and file name is sent as the parameter.

{% highlight javascript %}

function exportBtnClick(args)
{
    var chartObj = $('#PivotChart1').data("ejPivotChart ");
    chartObj.exportPivotChart("http://js.syncfusion.com/ejservices/api/PivotChart/Olap/ExcelExport","fileName");
}

{% endhighlight %}  

### Server Mode

To achieve Excel export, we need to add the following dependency libraries into the application.

* Syncfusion.Compression.Base
* Syncfusion.XlsIO.Base

For Excel export, **“ej.PivotChart.ExportOptions.Excel”** enumeration value is sent as the parameter.

{% highlight javascript %}

function exportBtnClick(args)
{
    var chartObj = $('#PivotChart1').data("ejPivotChart");
    //Setting export option as Excel in the exportPivotChart method for ServerMode
    chartObj.exportPivotChart(ej.PivotChart.ExportOptions.Excel);
}

{% endhighlight %}  

## Word Export

User can export contents of the PivotChart to Word document for future archival, references and analysis purposes.

### Client Mode

To achieve Word export, service URL and file name is sent as the parameter.

{% highlight javascript %}

function exportBtnClick(args)
{
    var chartObj = $('#PivotChart1').data("ejPivotChart ");
    chartObj.exportPivotChart("http://js.syncfusion.com/ejservices/api/PivotChart/Olap/WordExport","fileName");
}

{% endhighlight %}  

### Server Mode

 To achieve Word export, we need to add the following dependency libraries into the application.

* Syncfusion.Compression.Base
* Syncfusion.DocIo.Base

For Word export, **“ej.PivotChart.ExportOptions.Word”** enumeration value is sent as the parameter.

{% highlight javascript %}

function exportBtnClick(args)
{
    var chartObj = $('#PivotChart1').data("ejPivotChart");
    //Setting export option as Word in the exportPivotChart method
    chartObj.exportPivotChart(ej.PivotChart.ExportOptions.Word);
}

{% endhighlight %}

## PDF Export

User can export contents of the PivotChart to PDF document for future archival, references and analysis purposes.

### Client Mode

To achieve PDF export, service URL and file name is sent as the parameter.

{% highlight javascript %}

function exportBtnClick(args)
{
    var chartObj = $('#PivotChart1').data("ejPivotChart ");
    chartObj.exportPivotChart("http://js.syncfusion.com/ejservices/api/PivotChart/Olap/PDFExport","fileName");
}

{% endhighlight %}  

### Server Mode

To achieve PDF export, we need to add the following dependency libraries into the application.

* Syncfusion.Compression.Base
* Syncfusion.Pdf.Base

For PDF export, **“ej.PivotChart.ExportOptions.PDF”** enumeration value is sent as the parameter.

{% highlight javascript %}

function exportBtnClick(args)
{
    var chartObj = $('#PivotChart1').data("ejPivotChart ");
    //Setting export option as PDF in the exportPivotChart method
    chartObj.exportPivotChart(ej.PivotChart.ExportOptions.PDF);
}

{% endhighlight %} 

## Image Export

User can export contents of the PivotChart to image format for future archival, references and analysis purposes. We can export PivotChart to the following image formats.

* PNG
* EMF
* JPG
* GIF
* BMP

### Client Mode

To export PivotChart in PNG format, service URL, file name and **“ej.PivotChart.ExportOptions.PNG”** enumeration value is sent as the parameter. This is similar to other image formats.

{% highlight javascript %}

function exportBtnClick(args)
{
    var chartObj = $('#PivotChart1').data("ejPivotChart ");
    chartObj.exportPivotChart("http://js.syncfusion.com/ejservices/api/PivotChart/Olap/ImageExport","fileName", ej.PivotChart.ExportOptions.PNG);
}

{% endhighlight %}  

### Server Mode

To export PivotChart in PNG format, **“ej.PivotChart.ExportOptions.PNG”** enumeration value is sent as the parameter. This is similar to other image formats.

{% highlight javascript %}

function exportBtnClick(args)
{
    var chartObj = $('#PivotChart1').data("ejPivotChart ");
    //Setting export option as PNG in the exportPivotChart method
    chartObj.exportPivotChart(ej.PivotChart.ExportOptions.PNG);
}

{% endhighlight %}  

## Exporting Customization

You can add title and description to the exporting document by using title and description property obtained in the "beforeExport" event.

N> Title and description cannot be added to image formats.

{% highlight html %}

<html> 
    //...
<body> 
    //...
    <div id="PivotChart1" style="min-height: 275px; min-width: 525px; height: 460px; width: 720px"></div>
    <button id="btnExport">Export</button>
    <script type="text/javascript">
        $(function()
        {
            $("#PivotChart1").ejPivotChart(
            {
               //...
               beforeExport:"Exporting",
            });
            $("#btnExport").ejButton(
            {
                click: "exportBtnClick"
            });
        });
        function Exporting(args) {
            args.title = "PivotChart";
            args.description = "Visualizes both OLAP and Relational datasource in graphical format";
        }
        function exportBtnClick(args)
        {
            var chartObj = $('#PivotChart1').data("ejPivotChart");
            
            //If you render PivotChart in Client Mode, set the export option like below.
            chartObj.exportPivotChart("http://js.syncfusion.com/ejservices/api/PivotChart/Olap/ExcelExport","fileName");
            
            //If you render PivotChart in Server Mode, set the export option like below.
            chartObj.exportPivotChart(ej.PivotChart.ExportOptions.Excel);
        }
    </script>
</body>
</html>                                           

{% endhighlight %}

You can also edit the exporting document with the use of a server side event for required exporting option.

{% highlight c# %}

//...
using Syncfusion.EJ.Export;
using Syncfusion.Compression.Base;
using Syncfusion.XlsIO;
using Syncfusion.DocIO.Base;
using Syncfusion.Pdf.Base;

 //Following service method needs to be added in WebAPI for JSON export.
[System.Web.Http.ActionName("ExcelExport")]
[System.Web.Http.HttpPost]
public void ExcelExport()
{
    PivotChartExcelExport pivotChartExcelExport = new PivotChartExcelExport();
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    pivotChartExcelExport.ExcelExport += pivotChartExcelExport_ExcelExport;
    Dictionary<string, string> chartParams = serializer.Deserialize<Dictionary<string, string>>(args);
    pivotChartExcelExport.ExportToExcel(chartParams);
}

void pivotChartExcelExport_ExcelExport(object sender, Syncfusion.XlsIO.IWorkbook workBook)
{
    //You can customize exporting document here.
}

[System.Web.Http.ActionName("WordExport")]
[System.Web.Http.HttpPost]
public void WordExport()
{
    PivotChartWordExport pivotChartWordExport = new PivotChartWordExport();
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    pivotChartWordExport.WordExport += pivotChartWordExport_WordExport;
    Dictionary<string, string> chartParams = serializer.Deserialize<Dictionary<string, string>>(args);
    pivotChartWordExport.ExportToWord(chartParams);
}

void pivotChartWordExport_WordExport(object sender, Syncfusion.DocIO.DLS.WordDocument document)
{
    //You can customize exporting document here.
}

[System.Web.Http.ActionName("PdfExport")]
[System.Web.Http.HttpPost]
public void PdfExport()
{
    PivotChartPDFExport pivotChartPDFExport = new PivotChartPDFExport();
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    pivotChartPDFExport.AddPDFHeaderFooter += pivotChartPDFExport_AddPDFHeaderFooter;
    pivotChartPDFExport.PDFExport += pivotChartPDFExport_PDFExport;
    Dictionary<string, string> chartParams = serializer.Deserialize<Dictionary<string, string>>(args);
    pivotChartPDFExport.ExportToPDF(chartParams);
}

void pivotChartPDFExport_PDFExport(object sender, Syncfusion.Pdf.PdfDocument pdfDoc)
{
    //You can customize exporting document here.
}

void pivotChartPDFExport_AddPDFHeaderFooter(object sender, Syncfusion.Pdf.PdfDocument pdfDoc)
{
    //You can add header/footer information to the pdf document.
}

 //Following service method needs to be added in WCF/WebAPI for PivotEngine export.

[System.Web.Http.ActionName("Export")]
[System.Web.Http.HttpPost]
public void Export()
{
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    string fileName = "Sample";
    htmlHelper.ExcelExport += htmlHelper_ExcelExport;
    htmlHelper.WordExport += htmlHelper_WordExport;
    htmlHelper.AddPDFHeaderFooter += htmlHelper_AddPDFHeaderFooter;
    htmlHelper.PDFExport += htmlHelper_PDFExport;
    htmlHelper.ExportPivotChart(args, fileName, System.Web.HttpContext.Current.Response);
}

void htmlHelper_PDFExport(object sender, Syncfusion.Pdf.PdfDocument pdfDoc)
{
    //You can customize exporting document here.
}

void htmlHelper_AddPDFHeaderFooter(object sender, Syncfusion.Pdf.PdfDocument pdfDoc)
{
    //You can add header/footer information to the pdf document.
}

void htmlHelper_WordExport(object sender, Syncfusion.DocIO.DLS.WordDocument document)
{
    //You can customize exporting document here.
}

void htmlHelper_ExcelExport(object sender, Syncfusion.XlsIO.IWorkbook workBook)
{
    //You can customize exporting document here.
}

{% endhighlight %}

The name of the document can be customized as per the users requirement.

For Client mode, we need to send file name as parameter to the **“exportPivotChart”**  method along with service URL.

{% highlight javascript %}

function exportBtnClick(args)
{
    var chartObj = $('#PivotChart1').data("ejPivotChart ");
    chartObj.exportPivotChart("http://js.syncfusion.com/ejservices/api/PivotChart/Olap/ExcelExport", "fileName");
}
{% endhighlight %}    

For Server mode, the exporting document name is provided in the WebAPI controller as found in the below code snippet.

{% highlight c# %}

[System.Web.Http.ActionName("Export")]
[System.Web.Http.HttpPost]
public void Export() {
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    string fileName = "File name is customized here";
    htmlHelper.ExportPivotChart(args, fileName, System.Web.HttpContext.Current.Response);
}

{% endhighlight %}

For customizing name in WCF Service, below code snippet is used.

{% highlight c# %}

public void Export(System.IO.Stream stream) {
    System.IO.StreamReader sReader = new System.IO.StreamReader(stream);
    string args = System.Web.HttpContext.Current.Server.UrlDecode(sReader.ReadToEnd()).Remove(0, 5);
    string fileName = " File name is customized here ";
    htmlHelper.ExportPivotChart(args, fileName, System.Web.HttpContext.Current.Response);
}

{% endhighlight %}

The below screenshot shows the PivotChart control exported to Excel document.

![](Export_images/Export_ExcelClient.png)

The below screenshot shows the PivotChart control exported to Word document.

![](Export_images/Export_WordClient.png)

The below screenshot shows the PivotChart control exported to PDF document.

![](Export_images/Export_PDFClient.png)

The below screenshot shows the PivotChart control exported to PNG format.

![](Export_images/Export_PNGClient.png)