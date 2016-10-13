---
layout: post
title: Export
description: export
platform: js
control: PivotClient
documentation: ug
---

# Exporting

PivotChart and PivotGrid in the PivotClient widget can be exported to Excel, Word and PDF documents by clicking the respective toolbar icons.

![](Export_images/exporting-icons.png) 

Exporting feature provides an option that allows you to export either PivotChart or PivotGrid or both with the use of the property [`clientExportMode`](/js/api/ejpivotclient#enum:clientexportmode).

The property [`clientExportMode`](/js/api/ejpivotclient#enum:clientexportmode) takes any one of the following value:

* **ChartAndGrid** – Exports both PivotChart and PivotGrid controls. This is the default mode.
* **ChartOnly** – Exports PivotChart control alone.
* **GridOnly** – Exports PivotGrid control alone.

## JSON Export

I> By default, exporting is done with the use of JSON Records maintained in client-side for both client and server modes.

In order to perform exporting with the use of a custom service method, the service containing the exporting method is hosted and its link is given in url as shown below.  Without giving any value to the 'url' property it takes our default exporting service link.

{% highlight javascript %}

        $("#PivotClient1").ejPivotClient({
            //...
            beforeExport:"Export",
            clientExportMode: ej.PivotClient.ClientExportMode.ChartAndGrid
        });
        
        function Export(args) {
            args.url = "http://js.syncfusion.com/demos/ejservices/api/JSPivotClientExport/ExportPivotClient";//Exporting url can be modified here
        }
{% endhighlight %}

### Customize the export document name

The document name could be customized. Following code sample illustrates the same.

{% highlight javascript %}

        $("#PivotClient1").ejPivotClient({
            //...
            beforeExport:"Export",
            clientExportMode: ej.PivotClient.ClientExportMode.ChartAndGrid
        });
        
        function Export(args) {
            args.url = "http://js.syncfusion.com/demos/ejservices/api/JSPivotClientExport/ExportPivotClient";
            args.fileName="File name is customized here";
        }
{% endhighlight %}

## PivotEngine Export

I> This feature is applicable only at server mode operation.

In order to perform exporting with the use of PivotEngine available in server-side, the 'url' property obtained in the “beforeExport” event is set to empty as shown below.

{% highlight javascript %}

        $("#PivotClient1").ejPivotClient({
            url: "/OlapService",
            beforeExport:"Export"
        });
        
        function Export(args) {
            args.url = "";
        }
        
 {% endhighlight %}

For WebAPI controller, the below method needs to be added to perform exporting with PivotEngine.

{% highlight c# %}

    [System.Web.Http.ActionName("Export")]
    [System.Web.Http.HttpPost]
    public void Export() {
        string args = HttpContext.Current.Request.Form.GetValues(0)[0];
        OlapDataManager DataManager = new OlapDataManager(connectionString);
        string fileName = "Sample";
        olapClientHelper.ExportOlapClient(DataManager, args, fileName, System.Web.HttpContext.Current.Response);
    }

{% endhighlight %}

For WCF service, the below service method needs to be added to perform exporting with PivotEngine.

{% highlight c# %}

    public void Export(Stream stream) {
        System.IO.StreamReader sReader = new System.IO.StreamReader(stream);
        string args = System.Web.HttpContext.Current.Server.UrlDecode(sReader.ReadToEnd());
        OlapDataManager DataManager = new OlapDataManager(connectionString);
        string fileName = "OlapClient";
        olapClientHelper.ExportOlapClient(DataManager, args, fileName,
            System.Web.HttpContext.Current.Response);
    }

{% endhighlight %}

The below screenshot shows the PivotGrid and PivotChart controls exported to Excel document.

![](Export_images/excel-export.png)

The below screenshot shows the PivotGrid and PivotChart controls exported to Word document.

![](Export_images/Word-Export.png)

The below screenshot shows the PivotGrid and PivotChart controls exported to PDF document.

![](Export_images/Pdf-Export.png)

### Customize the export document name

The document name could be customized inside the method in WebAPI Controller. Following code sample illustrates the same.

{% highlight c# %}

    [System.Web.Http.ActionName("Export")]
    [System.Web.Http.HttpPost]
    public void Export() {
        string args = HttpContext.Current.Request.Form.GetValues(0)[0];
        OlapDataManager DataManager = new OlapDataManager(connectionString);
        string fileName = " File name is customized here ";
        olapClientHelper.ExportOlapClient(DataManager, args, fileName, System.Web.HttpContext.Current.Response);
    }

{% endhighlight %}

For customizing name in WCF Service, below code snippet is used.

{% highlight c# %}

    public void Export(Stream stream) {
        System.IO.StreamReader sReader = new System.IO.StreamReader(stream);
        string args = System.Web.HttpContext.Current.Server.UrlDecode(sReader.ReadToEnd()).Remove(0, 5);
        OlapDataManager DataManager = new OlapDataManager(connectionString);
        string fileName = " File name is customized here ";
        olapClientHelper.ExportOlapClient(DataManager, args, fileName, System.Web.HttpContext.Current.Response);
    }

{% endhighlight %}



