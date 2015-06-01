---
layout: post
title: Export
description: export
platform: js
control: PivotGrid
documentation: ug
---

# Export

_**Note: This feature is applicable only for OLAP datasource.**_

The **PivotGrid** is exported from cell mode to a worksheet of an Excel Workbook. The Excel Workbook is saved from the browser to the local disk drive.

The following code example illustrates how to save the document to Excel via service.

**For PivotGrid**

{% highlight c# %}

**[C#]**
public void ExportOptions(Stream stream)
{
PivotGrid pivotGridHelper = new PivotGrid();
OlapDataManager DataManager=new OlapDataManager(connectionString);
pivotGridHelper.ExportToExcel(DataManager, newStreamReader(stream).ReadToEnd(), "Sample.xls",HttpContext.Current.Response);
}


{% endhighlight %}





{% highlight javascript %}

**[JS]**
<button id="Button1">Export Grid</button>
<div id="PivotGrid1" style="height: 350px; width: 100%; overflow: auto"> </div> 
<script type="text/javascript">
 $(function () {
     $("#PivotGrid1").ejPivotGrid({ url: "../wcf/PivotGridService.svc"});

  $("#Button1").ejButton({size: "normal",roundedCorner: true,click: "btnClick"});
 });
  function btnClick(e) {
      pivotGridObj = $('#PivotGrid').data("ejPivotGrid");
      pivotGridObj.exportToExcel();
}
</script>



{% endhighlight %}



{% include image.html url="/js/PivotGrid/Concepts-and-Features/Export_images/Export_img1.png" Caption="Exported Excel Worksheet"%}

