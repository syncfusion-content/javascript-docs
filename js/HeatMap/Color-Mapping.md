---
layout: post
title: Create and configure color codes for heatmap value. 
description: How to configure colors codes for heatmap?
platform: js
control: ejHeatMap
documentation: ug
api: /api/js/ejheatmap
---

# Color Mapping

* Color mapping is used to indicate values as colors instead of numerical values. For example, if a HeatMap represents a data from 0 to 100. `ColorMapping` is used to specify a color for lower value and higher value. For any value between two values, a medium color will be automatically be chosen.

* You can set size for heatmap and heatmap legend using [width](/api/js/ejheatmaplegend#members:width "width") and [height](/api/js/ejheatmaplegend#members:height "height"),

* You can specify different color for range of data present in columns using heatmap [value](/api/js/ejheatmaplegend#members:colormappingcollection-value "value") and heatmap legend [color](/api/js/ejheatmaplegend#members:colormappingcollection-color "color") properties.

* The heatmap [label](/api/js/ejheatmaplegend#members:colormappingcollection-label "label") can be customized with [bold](/api/js/ejheatmaplegend#members:colormappingcollection-label-bold "bold"), [italic](/api/js/ejheatmaplegend#members:colormappingcollection-label-italic "italic"), [text](/api/js/ejheatmaplegend#members:colormappingcollection-label-text "text"), [textDecoration](/api/js/ejheatmaplegend#members:colormappingcollection-label-textdecoration "textDecoration"), [fontSize](/api/js/ejheatmaplegend#members:colormappingcollection-label-fontsize "fontSize"), [fontFamily](/api/js/ejheatmaplegend#members:colormappingcollection-label-fontfamily "fontFamily") and [fontColor](/api/js/ejheatmaplegend#members:colormappingcollection-label-fontcolor "fontColor") properties.


In color mapping, when white color is set to value 0 and red color is set for value 30, as shown below.

{% highlight js %}

var colorMappingCollection = [
    { value: 0, color: "#8ec8f8", label: { text: "0" } },
    { value: 100, color: "#0d47a1", label: { text: "100" } },
];

$("#heatmap").ejHeatMap({
    colorMappingCollection: colorMappingCollection
});

{% endhighlight %}

Resultant HeatMap will be as shown below.

![](Color-Mapping_images/Color-Mapping_img1.png)
 