---
layout: post
title: Swim-lane
description: swim lane 
platform: js
control: Diagram
documentation: ug
---

# Swim lane 

Swim-lane diagrams are typically used to visualize a relationship between a business process and the department responsible for it by focusing on the logical relationships between activities. Swim lanes may be arranged either horizontally or vertically.

{% include image.html url="/js/Diagram/Swim-lane_images/Swim-lane_img1.png" %}

The following steps illustrates how to create a simple **swim lane**.

## Creating a Swim Lane 
Creating a swim lane is as simple as adding a node with some nested properties. Just add an object in the node's collection with the type as swimlane and specify its name, orientation, size, and position. The swim lane cannot be blank; therefore, lanes and phases have to be added.
{% highlight js %}
var swimlane = {
      
      // Type is used to identify which kind of node is added in the diagram.
      type: "swimlane",
      
      // Name is used as a unique identifier of the object.
      name: "swimlaneNode",
      
      // Orientation is used to set the orientation.
      orientation: "horizontal",
      
      // These specify the swim lane's dimensions.
      offsetX: 400,
      offsetY: 200,
      height: 100,
      width: 700,
}
{% endhighlight %}
## Adding Lanes 
Any number of lanes can be added by using the lanes collection, as shown in the following code. To visualize the lanes, each lane's size and color have to be specified.
{% highlight js %}
var swimlane = {
    type: "swimlane",
    //...

    // Adds lanes by using the lanes collection.
    lanes: [{
        name: "lane1",
        fillColor: "#f5f5f5",
        height: 120
    }]
}
{% endhighlight %}
## Adding Phases 
Any number of phases can be added by using the phases collection, as shown in the following code. Offset is used to define the phase's distance from the left side of the lane or from the previous phase.
{% highlight js %}
var swimlane = {
    type: "swimlane",
    //...

    // Adds phases by using the phases collection.
    phases: [{
        name: "phase1",
        offset: 300,
    }]
}
{% endhighlight %}
## Specifying headers 
By using the `header` property, headers can be added to `lanes` and `phases` of the swim lane.
{% highlight js %}
var swimlane = {
    type: "swimlane",
    name: "swimlaneNode",
    orientation: "horizontal",
    offsetX: 400,
    offsetY: 200,
    height: 100,
    width: 700,

    //Initializes swim-lane header.
    header: {
        text: "Swimlane",
        height: 50,
        fillColor: "#C7D4DF",
        fontSize: 11
    },

    lanes: [{
        name: "lane1",
        fillColor: "#f5f5f5",
        height: 120,

        //Initializes lane header.
        header: {
            text: "Lane",
            width: 50,
            fillColor: "#C7D4DF",
            fontSize: 11
        }
    }],

    phases: [{
        name: "Phase1",
        offset: 300,
        //Initializes labels for phases.
        label: { text: "Phase1" }
    }, {
        name: "Phase2",
        label: { text: "Phase2" }
    }]
}
{% endhighlight %}
The following screenshot is the swim lane generated from the example code.
{% include image.html url="/js/Diagram/Swim-lane_images/Swim-lane_img2.png" %}

## Adding Nodes into the Lane 
Now that the overall swim-lane skeleton is ready, add a node into the lane programmatically.
{% highlight js %}
var swimlane = {
    type: "swimlane",
    //...
    lanes: [{
        //... 
        // Adds a node into a lane.
        children: [{
            name: "node1",
            labels: [{ text: "Node", fontSize: 11 }],
            marginLeft: 70,
            marginTop: 1,
        }],
    }]
}
{% endhighlight %}
After adding a `node` into a `lane`, the swim lane will display as follows.
{% include image.html url="/js/Diagram/Swim-lane_images/Swim-lane_img3.png" %}
Nodes can also be added into the `lanes` interactively by dropping nodes from the palette. Similarly `connectors` can also be added using `lane`'s `children` or from palette.