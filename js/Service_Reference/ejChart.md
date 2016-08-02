---
layout: post
title: Service reference for ejChart widget
description: What are the services used in Essential JavaScript Chart.
documentation: api
platform: js
keywords: ejChart, Services, Essential JS Chart, Chart, Northwind Service, Excel Exporting Service, Chart Exporting
metaname: 
metacontent:
control: ejChart
---

#ejChart
<ts root="datavisualization" />

Essential chart uses services to export Chart as a PDF, Word or Excel document. Data from a remote server can be bound to ejChart using ejDataManager widget.

##Northwnd Service
{:#members:chart-northwnd-service}

### Description

To retrieve first ten records from *Orders* table in *Northwnd service*.

### URL
[http://mvc.syncfusion.com/Services/Northwnd.svc/](http://mvc.syncfusion.com/Services/Northwnd.svc/)

### Parameter
<table>
<tr>
<td>$top</td><td>10</td>
<td>$filter</td><td>UnitPrice gt 18 and UnitPrice le 40 and Quantity gt 5 and Quantity le 45</td>
</tr>
</table>

### Request

{% highlight js %}
 
var dataManger = new ej.DataManager(
{
    url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
});

{% endhighlight %}

###Response

####Code: 200

####Content-Type: application/json;odata=verbose;charset=utf-8

####Response (JSON):

{% highlight js %}

	{
	    'd': [
            {
                '_metadata': {
                    'id': 'http://mvc.syncfusion.com/Services/Northwnd.svc/Orders(10248)',
                    'uri': 'http://mvc.syncfusion.com/Services/Northwnd.svc/Orders(10248)',
                    'type': 'http://mvc.syncfusion.com/Services/Northwnd.svc/Orders(10248)'
                },
                'Customer': {
                    '_deferred': {
                        'uri':'http://mvc.syncfusion.com/Services/Northwnd.svc/Orders(10248)/Customer'
                    }
                },
                'Employee': {
                    '_deferred': {
                        'uri': 'http://mvc.syncfusion.com/Services/Northwnd.svc/Orders(10248)/Employee'
                    }
                },
                'Order_Details': {
                    '_deferred': {
                        'uri': 'http://mvc.syncfusion.com/Services/Northwnd.svc/Orders(10248)/Order_Details'
                    },
                    'Shipper': {
                        '_deferred': {
                            'uri': 'http://mvc.syncfusion.com/Services/Northwnd.svc/Orders(10248)/Shipper'
                        },
                        'OrderID': 10248,
                        'CustomerID': 'VINET',
                        'EmployeeID': 1,
                        'OrderDate': '/Date(1423027800000)/',
                        'RequiredDate': '/Date(1424951652613)/',
                        'ShippedDate': '/Date(1424608518217)/',
                        'ShipVia': null,
                        'Freight': '6.0000',
                        'ShipName': 'SURINDER',
                        'ShipAddress': 'OLDTOWN',
                        'ShipCity': 'STOCKHOLM',
                        'ShipRegion': 'New Delhi HO',
                        'ShipPostalCode': '110001',
                        'ShipCountry':'SWEDEN'
                    },
                },
            },

            //... 9 more records
	    ]
	}
{% endhighlight %}

##Exporting service

### Description

To export Chart as PNG, JPG, SVG, PDF document, Excel document or Word document.

### URL
[http://js.syncfusion.com/ExportingServices/api/JSChartExport/ExportChart](http://js.syncfusion.com/ExportingServices/api/JSChartExport/ExportChart)

### Parameter
<table>
<tr>
<td>type</td><td>image</td>
<td>URL</td><td>http://js.syncfusion.com/ExportingServices/api/JSChartExport/ExportChart</td>
<td>exportMultipleChart</td><td>false</td>
</tr>
</table>

### Request

{% highlight js %}
 
var chart = $(".e-datavisualization-chart").ejChart("instance");
var exportSettings = chart.model.exportSettings;
exportSettings.fileName = "Chart";
exportSettings.angle = "90";
exportSettings.type = "png";
exportSettings.mode = 'server';
exportSettings.action = 'http://js.syncfusion.com/ExportingServices/api/JSChartExport/ExportChart';
data = chart.export();

{% endhighlight %}

###Response

####Code: 200

####Content-Type: application/octet-stream

####Response (PNG, JPG, SVG, PDF, Word or Excel):

Browser will prompt a dialog box to save the file (image or document).


