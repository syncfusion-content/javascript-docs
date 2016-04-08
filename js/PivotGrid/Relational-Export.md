---
layout: post
title: Export
description: export
platform: js
control: PivotGrid
documentation: ug
---

# Exporting

The following table lists the exported file format for both Client and Server Mode of Relational datasource.

<table>
<tr>
<th>
Mode
</th>
<th>
File Formats
</th>
</tr>
<tr>
<td>
Client Mode
</td>
<td>
Excel
</td>
</tr>
<tr>
<td>
Server Mode
</td>
<td>
Excel, Word and PDF
</td>
</tr>
</table>

The PivotGrid control can be exported by invoking **"exportPivotGrid"** method, with an appropriate export option as parameter.

## Client Mode

For client side, Relational datasource contents can be exported only to Excel. The document can be saved from the browser to the local disk drive for later use.

To achieve Excel export, we need to add the following dependency library into the application.

* Syncfusion.EJ.Export

{% highlight js %}

<html>
//...

<body>
    //...
    <div id="PivotGrid1" style="min-height: 275px; min-width: 525px; height: 460px; width: 720px"></div>
    <button id="btnExport">Export</button>
    <script type="text/javascript">
        $(function() {
            $("#PivotGrid1").ejPivotGrid({
                dataSource: {
                    data: pivot_dataset,
                    rows: [{
                        fieldName: "Country",
                        fieldCaption: "Country"
                    }],
                    columns: [

                        {
                            fieldName: "Product",
                            fieldCaption: "Product"
                        }
                    ],
                    values: [{
                        fieldName: "Amount",
                        fieldCaption: "Amount"
                    }]
                }
            });
            $("#btnExport").ejButton({
                click: "btnExportClick",
                contentType: "textandimage",
                prefixIcon: "e-excel-export"
            });
        });

        function btnExportClick(args) {
            var gridObj = $('#PivotGrid1').data("ejPivotGrid");
            gridObj.exportPivotGrid("http://js.syncfusion.com/ExportingServices/api/JSPivotGridExport/Export"); 
        }
    </script>
</body>

</html>

{% endhighlight %}

![](Export_images/Exportingpure.png)


## Server Mode

{% highlight html %}

<html>
    //...
    <body>
       //...
       <div id="PivotGrid1" style="min-height: 275px; min-width: 525px; height: 460px; width: 720px"></div>
       <button id="exportBtn">Export</button>
       <script type="text/javascript">
           $(function () {
               $("#PivotGrid1").ejPivotGrid({
                 url: "../RelationalService",
               });
               $("#ExportBtn").ejButton({
                 click: "exportBtnClick"
               });
           });
           function exportBtnClick(args) {
             var gridObj = $('#PivotGrid1').data("ejPivotGrid");
             //Provide an appropriate export option as parameter.
             gridObj.exportPivotGrid(ej.PivotGrid.ExportOptions.Excel);
           }
                </script>
    </body>
</html>                                            

{% endhighlight %}

For WebAPI controller, the below method needs to be added to perform exporting.

{% highlight c# %}

public class JSPivotGridExportController : ApiController
{
PivotGridExport pGrid = new PivotGridExport();
[System.Web.Http.ActionName("Export")]
[System.Web.Http.HttpPost]
public void Export()
{
string args = HttpContext.Current.Request.Form.GetValues(0)[0];
string fileName = "Sample";
pGrid.ExportToExcel(fileName, args, HttpContext.Current.Response);
}
}

{% endhighlight %}

### Excel Export
User can export contents of the PivotGrid to Excel document for future archival, references and analysis purposes. To achieve Excel export, we need to add the following dependency libraries into the application.

* Syncfusion.Compression.Base
* Syncfusion.XlsIO.Base

For Excel export, **"ej.PivotGrid.ExportOptions.Excel"** enumeration value is sent as the parameter.

{% highlight js %}

function exportBtnClick(args) {
   var gridObj = $('#PivotGrid1').data("ejPivotGrid");
   gridObj.exportPivotGrid(ej.PivotGrid.ExportOptions.Excel);
}

{% endhighlight %}  

![](Export_images/Sampleexcel.png)

### Word Export
User can export contents of the PivotGrid to Word document for future archival, references and analysis purposes. To achieve Word export, we need to add the following dependency libraries into the application.

* Syncfusion.Compression.Base
* Syncfusion.DocIo.Base

For Word export, **"ej.PivotGrid.ExportOptions.Word"** enumeration value is sent as the parameter.

{% highlight js %}

function exportBtnClick(args) {
   var gridObj = $('#PivotGrid1').data("ejPivotGrid");
   gridObj.exportPivotGrid(ej.PivotGrid.ExportOptions.Word);
}

{% endhighlight %}

![](Export_images/Sampleword.png)

### PDF Export  
User can export contents of the PivotGrid to PDF document for future archival, references and analysis purposes. To achieve PDF export, we need to add the following dependency libraries into the application.

* Syncfusion.Compression.Base
* Syncfusion.Pdf.Base

For PDF export, **"ej.PivotGrid.ExportOptions.PDF"** enumeration value is sent as the parameter.

{% highlight js %}

function exportBtnClick(args) {
   var gridObj = $('#PivotGrid1').data("ejPivotGrid");
   gridObj.exportPivotGrid(ej.PivotGrid.ExportOptions.PDF);
}

{% endhighlight %} 

![](Export_images/Samplepdf.png)


### Customize the export document name

The document name could be customized inside the method in WebAPI Controller. Following code sample illustrates the same.

{% highlight c# %}

[System.Web.Http.ActionName("Export")]
[System.Web.Http.HttpPost]
public void Export() {
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    string fileName = " File name is customized here ";
    htmlHelper.ExportPivotGrid(DataManager, args, fileName, System.Web.HttpContext.Current.Response);
}

{% endhighlight %}

For customizing name in WCF Service, below code snippet is used.

{% highlight c# %}

public void Export(System.IO.Stream stream) {
    System.IO.StreamReader sReader = new System.IO.StreamReader(stream);
    string args = System.Web.HttpContext.Current.Server.UrlDecode(sReader.ReadToEnd()).Remove(0, 5);;
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    string fileName = " File name is customized here ";
    htmlHelper.ExportPivotGrid(DataManager, args, fileName, System.Web.HttpContext.Current.Response);
}

{% endhighlight %}


