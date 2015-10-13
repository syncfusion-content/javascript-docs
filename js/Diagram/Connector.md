---
layout: post
title: Connector
description: connector
platform: js
control: Diagram
documentation: ug
---

# Connector

Connectors are objects used to create link between two points, nodes or ports to represent the relationships between them. 

{% include image.html url="/js/Diagram/Connector_images/Connector_img1.png"%}

## Create Connector

Connector can be created by defining the start and end points. The path to be drawn can be defined with a collection of segments.
To explore the properties of a connector, refer [Connector Properties](/js/api/ejDiagram "members:connectors").

### Add connectors through connectors collection

The `sourcePoint` and ` targetPoint` properties of connector allows you to define the end points of a connector. Following code snippet illustrates how to add a connector through connector collection.

{% highlight js %}

    //Create connector
    var connectors = [
        // Define JSON
        {
            //Name of the connector
            name: "connector",

            //Set source and target points 
            sourcePoint: {
                x: 100,
                y: 100
            },
            targetPoint: {
                x: 200,
                y: 200
            }
        }
    ];

    //Initialize Diagram
    $("#DiagramContent").ejDiagram({
        //Assign connectors collection to diagram
        connectors: connectors
    });

{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img2.png"%}

### Add connector at run time

Connectors can be added at runtime with the client side method `add`. Following code snippet illustrates how to add connector at runtime.

{% highlight js %}

    // Define JSON
    var connector = {
        name: "connector",
        sourcePoint: {
            x: 100,
            y: 100
        },
        targetPoint: {
            x: 200,
            y: 200
        }
    };
    var diagram = $("#DiagramContent").ejDiagram("instance");
    // Add to diagram
    diagram.add(connector);

{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img3.png"%}

### Connectors from palette

Connectors can be predefined and added to symbol palette. You can drop those connectors into diagram when needed.

For more information about adding connectors from symbol palette, refer [Symbol Palette](/js/Diagram/Symbol-Palette).

### Connectors through data source

Connectors will be automatically generated based on the relationships defined through data source.
The default properties for these connectors will be fetched from default settings. 

For more information about data source, refer [Data Binding](/js/Diagram/Data-Binding).

### Draw connectors

Connectors can be interactively drawn by clicking and dragging on diagram surface using **DrawingTool**. For more information about drawing connectors, refer [Draw Connectors](/js/Diagram/Tools "Drawing-Tools:Connectors").

### Update Connector at runtime
     
The client side method `updateConnector` is used to update the connectors at run time. Following code snippet illustrates how to update a connector at runtime.

{% highlight js %}

    var diagram = $("#DiagramContent").ejDiagram("instance");
    diagram.updateConnector("connectorName", {
                lineColor: "#1BA0E2",
                lineWidth: 5,
                lineDashArray: "5,5"
            });
            
{% endhighlight %}

## Connect nodes

The `SourceNode` and `targetNode` properties allow to define the nodes that have to be connected. Following snippet illustrates how to connect two nodes.

{% highlight js %}

// Define JSON to create tasks
var task1 = { name: "task1", offsetX: 200, offsetY: 200, labels: [{ text: "Task 1" }] };
var task2 = { name: "task2", offsetX: 400, offsetY: 200, labels: [{ text: "Task 2" }] };

//Add tasks to nodes collection
var nodes = [
     task1,
     task2
  ];

var connectors = [
   //Define JSON
   {
      //Name of the connector
      name: "flow1",

      //Name of the source and target nodes
      sourceNode: "task1",      
      targetNode: "task2"

   }];
   
$("#DiagramContent").ejDiagram({
        //Set nodes collection to diagram model
        nodes: nodes,

        //Set connectors collection
        connectors: connectors,

        //Define the properties that carries the common values
        defaultSettings: {
            //Define the common values for the nodes
            node: {
                width: 100,
                height: 50,
                fillColor: "darkCyan",
                borderColor: "black",
                type: ej.datavisualization.Diagram.Shapes.Flow,
                shape: ej.datavisualization.Diagram.FlowShapes.Process,
                labels: [{ fontColor: "white" }]
            }
        }
    });

{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img4.png"%}

N> By default, connections will be created at the intersecting point of segments and node bounds. If connection needs to be created in between any specific points of source and target nodes, it can be achieved with connection ports. 

### Connections with ports

The `sourcePort` and `targetPort` properties allows to create connections between some specific points of source/target nodes. 
Following code snippet illustrates how to create port to port connections.


{% highlight js %}

    //Define ports for task2 
    var ports = [
      { name: "in", offset: { x: 1, y: 0.65 }, shape: "circle", visibility: "visible",  
        fillColor: "black" },
      { name: "out", offset: { x: 1, y: 0.35 }, shape: "circle", visibility: "visible",  
        fillColor: "black" }
    ];

    // Define JSON to create tasks
    var task1 = { name: "task1", offsetX: 350, offsetY: 300, labels: [{ text: "Task 1" }] };
    var task2 = { name: "task2", offsetX: 200, offsetY: 250, labels: [{ text: "Task 2" }],   
     // Add ports to node
     ports: ports };
    var task3 = { name: "task3", offsetX: 350, offsetY: 200, labels: [{ text: "Task 3" }] };

    //Add tasks to nodes collection
    var nodes = [task1, task2, task3];
    var connectors = [
        {
            name: "flow1", sourceNode: "task1", targetNode: "task2",
            //Name of the target port that is defined in target node
            targetPort: "in"
        },
        {
            name: "flow2", sourceNode: "task2", targetNode: "task3",
            //Name of the source port that is defined in source node
            sourcePort: "out"
        }];

     $("#DiagramContent").ejDiagram({
        //Set nodes collection to diagram model
        nodes: nodes,

        //Set connectors collection
        connectors: connectors,

        //Define the properties that carries the common values
        defaultSettings: {
            //Define the common values for the nodes
            //Define common values for connectors
            connector: { segments: [{ type: "orthogonal" }] }
        }
    });

{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img5.png"%}

## Segments

The path of the connector is defined with a collection of segments. There are three types of segments.

### Straight

Straight segment allows to create a straight line. 
To create a straight line, you have to add a straight segment to `segments` collection of connector and the `type` of the segment should be specified as "straight". Following code snippet illustrates how to create a default straight segment.

{% highlight js %}

    //Define JSON
    var connector = {
        name: "connector",
        sourcePoint: { x: 100, y: 100 },
        targetPoint: { x: 200, y: 200 },

        //Define segment collection
        segments: [
            {
                //If there is no previous segment, line will start from source point
                //If the end point is not specified, line will end at target point
                //Define the type of the segment
                type: "straight"
            }]
    };
    connectors.push(connector);

{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img6.png"%}

The `point` property of straight segment allows you to define the end point of it. Following code snippet illustrates how to define the end point of a straight segment.

{% highlight js %}

    var connectors = [];
    //Define JSON
    var connector = {
        name: "connector",
        sourcePoint: { x: 100, y: 100 },
        targetPoint: { x: 200, y: 300 },

        //Define segment collection
        segments: [
            {
                // Define the type of the segment
                type: "straight",
                // Define the end point of the segment
                point: { x: 100, y: 200 }
                //An additional straight line will be drawn from this end point to the target point
            }]
    };
    connectors.push(connector);

{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img7.png"%}

### Orthogonal

Orthogonal segments are used to create segments that are perpendicular to each other. 

You need to set the segment `type` as "othogonal" to create a default orthogonal segment. Following code snippet illustrates how to create a default orthogonal segment.

{% highlight js %}

    var connectors = [];
    //Define JSON
    var connector = {
        name: "connector",
        sourcePoint: { x: 100, y: 100 },
        targetPoint: { x: 200, y: 200 },
        //Define segment collection
        segments: [
            {
                // Define the type of the segment
                type: "orthogonal"
            }]
    };
    connectors.push(connector);

{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img8.png"%}

The `length` and `direction` properties allow to define the flow and length of segment. Following code snippet illustrates how to create customized orthogonal segments.

{% highlight js %}

    var connectors = [];
    //Define JSON
    var connector = {
        name: "connector",
        sourcePoint: { x: 100, y: 100 },
        targetPoint: { x: 200, y: 200 },
        //Define segment collection
        segments: [
            {
                // Orthogonal segment of 50px length to the bottom
                type: "orthogonal",
                length: 50,
                direction: "bottom"
                // An additional orthogonal segment will be added from the end of the   
                 last segment to the target point
            }]
    };
    connectors.push(connector);

{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img9.png"%}

#### Avoid overlapping

Orthogonal segments will be automatically re-routed, in order to avoid overlapping with the source and target nodes. Following images illustrate how orthogonal segments are re-routed. 

{% include image.html url="/js/Diagram/Connector_images/Connector_img10.png"%}

{% include image.html url="/js/Diagram/Connector_images/Connector_img11.png"%}

N> Overlapping with source and target nodes only will be avoided. Other nodes will not be considered as obstacles.

### Bezier

Bezier segments are used to create curve segments and the curves are configurable either with the control points or with vectors.

To create a bezier segment, the `type` property of segment needs to be set as "bezier". Following code snippet illustrates how to create a default Bezier segment.

{% highlight js %}

    var connectors = [];
    //Define JSON
    var connector = {
        name: "connector",
        sourcePoint: { x: 100, y: 100 },
        targetPoint: { x: 200, y: 200 },
        //Define segment collection
        segments: [
            {
                // Define the type of the segment
                type: "bezier"
            }]
    };
    connectors.push(connector);

{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img12.png"%}

The `point1` and `point2` properties of bezier segment enable you to set the control points. Following code snippet illustrates how to configure the Bezier segments with control points.

{% highlight js %}

    var connectors = [];
    //Define JSON
    var connector = {
        name: "connector",
        sourcePoint: { x: 100, y: 200 },
        targetPoint: { x: 250, y: 200 },
        //Define segment collection
        segments: [
            {
                // Define the type of the segment
                type: "bezier",
                // First control point – 
                // an absolute position from the page origin
                point1: { x: 125, y: 75 },
                // Second control point – 
                // an absolute position from the page origin
                point2: { x: 225, y: 75 }
            }]
    };
    connectors.push(connector);
    
{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img13.png"%}


The `vactor1` and `vector2` properties of bezier segment enable you to define the vectors. Following code illustrates how to configure a bezier curve with vectors.

{% highlight js %}

    //Define JSON
    var connector = {
        name: "connector",
        sourcePoint: { x: 100, y: 200 },
        targetPoint: { x: 250, y: 200 },
        //Define segment collection
        segments: [
            {
                // Define the type of the segment
                type: "bezier",
                // Length and angle between the source point and the first control point
                vector1: { angle: 270, distance: 75 },
                // Length and angle between the target point and the second control point
                vector2: { angle: 270, distance: 75 }
            }]
    };
    connectors.push(connector);
    
 {% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img14.png"%}

### Complex segments

Multiple segments can be defined one after another. To create a connector with multiple segments, you need to define and add the segments to`segments` collection of connector. Following code snippet illustrates how to create a connector with multiple segments.

{% highlight js %}

    var connectors = [];
    //Define JSON
    var connector = {
        name: "connector",
        sourcePoint: { x: 100, y: 200 },
        targetPoint: { x: 250, y: 300 },
        //Define segment collection
        segments: [
            {
                // Segment of length 100px to the bottom
                type: "orthogonal",
                length: 150,
                direction: "bottom"
            },
            {
                //Defines a segment of 150px length to the right
                type: "orthogonal",
                direction: "right",
                length: 150
            }
            //An additional orthogonal segment will be added from the end of the last segment to the target point
        ]
    };
    connectors.push(connector);
    
{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img15.png"%}

## Decorator

Start and end points of a connector can be decorated with some customizable shapes like arrows, circles, diamond or path. You can decorate the connection end points with the `sourceDecorator` and `targetDecorator` properties of connector.
To explore the properties of decorators, refer [Decorator Properties](/js/api/ejDiagram "members:connectors-sourceDecorator").

The `shape` property of decorator allows to define the shape of the decorators. Following code snippet illustrates how to create decorators of various shapes.

{% highlight js %}

    var DecoratorShapes = ej.datavisualization.Diagram.DecoratorShapes;
    var connectors = [];
    //Define JSON
    var connector = {
        name: "connector", sourcePoint: { x: 100, y: 100 }, 
        targetPoint: { x: 200, y: 200 },
        // Decorator shape- circle
        sourceDecorator: {
            shape: DecoratorShapes.Circle,
            width: 10, height: 10
        },

        // Decorator shape - Arrow
        targetDecorator: {
            shape: DecoratorShapes.Arrow, 
            width: 10, height: 10
        }
    };
    connectors.push(connector);

    var connector2 = {
        name: "connector2", sourcePoint: { x: 300, y: 100 }, 
        targetPoint: { x: 400, y: 200 },
        // Decorator shape - Open arrow
        sourceDecorator: {
            shape: DecoratorShapes.Diamond, 
            width: 10, height: 10
        },

        // Decorator shape - Diamond
        targetDecorator: {
            shape: DecoratorShapes.OpenArrow, 
            width: 10, height: 10
        }
    };
    connectors.push(connector2);

    var connector3 = {
        name: "connector3", sourcePoint: { x: 500, y: 100 },  
        targetPoint: { x: 600, y: 200 },

        // Decorator shape - Path
        targetDecorator: {
            shape: DecoratorShapes.Path,
            pathData: "M 376.892,225.284L 371.279,211.95L 376.892,198.617L 350.225,211.95L 376.892,225.284 Z"
        }
    };
    connectors.push(connector3);

{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img16.png"%}

## Padding

Padding is used to leave space between the Connector's end point and the object to which it is connected.

The `sourcePadding` and `targerPadding` properties of connector define the space to be left between the connection end points and the source and target nodes of connector. Following code snippet illustrates how to leave space between the connection end points and source, target nodes.

{% highlight js %}

// Define JSON to create tasks
    var task1 = { name: "task1", offsetX: 200, offsetY: 200, labels: [{ text: "Task 1" }] };
    var task2 = { name: "task2", offsetX: 400, offsetY: 200, labels: [{ text: "Task 2" }] };

    //Add tasks to nodes collection
    var nodes = [
        task1,
        task2
    ];

    var connectors = [
        //Define JSON
        {
            name: "flow1", sourceNode: "task1", targetNode: "task2",
            // Space between source point and source object
            sourcePadding: 5,
            // Space between target point and target object
            targetPadding: 10
        }];

{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img17.png"%}

The `connectorPadding` property of node defines the space to be left between the node bounds and its edges. Following code snippet illustrates how to leave space between a node and its connections.

{% highlight js %}

    // Define JSON to create tasks
    var task1 = {
        name: "task1", offsetX: 200, offsetY: 200, labels: [{ text: "Task 1" }],
        //Space between the node and its edges
        connectorPadding: 5
    };

    var task2 = { name: "task2", offsetX: 400, offsetY: 200, labels: [{ text: "Task 2" }] };

    //Add tasks to nodes collection
    var nodes = [
        task1,
        task2
    ];
    var connectors = [
        //Define JSON
        {
            name: "flow1", sourceNode: "task1", targetNode: "task2"
        }];

{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img18.png"%}

The `connectorPadding` property of port defines the space between the ports and its in/out edges. Following code snippet illustrates how to leave space between ports and its connections.

{% highlight js %}

// Define JSON to create tasks
    var ports = [{
        name: "port", offset: { x: 0, y: 0.5 }, shape: "circle",
        visibility: "visible", fillColor: "black",
        //space between port and its edges
        connectorPadding: 5
    }];

    var task1 = { name: "task1", offsetX: 200, offsetY: 200, labels: [{ text: "Task 1" }] };
    var task2 = { name: "task2", offsetX: 400, offsetY: 200, labels: [{ text: "Task 2" }], ports: ports };

    //Add tasks to nodes collection

    var nodes = [
        task1,
        task2
    ];

    var connectors = [
        //Define JSON
        {
            name: "flow1", sourceNode: "task1", targetNode: "task2",
            targetPort: "port"
        }];

{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img19.png"%}

## Bridging

Line Bridging creates a bridge for lines to smartly cross over other lines, at points of intersection. When two line connectors meet each other, the line with the higher z-order (upper one) draws an arc over the underlying connector. 
Bridging can be enabled/disabled either with the `constraints` property of connector or with diagram `constraints`. Following code snippet illustrates how to enable line bridging.

{% highlight js %}

var Diagram = ej.datavisualization.Diagram;

//Enable briding for a single connector
    var connector = {    
        name: "connector1", sourcePoint: { x: 100, y: 100 }, 
        targetPoint: { x: 200, y: 200 },
        constraints: Diagram.ConnectorConstraints.Default
// Remove inherit bridging or else bridging will be enabled/disabled based on diagram constraints
         & ~Diagram.ConnectorConstraints.InheritBridging
//Include bridging
         | Diagram.ConnectorConstraints.Bridging    };    

//Enable bridging for every connector added in the model
    $("#DiagramContent").ejDiagram({
        constraints: Diagram.DiagramConstraints.Default |   
        Diagram.DiagramConstraints.Bridging
    });    
{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img20.png"%}

The direction of the bridge can be customized with the property `bridgeDirection`. bridgeDirection defines in which intersecting segment, the bridge has to be inserted. By default, the bridge direction will be top.

To explore the bridge directions, refer [Bridge Directions](/js/Diagram/Interaction "Connection-Editing").

Following code snippet illustrates how to draw the bridge at the bottom direction.

{% highlight js %}

    var DiagramConstraints= ej.datavisualization.Diagram.DiagramConstraints;   

    $("#DiagramContent").ejDiagram({
        //Set the bridge direction
        bridgeDirection: "bottom",
        //Enable bridging
        constraints:DiagramConstraints.Default | DiagramConstraints.Bridging
    });

{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img21.png"%}

**Limitation**: Bezier segments do not support bridging.

## Corner radius

Corner radius allows to create connectors with rounded corners. The radius of the rounded corner is set with `cornerRadius` property.

{% highlight js %}
    // Define JSON to create tasks
    var task1 = { name: "task1", offsetX: 200, offsetY: 200, labels: [{ text: "Task 1" }] };
    var task2 = { name: "task2", offsetX: 350, offsetY: 300, labels: [{ text: "Task 2" }] };

    //Add tasks to nodes collection
    var nodes = [
        task1,
        task2
    ];

    var connectors = [
        //Define JSON
        {
            name: "flow1", sourceNode: "task1", targetNode: "task2",
            //Set the radius for the rounded corner
            cornerRadius: 10
        }];
        
{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img22.png"%}

## Appearance

Stroke width, stroke color and style of the lines and decorators can be customized with a set of defined properties.

### Segment Appearance

Following code snippet illustrates how to customize the segment appearance.

{% highlight js %}

    //Customize the appearance of the connector
    var connectors = [{
        name: "connector",
        sourcePoint: { x: 100, y: 100 },
        targetPoint: { x: 200, y: 200 },
        //stroke width of the line
        lineWidth: 2,
        //stroke color 
        lineColor: "green",
        //line style 
        lineDashArray: "2,2",
        //opiquity of the line
        opacity: 0.8,
        //defined in the decorator appearance section
        targetDecorator: targetDecorator
    }];
    
 {% endhighlight %}   
 
### Decorator Appearance

Following code snippet illustrates how to customize the appearance of the decorator.

{% highlight js %}
//Customize the appearance of decorator    

 var targetDecorator = {
        //define the shape
        shape: ej.datavisualization.Diagram.DecoratorShapes.Arrow,
        //fill color of the decorator
        fillColor: "red",
        //stroke color
        borderColor: "green",
        //stroke width
        borderWidth: 2,
        width: 10,
        height: 10
    };
{% endhighlight %}

{% include image.html url="/js/Diagram/Connector_images/Connector_img23.png"%}

## Interaction
Diagram allows to edit the connectors at runtime. To edit the connector segments at runtime, refer [Connection Editing](/js/Diagram/Interaction "Connection-Editing").

## Constraints
The `constraints` property of connector allows to enable/disable certain features of connectors. For more information about constraints, refer [Connector Constraints](/js/Diagram/Constraints "ConnectorConstraints").