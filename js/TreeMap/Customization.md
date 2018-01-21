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

You can customize the color of leaf nodes in **Treemap** either using ColorMapping support of the **Treemap** or mapping a field in the datasource.

## Binding color from the datasource

You can set color for each leaf items from data source by using [`colorPath`](../api/ejtreemap#members:colorpath) property. 

N> While setting color, do not set any other color mapping for treemap because color mapping has higher priority than [`colorPath`](../api/ejtreemap#members:colorpath) property. And also, if [`colorPath`](../api/ejtreemap#members:colorpath) is set, the legend will be generated for each leaf item in treemap. 

{% highlight js %}

        jQuery(function ($) {

            $("#treemapContainer").ejTreeMap({
                // ...  
                colorPath : ‘fill’
                // ...  
            });
        });

{% endhighlight %}

![](/js/TreeMap/Customization_images/Customization_img5.png)

ColorMapping is categorized into three different types such as,

* [`uniColorMapping`](../api/ejtreemap#members:unicolormapping)
* [`rangeColorMapping`](../api/ejtreemap#members:rangecolormapping)
* [`desaturationColorMapping`](../api/ejtreemap#members:desaturationcolormapping)

### Uni Color Mapping

You can color, all the leaf nodes with the same color by setting the [`color`](../api/ejtreemap#members:unicolormapping-color) value of the [`uniColorMapping`](../api/ejtreemap#members:unicolormapping) property of the **TreeMap**.

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

Try it: [UniColorMapping](http://jsplayground.syncfusion.com/2v542ver)

### Range Color Mapping

You can group the leaf nodes based on the range of the data’s color values. You can set a unique color for every ranges. To achieve this, specify the [`to`](../api/ejtreemap#members:rangecolormapping-to) and [`from`](../api/ejtreemap#members:rangecolormapping-from) values as range bound and [`color`](../api/ejtreemap#members:rangecolormapping-color) or [`gradient colors`](../api/ejtreemap#members:rangecolormapping-gradientcolors) values to fill the leaf nodes of the particular range, through the [`range color mapping`](../api/ejtreemap#members:rangecolormapping) property of the **TreeMap**.

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

Try it: [RangeColorMapping](http://jsplayground.syncfusion.com/cbcyugjn)

### Desaturation Color Mapping

You can differentiate all the leaf nodes using the [`desaturation color mapping`](../api/ejtreemap#members:desaturationcolormapping) property of the **TreeMap**. Differentiation is achieved, even though same color is applied for all the leaf nodes by varying the opacity of the leaf nodes based on the color value specified in the [`color`](../api/ejtreemap#members:desaturationcolormapping-color) value range using [`rangeMinimum`](../api/ejtreemap#members:desaturationcolormapping-rangemaximum) and [`rangeMaximum`](../api/ejtreemap#members:desaturationcolormapping-rangeminimum) value of the data collection. You can also bound the opacity range by setting [`from`](../api/ejtreemap#members:desaturationcolormapping-from) and [`to`](../api/ejtreemap#members:desaturationcolormapping-to) property of the `desaturationColorMapping`.

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

Try it: [DesaturationColorMapping](http://jsplayground.syncfusion.com/qoh2upwr)

### Palette Color Mapping

You can customize the [`color`](../api/ejtreemap#members:palettecolormapping-colors) of each leaf nodes by providing a color palette of your choice by using the [`paletteColorMapping`](../api/ejtreemap#members:palettecolormapping) property.

{% highlight js %}
]
        jQuery(function ($) {

            $("#treemapContainer").ejTreeMap({
                // ...  
                paletteColorMapping: {
                        colors: ["red","green","blue", "yellow"]
                },
                // ...  
            });
        });


{% endhighlight %}


## Tooltip

You can enable the tooltip support for the TreeMap by setting the [`showTooltip`](../api/ejtreemap#members:showTooltip) property to true. By default, it takes the property of the bound object that is referred to in the groupPath and displays its content when the corresponding node is tapped. The [`tooltipTemplate`](../api/ejtreemap#members:tooltiptemplate) is a **HTML** element that is used to expose the custom template for the tooltip.

## Leaf Item Setting

You can customize the **Leaf level TreeMap items** using [`leafItemSettings`](../api/ejtreemap#members:leafitemsettings). In [`leftItemSettings`](../api/ejtreemap#members:leafitemsettings) following customization options are available.

* You can specify the border color using [`border brush`](../api/ejtreemap#members:leafitemsettings-borderbrush) property.

* For customizing border thickness, you can use [`border thickness`](../api/ejtreemap#members:leafitemsettings-borderthickness) property.

* To customize the gap between the leaf items, you can use [`gap`](../api/ejtreemap#members:leafitemsettings-gap) property.

* You can specify the label template for the leaf item using [`item template`](../api/ejtreemap#members:leafitemsettings-itemtemplate) property.

* The Label and tooltip values take the property of bound object that is referred in the [`labelPath`](../api/ejtreemap#members:leafitemsettings-labelpath) when defined.

* You can specify the position of the leaf labels using [`labelPosition`](../api/ejtreemap#members:leafitemsettings-labelposition) property.

* You can control the mode of label visibility of the labels using [`labelVisibilityMode`](../api/ejtreemap#members:leafitemsettings-labelvisibilitymode) property.

* To show or hide the visibility of the leaf item labels you can use [`showLabels`](../api/ejtreemap#members:leafitemsettings-showlabels) property.

* For specifying over flow action of left item labels you can use [`textOverflow`](../api/ejtreemap#members:leafitemsettings-textOverflow) property.

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

Try it: [LeafItemSettings](http://jsplayground.syncfusion.com/gec0w4gb)

## Border Brush

You can able to customize the border color of the treemap using the property [`borderBrush`](../api/ejtreemap#members:borderbrush). 

{% highlight js %}
 
//To set borderBrush API value during initialization 
  $("#container").ejTreeMap( {borderBrush:'white'});

{% endhighlight %}

## Border Thickness

For customizing the border thickness of the treemap, you can use the [`borderThickness`](../api/ejtreemap#members:borderthickness) property.

{% highlight js %}
 
//To set borderThickness API value during initialization 
  $("#container").ejTreeMap({borderThickness:1});

{% endhighlight %}

## Dock Position

You can position the legend at top, bottom, left and right side of the treemap as per your requirement. For changing the position as per your requirement, you can use [`dockPosition`](../api/ejtreemap#members:dockposition) property.

<ts name="ej.datavisualization.TreeMap.DockPosition"/>
Specifies the dockPosition for legend

<table class="params">
	<thead>
		<tr>
			<th>Name </th>			
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">top</td>			
			<td class="description">specifies the top position</td>
		</tr>
		<tr>
			<td class="name">bottom</td>			
			<td class="description">specifies the bottom position</td>
		</tr>
    <tr>
			<td class="name">right</td>			
			<td class="description">specifies the bottom position</td>
		</tr>
    <tr>
			<td class="name">left</td>			
			<td class="description">specifies the left position</td>
		</tr>
	</tbody>
</table>

{% highlight js %}
 
//To set dockPosition API value during initialization 
  $("#container").ejTreeMap( {legendSettings:{ dockPosition: "top"}});

{% endhighlight %}

## Clicking and Dragging

You can select the single treemap element on click and drag. To click and drag treemap items, you have to enable the [`draggingOnSelection`](../api/ejtreemap#members:draggingOnSelection) property.

{% highlight js %}
 
//To set draggingOnSelection API value during initialization 
  $("#container").ejTreeMap({draggingOnSelection:false});
{% endhighlight %}

For selecting the group element of treemap while clicking and dragging, you can use [`draggingGroupOnSelection`] property.

{% highlight js %}
 
//To set draggingGroupOnSelectionAPI value during initialization 
  $("#container").ejTreeMap({draggingGroupOnSelection:false});
{% endhighlight %}

## Fill with Gradient

You can customize that whether gradient color have to be applied for treemap or not. This can be customized using the property [`enableGradient`](../api/ejtreemap#members:enableGradient).

{% highlight js %}
 
//To set enableGradient API value during initialization 
  $("#container").ejTreeMap({enableGradient:true});

{% endhighlight %}

## Responsive Treemap

You can customize whether treemap have to be [`responsive`](../api/ejtreemap#members:isresponsive) or not while resizing the container. For making treemap responsive you can use [`enableResize`](../api/ejtreemap#members:enableresize) property.

{% highlight js %}
 
//To set enableResize API value during initialization 
  $("#container").ejTreeMap({enableResize:false});

{% endhighlight %}

## GroupColorMapping

You can customize the color of the each group using **groupColorMapping** property. To use group color mapping, kindly specify [`groupId`](../api/ejtreemap#members:groupcolormapping-groupid) and `rangeColorMapping` inside the [`groupColorMapping`](../api/ejtreemap#members:groupcolormapping). 

{% highlight js %}

//To set groupColorMapping API value during initialization 
  $("#container").ejTreeMap( {groupColorMapping:[{ groupID: "Asia", rangeColorMapping:[{ color: "#77D8D8", from: "0", to: "1"}]}] });

{% endhighlight %}

## GroupSelectionMode

You can specifies the [`selection mode`](../api/ejtreemap#members:selectionmode) of the treemap using [`groupSelectionMode`](../api/ejtreemap#members:groupselectionmode) property. You can set either group selection mode value as `Default` or  `Multiple`. 

{% highlight js %}

// Set the selection mode during initialization.                                        
          $("#container").ejTreeMap({groupSelectionMode:'default'});

{% endhighlight %}

## Header

You can specify the header for the parent item using the property [`header`](../api/ejtreemap#members:header). This is applicable only for hierarchical data source. 

{% highlight js %}

//To set header API value during initialization 
  $("#container").ejTreeMap({header:"Country"});

{% endhighlight %}

## Specifying HierarchicalDatasource

You can specify whether data source bound for the treemap is hierarchical or not using the property [`isHierarchicalDatasource`](../api/ejtreemap#members:ishierarchicaldatasource).

{% highlight js %}

//To set isHierarchicalDatasource API value during initialization 
  $("#container").ejTreeMap({isHierarchicalDatasource : true});

{% endhighlight %}

## Localization

You can specify the name of the culture based on which treemap is localized. To achieve this you can use the treemap property [`locale`](../api/ejtreemap#members:locale).

**Enable Group Separator** is used to Convert the date object to string while using the locale settings, you can set [`enableGroupSeparator`](../api/ejtreemap#members:enablegroupseparator) property as **true**.

{% highlight js %}
         
   //Sets the locale value
   $("#container").data("ejTreeMap").model.locale = "en-US";

{% endhighlight %}

## Treemap Items

You can specify the treemap items which you want to display in the treemap using the property [`treeMapItems`](../api/ejtreemap#members:treemapitems).

{% highlight js %}

// Set the treeMapItems during initialization. 
  $("#container").ejTreeMap({treeMapItems:[]});
  
{% endhighlight %}

