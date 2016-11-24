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