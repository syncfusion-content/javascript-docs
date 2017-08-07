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

The `Ruler` provides a Horizontal and Vertical guide for measuring in the Diagram control. The Ruler can be used to measure the Diagram objects, indicate positions, and align Diagram elements. This is especially useful in creating scale models. 

## Adding Rulers to the Diagram

Rulers can be enabled by setting the ruler Setting’s `showRulers` property for the diagram control.

Use the following code example to enable/disable the ruler to the Diagram.

{% highlight javascript %}

$("#diagram").ejDiagram({
    rulerSettings: {
        showRulers: true
    }
});

{% endhighlight %}

![](/js/Diagram/Rulers_images/Rulers_images1.png)

## Customizing the Ruler

The rulerSetting's `interval` property is used to define the number of tick's between two major stroke lines of the ruler. 

The ruler Setting’s `segmentWidth` is used to defines the space between the two major tick strokes.

The `arrangeTick` event will be triggered when each tick have been drawn.By using this event you can customize the length of the tick.

Use the following code example to customize the ruler's segment.

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
            arrangeTick: "arrangeTick"
        },
        verticalRuler: {
            interval: 6,
            segmentWidth: 100,
            arrangeTick: "arrangeTick"
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

The width of the ruler can be set through `thickness` property. If it’s an horizontal ruler, thickness will be taken as height of the ruler.

Tick alignment can be modified using `tickAlignment` as either `LeftOrTop` or `RightOrBottom`.

The `markerColor` property of the ruler is used to indicate the position of the mouse cursor.

Use the following code example to customize the ruler's tick.

{% highlight javascript %}

$("#diagram").ejDiagram({
    // Customizing the Ruler
    rulerSettings: {
        showRulers: true,
        //Customizing the horizontal ruler.
        horizontalRuler: {
            // Customizing the Ruler ticks alignment.
            tickAlignment: ej.datavisualization.Diagram.TickAlignment.LeftOrTop,
            // Customizing the Ruler marker color
            markerColor: "blue",
            // Customizing the thickness of the ruler bar.
            thickness: 25
        },
        verticalRuler: {
            tickAlignment: ej.datavisualization.Diagram.TickAlignment.LeftOrTop,
            markerColor: "blue",
            thickness: 25
        }
    }
}); 
{% endhighlight %}

![](/js/Diagram/Rulers_images/Rulers_images2.png)



