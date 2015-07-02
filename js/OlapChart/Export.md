---
layout: post
title: Export
description: export
platform: js
control: OlapChart
documentation: ug
---

# Export

The OLAP Chart control can be exported to the following formats:
* Excel
* Word
* PDF
* CSV
* PNG
* EMF
* GIF
* JPG
* BMP

{% highlight html %}

<div>
    <button id="ExportBtn">Export</button>
</div>

{% endhighlight %}

{% highlight js %}

$(function () {
    $("#OlapChart").ejOlapChart({
         url: "../wcf/OlapChartService.svc"
    });
    $("#ExportBtn").ejButton({
         roundedCorner: true,
         size: "small",
         click: "exportBtnClick"
    });
});
function exportBtnClick(args) {
    var chartObj = $('#OlapChart').data("ejOlapChart");
    chartObj.exportOlapChart(ej.olap.OlapChart.ExportOptions.Excel);   
}

{% endhighlight %}

Export type which is to be mentioned in the parameter takes any one of the enumerated values – Excel, Word, PDF, CSV, PNG, EMF, GIF, JPG and BMP.

The following service method needs to be added in-order to perform exporting in OlapChart.

{% highlight c# %}

public void Export(System.IO.Stream stream)
{
    System.IO.StreamReader sReader = new System.IO.StreamReader(stream);
    string args = System.Web.HttpContext.Current.Server.UrlDecode(sReader.ReadToEnd());
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    string fileName = "OlapChart";
    htmlHelper.ExportOlapChart(DataManager, args, fileName,
    System.Web.HttpContext.Current.Response);
}

{% endhighlight %}

{% include image.html url="/js/OlapChart/Export_images/Export_img1.png" Caption="Exported OlapChart in Excel"%}

{% include image.html url="/js/OlapChart/Export_images/Export_img2.png" Caption="Exported OlapChart in Word"%}

{% include image.html url="/js/OlapChart/Export_images/Export_img3.png" Caption="Exported OlapChart in PDF"%}

{% include image.html url="/js/OlapChart/Export_images/Export_img4.png" Caption="Exported OlapChart in image formats"%}


