---
layout: post
title: Map-Elements
description: map elements
platform: js
control: Maps
documentation: ug
api: /api/js/ejmap
---

# Map Elements

Map control contains a set of map elements such as shapes, bubbles, markers, legend, labels and data items that can be visualized with the customized appearance showing additional information on the map by using the bound data.

## Markers

Markers are notes used to leave some message on the map. 

There are two ways to set marker for map.

1. Marker and marker template

2. Adding marker objects to map.

### Markers and Marker Template 

The [`markers`](../api/ejmap#members:layers-markers) property has a list of objects that contains the data for Annotation. By default, it displays the bound data at the specified latitude and longitude. The [`markerTemplate`](../api/ejmap#members:layers-markertemplate) property is used for customizing the [`template`](../api/ejmap#members:layers-mapitemstemplate) for markers.	

{% highlight javascript %}

    var markers = [
        { latitude: 37.0000, longitude: -120.0000, city: "California" },
        { latitude: 40.7127, longitude: -74.0059, city: "New York" },
        { latitude: 42, longitude: -93, city: "Iowa" }            
    ];
      
    jQuery(function ($) {
        $("#mapContainer").ejMap({
            layers: [ 
            {
                // ...                        
                markers: markers,
                markerTemplate: 'template'
            }]
        });
    });

    <div  id="template" style="display: none;">
        <div>
            <div  style="background-image:url(http://js.syncfusion.com/demos/web/Images/map/pin.png);margin-left:3px;height:40px;width:25px;margin-top:-15px;">
	   	   </div>
        </div>
    </div>  

{% endhighlight %}



![](/js/Maps/Map-Elements_images/Map-Elements_img1.png)

### Adding Marker objects to the map

Without datasource, n number of markers can be added to shape layers with `markers` property. Each marker object contains the following list of properties.

* [`label`](../api/ejmap#layersmarkerslabel-string) - Text that displays some information about the annotation in text format.
* [`latitude`](../api/ejmap#layersmarkerslatitude-number) - Latitude point determine the Y-axis position of annotation.
* [`longitude`](../api/ejmap#layersmarkerslongitude-number) - Longitude point determine the X-axis position of annotation.



{% highlight javascript %}

    var markers = [
        { latitude: 37.0000, longitude: -120.0000, city: "California" },
        { latitude: 40.7127, longitude: -74.0059, city: "New York" },
        { latitude: 42, longitude: -93, city: "Iowa" }            
    ];

    jQuery(function ($) {
        $("#mapContainer").ejMap({
            layers: [ 
            {
                // ...                        
                markers: markers,
                markerTemplate: 'template'
            }]
        });
    });

    <div  id="template" style="display: none;">
        <div>
            <div style="margin-left:8px;height:45px;width:120px;margin-top:-23px;">					
	           <label class="label1" style="color:black;margin-left:15px;font-weight:normal">{{:city}}</label>				 			 
	        </div>
        </div>
    </div>  


{% endhighlight %}



![](/js/Maps/Map-Elements_images/Map-Elements_img2.png)

## Bubbles

Bubbles in the **Maps** control represent the underlying data values of the map. Bubbles are scattered throughout the map shapes that contain bound values.

Bubbles are included when data binding and the [`bubbleSettings`](../api/ejmap#members:layers-bubblesettings) is set to the shape layers. 

### Properties


<table>
<tr>
<th>
Property</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
maxValue</td><td>
String</td><td>
Get or sets the maximum height and width of the bubble.</td></tr>
<tr>
<td>
minValue</td><td>
String</td><td>
Gets or sets the minimum height and width of the bubble.</td></tr>
<tr>
<td>
colorValuePath</td><td>
String</td><td>
Get or sets the field value that is to be fetched from data for each bubble used for determining the bubble color.</td></tr>
<tr>
<td>
valuePath</td><td>
String</td><td>
Gets or sets the field value that is to be fetched from data for each bubble.</td></tr>
<tr>
<td>
colorMappings</td><td>
Collection of RangeColorMapping</td><td>
Gets or sets the tree map colors.</td></tr>
<tr>
<td>
Color</td><td>
String</td><td>
Gets or sets the fill [`color`](../api/ejmap#members:layers-bubblesettings-color) for bubbles.</td></tr>
<tr>
<td>
showTooltip</td><td>
Boolean</td><td>
Enable or disable the tooltip for bubbles.</td></tr>
<tr>
<td>
tooltipTemplate</td><td>
String</td><td>
Gets or sets the tooltip template for bubbles.</td></tr>
<tr>
<td>
bubbleOpacity</td><td>
Boolean</td><td>
Specifies the [`bubbleOpacity`](../api/ejmap#members:layers-bubblesettings-bubbleopacity) value of bubbles for shape layer in map.</td></tr>
<tr>
<td>
showBubble</td><td>
Boolean</td><td>
Specifies the [`showBubble`](../api/ejmap#members:layers-bubblesettings-showbubble) visibility status map.</td></tr>
</table>

### Add Bubbles to the Map

To add bubbles to a map, the bubble marker setting is added to the shape file layer. Create the Model and ViewModel as illustrated in the Data Binding topic and add the following code. Also set the [`maxValue`](../api/ejmap#members:layers-bubblesettings-maxvalue), [`minValue`](../api/ejmap#members:layers-bubblesettings-minvalue),['colorValuePath'](../api/ejmap#members:layers-bubblesettings-colorvaluepath) and [`valuePath`](../api/ejmap#members:layers-bubblesettings-valuepath) properties as illustrated in the following code sample.

N> `Tooltip` and [`Color Mappings`](../api/ejmap#members:layers-bubblesettings-colormappings) for bubble is to be set as similar to the tooltip and color mappings set in the layers and shapeSettings. For more details, refer to the Tooltip and Color Mappings section.



{% highlight javascript %}

    jQuery(function ($) {
        $("#mapContainer").ejMap({
            layers: [
            {
                shapeData: usMap,
                shapeDataPath: "name",
                shapePropertyPath: "name",
                dataSource: [
                    { name: "California", population: "38332521" },
                    { name: "New York", population: "19651127" },
                    { name: "Iowa", population: "3090416" }
                ],
                enableMouseHover: true,
                shapeSettings: {
                    fill: "#9CBF4E",
                    strokeThickness: "0.5",
                    stroke: "White"
                },
                bubbleSettings: {
                    showBubble:true,
                    minValue: "20",
                    maxValue: "40",
                    color: "#C99639",
                    valuePath: "population"
                }
            }]
        });
    });

{% endhighlight %}



![](/js/Maps/Map-Elements_images/Map-Elements_img3.png)

## Add bubbles to the map

You can set color for each bubble by using [`colorPath`](../api/ejmap#members:layers-bubblesettings-colorpath) property in bubble settings. 

N> While settings color for bubbles by using [`colorPath`], do not set any other color mapping hence color mapping is having higher priority than [`colorPath`]. 

{% highlight javascript %}

    jQuery(function ($) {

        $("#maps").ejMap({ 
        //…
            layers: [ 
            {
                shapeSettings: {
                    colorPath: "shapeFill",
                },
                bubbleSettings: {
                    showBubbles: true,
                    colorPath: “fill”
                }
            //…
        });

    });

{% endhighlight %}

![](/js/Maps/Map-Elements_images/Map-Elements_img7.png)

While binding [`colorPath`](../api/ejmap#members:layers-bubblesettings-colorpath) for bubbles, it is possible to render the legend for each bubble. To achieve this, set the [`textPath`](../api/ejmap#members:layers-legendsettings-text) for legend. [`textPath`] contains another field name in the datasource. As per the text, content in the field legend will be generated. 

{% highlight javascript %}

$("#maps").ejMap({ 
     //…
     layers: [ 
     {
            shapeSettings: {
               colorPath: "shapeFill",
            },
            bubbleSettings: {
               showBubbles: true,
               colorPath: “fill”
            },
            legendSettings:{
               showLegend: true,
               textPath: “name”
            }
     //…
});

{% endhighlight %}

![](/js/Maps/Map-Elements_images/Map-Elements_img8.png)

## Legend

A legend is a key used on a map that contains swatches of symbols with descriptions. It provides valuable information for interpreting what the map is displaying and can be represented in various colors, shapes or other identifiers based on the data. It gives a breakdown of what each symbol represents throughout the map.

### Visibility

The Legends can be made visible by setting the [`showLegend`](../api/ejmap#members:layers-legendsettings-showlegend) property of legendSettings to true. 

### Positioning of the Legend

The legend can be positioned in two ways.

1. Absolute Position.

2. Dock Position.

#### Absolute Position

Based on the margin values of X and Y-axes, the Map legends can be positioned with the support of [`positionX`](../api/ejmap#members:layers-legendsettings-positionx) and [`positionY`](../api/ejmap#members:layers-legendsettings-positiony) properties available in `legendSettings`. For positioning the legend based on margins corresponding to a map, [`position`](../api/ejmap#members:layers-legendsettings-position) value is set as ‘_none_’.

#### Dock Position

The map legends can be positioned in following locations within the container.

1. topLeft

2. topCenter

3. topRight

4. centerLeft

5. center

6. centerRight

7. bottomLeft

8. bottomRight

9. bottomCenter

10. bottomRight

11. none

You can set this option by using [`dockPosition`](../api/ejmap#members:layers-legendsettings-dockposition) property in [`legendSettings`](../api/ejmap#members:layers-legendsettings).

### Legend Size

The map legend size can be modified by using the [`height`](../api/ejmap#members:layers-legendsettings-height) and [`width`](../api/ejmap#members:layers-legendsettings-width) properties in [`legendSettings`](../api/ejmap#members:layers-legendsettings).

### Legend for Shapes

The Layer shape type legends can be generated for each color mappings in shape settings. 

N> Here, Equal Color Mapping code sample for shapeSettings with color mappings is referred.



{% highlight javascript %}

    jQuery(function ($) {
        $("#mapContainer").ejMap({
            layers: [
            {
                // ...
                legendSettings:{
                    showLegend:true,
                    position:"bottomleft",
                    height: 30,
                    width: 70,                         
                },
                // ...                        
            }]
        });
    });

{% endhighlight %}



![](/js/Maps/Map-Elements_images/Map-Elements_img4.png)

### Interactive Legend

The legends can be made interactive with an arrow mark indicating the exact range color in the legend when the mouse hovers over the corresponding shapes. You can enable this option by setting [`mode`](..) property in [`legendSettings`](../api/ejmap#members:layers-legendsettings) value as “interactive” and default value of [`mode`](../api/ejmap#members:layers-legendsettings-mode) property is “default” to enable the normal legend.

#### Title for Interactive Legend

You can provide the title for interactive legend by using [`title`](../api/ejmap#members:layers-legendsettings-title) property in `legendSettings`.

#### Label for Interactive Legend

You can provide the left and right labels to interactive legend by using [`leftLabel`](../api/ejmap#members:layers-legendsettings-leftlabel) and [`rightLabel`](../api/ejmap#members:layers-legendsettings-rightlabel) properties in `legendSettings`. 

N> Here, Range Color Mapping code snippet for shapeSettings with color mappings is referred.



{% highlight javascript %}

    jQuery(function ($) {
        $("#mapContainer").ejMap({
            layers: [
            {
                // ...
                legendSettings: {
                    showLegend: true,
                    dockOnMap:true,
                    height: 15,
                    width: 150,
                    position: "topleft",
                    mode: "interactive",
                    title: "Population",
                    leftLabel: "0.5M",
                    rightLabel: "40M"
                },
                // ...                        
            }]
        }); 
    });

{% endhighlight %}



![](/js/Maps/Map-Elements_images/Map-Elements_img5.png)

### Bubble Legend

A bubble legend feature is used to provide the key (legend) for another map element bubble. You can activate the Bubble legend by setting the enum [`type`](../api/ejmap#members:layers-legendsettings-type) in `legendSettings` as “bubble” and this enables you to easily identify what value a particular bubble is representing.

{% highlight javascript %}

    jQuery(function ($) {
        $("#map").ejMap({
            layers: [
            {
                legendSettings: {
                    // ...
                    type: "bubbles",                            
                    // ...
                },
                
                bubbleSettings: {
                    showBubble:true,
                    valuePath: "population",
                    minValue: 20,
                    maxValue: 40,	
                    colorMappings:
                    {
                        rangeColorMapping:
                        [
                            {
                                from: 500000,
                                to: 1000000,
                                color: "#9CBF4E",
                                range: 10688
                            },
                            {
                                from: 1000001,
                                to: 5000000,
                                color: "#45D6BD",
                                range: 19390
                            },
                            {
                                from: 5000001,
                                to: 10000000,
                                color: "#FF567C",
                                range: 18718
                            },
                            {
                                from: 10000001,
                                to: 40000000,
                                color: "#470F52",
                                range: 30716
                            }
                        ],
                    }                                
                },
                shapeData: usMap
                }
            ]
        });
    });


{% endhighlight %}



![](/js/Maps/Map-Elements_images/Map-Elements_img6.png)

### Legend Icon

To get the legend icon value for legend settings by using icon property. You can customize the icon by using the [`icon width`](../api/ejmap#members:layers-legendsettings-iconheight) and [`icon height`](../api/ejmap#members:layers-legendsettings-iconwidth) property.

{% highlight javascript %}

 $("#container").ejMap({layers: [{legendSettings: {icon:"rectangle"} }]})

{% endhighlight %}



