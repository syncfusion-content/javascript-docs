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
* You can use  and [column](/api/js/ejheatmap#members:itemsmapping-column "column") property to specify the rows and columns of heatmap.

* You can bind the user data in rows using [row](/api/js/ejheatmap#members:itemsmapping-row "row") [propertyName](/api/js/ejheatmap#members:itemsmapping-row-propertyname "propertyName") property and  display value using [displayName](/api/js/ejheatmap#members:itemsmapping-row-displayname "displayName") property.

* Similarly, you can bind the user data in columns using [propertyName](/api/js/ejheatmap#members:itemsmapping-column-propertyname "propertyName") property and display column values using [displayName](/api/js/ejheatmap#members:itemsmapping-column-displayname "displayName") property.  

* To bind the values for heatmap, use [value](/api/js/ejheatmap#members:itemsmapping-value "value") property.You can use [propertyName](/api/js/ejheatmap#members:itemsmapping-value-propertyname "propertyName") property and [displayName](/api/js/ejheatmap#members:itemsmapping-value-displayname "displayName") property to specify name and value respectively for row or column.
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

* The [headerMapping](/api/js/ejheatmap#members:itemsmapping-headermapping "headerMapping") property allows you to bind the header column(first column) with user data. 

* You can specify the collections of data which you need to bind it in a heatmap header using [propertyName](/api/js/ejheatmap#members:itemsmapping-headermapping-propertyname "propertyName") property and use [displayName](/api/js/ejheatmap#members:itemsmapping-headermapping-displayname "displayName") property to show the header value.

### ColumnMapping

* The [columnMapping](/api/js/ejheatmap#members:itemsmapping-columnmapping "columnMapping") property allows you to bind the columns with user data.

* In columnMapping, you can specify the collections of data which you need to bind it in heatmap columns using [propertyName](/api/js/ejheatmap#members:itemsmapping-columnmapping-propertyname "propertyName") property and use [displayName](/api/js/ejheatmap#members:itemsmapping-columnmapping-displayname "displayName") property to specify the column value.

## Appearance

* You can customize the individual heatmap column using [columnStyle](/api/js/ejheatmap#members:itemsmapping-columnstyle "columnStyle") [width](/api/js/ejheatmap#members:itemsmapping-columnstyle-width "width"), [textAlign](/api/js/ejheatmap#members:itemsmapping-columnstyle-textalign "textAlign"), [headerTemplateID](/api/js/ejheatmap#members:itemsmapping-columnstyle-headertemplateid "headerTemplateID") and [templateID](/api/js/ejheatmap#members:itemsmapping-columnstyle-templateid "templateID") property.

* You can customize the entire heatmap column using [defaultColumnStyle](/api/js/ejheatmap#members:defaultcolumnstyle "defaultColumnStyle"), [textAlign](/api/js/ejheatmap#members:defaultcolumnstyle-textalign "textAlign"), [headerTemplateID](/api/js/ejheatmap#members:defaultcolumnstyle-headertemplateid "headerTemplateID") and [templateID](/api/js/ejheatmap#members:defaultcolumnstyle-templateid "templateID") property.

* You can enable/disable virtualization for heatmap using [enableVirtualization](/api/js/ejheatmap#members:enablevirtualization "enableVirtualization") property.

* You can enable/disable responsive mode for heatmap by using [isResponsive](/api/js/ejheatmap#members:isresponsive "isResponsive") property.

* To hide the cell content, use [heatmapCell](/api/js/ejheatmap#members:heatmapcell "heatmapCell") [showContent](/api/js/ejheatmap#members:heatmapcell-showcontent "showContent") property as hidden and use [showColor](/api/js/ejheatmap#members:heatmapcell-showcolor "showColor") property to specify whether the cell color can be visible or not.

## Tooltip

* HeatMap provides support to show tooltip when mouse hovers over any rows/columns.

* To show/hide the tooltip of heatmap, use [enableTooltip](/api/js/ejheatmap#members:enabletooltip "enableTooltip") property.

* To show tooltip on mouse over, the [tooltipSettings](/api/js/ejheatmap#members:tooltipsettings "tooltipSettings") property of model needs to be set with the tooltipSettings [templateId](/api/js/ejheatmap#members:tooltipsettings-templateid "templateId") and [position](/api/js/ejheatmap#members:position "position").

* The [trigger](/api/js/ejheatmap#members:tooltipsettings-trigger "trigger") property specify the event action to showcase the tooltip. 


### Animation Effects

Determines the type of effect that takes place when showing/hiding the tooltip.

We can specify the [effect](/api/js/ejheatmap#members:tooltipsettings-animation-effect "effect") and the [speed](/api/js/ejheatmap#members:tooltipsettings-animation-speed "speed") for the animation using [animation](/api/js/ejheatmap#members:tooltipsettings-animation "animation") property.

### position

* The position object defines various attributes of the Tooltip position, including the element it is positioned in relation to, and how the position is adjusted within the defined container.

* The [associate](/api/js/ejheatmap#members:tooltipsettings-associate "associate") property is used to position the tooltip in relation with the target element.It can also be set to ‘mouse’ or the window, or an absolute x/y position on the page. 

* The [target](/api/js/ejheatmap#members:tooltipsettings-position-target "target") property is used to position the tooltip based on the associate property. You can position the tooltip at current mouse position when associate property set as `mouseenter`. It also possible to place the tooltip relation to the window when associate property set as `window` and can set target [horizontal](/api/js/ejheatmap#members:tooltipsettings-position-target-horizontal "horizontal") and [vertical](/api/js/ejheatmap#members:tooltipsettings-position-target-vertical "vertical") properties to position tooltip horizontal/vertical.

* To enable the arrow in tooltip, use [isBalloon](/api/js/ejheatmap#members:tooltipsettings-isballoon "isBalloon") property.

* To set the arrow position against popup, use [stem](/api/js/ejheatmap#members:tooltipsettings-position-stem "stem") [horizontal](/api/js/ejheatmap#members:tooltipsettings-position-stem-horizontal "horizontal") and [vertical](/api/js/ejheatmap#members:tooltipsettings-position-stem-vertical "vertical") property.

Please refer to the below code example which shows how to use tooltip in heatmap.

{% highlight html %}

<!--Define tooltip template-->
<script type="text/x-jsrender" id="mouseovertoolTipId">
    <div class="tooltip-style">Custom Tooltip
        <div style="height:0px;width:100%;border:1px solid white;"></div>
            <table>
                <tr>
                    <td style="width:50px;">Year  </td>
                    <td>{{:data.Year}}</td>
                </tr>
                <tr>
                    <td>Value  </td>
                    <td>{{:cellValue}}</td>
                </tr>
            </table>
    </div>
</script>
{% endhighlight %}

{% highlight js %}

$("#heatmap").ejHeatMap({
    //Defines mouse over tooltip
    toolTipSettings: {
        templateId:"mouseovertoolTipId",
        associate:"mouseFollow",
        position: {
            stem: { horizontal: "left", vertical: "top" }
            };
         }
    });
            
{% endhighlight %}

![](Getting-Started_images/Getting-Started_img4.png)
