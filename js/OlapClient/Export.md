---
layout: post
title: Export
description: export
platform: js
control: OLAPClient
documentation: ug
---

# Export

Content in the OLAP Client control can be exported to Excel, Word and PDF documents.

{% include image.html url="/js/OlapClient/Export_images/Export_img1.png" %}

Exporting feature comes with a mode option that allows you to export either OlapChart or PivotGrid or both. The following code example illustrates the same. 

{% highlight js %}

$("#OlapClient").ejOlapClient({ 
    url: "../wcf/OlapClientService.svc", 
    title: "OLAP Browser", 
    clientExportMode: ej.olap.OlapClient.ClientExportMode.ChartAndGrid
});

{% endhighlight %}

The property `clientExportMode` takes any one of the following value:
1. ChartAndGrid – Exports both OlapChart and PivotGrid controls. This is the default mode.
2. ChartOnly – Exports OlapChart control alone.
3. GridOnly – Exports PivotGrid control alone.

The following service method needs to be added in-order to perform exporting in OlapClient.

{% highlight c# %}

public void Export(Stream stream)
{
    System.IO.StreamReader sReader = new System.IO.StreamReader(stream);
    string args = System.Web.HttpContext.Current.Server.UrlDecode(sReader.ReadToEnd());
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    string fileName = "OlapClient";
    olapClientHelper.ExportOlapClient(DataManager, args, fileName,
    System.Web.HttpContext.Current.Response);
}

{% endhighlight %}

{% include image.html url="/js/OlapClient/Export_images/Export_img2.png" Caption="Exported OlapClient in Excel worksheet"%}

{% include image.html url="/js/OlapClient/Export_images/Export_img3.png" Caption="Exported OlapClient in Word document"%}

{% include image.html url="/js/OlapClient/Export_images/Export_img4.png" Caption="Exported OlapClient in PDF document"%}


