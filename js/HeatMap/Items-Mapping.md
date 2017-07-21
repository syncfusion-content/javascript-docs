---
layout: post
title: Data source given to HeatMap is configured using ItemsMapping
description: How to populate data for heatmap?
platform: JS
control: HeatMap
documentation: ug
api: /api/js/ejheatmap
---

#Items Mapping

External data source can be mapped with HeatMap using `itemsMapping` property. It supports 2 kind of data source.

* In `TableMapping` rows represents an objects in collection, columns represents numerical properties of that object.
* In `CellMapping` each cell represent an object in collection, this collection is grouped based on specific property to form as rows and columns.

Let us see the difference between two types of mapping. Following table represents two different data structure to represent the same HeatMap.

<table>
    <tr>
        <th>CellMapping</th>
        <th>TableMapping</th>
    </tr>
    <tr>
        <td>
            {% highlight js %}
                var itemSource = [
                    { Year: "2010", ProductName: "Veggie-spread", Value: 64 },
                    { Year: "2010", ProductName: "Tofu", Value: 26 },
                    { Year: "2010", ProductName: "Alice Mutton", Value: 47 },
                    { Year: "2010", ProductName: "Donut", Value: 67 },

                    { Year: "2011", ProductName: "Veggie-spread", Value: 56 },
                    { Year: "2011", ProductName: "Tofu", Value: 93 },
                    { Year: "2011", ProductName: "Alice Mutton", Value: 67 },
                    { Year: "2011", ProductName: "Donut", Value: 36 },

                    { Year: "2012", ProductName: "Veggie-spread", Value: 15 },
                    { Year: "2012", ProductName: "Tofu", Value: 34 },
                    { Year: "2012", ProductName: "Alice Mutton", Value: 12 },
                    { Year: "2012", ProductName: "Donut", Value: 39 },

                    { Year: "2013", ProductName: "Veggie-spread", Value: 24 },
                    { Year: "2013", ProductName: "Tofu", Value: 73 },
                    { Year: "2013", ProductName: "Alice Mutton", Value: 56 },
                    { Year: "2013", ProductName: "Donut", Value: 10 }
                ];
            {% endhighlight %}
        </td>
        <td>
            {% highlight js %}
    
                var itemsSource = [
                    { ProductName: "Veggie-spread", Y2010: 10, Y2011: 15, Y2012: 56, Y2013: 75 },
                    { ProductName: "Tofu", Y2010: 56, Y2011: 34, Y2012: 93, Y2013: 26 },
                    { ProductName: "Alice Mutton", Y2010: 73, Y2011: 12, Y2012: 67, Y2013: 47 },
                    { ProductName: "Donut", Y2010: 24, Y2011: 39, Y2012: 36, Y2013: 67 }
                ];
        
            {% endhighlight %}
        </td>
    </tr>
    <tr>
        <td>
            Here, a single `ProductInfo` object represent a value for a particular product in a particular year
        </td>
        <td>
            Here, a single `ProductInfo` object represents value for a particular product from year 2010 to 2015.	
        </td>
    </tr>
    <tr>
        <td>
            {% highlight js %}
            
                $("#heatmap").ejHeatMap({
                    itemsMapping: {
                        column: { "propertyName": "Year", "displayName": "Product Name" },
                        row: { "propertyName": "ProductName", "displayName": "ProductName", },
                        value: { "propertyName": "Value" },
                        headerMapping: { "propertyName": "ProductName", "displayName": "ProductName", columnStyle: { width: 140 } },
                        columnMapping: [
                            { "propertyName": "2010", "displayName": "Y2010", columnStyle: { width: 100 } },
                            { "propertyName": "2011", "displayName": "Y2011", columnStyle: { width: 100 } },
                            { "propertyName": "2012", "displayName": "Y2012", columnStyle: { width: 100 } },
                            { "propertyName": "2013", "displayName": "Y2013", columnStyle: { width: 100 } }
                        ]
                    }
                });
            
			{% endhighlight %}
        </td>
        <td>
            {% highlight js %}
    
                $("#heatmap").ejHeatMap({
                    colorMappingCollection: colorMappingCollection,
                    isResponsive: true,
                    width: "540",
                    itemsMapping: {
                        headerMapping: { "propertyName": "ProductName", "displayName": "Product Name", columnStyle: { width: 140 } },
                        columnMapping: [
                            { "propertyName": "Y2010", "displayName": "Y2010", columnStyle: { width: 100 } },
                            { "propertyName": "Y2011", "displayName": "Y2011", columnStyle: { width: 100 } },
                            { "propertyName": "Y2012", "displayName": "Y2012", columnStyle: { width: 100 } },
                            { "propertyName": "Y2013", "displayName": "Y2013", columnStyle: { width: 100 } }
                        ]
                    }
                });
                
            {% endhighlight %}
        </td>
    </tr>
    <tr>
        <td>
            ![](Items-Mapping_images/ItemsMapping_img1.png)
        </td>
        <td>
            ![](Items-Mapping_images/ItemsMapping_img1.png)
        </td>
    </tr>
</table>