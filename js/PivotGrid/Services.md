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

### Excel Export

User can export the contents of PivotGrid to an Excel document for future archival, references and analysis purposes.

#### URL

[http://js.syncfusion.com/ejservices/api/PivotGrid/Olap/ExcelExport](http://js.syncfusion.com/ejservices/api/PivotGrid/Olap/ExcelExport)

#### Parameter

<table>
   <th>Type</th>
   <th>URL </th>
   <th>MultipleExport </th>
   <tr>
      <td>Excel</td>
      <td>http://js.syncfusion.com/ejservices/api/PivotGrid/Olap/ExcelExport</td>
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
        pGridObj.exportPivotGrid("http://js.syncfusion.com/ejservices/api/PivotGrid/Olap/ExcelExport","fileName");
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

##### Response for Excel Export:
Browser will prompt a dialog box to save the Excel document.

### Word Export

User can export the contents of PivotGrid to a Word document for future archival, references and analysis purposes.

#### URL

[http://js.syncfusion.com/ejservices/api/PivotGrid/Olap/WordExport](http://js.syncfusion.com/ejservices/api/PivotGrid/Olap/WordExport)

#### Parameter

<table>
   <th>Type</th>
   <th>URL </th>
   <th>MultipleExport </th>
   <tr>
      <td>Word</td>
      <td>http://js.syncfusion.com/ejservices/api/PivotGrid/Olap/WordExport</td>
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
        pGridObj.exportPivotGrid("http://js.syncfusion.com/ejservices/api/PivotGrid/Olap/WordExport","fileName");
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

### PDF Export

User can export the contents of PivotGrid to a PDF document for future archival, references and analysis purposes.

#### URL

[http://js.syncfusion.com/ejservices/api/PivotGrid/Olap/PDFExport](http://js.syncfusion.com/ejservices/api/PivotGrid/Olap/PDFExport)

#### Parameter

<table>
   <th>Type</th>
   <th>URL </th>
   <th>MultipleExport </th>
   <tr>
      <td>PDF</td>
      <td>http://js.syncfusion.com/ejservices/api/PivotGrid/Olap/PDFExport</td>
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
        pGridObj.exportPivotGrid("http://js.syncfusion.com/ejservices/api/PivotGrid/Olap/PDFExport","fileName");
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

### CSV Export

User can export the contents of PivotGrid to a CSV document for future archival, references and analysis purposes.

#### URL

[http://js.syncfusion.com/ejservices/api/PivotGrid/Olap/CSVExport](http://js.syncfusion.com/ejservices/api/PivotGrid/Olap/CSVExport)

#### Parameter

<table>
   <th>Type</th>
   <th>URL </th>
   <th>MultipleExport </th>
   <tr>
      <td>CSV</td>
      <td>http://js.syncfusion.com/ejservices/api/PivotGrid/Olap/CSVExport</td>
      <td>False</td>
   </tr>
</table>

#### Request

To achieve CSV export, service URL and file name is sent as the parameter.

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
        pGridObj.exportPivotGrid("http://js.syncfusion.com/ejservices/api/PivotGrid/Olap/CSVExport","fileName");
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

