---
layout: post
title: Export
description: export
platform: js
control: PivotClient
documentation: ug
---

# Exporting

Chart and Grid in the PivotClient widget can be exported to Excel, Word and PDF documents by clicking the respective toolbar icons.

![](Export_images/exporting-icons.png) 

Exporting feature provides an option that allows you to export either PivotChart or PivotGrid or both with the use of the property [`clientExportMode`](/api/js/ejpivotclient#enum:clientexportmode).

The property [`clientExportMode`](/api/js/ejpivotclient#enum:clientexportmode) takes any one of the following value:

* **ChartAndGrid** – Exports both PivotChart and PivotGrid controls. This is the default mode.
* **ChartOnly** – Exports PivotChart control alone.
* **GridOnly** – Exports PivotGrid control alone.

## JSON Export

I> By default JSON export mode will be applied for server and client mode.

In order to perform exporting with the use of a custom service method, the service containing the exporting method is hosted and its link is given in url as shown below.  Without giving any value to the 'url' property it takes our default exporting service link.

{% highlight javascript %}

        $("#PivotClient1").ejPivotClient({
            //...
            beforeExport:"Export",
            clientExportMode: ej.PivotClient.ClientExportMode.ChartAndGrid
        });
        
        function Export(args) {
            args.url = "http://js.syncfusion.com/demos/ejservices/api/JSPivotClientExport/ExportPivotClient";
        }

{% endhighlight %}

### Customize the export document name

The name of the document to be exported could be customized. Following code sample illustrates the same.

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
            url: "/RelationalClient",            
            beforeExport:"Export",
            clientExportMode: ej.PivotClient.ClientExportMode.ChartAndGrid
        });
        
        function Export(args) {
            args.url = "";
        }

 {% endhighlight %}


For WebAPI controller, the below method needs to be added to perform exporting with PivotEngine.

{% highlight c# %}

        [System.Web.Http.ActionName("Export")]
        [System.Web.Http.HttpPost]
        public void Export()
        {
            string args = HttpContext.Current.Request.Form.GetValues(0)[0];
            Dictionary<string, string> gridParams = serializer.Deserialize<Dictionary<string, string>>(args);
            pivotClient.PopulateData(gridParams["currentReport"]);
            string fileName = "Sample";
            pivotClient.ExportPivotClient(ProductSales.GetSalesData(), args, fileName, System.Web.HttpContext.Current.Response);
        }

{% endhighlight %}

For WCF service, the below service method needs to be added to perform exporting with PivotEngine.

{% highlight c# %}

       public void Export(System.IO.Stream stream)
       {
            System.IO.StreamReader sReader = new System.IO.StreamReader(stream);
            string args = System.Web.HttpContext.Current.Server.UrlDecode(sReader.ReadToEnd()).Remove(0, 5);
            Dictionary<string, string> gridParams = serializer.Deserialize<Dictionary<string, string>>(args);
            pivotClient.PopulateData(gridParams["currentReport"]);
            string fileName = "Sample";
            pivotClient.ExportPivotClient(ProductSales.GetSalesData(), args, fileName, System.Web.HttpContext.Current.Response);
       }

{% endhighlight %}

The below screenshot shows the PivotGrid and PivotChart controls exported to Excel document.

![](Export_images/relational-excel-export.png)

The below screenshot shows the PivotGrid and PivotChart controls exported to Word document.

![](Export_images/relational-word-Export.png)

The below screenshot shows the PivotGrid and PivotChart controls exported to PDF document.

![](Export_images/relational-Pdf-Export.png)

### Customize the export document name

The document name could be customized inside the method in WebAPI Controller. Following code sample illustrates the same.

{% highlight c# %}
  
        [System.Web.Http.ActionName("Export")]
        [System.Web.Http.HttpPost]
        public void Export()
        {
            string args = HttpContext.Current.Request.Form.GetValues(0)[0];
            Dictionary<string, string> gridParams = serializer.Deserialize<Dictionary<string, string>>(args);
            pivotClient.PopulateData(gridParams["currentReport"]);
            string fileName = " File name is customized here ";
            pivotClient.ExportPivotClient(ProductSales.GetSalesData(), args, fileName, System.Web.HttpContext.Current.Response);
        }

{% endhighlight %}

For customizing name in WCF Service, below code snippet is used.

{% highlight c# %}

       public void Export(System.IO.Stream stream)
       {
            System.IO.StreamReader sReader = new System.IO.StreamReader(stream);
            string args = System.Web.HttpContext.Current.Server.UrlDecode(sReader.ReadToEnd()).Remove(0, 5);
            Dictionary<string, string> gridParams = serializer.Deserialize<Dictionary<string, string>>(args);
            pivotClient.PopulateData(gridParams["currentReport"]);
            string fileName = " File name is customized here ";
            pivotClient.ExportPivotClient(ProductSales.GetSalesData(), args, fileName, System.Web.HttpContext.Current.Response);
       }
       
{% endhighlight %}



