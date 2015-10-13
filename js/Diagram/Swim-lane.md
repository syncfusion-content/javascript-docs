---
layout: post
title: swim lane
description: swim lane
platform: js
control: Control Name undefined
documentation: ug
---


# Swim lane

Swim-lane diagrams are typically used to visualize the relationship between a business process and the department responsible for it by focusing on the logical relationships between activities. Swimlanes may be arranged either horizontally or vertically.

## Create a swimlane

To create a swimlane, you need to define an object with `isSwimlane` property that helps to identify the object as a swimlane. By default, the swimlanes will be arranged vertically. You can change that with the `orientation` property of swimlane.

The following code snippet illustrates how to define a swimlane object.

 {% highlight js %}
 
        var swimlane = {
            name: "swimlaneNode",
            
            //Change the orientation
            orientation: "horizontal",
            
            //Set the position and size
            offsetX: 400,
            offsetY: 200,
            height: 100,
            width: 700,
            
            //Set the type of object as swimlane
            isSwimlane: true
        };
{% endhighlight %}

Adding a swimlane to diagram is same as adding a node, You can add either through the `nodes` collection or through the client side method `add`. You can also drag and drop a swimlane from symbol palette.
For more information about adding a node/swimlane to diagram, refer [Add Nodes](/js/Diagram/Node "Create-Node").

Following code snippet illustrates how to add a swimlane to diagram through `nodes` collection.

{% highlight js %}
        $("#diagram").ejDiagram({
            nodes: [swimlane]
        });

{% endhighlight %}

{% include image.html url="/js/Diagram/Swim-lane_images/Swim-lane_img2.png" %}

## Headers

Swimlane allows to define a header to textually describe it. The `header` property of swimlane allows you to define its textual description(`text`) and to customize its appearance. Following code snippet illustrates how to define swimlane header.

{% highlight js %}

        //Define the header and format its text
        var header = {
            text: "Swimlane",            
            height: 50,
            fillColor: "#C7D4DF",
            fontColor: "black", fontSize: 11, fontFamily: "Arial",
            bold: true, italic: true, textDecoration: "underline"
        };
        
       //Initialize swimlane with header 
        var swimlane = {
            type: "swimlane",
            name: "swimlaneNode",
            orientation: "horizontal",
            offsetX: 400,
            offsetY: 200,
            height: 100,
            width: 700,
            isSwimlane: true,
            
            //Define header
            header:header
        };

        $("#diagram").ejDiagram({
            nodes: [swimlane],
        });
        
        //To update the swimlane header at runtime
        var diagram = $("#diagram").ejDiagram("instance");
        diagram.updateNode("swimlaneName", { header: {fontColor:"white"} })

{% endhighlight %}

{% include image.html url="/js/Diagram/Swim-lane_images/Swim-lane_img3.png" %}

### Update Header

Swimlane headers can be updated at runtime with the client side method `updateNode`. The following code snippet illustrates how to update a lane's header at runtime.

{% highlight js %}
  
     var diagram = $("#diagram").ejDiagram("instance");
     
     //Define the header and format its text
        var header = {            
            text: "swimlane",
            bold: true,
            italic: true
        };
        
     diagram.updateNode("swimlane", { header: header });

{% endhighlight %}

### Disable headers

You can hide the swimlane headers. Following code snippet illustrates how to hide headers.

{% highlight js %}

        var header = {
            text: "Swimlane",  
            //Set "0" to hide header          
            height: 0
        };

{% endhighlight %}

## Lane 
 
Lane is a functional unit or a responsible department of a business process that helps to map a process within the functional unit or in between other functional units. 
You can add any number of lanes to a swimlane and the lanes will be automatically stacked inside a swimlane based on the order in which they are added.

### Create an empty lane

To create an empty lane, you need to define an object with `isLane` property, that helps to identify the object as a lane. The following snippet illustrates how to define a swimlane with a lane.

{% highlight js %}
 
        //Define an empty lane   
        var lane = {
            name: "lane1",
            fillColor: "#f5f5f5",
            height: 120,
            
            //Set the object as Lane
            isLane:"true"
        };
        
       //Initialize swimlane with a header and a lane
        var swimlane = {
            type: "swimlane",
            name: "swimlaneNode",
            orientation: "horizontal",
            offsetX: 400,
            offsetY: 200,
            height: 100,
            width: 700,
            isSwimlane: true,
            
            //Define header - header defined in the headers section
            header:header,
            
            //Define lanes collection
            lanes: [lane]
        };

{% endhighlight %}

### Create a lane with header

