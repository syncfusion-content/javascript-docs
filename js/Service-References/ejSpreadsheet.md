---
layout: post
title: Service reference for ejSpreadsheet widget
description: What are the services used in Essential JavaScript Spreadsheet.
documentation: api
platform: js
keywords: ejSpreadsheet, Services, Essential JS Spreadsheet, Spreadsheet,Importing Service, Spreadsheet Importing,Spreadsheet Importing Service, Excel Exporting Service, Spreadsheet Exporting, PDF Exporting Service, CSV Exporting Service
metaname: 
metacontent:
control: ejSpreadsheet
---

#ejSpreadsheet Services

##Importing Service

### Description

To import excel file in Spreadsheet by using import service.

Note: allowImport must be true while using this property.

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
      <td>Bool</td>
      <td>To specify the  a value indicating whether the sheet on demand is enable or not.</td>
   </tr>
    <tr>
      <td>Password</td>
      <td>String</td>
      <td>To specify the password for the protected import file.</td>
   </tr>
</table>

### Request

{% highlight js %}
 
<div id=”Spreadsheet”></div>
<script>
  var Spreadsheet = $("#Spreadsheet").data("ejSpreadsheet");// Spreadsheet Object
  var importSettings = Spreadsheet.model.importSettings;
  importSettings.allowImport = true; 
  importSettings.importMapper = "http://js.syncfusion.com/demos/ejservices/api/JSXLExport/Import";
  importSettings.importUrl = "http://mvc.syncfusion.com/Spreadsheet/LargeData.xlsx";
  importSettings.allowSheetOnDemand = false;
  importSettings.password = "";
  Spreadsheet.import({ url:importSettings.importUrl, allowSheetOnDemand:importSettings.allowSheetOnDemand });
</script>


{% endhighlight %}

###Response (JSON):

Excel file document imported in spreadsheet.

##Exporting services

### Description

The following exporting options available in Spreadsheet.
*	Excel Export
*	CSV Export
*	PDF Export

Note: allowExport must be true while using this property.

##Excel Export

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

{% highlight js %}
 
<div id=”Spreadsheet”></div>
<script>

var Spreadsheet = $("#Spreadsheet").data("ejSpreadsheet");// Spreadsheet Object
var exportSettings = Spreadsheet.model.exportSettings;
exportSettings.allowExporting = true; 
exportSettings.excelUrl = "http://js.syncfusion.com/demos/ejservices/api/JSXLExport/ExportToExcel";
exportSettings.password = "";
Spreadsheet.XLExport.export("Excel");

</script>


{% endhighlight %}

###Response

####Code: 200

####Content-Type: application/octet-stream

####Response (XLSX,XLS):

Browser will prompt a dialog box to save the file (document).

##CSV Export

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
      <td>type</td>
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

{% highlight js %}
 
<div id=”Spreadsheet”></div>
<script>

var Spreadsheet = $("#Spreadsheet").data("ejSpreadsheet");// Spreadsheet Object
var exportSettings = Spreadsheet.model.exportSettings;
exportSettings.allowExporting = true; 
exportSettings.excelUrl = "http://js.syncfusion.com/demos/ejservices/api/JSXLExport/ExportToCsv";
exportSettings.password = "";
Spreadsheet.XLExport.export("Csv");

</script>


{% endhighlight %}

###Response

####Code: 200

####Content-Type: application/octet-stream

####Response (CSV):

Browser will prompt a dialog box to save the file (document).


##PDF Export

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

{% highlight js %}
 
<div id=”Spreadsheet”></div>
<script>

var Spreadsheet = $("#Spreadsheet").data("ejSpreadsheet");// Spreadsheet Object
var exportSettings = Spreadsheet.model.exportSettings;
exportSettings.allowExporting = true; 
exportSettings.excelUrl = "http://js.syncfusion.com/demos/ejservices/api/JSXLExport/ExportToPdf";
exportSettings.password = "";
Spreadsheet.XLExport.export("Pdf");

</script>


{% endhighlight %}

###Response

####Code: 200

####Content-Type: application/octet-stream

####Response (PDF):

Browser will prompt a dialog box to save the file (document).