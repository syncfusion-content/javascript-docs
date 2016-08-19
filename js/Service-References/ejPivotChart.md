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

## WCF/WebAPI Service
You can populate a simple PivotChart with OLAP/Relational data completely from the server-side using WCF/WebAPI service. You can refer the **Getting Started** document available in the following UG documentation section.
 
For Relational data source, [click here.](https://help.syncfusion.com/js/pivotchart/relational-getting-started#creating-a-simple-application-with-pivotchart-and-relational-datasource-server-mode)

For OLAP data source, [click here.](https://help.syncfusion.com/js/pivotchart/olap-getting-started#creating-a-simple-application-with-pivotchart-and-olap-datasource-server-mode)
 
## Exporting Service

### Description

To export PivotChart data to an Excel, Word, PDF or Image document.

### URL

[http://js.syncfusion.com/demos/ejservices/api/JSPivotChartExport/ExcelExport](http://js.syncfusion.com/demos/ejservices/api/JSPivotChartExport/ExcelExport)
[http://js.syncfusion.com/demos/ejservices/api/JSPivotChartExport/WordExport](http://js.syncfusion.com/demos/ejservices/api/JSPivotChartExport/WordExport)
[http://js.syncfusion.com/demos/ejservices/api/JSPivotChartExport/PDFExport](http://js.syncfusion.com/demos/ejservices/api/JSPivotChartExport/PDFExport)
[http://js.syncfusion.com/demos/ejservices/api/JSPivotChartExport/ImageExport](http://js.syncfusion.com/demos/ejservices/api/JSPivotChartExport/ImageExport)

### Parameter
<table>
   <th>Type</th>
   <th>URL </th>
   <th>MultipleExport </th>
   <tr>
      <td>Excel</td>
      <td>http://js.syncfusion.com/demos/ejservices/api/JSPivotChartExport/ExcelExport</td>
      <td>False</td>
   </tr>
   <tr>
      <td>Word</td>
      <td>http://js.syncfusion.com/demos/ejservices/api/JSPivotChartExport/WordExport</td>
      <td>False</td>
   </tr>
   <tr>
      <td>PDF</td>
      <td>http://js.syncfusion.com/demos/ejservices/api/JSPivotChartExport/PDFExport</td>
      <td>False</td>
   </tr>
   <tr>
      <td>Image</td>
      <td>http://js.syncfusion.com/demos/ejservices/api/JSPivotChartExport/ImageExport</td>
      <td>False</td>
   </tr>
</table>

### Request

#### PivotChart Exporting in JS

{% highlight %}
<div id="PivotChart1" style="min-height: 275px; min-width: 525px; height: 460px; width: 950px">
<button id="btnExport">Export</button>
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
        var pGridObj = $('#PivotChart1').data("ejPivotChart");
        pGridObj.exportPivotChart("http://js.syncfusion.com/demos/ejservices/api/JSPivotChartExport/ExcelExport");  //Excel Export
        pGridObj.exportPivotChart("http://js.syncfusion.com/demos/ejservices/api/JSPivotChartExport/WordExport");   //Word Export
        pGridObj.exportPivotChart("http://js.syncfusion.com/demos/ejservices/api/JSPivotChartExport/PDFExport");    //PDF Export
        pGridObj.exportPivotChart("http://js.syncfusion.com/demos/ejservices/api/JSPivotChartExport/ImageExport","PivotChart", ej.PivotChart.ExportOptions.PNG); //PNG Export
        pGridObj.exportPivotChart("http://js.syncfusion.com/demos/ejservices/api/JSPivotChartExport/ImageExport","PivotChart", ej.PivotChart.ExportOptions.EMF); //EMF Export
        pGridObj.exportPivotChart("http://js.syncfusion.com/demos/ejservices/api/JSPivotChartExport/ImageExport","PivotChart", ej.PivotChart.ExportOptions.JPG); //JPG Export
        pGridObj.exportPivotChart("http://js.syncfusion.com/demos/ejservices/api/JSPivotChartExport/ImageExport","PivotChart", ej.PivotChart.ExportOptions.GIF); //GIF Export
        pGridObj.exportPivotChart("http://js.syncfusion.com/demos/ejservices/api/JSPivotChartExport/ImageExport","PivotChart", ej.PivotChart.ExportOptions.BMP); //BMP Export
     }
{% endhighlight %}
#### PivotChart Exporting in C# 

{% highlight %}

        [System.Web.Http.ActionName("ExcelExport")]
        [System.Web.Http.HttpPost]
        public void ExcelExport()
        {
            PivotChartExcelExport pivotChartExcelExport = new PivotChartExcelExport();
            string args = HttpContext.Current.Request.Form.GetValues(0)[0];
            Dictionary<string, string> chartParams = serializer.Deserialize<Dictionary<string, string>>(args);
            pivotChartExcelExport.ExportToExcel(chartParams);
        }

        [System.Web.Http.ActionName("WordExport")]
        [System.Web.Http.HttpPost]
        public void WordExport()
        {
            PivotChartWordExport pivotChartWordExport = new PivotChartWordExport();
            string args = HttpContext.Current.Request.Form.GetValues(0)[0];
            Dictionary<string, string> chartParams = serializer.Deserialize<Dictionary<string, string>>(args);
            pivotChartWordExport.ExportToWord(chartParams);
        }

        [System.Web.Http.ActionName("PDFExport")]
        [System.Web.Http.HttpPost]
        public void PDFExport()
        {
            PivotChartPDFExport pivotChartPDFExport = new PivotChartPDFExport();
            string args = HttpContext.Current.Request.Form.GetValues(0)[0];
            Dictionary<string, string> chartParams = serializer.Deserialize<Dictionary<string, string>>(args);
            pivotChartPDFExport.ExportToPDF(chartParams);
        }

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
 
###Response

####Code: 200

####Content-Type: application/octet-stream

####Response (Excel, Word, PDF or Image):
Browser will prompt a dialog box to save the file.


