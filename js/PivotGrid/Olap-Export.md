---
layout: post
title: Export
description: export
platform: js
control: PivotGrid
documentation: ug
api: /api/js/ejpivotgrid
---

# Exporting

The PivotGrid control can be exported to the following file formats:

* Excel
* Word
* PDF
* CSV

The PivotGrid control can be exported by invoking the **"exportPivotGrid"** method, with an appropriate export option as parameter.

## JSON export

I> By default, JSON export mode will be applied for server and client modes.

{% highlight html %}

    <div id="PivotGrid1"></div>
    <button id="btnExport">Export</button>
    
    <script type="text/javascript">
        $(function () {
            $("#PivotGrid1").ejPivotGrid({
                //...
            });
            $("#btnExport").ejButton({
                click: "exportBtnClick"
            });
        });
        function exportBtnClick(args) {
            var pGridObj = $('#PivotGrid1').data("ejPivotGrid");
            pGridObj.exportPivotGrid("http://js.syncfusion.com/ejservices/api/PivotGrid/Olap/ExcelExport", "fileName");
        }
    </script>                                        

{% endhighlight %}

### Excel export

You can export the contents of the PivotGrid to an Excel document for future archival, references, and analysis purposes.

To achieve Excel export, the service URL and the file name are set as parameters.

{% highlight javascript %}

    function exportBtnClick(args)
    {
        var pGridObj = $('#PivotGrid1').data("ejPivotGrid");
        pGridObj.exportPivotGrid("http://js.syncfusion.com/ejservices/api/PivotGrid/Olap/ExcelExport", "fileName");
    }

{% endhighlight %}

### Word export

You can export the contents of the PivotGrid to a Word document for future archival, references, and analysis purposes.

To achieve Word export, the service URL and the file name are set as parameters.

{% highlight javascript %}

    function exportBtnClick(args)
    {
        var pGridObj = $('#PivotGrid1').data("ejPivotGrid");
        pGridObj.exportPivotGrid("http://js.syncfusion.com/ejservices/api/PivotGrid/Olap/WordExport", "fileName");
    }

{% endhighlight %}  

### PDF export

You can export the contents of PivotGrid to a PDF document for future archival, references, and analysis purposes.

To achieve PDF export, the service URL and the file name are set as parameters.

{% highlight javascript %}

    function exportBtnClick(args)
    {
        var pGridObj = $('#PivotGrid1').data("ejPivotGrid");
        pGridObj.exportPivotGrid("http://js.syncfusion.com/ejservices/api/PivotGrid/Olap/PDFExport", "fileName");
    }

{% endhighlight %}  

### CSV Export

You can export the contents of PivotGrid to a CSV document for future archival, references, and analysis purposes.

To achieve CSV export, the service URL and the file name are set as parameters.

{% highlight javascript %}

    function exportBtnClick(args)
    {
        var pGridObj = $('#PivotGrid1').data("ejPivotGrid");
        pGridObj.exportPivotGrid("http://js.syncfusion.com/ejservices/api/PivotGrid/Olap/CSVExport", "fileName");
    }

{% endhighlight %}  

### Customize the export document name

For customizing the file name, you should set the file name as parameter to the **exportPivotGrid**  method along with the service URL.

{% highlight javascript %}

    function exportBtnClick(args)
    {
        var pGridObj = $('#PivotGrid1').data("ejPivotGrid");
        pGridObj.exportPivotGrid("http://js.syncfusion.com/ejservices/api/PivotGrid/Olap/ExcelExport", "File name is customized here");
    }
    
{% endhighlight %}

## PivotEngine export

I> This feature is applicable only at server mode operation.

To perform exporting with the use of PivotEngine available in the server-side, the 'exportMode' property obtained in the “beforeExport” event is set to the value "ej.PivotGrid.ExportMode.PivotEngine" as shown below:

