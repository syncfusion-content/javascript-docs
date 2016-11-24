---
layout: post
title: webAPI reference for ejService related controls
description: webAPI reference for ejService related controls
documentation: WebAPI
platform: js-webapi

---

# WebAPI reference for ej Controls

The details of WebAPI has been shown in the below table.
### Chart

| WebAPI | Description  |
|---|---|
|[Export](WebAPI\Chart#Export)|It is used to export the Chart control to the specified format.|
|[SvgExport](WebAPI\Chart#SvgExport)|It is used to export the Chart control as an SVG image.|
|[ExcelExport](WebAPI\Chart#ExcelExport)|It is used to export the Chart control as an Excel document.|
|[WordExport](WebAPI\Chart#WordExport)|It is used to export the Chart control as a Word document.|
|[PdfExport](WebAPI\Chart#PdfExport)|It is used to export the Chart control as a PDF document.|
|[ImageExport](WebAPI\Chart#ImageExport)|It is used to export the chart control as an image (PNG/JPG).|


### Diagram

|  WebAPI | Description  |
|---|---|
|[GetNodes](WebAPI\Diagram#GetNodes)|It fetches the collection of records from database and further it will be used to generate the shapes.|
|[GetConnectors](WebAPI\Diagram#GetConnectors)|It fetches the collection of records from database and further it will be used to generate the connectors.|
|[AddNodes](WebAPI\Diagram#AddNodes)|It is used to send one or more shapes which needs to be inserted into database.|
|[UpdateNodes](WebAPI\Diagram#UpdateNodes)|Send one or more shapes which needs to be modified into database.|
|[DeleteNodes](WebAPI\Diagram#DeleteNodes)|Send one or more shapes which needs to be deleted from database.|
|[AddConnectors](WebAPI\Diagram#)|Send one or more connectors which needs to be inserted into database.|
|[UpdateConnectors](WebAPI\Diagram#UpdateConnectors)|Send one or more connectors which needs to be modified into database.|
|[DeleteConnectors](WebAPI\Diagram#DeleteConnectors)|Send one or more connectors which needs to be deleted from database.|

### DocIO

|  WebAPI | Description  |
|---|---|
|[ConvertToPDF](WebAPI\DocIO#ConvertToPDF)|It is used to generate the PDF document.|

### DocumentEditor

|  WebAPI | Description  |
|---|---|
|[Import](WebAPI\DocumentEditor#Import)|It loads the document from specified path in DocumentEditor.|
|[FileUpload](WebAPI\DocumentEditor#FileUpload)|It loads the default document in DocumentEditor.|


### FileExplorer

|  WebAPI | Description  |
|---|---|
|[FileOperations](WebAPI\FileExplorer#FileOperations)|It helps to handle the FileExplorer operations like Read, Upload, Download, GetDetails, Rename, Remove etc|
|[FileOperationsCors](WebAPI\FileExplorer#FileOperationsCors)|It helps to handle the FileExplorer operations in cross origin.|

### Gantt

|  WebAPI | Description  |
|---|---|
|[ExcelExport](WebAPI\Gantt#ExcelExport)|It is used to export the Gantt data to PDF file.


### Grid
|  WebAPI | Description  |
|---|---|
|[Northwind Data Service](WebAPI\Grid#NorthwindDataService)|Used to retrieve the records from “Orders” table in Remote Data Service.|
|[PdfExport](WebAPI\Grid#PdfExport)|Used to export the Grid data in PDF.|  
|[ExcelExport](WebAPI\Grid#ExcelExport)|Used to export the Grid data in Excel.|
|[WordExport](WebAPI\Grid#WordExport)|Used to export the Grid data in Word.|  
|[Get](WebAPI\Grid#Get)|It is used to get the dataSource from Northwind dataSource.|  
|[Post](WebAPI\Grid#Post)|It is used to add the data to the grid column. .|  
|[Put](WebAPI\Grid#Put)|It is used to update the Grid data.|  
|[Delete](WebAPI\Grid#Delete)|It is used to delete the data which is present in Grid column.| 

### OlapChart

|  WebAPI | Description  |
|---|---|
|[Initialize](WebAPI\OlapChart#Initialize)|It fetches the OLAP data required to initialize the PivotChart from server-end.|
|[Drill](WebAPI\OlapChart#Drill)|It fetches the drilled OLAP data required to render the PivotChart control from server-end.|
|[Export](WebAPI\OlapChart#Export)|It exports the PivotChart control at the instant to the specified format.|
|[ExcelExport](WebAPI\OlapChart#ExcelExport)|It exports the PivotChart control at the instant to an Excel document.|
|[WordExport](WebAPI\OlapChart#WordExport)|It exports the PivotChart control at the instant to an Word document.|
|[PdfExport](WebAPI\OlapChart#PdfExport)|It exports the PivotChart control at the instant to an PDF document.| 
|[ImageExport](WebAPI\OlapChart#ImageExport)|It exports the PivotChart control at the instant as an Image in specified format.|

### OlapClient

|  WebAPI | Description  |
|---|---|
|[Initialize](WebAPI\OlapClient#Initialize)||
|[InitializeGrid](WebAPI\OlapClient#InitializeGrid)||
|[InitializeChart](WebAPI\OlapClient#InitializeChart)||
|[InitializeTreeMap](WebAPI\OlapClient#InitializeTreeMap)||
|[DrillChart](WebAPI\OlapClient#DrillChart)||
|[DrillTreeMap](WebAPI\OlapClient#DrillTreeMap)||
|[DrillGrid](WebAPI\OlapClient#DrillGrid)||
|[FilterElement](WebAPI\OlapClient#FilterElement)||
|[RemoveSplitButton](WebAPI\OlapClient#RemoveSplitButton)||
|[FetchMemberTreeNodes](WebAPI\OlapClient#FetchMemberTreeNodes)||
|[DropNode](WebAPI\OlapClient#DropNode)||
|[CubeChange](WebAPI\OlapClient#CubeChange)||
|[MeasureGroup](WebAPI\OlapClient#MeasureGroup)||
|[ToolbarOperations](WebAPI\OlapClient#ToolbarOperations)||
|[UpdateReport](WebAPI\OlapClient#UpdateReport)||
|[SaveReportToDB](WebAPI\OlapClient#SaveReportToDB)||
|[FetchReportListFromDB](WebAPI\OlapClient#FetchReportListFromDB)||
|[LoadReportFromDB](WebAPI\OlapClient#LoadReportFromDB)||
|[Export](WebAPI\OlapClient#Export)||
|[ExportOlapClient](WebAPI\OlapClient#ExportOlapClient)||
|[GetMDXQuery](WebAPI\OlapClient#GetMDXQuery)||
|[ToggleAxis](WebAPI\OlapClient#ToggleAxis)||
|[Paging](WebAPI\OlapClient#Paging)||

### OlapGauge

|  WebAPI | Description  |
|---|---|
|[Initialize](WebAPI\OlapGauge#Initialize)|It fetches the OLAP data required to render the PivotGauge control from server-end.|


### OlapGrid

|  WebAPI | Description  |
|---|---|
|[Initialize](WebAPI\OlapGrid#Initialize)|It fetches the OLAP data required to render the PivotGrid initially from server-end.|
|[Drill](WebAPI\OlapGrid#Drill)|It fetches the OLAP data required to render the PivotGrid control after drilling it.|
|[DropNode](WebAPI\OlapGrid#DropNode)|It fetches the data required to render the control after performing node drop operation.|
|[Filtering](WebAPI\OlapGrid#Filtering)|It fetches the OLAP data required to render the specific page of PivotGrid with paging enabled.|
|[FetchMembers](WebAPI\OlapGrid#FetchMembers)|It fetches the OLAP data required to render the specific page of PivotGrid with paging enabled.|
|[Paging](WebAPI\OlapGrid#Paging)|It fetches the members of the selected hierarchy to render the member editor.|
|[RemoveButton](WebAPI\OlapGrid#RemoveButton)|It fetches the data required to render the control after removing a button.|
|[ExpandMember](WebAPI\OlapGrid#ExpandMember)|It fetches the data to render children nodes of a member in Member Editor Tree.|
|[Export](WebAPI\OlapGrid#Export)|It is used to export the PivotGrid data as an Excel document.|
|[SaveReport](WebAPI\OlapGrid#SaveReport)|It loads a report from the database and refreshes the control with it.|
|[LoadReportFromDB](WebAPI\OlapGrid#LoadReportFromDB)|It loads a report from the database and refreshes the control with it.|
|[DeferUpdate](WebAPI\OlapGrid#DeferUpdate)|It fetches the data with respect to the report available at that instant (i.e) updates the control with current report.|
|[ExcelExport](WebAPI\OlapGrid#ExcelExport)|It exports the PivotGrid control at that instant to the Excel format.|
|[PdfExport](WebAPI\OlapGrid#PdfExport)|It exports the PivotGrid control at the instant to PDF document.|
|[WordExport](WebAPI\OlapGrid#WordExport)|It exports the PivotGrid control at the instant to Word document.|
|[CsvExport](WebAPI\OlapGrid#CsvExport)|It exports the PivotGrid control at the instant to Csv document.|


### OlapTreeMap

|  WebAPI | Description  |
|---|---|
|[Initialize](WebAPI\OlapTreeMap#Initialize)|It fetches the OLAP data required to render the PivotTreeMap control from server-end.|
|[Drill](WebAPI\OlapTreeMap#Drill)|It fetches the OLAP data required to render the drilled PivotTreeMap.|


### PDF

|  WebAPI | Description  |
|---|---|
|[GeneratePdfDocument](WebAPI\PDF#GeneratePdfDocument)||
|[GetFormFillTemplate](WebAPI\PDF#GetFormFillTemplate)||
|[GenerateFormFillTemplate](WebAPI\PDF#GenerateFormFillTemplate)||
|[GenerateInteractiveFeature](WebAPI\PDF#GenerateInteractiveFeature)||
|[GenerateEncryptDocument](WebAPI\PDF#GenerateEncryptDocument)||
|[GenerateTableFeature](WebAPI\PDF#GenerateTableFeature)||


### PdfViewer

|  WebAPI | Description  |
|---|---|
|[Load](WebAPI\PdfViewer#Load)|It loads the PDF document in the PDF viewer control and process the PDF document for each request.|
|[FileUpload](WebAPI\PdfViewer#FileUpload)|It uploads and loads the PDF document to the PDF viewer control.|
|[Download](WebAPI\PdfViewer#Download)|It downloads the PDF document that is in view of the PDF viewer control.|


### Predictive Analysis

|  WebAPI | Description  |
|---|---|
|[Load](WebAPI\PredictiveAnalysis#Load)|It is used to the load the data.|


### RelationalChart

|  WebAPI | Description  |
|---|---|
|[](WebAPI\RelationalChart#)||
|[](WebAPI\RelationalChart#)||

### RelationalClient

|  WebAPI | Description  |
|---|---|
|[](WebAPI\RelationalClient#)||

### RelationalGauge

|  WebAPI | Description  |
|---|---|
|[](WebAPI\RelationalGauge#)||

### RelationalGrid

|  WebAPI | Description  |
|---|---|
|[](WebAPI\RelationalGrid#)||

### RichTextEditor

|  WebAPI | Description  |
|---|---|
|[Import](WebAPI\RichTextEdtior#Import)|It is used to Import a Word document into RTE.|
|[WordExport](WebAPI\RichTextEdtior#WordExport)|It is used for exporting the contents of RTE into a Word document.|
|[PdfExport](WebAPI\RichTextEdtior#PdfExport)|It is used for exporting the contents of RTE into a PDF document.|


### Schedule

|  WebAPI | Description  |
|---|---|
|[LoadData](WebAPI\Schedule#LoadData)|It fetches the records from Default Schedule table and binding it to the Scheduler.|
|[PdfExport](WebAPI\Schedule#PdfExport)|It exports the entire Scheduler content into a PDF file format.|
|[IcsExport](WebAPI\Schedule#IcsExport)|It exports the complete appointment data from Scheduler into an ICS file format.|
|[Save](WebAPI\Schedule#Save)|It imports the appointment data generated from external calendar into Scheduler.|


### SpellCheck

| WebAPI | Description  |
|---|---|
|[CheckWords](WebAPI\SpellCheck#CheckWords)|It is used for splitting the input string into separate words and checking whether it is an erroneous word or not. Also, it forms a list of error words and its corresponding suggestions as a collection.|   
|[AddToDictionary](WebAPI\SpellCheck#AddToDictionary)|It is used to add the custom word into the custom dictionary file.|   


### Spreadsheet

|  WebAPI | Description  |
|---|---|
|[ExcelExport](WebAPI\Spreadsheet#ExcelExport)|It is used to export the Spreadsheet data as an Excel document.|
|[CsvExport](WebAPI\Spreadsheet#CsvExport)|It is used to export the Spreadsheet data to Csv file.|
|[PdfExport](WebAPI\Spreadsheet#PdfExport)|It is used to export the Spreadsheet data as a PDF document.|
|[Import](WebAPI\Spreadsheet#Import)|It loads the document from specified path in Spreadsheet.|

### TreeGrid

|  WebAPI | Description  |
|---|---|
|[PdfExport](WebAPI\TreeGrid#PdfExport)|It is used to export the TreeGrid data to PDF file.|
|[ExcelExport](WebAPI\TreeGrid#ExcelExport)|It is used to export the TreeGrid data to Excel file.|

### UploadBox

|  WebAPI | Description  |
|---|---|
|[Save](WebAPI\UploadBox#Save)|It is used for storing the uploaded file.|
|[Remove](WebAPI\UploadBox#Remove)|It is used for removing the stored files from server.|

