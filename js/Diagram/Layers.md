---
layout: post
title: Layers | Diagram | Javascript | Syncfusion
description: This section explains about how to control the set of specific nodes on the diagram page.
platform: js
control: Diagram
documentation: ug
api: /api/js/ejdiagram
---

# Layers

**Layer** is used to organize related shapes on a diagram control. A layer is a named category of shapes. By assigning shapes to different layers, we can selectively view, print, remove and lock different categories of shapes

[Layers](/api/js/ejdiagram#members:layers "layers") in diagram provide a way to change properties of all shapes that have been assigned to that layer. The following properties can be set.

* Visible
* Print 
* Active
* Lock  
* Objects 

## Visible 

The layer's [visible](/api/js/ejdiagram#members:layers-visible "visible") property is used to control the visibility of the elements assigned to the layer.

{% highlight javascript %}

        var nodes = [
            { name: "Ellipse1", width: 40, height: 40, offsetX: 100, offsetY: 100, shape: "ellipse" },
            { name: "Ellipse2", width: 40, height: 40, offsetX: 200, offsetY: 100, shape: "ellipse" },
            { name: "Ellipse3", width: 40, height: 40, offsetX: 100, offsetY: 300, shape: "ellipse" },
            { name: "Ellipse4", width: 40, height: 40, offsetX: 200, offsetY: 300, shape: "ellipse" }
        ];
        $("#diagram").ejDiagram({
            width: "100%",
            height: "600px",
            nodes: nodes,
            // control the visibility of the set of diagram elements
            layers: [
                { name: "Layer1", visible: true, objects: ["Ellipse1", "Ellipse2"] },
                { name: "Layer1", visible: false, objects: ["Ellipse3", "Ellipse4"] }
            ]
        });
{% endhighlight %}

## Print  

The layer's [print](/api/js/ejdiagram#members:layers-print "print") property is used to include or exclude the elements assigned to the layer when the diagram is printed.

Diagram layer provides the support to Include or exclude the shapes when the diagram is printed.

{% highlight javascript %}

        var nodes = [
            { name: "Ellipse1", width: 40, height: 40, offsetX: 100, offsetY: 100, shape: "ellipse" },
            { name: "Ellipse2", width: 40, height: 40, offsetX: 200, offsetY: 100, shape: "ellipse" },
            { name: "Ellipse3", width: 40, height: 40, offsetX: 100, offsetY: 300, shape: "ellipse" },
            { name: "Ellipse4", width: 40, height: 40, offsetX: 200, offsetY: 300, shape: "ellipse" }
        ];
        $("#diagram").ejDiagram({
            width: "100%",
            height: "600px",
            nodes: nodes,
            //  Include or exclude the shapes when the diagram is printed
            layers: [
                { name: "Layer1", print: true, objects: ["Ellipse1", "Ellipse2"] },
                { name: "Layer1", print: false, objects: ["Ellipse3", "Ellipse4"] }
            ]
        });
{% endhighlight %}

## Active  

The layer's [active](/api/js/ejdiagram#members:layers-active "active") property is used to automatically assign shapes to active layers when the shapes are added to the diagram.

{% highlight javascript %}

        var nodes = [
            { name: "Ellipse1", width: 40, height: 40, offsetX: 100, offsetY: 100, shape: "ellipse" },
            { name: "Ellipse2", width: 40, height: 40, offsetX: 200, offsetY: 100, shape: "ellipse" },
            { name: "Ellipse3", width: 40, height: 40, offsetX: 100, offsetY: 300, shape: "ellipse" },
            { name: "Ellipse4", width: 40, height: 40, offsetX: 200, offsetY: 300, shape: "ellipse" }
        ];
        $("#diagram").ejDiagram({
            width: "100%",
            height: "600px",
            nodes: nodes,
            // set the specific layer as active 
            layers: [
                { name: "Layer1", active: true },
                { name: "Layer1", active: false } 
            ]
        });
{% endhighlight %}

## Lock  

The layer's [lock](/api/js/ejdiagram#members:layers-lock "lock") property is used to prevent or allow changes to the elements dimension and position.

{% highlight javascript %}

        var nodes = [
            { name: "Ellipse1", width: 40, height: 40, offsetX: 100, offsetY: 100, shape: "ellipse" },
            { name: "Ellipse2", width: 40, height: 40, offsetX: 200, offsetY: 100, shape: "ellipse" },
            { name: "Ellipse3", width: 40, height: 40, offsetX: 100, offsetY: 300, shape: "ellipse" },
            { name: "Ellipse4", width: 40, height: 40, offsetX: 200, offsetY: 300, shape: "ellipse" }
        ];
        $("#diagram").ejDiagram({
            width: "100%",
            height: "600px",
            nodes: nodes,
            // prevent or allow changes to the shapes dimension and position
            layers: [
                { name: "Layer1", lock: true, objects: ["Ellipse1", "Ellipse2"] },
                { name: "Layer1", lock: false, objects: ["Ellipse3", "Ellipse4"] }
            ]
        });
{% endhighlight %}

 
## Objects  

The layer's [objects](/api/js/ejdiagram#members:layers-objects "objects") property is used to define the diagram elements to the layer.

{% highlight javascript %}

        var nodes = [
            { name: "Ellipse1", width: 40, height: 40, offsetX: 100, offsetY: 100, shape: "ellipse" },
            { name: "Ellipse2", width: 40, height: 40, offsetX: 200, offsetY: 100, shape: "ellipse" },
            { name: "Ellipse3", width: 40, height: 40, offsetX: 100, offsetY: 300, shape: "ellipse" },
            { name: "Ellipse4", width: 40, height: 40, offsetX: 200, offsetY: 300, shape: "ellipse" }
        ];
        $("#diagram").ejDiagram({
            width: "100%",
            height: "600px",
            nodes: nodes,
            // sets the set of objects will be assigned to specific layers.
            layers: [
                { name: "Layer1", lock: true, objects: ["Ellipse1", "Ellipse2"] },
                { name: "Layer1", lock: false, objects: ["Ellipse3", "Ellipse4"] }
            ]
        });
{% endhighlight %}

### Add layer at runtime

Layers can be added at runtime by using public method, [addLayers](/api/js/ejdiagram#methods:addLayers "addLayers"). 

The layer's [name](/api/js/ejdiagram#members:layers-name "name") property is used to define the name of the layer.

The following code illustrates how to add a layer.

{% highlight javascript %}

        // creating the instance for the diagram
        var diagram = $("#diagram").ejDiagram("instance");
        // creating the layer collection
        var layers = [{ name: "Layer1", visible: true, objects: ["Ellipse1", "Ellipse2"] }];
        // add the layers to the existing diagram layer collection
        diagram.addLayers(layers)

{% endhighlight %}

### Add node to layer at runtime

nodes can be added to layer at runtime by using public method, [addNodeToLayer](/api/js/ejdiagram#methods:addNodeToLayer "addNodeToLayer").  
 
The following code illustrates how to add a node to layer.

{% highlight javascript %}

        // creating the nodes
        var nodes = [
            { name: "Ellipse1", width: 40, height: 40, offsetX: 100, offsetY: 100, shape: "ellipse" },
            { name: "Ellipse2", width: 40, height: 40, offsetX: 200, offsetY: 100, shape: "ellipse" }
        ];
        $("#diagram").ejDiagram({
            width: "100%",
            height: "600px",
            nodes: nodes,
        });
        // creating the instance for the diagram
        var diagram = $("#diagram").ejDiagram("instance");
 
        // add the node to the specific layer.
        diagram.addNodeToLayer('Layer1', ['Ellipse1'])

{% endhighlight %}

### Remove layer at runtime

Layers can be removed at runtime by using public method, [removeLayers](/api/js/ejdiagram#methods:removeLayers "removeLayers").  

The following code illustrates how to add a layer.

{% highlight javascript %}

        // creating the instance for the diagram
        var diagram = $("#diagram").ejDiagram("instance");
        // remove the diagram layers from model 
        diagram.removeLayers([diagram.model.layers[i]]);

{% endhighlight %}

### Remove node to layer at runtime

nodes can be removed from layer at runtime by using public removeNodeToLayer, [removeNodeToLayer](/api/js/ejdiagram#methods:removeNodeToLayer "addNodeToLayer").  
 
The layer's [name](/api/js/ejdiagram#members:layers-name "name") property is used to define the name of the layer.

The following code illustrates how to remove a node from layer.

{% highlight javascript %}

        // creating the nodes
        var nodes = [
            { name: "Ellipse1", width: 40, height: 40, offsetX: 100, offsetY: 100, shape: "ellipse" },
            { name: "Ellipse2", width: 40, height: 40, offsetX: 200, offsetY: 100, shape: "ellipse" }
        ];
        $("#diagram").ejDiagram({
            width: "100%",
            height: "600px",
            nodes: nodes,
        });
        // creating the instance for the diagram
        var diagram = $("#diagram").ejDiagram("instance");

        
        // remove the node from the specific layer.
        diagram.removeNodeToLayer('Layer1', ['Ellipse1'])

{% endhighlight %}

### Update layer at runtime

Layers can be updated at runtime by using public updateLayer, [updateLayer](/api/js/ejdiagram#methods:updateLayer "updateLayer").  
 
The following code illustrates how to add a node to layer.  

{% highlight javascript %}

        // creating the instance for the diagram
        var diagram = $("#diagram").ejDiagram("instance");
        // update the layer objects will be hidden on printing.
        diagram.updateLayer('Layer1', { print: false })

{% endhighlight %}