{% highlight html %}

    <div id="PivotGrid1"></div>
    <button id="btnExport">Export</button>
    
    <script type="text/javascript">
        $(function () {
            $("#PivotGrid1").ejPivotGrid({
                //...
                beforeExport: "Export"
            });
            $("#btnExport").ejButton({
                click: "exportBtnClick"
            });
        });
        
        function exportBtnClick(args) {
            var pGridObj = $('#PivotGrid1').data("ejPivotGrid");
            pGridObj.exportPivotGrid(ej.PivotGrid.ExportOptions.Excel);
        }
        
        function Export(args) {
            args.exportMode = ej.PivotGrid.ExportMode.PivotEngine; 
        }
    </script>
</html>                                            

{% endhighlight %}

A service method should be added in the WCF/WebAPI for server side operations.

For WebAPI controller, the below method needs to be added.

{% highlight c# %}

//...
using Syncfusion.Compression.Base;
using Syncfusion.XlsIO;
using Syncfusion.DocIO.Base;
using Syncfusion.Pdf.Base;

[System.Web.Http.ActionName("Export")]
[System.Web.Http.HttpPost]
public void Export()
{
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    string fileName = "Sample";
    htmlHelper.ExportPivotGrid(DataManager, args, fileName, System.Web.HttpContext.Current.Response);
}

{% endhighlight %}

For WCF service, the below method needs to be added.

{% highlight c# %}

//...
using Syncfusion.Compression.Base;
using Syncfusion.XlsIO;
using Syncfusion.DocIO.Base;
using Syncfusion.Pdf.Base;

public void Export(System.IO.Stream stream)
{
    System.IO.StreamReader sReader = new System.IO.StreamReader(stream);
    string args = System.Web.HttpContext.Current.Server.UrlDecode(sReader.ReadToEnd()).Remove(0, 5);
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    string fileName = "Sample";
    htmlHelper.ExportPivotGrid(DataManager, args, fileName, System.Web.HttpContext.Current.Response);
}

{% endhighlight %}

### Excel export

You can export the contents of PivotGrid to a Excel document for future archival, references, and analysis purposes.

To achieve Excel export, you should add the following dependency libraries to the application.

* Syncfusion.Compression.Base
* Syncfusion.XlsIO.Base

For Excel export, the **“ej.PivotGrid.ExportOptions.Excel”** enumeration value is set as parameter.

{% highlight javascript %}

function exportBtnClick(args)
{
    var pGridObj = $('#PivotGrid1').data("ejPivotGrid");
    //Setting export option as Excel in the exportPivotGrid method
    pGridObj.exportPivotGrid(ej.PivotGrid.ExportOptions.Excel);
}

{% endhighlight %}  

### Word export

You can export the contents of PivotGrid to a Word document for future archival, references, and analysis purposes.

 To achieve Word export, you should add the following dependency libraries to the application.

* Syncfusion.Compression.Base
* Syncfusion.DocIO.Base

For Word export, the **“ej.PivotGrid.ExportOptions.Word”** enumeration value is set as parameter.

{% highlight javascript %}

function exportBtnClick(args)
{
    var pGridObj = $('#PivotGrid1').data("ejPivotGrid");
    //Setting export option as Word in the exportPivotGrid method
    pGridObj.exportPivotGrid(ej.PivotGrid.ExportOptions.Word);
}

{% endhighlight %}

### PDF export

You can export the contents of PivotGrid to a PDF document for future archival, references, and analysis purposes.

To achieve PDF export, you should add the following dependency libraries to the application.

* Syncfusion.Compression.Base
* Syncfusion.Pdf.Base

For PDF export, the **“ej.PivotGrid.ExportOptions.PDF”** enumeration value is set as parameter.

{% highlight javascript %}

function exportBtnClick(args)
{
    var pGridObj = $('#PivotGrid1').data("ejPivotGrid");
    //Setting export option as PDF in the exportPivotGrid method
    pGridObj.exportPivotGrid(ej.PivotGrid.ExportOptions.PDF);
}

{% endhighlight %} 

### CSV export

You can export the contents of PivotGrid to a CSV document for future archival, references, and analysis purposes.

For CSV export, the **“ej.PivotGrid.ExportOptions.CSV"** enumeration value is set as parameter.

{% highlight javascript %}

function exportBtnClick(args)
{
    var pGridObj = $('#PivotGrid1').data("ejPivotGrid");
    //Setting export option as CSV in the exportPivotGrid method
    pGridObj.exportPivotGrid(ej.PivotGrid.ExportOptions.CSV);
}

{% endhighlight %} 

### File format selection

I> This option is applicable only for the PivotGrid when exporting to Excel document.

You can set the option for exporting the widget to Excel document either in *.xls* or *.xlsx* format, using the `fileFormat` property in the `beforeExport` event.

N> By default, the excel document will be exported to ".xls" format using the PivotEngine export.

{% highlight javascript %}

        $("#PivotGrid1").ejPivotGrid({
                //..
                beforeExport: "Export"
            });
        
        function Export(args) {
            args.exportMode = ej.PivotGrid.ExportMode.PivotEngine; 
            args.fileFormat = ".xlsx"; //you can set the excel sheet format here
        }
        
 {% endhighlight %}

### Customize the export document name

For customizing name in the WebAPI controller, the below code sample is used:

{% highlight c# %}

//...
using Syncfusion.Compression.Base;
using Syncfusion.XlsIO;
using Syncfusion.DocIO.Base;
using Syncfusion.Pdf.Base;

[System.Web.Http.ActionName("Export")]
[System.Web.Http.HttpPost]
public void Export() {
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    string fileName = " File name is customized here ";
    htmlHelper.ExportPivotGrid(DataManager, args, fileName, System.Web.HttpContext.Current.Response);
}

{% endhighlight %}

For customizing name in the WCF Service, the below code snippet is used:

{% highlight c# %}

//...
using Syncfusion.Compression.Base;
using Syncfusion.XlsIO;
using Syncfusion.DocIO.Base;
using Syncfusion.Pdf.Base;

public void Export(System.IO.Stream stream) {
    System.IO.StreamReader sReader = new System.IO.StreamReader(stream);
    string args = System.Web.HttpContext.Current.Server.UrlDecode(sReader.ReadToEnd()).Remove(0, 5);;
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    string fileName = " File name is customized here ";
    htmlHelper.ExportPivotGrid(DataManager, args, fileName, System.Web.HttpContext.Current.Response);
}

{% endhighlight %}

## Exporting customization

You can add title and description to the exporting document by using the title and description property obtained in the "beforeExport" event.

{% highlight html %}
<html> 
    //...
<body> 
    //...
    <div id="PivotGrid1" style="height: 350px; width: 100%; overflow: auto"></div>
    <button id="btnExport">Export</button>
    
    <script type="text/javascript">
        $(function () {
            $("#PivotGrid1").ejPivotGrid({
                //..
                beforeExport: "Exporting"
            });
            $("#btnExport").ejButton({
                click: "exportBtnClick"
            });
        });
        function exportBtnClick(args) {
            var pGridObj = $('#PivotGrid1').data("ejPivotGrid");
            //JSON export
            pGridObj.exportPivotGrid("http://js.syncfusion.com/ejservices/api/PivotGrid/Olap/ExcelExport", "fileName");
            //PivotEngine Export 
            pGridObj.exportPivotGrid(ej.PivotGrid.ExportOptions.Excel);
        }
        function Exporting(args) {
            args.title = "PivotGrid";
            args.description = "Displays both OLAP and Relational datasource in tabular format";
        }
    </script>
</body>
</html>                                            

{% endhighlight %}

You can also edit the exporting document with the use of a server side event for the required exporting option.

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
    PivotGridExcelExport pGrid = new PivotGridExcelExport();
    pGrid.ExcelExport += pGrid_ExcelExport;
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    pGrid.ExportToExcel(string.Empty, args, HttpContext.Current.Response);
}

void pGrid_ExcelExport(object sender, Syncfusion.XlsIO.IWorkbook workBook)
{
    //You can customize exporting document here.
}
[System.Web.Http.ActionName("PdfExport")]
[System.Web.Http.HttpPost]
public void PdfExport()
{
    PivotGridPDFExport pGrid = new PivotGridPDFExport();
    pGrid.AddPDFHeaderFooter += pGrid_AddPDFHeaderFooter;
    pGrid.PDFExport += pGrid_PDFExport;
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    pGrid.ExportToPDF(string.Empty, args, HttpContext.Current.Response);
}

void pGrid_PDFExport(object sender, Syncfusion.Pdf.PdfDocument pdfDoc)
{
    //You can customize exporting document here.
}

void pGrid_AddPDFHeaderFooter(object sender, Syncfusion.Pdf.PdfDocument pdfDoc)
{
    //You can add header/footer information to the PDF document.
}

[System.Web.Http.ActionName("WordExport")]
[System.Web.Http.HttpPost]
public void WordExport()
{
    PivotGridWordExport pGrid = new PivotGridWordExport();
    pGrid.WordExport += pGrid_WordExport;
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    pGrid.ExportToWord(string.Empty, args, HttpContext.Current.Response);
}

void pGrid_WordExport(object sender, Syncfusion.DocIO.DLS.WordDocument document)
{
    //You can customize exporting document here.
}

[System.Web.Http.ActionName("CsvExport")]
[System.Web.Http.HttpPost]
public void CsvExport()
{
    PivotGridCSVExport pGrid = new PivotGridCSVExport();
    pGrid.CSVExport += pGrid_CSVExport;
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    pGrid.ExportToCSV(string.Empty, args, HttpContext.Current.Response);
}

void pGrid_CSVExport(object sender, string csvString)
{
    //You can customize exporting document here.
}


 //Following service method should be added in the WCF/WebAPI for PivotEngine export.

[System.Web.Http.ActionName("Export")]
[System.Web.Http.HttpPost]
public void Export()
{
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    string fileName = "Sample";
    htmlHelper.ExcelExport += htmlHelper_ExcelExport;
    htmlHelper.WordExport += htmlHelper_WordExport;
    htmlHelper.AddPDFHeaderFooter += htmlHelper_AddPDFHeaderFooter;
    htmlHelper.PDFExport += htmlHelper_PDFExport;
    htmlHelper.CSVExport += htmlHelper_CSVExport;
    htmlHelper.ExportPivotGrid(DataManager, args, fileName, System.Web.HttpContext.Current.Response);
}

void htmlHelper_ExcelExport(object sender, Syncfusion.XlsIO.IWorkbook workBook)
{
    //You can customize exporting document here.
}
void htmlHelper_WordExport(object sender, Syncfusion.DocIO.DLS.WordDocument document)
{
    //You can customize exporting document here.
}
void htmlHelper_AddPDFHeaderFooter(object sender, Syncfusion.Pdf.PdfDocument pdfDoc)
{
    //You can add header/footer information to the PDF document.
}
void htmlHelper_PDFExport(object sender, Syncfusion.Pdf.PdfDocument pdfDoc)
{
    //You can customize exporting document here.
}
void htmlHelper_CSVExport(object sender, string csvString)
{
    //You can customize exporting document here.
}

{% endhighlight %}

The below screenshot shows the PivotGrid control exported to the Excel document:

![](Export_images/ExportOLAPExcel.png)

The below screenshot shows the PivotGrid control exported to the Word document:

![](Export_images/ExportOLAPWord.png)

The below screenshot shows the PivotGrid control exported to the PDF document:

![](Export_images/ExportOLAPPDF.png)

The below screenshot shows the PivotGrid control exported to the CSV document:

![](Export_images/ExportOLAPCSV.png)



