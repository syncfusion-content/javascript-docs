---
layout: post
title: Export
description: export
platform: js
control: PivotGrid
documentation: ug
---

# Export



The **PivotGrid** is exported to a worksheet of an Excel Workbook. The Excel Workbook is saved from the browser to the local disk drive.

The following code example illustrates how to save the document to Excel via service.

> **Note:** This feature is applicable only for OLAP datasource.

{% highlight c# %}

public void Export(System.IO.Stream stream) 
{
System.IO.StreamReader sReader = new System.IO.StreamReader(stream);
string args = System.Web.HttpContext.Current.Server.UrlDecode(sReader.ReadToEnd());
OlapDataManager DataManager = new OlapDataManager(connectionString);
string fileName = "Sample";
htmlHelper.ExportPivotGrid(DataManager, args, fileName, System.Web.HttpContext.Current.Response);
}
{% endhighlight %}

{% highlight html %}

<button id="Button1">Export Grid</button>
<div id="PivotGrid1" style="height: 350px; width: 100%; overflow: auto"> </div>

{% endhighlight %}

{% highlight js %}

$(function() {
    $("#PivotGrid1").ejPivotGrid({
        url: "../wcf/PivotGridService.svc"
    });
    $("#Button1").ejButton({
        size: "normal",
        roundedCorner: true,
        click: "btnClick"
    });
});

function btnClick(e) {
    pivotGridObj = $('#PivotGrid').data("ejPivotGrid");
    pivotGridObj.exportPivotGrid("excel");
}

{% endhighlight %}

{% include image.html url="/js/PivotGrid/Export_images/Export_img1.png" %}

