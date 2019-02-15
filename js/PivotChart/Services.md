---
layout: post
title: Service Reference for PivotChart widget in Syncfusion Essential JS
description: What are the services used in JavaScript ejPivotChart widget
platform: js
control: ejPivotChart
documentation: ug
keywords: ejPivotChart, Services, JS PivotChart, PivotChart, PivotChart Exporting, Image Exporting
api: /api/js/ejpivotchart
---

# ejPivotChart

The pivot chart widget is a lightweight control that reads both OLAP and relational data sources and visualizes it in a graphical format with the ability to drill up and down. The pivot chart uses services to initialize and operate the widget and also to export the pivot chart to a Microsoft Excel, Microsoft Word, PDF, or image document.

## WCF/WebAPI service to populate pivot chart
You can populate a simple pivot chart with the OLAP/relational data completely from the server-side using the WCF/WebAPI service. You can refer the **Getting Started** document available in the following UG documentation section.

For relational data source, [click here.](https://help.syncfusion.com/js/pivotchart/relational-getting-started#creating-a-simple-application-with-pivotchart-and-relational-datasource-server-mode)

For OLAP data source, [click here.](https://help.syncfusion.com/js/pivotchart/olap-getting-started#creating-a-simple-application-with-pivotchart-and-olap-datasource-server-mode)

## Exporting service

### Excel export

You can export the contents of the pivot chart to Excel document for future archival, references, and analysis purposes.

#### URL

[https://js.syncfusion.com/ejservices/api/PivotChart/Olap/ExcelExport](https://js.syncfusion.com/ejservices/api/PivotChart/Olap/ExcelExport)

#### Parameter
<table>
   <th>Type</th>
   <th>URL </th>
   <th>MultipleExport </th>
   <tr>
      <td>Excel</td>
      <td>https://js.syncfusion.com/ejservices/api/PivotChart/Olap/ExcelExport</td>
      <td>False</td>
   </tr>
</table>

#### Request

To achieve Excel export, the service URL and the file name are set as parameters.

##### JS

{% highlight html %}

<html>
//...
<body>

     <div id="PivotChart1" style="min-height: 275px; min-width: 525px; height: 460px; width: 950px"></div>
     <button id="btnExport">Export</button>
     <script type="text/javascript">
        $(function() {
            $("#PivotChart1").ejPivotChart({
                dataSource: {
                   data: pivot_dataset,
                   rows: [{
                      fieldName: "Country",
                      fieldCaption: "Country"
                   }],
                  columns: [{
                      fieldName: "Product",
                      fieldCaption: "Product"
                  }],
                  values: [{
                      fieldName: "Amount",
                      fieldCaption: "Amount"
                  }]
               }
           });
           $("#btnExport").ejButton({
              click: "exportBtnClick"
           });
       });
       function exportBtnClick(args)
       {
          var pChartObj = $('#PivotChart1').data("ejPivotChart");
          pChartObj.exportPivotChart("https://js.syncfusion.com/ejservices/api/PivotChart/Olap/ExcelExport","fileName");
       }

     </script>
</body>
</html>

{% endhighlight %}

##### C\#

{% highlight c# %}

[System.Web.Http.ActionName("ExcelExport")]
[System.Web.Http.HttpPost]
public void ExcelExport()
{
    PivotChartExcelExport pivotChartExcelExport = new PivotChartExcelExport();
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    Dictionary<string, string> chartParams = serializer.Deserialize<Dictionary<string, string>>(args);
    pivotChartExcelExport.ExportToExcel(chartParams);
}

{% endhighlight %}

#### Response

##### Code: 200

##### Content-Type: application/octet-stream

##### Response for Excel export:
The browser will prompt a dialog box to save the Excel document.

### Word export

You can export the contents of the pivot chart to a Word document for future archival, references, and analysis purposes.

#### URL

[https://js.syncfusion.com/ejservices/api/PivotChart/Olap/WordExport](https://js.syncfusion.com/ejservices/api/PivotChart/Olap/WordExport)

#### Parameter
<table>
   <th>Type</th>
   <th>URL </th>
   <th>MultipleExport </th>
   <tr>
      <td>Word</td>
      <td>https://js.syncfusion.com/ejservices/api/PivotChart/Olap/WordExport</td>
      <td>False</td>
   </tr>
</table>

#### Request

To achieve Word export, the service URL and the file name are set as parameters.

##### JS

{% highlight html %}

<html>
//...
<body>

     <div id="PivotChart1" style="min-height: 275px; min-width: 525px; height: 460px; width: 950px"></div>
     <button id="btnExport">Export</button>
     <script type="text/javascript">
        $(function() {
            $("#PivotChart1").ejPivotChart({
                dataSource: {
                   data: pivot_dataset,
                   rows: [{
                      fieldName: "Country",
                      fieldCaption: "Country"
                   }],
                  columns: [{
                      fieldName: "Product",
                      fieldCaption: "Product"
                  }],
                  values: [{
                      fieldName: "Amount",
                      fieldCaption: "Amount"
                  }]
               }
           });
           $("#btnExport").ejButton({
              click: "exportBtnClick"
           });
       });
       function exportBtnClick(args)
       {
          var pChartObj = $('#PivotChart1').data("ejPivotChart");
          pChartObj.exportPivotChart("https://js.syncfusion.com/ejservices/api/PivotChart/Olap/WordExport","fileName");
       }

     </script>
</body>
</html>

{% endhighlight %}

##### C\#

{% highlight c# %}

[System.Web.Http.ActionName("WordExport")]
[System.Web.Http.HttpPost]
public void WordExport()
{
    PivotChartWordExport pivotChartWordExport = new PivotChartWordExport();
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    Dictionary<string, string> chartParams = serializer.Deserialize<Dictionary<string, string>>(args);
    pivotChartWordExport.ExportToWord(chartParams);
}

{% endhighlight %}

#### Response

##### Code: 200

##### Content-Type: application/octet-stream

##### Response for Word export:
The browser will prompt a dialog box to save the Word document.

### PDF export

You can export the contents of the pivot chart to a PDF document for future archival, references, and analysis purposes.

#### URL

[https://js.syncfusion.com/ejservices/api/PivotChart/Olap/PDFExport](https://js.syncfusion.com/ejservices/api/PivotChart/Olap/PDFExport)

#### Parameter
<table>
   <th>Type</th>
   <th>URL </th>
   <th>MultipleExport </th>
   <tr>
      <td>PDF</td>
      <td>https://js.syncfusion.com/ejservices/api/PivotChart/Olap/PDFExport</td>
      <td>False</td>
   </tr>
</table>

#### Request

To achieve PDF export, the service URL and the file name are set as parameters.

##### JS

{% highlight html %}

<html>
//...
<body>

     <div id="PivotChart1" style="min-height: 275px; min-width: 525px; height: 460px; width: 950px"></div>
     <button id="btnExport">Export</button>
     <script type="text/javascript">
        $(function() {
            $("#PivotChart1").ejPivotChart({
                dataSource: {
                   data: pivot_dataset,
                   rows: [{
                      fieldName: "Country",
                      fieldCaption: "Country"
                   }],
                  columns: [{
                      fieldName: "Product",
                      fieldCaption: "Product"
                  }],
                  values: [{
                      fieldName: "Amount",
                      fieldCaption: "Amount"
                  }]
               }
           });
           $("#btnExport").ejButton({
              click: "exportBtnClick"
           });
       });
       function exportBtnClick(args)
       {
          var pChartObj = $('#PivotChart1').data("ejPivotChart");
          pChartObj.exportPivotChart("https://js.syncfusion.com/ejservices/api/PivotChart/Olap/PDFExport","fileName");
       }

     </script>
</body>
</html>

{% endhighlight %}

##### C\#

{% highlight c# %}

[System.Web.Http.ActionName("PDFExport")]
[System.Web.Http.HttpPost]
public void PDFExport()
{
    PivotChartPDFExport pivotChartPDFExport = new PivotChartPDFExport();
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    Dictionary<string, string> chartParams = serializer.Deserialize<Dictionary<string, string>>(args);
    pivotChartPDFExport.ExportToPDF(chartParams);
}

{% endhighlight %}

#### Response

##### Code: 200

##### Content-Type: application/octet-stream

##### Response for PDF export:
The browser will prompt a dialog box to save the PDF document.

### Image export

You can export the contents of the pivot chart to an image format for future archival, references, and analysis purposes. You can export the pivot chart to the following image formats:

* PNG
* EMF
* JPG
* GIF
* BMP

#### URL

[https://js.syncfusion.com/ejservices/api/PivotChart/Olap/ImageExport](https://js.syncfusion.com/ejservices/api/PivotChart/Olap/ImageExport)

#### Parameter
<table>
   <th>Type</th>
   <th>URL </th>
   <th>MultipleExport </th>
   <tr>
      <td>Image</td>
      <td>https://js.syncfusion.com/ejservices/api/PivotChart/Olap/ImageExport</td>
      <td>False</td>
   </tr>
</table>

#### Request

To export pivot chart in the PNG format, the service URL, file name and **“ej.PivotChart.ExportOptions.PNG”** enumeration value are set as parameters. This is similar to other image formats.

##### JS

{% highlight html %}

<html>
//...
<body>

     <div id="PivotChart1" style="min-height: 275px; min-width: 525px; height: 460px; width: 950px"></div>
     <button id="btnExport">Export</button>
     <script type="text/javascript">
        $(function() {
            $("#PivotChart1").ejPivotChart({
                dataSource: {
                   data: pivot_dataset,
                   rows: [{
                      fieldName: "Country",
                      fieldCaption: "Country"
                   }],
                  columns: [{
                      fieldName: "Product",
                      fieldCaption: "Product"
                  }],
                  values: [{
                      fieldName: "Amount",
                      fieldCaption: "Amount"
                  }]
               }
           });
           $("#btnExport").ejButton({
              click: "exportBtnClick"
           });
       });
       function exportBtnClick(args)
       {
          var pChartObj = $('#PivotChart1').data("ejPivotChart");
          pChartObj.exportPivotChart("https://js.syncfusion.com/ejservices/api/PivotChart/Olap/ImageExport","fileName", ej.PivotChart.ExportOptions.PNG); //PNG Export
          pChartObj.exportPivotChart("https://js.syncfusion.com/ejservices/api/PivotChart/Olap/ImageExport","fileName", ej.PivotChart.ExportOptions.EMF); //EMF Export
          pChartObj.exportPivotChart("https://js.syncfusion.com/ejservices/api/PivotChart/Olap/ImageExport","fileName", ej.PivotChart.ExportOptions.JPG); //JPG Export
          pChartObj.exportPivotChart("https://js.syncfusion.com/ejservices/api/PivotChart/Olap/ImageExport","fileName", ej.PivotChart.ExportOptions.GIF); //GIF Export
          pChartObj.exportPivotChart("https://js.syncfusion.com/ejservices/api/PivotChart/Olap/ImageExport","fileName", ej.PivotChart.ExportOptions.BMP); //BMP Export
       }

     </script>
</body>
</html>

{% endhighlight %}

##### C\#

{% highlight c# %}

[System.Web.Http.ActionName("ImageExport")]
[System.Web.Http.HttpPost]
public void ImageExport()
{
    PivotChartImageExport pivotChartImageExport = new PivotChartImageExport();
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    Dictionary<string, string> chartParams = serializer.Deserialize<Dictionary<string, string>>(args);
    pivotChartImageExport.ExportToImage(chartParams);
}

{% endhighlight %}

#### Response

##### Code: 200

##### Content-Type: application/octet-stream

##### Response for PNG export:
The browser will prompt a dialog box to save the PNG image.

