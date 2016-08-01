---
layout: post
title: Properties, Methods and Events of ejDiagram Widget
description: API reference for ejDiagram
documentation: API
platform: js
keywords: diagram, ejDiagram, diagram api, syncfusion
---

# ejDiagram
<ts root="datavisualization" />

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

Defines the background color of diagram elements

#### Default Value:

* "transparent"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({ backgroundColor: "red"});
</script>

{% endhighlight %}

### backgroundImage `String`
{:#members:backgroundimage}

Defines the path of the background image of diagram elements

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({ backgroundImage: "Syncfusion.png" });
</script>

{% endhighlight %}

### backgroundImage.alignment `enum`
{:#members:backgroundimage-alignment}

<ts name = "ej.datavisualization.Diagram.ImageAlignment "/>
    
Defines how to align the background image over the diagram area.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">None</td>
            <td class="description last">Scales the graphic content non-uniformly to the width and height of the diagram area
</td>
       </tr>
        <tr>
            <td class="name">XMinYMin</td>
            <td class="description last">Used to align the image at the top left of diagram area </td>
       </tr>
        <tr>
            <td class="name">XMinYMid</td>
            <td class="description last">Used to align the image at the left center of diagram area</td>
       </tr>
        <tr>
            <td class="name">XMinYMax</td>
            <td class="description last">Used to align the image at the bottom left of diagram area</td>
       </tr>
        <tr>
            <td class="name">XMidYMin</td>
            <td class="description last">Used to align the image at the top center of diagram area</td>
       </tr>
        <tr>
            <td class="name">XMidYMid</td>
            <td class="description last">Used to align the image at the center of diagram area</td>
       </tr>
        <tr>
            <td class="name">XMidYMax</td>
            <td class="description last">Used to align the image at the bottom center of diagram area</td>
       </tr>
        <tr>
            <td class="name">XMaxYMin</td>
            <td class="description last">Used to align the image at the top right of diagram area/node</td>
       </tr>
        <tr>
            <td class="name">XMaxYMid</td>
            <td class="description last">Used to align the image at the right center of diagram area/node</td>
       </tr>
        <tr>
            <td class="name">XMaxYMax</td>
            <td class="description last">Used to align the image at the bottom right of diagram area/node</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.ImageAlignment.XMidYMid

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({ backgroundImage:{alignment: ej.datavisualization.Diagram.ImageAlignment.XMidYMid }});
</script>

{% endhighlight %}


### backgroundImage.scale `enum`
{:# members:backgroundimage-scale}

<ts name = "ej.datavisualization.Diagram.ScaleConstraints "/>
    
Defines how the background image should be scaled/stretched

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">None</td>
            <td class="description last">Used to scale the image non-uniformly to the given width/height</td>
       </tr>
        <tr>
            <td class="name">Meet</td>
            <td class="description last">Used to scale the image uniformly so that it fits the viewport</td>
       </tr>
        <tr>
            <td class="name">Slice</td>
            <td class="description last">Used to scale the image uniformly to the maximum</td>
       </tr>
    </tbody>
</table>
 
#### Default Value:

* ej.datavisualization.Diagram.ScaleConstraints.Meet

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({ backgroundImage:{scale:ej.datavisualization.Diagram.ScaleConstraints.Meet }});
</script>

{% endhighlight %}

### backgroundImage.source `String`
{:# members:backgroundimage-source}

Sets the source path of the background image

#### Default Value:

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({ backgroundImage:{ source:"Syncfusion.png" }});
</script>

{% endhighlight %}

### bridgeDirection `enum`
{:#members:bridgedirection}

<ts name = "ej.datavisualization.Diagram.BridgeDirection"/>
    
Sets the direction of line bridges.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">Left</td>
            <td class="description last">Used to set the direction of line bridges as left</td>
       </tr>
        <tr>
            <td class="name">Right</td>
            <td class="description last">Used to set the direction of line bridges as right</td>
       </tr>
        <tr>
            <td class="name">Top</td>
            <td class="description last">Used to set the direction of line bridges as top</td>
       </tr>
        <tr>
            <td class="name">Bottom</td>
            <td class="description last">Used to set the direction of line bridges as bottom</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.BridgeDirection.Top

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({ bridgeDirection:ej.datavisualization.Diagram.BridgeDirection.Bottom } });
</script>

{% endhighlight %}

### commandManager `Object`
{:#members:commandmanager}

Defines a set of custom commands and binds them with a set of desired key gestures.

### commandManager.commands `Object`
{:#members:commandmanager-commands}

An object that maps a set of command names with the corresponding command objects 

#### Default Value:

* {}

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
	
$("#diagramcontent").ejDiagram( {
   commandManager:{
      commands: { 
		//Command Name
        "clone" : 
		//Command Definition
        { 
            gesture: { key:ej.datavisualization.Diagram.Keys.C, 
				keyModifiers: ej.datavisualization.Diagram.KeyModifiers.Shift },
            canExecute : function(args) {
                var diagram = $("#diagramcontent").ejDiagram("instance");
                return diagram.model.selectedItems.children.length;
            },
            execute : function(args){
                var diagram = $("#diagramcontent").ejDiagram("instance");
                diagram.copy();
                diagram.paste();
            } 
        } 
     }
   }
});

</script>

{% endhighlight %}

### commandManager.commands.canExecute `function`
{:#members:commandmanager-commands-canexecute}

A method that defines whether the command is executable at the moment or not. 

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>

$("#diagramcontent").ejDiagram( {
   commandManager:{
      commands: { 
		//Command Name
        "clone" : 
		//Method to define whether the command is executable at the moment
        { 
            canExecute : function(args) {
                var diagram = $("#diagramcontent").ejDiagram("instance");
                return diagram.model.selectedItems.children.length;
            }
        } 
     }
   }
});
</script>

{% endhighlight %}

### commandManager.commands.execute `function`
{:#members:commandmanager-commands-execute}

A method that defines what to be executed when the key combination is recognized.

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>

$("#diagramcontent").ejDiagram( {
   commandManager:{
      commands: { 
		//Command Name
        "clone" : 
		//Defines what to be executed when the key combination is recognized
        { 
            execute : function(args){
                var diagram = $("#diagramcontent").ejDiagram("instance");
                diagram.copy();
                diagram.paste();
            } 
        } 
     }
   }
});
</script>

{% endhighlight %}

### commandManager.commands.gesture `Object`
{:#members:commandmanager-commands-gesture}

Defines a combination of keys and key modifiers, on recognition of which the command will be executed

### commandManager.commands.gesture.key `enum`
{:#members:commandmanager-commands-gesture-key}

<ts name = "ej.datavisualization.Diagram.Keys"/>

Sets the key value, on recognition of which the command will be executed.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">None</td>
            <td class="description last">No key pressed.</td>
        </tr>
        <tr>
            <td class="name">A</td>
            <td class="description last">The A key.</td>
        </tr>
        <tr>
            <td class="name">B</td>
            <td class="description last">The B key.</td>
        </tr>
        <tr>
            <td class="name">C</td>
            <td class="description last">The C key.</td>
        </tr>
        <tr>
            <td class="name">D</td>
            <td class="description last">The D Key.</td>
        </tr>
        <tr>
            <td class="name">E</td>
            <td class="description last">The E key.</td>
        </tr>
        <tr>
            <td class="name">F</td>
            <td class="description last">The F key.</td>
        </tr>
        <tr>
            <td class="name">G</td>
            <td class="description last">The G key.</td>
        </tr>
        <tr>
            <td class="name">H</td>
            <td class="description last">The H Key.</td>
        </tr>
        <tr>
            <td class="name">I</td>
            <td class="description last">The I key.</td>
        </tr>
        <tr>
            <td class="name">J</td>
            <td class="description last">The J key.</td>
        </tr>
        <tr>
            <td class="name">K</td>
            <td class="description last">The K key.</td>
        </tr>
        <tr>
            <td class="name">L</td>
            <td class="description last">The L Key.</td>
        </tr>
        <tr>
            <td class="name">M</td>
            <td class="description last">The M key.</td>
        </tr>
        <tr>
            <td class="name">N</td>
            <td class="description last">The N key.</td>
        </tr>
        <tr>
            <td class="name">O</td>
            <td class="description last">The O key.</td>
        </tr>
        <tr>
            <td class="name">P</td>
            <td class="description last">The P Key.</td>
        </tr>
        <tr>
            <td class="name">Q</td>
            <td class="description last">The Q key.</td>
        </tr>
        <tr>
            <td class="name">R</td>
            <td class="description last">The R key.</td>
        </tr>
        <tr>
            <td class="name">S</td>
            <td class="description last">The S key.</td>
        </tr>
        <tr>
            <td class="name">T</td>
            <td class="description last">The T Key.</td>
        </tr>
        <tr>
            <td class="name">U</td>
            <td class="description last">The U key.</td>
        </tr>
        <tr>
            <td class="name">V</td>
            <td class="description last">The V key.</td>
        </tr>
        <tr>
            <td class="name">W</td>
            <td class="description last">The W key.</td>
        </tr>
        <tr>
            <td class="name">X</td>
            <td class="description last">The X key.</td>
        </tr>
        <tr>
            <td class="name">Y</td>
            <td class="description last">The Y key.</td>
        </tr>
        <tr>
            <td class="name">Z</td>
            <td class="description last">The Z key.</td>
        </tr>
        <tr>
            <td class="name">Number0</td>
            <td class="description last">The 0 key.</td>
        </tr>
        <tr>
            <td class="name">Number1</td>
            <td class="description last">The 1 key.</td>
        </tr>
        <tr>
            <td class="name">Number2</td>
            <td class="description last">The 2 key.</td>
        </tr>
        <tr>
            <td class="name">Number3</td>
            <td class="description last">The 3 key.</td>
        </tr>
        <tr>
            <td class="name">Number4</td>
            <td class="description last">The 4 key.</td>
        </tr>
        <tr>
            <td class="name">Number5</td>
            <td class="description last">The 5 key.</td>
        </tr>
        <tr>
            <td class="name">Number6</td>
            <td class="description last">The 6 key.</td>
        </tr>
        <tr>
            <td class="name">Number7</td>
            <td class="description last">The 7 key.</td>
        </tr>
        <tr>
            <td class="name">Number8</td>
            <td class="description last">The 8 key.</td>
        </tr>
        <tr>
            <td class="name">Number9</td>
            <td class="description last">The 9 key.</td>
        </tr>
        <tr>
            <td class="name">Left</td>
            <td class="description last">The LEFT ARROW key.</td>
        </tr>
        <tr>
            <td class="name">Up</td>
            <td class="description last">The UP ARROW key.</td>
        </tr>
        <tr>
            <td class="name">Right</td>
            <td class="description last">The RIGHT ARROW key.</td>
        </tr>
        <tr>
            <td class="name">Down</td>
            <td class="description last">The DOWN ARROW key.</td>
        </tr>
        <tr>
            <td class="name">Escape</td>
            <td class="description last">The ESC key.</td>
        </tr>
        <tr>
            <td class="name">Delete</td>
            <td class="description last">The DEL key.</td>
        </tr>
        <tr>
            <td class="name">Tab</td>
            <td class="description last">The TAB key.</td>
        </tr>
        <tr>
            <td class="name">Enter</td>
            <td class="description last">The ENTER key.</td>
        </tr>
    </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.Keys.None

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram( {
   commandManager:{
      commands: { 
		//Command Name
        "clone" : 
		//Sets the key corresponding to the command
        { 
            gesture: { key:ej.datavisualization.Diagram.Keys.C, 
				keyModifiers: ej.datavisualization.Diagram.KeyModifiers.Shift }
        } 
     }
   }
});	
</script>

{% endhighlight %}

### commandManager.commands.gesture.keyModifiers `enum`
{:#members:commandmanager-commands-gesture-keymodifiers}

<ts name = "ej.datavisualization.Diagram.KeyModifiers"/>
	
Sets a combination of key modifiers, on recognition of which the command will be executed.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">None</td>
            <td class="description last">No modifiers are pressed.</td>
       </tr>
        <tr>
            <td class="name">Alt</td>
            <td class="description last">The ALT key.</td>
       </tr>
        <tr>
            <td class="name">Control</td>
            <td class="description last">The CTRL key.</td>
       </tr>
        <tr>
            <td class="name">Shift</td>
            <td class="description last">The SHIFT key.</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.KeyModifiers.None

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram( {
   commandManager:{
      commands: { 
		//Command Name
        "clone" : 
		//Sets the key modifiers
        { 
            gesture: { key:ej.datavisualization.Diagram.Keys.C, 
				keyModifiers: ej.datavisualization.Diagram.KeyModifiers.Shift }
        } 
     }
   }
});	
</script>

{% endhighlight %}

### commandManager.commands.parameter `Object`
{:#members:commandmanager-commands-parameter}

Defines any additional parameters that are required at runtime

#### Default Value:

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram( {
   commandManager:{
      commands: { 
        "clone" : 
        { 
            execute : function(args){
                var diagram = $("#diagramcontent").ejDiagram("instance");
				//Checks args.parameter
                if(diagram.getObjectType(diagram.model.selectedItems.children[0]) == args.parameter)
                {
                    diagram.copy();
                    diagram.paste();
                }
            },
			// any static value that is required when the command is executed
            parameter : "node" 
        } 
     }
   }
});
</script>

{% endhighlight %}

### connectors `Array`
{:#members:connectors}

A collection of JSON objects where each object represents a connector

#### Default Value:

* []

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = {name:"connector1", sourcePoint:{ x:100, y:100 }, targetPoint:{ x:200,y:200 }};
$("#diagramcontent").ejDiagram({ connectors:[connector] });
</script>

{% endhighlight %}

### connectors.addInfo `Object`
{:#members:connectors-addinfo}

To maintain additional information about connectors

#### Default Value:

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var addInfo = { Description: "Bidirectional Flow" };
var connector = { name:"connector1", sourcePoint:{ x:100, y:100 }, targetPoint:{ x:200,y:200 }, addInfo:addInfo };
$("#diagramcontent").ejDiagram({ connectors:[connector] });
</script>

{% endhighlight %}

### connectors.bridgeSpace `Number`
{:#members:connectors-bridgespace}

Defines the width of the line bridges

#### Default Value:

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
$("#diagramcontent").ejDiagram(
{ 
	connectors:[connector1, connector2],
	//Enable bridging
	constraints:DiagramConstraints.Default | DiagramConstraints.Bridging 
});
</script>

{% endhighlight %}

### connectors.constraints `enum`
{:#members:connectors-constraints}

<ts name = "ej.datavisualization.Diagram.ConnectorConstraints"/>

Enables or disables the behaviors of connectors.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">None</td>
            <td class="description last">Disable all connector Constraints</td>
       </tr>
        <tr>
            <td class="name">Select</td>
            <td class="description last">Enables connector to be selected</td>
       </tr>
        <tr>
            <td class="name">Delete</td>
            <td class="description last">Enables connector to be Deleted</td>
       </tr>
        <tr>
            <td class="name">Drag</td>
            <td class="description last">Enables connector to be Dragged</td>
       </tr>
        <tr>
            <td class="name">DragSourceEnd</td>
            <td class="description last">Enables connectors source end to be selected</td>
       </tr>
        <tr>
            <td class="name">DragTargetEnd</td>
            <td class="description last">Enables connectors target end to be selected</td>
       </tr>
        <tr>
            <td class="name">DragSegmentThumb</td>
            <td class="description last">Enables control point and end point of every segment in a connector for editing</td>
       </tr>
        <tr>
            <td class="name">Bridging</td>
            <td class="description last">Enables bridging to the connector</td>
       </tr>
        <tr>
            <td class="name">DragLabel</td>
            <td class="description last">Enables label of node to be Dragged</td>
       </tr>
        <tr>
            <td class="name">InheritBridging</td>
            <td class="description last">Enables bridging to the connector</td>
       </tr>
        <tr>
            <td class="name">PointerEvents</td>
            <td class="description last">Enables user interaction to the connector</td>
       </tr>
        <tr>
            <td class="name">Default</td>
            <td class="description last">Enables all constraints</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.ConnectorConstraints.Default

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var ConnectorConstraints = ej.datavisualization.Diagram.ConnectorConstraints;
var connector = { name:"connector1", sourcePoint:{ x:100, y:100 }, targetPoint:{ x:200,y:200 }, 
	              //Disable selection
                  constraints: ConnectorConstraints.Default & ~ConnectorConstraints.Select };
$("#diagramcontent").ejDiagram({ connectors:[connector] });
</script>

{% endhighlight %}

### connectors.cornerRadius `Number`
{:#members:connectors-cornerradius}

Defines the radius of the rounded corner

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{ x:100, y:100 }, targetPoint:{ x:200,y:200 }, 
	              //Set corner radius
                  cornerRadius: 10, segments:[{ type: "orthogonal"}] };
$("#diagramcontent").ejDiagram({ connectors:[connector] });
</script>

{% endhighlight %}

### connectors.cssClass `String`
{:#members:connectors-cssclass}

Configures the styles of shapes

#### Default Value:

* ""

#### Example

{% highlight html %}

<style>
    .hoverConnector:hover {
        stroke:blue
    }
</style>

<div id="diagramcontent"></div>
<script>
var connector = { name: "connector", 
	         cssClass: "hoverConnector", 
	         sourcePoint:{ x:100, y: 100 }, targetPoint: { x: 200, y: 200 } };			 
$("#diagramcontent").ejDiagram({ connectors:[ connector ] });
</script>

{% endhighlight %}

### connectors.horizontalAlign `enum`
{:#members:connectors-horizontalalign}

<ts name = "ej.datavisualization.Diagram.HorizontalAlignment"/>

Sets the horizontal alignment of the connector. Applicable, if the parent of the connector is a container.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">Left</td>
            <td class="description last">Used to align text horizontally on left side of node/connector</td>
       </tr>
        <tr>
            <td class="name">Center</td>
            <td class="description last">Used to align text horizontally on center of node/connector</td>
       </tr>
        <tr>
            <td class="name">Right</td>
            <td class="description last">Used to align text horizontally on right side of node/connector</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.HorizontalAlignment.Left

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector1 = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:150, y:150}, 
	               //Set the horizontal alignment
	               horizontalAlign:ej.datavisualization.Diagram.HorizontalAlignment.Right }; 
				   
var group = { name :"group", children:[ connector1 ], 
              container: { type: "canvas" }, offsetX:200, offsetY:100, 
              minWidth:200, minHeight: 200, fillColor:"gray" };
			  
$("#diagramcontent").ejDiagram({nodes:[group]});
</script>

{% endhighlight %}

### connectors.labels `Array`
{:#members:connectors-labels}

A collection of JSON objects where each object represents a label.

<ts name="ej.datavisualization.Diagram.ConnectorLabel"/>

#### Default Value:

* []

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
	              //Define the labels collection
                  labels:[{ text:"connector" }]}; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.labels.alignment `enum`
{:#members:connectors-labels-alignment}

<ts name = "ej.datavisualization.Diagram.Alignment"/>

Defines how the label should be aligned with respect to the segment

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">Before</td>
            <td class="description last">Used to align the label either top or left(before) of the connector segment</td>
       </tr>
        <tr>
            <td class="name">Center</td>
            <td class="description last">Used to align the label at center of the connector segment</td>
       </tr>
        <tr>
            <td class="name">After</td>
            <td class="description last">Used to align the label either bottom or right(after) of the connector segment</td>
       </tr>
   </tbody>
</table>


#### Default Value:

* ej.datavisualization.Diagram.Alignment.Center

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
	              //Define the labels collection
                  labels:[{ text:"connector", alignment:"before" }]}; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.labels.bold `Boolean`
{:#members:connectors-labels-bold}

Enables/disables the bold style

#### Default Value:

* false

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connectors;
connectors=[{ name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
         labels:[{ text:"label", bold:true}]
      }];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>

{% endhighlight %}

### connectors.labels.borderColor `String`
{:#members:connectors-labels-bordercolor}

Sets the border color of the label

#### Default Value:

* "transparent"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connectors;
connectors=[{ name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
         labels:[{ text:"label", borderColor:"red", borderWidth: 2}]
      }];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>

{% endhighlight %}

### connectors.labels.borderWidth `Number`
{:#members:connectors-labels-borderwidth}

Sets the border width of the label

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connectors;
connectors=[{ name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
         labels:[{ text:"label", borderColor:"red", borderWidth: 2}]
      }];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>

{% endhighlight %}

### connectors.labels.boundaryConstraints `Boolean`
{:#members:connectors-labels-boundaryConstraints}

Defines whether the label should be aligned within the connector boundaries

#### Default Value:

* true

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connectors;
connectors=[{ name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
         labels:[{ text:"label", boundaryConstraints: "false"}]
      }];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>

{% endhighlight %}


### connectors.labels.fillColor `String`
{:#members:connectors-labels-fillcolor}

Sets the fill color of the text area

#### Default Value:

* "transparent"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connectors;
connectors=[{ name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
         labels:[{ text:"label", fillColor: "green"}]
      }];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>

{% endhighlight %}

### connectors.labels.fontColor `String`
{:#members:connectors-labels-fontcolor}

Sets the font color of the text

#### Default Value:

* "black"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connectors;
connectors=[{ name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
         labels:[{ text:"label", fontColor: "green"}]
      }];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>

{% endhighlight %}

### connectors.labels.fontFamily `String`
{:#members:connectors-labels-fontfamily}

Sets the font family of the text

#### Default Value:

* "Arial"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connectors;
connectors=[{ name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
         labels:[{ text:"label", fontColor: "green", fontFamily:"seugoe UI"}]
      }];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>

{% endhighlight %}

### connectors.labels.fontSize `Number`
{:#members:connectors-labels-fontsize}

Defines the font size of the text

#### Default Value:

* 12

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connectors;
connectors=[{ name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
         labels:[{ text:"label", fontSize: 14}]
      }];
$("#diagramcontent").ejDiagram({connectors:connectors});

</script>

{% endhighlight %}

### connectors.labels.horizontalAlignment `enum`
{:#members:connectors-labels-horizontalalignment}

<ts ref = "ej.datavisualization.Diagram.HorizontalAlignment"/>

Sets the horizontal alignment of the label.

#### Default Value:

* ej.datavisualization.Diagram.HorizontalAlignment.Center

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connectors;
connectors=[{ name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
	     //Align the text at the left most position of connector
         labels:[{ text:"label", offset:{ x:0 }, horizontalAlignment:ej.datavisualization.Diagram.HorizontalAlignment.Left}]
      }];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>

{% endhighlight %}

### connectors.labels.italic `Boolean`
{:#members:connectors-labels-italic}

Enables/disables the italic style

#### Default Value:

* false

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connectors;
connectors=[{ name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
         labels:[{ text:"label", italic:true}]
      }];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>

{% endhighlight %}

### connectors.labels.margin `Object`
{:#members:connectors-labels-margin}

To set the margin of the label

#### Default Value:

* ej.datavisualization.Diagram.Margin()

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connectors;
connectors=[{ name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
	     //Leaves 5px space between the left boundary of connector and label
         labels:[{ text:"label", offset:{ x:0 }, horizontalAlignment:"left", margin:{ left: 5 }}]
      }];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>

{% endhighlight %}

### connectors.labels.mode `enum`
{:#members:connectors-labels-mode}

<ts ref = "ej.datavisualization.Diagram.LabelEditMode"/>

Gets whether the label is currently being edited or not.

#### Default Value:

* ej.datavisualization.Diagram.LabelEditMode.Edit

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = diagram.selectionList[0];
console.log(connector.labels[0].mode);
</script>

{% endhighlight %}

### connectors.labels.name `String`
{:#members:connectors-labels-name}

Sets the unique identifier of the label

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connectors;
connectors=[{ name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
         labels:[{ text:"label", name:"label1"}]
      }];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>

{% endhighlight %}

### connectors.labels.offset `Object`
{:#members:connectors-labels-offset}

Sets the fraction/ratio(relative to connector) that defines the position of the label

#### Default Value:

* ej.datavisualization.Diagram.Point(0.5, 0.5)

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connectors;
connectors=[{ name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
         labels:[{ text:"label", offset:ej.datavisualization.Diagram.Point(0,0.5) }]
      }];
$("#diagramcontent").ejDiagram({connectors:connectors});

</script>

{% endhighlight %}

### connectors.labels.opacity `Number`
{:#members:connectors-labels-opacity}

Defines the transparency of labels

#### Default Value:

* 1

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connectors;
connectors=[{ name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
         labels:[{ text:"label", opacity: 0.7}
             ]
      }];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>

{% endhighlight %}

### connectors.labels.readOnly `Boolean`
{:#members:connectors-labels-readonly}

Defines whether the label is editable or not

#### Default Value:

* false

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connectors;
connectors=[{ name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
         labels:[{ text:"label", readOnly:true}]
      }];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>

{% endhighlight %}

### connectors.labels.relativeMode `enum`
{:#members:connectors-labels-relativemode}

<ts name = "ej.datavisualization.Diagram.LabelRelativeMode"/>

Defines whether the label should be positioned whether relative to segments or connector boundaries

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">SegmentPath</td>
            <td class="description last">Sets the relativeMode as SegmentPath</td>
       </tr>
        <tr>
            <td class="name">SegmentBounds</td>
            <td class="description last">Sets the relativeMode as SegmentBounds</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.LabelRelativeMode.SegmentPath

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connectors;
connectors=[{ name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
         labels:[{ text:"label", relativeMode:"segmentPath"}]
      }];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>

{% endhighlight %}

### connectors.labels.rotateAngle `Number`
{:#members:connectors-labels-rotateangle}

Defines the angle to which the label needs to be rotated

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connectors;
connectors=[{ name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
         labels:[{ text:"label", rotateAngle: 90}]
      }];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>

{% endhighlight %}

### connectors.labels.segmentOffset `String`
{:#members:connectors-labels-segmentOffset}

Sets the position of the label with respect to the total segment length

#### Default Value:

* 0.5

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connectors;
connectors=[{name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
         labels:[{ text:"Label", segmentOffset:0.7}]
      }];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>

{% endhighlight %}


### connectors.labels.text `String`
{:#members:connectors-labels-text}

Defines the label text

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connectors;
connectors=[{name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
         labels:[{ text:"Label"}]
      }];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>

{% endhighlight %}

### connectors.labels.textAlign `enum`
{:#members:connectors-labels-textalign}

<ts ref = "ej.datavisualization.Diagram.TextAlign"/>
	
Defines how to align the text inside the label.

#### Default Value:

* ej.datavisualization.Diagram.TextAlign.Center

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connectors;
connectors=[{ name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
         labels:[{ text:"node Label", textAlign:ej.datavisualization.Diagram.TextAlign.Left}]
      }];
$("#diagramcontent").ejDiagram({ connectors:connectors });
</script>

{% endhighlight %}

### connectors.labels.textDecoration `enum`
{:#members:connectors-labels-textdecoration}

<ts ref = "ej.datavisualization.Diagram.TextDecorations"/>

Sets how to decorate the label text.

#### Default Value:

* ej.datavisualization.Diagram.TextDecorations.None

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connectors;
connectors=[{ name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
	     //Decorate the text with an underline
         labels:[{ text:"Label", textDecoration: ej.datavisualization.Diagram.TextDecorations.Underline}]
      }];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>

{% endhighlight %}

### connectors.labels.verticalAlignment `enum`
{:#members:connectors-labels-verticalalignment}

<ts ref = "ej.datavisualization.Diagram.VerticalAlignment"/>

Sets the vertical alignment of the label.

#### Default Value:

* ej.datavisualization.Diagram.VerticalAlignment.Center

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
<script>
var connectors;
connectors=[{ name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
	     //Aligns the text at the top most position of connector
         labels:[{ text:"label", offset:{ y:0 }, verticalAlignment:ej.datavisualization.Diagram.VerticalAlignment.Top }]
      }];
$("#diagramcontent").ejDiagram({ connectors:connectors });
</script>

{% endhighlight %}

### connectors.labels.visible `Boolean`
{:#members:connectors-labels-visible}

Enables or disables the visibility of the label

#### Default Value:

* true

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connectors;
connectors=[{ name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
         labels:[{ text:"Label", visible: false}]
      }];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>

{% endhighlight %}

### connectors.labels.width `Number`
{:#members:connectors-labels-width}

Sets the width of the label(the maximum value of label width and the connector width will be considered as label width)

#### Default Value:

* 50

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connectors;
connectors=[{ name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
         labels:[{ text:"Label", width: 100}]
      }];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>

{% endhighlight %}

### connectors.labels.wrapping `enum`
{:#members:connectors-labels-wrapping}

<ts ref = "ej.datavisualization.Diagram.TextWrapping"/>

Defines how the label text needs to be wrapped.

#### Default Value:

* ej.datavisualization.Diagram.TextWrapping.WrapWithOverflow

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connectors;
connectors=[{ name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, 
         labels:[{ text:"Enter Your Text", wrapping:ej.datavisualization.Diagram.TextWrapping.NoWrap}]
      }];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>

{% endhighlight %}

### connectors.lineColor `String`
{:#members:connectors-linecolor}

Sets the stroke color of the connector

#### Default Value:

* "black"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
                  lineColor:"blue" }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.lineDashArray `String`
{:#members:connectors-linedasharray}

Sets the pattern of dashes and gaps used to stroke the path of the connector

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
                  lineColor:"blue", lineDashArray: "2,2" }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.lineHitPadding `Number`
{:#members:connectors-linehitpadding}

Defines the padding value to ease the interaction with connectors

#### Default Value:

* 10

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
                  lineHitPadding: 15 }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.lineWidth `Number`
{:#members:connectors-linewidth}

Sets the width of the line

#### Default Value:

* 1

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
                  lineWidth: 10 }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.marginBottom `Number`
{:#members:connectors-marginbottom}

Defines the minimum space to be left between the bottom of parent bounds and the connector. Applicable, if the parent is a container.

#### Default Value:

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
$("#diagramcontent").ejDiagram({nodes:[group]});

</script>

{% endhighlight %}

### connectors.marginLeft `Number`
{:#members:connectors-marginleft}

Defines the minimum space to be left between the left of parent bounds and the connector. Applicable, if the parent is a container.

#### Default Value:

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
$("#diagramcontent").ejDiagram({nodes:[group]});
</script>

{% endhighlight %}

### connectors.marginRight `Number`
{:#members:connectors-marginright}

Defines the minimum space to be left between the right of parent bounds and the connector. Applicable, if the parent is a container.

#### Default Value:

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
$("#diagramcontent").ejDiagram({nodes:[group]});
</script>

{% endhighlight %}

### connectors.marginTop `Number`
{:#members:connectors-margintop}

Defines the minimum space to be left between the top of parent bounds and the connector. Applicable, if the parent is a container.

#### Default Value:

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
$("#diagramcontent").ejDiagram({nodes:[group]});
</script>

{% endhighlight %}

### connectors.name `String`
{:#members:connectors-name}

Sets a unique name for the connector

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200} }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.opacity `Number`
{:#members:connectors-opacity}

Defines the transparency of the connector

#### Default Value:

* 1

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, 
	              opacity: 0.5 }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.paletteItem `Object`
{:#members:connectors-paletteitem}

Defines the size and preview size of the node to add that to symbol palette. To explore palette item, refer [Palette Item](#nodes-paletteitem)

#### Default Value:

* null

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
	
$("#symbolpalette").ejSymbolPalette({
	//Defines the palette collection 
	palettes: [{
		name: "Connectors", expanded: true,
		items: [
		{
			name: "connector", sourcePoint:{x: 0, y: 0}, targetPoint:{x:50, y: 50}, 
			segments:[{ type:"bezier" }],
			//Sets preview size
			paletteItem: {
                previewWidth: 100,
				previewHeight: 100
			}
		}]
	}]
});
</script>

{% endhighlight %}

### connectors.parent `String`
{:#members:connectors-parent}

Sets the parent name of the connector.

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, parent:"group"}; 
var group = { name :"group", children:["connector1"] };
$("#diagramcontent").ejDiagram({ nodes:[group], connectors : [connector]});
</script>

{% endhighlight %}

### connectors.segments `Array`
{:#members:connectors-segments}

An array of JSON objects where each object represents a segment

#### Default Value:

* [ { type:"straight" } ]

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, 
	              //Defines a collection of segments
                  segments: [{type:"straight", point: { x:75, y:150 }}] }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.segments.direction `String`
{:#members:connectors-segments-direction}

Sets the direction of orthogonal segment

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, 
                  segments: [{type:"orthogonal", direction:"bottom", length:50}] }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.segments.length `Number`
{:#members:connectors-segments-length}

Describes the length of orthogonal segment

#### Default Value:

* undefined

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, 
                  segments: [{type:"orthogonal", direction:"bottom", length:50}] }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.segments.point `object`
{:#members:connectors-segments-point}

<ts ref="ej.datavisualization.Diagram.ConnectorsSourcePoint"/>

Describes the end point of bezier/straight segment

#### Default Value:

* Diagram.Point()

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, 
	              //Defines a collection of segments
                  segments: [{ type:"straight", point: { x:75, y:150 }}] }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.segments.point1 `object`
{:#members:connectors-segments-point1}

<ts ref="ej.datavisualization.Diagram.ConnectorsSourcePoint"/>

Defines the first control point of the bezier segment

#### Default Value:

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, 
                  segments: [{ type:"bezier", point1: { x:150, y:50} }] }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.segments.point2 `object`
{:#members:connectors-segments-point2}

<ts ref="ej.datavisualization.Diagram.ConnectorsSourcePoint"/>

Defines the second control point of bezier segment

#### Default Value:

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, 
                  segments: [{ type:"bezier", point1: { x:150, y:50}, point2:{ x: 150, y: 150 } }] }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.segments.type `enum`
{:#members:connectors-segments-type}

<ts name = "ej.datavisualization.Diagram.Segments"/>

Sets the type of the segment.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">Straight</td>
            <td class="description last">Used to specify the lines as Straight</td>
       </tr>
        <tr>
            <td class="name">Orthogonal</td>
            <td class="description last">Used to specify the lines as Orthogonal</td>
       </tr>
        <tr>
            <td class="name">Bezier</td>
            <td class="description last">Used to specify the lines as Bezier</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.Segments.Straight

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, 
                  segments: [{ type: ej.datavisualization.Diagram.Segments.Bezier }] }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.segments.vector1 `Object`
{:#members:connectors-segments-vector1}

Describes the length and angle between the first control point and the start point of bezier segment

#### Default Value:

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, 
                  segments: [{ type:"bezier", 
                  vector1: { distance:75, angle: 0}, 
                  vector2: { distance:75, angle: 180} }] }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.segments.vector2 `Object`
{:#members:connectors-segments-vector2}

Describes the length and angle between the second control point and end point of bezier segment

#### Default Value:

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, 
                  segments: [{ type:"bezier", 
                  vector1: { distance:75, angle: 0}, 
                  vector2: { distance:75, angle: 180} }] }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.shape `Object`
{:#members:connectors-shape}

Defines the role/meaning of the connector

#### Default Value:

* null

### connectors.shape.type `enum`
{:#members:connectors-shape-type}

<ts name = "ej.datavisualization.Diagram.ConnectorShapes"/>

Sets the type of the connector

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">BPMN</td>
            <td class="description last">Used to specify connector type as BPMN</td>
       </tr>
        <tr>
            <td class="name">Classifier</td>
            <td class="description last">Used to specify connector type as Classifier</td>
       </tr>
          </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.ConnectorShapes.BPMN

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>        
var connector = [{ name: "connector1", sourcePoint: { x: 50, y: 200 }, targetPoint: { x: 200, y: 200 }, 
     segments: [{ type: "straight" }], shape: { type: "bpmn"} }]

$("#diagramcontent").ejDiagram({connectors : connector});
</script>


{% endhighlight %}

### connectors.shape.flow `enum`
{:#members:connectors-shape-flow}

<ts name = "ej.datavisualization.Diagram.BPMNFlows"/>

Sets the type of the flow in a BPMN Process

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">Sequence</td>
            <td class="description last">Used to specify the Sequence flow in a BPMN Process</td>
       </tr>
        <tr>
            <td class="name">Association</td>
            <td class="description last">Used to specify the Association flow in a BPMN Process </td>
       </tr>
        <tr>
            <td class="name">Message</td>
            <td class="description last">Used to specify the Message flow in a BPMN Process</td>
       </tr>
     </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.BPMNFlows.Sequence

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>        
var connector = [{ name: "connector1", sourcePoint: { x: 50, y: 200 }, targetPoint: { x: 200, y: 200 }, 
     segments: [{ type: "straight" }], shape: { type: "bpmn", flow: "message" } }],

$("#diagramcontent").ejDiagram({connectors : connector});
</script>

{% endhighlight %}

### connectors.shape.association `enum`
{:#members:connectors-shape-flow-association}

<ts name = "ej.datavisualization.Diagram.AssociationFlows"/>

Sets the type of the Association in a BPMN Process

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">Default</td>
            <td class="description last">Used to notate default association in a BPMN Process</td>
       </tr>
        <tr>
            <td class="name">Directional</td>
            <td class="description last">Used to notate directional association in a BPMN Process</td>
       </tr>
        <tr>
            <td class="name">BiDirectional</td>
            <td class="description last">User to notate bi-directional association in a BPMN Process</td>
       </tr>
     </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.AssociationFlows.Default

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>        
var connector = [{ name: "connector1", sourcePoint: { x: 50, y: 300 }, targetPoint: { x: 200, y: 300 }, 
     segments: [{ type: "straight" }], shape: { type: "bpmn", flow: "association", association: "bidirectional" } }],

$("#diagramcontent").ejDiagram({connectors : connector});
</script>

{% endhighlight %}

### connectors.shape.message `enum`
{:#members:connectors-shape-message}

<ts name = "ej.datavisualization.Diagram.BPMNMessageFlows"/>

Sets the type of the message flow. Applicable, if the connector is of type "BPMN"

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">Default</td>
            <td class="description last">Used to notate the default message flow in a BPMN Process</td>
       </tr>
        <tr>
            <td class="name">InitiatingMessage</td>
            <td class="description last">Used to notate the instantiating message flow in a BPMN Process</td>
       </tr>
        <tr>
            <td class="name">NonInitiatingMessage</td>
            <td class="description last">Used to notate the non-instantiating message flow in a BPMN Process</td>
       </tr>
     </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.BPMNMessageFlows.Default

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>        
var connector = [{ name: "connector1", sourcePoint: { x: 50, y: 600 }, targetPoint: { x: 200, y: 600 }, 
     segments: [{ type: "straight" }], shape: { type: "bpmn", flow: "message", message: "noninitiatingmessage" } }],

$("#diagramcontent").ejDiagram({connectors : connector});
</script>

{% endhighlight %}

### connectors.shape.sequence `enum`
{:#members:connectors-shape-sequence}

<ts name = "ej.datavisualization.Diagram.BPMNSequenceFlows"/>

Sets the type of BPMN sequence flow

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">Normal</td>
            <td class="description last">Used to notate the normal sequence flow in a BPMN Process</td>
       </tr>
        <tr>
            <td class="name">Conditional</td>
            <td class="description last">Used to notate the conditional sequence flow in a BPMN Process</td>
       </tr>
        <tr>
            <td class="name">Default</td>
            <td class="description last">Used to notate the default sequence flow in a BPMN Process</td>
       </tr>
     </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.BPMNSequenceFlows.Normal

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>        
var connector = [{ name: "connector1", sourcePoint: { x: 50, y: 600 }, targetPoint: { x: 200, y: 600 }, 
     segments: [{ type: "straight" }], shape: { type: "bpmn", flow: "sequence", sequence: "default" } }]

$("#diagramcontent").ejDiagram({connectors : connector});
</script>

{% endhighlight %}

### connectors.shape.relationship`String`
{:#members:connectors-shape.relationship}

Defines the role of the connector in a UML Class Diagram. Applicable, if the type of the connector is "classifier".

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">Association</td>
            <td class="description last">Used to notate association in UML Class Diagram</td>
       </tr>
        <tr>
            <td class="name">Aggregation</td>
            <td class="description last">Used to notate aggregation in a UML Class Diagram</td>
       </tr>
        <tr>
            <td class="name">Composition</td>
            <td class="description last">Used to notate composition in a UML Class Diagram</td>
       </tr>
        <tr>
            <td class="name">Dependency</td>
            <td class="description last">Used to notate dependency in a UML Class Diagram</td>
       </tr>
        <tr>
            <td class="name">Inheritance</td>
            <td class="description last">Used to notate inheritance in a UML Class Diagram</td>
       </tr>
     </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.ClassifierShapes.Association

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, 
                  shape: {type: "umlclassifier", relationship: ej.datavisualization.Diagram.ClassifierShapes.Aggregation,
                 } }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.shape.multiplicity`String`
{:#members:connectors-shape.multiplicity}

Defines the multiplicity of a relationship in UML class diagram

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
       <tr>
            <td class="name">OneToOne</td>
            <td class="description last">Used to specify the one to one relationship</td>
       </tr>
        <tr>
            <td class="name">OneToMany</td>
            <td class="description last">Used to specify the one to many relationship</td>
       </tr>
        <tr>
            <td class="name">ManyToOne</td>
            <td class="description last">Used to specify the many to one relationship</td>
       </tr>
      </tbody>
</table>

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, 
                  shape: {type: "umlclassifier", relationship: ej.datavisualization.Diagram.ClassifierShapes.Dependency, multiplicity:"onetomany"
                 } }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.sourceDecorator `Object`
{:#members:connectors-sourcedecorator}

Defines the source decorator of the connector

#### Default Value:

* { shape:"arrow", width: 8, height:8, borderColor:"black", fillColor:"black" }

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
                  sourceDecorator : { shape:"openarrow" } }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.sourceDecorator.borderColor `String`
{:#members:connectors-sourcedecorator-bordercolor}

Sets the border color of the source decorator

#### Default Value:

* "black"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, lineColor:"red",
                  sourceDecorator : { shape:"openarrow" , borderColor:"red"} }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.sourceDecorator.borderWidth `Number`
{:#members:connectors-sourcedecorator-borderwidth}

Sets the border width of the decorator

#### Default Value:

* 1

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
                  sourceDecorator : { shape:"openarrow" , borderWidth: 5} }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.sourceDecorator.fillColor `String`
{:#members:connectors-sourcedecorator-fillcolor}

Sets the fill color of the source decorator

#### Default Value:

* "black"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, lineColor:"red",
                  sourceDecorator : { shape:"circle" , fillColor:"red"} }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.sourceDecorator.height `Number`
{:#members:connectors-sourcedecorator-height}

Sets the height of the source decorator

#### Default Value:

* 8

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, lineColor:"red",
                  sourceDecorator : { width: 10, height:10 } }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.sourceDecorator.pathData `String`
{:#members:connectors-sourcedecorator-pathdata}

Defines the custom shape of the source decorator

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
                  sourceDecorator : { shape:"path", pathData:"M 376.892,225.284L 371.279,211.95L 376.892,198.617L 350.225,211.95L 376.892,225.284 Z"} }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.sourceDecorator.shape `enum`
{:#members:connectors-sourcedecorator-shape}

<ts name = "ej.datavisualization.Diagram.DecoratorShapes"/>

Defines the shape of the source decorator.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">None</td>
            <td class="description last">Used to set decorator shape as none</td>
       </tr>
        <tr>
            <td class="name">Arrow</td>
            <td class="description last">Used to set decorator shape as Arrow</td>
       </tr>
        <tr>
            <td class="name">OpenArrow</td>
            <td class="description last">Used to set decorator shape as Open Arrow</td>
       </tr>
        <tr>
            <td class="name">Circle</td>
            <td class="description last">Used to set decorator shape as Circle</td>
       </tr>
        <tr>
            <td class="name">Diamond</td>
            <td class="description last">Used to set decorator shape as Diamond</td>
       </tr>
        <tr>
            <td class="name">Path</td>
            <td class="description last">Used to set decorator shape as path</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.DecoratorShapes.Arrow

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
                  sourceDecorator : { shape: ej.datavisualization.Diagram.DecoratorShapes.Circle } }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.sourceDecorator.width `Number`
{:#members:connectors-sourcedecorator-width}

Defines the width of the source decorator

#### Default Value:

* 8

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, lineColor:"red",
                  sourceDecorator : { width: 10, height:10 } }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.sourceNode `String`
{:#members:connectors-sourcenode}

Sets the source node of the connector

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
	
var node1 = {name:"source", offsetX:100, offsetY:100, width: 50, height: 50 };
var node2 = {name:"target", offsetX:300, offsetY:300, width: 50, height: 50 };
var connector = { name:"connector1", sourceNode:"source", targetNode:"target" }; 
$("#diagramcontent").ejDiagram({nodes:[ node1, node2 ],connectors : [connector]});

</script>

{% endhighlight %}

### connectors.sourcePadding `Number`
{:#members:connectors-sourcepadding}

Defines the space to be left between the source node and the source point of a connector

#### Default Value:

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
$("#diagramcontent").ejDiagram({nodes:[ node1, node2 ],connectors : [connector]});
</script>

{% endhighlight %}

### connectors.sourcePoint `object`
{:#members:connectors-sourcepoint}

Describes the start point of the connector

#### Default Value:

* ej.datavisualization.Diagram.Point()

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", 
				  sourcePoint:{x:100, y:100}, 
				  targetPoint:{x:200, y:200} }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.sourcePoint.x `Number`
{:#members:connectors-sourcepoint-x}

Defines the x-coordinate of a position

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var point = {x: 10};
</script>

{% endhighlight %}

### connectors.sourcePoint.y `Number`
{:#members:connectors-sourcepoint-y}

Defines the y-coordinate of a position

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var point = {y: 10};
</script>

{% endhighlight %}

### connectors.sourcePort `String`
{:#members:connectors-sourceport}

Sets the source port of the connector

#### Default Value:

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
$("#diagramcontent").ejDiagram({nodes:[ node1, node2 ],connectors : [connector]});
</script>

{% endhighlight %}

### connectors.targetDecorator `Object`
{:#members:connectors-targetdecorator}

Defines the target decorator of the connector

#### Default Value:

* { shape:"arrow", width: 8, height:8, borderColor:"black", fillColor:"black" }

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
                  targetDecorator : { shape:"openarrow" } }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.targetDecorator.borderColor `String`
{:#members:connectors-targetdecorator-bordercolor}

Sets the border color of the decorator

#### Default Value:

* "black"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, lineColor:"red",
                  sourceDecorator : { shape:"openarrow" , borderColor:"red"} }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.targetDecorator.fillColor `String`
{:#members:connectors-targetdecorator-fillcolor}

Sets the color with which the decorator will be filled

#### Default Value:

* "black"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, lineColor:"red",
                  targetDecorator : { shape:"circle" , fillColor:"red"} }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.targetDecorator.height `Number`
{:#members:connectors-targetdecorator-height}

Defines the height of the target decorator

#### Default Value:

* 8

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, lineColor:"red",
                  targetDecorator : { width: 10, height:10 } }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.targetDecorator.pathData `String`
{:#members:connectors-targetdecorator-pathdata}

Defines the custom shape of the target decorator

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
                  targetDecorator : { shape:"path", pathData:"M 376.892,225.284L 371.279,211.95L 376.892,198.617L 350.225,211.95L 376.892,225.284 Z"} }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.targetDecorator.shape `enum`
{:#members:connectors-targetdecorator-shape}

<ts name = "ej.datavisualization.Diagram.DecoratorShapes"/>

Defines the shape of the target decorator.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">None</td>
            <td class="description last">Used to set decorator shape as none</td>
       </tr>
        <tr>
            <td class="name">Arrow</td>
            <td class="description last">Used to set decorator shape as Arrow</td>
       </tr>
        <tr>
            <td class="name">OpenArrow</td>
            <td class="description last">Used to set decorator shape as Open Arrow</td>
       </tr>
        <tr>
            <td class="name">Circle</td>
            <td class="description last">Used to set decorator shape as Circle</td>
       </tr>
        <tr>
            <td class="name">Diamond</td>
            <td class="description last">Used to set decorator shape as Diamond</td>
       </tr>
        <tr>
            <td class="name">Path</td>
            <td class="description last">Used to set decorator shape as path</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.DecoratorShapes.Arrow

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200},
                  targetDecorator : { shape:ej.datavisualization.Diagram.DecoratorShapes.Circle } }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.targetDecorator.width `Number`
{:#members:connectors-targetdecorator-width}

Defines the width of the target decorator

#### Default Value:

* 8

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, lineColor:"red",
                  targetDecorator : { width: 10, height:10 } }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.targetNode `String`
{:#members:connectors-targetnode}

Sets the target node of the connector

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var node1 = {name:"source", offsetX:100, offsetY:100, width: 50, height: 50 };
var node2 = {name:"target", offsetX:300, offsetY:300, width: 50, height: 50 };
var connector = { name:"connector1", sourceNode:"source", targetNode:"target" }; 
$("#diagramcontent").ejDiagram({nodes:[ node1, node2 ],connectors : [connector]});
</script>

{% endhighlight %}

### connectors.targetPadding `Number`
{:#members:connectors-targetpadding}

Defines the space to be left between the target node and the target point of the connector

#### Default Value:

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
$("#diagramcontent").ejDiagram({nodes:[ node1, node2 ],connectors : [connector]});
</script>

{% endhighlight %}

### connectors.targetPoint `object`
{:#members:connectors-targetpoint}

<ts ref = "ej.datavisualization.Diagram.ConnectorsSourcePoint"/>

Describes the end point of the connector

#### Default Value:

* ej.datavisualization.Diagram.Point()

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", 
				  sourcePoint:{x:100, y:100}, 
				  targetPoint:{x:200, y:200} }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.targetPort `String`
{:#members:connectors-targetport}

Sets the targetPort of the connector

#### Default Value:

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
$("#diagramcontent").ejDiagram({nodes:[ node1, node2 ],connectors : [connector]});
</script>

{% endhighlight %}

### connectors.tooltip `Object`
{:#members:connectors-tooltip}

Defines the tooltip that should be shown when the mouse hovers over connector. For tooltip properties, refer [Tooltip](#members:tooltip)

#### Default Value:

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>

<script type="text/x-jsrender" id="mouseovertooltip">
   <div style="background-color: #F08080; color: white; white-space: nowrap; height: 20px">
        <span style="padding: 5px;"> {{:name}} </span>
   </div>
</script>

<script>
var tooltip = {
		templateId: "mouseovertooltip",
		alignment: {
			horizontal: "center",
			vertical: "bottom"
		}
	};
var ConnectorConstraints = ej.datavisualization.Diagram.ConnectorConstraints;
$("#diagramcontent").ejDiagram({	
//Defines connectors
	connectors: [{
		name: "flow1",sourcePoint: { x:100, y: 100 }, targetPoint :{ x:200, y:200 },
		//Define tooltip
        constraints: ConnectorConstraints.Default & ~ConnectorConstraints.InheritTooltip, 
        tooltip:tooltip
	}]
});
</script>

{% endhighlight %}

### connectors.verticalAlign `enum`
{:#members:connectors-verticalalign}

<ts name = "ej.datavisualization.Diagram.VerticalAlignment"/>

To set the vertical alignment of connector (Applicable,if the parent is group).

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">Top</td>
            <td class="description last">Used to align text Vertically on left side of node/connector</td>
       </tr>
        <tr>
            <td class="name">Center</td>
            <td class="description last">Used to align text Vertically on center of node/connector</td>
       </tr>
        <tr>
            <td class="name">Bottom</td>
            <td class="description last">Used to align text Vertically on bottom of node/connector</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.VerticalAlignment.Top

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector1 = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:150, y:150}, 
	               //Set the horizontal alignment
	               verticalAlign:ej.datavisualization.Diagram.VerticalAlignment.Bottom }; 
				   
var group = { name :"group", children:[ connector1 ], 
              container: { type: "canvas" }, offsetX:200, offsetY:100, 
              minWidth:200, minHeight: 200, fillColor:"gray" };
			  
$("#diagramcontent").ejDiagram({nodes:[group]});
</script>

{% endhighlight %}

### connectors.visible `Boolean`
{:#members:connectors-visible}

Enables or disables the visibility of connector

#### Default Value:

* true

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connector1", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, 
                  visible: false }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectors.zOrder `Number`
{:#members:connectors-zorder}

Sets the z-index of the connector

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var connector = { name:"connectorghj", sourcePoint:{x:100, y:100}, targetPoint:{x:200, y:200}, 
                  zOrder: 1000 }; 
$("#diagramcontent").ejDiagram({connectors : [connector]});
</script>

{% endhighlight %}

### connectorTemplate `Object`
{:#members:connectortemplate}

Binds the custom JSON data with connector properties

#### Default Value:

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
   var data = [
        { "Id": "E1", "Name": "Maria Anders", "Designation": "Managing Director" },
        { "Id": "E2" , "Name": "Ana Trujillo", "Designation": "Project Manager", "ReportingPerson": "E1" } ];
		
   $("#diagramcontent").ejDiagram({
	   dataSourceSettings: { id: "Id", parent: "ReportingPerson", dataSource: data },
	   //Sets the method name to connector template 
	   connectorTemplate :"connectorTemplate"
   });
   
   //Sets the default styles and binds custom data with connector
    function connectorTemplate(diagram, connector) {
         if(connector.sourceNode && connector.targetNode){
			 connector.linecolor = "green";
		 }
     }
</script>

{% endhighlight %}

### constraints `enum`
{:#members:constraints}

<ts name = "ej.datavisualization.Diagram.DiagramConstraints"/>

Enables/Disables the default behaviors of the diagram.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">None</td>
            <td class="description last">Disables all DiagramConstraints</td>
       </tr>
        <tr>
            <td class="name">PageEditable</td>
            <td class="description last">Enables/Disables PageEditing</td>
       </tr>
        <tr>
            <td class="name">Bridging</td>
            <td class="description last">Enables/Disables Bridging</td>
       </tr>
        <tr>
            <td class="name">Zoomable</td>
            <td class="description last">Enables/Disables Zooming</td>
       </tr>
        <tr>
            <td class="name">PannableX</td>
            <td class="description last">Enables/Disables panning on horizontal axis</td>
       </tr>
        <tr>
            <td class="name">PannableY</td>
            <td class="description last">Enables/Disables panning on vertical axis</td>
       </tr>
        <tr>
            <td class="name">Pannable</td>
            <td class="description last">Enables/Disables Panning</td>
       </tr>
        <tr>
            <td class="name">Undoable</td>
            <td class="description last">Enables/Disables undo actions</td>
       </tr>
        <tr>
            <td class="name">Default</td>
            <td class="description last">Enables all Constraints</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.DiagramConstraints.All

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var DiagramConstraints = ej.datavisualization.Diagram.DiagramConstraints;
//Enables line bridging
$("#diagramcontent").ejDiagram({
	constraints: DiagramConstraints.Default | DiagramConstraints.Bridging });
</script>

{% endhighlight %}

### contextMenu `object`
{:#members:contextmenu}

An object to customize the context menu of diagram

### contextMenu.items `Array`
{:#members:contextmenu-items}

Defines the collection of context menu items

#### Default Value:

* []

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
//Collection of items
var menuitems = [{ "name": "hyperLink", "text": "Hyperlink", "image": "", "style": "" }];
var contextMenu = { items: menuitems};
$("#diagramcontent").ejDiagram({contextMenu: contextMenu});
</script>

{% endhighlight %}

### contextMenu.showCustomMenuItemsOnly `Boolean`
{:#members:contextmenu-showcustommenuitemsonly}

To set whether to display the default context menu items or not

#### Default Value:

* false

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var contextMenu = { showCustomMenuItemsOnly: true };
$("#diagramcontent").ejDiagram({contextMenu: contextMenu});
</script>

{% endhighlight %}

### dataSourceSettings `object`
{:#members:datasourcesettings}

Configures the data source that is to be bound with diagram

### dataSourceSettings.dataSource `Object`
{:#members:datasourcesettings-datasource}

Defines the data source either as a collection of objects or as an instance of ej.DataManager

#### Default Value:

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
	
var data = [
        { "Id": "E1", "Name": "Maria Anders", "Designation": "Managing Director" },
        { "Id": "E2" , "Name": "Ana Trujillo", "Designation": "Project Manager", "ReportingPerson": "E1" } ];

   $("#diagramcontent").ejDiagram({
	   dataSourceSettings: { dataSource: data }
   });
   
</script>

{% endhighlight %}

### dataSourceSettings.id `String`
{:#members:datasourcesettings-id}

Sets the unique id of the data source items

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
   var data = [
        { "Id": "E1", "Name": "Maria Anders", "Designation": "Managing Director" },
        { "Id": "E2" , "Name": "Ana Trujillo", "Designation": "Project Manager", "ReportingPerson": "E1" } ];
		
   $("#diagramcontent").ejDiagram({
	   dataSourceSettings: { id: "Id", dataSource: data }
   });
</script>

{% endhighlight %}

### dataSourceSettings.parent `String`
{:#members:datasourcesettings-parent}

Defines the parent id of the data source item

#### Default Value:

* ''

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
   var data = [
        { "Id": "E1", "Name": "Maria Anders", "Designation": "Managing Director" },
        { "Id": "E2" , "Name": "Ana Trujillo", "Designation": "Project Manager", "ReportingPerson": "E1" } ];
		
   $("#diagramcontent").ejDiagram({
	   dataSourceSettings: { id: "Id", parent: "ReportingPerson", dataSource: data }
   });
</script>

{% endhighlight %}

### dataSourceSettings.query `String`
{:#members:datasourcesettings-query}

Describes query to retrieve a set of data from the specified datasource

#### Default Value:

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
   $("#diagramcontent").ejDiagram({
	   dataSourceSettings: {
       dataSource: ej.DataManager({ url: "http://mvc.syncfusion.com/Services/Northwnd.svc/" }),
       query: ej.Query().from("Employees").select("EmployeeID,ReportsTo,FirstName"),
       tableName: "Employees", id: "EmployeeID", parent: "ReportsTo" }
   });
</script>

{% endhighlight %}

### dataSourceSettings.root `String`
{:#members:datasourcesettings-root}

Sets the unique id of the root data source item

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
   var data = [
        { "Id": "E1", "Name": "Maria Anders", "Designation": "Managing Director" },
        { "Id": "E2" , "Name": "Ana Trujillo", "Designation": "Project Manager", "ReportingPerson": "E1" } ];
		
   $("#diagramcontent").ejDiagram({
	   dataSourceSettings: { id: "Id", parent: "ReportingPerson", root:"E1", dataSource: data }
   });
</script>

{% endhighlight %}

### dataSourceSettings.tableName `String`
{:#members:datasourcesettings-tablename}

Describes the name of the table on which the specified query has to be executed

#### Default Value:

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
   $("#diagramcontent").ejDiagram({
	   dataSourceSettings: {
       dataSource: ej.DataManager({ url: "http://mvc.syncfusion.com/Services/Northwnd.svc/" }),
       query: ej.Query().from("Employees").select("EmployeeID,ReportsTo,FirstName"),
	   //Table name
       tableName: "Employees", 
	   id: "EmployeeID", parent: "ReportsTo" }
   });
</script>

{% endhighlight %}

### defaultSettings `Object`
{:#members:defaultsettings}

Initializes the default values for nodes and connectors

#### Default Value:

* {}

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({
    defaultSettings: { node: { fillColor:"red"} }
});
</script>

{% endhighlight %}

### defaultSettings.connector `Object`
{:#members:defaultsettings-connector}

Initializes the default connector properties

#### Default Value:

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({
	//Apply default styles to all connectors
    defaultSettings: { connector: { lineColor:"red", lineWidth:4, lineDashArray:"2,2" } }
});
</script>

{% endhighlight %}

### defaultSettings.group `Object`
{:#members:defaultsettings-group}

Initializes the default properties of groups

#### Default Value:

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var NodeConstraints = ej.datavisualization.Diagram.NodeConstraints;
$("#diagramcontent").ejDiagram({
	//Disable dragging all groups
    defaultSettings: { group: {constraints: NodeConstraints.Default & ~NodeConstraints.Drag } }
});
</script>

{% endhighlight %}

### defaultSettings.node `Object`
{:#members:defaultsettings-node}

Initializes the default properties for nodes

#### Default Value:

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({
	//Apply same style to all nodes
    defaultSettings: { node: { fillColor:"red", borderColor:"black" } }
});
</script>

{% endhighlight %}

### drawType `Object`
{:#members:drawtype}

Sets the type of JSON object to be drawn through drawing tool

#### Default Value:

* {}

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({drawType:{type:"node"}});
</script>

{% endhighlight %}

### enableAutoScroll `Boolean`
{:#members:enableautoscroll}

Enables or disables auto scroll in diagram

#### Default Value:

* true

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({ enableAutoScroll: false });
</script>

{% endhighlight %}

### enableContextMenu `Boolean`
{:#members:enablecontextmenu}

Enables or disables diagram context menu

#### Default Value:

* true

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({ enableContextMenu: false });
</script>

{% endhighlight %}

### height `String`
{:#members:height}

Specifies the height of the diagram

#### Default Value

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({ height:"500" });
</script>

{% endhighlight %}

### historyManager `Object`
{:#members:historymanager}

Customizes the undo redo functionality

### historyManager.canPop `function`
{:#members:historymanager-canpop}

A method that takes a history entry as argument and returns whether the specific entry can be popped or not

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>

//Add a change to history manager
var diagram = $("#diagramcontent").ejDiagram("instance");
var entry = { object: node, prevState: node.empInfo };
diagram.model.historyManager.push(entry);
var newValue = { role: "New role" };
node.empInfo = newValue;

//Pop if the change doesn't need to be tracked
if(diagram.model.historyManager.canPop(entry))
	diagram.model.historyManager.pop();
	
</script>

{% endhighlight %}

### historyManager.closeGroupAction `function`
{:#members:historymanager-closegroupaction}

A method that ends grouping the changes

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var group = diagram.model.selectedItems

// Start to group the changes
diagram.model.historyManager.startGroupAction();

//Makes the changes
for (var i = 0; i < group.children.length; i++) {
	var option = {};
	var item = group.children[i];
	// Updates the fillColor for all the child elements.
	option.fillColor = args.style.backgroundColor;
	diagram.updateNode(item.name, option);
}

//Ends grouping the changes
diagram.model.historyManager.closeGroupAction();
</script>

{% endhighlight %}

### historyManager.pop `function`
{:#members:historymanager-pop}

A method that removes the history of a recent change made in diagram 

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>

var diagram = $("#diagramcontent").ejDiagram("instance");
//Pop the last change
diagram.model.historyManager.pop();	
</script>
{% endhighlight %}

### historyManager.push `function`
{:#members:historymanager-push}

A method that allows to track the custom changes made in diagram

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>

var diagram = $("#diagramcontent").ejDiagram("instance");

//Creates a custom entry and adds that to history manager
var entry = { object: node, prevState: node.empInfo };
diagram.model.historyManager.push(entry);

//Updates the new information
var newValue = { role: "New role" };
node.empInfo = newValue;

</script>

{% endhighlight %}

### historyManager.redo `function`
{:#members:historymanager-redo}

Defines what should be happened while trying to restore a custom change

#### Default Value:

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({
	historyManager: {
		//Called to revert a custom action
		undo: customUndoRedo,
		//Called to restore the reverted custom action
		redo: customUndoRedo
	}
});

//Method to handle the custom action
function customUndoRedo(args) {
	var diagram = $("#diagramcontent").ejDiagram("instance");
	var node = args.object;
	var currentState = node.empInfo;

	//Resets the state
	node.empInfo = args.prevState;

	//Saves the previous state
	args.prevState = currentState;
}	
</script>

{% endhighlight %}

### historyManager.startGroupAction `function`
{:#members:historymanager-startgroupaction}

A method that starts to group the changes to revert/restore them in a single undo or redo

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var group = diagram.model.selectedItems

// Start to group the changes
diagram.model.historyManager.startGroupAction();

//Makes the changes
for (var i = 0; i < group.children.length; i++) {
	var option = {};
	var item = group.children[i];
	// Updates the fillColor for all the child elements.
	option.fillColor = args.style.backgroundColor;
	diagram.updateNode(item.name, option);
}

//Ends grouping the changes
diagram.model.historyManager.closeGroupAction();
</script>

{% endhighlight %}

### historyManager.undo `function`
{:#members:historymanager-undo}

Defines what should be happened while trying to revert a custom change

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({
	historyManager: {
		//Called to revert a custom action
		undo: customUndoRedo,
		//Called to restore the reverted custom action
		redo: customUndoRedo
	}
});

//Method to handle the custom action
function customUndoRedo(args) {
	var diagram = $("#diagramcontent").ejDiagram("instance");
	var node = args.object;
	var currentState = node.empInfo;

	//Resets the state
	node.empInfo = args.prevState;

	//Saves the previous state
	args.prevState = currentState;
}	
</script>

{% endhighlight %}

### layout `object`
{:#members:layout}

Automatically arranges the nodes and connectors in a predefined manner.

### layout.bounds `Object`
{:#members:layout-bounds}

Specifies the custom bounds to arrange/align the layout

#### Default Value:

* ej.datavisualization.Diagram.Rectangle() 

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
// bounds of the layout
$("#diagramcontent").ejDiagram({layout: { bounds:{ x: 0, y: 0, width: 1000, height: 1000} }});
</script>

{% endhighlight %}


### layout.fixedNode `String`
{:#members:layout-fixednode}

Defines the fixed node with reference to which, the layout will be arranged and fixed node will not be repositioned

#### Default Value:

* ""

#### Example

{% highlight html %}

//fixedNode of the layout
$("#diagramcontent").ejDiagram({ layout: { fixedNode: "nodename"}});

{% endhighlight %}

### layout.getLayoutInfo `Object`
{:#members:layout-getlayoutinfo}

Customizes the orientation of trees/sub trees. For orientations, see [Chart Orientations](/js/api/global#chartorientations). For chart types, see [Chart Types](/js/api/global#charttypes)

#### Default Value:

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
function getLayoutInfo(diagram, node, options) { options.orientation = "vertical"; options.type = "left"; offset = 10;};
$("#diagramcontent").ejDiagram({layout: { getLayoutInfo:getLayoutInfo } });
</script>

{% endhighlight %}

### layout.horizontalSpacing `Number`
{:#members:layout-horizontalspacing}

Sets the space to be horizontally left between nodes

#### Default Value:

* 30

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
//horizontalSpacing of the layout
$("#diagramcontent").ejDiagram({layout: { horizontalSpacing: 50 }});
</script>

{% endhighlight %}


### layout.margin `Object`
{:#members:layout-margin}

Defines the space to be left between layout bounds and layout.

#### Default Value:

* ej.datavisualization.Diagram.Margin()

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
// margin of the layout
$("#diagramcontent").ejDiagram({layout: { margin:{ left: 10, right: 10, top: 10, bottom: 10} }});
</script>

{% endhighlight %}

### layout.horizontalAlignment `enum`
{:#members:layout-horizontalalignment}

<ts name = "ej.datavisualization.Diagram.HorizontalAlignment"/>

Defines how to horizontally align the layout within the layout bounds

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">Left</td>
            <td class="description last">Used to align layout horizontally on left side of layout bounds</td>
        </tr>
        <tr>
            <td class="name">Center</td>
            <td class="description last">Used to align layout horizontally on center of layout bounds</td>
        </tr>
        <tr>
            <td class="name">Right</td>
            <td class="description last">Used to align layout horizontally on right side of layout bounds</td>
        </tr>
    </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.HorizontalAlignment.Center

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({layout: { horizontalAlignment:ej.datavisualization.Diagram.HorizontalAlignment.Center }});
</script>

{% endhighlight %}


### layout.verticalAlignment `enum`
{:#members:layout-verticalalignment }

<ts name = "ej.datavisualization.Diagram.VerticalAlignment"/>

Defines how to vertically align the layout within the layout bounds

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">Top</td>
            <td class="description last">Used to align layout vertically on top of layout bounds</td>
       </tr>
        <tr>
            <td class="name">Center</td>
            <td class="description last">Used to align layout vertically on center of layout bounds</td>
       </tr>
        <tr>
            <td class="name">Bottom</td>
            <td class="description last">Used to align layout vertically on bottom of layout bounds</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.VerticalAlignment.Center

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({layout: { verticalAlignment:ej.datavisualization.Diagram.VerticalAlignment.Center }});
</script>

{% endhighlight %}

### layout.orientation `enum`
{:#members:layout-orientation}

<ts name = "ej.datavisualization.Diagram.LayoutOrientations"/>

Sets the orientation/direction to arrange the diagram elements.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">TopToBottom</td>
            <td class="description last">Used to set LayoutOrientation from top to bottom</td>
       </tr>
        <tr>
            <td class="name">BottomToTop</td>
            <td class="description last">Used to set LayoutOrientation from bottom to top</td>
       </tr>
        <tr>
            <td class="name">LeftToRight</td>
            <td class="description last">Used to set LayoutOrientation from left to right</td>
       </tr>
        <tr>
            <td class="name">RightToLeft</td>
            <td class="description last">Used to set LayoutOrientation from right to left</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.LayoutOrientations.TopToBottom

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
//orientation of the layout
$("#diagramcontent").ejDiagram({layout: { orientation: ej.datavisualization.Diagram.LayoutOrientations.LeftToRight }});
</script>

{% endhighlight %}

### layout.type `enum`
{:#members:layout-type}

<ts name = "ej.datavisualization.Diagram.LayoutTypes"/>

Sets the type of the layout based on which the elements will be arranged.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">None</td>
            <td class="description last">Used not to set any specific layout</td>
       </tr>
        <tr>
            <td class="name">HierarchicalTree</td>
            <td class="description last">Used to set layout type as hierarchical layout</td>
       </tr>
        <tr>
            <td class="name">OrganizationalChart</td>
            <td class="description last">Used to set layout type as organnizational chart</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.LayoutTypes.None

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
//type of the layout
$("#diagramcontent").ejDiagram({ layout: { type: ej.datavisualization.Diagram.LayoutTypes.HierarchicalTree } });
</script>

{% endhighlight %}

### layout.verticalSpacing `Number`
{:#members:layout-verticalspacing}

Sets the space to be vertically left between nodes

#### Default Value:

* 30

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
//verticalSpacing of the layout
$("#diagramcontent").ejDiagram({layout: { verticalSpacing: 50 }});
</script>
{% endhighlight %}

### locale `String`
{:#members:locale}

Defines the current culture of diagram

#### Default Value:

* "en-US"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({ locale: "en-US" });
</script>

{% endhighlight %}

### nodes `Array`
{:#members:nodes}

Array of JSON objects where each object represents a node

#### Default Value:

* []

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes = [{ name: "node1", width: 175, height: 60, offsetX:100, offsetY:100}];
$("#diagramcontent").ejDiagram({ nodes:nodes });
</script>

{% endhighlight %}

### nodes.activity `enum`
{:#members:nodes-activity}

<ts name = "ej.datavisualization.Diagram.BPMNActivity"/>

Defines the type of BPMN Activity. Applicable, if the node is a BPMN activity.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">None</td>
            <td class="description last">Used to set BPMN Activity as None</td>
       </tr>
        <tr>
            <td class="name">Task</td>
            <td class="description last">Used to set BPMN Activity as Task</td>
       </tr>
        <tr>
            <td class="name">SubProcess</td>
            <td class="description last">Used to set BPMN Activity as SubProcess</td>
       </tr>
   </tbody>
</table>


#### Default Value:

* ej.datavisualization.Diagram.BPMNActivity.Task

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{type: "bpmn", shape: ej.datavisualization.Diagram.BPMNShapes.Activity, activity: ej.datavisualization.Diagram.BPMNActivity.SubProcess, width:50, height:50}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.addInfo `Object`
{:#members:nodes-addinfo}

To maintain additional information about nodes

#### Default Value:

* {}

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var addInfo = { TooltipData: "Shares the information with the customer" };
//Add Info for nodes
var node1 = { name: "node1", addInfo: addInfo, offsetX:100, offsetY:100, width:50, height:50 };

//Define add Info for swimlane
var node2 = { type: "swimlane", name: "swimlane", addInfo: addInfo };
$("#diagramcontent").ejDiagram({nodes:[node1, node2]});
</script>

{% endhighlight %}

### nodes.annotation `Object`
{:#members:nodes-annotation}

Defines the additional information of a process. It is not directly related to the message flows or sequence flows of the process.

#### Default Value:

* ej.datavisualization.Diagram.BPMNTextAnnotation()

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
		type:"bpmn", shape: "activity",
        annotation: { text: "This is a BPMN Activity shape", width: 100, height: 50,
            angle: -45, length: 150, direction: "top" } }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}
            
### nodes.annotation.angle `Number`
{:#members:nodes-annotation-angle}

Sets the angle between the BPMN shape and the annotation 

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
		type:"bpmn", shape: "activity",
        annotation: { text: "This is a BPMN Activity shape", width: 100, height: 50,
            angle: -45  } }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}
            
### nodes.annotation.direction `enum`
{:#members:nodes-annotation-direction}

<ts name = "ej.datavisualization.Diagram.BPMNAnnotationDirection"/>

Sets the direction of the text annotation

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">Left</td>
            <td class="description last">Used to set the direction of BPMN Annotation as left</td>
       </tr>
        <tr>
            <td class="name">Right</td>
            <td class="description last">Used to set the direction of BPMN Annotation as right</td>
       </tr>
        <tr>
            <td class="name">Top</td>
            <td class="description last">Used to set the direction of BPMN Annotation as top</td>
       </tr>
        <tr>
            <td class="name">Bottom</td>
            <td class="description last">Used to set the direction of BPMN Annotation as bottom</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.BPMNAnnotationDirections.Left

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
		type:"bpmn", shape: "activity",
        annotation: { text: "This is a BPMN Activity shape", 
            direction:"right", length: 130, angle: -45, 
            width: 100, height: 50 } }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.annotation.height `Number`
{:#members:nodes-annotation-height}

Sets the height of the text annotation
			
#### Default Value:

* 20

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
		type:"bpmn", shape: "activity",
        annotation: { text: "This is a BPMN Activity shape", height: 50,
            } }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.annotation.length `Number`
{:#members:nodes-annotation-length}

Sets the distance between the BPMN shape and the annotation 
			
#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
		type:"bpmn", shape: "activity",
        annotation: { text: "This is a BPMN Activity shape", width: 100, height: 50,
           length: 150  } }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.annotation.text `String`
{:#members:nodes-annotation-text}

Defines the additional information about the flow object in a BPMN Process
			
#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
		type:"bpmn", shape: "activity",
        annotation: { text: "This is a BPMN Activity shape", width: 100
            } }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.annotation.width `Number`
{:#members:nodes-annotation-width}

Sets the  width of the text annotation
			
#### Default Value:

* 20

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
		type:"bpmn", shape: "activity",
        annotation: { text: "This is a BPMN Activity shape", width: 100
            } }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.borderColor `String`
{:#members:nodes-bordercolor}

Sets the border color of node

#### Default Value:

* "black"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, borderColor: "red" }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.borderDashArray `String`
{:#members:nodes-borderdasharray}

Sets the pattern of dashes and gaps to stroke the border

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>

<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, borderColor: "red" , borderDashArray: "4,2"}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.borderWidth `Number`
{:#members:nodes-borderwidth}

Sets the border width of the node

#### Default Value:

* 1

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, borderColor: "red" , borderDashArray: "2,2", borderWidth:2}];
$("#diagramcontent").ejDiagram({ nodes:nodes });
</script>

{% endhighlight %}

### nodes.canUngroup `Boolean`
{:#members:nodes-canungroup}

Defines whether the group can be ungrouped or not

#### Default Value:

* true

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
var node1 = { name: "node1", width: 50, height:50, offsetX:50, offsetY:50, borderColor: "red" , borderDashArray: "4,2"};
var node2 = { name: "node2", width: 50, height:50, offsetX:150, offsetY:150, borderColor: "red" , borderDashArray: "4,2"};
var group = { name :"group", children:[node1, node2], canUngroup: false };
$("#diagramcontent").ejDiagram({nodes:[group]});
</script>

{% endhighlight %}

### nodes.children `Array`
{:#members:nodes-children}

Array of JSON objects where each object represents a child node/connector

#### Default Value:

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
$("#diagramcontent").ejDiagram({ nodes:[group] });
</script>

{% endhighlight %}

### nodes.classifier `enum`
{:#members:nodes-classifier}

<ts name = "ej.datavisualization.Diagram.ClassifierShapes"/>

Sets the type of UML classifier. Applicable, if the node is a UML Class Diagram shape.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">class</td>
            <td class="description last">Used to define a Class</td>
       </tr>
        <tr>
            <td class="name">Interface</td>
            <td class="description last">Used to define an Interface</td>
       </tr>
        <tr>
            <td class="name">Enumeration</td>
            <td class="description last">Used to define an Enumeration</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.ClassifierShapes.Class

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ name: "Patient",offsetX: 100,offsetY: 100,borderWidth: 2,borderColor: "black",type: "umlclassifier", classifier: ej.datavisualization.Diagram.ClassifierShapes.Class}];
$("#DiagramContent").ejDiagram({ nodes:nodes });
</script>

{% endhighlight %}

### nodes.class `Object`
{:#members:nodes-class}

Defines the name, attributes and methods of a Class. Applicable, if the node is a Class.

#### Default Value:

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ name: "Patient",offsetX: 100,offsetY: 100,borderWidth: 2,borderColor: "black",type: "umlclassifier", classifier: ej.datavisualization.Diagram.ClassifierShapes.Class,
          "class": {name: "Patient", },}];
$("#DiagramContent").ejDiagram({ nodes:nodes });
</script>

{% endhighlight %}

### nodes.class.name `String`
{:#members:nodes-class.name}

Sets the name of class.

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ name: "Patient",offsetX: 100,offsetY: 100,borderWidth: 2,borderColor: "black",type: "umlclassifier", classifier: ej.datavisualization.Diagram.ClassifierShapes.Class,
          "class": {name: "Patient", },}];
$("#DiagramContent").ejDiagram({ nodes:nodes });
</script>

{% endhighlight %}

### nodes.class.attributes `Array`
{:#members:nodes-class.attributes}

Defines the collection of attributes

#### Default Value:

* []

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ name: "Patient",offsetX: 100,offsetY: 100,borderWidth: 2,borderColor: "black",type: "umlclassifier", classifier: ej.datavisualization.Diagram.ClassifierShapes.Class,
          "class": {name: "Patient", attributes: [{ name: "accepted",}], },}];
$("#DiagramContent").ejDiagram({ nodes:nodes });

</script>

{% endhighlight %}

### nodes.class.attributes.name `String`
{:#members:nodes-class.attributes.name}

Sets the name of the attribute

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ name: "Patient",offsetX: 100,offsetY: 100,borderWidth: 2,borderColor: "black",type: "umlclassifier", classifier: ej.datavisualization.Diagram.ClassifierShapes.Class,
          "class": {name: "Patient", attributes: [{ name: "accepted" }], },}];
$("#DiagramContent").ejDiagram({ nodes:nodes });

</script>

{% endhighlight %}

### nodes.class.attributes.type `String`
{:#members:nodes-class.attributes.type}

Sets the data type of attribute

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ name: "Patient",offsetX: 100,offsetY: 100,borderWidth: 2,borderColor: "black",type: "umlclassifier", classifier: ej.datavisualization.Diagram.ClassifierShapes.Class,
          "class": {name: "Patient", attributes: [{ name: "accepted", type: "Date", }], },}];
$("#DiagramContent").ejDiagram({ nodes:nodes });

</script>

{% endhighlight %}

### nodes.class.attributes.scope `String`
{:#members:nodes-class.attributes.scope}

Defines the visibility of the attribute

#### Default Value:

* ej.datavisualization.Diagram.ScopeValueDefaults.Public

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ name: "Patient",offsetX: 100,offsetY: 100,borderWidth: 2,borderColor: "black",type: "umlclassifier", classifier: ej.datavisualization.Diagram.ClassifierShapes.Class,
          "class": {name: "Patient", attributes: [{ name: "accepted", type: "Date", scope:"protected" }], },}];
$("#DiagramContent").ejDiagram({ nodes:nodes });

</script>

{% endhighlight %}

### nodes.class.methods `Array`
{:#members:nodes-class.methods}

Defines the collection of methods of a Class.

#### Default Value:

* []

#### Example

{% highlight html %}

<<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ name: "Patient",offsetX: 100,offsetY: 100,borderWidth: 2,borderColor: "black",type: "umlclassifier", classifier: ej.datavisualization.Diagram.ClassifierShapes.Class,
          "class": {name: "Patient", methods: [{ name: "getHistory" }]  },}];
$("#DiagramContent").ejDiagram({ nodes:nodes });

</script>

{% endhighlight %}

## nodes.class.methods.name `String`
{:#members:nodes-class.methods.name}

Sets the name of the method.

#### Default Value:

* ""

#### Example

{% highlight html %}

<<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ name: "Patient",offsetX: 100,offsetY: 100,borderWidth: 2,borderColor: "black",type: "umlclassifier", classifier: ej.datavisualization.Diagram.ClassifierShapes.Class,
          "class": {name: "Patient", methods: [{ name: "getHistory", arguments: [{name: "Date" }], }]  },}];
$("#DiagramContent").ejDiagram({ nodes:nodes });

</script>

{% endhighlight %}

## nodes.class.methods.arguments `Array`
{:#members:nodes-class.methods.arguments}

Defines the arguments of the method.

#### Default Value:

* []

#### Example

{% highlight html %}

<<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ name: "Patient",offsetX: 100,offsetY: 100,borderWidth: 2,borderColor: "black",type: "umlclassifier", classifier: ej.datavisualization.Diagram.ClassifierShapes.Class,
          "class": {name: "Patient", methods: [{ name: "getHistory", arguments: [{name: "Date",type:"String" }], }]  },}];
$("#DiagramContent").ejDiagram({ nodes:nodes });

</script>

{% endhighlight %}

## nodes.class.methods.arguments.name `String`
{:#members:nodes-class.methods.arguments.name}

Sets the name of the argument

#### Default Value:

* ""

#### Example

{% highlight html %}

<<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ name: "Patient",offsetX: 100,offsetY: 100,borderWidth: 2,borderColor: "black",type: "umlclassifier", classifier: ej.datavisualization.Diagram.ClassifierShapes.Class,
          "class": {name: "Patient", methods: [{ name: "getHistory", arguments: [{name: "Date" }], type: "History" }]  },}];
$("#DiagramContent").ejDiagram({ nodes:nodes });

</script>

{% endhighlight %}

## nodes.class.methods.arguments.type `String`
{:#members:nodes-class.methods.arguments.type}

Sets the type of the argument

#### Default Value:

* ""

#### Example

{% highlight html %}

<<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ name: "Patient",offsetX: 100,offsetY: 100,borderWidth: 2,borderColor: "black",type: "umlclassifier", classifier: ej.datavisualization.Diagram.ClassifierShapes.Class,
          "class": {name: "Patient", methods: [{ name: "getHistory", arguments: [{name: "Date" }], type: "History" }]  },}];
$("#DiagramContent").ejDiagram({ nodes:nodes });

</script>

{% endhighlight %}

## nodes.class.methods.type `String`
{:#members:nodes-class.methods.type}

Sets the return type of the method

#### Default Value:

* ""

#### Example

{% highlight html %}

<<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ name: "Patient",offsetX: 100,offsetY: 100,borderWidth: 2,borderColor: "black",type: "umlclassifier", classifier: ej.datavisualization.Diagram.ClassifierShapes.Class,
          "class": {name: "Patient", methods: [{ name: "getHistory", arguments: [{name: "Date" }], type: "History" }]  },}];
$("#DiagramContent").ejDiagram({ nodes:nodes });

</script>

{% endhighlight %}

### nodes.class.methods.scope `String`
{:#members:nodes-class.methods.scope}

Sets the visibility of the method.

#### Default Value:

* ej.datavisualization.Diagram.ScopeValueDefaults.Public

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ name: "Patient",offsetX: 100,offsetY: 100,borderWidth: 2,borderColor: "black",type: "umlclassifier", classifier: ej.datavisualization.Diagram.ClassifierShapes.Class,
          "class": {name: "Patient", methods: [{ name: "getHistory", arguments: [{name: "Date" }], type: "History",scope:"protected" }]  },}];
$("#DiagramContent").ejDiagram({ nodes:nodes });

</script>

{% endhighlight %}

### nodes.connectorPadding `Number`
{:#members:nodes-connectorpadding}

Defines the distance to be left between a node and its connections(In coming and out going connections).

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, connectorPadding: 5}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.constraints `enum`
{:#members:nodes-constraints}

<ts name = "ej.datavisualization.Diagram.NodeConstraints"/>

Enables or disables the default behaviors of the node.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">None</td>
            <td class="description last">Disable all node Constraints</td>
       </tr>
        <tr>
            <td class="name">Select</td>
            <td class="description last">Enables node to be selected</td>
       </tr>
        <tr>
            <td class="name">Delete</td>
            <td class="description last">Enables node to be Deleted</td>
       </tr>
        <tr>
            <td class="name">Drag</td>
            <td class="description last">Enables node to be Dragged</td>
       </tr>
        <tr>
            <td class="name">Rotate</td>
            <td class="description last">Enables node to be Rotated</td>
       </tr>
        <tr>
            <td class="name">Connect</td>
            <td class="description last">Enables node to be connected</td>
       </tr>
        <tr>
            <td class="name">ResizeNorthEast</td>
            <td class="description last">Enables node to be resize north east</td>
       </tr>
        <tr>
            <td class="name">ResizeEast</td>
            <td class="description last">Enables node to be resize east</td>
       </tr>
        <tr>
            <td class="name">ResizeSouthEast</td>
            <td class="description last">Enables node to be resize south east</td>
       </tr>
        <tr>
            <td class="name">ResizeSouth</td>
            <td class="description last">Enables node to be resize south</td>
       </tr>
        <tr>
            <td class="name">ResizeSouthWest</td>
            <td class="description last">Enables node to be resize south west</td>
       </tr>
        <tr>
            <td class="name">ResizeWest</td>
            <td class="description last">Enables node to be resize west</td>
       </tr>
        <tr>
            <td class="name">ResizeNorthWest</td>
            <td class="description last">Enables node to be resize north west</td>
       </tr>
        <tr>
            <td class="name">ResizeNorth</td>
            <td class="description last">Enables node to be resize north</td>
       </tr>
        <tr>
            <td class="name">Resize</td>
            <td class="description last">Enables node to be Resized</td>
       </tr>
        <tr>
            <td class="name">Shadow</td>
            <td class="description last">Enables shadow</td>
       </tr>
        <tr>
            <td class="name">DragLabel</td>
            <td class="description last">Enables label of node to be Dragged</td>
       </tr>
        <tr>
            <td class="name">AllowPan</td>
            <td class="description last">Enables panning should be done while node dragging</td>
       </tr>
        <tr>
            <td class="name">AspectRatio</td>
            <td class="description last">Enables Proportional resize for node</td>
       </tr>
        <tr>
            <td class="name">PointerEvents</td>
            <td class="description last">Enables the user interaction with the node</td>
       </tr>
        <tr>
            <td class="name">Default</td>
            <td class="description last">Enables all node constraints</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.NodeConstraints.Default

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var NodeConstraints = ej.datavisualization.Diagram.NodeConstraints;
//Disable selection
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
	constraints: NodeConstraints.Default & ~NodeConstraints.Select}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.container `Object`
{:#members:nodes-container}

Defines how the child objects need to be arranged(Either in any predefined manner or automatically). Applicable, if the node is a group.

#### Default Value:

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var node1 = { name: "node1", width: 50, height:50, borderColor: "red" , borderDashArray: "4,2"};
var node2 = { name: "node2", width: 50, height:50, borderColor: "red" , borderDashArray: "4,2"};
var group = {name :"group", children:[node1, node2], container: { type: "stack" }, offsetX:200, offsetY:100 };
$("#diagramcontent").ejDiagram({nodes:[group]});
</script>

{% endhighlight %}

### nodes.container.orientation `String`
{:#members:nodes-container-orientation}

Defines the orientation of the container. Applicable, if the group is a container.

#### Default Value:

* "vertical"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
var node1 = { name: "node1", width: 50, height:50, borderColor: "red" , borderDashArray: "4,2"};
var node2 = { name: "node2", width: 50, height:50, borderColor: "red" , borderDashArray: "4,2"};
var group = {name :"group", children:[node1, node2], container: { type: "stack", orientation: "horizontal" }, offsetX:200, offsetY:100 };
$("#diagramcontent").ejDiagram({nodes:[group]});
</script>

{% endhighlight %}

### nodes.container.type `enum`
{:#members:nodes-container-type}

<ts name = "ej.datavisualization.Diagram.ContainerType"/>

Sets the type of the container. Applicable if the group is a container.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">Canvas</td>
            <td class="description last">Sets the container type as Canvas</td>
       </tr>
        <tr>
            <td class="name">Stack</td>
            <td class="description last">Sets the container type as Stack</td>
       </tr>
   </tbody>
</table>

#### Default Value:

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
$("#diagramcontent").ejDiagram({nodes:[group]});
</script>

{% endhighlight %}

### nodes.cornerRadius `Number`
{:#members:nodes-cornerradius}

Defines the corner radius of rectangular shapes.

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
	type:"basic", shape:"rectangle", cornerRadius:5}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.cssClass `String`
{:#members:nodes-cssclass}

Configures the styles of shapes

#### Default Value:

* ""

#### Example

{% highlight html %}

<style>
    .hoverNode:hover {
        fill:blue
    }
</style>

<div id="diagramcontent"></div>
<script>
var node = { name: "node", 
	         cssClass: "hoverNode", 
	         width: 50, height: 50, offsetX: 100, offsetY: 100 };
			 
$("#diagramcontent").ejDiagram({ nodes:[node] });
</script>

{% endhighlight %}

### nodes.data `Object`
{:#members:nodes-data}
 
Defines the BPMN data object

### nodes.data.type `enum`
{:#members:nodes-data-type}

<ts name = "ej.datavisualization.Diagram.BPMNDataObjects"/>
 
Sets the type of the BPMN Data object

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">Input</td>
            <td class="description last">Used to notate the Input type BPMN data object</td>
       </tr>
        <tr>
            <td class="name">Output</td>
            <td class="description last">Used to notate the Output type BPMN data object</td>
       </tr>
        <tr>
            <td class="name">None</td>
            <td class="description last">Used to set BPMN data object type as None</td>
       </tr>
    </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.BPMNDataObjects.None

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{name:"dataobject", type: "bpmn", shape:ej.datavisualization.Diagram.BPMNShapes.DataObject, data: { type: ej.datavisualization.Diagram.BPMNDataObjects.Input }, width:50, height: 50, offsetX:100, offsetY:100}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.data.collection `Boolean`
{:#members:nodes-data-collection}

Defines whether the BPMN data object is a collection or not

#### Default Value:

* false

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{name:"dataobject", type: "bpmn", shape:ej.datavisualization.Diagram.BPMNShapes.DataObject, data: { type: ej.datavisualization.Diagram.BPMNDataObjects.Input, collection: false }, width:50, height: 50, offsetX:100, offsetY:100}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}


### nodes.enumeration `Object`
{:#members:nodes-enumeration}

Defines an Enumeration in a UML Class Diagram

#### Default Value:

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ name: "Enums",offsetX: 100,offsetY: 100,borderWidth: 2,borderColor: "black",type: "umlclassifier",classifier: ej.datavisualization.Diagram.ClassifierShapes.Enumeration, 
      enumeration:{ name: "AccountType", }}];
$("#DiagramContent").ejDiagram({ nodes:nodes });

</script>

{% endhighlight %}

### nodes.enumeration.name `String`
{:#members:nodes-enumeration.name}

Sets the name of the Enumeration

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ name: "Enums",offsetX: 100,offsetY: 100,borderWidth: 2,borderColor: "black",type: "umlclassifier",classifier: ej.datavisualization.Diagram.ClassifierShapes.Enumeration, 
      enumeration:{ name: "AccountType", }}];
$("#DiagramContent").ejDiagram({ nodes:nodes });

</script>

{% endhighlight %}

### nodes.enumeration.members `Array`
{:#members:nodes-enumeration.members}

Defines the collection of enumeration members

#### Default Value:

* []

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ name: "Enums",offsetX: 100,offsetY: 100,borderWidth: 2,borderColor: "black",type: "umlclassifier",classifier: ej.datavisualization.Diagram.ClassifierShapes.Enumeration, 
      enumeration:{ name: "AccountType", members: [{ name: "CheckingAccount"}]}}];
$("#DiagramContent").ejDiagram({ nodes:nodes });

</script>

{% endhighlight %}

### nodes.enumeration.members.name `String`
{:#members:nodes-enumeration.members.name}

Sets the name of the enumeration member

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ name: "Enums",offsetX: 100,offsetY: 100,borderWidth: 2,borderColor: "black",type: "umlclassifier",classifier: ej.datavisualization.Diagram.ClassifierShapes.Enumeration, 
      enumeration:{ name: "AccountType", members: [{ name: "CheckingAccount"}]}}];
$("#DiagramContent").ejDiagram({ nodes:nodes });

</script>

{% endhighlight %}

### nodes.event `enum`
{:#members:nodes-event}

<ts name = "ej.datavisualization.Diagram.BPMNEvents"/>

Sets the type of the BPMN Events. Applicable, if the node is a BPMN event.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">Start</td>
            <td class="description last">Used to set BPMN Event as Start</td>
       </tr>
        <tr>
            <td class="name">Intermediate</td>
            <td class="description last">Used to set BPMN Event as Intermediate</td>
       </tr>
        <tr>
            <td class="name">End</td>
            <td class="description last">Used to set BPMN Event as End</td>
       </tr>
        <tr>
            <td class="name">NonInterruptingStart</td>
            <td class="description last">Used to set BPMN Event as NonInterruptingStart</td>
       </tr>
        <tr>
            <td class="name">NonInterruptingIntermediate</td>
            <td class="description last">Used to set BPMN Event as NonInterruptingIntermediate</td>
       </tr>
        <tr>
            <td class="name">ThrowingIntermediate</td>
            <td class="description last">Used to set BPMN Event as ThrowingIntermediate</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.BPMNEvents.Start

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ type: "bpmn", shape: "event" , 
	     event: ej.datavisualization.Diagram.BPMNEvents.Intermediate, width:50, height:50}];
$("#diagramcontent").ejDiagram({ nodes:nodes });
</script>

{% endhighlight %}

### nodes.excludeFromLayout `Boolean`
{:#members:nodes-excludefromlayout}

Defines whether the node can be automatically arranged using layout or not

#### Default Value:

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

$("#diagramcontent").ejDiagram({
      nodes:[ node1, node2, node3 ],
      layout:{type:"hierarchicaltree"}
});

</script>

{% endhighlight %}

### nodes.fillColor `String`
{:#members:nodes-fillcolor}

Defines the fill color of the node

#### Default Value:

* "white"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, fillColor:"red" }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.gateway `enum`
{:#members:nodes-gateway}

<ts name = "ej.datavisualization.Diagram.BPMNGateways"/>

Sets the type of the BPMN Gateway. Applicable, if the node is a BPMN gateway.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">None</td>
            <td class="description last">Used to set BPMN Gateway as None</td>
       </tr>
        <tr>
            <td class="name">Exclusive</td>
            <td class="description last">Used to set BPMN Gateway as Exclusive</td>
       </tr>
        <tr>
            <td class="name">Inclusive</td>
            <td class="description last">Used to set BPMN Gateway as Inclusive</td>
       </tr>
        <tr>
            <td class="name">Parallel</td>
            <td class="description last">Used to set BPMN Gateway as Parallel</td>
       </tr>
        <tr>
            <td class="name">Complex</td>
            <td class="description last">Used to set BPMN Gateway as Complex</td>
       </tr>
        <tr>
            <td class="name">EventBased</td>
            <td class="description last">Used to set BPMN Gateway as EventBased</td>
       </tr>
        <tr>
            <td class="name">ExclusiveEventBased</td>
            <td class="description last">Used to set BPMN Gateway as ExclusiveEventBased</td>
       </tr>
        <tr>
            <td class="name">ParallelEventBased</td>
            <td class="description last">Used to set BPMN Gateway as ParallelEventBased</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.BPMNGateways.None

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ type: "bpmn", shape: "gateway" , gateway: ej.datavisualization.Diagram.BPMNGateways.Exclusive, width:50, height:50 }];
$("#diagramcontent").ejDiagram({ nodes:nodes });
</script>

{% endhighlight %}

### nodes.gradient `object`
{:#members:nodes-gradient}

Paints the node with a smooth transition from one color to another color

### nodes.gradient.LinearGradient `Object`
{:#members:nodes-gradient-lineargradient}

Paints the node with linear color transitions

### nodes.gradient.LinearGradient.stops `Array`
{:#members:nodes-gradient-lineargradient-stops}

Defines the different colors and the region of color transitions

#### Default Value:

* []

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
 var gradient = {
     type: "linear", x1: 0, x2: 50, y1: 0, y2: 50, stops: [
     { color: "white", offset: 0}, { color: "red", offset: 50}]
};
var nodes = [{name: "Node1", width: 100, height: 100, gradient : gradient}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.gradient.LinearGradient.x1 `Number`
{:#members:nodes-gradient-lineargradient-x1}

Defines the left most position(relative to node) of the rectangular region that needs to be painted

#### Default Value:

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
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.gradient.LinearGradient.x2 `Number`
{:#members:nodes-gradient-lineargradient-x2}

Defines the right most position(relative to node) of the rectangular region that needs to be painted

#### Default Value:

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
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.gradient.LinearGradient.y1 `Number`
{:#members:nodes-gradient-lineargradient-y1}

Defines the top most position(relative to node) of the rectangular region that needs to be painted

#### Default Value:

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
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.gradient.LinearGradient.y2 `Number`
{:#members:nodes-gradient-lineargradient-y2}

Defines the bottom most position(relative to node) of the rectangular region that needs to be painted

#### Default Value:

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
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.gradient.RadialGradient `Object`
{:#members:nodes-gradient-radialgradient}

Paints the node with radial color transitions. A focal point defines the beginning of the gradient, and a circle defines the end point of the gradient.

### nodes.gradient.RadialGradient.cx `Number`
{:#members:nodes-gradient-radialgradient-cx}

Defines the position of the outermost circle

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var node = { name: "node", width: 50, height: 50, offsetX: 100, offsetY:100,
             gradient:{ type:"radial", fx:50, fy:50, 
		     cx:50, cy:50,
             stops:[{color:"white", offset:0 }, {color:"red", offset:100}] } };

$("#diagramcontent").ejDiagram({ nodes:[node] });
</script>

{% endhighlight %}

### nodes.gradient.RadialGradient.cy `Number`
{:#members:nodes-gradient-radialgradient-cy}

Defines the outer most circle of the radial gradient

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var node = { name: "node", width: 50, height: 50, offsetX: 100, offsetY:100,
             gradient:{ type:"radial", fx:50, fy:50, 
		     cx:50, cy:50,
             stops:[{color:"white", offset:0 }, {color:"red", offset:100}] } };

$("#diagramcontent").ejDiagram({ nodes:[node] });
</script>

{% endhighlight %}

### nodes.gradient.RadialGradient.fx `Number`
{:#members:nodes-gradient-radialgradient-fx}

Defines the innermost circle of the radial gradient

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var node = { name: "node", width: 50, height: 50, offsetX: 100, offsetY:100,
             gradient:{ type:"radial", 
		     fx:50, fy:50, 
		     cx:50, cy:50,
             stops:[{color:"white", offset:0 }, {color:"red", offset:100}] } };

$("#diagramcontent").ejDiagram({ nodes:[node] });
</script>

{% endhighlight %}

### nodes.gradient.RadialGradient.fy `Number`
{:#members:nodes-gradient-radialgradient-fy}

Defines the innermost circle of the radial gradient

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var node = { name: "node", width: 50, height: 50, offsetX: 100, offsetY:100,
             gradient:{ type:"radial", fx:50, fy:50, 
		     cx:50, cy:50,
             stops:[{color:"white", offset:0 }, {color:"red", offset:100}] } };

$("#diagramcontent").ejDiagram({ nodes:[node] });
</script>

{% endhighlight %}

### nodes.gradient.RadialGradient.stops `Array`
{:#members:nodes-gradient-radialgradient-stops}

Defines the different colors and the region of color transitions.

#### Default Value:

* []

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var node = { name: "node", width: 50, height: 50, offsetX: 100, offsetY:100,
             gradient:
			 { 
				 type:"radial", fx:50, fy:50, 
		     	 cx:50, cy:50,
                 stops:[{color:"white", offset:0 }, 
			     { color:"red", offset:100 }] } };

$("#diagramcontent").ejDiagram({ nodes:[node] });
</script>

{% endhighlight %}

### nodes.gradient.Stop `Object`
{:#members:nodes-gradient-stop}

Defines the color and a position where the previous color transition ends and a new color transition starts

### nodes.gradient.Stop.color `String`
{:#members:nodes-gradient-stop-color}

Sets the color to be filled over the specified region

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var node = { name: "node", width: 50, height: 50, offsetX: 100, offsetY:100,
             gradient:{ type:"radial", fx:50, fy:50, 
		     cx:50, cy:50,
             stops:[
				 {color:"white", offset:0 }, 
				 {color:"red", offset:100}] } 
			};

$("#diagramcontent").ejDiagram({ nodes:[node] });
</script>

{% endhighlight %}

### nodes.gradient.Stop.offset `Number`
{:#members:nodes-gradient-stop-offset}

Sets the position where the previous color transition ends and a new color transition starts

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var node = { name: "node", width: 50, height: 50, offsetX: 100, offsetY:100,
             gradient:{ type:"radial", fx:50, fy:50, 
		     cx:50, cy:50,
             stops:[
				 {color:"white", offset:0 }, 
				 {color:"red", offset:100}] } 
			};

$("#diagramcontent").ejDiagram({ nodes:[node] });
</script>

{% endhighlight %}

### nodes.gradient.Stop.opacity `Number`
{:#members:nodes-gradient-stop-opacity}

Describes the transparency level of the region

#### Default Value:

* 1

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var node = { name: "node", width: 50, height: 50, offsetX: 100, offsetY:100,
			 gradient:{ type:"radial", 
			    fx:50, fy:50, cx:50, cy:70,
				stops:[
				{color:"white", offset:0 }, 
				//Sets the opacity
				{color:"red", offset:100, opacity: 0.5}] } 
			};
</script>

{% endhighlight %}

### nodes.group `Object`
{:#members:nodes-group}

Sets the type of the BPMN Shapes as group. Applicable, if the node is a BPMN.

#### Default Value:

* ej.datavisualization.Diagram.BPMNShapes

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{type: "bpmn", shape: ej.datavisualization.Diagram.BPMNShapes.Group}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.header `Object`
{:#members:nodes-header}

Defines the header of a swimlane/lane

#### Default Value:

* { text: "Title", fontSize: 11 }

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = { type: "swimlane", name: "swimlane", header: { text: "Swimlane", fontSize: 12, bold: true } };
$("#diagramcontent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.height `Number`
{:#members:nodes-height}

Defines the height of the node

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
// Set the height as 150
nodes = [{ name: "node1", width: 50, height:150, offsetX:50, offsetY:50 }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.horizontalAlign `enum`
{:#members:nodes-horizontalalign}

<ts name = "ej.datavisualization.Diagram.HorizontalAlignment"/>

Sets the horizontal alignment of the node. Applicable, if the parent of the node is a container.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">Left</td>
            <td class="description last">Used to align text horizontally on left side of node/connector</td>
       </tr>
        <tr>
            <td class="name">Center</td>
            <td class="description last">Used to align text horizontally on center of node/connector</td>
       </tr>
        <tr>
            <td class="name">Right</td>
            <td class="description last">Used to align text horizontally on right side of node/connector</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.HorizontalAlignment.Left

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
var node1 = { name: "node1", width: 50, height:50};
//Align the node at the right most position of the canvas
var node2 = { name: "node2", width: 50, height:50, horizontalAlign: ej.datavisualization.Diagram.HorizontalAlignment.Right };
var group = { name :"group", children:[ node1, node2 ], container: { type: "canvas" }, offsetX:200, offsetY:100, minWidth:200, minHeight: 200, fillColor:"gray" };
$("#diagramcontent").ejDiagram({nodes:[group]});
</script>

{% endhighlight %}

### nodes.inEdges `Array`
{:#members:nodes-inedges}

A read only collection of the incoming connectors/edges of the node

#### Default Value:

* []

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
//Read the incoming connections to the selected node
var node = diagram.selectionList[0];
for(var i = 0; i < node.inEdges.length; i++){
    console.log(node.inEdges[i]);
}
</script>

{% endhighlight %}

### nodes.interface `Object`
{:#members:nodes-interface}

Defines an interface in a UML Class Diagram

#### Default Value:

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ name: "Bank",offsetX: 100,offsetY: 100,borderWidth: 2,borderColor: "black",type: "umlclassifier", classifier: ej.datavisualization.Diagram.ClassifierShapes.Interface,}];
$("#DiagramContent").ejDiagram({ nodes:nodes });
</script>

{% endhighlight %}

### nodes.interface.name `String`
{:#members:nodes-interface.name}

Sets the name of the interface

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ name: "Bank",offsetX: 100,offsetY: 100,borderWidth: 2,borderColor: "black",type: "umlclassifier", classifier: ej.datavisualization.Diagram.ClassifierShapes.Interface,
          "interface": {name: "BankAccount",} }];
$("#DiagramContent").ejDiagram({ nodes:nodes });
</script>

{% endhighlight %}

### nodes.interface.attributes `Array`
{:#members:nodes-interface.attributes}

Defines a collection of attributes of the interface

#### Default Value:

* []

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ name: "Bank",offsetX: 100,offsetY: 100,borderWidth: 2,borderColor: "black",type: "umlclassifier", classifier: ej.datavisualization.Diagram.ClassifierShapes.Interface,
          "interface": {name: "BankAccount", attributes: [{ name: "ownar"}], },}];
$("#DiagramContent").ejDiagram({ nodes:nodes });

</script>

{% endhighlight %}

### nodes.interface.attributes.name `String`
{:#members:nodes-interface.attributes.name}

Sets the name of the attribute

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ name: "Bank",offsetX: 100,offsetY: 100,borderWidth: 2,borderColor: "black",type: "umlclassifier", classifier: ej.datavisualization.Diagram.ClassifierShapes.Interface,
          "interface": {name: "BankAccount", attributes: [{ name: "ownar"}], },}];
$("#DiagramContent").ejDiagram({ nodes:nodes });

</script>

{% endhighlight %}

### nodes.interface.attributes.type `String`
{:#members:nodes-interface.attributes.type}

Sets the type of the attribute

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ name: "Bank",offsetX: 100,offsetY: 100,borderWidth: 2,borderColor: "black",type: "umlclassifier", classifier: ej.datavisualization.Diagram.ClassifierShapes.Interface,
          "interface": {name: "BankAccount", attributes: [{ name: "ownar",  type: "String[*]" ,  }], },}];
$("#DiagramContent").ejDiagram({ nodes:nodes });

</script>

{% endhighlight %}

### nodes.interface.attributes.scope `String`
{:#members:nodes-interface.attributes.scope}

Sets the visibility of the attribute

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ name: "Bank",offsetX: 100,offsetY: 100,borderWidth: 2,borderColor: "black",type: "umlclassifier", classifier: ej.datavisualization.Diagram.ClassifierShapes.Interface,
          "interface": {name: "BankAccount", attributes: [{ name: "ownar",  type: "String[*]",scope:"protected" }], },}];
$("#DiagramContent").ejDiagram({ nodes:nodes });
</script>

{% endhighlight %}

### nodes.interface.methods `Array`
{:#members:nodes-interface.methods}

Defines the collection of public methods of an interface

#### Default Value:

* []

#### Example

{% highlight html %}

<<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ name: "Bank",offsetX: 100,offsetY: 100,borderWidth: 2,borderColor: "black",type: "umlclassifier", classifier: ej.datavisualization.Diagram.ClassifierShapes.Interface,
          "interface": {name: "BankAccount",methods: [{ name: "deposit", }]  },}];
$("#DiagramContent").ejDiagram({ nodes:nodes });

</script>

{% endhighlight %}

## nodes.interfaces.methods.name `String`
{:#members:nodes-interface.methods.name}

Sets the name of the method.

#### Default Value:

* ""

#### Example

{% highlight html %}

<<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ name: "Bank",offsetX: 100,offsetY: 100,borderWidth: 2,borderColor: "black",type: "umlclassifier", classifier: ej.datavisualization.Diagram.ClassifierShapes.Interface,
          "interface": {name: "BankAccount",methods: [{ name: "deposit", }]  },}];
$("#DiagramContent").ejDiagram({ nodes:nodes });

</script>

{% endhighlight %}

## nodes.interface.methods.arguments `Array`
{:#members:nodes-interface.methods.arguments}

Defines the collection of arguments of a method

#### Default Value:

* []

#### Example

{% highlight html %}

<<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ name: "Bank",offsetX: 100,offsetY: 100,borderWidth: 2,borderColor: "black",type: "umlclassifier", classifier: ej.datavisualization.Diagram.ClassifierShapes.Interface,
          "interface": {name: "BankAccount",methods: [{ name: "deposit", arguments: [{name:"amount", }],  }]  },}];
$("#DiagramContent").ejDiagram({ nodes:nodes });


</script>

{% endhighlight %}

## nodes.interface.methods.arguments.name `String`
{:#members:nodes-interface.methods.arguments.name}

Sets the name of the argument

#### Default Value:

* ""

#### Example

{% highlight html %}

<<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ name: "Bank",offsetX: 100,offsetY: 100,borderWidth: 2,borderColor: "black",type: "umlclassifier", classifier: ej.datavisualization.Diagram.ClassifierShapes.Interface,
          "interface": {name: "BankAccount",methods: [{ name: "deposit", arguments: [{name:"amount", }],  }]  },}];
$("#DiagramContent").ejDiagram({ nodes:nodes });

</script>

{% endhighlight %}

## nodes.interface.methods.arguments.type `String`
{:#members:nodes-interface.methods.arguments.type}

Sets the type of the argument

#### Default Value:

* ""

#### Example

{% highlight html %}

<<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ name: "Bank",offsetX: 100,offsetY: 100,borderWidth: 2,borderColor: "black",type: "umlclassifier", classifier: ej.datavisualization.Diagram.ClassifierShapes.Interface,
          "interface": {name: "BankAccount",methods: [{ name: "deposit", arguments: [{name:"amount", type:"Dollars"  }],  }]  },}];
$("#DiagramContent").ejDiagram({ nodes:nodes });

</script>

{% endhighlight %}

## nodes.interface.methods.type `String`
{:#members:interface-interface.methods.type}

Sets the return type of the method

#### Default Value:

* ""

#### Example

{% highlight html %}

<<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ name: "Bank",offsetX: 100,offsetY: 100,borderWidth: 2,borderColor: "black",type: "umlclassifier", classifier: ej.datavisualization.Diagram.ClassifierShapes.Interface,
          "interface": {name: "BankAccount",methods: [{ name: "deposit", arguments: [{name:"amount", type:"Dollars"  }],  type:"account"}]  },}];
$("#DiagramContent").ejDiagram({ nodes:nodes });

</script>

{% endhighlight %}

### nodes.interface.methods.scope `String`
{:#members:nodes-interface.attributes.scope}

Sets the visibility of the method

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{ name: "Bank",offsetX: 100,offsetY: 100,borderWidth: 2,borderColor: "black",type: "umlclassifier", classifier: ej.datavisualization.Diagram.ClassifierShapes.Interface,
          "interface": {name: "BankAccount",methods: [{ name: "deposit", arguments: [{name:"amount", type:"Dollars"  }],  type:"account",scope:"private"}]  },}];
$("#DiagramContent").ejDiagram({ nodes:nodes });

</script>

{% endhighlight %}

### nodes.isExpanded `Boolean`
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
$("#diagramcontent").ejDiagram({
      nodes:[node1, node2],
      connectors:[connector],
      layout:{type:"hierarchicaltree"}
});
</script>

{% endhighlight %}

### nodes.isSwimlane `Boolean`
{:#members:nodes-isswimlane}

Sets the node as a swimlane

#### Default Value:

* false

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = {type: "swimlane",name: "swimlane", isSwimlane:true, header: {text: "Swimlane", fontSize: 12, bold: true} };
$("#diagramcontent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.labels `Array`
{:#members:nodes-labels}

A collection of objects where each object represents a label

<ts name="ej.datavisualization.Diagram.NodeLabel"/>

#### Default Value:

* []

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

#### Default Value:

* false

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"label", bold:true}]
      }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.borderColor `String`
{:#members:nodes-labels-bordercolor}

Sets the border color of the label

#### Default Value:

* "transparent"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"label", borderColor:"red", borderWidth: 2}]
      }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.borderWidth `Number`
{:#members:nodes-labels-borderwidth}

Sets the border width of the label

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"label", borderColor:"red", borderWidth: 2}]
      }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.fillColor `String`
{:#members:nodes-labels-fillcolor}

Sets the fill color of the text area

#### Default Value:

* "transparent"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"label", fillColor: "green"}]
      }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.fontColor `String`
{:#members:nodes-labels-fontcolor}

Sets the font color of the text

#### Default Value:

* "black"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"label", fontColor: "green"}]
      }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.fontFamily `String`
{:#members:nodes-labels-fontfamily}

Sets the font family of the text

#### Default Value:

* "Arial"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"label", fontColor: "green", fontFamily:"seugoe UI"}]
      }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.fontSize `Number`
{:#members:nodes-labels-fontsize}

Defines the font size of the text

#### Default Value:

* 12

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"label", fontSize: 14}]
      }];
$("#diagramcontent").ejDiagram({nodes:nodes});

</script>

{% endhighlight %}

### nodes.labels.horizontalAlignment `enum`
{:#members:nodes-labels-horizontalalignment}

<ts name = "ej.datavisualization.Diagram.HorizontalAlignment"/>

Sets the horizontal alignment of the label.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">Left</td>
            <td class="description last">Used to align text horizontally on left side of node/connector</td>
       </tr>
        <tr>
            <td class="name">Center</td>
            <td class="description last">Used to align text horizontally on center of node/connector</td>
       </tr>
        <tr>
            <td class="name">Right</td>
            <td class="description last">Used to align text horizontally on right side of node/connector</td>
       </tr>
     </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.HorizontalAlignment.Center

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
	     //Align the text at the left most position of node
         labels:[{ text:"label", offset:{ x:0 }, horizontalAlignment:ej.datavisualization.Diagram.HorizontalAlignment.Left}]
      }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.italic `Boolean`
{:#members:nodes-labels-italic}

Enables/disables the italic style

#### Default Value:

* false

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"label", italic:true}]
      }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.margin `Object`
{:#members:nodes-labels-margin}

To set the margin of the label

#### Default Value:

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
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.mode `enum`
{:#members:nodes-labels-mode}

<ts name = "ej.datavisualization.Diagram.LabelEditMode"/>

Gets whether the label is currently being edited or not.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">Edit</td>
            <td class="description last">Used to set label edit mode as edit</td>
       </tr>
        <tr>
            <td class="name">View</td>
            <td class="description last">Used to set label edit mode as view</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.LabelEditMode.Edit

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var node = diagram.selectionList[0];
console.log(node.labels[0].mode);
</script>

{% endhighlight %}

### nodes.labels.name `String`
{:#members:nodes-labels-name}

Sets the unique identifier of the label

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"label", name:"label1"}]
      }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.offset `object`
{:#members:nodes-labels-offset}

Sets the fraction/ratio(relative to node) that defines the position of the label

#### Default Value:

* ej.datavisualization.Diagram.Point(0.5, 0.5)

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"label", offset:ej.datavisualization.Diagram.Point(0,0.5) }]
      }];
$("#diagramcontent").ejDiagram({nodes:nodes});

</script>

{% endhighlight %}

### nodes.labels.opacity `Number`
{:#members:nodes-labels-opacity}

Defines the transparency of the labels

#### Default Value:

* 1

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"label", opacity: 0.7}]
      }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.readOnly `Boolean`
{:#members:nodes-labels-readonly}

Defines whether the label is editable or not

#### Default Value:

* false

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"label", readOnly:true}]
      }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.rotateAngle `Number`
{:#members:nodes-labels-rotateangle}

Defines the angle to which the label needs to be rotated

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"label", rotateAngle: 90}]
      }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.text `String`
{:#members:nodes-labels-text}

Defines the label text

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"Label"}]
      }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.textAlign `enum`
{:#members:nodes-labels-textalign}

<ts name = "ej.datavisualization.Diagram.TextAlign"/>
	
Defines how to align the text inside the label.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">Left</td>
            <td class="description last">Used to align text on left side of node/connector</td>
       </tr>
        <tr>
            <td class="name">Center</td>
            <td class="description last">Used to align text on center of node/connector</td>
       </tr>
        <tr>
            <td class="name">Right</td>
            <td class="description last">Used to align text on Right side of node/connector</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.TextAlign.Center

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"node Label", textAlign:ej.datavisualization.Diagram.TextAlign.Left}]
      }];
$("#diagramcontent").ejDiagram({ nodes:nodes });
</script>

{% endhighlight %}

### nodes.labels.textDecoration `enum`
{:#members:nodes-labels-textdecoration}

<ts name = "ej.datavisualization.Diagram.TextDecorations"/>

Sets how to decorate the label text.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">Underline</td>
            <td class="description last">Used to set text decoration of the label as Underline</td>
       </tr>
        <tr>
            <td class="name">Overline</td>
            <td class="description last">Used to set text decoration of the label as Overline</td>
       </tr>
        <tr>
            <td class="name">LineThrough</td>
            <td class="description last">Used to set text decoration of the label as LineThrough</td>
       </tr>
        <tr>
            <td class="name">None</td>
            <td class="description last">Used to set text decoration of the label as None</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.TextDecorations.None

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
	     //Decorate the text with an underline
         labels:[{ text:"Label", textDecoration: ej.datavisualization.Diagram.TextDecorations.Underline}]
      }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.verticalAlignment `enum`
{:#members:nodes-labels-verticalalignment}

<ts name = "ej.datavisualization.Diagram.VerticalAlignment"/>

Sets the vertical alignment of the label.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">Top</td>
            <td class="description last">Set vertical alignment as top</td>
       </tr>
        <tr>
            <td class="name">Middle</td>
            <td class="description last">Set vertical alignment as middle</td>
       </tr>
        <tr>
            <td class="name">Bottom</td>
            <td class="description last">Set vertical alignment as bottom</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.VerticalAlignment.Center

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
	     //Aligns the text at the top most position of node
         labels:[{ text:"label", offset:{ y:0 }, verticalAlignment:ej.datavisualization.Diagram.VerticalAlignment.Top }]
      }];
$("#diagramcontent").ejDiagram({ nodes:nodes });
</script>

{% endhighlight %}

### nodes.labels.visible `Boolean`
{:#members:nodes-labels-visible}

Enables or disables the visibility of the label

#### Default Value:

* true

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"Label", visible: false}]
      }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.width `Number`
{:#members:nodes-labels-width}

Sets the width of the label(the maximum value of label width and the node width will be considered as label width)

#### Default Value:

* 50

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"Label", width: 100}]
      }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.labels.wrapping `enum`
{:#members:nodes-labels-wrapping}

<ts name = "ej.datavisualization.Diagram.TextWrapping"/>

Defines how the label text needs to be wrapped.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">NoWrap</td>
            <td class="description last">Disables wrapping</td>
       </tr>
        <tr>
            <td class="name">Wrap</td>
            <td class="description last">Enables Line-break at normal word break points</td>
       </tr>
        <tr>
            <td class="name">WrapWithOverflow</td>
            <td class="description last">Enables Line-break at normal word break points with longer word overflows</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.TextWrapping.WrapWithOverflow

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
         labels:[{ text:"Enter Your Text", wrapping:ej.datavisualization.Diagram.TextWrapping.NoWrap}]
      }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.lanes `Array`
{:#members:nodes-lanes}

An array of objects where each object represents a lane. Applicable, if the node is a swimlane.

#### Default Value:

* []

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = { type: "swimlane",name: "swimlane", offsetX:300, offsetY:200,
//Define the collection of lanes
				 lanes:[{name:"lane1", width:200 },
				 {name:"lane2", width:100}] };
$("#diagramcontent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.lanes.addInfo `Object`
{:#members:nodes-lanes-addinfo}

Allows to maintain additional information about lane

#### Default Value:

* {}

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var addInfo = { Description:"Describe the functionality" };
var swimlane = {type: "swimlane",name: "swimlane", offsetX:300, offsetY:200,
lanes:[{ name:"lane1", width:200, addInfo: addInfo }] };
$("#diagramcontent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.lanes.children `Array`
{:#members:nodes-lanes-children}

An array of objects where each object represents a child node of the lane

#### Default Value:

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
$("#diagramcontent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.lanes.fillColor `String`
{:#members:nodes-lanes-fillcolor}

Defines the fill color of the lane

#### Default Value:

* "white"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = {type: "swimlane",name: "swimlane", offsetX:300, offsetY:100,
lanes:[{name:"lane1", width:200 ,fillColor:"lightgray" }]}
$("#diagramcontent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.lanes.header `Object`
{:#members:nodes-lanes-header}

Defines the header of the lane

#### Default Value:

* { text: "Function", fontSize: 11 }

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = {type: "swimlane",name: "swimlane", offsetX:300, offsetY:100,
lanes:[{name:"lane1", width:200, 
	//Defines the lane header
	header:{fillColor:"blue", fontColor:"white", text:"Functon 1"} }]}
$("#diagramcontent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.lanes.isLane `Boolean`
{:#members:nodes-lanes-islane}

Defines the object as a lane

#### Default Value:

* false

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = {type: "swimlane",name: "swimlane", offsetX:300, offsetY:200,
lanes:[{name:"lane1", width:200 , isLane:true }]}
$("#diagramcontent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.lanes.name `String`
{:#members:nodes-lanes-name}

Sets the unique identifier of the lane

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = {type: "swimlane",name: "swimlane", offsetX:300, offsetY:100,
lanes:[{ name:"function1", width:200 }]}
$("#diagramcontent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.lanes.orientation `String`
{:#members:nodes-lanes-orientation}

Sets the orientation of the lane. 

#### Default Value:

* "vertical"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = { type: "swimlane",name: "swimlane", offsetX:300, offsetY:100, orientation:"horizontal",
lanes:[{ name:"function1", width:200 , orientation:"vertical" }]}
$("#diagramcontent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.marginBottom `Number`
{:#members:nodes-marginbottom}

Defines the minimum space to be left between the bottom of parent bounds and the node. Applicable, if the parent is a container.

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = {type: "swimlane",name: "swimlane", offsetX:300, offsetY:200,
lanes:[{name:"lane1", width:200 , 
      children:[{name:"process1", width: 50, height: 50, marginBottom: 50 }]
 }]}
$("#diagramcontent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.marginLeft `Number`
{:#members:nodes-marginleft}

Defines the minimum space to be left between the left of parent bounds and the node. Applicable, if the parent is a container.

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = {type: "swimlane",name: "swimlane", offsetX:300, offsetY:200,
lanes:[{name:"lane1", width:200 , 
      children:[{name:"process1", width: 50, height: 50, marginLeft: 10 }]
 }]}
$("#diagramcontent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.marginRight `Number`
{:#members:nodes-marginright}

Defines the minimum space to be left between the right of the parent bounds and the node. Applicable, if the parent is a container.

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = {type: "swimlane",name: "swimlane", offsetX:300, offsetY:200,
lanes:[{name:"lane1", width:200 , 
      children:[{name:"process1", width: 50, height: 50, marginRight: 10 }]
 }]}
$("#diagramcontent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.marginTop `Number`
{:#members:nodes-margintop}

Defines the minimum space to be left between the top of parent bounds and the node. Applicable, if the parent is a container.

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = {type: "swimlane",name: "swimlane", offsetX:300, offsetY:200,
lanes:[{name:"lane1", width:200 , 
      children:[{name:"process1", width: 50, height: 50, marginTop: 10 }]
 }]}
$("#diagramcontent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.maxHeight `Number`
{:#members:nodes-maxheight}

Defines the maximum height limit of the node

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, maxHeight: 100}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.maxWidth `Number`
{:#members:nodes-maxwidth}

Defines the maximum width limit of the node

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, maxWidth: 100}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.minHeight `Number`
{:#members:nodes-minheight}

Defines the minimum height limit of the node

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, minHeight: 10 }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.minWidth `Number`
{:#members:nodes-minwidth}

Defines the minimum width limit of the node

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, minWidth: 10 }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.name `String`
{:#members:nodes-name}

Sets the unique identifier of the node

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50 }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.offsetX `Number`
{:#members:nodes-offsetx}

Defines the position of the node on X-Axis

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50 }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.offsetY `Number`
{:#members:nodes-offsety}

Defines the position of the node on Y-Axis

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50 }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.opacity `Number`
{:#members:nodes-opacity}

Defines the opaque of the node

#### Default Value:

* 1

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, opacity:0.7 }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.orientation `String`
{:#members:nodes-orientation}

Defines the orientation of nodes. Applicable, if the node is a swimlane.

#### Default Value:

* "vertical"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = { type: "swimlane",name: "swimlane", offsetX:300, offsetY:100, orientation:"horizontal" };
$("#diagramcontent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.outEdges `Array`
{:#members:nodes-outedges}

A read only collection of outgoing connectors/edges of the node

#### Default Value:

* []

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
//Read the outgoing connectors of the selected node
var node = diagram.selectionList[0];
for(var i = 0; i<node.outEdges.length; i++){
    console.log(node.outEdges[i]);
}
</script>

{% endhighlight %}

### nodes.paddingBottom `Number`
{:#members:nodes-paddingbottom}

Defines the minimum padding value to be left between the bottom most position of a group and its children. Applicable, if the group is a container.

#### Default Value:

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
$("#diagramcontent").ejDiagram({nodes:[group]});
</script>

{% endhighlight %}

### nodes.paddingLeft `Number`
{:#members:nodes-paddingleft}

Defines the minimum padding value to be left between the left most position of a group and its children. Applicable, if the group is a container.

#### Default Value:

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
$("#diagramcontent").ejDiagram({nodes:[group]});
</script>

{% endhighlight %}

### nodes.paddingRight `Number`
{:#members:nodes-paddingright}

Defines the minimum padding value to be left between the right most position of a group and its children. Applicable, if the group is a container.

#### Default Value:

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
$("#diagramcontent").ejDiagram({nodes:[group]});
</script>

{% endhighlight %}

### nodes.paddingTop `Number`
{:#members:nodes-paddingtop}

Defines the minimum padding value to be left between the top most position of a group and its children. Applicable, if the group is a container.

#### Default Value:

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
$("#diagramcontent").ejDiagram({nodes:[group]});
</script>

{% endhighlight %}

### nodes.paletteItem `Object`
{:#members:nodes-paletteitem}

Defines the size and preview size of the node to add that to symbol palette

#### Default Value:

* null

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
	
$("#symbolpalette").ejSymbolPalette({
	//Defines the palette collection 
	palettes: [{
		name: "Basic Shapes", expanded: true,
		items: [
		{
			name: "Rectangle", height: 40, width: 80,
			//Sets preview size
			paletteItem: {			
                previewWidth: 100,
				previewHeight: 100
			}
		}]
	}]
});

</script>

{% endhighlight %}

### nodes.paletteItem.enableScale `Boolean`
{:#members:nodes-paletteitem-enablescale}

Defines whether the symbol should be drawn at its actual size regardless of precedence factors or not

#### Default Value:

* true

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({
	//Defines the palette collection 
	palettes: [{
		name: "Nodes", expanded: true,
		items: [
		{
			name: "Rectangle", width:50, height:50,
			//Draw symbol of size(50,50)
			paletteItem: {
                width: 100,
                height: 100,
                enableScale:false
			}
		}]
	}]
});
</script>

{% endhighlight %}

### nodes.paletteItem.height `Number`
{:#members:nodes-paletteitem-height}

Defines the height of the symbol

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#symbolpalette").ejSymbolPalette({
	//Defines the palette collection 
	palettes: [{
		name: "Nodes", expanded: true,
		items: [
		{
			name: "Rectangle", 
			//Sets the size of the symbol
			paletteItem: {
                width: 200,
                height: 200,
				enableScale: false
			}
		}]
	}]
});
</script>

{% endhighlight %}

### nodes.paletteItem.margin `Object`
{:#members:nodes-paletteitem-margin}

Defines the margin of the symbol item

#### Default Value:

* { left: 4, right: 4, top: 4, bottom: 4 }

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({
	//Defines the palette collection 
	palettes: [{
		name: "Nodes", expanded: true,
		items: [
		{
			name: "Rectangle", width:50, height:50,
			//Sets symbol margin
			paletteItem: {
                margin: { left: 30 }
			}
		}]
	}]
});
</script>

{% endhighlight %}

### nodes.paletteItem.previewHeight `Number`
{:#members:nodes-paletteitem-previewheight}

Defines the preview height of the symbol

#### Default Value:

* undefined

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
	$("#symbolpalette").ejSymbolPalette({
	//Defines the palette collection 
	palettes: [{
		name: "Nodes", expanded: true,
		items: [
		{
			name: "Rectangle", width:50, height:50,
			//Sets preview size
			paletteItem: {
                previewWidth: 100,
				previewHeight: 100
			}
		}]
	}]
});
</script>

{% endhighlight %}

### nodes.paletteItem.previewWidth `Number`
{:#members:nodes-paletteitem-previewwidth}

Defines the preview width of the symbol

#### Default Value:

* undefined

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({
	//Defines the palette collection 
	palettes: [{
		name: "Nodes", expanded: true,
		items: [
		{
			name: "Rectangle", width:50, height:50,
			//Sets preview size
			paletteItem: {
                previewWidth: 100,
				previewHeight: 100
			}
		}]
	}]
});
</script>

{% endhighlight %}

### nodes.paletteItem.width `Number`
{:#members:nodes-paletteitem-width}

Defines the width of the symbol 

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="symbolpalette"></div>
<script>
$("#symbolpalette").ejSymbolPalette({
	//Defines the palette collection 
	palettes: [{
		name: "Nodes", expanded: true,
		items: [
		{
			name: "Rectangle", width:50, height:50,
			//Sets the size of the symbol
			paletteItem: {
                width: 200,
                height: 200,
                enableScale : false
			}
		}]
	}]
});
</script>

{% endhighlight %}

### nodes.parent `String`
{:#members:nodes-parent}

Sets the name of the parent group

#### Default Value:

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
$("#diagramcontent").ejDiagram({nodes:[node1, node2, group]});
</script>

{% endhighlight %}

### nodes.pathData `String`
{:#members:nodes-pathdata}

Sets the path geometry that defines the shape of a path node

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
      type:"basic", shape:"path", pathData: "M370.9702,194.9961L359.5112,159.7291L389.5112,137.9341L419.5112,159.7291L408.0522,194.9961L370.9702,194.9961z" }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.phases `Array`
{:#members:nodes-phases}

An array of objects, where each object represents a smaller region(phase) of a swimlane.

#### Default Value:

* []

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = { type: "swimlane",name: "swimlane", offsetX:300, offsetY:100, 
width: 300, orientation:"horizontal",
phases:[{ name:"phase1", offset:150, label:{text:"Phase1"}},    
       { name:"phase2", label:{ text:"Phase2"} }]};
$("#diagramcontent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.phases.label `Object`
{:#members:nodes-phases-label}

Defines the header of the smaller regions

#### Default Value:

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = { type: "swimlane",name: "swimlane", offsetX:300, offsetY:100, 
width: 300, orientation:"horizontal",
phases:[{ name:"phase1", offset:150, label:{text:"Phase1"}},    
       { name:"phase2", label:{ text:"Phase2"} }]};
$("#diagramcontent").ejDiagram({nodes:[swimlane]});

</script>

{% endhighlight %}

### nodes.phases.lineColor `String`
{:#members:nodes-phases-linecolor}

Defines the line color of the splitter that splits adjacent phases.

#### Default Value:

* "#606060"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = { type: "swimlane",name: "swimlane", offsetX:300, offsetY:100, 
width: 300, orientation:"horizontal",
phases:[{ name:"phase1", offset:150, label:{text:"Phase1"}, lineColor:"green"},    
       { name:"phase2", label:{ text:"Phase2"} }]};
$("#diagramcontent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.phases.lineDashArray `String`
{:#members:nodes-phases-linedasharray}

Sets the dash array that used to stroke the phase splitter

#### Default Value:

* "3,3"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = { type: "swimlane",name: "swimlane", offsetX:300, offsetY:100, 
width: 300, orientation:"horizontal",
phases:[{ name:"phase1", offset:150, label:{text:"Phase1"}, lineDashArray:"2,2"},    
       { name:"phase2", label:{ text:"Phase2"} }]};
$("#diagramcontent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.phases.lineWidth `Number`
{:#members:nodes-phases-linewidth}

Sets the lineWidth of the phase

#### Default Value:

* 1

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = { type: "swimlane",name: "swimlane", offsetX:300, offsetY:100, 
width: 300, orientation:"horizontal",
phases:[{ name:"phase1", offset:150, label:{text:"Phase1"}, lineWidth:3 },    
       { name:"phase2", label:{ text:"Phase2"} }]};
$("#diagramcontent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.phases.name `String`
{:#members:nodes-phases-name}

Sets the unique identifier of the phase

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = { type: "swimlane",name: "swimlane", offsetX:300, offsetY:100, 
width: 300, orientation:"horizontal",
phases:[{ name:"phase1", label:{text:"Phase1"}, lineWidth:3 } ]};
$("#diagramcontent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.phases.offset `Number`
{:#members:nodes-phases-offset}

Sets the length of the smaller region(phase) of a swimlane

#### Default Value:

* 100

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", phases:[{offset: 200}]}});
</script>

{% endhighlight %}

### nodes.phases.orientation `String`
{:#members:nodes-phases-orientation}

Sets the orientation of the phase

#### Default Value:

* "horizontal"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram = $("#diagramcontent").ejDiagram("instance");
diagram.addPhase(diagram.selectionList[0].name, 
	{ 
		name: "verticalPhase", 
	    type: "phase", offset: 200, orientation: "vertical", 
		label: { text: "New Phase" } 
	} );
</script>

{% endhighlight %}

### nodes.phases.type `String`
{:#members:nodes-phases-type}

Sets the type of the object as phase

#### Default Value:

* "phase"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram = $("#diagramcontent").ejDiagram("instance");
diagram.addPhase(diagram.selectionList[0].name, 
	{ 
		name: "verticalPhase", 
		type: "phase", offset: 200, label: { text: "New Phase" } 
	});	
</script>

{% endhighlight %}

### nodes.phaseSize `Number`
{:#members:nodes-phasesize}

Sets the height of the phase headers

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var swimlane = { type: "swimlane",name: "swimlane", offsetX:300, offsetY:100, 
width: 300, orientation:"horizontal",phaseSize:50,
phases:[{ name:"phase1", offset:150, label:{text:"Phase 1"} }] };
$("#diagramcontent").ejDiagram({nodes:[swimlane]});
</script>

{% endhighlight %}

### nodes.pivot `object`
{:#members:nodes-pivot}

Sets the ratio/ fractional value relative to node, based on which the node will be transformed(positioning, scaling and rotation) 

#### Default Value:

* ej.datavisualization.Diagram.Points(0.5,0.5)

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
//The node will be transformed with respect to its top left corner
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, pivot: {x:0, y:0}}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.points `Array`
{:#members:nodes-points}

Defines a collection of points to draw a polygon. Applicable, if the shape is a polygon.

#### Default Value:

* []

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50,
type: "basic",shape:"polygon", points:[{ x: 0, y: 12.5 }, { x: 0, y: 50 }, { x: 50, y: 50 }, { x: 50, y: 0 }, { x: 12.5, y: 0 }, { x: 0, y: 12.5 }]}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.ports `Array`
{:#members:nodes-ports}

An array of objects where each object represents a port

#### Default Value:

* []

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50,
      ports:[{name:"port1", offset:{ x:0.5, y:0 }}, 
            {name:"port2", offset:{ x:0.5, y:1 }}]}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.ports.borderColor `String`
{:#members:nodes-ports-bordercolor}

Sets the border color of the port

#### Default Value:

* "#1a1a1a"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50,
      ports:[{name:"port1", offset:{ x:0.5, y:0.5 }, borderColor:"yellow" }] }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.ports.borderWidth `Number`
{:#members:nodes-ports-borderwidth}

Sets the stroke width of the port

#### Default Value:

* 1

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50,
      ports:[{name:"port1", offset:{ x:0.5, y:0.5 }, borderColor:"yellow", borderWidth: 3 }] }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.ports.connectorPadding `Number`
{:#members:nodes-ports-connectorpadding}

Defines the space to be left between the port bounds and its incoming and outgoing connections.

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50,
      ports:[{name:"port1", offset:{ x:0.5, y:0.5 }, connectorPadding:10 }] }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.ports.constraints `enum`
{:#members:nodes-ports-constraints}

<ts name = "ej.datavisualization.Diagram.PortConstraints"/>
	
Defines whether connections can be created with the port

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">None</td>
            <td class="description last">Disable all constraints</td>
       </tr>
        <tr>
            <td class="name">Connect</td>
            <td class="description last">Enables connections with connector</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.PortConstraints.Connect

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var PortConstraints = ej.datavisualization.Diagram.PortConstraints;
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50,
	  //Disable creating connections with the port
      ports:[{name:"port1", offset:{ x:0.5, y:0.5 }, constraints: PortConstraints.Default &~ PortConstraints.Connect }] }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.ports.fillColor `String`
{:#members:nodes-ports-fillcolor}

Sets the fill color of the port

#### Default Value:

* "white"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50,
      ports:[{name:"port1", offset:{ x:0.5, y:0.5 }, fillColor:"red" }] }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.ports.name `String`
{:#members:nodes-ports-name}

Sets the unique identifier of the port

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50,
      ports:[{ name:"port1", offset:{ x:0.5, y:0.5 } }] }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.ports.offset `object`
{:#members:nodes-ports-offset}

Defines the position of the port as fraction/ ratio relative to node

#### Default Value:

* ej.datavisualization.Diagram.Point(0, 0)

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50,
	  //Add port at the center of the node
      ports:[{name:"port1", offset:{ x:0.5, y:0.5 } }] }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.ports.pathData `String`
{:#members:nodes-ports-pathdata}

Defines the path data to draw the port. Applicable, if the port `shape` is path.

#### Default Value:

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
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.ports.shape `enum`
{:#members:nodes-ports-shape}

<ts name = "ej.datavisualization.Diagram.PortShapes"/>
	
Defines the shape of the port.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">X</td>
            <td class="description last">Used to set port shape as X</td>
       </tr>
        <tr>
            <td class="name">Circle</td>
            <td class="description last">Used to set port shape as Circle</td>
       </tr>
        <tr>
            <td class="name">Square</td>
            <td class="description last">Used to set port shape as Square</td>
       </tr>
        <tr>
            <td class="name">Path</td>
            <td class="description last">Used to set port shape as Path</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.PortShapes.Square

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50,
      ports:[{name:"port1", offset:{ x:0.5, y:0.5 }, 
      shape:ej.datavisualization.Diagram.PortShapes.Circle}] }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.ports.size `Number`
{:#members:nodes-ports-size}

Defines the size of the port

#### Default Value:

* 8

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50,
      ports:[{name:"port1", offset:{ x:0.5, y:0.5 }, size: 10}] }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.ports.visibility `enum`
{:#members:nodes-ports-visibility}

<ts name = "ej.datavisualization.Diagram.PortVisibility"/>

Defines when the port should be visible.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">Visible</td>
            <td class="description last">Set the port visibility as Visible</td>
       </tr>
        <tr>
            <td class="name">Hidden</td>
            <td class="description last">Set the port visibility as Hidden</td>
       </tr>
        <tr>
            <td class="name">Hover</td>
            <td class="description last">Port get visible when hover connector on node</td>
       </tr>
        <tr>
            <td class="name">Connect</td>
            <td class="description last">Port gets visible when connect connector to node</td>
       </tr>
        <tr>
            <td class="name">Default</td>
            <td class="description last">Specifies the port visibility as default</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.PortVisibility.Default

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50,
      ports:[{name:"port1", offset:{ x:0.5, y:0.5 }, 
      visibility:ej.datavisualization.Diagram.PortVisibility.Visible }] }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.rotateAngle `Number`
{:#members:nodes-rotateangle}

Sets the angle to which the node should be rotated

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, rotateAngle: 45 }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.scale `enum`
{:# members:nodes-scale}

<ts name = "ej.datavisualization.Diagram.ScaleConstraints "/>
    
Defines how the node should be scaled/stretched

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">None</td>
            <td class="description last">Set the scale as none</td>
       </tr>
        <tr>
            <td class="name">Meet</td>
            <td class="description last">Used to scale the node uniformly so that it fits the node bounds</td>
       </tr>
        <tr>
            <td class="name">Slice</td>
            <td class="description last">Used to scale the node uniformly to the maximum</td>
       </tr>
        <tr>
            <td class="name">Stretch</td>
            <td class="description last">Used to scale the node non-uniformly to be stretched</td>
       </tr>
    </tbody>
</table>
 
#### Default Value:

* ej.datavisualization.Diagram.ScaleConstraints.Meet

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({ node:{scale:ej.datavisualization.Diagram.ScaleConstraints.Slice }});
</script>

{% endhighlight %}

### nodes.shadow `Object`
{:#members:nodes-shadow}

Defines the opacity and the position of shadow

#### Default Value:

* ej.datavisualization.Diagram.Shadow()

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var NodeConstraints = ej.datavisualization.Diagram.NodeConstraints;
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50,
      constraints: NodeConstraints.Default | NodeConstraints.Shadow,
      shadow: {opacity: 0.5, distance: 10, angle: 45} }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.shadow.angle `Number`
{:#members:nodes-shadow-angle}

Defines the angle of the shadow relative to node

#### Default Value:

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
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.shadow.distance `Number`
{:#members:nodes-shadow-distance}

Sets the distance to move the shadow relative to node

#### Default Value:

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
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.shadow.opacity `Number`
{:#members:nodes-shadow-opacity}

Defines the opaque of the shadow

#### Default Value:

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
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.shape `enum`
{:#members:nodes-shape}

<ts name = "ej.datavisualization.Diagram.BasicShapes"/>

Sets the shape of the node. It depends upon the type of node.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">Rectangle</td>
            <td class="description last">Used to specify node Shape as Rectangle</td>
       </tr>
        <tr>
            <td class="name">Ellipse</td>
            <td class="description last">Used to specify node Shape as Ellipse</td>
       </tr>
        <tr>
            <td class="name">Path</td>
            <td class="description last">Used to specify node Shape as Path</td>
       </tr>
        <tr>
            <td class="name">Polygon</td>
            <td class="description last">Used to specify node Shape as Polygon</td>
       </tr>
        <tr>
            <td class="name">Triangle</td>
            <td class="description last">Used to specify node Shape as Triangle</td>
       </tr>
        <tr>
            <td class="name">Plus</td>
            <td class="description last">Used to specify node Shape as Plus</td>
       </tr>
        <tr>
            <td class="name">Star</td>
            <td class="description last">Used to specify node Shape as Star</td>
       </tr>
        <tr>
            <td class="name">Pentagon</td>
            <td class="description last">Used to specify node Shape as Pentagon</td>
       </tr>
        <tr>
            <td class="name">Heptagon</td>
            <td class="description last">Used to specify node Shape as Heptagon</td>
       </tr>
        <tr>
            <td class="name">Octagon</td>
            <td class="description last">Used to specify node Shape as Octagon</td>
       </tr>
        <tr>
            <td class="name">Trapezoid</td>
            <td class="description last">Used to specify node Shape as Trapezoid</td>
       </tr>
        <tr>
            <td class="name">Decagon</td>
            <td class="description last">Used to specify node Shape as Decagon</td>
       </tr>
        <tr>
            <td class="name">RightTriangle</td>
            <td class="description last">Used to specify node Shape as RightTriangle</td>
       </tr>
        <tr>
            <td class="name">Cylinder</td>
            <td class="description last">Used to specify node Shape as Cylinder</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.BasicShapes.Rectangle

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
	  // Sets the shape as ellipse
      type:"basic", shape:ej.datavisualization.Diagram.BasicShapes.Ellipse }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.source `String`
{:#members:nodes-source}

Sets the source path of the image. Applicable, if the type of the node is image.

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 50, height:50, offsetX:50, offsetY:50, 
type:"image", source: "Clayton.png" }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.subProcess `Object`
{:#members:nodes-subprocess}

Defines the sub process of a BPMN Activity. Applicable, if the type of the BPMN activity is sub process.

#### Default Value:

* ej.datavisualization.Diagram.BPMNSubProcess()

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
		type:"bpmn", shape:"activity", activity:"subprocess", 
		subProcess:{ loop: ej.datavisualization.Diagram.BPMNLoops.Standard } }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.subProcess.adhoc `Boolean`
{:#members:nodes-subprocess-adhoc}

Defines whether the BPMN sub process is without any prescribed order or not

#### Default Value:

* false

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
type:"bpmn", shape:"activity", activity:"subprocess", 
subProcess:{ adhoc: true } }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.subProcess.boundary `enum`
{:#members:nodes-subprocess-boundary}

<ts name = "ej.datavisualization.Diagram.BPMNBoundary"/>

Sets the boundary of the BPMN process

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">Default</td>
            <td class="description last">Used to set BPMN SubProcess's Boundary as Default</td>
       </tr>
        <tr>
            <td class="name">Call</td>
            <td class="description last">Used to set BPMN SubProcess's Boundary as Call</td>
       </tr>
        <tr>
            <td class="name">Event</td>
            <td class="description last">Used to set BPMN SubProcess's Boundary as Event</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.BPMNBoundary.Default

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
		type:"bpmn", shape:"activity", activity:"subprocess", 
		subProcess:{ boundary: ej.datavisualization.Diagram.BPMNBoundary.Call } }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.subProcess.compensation `Boolean`
{:#members:nodes-subprocess-compensation}

Sets whether the BPMN subprocess is triggered as a compensation of a specific activity

#### Default Value:

* false

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
		type:"bpmn", shape:"activity", activity:"subprocess", 
		subProcess:{ compensation: true } }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.subProcess.collapsed `Boolean`
{:#members:nodes-subprocess-collapsed}

Sets whether the BPMN subprocess is triggered as a collapsed of a specific activity

#### Default Value:

* true

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
		type:"bpmn", shape:"activity", activity:"subprocess", 
		subProcess:{ collapsed: false } }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.subProcess.event `enum`
{:#members:nodes-subprocess-event}

<ts ref = "ej.datavisualization.Diagram.BPMNEvents"/>

Sets the type of the event by which the sub-process will be triggered

#### Default Value:

* ej.datavisualization.Diagram.BPMNEvents.Start

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
		type:"bpmn", shape:"activity", activity:"subprocess", 
        subProcess: { type: "event", event: "start" }
         }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.subProcess.events `array`
{:#members:nodes-subprocess-events}

Defines the collection of events that need to be appended with BPMN Sub-Process

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes = [{name: "node1", width: 100, height: 100, offsetX: 50, offsetY: 50,
    type: "bpmn", shape: "activity", activity: "subprocess",
    subProcess: {
        type: "transaction",
        events: [
            { event: "intermediate", offset: { x: 0.25, y: 1 } },
            { event: "intermediate", trigger: "error", offset: { x: 0.75, y: 1 } }]}
            }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.subProcess.loop `enum`
{:#members:nodes-subprocess-loop}

<ts name = "ej.datavisualization.Diagram.BPMNLoops"/>

Defines the loop type of a sub process.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">None</td>
            <td class="description last">Used to set BPMN Activity's Loop as None</td>
       </tr>
        <tr>
            <td class="name">Standard</td>
            <td class="description last">Used to set BPMN Activity's Loop as Standard</td>
       </tr>
        <tr>
            <td class="name">ParallelMultiInstance</td>
            <td class="description last">Used to set BPMN Activity's Loop as ParallelMultiInstance</td>
       </tr>
        <tr>
            <td class="name">SequenceMultiInstance</td>
            <td class="description last">Used to set BPMN Activity's Loop as SequenceMultiInstance</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.BPMNLoops.None

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
type:"bpmn", shape:"activity", activity:"subprocess", 
subProcess:{ loop: ej.datavisualization.Diagram.BPMNLoops.ParallelMultiInstance} }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.subProcess.trigger `enum`
{:#members:nodes-subprocess-trigger}

<ts ref = "ej.datavisualization.Diagram.BPMNTriggers"/>

Defines the type of the event trigger

#### Default Value:

* ej.datavisualization.Diagram.BPMNTriggers.Message

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
		type:"bpmn", shape:"activity", activity:"subprocess", 
            subProcess: { type: "event",  trigger: "conditional", offset: { x: 0.75, y: 1 } }
            }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}


### nodes.subProcess.type `enum`
{:#members:nodes-subprocess-type}

<ts name = "ej.datavisualization.Diagram.BPMNSubProcessTypes"/>

Defines the type of a sub process

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">None</td>
            <td class="description last">Used to set BPMN SubProcess type as None</td>
       </tr>
        <tr>
            <td class="name">Transaction</td>
            <td class="description last">Used to set BPMN SubProcess type as Transaction</td>
       </tr>
        <tr>
            <td class="name">Event</td>
            <td class="description last">Used to set BPMN SubProcess type as Event</td>
       </tr>
     </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.BPMNSubProcessTypes.None

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
 var nodes;
        nodes = [{
            name: "node1", width: 100, height: 100, offsetX: 50, offsetY: 50,
            type: "bpmn", shape: "activity", activity: "subprocess",
            subProcess: { type: event }
        }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.task `Object`
{:#members:nodes-task}

Defines the task of the BPMN activity. Applicable, if the type of activity is set as task.

#### Default Value:

* ej.datavisualization.Diagram.BPMNTask()

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
		type:"bpmn", shape:"activity", activity:"task", 
		task:{ compensation: true } }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.task.call `Boolean`
{:#members:nodes-tasks-call}

To set whether the task is a global task or not

#### Default Value:

* false

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
		type:"bpmn", shape:"activity", activity:"task", 
		task:{ call: true } }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.task.compensation `Boolean`
{:#members:nodes-tasks-compensation}

Sets whether the task is triggered as a compensation of another specific activity

#### Default Value:

* false

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
		type:"bpmn", shape:"activity", activity:"task", 
		task:{ compensation: true } }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.task.loop `enum`
{:#members:nodes-tasks-loop}

<ts name = "ej.datavisualization.Diagram.BPMNLoops"/>

Sets the loop type of a BPMN task.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">X</td>
            <td class="description last">Used to set port shape as X</td>
       </tr>
        <tr>
            <td class="name">Circle</td>
            <td class="description last">Used to set port shape as Circle</td>
       </tr>
        <tr>
            <td class="name">Square</td>
            <td class="description last">Used to set port shape as Square</td>
       </tr>
        <tr>
            <td class="name">Path</td>
            <td class="description last">Used to set port shape as Path</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.BPMNLoops.None

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
		type:"bpmn", shape:"activity", activity:"task", 
		task:{ loop: ej.datavisualization.Diagram.BPMNLoops.Standard } }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.task.type `enum`
{:#members:nodes-tasks-type}

<ts name = "ej.datavisualization.Diagram.BPMNTasks"/>

Sets the type of the BPMN task.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">None</td>
            <td class="description last">Used to set BPMN Task Type as None</td>
       </tr>
        <tr>
            <td class="name">Service</td>
            <td class="description last">Used to set BPMN Task Type as Service</td>
       </tr>
        <tr>
            <td class="name">Receive</td>
            <td class="description last">Used to set BPMN Task Type as Receive</td>
       </tr>
        <tr>
            <td class="name">Send</td>
            <td class="description last">Used to set BPMN Task Type as Send</td>
       </tr>
        <tr>
            <td class="name">InstantiatingReceive</td>
            <td class="description last">Used to set BPMN Task Type as InstantiatingReceive</td>
       </tr>
        <tr>
            <td class="name">Manual</td>
            <td class="description last">Used to set BPMN Task Type as Manual</td>
       </tr>
        <tr>
            <td class="name">BusinessRule</td>
            <td class="description last">Used to set BPMN Task Type as BusinessRule</td>
       </tr>
        <tr>
            <td class="name">User</td>
            <td class="description last">Used to set BPMN Task Type as User</td>
       </tr>
        <tr>
            <td class="name">Script</td>
            <td class="description last">Used to set BPMN Task Type as Script</td>
       </tr>
        <tr>
            <td class="name">Parallel</td>
            <td class="description last">Used to set BPMN Task Type as Parallel</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.BPMNTasks.None

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
		type:"bpmn", shape:"activity", activity:"task", 
		task:{ type: ej.datavisualization.Diagram.BPMNTasks.Service } }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.templateId `String`
{:#members:nodes-templateid}

Sets the id of svg/html templates. Applicable, if the node is HTML or native.

#### Default Value:

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
$("#diagramcontent").ejDiagram({nodes:nodes});

</script>

{% endhighlight %}

### nodes.textBlock `Object`
{:#members:nodes-textblock}

Defines the textBlock of a text node

#### Default Value:

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
		type:"text", textBlock:{ text: "Text Node", fontColor:"red" } }];
$("#diagramcontent").ejDiagram({nodes:nodes});

</script>

{% endhighlight %}

### nodes.tooltip `Object`
{:#members:nodes-tooltip}

Defines the tooltip that should be shown when the mouse hovers over node. For tooltip properties, refer [Tooltip](#members:tooltip)

#### Default Value:

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>

<script type="text/x-jsrender" id="mouseovertooltip">
   <div style="background-color: #F08080; color: white; white-space: nowrap; height: 20px">
        <span style="padding: 5px;"> {{:name}} </span>
   </div>
</script>

<script>
var tooltip = {
		templateId: "mouseovertooltip",
		alignment: {
			horizontal: "center",
			vertical: "bottom"
		}
	};
var NodeConstraints = ej.datavisualization.Diagram.NodeConstraints;
$("#diagramcontent").ejDiagram({	
//Defines nodes
	nodes: [{
		name:"Rectangle", width:50, height: 50, offsetX: 100, offsetY: 100,
        constraints: NodeConstraints.Default & ~NodeConstraints.InheritTooltip, 
        tooltip:tooltip
	}]
});
</script>

{% endhighlight %}

### nodes.trigger `enum`
{:#members:nodes-trigger}

<ts name = "ej.datavisualization.Diagram.BPMNTriggers"/>

Sets the type of BPMN Event Triggers.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">None</td>
            <td class="description last">Used to set Event Trigger as None</td>
       </tr>
        <tr>
            <td class="name">Message</td>
            <td class="description last">Used to set Event Trigger as Message</td>
       </tr>
        <tr>
            <td class="name">Timer</td>
            <td class="description last">Used to set Event Trigger as Timer</td>
       </tr>
        <tr>
            <td class="name">Escalation</td>
            <td class="description last">Used to set Event Trigger as Escalation</td>
       </tr>
        <tr>
            <td class="name">Link</td>
            <td class="description last">Used to set Event Trigger as Link</td>
       </tr>
        <tr>
            <td class="name">Error</td>
            <td class="description last">Used to set Event Trigger as Error</td>
       </tr>
        <tr>
            <td class="name">Compensation</td>
            <td class="description last">Used to set Event Trigger as Compensation</td>
       </tr>
        <tr>
            <td class="name">Signal</td>
            <td class="description last">Used to set Event Trigger as Signal</td>
       </tr>
        <tr>
            <td class="name">Multiple</td>
            <td class="description last">Used to set Event Trigger as Multiple</td>
       </tr>
        <tr>
            <td class="name">Parallel</td>
            <td class="description last">Used to set Event Trigger as Parallel</td>
       </tr>
        <tr>
            <td class="name">Conditional</td>
            <td class="description last">Used to set Event Trigger as Conditional</td>
       </tr>
        <tr>
            <td class="name">Termination</td>
            <td class="description last">Used to set Event Trigger as Termination</td>
       </tr>
       <tr>
            <td class="name">Cancel</td>
            <td class="description last">Used to set Event Trigger as Cancel</td>
       </tr>
   </tbody>
</table>

#### Default Value:

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

<ts name = "ej.datavisualization.Diagram.Shapes"/>

Defines the type of the node.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">None</td>
            <td class="description last">Used to set decorator shape as none</td>
       </tr>
        <tr>
            <td class="name">Arrow</td>
            <td class="description last">Used to set decorator shape as Arrow</td>
       </tr>
        <tr>
            <td class="name">OpenArrow</td>
            <td class="description last">Used to set decorator shape as Open Arrow</td>
       </tr>
        <tr>
            <td class="name">Circle</td>
            <td class="description last">Used to set decorator shape as Circle</td>
       </tr>
        <tr>
            <td class="name">Diamond</td>
            <td class="description last">Used to set decorator shape as Diamond</td>
       </tr>
        <tr>
            <td class="name">Path</td>
            <td class="description last">Used to set decorator shape as path</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.Shapes.Basic

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, 
		type: ej.datavisualization.Diagram.Shapes.BPMN }];
$("#diagramcontent").ejDiagram({nodes:nodes})
</script>

{% endhighlight %}

### nodes.verticalAlign `enum`
{:#members:nodes-verticalalign}

<ts name = "ej.datavisualization.Diagram.VerticalAlignment"/>

Sets the vertical alignment of a node. Applicable, if the parent of a node is a container.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">Top</td>
            <td class="description last">Set vertical alignment as top</td>
       </tr>
        <tr>
            <td class="name">Middle</td>
            <td class="description last">Set vertical alignment as middle</td>
       </tr>
        <tr>
            <td class="name">Bottom</td>
            <td class="description last">Set vertical alignment as bottom</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.VerticalAlignment.Top

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
var node1 = { name: "node1", width: 50, height:50};
var node2 = { name: "node2", width: 50, height:50, verticalAlign: ej.datavisualization.Diagram.VerticalAlignment.Bottom };
var group = { name :"group", children:[ node1, node2 ], 
              container: { type: "canvas" }, offsetX:200, offsetY:100, 
              fillColor:"gray", minWidth:200, minHeight:200
            };
$("#diagramcontent").ejDiagram({nodes:[group]});
</script>

{% endhighlight %}

### nodes.visible `Boolean`
{:#members:nodes-visible}

Defines the visibility of the node

#### Default Value:

* true

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, visible:false }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.width `Number`
{:#members:nodes-width}

Defines the width of the node

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:50, offsetX:50, offsetY:50 }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodes.zOrder `Number`
{:#members:nodes-zorder}

Defines the z-index of the node

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var nodes;
nodes=[{ name: "node1", width: 100, height:100, offsetX:50, offsetY:50, zOrder: 10 }];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>

{% endhighlight %}

### nodeTemplate `Object`
{:#members:nodetemplate}

Binds the custom JSON data with node properties

#### Default Value:

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
   var data = [
        { "Id": "E1", "Name": "Maria Anders", "Designation": "Managing Director" },
        { "Id": "E2" , "Name": "Ana Trujillo", "Designation": "Project Manager", "ReportingPerson": "E1" } ];
		
   $("#diagramcontent").ejDiagram({
	   dataSourceSettings: { id: "Id", parent: "ReportingPerson", dataSource: data },
	   //Sets the method name to node template 
	   nodeTemplate :"nodeTemplate"
   });
   
   //Binds the custom properties with node properties and sets the styles
    function nodeTemplate(diagram, node) {
         node.labels[0].text = node.Name;
     }
   
</script>

{% endhighlight %}

### pageSettings `Object`
{:#members:pagesettings}

Defines the size and appearance of diagram page

### pageSettings.autoScrollBorder `Object`
{:#members:pagesettings-autoscrollborder}

Defines the maximum distance to be left between the object and the scroll bar to trigger auto scrolling

#### Default Value:

* { left: 15, top: 15, right: 15, bottom: 15 }

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({
    pageSettings:{ autoScrollBorder: { left: 50, top: 50, right: 50, bottom: 50 } }
});
</script>

{% endhighlight %}

### pageSettings.multiplePage `Boolean`
{:#members:pagesettings-multiplepage}

Sets whether multiple pages can be created to fit all nodes and connectors

#### Default Value:

* false

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({
    pageSettings:{multiplePage:false}
});
</script>

{% endhighlight %}

### pageSettings.pageBackgroundColor `String`
{:#members:pagesettings-pagebackgroundcolor}

Defines the background color of diagram pages

#### Default Value:

* "#ffffff"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({
    pageSettings:{ pageBackgroundColor:"lightgray"}
});
</script>

{% endhighlight %}

### pageSettings.pageBorderColor `String`
{:#members:pagesettings-pagebordercolor}

Defines the page border color

#### Default Value:

* "#565656"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({
    pageSettings:{ pageBorderColor:"black", pageBorderWidth: 2}
});
</script>

{% endhighlight %}

### pageSettings.pageBorderWidth `Number`
{:#members:pagesettings-pageborderwidth}

Sets the border width of diagram pages

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({
    pageSettings:{ pageBorderColor:"black", pageBorderWidth: 2}
});
</script>

{% endhighlight %}

### pageSettings.pageHeight `Number`
{:#members:pagesettings-pageheight}

Defines the height of a page

#### Default Value:

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({
    pageSettings:{ pageWidth: 500, pageHeight: 500 }
});
</script>

{% endhighlight %}

### pageSettings.pageMargin `Number`
{:#members:pagesettings-pagemargin}

Defines the page margin

#### Default Value:

* 24

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({
    pageSettings:{ pageMargin : 20 }
});
</script>

{% endhighlight %}

### pageSettings.pageOrientation `enum`
{:#members:pagesettings-pageorientation}

<ts name = "ej.datavisualization.Diagram.PageOrientations"/>

Sets the orientation of the page.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">Landscape</td>
            <td class="description last">Used to set orientation as Landscape</td>
       </tr>
        <tr>
            <td class="name">Portrait</td>
            <td class="description last">Used to set orientation as portrait</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.PageOrientations.Portrait

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({
    pageSettings:{ pageWidth: 800, pageHeight: 500, 
	pageOrientation:ej.datavisualization.Diagram.PageOrientations.Landscape }
});
</script>

{% endhighlight %}

### pageSettings.pageWidth `Number`
{:#members:pagesettings-pagewidth}

Defines the height of a diagram page

#### Default Value:

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({
    pageSettings:{ pageWidth: 500, pageHeight: 500 }
});
</script>

{% endhighlight %}

### pageSettings.scrollableArea `Object`
{:#members:pagesettings-scrollablearea}

Defines the scrollable area of diagram. Applicable, if the scroll limit is "limited".

#### Default Value:

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({
    pageSettings:{ scrollLimit: "limited",
    scrollableArea: {x:0, y:0, width:1000, height:1000} }
});
</script>
{% endhighlight %}

### pageSettings.scrollLimit `enum`
{:#members:pagesettings-scrolllimit}

<ts name = "ej.datavisualization.Diagram.ScrollLimit"/>

Defines the scrollable region of diagram.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">Infinite</td>
            <td class="description last">Used to set scrollLimit as Infinite</td>
       </tr>
        <tr>
            <td class="name">Diagram</td>
            <td class="description last">Used to set scrollLimit as Diagram</td>
       </tr>
        <tr>
            <td class="name">Limited</td>
            <td class="description last">Used to set scrollLimit as Limited</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.ScrollLimit.Infinite

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({
    pageSettings:{ scrollLimit: ej.datavisualization.Diagram.ScrollLimit.Diagram }
});
</script>
{% endhighlight %}


### pageSettings.boundaryConstraints `enum`
{:#members:pagesettings-boundaryconstraints}

<ts name = "ej.datavisualization.Diagram.BoundaryConstraints"/>

Defines the draggable region of diagram elements.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">Infinite</td>
            <td class="description last">Used to set boundaryConstraints as Infinite</td>
       </tr>
        <tr>
            <td class="name">Diagram</td>
            <td class="description last">Used to set boundaryConstraints as Diagram</td>
       </tr>
        <tr>
            <td class="name">Page</td>
            <td class="description last">Used to set boundaryConstraints as Page</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.BoundaryConstraints.Infinite

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({
    pageSettings:{ boundaryConstraints: ej.datavisualization.Diagram.BoundaryConstraints.Diagram }
});
</script>
{% endhighlight %}

### pageSettings.showPageBreak `Boolean`
{:#members:pagesettings-showpagebreak}

Enables or disables the page breaks

#### Default Value:

* false

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({
    pageSettings:{ showPageBreak: true }
});
</script>

{% endhighlight %}

### scrollSettings `Object`
{:#members:scrollsettings}

Defines the zoom value, zoom factor, scroll status and view port size of the diagram

### scrollSettings.currentZoom `Number`
{:#members:scrollsettings-currentzoom}

Allows to read the zoom value of diagram

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>	
var diagram = $("#diagramcontent").ejDiagram("instance");
console.log(diagram.model.scrollSettings.currentZoom);
</script>

{% endhighlight %}

### scrollSettings.horizontalOffset `Number`
{:#members:scrollsettings-horizontaloffset}

Sets the horizontal scroll offset

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({
	scrollSettings:{ horizontalOffset: 50 }
})
</script>

{% endhighlight %}

### scrollSettings.padding `Object`
{:#members:scrollsettings-padding}

Allows to extend the scrollable region that is based on the scroll limit

#### Default Value:

* {left: 0, right: 0, top:0, bottom: 0}

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({
	//Sets the region to be extended
    scrollSettings: { padding: { left: 25, right: 25, top: 25, bottom: 25} }
});
</script>

{% endhighlight %}

### scrollSettings.verticalOffset `Number`
{:#members:scrollsettings-verticaloffset}

Sets the vertical scroll offset

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({
	scrollSettings:{ verticalOffset: 50 }
})
</script>

{% endhighlight %}

### scrollSettings.viewPortHeight `Number`
{:#members:scrollsettings-viewportheight}

Allows to read the view port height of the diagram

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
	
var diagram = $("#diagramcontent").ejDiagram("instance");
console.log(diagram.model.scrollSettings.viewPortHeight);

</script>

{% endhighlight %}

### scrollSettings.viewPortWidth `Number`
{:#members:scrollsettings-viewportwidth}

Allows to read the view port width of the diagram

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
	
var diagram = $("#diagramcontent").ejDiagram("instance");
console.log(diagram.model.scrollSettings.viewPortWidth);

</script>

{% endhighlight %}

### selectedItems `Object`
{:#members:selecteditems}

Defines the size and position of selected items and defines the appearance of selector

### selectedItems.children `Array`
{:#members:selecteditems-children}

A read only collection of the selected items

#### Default Value:

* []

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram = $("#diagramcontent").ejDiagram("instance");
//Read the selected items 
for(var i =0; i< diagram.model.selectedItems.children; i++){
    //Do your actions here
}
</script>

{% endhighlight %}

### selectedItems.constraints `enum`
{:#members:selecteditems-constraints}

<ts name = "ej.datavisualization.Diagram.SelectorConstraints"/>

Controls the visibility of selector.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">None</td>
            <td class="description last">Hides the selector</td>
       </tr>
        <tr>
            <td class="name">Rotator</td>
            <td class="description last">Sets the visibility of rotation handle as visible</td>
       </tr>
        <tr>
            <td class="name">Resizer</td>
            <td class="description last">Sets the visibility of resize handles as visible</td>
       </tr>
        <tr>
            <td class="name">UserHandles</td>
            <td class="description last">Sets the visibility of user handles as visible</td>
       </tr>
        <tr>
            <td class="name">All</td>
            <td class="description last">Sets the visibility of all selection handles as visible</td>
       </tr>
   </tbody>
</table>


#### Default Value:

* ej.datavisualization.Diagram.SelectorConstraints.All

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({
     selectedItems: { constraints: ej.datavisualization.Diagram.SelectorConstraints.UserHandles } 
});
</script>

{% endhighlight %}

### selectedItems.getConstraints `Object`
{:#members:selecteditems-getconstraints}

Defines a method that dynamically enables/ disables the interaction with multiple selection.

#### Default Value:

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({
selectedItems: { 
	getConstraints: function() {
		//Allows to drag the multiple selected elements even when the selected elements are not movable 
		return ej.datavisualization.Diagram.NodeConstraints.Drag | ej.datavisualization.Diagram.NodeConstraints.Resize
    } }
});
</script>

{% endhighlight %}

### selectedItems.height `Number`
{:#members:selecteditems-height}

Sets the height of the selected items

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
//Sets the height of the selector as 100
$("#diagramcontent").ejDiagram({
     selectedItems: { height:100, width: 100 }
});
</script>

{% endhighlight %}

### selectedItems.offsetX `Number`
{:#members:selecteditems-offsetx}

Sets the x position of the selector 

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({
     selectedItems: { offsetX:100, offsetY: 100 }
});;
</script>

{% endhighlight %}

### selectedItems.offsetY `Number`
{:#members:selecteditems-offsety}

Sets the y position of the selector

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({
     selectedItems: { offsetX:100, offsetY: 100 }
});
</script>

{% endhighlight %}

### selectedItems.rotateAngle `Number`
{:#members:selecteditems-rotateangle}

Sets the angle to rotate the selected items

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({
     selectedItems: { rotateAngle: 90 }
});
</script>

{% endhighlight %}

### selectedItems.tooltip `Object`
{:#members:selecteditems-tooltip}

Sets the angle to rotate the selected items. For tooltip properties, refer [Tooltip](#members:tooltip)

#### Default Value:

* ej.datavisualization.Diagram.Tooltip()

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({
     selectedItems: { tooltip : { alignment:{ vertical:"top" } } }
});
</script>

{% endhighlight %}

### selectedItems.userHandles `Array`
{:#members:selecteditems-userhandles}

A collection of frequently used commands that will be added around the selector

#### Default Value:

* []

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var userHandle= [];
var cloneHandle = ej.datavisualization.Diagram.UserHandle();
userHandle.push(cloneHandle);
$("#diagramcontent").ejDiagram({selectedItems:{userHandles:userHandle}});
</script>

{% endhighlight %}

### selectedItems.userHandles.backgroundColor `String`
{:#members:selecteditems-userhandles-backgroundcolor}

Defines the background color of the user handle

####Default Value:

* "#2382c3"

####Example

{% highlight html %}
<div id="diagramcontent"></div>
<script>
 var userHandle = [];
        var cloneHandle = ej.datavisualization.Diagram.UserHandle();
        cloneHandle.name = "cloneHandle";
        cloneHandle.backgroundColor = "#4D4D4D";
        userHandle.push(cloneHandle);
$("#diagramcontent").ejDiagram({selectedItems:{userHandles:userHandle}});
</script>

{% endhighlight %}

### selectedItems.userHandles.borderColor `String`
{:#members:selecteditems-userhandles-bordercolor}

Sets the border color of the user handle

#### Default Value:

* "transparent"

#### Example

{% highlight html %}
<div id="diagramcontent"></div>
<script>
 var userHandle = [];
        var cloneHandle = ej.datavisualization.Diagram.UserHandle();
        cloneHandle.name = "cloneHandle";
        cloneHandle.borderColor = "red";
        userHandle.push(cloneHandle);
$("#diagramcontent").ejDiagram({selectedItems:{userHandles:userHandle}});
</script>

{% endhighlight %}

### selectedItems.userHandles.enableMultiSelection `Boolean`
{:#members:selecteditems-userhandles-enablemultiselection}

Defines whether the user handle should be added, when more than one element is selected

#### Default Value:

* false

#### Example

{% highlight html %}
<div id="diagramcontent"></div>
<script>
 var userHandle = [];
        var cloneHandle = ej.datavisualization.Diagram.UserHandle();
        cloneHandle.name = "cloneHandle";
        cloneHandle.enableMultiSelection = true;
        userHandle.push(cloneHandle);
$("#diagramcontent").ejDiagram({selectedItems:{userHandles:userHandle}});
</script>

{% endhighlight %}

### selectedItems.userHandles.pathColor `String`
{:#members:selecteditems-userhandles-pathcolor}

Sets the stroke color of the user handle

####Default Value:

* transparent

####Example

{% highlight html %}
<div id="diagramcontent"></div>
<script>
 var userHandle = [];
        var cloneHandle = ej.datavisualization.Diagram.UserHandle();
        cloneHandle.name = "cloneHandle"; 
        cloneHandle.pathData = "M4.6350084,4.8909971 L4.6350084,9.3649971 9.5480137,9.3649971 9.5480137,4.8909971 z M3.0000062,2.8189973 L11.184016,2.8189973 11.184016,10.999997 3.0000062,10.999997 z M0,0 L7.3649998,0 7.3649998,1.4020001 1.4029988,1.4020001 1.4029988,8.0660002 0,8.0660002 0,1.4020001 0,0.70300276 z";
        cloneHandle.tool = new CloneTool(cloneHandle.name);
        cloneHandle.pathColor = "white";
        userHandle.push(cloneHandle);
        $("#diagramcontent").ejDiagram({selectedItems:{userHandles:userHandle}});
</script>

{% endhighlight %}

### selectedItems.userHandles.pathData `String`
{:#members:selecteditems-userhandles-pathdata}

Defines the custom shape of the user handle

####Default Value:

* ""

####Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
 var userHandle = [];
        var cloneHandle = ej.datavisualization.Diagram.UserHandle();
        cloneHandle.name = "cloneHandle";
        cloneHandle.pathData = "M4.6350084,4.8909971 L4.6350084,9.3649971 9.5480137,9.3649971 9.5480137,4.8909971 z M3.0000062,2.8189973 L11.184016,2.8189973 11.184016,10.999997 3.0000062,10.999997 z M0,0 L7.3649998,0 7.3649998,1.4020001 1.4029988,1.4020001 1.4029988,8.0660002 0,8.0660002 0,1.4020001 0,0.70300276 z";
        cloneHandle.tool = new CloneTool(cloneHandle.name);
        userHandle.push(cloneHandle);
$("#diagramcontent").ejDiagram({selectedItems:{userHandles:userHandle}});
</script>

{% endhighlight %}
      
### selectedItems.userHandles.position `enum`
{:#members:selecteditems-userhandles-position}

<ts name = "ej.datavisualization.Diagram.UserHandlePositions "/>
    
Defines the position of the user handle
    
<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">TopLeft</td>
            <td class="description last">Set the position of the userhandle as topleft</td>
       </tr>
        <tr>
            <td class="name">TopCenter</td>
            <td class="description last">Set the position of the userhandle as topcenter</td>
       </tr>
        <tr>
            <td class="name">TopRight</td>
            <td class="description last">Set the position of the userhandle as topright</td>
       </tr>
       <tr>
            <td class="name">MiddleLeft</td>
            <td class="description last">Set the position of the userhandle as middleleft</td>
       </tr>
       <tr>
            <td class="name">MiddleRight</td>
            <td class="description last">Set the position of the userhandle as middleright</td>
       </tr>
       <tr>
            <td class="name">BottomLeft</td>
            <td class="description last">Set the position of the userhandle as bottomleft</td>
       </tr>
       <tr>
            <td class="name">BottomCenter</td>
            <td class="description last">Set the position of the userhandle as bottomcenter</td>
       </tr>
        <tr>
            <td class="name">BottomRight</td>
            <td class="description last">Set the position of the userhandle as bottom right</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.UserHandlePositions.BottomCenter

#### Example

{% highlight html %}
<div id="diagramcontent"></div>
<script>
 var userHandle = [];
        var cloneHandle = ej.datavisualization.Diagram.UserHandle();
        cloneHandle.name = "cloneHandle";
        cloneHandle.position =" middleleft";
        userHandle.push(cloneHandle);
$("#diagramcontent").ejDiagram({selectedItems:{userHandles:userHandle}});
</script>

{% endhighlight %}

### selectedItems.userHandles.size `Number`
{:#members:selecteditems-userhandles-size}

Defines the size of the user handle

#### Default Value:

* 8

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
 var userHandle = [];
        var cloneHandle = ej.datavisualization.Diagram.UserHandle();
        cloneHandle.name = "cloneHandle";
        cloneHandle.size = 20;
        userHandle.push(cloneHandle);
$("#diagramcontent").ejDiagram({selectedItems:{userHandles:userHandle}});
</script>

{% endhighlight %}


### selectedItems.userHandles.tool `Object`
{:#members:selecteditems-userhandles-tool}

Defines the interactive behaviors of the user handle

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script> 
  var CloneTool = (function (base) {
            ej.datavisualization.Diagram.extend(CloneTool, base);
            function CloneTool(name) {
                base.call(this, name);
                this.singleAction = true;
                this.clonedNodes = [];
                this.cursor = "pointer";
            }
            CloneTool.prototype.mouseup = function (evt) {
                    this.diagram.copy();
                    this.diagram.paste();
                }
            }
            return CloneTool;
        })(ej.datavisualization.Diagram.ToolBase);
var userHandle = [];
var cloneHandle = ej.datavisualization.Diagram.UserHandle();
cloneHandle.name = "cloneHandle";
cloneHandle.pathData = "M4.6350084,4.8909971 L4.6350084,9.3649971 9.5480137,9.3649971 9.5480137,4.8909971 z M3.0000062,2.8189973 L11.184016,2.8189973 11.184016,10.999997 3.0000062,10.999997 z M0,0 L7.3649998,0 7.3649998,1.4020001 1.4029988,1.4020001 1.4029988,8.0660002 0,8.0660002 0,1.4020001 0,0.70300276 z";
cloneHandle.tool =  new CloneTool(cloneHandle.name);;
userHandle.push(cloneHandle);
$("#diagramcontent").ejDiagram({selectedItems:{userHandles:userHandle}});
</script>

{% endhighlight %}

### selectedItems.userHandles.visible `Boolean`
{:#members:selecteditems-userhandles-visible}

Defines the visibility of the user handle

#### Default Value:

* true

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
 var userHandle = [];
        var cloneHandle = ej.datavisualization.Diagram.UserHandle();
        cloneHandle.name = "cloneHandle";
        cloneHandle.visible = "true";
        userHandle.push(cloneHandle);
$("#diagramcontent").ejDiagram({selectedItems:{userHandles:userHandle}});
</script>

{% endhighlight %}

### selectedItems.width `Number`
{:#members:selecteditems-width}

Sets the width of the selected items

#### Default Value:

* 0

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
	
//Sets the width of the selector as 100
$("#diagramcontent").ejDiagram({
     selectedItems: { height:100, width: 100 }
});
</script>

{% endhighlight %}

### showTooltip `Boolean`
{:#members:showtooltip}

Enables or disables tooltip of diagram

#### Default Value:

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

Defines the gridlines and defines how and when the objects have to be snapped

### snapSettings.enableSnapToObject `Boolean`
{:#members:snapsettings-enablesnaptoobject}

Enables or disables snapping nodes/connectors to objects

#### Default Value:

* true

#### Example

{% highlight html %}

$("#diagramcontent").ejDiagram({ snapSettings:{ enableSnapToObject: false } });

{% endhighlight %}

### snapSettings.horizontalGridLines `Object`
{:#members:snapsettings-horizontalgridlines}

Defines the appearance of horizontal gridlines

### snapSettings.horizontalGridLines.lineColor `String`
{:#members:snapsettings-horizontalgridlines-linecolor}

Defines the line color of horizontal grid lines

#### Default Value:

* "lightgray"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var gridline = { lineColor :"blue" };
$("#diagramcontent").ejDiagram({ snapSettings: { horizontalGridLines: gridline} });
</script>

{% endhighlight %}

### snapSettings.horizontalGridLines.lineDashArray `String`
{:#members:snapsettings-horizontalgridlines-linedasharray}

Specifies the pattern of dashes and gaps used to stroke horizontal grid lines

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var gridline = { lineColor :"blue", lineDashArray:"2,2" };
$("#diagramcontent").ejDiagram({snapSettings: { horizontalGridLines: gridline} });
</script>

{% endhighlight %}

### snapSettings.horizontalGridLines.linesInterval `Array`
{:#members:snapsettings-horizontalgridlines-linesinterval}

A pattern of lines and gaps that defines a set of horizontal gridlines

#### Default Value:

* [1.25, 18.75, 0.25, 19.75, 0.25, 19.75, 0.25, 19.75, 0.25, 19.75]

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var gridline = { linesInterval: [1, 14, 0.5, 14.5 ] };
$("#diagramcontent").ejDiagram({snapSettings: { horizontalGridLines: gridline} });
}});
</script>

{% endhighlight %}

### snapSettings.horizontalGridLines.snapInterval `Array`
{:#members:snapsettings-horizontalgridlines-snapinterval}

Specifies a set of intervals to snap the objects

#### Default Value:

* [20]

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
//Snap objects to every 5th pixel
var gridline = { snapInterval : [5] };
$("#diagramcontent").ejDiagram({snapSettings: { horizontalGridLines: gridline} });
</script>

{% endhighlight %}

### snapSettings.snapAngle `Number`
{:#members:snapsettings-snapangle}

Defines the angle by which the object needs to be snapped

#### Default Value:

* 5

#### Example

{% highlight html %}

$("#diagramcontent").ejDiagram({snapSettings: { snapAngle: 10} });

{% endhighlight %}

### snapSettings.snapObjectDistance `Number`
{:#members:snapsettings-snapobjectdistance}

Defines the minimum distance between the selected object and the nearest object

#### Default Value:

* 5

#### Example

{% highlight html %}

var snap = {"snapObjectDistance":5};
//snapObjectDistance
$("#diagramcontent").ejDiagram({snapSettings: snap});

{% endhighlight %}

### snapSettings.verticalGridLines `Object`
{:#members:snapsettings-verticalgridlines}

Defines the appearance of horizontal gridlines

### snapSettings.verticalGridLines.lineColor `String`
{:#members:snapsettings-verticalgridlines-linecolor}

Defines the line color of horizontal grid lines

#### Default Value:

* "lightgray"

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var gridline = { lineColor :"blue" };
$("#diagramcontent").ejDiagram({snapSettings: { verticalGridLines: gridline} });
</script>

{% endhighlight %}

### snapSettings.verticalGridLines.lineDashArray `String`
{:#members:snapsettings-verticalgridlines-linedasharray}

Specifies the pattern of dashes and gaps used to stroke horizontal grid lines

#### Default Value:

* ""

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var gridline = { lineColor :"blue", lineDashArray:"2,2" };
$("#diagramcontent").ejDiagram({snapSettings: { verticalGridLines: gridline} });
</script>

{% endhighlight %}

### snapSettings.verticalGridLines.linesInterval `Array`
{:#members:snapsettings-verticalgridlines-linesinterval}

A pattern of lines and gaps that defines a set of horizontal gridlines

#### Default Value:

* [1.25, 18.75, 0.25, 19.75, 0.25, 19.75, 0.25, 19.75, 0.25, 19.75]

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var gridline = { linesInterval: [1, 14, 0.5, 14.5 ] };
$("#diagramcontent").ejDiagram({snapSettings: { verticalGridLines: gridline} });
</script>

{% endhighlight %}

### snapSettings.verticalGridLines.snapInterval `Array`
{:#members:snapsettings-verticalgridlines-snapinterval}

Specifies a set of intervals to snap the objects

#### Default Value:

* [20]

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
//Snap objects to every 5th pixel
var gridline = { snapInterval : [5] };
$("#diagramcontent").ejDiagram({snapSettings: { verticalGridLines: gridline} });
</script>

{% endhighlight %}

### tool `enum`
{:#members:tool}

<ts name = "ej.datavisualization.Diagram.Tool"/>

Enables/Disables the interactive behaviors of diagram.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">None</td>
            <td class="description last">Disables all Tools</td>
       </tr>
        <tr>
            <td class="name">SingleSelect</td>
            <td class="description last">Enables/Disables SingleSelect tool</td>
       </tr>
        <tr>
            <td class="name">MultipleSelect</td>
            <td class="description last">Enables/Disables MultiSelect tool</td>
       </tr>
        <tr>
            <td class="name">ZoomPan</td>
            <td class="description last">Enables/Disables ZoomPan tool</td>
       </tr>
        <tr>
            <td class="name">DrawOnce</td>
            <td class="description last">Enables/Disables DrawOnce tool</td>
       </tr>
        <tr>
            <td class="name">ContinuesDraw</td>
            <td class="description last">Enables/Disables ContinuousDraw tool</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.Tool.All

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
//Prevents editing and allows only to zoom/pan
$("#diagramcontent").ejDiagram({tool: ej.datavisualization.Diagram.Tool.ZoomPan});
</script>

{% endhighlight %}

### tooltip `Object`
{:#members:tooltip}

An object that defines the description, appearance and alignments of tooltips

#### Default Value:

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script type="text/x-jsrender" id="mouseovertooltip">
   <div style="background-color: #F08080; color: white; white-space: nowrap; height: 20px">
        <span style="padding: 5px;"> {{:Designation}} </span>
   </div>
</script>

<script>
$("#diagramcontent").ejDiagram({
	//Defines mouse over tooltip
	tooltip: {
		templateId: "mouseovertooltip",
		alignment: {
			horizontal: "center",
			vertical: "bottom"
		}
	},
	//Defines nodes
	nodes: [{
		name: "elizabeth",width: 70,height: 40,	offsetX: 100,offsetY: 100,
		Designation: "Managing Director"
	}]
});
</script>

{% endhighlight %}

### tooltip.alignment `Object`
{:#members:tooltip-alignment}

Aligns the tooltip around nodes/connectors

### tooltip.alignment.horizontal `enum`
{:#members:tooltip-alignment-horizontal}

<ts name = "ej.datavisualization.Diagram.HorizontalAlignment"/>

Defines the horizontal alignment of tooltip.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">Left</td>
            <td class="description last">Used to align text horizontally on left side of node/connector</td>
       </tr>
        <tr>
            <td class="name">Center</td>
            <td class="description last">Used to align text horizontally on center of node/connector</td>
       </tr>
        <tr>
            <td class="name">Right</td>
            <td class="description last">Used to align text horizontally on right side of node/connector</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.HorizontalAlignment.Center

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({
	tooltip: {
		alignment: {
			horizontal: ej.datavisualization.Diagram.HorizontalAlignment.Center
		}
	}
});
</script>

{% endhighlight %}

### tooltip.alignment.vertical `enum`
{:#members:tooltip-alignment-vertical}

<ts name = "ej.datavisualization.Diagram.VerticalAlignment"/>

Defines the vertical alignment of tooltip.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">Top</td>
            <td class="description last">Used to align text Vertically on left side of node/connector</td>
       </tr>
        <tr>
            <td class="name">Center</td>
            <td class="description last">Used to align text Vertically on center of node/connector</td>
       </tr>
        <tr>
            <td class="name">Bottom</td>
            <td class="description last">Used to align text Vertically on bottom of node/connector</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.VerticalAlignment.Bottom

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({
	tooltip: {
		alignment: {
			vertical: ej.datavisualization.Diagram.VerticalAlignment.Bottom
		}
	}
});
</script>

{% endhighlight %}

### tooltip.margin `Object`
{:#members:tooltip-margin}

Sets the margin of the tooltip

#### Default Value:

* { left: 5, right: 5, top: 5, bottom: 5 }

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({
	tooltip: {
		margin : { top:10 }
	}
});
</script>

{% endhighlight %}

### tooltip.relativeMode `enum`
{:#members:tooltip-relativemode}

<ts name = "ej.datavisualization.Diagram.RelativeMode"/>

Defines whether the tooltip should be shown at the mouse position or around node.

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
    <tbody>
        <tr>
            <td class="name">object</td>
            <td class="description last">Shows tooltip around the node</td>
       </tr>
        <tr>
            <td class="name">Mouse</td>
            <td class="description last">Shows tooltip at the mouse position</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.datavisualization.Diagram.RelativeMode.Object

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({
	tooltip: {
		//Shows tooltip at the mouse position
		relativeMode: ej.datavisualization.Diagram.RelativeMode.Mouse
	}
});
</script>

{% endhighlight %}

### tooltip.templateId `String`
{:#members:tooltip-templateid}

Sets the svg/html template to be bound with tooltip

#### Default Value:

* ""

#### Example

{% highlight html %}

<script type="text/x-jsrender" id="mouseovertooltip">
   <div style="background-color: #F08080; color: white; white-space: nowrap; height: 20px">
        <span style="padding: 5px;"> {{:Designation}} </span>
   </div>
</script>

<script>	
$("#diagramcontent").ejDiagram({
	//Defines mouse over tooltip
	tooltip: {
		templateId: "mouseovertooltip"
	} });	
</script>

{% endhighlight %}

### width `String`
{:#members:width}

Specifies the width of the diagram

#### Default Value:

* null

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({ width:"1000" });
</script>

{% endhighlight %}

### zoomFactor `Number`
{:#members:zoomfactor}

Sets the factor by which we can zoom in or zoom out

#### Default Value:

* 0.2

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({zoomFactor: 1});
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
			<td class="type">object</td>
			<td class="description last">a JSON to define a node/connector or an array of nodes and connector</td>
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
			<td class="description last">name of the node to which label will be added</td>
		</tr>
		<tr>
			<td class="name">newLabel</td>
			<td class="type">object</td>
			<td class="description last">JSON for the new label to be added</td>
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
			<td class="type">string</td>
			<td class="description last">name of the swimlane to which the phase will be added</td>
		</tr>
		<tr>
			<td class="name">options</td>
			<td class="type">object</td>
			<td class="description last">JSON object to define the phase to be added</td>
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
			<td class="type">string</td>
			<td class="description last">name of the node to which the ports have to be added</td>
		</tr>
		<tr>
			<td class="name">ports</td>
			<td class="type">array</td>
			<td class="description last">a collection of ports to be added to the specified node</td>
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
			<td class="type">object</td>
			<td class="description last">the node to be selected</td>
		</tr>
		<tr>
			<td class="name">[clearSelection]</td>
			<td class="type">boolean</td>
			<td class="description last">to define whether to clear the existing selection or not</td>
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
			<td class="type">string</td>
			<td class="description last">to specify the direction towards which the selected objects are to be aligned("left","right",top","bottom")</td>
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
			<td class="type">object</td>
			<td class="description last">the rectangular region that is to be brought into diagram viewport</td>
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
			<td class="type">object</td>
			<td class="description last">the rectangular region that is to be brought to the center of diagram viewport</td>
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

#### Returns:

* Object

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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">[options]</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">options to export the desired region of diagram to the desired formats.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">fileName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">name of the file to be downloaded.</td>
</tr>
<tr>
<td class="name">format</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">format of the exported file/data. See [File Formats](/js/api/global#fileformats).</td>
</tr>
<tr>
<td class="name">mode</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">to set whether to export diagram as a file or as raw data. See [Export Modes](/js/api/global#exportmodes).</td>
</tr>
<tr>
<td class="name">region</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">to set the region of the diagram to be exported. See [Region](/js/api/global#region).</td>
</tr>
<tr>
<td class="name">bounds</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">to export any custom region of diagram.</td>
</tr>
<tr>
<td class="name">margin</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">to set margin to the exported data.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Returns:

* String

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
			<td class="type">string</td>
			<td class="description last">name of the node/connector that is to be identified</td>
		</tr>
	</tbody>
</table>

#### Returns:

* Object

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
			<td class="name">[mode]</td>
			<td class="type">string</td>
			<td class="description last">to set the mode of fit to command. See [Fit Mode](/js/api/global#fitmode)</td>
		</tr>
		<tr>
			<td class="name">[region]</td>
			<td class="type">string</td>
			<td class="description last">to set whether the region to be fit will be based on diagram elements or page settings [Region](/js/api/global#region)</td>
		</tr>
		<tr>
			<td class="name">[margin]</td>
			<td class="type">object</td>
			<td class="description last">to set the required margin</td>
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
			<td class="type">string</td>
			<td class="description last">name of the node to which the label has to be inserted</td>
		</tr>
		<tr>
			<td class="name">label</td>
			<td class="type">object</td>
			<td class="description last">JSON to define the new label</td>
		</tr>
		<tr>
			<td class="name">[index]</td>
			<td class="type">number</td>
			<td class="description last">index to insert the label into the node</td>
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
			<td class="type">object</td>
			<td class="description last">JSON data to load the diagram</td>
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
			<td class="type">string</td>
			<td class="description last">specifies the direction to move the selected objects ("left","right",top","bottom")</td>
		</tr>
		<tr>
			<td class="name">[delta]</td>
			<td class="type">number</td>
			<td class="description last">specifies the number of pixels by which the selected objects have to be moved</td>
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
			<td class="name">[object]</td>
			<td class="type">object</td>
			<td class="description last">object to be added to diagram</td>
		</tr>
		<tr>
			<td class="name">[rename]</td>
			<td class="type">boolean</td>
			<td class="description last">to define whether the specified object is to be renamed or not</td>
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
			<td class="name">[node]</td>
			<td class="type">object</td>
			<td class="description last">the node/connector to be removed from diagram</td>
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
			<td class="type">object</td>
			<td class="description last">the node/connector to be removed from selection list</td>
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

#### Returns:

* Object

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
			<td class="type">object</td>
			<td class="description last">the node/connector to be brought into view</td>
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
			<td class="type">object</td>
			<td class="description last">node/connector that contains the label to be edited</td>
		</tr>
		<tr>
			<td class="name">label</td>
			<td class="type">object</td>
			<td class="description last">to be edited</td>
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
			<td class="type">object</td>
			<td class="description last">JSON to specify the diagram properties that have to be modified</td>
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
</script>

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
			<td class="type">string</td>
			<td class="description last">name of the connector to be updated</td>
		</tr>
		<tr>
			<td class="name">options</td>
			<td class="type">object</td>
			<td class="description last">JSON to specify the connector properties that have to be updated</td>
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
			<td class="type">string</td>
			<td class="description last">the name of node/connector which contains the label to be updated</td>
		</tr>
		<tr>
			<td class="name">label</td>
			<td class="type">object</td>
			<td class="description last">the label to be modified</td>
		</tr>
		<tr>
			<td class="name">options</td>
			<td class="type">object</td>
			<td class="description last">JSON to specify the label properties that have to be updated</td>
		</tr>
	</tbody>
</table>

#### Returns:

* Object

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
			<td class="type">string</td>
			<td class="description last">name of the node that is to be updated</td>
		</tr>
		<tr>
			<td class="name">options</td>
			<td class="type">object</td>
			<td class="description last">JSON to specify the properties of node that have to be updated</td>
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
			<td class="type">string</td>
			<td class="description last">the name of node which contains the port to be updated</td>
		</tr>
		<tr>
			<td class="name">port</td>
			<td class="type">object</td>
			<td class="description last">the port to be updated</td>
		</tr>
		<tr>
			<td class="name">options</td>
			<td class="type">object</td>
			<td class="description last">JSON to specify the properties of the port that have to be updated</td>
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
			<td class="type">string</td>
			<td class="description last">name of the node to be updated as selected object</td>
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
			<td class="name">[showUserHandles]</td>
			<td class="type">boolean</td>
			<td class="description last">to specify whether to show the user handles or not</td>
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

Update user handles with respect to the given node

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
			<td class="type">object</td>
			<td class="description last">node/connector with respect to which, the user handles have to be updated</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
var node = diagram.selectionList[0];
diagram.updateUserHandles(node);
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
			<td class="type">object</td>
			<td class="description last">to be upgraded</td>
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
			<td class="type">object</td>
			<td class="description last">options to zoom the diagram(zoom factor, zoomIn/zoomOut)</td>
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
			<td class="type">string</td>
			<td class="description last">Returns the delay between subsequent auto scrolls</td>
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
			<td class="type">object</td>
			<td class="description last">parameter returns the clicked node, connector or diagram</td>
		</tr>
		<tr>
			<td class="name">actualObject</td>
			<td class="type">number</td>
			<td class="description last">parameter returns the object that is actually clicked</td>
		</tr>
		<tr>
			<td class="name">offsetX</td>
			<td class="type">number</td>
			<td class="description last">parameter returns the horizontal coordinate of the mouse pointer, relative to the diagram</td>
		</tr>
		<tr>
			<td class="name">offsetY</td>
			<td class="type">number</td>
			<td class="description last">parameter returns  the vertical coordinate of the mouse pointer, relative to the diagram</td>
		</tr>
		<tr>
			<td class="name">count</td>
			<td class="type">number</td>
			<td class="description last">parameter returns the count of how many times the mouse button is pressed</td>
		</tr>
		<tr>
			<td class="name">event</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the actual click event arguments that explains which button is clicked</td>
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
			<td class="type">object</td>
			<td class="description last">parameter returns the connection that is changed between nodes, ports or points</td>
		</tr>
		<tr>
			<td class="name">connection</td>
			<td class="type">string</td>
			<td class="description last">parameter returns the new source node or target node of the connector</td>
		</tr>
		<tr>
			<td class="name">port</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the new source port or target port of the connector</td>
		</tr>
		<tr>
			<td class="name">cancel</td>
			<td class="type">boolean</td>
			<td class="description last">parameter defines whether to cancel the change or not</td>
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
			<td class="type">string</td>
			<td class="description last">parameter returns whether the connector is inserted or removed</td>
		</tr>
		<tr>
			<td class="name">element</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the connector that is to be added or deleted</td>
		</tr>
		<tr>
			<td class="name">cancel</td>
			<td class="type">boolean</td>
			<td class="description last">parameter defines whether to cancel the collection change or not</td>
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
			<td class="type">object</td>
			<td class="description last">returns the connector, the source point of which is being dragged</td>
		</tr>
		<tr>
			<td class="name">node</td>
			<td class="type">object</td>
			<td class="description last">returns the source node of the element</td>
		</tr>
		<tr>
			<td class="name">point</td>
			<td class="type">object</td>
			<td class="description last">returns the source point of the element</td>
		</tr>
		<tr>
			<td class="name">port</td>
			<td class="type">object</td>
			<td class="description last">returns the source port of the element</td>
		</tr>
		<tr>
			<td class="name">dragState</td>
			<td class="type">string</td>
			<td class="description last">returns the state of connection end point dragging(starting, dragging, completed)</td>
		</tr>
		<tr>
			<td class="name">cancel</td>
			<td class="type">boolean</td>
			<td class="description last">parameter defines whether to cancel the change or not</td>
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
			<td class="type">object</td>
			<td class="description last">parameter returns the connector, the target point of which is being dragged</td>
		</tr>
		<tr>
			<td class="name">node</td>
			<td class="type">object</td>
			<td class="description last">returns the target node of the element</td>
		</tr>
		<tr>
			<td class="name">point</td>
			<td class="type">object</td>
			<td class="description last">returns the target point of the element</td>
		</tr>
		<tr>
			<td class="name">port</td>
			<td class="type">object</td>
			<td class="description last">returns the target port of the element</td>
		</tr>
		<tr>
			<td class="name">dragState</td>
			<td class="type">string</td>
			<td class="description last">returns the state of connection end point dragging(starting, dragging, completed)</td>
		</tr>
		<tr>
			<td class="name">cancel</td>
			<td class="type">boolean</td>
			<td class="description last">parameter defines whether to cancel the change or not</td>
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
			<td class="type">object</td>
			<td class="description last">parameter returns the diagram object</td>
		</tr>
		<tr>
			<td class="name">contextmenu</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the actual arguments from context menu</td>
		</tr>
		<tr>
			<td class="name">target</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the object that was clicked</td>
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
			<td class="type">string</td>
			<td class="description last">parameter returns the id of the selected context menu item</td>
		</tr>
		<tr>
			<td class="name">text</td>
			<td class="type">string</td>
			<td class="description last">parameter returns the text of the selected context menu item</td>
		</tr>
		<tr>
			<td class="name">parentId</td>
			<td class="type">string</td>
			<td class="description last">parameter returns the parent id of the selected context menu item</td>
		</tr>
		<tr>
			<td class="name">parentText</td>
			<td class="type">string</td>
			<td class="description last">parameter returns the parent text of the selected context menu item</td>
		</tr>
		<tr>
			<td class="name">target</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the object that was clicked</td>
		</tr>
		<tr>
			<td class="name">canExecute</td>
			<td class="type">boolean</td>
			<td class="description last">parameter defines whether to execute the click event or not</td>
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
			<td class="type">object</td>
			<td class="description last">parameter returns the object that is actually clicked</td>
		</tr>
		<tr>
			<td class="name">element</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the selected object</td>
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
			<td class="type">object</td>
			<td class="description last">parameter returns the node or connector that is being dragged</td>
		</tr>
		<tr>
			<td class="name">oldValue</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the previous position of the node/connector</td>
		</tr>
		<tr>
			<td class="name">newValue</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the new position of the node/connector</td>
		</tr>
		<tr>
			<td class="name">dragState</td>
			<td class="type">string</td>
			<td class="description last">parameter returns the state of drag event (Starting, dragging, completed)</td>
		</tr>
		<tr>
			<td class="name">cancel</td>
			<td class="type">boolean</td>
			<td class="description last">parameter returns whether or not to cancel the drag event</td>
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
			<td class="type">object</td>
			<td class="description last">parameter returns the node or connector that is dragged into diagram</td>
		</tr>
		<tr>
			<td class="name">cancel</td>
			<td class="type">boolean</td>
			<td class="description last">parameter returns whether to add or remove the symbol from diagram</td>
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

### dragLeave
{:#events:dragleave}

Triggers when a symbol is dragged outside of the diagram.

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
			<td class="type">object</td>
			<td class="description last">parameter returns the node or connector that is dragged outside of the diagram</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

// drag leave event for diagram
$("#diagramcontent").ejDiagram({
dragLeave:function (args) {}
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
			<td class="type">object</td>
			<td class="description last">parameter returns the node or connector that is dragged over diagram</td>
		</tr>
		<tr>
			<td class="name">allowDrop</td>
			<td class="type">boolean</td>
			<td class="description last">parameter defines whether the symbol can be dropped at the current mouse position</td>
		</tr>
		<tr>
			<td class="name">target</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the node/connector over which the symbol is dragged</td>
		</tr>
		<tr>
			<td class="name">oldValue</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the previous position of the node/connector</td>
		</tr>
		<tr>
			<td class="name">newValue</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the new position of the node/connector</td>
		</tr>
		<tr>
			<td class="name">cancel</td>
			<td class="type">boolean</td>
			<td class="description last">parameter returns whether or not to cancel the dragOver event</td>
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
			<td class="type">object</td>
			<td class="description last">parameter returns node or connector that is being dropped</td>
		</tr>
		<tr>
			<td class="name">cancel</td>
			<td class="type">boolean</td>
			<td class="description last">parameter returns whether or not to cancel the drop event</td>
		</tr>
		<tr>
			<td class="name">source</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the object from where the element is dragged</td>
		</tr>
		<tr>
			<td class="name">target</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the object over which the object will be dropped</td>
		</tr>
		<tr>
			<td class="name">sourceType</td>
			<td class="type">String</td>
			<td class="description last">parameter returns the enum which defines the type of the source</td>
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
			<td class="type">object</td>
			<td class="description last">parameter returns the object that is added to/removed from a group</td>
		</tr>
		<tr>
			<td class="name">oldParent</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the old parent group(if any) of the object</td>
		</tr>
		<tr>
			<td class="name">newParent</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the new parent group(if any) of the object</td>
		</tr>
		<tr>
			<td class="name">cause</td>
			<td class="type">string</td>
			<td class="description last">parameter returns the cause of group change("group", unGroup")</td>
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

### historyChange 
{:#events:historychange}

Triggers when a change is reverted or restored(undo/redo)

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
			<td class="name">changes</td>
			<td class="type">Array</td>			 
			<td class="description">An array of objects, where each object represents the changes made in last undo/redo. To explore how the changes are defined, refer [Undo Redo Changes](#undo-redo-changes)</td>
		</tr>
		<tr>
			<td class="name">Source</td>
			<td class="type">Array</td>			 
			<td class="description">A collection of objects that are changed in the last undo/redo</td>
		</tr>		 
	</tbody>
</table>

#### Undo Redo Changes
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
			<td class="name">type</td>
			<td class="type">string</td>			 
			<td class="description">Returns the type of change that is reverted/restored (example:positionChanged, sizeChanged)</td>
		</tr>
		<tr>
			<td class="name">newValues</td>
			<td class="type">Object</td>			 
			<td class="description">Returns the new values of the properties that are changed.(example:newValues:{offset:60,offset:60,width:60,height:60})</td>
		</tr>
		<tr>
			<td class="name">oldValues</td>
			<td class="type">Object</td>			 
			<td class="description">Returns the old values of the properties that are changed.(example:oldValues:{offset:60,offset:60,width:60,height:60})</td>
		</tr>
		<tr>
			<td class="name">addedItems</td>
			<td class="type">Array</td>			 
			<td class="description">Returns the items that are newly added to model</td>
		</tr>
		<tr>
			<td class="name">deletedItems</td>
			<td class="type">Array</td>			 
			<td class="description">Returns the items that are deleted from model</td>
		</tr>		 
	</tbody>
</table>

#### Example

{% highlight html %}

// history change event for diagram
$("#diagramcontent").ejDiagram({
historyChange:function (args) {}
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
			<td class="type">object</td>
			<td class="description last">parameter returns the object that was actually clicked</td>
		</tr>
		<tr>
			<td class="name">selectedObject</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the object that is selected</td>
		</tr>
		<tr>
			<td class="name">cancel</td>
			<td class="type">boolean</td>
			<td class="description last">parameter returns whether or not to cancel the drop event</td>
		</tr>
		<tr>
			<td class="name">event</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the actual click event arguments that explains which button is clicked</td>
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
			<td class="type">object</td>
			<td class="description last">parameter returns the target node or connector</td>
		</tr>
		<tr>
			<td class="name">source</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the object from where the selected object is dragged</td>
		</tr>
		<tr>
			<td class="name">target</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the target object over which the selected object is dragged</td>
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
			<td class="type">object</td>
			<td class="description last">parameter returns the target node or connector</td>
		</tr>
		<tr>
			<td class="name">source</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the object from where the selected object is dragged</td>
		</tr>
		<tr>
			<td class="name">target</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the target object over which the selected object is dragged</td>
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
			<td class="type">object</td>
			<td class="description last">parameter returns the target node or connector</td>
		</tr>
		<tr>
			<td class="name">source</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the object from where the element is dragged</td>
		</tr>
		<tr>
			<td class="name">target</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the object over which the element is being dragged.</td>
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
			<td class="type">string</td>
			<td class="description last">parameter returns whether the node is to be added or removed</td>
		</tr>
		<tr>
			<td class="name">element</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the node which needs to be added or deleted</td>
		</tr>
		<tr>
			<td class="name">cancel</td>
			<td class="type">boolean</td>
			<td class="description last">parameter defines whether to cancel the collection change or not</td>
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
			<td class="type">object</td>
			<td class="description last">parameter returns the selected element</td>
		</tr>
		<tr>
			<td class="name">cause</td>
			<td class="type">String</td>
			<td class="description last">parameter returns the action is nudge or not</td>
		</tr>
		<tr>
			<td class="name">newValue</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the new value of the node property that is being changed</td>
		</tr>
		<tr>
			<td class="name">oldValue</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the old value of the property that is being changed</td>
		</tr>
		<tr>
			<td class="name">propertyName</td>
			<td class="type">string</td>
			<td class="description last">parameter returns the name of the property that is changed</td>
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
			<td class="type">object</td>
			<td class="description last">parameter returns the node that is rotated</td>
		</tr>
		<tr>
			<td class="name">oldValue</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the previous rotation angle</td>
		</tr>
		<tr>
			<td class="name">newValue</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the new rotation angle</td>
		</tr>
		<tr>
			<td class="name">cancel</td>
			<td class="type">boolean</td>
			<td class="description last">parameter to specify whether or not to cancel the event</td>
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
			<td class="type">object</td>
			<td class="description last">Parameter returns the new zoom value, horizontal and vertical scroll offsets.</td>
		</tr>
		<tr>
			<td class="name">oldValues</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the previous zoom value, horizontal and vertical scroll offsets.</td>
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
			<td class="type">object</td>
			<td class="description last">Parameter returns the connector that is being edited</td>
		</tr>
		<tr>
			<td class="name">dragState</td>
			<td class="type">string</td>
			<td class="description last">parameter returns the state of editing (starting, dragging, completed)</td>
		</tr>
		<tr>
			<td class="name">point</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the current mouse position</td>
		</tr>
		<tr>
			<td class="name">cancel</td>
			<td class="type">boolean</td>
			<td class="description last">parameter to specify whether or not to cancel the event</td>
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
			<td class="name">changeType</td>
			<td class="type">string</td>
			<td class="description last">parameter returns whether the item is selected or removed selection</td>
		</tr>
		<tr>
			<td class="name">element</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the item which is selected or to be selected</td>
		</tr>
		<tr>
			<td class="name">oldItems</td>
			<td class="type">array</td>
			<td class="description last">parameter returns the collection of nodes and connectors that have to be removed from selection list</td>
		</tr>
		<tr>
			<td class="name">newItems</td>
			<td class="type">array</td>
			<td class="description last">parameter returns the collection of nodes and connectors that have to be added to selection list</td>
		</tr>
		<tr>
			<td class="name">selectedItems</td>
			<td class="type">array</td>
			<td class="description last">parameter returns the collection of nodes and connectors that will be selected after selection change</td>
		</tr>
		<tr>
			<td class="name">cancel</td>
			<td class="type">boolean</td>
			<td class="description last">parameter to specify whether or not to cancel the selection change event</td>
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

### sizeChange
{:#events:sizechange}

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
			<td class="type">object</td>
			<td class="description last">parameter returns node that was resized</td>
		</tr>
		<tr>
			<td class="name">cancel</td>
			<td class="type">boolean</td>
			<td class="description last">parameter to cancel the size change</td>
		</tr>
		<tr>
			<td class="name">newValue</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the new width, height, offsetX and offsetY values of the element that is being resized</td>
		</tr>
		<tr>
			<td class="name">oldValue</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the previous width,height,offsetX and offsetY values of the element that is being resized</td>
		</tr>
		<tr>
			<td class="name">resizeState</td>
			<td class="type">string</td>
			<td class="description last">parameter returns the state of resizing(starting,resizing,completed)</td>
		</tr>
		<tr>
			<td class="name">offset</td>
			<td class="type">object</td>
			<td class="description last">parameter returns the difference between new and old value</td>
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

### textChange
{:#events:textchange}

Triggers when label editing is ended

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
			<td class="type">object</td>
			<td class="description last">parameter returns the node that contains the text being edited</td>
		</tr>
		<tr>
			<td class="name">value</td>
			<td class="type">string</td>
			<td class="description last">parameter returns the new text</td>
		</tr>
		<tr>
			<td class="name">keyCode</td>
			<td class="type">string</td>
			<td class="description last">parameter returns the keyCode of the key entered</td>
		</tr>
	</tbody>
</table>

#### Example

{% highlight html %}

// textChange event for diagram
$("#diagramcontent").ejDiagram({
textChange:function (args) {}
});

{% endhighlight %}
