---
layout: post
title: User-Interaction
description: user interaction
platform: js
control: Maps
documentation: ug
---

# User Interaction

Options like zooming, panning and map selection enables the effective interaction on map elements.

##Map Selection

Each shape in the map can be selected and deselected during interaction with shapes. 

The **selectionColor** property is used to get or set the selected shape color. The **selectionStroke** and **selectionStrokeWidth** properties are used to customize the selected shape border.

You can select the shape by tapping on the shape. The Single selection is enabled by the **enableSelection** property of shape layer. When **enableSelection** is set to false, the shapes cannot be selected. 

{% highlight html %}

        jQuery(function($) {
            $("#mapContainer").ejMap({
                layers: [
                    {
                        shapeData: usMap,
                        ShapeSettings: {
                            fill: "#9CBF4E",
                            strokeThickness: "0.5",
                            stroke: "White",
                            selectionStrokeWidth: 2,
                            selectionStroke:"white",
                            selectionColor: "#BC5353"
                        },
                        enableSelection: true
                    }
                ]
            });
        }); 


{% endhighlight %}



{% include image.html url="/js/Maps/User-Interaction_images/User-Interaction_img1.png" Caption="Map with enable selection property"%}

##Zooming

The zooming feature enables you to zoom in and out of the map to show in-depth information. It is controlled by the **level** property of the map. When the zoom level of the **Map** control is increased, the map is zoomed in. When the zoom level is decreased, then the map is zoomed out.

###Properties Related to Zooming

The following properties are related to the zooming feature of the **Maps** control:

1. level

2. enableZoom

3. minValue

4. maxValue

###level

The **level** property determines the map’s scale size when zooming. The default value of **level** is 1. 

> _**Note:**_ level cannot be less than 1.

###enableZoom

The **enableZoom** property enables or disables the zooming feature. 

###minValue

The **minValue** property is used to set the minimum zoom level of the map. 

###maxValue

The **maxValue** property is used to set the maximum zoom level of the map.

{% highlight html %}


        jQuery(function($) {
            $("#mapContainer").ejMap({
                layers: [
                    {
                        shapeData: usMap
                    }
                ],
                zoomSettings:{
                    enableZoom: true,
                    minValue: 1,
                    maxValue: 20,
                    level: 1
                }
            });
        }); 	


{% endhighlight %}

##Additional Options to Zoom the Map

Maps can be zoomed using the following options also,

* Using Zoom method.

* Using mouse scroll.

* Using mouse double tap.

* Using shape selection

* Using Position

###Using Zoom method

You can zoom the Maps using **zoom** method. The zoom method contains parameter zoom value. The map can be zoomed or scaled based on zoom value parameter.

{% highlight html %}
 
        $("#map").ejMap("zoom", 2);


{% endhighlight %}

###Using mouse scroll

You can zoom the map with mouse events using mouse scroll. When the mouse is scrolled up, the map is zoomed in and when the mouse is scrolled down, the map is zoomed out.

###Using mouse double tap

When the map is double-tapped using mouse, the zoom in operation is performed. 

{% include image.html url="/js/Maps/User-Interaction_images/User-Interaction_img2.png" Caption="Map with zoom"%}

###Using Shape Selection

Map shape is zoomed to the whole map area, on the shape selected. Animation can be applied for that zooming, using the **enableAnimation** property as true. 

You can enable this feature by setting **enableZoomOnSelection** property value as ‘_True_’. 

When **enableZoomOnSelection** property is set to true, then, zoom on double click is muted.

{% highlight html %}

        jQuery(function($) {
            $("#mapContainer").ejMap({
                // ...
                zoomSettings:
                {
                     enableZoomOnSelection: true
                },
                // ...          
            });
        }); 

{% endhighlight %}

###Using Position

Depending on the latitude and longitude, you can zoom the map to the exact position. All locations are considered as latitude and longitude values and the exact location is considered as map coordinates.

The **navigateTo** is a method defined that allows you to zoom the map control to the given location. This method contains three attributes as follows.

_Attribute Table_

<table>
<tr>
<td>
<b>Attribute</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
Latitude</td><td>
Double</td><td>
Latitude point of the position </td></tr>
<tr>
<td>
Longitude</td><td>
Double</td><td>
Longitude point of the postion</td></tr>
<tr>
<td>
level</td><td>
Double</td><td>
Zoom level of the map</td></tr>
</table>


{% highlight html %}

    <script type="text/javascript">
        function buttonClick() {
            $("#map").ejMap("navigateTo", 13, 80, 5);
        }
    </script> 

{% endhighlight %}

 ##Panning

The panning feature enables map navigation. The **enablePan** property is used to enable or disable the panning support.

{% highlight html %}

        jQuery(function($) {
            $("#mapContainer").ejMap({
                // ...
                enablePan: true
                // ...          
            });
        }); 	

{% endhighlight %}

##Navigation Control

**Navigation** control is built-in with **Maps** control. With Navigation control, **Maps** can be panned in any direction and zoomed. It is possible to show or hide the NavigationControl by **enableNavigation** property.

###Structure of Navigation Control

{% include image.html url="/js/Maps/User-Interaction_images/User-Interaction_img3.png" Caption="Structure of Navigation Control"%}



{% highlight html %}

        jQuery(function($) {
            $("#mapContainer").ejMap({
                // ...
                navigationControl:{enableNavigation:true},
                // ...          
            });
        });	


{% endhighlight %}

###Zoom with Navigation Control

With Navigation control, the **Maps** can be zoomed. When you click on the ZoomIn button the Map is zoomed in and when you click on the ZoomOut button the Map is zoomed out.

###Panning with Navigation Control

Maps can be panned with Pan buttons (TopPan button, RightPan button, BottomPan button and LeftPan button). When you click on a particular Pan button the **Map** is panned on the respective directions.

###Navigation Control Positions

The Navigation control can be positioned in two ways.

* Absolute Position

* Dock Position

####Absolute Position

Based on the margin values of X and Y-axes, the navigation control can be positioned with the help of the **x** and **y** properties available in **absolutePosition**. For positioning the navigation control based on margins corresponding to a map, **dockPosition** value is set as _‘_none’.

####Dock Position

The navigation control can be positioned in following locations within the container.

* topLeft

* topCenter

* topRight

* centerLeft

* center

* centerRight

* bottomLeft

* bottomRight

* bottomCenter

* bottomRight

* none

You can set this option by using **dockPosition** property in **navigationControl**.****

{% highlight html %}

        jQuery(function($) {
            $("#mapContainer").ejMap({
                // ...
                navigationControl:{enableNavigation:true,orientation:'vertical',absolutePosition:{x:5,y:16},dockPosition:'none'},
                // ...          
            });
        }); 	


{% endhighlight %}



