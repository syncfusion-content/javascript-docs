---
layout: post
title: Export
description: export
platform: js
control: OLAP Client
documentation: ug
---

## Export

The **OLAP Grid** inside the **OLAP Client** component can be exported to an Excel worksheet. A toolbar icon has been added for the implementation of the Excel export feature. On clicking the icon, the OLAP Grid is exported in cell mode to the worksheet of an Excel workbook. The workbook can be saved from the browser to the local disk drive.

{% include image.html url="/js/OlapClient/Concepts-and-Features/Export_images/Export_img1.png" Caption="Excel Export Icon"%}

{% include image.html url="/js/OlapClient/Concepts-and-Features/Export_images/Export_img2.png" Caption="Exported Excel Worksheet"%}

The following code example illustrates how to save the document to Excel via a service.

{% highlight c# %}

public void ExportOptions(Stream stream)
{
OlapGrid olapGridHelper = new OlapGrid();
OlapDataManager DataManager=new OlapDataManager(connectionString);
olapGridHelper.ExportToExcel(DataManager,newStreamReader(stream).ReadToEnd(),"Sample.xls",HttpContext.Current.Response);
}

{% endhighlight %}



