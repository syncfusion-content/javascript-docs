---
layout: post
title: export
description: export
platform: js
control: PivotGrid
documentation: ug
---

# Export

> ![](export_images\export_img1.jpeg)_**Note:This feature is applicable only for OLAP datasource.**_

The **PivotGrid** is exported from cell mode to a worksheet of an Excel Workbook. The Excel Workbook is saved from the browser to the local disk drive.

The following code example illustrates how to save the document to Excel via service.

**For PivotGrid**

{% highlight c# %}

**[C#]**
Public void ExportOptions(Stream stream)
{
PivotGrid pivotGridHelper = new PivotGrid();
OlapDataManager DataManager=new OlapDataManager(connectionString);
pivotGridHelper.ExportToExcel(DataManager,newStreamReader(stream).ReadToEnd(),"Sample.xls",HttpContext.Current.Response);
}


{% endhighlight %}





{% highlight js %}

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



{% include image.html url="\js\PivotGrid\concepts-and-features\export_images\export_img2.png" Caption="Exported Excel Worksheet"%}

