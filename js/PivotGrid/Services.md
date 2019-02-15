---
layout: post
title: Service Reference for PivotGrid widget in Syncfusion Essential JS
description: What are the services used in JavaScript ejPivotGrid widget
platform: js
control: ejPivotGrid
documentation: ug
keywords: ejPivotGrid, Services, JS PivotGrid, PivotGrid, PivotGrid Exporting
api: /api/js/ejpivotgrid
---

# ejPivotGrid

PivotGrid widget is an easily configurable, presentation-quality business control that reads both OLAP and relational data sources. It allows you to create multi-dimensional views for analyzing and satisfying business user needs. PivotGrid uses services to initialize and operate widget and also to export PivotGrid to an Excel, Word, PDF, or CSV document.

## WCF/WebAPI service to populate PivotGrid
You can populate a simple PivotGrid with the OLAP/relational data completely from the server-side by using the WCF/WebAPI service. You can refer the **Getting Started** document available in the following UG documentation section.

For relational data source, [click here.](https://help.syncfusion.com/js/pivotgrid/relational-getting-started#creating-a-simple-application-with-pivotgrid-and-relational-datasource-server-mode)

For OLAP data source, [click here.](https://help.syncfusion.com/js/pivotgrid/olap-getting-started#creating-a-simple-application-with-pivotgrid-and-olap-datasource-server-mode)

## Exporting service

### Excel export

You can export the contents of PivotGrid to an Excel document for future archival, references, and analysis purposes.

#### URL

[https://js.syncfusion.com/ejservices/api/PivotGrid/Olap/ExcelExport](https://js.syncfusion.com/ejservices/api/PivotGrid/Olap/ExcelExport)

#### Parameter

<table>
   <th>Type</th>
   <th>URL </th>
   <th>MultipleExport </th>
   <tr>
      <td>Excel</td>
      <td>https://js.syncfusion.com/ejservices/api/PivotGrid/Olap/ExcelExport</td>
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

    <div id="PivotGrid1" style="min-height: 275px; min-width: 525px; height: 460px; width: 720px"></div>
    <button id="btnExport">Export</button>
    <script type="text/javascript">
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
        pGridObj.exportPivotGrid("https://js.syncfusion.com/ejservices/api/PivotGrid/Olap/ExcelExport","fileName");
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
    PivotGridExcelExport pGrid = new PivotGridExcelExport();
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    pGrid.ExportToExcel(string.Empty, args, HttpContext.Current.Response);
}

{% endhighlight %}


#### Response

##### Code: 200

##### Content-Type: application/octet-stream

##### Response for Excel export:
Browser will prompt a dialog box to save the Excel document.

### Word export

You can export the contents of PivotGrid to a Word document for future archival, references, and analysis purposes.

#### URL

[https://js.syncfusion.com/ejservices/api/PivotGrid/Olap/WordExport](https://js.syncfusion.com/ejservices/api/PivotGrid/Olap/WordExport)

#### Parameter

<table>
   <th>Type</th>
   <th>URL </th>
   <th>MultipleExport </th>
   <tr>
      <td>Word</td>
      <td>https://js.syncfusion.com/ejservices/api/PivotGrid/Olap/WordExport</td>
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

    <div id="PivotGrid1" style="min-height: 275px; min-width: 525px; height: 460px; width: 720px"></div>
    <button id="btnExport">Export</button>
    <script type="text/javascript">
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
        pGridObj.exportPivotGrid("https://js.syncfusion.com/ejservices/api/PivotGrid/Olap/WordExport","fileName");
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
    PivotGridWordExport pGrid = new PivotGridWordExport();
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    pGrid.ExportToWord(string.Empty, args, HttpContext.Current.Response);
}

{% endhighlight %}

#### Response

##### Code: 200

##### Content-Type: application/octet-stream

##### Response for Word export:
Browser will prompt a dialog box to save the Word document.

### PDF export

You can export the contents of PivotGrid to a PDF document for future archival, references, and analysis purposes.

#### URL

[https://js.syncfusion.com/ejservices/api/PivotGrid/Olap/PDFExport](https://js.syncfusion.com/ejservices/api/PivotGrid/Olap/PDFExport)

#### Parameter

<table>
   <th>Type</th>
   <th>URL </th>
   <th>MultipleExport </th>
   <tr>
      <td>PDF</td>
      <td>https://js.syncfusion.com/ejservices/api/PivotGrid/Olap/PDFExport</td>
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

    <div id="PivotGrid1" style="min-height: 275px; min-width: 525px; height: 460px; width: 720px"></div>
    <button id="btnExport">Export</button>
    <script type="text/javascript">
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
        pGridObj.exportPivotGrid("https://js.syncfusion.com/ejservices/api/PivotGrid/Olap/PDFExport","fileName");
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
    PivotGridPDFExport pGrid = new PivotGridPDFExport();
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    pGrid.ExportToPDF(string.Empty, args, HttpContext.Current.Response);
}

{% endhighlight %}

#### Response

##### Code: 200

##### Content-Type: application/octet-stream

##### Response for PDF export:
Browser will prompt a dialog box to save the PDF document.

### CSV export

You can export the contents of PivotGrid to a CSV document for future archival, references, and analysis purposes.

#### URL

[https://js.syncfusion.com/ejservices/api/PivotGrid/Olap/CSVExport](https://js.syncfusion.com/ejservices/api/PivotGrid/Olap/CSVExport)

#### Parameter

<table>
   <th>Type</th>
   <th>URL </th>
   <th>MultipleExport </th>
   <tr>
      <td>CSV</td>
      <td>https://js.syncfusion.com/ejservices/api/PivotGrid/Olap/CSVExport</td>
      <td>False</td>
   </tr>
</table>

#### Request

To achieve CSV export, the service URL and the file name are set as parameters.

##### JS

{% highlight html %}

<html>
//...
<body>

    <div id="PivotGrid1" style="min-height: 275px; min-width: 525px; height: 460px; width: 720px"></div>
    <button id="btnExport">Export</button>
    <script type="text/javascript">
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
        pGridObj.exportPivotGrid("https://js.syncfusion.com/ejservices/api/PivotGrid/Olap/CSVExport","fileName");
      }

     </script>
</body>
</html>

{% endhighlight %}

##### C\#

{% highlight c# %}

[System.Web.Http.ActionName("CSVExport")]
[System.Web.Http.HttpPost]
public void CSVExport()
{
    PivotGridCSVExport pGrid = new PivotGridCSVExport();
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    pGrid.ExportToCSV(string.Empty, args, HttpContext.Current.Response);
}

{% endhighlight %}

#### Response

##### Code: 200

##### Content-Type: application/octet-stream

##### Response for CSV export:
Browser will prompt a dialog box to save the CSV document.

