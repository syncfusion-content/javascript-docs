---
layout: post
title: webAPI reference for ejService related controls
description: webAPI reference for ejService related controls
documentation: ug
platform: js
---

# WebAPI reference for ej Controls

The details of WebAPI has been shown in the below table.

### Chart

| WebAPI | Description |
|---|---|
|[Export](WebAPI/Chart#export)|It is used to export the Chart control to the specified format.|
|[SvgExport](WebAPI/Chart#svgexport)|It is used to export the Chart control as an SVG image.|
|[ExcelExport](WebAPI/Chart#excelexport)|It is used to export the Chart control as an Excel document.|
|[WordExport](WebAPI/Chart#wordexport)|It is used to export the Chart control as a Word document.|
|[PdfExport](WebAPI/Chart#pdfexport)|It is used to export the Chart control as a PDF document.|
|[ImageExport](WebAPI/Chart#imageexport)|It is used to export the chart control as an image (PNG/JPG).|

### Diagram

| WebAPI | Description |
|---|---|
|[GetNodes](WebAPI/Diagram#getnodes)|It fetches the collection of records from database and further it will be used to generate the shapes.|
|[GetConnectors](WebAPI/Diagram#getconnectors)|It fetches the collection of records from database and also it will be used to generate the connectors.|
|[AddNodes](WebAPI/Diagram#addnodes)|It is used to send one or more shapes which needs to be inserted into database.|
|[UpdateNodes](WebAPI/Diagram#updatenodes)|It sends one or more shapes which needs to be modified into database.|
|[DeleteNodes](WebAPI/Diagram#deletenodes)|It sends one or more shapes which needs to be deleted from database.|
|[AddConnectors](WebAPI/Diagram#addconnectors)|It sends one or more connectors which needs to be inserted into database.|
|[UpdateConnectors](WebAPI/Diagram#updateconnectors)|It sends one or more connectors which needs to be modified into database.|
|[DeleteConnectors](WebAPI/Diagram#deleteconnectors)|It sends one or more connectors which needs to be deleted from database.|

### DocIO

| WebAPI | Description |
|---|---|
|[GenerateWordDocument](WebAPI/DocIO#generateworddocument)|It is used to create a simple Word document with text, image and tables.|
|[ConvertToPDF](WebAPI/DocIO#converttopdf)|It is used to generate the PDF document.|
|[ApplyTextFormat](WebAPI/DocIO#applytextformat)|It is used to generate Word Document with various text formats such as character/text level formatting, paragraph level formatting and list level formatting.|
|[GetInvoiceTemplate](WebAPI/DocIO#getinvoicetemplate)|It is used to get invoice template Word document.|
|[GenerateInvoice](WebAPI/DocIO#generateinvoice)|It is used to generate sales invoice report using Mail merge functionality.|
|[GetMailmergeTemplate](WebAPI/DocIO#getmailmergetemplate)|It is used to get Mail merge template Word Document.|
|[ExecuteNestedMailmerge](WebAPI/DocIO#executenestedmailmerge)|It is used to perform Mail merge for nested groups in Word Document.|


### DocumentEditor

| WebAPI | Description |
|---|---|
|[Import](WebAPI/DocumentEditor#import)|It loads the document from specified path in DocumentEditor.|
|[LoadDefault](WebAPI/DocumentEditor#loaddefault)|It loads the default document in DocumentEditor.|

### FileExplorer

| WebAPI | Description |
|---|---|
|[FileOperations](WebAPI/FileExplorer#fileOoerations)|It helps to handle the FileExplorer operations like Read, Upload, Download, GetDetails, Rename, Remove etc.|
|[FileOperationsCors](WebAPI/FileExplorer#fileoperationscors)|It helps to handle the FileExplorer operations in cross origin.|

### Gantt

| WebAPI | Description |
|---|---|
|[ExcelExport](WebAPI/Gantt#excelexport)|It is used to export the Gantt data to PDF file.|

### Grid

| WebAPI | Description |
|---|---|
|[PdfExport](WebAPI/Grid#pdfexport)|It is used to export the Grid data in PDF.|  
|[ExcelExport](WebAPI/Grid#excelexport)|It is used to export the Grid data in Excel.|
|[WordExport](WebAPI/Grid#wordexport)|It is used to export the Grid data in Word.|  
|[Get](WebAPI/Grid#get)|It is used to get the dataSource from Northwind dataSource.|  
|[Post](WebAPI/Grid#post)|It is used to add the data to the grid column.|  
|[Put](WebAPI/Grid#put)|It is used to update the Grid data.|  
|[Delete](WebAPI/Grid#delete)|It is used to delete the data which is present in Grid column.| 

### PDF

| WebAPI | Description |
|---|---|
|[GeneratePdfDocument](WebAPI/PDF#generatepdfdocument)||
|[GetFormFillTemplate](WebAPI/PDF#getformfilltemplate)||
|[GenerateFormFillTemplate](WebAPI/PDF#generateformfilltemplate)||
|[GenerateInteractiveFeature](WebAPI/PDF#generateinteractivefeature)||
|[GenerateEncryptDocument](WebAPI/PDF#generateencryptdocument)||
|[GenerateTableFeature](WebAPI/PDF#generatetablefeature)||

### PdfViewer

| WebAPI | Description |
|---|---|
|[Load](WebAPI/PdfViewer#load)|It loads the PDF document in the PDF viewer control and process the PDF document for each request.|
|[FileUpload](WebAPI/PdfViewer#fileupload)|It uploads and loads the PDF document to the PDF viewer control.|
|[Download](WebAPI/PdfViewer#download)|It downloads the PDF document that is in view of the PDF viewer control.|

### PivotChart (Relational)

| WebAPI | Description |
|---|---|
|[Initialize](WebAPI/RelationalChart#initialize)|It fetches the Relational data required to initialize the PivotChart from server-end.|
|[Drill](WebAPI/RelationalChart#drill)|It fetches the drilled Relational data required to render the PivotChart control from server-end.|
|[Export](WebAPI/RelationalChart#export)|It exports the PivotChart control at the instant to the specified format.|

### PivotChart (OLAP)

| WebAPI | Description |
|---|---|
|[Initialize](WebAPI/OlapChart#initialize)|It fetches the OLAP data required to initialize the PivotChart from server-end.|
|[Drill](WebAPI/OlapChart#drill)|It fetches the drilled OLAP data required to render the PivotChart control from server-end.|
|[Export](WebAPI/OlapChart#export)|It exports the PivotChart control at the instant to the specified format.|
|[ExcelExport](WebAPI/OlapChart#excelexport)|It exports the PivotChart control at the instant to an Excel document.|
|[WordExport](WebAPI/OlapChart#wordexport)|It exports the PivotChart control at the instant to a Word document.|
|[PdfExport](WebAPI/OlapChart#pdfexport)|It exports the PivotChart control at the instant to a PDF document.|
|[ImageExport](WebAPI/OlapChart#imageexport)|It exports the PivotChart control at the instant as an Image in specified format.|

### PivotClient (Relational)

| WebAPI | Description |
|---|---|
|[Initialize](WebAPI/RelationalClient#initialize)|It fetches the data required to initialize the control.|
|[FetchMembers](WebAPI/RelationalClient#fetchmembers)|It fetches the details of the members in the selected field on opening member editor.|
|[DrillChart](WebAPI/RelationalClient#drillchart)|It fetches the drilled data required to render the control on performing drilldown in PivotChart.|
|[Filtering](WebAPI/RelationalClient#filtering)|It fetches the data required to render the control on performing filtering.|
|[DropNode](WebAPI/RelationalClient#dropnode)|It fetches the data required to render the control on performing node drop action.|
|[ToolbarOperations](WebAPI/RelationalClient#toolbaroperations)|It fetches the data required to render the control on performing toolbar operations.|
|[SaveReportToDB](WebAPI/RelationalClient#savereporttodb)|It saves the current report to database with the specified name.|
|[Export](WebAPI/RelationalClient#export)|It exports the PivotGrid or PivotChart or both to the selected format.|
|[FetchReportListFromDB](WebAPI/RelationalClient#fetchreportlistfromdb)|It fetches the list of names of reports stored in database.|
|[LoadReportFromDB](WebAPI/RelationalClient#loadreportfromdb)|It loads the report with specified name from the database to the control.|

### PivotClient (OLAP)

| WebAPI | Description |
|---|---|
|[Initialize](WebAPI/OlapClient#initialize)|It fetches the data required to render the PivotClient control initially.|
|[InitializeGrid](WebAPI/OlapClient#initializegrid)|It fetches the data required to render the PivotGrid control inside PivotClient.|
|[InitializeChart](WebAPI/OlapClient#initializechart)|It fetches the data required to render the PivotChart control inside PivotClient.|
|[InitializeTreeMap](WebAPI/OlapClient#initializetreemap)|It fetches the data required to render the PivotTreeMap control inside PivotClient.|
|[DrillChart](WebAPI/OlapClient#drillchart)|It fetches the drilled data required to render the PivotChart on drilling.|
|[DrillTreeMap](WebAPI/OlapClient#drilltreemap)|It fetches the drilled data required to render the PivotTreeMap on drilling.|
|[DrillGrid](WebAPI/OlapClient#drillgrid)|It fetches the drilled data required to render the PivotGrid on drilling.|
|[FilterElement](WebAPI/OlapClient#filterelement)|It fetches the filtered data required to render the control after performing filtering.|
|[RemoveSplitButton](WebAPI/OlapClient#removesplitbutton)|It fetches the drilled data required to render the PivotChart on removing an item from report.|
|[FetchMemberTreeNodes](WebAPI/OlapClient#fetchmembertreenodes)|It fetches the details of the members to render the member editor dialog.|
|[DropNode](WebAPI/OlapClient#dropnode)|It fetches the data required to render the control after drag and drop action.|
|[CubeChange](WebAPI/OlapClient#cubechange)|It fetches the data required to render the control on changing the cube.|
|[MeasureGroup](WebAPI/OlapClient#measuregroup)|It fetches the data required to render the control on changing the measure group.|
|[ToolbarOperations](WebAPI/OlapClient#toolbaroperations)|It fetches the data required to render the control on performing toolbar operations.|
|[ExpandMember](WebAPI/OlapClient#expandmember)|It fetches the children nodes on expanding a node in Member Editor.|
|[UpdateReport](WebAPI/OlapClient#updatereport)|It updates the report in server side.|
|[SaveReportToDB](WebAPI/OlapClient#savereporttodb)|It saves the current report to database with the specified name.|
|[FetchReportListFromDB](WebAPI/OlapClient#fetchreportlistfromdb)|It fetches the list of names of reports stored in database.|
|[LoadReportFromDB](WebAPI/OlapClient#loadreportfromdb)|It loads the report with specified name from the database to the control.|
|[Export](WebAPI/OlapClient#export)|It exports the PivotGrid or PivotChart or both to the selected format.|
|[ExportOlapClient](WebAPI/OlapClient#exportolapclient)|It exports the PivotGrid or PivotChart or both with OLAP data to the selected format.|
|[GetMDXQuery](WebAPI/OlapClient#getmdxquery)|It retrieves the MDX query formed to fetch the data at that instant.|
|[ToggleAxis](WebAPI/OlapClient#toggleaxis)|It fetches the data after interchanging the elements in row and column axes.|
|[Paging](WebAPI/OlapClient#paging)|It fetches the data on navigating between pages in PivotClient with OLAP data.|

### PivotGauge (Relational)

| WebAPI | Description |
|---|---|
|[Initialize](WebAPI/RelationalGauge#initialize)|It fetches the Relational data required to render the PivotGauge control from server-end.|

### PivotGauge (OLAP)

| WebAPI | Description |
|---|---|
|[Initialize](WebAPI/OlapGauge#initialize)|It fetches the OLAP data required to render the PivotGauge control from server-end.|

### PivotGrid (Relational)

| WebAPI | Description |
|---|---|
|[Initialize](WebAPI/RelationalGrid#initialize)|It fetches the data required to render the PivotGrid initially.|
|[FetchMembers](WebAPI/RelationalGrid#fetchmembers)|It fetches the members of the selected field to render the member editor tree.|
|[Filtering](WebAPI/RelationalGrid#filtering)|It fetches the data required to render the PivotGrid control on performing filtering action.|
|[ModifyNodeState](WebAPI/RelationalGrid#modifynodestate)|It fetches the relational data required to render the PivotGrid control on selecting/unselecting fields in Field list.|
|[DropNode](WebAPI/RelationalGrid#dropnode)|It fetches the relational data required to render the PivotGrid control on node drop action.|
|[Sorting](WebAPI/RelationalGrid#sorting)|It fetches the sorted data to render the PivotGrid control on performing sorting.|
|[CalculatedField](WebAPI/RelationalGrid#calculatedfield)|It forms a calculated field in values area and fetches the data along with it to render the PivotGrid control.|
|[Export](WebAPI/RelationalGrid#export)|It is used to export the PivotGrid data to specified format.|
|[SaveReport](WebAPI/RelationalGrid#savereport)|It saves the current report to database with the specified name.|
|[LoadReportFromDB](WebAPI/RelationalGrid#loadreportfromdb)|It loads a report from the database and refreshes the control with it.|
|[DeferUpdate](WebAPI/RelationalGrid#deferupdate)|It fetches the data with respect to the report available at that instant (i.e) updates the control with current report.|
|[CellEditing](WebAPI/RelationalGrid#cellediting)|It rewrites the content of database on editing a cell.|

### PivotGrid (OLAP)

| WebAPI | Description |
|---|---|
|[Initialize](WebAPI/OlapGrid#initialize)|It fetches the OLAP data required to render the PivotGrid initially from server-end.|
|[Drill](WebAPI/OlapGrid#drill)|It fetches the OLAP data required to render the PivotGrid control after drilling it.|
|[DropNode](WebAPI/OlapGrid#dropnode)|It fetches the data required to render the control after performing node drop operation.|
|[Filtering](WebAPI/OlapGrid#filtering)|It fetches the OLAP data required to render the control after performing filtering.|
|[FetchMembers](WebAPI/OlapGrid#fetchmembers)|It fetches the members of the selected hierarchy to render the member editor.|
|[Paging](WebAPI/OlapGrid#paging)|It fetches the OLAP data required to render the specific page of PivotGrid with paging enabled.|
|[RemoveButton](WebAPI/OlapGrid#removebutton)|It fetches the data required to render the control after removing a button.|
|[ExpandMember](WebAPI/OlapGrid#expandmember)|It fetches the data to render children nodes of a member in Member Editor Tree.|
|[Export](WebAPI/OlapGrid#export)|It is used to export the PivotGrid data to specified format.|
|[SaveReport](WebAPI/OlapGrid#savereport)|It saves the current report to database with the specified name.|
|[LoadReportFromDB](WebAPI/OlapGrid#loadreportfromdb)|It loads a report from the database and refreshes the control with it.|
|[DeferUpdate](WebAPI/OlapGrid#deferupdate)|It fetches the data with respect to the report available at that instant (i.e) updates the control with current report.|
|[ExcelExport](WebAPI/OlapGrid#excelexport)|It exports the PivotGrid control at that instant to Excel document.|
|[PdfExport](WebAPI/OlapGrid#pdfexport)|It exports the PivotGrid control at the instant to PDF document.|
|[WordExport](WebAPI/OlapGrid#wordexport)|It exports the PivotGrid control at the instant to Word document.|
|[CsvExport](WebAPI/OlapGrid#csvexport)|It exports the PivotGrid control at the instant to CSV document.|

### PivotTreeMap (OLAP)

| WebAPI | Description |
|---|---|
|[Initialize](WebAPI/OlapTreeMap#initialize)|It fetches the OLAP data required to render the PivotTreeMap control from server-end.|
|[Drill](WebAPI/OlapTreeMap#drill)|It fetches the OLAP data required to render the drilled PivotTreeMap.|

### Presentation

|  WebAPI | Description  |
|---|---|
|[CreatePresentation](WebAPI/Presentation#createpresentation)|It is used to generate a simple PowerPoint presentation.|
|[ManipulateSmartArt](WebAPI/Presentation#manipulatesmartart)|It is used to manipulate SmartArt in PowerPoint slides.|
|[MergePresentations](WebAPI/Presentation#mergepresentations)|It is used to merge two PowerPoint presentations.|
|[CreateNotes](WebAPI/Presentation#createnotes)|It is used to add notes page in PowerPoint slides and converts the notes page to PDF document.|
|[ConvertToPDF](WebAPI/Presentation#converttopdf)|It is used to convert the PowerPoint presentation to PDF.|

### Predictive Analytics

| WebAPI | Description |
|---|---|
|[Load](WebAPI/PredictiveAnalytics#load)|It is used to the load the data.|

### RichTextEditor

| WebAPI | Description |
|---|---|
|[Import](WebAPI/RichTextEditor#import)|It is used to Import a Word document into RTE.|
|[WordExport](WebAPI/RichTextEditor#wordexport)|It is used for exporting the contents of RTE into a Word document.|
|[PdfExport](WebAPI/RichTextEditor#pdfexport)|It is used for exporting the contents of RTE into a PDF document.|

### Schedule

| WebAPI | Description |
|---|---|
|[LoadData](WebAPI/Schedule#loaddata)|It fetches the records from Default Schedule table and binding it to the Scheduler.|
|[PdfExport](WebAPI/Schedule#pdfexport)|It exports the entire Scheduler content into a PDF file format.|
|[IcsExport](WebAPI/Schedule#icsexport)|It exports the complete appointment data from Scheduler into an ICS file format.|
|[Save](WebAPI/Schedule#save)|It imports the appointment data generated from external calendar into Scheduler.|

### SpellCheck

| WebAPI | Description |
|---|---|
|[CheckWords](WebAPI/SpellCheck#checkwords)|It is used for splitting the input string into separate words and checking whether it is an erroneous word or not. Also, it forms a list of error words and its corresponding suggestions as a collection.|   
|[AddToDictionary](WebAPI/SpellCheck#addtodictionary)|It is used to add the custom word into the custom dictionary file.|   

### Spreadsheet

| WebAPI | Description |
|---|---|
|[ExcelExport](WebAPI/Spreadsheet#excelexport)|It is used to export the Spreadsheet data as an Excel document.|
|[CsvExport](WebAPI/Spreadsheet#csvexport)|It is used to export the Spreadsheet data to Csv file.|
|[PdfExport](WebAPI/Spreadsheet#pdfexport)|It is used to export the Spreadsheet data as a PDF document.|
|[Import](WebAPI/Spreadsheet#import)|It loads the document from specified path in Spreadsheet.|

### TreeGrid

| WebAPI | Description |
|---|---|
|[PdfExport](WebAPI/TreeGrid#pdfexport)|It is used to export the TreeGrid data to PDF file.|
|[ExcelExport](WebAPI/TreeGrid#excelexport)|It is used to export the TreeGrid data to Excel file.|

### UploadBox

| WebAPI | Description |
|---|---|
|[Save](WebAPI/UploadBox#save)|It is used for storing the uploaded file.|
|[Remove](WebAPI/UploadBox#remove)|It is used for removing the stored files from server.|

### XlsIO

|  WebAPI | Description  |
|---|---|
|[CreateDocument](WebAPI/XlsIO#createdocument)|To generate an Excel document format like XLS, XLSX, CSV, Excel Template, Excel Macro Enabled Template.|
|[WriteFormula](WebAPI/XlsIO#writeformula)|This method will generate an Excel document with different formulae.|
|[ReadFormula](WebAPI/XlsIO#readformula)|To read the formula string as well as value from the Excel document.|
|[CreateChart](WebAPI/XlsIO#createchart)|To create an embedded chart in Excel document.|
|[ImportDataObject](WebAPI/XlsIO#importdataobject)|To import data directly from various objects like DataTable, Business Objects, etc to an Excel document.|
|[ApplyTemplateMarker](WebAPI/XlsIO#applytemplatemarker)|Import data to an Excel document using [template marker](https://help.syncfusion.com/file-formats/xlsio/working-with-template-markers). |
[InputTemplate](WebAPI/XlsIO#inputtemplate)|To get an Excel template document used for various template marker types.|