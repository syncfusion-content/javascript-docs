---
layout: post
title: Gridlines
description: gridlines
platform: js
control: Diagram
documentation: ug
---

# Gridlines

**Gridlines** are the pattern of lines drawn behind diagram elements. It provides a visual guidance while dragging or arranging the objects on the Diagram surface.

## Customize the gridlines visibility

The `snapConstraints` property of `snapSettings` enables you to show/hide the gridlines. The following code snippet illustrates how to show or hide gridlines.

{% highlight js %}

//show both horizontal and vertical gridlines
var snapSettings = {
    snapConstraints: ej.datavisualization.Diagram.SnapConstraints.ShowLines
};

$(function() {
    $("#diagram").ejDiagram({
        width: "400px",
        height: "400px",
        snapSettings: snapSettings
    });
});

{% endhighlight %}

{% include image.html url="/js/Diagram/Gridlines_images/Gridlines_img1.png" %}

To show only horizontal/vertical gridlines or to hide gridlines refer [Constraints](/js/Diagram/Constraints "snapConstraints")

## Appearance

You can customize the appearance of the gridlines by using a set of predefined properties. To explore those properties,  refer [Gridlines](/js/api/diagram "snapSettings:horizontalGridLines")
The `horizontalGridLines` and `verticalGridLines` properties allows to customize the appearance of the gridlines. The following code snippet illustrates how to customize the appearance of gridlines.

{% highlight js %}

var snapSettings = {
    snapConstraints: ej.datavisualization.Diagram.SnapConstraints.ShowLines,
    // customize the line color and line style to the gridlines.
    horizontalGridLines: {
        lineColor: "blue",
        lineDashArray: "2  2"
    },
    verticalGridLines: {
        lineColor: "blue",
        lineDashArray: "2  2"
    }
};

$(function() {
    $("#diagram").ejDiagram({
        width: "400px",
        height: "400px",
        snapSettings: snapSettings
    });
});

{% endhighlight %}

{% include image.html url="/js/Diagram/Gridlines_images/Gridlines_img4.png" %}

### Line Intervals

Thickness and the space between gridlines can be customized using `linesInterval` property. In the linesInterval collections, values at the odd places are refered as the thickness of lines and the values at the even places are referred as the space between gridlines.

The following code snippet illustrates how to customize the thickness of lines and the line intervals.

{% highlight js %}

var snapSettings = {
    snapConstraints: ej.datavisualization.Diagram.SnapConstraints.ShowLines,
    horizontalGridLines: {
        // define the thickness and intervals for a pattern of lines
        linesInterval: [1.25, 14, 0.25, 15, 0.25, 15, 0.25, 15, 0.25, 15],
        lineColor: "blue",
        lineDashArray: "2  2"
    },
    verticalGridLines: {
        linesInterval: [1.25, 14, 0.25, 15, 0.25, 15, 0.25, 15, 0.25, 15],
        lineColor: "blue",
        lineDashArray: "2  2"
    }
};

$(function() {
    $("#diagram").ejDiagram({
        width: "400px",
        height: "400px",
        snapSettings: snapSettings
    });
});

{% endhighlight %}

{% include image.html url="/js/Diagram/Gridlines_images/Gridlines_img2.png" %}

# Snapping

## Snap To Lines

This feature allows diagram objects to snap to the nearest intersection of gridlines while being dragged or resized. This feature enables easier alignment during layout or design.

Snapping to gridlines can be enabled/disabled with the `snapConstraints` property of snapSettings. The following code snippet illustrates how to enable/disable the snapping to gridlines.

{% highlight js %}

//Enables snapping to both horizontal and vertical lines.
snapSettings = {
    snapConstraints: ej.datavisualization.Diagram.SnapConstraints.SnapToLines
};

$(function() {
    $("#diagram").ejDiagram({
        width: "400px",
        height: "400px",
        snapSettings: snapSettings,
    });
});

{% endhighlight %}

To enable/disable snapping to horizontal/vertical lines refer [Constraints] [/js/Diagram/Constraints "SnapConstraints"]

## Customization of Snap Intervals    

By default, the objects will be snapped towards the nearest gridline. The gridline or position, towards which the diagram object snaps, can be customized with the property `snapInterval`. The following code snippet illustrates how to customize the snap intervals.

{% highlight js %}

$("#diagram").ejDiagram({
    width: "400px",
    height: "400px",
    snapSettings: {
        horizontalGridLines: {
            //define a set of intervals to which the object will be snapped. 
            //In this example the object will be snapped to every 10px.
            snapInterval: [10]
        },
        verticalGridLines: {
            //The object will be snapped to every 10px.
            snapInterval: [10]
        },
        snapConstraints: ej.datavisualization.Diagram.SnapConstraints.All
    },
});

{% endhighlight %}

## Snap To Objects

The snap-to-object provides visual cues to assist with aligning and spacing diagram elements. A node can be snapped with its neighbouring objects based on certain alignments. Such alignments are visually represented as smart guides. 

The `enableSnapToObject` property allows you to enable/disable smart guides. The following code snippet illustrates how to enable/disable the smart guides.

{% highlight js %}

$("#diagram").ejDiagram({
    width: "400px",
    height: "400px",
    //Enable smart guides
    snapSettings: {
        enableSnapToObject: true
    },
});

{% endhighlight %}

{% include image.html url="/js/Diagram/Gridlines_images/Gridlines_img4.png" %}