The `header` property of the lane allows you to textually describe the lane(`text`) and to customize the appearance of the description. The following code snippet illustrates the how to define a lane header.
You can limit the size of a lane with its `minWidth`, `minHeight`, `maxWidth` and `maxHeight` properties.

 {% highlight js %}
 
       //Define the lane header
        var laneHeader = {
            text: "swimlane label",
            fillColor: "#C7D4DF",
            fontColor: "black", fontSize: 15, fontFamily: "Arial",
            bold: false, italic: false, textDecoration: "none"
        };

        //Initialize the lane
        var lane = {
            name: "lane1",
            fillColor: "#f5f5f5",
            height: 120,
            isLane: true,
            
            //Specify the lane header
            header: laneHeader,
            
            //Specify the minimum and maximum size of the lane
            minWidth: 500,
            maxWidth: 700,
            minHeight: 120,
            maxHeight: 200,
        };
        
        //Add lanes to swimlane
        var swimlane = {
            type: "swimlane",
            name: "swimlaneNode",
            orientation: "horizontal",
            offsetX: 400,
            offsetY: 200,
            height: 100,
            width: 700,
            isSwimlane: true,
            //Define header - header defined in the headers section
            header:header,
            //Add lanes to swimlane
            lanes: [lane]
        };

{% endhighlight %}

#### Disable/Update header

You can disable/update the lane header at runtime with the client side method `updateNode`. The following code snippet illustrates how to disable the lane header at run time.

{% highlight js %}
 
     var diagram = $("#diagram").ejDiagram("instance");
     
     //Set "0" to hide header
     diagram.updateNode("laneName", { header: {height: 0} })

{% endhighlight %}

### Add nodes to a lane

To add nodes to a lane, You need to add them to the `children` collection of lane. The following code snippet illustrates the how to add nodes to a lane.

{% highlight js %}
        
        //Define children of lane
        var children = [
        {
            name: "node",
            width: 70,
            height: 30,
            labels: [{
                text: "Node",
            }],
            // specifies the margin values of the child
            marginLeft: 70,
            marginTop: 1
        }];

        //Initialize the lane
        var lane = {
            name: "lane1",
            fillColor: "#f5f5f5",
            height: 120,
            isLane: true,
            
            //Define header - as above snippet
            header: laneHeader,
            
            //Add nodes to lane
            children:children,
            
            //Specifies the minimum and maximum size of the lane
            minWidth: 500,
            maxWidth: 700,
            minHeight: 120,
            maxHeight: 200,
        };
        
        //Add lanes to swimlane
        var swimlane = {
            type: "swimlane",
            name: "swimlaneNode",
            orientation: "horizontal",
            offsetX: 400,
            offsetY: 200,
            height: 100,
            width: 700,
            isSwimlane: true,
            //Define header - header defined in the headers section
            header:header,
            //Add lanes to swimlane
            lanes: [lane]
        };

{% endhighlight %}

{% include image.html url="/js/Diagram/Swim-lane_images/Swim-lane_img4.png" %}

## Phase 

Phases are the sub-processes that are used to break the swimlane into multiple smaller regions.

### Add phase

To define a phase, you have to set the length of the region to the `offset` property of phase. Every region can be textually described with the `label` property of phase.

The following snippet illustrates how to add a phase on initializing swimlane.

 {% highlight js %}

        //create a phase  
        var phase1 = {
            name: "Phase1",
            
            //Length of the first region
            offset: 300,
            
            //Initializes labels for phases
            label: { text: "Phase1" },
            
            //Specify the appearance of separator
            lineWidth: 1,
            lineDashArray: "3,3",
            lineColor: "#606060"
        };

        var phase2 = {
            name: "Phase2",
            label: { text: "Phase2" }
        };

        var swimlane = {
                type: "swimlane",
                name: "swimlaneNode",
                orientation: "horizontal",
                offsetX: 400, offsetY: 200,
                height: 100,width: 500,
                
                //Initialize the phase collection
                phases: [phase1, phase2],       
               
                //Add lanes and header as mentioned in header and lane section
                lanes: [lane],
                header: header
        };


{% endhighlight %}

{% include image.html url="/js/Diagram/Swim-lane_images/Swim-lane_img5.png" %}

### Add phase at runtime

You can add a region at runtime with the client side method `addPhase`. The following code snippet illustrates how to add a phase at runtime. 

 {% highlight js %}
 
         var phase = {
            name: "Phase3",
            label: { text: "Phase3" }
        };
        
        var diagram = $("#diagram").ejDiagram("instance");
        diagram.addPhase("swimlaneName", phase);

{% endhighlight %}

A phase can be updated at runtime with the client side API `updateNode`. Following code snippet illustrates how to a update phase at runtime.

 {% highlight js %}
 
        var diagram = $("#diagram").ejDiagram("instance");
        var options = {
            //specifies the style of the phase to be updated
            lineDashArray: "3,3",
            lineColor: "#C7D4DF",
            lineWidth: 2
        }
        diagram.updateNode("phaseName", options);

{% endhighlight %}

N> A default phase will be added, when the phase collection of the swimlane is empty. If the phase collection is initialized, a default phase will be appended at the end of swimlane.

## Limitations

* You cannot add connectors as the children of lanes. 