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

| WebAPI | Description |
|---|---|
|[Export](WebAPI\Chart#Export)|It is used to export the Chart control to the specified format.|
|[SvgExport](WebAPI\Chart#SvgExport)|It is used to export the Chart control as an SVG image.|
|[ExcelExport](WebAPI\Chart#ExcelExport)|It is used to export the Chart control as an Excel document.|
|[WordExport](WebAPI\Chart#WordExport)|It is used to export the Chart control as a Word document.|
|[PdfExport](WebAPI\Chart#PdfExport)|It is used to export the Chart control as a PDF document.|
|[ImageExport](WebAPI\Chart#ImageExport)|It is used to export the chart control as an image (PNG/JPG).|

### Diagram

| WebAPI | Description |
|---|---|
|[GetNodes](WebAPI\Diagram#GetNodes)|It fetches the collection of records from database and further it will be used to generate the shapes.|
|[GetConnectors](WebAPI\Diagram#GetConnectors)|It fetches the collection of records from database and also it will be used to generate the connectors.|
|[AddNodes](WebAPI\Diagram#AddNodes)|It is used to send one or more shapes which needs to be inserted into database.|
|[UpdateNodes](WebAPI\Diagram#UpdateNodes)|It sends one or more shapes which needs to be modified into database.|
|[DeleteNodes](WebAPI\Diagram#DeleteNodes)|It sends one or more shapes which needs to be deleted from database.|
|[AddConnectors](WebAPI\Diagram#AddConnectors)|It sends one or more connectors which needs to be inserted into database.|
|[UpdateConnectors](WebAPI\Diagram#UpdateConnectors)|It sends one or more connectors which needs to be modified into database.|
|[DeleteConnectors](WebAPI\Diagram#DeleteConnectors)|It sends one or more connectors which needs to be deleted from database.|

### DocIO

| WebAPI | Description |
|---|---|
|[GenerateWordDocument](WebAPI\DocIO#GenerateWordDocument)|It is used to generate the simple Word document or PDF.|
|[ApplyTextFormat](WebAPI\DocIO#ApplyTextFormat)|It is used to generate the Word document or PDF with applied text format.|
|[GetInvoiceTemplate](WebAPI\DocIO#GetInvoiceTemplate)|It is used to get sales invoice template Word document.|
|[GenerateInvoice](WebAPI\DocIO#GenerateInvoice)|It is used to generate sales invoice Word document or PDF.|
|[GetMailmergeTemplate](WebAPI\DocIO#GetMailmergeTemplate)|It is used to  get Mail merge template Word document.|
|[ExecuteNestedMailmerge](WebAPI\DocIO#ExecuteNestedMailmerge)|It is used to execute nested Mail merge in Word document or PDF.|
|[ConvertToPDF](WebAPI\DocIO#ConvertToPDF)|It is used to convert the Word document to PDF.|

### DocumentEditor

| WebAPI | Description |
|---|---|
|[Import](WebAPI\DocumentEditor#Import)|It loads the document from specified path in DocumentEditor.|
|[FileUpload](WebAPI\DocumentEditor#FileUpload)|It loads the default document in DocumentEditor.|

### FileExplorer

| WebAPI | Description |
|---|---|
|[FileOperations](WebAPI\FileExplorer#FileOperations)|It helps to handle the FileExplorer operations like Read, Upload, Download, GetDetails, Rename, Remove etc.|
|[FileOperationsCors](WebAPI\FileExplorer#FileOperationsCors)|It helps to handle the FileExplorer operations in cross origin.|

### Gantt

| WebAPI | Description |
|---|---|
|[ExcelExport](WebAPI\Gantt#ExcelExport)|It is used to export the Gantt data to PDF file.|

### Grid

| WebAPI | Description |
|---|---|
|[PdfExport](WebAPI\Grid#PdfExport)|It is used to export the Grid data in PDF.|  
|[ExcelExport](WebAPI\Grid#ExcelExport)|It is used to export the Grid data in Excel.|
|[WordExport](WebAPI\Grid#WordExport)|It is used to export the Grid data in Word.|  
|[Get](WebAPI\Grid#Get)|It is used to get the dataSource from Northwind dataSource.|  
|[Post](WebAPI\Grid#Post)|It is used to add the data to the grid column.|  
|[Put](WebAPI\Grid#Put)|It is used to update the Grid data.|  
|[Delete](WebAPI\Grid#Delete)|It is used to delete the data which is present in Grid column.| 

### PivotChart (Relational)

| WebAPI | Description |
|---|---|
|[Initialize](WebAPI\RelationalChart#Initialize)|It fetches the Relational data required to initialize the PivotChart from server-end.|
|[Drill](WebAPI\RelationalChart#Drill)|It fetches the drilled Relational data required to render the PivotChart control from server-end.|
|[Export](WebAPI\RelationalChart#Export)|It exports the PivotChart control at the instant to the specified format.|

### PivotChart (OLAP)

| WebAPI | Description |
|---|---|
|[Initialize](WebAPI\OlapChart#Initialize)|It fetches the OLAP data required to initialize the PivotChart from server-end.|
|[Drill](WebAPI\OlapChart#Drill)|It fetches the drilled OLAP data required to render the PivotChart control from server-end.|
|[Export](WebAPI\OlapChart#Export)|It exports the PivotChart control at the instant to the specified format.|
|[ExcelExport](WebAPI\OlapChart#ExcelExport)|It exports the PivotChart control at the instant to an Excel document.|
|[WordExport](WebAPI\OlapChart#WordExport)|It exports the PivotChart control at the instant to a Word document.|
|[PdfExport](WebAPI\OlapChart#PdfExport)|It exports the PivotChart control at the instant to a PDF document.|
|[ImageExport](WebAPI\OlapChart#ImageExport)|It exports the PivotChart control at the instant as an Image in specified format.|

### PivotClient (Relational)

| WebAPI | Description |
|---|---|
|[Initialize](WebAPI\RelationalClient#Initialize)|It fetches the data required to initialize the control.|
|[FetchMembers](WebAPI\RelationalClient#FetchMembers)|It fetches the details of the members in the selected field on opening member editor.|
|[DrillChart](WebAPI\RelationalClient#DrillChart)|It fetches the drilled data required to render the control on performing drilldown in PivotChart.|
|[Filtering](WebAPI\RelationalClient#Filtering)|It fetches the data required to render the control on performing filtering.|
|[DropNode](WebAPI\RelationalClient#DropNode)|It fetches the data required to render the control on performing node drop action.|
|[ToolbarOperations](WebAPI\RelationalClient#ToolbarOperations)|It fetches the data required to render the control on performing toolbar operations.|
|[SaveReportToDB](WebAPI\RelationalClient#SaveReportToDB)|It saves the current report to database with the specified name.|
|[Export](WebAPI\RelationalClient#Export)|It exports the PivotGrid or PivotChart or both to the selected format.|
|[FetchReportListFromDB](WebAPI\RelationalClient#FetchReportListFromDB)|It fetches the list of names of reports stored in database.|
|[LoadReportFromDB](WebAPI\RelationalClient#LoadReportFromDB)|It loads the report with specified name from the database to the control.|

### PivotClient (OLAP)

| WebAPI | Description |
|---|---|
|[Initialize](WebAPI\OlapClient#Initialize)|It fetches the data required to render the PivotClient control initially.|
|[InitializeGrid](WebAPI\OlapClient#InitializeGrid)|It fetches the data required to render the PivotGrid control inside PivotClient.|
|[InitializeChart](WebAPI\OlapClient#InitializeChart)|It fetches the data required to render the PivotChart control inside PivotClient.|
|[InitializeTreeMap](WebAPI\OlapClient#InitializeTreeMap)|It fetches the data required to render the PivotTreeMap control inside PivotClient.|
|[DrillChart](WebAPI\OlapClient#DrillChart)|It fetches the drilled data required to render the PivotChart on drilling.|
|[DrillTreeMap](WebAPI\OlapClient#DrillTreeMap)|It fetches the drilled data required to render the PivotTreeMap on drilling.|
|[DrillGrid](WebAPI\OlapClient#DrillGrid)|It fetches the drilled data required to render the PivotGrid on drilling.|
|[FilterElement](WebAPI\OlapClient#FilterElement)|It fetches the filtered data required to render the control after performing filtering.|
|[RemoveSplitButton](WebAPI\OlapClient#RemoveSplitButton)|It fetches the drilled data required to render the PivotChart on removing an item from report.|
|[FetchMemberTreeNodes](WebAPI\OlapClient#FetchMemberTreeNodes)|It fetches the details of the members to render the member editor dialog.|
|[DropNode](WebAPI\OlapClient#DropNode)|It fetches the data required to render the control after drag and drop action.|
|[CubeChange](WebAPI\OlapClient#CubeChange)|It fetches the data required to render the control on changing the cube.|
|[MeasureGroup](WebAPI\OlapClient#MeasureGroup)|It fetches the data required to render the control on changing the measure group.|
|[ToolbarOperations](WebAPI\OlapClient#ToolbarOperations)|It fetches the data required to render the control on performing toolbar operations.|
|[ExpandMember](WebAPI\OlapClient#ExpandMember)|It fetches the children nodes on expanding a node in Member Editor.|
|[UpdateReport](WebAPI\OlapClient#UpdateReport)|It updates the report in server side.|
|[SaveReportToDB](WebAPI\OlapClient#SaveReportToDB)|It saves the current report to database with the specified name.|
|[FetchReportListFromDB](WebAPI\OlapClient#FetchReportListFromDB)|It fetches the list of names of reports stored in database.|
|[LoadReportFromDB](WebAPI\OlapClient#LoadReportFromDB)|It loads the report with specified name from the database to the control.|
|[Export](WebAPI\OlapClient#Export)|It exports the PivotGrid or PivotChart or both to the selected format.|
|[ExportOlapClient](WebAPI\OlapClient#ExportOlapClient)|It exports the PivotGrid or PivotChart or both with OLAP data to the selected format.|
|[GetMDXQuery](WebAPI\OlapClient#GetMDXQuery)|It retrieves the MDX query formed to fetch the data at that instant.|
|[ToggleAxis](WebAPI\OlapClient#ToggleAxis)|It fetches the data after interchanging the elements in row and column axes.|
|[Paging](WebAPI\OlapClient#Paging)|It fetches the data on navigating between pages in PivotClient with OLAP data.|

### PivotGauge (Relational)

| WebAPI | Description |
|---|---|
|[Initialize](WebAPI\RelationalGauge#Initialize)|It fetches the Relational data required to render the PivotGauge control from server-end.|

### PivotGauge (OLAP)

| WebAPI | Description |
|---|---|
|[Initialize](WebAPI\OlapGauge#Initialize)|It fetches the OLAP data required to render the PivotGauge control from server-end.|

### PivotGrid (Relational)

| WebAPI | Description |
|---|---|
|[Initialize](WebAPI\RelationalGrid#Initialize)|It fetches the data required to render the PivotGrid initially.|
|[FetchMembers](WebAPI\RelationalGrid#FetchMembers)|It fetches the members of the selected field to render the member editor tree.|
|[Filtering](WebAPI\RelationalGrid#Filtering)|It fetches the data required to render the PivotGrid control on performing filtering action.|
|[ModifyNodeState](WebAPI\RelationalGrid#ModifyNodeState)|It fetches the relational data required to render the PivotGrid control on selecting/unselecting fields in Field list.|
|[DropNode](WebAPI\RelationalGrid#DropNode)|It fetches the relational data required to render the PivotGrid control on node drop action.|
|[Sorting](WebAPI\RelationalGrid#Sorting)|It fetches the sorted data to render the PivotGrid control on performing sorting.|
|[CalculatedField](WebAPI\RelationalGrid#CalculatedField)|It forms a calculated field in values area and fetches the data along with it to render the PivotGrid control.|
|[Export](WebAPI\RelationalGrid#Export)|It is used to export the PivotGrid data to specified format.|
|[SaveReport](WebAPI\RelationalGrid#SaveReport)|It saves the current report to database with the specified name.|
|[LoadReportFromDB](WebAPI\RelationalGrid#LoadReportFromDB)|It loads a report from the database and refreshes the control with it.|
|[DeferUpdate](WebAPI\RelationalGrid#DeferUpdate)|It fetches the data with respect to the report available at that instant (i.e) updates the control with current report.|
|[CellEditing](WebAPI\RelationalGrid#CellEditing)|It rewrites the content of database on editing a cell.|

### PivotGrid (OLAP)

| WebAPI | Description |
|---|---|
|[Initialize](WebAPI\OlapGrid#Initialize)|It fetches the OLAP data required to render the PivotGrid initially from server-end.|
|[Drill](WebAPI\OlapGrid#Drill)|It fetches the OLAP data required to render the PivotGrid control after drilling it.|
|[DropNode](WebAPI\OlapGrid#DropNode)|It fetches the data required to render the control after performing node drop operation.|
|[Filtering](WebAPI\OlapGrid#Filtering)|It fetches the OLAP data required to render the control after performing filtering.|
|[FetchMembers](WebAPI\OlapGrid#FetchMembers)|It fetches the members of the selected hierarchy to render the member editor.|
|[Paging](WebAPI\OlapGrid#Paging)|It fetches the OLAP data required to render the specific page of PivotGrid with paging enabled.|
|[RemoveButton](WebAPI\OlapGrid#RemoveButton)|It fetches the data required to render the control after removing a button.|
|[ExpandMember](WebAPI\OlapGrid#ExpandMember)|It fetches the data to render children nodes of a member in Member Editor Tree.|
|[Export](WebAPI\OlapGrid#Export)|It is used to export the PivotGrid data to specified format.|
|[SaveReport](WebAPI\OlapGrid#SaveReport)|It saves the current report to database with the specified name.|
|[LoadReportFromDB](WebAPI\OlapGrid#LoadReportFromDB)|It loads a report from the database and refreshes the control with it.|
|[DeferUpdate](WebAPI\OlapGrid#DeferUpdate)|It fetches the data with respect to the report available at that instant (i.e) updates the control with current report.|
|[ExcelExport](WebAPI\OlapGrid#ExcelExport)|It exports the PivotGrid control at that instant to Excel document.|
|[PdfExport](WebAPI\OlapGrid#PdfExport)|It exports the PivotGrid control at the instant to PDF document.|
|[WordExport](WebAPI\OlapGrid#WordExport)|It exports the PivotGrid control at the instant to Word document.|
|[CsvExport](WebAPI\OlapGrid#CsvExport)|It exports the PivotGrid control at the instant to CSV document.|

### PivotTreeMap (OLAP)

| WebAPI | Description |
|---|---|
|[Initialize](WebAPI\OlapTreeMap#Initialize)|It fetches the OLAP data required to render the PivotTreeMap control from server-end.|
|[Drill](WebAPI\OlapTreeMap#Drill)|It fetches the OLAP data required to render the drilled PivotTreeMap.|


### PDF

| WebAPI | Description |
|---|---|
|[GeneratePdfDocument](WebAPI\PDF#GeneratePdfDocument)||
|[GetFormFillTemplate](WebAPI\PDF#GetFormFillTemplate)||
|[GenerateFormFillTemplate](WebAPI\PDF#GenerateFormFillTemplate)||
|[GenerateInteractiveFeature](WebAPI\PDF#GenerateInteractiveFeature)||
|[GenerateEncryptDocument](WebAPI\PDF#GenerateEncryptDocument)||
|[GenerateTableFeature](WebAPI\PDF#GenerateTableFeature)||

### PdfViewer

| WebAPI | Description |
|---|---|
|[Load](WebAPI\PdfViewer#Load)|It loads the PDF document in the PDF viewer control and process the PDF document for each request.|
|[FileUpload](WebAPI\PdfViewer#FileUpload)|It uploads and loads the PDF document to the PDF viewer control.|
|[Download](WebAPI\PdfViewer#Download)|It downloads the PDF document that is in view of the PDF viewer control.|

### Predictive Analytics

| WebAPI | Description |
|---|---|
|[Load](WebAPI\PredictiveAnalytics#Load)|It is used to the load the data.|

### RichTextEditor

| WebAPI | Description |
|---|---|
|[Import](WebAPI\RichTextEditor#Import)|It is used to Import a Word document into RTE.|
|[WordExport](WebAPI\RichTextEditor#WordExport)|It is used for exporting the contents of RTE into a Word document.|
|[PdfExport](WebAPI\RichTextEditor#PdfExport)|It is used for exporting the contents of RTE into a PDF document.|

### Schedule

| WebAPI | Description |
|---|---|
|[LoadData](WebAPI\Schedule#LoadData)|It fetches the records from Default Schedule table and binding it to the Scheduler.|
|[PdfExport](WebAPI\Schedule#PdfExport)|It exports the entire Scheduler content into a PDF file format.|
|[IcsExport](WebAPI\Schedule#IcsExport)|It exports the complete appointment data from Scheduler into an ICS file format.|
|[Save](WebAPI\Schedule#Save)|It imports the appointment data generated from external calendar into Scheduler.|

### SpellCheck

| WebAPI | Description |
|---|---|
|[CheckWords](WebAPI\SpellCheck#CheckWords)|It is used for splitting the input string into separate words and checking whether it is an erroneous word or not. Also, it forms a list of error words and its corresponding suggestions as a collection.|   
|[AddToDictionary](WebAPI\SpellCheck#AddToDictionary)|It is used to add the custom word into the custom dictionary file.|   

### Spreadsheet

| WebAPI | Description |
|---|---|
|[ExcelExport](WebAPI\Spreadsheet#ExcelExport)|It is used to export the Spreadsheet data as an Excel document.|
|[CsvExport](WebAPI\Spreadsheet#CsvExport)|It is used to export the Spreadsheet data to Csv file.|
|[PdfExport](WebAPI\Spreadsheet#PdfExport)|It is used to export the Spreadsheet data as a PDF document.|
|[Import](WebAPI\Spreadsheet#Import)|It loads the document from specified path in Spreadsheet.|

### TreeGrid

| WebAPI | Description |
|---|---|
|[PdfExport](WebAPI\TreeGrid#PdfExport)|It is used to export the TreeGrid data to PDF file.|
|[ExcelExport](WebAPI\TreeGrid#ExcelExport)|It is used to export the TreeGrid data to Excel file.|

### UploadBox

| WebAPI | Description |
|---|---|
|[Save](WebAPI\UploadBox#Save)|It is used for storing the uploaded file.|
|[Remove](WebAPI\UploadBox#Remove)|It is used for removing the stored files from server.|