---
layout: post
title: Export
description: export
platform: js
control: PivotGrid
documentation: ug
---

# Exporting

The PivotGrid control can be exported to the following file formats.

* Excel
* Word
* PDF
* CSV

The PivotGrid control can be exported by invoking **"exportPivotGrid"** method, with an appropriate export option as parameter.

{% highlight html %}

<html>
    //...
    <body>
       //...
       <div id="PivotGrid1" style="min-height: 275px; min-width: 525px; height: 460px; width: 720px"></div>
       <button id="btnExport">Export</button>
       <script type="text/javascript">
           $(function () {
               $("#PivotGrid1").ejPivotGrid({
                  ....
               });
               $("#btnExport").ejButton({
                 click: "exportBtnClick"
               });
           });
           function exportBtnClick(args) {
             var pGridObj = $('#PivotGrid1').data("ejPivotGrid")
             
            //If you render PivotGrid in Client Mode, set the export option like below.
            pGridObj.exportPivotGrid("http://js.syncfusion.com/demos/ejservices/api/JSPivotGridExport/ExcelExport","fileName");
            
            //If you render PivotGrid in Server Mode, set the export option like below.
            pGridObj.exportPivotGrid(ej.PivotGrid.ExportOptions.Excel);
           }
    </script>
    </body>
</html>                                            

{% endhighlight %}

When PivotGrid is rendered in Server Mode, a service method needs to be added in WCF/WebAPI for server side operations.

For WebAPI controller, the below method needs to be added.

