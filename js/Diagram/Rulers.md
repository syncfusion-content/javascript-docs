---
layout: post
title: Ruler is used to measure the distance of nodes and connectors from origin of the page.
description: how to measure the distance of Nodes and Connectors?
platform: js
control: Diagram
documentation: ug
api: /api/js/ejdiagram
---

# Rulers

The Ruler provides a Horizontal and Vertical guide for measuring in the Diagram control. The Ruler can be used to measure the Diagram objects, indicate positions, and align Diagram elements. This is especially useful in creating scale models. 

## Adding Rulers to the Diagram
Use the following code example to add the ruler to the Diagram.

{% highlight javascript %}

$("#diagram").ejDiagram({
    rulerSettings: {
        showRulers: true
    }
});

{% endhighlight %}

![](/js/Diagram/Rulers_images/Rulers_images1.png)

## Customizing the Ruler

By default, ruler segments are arranged based on measurement units.

Segment width, the textual description of the ruler segment, and the appearance of the ruler ticks can be customized. Use the following code example to customize the ruler.
 
{% highlight javascript %}

$("#diagram").ejDiagram({
    // Customizing the Ruler
    rulerSettings: {
        showRulers: true,
        //Customizing the horizontal ruler.
        horizontalRuler: {
            //Creating a custom segment with 6 intervals.
            interval: 6,
            // Customizing the ruler segment width.
            segmentWidth: 100,
            // Customizing the Ruler ticks.
            arrangeTick: "arrangeTick",
            // Customizing the Ruler ticks alignment.
            tickAlignment: ej.datavisualization.Diagram.TickAlignment.LeftOrTop,
            // Customizing the Ruler marker color
            markerColor: "blue",
            // Customizing the thickness of the ruler bar.
            thickness: 25
        },
        verticalRuler: {
            interval: 6,
            segmentWidth: 100,
            arrangeTick: "arrangeTick",
            tickAlignment: ej.datavisualization.Diagram.TickAlignment.LeftOrTop,
            markerColor: "blue",
            thickness: 25
        }
    }
});


function arrangeTick(args) {
	// Customizing the Ruler ticks.
    if (args.tickInterval % 100 == 0) {
    }
    else if (args.tickInterval % 50 == 0) {
        args.tickLength = 12.5
    }
}

{% endhighlight %}

![](/js/Diagram/Rulers_images/Rulers_images2.png)

