---
layout: post
title: Legend gives visual guideline for mapping between value and color.
description: How to create and configure legend for HeatMap
platform: js
control: HeatMapLegend
documentation: ug
---

# Legend

Legend is a control used to summarize the range of colors in HeatMap. This gives visual guideline for mapping between value and color.

##Create Legend

Legend can be created with color mapping as shown below.

{% highlight js %}

var colorMappingCollection = [
    { value: 0, color: "#fe0002", label: { text: "Poor" } },
    { value: 3, color: "#ffff01", label: { text: "Average" } },
    { value: 6, color: "#13ab11", label: { text: "Good" } },
    { value: 10, color: "#005ba2 ", label: { text: "Excellent" } }
];

$("#heatmap_legend").ejHeatMapLegend({
    colorMappingCollection: colorMappingCollection,
    height: "50px",
    width: "75%"
});

{% endhighlight %}

Resultant legend will be like following image.

![](Legend_images/Legend_img1.png)
 
##Legend Mode

There are two modes for Legend
* Gradient
* List

###Gradient:

{% highlight js %} 

$("#heatmap_legend").ejHeatMapLegend({
    colorMappingCollection: colorMappingCollection,
    height: "50px",
    width: "75%",
    legendMode: ej.HeatMap.LegendMode.Gradient   
});
        
{% endhighlight %}

![](Legend_images/Legend_img2.png)

###List:

{% highlight js %} 

$("#heatmap_legend").ejHeatMapLegend({
    colorMappingCollection: colorMappingCollection,
    height: "50px",
    width: "75%",
    legendMode: ej.HeatMap.LegendMode.List   
});
        
{% endhighlight %}

![](Legend_images/Legend_img3.png)

##Orientation

There are 2 types of Orientation, applicable for Gradient and List Mode 
* Horizontal
* Vertical

###Horizontal:

{% highlight js %} 

$("#heatmap_legend").ejHeatMapLegend({
    colorMappingCollection: colorMappingCollection,
    height: "50px",
    width: "75%",
    legendMode: ej.HeatMap.LegendMode.List   
});
        
{% endhighlight %}

![](Legend_images/Legend_img3.png)

###Vertical:

{% highlight js %} 

$("#heatmap_legend").ejHeatMapLegend({
    colorMappingCollection: colorMappingCollection,
    height: "550px",
    width: "100px",
    orientation: ej.HeatMap.LegendOrientation.Vertical,
    legendMode: ej.HeatMap.LegendMode.List
});
        
{% endhighlight %}

![](Legend_images/Legend_img4.png)