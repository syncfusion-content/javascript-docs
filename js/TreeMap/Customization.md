---
layout: post
title: Customization
description: customization
platform: js
control: TreeMap
documentation: ug
api: /api/js/ejtreemap
---

# Customization

**TreeMap** control supports color customization to determine the exact combination of colors for tree nodes displayed in **TreeMap** and tooltip support to display additional information of treemap data.

## Color

You can customize the colors of the leaf nodes of **TreeMap** using the ColorMapping support of the **TreeMap**. 

ColorMapping is categorized into three different types such as,

* uniColorMapping
* rangeBrushColorMapping
* desaturationColorMapping

### Uni Color Mapping

You can color, all the leaf nodes with the same color by setting the `color` value of the `uniColorMapping` property of the **TreeMap**.

{% highlight js %}

       jQuery(function ($) {

            $("#treemapContainer").ejTreeMap({
                // ...   
                uniColorMapping: {
                    color: "Crimson"
                },         
                // ...   
            });
        });



{% endhighlight %}



![](/js/TreeMap/Customization_images/Customization_img1.png)

### Range Color Mapping

You can group the leaf nodes based on the range of the data’s color values. You can set a unique color for every ranges. To achieve this, specify the `to` and `from` values as range bound and `color` value to fill the leaf nodes of the particular range, through the `rangeColorMapping` property of the **TreeMap**.

{% highlight js %}

        jQuery(function ($) {

            $("#treemapContainer").ejTreeMap({
                // ...   
                rangeColorMapping: [
                        { color: "#77D8D8", from: "0", to: "1" },
                        { color: "#AED960", from: "0", to: "2" },
                        { color: "#FFAF51", from: "0", to: "3" },
                        { color: "#F3D240", from: "0", to: "4" }
                ],
                // ...   
            });
        });



{% endhighlight %}



![](/js/TreeMap/Customization_images/Customization_img2.png)

### Desaturation Color Mapping

You can differentiate all the leaf nodes using the `desaturationColorMapping` property of the **TreeMap**. Differentiation is achieved, even though same color is applied for all the leaf nodes by varying the opacity of the leaf nodes based on the color value specified in the color value range using `rangeMinimum` and `rangeMaximum` value of the data collection. You can also bound the opacity range by setting `from` and `to` property of the `desaturationColorMapping`.

{% highlight js %}


        jQuery(function ($) {

            $("#treemapContainer").ejTreeMap({
                // ...  
                desaturationColorMapping: {
                        color: "DeepSkyBlue", from: "1", to: "0.2", rangeMinimum: "0",  
                        rangeMaximum: "4"                        
                },
                // ...  
            });
        });


{% endhighlight %}



![](/js/TreeMap/Customization_images/Customization_img3.png)

## Tooltip

You can enable the tooltip support for the TreeMap by setting the `showTooltip` property to true. By default, it takes the property of the bound object that is referred to in the groupPath and displays its content when the corresponding node is tapped. The `tooltipTemplate` is a **HTML** element that is used to expose the custom template for the tooltip.

## Leaf Item Setting

You can customize the **Leaf level TreeMap items** using `leafItemSettings`. The Label and tooltip values take the property of bound object that is referred in the `labelPath` when defined.

{% highlight js %}

    <script type="text/javascript">
        jQuery(function ($) {
            $( "#treemapContainer").ejTreeMap({
                dataSource: population_data,
                colorValuePath: "Growth",
                weightValuePath: "Population",
                rangeColorMapping: [
                        { color: "#77D8D8", from: "0", to: "1" },
                        { color: "#AED960", from: "0", to: "2" },
                        { color: "#FFAF51", from: "0", to: "3" },
                        { color: "#F3D240", from: "0", to: "4" }
                ],                   
                levels: [
                  { groupPath: "Continent", groupGap: 5}
                ],

                leafItemSettings: { labelPath: "Region" },
                showTooltip:true,
                tooltipTemplate:'template' 
            });
        });
    </script>
    
    <script  id="template" type="application/jsrender">
        <div  style="margin-left:17px;margin-top:-45px;">      
            <div style="height:auto;width:auto;background:black;border-radius:3px;opacity:0.6">
                <div style="margin-top:-20px;margin-left:9px;padding-top:3px;margin-right:9px;">
                    <label style="margin-top:-20px;font-weight:normal;font-size:12px;color:white;font-family:Segoe UI;">{{:Region}}</label>
                </div>
                <div style="height:10px;"></div>
                <div style="margin-top:-10px;margin-left:9px;margin-right:9px;padding-bottom:3px;">
                    <label style="margin-top:-10px;font-weight:normal;font-size:14px;color:white;font-family:segoe ui light;">{{:Population}}</label>
                </div>
            </div>
        </div>            
    </script>


{% endhighlight %}



![](/js/TreeMap/Customization_images/Customization_img4.png)

