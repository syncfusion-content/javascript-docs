---
layout: post
title: Service Reference for ejPivotChart widget
description: What are the services used in JavaScript ejPivotChart widget
platform: js
control: ejPivotChart
documentation: api
keywords: ejPivotChart, Services, JS PivotChart, PivotChart, PivotChart Exporting, Image Exporting
---

# ejPivotChart

PivotChart widget is a lightweight control that reads both OLAP and Relational data source and visualizes it in graphical format with the ability to drill up and down. PivotChart uses services to initialize and operate widget and also to export PivotChart to an Excel, Word, PDF or Image document.

## WCF/WebAPI Service to populate PivotChart 
You can populate a simple PivotChart with OLAP/Relational data completely from the server-side using WCF/WebAPI service. You can refer the **Getting Started** document available in the following UG documentation section.
 
For Relational data source, [click here.](https://help.syncfusion.com/js/pivotchart/relational-getting-started#creating-a-simple-application-with-pivotchart-and-relational-datasource-server-mode)

For OLAP data source, [click here.](https://help.syncfusion.com/js/pivotchart/olap-getting-started#creating-a-simple-application-with-pivotchart-and-olap-datasource-server-mode)
 
## Exporting Service

### Excel Export

User can export contents of the PivotChart to Excel document for future archival, references and analysis purposes.

#### URL

[http://js.syncfusion.com/ejservices/api/JSPivotChartExport/ExcelExport](http://js.syncfusion.com/ejservices/api/JSPivotChartExport/ExcelExport)

#### Parameter
<table>
   <th>Type</th>
   <th>URL </th>
   <th>MultipleExport </th>
   <tr>
      <td>Excel</td>
      <td>http://js.syncfusion.com/ejservices/api/JSPivotChartExport/ExcelExport</td>
      <td>False</td>
   </tr>
</table>

#### Request

To achieve Excel export, service URL and file name is sent as the parameter.

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
          pChartObj.exportPivotChart("http://js.syncfusion.com/ejservices/api/JSPivotChartExport/ExcelExport","fileName"); 
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

##### Response for Excel Export:
Browser will prompt a dialog box to save the Excel document.

### Word Export

User can export contents of the PivotChart to Word document for future archival, references and analysis purposes.

#### URL

[http://js.syncfusion.com/ejservices/api/JSPivotChartExport/WordExport](http://js.syncfusion.com/ejservices/api/JSPivotChartExport/WordExport)

#### Parameter
<table>
   <th>Type</th>
   <th>URL </th>
   <th>MultipleExport </th>
   <tr>
      <td>Word</td>
      <td>http://js.syncfusion.com/ejservices/api/JSPivotChartExport/WordExport</td>
      <td>False</td>
   </tr>
</table>

#### Request

To achieve Word export, service URL and file name is sent as the parameter.

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
          pChartObj.exportPivotChart("http://js.syncfusion.com/ejservices/api/JSPivotChartExport/WordExport","fileName");
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

##### Response for Word Export:
Browser will prompt a dialog box to save the Word document.

### PDF Export

User can export contents of the PivotChart to PDF document for future archival, references and analysis purposes.

#### URL

[http://js.syncfusion.com/ejservices/api/JSPivotChartExport/PDFExport](http://js.syncfusion.com/ejservices/api/JSPivotChartExport/PDFExport)

#### Parameter
<table>
   <th>Type</th>
   <th>URL </th>
   <th>MultipleExport </th>
   <tr>
      <td>PDF</td>
      <td>http://js.syncfusion.com/ejservices/api/JSPivotChartExport/PDFExport</td>
      <td>False</td>
   </tr>
</table>

#### Request

To achieve PDF export, service URL and file name is sent as the parameter.

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
          pChartObj.exportPivotChart("http://js.syncfusion.com/ejservices/api/JSPivotChartExport/PDFExport","fileName");   
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

##### Response for PDF Export:
Browser will prompt a dialog box to save the PDF document.

### Image Export

User can export contents of the PivotChart to image format for future archival, references and analysis purposes. We can export PivotChart to the following image formats.

* PNG
* EMF
* JPG
* GIF
* BMP

#### URL

[http://js.syncfusion.com/ejservices/api/JSPivotChartExport/ImageExport](http://js.syncfusion.com/ejservices/api/JSPivotChartExport/ImageExport)

#### Parameter
<table>
   <th>Type</th>
   <th>URL </th>
   <th>MultipleExport </th>
   <tr>
      <td>Image</td>
      <td>http://js.syncfusion.com/ejservices/api/JSPivotChartExport/ImageExport</td>
      <td>False</td>
   </tr>
</table>

#### Request

To export PivotChart in PNG format, service URL, file name and **“ej.PivotChart.ExportOptions.PNG”** enumeration value is sent as the parameter. This is similar to other image formats.

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
          pChartObj.exportPivotChart("http://js.syncfusion.com/ejservices/api/JSPivotChartExport/ImageExport","fileName", ej.PivotChart.ExportOptions.PNG); //PNG Export
          pChartObj.exportPivotChart("http://js.syncfusion.com/ejservices/api/JSPivotChartExport/ImageExport","fileName", ej.PivotChart.ExportOptions.EMF); //EMF Export
          pChartObj.exportPivotChart("http://js.syncfusion.com/ejservices/api/JSPivotChartExport/ImageExport","fileName", ej.PivotChart.ExportOptions.JPG); //JPG Export
          pChartObj.exportPivotChart("http://js.syncfusion.com/ejservices/api/JSPivotChartExport/ImageExport","fileName", ej.PivotChart.ExportOptions.GIF); //GIF Export
          pChartObj.exportPivotChart("http://js.syncfusion.com/ejservices/api/JSPivotChartExport/ImageExport","fileName", ej.PivotChart.ExportOptions.BMP); //BMP Export
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

##### Response for PNG Export:
Browser will prompt a dialog box to save the PNG image.

