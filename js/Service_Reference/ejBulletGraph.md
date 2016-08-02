---
layout: post
title: Service reference for ejBulletGraph widget
description: What are the services used in Essential JavaScript Bullet Graph widget.
documentation: api
platform: js
keywords: ejBulletGraph, Services, Essential JS Bullet Graph, Bullet Graph, Northwind Service
metaname: 
metacontent:
control: ejBulletGraph
---

#ejBulletGraph
<ts root="datavisualization" />

Data from a remote server can be bound to ejBulletGraph using ejDataManager widget.

##Northwnd Service
{:#members:chart-northwnd-service}

### Description

To retrieve ten records from *Order_Details* table in *Northwnd service*.

### URL
[http://mvc.syncfusion.com/Services/Northwnd.svc/](http://mvc.syncfusion.com/Services/Northwnd.svc/)

### Parameter
<table>
<tr>
<td>$top</td><td>10</td>
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
                    'id': 'http://mvc.syncfusion.com/Services/Northwnd.svc/Order_Details(OrderID=10249,ProductID=14)',
                    'uri': 'http://mvc.syncfusion.com/Services/Northwnd.svc/Order_Details(OrderID=10249,ProductID=14)',
                    'type': 'NORTHWNDModel.Order_Detail'
                },
                'Order': {
                    '_deferred': {
                        'uri': 'http://mvc.syncfusion.com/Services/Northwnd.svc/Order_Details(OrderID=10249,ProductID=14)/Order'
                    }
                },
                'Product': {
                    '_deferred': {
                        'uri': 'http://mvc.syncfusion.com/Services/Northwnd.svc/Order_Details(OrderID=10249,ProductID=14)/Product'
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
                        'OrderID': 10249,
                        'ProductID': 14,
                        'UnitPrice': '18.6000',
                        'Quantity': 9,
                        'Discount':0
                    },
                },
            },

            //... 9 more similar records
	    ]
	}

{% endhighlight %}