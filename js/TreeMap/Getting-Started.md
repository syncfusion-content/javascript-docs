---
layout: post
title: Getting-Started
description: getting started
platform: js
control: TreeMap
documentation: ug
api: /api/js/ejtreemap
---

# Getting Started

This section explains briefly about how to create a **TreeMap** in your application with **JavaScript**.

## Create your first TreeMap in JavaScript

You can configure an **Essential JavaScript TreeMap** in simple steps. In this section, you can learn how to configure a TreeMap control in a real-time scenario where it is used to visually represent the percentage of growth in population in each continent. It also provides a walk-through on some of the customization features available in TreeMap control. 

![](/js/TreeMap/Getting-Started_images/Getting-Started_img1.png)

## Add Libraries

To add a **TreeMap** control in your application, refer the following libraries in an **HTML** page. 

* [jQuery](http://jquery.com/) version  1.10.1 and above
* ej.widgets.all  
* JsRender
* ej.web.all

The following code sample explains how to link these libraries from a [Content Delivery Network (CDN)](https://en.wikipedia.org/wiki/Content_delivery_network).

{% highlight js %}

    <!--  jquery script  -->
      <script src="http://code.jquery.com/jquery-1.10.1.min.js"                      type="text/javascript"></script>
    <!-- Essential JS UI widget -->
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/ej.widgets.all.min.js"></script>
    <!-- JS Render widget -->
      <script src="http://cdn.jsdelivr.net/jsrender/1.0pre35/jsrender.min.js" type="text/javascript"></script>  
    <!-- Essential JS theme  -->
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" type="text/javascript"></script>

{% endhighlight %}

## Initialize TreeMap

Create a **&lt;div&gt;** tag with a specific id and set the height and width to determine the **TreeMap** size to be rendered.

{% highlight js %}

    <body>
      <div id="treemapContainer" style="width: 700px; height: 430px;"></div>
    </body>

{% endhighlight %}

### Populate DataSource

The [`dataSource`](../api/ejtreemap#members:datasource) property accepts the collection values as input. For example, you can provide the list of objects as input.

### Weight Value Path

You can calculate the size of the object using [`weightValuePath`](../api/ejtreemap#members:weightvaluepath) of **TreeMap**.

Add a **&lt;script&gt;** tag anywhere in a web page and initialize **TreeMap** as illustrated in the following code sample. 

{% highlight html %}

    <script type="text/javascript">
      jQuery(function ($) {	
        $("#treemapContainer").ejTreeMap({
          dataSource: population_data,
          weightValuePath: "Population",
        });
      });
    </script>


{% endhighlight %}



Populate the TreeMap data in JSON object. For example, you can use population data of countries to generate TreeMap data as illustrated in the following code sample.

{% highlight js %}

    <head>
      <!-- TreeMapData -->
      <script type="text/javascript">

        var population_data = [
                   { Continent: "Asia", Region: "Southern Asia", Growth: 1.32, Population: 1749046000 },
                   { Continent: "Asia", Region: "Eastern Asia", Growth: 0.57, Population: 1620807000 },
                   { Continent: "Asia", Region: "South-Eastern Asia", Growth: 1.20, Population: 618793000 },
                   { Continent: "Asia", Region: "Western Asia", Growth: 1.98, Population: 245707000 },
                   { Continent: "Asia", Region: "Central Asia", Growth: 1.43, Population: 64370000 },
                   { Continent: "Europe", Region: "Europe", Growth: 0.10, Population: 742452000 },
                   { Continent: "America", Region: "South America", Growth: 1.06, Population: 406740000 },
                   { Continent: "America", Region: "Northern America", Growth: 0.85, Population: 355361000 },
                   { Continent: "America", Region: "Central America", Growth: 1.40, Population: 167387000 },
                   { Continent: "Africa", Region: "Eastern Africa", Growth: 2.89, Population: 373202000 },
                   { Continent: "Africa", Region: "Western Africa", Growth: 2.78, Population: 331255000 },
                   { Continent: "Africa", Region: "Northern Africa", Growth: 1.70, Population: 210002000 },
                   { Continent: "Africa", Region: "Middle Africa", Growth: 2.79, Population: 135750000 },
                   { Continent: "Africa", Region: "Southern Africa", Growth: 0.91, Population: 60425000 }
        ]
      </script>
    </head>


{% endhighlight %}



N> Population data is referred from [List of continents by population](http://en.wikipedia.org/wiki/List_of_continents_by_population).

The final **HTML** file is illustrated in the following code sample.

{% highlight html %}

    <html xmlns="http://www.w3.org/1999/xhtml">
      <head>
        <title></title>
            
        <!--  jquery script  -->
        <script src="http://code.jquery.com/jquery-1.10.1.min.js" type="text/javascript"></script>
    
        <!-- Essential JS UI widget -->
        <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/ej.widgets.all.min.js"></script>

        <!-- JS Render widget -->
        <script src="http://cdn.jsdelivr.net/jsrender/1.0pre35/jsrender.min.js" type="text/javascript"></script>
      
        <!-- Essential JS theme -->
        <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" type="text/javascript"></script>

        <!-- TreeMapData -->
        <script type="text/javascript">

            var population_data = [
                   { Continent: "Asia", Region: "Southern Asia", Growth: 1.32, Population: 1749046000 },
                   { Continent: "Asia", Region: "Eastern Asia", Growth: 0.57, Population: 1620807000 },
                   { Continent: "Asia", Region: "South-Eastern Asia", Growth: 1.20, Population: 618793000 },
                   { Continent: "Asia", Region: "Western Asia", Growth: 1.98, Population: 245707000 },
                   { Continent: "Asia", Region: "Central Asia", Growth: 1.43, Population: 64370000 },
                   { Continent: "Europe", Region: "Europe", Growth: 0.10, Population: 742452000 },
                   { Continent: "America", Region: "South America", Growth: 1.06, Population: 406740000 },
                   { Continent: "America", Region: "Northern America", Growth: 0.85, Population: 355361000 },
                   { Continent: "America", Region: "Central America", Growth: 1.40, Population: 167387000 },
                   { Continent: "Africa", Region: "Eastern Africa", Growth: 2.89, Population: 373202000 },
                   { Continent: "Africa", Region: "Western Africa", Growth: 2.78, Population: 331255000 },
                   { Continent: "Africa", Region: "Northern Africa", Growth: 1.70, Population: 210002000 },
                   { Continent: "Africa", Region: "Middle Africa", Growth: 2.79, Population: 135750000 },
                   { Continent: "Africa", Region: "Southern Africa", Growth: 0.91, Population: 60425000 }
            ]

        </script>
      </head>
    <body>
    	   
      <div id="treemapContainer" style="width: 700px; height: 430px;"></div>
  
      <script type="text/javascript">
        jQuery(function ($) {	
            $("#treemapContainer").ejTreeMap({
                dataSource: population_data,
                weightValuePath: "Population",
            });
        });
      </script>	        
    </body>
    </html>


{% endhighlight %}



The following screenshot displays a TreeMap control that is rendered after executing the above code sample. The control is rendered with the default properties using the above code. 

![](/js/TreeMap/Getting-Started_images/Getting-Started_img2.png)

Try it: [WeightValuePath](http://jsplayground.syncfusion.com/lxhlxr0m)

## Group with Levels

You can group TreeMap items using the [`levels`](../api/ejtreemap#members:levels) in it.

### Group Path

You can use [`groupPath`](../api/ejtreemap#members:levels-grouppath) property for every flat level of the TreeMap control. It is a path to a field on the source object that serves as the “Group” for the level specified. You can group the data based on the [`groupPath`](../api/ejtreemap#members:levels-grouppath) in the TreeMap control. When the [`groupPath`](../api/ejtreemap#members:levels-grouppath) is not specified, then the items are not grouped and the data is displayed in the order specified in the [`dataSource`](../api/ejtreemap#members:datasource).

### Group Gap

You can use [`groupGap`](../api/ejtreemap#members:levels-groupgap) property to separate the items from every flat level and to differentiate the levels mentioned in the TreeMap control.

The following code sample explains how to group TreeMap Items using ‘Levels’.

{% highlight html %}

    <script type="text/javascript">
        jQuery(function ($) {
            $("#treemapContainer").ejTreeMap({
               dataSource: population_data,
               weightValuePath: "Population",
               levels: [
                     { groupPath: "Continent", groupGap: 5}
                   ]
            });
        });
    </script>


{% endhighlight %}



The following screenshot displays grouping of **TreeMap****Items** using **Levels**.

![](/js/TreeMap/Getting-Started_images/Getting-Started_img3.png)

Try it: [Grouping Levels](http://jsplayground.syncfusion.com/mngx4smn)

## Customize TreeMap by Range

You can differentiate the nodes based on its value and color ranges using [`Range color`](../api/ejtreemap#members:rangecolormapping). You can also define the color value range using from and to properties. 

### Color Value Path

The [`colorValuePath`](../api/ejtreemap#members:colorvaluepath) of TreeMap is a path to a field on the source object. You can determine the color for the object using [`colorValuePath`](../api/ejtreemap#members:colorvaluepath) of TreeMap.

The following code sample explains how to customize TreeMap appearance using Range.

{% highlight html %}

    <script type="text/javascript">
        jQuery(function ($) {
            $("#treemapContainer").ejTreeMap({
                dataSource: population_data,
                weightValuePath: "Population",
                levels: [
                    { groupPath: "Continent", groupGap: 5 }
                ],
                colorValuePath: "Growth",
                rangeColorMapping: [
                    { color: "#DC562D", from: "0", to: "1" },
                    { color: "#FED124", from: "1", to: "1.5" },
                    { color: "#487FC1", from: "1.5", to: "2" },
                    { color: "#0E9F49", from: "2", to: "3" }
                ]
            });
        });
    </script>


{% endhighlight %}



The following screenshot displays a customized **TreeMap** control. 

![](/js/TreeMap/Getting-Started_images/Getting-Started_img4.png)

Try it: [ColorValuePath](http://jsplayground.syncfusion.com/dzkekv33)

## Enable Tooltip

You can enable the tooltip by setting [`showTooltip`](../api/ejtreemap#members:showTooltip) property to “true”. By default, it takes the property of the bound object that is referred in the [`weightValuePath`](../api/ejtreemap#members:weightvaluepath) and displays its content when the corresponding node is hovered. You can customize the template for tooltip using [`tooltipTemplate`](../api/ejtreemap#members:tooltiptemplate) property.

## Leaf ItemSettings

You can customize the Leaf level TreeMap items using [`leafItemSettings`](../api/ejtreemap#members:leafitemsettings). The Label and tooltip values take the property of bound object that is referred in the [`labelPath`](../api/ejtreemap#members:leafitemsettings-labelpath) when defined. The following code sample displays how the tooltip is enabled.

{% highlight html %}

    <script type="text/javascript">
      jQuery(function ($) {
            $("#treemapContainer").ejTreeMap({
                dataSource: population_data,
                weightValuePath: "Population", 
                levels: [
                     { groupPath: "Continent", groupGap: 5}
                   ], 
                colorValuePath: "Growth",
                rangeColorMapping: [
                      { color: "#DC562D", from: "0", to: "1" },
                      { color: "#FED124", from: "1", to: "1.5" },
                      { color: "#487FC1", from: "1.5", to: "2" },
                      { color: "#0E9F49", from: "2", to: "3" }
                ],
                showTooltip:true,
                leafItemSettings: { labelPath: "Region" }
            });
        });
    </script>


{% endhighlight %}



The following screenshot displays a ToolTip in a **TreeMap** control.

![](/js/TreeMap/Getting-Started_images/Getting-Started_img5.png)

Try it: [LeafItemSettings](http://jsplayground.syncfusion.com/apibaesy)

## Enable Legend

You can set the color value of leaf nodes using [`TreeMap Legend`](../api/ejtreemap#members:legendsettings). This legend is appropriate only for the TreeMap whose leaf nodes are colored using `rangeColorMapping`. You can set [`showLegend`](../api/ejtreemap#members:showlegend) property value to “true” to make a legend visible.

### Label for Legend

You can customize the labels of the legend item using [`legendLabel`](../api/ejtreemap#members:rangecolormapping-legendlabel) property of [`rangeColorMapping`](../api/ejtreemap#members:rangecolormapping). 

The following code sample illustrates how to add labels for legend in a TreeMap.

{% highlight html %}

    <script type="text/javascript">
      jQuery(function ($) {
            $("#treemapContainer").ejTreeMap({
                dataSource: population_data,
                weightValuePath: "Population", 
                levels: [
                     { groupPath: "Continent", groupGap: 5}
                   ], 
                colorValuePath: "Growth",
                rangeColorMapping: [
                  { color: "#DC562D", from: "0", to: "1", **legendLabel: "0 - 1 %    Growth"** },
                  { color: "#FED124", from: "1", to: "1.5", **legendLabel: "1 - 1.5 % Growth"** },
                  { color: "#487FC1", from: "1.5", to: "2", **legendLabel: "1.5 - 2 % Growth"** },
                  { color: "#0E9F49", from: "2", to: "3", **legendLabel: "2 - 3 % Growth"** }                   
                ],
                showTooltip:true,
                leafItemSettings: { labelPath: "Region" },
                showLegend: true,
                legendSettings: {
                  showLegend:true,                                                                      
                  height:38,
                  width:690,
                },
            });
        });
    </script>


{% endhighlight %}



The following screenshot displays labels in a **TreeMap** control. 

![](/js/TreeMap/Getting-Started_images/Getting-Started_img6.png)

Try it: [Legend Label](http://jsplayground.syncfusion.com/lhtvawqv)

N> Population data is referred from [List of continents by population](http://en.wikipedia.org/wiki/List_of_continents_by_population).



