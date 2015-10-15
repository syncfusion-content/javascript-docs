---
layout: post
title: Export
description: export
platform: js
control: PivotGrid
documentation: ug
---

# Export

N>  This feature is applicable only for OLAP datasource.

The PivotGrid control can be exported to the following formats:

* Excel (Cell Mode)
* Word
* PDF
* CSV

{% highlight html %}

<div>
    <button id="ExportBtn">Export</button>
</div>

{% endhighlight %}

{% highlight js %}

$(function () {
     $("#PivotGrid").ejPivotGrid({ 
           url: "../wcf/OLAPService.svc"
     });
     $("#ExportBtn").ejButton({
           roundedCorner: true,
           size: "small",
           click: "exportBtnClick"
     });
});
function exportBtnClick(args) {
    var gridObj = $('#PivotGrid').data("ejPivotGrid");
    gridObj.exportPivotGrid(ej.PivotGrid.ExportOptions.Excel);
}

{% endhighlight %}

Export type which is to be mentioned in the parameter takes any one of the enumerated values such as Excel, Word, PDF and CSV.

The following service method needs to be added in-order to perform exporting in PivotGrid.

{% highlight c# %}

public void Export(System.IO.Stream stream)
{
    System.IO.StreamReader sReader = new System.IO.StreamReader(stream);
    string args = System.Web.HttpContext.Current.Server.UrlDecode(sReader.ReadToEnd());
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    string fileName = "PivotGrid";
    htmlHelper.ExportPivotGrid(DataManager, args, fileName,
    System.Web.HttpContext.Current.Response);
}

{% endhighlight %}

![]("/js/PivotGrid/Export_images/Export_img1.png" Caption="Exported PivotGrid in Excel")

![]("/js/PivotGrid/Export_images/Export_img2.png" Caption="Exported PivotGrid in Word")

![]("/js/PivotGrid/Export_images/Export_img3.png" Caption="Exported PivotGrid in PDF")

![]("/js/PivotGrid/Export_images/Export_img4.png" Caption="Exported PivotGrid in CSV")


