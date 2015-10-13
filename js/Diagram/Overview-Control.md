---
layout: post
title: Overview-Control
description: overview control
platform: js
control: Diagram
documentation: ug
---


# Overview Control

**Overview** control allows you to see a preview or an overall view, of the entire content of a diagram. This helps you to look at the overall picture of large diagram and also to navigate, pan or zoom, on a particular position of the page.

{% include image.html url="/js/Diagram/Overview-Control_images/Overview-Control_img1.png" %}

When you work on a very large diagram, you may not know the part you are actually working on, or navigation from one part to another, might be difficult. One solution for navigation is to zoom out of the entire diagram and find where you are. Then you can zoom in on to a particular area where you want to be. This solution is not suitable when you need some frequent navigation.

Overview control solves these problems by showing you a preview, that is, an overall view of the entire diagram. A rectangle indicates viewport of the diagram. Navigation becomes easy by dragging this rectangle.

## Create overview

The `sourceId` property of overview should be set with the corresponding diagram id for which you need the over all view. The following code illustrates how to create overview.  

{% highlight html %}

    <!--Initialize diagram element-->
    <div id="diagram"></div>;     
    
    <!-- Initialize overview element -->    
    <div id="overview"></div>;  
      
{% endhighlight %}
 
{% highlight js %}
    // initialize the diagram control    
    $("#diagram").ejDiagram({    
        width: "1020px",    
        height: "600px"    
    });
    
    // initialize the overview control    
    $("#overview").ejOverview({    
        // Relate diagram with overview     
        sourceID: "diagram",    
        width: "100%",    
        height: "100%"
    });

{% endhighlight %}

## Zoom and Pan

In overview, the view port of the diagram is highlighted with a red colored rectangle. Diagram can be zoomed/panned by interacting with that. You can interact with overview as follows. 

* Resize the rectangle - Zooms in/out the diagram
* Drag the rectangle - Pans the diagram
* Click at a position - Navigates to the clicked region
* Choose a particular region by clicking and dragging - Navigates to the specified region

Following image shows how the diagram is zoomed/panned with overview.
{% include image.html url="/js/Diagram/Overview-Control_images/Overview-Control_img2.png" %}