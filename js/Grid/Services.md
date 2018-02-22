---
layout: post
title: Service reference for ejGrid widget
description: What are the services used in Essential JavaScript Grid.
documentation: api
platform: js
keywords: ejGrid, Services, Essential JS Grid, Grid, Northwind Service, Excel Exporting Service, Grid Exporting
metaname: 
metacontent:
control: ejGrid
api: /api/js/ejgrid
---

# ejGrid

Essential Grid is export as a PDF, Word or Excel document by using services . Data from a remote server can be bound to ejGrid using ejDataManager widget.

## Northwnd service
{:#members:grid-northwnd-service}

### Description

To retrieve the records from *Orders* table in *Northwnd service*.

### URL
[http://mvc.syncfusion.com/Services/Northwnd.svc/](http://mvc.syncfusion.com/Services/Northwnd.svc/)

### Parameter
<table>
<tr>
<td>$top</td><td>10</td>
<td>$filter</td><td>EmployeeID eq 5</td>
<td>$skip</td><td>2</td>
</tr>
</table>

### Request

{% highlight js %}
 
var dataManger = new ej.DataManager(
{
    url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
});

{% endhighlight %}

### Response

#### Code: 200

#### Content-Type: application/json;odata=verbose;charset=utf-8

#### Response (JSON):

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

## Exporting service

### Description

To export grid data as Excel, Word or PDF document.

### URL

[http://js.syncfusion.com/ExportingServices/api/JSGridExport/ExcelExport](http://js.syncfusion.com/ExportingServices/api/JSGridExport/ExcelExport)
[http://js.syncfusion.com/ExportingServices/api/JSGridExport/WordExport](http://js.syncfusion.com/ExportingServices/api/JSGridExport/WordExport)
[http://js.syncfusion.com/ExportingServices/api/JSGridExport/PdfExport](http://js.syncfusion.com/ExportingServices/api/JSGridExport/PdfExport)


### Parameter
<table>
   <th>type</th>
   <th>URL </th>
   <th>multipleExport</th>
   <tr>
      <td>Excel</td>
      <td>http://js.syncfusion.com/ExportingServices/api/JSGridExport/ExcelExport</td>
      <td>false</td>
   </tr>
   <tr>
      <td>Word</td>
      <td>http://js.syncfusion.com/ExportingServices/api/JSGridExport/WordExport</td>
      <td>false</td>
   </tr>
   <tr>
      <td>PDF</td>
      <td>http://js.syncfusion.com/ExportingServices/api/JSGridExport/PdfExport</td>
      <td>false</td>
   </tr>
</table>

### Request

#### Essential grid exporting in JavaScript platform
{% highlight js %}
$(function() {
    $("#Grid").ejGrid({
        dataSource: window.gridData,
        allowPaging: true,
        toolbarSettings: {
            showToolbar: true,
            toolbarItems: [ej.Grid.ToolBarItems.ExcelExport, ej.Grid.ToolBarItems.WordExport, ej.Grid.ToolBarItems.PdfExport]
        },
        toolbarClick: function(e) {
            this.exportGrid = this["export"];
            if (e.itemName == "Excel Export") {
                this.exportGrid('http://js.syncfusion.com/ExportingServices/api/JSGridExport/ExcelExport')
                e.cancel = true;
            } else if (e.itemName == "Word Export") {
                this.exportGrid('http://js.syncfusion.com/ExportingServices/api/JSGridExport/WordExport')
                e.cancel = true;
            } else if (e.itemName == "PDF Export") {
                this.exportGrid('http://js.syncfusion.com/ExportingServices/api/JSGridExport/PdfExport')
                e.cancel = true;
            }
        },
    })

})
{% endhighlight %}

#### Essential grid exporting in C# 

{% highlight c# %}
public void ExportToExcel(string GridModel)
        {
            ExcelExport exp = new ExcelExport();
            var DataSource = new NorthwindDataContext().OrdersViews.Take(100).ToList();
            GridProperties obj = ConvertGridObject(GridModel);
            exp.Export(obj, DataSource, "Export.xlsx", ExcelVersion.Excel2010, false, false, "flat-saffron");
        }
        public void ExportToWord(string GridModel)
        {
            WordExport exp = new WordExport();
            var DataSource = new NorthwindDataContext().OrdersViews.Take(100).ToList();
            GridProperties obj = ConvertGridObject(GridModel);
            exp.Export(obj, DataSource, "Export.docx", false, false, "flat-saffron");
        }
        public void ExportToPdf(string GridModel)
        {
            PdfExport exp = new PdfExport();
            var DataSource = new NorthwindDataContext().OrdersViews.Take(100).ToList();
            GridProperties obj = ConvertGridObject(GridModel);
            exp.Export(obj, DataSource, "Export.pdf", false, false, "flat-saffron");
        }
{% endhighlight %}

### Response

#### Code: 200

#### Content-Type: application/octet-stream