{% highlight c# %}

[System.Web.Http.ActionName("Export")]
[System.Web.Http.HttpPost]
public void Export()
{
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    Dictionary<string, string> gridParams = serializer.Deserialize<Dictionary<string, string>>(args);
    htmlHelper.PopulateData(gridParams["currentReport"]);
    string fileName = "Sample";
    htmlHelper.ExportPivotGrid(ProductSales.GetSalesData(), args, fileName, HttpContext.Current.Response);
}

{% endhighlight %}

For WCF service, the below method needs to be added.

{% highlight c# %}

public void Export(System.IO.Stream stream)
{
    System.IO.StreamReader sReader = new System.IO.StreamReader(stream);
    string args = System.Web.HttpContext.Current.Server.UrlDecode(sReader.ReadToEnd()).Remove(0, 5);
    Dictionary<string, string> gridParams = serializer.Deserialize<Dictionary<string, string>>(args);
    htmlHelper.PopulateData(gridParams["currentReport"]);
    string fileName = "Sample";
    htmlHelper.ExportPivotGrid(ProductSales.GetSalesData(), args, fileName, System.Web.HttpContext.Current.Response);
}

{% endhighlight %}

##Excel Export

User can export contents of the PivotGrid to Excel document for future archival, references and analysis purposes.

###Client Mode

To achieve Excel export, service URL and file name is sent as the parameter.

{% highlight javascript %}

function exportBtnClick(args)
{
    var pGridObj = $('#PivotGrid1').data("ejPivotGrid ");
    pGridObj.exportPivotGrid("http://js.syncfusion.com/demos/ejservices/api/JSPivotGridExport/ExcelExport","fileName");
}

{% endhighlight %}  

###Server Mode

To achieve Excel export, we need to add the following dependency libraries into the application.

* Syncfusion.Compression.Base
* Syncfusion.XlsIO.Base

For Excel export, **“ej.PivotGrid.ExportOptions.Excel”** enumeration value is sent as the parameter.

{% highlight javascript %}

function exportBtnClick(args)
{
    var pGridObj = $('#PivotGrid1').data("ejPivotGrid");
    //Setting export option as Excel in the exportPivotGrid method for ServerMode
    pGridObj.exportPivotGrid(ej.PivotGrid.ExportOptions.Excel);
}

{% endhighlight %}  

![](Export_images/ExportPivotExcel.png)

##Word Export

User can export contents of the PivotGrid to Word document for future archival, references and analysis purposes.

###Client Mode

To achieve Word export, service URL and file name is sent as the parameter.

{% highlight javascript %}

function exportBtnClick(args)
{
    var pGridObj = $('#PivotGrid1').data("ejPivotGrid ");
    pGridObj.exportPivotGrid("http://js.syncfusion.com/demos/ejservices/api/JSPivotGridExport/WordExport","fileName");
}

{% endhighlight %}  

###Server Mode

 To achieve Word export, we need to add the following dependency libraries into the application.

* Syncfusion.Compression.Base
* Syncfusion.DocIO.Base

For Word export, **“ej.PivotGrid.ExportOptions.Word”** enumeration value is sent as the parameter.

{% highlight javascript %}

function exportBtnClick(args)
{
    var pGridObj = $('#PivotGrid1').data("ejPivotGrid");
    //Setting export option as Word in the exportPivotGrid method
    pGridObj.exportPivotGrid(ej.PivotGrid.ExportOptions.Word);
}

{% endhighlight %}

![](Export_images/ExportPivotWord.png)

##PDF Export

User can export contents of the PivotGrid to PDF document for future archival, references and analysis purposes.

###Client Mode

To achieve PDF export, service URL and file name is sent as the parameter.

{% highlight javascript %}

function exportBtnClick(args)
{
    var pGridObj = $('#PivotGrid1').data("ejPivotGrid ");
    pGridObj.exportPivotGrid("http://js.syncfusion.com/demos/ejservices/api/JSPivotGridExport/PDFExport","fileName");
}

{% endhighlight %}  

###Server Mode

To achieve PDF export, we need to add the following dependency libraries into the application.

* Syncfusion.Compression.Base
* Syncfusion.Pdf.Base

For PDF export, **“ej.PivotGrid.ExportOptions.PDF”** enumeration value is sent as the parameter.

{% highlight javascript %}

function exportBtnClick(args)
{
    var pGridObj = $('#PivotGrid1').data("ejPivotGrid ");
    //Setting export option as PDF in the exportPivotGrid method
    pGridObj.exportPivotGrid(ej.PivotGrid.ExportOptions.PDF);
}

{% endhighlight %} 

![](Export_images/ExportPivotPDF.png)

##CSV Export

User can export contents of the PivotGrid to CSV document for future archival, references and analysis purposes.

###Client Mode

To achieve CSV export, service URL and file name is sent as the parameter.

{% highlight javascript %}

function exportBtnClick(args)
{
    var pGridObj = $('#PivotGrid1').data("ejPivotGrid ");
    pGridObj.exportPivotGrid("http://js.syncfusion.com/demos/ejservices/api/JSPivotGridExport/CSVExport","fileName");
}

{% endhighlight %}  

###Server Mode

For CSV export, **“ej.PivotGrid.ExportOptions.CSV"** enumeration value is sent as the parameter.

{% highlight javascript %}

function exportBtnClick(args)
{
    var pGridObj = $('#PivotGrid1').data("ejPivotGrid ");
    //Setting export option as CSV in the exportPivotGrid method
    pGridObj.exportPivotGrid(ej.PivotGrid.ExportOptions.CSV);
}

{% endhighlight %} 

![](Export_images/ExportPivotCSV.png)

### Customize the export document name

###Client Mode

For customizing file name, we need to send file name as parameter to the **exportPivotGrid**  method along with service URL.

{% highlight javascript %}

function exportBtnClick(args)
{
    var pGridObj = $('#PivotGrid1').data("ejPivotGrid ");
    pGridObj.exportPivotGrid("http://js.syncfusion.com/demos/ejservices/api/JSPivotGridExport/ExcelExport","fileName");
}
    
{% endhighlight %}
 
###Server Mode

For customizing name in WebAPI controller, below code sample is used.

{% highlight c# %}

[System.Web.Http.ActionName("Export")]
[System.Web.Http.HttpPost]
public void Export()
{
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    Dictionary<string, string> gridParams = serializer.Deserialize<Dictionary<string, string>>(args);
    htmlHelper.PopulateData(gridParams["currentReport"]);
    string fileName = " File name is customized here ";
    htmlHelper.ExportPivotGrid(ProductSales.GetSalesData(), args, fileName, HttpContext.Current.Response);
}

{% endhighlight %}

For customizing name in WCF Service, below code sample is used.

{% highlight c# %}

public void Export(System.IO.Stream stream)
{
    System.IO.StreamReader sReader = new System.IO.StreamReader(stream);
    string args = System.Web.HttpContext.Current.Server.UrlDecode(sReader.ReadToEnd()).Remove(0, 5);
    Dictionary<string, string> gridParams = serializer.Deserialize<Dictionary<string, string>>(args);
    htmlHelper.PopulateData(gridParams["currentReport"]);
    string fileName = " File name is customized here ";
    htmlHelper.ExportPivotGrid(ProductSales.GetSalesData(), args, fileName, System.Web.HttpContext.Current.Response);
}

{% endhighlight %}


