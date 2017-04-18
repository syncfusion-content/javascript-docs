---
layout: post
title: webAPI reference for ejGantt
description: webAPI reference for ejGantt
documentation: ug
platform: js
keywords: ejGantt,Gantt, syncfusion,ejGantt webapi
---

## ExcelExport

 [POST] [/Api/Gantt/ExcelExport](http://js.syncfusion.com/demos/ejServices/api/Gantt/ExcelExport)

It is used to export the Gantt data to excel file.

### URL parameters

|  Parameter |  Description | 
|---|---|
|GanttModel|It contains the model of the Gantt.|  

### Response information 

Code: 200

Content-Type: application/octet-stream	

### Code example 

{% highlight js %}

$(function () {
      $("#GanttContainer").ejGantt({
      dataSource: projectData,
      toolbarSettings: {
      showToolbar: true,
      toolbarItems: [
      ej.Gantt.ToolbarItems.ExcelExport,            
      ]
      },
      toolbarClick: toolbarclick
      });
});

function toolbarclick(args) {
var id = $(args.currentTarget).attr("id");
this.exportGrid = this["export"];
if (id == "GanttContainer_excelExport") {			
      this.exportGrid("http://js.syncfusion.com/demos/ejServices/api/Gantt/ExcelExport", "", false);
      args.cancel = true;
}
}

{% endhighlight %}
