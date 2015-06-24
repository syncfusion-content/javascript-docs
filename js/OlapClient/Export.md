---
layout: post
title: Export
description: export
platform: js
control: OlapClient
documentation: ug
---

# Export

The **PivotGrid** inside the **OlapClient** component can be exported to an Excel worksheet. A toolbar icon has been added for the implementation of the Excel export feature. On clicking the icon, the PivotGrid is exported in cell mode to the worksheet of an Excel workbook. The workbook can be saved from the browser to the local disk drive.

{% include image.html url="/js/OlapClient/Export_images/Export_img1.png" Caption="Excel Export Icon"%}

{% include image.html url="/js/OlapClient/Export_images/Export_img2.png" Caption="Exported Excel Worksheet"%}

The following code example illustrates how to save the document to Excel via a service.

{% highlight c# %}

public void ExportOptions(Stream stream)
{
PivotGrid pivotGridHelper = new PivotGrid();
OlapDataManager DataManager=new OlapDataManager(connectionString);
pivotGridHelper.ExportToExcel(DataManager,newStreamReader(stream).ReadToEnd(),"Sample.xls",HttpContext.Current.Response);
}

{% endhighlight %}



