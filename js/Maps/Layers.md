---
layout: post
title: Layers
description: layers
platform: js
control: Maps
documentation: ug
---

# Layers

Map is maintained through Layers and it can accommodate one or more layers.

##Multilayers

The Multilayer support allows you to load multiple shape files in a single container, enabling maps to display more information.

###Loading Multiple Shape files in a Single Container

This feature allows the map to load multiple types of shape files in a single container.

###Adding Multiple Layers in the Map

The shape layers is the core layer of the map. The multiple layers can be added in the shape Layers as **subShapeFileLayers** within the shape Layers.

##SubLayer

The subLayer is the collection of shape Layers. 

In this example, World Map shape is used as shape data by utilizing the “**WorldMap.json**” file in the following folder structure obtained from downloaded Maps_GeoJSON folder.

..\ Maps_GeoJSON\

You can assign the complete contents in “**WorldMap.json**” file to new **JSON** object. For better understanding, a JS file “**WorldMap.js”** is already created to store **JSON** data in **JSON** object “usMap”****

**[usa.js]**

{% highlight js %}

    var world_map = //Paste all the content copied from the JSON file// 

{% endhighlight %}

{% highlight js %}

    jQuery(function ($) {
        $("#mapContainer").ejMap({
            layers: [
            {
                shapeData: world_map,
                shapeSettings: {
                    fill: "#9CBF4E",
                    strokeThickness: "0.5",
                    stroke: "White"
                },
                subLayers: [{
                    shapeData: usMap,
                    shapeSettings: {
                        fill: "orange",
                        strokeThickness: "1",
                        stroke: "White"
                    }
                }]
            }]
        });
    }); 


{% endhighlight %}


{% include image.html url="/js/Maps/Layers_images/Layers_img1.png" Caption="Map with layers"%}

