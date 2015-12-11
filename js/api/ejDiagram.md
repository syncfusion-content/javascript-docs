---
layout: post
title: ejDiagram
description: API reference for ejDiagram
documentation: API
platform: js
keywords: diagram, ejDiagram, diagram api, syncfusion
---

# ejDiagram

The diagram control provides 2D surface to visualize the data as shapes, lines, text and images. It can be configured to DOM element such as DIV.

#### Syntax
$(element).ejDiagram();

#### Example

{% highlight html %}
 
<div id="diagram"></div>
<script>
//Create Diagram
$("#diagram").ejDiagram();
</script>

{% endhighlight %}

#### Requires

* module:jquery.js
* module:jquery.easing.min.js
* module:jsrender.min.js
* module:ej.core.js
* module:ej.draggable.js
* module:ej.scroller.js
* module:ej.touch.js
* module:ej.diagram.js
* module:ej.diagramcommon.js
* module:ej.diagraminteraction.js
* module:ej.diagramsvg.js
* module:ej.diagramtools.js
* module:ej.diagramlayout.js
* module:ej.matrix.js

## Members

### backgroundColor `String`
{:#members:backgroundcolor}

Color to be set as the background of the elements

#### Default Value

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({ backgroundColor: "red"});
</script>

{% endhighlight %}

### backgroundImage `String`
{:#members:backgroundimage}

Image to be set as the background of the elements

#### Default Value

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({ backgroundImage: "Syncfusion.png"});
</script>

{% endhighlight %}

### bridgeDirection `String`
{:#members:bridgedirection}

Sets the bridge direction of connectors

#### Default Value

* "top"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramContent").ejDiagram({bridgeDirection: "top"} });
</script>

{% endhighlight %}

### connectors `Array`
{:#members:connectors}

A collection of JSON objects where each object represents a connector

#### Default Value

* []

#### Example

{% highlight html %}

<div id="diagram"></div>
<script>
var connector = {name:"connector1", sourcePoint:{ x:100, y:100 }, targetPoint:{ x:200,y:200 }};
$("#DiagramContent").ejDiagram({ connectors:[connector] });
</script>

{% endhighlight %}

### connectors.addInfo `Object`
{:#members:connectors-addinfo}

To maintain additional information about connectors

#### Default Value

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var addInfo = { Description: "Bidirectional Flow" };
var connector = { name:"connector1", sourcePoint:{ x:100, y:100 }, targetPoint:{ x:200,y:200 }, addInfo:addInfo };
$("#DiagramContent").ejDiagram({ connectors:[connector] });
</script>

{% endhighlight %}

### connectors.bridgeSpace `Number`
{:#members:connectors-bridgespace}

Defines the width of the line bridges

#### Default Value

* 10

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector1 = { name:"connector1", sourcePoint:{ x:100, y:100 }, targetPoint:{ x:200,y:200 }, 
	               //Set bridge space
	               bridgeSpace: 15 };
var connector2 = { name:"connector2", sourcePoint:{x:150, y:100}, targetPoint:{x:150, y:200}};
var DiagramConstraints = ej.datavisualization.Diagram.DiagramConstraints;
$("#DiagramContent").ejDiagram(
{ 
	connectors:[connector1, connector2],
	//Enable bridging
	constraints:DiagramConstraints.Default | DiagramConstraints.Bridging 
});
</script>

{% endhighlight %}

### connectors.constraints `Number`
{:#members:connectors-constraints}

Enables or disables the behaviors of connectors. see<a href="global.html#connectorconstraints">ConnectorConstraints</a>

#### Default Value

* ConnectorConstraints.Default

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var ConnectorConstraints = ej.datavisualization.Diagram.ConnectorConstraints;
var connector = { name:"connector1", sourcePoint:{ x:100, y:100 }, targetPoint:{ x:200,y:200 }, 
	              //Disable selection
                  constraints: ConnectorConstraints.Default & ~ConnectorConstraints.Select };
$("#DiagramContent").ejDiagram({ connectors:[connector] });
</script>

{% endhighlight %}

### connectors.cornerRadius `Number`
{:#members:connectors-cornerradius}

Defines the radius of the rounded corner

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{ x:100, y:100 }, targetPoint:{ x:200,y:200 }, 
	              //Set corner radius
                  cornerRadius: 10, segments:[{ type: "orthogonal"}] };
$("#DiagramContent").ejDiagram({ connectors:[connector] });
</script>

{% endhighlight %}

### connectors.horizontalAlign `String`
{:#members:connectors-horizontalalign}

Sets the horizontal alignment of the connector. Applicable, if the parent of the connector is a container

#### Default Value

* HorizontalAlignment.Left

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector1 = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:150, y:150}, 
	               //Set the horizontal alignment
	               horizontalAlign:"right" }; 
				   
var group = { name :"group", children:[ connector1 ], 
              container: { type: "canvas" }, offsetX:200, offsetY:100, 
              minWidth:200, minHeight: 200, fillColor:"gray" };
			  
$("#DiagramContent").ejDiagram({nodes:[group]});
</script>

{% endhighlight %}

### connectors.labels `Array`
{:#members:connectors-labels}

A collection of JSON objects where each object represents a label. For label properties, refer [add link]

#### Default Value

* []

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
	              //Define the labels collection
                  labels:[{ text:"connector" }]}; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.lineColor `String`
{:#members:connectors-linecolor}

Sets the stroke color of the connector

#### Default Value

* black

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
                  lineColor:"blue" }; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.lineDashArray `String`
{:#members:connectors-linedasharray}

Sets the pattern of dashes and gaps used to stroke the path of the connector

#### Default Value

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
                  lineColor:"blue", lineDashArray: "2,2" }; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.lineHitPadding `Number`
{:#members:connectors-linehitpadding}

Defines the padding value to ease the interaction with connectors

#### Default Value

* 10

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
                  lineHitPadding: 15 }; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.lineWidth `Number`
{:#members:connectors-linewidth}

Sets the width of the line

#### Default Value

* 1

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
                  lineWidth: 10 }; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.marginBottom `Number`
{:#members:connectors-marginbottom}

Defines the minimum space to be left between the bottom of parent bounds and the connector. Applicable, if the parent is a container.

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
	
var connector1 = { name:"connector1", sourcePoint:{x:100, y:100}, 
                   targetPoint:{x:150, y:150}, verticalAlign:"bottom", marginBottom: 10 }; 
var group = { name :"group", children:[ connector1 ], 
              container: { type: "canvas" }, offsetX:200, offsetY:100, 
              minWidth:200, minHeight: 200, fillColor:"gray" };
$("#DiagramContent").ejDiagram({nodes:[group]});

</script>

{% endhighlight %}

### connectors.marginLeft `Number`
{:#members:connectors-marginleft}

Defines the minimum space to be left between the left of parent bounds and the connector. Applicable, if the parent is a container.

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector1 = { name:"connector1", sourcePoint:{x:100, y:100}, 
                   targetPoint:{x:150, y:150}, horizontalAlign:"left", marginLeft: 10 }; 
var group = { name :"group", children:[ connector1 ], 
              container: { type: "canvas" }, offsetX:200, offsetY:100, 
              minWidth:200, minHeight: 200, fillColor:"gray" };
$("#DiagramContent").ejDiagram({nodes:[group]});
</script>

{% endhighlight %}

### connectors.marginRight `Number`
{:#members:connectors-marginright}

Defines the minimum space to be left between the right of parent bounds and the connector. Applicable, if the parent is a container.

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector1 = { name:"connector1", sourcePoint:{x:100, y:100}, 
                   targetPoint:{x:150, y:150}, horizontalAlign:"right", marginRight: 10 }; 
var group = { name :"group", children:[ connector1 ], 
              container: { type: "canvas" }, offsetX:200, offsetY:100, 
              minWidth:200, minHeight: 200, fillColor:"gray" };
$("#DiagramContent").ejDiagram({nodes:[group]});
</script>

{% endhighlight %}

### connectors.marginTop `Number`
{:#members:connectors-margintop}

Defines the minimum space to be left between the top of parent bounds and the connector. Applicable, if the parent is a container.

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector1 = { name:"connector1", sourcePoint:{x:100, y:100}, 
                   targetPoint:{x:150, y:150}, verticalAlign:"top", marginTop: 10 }; 
var group = { name :"group", children:[ connector1 ], 
              container: { type: "canvas" }, offsetX:200, offsetY:100, 
              minWidth:200, minHeight: 200, fillColor:"gray" };
$("#DiagramContent").ejDiagram({nodes:[group]});
</script>

{% endhighlight %}

### connectors.name `String`
{:#members:connectors-name}

Sets a unique name for the connector

#### Default Value

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200} }; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.opacity `Number`
{:#members:connectors-opacity}

Defines the transparency of the connector

#### Default Value

* 1

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, 
	              opacity: 0.5 }; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.parent `String`
{:#members:connectors-parent}

Sets the parent name of the connector.

#### Default Value

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, parent:"group"}; 
var group = { name :"group", children:["connector1"] };
$("#DiagramContent").ejDiagram({ nodes:[group], connectors : [connector]});
</script>

{% endhighlight %}

### connectors.segments `Array`
{:#members:connectors-segments}

An array of JSON objects where each object represents a segment

#### Default Value

* [ { type:"straight" } ]

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, 
	              //Defines a collection of segments
                  segments: [{type:"straight", point: { x:75, y:150 }}] }; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.segments.direction `String`
{:#members:connectors-segments-direction}

Sets the direction of orthogonal segment

#### Default Value

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, 
                  segments: [{type:"orthogonal", direction:"bottom", length:50}] }; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.segments.length `Number`
{:#members:connectors-segments-length}

Describes the length of orthogonal segment

#### Default Value

* undefined

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, 
                  segments: [{type:"orthogonal", direction:"bottom", length:50}] }; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.segments.point `Point`
{:#members:connectors-segments-point}

Describes the end point of bezier/straight segment

#### Default Value

* Diagram.Point()

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, 
	              //Defines a collection of segments
                  segments: [{ type:"straight", point: { x:75, y:150 }}] }; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.segments.point1 `Point`
{:#members:connectors-segments-point1}

Defines the first control point of the bezier segment

#### Default Value

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, 
                  segments: [{ type:"bezier", point1: { x:150, y:50} }] }; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.segments.point2 `Point`
{:#members:connectors-segments-point2}

Defines the second control point of bezier segment

#### Default Value

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, 
                  segments: [{ type:"bezier", point1: { x:150, y:50}, point2:{ x: 150, y: 150 } }] }; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.segments.type `enum`
{:#members:connectors-segments-type}

Sets the type of the segment. See <a href="global.html#segments">Segments</a>

#### Default Value

* ej.datavisualization.Diagram.Segments.Straight

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, 
                  segments: [{ type:"bezier" }] }; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.segments.vector1 `Point`
{:#members:connectors-segments-vector1}

Describes the length and angle between the first control point and the start point of bezier segment

#### Default Value

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, 
                  segments: [{ type:"bezier", 
                  vector1: { distance:75, angle: 0}, 
                  vector2: { distance:75, angle: 180} }] }; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.segments.vector2 `Point`
{:#members:connectors-segments-vector2}

Describes the length and angle between the second control point and end point of bezier segment

#### Default Value

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, 
                  segments: [{ type:"bezier", 
                  vector1: { distance:75, angle: 0}, 
                  vector2: { distance:75, angle: 180} }] }; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.sourceDecorator `String`
{:#members:connectors-sourcedecorator}

Defines the source decorator of the connector

#### Default Value

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
                  sourceDecorator : { shape:"openarrow" } }; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.sourceDecorator.borderColor `String`
{:#members:connectors-sourcedecorator-bordercolor}

Sets the border color of the source decorator

#### Default Value

* "black"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, lineColor:"red",
                  sourceDecorator : { shape:"openarrow" , borderColor:"red"} }; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.sourceDecorator.borderWidth `Number`
{:#members:connectors-sourcedecorator-borderwidth}

Sets the border width of the decorator

#### Default Value

* 1

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var link=[];
link={[targetDecorator:{borderWidth: 1}]};
$("#diagramcontent").ejDiagram({connectors:link});
</script>

{% endhighlight %}

### connectors.sourceDecorator.fillColor `String`
{:#members:connectors-sourcedecorator-fillcolor}

Sets the fill color of the source decorator

#### Default Value

* "black"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, lineColor:"red",
                  sourceDecorator : { shape:"circle" , fillColor:"red"} }; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.sourceDecorator.height `Number`
{:#members:connectors-sourcedecorator-height}

Sets the height of the source decorator

#### Default Value

* 8

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, lineColor:"red",
                  sourceDecorator : { width: 10, height:10 } }; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.sourceDecorator.pathData `String`
{:#members:connectors-sourcedecorator-pathdata}

Defines the custom shape of the source decorator

#### Default Value

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
                  sourceDecorator : { shape:"path", pathData:"M 376.892,225.284L 371.279,211.95L 376.892,198.617L 350.225,211.95L 376.892,225.284 Z"} }; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.sourceDecorator.shape `enum`
{:#members:connectors-sourcedecorator-shape}

Defines the shape of the source decorator. See <a href="global.html#decoratorshapes">DecoratorShapes</a>

#### Default Value

* ej.datavisualization.Diagram.DecoratorShapes.Arrow

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
                  sourceDecorator : { shape:"circle" } }; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.sourceDecorator.width `Number`
{:#members:connectors-sourcedecorator-width}

Defines the width of the source decorator

#### Default Value

* 8

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, lineColor:"red",
                  sourceDecorator : { width: 10, height:10 } }; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.sourceNode `String`
{:#members:connectors-sourcenode}

Sets the sourceNode of the connector

#### Default Value

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
	
var node1 = {name:"source", offsetX:100, offsetY:100, width: 50, height: 50 };
var node2 = {name:"target", offsetX:300, offsetY:300, width: 50, height: 50 };
var connector = { name:"connector1", sourceNode:"source", targetNode:"target" }; 
$("#DiagramContent").ejDiagram({nodes:[ node1, node2 ],connectors : [connector]});

</script>

{% endhighlight %}

### connectors.sourcePadding `Number`
{:#members:connectors-sourcepadding}

Defines the space to be left between the source node and the source point of a connector

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var node1 = {name:"source", offsetX:100, offsetY:100, width: 50, height: 50 };
var node2 = {name:"target", offsetX:300, offsetY:300, width: 50, height: 50 };
var connector = { name:"connector1", 
                  sourceNode:"source", targetNode:"target",
                  sourcePadding: 2, targetPadding: 2 }; 
$("#DiagramContent").ejDiagram({nodes:[ node1, node2 ],connectors : [connector]});
</script>

{% endhighlight %}

### connectors.sourcePoint `Point`
{:#members:connectors-sourcepoint}

Describes the start point of the connector

#### Default Value

* Point

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", 
				  sourcePoint:{x:100, y:100}, 
				  targetPoint:{x:200, y:200} }; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.sourcePort `String`
{:#members:connectors-sourceport}

Sets the source port of the connector

#### Default Value

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var node1 = {name:"source", offsetX:100, offsetY:100, width: 50, height: 50,
             ports:[{ name:"port", offset: { x:1, y:0.5 } }] };
var node2 = {name:"target", offsetX:200, offsetY:200, width: 50, height: 50, 
             ports:[{ name:"port", offset: { x:0, y:0.5 } }] };
var connector = { name:"connector1", 
                  sourceNode:"source", targetNode:"target",
                  sourcePort: "port", targetPort:"port" }; 
$("#DiagramContent").ejDiagram({nodes:[ node1, node2 ],connectors : [connector]});
</script>

{% endhighlight %}

### connectors.targetDecorator `String`
{:#members:connectors-targetdecorator}

Defines the target decorator of the connector

#### Default Value

* { shape:"arrow", width: 8, height:8, borderColor:"black", fillColor:"black" }

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
                  targetDecorator : { shape:"openarrow" } }; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.targetDecorator.borderColor `String`
{:#members:connectors-targetdecorator-bordercolor}

Sets the border color of the decorator

#### Default Value

* "black"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, lineColor:"red",
                  sourceDecorator : { shape:"openarrow" , borderColor:"red"} }; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.targetDecorator.fillColor `String`
{:#members:connectors-targetdecorator-fillcolor}

Sets the color with which the decorator will be filled

#### Default Value

* "black"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, lineColor:"red",
                  targetDecorator : { shape:"circle" , fillColor:"red"} }; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.targetDecorator.height `Number`
{:#members:connectors-targetdecorator-height}

Defines the height of the target decorator

#### Default Value

* 8

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, lineColor:"red",
                  targetDecorator : { width: 10, height:10 } }; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.targetDecorator.pathData `String`
{:#members:connectors-targetdecorator-pathdata}

Defines the custom shape of the target decorator

#### Default Value

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
                  targetDecorator : { shape:"path", pathData:"M 376.892,225.284L 371.279,211.95L 376.892,198.617L 350.225,211.95L 376.892,225.284 Z"} }; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.targetDecorator.shape `enum`
{:#members:connectors-targetdecorator-shape}

Defines the shape of the target decorator See <a href="global.html#DecoratorShapes">DecoratorShapes</a>

#### Default Value

* ej.datavisualization.Diagram.DecoratorShapes.Arrow

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
                  targetDecorator : { shape:"circle" } }; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.targetDecorator.width `Number`
{:#members:connectors-targetdecorator-width}

Defines the width of the target decorator

#### Default Value

* 8

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, lineColor:"red",
                  targetDecorator : { width: 10, height:10 } }; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.targetNode `String`
{:#members:connectors-targetnode}

Sets the target node of the connector

#### Default Value

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var node1 = {name:"source", offsetX:100, offsetY:100, width: 50, height: 50 };
var node2 = {name:"target", offsetX:300, offsetY:300, width: 50, height: 50 };
var connector = { name:"connector1", sourceNode:"source", targetNode:"target" }; 
$("#DiagramContent").ejDiagram({nodes:[ node1, node2 ],connectors : [connector]});
</script>

{% endhighlight %}

### connectors.targetPadding `Number`
{:#members:connectors-targetpadding}

Defines the space to be left between the target node and the target point of the connector

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var node1 = {name:"source", offsetX:100, offsetY:100, width: 50, height: 50 };
var node2 = {name:"target", offsetX:300, offsetY:300, width: 50, height: 50 };
var connector = { name:"connector1", 
                  sourceNode:"source", targetNode:"target",
                  sourcePadding: 2, targetPadding: 2 }; 
$("#DiagramContent").ejDiagram({nodes:[ node1, node2 ],connectors : [connector]});
</script>

{% endhighlight %}

### connectors.targetPoint `Point`
{:#members:connectors-targetpoint}

Describes the end point of the connector

#### Default Value

* Point

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", 
				  sourcePoint:{x:100, y:100}, 
				  targetPoint:{x:200, y:200} }; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.targetPort `String`
{:#members:connectors-targetport}

Sets the targetPort of the connector

#### Default Value

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var node1 = {name:"source", offsetX:100, offsetY:100, width: 50, height: 50,
             ports:[{ name:"port", offset: { x:1, y:0.5 } }] };
var node2 = {name:"target", offsetX:200, offsetY:200, width: 50, height: 50, 
             ports:[{ name:"port", offset: { x:0, y:0.5 } }] };
var connector = { name:"connector1", 
                  sourceNode:"source", targetNode:"target",
                  sourcePort: "port", targetPort:"port" }; 
$("#DiagramContent").ejDiagram({nodes:[ node1, node2 ],connectors : [connector]});
</script>

{% endhighlight %}

### connectors.verticalAlign `VerticalAlignment`
{:#members:connectors-verticalalign}

To set the vertical alignment of connector (Applicable,if the parent is group)

#### Default Value

* VerticalAlignment.Top

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector1 = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:150, y:150}, 
	               //Set the horizontal alignment
	               verticalAlign:"bottom" }; 
				   
var group = { name :"group", children:[ connector1 ], 
              container: { type: "canvas" }, offsetX:200, offsetY:100, 
              minWidth:200, minHeight: 200, fillColor:"gray" };
			  
$("#DiagramContent").ejDiagram({nodes:[group]});
</script>

{% endhighlight %}

### connectors.visible `Boolean`
{:#members:connectors-visible}

Enables or disables the visibility of connector

#### Default Value

* true

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, 
                  visible: false }; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.zOrder `Number`
{:#members:connectors-zorder}

Sets the z-index of the connector

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connectorghj", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, 
                  zOrder: 1000 }; 
$("#DiagramContent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectorTemplate `Object`
{:#members:connectortemplate}

To customize the connector properties before rendering the connector

#### Default Value

* null

#### Example

{% highlight html %}

<div id="diagram"></div>
<script>
function connectorTemplate(diagram, connector, data) {connector.labels[0].text = data.Name};
$("#diagram").ejDiagram({ connectorTemplate:connectorTemplate});
</script>

{% endhighlight %}

### constraints `enum`
{:#members:constraints}

Sets the default behavior of the diagram see <a href="global.html#diagramconstraints">DiagramConstraints</a>

#### Default Value

* constraints.All

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramContent").ejDiagram({constraints: ej.datavisualization.Diagram.DiagramConstraints.Default} });
</script>

{% endhighlight %}

### contextMenu
{:#members:contextmenu}

Object to customize the context menu for diagram

### contextMenu.items `Array`
{:#members:contextmenu-items}

Define the collection of context menu items

#### Default Value

* []

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
//Collection of items
var menucollection = [{ "name": "hyperLink", "text": "Hyperlink", "image": "", "style": "" }];
var contextMenu = { items: menucollection};
$("#diagramContent").ejDiagram({contextMenu: contextMenu});
</script>

{% endhighlight %}

### contextMenu.showCustomMenuItemsOnly `Boolean`
{:#members:contextmenu-showcustommenuitemsonly}

To set whether to display the default context menu items or not

#### Default Value

* true

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({showCustomMenuItemsOnly: true});
</script>

{% endhighlight %}

### dataSourceSettings
{:#members:datasourcesettings}

Object to set dataSource to diagram

### dataSourceSettings.dataSource `Object`
{:#members:datasourcesettings-datasource}

Describes the data source either as a collection of objects or an instance of ej.DataManager

#### Default Value

* null

#### Example

{% highlight html %}

<div id="diagram"></div>
<script>
$("#diagram").ejDiagram({ dataSourceSettings: {dataSource: localData}});
</script>

{% endhighlight %}

### dataSourceSettings.id `String`
{:#members:datasourcesettings-id}

Describes the unique id of data source items.

#### Default Value

* null

#### Example

{% highlight html %}

<div id="diagram"></div>
<script>
$("#diagram").ejDiagram({ dataSourceSettings: {id: "CategoryID"}});
</script>

{% endhighlight %}

### dataSourceSettings.parent `String`
{:#members:datasourcesettings-parent}

Describes the parent id of data source items.

#### Default Value

* null

#### Example

{% highlight html %}

<div id="diagram"></div>
<script>
$("#diagram").ejDiagram({ dataSourceSettings: { parent: "reportingPerson"}});
</script>

{% endhighlight %}

### dataSourceSettings.query `Object`
{:#members:datasourcesettings-query}

Describes query to retrieve a set of data from the specified datasource.

#### Default Value

* null

#### Example

{% highlight html %}

<div id="diagram"></div>
<script>
query: ej.Query().from("Categories").select("CategoryID,CategoryName").take(3);
</script>

{% endhighlight %}

### dataSourceSettings.root `String`
{:#members:datasourcesettings-root}

Describes the root node.

#### Default Value

* null

#### Example

{% highlight html %}

<div id="diagram"></div>
<script>
$("#diagram").ejDiagram({ dataSourceSettings: { root: "1"}});
</script>

{% endhighlight %}

### dataSourceSettings.tablename `String`
{:#members:datasourcesettings-tablename}

Describes the name of the table on which the specified query to be executed

#### Default Value

* null

#### Example

{% highlight html %}

<div id="diagram"></div>
<script>
$("#diagram").ejDiagram({ dataSourceSettings:{tableName: "Categories"}});
</script>

{% endhighlight %}

### defaultSettings `Object`
{:#members:defaultsettings}

To set the default values to nodes and connector properties

#### Default Value

* {}

#### Example

{% highlight html %}

<div id="diagram"></div>
<script>
$("#diagram").ejDiagram({ defaultSettings: { node: {width: 110, height: 40, fillColor:"skyblue"}}});
</script>

{% endhighlight %}

### defaultSettings.connector `Object`
{:#members:defaultsettings-connector}

To set the default values to connector properties

#### Default Value

* null

#### Example

{% highlight html %}

<div id="diagram"></div>
<script>
$("#diagram").ejDiagram({ defaultSettings:{ connector:{ lineColor: "gray", lineWidth: 2 }}});
</script>

{% endhighlight %}

### defaultSettings.node `Object`
{:#members:defaultsettings-node}

To set the default values to node properties

#### Default Value

* null

#### Example

{% highlight html %}

<div id="diagram"></div>
<script>
$("#diagram").ejDiagram({ defaultSettings:{node: { fillColor: "#83A93F", borderColor: "#000000" }}});
</script>

{% endhighlight %}

### drawingTools `Object`
{:#members:drawingtools}

Describes the interactive features to be performed

#### Default Value

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({ drawingTools: {textTool: ej.datavisualization.Diagram.TextTool()}});
</script>

{% endhighlight %}

### drawType `Object`
{:#members:drawtype}

Sets the type of Json object to be drawn through drawing tool

#### Default Value

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({drawType:{type:"node"}});
</script>

{% endhighlight %}

### enableAutoScroll `Boolean`
{:#members:enableautoscroll}

Enables or disables Auto scroll in diagram

#### Default Value

* true

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({enableAutoScroll: true});
</script>

{% endhighlight %}

### enableContextMenu `Boolean`
{:#members:enablecontextmenu}

Enables or disables diagram context menu

#### Default Value

* true

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({enableContextMenu: true});
</script>

{% endhighlight %}

### height `String`
{:#members:height}

Specifies the height of the diagram.

#### Default Value

* null

#### Example

{% highlight html %}

<div id="diagram"></div>
<script>
$("#diagram").ejDiagram({ height:"100%" });
</script>

{% endhighlight %}

### layout
{:#members:layout}

To arrange the diagram elements on page

### layout. fixedNode `String`
{:#members:layout- fixednode}

Sets the fixed node with respect to which the layout will be aligned

#### Default Value

* ""

#### Example

{% highlight html %}

//fixedNode of the layout
$("#diagramContent").ejDiagram({layout: { fixedNode: "nodename"}});

{% endhighlight %}

### layout. getLayoutInfo `Object`
{:#members:layout- getlayoutinfo}

To customize the orientation of trees/sub trees For orientations see <a href="global.html#ChartOrientations">ChartOrientations</a> For chart types see <a href="global.html#ChartTypes">ChartTypes</a>

#### Default Value

* null

#### Example

{% highlight html %}

<div id="diagram"></div>
<script>
function getLayoutInfo(diagram, node, options) { options.orientation = "vertical"; options.type = "left"; offset = 10;};
$("#diagram").ejDiagram({layout: { getLayoutInfo:getLayoutInfo } });
</script>

{% endhighlight %}

### layout. marginY `Number`
{:#members:layout- marginy}

Sets the margin value to be vertically left between layout and diagram

#### Default Value

* 0

#### Example

{% highlight html %}

// marginY of the layout
$("#diagramContent").ejDiagram({layout: { marginY: 0}});

{% endhighlight %}

### layout.horizontalSpacing `Number`
{:#members:layout-horizontalspacing}

Sets the space to be horizontally left between nodes

#### Default Value

* 30

#### Example

{% highlight html %}

//horizontalSpacing of the layout
$("#diagramContent").ejDiagram({layout: {horizontalSpacing: 30}});

{% endhighlight %}

### layout.marginX `Number`
{:#members:layout-marginx}

Sets the margin value to be horizontally left between layout and diagram

#### Default Value

* 0

#### Example

{% highlight html %}

//marginX of the layout
$("#diagramContent").ejDiagram({layout: {marginX: 0}});

{% endhighlight %}

### layout.orientation `String`
{:#members:layout-orientation}

Sets the orientation/direction to arrange the diagram elements see <a href="global.html#LayoutOrientations">LayoutOrientations</a>

#### Default Value

* "topToBottom"

#### Example

{% highlight html %}

//orientation of the layout
$("#diagramContent").ejDiagram({layout: {orientation: "topToBottom"}});

{% endhighlight %}

### layout.type `String`
{:#members:layout-type}

Sets the type of the layout based on which the elements will be arranged

#### Default Value

* "none"

#### Example

{% highlight html %}

//type of the layout
$("#diagramContent").ejDiagram({layout: {type: "none"}});

{% endhighlight %}

### layout.verticalSpacing `Number`
{:#members:layout-verticalspacing}

Sets the space to be vertically left between nodes

#### Default Value

* 30

#### Example

{% highlight html %}

//verticalSpacing of the layout
$("#diagramContent").ejDiagram({layout: {verticalSpacing: 30}});

{% endhighlight %}

### locale `String`
{:#members:locale}

To define the current culture of diagram

#### Default Value

* "en-US"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({locale: "en-US"});
</script>

{% endhighlight %}

### nodes `Array`
{:#members:nodes}

Array of JSON objects where each object represents a node

#### Default Value

* []

#### Example

{% highlight html %}

<div id="diagram"></div>
<script>
var nodes = [{ name: "node1", width: 175, height: 60, offsetX:100, offsetY:100}];
$("#DiagramContent").ejDiagram({ nodes:nodes });
</script>

{% endhighlight %}

### nodes.activity `String`
{:#members:nodes-activity}

Defines the type of BPMN Activity. Applicable, if the node is a bpmn activity. See <a href="global.html#bpmnactivity">BPMNActivity</a>

#### Default Value

* ej.datavisualization.Diagram.BPMNActivity.Task

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{type: "bpmn", shape: ej.datavisualization.Diagram.BPMNShapes.Activity, activity: ej.datavisualization.Diagram.BPMNActivity.SubProcess, width:50, height:50}];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.addInfo `Object`
{:#members:nodes-addinfo}

To maintain additional information about nodes

#### Default Value

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var addInfo = { TooltipData: "Shares the information with the customer" };
//Add Info for nodes
var node1 = { name: "node1", addInfo: addInfo, offsetX:100, offsetY:100, width:50, height:50 };

//Define add Info for swimlane
var node2 = { type: "swimlane", name: "swimlane", addInfo: addInfo };
$("#DiagramContent").ejDiagram({nodes:[node1, node2]});
</script>

{% endhighlight %}

### nodes.borderColor `String`
{:#members:nodes-bordercolor}

Sets the border color of node

#### Default Value

* "black"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, borderColor: "red" }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.borderDashArray `String`
{:#members:nodes-borderdasharray}

Sets the pattern of dashes and gaps to stroke the border

#### Default Value

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>

<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, borderColor: "red" , borderDashArray: "4,2"}];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.borderWidth `Number`
{:#members:nodes-borderwidth}

Sets the border width of the node

#### Default Value

* 1

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, borderColor: "red" , borderDashArray: "2,2", borderWidth:2}];
$("#DiagramContent").ejDiagram({ nodes:nodes });
</script>

{% endhighlight %}

### nodes.canUngroup `Boolean`
{:#members:nodes-canungroup}

Defines whether the group can be ungrouped or not

#### Default Value

* true

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
var node1 = { name: "node1", width: 50, height:50, offsetX:50, offsetY:50, borderColor: "red" , borderDashArray: "4,2"};
var node2 = { name: "node2", width: 50, height:50, offsetX:150, offsetY:150, borderColor: "red" , borderDashArray: "4,2"};
var group = { name :"group", children:[node1, node2], canUngroup: false };
$("#DiagramContent").ejDiagram({nodes:[group]});
</script>

{% endhighlight %}

### nodes.children `Array`
{:#members:nodes-children}

Array of JSON objects where each object represents a child node/connector

#### Default Value

* []

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
var node1 = { name: "node1", width: 50, height:50, offsetX:50, offsetY:50, borderColor: "red" , borderDashArray: "4,2"};
var node2 = { name: "node2", width: 50, height:50, offsetX:150, offsetY:150, borderColor: "red" , borderDashArray: "4,2"};
//A group node with two child nodes
var group = { name :"group", children:[node1, node2]};
$("#DiagramContent").ejDiagram({ nodes:[group] });
</script>

{% endhighlight %}

### nodes.collection `Boolean`
{:#members:nodes-collection}

Defines whether the BPMN data object is a collection or not

#### Default Value

* false

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{name:"dataobject", type: "bpmn", shape:"dataObject", collection: true, width:50, height: 50, offsetX:100, offsetY:100}];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.connectorPadding `Number`
{:#members:nodes-connectorpadding}

Defines the distance to be left between a node and its connections(In coming and out going connections).

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, connectorPadding: 5}];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.constraints `enum`
{:#members:nodes-constraints}

Enables or disables the default behaviors of the node see<a href="global.html#nodeconstraints">NodeConstraints</a>

#### Default Value

* NodeConstraints.Default

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var NodeConstraints = ej.datavisualization.Diagram.NodeConstraints;
//Disable selection
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
	constraints: NodeConstraints.Default & ~NodeConstraints.Select}];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.constraints `enum`
{:#members:nodes-constraints}

Enables or disables the behaviors of swimlane. see <a href="global.html#nodeconstraints">NodeConstraints</a> 

#### Default Value

ej.datavisualization.Diagram.NodeConstraints.Default & ~(ej.datavisualization.Diagram.NodeConstraints.ResizeNorth | ej.datavisualization.Diagram.NodeConstraints.ResizeWest | ej.datavisualization.Diagram.NodeConstraints.ResizeNorthWest | ej.datavisualization.Diagram.NodeConstraints.ResizeNorthEast | ej.datavisualization.Diagram.NodeConstraints.ResizeSouthWest)

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var NodeConstraints = ej.datavisualization.Diagram.NodeConstraints;
//Disables selection
var swimlane = { type: "swimlane",name: "swimlane",constraints: NodeConstraints.Default & ~NodeConstraints.Select };
$("#DiagramContent").ejDiagram({nodes:[swimlane]});

</script>

{% endhighlight %}

### nodes.container `Object`
{:#members:nodes-container}

Defines how the child objects need to be arranged(Either in any predefined manner or automatically). Applicable, if the node is a group.

#### Default Value

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
ar nodes;
var node1 = { name: "node1", width: 50, height:50, borderColor: "red" , borderDashArray: "4,2"};
var node2 = { name: "node2", width: 50, height:50, borderColor: "red" , borderDashArray: "4,2"};
var group = {name :"group", children:[node1, node2], container: { type: "stack" }, offsetX:200, offsetY:100 };
$("#DiagramContent").ejDiagram({nodes:[group]});
</script>

{% endhighlight %}

### nodes.container.orientation `String`
{:#members:nodes-container-orientation}

Defines the orientation of the container. Applicable, if the group is a container.

#### Default Value

* "vertical"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
var node1 = { name: "node1", width: 50, height:50, borderColor: "red" , borderDashArray: "4,2"};
var node2 = { name: "node2", width: 50, height:50, borderColor: "red" , borderDashArray: "4,2"};
var group = {name :"group", children:[node1, node2], container: { type: "stack", orientation: "horizontal" }, offsetX:200, offsetY:100 };
$("#DiagramContent").ejDiagram({nodes:[group]});
</script>

{% endhighlight %}

### nodes.container.type `enum`
{:#members:nodes-container-type}

Sets the type of the container. Applicable if the group is a container.

#### Default Value

* ej.datavisualization.Diagram.ContainerType.Canvas

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
var node1 = { name: "node1", width: 50, height:50, borderColor: "red" , borderDashArray: "4,2"};
var node2 = { name: "node2", width: 50, height:50, borderColor: "red" , borderDashArray: "4,2"};
//Define a stack type container
var group = {name :"group", children:[node1, node2], container: { 
	type: ej.datavisualization.Diagram.ContainerType.Stack }, 
	offsetX:200, offsetY:100 };
$("#DiagramContent").ejDiagram({nodes:[group]});
</script>

{% endhighlight %}

### nodes.cornerRadius `Number`
{:#members:nodes-cornerradius}

Defines the corner radius of rectangular shapes.

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
	type:"basic", shape:"rectangle", cornerRadius:5}];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.event `enum`
{:#members:nodes-event}

Sets the type of the BPMN Events. Applicable, if the node is a bpmn event. See <a href="global.html#bpmnevents">BPMNEvents</a>

#### Default Value

* ej.datavisualization.Diagram.BPMNEvents.Start

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ type: "bpmn", shape: "event" , 
	     event: ej.datavisualization.Diagram.BPMNEvents.Intermediate, width:50, height:50}];
$("#DiagramContent").ejDiagram({ nodes:nodes });
</script>

{% endhighlight %}

### nodes.excludeFromLayout `Boolean`
{:#members:nodes-excludefromlayout}

Defines whether the node can be automatically arranged using layout or not

#### Default Value

* false

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;

//Manually positioned
var node1 = { name: "node1", width: 50, height:50, offsetX:50, offsetY:50, excludeFromLayout: true};

//Automatically arranged
var node2 = { name: "node2", width: 50, height:50 };
var node3 = { name: "node3", width: 50, height:50 };

$("#DiagramContent").ejDiagram({
      nodes:[ node1, node2, node3 ],
      layout:{type:"hierarchicaltree"}
});

</script>

{% endhighlight %}

### nodes.isexpanded `Boolean`
{:#members:nodes-isexpanded}

Defines whether the sub tree of the node is expanded or collapsed

#### Default Value

* true

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
//Collapse its subtree
var node1 = { name: "node1", width: 50, height:50, offsetX:50, offsetY:50, isExpanded: false};

var node2 = { name: "node2", width: 50, height:50 };
var connector = { sourceNode:"node1", targetNode:"node2" , name:"connector" };
$("#DiagramContent").ejDiagram({
      nodes:[node1, node2],
      connectors:[connector],
      layout:{type:"hierarchicaltree"}
});
</script>

{% endhighlight %}

### nodes.fillColor `String`
{:#members:nodes-fillcolor}

Defines the fill color of the node

#### Default Value

* "White"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, fillColor:"red" }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.gateway `enum`
{:#members:nodes-gateway}

Sets the type of the BPMN Gateway. Applicable, if the node is a bpmn gateway. See <a href="global.html#bpmngateways">BPMNGateways</a>

#### Default Value

* ej.datavisualization.Diagram.BPMNGateways.None

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ type: "bpmn", shape: "gateway" , gateway: ej.datavisualization.Diagram.BPMNGateways.Exclusive, width:50, height:50 }];
$("#DiagramContent").ejDiagram({ nodes:nodes });
</script>

{% endhighlight %}

### nodes.gradient
{:#members:nodes-gradient}

Paints the node with a smooth transition from one color to another color

### nodes.gradient.LinearGradient `Object`
{:#members:nodes-gradient-lineargradient}

Paints the node with linear color transitions

### nodes.gradient.LinearGradient.stops `Array`
{:#members:nodes-gradient-lineargradient-stops}

Defines the different colors and the region of color transitions

#### Default Value

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
 var gradient = {
     type: "linear", x1: 0, x2: 50, y1: 0, y2: 50, stops: [
     { color: "white", offset: 0}, { color: "red", offset: 50}]
};
var nodes = [{name: "Node1", width: 100, height: 100, gradient : gradient}];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.gradient.LinearGradient.x1 `Number`

{:#members:nodes-gradient-lineargradient-x1}

Defines the left most position(relative to node) of the rectangular region that needs to be painted

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
// Apply the gradient from the left most position of node
 var gradient = {
     type: "linear", x1: 0, x2: 100, y1: 0, y2: 100, stops: [
     { color: "white", offset: 0}, { color: "red", offset: 100 }]
};
var nodes = [{name: "node1", width: 100, height: 100, gradient : gradient}];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.gradient.LinearGradient.x2 `Number`
{:#members:nodes-gradient-lineargradient-x2}

Defines the right most position(relative to node) of the rectangular region that needs to be painted

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
// Apply the gradient till the right most position of node
 var gradient = {
     type: "linear", x1: 0, x2: 100, y1: 0, y2: 100, stops: [
     { color: "white", offset: 0}, { color: "red", offset: 100 }]
};
var nodes = [{name: "node1", width: 100, height: 100, gradient : gradient}];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.gradient.LinearGradient.y1 `Number`
{:#members:nodes-gradient-lineargradient-y1}

Defines the top most position(relative to node) of the rectangular region that needs to be painted

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
// Apply the gradient from the top most position of node
 var gradient = {
     type: "linear", x1: 0, x2: 100, y1: 0, y2: 100, stops: [
     { color: "white", offset: 0}, { color: "red", offset: 100 }]
};
var nodes = [{name: "node1", width: 100, height: 100, gradient : gradient}];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.gradient.LinearGradient.y2 `Number`
{:#members:nodes-gradient-lineargradient-y2}

Defines the bottom most position(relative to node) of the rectangular region that needs to be painted

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
// Apply the gradient till the bottom most position of node
 var gradient = {
     type: "linear", x1: 0, x2: 100, y1: 0, y2: 100, stops: [
     { color: "white", offset: 0}, { color: "red", offset: 100 }]
};
var nodes = [{name: "node1", width: 100, height: 100, gradient : gradient}];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}


### nodes.gradient.RadialGradient `Object`
{:#members:nodes-gradient-radialgradient}

Paints the node with radial color transitions. A focal point defines the beginning of the gradient, and a circle defines the end point of the gradient.

### nodes.gradient.RadialGradient.cx `Number`
{:#members:nodes-gradient-radialgradient-cx}

Defines the center position where color transition is to be applied

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var gradient = {
     type: "radial", fx:50, fy: 50, cx :50, cy: 50, stops: [
     { color: "white", offset:0 }, { color: "red", offset:100}]
};
var nodes = [{name: "node1", width: 100, height: 100, gradient : gradient}];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.gradient.RadialGradient.cy `Number`
{:#members:nodes-gradient-radialgradient-cy}

The ending X-Axis for the region

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var gradient = ej.datavisualization.Diagram.RadialGradientDefaults();
gradient.type = "linear;
gradient.cx = 20;
gradient.cy = 50;
gradient.fx = 20;
gradient.fy = 50;
var nodes = [{name:"Node1",width: 100,height: 100,gradient : gradient}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.gradient.RadialGradient.fx `Number`
{:#members:nodes-gradient-radialgradient-fx}

The starting X-Axis for the region

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var gradient = ej.datavisualization.Diagram.RadialGradientDefaults();
gradient.type = "linear;
gradient.cx = 20;
gradient.cy = 50;
gradient.fx = 20;
gradient.fy = 50;
var nodes = [{name:"Node1",width: 100,height: 100,gradient : gradient}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.gradient.RadialGradient.fy `Number`
{:#members:nodes-gradient-radialgradient-fy}

The ending Y-Axis for the region

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var gradient = ej.datavisualization.Diagram.RadialGradientDefaults();
gradient.type = "linear;
gradient.cx = 20;
gradient.cy = 50;
gradient.fx = 20;
gradient.fy = 50;
var nodes = [{name:"Node1",width: 100,height: 100,gradient : gradient}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.gradient.RadialGradient.stops `Array`
{:#members:nodes-gradient-radialgradient-stops}

Defines the different colors and the region of color transitions.

#### Default Value

* []

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var gradient = {
     type: "radial", fx:50, fy: 50, cx :50, cy: 50, stops: [
     { color: "white", offset:0 }, { color: "red", offset:100}]
};
var nodes = [{name: "Node1", width: 100, height: 100, gradient : gradient}];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.gradient.Stop `Object`
{:#members:nodes-gradient-stop}

Defines the color and a position where the previous color transition ends and a new color transition starts

### nodes.gradient.Stop.color `String`
{:#members:nodes-gradient-stop-color}

Sets the color to be filled over the specified region

#### Default Value

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
// Apply the gradient till the bottom most position of node
var gradient = {
     type: "linear", x1: 0, x2: 100, y1: 0, y2: 100, stops: [
     { color: "white", offset: 0}, { color: "red", offset: 100 }]
};
var nodes = [{name: "node1", width: 100, height: 100, gradient : gradient}];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.gradient.Stop.offset `Number`
{:#members:nodes-gradient-stop-offset}

Sets the position where the previous color transition ends and a new color transition starts

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
// Apply the gradient till the bottom most position of node
var gradient = {
     type: "linear", x1: 0, x2: 100, y1: 0, y2: 100, stops: [
     { color: "white", offset: 0}, { color: "red", offset: 100 }]
};
var nodes = [{name: "node1", width: 100, height: 100, gradient : gradient}];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.gradient.Stop.opacity `Number`
{:#members:nodes-gradient-stop-opacity}

Decribes the transparency level of the region

#### Default Value

* 1

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
// Apply the gradient till the bottom most position of node
var gradient = {
     type: "linear", x1: 0, x2: 100, y1: 0, y2: 100, 
	 stops: [
        { color: "white", offset: 0, opacity: 0.7}, 
	    { color: "red", offset: 100, opacity: 0.5 }
	 ]
};
var nodes = [{name: "node1", width: 100, height: 100, gradient : gradient}];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.header `Object`
{:#members:nodes-header}

Defines the header of a swimlane/lane

#### Default Value

* { text: "Title", fontSize: 11 }

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = { type: "swimlane", name: "swimlane", header: { text: "Swimlane", fontSize: 12, bold: true } };
$("#DiagramContent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.height `Number`
{:#members:nodes-height}

Defines the height of the node

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
// Set the height as 150
nodes = [{ name: "node1", width: 50, height:150, offsetX:50, offsetY:50 }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.horizontalAlign `HorizontalAlignment`
{:#members:nodes-horizontalalign}

Sets the horizontal alignment of the node. Applicable, if the parent of the node is a container

#### Default Value

* HorizontalAlignment.Left

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
var node1 = { name: "node1", width: 50, height:50};
//Align the node at the right most position of the canvas
var node2 = { name: "node2", width: 50, height:50, horizontalAlign: "right"};
var group = { name :"group", children:[ node1, node2 ], container: { type: "canvas" }, offsetX:200, offsetY:100, minWidth:200, minHeight: 200, fillColor:"gray" };
$("#DiagramContent").ejDiagram({nodes:[group]});
</script>

{% endhighlight %}

### nodes.inEdges `Array`
{:#members:nodes-inedges}

A read only collection of incoming connectors/edges of the node

#### Default Value

* []

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connectors = [{ name: "connector1", sourceNode: "node1", targetNode: "Node2"}];
nodes=[{ inEdges:connectors }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.isSwimlane `Boolean`
{:#members:nodes-isswimlane}

Sets the node as a swimlane

#### Default Value

* false

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = {type: "swimlane",name: "swimlane", isSwimlane:true, header: {text: "Swimlane", fontSize: 12, bold: true} };
$("#DiagramContent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.labels `Array`
{:#members:nodes-labels}

A collection of objects where each object represents a label

#### Default Value

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var label = [];
label = { "text": "Node1", "fontColor": "Red"};
nodes=[{labels:label}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.bold `Boolean`
{:#members:nodes-labels-bold}

Enables/disables the bold style

#### Default Value

* false

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"label", bold:true}]
      }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.borderColor `String`
{:#members:nodes-labels-bordercolor}

Sets the border color of the label

#### Default Value

* "transparent"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"label", borderColor:"red", borderWidth: 2}]
      }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.borderWidth `Number`
{:#members:nodes-labels-borderwidth}

Sets the border width of the label

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"label", borderColor:"red", borderWidth: 2}]
      }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.fillColor `String`
{:#members:nodes-labels-fillcolor}

Sets the fill color of the text area

#### Default Value

* "transparent"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"label", fillColor: "green"}]
      }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.fontColor `String`
{:#members:nodes-labels-fontcolor}

Sets the font color of the text

#### Default Value

* "black"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"label", fontColor: "green"}]
      }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.fontFamily `String`
{:#members:nodes-labels-fontfamily}

Sets the font family of the text

#### Default Value

* "Arial"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"label", fontColor: "green", fontFamily:"seugoe UI"}]
      }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.fontSize `Number`
{:#members:nodes-labels-fontsize}

Defines the font size of the text

#### Default Value

* 12

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"label", fontSize: 14}]
      }];
$("#DiagramContent").ejDiagram({nodes:nodes});

</script>

{% endhighlight %}

### nodes.labels.horizontalAlignment `enum`
{:#members:nodes-labels-horizontalalignment}

Sets the horizontal alignment of the label. See<a href="global.html#horizontalalignment">HorizontalAlignment</a>

#### Default Value

* HorizontalAlignment.Center

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
	     //Align the text at the left most position of node
         labels:[{ text:"label", offset:{ x:0 }, horizontalAlignment:"left"}]
      }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.italic `Boolean`
{:#members:nodes-labels-italic}

Enables/disables the italic style

#### Default Value

* false

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"label", italic:true}]
      }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.margin `Object`
{:#members:nodes-labels-margin}

To set the margin of the label

#### Default Value

* ej.datavisualization.Diagram.Margin()

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
	     //Leaves 5px space between the left boundary of node and label
         labels:[{ text:"label", offset:{ x:0 }, horizontalAlignment:"left", margin:{ left: 5 }}]
      }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.mode `enum`
{:#members:nodes-labels-mode}

Returns whether the label currently being edited or not. See <a href="global.html#labeleditmode">LabelEditMode</a>

#### Default Value

* LabelEditMode.Edit

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"label", mode: ej.datavisualization.Diagram.LabelEditMode.View }]
      }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.name `String`
{:#members:nodes-labels-name}

Sets the unique identifier of the label

#### Default Value

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"label", name:"label1"}]
      }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.offset `Point`
{:#members:nodes-labels-offset}

Sets the fraction/ratio(relative to node) that defines the position of the label

#### Default Value

* Point(0.5, 0.5)

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"label", offset:ej.datavisualization.Diagram.Point({x:0, y:0.5}) }]
      }];
$("#DiagramContent").ejDiagram({nodes:nodes});

</script>

{% endhighlight %}

### nodes.labels.readOnly `Boolean`
{:#members:nodes-labels-readonly}

Defines whether the label is editable or not

#### Default Value

* false

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"label", readOnly:true}]
      }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.rotateAngle `Number`
{:#members:nodes-labels-rotateangle}

Defines the angle to which the label needs to be rotated

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"label", rotateAngle: 90}]
      }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.text `String`
{:#members:nodes-labels-text}

Defines the label text

#### Default Value

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"Label"}]
      }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.textAlign `enum`
{:#members:nodes-labels-textalign}

Defines how to align the text inside the label. See <a href="global.html#textalign">TextAlign</a>

#### Default Value

* TextAlign.Center

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"node Label", textAlign:ej.datavisualization.Diagram.TextAlign.Left}]
      }];
$("#DiagramContent").ejDiagram({ nodes:nodes });
</script>

{% endhighlight %}

### nodes.labels.textDecoration `enum`
{:#members:nodes-labels-textdecoration}

Sets how to decorate the label text. See<a href="global.html#TextDecorations">TextDecorations</a>

#### Default Value

* TextDecorations.None

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
	     //Decorate the text with an underline
         labels:[{ text:"Label", textDecoration: ej.datavisualization.Diagram.TextDecorations.Underline}]
      }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.verticalAlignment `enum`
{:#members:nodes-labels-verticalalignment}

Sets the vertical alignment of the label. See<a href="global.html#VerticalAlignment">VerticalAlignment</a>

#### Default Value

* VerticalAlignment.Center

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
	     //Aligns the text at the top most position of node
         labels:[{ text:"label", offset:{ y:0 }, verticalAlignment:"top"}]
      }];
$("#DiagramContent").ejDiagram({ nodes:nodes });
</script>

{% endhighlight %}

### nodes.labels.visible `Boolean`
{:#members:nodes-labels-visible}

Enables or disables the visibility of the label

#### Default Value

* true

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"Label", visible: false}]
      }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.width `Number`
{:#members:nodes-labels-width}

Sets the width of the label(the maximum value of label width and the node width will be considered as label width)

#### Default Value

* 50

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"Label", width: 100}]
      }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.wrapping `enum`
{:#members:nodes-labels-wrapping}

Defines how the label text needs to be wrapped. See <a href="global.html#textwrapping">TextWrapping</a>

#### Default Value

* TextWrapping.WrapWithOverflow

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"Enter Your Text", wrapping:ej.datavisualization.Diagram.TextWrapping.NoWrap}]
      }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.lanes `Array`
{:#members:nodes-lanes}

An array of objects where each object represents a lane. Appilicable, if the node is a swimlane.

#### Default Value

* []

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = { type: "swimlane",name: "swimlane", offsetX:300, offsetY:200,
//Define the collection of lanes
				 lanes:[{name:"lane1", width:200 },
				 {name:"lane2", width:100}] };
$("#DiagramContent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.lanes.addInfo `Object`
{:#members:nodes-lanes-addinfo}

Allows to maintain additional information about lane

#### Default Value

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var addInfo = { Description:"Describe the functionality" };
var swimlane = {type: "swimlane",name: "swimlane", offsetX:300, offsetY:200,
lanes:[{ name:"lane1", width:200, addInfo: addInfo }] };
$("#DiagramContent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.lanes.children `Array`
{:#members:nodes-lanes-children}

An array of objects where each object represents a child node of the lane

#### Default Value

* []

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = {type: "swimlane",name: "swimlane", offsetX:300, offsetY:200,
lanes:[{name:"lane1", width:200 , 
	  //Defines the collection of child objects
      children:[{name:"process1", width: 50, height: 50 }]
 }]}
$("#DiagramContent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.lanes.fillColor `String`
{:#members:nodes-lanes-fillcolor}

Defines the fill color of the lane

#### Default Value

* "white"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = {type: "swimlane",name: "swimlane", offsetX:300, offsetY:100,
lanes:[{name:"lane1", width:200 ,fillColor:"lightgray" }]}
$("#DiagramContent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.lanes.header `Object`
{:#members:nodes-lanes-header}

Defines the header of the lane

#### Default Value

* { text: "Function", fontSize: 11 }

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = {type: "swimlane",name: "swimlane", offsetX:300, offsetY:100,
lanes:[{name:"lane1", width:200, 
	//Defines the lane header
	header:{fillColor:"blue", fontColor:"white", text:"Functon 1"} }]}
$("#DiagramContent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.lanes.isLane `Boolean`
{:#members:nodes-lanes-islane}

Defines the object as a lane

#### Default Value

* false

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = {type: "swimlane",name: "swimlane", offsetX:300, offsetY:200,
lanes:[{name:"lane1", width:200 , isLane:true }]}
$("#DiagramContent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.lanes.name `String`
{:#members:nodes-lanes-name}

Sets the unique identifier of the lane

#### Default Value

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = {type: "swimlane",name: "swimlane", offsetX:300, offsetY:100,
lanes:[{ name:"function1", width:200 }]}
$("#DiagramContent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.lanes.orientation `String`
{:#members:nodes-lanes-orientation}

Sets the orientation of the lane. 

#### Default Value

* "vertical"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = { type: "swimlane",name: "swimlane", offsetX:300, offsetY:100, orientation:"horizontal",
lanes:[{ name:"function1", width:200 , orientation:"vertical" }]}
$("#DiagramContent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.marginBottom `Number`
{:#members:nodes-marginbottom}

Defines the minimum space to be left between the bottom of parent bounds and the node. Applicable, if the parent is a container.

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = {type: "swimlane",name: "swimlane", offsetX:300, offsetY:200,
lanes:[{name:"lane1", width:200 , 
      children:[{name:"process1", width: 50, height: 50, marginBottom: 50 }]
 }]}
$("#DiagramContent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.marginLeft `Number`
{:#members:nodes-marginleft}

Defines the minimum space to be left between the left of parent bounds and the node. Applicable, if the parent is a container.

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = {type: "swimlane",name: "swimlane", offsetX:300, offsetY:200,
lanes:[{name:"lane1", width:200 , 
      children:[{name:"process1", width: 50, height: 50, marginLeft: 10 }]
 }]}
$("#DiagramContent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.marginRight `Number`
{:#members:nodes-marginright}

Defines the minimum space to be left between the right of the parent bounds and the node. Applicable, if the parent is a container.

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = {type: "swimlane",name: "swimlane", offsetX:300, offsetY:200,
lanes:[{name:"lane1", width:200 , 
      children:[{name:"process1", width: 50, height: 50, marginRight: 10 }]
 }]}
$("#DiagramContent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.marginTop `Number`
{:#members:nodes-margintop}

Defines the minimum space to be left between the top of parent bounds and the node. Applicable, if the parent is a container.

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = {type: "swimlane",name: "swimlane", offsetX:300, offsetY:200,
lanes:[{name:"lane1", width:200 , 
      children:[{name:"process1", width: 50, height: 50, marginTop: 10 }]
 }]}
$("#DiagramContent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.maxHeight `Number`
{:#members:nodes-maxheight}

Defines the maximum height limit of the node

#### Default Value

* undefined

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, maxHeight: 100}];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.maxWidth `Number`
{:#members:nodes-maxwidth}

Defines the maximum width limit of the node

#### Default Value

* undefined

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, maxWidth: 100}];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.minHeight `Number`
{:#members:nodes-minheight}

Defines the minimum height limit of the node

#### Default Value

* undefined

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, minHeight: 10 }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.minWidth `Number`
{:#members:nodes-minwidth}

Defines the minimum width limit of the node

#### Default Value

* undefined

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, minWidth: 10 }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.name `String`
{:#members:nodes-name}

Sets the unique identifier of the node

#### Default Value

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50 }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.offsetX `Number`
{:#members:nodes-offsetx}

Defines the position of the node on X-Axis

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50 }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.offsetY `Number`
{:#members:nodes-offsety}

Defines the position of the node on Y-Axis

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50 }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.opacity `Number`
{:#members:nodes-opacity}

Defines the opaque of the node

#### Default Value

* 1

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, opacity:0.7 }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.orientation `String`
{:#members:nodes-orientation}

Defines the orientation of nodes. Applicable, if the node is a swimlane.

#### Default Value

* "vertical"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = { type: "swimlane",name: "swimlane", offsetX:300, offsetY:100, orientation:"horizontal" };
$("#DiagramContent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.outEdges `Array`
{:#members:nodes-outedges}

A read only collection of outgoing connectors/edges of the node

#### Default Value

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connectors = [{ name: "connector1", sourceNode: "Node1", targetNode: "Node2"}];
nodes=[{outEdges:connectors}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.paddingBottom `Number`
{:#members:nodes-paddingbottom}

Defines the minimum padding value to be left between the bottom most position of a group and its children. Applicable, if the group is a container.

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
var node1 = { name: "node1", width: 50, height:50};
var node2 = { name: "node2", width: 50, height:50, verticalAlign: "bottom"};
var group = { name :"group", children:[ node1, node2 ], 
              container: { type: "canvas" }, offsetX:200, offsetY:100, 
              fillColor:"gray", minWidth:200, minHeight:200,
              paddingBottom:10
            };
$("#DiagramContent").ejDiagram({nodes:[group]});
</script>

{% endhighlight %}

### nodes.paddingLeft `Number`
{:#members:nodes-paddingleft}

Defines the minimum padding value to be left between the left most position of a group and its children. Applicable, if the group is a container.

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
var node1 = { name: "node1", width: 50, height:50};
var node2 = { name: "node2", width: 50, height:50, horizontalAlign: "right"};
var group = { name :"group", children:[ node1, node2 ], 
              container: { type: "canvas" }, offsetX:200, offsetY:100, 
              fillColor:"gray", minWidth:200, minHeight:200,
              paddingLeft:10
            };
$("#DiagramContent").ejDiagram({nodes:[group]});
</script>

{% endhighlight %}

### nodes.paddingRight `Number`
{:#members:nodes-paddingright}

Defines the minimum padding value to be left between the right most position of a group and its children. Applicable, if the group is a container.

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
var node1 = { name: "node1", width: 50, height:50};
var node2 = { name: "node2", width: 50, height:50, horizontalAlign: "right"};
var group = { name :"group", children:[ node1, node2 ], 
              container: { type: "canvas" }, offsetX:200, offsetY:100, 
              fillColor:"gray", minWidth:200, minHeight:200,
              paddingRight:10
            };
$("#DiagramContent").ejDiagram({nodes:[group]});
</script>

{% endhighlight %}

### nodes.paddingTop `Number`
{:#members:nodes-paddingtop}

Defines the minimum padding value to be left between the top most position of a group and its children. Applicable, if the group is a container.

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
var node1 = { name: "node1", width: 50, height:50};
var node2 = { name: "node2", width: 50, height:50, verticalAlign: "bottom"};
var group = { name :"group", children:[ node1, node2 ], 
              container: { type: "canvas" }, offsetX:200, offsetY:100, 
              fillColor:"gray", minWidth:200, minHeight:200,
              paddingTop:10
            };
$("#DiagramContent").ejDiagram({nodes:[group]});
</script>

{% endhighlight %}

### nodes.parent `String`
{:#members:nodes-parent}

Sets the name of the parent group

#### Default Value

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
//Sets the group name as parent
var node1 = { name: "node1", width: 50, height:50, offsetX:50, offsetY:50, parent:"group" };
var node2 = { name: "node2", width: 50, height:50, offsetX:150, offsetY:150, parent :"group" };

var group = { name :"group", children:["node1", "node2"] };
$("#DiagramContent").ejDiagram({nodes:[node1, node2, group]});
</script>

{% endhighlight %}

### nodes.pathData `String`
{:#members:nodes-pathdata}

Sets the path geometry that defines the shape of a path node

#### Default Value

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
      type:"basic", shape:"path", pathData: "M370.9702,194.9961L359.5112,159.7291L389.5112,137.9341L419.5112,159.7291L408.0522,194.9961L370.9702,194.9961z" }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.phases `Array`
{:#members:nodes-phases}

An array of objects, where each object represents a smaller region(phase) of a swimlane.

#### Default Value

* []

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = { type: "swimlane",name: "swimlane", offsetX:300, offsetY:100, 
width: 300, orientation:"horizontal",
phases:[{ name:"phase1", offset:150, label:{text:"Phase1"}},    
       { name:"phase2", label:{ text:"Phase2"} }]};
$("#DiagramContent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.phases.label `Object`
{:#members:nodes-phases-label}

Defines the header of the smaller regions

#### Default Value

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = { type: "swimlane",name: "swimlane", offsetX:300, offsetY:100, 
width: 300, orientation:"horizontal",
phases:[{ name:"phase1", offset:150, label:{text:"Phase1"}},    
       { name:"phase2", label:{ text:"Phase2"} }]};
$("#DiagramContent").ejDiagram({nodes:[swimlane]});

</script>

{% endhighlight %}

### nodes.phases.lineColor `String`
{:#members:nodes-phases-linecolor}

Defines the line color of the splitter, that splits different phases.

#### Default Value

* "#606060"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = { type: "swimlane",name: "swimlane", offsetX:300, offsetY:100, 
width: 300, orientation:"horizontal",
phases:[{ name:"phase1", offset:150, label:{text:"Phase1"}, lineColor:"green"},    
       { name:"phase2", label:{ text:"Phase2"} }]};
$("#DiagramContent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.phases.lineDashArray `String`
{:#members:nodes-phases-linedasharray}

Sets the dash array that used to stroke the phase splitter

#### Default Value

* "3,3"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = { type: "swimlane",name: "swimlane", offsetX:300, offsetY:100, 
width: 300, orientation:"horizontal",
phases:[{ name:"phase1", offset:150, label:{text:"Phase1"}, lineDashArray:"2,2"},    
       { name:"phase2", label:{ text:"Phase2"} }]};
$("#DiagramContent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.phases.lineWidth `Number`
{:#members:nodes-phases-linewidth}

Sets the lineWidth of the phase

#### Default Value

* 1

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = { type: "swimlane",name: "swimlane", offsetX:300, offsetY:100, 
width: 300, orientation:"horizontal",
phases:[{ name:"phase1", offset:150, label:{text:"Phase1"}, lineWidth:3 },    
       { name:"phase2", label:{ text:"Phase2"} }]};
$("#DiagramContent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.phases.name `String`
{:#members:nodes-phases-name}

Sets the unique identifier of the phase

#### Default Value

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = { type: "swimlane",name: "swimlane", offsetX:300, offsetY:100, 
width: 300, orientation:"horizontal",
phases:[{ name:"phase1", label:{text:"Phase1"}, lineWidth:3 } ]};
$("#DiagramContent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.phases.offset `Number`
{:#members:nodes-phases-offset}

Sets the length of the smaller region(phase) of a swimlane

#### Default Value

* undefined

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", phases:[{offset: 100}]}});
</script>

{% endhighlight %}

### nodes.phases.orientation `String`
{:#members:nodes-phases-orientation}

Sets the orientation of the phase. Applicable if type is lane.

#### Default Value

* "horizontal"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = { type: "swimlane",name: "swimlane", offsetX:300, offsetY:100, 
width: 300, orientation:"horizontal",
phases:[{ name:"phase1", offset:150, label:{text:"Phase1"} },    
       { name:"phase2", label:{ text:"Phase2"} }]};
$("#DiagramContent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.phases.parent `String`
{:#members:nodes-phases-parent}

Sets the parent of the phase.

#### Default Value

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", phases:[{parent: "parent"}]}});
</script>

{% endhighlight %}

### nodes.phases.type `String`
{:#members:nodes-phases-type}

Sets the type of the object as phase

#### Default Value

* "phase"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>

</script>

{% endhighlight %}

### nodes.phaseSize `Number`
{:#members:nodes-phasesize}

Sets the height of the phase headers

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = { type: "swimlane",name: "swimlane", offsetX:300, offsetY:100, 
width: 300, orientation:"horizontal",phaseSize:50,
phases:[{ name:"phase1", offset:150, label:{text:"Phase 1"} }] };
$("#DiagramContent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.pivot `Point`
{:#members:nodes-pivot}

Sets the ratio/ fractional value relative to node, based on which the node will be transformed(positioning, scaling and rotation) 

#### Default Value

* Points(0.5,0.5)

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
//The node will be transformed with respect to its top left corner
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, pivot: {x:0, y:0}}];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.points `Array`
{:#members:nodes-points}

Defines a collection of points to draw a polygon. Applicable, if the shape is a polygon.

#### Default Value

* []

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50,
type: "basic",shape:"polygon", points:[{ x: 0, y: 12.5 }, { x: 0, y: 50 }, { x: 50, y: 50 }, { x: 50, y: 0 }, { x: 12.5, y: 0 }, { x: 0, y: 12.5 }]}];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.ports `Array`
{:#members:nodes-ports}

An array of objects where each object represents a port

#### Default Value

* []

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50,
      ports:[{name:"port1", offset:{ x:0.5, y:0 }}, 
            {name:"port2", offset:{ x:0.5, y:1 }}]}];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.ports.borderColor `String`
{:#members:nodes-ports-bordercolor}

Sets the border color of the port

#### Default Value

* "#1a1a1a"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50,
      ports:[{name:"port1", offset:{ x:0.5, y:0.5 }, borderColor:"yellow" }] }];
$("#DiagramContent").ejDiagram({nodes:nodes});

</script>

{% endhighlight %}

### nodes.ports.borderWidth `Number`
{:#members:nodes-ports-borderwidth}

Sets the stroke width of the port

#### Default Value

* 1

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50,
      ports:[{name:"port1", offset:{ x:0.5, y:0.5 }, borderColor:"yellow", borderWidth: 3 }] }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.ports.connectorPadding `Number`
{:#members:nodes-ports-connectorpadding}

Defines the space to be left between the port bounds and its incoming and outgoing connections.

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50,
      ports:[{name:"port1", offset:{ x:0.5, y:0.5 }, connectorPadding:10 }] }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.ports.constraints `enum`
{:#members:nodes-ports-constraints}

Defines whether connections can be created with the port See <a href="global.html#portconstraints">PortConstraints</a>

#### Default Value

* PortConstraints.Connect

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var PortConstraints = ej.datavisualization.Diagram.PortConstraints;
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50,
	  //Disable creating connections with the port
      ports:[{name:"port1", offset:{ x:0.5, y:0.5 }, constraints: PortConstraints.Default &~ PortConstraints.Connect }] }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.ports.fillColor `String`
{:#members:nodes-ports-fillcolor}

Sets the fill color of the port

#### Default Value

* "white"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50,
      ports:[{name:"port1", offset:{ x:0.5, y:0.5 }, fillColor:"red" }] }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.ports.name `String`
{:#members:nodes-ports-name}

Sets the unique identifier of the port

#### Default Value

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50,
      ports:[{ name:"port1", offset:{ x:0.5, y:0.5 } }] }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.ports.offset `Point`
{:#members:nodes-ports-offset}

Defines the position of the port as fraction/ ratio relative to node

#### Default Value

* Point(0, 0)

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50,
	  //Add port at the center of the node
      ports:[{name:"port1", offset:{ x:0.5, y:0.5 } }] }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.ports.pathData `String`
{:#members:nodes-ports-pathdata}

Defines the path data to draw the port. Applicable, if the port `shape` is path.

#### Default Value

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50,
      ports:[{name:"port1", offset:{ x:0.5, y:0.5 }, 
      //Define the shape of the port
      shape:"path", pathData: "M5,0 L10,10 L0,10 z"}] }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.ports.shape `enum`
{:#members:nodes-ports-shape}

Defines the shape of the port. See <a href="global.html#portshapes">PortShapes</a>

#### Default Value

* PortShapes.Square

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50,
      ports:[{name:"port1", offset:{ x:0.5, y:0.5 }, 
      shape:ej.datavisualization.Diagram.PortShapes.Circle}] }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.ports.size `Number`
{:#members:nodes-ports-size}

Defines the size of the port

#### Default Value

* 8

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50,
      ports:[{name:"port1", offset:{ x:0.5, y:0.5 }, size: 10}] }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.ports.visibility `enum`
{:#members:nodes-ports-visibility}

Defines when the port should be visible .See <a href="global.html#portvisibility">PortVisibility</a>

#### Default Value

* PortVisibility.Default

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50,
      ports:[{name:"port1", offset:{ x:0.5, y:0.5 }, 
      visibility:ej.datavisualization.Diagram.PortVisibility.Visible }] }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.rotateAngle `Number`
{:#members:nodes-rotateangle}

Sets the angle to which the node should be rotated

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, rotateAngle: 45 }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.shadow `Object`
{:#members:nodes-shadow}

Defines the opacity and the position of shadow

#### Default Value

* Diagram.Shadow()

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var NodeConstraints = ej.datavisualization.Diagram.NodeConstraints;
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50,
      constraints: NodeConstraints.Default | NodeConstraints.Shadow,
      shadow: {opacity: 0.5, distance: 10, angle: 45} }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.shadow.angle `Number`
{:#members:nodes-shadow-angle}

Defines the angle of the shadow relative to node

#### Default Value

* 45

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var NodeConstraints = ej.datavisualization.Diagram.NodeConstraints;
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50,
      constraints: NodeConstraints.Default | NodeConstraints.Shadow,
      shadow: { angle: 135} }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.shadow.distance `Number`
{:#members:nodes-shadow-distance}

Sets the distance to move the shadow relative to node

#### Default Value

* 5

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var NodeConstraints = ej.datavisualization.Diagram.NodeConstraints;
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50,
      constraints: NodeConstraints.Default | NodeConstraints.Shadow,
      shadow: { distance: 10 } }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.shadow.opacity `Number`
{:#members:nodes-shadow-opacity}

Defines the opaque of the shadow

#### Default Value

* 0.7

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var NodeConstraints = ej.datavisualization.Diagram.NodeConstraints;
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50,
      constraints: NodeConstraints.Default | NodeConstraints.Shadow,
      shadow: {opacity: 0.9 } }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.shape `enum`
{:#members:nodes-shape}

Sets the shape of the node. It depends upon the type of node. See {Link Shapes}

#### Default Value

* "rectangle"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
	  // Sets the shape as ellipse
      type:"basic", shape:ej.datavisualization.Diagram.BasicShapes.Ellipse }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.source `String`
{:#members:nodes-source}

Sets the source path of the image. Applicable, if the type of the node is image.

#### Default Value

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
type:"image", source: "Clayton.png" }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.subProcess `Object`
{:#members:nodes-subprocess}

Defines the sub process of a BPMN Activity. Applicable, if the type of the bpmn activity is sub process.

#### Default Value

* Diagram.BPMNSubProcess()

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
		type:"bpmn", shape:"activity", activity:"subprocess", 
		subProcess:{ loop: ej.datavisualization.Diagram.BPMNLoops.Standard } }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.subProcess.adhoc `Boolean`
{:#members:nodes-subprocess-adhoc}

Defines whether the bpmn sub process is without any prescribed order or not

#### Default Value

* false

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
type:"bpmn", shape:"activity", activity:"subprocess", 
subProcess:{ adhoc: true } }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.subProcess.boundary `enum`
{:#members:nodes-subprocess-boundary}

Sets the boundary of the BPMN process See <a href="global.html#bpmnboundary">BPMNBoundary</a>

#### Default Value

* ej.datavisualization.Diagram.BPMNBoundary.Default

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
		type:"bpmn", shape:"activity", activity:"subprocess", 
		subProcess:{ boundary: ej.datavisualization.Diagram.BPMNBoundary.Call } }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.subProcess.compensation `Boolean`
{:#members:nodes-subprocess-compensation}

Sets whether the bpmn subprocess is triggered as a compensation of a specific activity

#### Default Value

* false

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
		type:"bpmn", shape:"activity", activity:"subprocess", 
		subProcess:{ compensation: true } }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.subProcess.loop `enum`
{:#members:nodes-subprocess-loop}

Defines the loop type of a sub process .See <a href="global.html#bpmnloops">BPMNLoops</a>

#### Default Value

* ej.datavisualization.Diagram.BPMNLoops.None

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
type:"bpmn", shape:"activity", activity:"subprocess", 
subProcess:{ loop: ej.datavisualization.Diagram.BPMNLoops.ParallelMultiInstance} }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.task `Object`
{:#members:nodes-task}

Defines the task of the bpmn activity. Applicable, if the type of activity is set as task

#### Default Value

* Diagram.BPMNTask()

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
		type:"bpmn", shape:"activity", activity:"task", 
		task:{ compensation: true } }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.tasks.call `Boolean`
{:#members:nodes-tasks-call}

To set whether the task is a global task or not

#### Default Value

* false

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
		type:"bpmn", shape:"activity", activity:"task", 
		task:{ call: true } }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.tasks.compensation `Boolean`
{:#members:nodes-tasks-compensation}

Sets whether the task is triggered as a compensation of another specific activity

#### Default Value

* false

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
		type:"bpmn", shape:"activity", activity:"task", 
		task:{ compensation: true } }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.tasks.loop `enum`
{:#members:nodes-tasks-loop}

Sets the loop type of a bpmn task .See <a href="global.html#BPMNLoops">BPMNLoops</a>

#### Default Value

* ej.datavisualization.Diagram.BPMNLoops.None

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
		type:"bpmn", shape:"activity", activity:"task", 
		task:{ loop: ej.datavisualization.Diagram.BPMNLoops.Standard } }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.tasks.type `enum`
{:#members:nodes-tasks-type}

Sets the type of the BPMN task. See <a href="global.html#bpmntasks">BPMNTasks</a>

#### Default Value

* ej.datavisualization.Diagram.BPMNTasks.None

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
		type:"bpmn", shape:"activity", activity:"task", 
		task:{ type: ej.datavisualization.Diagram.BPMNTasks.Service } }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.templateId `String`
{:#members:nodes-templateid}

Sets the id of svg/html templates. Applicable, if the node is html or native.

#### Default Value

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>

<script id="svgTemplate" type="text/x-jsrender">
    <svg version="1.0" xmlns="http://www.w3.org/2000/svg" width="70px" height="30px">
        <g visibility="visible">
            <image width="70px" height="35px" opacity="1" xmlns:xlink="http://www.w3.org/1999/xlink" xlink:href="{{:addInfo.source}}"></image>
            <text x="25" y="20" font-size="11" style="height:30px">
                <tspan>{{:name}}</tspan>
            </text>
        </g>
    </svg>
</script>
	
<script>
var nodes;
nodes=[{ name: "Clayton", width: 100, height:50, offsetX:50, offsetY:50, 
		addInfo:{source:"clayton.png"},
		type:"native", templateId:"svgTemplate" }];
$("#DiagramContent").ejDiagram({nodes:nodes});

</script>

{% endhighlight %}

### nodes.textBlock `Number`
{:#members:nodes-textblock}

Defines the textBlock of a text node

#### Default Value

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
		type:"text", textBlock:{ text: "Text Node", fontColor:"red" } }];
$("#DiagramContent").ejDiagram({nodes:nodes});

</script>

{% endhighlight %}

### nodes.trigger `enum`
{:#members:nodes-trigger}

Sets the type of BPMN Event Triggers. See <a href="global.html#bpmntriggers">BPMNTriggers</a>

#### Default Value

* ej.datavisualization.Diagram.BPMNTriggers.None

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{type: "bpmn", shape: ej.datavisualization.Diagram.BPMNShapes.Event, trigger: ej.datavisualization.Diagram.BPMNTriggers.None}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.type `enum`
{:#members:nodes-type}

Defines the type of the node. See <a href="global.html#shapes">Shapes</a>

#### Default Value

* ej.datavisualization.Diagram.Shapes.Basic

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
		type: ej.datavisualization.Diagram.Shapes.BPMN }];
$("#DiagramContent").ejDiagram({nodes:nodes})
</script>

{% endhighlight %}

### nodes.verticalAlign `VerticalAlignment`
{:#members:nodes-verticalalign}

Sets the vertical aligment of a node. Applicable, if the parent of a node is a container.

#### Default Value

* VerticalAlignment.Top

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
var node1 = { name: "node1", width: 50, height:50};
var node2 = { name: "node2", width: 50, height:50, verticalAlign: "bottom"};
var group = { name :"group", children:[ node1, node2 ], 
              container: { type: "canvas" }, offsetX:200, offsetY:100, 
              fillColor:"gray", minWidth:200, minHeight:200
            };
$("#DiagramContent").ejDiagram({nodes:[group]});
</script>

{% endhighlight %}

### nodes.visible `Boolean`
{:#members:nodes-visible}

Defines the visibility of the node

#### Default Value

* true

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, visible:false }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.width `Number`
{:#members:nodes-width}

Defines the width of the node

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:50, offsetX:50, offsetY:50 }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.zOrder `Number`
{:#members:nodes-zorder}

Defines the z-index of the node

#### Default Value

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, zOrder: 10 }];
$("#DiagramContent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodeTemplate `Object`
{:#members:nodetemplate}

To customize the node properties before rendering the node.

#### Default Value

* null

#### Example

{% highlight html %}

<div id="diagram"></div>
<script>
function nodeTemplate(diagram, node) {node.labels[0].text = node.Name};
$("#diagram").ejDiagram({ nodeTemplate:nodeTemplate});
</script>

{% endhighlight %}

### pageSettings
{:#members:pagesettings}

To define the page settings of diagram

### pageSettings.multiplePage `Boolean`
{:#members:pagesettings-multiplepage}

To set whether the number of pages can be extended based on the region covered by elements

#### Default Value

* false

#### Example

{% highlight html %}

//multiplePage of the diagram
$("#diagramContent").ejDiagram({pageSettings: {multiplePage: false}});

{% endhighlight %}

### pageSettings.pageBackgroundColor `String`
{:#members:pagesettings-pagebackgroundcolor}

To set the background color of page

#### Default Value

* "#ffffff"

#### Example

{% highlight html %}

//pageBackgroundColor of the diagram
$("#diagramContent").ejDiagram({pageSettings: {pageBackgroundColor: "#ffffff"}});

{% endhighlight %}

### pageSettings.pageBorderColor `String`
{:#members:pagesettings-pagebordercolor}

To set the border color of page

#### Default Value

* "#565656"

#### Example

{% highlight html %}

//pageBorderColor of the diagram
$("#diagramContent").ejDiagram({pageSettings: {pageBorderColor: "#565656"}});

{% endhighlight %}

### pageSettings.pageBorderWidth `Number`
{:#members:pagesettings-pageborderwidth}

To set the border width of the page

#### Default Value

* 0

#### Example

{% highlight html %}

//pageBorderWidth of the diagram
$("#diagramContent").ejDiagram({pageSettings: {pageBorderWidth: 3}});

{% endhighlight %}

### pageSettings.pageHeight `Number`
{:#members:pagesettings-pageheight}

To set the height of the page

#### Default Value

* null

#### Example

{% highlight html %}

//pageHeight of the diagram
$("#diagramContent").ejDiagram({pageSettings: {pageHeight: 4500}});

{% endhighlight %}

### pageSettings.pageMargin `Number`
{:#members:pagesettings-pagemargin}

To set the margin of page

#### Default Value

* 24

#### Example

{% highlight html %}

//pageMargin of the diagram
$("#diagramContent").ejDiagram({pageSettings: {pageMargin: 24}});

{% endhighlight %}

### pageSettings.pageWidth `Number`
{:#members:pagesettings-pagewidth}

To set the width of the page

#### Default Value

* null

#### Example

{% highlight html %}

//pageWidth
$("#diagramContent").ejDiagram({pageSettings: {pageWidth: 4500}});

{% endhighlight %}

### pageSettings.showPageBreak `Boolean`
{:#members:pagesettings-showpagebreak}

Enables or disables the page breaks in diagram

#### Default Value

* false

#### Example

{% highlight html %}

//showPageBreak of the diagram
$("#diagramContent").ejDiagram({pageSettings: {showPageBreak: false}});

{% endhighlight %}

### selectedItems `Object`
{:#members:selecteditems}

The object to define the behavior of the selected items

### selectedItems.constraints `enum`
{:#members:selecteditems-constraints}

Sets the visible items of selector see <a href="global.html#SelectorConstraints">SelectorConstraints</a>

#### Default Value

* SelectorConstraints.All

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramContent").ejDiagram({selectedItems:{constraints: ej.datavisualization.Diagram.SelectorConstraints.None} }});
</script>

{% endhighlight %}

### selectedItems.height `Number`
{:#members:selecteditems-height}

Sets the height of the selected items

#### Default Value

* 0

#### Example

{% highlight html %}

$("#diagramContent").ejDiagram({selectedItems: {height: 50}});

{% endhighlight %}

### selectedItems.offsetX `Number`
{:#members:selecteditems-offsetx}

Defines the X co-ordinate of the selected item

#### Default Value

* 0

#### Example

{% highlight html %}

$("#diagramContent").ejDiagram({selectedItems: {offsetX: 50}});

{% endhighlight %}

### selectedItems.offsetY `Number`
{:#members:selecteditems-offsety}

Defines the Y co-ordinate of the selected item

#### Default Value

* 0

#### Example

{% highlight html %}

$("#diagramContent").ejDiagram({selectedItems: {offsetY: 50}});

{% endhighlight %}

### selectedItems.rotateAngle `Number`
{:#members:selecteditems-rotateangle}

Sets the rotation angle of the selected items.

#### Default Value

* 0

#### Example

{% highlight html %}

$("#diagramContent").ejDiagram({selectedItems: {rotateAngle: 50}});

{% endhighlight %}

### selectedItems.userHandles `Array`
{:#members:selecteditems-userhandles}

To add frequently using commands around selector

#### Default Value

* []

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var userHandle= [];
function createUserHandles() {
var cloneHandle = ej.datavisualization.Diagram.UserHandle();
userhandle.push(cloneHandles);
}
$("#diagramcontent").ejDiagram({selectedItems:{userHandles:userHandle}});
</script>

{% endhighlight %}

### selectedItems.width `Number`
{:#members:selecteditems-width}

Sets the width of the selected items

#### Default Value

* 0

#### Example

{% highlight html %}

$("#diagramContent").ejDiagram({selectedItems: {width: 50}});

{% endhighlight %}

### showTooltip `Boolean`
{:#members:showtooltip}

Enables or disables tooltip of diagram

#### Default Value

* true

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({showTooltip: true});
</script>

{% endhighlight %}

### snapSettings `Object`
{:#members:snapsettings}

Specifies the snap settings of the diagram.

### snapSettings.enableSnapToObject `Boolean`
{:#members:snapsettings-enablesnaptoobject}

Enables or disables the snap to object

#### Default Value

* true

#### Example

{% highlight html %}

var snap = {"enableSnapToObject":true};
//enableSnapToObject:
$("#diagramContent").ejDiagram({snapSettings: snap});

{% endhighlight %}

### snapSettings.horizontalGridLines `Object`
{:#members:snapsettings-horizontalgridlines}

Specifies the settings of horizontal grid lines.

### snapSettings.horizontalGridLines.lineColor `String`
{:#members:snapsettings-horizontalgridlines-linecolor}

Sets the line color for horizontal gridlines

#### Default Value

* "lightgray"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var gridline = { "snapConstraints":"lineColor": "blue" };
//Linecolor of the horizontal gridlines
$("#diagramContent").ejDiagram({snapSettings: { horizontalGridLines: gridline} });
</script>

{% endhighlight %}

### snapSettings.horizontalGridLines.lineDashArray `String`
{:#members:snapsettings-horizontalgridlines-linedasharray}

Specifies the pattern of dashes and gaps used to stroke horizontal grid lines

#### Default Value

* "0"

#### Example

{% highlight html %}

<div id="diagram"></div>
<script>
$("#diagram").ejDiagram({ snapSettings: { horizontalGridLines: { lineDashArray: "2 2"}}});
</script>

{% endhighlight %}

### snapSettings.horizontalGridLines.linesInterval `Array`
{:#members:snapsettings-horizontalgridlines-linesinterval}

Specifies pattern of lines and gaps of horizontal gridlines

#### Default Value

* [1.25, 18.75, 0.25, 19.75, 0.25, 19.75, 0.25, 19.75, 0.25, 19.75]

#### Example

{% highlight html %}

<div id="diagram"></div>
<script>
$("#diagram").ejDiagram({ snapSettings: {
horizontalGridLines: { linesInterval: [1, 14, 0.25, 15, 0.25, 15, 0.25, 15, 0.25, 15] }
}});
</script>

{% endhighlight %}

### snapSettings.horizontalGridLines.snapInterval `Array`
{:#members:snapsettings-horizontalgridlines-snapinterval}

Specifies the snap intervals of horizontal grid lines.

#### Default Value

* [20]

#### Example

{% highlight html %}

<div id="diagram"></div>
<script>
$("#diagram").ejDiagram({ snapSettings: { horizontalGridLines: { snapInterval: [10] }}});
</script>

{% endhighlight %}

### snapSettings.snapAngle `Number`
{:#members:snapsettings-snapangle}

The Angle by which the object to be snapped

#### Default Value

* 5

#### Example

{% highlight html %}

var snap = {"snapAngle":5};
//enableSnapToObject:
$("#diagramContent").ejDiagram({snapSettings: snap});

{% endhighlight %}

### snapSettings.snapObjectDistance `Number`
{:#members:snapsettings-snapobjectdistance}

Relative distance between the nearer object and selected object

#### Default Value

* 5

#### Example

{% highlight html %}

var snap = {"snapObjectDistance":5};
//snapObjectDistance
$("#diagramContent").ejDiagram({snapSettings: snap});

{% endhighlight %}

### snapSettings.verticalGridLines `Object`
{:#members:snapsettings-verticalgridlines}

Specifies the settings of vertical grid lines.

### snapSettings.verticalGridLines.lineColor `String`
{:#members:snapsettings-verticalgridlines-linecolor}

Sets the line color of vertical gridlines

#### Default Value

* "lightgray"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var gridline = { "snapConstraints":"lineColor": "blue" };
//Linecolor of the vertical gridlines
$("#diagramContent").ejDiagram({snapSettings: { verticalGridLines: gridline} });
</script>

{% endhighlight %}

### snapSettings.verticalGridLines.lineDashArray `String`
{:#members:snapsettings-verticalgridlines-linedasharray}

Specifies the pattern of dashes and gaps used to stroke vertical grid lines

#### Default Value

* "0"

#### Example

{% highlight html %}

<div id="diagram"></div>
<script>
$("#diagram").ejDiagram({ snapSettings: { verticalGridLines: { lineDashArray: "2 2"}}});
</script>

{% endhighlight %}

### snapSettings.verticalGridLines.linesInterval `Array`
{:#members:snapsettings-verticalgridlines-linesinterval}

Specifies pattern of lines and gaps of vertical gridlines

#### Default Value

* [1.25, 18.75, 0.25, 19.75, 0.25, 19.75, 0.25, 19.75, 0.25, 19.75]

#### Example

{% highlight html %}

<div id="diagram"></div>
<script>
$("#diagram").ejDiagram({ snapSettings: {
verticalGridLines: { linesInterval: [1, 14, 0.25, 15, 0.25, 15, 0.25, 15, 0.25, 15] }
}});
</script>

{% endhighlight %}

### snapSettings.verticalGridLines.snapInterval `Array`
{:#members:snapsettings-verticalgridlines-snapinterval}

Specifies the snap intervals for vertical grid lines.

#### Default Value

* [20]

#### Example

{% highlight html %}

<div id="diagram"></div>
<script>
$("#diagram").ejDiagram({ snapSettings: { verticalGridLines: { snapInterval: [10] }}});
</script>

{% endhighlight %}

### tool `enum`
{:#members:tool}

Sets the default behavior of the diagram see<a href="global.html#Tool">Tool</a>

#### Default Value

* Tool.All

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramContent").ejDiagram({tool: ej.datavisualization.Diagram.Tool.Default} });
</script>

{% endhighlight %}

### tooltipTemplateId `String`
{:#members:tooltiptemplateid}

To set custom style for tool tip of diagram

#### Default Value

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script type="text/x-jsrender" id="toolTipId">
<span >{{:offsetX}}{{:x}}{{:offsetY}}{{:y}}
</span>
</script>
<script>
$("#diagramcontent").ejDiagram({ tooltipTemplateId: "toolTipId"});
</script>

{% endhighlight %}

### version `String`
{:#members:version}

Sets the version of the diagram

#### Default Value

* "13.1"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram("instance");
</script>

{% endhighlight %}

### width `String`
{:#members:width}

Specifies the width of the diagram.

#### Default Value

* null

#### Example

{% highlight html %}

<div id="diagram"></div>
<script>
$("#diagram").ejDiagram({ width:"100%" });
</script>

{% endhighlight %}

### zoomFactor `Number`
{:#members:zoomfactor}

Sets the factor by which we can zoom in or zoom out

#### Default Value

* 0.2

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramContent").ejDiagram({zoomFactor: 1});
</script>

{% endhighlight %}

## Methods

### add(node)
{:#methods:add}

Add nodes and connectors to diagram at runtime

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">node</td>
			<td class="type">Object</td>
			<td class="description">a JSON to define a node/connector or an array of nodes and connector</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram = $("#diagramcontent").ejDiagram("instance");
//add a single node to diagram
var BasicShapes = ej.datavisualization.Diagram.BasicShapes;
var node = { name: "rectangle1", width: 100, height: 100, offsetX: 100, offsetY: 100, type: "node", shape: BasicShapes.Rectangle };
diagram.add(node);
// add multiple nodes to diagram
var nodes = [
{ name: "rectangle2", width: 100, height: 100, offsetX: 200, offsetY: 100, type: "node", shape: BasicShapes.Rectangle },
{ name: "ellipse1", width: 100, height: 100, offsetX: 300, offsetY: 100, type: "node", shape: BasicShapes.Ellipse },
]
diagram.add(nodes);
</script>

{% endhighlight %}

### addLabel(nodeName, newLabel)
{:#methods:addlabel}

Add a label to a node at runtime

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">nodeName</td>
			<td class="type">string</td>
			<td class="description">name of the node to which label will be added</td>
		</tr>
		<tr>
			<td class="name">newLabel</td>
			<td class="type">Object</td>
			<td class="description">JSON for the new label to be added</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
var node=diagram.selectionList[0];
diagram.addLabel(node.name, {fontColor:"red", text:"newLabel"});
</script>

{% endhighlight %}

### addPhase(name, options)
{:#methods:addphase}

Add a phase to a swimlane at runtime

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">name</td>
			<td class="type">String</td>
			<td class="description">name of the swimlane to which the phase will be added</td>
		</tr>
		<tr>
			<td class="name">options</td>
			<td class="type">Object</td>
			<td class="description">JSON object to define the phase to be added</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.addPhase("swimlane", { name: "CustomPhase", offset: 600, label: { text: "CustomPhase" } });
</script>

{% endhighlight %}

### addPorts(name, ports)
{:#methods:addports}

Add a collection of ports to the node specified by name

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">name</td>
			<td class="type">String</td>
			<td class="description">name of the node to which the ports have to be added</td>
		</tr>
		<tr>
			<td class="name">ports</td>
			<td class="type">Array</td>
			<td class="description">a collection of ports to be added to the specified node</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram = $("#diagramcontent").ejDiagram("instance");
var port = [{ offset: { x: 0, y: 0.5 }, name: "aport", fillColor: "yellow"}, { offset: { x: 0.5, y: 0.5 }, name: "bport", fillColor: "yellow", }];
diagram.addPorts("Rect1", port);
</script>

{% endhighlight %}

### addSelection(node, \[clearSelection\])
{:#methods:addselection}

Add the specified node to selection list

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">node</td>
			<td class="type">Object</td>
			<td class="description">the node to be selected</td>
		</tr>
		<tr>
			<td class="name">clearSelection</td>
			<td class="type">Boolean [optional]</td>
			<td class="description">to define whether to clear the existing selection or not</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
var node=diagram.model.nodes[0];
diagram.addSelection(node);
</script>

{% endhighlight %}

### align(direction)
{:#methods:align}

Align the selected objects based on the reference object and direction

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">direction</td>
			<td class="type">String</td>
			<td class="description">to specify the direction towards which the selected objects are to be aligned("left","right",top","bottom")</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.align("left");
</script>

{% endhighlight %}

### bringIntoView(rect)
{:#methods:bringintoview}

Bring the specified portion of the diagram content to the diagram viewport

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">rect</td>
			<td class="type">Object</td>
			<td class="description">the rectangular region that is to be brought into diagram viewport</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.bringIntoView(ej.datavisualization.Diagram.Rectangle(700, 500, 80, 80));
</script>

{% endhighlight %}

### bringToCenter(rect)
{:#methods:bringtocenter}

Bring the specified portion of the diagram content to the center of the diagram viewport

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">rect</td>
			<td class="type">Object</td>
			<td class="description">the rectangular region that is to be brought to the center of diagram viewport</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.bringToCenter(ej.datavisualization.Diagram.Rectangle(700, 500, 80, 80));
</script>

{% endhighlight %}

### bringToFront()
{:#methods:bringtofront}

Visually move the selected object over all other intersected objects

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.bringToFront();
</script>

{% endhighlight %}

### clear()
{:#methods:clear}

Remove all the elements from diagram

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.clear();
</script>

{% endhighlight %}

### clearSelection()
{:#methods:clearselection}

Remove the current selection in diagram

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.clearSelection();
</script>

{% endhighlight %}

### copy()
{:#methods:copy}

Copy the selected object to internal clipboard and get the copied object

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
//Save the copied object
var obj = diagram.copy();
</script>

{% endhighlight %}

### cut()
{:#methods:cut}

Cut the selected object from diagram to diagram internal clipboard

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.cut();
</script>

{% endhighlight %}

### exportDiagram(\[options\])
{:#methods:exportdiagram}

Export the diagram as downloadable files or as data

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">options</td>
			<td class="type">Object [optional]</td>
			<td class="description">options to export the desired region of diagram to the desired formats</td>
		</tr>
		<tr>
			<td class="name">options.fileName</td>
			<td class="type">String</td>
			<td class="description">name of the file to be downloaded</td>
		</tr>
		<tr>
			<td class="name">options.format</td>
			<td class="type">String</td>
			<td class="description">format of the exported file/data See <a href="global.html#fileformats">FileFormats</a></td>
		</tr>
		<tr>
			<td class="name">options.mode</td>
			<td class="type">String</td>
			<td class="description">to set whether to export diagram as a file or as raw data See <a href="global.html#exportmodes">ExportModes</a></td>
		</tr>
		<tr>
			<td class="name">options.region</td>
			<td class="type">String</td>
			<td class="description">to set the region of the diagram to be exported See <a href="global.html#region">Region</a></td>
		</tr>
		<tr>
			<td class="name">options.bounds</td>
			<td class="type">Object</td>
			<td class="description">to export any custom region of diagram</td>
		</tr>
		<tr>
			<td class="name">options.margin</td>
			<td class="type">Object</td>
			<td class="description">to set margin to the exported data</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
//Exports the whole diagram content as an image of JPEG format
diagram.exportDiagram();
var options = {
//name of the file to be downloaded
fileName: "diagram",
//Specifies whether to export as files/data
mode: "download",
//Format of the exported file
format: "jpg",
// Define the custom bounds that has to be exported
bounds: { x: 1000, y: 1000, width: 500, height: 500 },
};
diagram.exportDiagram(options);
</script>

{% endhighlight %}

### findNode(name)
{:#methods:findnode}

Read a node/connector object by its name

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">name</td>
			<td class="type">String</td>
			<td class="description">name of the node/connector that is to be identified</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
var node = diagram.findNode("nodeName");
</script>

{% endhighlight %}

### fitToPage(\[mode\], \[region\], \[margin\])
{:#methods:fittopage}

Fit the diagram content into diagram viewport

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">mode</td>
			<td class="type">String [optional]</td>
			<td class="description">to set the mode of fit to command. See <a href="global.html#fitmode">FitMode</a></td>
		</tr>
		<tr>
			<td class="name">region</td>
			<td class="type">String [optional]</td>
			<td class="description">to set whether the region to be fit will be based on diagram elements or page settings <a href="global.html#region">Region</a></td>
		</tr>
		<tr>
			<td class="name">margin</td>
			<td class="type">Object [optional]</td>
			<td class="description">to set the required margin</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.fitToPage(mode,region,margin);
</script>

{% endhighlight %}

### group()
{:#methods:group}

Group the selected nodes and connectors

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.group();
</script>

{% endhighlight %}

### insertLabel(name, label, \[index\])
{:#methods:insertlabel}

Insert a label into a node's label collection at runtime

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">name</td>
			<td class="type">String</td>
			<td class="description">name of the node to which the label has to be inserted</td>
		</tr>
		<tr>
			<td class="name">label</td>
			<td class="type">Object</td>
			<td class="description">JSON to define the new label</td>
		</tr>
		<tr>
			<td class="name">index</td>
			<td class="type">Number [optional]</td>
			<td class="description">index to insert the label into the node</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
var node=diagram.selectionList[0];
diagram.insertLabel(node.name, {fontColor:"red", text:"newLabel"},0);
</script>

{% endhighlight %}

### layout()
{:#methods:layout}

Refresh the diagram with the specified layout

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.layout();
</script>

{% endhighlight %}

### load(data)
{:#methods:load}

Load the diagram

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">data</td>
			<td class="type">Object</td>
			<td class="description">JSON data to load the diagram</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.load(data);
</script>

{% endhighlight %}

### moveForward()
{:#methods:moveforward}

Visually move the selected object over its closest intersected object

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.moveForward();
</script>

{% endhighlight %}

### nudge(direction, \[delta\])
{:#methods:nudge}

Move the selected objects by either one pixel or by the pixels specified through argument

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">direction</td>
			<td class="type">String</td>
			<td class="description">specifies the direction to move the selected objects ("left","right",top","bottom")</td>
		</tr>
		<tr>
			<td class="name">delta</td>
			<td class="type">Number [optional]</td>
			<td class="description">specifies the number of pixels by which the selected objects have to be moved</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.nudge("direction", 5);
</script>

{% endhighlight %}

### paste(\[object\], \[rename\])
{:#methods:paste}

Paste the selected object from internal clipboard to diagram

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">object</td>
			<td class="type">Object [optional]</td>
			<td class="description">object to be added to diagram</td>
		</tr>
		<tr>
			<td class="name">rename</td>
			<td class="type">Boolean [optional]</td>
			<td class="description">to define whether the specified object is to be renamed or not</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
//Paste the object from internal clipboard to diagram
diagram.paste();
//Add the specific object to diagram
diagram.paste(obj, true);
</script>

{% endhighlight %}

### print()
{:#methods:print}

Print the diagram as image

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.print();
</script>

{% endhighlight %}

### redo()
{:#methods:redo}

Restore the last action that was reverted

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.redo();
</script>

{% endhighlight %}

### refresh()
{:#methods:refresh}

Refresh the diagram at runtime

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.refresh();
</script>

{% endhighlight %}

### remove(\[node\])
{:#methods:remove}

Remove either the given node/connector or the selected element from diagram

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">node</td>
			<td class="type">Object [optional]</td>
			<td class="description">the node/connector to be removed from diagram</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.remove();
</script>

{% endhighlight %}

### removeSelection(node)
{:#methods:removeselection}

Remove a particular object from selection list

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">node</td>
			<td class="type">Object</td>
			<td class="description">the node/connector to be removed from selection list</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
var node=diagram.selectionList[0];
diagram.removeSelection(node);
</script>

{% endhighlight %}

### sameHeight()
{:#methods:sameheight}

Scale the selected objects to the height of the first selected object

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.sameHeight();
</script>

{% endhighlight %}

### sameSize()
{:#methods:samesize}

Scale the selected objects to the size of the first selected object

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.sameSize();
</script>

{% endhighlight %}

### sameWidth()
{:#methods:samewidth}

Scale the selected objects to the width of the first selected object

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.sameWidth();
</script>

{% endhighlight %}

### save()
{:#methods:save}

Returns the diagram as serialized JSON

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
var savedDiagram = diagram.save();
</script>

{% endhighlight %}

### scrollToNode(node)
{:#methods:scrolltonode}

Bring the node into view

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">node</td>
			<td class="type">Object</td>
			<td class="description">the node/connector to be brought into view</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
var node = diagram.selectionList[0];
diagram.scrollToNode(node);
</script>

{% endhighlight %}

### selectAll()
{:#methods:selectall}

Select all nodes and connector in diagram

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.selectAll();
</script>

{% endhighlight %}

### sendBackward()
{:#methods:sendbackward}

Visually move the selected object behind its closest intersected object

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.sendBackward();
</script>

{% endhighlight %}

### sendToBack()
{:#methods:sendtoback}

Visually move the selected object behind all other intersected objects

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.sendToBack();
</script>

{% endhighlight %}

### spaceAcross()
{:#methods:spaceacross}

Update the horizontal space between the selected objects as equal and within the selection boundary

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.spaceAcross();
</script>

{% endhighlight %}

### spaceDown()
{:#methods:spacedown}

Update the vertical space between the selected objects as equal and within the selection boundary

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.spaceDown();
</script>

{% endhighlight %}

### startLabelEdit(node, label)
{:#methods:startlabeledit}

Move the specified label to edit mode

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">node</td>
			<td class="type">Object</td>
			<td class="description">node/connector that contains the label to be edited</td>
		</tr>
		<tr>
			<td class="name">label</td>
			<td class="type">Object</td>
			<td class="description">to be edited</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
var node=diagram.selectionList[0];
diagram.startLabelEdit(node,node.labels[0]);
</script>

{% endhighlight %}

### undo()
{:#methods:undo}

Reverse the last action that was performed

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.undo();
</script>

{% endhighlight %}

### ungroup()
{:#methods:ungroup}

Ungroup the selected group

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.ungroup();
</script>

{% endhighlight %}

### update(options)
{:#methods:update}

Update diagram at runtime

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">options</td>
			<td class="type">Object</td>
			<td class="description">JSON to specify the diagram properties that have to be modified</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
var tool = ej.datavisualization.Diagram.Tool.ZoomPan;
//update the tool
diagram.update({ tool: tool });

{% endhighlight %}

### updateConnector(name, options)
{:#methods:updateconnector}

Update Connectors at runtime

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">name</td>
			<td class="type">String</td>
			<td class="description">name of the connector to be updated</td>
		</tr>
		<tr>
			<td class="name">options</td>
			<td class="type">Object</td>
			<td class="description">JSON to specify the connector properties that have to be updated</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.updateConnector("connector1", { lineColor: "red", lineWidth: 3 });
</script>

{% endhighlight %}

### updateLabel(nodeName, label, options)
{:#methods:updatelabel}

Update the given label at runtime

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">nodeName</td>
			<td class="type">String</td>
			<td class="description">the name of node/connector which contains the label to be updated</td>
		</tr>
		<tr>
			<td class="name">label</td>
			<td class="type">Object</td>
			<td class="description">the label to be modified</td>
		</tr>
		<tr>
			<td class="name">options</td>
			<td class="type">Object</td>
			<td class="description">JSON to specify the label properties that have to be updated</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
var node=diagram.selectionList[0];
var label = [];
label =[{"name":"node1" "text": "node", "bold": true, "italic": true}]
diagram.updateLabel(node.name,node.labels[0],label);
</script>

{% endhighlight %}

### updateNode(name, options)
{:#methods:updatenode}

Update nodes at runtime

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">name</td>
			<td class="type">String</td>
			<td class="description">name of the node that is to be updated</td>
		</tr>
		<tr>
			<td class="name">options</td>
			<td class="type">Object</td>
			<td class="description">JSON to specify the properties of node that have to be updated</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.updateNode("node1", { fillColor: "red", borderWidth: "3" });
</script>

{% endhighlight %}

### updatePort(nodeName, port, options)
{:#methods:updateport}

Update a port with its modified properties at runtime

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">nodeName</td>
			<td class="type">String</td>
			<td class="description">the name of node which contains the port to be updated</td>
		</tr>
		<tr>
			<td class="name">port</td>
			<td class="type">Object</td>
			<td class="description">the port to be updated</td>
		</tr>
		<tr>
			<td class="name">options</td>
			<td class="type">Object</td>
			<td class="description">JSON to specify the properties of the port that have to be updated</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
var node=diagram.selectionList[0];
var port ={fillColor:"red", visibility:ej.datavisualization.Diagram.PortVisibility.Visible}
diagram.updatePort(node.name,node.ports[0], port);
</script>

{% endhighlight %}

### updateSelectedObject(name)
{:#methods:updateselectedobject}

Update the specified node as selected object

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">name</td>
			<td class="type">String</td>
			<td class="description">name of the node to be updated as selected object</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.updateSelectedObject(name);
</script>

{% endhighlight %}

### updateSelection(\[showUserHandles\])
{:#methods:updateselection}

Update the selection at runtime

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">showUserHandles</td>
			<td class="type">Boolean [optional]</td>
			<td class="description">to specify whether to show the user handles or not</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.updateSelection(true);
</script>

{% endhighlight %}

### updateUserHandles(node)
{:#methods:updateuserhandles}

Update userhandles with respect to the given node

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">node</td>
			<td class="type">Object</td>
			<td class="description">node/connector with respect to which, the user handles have to be updated</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
var node = diagram.selectionList[0];
diagram.updateUSerHandles(node);
</script>

{% endhighlight %}

### updateViewPort()
{:#methods:updateviewport}

Update the diagram viewport at runtime

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.updateViewPort();
</script>

{% endhighlight %}

### upgrade(data)
{:#methods:upgrade}

Upgrade the diagram from old version

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">data</td>
			<td class="type">Object</td>
			<td class="description">to be upgraded</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.upgrade(jsonData);
diagram.load(jsonData);
</script>

{% endhighlight %}

### zoomTo(zoom)
{:#methods:zoomto}

Used to zoomIn/zoomOut diagram

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">zoom</td>
			<td class="type">Object</td>
			<td class="description">options to zoom the diagram(zoom factor, zoomin/zoomout)</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
var zoom = ej.datavisualization.Diagram.Zoom();
zoom.zoomFactor = .1;
zoom.zoomCommand = ej.datavisualization.Diagram.ZoomCommand.ZoomIn;
diagram.zoomTo(zoom);
</script>

{% endhighlight %}

## Events

### autoScrollChange
{:#events:autoscrollchange}

Triggers When auto scroll is changed

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">delay</td>
			<td class="type">String</td>
			<td class="description">parameter returns the delay between subsequent auto scrolls</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

// autoScrollChange event for diagram
$("#diagramcontent").ejDiagram({
autoScrollChange:function (args) {}
});

{% endhighlight %}

### click
{:#events:click}

Triggers when a node, connector or diagram is clicked

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">element</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the clicked node, connector or diagram</td>
		</tr>
		<tr>
			<td class="name">count</td>
			<td class="type">Number</td>
			<td class="description">parameter returns the count of how many times the mouse button is pressed</td>
		</tr>
		<tr>
			<td class="name">event</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the actual click event arguments that explains which button is clicked</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

// click event for diagram
$("#diagramcontent").ejDiagram({
click:function (args) {}
});

{% endhighlight %}

### connectionChange
{:#events:connectionchange}

Triggers when the connection is changed

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">element</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the connection that is changed between nodes, ports or points</td>
		</tr>
		<tr>
			<td class="name">connection</td>
			<td class="type">String</td>
			<td class="description">parameter returns the changed source or target node of the connector</td>
		</tr>
		<tr>
			<td class="name">port</td>
			<td class="type">String</td>
			<td class="description">parameter returns the changed source or target port of the connector</td>
		</tr>
		<tr>
			<td class="name">cancel</td>
			<td class="type">Boolean</td>
			<td class="description">parameter defines whether to cancel the change or not</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

// connectionChange event for diagram
$("#diagramcontent").ejDiagram({
connectionChange:function (args) {}
});

{% endhighlight %}

### connectorCollectionChange
{:#events:connectorcollectionchange}

Triggers when the connector collection is changed

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">changeType</td>
			<td class="type">String</td>
			<td class="description">parameter returns whether the connector is inserted or removed</td>
		</tr>
		<tr>
			<td class="name">element</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the connector that is to be added or deleted</td>
		</tr>
		<tr>
			<td class="name">cancel</td>
			<td class="type">Boolean</td>
			<td class="description">parameter defines whether to cancel the collection change or not</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

// connectorCollectionChange event for diagram
$("#diagramcontent").ejDiagram({
connectorCollectionChange:function (args) {}
});

{% endhighlight %}

### connectorSourceChange
{:#events:connectorsourcechange}

Triggers when the connectors' source point is changed

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">element</td>
			<td class="type">Object</td>
			<td class="description">returns the connector, the source point of which is being dragged</td>
		</tr>
		<tr>
			<td class="name">point</td>
			<td class="type">Object</td>
			<td class="description">returns the source point of the element</td>
		</tr>
		<tr>
			<td class="name">port</td>
			<td class="type">String</td>
			<td class="description">returns the source port of the element</td>
		</tr>
		<tr>
			<td class="name">dragState</td>
			<td class="type">String</td>
			<td class="description">returns the state of connection end point dragging(starting, dragging, completed)</td>
		</tr>
		<tr>
			<td class="name">cancel</td>
			<td class="type">Boolean</td>
			<td class="description">parameter defines whether to cancel the change or not</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

// connectorSourceChange event for diagram
$("#diagramcontent").ejDiagram({
connectorSourceChange:function (args) {}
});

{% endhighlight %}

### connectorTargetChange
{:#events:connectortargetchange}

Triggers when the connectors' target point is changed

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">element</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the connector, the target point of which is being dragged</td>
		</tr>
		<tr>
			<td class="name">point</td>
			<td class="type">Object</td>
			<td class="description">returns the target point of the element</td>
		</tr>
		<tr>
			<td class="name">port</td>
			<td class="type">String</td>
			<td class="description">returns the target port of the element</td>
		</tr>
		<tr>
			<td class="name">dragState</td>
			<td class="type">String</td>
			<td class="description">returns the state of connection end point dragging(starting, dragging, completed)</td>
		</tr>
		<tr>
			<td class="name">cancel</td>
			<td class="type">Boolean</td>
			<td class="description">parameter defines whether to cancel the change or not</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

// connectorTargetChange event for diagram
$("#diagramcontent").ejDiagram({
connectorTargetChange:function (args) {}
});

{% endhighlight %}

### contextMenuBeforeOpen
{:#events:contextmenubeforeopen}

Triggers before opening the context menu

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">diagram</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the diagram object</td>
		</tr>
		<tr>
			<td class="name">contextmenu</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the actual arguments from context menu</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

// contextMenuBeforeOpen event for diagram
$("#diagramcontent").ejDiagram({
contextMenuBeforeOpen:function (args) {}
});

{% endhighlight %}

### contextMenuClick
{:#events:contextmenuclick}

Triggers when a context menu item is clicked

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">id</td>
			<td class="type">String</td>
			<td class="description">parameter returns the id of the selected context menu item</td>
		</tr>
		<tr>
			<td class="name">text</td>
			<td class="type">String</td>
			<td class="description">parameter returns the text of the selected context menu item</td>
		</tr>
		<tr>
			<td class="name">parentId</td>
			<td class="type">String</td>
			<td class="description">parameter returns the parent id of the selected context menu item</td>
		</tr>
		<tr>
			<td class="name">parentText</td>
			<td class="type">String</td>
			<td class="description">parameter returns the parent text of the selected context menu item</td>
		</tr>
		<tr>
			<td class="name">target</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the object that was clicked</td>
		</tr>
		<tr>
			<td class="name">canExecute</td>
			<td class="type">Boolean</td>
			<td class="description">parameter defines whether to execute the click event or not</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

// contextMenuClick event for diagram
$("#diagramcontent").ejDiagram({
contextMenuClick:function (args) {}
});

{% endhighlight %}

### doubleClick
{:#events:doubleclick}

Triggers when a node, connector or diagram model is clicked twice

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">actualObject</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the object that is actually clicked</td>
		</tr>
		<tr>
			<td class="name">element</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the selected obejct</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

// doubleClick event for diagram
$("#diagramcontent").ejDiagram({
doubleClick:function (args) {}
});

{% endhighlight %}

### drag
{:#events:drag}

Triggers while dragging the elements in diagram

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">element</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the node or connector that is being dragged</td>
		</tr>
		<tr>
			<td class="name">oldValue</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the previous position of the node/connector</td>
		</tr>
		<tr>
			<td class="name">newValue</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the new position of the node/connector</td>
		</tr>
		<tr>
			<td class="name">cancel</td>
			<td class="type">Boolean</td>
			<td class="description">parameter returns whether or not to cancel the drag event</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

// deag event for diagram
$("#diagramcontent").ejDiagram({
drag:function (args) {}
});

{% endhighlight %}

### dragEnter
{:#events:dragenter}

Triggers when a symbol is dragged into diagram from symbol palette

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">element</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the node or connector that is dragged into diagram</td>
		</tr>
		<tr>
			<td class="name">cancel</td>
			<td class="type">Boolean</td>
			<td class="description">parameter returns whether to add or remove the symbol from diagram</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

// drag enter event for diagram
$("#diagramcontent").ejDiagram({
dragEnter:function (args) {}
});

{% endhighlight %}

### dragOver
{:#events:dragover}

Triggers when a symbol is dragged over diagram

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">element</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the node or connector that is dragged over diagram</td>
		</tr>
		<tr>
			<td class="name">allowDrop</td>
			<td class="type">Boolean</td>
			<td class="description">parameter defines whether the symbol can be dropped at the current mouse position</td>
		</tr>
		<tr>
			<td class="name">target</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the node/connector over which the symbol is dragged</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

// drag over event for diagram
$("#diagramcontent").ejDiagram({
dragOver:function (args) {}
});

{% endhighlight %}

### drop
{:#events:drop}

Triggers when a symbol is dragged and dropped from symbol palette to drawing area

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">element</td>
			<td class="type">Object</td>
			<td class="description">parameter returns node or connector that is being dropped</td>
		</tr>
		<tr>
			<td class="name">cancel</td>
			<td class="type">Boolean</td>
			<td class="description">parameter returns whether or not to cancel the drop event</td>
		</tr>
		<tr>
			<td class="name">source</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the object from where the element is dragged</td>
		</tr>
		<tr>
			<td class="name">target</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the object over which the objecct will be dropped</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

// drop event for diagram
$("#diagramcontent").ejDiagram({
drop:function (args) {}
});

{% endhighlight %}

### groupChange
{:#events:groupchange}

Triggers when a child is added to or removed from a group

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">element</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the object that is added to/removed from a group</td>
		</tr>
		<tr>
			<td class="name">oldParent</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the old parent group(if any) of the object</td>
		</tr>
		<tr>
			<td class="name">newParent</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the new parent group(if any) of the object</td>
		</tr>
		<tr>
			<td class="name">cause</td>
			<td class="type">String</td>
			<td class="description">parameter returns the cause of group change("group", unGroup")</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

// group change event for diagram
$("#diagramcontent").ejDiagram({
groupChange:function (args) {}
});

{% endhighlight %}

### itemClick
{:#events:itemclick}

Triggers when a diagram element is clicked

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">actualObject</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the object that was actually clicked</td>
		</tr>
		<tr>
			<td class="name">selectedObject</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the object that is selected</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

// itemClick event for diagram
$("#diagramcontent").ejDiagram({
itemClick:function (args) {}
});

{% endhighlight %}

### mouseEnter
{:#events:mouseenter}

Triggers when mouse enters a node/connector

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">element</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the target node or connector</td>
		</tr>
		<tr>
			<td class="name">source</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the object from where the selected object is dragged</td>
		</tr>
		<tr>
			<td class="name">target</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the target object over which the selected object is dragged</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

// mouseEnter event for diagram
$("#diagramcontent").ejDiagram({
mouseEnter:function (args) {}
});

{% endhighlight %}

### mouseLeave
{:#events:mouseleave}

Triggers when mouse leaves node/connector

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">element</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the target node or connector</td>
		</tr>
		<tr>
			<td class="name">source</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the object from where the selected object is dragged</td>
		</tr>
		<tr>
			<td class="name">target</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the target object over which the selected object is dragged</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

// mouseLeave event for diagram
$("#diagramcontent").ejDiagram({
mouseLeave:function (args) {}
});

{% endhighlight %}

### mouseOver
{:#events:mouseover}

Triggers when mouse hovers over a node/connector

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">element</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the target node or connector</td>
		</tr>
		<tr>
			<td class="name">source</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the object from where the element is dragged</td>
		</tr>
		<tr>
			<td class="name">target</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the object over which the element is being dragged.</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

// mouseOver event for diagram
$("#diagramcontent").ejDiagram({
mouseOver:function (args) {}
});

{% endhighlight %}

### nodeCollectionChange
{:#events:nodecollectionchange}

Triggers when node collection is changed

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">changeType</td>
			<td class="type">String</td>
			<td class="description">parameter returns whether the node is to be added or removed</td>
		</tr>
		<tr>
			<td class="name">element</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the node which needs to be added or deleted</td>
		</tr>
		<tr>
			<td class="name">cancel</td>
			<td class="type">Boolean</td>
			<td class="description">parameter defines whether to cancel the collection change or not</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

// nodeCollectionChange event for diagram
$("#diagramcontent").ejDiagram({
nodeCollectionChange:function (args) {}
});

{% endhighlight %}

### nodeSizeChange
{:#events:nodesizechange}

Triggers when a node is resized

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">element</td>
			<td class="type">Object</td>
			<td class="description">parameter returns node that was resized</td>
		</tr>
		<tr>
			<td class="name">cancel</td>
			<td class="type">Boolean</td>
			<td class="description">parameter to cancel the size change</td>
		</tr>
		<tr>
			<td class="name">newValue</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the new width, height, offsetX and offsetY values of the element that is being resized</td>
		</tr>
		<tr>
			<td class="name">oldValue</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the previous width,height,offsetX and offsetY values of the element that is being resized</td>
		</tr>
		<tr>
			<td class="name">resizeState</td>
			<td class="type">String</td>
			<td class="description">parameter returns the state of resizing(starting,resizing,completed)</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

// sizeChange event for diagram
$("#diagramcontent").ejDiagram({
sizeChange:function (args) {}
});

{% endhighlight %}

### propertyChange
{:#events:propertychange}

Triggers when the node properties(x, y,width and height alone) are changed using nudge commands or updateNode API.

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">element</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the selected element</td>
		</tr>
		<tr>
			<td class="name">newValue</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the new value of the node property that is being changed</td>
		</tr>
		<tr>
			<td class="name">oldValue</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the old value of the property that is being changed</td>
		</tr>
		<tr>
			<td class="name">propertyName</td>
			<td class="type">String</td>
			<td class="description">parameter returns the name of the property that is changed</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

// propertyChange event for diagram
$("#diagramcontent").ejDiagram({
propertyChange:function (args) {}
});

{% endhighlight %}

### rotationChange
{:#events:rotationchange}

Triggers when the diagram elements are rotated

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">element</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the node that is rotated</td>
		</tr>
		<tr>
			<td class="name">oldValue</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the previous rotation angle</td>
		</tr>
		<tr>
			<td class="name">newValue</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the new rotation angle</td>
		</tr>
		<tr>
			<td class="name">cancel</td>
			<td class="type">Boolean</td>
			<td class="description">parameter to specify whether or not to cancel the event</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

// rotationChange event for diagram
$("#diagramcontent").ejDiagram({
rotationChange:function (args) {}
});

{% endhighlight %}

### scrollChange
{:#events:scrollchange}

Triggers when the diagram is zoomed or panned

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">newValues</td>
			<td class="type">Object</td>
			<td class="description">Parameter returns the new zoom value, horizontal and vertical scroll offsets.</td>
		</tr>
		<tr>
			<td class="name">oldValues</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the previous zoom value, horizontal and vertical scroll offsets.</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

// ScrollChange event
$("#diagramcontent").ejDiagram({
scrollChange :function (args) {
} });

{% endhighlight %}

### segmentChange
{:#events:segmentchange}

Triggers when a connector segment is edited

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">element</td>
			<td class="type">Object</td>
			<td class="description">Parameter returns the connector that is being edited</td>
		</tr>
		<tr>
			<td class="name">dragState</td>
			<td class="type">String</td>
			<td class="description">parameter returns the state of editing (starting, dragging, completed)</td>
		</tr>
		<tr>
			<td class="name">point</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the current mouse position</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

// segment changed event for diagram
$("#diagramcontent").ejDiagram({
segmentChange:function (args) {}
});

{% endhighlight %}

### selectionChange
{:#events:selectionchange}

Triggers when the selection is changed in diagram

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">oldItems</td>
			<td class="type">Array</td>
			<td class="description">parameter returns the collection of nodes and connectors that have to be removed from selection list</td>
		</tr>
		<tr>
			<td class="name">newItems</td>
			<td class="type">Array</td>
			<td class="description">parameter returns the collection of nodes and connectors that have to be added to selection list</td>
		</tr>
		<tr>
			<td class="name">selectedItems</td>
			<td class="type">Array</td>
			<td class="description">parameter returns the collection of nodes and connectors that will be selected after selection change</td>
		</tr>
		<tr>
			<td class="name">cancel</td>
			<td class="type">Boolean</td>
			<td class="description">parameter to specify whether or not to cancel the selection change event</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

// selectionChange event for diagram
$("#diagramcontent").ejDiagram({
selectionChange:function (args) {}
});

{% endhighlight %}

### textchanged
{:#events:textchanged}

Triggers When label editing is ended

<table class="params">
	<thead>
		<tr>
			<th>Name</th>
			<th>Type</th>
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">element</td>
			<td class="type">Object</td>
			<td class="description">parameter returns the node that contains the text being edited</td>
		</tr>
		<tr>
			<td class="name">value</td>
			<td class="type">String</td>
			<td class="description">parameter returns the new text</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

// textChanged event for diagram
$("#diagramcontent").ejDiagram({
textChanged:function (args) {}
});

{% endhighlight %}
