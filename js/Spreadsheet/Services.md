---
layout: post
title: Service reference for ejSpreadsheet widget
description: What is the service used for importing and exporting  ejSpreadsheet
platform: js
keywords: ejSpreadsheet, Services, Essential JS Spreadsheet, Spreadsheet,Importing Service, Spreadsheet Importing,Spreadsheet Importing Service, Excel Exporting Service, Spreadsheet Exporting, PDF Exporting Service, CSV Exporting Service
metaname: 
metacontent:
control: ejSpreadsheet
documentation: ug
api: /api/js/ejspreadsheet
---

## Importing service

### Description

To import an excel file in Spreadsheet by using import service.

N> [`allowImport`](https://help.syncfusion.com/api/js/ejspreadsheet#members:allowimport "allowImport") must be true.

### URL

[http://js.syncfusion.com/demos/ejservices/api/JSXLExport/Import](http://js.syncfusion.com/demos/ejservices/api/JSXLExport/Import)


### Parameter
<table>
   <th>Name</th>
   <th>DataType </th>
   <th>Description</th>
   <tr>
      <td>File</td>
      <td>HttpPostedFileBase</td>
      <td>To specify the excel file.</td>
   </tr>
   <tr>
      <td>Url</td>
      <td>String</td>
      <td>To specify the URL of the online files which is imported to the spreadsheet.</td>
   </tr>
    <tr>
      <td>AllowSheetOnDemand</td>
      <td>Boolean</td>
      <td>To specify the  a value indicating whether the sheet on demand is enable or not.</td>
   </tr>
    <tr>
      <td>Password</td>
      <td>String</td>
      <td>To specify the password for the protected import file.</td>
   </tr>
</table>

### Request

{% highlight html %}
<div id=”Spreadsheet”></div>
{% endhighlight %}

{% highlight js %}
  var Spreadsheet = $("#Spreadsheet").data("ejSpreadsheet");// Spreadsheet Object
  var importSettings = Spreadsheet.model.importSettings;
  importSettings.allowImport = true; 
  importSettings.importMapper = "http://js.syncfusion.com/demos/ejservices/api/JSXLExport/Import";
  importSettings.importUrl = "http://mvc.syncfusion.com/Spreadsheet/LargeData.xlsx";
  importSettings.allowSheetOnDemand = false;
  importSettings.password = "";
  Spreadsheet.import({ url:importSettings.importUrl, allowSheetOnDemand:importSettings.allowSheetOnDemand });
{% endhighlight %}

### Response (JSON)

Excel file document which is imported in spreadsheet.

## Exporting service

### Description

The following exporting options are available in Spreadsheet.

*	Excel Export
*	CSV Export
*	PDF Export

N> [`allowExporting`](https://help.syncfusion.com/api/js/ejspreadsheet#members:exportsettings-allowexporting "allowExporting") must be true.

## Excel Export

### Description

To export spreadsheet data as Excel document.

### URL

[http://js.syncfusion.com/demos/ejservices/api/JSXLExport/ExportToExcel](http://js.syncfusion.com/demos/ejservices/api/JSXLExport/ExportToExcel)

### Parameter

<table>
   <th>Name</th>
   <th>DataType </th>
   <th>Description</th>
   <tr>
      <td>type</td>
      <td>Enum</td>
      <td>To specify the type of the file to be downloaded (XLSX, XLS).</td>
   </tr>
   <tr>
      <td>Password</td>
      <td>String</td>
      <td>To set the password for the file to be downloaded</td>
   </tr>
</table>

### Request

{% highlight html %}
<div id=”Spreadsheet”></div>
{% endhighlight %}

{% highlight js %}
  var Spreadsheet = $("#Spreadsheet").data("ejSpreadsheet");// Spreadsheet Object
  var exportSettings = Spreadsheet.model.exportSettings;
  exportSettings.allowExporting = true; 
  exportSettings.excelUrl = "http://js.syncfusion.com/demos/ejservices/api/JSXLExport/ExportToExcel";
  exportSettings.password = "";
  Spreadsheet.XLExport.export("Excel");
{% endhighlight %}

### Response

#### Code: 200

#### Content-Type: application/octet-stream

#### Response (XLSX,XLS)

Browser will prompt a dialog box to save the file (document).

## CSV Export

### Description

To export spreadsheet data as CSV document.

### URL

[http://js.syncfusion.com/demos/ejservices/api/JSXLExport/ExportToCsv](http://js.syncfusion.com/demos/ejservices/api/JSXLExport/ExportToCsv)

### Parameter

<table>
   <th>Name</th>
   <th>DataType </th>
   <th>Description</th>
   <tr>
      <td>Type</td>
      <td>Enum</td>
      <td>To specify the type of the file to be downloaded (CSV).</td>
   </tr>
   <tr>
      <td>Password</td>
      <td>String</td>
      <td>To set the password for the file to be downloaded</td>
   </tr>
</table>

### Request

{% highlight html %}
<div id=”Spreadsheet”></div>
{% endhighlight %}

{% highlight js %}
  var Spreadsheet = $("#Spreadsheet").data("ejSpreadsheet");// Spreadsheet Object
  var exportSettings = Spreadsheet.model.exportSettings;  
  exportSettings.allowExporting = true; 
  exportSettings.csvUrl = "http://js.syncfusion.com/demos/ejservices/api/JSXLExport/ExportToCsv";
  exportSettings.password = "";
  Spreadsheet.XLExport.export("Csv");
{% endhighlight %}

### Response

#### Code: 200

#### Content-Type: application/octet-stream

#### Response (CSV):

Browser will prompt a dialog box to save the file (document).

## PDF Export

### Description

To export spreadsheet data as PDF document.

### URL

[http://js.syncfusion.com/demos/ejservices/api/JSXLExport/ExportToPdf](http://js.syncfusion.com/demos/ejservices/api/JSXLExport/ExportToPdf)

### Parameter

<table>
   <th>Name</th>
   <th>DataType </th>
   <th>Description</th>
   <tr>
      <td>type</td>
      <td>Enum</td>
      <td>To specify the type of the file to be downloaded (PDF).</td>
   </tr>
   <tr>
      <td>Password</td>
      <td>String</td>
      <td>To set the password for the file to be downloaded</td>
   </tr>
</table>

### Request

{% highlight html %}
<div id=”Spreadsheet”></div>
{% endhighlight %}

{% highlight js %}
  var Spreadsheet = $("#Spreadsheet").data("ejSpreadsheet");// Spreadsheet Object
  var exportSettings = Spreadsheet.model.exportSettings;
  exportSettings.allowExporting = true; 
  exportSettings.pdfUrl = "http://js.syncfusion.com/demos/ejservices/api/JSXLExport/ExportToPdf";
  exportSettings.password = "";
  Spreadsheet.XLExport.export("Pdf");
{% endhighlight %}

### Response

#### Code: 200

#### Content-Type: application/octet-stream

#### Response (PDF)

Browser will prompt a dialog box to save the file (document).