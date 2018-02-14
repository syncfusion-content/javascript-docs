---
layout: post
title: Data source given to HeatMap is configured using ItemsMapping
description: How to populate data for heatmap?
platform: JS
control: HeatMap
documentation: ug
api: /api/js/ejheatmap
---

# Items Mapping

External data source can be mapped with HeatMap using [itemsMapping](/api/js/ejheatmap#members:itemsmapping "itemsMapping") property. It supports 2 kind of data source.

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
 
* The [row](/api/js/ejheatmap#members:itemsmapping-row "row") [propertyName](/api/js/ejheatmap#members:itemsmapping-row-propertyname "propertyName") property is used to bind the row with specific field which is in datasource collection. The row [displayName](/api/js/ejheatmap#members:itemsmapping-row-displayname "displayName") property is used to specify your own name for row.

* The [column](/api/js/ejheatmap#members:itemsmapping-column "column") [propertyName](/api/js/ejheatmap#members:itemsmapping-column-propertyname "propertyName") property is used to bind the column with specific field which is in datasource collection. The column
 [displayName](/api/js/ejheatmap#members:itemsmapping-column-displayname "displayName") property is used to specify your own name for column.

* The [value](/api/js/ejheatmap#members:itemsmapping-value "value") [propertyName](/api/js/ejheatmap#members:itemsmapping-value-propertyname "propertyName") property is used to bind the heatmap column with specified data.
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

## Mapping

### HeaderMapping

* The [headerMapping](/api/js/ejheatmap#members:itemsmapping-headermapping "headerMapping") property allows you to bind the header column(first column) with specific field defined in user DataSource. 

* The headerMapping [propertyName](/api/js/ejheatmap#members:itemsmapping-headermapping-propertyname "propertyName") property is used to bind the specific field of datasource collection in it.

* The headerMapping [displayName](/api/js/ejheatmap#members:itemsmapping-headermapping-displayname "displayName") property allows you to set name for an header.

### ColumnMapping

* The [columnMapping](/api/js/ejheatmap#members:itemsmapping-columnmapping "columnMapping") property allows you to bind the columns with user defined data.

* The columnMapping [propertyName](/api/js/ejheatmap#members:itemsmapping-columnmapping-propertyname "propertyName") property is used to bind the heatmap columns with specified data.

* The columnMapping [displayName](/api/js/ejheatmap#members:itemsmapping-columnmapping-displayname "displayName") property is used to specify the column name.

## Appearance

* To Align the text of an individual heatmap column, [columnStyle](/api/js/ejheatmap#members:itemsmapping-columnstyle "columnStyle") use [textAlign](/api/js/ejheatmap#members:itemsmapping-columnstyle-textalign "textAlign") property and to align text for an entire heatmap column, use [defaultColumnStyle](/api/js/ejheatmap#members:defaultcolumnstyle "defaultColumnStyle"), [textAlign](/api/js/ejheatmap#members:defaultcolumnstyle-textalign "textAlign").

* The columnStyle [width](/api/js/ejheatmap#members:itemsmapping-columnstyle-width "width") property is used to define the width for a particular heatmap column.

* The columnStyle [headerTemplateID](/api/js/ejheatmap#members:itemsmapping-columnstyle-headertemplateid "headerTemplateID") is used to add the template within the header element of the particular column.  

* The columnStyle [templateID](/api/js/ejheatmap#members:itemsmapping-columnstyle-templateid "templateID") property is used to set an templateId for individual heatmap column. To set an template id for all heatmap columns, use defaultColumnStyle [templateID](/api/js/ejheatmap#members:defaultcolumnstyle-templateid "templateID") property.
 
* To customize the header column, use headerMapping [columnStyle](/api/js/ejheatmap#members:itemsmapping-headermapping-columnstyle "columnStyle") property.

* To hide the cell content, use [heatmapCell](/api/js/ejheatmap#members:heatmapcell "heatmapCell") [showContent](/api/js/ejheatmap#members:heatmapcell-showcontent "showContent") property as hidden and use [showColor](/api/js/ejheatmap#members:heatmapcell-showcolor "showColor") property to specify whether the cell color can be visible or not.

## Virtualization

Virtualization support is used to render large number of records in Heatmap with effective performance. This mode can be enabled by setting [enableVirtualization](/api/js/ejheatmap#members:enablevirtualization "enableVirtualization") property as true.

## Responsive

The heatmap control has support for the responsive behavior based on client browser’s width and height. To enable responsive, [isResponsive](/api/js/ejheatmap#members:isresponsive "isResponsive") property should be set as true.


