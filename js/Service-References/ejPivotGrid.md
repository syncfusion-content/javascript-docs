---
layout: post
title: Service Reference for ejPivotGrid widget
description: What are the services used in JavaScript ejPivotGrid widget
platform: js
control: ejPivotGrid
documentation: api
keywords: ejPivotGrid, Services, JS PivotGrid, PivotGrid, PivotGrid Exporting
---

# ejPivotGrid

PivotGrid widget is an easily configurable, presentation-quality business control that reads both OLAP and Relational data source, allows to create multi-dimensional views for analysis and satisfying business user needs. PivotGrid uses services to initialize and operate widget and also to export PivotGrid to an Excel, Word, PDF or CSV document.

## WCF/WebAPI Service to populate PivotGrid 
You can populate a simple PivotGrid with OLAP/Relational data completely from the server-side using WCF/WebAPI service. You can refer the **Getting Started** document available in the following UG documentation section.

For Relational data source, [click here.](https://help.syncfusion.com/js/pivotgrid/relational-getting-started#creating-a-simple-application-with-pivotgrid-and-relational-datasource-server-mode)

For OLAP data source, [click here.](https://help.syncfusion.com/js/pivotgrid/olap-getting-started#creating-a-simple-application-with-pivotgrid-and-olap-datasource-server-mode)
 
## Exporting Service

### Description

To export PivotGrid data to an Excel, Word, PDF or CSV document.

### URL

[http://js.syncfusion.com/demos/ejservices/api/JSPivotGridExport/ExcelExport](http://js.syncfusion.com/demos/ejservices/api/JSPivotGridExport/ExcelExport)
[http://js.syncfusion.com/demos/ejservices/api/JSPivotGridExport/WordExport](http://js.syncfusion.com/demos/ejservices/api/JSPivotGridExport/WordExport)
[http://js.syncfusion.com/demos/ejservices/api/JSPivotGridExport/PDFExport](http://js.syncfusion.com/demos/ejservices/api/JSPivotGridExport/PDFExport)
[http://js.syncfusion.com/demos/ejservices/api/JSPivotGridExport/CSVExport](http://js.syncfusion.com/demos/ejservices/api/JSPivotGridExport/CSVExport)

### Parameter
<table>
   <th>Type</th>
   <th>URL </th>
   <th>MultipleExport </th>
   <tr>
      <td>Excel</td>
      <td>http://js.syncfusion.com/demos/ejservices/api/JSPivotGridExport/ExcelExport</td>
      <td>False</td>
   </tr>
   <tr>
      <td>Word</td>
      <td>http://js.syncfusion.com/demos/ejservices/api/JSPivotGridExport/WordExport</td>
      <td>False</td>
   </tr>
   <tr>
      <td>PDF</td>
      <td>http://js.syncfusion.com/demos/ejservices/api/JSPivotGridExport/PDFExport</td>
      <td>False</td>
   </tr
   <tr>
      <td>CSV</td>
      <td>http://js.syncfusion.com/demos/ejservices/api/JSPivotGridExport/CSVExport</td>
      <td>False</td>
   </tr>
</table>

### Request

#### PivotGrid Exporting in JS

{% highlight %}

<div id="PivotGrid1" style="min-height: 275px; min-width: 525px; height: 460px; width: 720px"></div>
<button id="btnExport">Export</button>
 $(function() {
     $("#PivotGrid1").ejPivotGrid({
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
        var pGridObj = $('#PivotGrid1').data("ejPivotGrid");
        //If want to export to excel
        pGridObj.exportPivotGrid("http://js.syncfusion.com/demos/ejservices/api/JSPivotGridExport/ExcelExport");
        //If want to export to Word
        pGridObj.exportPivotGrid("http://js.syncfusion.com/demos/ejservices/api/JSPivotGridExport/WordExport");
        //If want to export to PDF
        pGridObj.exportPivotGrid("http://js.syncfusion.com/demos/ejservices/api/JSPivotGridExport/PDFExport");
        //If want to export to CSV
        pGridObj.exportPivotGrid("http://js.syncfusion.com/demos/ejservices/api/JSPivotGridExport/CSVExport");
     }
{% endhighlight %}

#### PivotGrid Exporting in C# 

{% highlight c# %}

        [System.Web.Http.ActionName("ExcelExport")]
        [System.Web.Http.HttpPost]
        public void ExcelExport()
        {
            PivotGridExcelExport pGrid = new PivotGridExcelExport();
            string args = HttpContext.Current.Request.Form.GetValues(0)[0];
            pGrid.ExportToExcel(string.Empty, args, HttpContext.Current.Response);
        }

        [System.Web.Http.ActionName("PDFExport")]
        [System.Web.Http.HttpPost]
        public void PDFExport()
        {
            PivotGridPDFExport pGrid = new PivotGridPDFExport();
            string args = HttpContext.Current.Request.Form.GetValues(0)[0];
            pGrid.ExportToPDF(string.Empty, args, HttpContext.Current.Response);
        }

        [System.Web.Http.ActionName("WordExport")]
        [System.Web.Http.HttpPost]
        public void WordExport()
        {
            PivotGridWordExport pGrid = new PivotGridWordExport();
            string args = HttpContext.Current.Request.Form.GetValues(0)[0];
            pGrid.ExportToWord(string.Empty, args, HttpContext.Current.Response);
        }

        [System.Web.Http.ActionName("CSVExport")]
        [System.Web.Http.HttpPost]
        public void CSVExport()
        {
            PivotGridCSVExport pGrid = new PivotGridCSVExport();
            string args = HttpContext.Current.Request.Form.GetValues(0)[0];
            pGrid.ExportToCSV(string.Empty, args, HttpContext.Current.Response);
        }
        
{% endhighlight %}
 

###Response

####Code: 200

####Content-Type: application/octet-stream

####Response (Excel, Word, PDF or CSV):
Browser will prompt a dialog box to save the file.

