---
layout: post
title: Export
description: export
platform: js
control: OlapChart
documentation: ug
---

#Exporting

The OlapChart control can be exported to the following file formats.

* Excel
* Word
* PDF
* CSV
* Image

The additional script files required for exporting OlapChart are mentioned below:

* rgbcolor.js 
* StackBlur.js 
* canvg.js

These files are referred under the <head> tag in HTML page. 

{% highlight html %}

<head>
    //...
    <script type="text/javascript" src="http://gabelerner.github.io/canvg/rgbcolor.js"></script>
    <script type="text/javascript" src="http://gabelerner.github.io/canvg/StackBlur.js"></script>
    <script type="text/javascript" src="http://gabelerner.github.io/canvg/canvg.js"></script>
</head>

{% endhighlight %}

The OlapChart control can be exported by invoking **“exportOlapChart”** method, with an appropriate export option as parameter.


{% highlight html %}

<html> 
    //...

<body> 
    //...
    <div id="OlapChart1" style="min-height: 275px; min-width: 525px; height: 460px; width: 720px"></div>
    <button id="exportBtn">Export</button>
    <script type="text/javascript">
        $(function()
        {
            $("#OlapChart1").ejOlapChart(
            {
                url: "../wcf/OlapChartService.svc"
                    //...
            });
            $("#exportBtn").ejButton(
            {
                click: "exportBtnClick"
            });
        });

        function exportBtnClick(args)
        {
            var chartObj = $('#OlapChart1').data("ejOlapChart");
            //Provide an appropriate export option as parameter.
            chartObj.exportOlapChart(ej.olap.OlapChart.ExportOptions.Excel);
        }
    </script>
</body>
</html>                                           

{% endhighlight %}

For WebAPI controller, the below method needs to be added to perform exporting.

{% highlight c# %}

[System.Web.Http.ActionName("Export")]
[System.Web.Http.HttpPost]
public void Export() {
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    string fileName = "Sample";
    htmlHelper.ExportOlapChart(DataManager, args, fileName, System.Web.HttpContext.Current.Response);
}

{% endhighlight %}

For WCF service, the below service method needs to be added to perform exporting.

{% highlight c# %}

public void Export(Stream stream) {
    System.IO.StreamReader sReader = new System.IO.StreamReader(stream);
    string args = System.Web.HttpContext.Current.Server.UrlDecode(sReader.ReadToEnd()).Remove(0, 5);
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    string fileName = "Sample";
    htmlHelper.ExportOlapChart(DataManager, args, fileName, System.Web.HttpContext.Current.Response);
}

{% endhighlight %}


##Excel Export
User can export contents of the OlapChart to Excel document for future archival, references and analysis purposes. To achieve Excel export, we need to add the following dependency libraries into the application.

* Syncfusion.Compression.Base
* Syncfusion.XlsIO.Base

For Excel export, **“ej.olap.OlapChart.ExportOptions.Excel”** enumeration value is sent as the parameter.

{% highlight javascript %}

function exportBtnClick(args)
{
    var chartObj = $('#OlapChart1').data("ejOlapChart ");
        //Setting export option as Excel in the exportOlapChart method
        chartObj.exportOlapChart(ej.olap.OlapChart.ExportOptions.Excel);
}

{% endhighlight %}  

![](Export_images/Export_img1.png)

##Word Export
User can export contents of the OlapChart to Word document for future archival, references and analysis purposes. To achieve Word export, we need to add the following dependency libraries into the application.

* Syncfusion.Compression.Base
* Syncfusion.DocIo.Base

For Word export, **“ej.olap.OlapChart.ExportOptions.Word”** enumeration value is sent as the parameter.

{% highlight javascript %}

function exportBtnClick(args)
{
    var chartObj = $('#OlapChart1').data("ejOlapChart ");
        //Setting export option as Word in the exportOlapChart method
        chartObj.exportOlapChart(ej.olap.OlapChart.ExportOptions.Word);
}

{% endhighlight %}

![](Export_images/Export_img2.png)

##CSV Export
User can export contents of the OlapChart to CSV document for future archival, references and analysis purposes.

For CSV export, **“ej.olap.OlapChart.ExportOptions.CSV”** enumeration value is sent as the parameter.

{% highlight javascript %}

function exportBtnClick(args)
{
    var chartObj = $('#OlapChart1').data("ejOlapChart ");
        //Setting export option as CSV in the exportOlapChart method
        chartObj.exportOlapChart(ej.olap.OlapChart.ExportOptions.CSV);
}

{% endhighlight %}

##PDF Export
User can export contents of the OlapChart to PDF document for future archival, references and analysis purposes. To achieve PDF export, we need to add the following dependency libraries into the application.

* Syncfusion.Compression.Base
* Syncfusion.Pdf.Base

For PDF export, **“ej.olap.OlapChart.ExportOptions.PDF”** enumeration value is sent as the parameter.

{% highlight javascript %}

function exportBtnClick(args)
{
    var chartObj = $('#OlapChart1').data("ejOlapChart ");
        //Setting export option as PDF in the exportOlapChart method
        chartObj.exportOlapChart(ej.olap.OlapChart.ExportOptions.PDF);
}

{% endhighlight %} 

![](Export_images/Export_img3.png)

##Image Export
User can export contents of the OlapChart to image format for future archival, references and analysis purposes. We can export OlapChart to the following image formats.

* PNG
* EMF
* JPG
* GIF
* BMP

For EMF export, **“ej.olap.OlapChart.ExportOptions.EMF”** enumeration value is sent as the parameter.

{% highlight javascript %}

function exportBtnClick(args)
{
    var chartObj = $('#OlapChart1').data("ejOlapChart ");
        //Setting export option as EMF in the exportOlapChart method
        chartObj.exportOlapChart(ej.olap.OlapChart.ExportOptions.EMF);
}

{% endhighlight %}  

![](Export_images/Export_img4.png)

##Customize the export document name

The document name could be customized inside the method in WebAPI Controller. Following code sample illustrates the same.

{% highlight c# %}

[System.Web.Http.ActionName("Export")]
[System.Web.Http.HttpPost]
public void Export() {
    string args = HttpContext.Current.Request.Form.GetValues(0)[0];
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    string fileName = "File name is customized here";
    htmlHelper.ExportOlapChart(DataManager, args, fileName, System.Web.HttpContext.Current.Response);
}

{% endhighlight %}

For customizing name in WCF Service, below code snippet is used.

{% highlight c# %}

public void Export(System.IO.Stream stream) {
    System.IO.StreamReader sReader = new System.IO.StreamReader(stream);
    string args = System.Web.HttpContext.Current.Server.UrlDecode(sReader.ReadToEnd()).Remove(0, 5);
    OlapDataManager DataManager = new OlapDataManager(connectionString);
    string fileName = " File name is customized here ";
    htmlHelper.ExportOlapChart(DataManager, args, fileName, System.Web.HttpContext.Current.Response);
}

{% endhighlight %}

