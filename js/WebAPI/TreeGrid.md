---
layout: post
title: webAPI reference for ejTreeGrid
description: webAPI reference for ejTreeGrid
documentation: ug
platform: js
keywords: ejTreeGrid,TreeGrid, syncfusion,ejTreeGrid webapi
---

## PdfExport

 [POST] [/Api/TreeGrid/PdfExport](http://js.syncfusion.com/demos/ejServices/api/TreeGrid/PdfExport)

It is used to export the TreeGrid data to PDF file.

### URL parameters

|  Parameter |  Description | 
|---|---|
|TreeGridModel|It contains the model of the TreeGrid|  

### Response information 

Code: 200

Content-Type: application/octet-stream	

### Code example 

{% highlight js %}

$(function () {
      var dateFormat = "{0:" + ej.preferredCulture()["calendars"]["standard"]["patterns"]["d"] + "}";
      $("#TreeGridContainer").ejTreeGrid({
      dataSource: sampleData,
      childMapping: "subtasks",
      toolbarClick: toolbarClickEvent,
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

function toolbarClickEvent(args) {
      var id= $(args.currentTarget).attr("id");
      this.exportGrid = this["export"];
      if (id == "TreeGridContainer_pdfExport") { this.exportGrid("http://js.syncfusion.com/demos/ejServices/api/TreeGrid/PdfExport", "", false);
      args.cancel = true;
      }

}

{% endhighlight %}

## ExcelExport

 [POST] [/Api/TreeGrid/ExcelExport](http://js.syncfusion.com/demos/ejServices/api/TreeGrid/ExcelExport)

It is used to export the TreeGrid data to Excel file.

### URL parameters

|  Parameter |  Description | 
|---|---|
|TreeGridModel|It contains the model of the TreeGrid|  

### Response information 

Code: 200

Content-Type: application/octet-stream	

{% highlight js %}

$(function () {
      var dateFormat = "{0:" + ej.preferredCulture()["calendars"]["standard"]["patterns"]["d"] + "}";
      $("#TreeGridContainer").ejTreeGrid({
      dataSource: sampleData,
      childMapping: "subtasks",
      toolbarClick: toolbarClickEvent,
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

function toolbarClickEvent(args) {
      var id= $(args.currentTarget).attr("id");
      this.exportGrid = this["export"];
      if (id == "TreeGridContainer_pdfExport") { this.exportGrid("http://js.syncfusion.com/demos/ejServices/api/TreeGrid/ExcelExport", "", false);
      args.cancel = true;
      }

}

{% endhighlight %}