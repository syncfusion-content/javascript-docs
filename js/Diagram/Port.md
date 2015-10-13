---
layout: post
title: Port
description: port
platform: js
control: Diagram
documentation: ug
---

# Port

Essential Diagram for JS provides support to define custom ports for making connections.

{% include image.html url="/js/Diagram/Port_images/Port_img3.png" %}

When a connector is connected between two nodes, its end points will be automatically docked to node's nearest boundary as shown in the image below. 

{% include image.html url="/js/Diagram/Port_images/Port_img4.png" %}

Ports acts as the connection points of node and allows to create connections with only those specific points as shown in the image below.

{% include image.html url="/js/Diagram/Port_images/Port_img5.png" %}

## Create Port

### Add ports when initializing nodes

To add a connection port, you need to define the port object and add it to node's `ports` collection. The `offset` property of port accepts an object of fractions and used to determine the position of ports. The following code illustrates how to add ports when initializing the node.

{% highlight js %}

    var nodes = [{
        width: 100, height: 100,
        // Define a collection of ports
        ports: [    
            //Define JSON to create port    
           {    
            //Set the port name    
            name: "port1",    
            // Specifies the port offset – fraction value relative         
            to node bounds     
            offset: {    
                x: 0,    
                y: 0.5    
            },    
        }]    
    }];
    
    $("#diagram").ejDiagram({    
        // set the nodes to diagram model    
        nodes: nodes,    
    });
    
{% endhighlight %} 

### Add ports at runtime

You can add ports at runtime using the client side method `addPorts`. The following code illustrates how to add ports to node at runtime.

{% highlight js %}

    // Define a collection of ports that have to be added at runtime    
    var ports = [{    
        name: "port1",    
        // Specifies the port offset – fraction value relative         
        to node bounds – determines the position of port on node    
        offset: {    
            x: 0,    
            y: 0.5    
        }},    
        { name: "port2",offset: {x: 1,y: 0.5 }},    
        { name: "port3",offset: {x: 0.5,y: 0 }},    
        { name: "port4",offset: {x: 0.5,y: 1 }}        
    ];
    
    // Get the instance for diagram    
    var diagram = $("#diagram").ejDiagram("instance");    
    // Add the ports to the node of name "node"    
    diagram.addPorts("node", ports)

{% endhighlight %}

{% include image.html url="/js/Diagram/Port_images/Port_img1.png" %}

To explore the set of properties to define a port, refer [Port Properties](/js/api/ejDiagram "members:nodes-ports")

### Update Port at runtime
     
The client side API `updatePort` is used to update the ports at run time. The following code snippet illustrates how to change the port properties.

{% highlight js %}

    var diagram = $("#diagram").ejDiagram("instance");
    var selectedObject = diagram.model.selectedItems.children[0];
    var visibility = ej.datavisualization.Diagram.PortVisibility.Visible;
    diagram.updatePort(selectedObject.name, selectedObject.ports[0], { fillColor: "red", visibility: visibility });

{% endhighlight %}

## Connect with ports    

Connector’s 'sourcePort' and 'targetPort' properties allows to create connections between some specific points of source/target nodes. 
For more information about creating connections with port, refer [Connections with ports](/js/Diagram/Connector "Connections with ports")  

## Appearance 

You can change the shape of port using its `shape` property. To explore the different types of port shapes, refer [Port Shapes](/js/api/global "PortShapes").
The appearance of ports can be customized with a set of style specific properties. 

The following code illustrates how to change the appearance of port.

{% highlight js %}

    var ports = [{     
        // Specifies the port position    
        offset: {    
            x: 1,    
            y: 0.5    
        },
        //Define the shape of port     
        shape: ej.datavisualization.Diagram.PortShapes.Circle ,
                        
        //Specifies the port visibility     
        visibility: true,    
        
        //Customize the appearance    
        fillColor: "yellow",  
        size: 12,    
        borderColor: "black",      
        borderWidth: 2    
    }];
    
    var nodes = [{ name: "node", ports: ports }];
   
{% endhighlight %}

{% include image.html url="/js/Diagram/Port_images/Port_img2.png" %}

## Constraints

The `constraints` property allows to enable/disable certain behaviors of ports. For more information about port constraints, refer [Constraints](/js/Diagram/Constraints "Port Constraints")



















 