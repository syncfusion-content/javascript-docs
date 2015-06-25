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

public void Export(Stream stream)
 {
System.IO.StreamReader sReader = new System.IO.StreamReader(stream);
string args = System.Web.HttpContext.Current.Server.UrlDecode(sReader.ReadToEnd());
OlapDataManager DataManager = new OlapDataManager(connectionString);
string fileName = "Sample";
olapClientHelper.ExportOlapClient(DataManager, args, fileName, System.Web.HttpContext.Current.Response);
}

{% endhighlight %}



