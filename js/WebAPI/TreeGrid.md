---
layout: post
title: webAPI reference for ejTreeGrid
description: webAPI reference for ejTreeGrid
documentation: API
platform: js-webapi
keywords: ejTreeGrid,TreeGrid, syncfusion,ejTreeGrid webapi
---

## PdfExport

[POST&nbsp;&nbsp;/Api/TreeGrid/PdfExport](http://js.syncfusion.com/demos/ejServices/api/TreeGrid/PdfExport)

It is used to export the TreeGrid data to PDF file.

### URL parameters

|  Parameter |  Description | 
|---|---|
|TreeGridModel|It contains the model of the TreeGrid|  

### Response information 

Code: 200

Content-Type: application/octet-stream	

### Code example 

```javascript

$(function () {
      var dateFormat = "{0:" + ej.preferredCulture()["calendars"]["standard"]["patterns"]["d"] + "}";
      $("#TreeGridContainer").ejTreeGrid({
      dataSource: sampleData,
      childMapping: "subtasks",
      toolbarClick: toolbarclick,
      toolbarSettings: {
      showToolbar: true,
      toolbarItems: [
      ej.TreeGrid.ToolbarItems.PdfExport
      ]
      },
      columns: [
      { field: "taskID", headerText: "Task Id", width: "45" },
      { field: "taskName", headerText: "Task Name" },
      { field: "startDate", headerText: "Start Date", format: dateFormat },               
      ]
      })
 });

function toolbarclick(args) {
      var id= $(args.currentTarget).attr("id");
      this.exportGrid = this["export"];
      if (id == "TreeGridContainer_pdfExport") { this.exportGrid("http://js.syncfusion.com/demos/ejServices/api/TreeGrid/PdfExport", "", false);
      args.cancel = true;
      }

}

```

## ExcelExport

[POST&nbsp;&nbsp;/Api/TreeGrid/ExcelExport](http://js.syncfusion.com/demos/ejServices/api/TreeGrid/ExcelExport)

It is used to export the TreeGrid data to Excel file.

### URL parameters

|  Parameter |  Description | 
|---|---|
|TreeGridModel|It contains the model of the TreeGrid|  

### Response information 

Code: 200

Content-Type: application/octet-stream	

```javascript

$(function () {
      var dateFormat = "{0:" + ej.preferredCulture()["calendars"]["standard"]["patterns"]["d"] + "}";
      $("#TreeGridContainer").ejTreeGrid({
      dataSource: sampleData,
      childMapping: "subtasks",
      toolbarClick: toolbarclick,
      toolbarSettings: {
      showToolbar: true,
      toolbarItems: [
      ej.TreeGrid.ToolbarItems.ExcelExport
      ]
      },
      columns: [
      { field: "taskID", headerText: "Task Id", width: "45" },
      { field: "taskName", headerText: "Task Name" },
      { field: "startDate", headerText: "Start Date", format: dateFormat },               
      ]
      })
 });

function toolbarclick(args) {
      var id= $(args.currentTarget).attr("id");
      this.exportGrid = this["export"];
      if (id == "TreeGridContainer_pdfExport") { this.exportGrid("http://js.syncfusion.com/demos/ejServices/api/TreeGrid/ExcelExport", "", false);
      args.cancel = true;
      }

}

```