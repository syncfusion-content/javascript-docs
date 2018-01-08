---
layout: post
title: Data-Binding
description: data binding
platform: js
control: BulletGraph	
documentation: ug
api: /api/js/ejbulletgraph
---

# Data Binding

**Bullet Graph** supports binding JSON data from a remote server or data created in client-side. You can use the [`fields`](../api/ejbulletgraph#members:quantitativescalesettings-fields) property to customize the data bound with **Bullet Graph**.

## Local Data

Data available in client-side (local data) can be bound with **Bullet Graph** using [`fields`](../api/ejbulletgraph#members:quantitativescalesettings-fields) property. This property provides option to specify data source, fields representing progress measure bar value, comparative measure value, category value and [`tableName`](../api/ejbulletgraph#members:quantitativescalesettings-fields-tablename).

{% highlight javascript %}



var localData = [
               {
                   value: 9.5, comparativeMeasureValue: 7.5,
                   category: 2001
               },
               {
                   value: 9.5, comparativeMeasureValue: 5,
                   category: 2002
               }]

$("#BulletGraph1").ejBulletGraph({

                    qualitativeRangeSize: 60,
                    quantitativeScaleSettings: {
                        location: { x:50, y:20 },
                    },
                    height: 120,
                    fields: {
                        dataSource: localData, category: "category",
                        featureMeasures: "value",
                        comparativeMeasure: "comparativeMeasureValue"
                    }

                });


{% endhighlight %}



The following screenshot displays **Bullet Graph** with local data generated using JavaScript

![](/js/BulletGraph/Data-Binding_images/Data-Binding_img1.png) 

## Remote Data

**Bullet Graph** provides option to bind data from a remote server using **ejDataManager** as data source in [`fields`](../api/ejbulletgraph#members:quantitativescalesettings-fields) property. A query object should also be passed to [`query`][`fields`](../api/ejbulletgraph#members:quantitativescalesettings-fields-query) property when using data manager as data source.

{% highlight javascript %}



               //Creating data manager instance
                var dataManger = new ej.DataManager({
                    url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
                });

                // Query creation
                var query = ej.Query().from("Order_Details").take(3).where("UnitPrice", ej.FilterOperators.greaterThan, 18, false)
                    .where("UnitPrice", ej.FilterOperators.lessThanOrEqual, 40, false)
                    .where("Quantity", ej.FilterOperators.greaterThan, 5, false)
                    .where("Quantity", ej.FilterOperators.lessThanOrEqual, 45, false);

                $("#BulletGraph1").ejBulletGraph({                                        

                    fields: {
                        dataSource: dataManger,
                        query: query,
                        category: "ProductID",
                        featureMeasures: "UnitPrice",
                        comparativeMeasure: "Quantity"
                    },

                    qualitativeRanges: [{ rangeEnd: 25 }, { rangeEnd: 37 }, { rangeEnd: 45 }],

                    qualitativeRangeSize: 60,
                    quantitativeScaleSettings: {
                        location: { x: 50, y: 20 },
                        minimum: 5,
                        maximum: 45,
                        interval: 10,
                    },

                });


{% endhighlight %}



The following screenshot displays a Bullet Graph bounded with data from a remote server

![](/js/BulletGraph/Data-Binding_images/Data-Binding_img2.png) 

