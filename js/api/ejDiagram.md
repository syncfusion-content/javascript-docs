---
layout: post
title: ejDiagram
documentation: API
platform: js
metaname: 
metacontent: 
---

The diagram control provides 2D surface to visualize the data as shapes, lines, text and images. It can be configured to DOM element such as DIV.










$(element).ejDiagram<span class="signature">()</span>











Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="diagram"&gt;&lt;/div&gt;
&lt;script&gt;
//Create Diagram
    $("#diagram").ejDiagram();
&lt;/script&gt;</code>
</pre>






Requires
{:.require}




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








### backgroundColor<span class="type-signature type string">String</span>
{:#backgroundColor}








Color to be set as the background of the elements




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagramcontent").ejDiagram({ backgroundColor: "red"});
&lt;/script&gt;</code>
</pre>






### backgroundImage<span class="type-signature type string">String</span>
{:#backgroundImage}








Image to be set as the background of the elements




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagramcontent").ejDiagram({ backgroundImage: "Syncfusion.png"});
&lt;/script&gt;</code>
</pre>






### bridgeDirection<span class="type-signature type string">String</span>
{:#bridgeDirection}








Sets the bridge direction of connectors




Default Value:
{:.param}






* "top"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagramContent").ejDiagram({bridgeDirection: "top"} }); 
&lt;/script&gt;</code>
</pre>






### connectors<span class="type-signature type array">array</span>
{:#connectors}








Array of connector objects where each object has definition/properties of connector.




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagram"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors = [{ name: "connector" sourceNode: "node1", targetNode: "node2"}];
$("#diagram").ejDiagram({ connectors:connectors });
&lt;/script&gt;</code>
</pre>






### connectors.addInfo<span class="type-signature type object">Object</span>
{:#connectors-addInfo}








To provide/save extra information about Connector




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors = [];
var addInfo = {Name1:"Connector1",Connector2:"Connector3"}
connectors=[{addInfo: addInfo}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.bridgeSpace<span class="type-signature type integer">Integer</span>
{:#connectors-bridgeSpace}








Defines width of the line bridges




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors=[];
connectors=[{bridgeSpace:15}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.constraints<span class="type-signature type enum">enum</span>
{:#connectors-constraints}








Enables or disables the behaviors of connector see<a href="global.html#ConnectorConstraints">ConnectorConstraints</a>




Default Value:
{:.param}






* ConnectorConstraints.Default








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors = [];
connectors=[{constraints: ej.datavisualization.Diagram.ConnectorConstraints.Select}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.cornerRadius<span class="type-signature type integer">Integer</span>
{:#connectors-cornerRadius}








Defines the radius of the rounded corner




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors=[];
connectors=[{cornerRadius:2}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.horizontalAlign<span class="type-signature type horizontalalignment"><a href="global.html#HorizontalAlignment">HorizontalAlignment</a></span>
{:#connectors-horizontalAlign}








To set the horizontal alignment of connector.Applicable if the parent is group.




Default Value:
{:.param}






* HorizontalAlignment.Left








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors = [];
connectors=[{HorizontalAlignment: ej.datavisualization.Diagram.HorizontalAlignment.Left}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.labels<span class="type-signature type array">Array</span>
{:#connectors-labels}








Sets the collection of labels of connector




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>Refer nodes label for label properties details 
&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var label = [];
label = [{ "text": "Connector1", "fontColor": "Red"}];
$("#diagramcontent").ejDiagram({label:label});
&lt;/script&gt;</code>
</pre>






### connectors.lineColor<span class="type-signature type string">String</span>
{:#connectors-lineColor}








Sets the stroke color of the connector




Default Value:
{:.param}






* black








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors = [];
connectors=[{lineColor:"blue"}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.lineDashArray<span class="type-signature type string">String</span>
{:#connectors-lineDashArray}








Sets the pattern of dashes and gaps used to stroke the path of connector




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors = [];
connectors=[{lineDashArray:"4 4"}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.lineHitPadding<span class="type-signature type int">Int</span>
{:#connectors-lineHitPadding}








Defines padding set to line to ease interaction




Default Value:
{:.param}






* 10








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors= [];
connectors=[{lineHitPadding: 30}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.lineWidth<span class="type-signature type int">Int</span>
{:#connectors-lineWidth}








Sets the width of the line




Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors = [];
connectors=[{lineWidth:4}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.marginBottom<span class="type-signature type int">Int</span>
{:#connectors-marginBottom}








To set margin bottom for the connector.Applicable if the parent is group.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors = [];
connectors=[{marginBottom: 1}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.marginLeft<span class="type-signature type int">Int</span>
{:#connectors-marginLeft}








To set left margin for the connector.Applicable if the parent is group.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors = [];
connectors=[{name:"connector",marginLeft: 1}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.marginRight<span class="type-signature type int">Int</span>
{:#connectors-marginRight}








To set right margin for the connector.Applicable if the parent is group.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors = [];
connectors=[{marginRight: 1}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.marginTop<span class="type-signature type int">Int</span>
{:#connectors-marginTop}








To set top margin for the connector.Applicable if the parent is group.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors = [];
connectors=[{marginTop: 1}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.name<span class="type-signature type string">String</span>
{:#connectors-name}








Sets the name of the connector




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors = [];
connectors=[{name:"Connector1"}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.opacity<span class="type-signature type int">Int</span>
{:#connectors-opacity}








Defines the transparency of the connector




Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors = [];
connectors=[{opacity:0.6}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.parent<span class="type-signature type string">String</span>
{:#connectors-parent}








Sets the parent name of the connector




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connector = [ {name: "rect",parent:"group1"}];
&lt;/script&gt;</code>
</pre>






### connectors.segments<span class="type-signature type array">Array</span>
{:#connectors-segments}








Describes the collection of segments




Default Value:
{:.param}






* [ Segment ]








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors = [];
var point= {x:20,y:20};
connectors=[{segments: [{type:"straight",point:point}]}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.segments.direction<span class="type-signature type string">String</span>
{:#connectors-segments-direction}








Describes the direction of orthogonal segment




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors = [];
connectors=[{segments: [{type:"orthogonal",direction:"left"}]}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.segments.length<span class="type-signature type number">Number</span>
{:#connectors-segments-length}








Describes the length of orthogonal segment




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors = [];
connectors=[{segments: [{type:"orthogonal",length:20}]}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.segments.point<span class="type-signature type point">Point</span>
{:#connectors-segments-point}








Describes the end point of segment




Default Value:
{:.param}






* Diagram.Point()








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var segments = [{ type: "straight",point:{x:10,y:30}}];
connectors = [{ name: "connector1", segments: segments, sourcePoint: { x: 450, y: 150 }, targetPoint: { x: 210, y: 40 }}];
$("#diagramcontent").ejDiagram({segments:segments});
&lt;/script&gt;</code>
</pre>






### connectors.segments.point1<span class="type-signature type point">Point</span>
{:#connectors-segments-point1}








Describes the first control point of bezier segment




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors = [];
var point1={x:10,y:10}];
connectors=[{segments: [{type:"bezier", point1:point1}]}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.segments.point2<span class="type-signature type point">Point</span>
{:#connectors-segments-point2}








Describes the second control point of bezier segment




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors = [];
var point2= {x:10,y:10};
connectors=[{segments: [{type:"bezier",point2:point2}]}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.segments.type<span class="type-signature type enum">enum</span>
{:#connectors-segments-type}








Type of the segments See <a href="global.html#Segments">Segments</a>




Default Value:
{:.param}






* ej.datavisualization.Diagram.Segments.Straight








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var link=[];
link=[{segments:[{type:"straight"}]}];
$("#diagramcontent").ejDiagram({connectors:link});
&lt;/script&gt;</code>
</pre>






### connectors.segments.vector1<span class="type-signature type point">Point</span>
{:#connectors-segments-vector1}








Describes the length and angle between the first control point and start point of segment




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors = [];
var vector1= {x:20,y:20};
connectors=[{segments: [{type:"bezier",vector1:vector1}]}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.segments.vector2<span class="type-signature type point">Point</span>
{:#connectors-segments-vector2}








Describes the length and angle between the second control point and end point of segment




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors = [];
var vector2= {x:20,y:20};
connectors=[{segments: [{type:"bezier",vector2:vector2}]}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.sourceDecorator<span class="type-signature type string">String</span>
{:#connectors-sourceDecorator}








To set sourceDecorator for connector




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors = [];
var targetDecorator = { shape: "arrow", borderColor: "#606060", width: "10", height: "10" };
connectors=[{targetDecorator:targetDecorator}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.sourceDecorator.borderColor<span class="type-signature type string">String</span>
{:#connectors-sourceDecorator-borderColor}








Sets the border color of the decorator




Default Value:
{:.param}






* "black"








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var link=[];
link={[targetDecorator:{borderColor: "green"}]};
$("#diagramcontent").ejDiagram({connectors:link});
&lt;/script&gt;</code>
</pre>






### connectors.sourceDecorator.borderColor<span class="type-signature type string">String</span>
{:#connectors-sourceDecorator-borderColor}








Sets the border color of the decorator




Default Value:
{:.param}






* "black"








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var link=[];
link={[targetDecorator:{borderColor: "green"}]};
$("#diagramcontent").ejDiagram({connectors:link});
&lt;/script&gt;</code>
</pre>






### connectors.sourceDecorator.borderWidth<span class="type-signature type number">Number</span>
{:#connectors-sourceDecorator-borderWidth}








Sets the border width of the decorator




Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var link=[];
link={[targetDecorator:{borderWidth: 1}]};
$("#diagramcontent").ejDiagram({connectors:link});
&lt;/script&gt;</code>
</pre>






### connectors.sourceDecorator.fillColor<span class="type-signature type string">String</span>
{:#connectors-sourceDecorator-fillColor}








Sets the color with which the decorator is to be filled




Default Value:
{:.param}






* "black"








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var link=[];
link={[targetDecorator:{fillColor: "green"}]};
$("#diagramcontent").ejDiagram({connectors:link});
&lt;/script&gt;</code>
</pre>






### connectors.sourceDecorator.fillColor<span class="type-signature type string">String</span>
{:#connectors-sourceDecorator-fillColor}








Sets the color with which the decorator is to be filled




Default Value:
{:.param}






* "black"








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var link=[];
link={[targetDecorator:{fillColor: "green"}]};
$("#diagramcontent").ejDiagram({connectors:link});
&lt;/script&gt;</code>
</pre>






### connectors.sourceDecorator.height<span class="type-signature type number">Number</span>
{:#connectors-sourceDecorator-height}








To set the height of the connection decorator




Default Value:
{:.param}






* 8








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var link=[];
link={[targetDecorator:{height:10}]};
$("#diagramcontent").ejDiagram({connectors:link});
&lt;/script&gt;</code>
</pre>






### connectors.sourceDecorator.height<span class="type-signature type number">Number</span>
{:#connectors-sourceDecorator-height}








To set the height of the connection decorator




Default Value:
{:.param}






* 8








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var link=[];
link={[targetDecorator:{height:10}]};
$("#diagramcontent").ejDiagram({connectors:link});
&lt;/script&gt;</code>
</pre>






### connectors.sourceDecorator.pathData<span class="type-signature type string">String</span>
{:#connectors-sourceDecorator-pathData}








Path data to draw decorator with custom shape




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var link=[];
link={[targetDecorator:{pathData: "M 269.711,29.3333C 269.711,44.061 257.772,56 243.044,56z"}]};
$("#diagramcontent").ejDiagram({connectors:link});
&lt;/script&gt;</code>
</pre>






### connectors.sourceDecorator.pathData<span class="type-signature type string">String</span>
{:#connectors-sourceDecorator-pathData}








Path data to decorator with custom shape




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var link=[];
link={[targetDecorator:{pathData: "M 269.711,29.3333C 269.711,44.061 257.772,56 243.044,56z"}]};
$("#diagramcontent").ejDiagram({connectors:link});
&lt;/script&gt;</code>
</pre>






### connectors.sourceDecorator.shape<span class="type-signature type enum">enum</span>
{:#connectors-sourceDecorator-shape}








To set the decorator shape of the connector See <a href="global.html#DecoratorShapes">DecoratorShapes</a>




Default Value:
{:.param}






* ej.datavisualization.Diagram.DecoratorShapes.Arrow








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var link=[];
link={[targetDecorator:{shape:"arrow"}]};
$("#diagramcontent").ejDiagram({connectors:link});
&lt;/script&gt;</code>
</pre>






### connectors.sourceDecorator.shape<span class="type-signature type enum">enum</span>
{:#connectors-sourceDecorator-shape}








Sets the decorator shape See <a href="global.html#DecoratorShapes">DecoratorShapes</a>




Default Value:
{:.param}






* ej.datavisualization.Diagram.DecoratorShapes.Arrow








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var link=[];
link={[targetDecorator:{shape:"arrow"}]};
$("#diagramcontent").ejDiagram({connectors:link});
&lt;/script&gt;</code>
</pre>






### connectors.sourceDecorator.width<span class="type-signature type number">Number</span>
{:#connectors-sourceDecorator-width}








To set the width of the connection decorator




Default Value:
{:.param}






* 8








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var link=[];
link={[targetDecorator:{width:10}]};
$("#diagramcontent").ejDiagram({connectors:link});
&lt;/script&gt;</code>
</pre>






### connectors.sourceDecorator.width<span class="type-signature type number">Number</span>
{:#connectors-sourceDecorator-width}








To set width of the connection decorator




Default Value:
{:.param}






* 8








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var link=[];
link={[targetDecorator:{width:10}]};
$("#diagramcontent").ejDiagram({connectors:link});
&lt;/script&gt;</code>
</pre>






### connectors.sourceNode<span class="type-signature type object">Object</span>
{:#connectors-sourceNode}








Sets the sourceNode of the connector




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
var connectors = [];
nodes = {name: "openBrowses", width: 175, height: 60};
connectors=[{sourceNode: "openBrowses"}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.sourcePadding<span class="type-signature type integer">Integer</span>
{:#connectors-sourcePadding}








Defines the space between node and connector's source point




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors=[];
connectors=[{sourcePadding:5}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.sourcePoint<span class="type-signature type point">Point</span>
{:#connectors-sourcePoint}








Describes the sourcePoint of connector




Default Value:
{:.param}






* Point








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors = [];
var sourcePoint= {x:20,y:20};
connectors=[{ name: "connector1",sourcePoint: { x: 450, y: 150 }}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.sourcePort<span class="type-signature type object">Object</span>
{:#connectors-sourcePort}








Sets the sourcePort of the connector




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
var ports = [];
var connectors = [];
nodes = {name: "openBrowses", width: 175, height: 60};
ports = { offset: { x: 0, y: 0.5 }, name: "bport" };
connectors=[{sourcePort: "bport"}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.targetDecorator<span class="type-signature type string">String</span>
{:#connectors-targetDecorator}








To set targetDecorator for connector




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors = [];
var targetDecorator = { shape: "arrow", borderColor: "#606060", width: "10", height: "10" };
connectors=[{targetDecorator:targetDecorator}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.targetDecorator.borderColor<span class="type-signature type string">String</span>
{:#connectors-targetDecorator-borderColor}








Sets the border color of the decorator




Default Value:
{:.param}






* "black"








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var link=[];
link={[targetDecorator:{borderColor: "green"}]};
$("#diagramcontent").ejDiagram({connectors:link});
&lt;/script&gt;</code>
</pre>






### connectors.targetDecorator.fillColor<span class="type-signature type string">String</span>
{:#connectors-targetDecorator-fillColor}








Sets the color with which the decorator is to be filled




Default Value:
{:.param}






* "black"








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var link=[];
link={[targetDecorator:{fillColor: "green"}]};
$("#diagramcontent").ejDiagram({connectors:link});
&lt;/script&gt;</code>
</pre>






### connectors.targetDecorator.height<span class="type-signature type number">Number</span>
{:#connectors-targetDecorator-height}








To set the height of the decorator




Default Value:
{:.param}






* 8








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var link=[];
link={[targetDecorator:{height:10}]};
$("#diagramcontent").ejDiagram({connectors:link});
&lt;/script&gt;</code>
</pre>






### connectors.targetDecorator.pathData<span class="type-signature type string">String</span>
{:#connectors-targetDecorator-pathData}








Path data to draw decorator with custom shape




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var link=[];
link={[targetDecorator:{pathData: "M 269.711,29.3333C 269.711,44.061 257.772,56 243.044,56z"}]};
$("#diagramcontent").ejDiagram({connectors:link});
&lt;/script&gt;</code>
</pre>






### connectors.targetDecorator.shape<span class="type-signature type enum">enum</span>
{:#connectors-targetDecorator-shape}








To set the shape of the decorator in connector See <a href="global.html#DecoratorShapes">DecoratorShapes</a>




Default Value:
{:.param}






* ej.datavisualization.Diagram.DecoratorShapes.Arrow








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var link=[];
link={[targetDecorator:{shape:"arrow"}]};
$("#diagramcontent").ejDiagram({connectors:link});
&lt;/script&gt;</code>
</pre>






### connectors.targetDecorator.width<span class="type-signature type number">Number</span>
{:#connectors-targetDecorator-width}








To set the width of the decorator




Default Value:
{:.param}






* 8








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var link=[];
link={[targetDecorator:{width:10}]};
$("#diagramcontent").ejDiagram({connectors:link});
&lt;/script&gt;</code>
</pre>






### connectors.targetNode<span class="type-signature type object">Object</span>
{:#connectors-targetNode}








Sets the target node of the connector




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes =[];
var connectors = [];
nodes = {name: "openBrowses", width: 175, height: 60};
connectors=[{targetNode: "openBrowses"}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.targetPadding<span class="type-signature type integer">Integer</span>
{:#connectors-targetPadding}








Defines the space between node and connector's target point




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors=[];
connectors=[{targetPadding:5}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.targetPoint<span class="type-signature type point">Point</span>
{:#connectors-targetPoint}








Describes the targetPoint of connector




Default Value:
{:.param}






* Point








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors = [];
var targetPoint= {x:20,y:20};
connectors=[{ name: "connector1",targetPoint: { x: 450, y: 150 }}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.targetPort<span class="type-signature type object">Object</span>
{:#connectors-targetPort}








Sets the targetPort of the connector




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
var ports = [];
var connectors = [];
nodes = {name: "openBrowses", width: 175, height: 60};
ports = { offset: { x: 0, y: 0.5 }, name: "aport" };
connectors=[{targetPort: "aport"}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.verticalAlign<span class="type-signature type verticalalignment"><a href="global.html#VerticalAlignment">VerticalAlignment</a></span>
{:#connectors-verticalAlign}








To set the vertical alignment of connector.Applicable if the parent is group.




Default Value:
{:.param}






* VerticalAlignment.Top








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors = [];
connectors=[{VerticalAlignment: ej.datavisualization.Diagram.VerticalAlignment.Top}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.visible<span class="type-signature type boolean">Boolean</span>
{:#connectors-visible}








Enables or disables the visibility of connector




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors = [];
connectors=[{visible: true}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectors.zOrder<span class="type-signature type int">Int</span>
{:#connectors-zOrder}








Sets the Zorder of the connector




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors= [];
connectors=[{connectors: 1}];
$("#diagramcontent").ejDiagram({connectors:connectors});
&lt;/script&gt;</code>
</pre>






### connectorTemplate<span class="type-signature type object">object</span>
{:#connectorTemplate}








To customize the connector properties before rendering the connector.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagram"&gt;&lt;/div&gt;
&lt;script&gt;
function connectorTemplate(diagram, connector, data) {connector.labels[0].text = data.Name};
$("#diagram").ejDiagram({ connectorTemplate:connectorTemplate});
&lt;/script&gt;</code>
</pre>






### constraints<span class="type-signature type enum">enum</span>
{:#constraints}








Sets the default behavior of the diagram see <a href="global.html#DiagramConstraints">DiagramConstraints</a>




Default Value:
{:.param}






* constraints.All








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagramContent").ejDiagram({constraints: ej.datavisualization.Diagram.DiagramConstraints.Default} }); 
&lt;/script&gt;</code>
</pre>






### contextMenu
{:#contextMenu}








Object to customize context menu behavior of diagram











### contextMenu.items<span class="type-signature type object">Object</span>
{:#contextMenu-items}








To define the collection of context menu items




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
//Collection of  items
var menucollection = [{ "name": "hyperLink", "text": "Hyperlink", "image": "", "style": "" }];
var contextMenu = { items: menucollection};
$("#diagramContent").ejDiagram({contextMenu: contextMenu}); 
&lt;/script&gt;</code>
</pre>






### contextMenu.showCustomMenuItemsOnly<span class="type-signature type boolean">Boolean</span>
{:#contextMenu-showCustomMenuItemsOnly}








To set whether to display the default context menu items or not




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagramcontent").ejDiagram({showCustomMenuItemsOnly: true});
&lt;/script&gt;</code>
</pre>






### dataSourceSettings
{:#dataSourceSettings}








Object to set dataSource to diagram











### dataSourceSettings.dataSource<span class="type-signature type object">object</span>
{:#dataSourceSettings-dataSource}








Describes data source either as a collection of objects or an instance of ej.DataManager




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagram"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagram").ejDiagram({ dataSourceSettings: {dataSource: localData}});
&lt;/script&gt;</code>
</pre>






### dataSourceSettings.id<span class="type-signature type string">String</span>
{:#dataSourceSettings-id}








Describes the unique id of data source items.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagram"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagram").ejDiagram({ dataSourceSettings: {id: "CategoryID"}});
&lt;/script&gt;</code>
</pre>






### dataSourceSettings.parent<span class="type-signature type string">String</span>
{:#dataSourceSettings-parent}








Describes the parent id of data source items.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagram"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagram").ejDiagram({ dataSourceSettings: { parent: "reportingPerson"}});
&lt;/script&gt;</code>
</pre>






### dataSourceSettings.query<span class="type-signature type object">object</span>
{:#dataSourceSettings-query}








Describes query to retrieve a set of data from the specified datasource.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagram"&gt;&lt;/div&gt;
&lt;script&gt;
query: ej.Query().from("Categories").select("CategoryID,CategoryName").take(3);
&lt;/script&gt;</code>
</pre>






### dataSourceSettings.root<span class="type-signature type string">String</span>
{:#dataSourceSettings-root}








Describes the root node.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagram"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagram").ejDiagram({ dataSourceSettings: { root: "1"}});
&lt;/script&gt;</code>
</pre>






### dataSourceSettings.tablename<span class="type-signature type string">String</span>
{:#dataSourceSettings-tablename}








Describes the name of the table on which the specified query to be executed




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagram"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagram").ejDiagram({ dataSourceSettings:{tableName: "Categories"}});
&lt;/script&gt;</code>
</pre>






### defaultSettings<span class="type-signature type object">object</span>
{:#defaultSettings}








To set the default values to nodes and connector properties




Default Value:
{:.param}






* {}








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagram"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagram").ejDiagram({ defaultSettings: { node:  {width: 110, height: 40, fillColor:"skyblue"}}});
&lt;/script&gt;</code>
</pre>






### defaultSettings.connector<span class="type-signature type object">object</span>
{:#defaultSettings-connector}








To set the default values to connector properties




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagram"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagram").ejDiagram({ defaultSettings:{ connector:{ lineColor: "gray", lineWidth: 2 }}});
&lt;/script&gt;</code>
</pre>






### defaultSettings.node<span class="type-signature type object">object</span>
{:#defaultSettings-node}








To set the default values to node properties




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagram"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagram").ejDiagram({ defaultSettings:{node: { fillColor: "#83A93F", borderColor: "#000000" }}});
&lt;/script&gt;</code>
</pre>






### drawingTools<span class="type-signature type object">Object</span>
{:#drawingTools}








Describes the interactive features to be performed




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagramcontent").ejDiagram({ drawingTools: {textTool: ej.datavisualization.Diagram.TextTool()}});
&lt;/script&gt;</code>
</pre>






### drawType<span class="type-signature type object">Object</span>
{:#drawType}








Sets the type of Json object to be drawn through drawing tool




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagramcontent").ejDiagram({drawType:{type:"node"}});
&lt;/script&gt;</code>
</pre>






### enableAutoScroll<span class="type-signature type boolean">Boolean</span>
{:#enableAutoScroll}








Enables or disables Auto scroll in diagram




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagramcontent").ejDiagram({enableAutoScroll: true});
&lt;/script&gt;</code>
</pre>






### enableContextMenu<span class="type-signature type boolean">Boolean</span>
{:#enableContextMenu}








Enables or disables diagram context menu




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagramcontent").ejDiagram({enableContextMenu: true});
&lt;/script&gt;</code>
</pre>






### height<span class="type-signature type string">string</span>
{:#height}








Specifies the height of the diagram.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagram"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagram").ejDiagram({ height:"100%" });
&lt;/script&gt;</code>
</pre>






### layout
{:#layout}








To arrange the diagram elements on page











### layout. fixedNode<span class="type-signature type string">String</span>
{:#layout-}








Sets the fixed node with respect to which the layout will be aligned




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
//fixedNode of the layout
$("#diagramContent").ejDiagram({layout: { fixedNode: "nodename"}}); </code>
</pre>






### layout. getLayoutInfo<span class="type-signature type object">object</span>
{:#layout-}








To customize the orientation of trees/sub trees For orientations see <a href="global.html#ChartOrientations">ChartOrientations</a> For chart types see <a href="global.html#ChartTypes">ChartTypes</a>




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagram"&gt;&lt;/div&gt;
&lt;script&gt;
function getLayoutInfo(diagram, node, options) { options.orientation = "vertical"; options.type = "left"; offset = 10;};
$("#diagram").ejDiagram({layout: { getLayoutInfo:getLayoutInfo } });
&lt;/script&gt;</code>
</pre>






### layout. marginY<span class="type-signature type number">Number</span>
{:#layout-}








Sets the margin value to be vertically left between layout and diagram




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
// marginY of the layout
$("#diagramContent").ejDiagram({layout: { marginY: 0}}); </code>
</pre>






### layout.horizontalSpacing<span class="type-signature type number">Number</span>
{:#layout-horizontalSpacing}








Sets the space to be horizontally left between nodes




Default Value:
{:.param}






* 30








Example
{:.example}

<pre class="prettyprint">
<code> 
//horizontalSpacing of the layout
$("#diagramContent").ejDiagram({layout: {horizontalSpacing: 30}}); </code>
</pre>






### layout.marginX<span class="type-signature type number">Number</span>
{:#layout-marginX}








Sets the margin value to be horizontally left between layout and diagram




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
//marginX of the layout
$("#diagramContent").ejDiagram({layout: {marginX: 0}}); </code>
</pre>






### layout.orientation<span class="type-signature type string">String</span>
{:#layout-orientation}








Sets the orientation/direction to arrange the diagram elements see <a href="global.html#LayoutOrientations">LayoutOrientations</a>




Default Value:
{:.param}






* "topToBottom"








Example
{:.example}

<pre class="prettyprint">
<code> 
//orientation of the layout
$("#diagramContent").ejDiagram({layout: {orientation: "topToBottom"}}); </code>
</pre>






### layout.type<span class="type-signature type string">String</span>
{:#layout-type}








Sets the type of the layout based on which the elements will be arranged




Default Value:
{:.param}






* "none"








Example
{:.example}

<pre class="prettyprint">
<code> 
//type of the layout
$("#diagramContent").ejDiagram({layout: {type: "none"}}); </code>
</pre>






### layout.verticalSpacing<span class="type-signature type number">Number</span>
{:#layout-verticalSpacing}








Sets the space to be vertically left between nodes




Default Value:
{:.param}






* 30








Example
{:.example}

<pre class="prettyprint">
<code> 
//verticalSpacing of the layout
$("#diagramContent").ejDiagram({layout: {verticalSpacing: 30}}); </code>
</pre>






### locale<span class="type-signature type string">String</span>
{:#locale}








To define the current culture of diagram




Default Value:
{:.param}






* "en-US"








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagramcontent").ejDiagram({locale: "en-US"});
&lt;/script&gt;</code>
</pre>






### nodes<span class="type-signature type array">array</span>
{:#nodes}








Array of node objects where each object has definition/properties of node.




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagram"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [{ name: "node", width: 175, height: 60}];
$("#diagram").ejDiagram({ nodes:nodes });
&lt;/script&gt;</code>
</pre>






### nodes.activity<span class="type-signature type enum">enum</span>
{:#nodes-activity}








Sets the type of BPMN Activity See <a href="global.html#BPMNActivity">BPMNActivity</a>




Default Value:
{:.param}






* ej.datavisualization.Diagram.BPMNActivity.Task








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{type: "bpmn", shape: ej.datavisualization.Diagram.BPMNShapes.Activity, activity: ej.datavisualization.Diagram.BPMNActivity.SubProcess}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.addInfo<span class="type-signature type object">Object</span>
{:#nodes-addInfo}








To provide/save extra information about Node




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
var addInfo = {Name1:"Node1",Name2:"Name2"}
nodes=[{addInfo: addInfo}];
$("#diagramcontent").ejDiagram({nodes:nodes});
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane",{addInfo: addInfo}}});
&lt;/script&gt;</code>
</pre>






### nodes.allowDrop<span class="type-signature type boolean">Boolean</span>
{:#nodes-allowDrop}








To indicate whether this element can be used as the target of a drop operation. Applicable if the type is group.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{name:"GroupNode",allowDrop:true}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.borderColor<span class="type-signature type string">String</span>
{:#nodes-borderColor}








Sets the border color of node




Default Value:
{:.param}






* "black"








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{borderColor: "black"}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.borderDashArray<span class="type-signature type string">String</span>
{:#nodes-borderDashArray}








The pattern of dashes and gaps to stroke the border




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{borderDashArray: "2 2"}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.borderWidth<span class="type-signature type number">Number</span>
{:#nodes-borderWidth}








Sets the border width of the node




Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{borderWidth: 3}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.canUngroup<span class="type-signature type boolean">Boolean</span>
{:#nodes-canUngroup}








To set whether the group can be ungrouped or not




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
var children = ["Node1","Node2"];
nodes=[{name:"GroupNode",children:children,canUngroup:false}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.children<span class="type-signature type array">Array</span>
{:#nodes-children}








Collection of children of the group node




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
var children = ["Node1","Node2"];
nodes=[{name:"GroupNode",children:children}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.collection<span class="type-signature type boolean">Boolean</span>
{:#nodes-collection}








To set whether the BPMN dataobject is a collection or not




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{type: "bpmn", shape:"dataObject", collection: false}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.connectorPadding<span class="type-signature type int">Int</span>
{:#nodes-connectorPadding}








To set the distance to be left between the node and connections.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
node={name:"node1",connectorPadding: 2};
$("#diagramcontent").ejDiagram({nodes:[node]});
&lt;/script&gt;</code>
</pre>






### nodes.constraints<span class="type-signature type enum">enum</span>
{:#nodes-constraints}








To enable or disable the default behaviors of the node see<a href="global.html#NodeConstraints">NodeConstraints</a>




Default Value:
{:.param}






* NodeConstraints.Default








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{Constraints: ej.datavisualization.Diagram.NodeConstraints.Select}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.constraints<span class="type-signature type enum">enum</span>
{:#nodes-constraints}








To set the constraints for the swimlane see <a href="global.html#NodeConstraints">NodeConstraints</a> ej.datavisualization.Diagram.NodeConstraints.Default &amp; ~(ej.datavisualization.Diagram.NodeConstraints.ResizeNorth | ej.datavisualization.Diagram.NodeConstraints.ResizeWest | ej.datavisualization.Diagram.NodeConstraints.ResizeNorthWest | ej.datavisualization.Diagram.NodeConstraints.ResizeNorthEast | ej.datavisualization.Diagram.NodeConstraints.ResizeSouthWest)





Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes = [ {type: "swimlane",name: "swimlane",constraints: ej.datavisualization.Diagram.NodeConstraints.Connect}
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.container<span class="type-signature type obj">obj</span>
{:#nodes-container}








To indicate whether this element can be used as a container.Applicable only if the object as Group.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{name:"GroupNode",container:{}}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.container.orientation<span class="type-signature type string">string</span>
{:#nodes-container-orientation}








To set the container orientation. Applicable if the group has container.




Default Value:
{:.param}






* "vertical"








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var container = ej.datavisualization.Diagram.ContainerType.Canvas
container.orientation = "vertical"; 
var nodes = [{name:"Node1",container : container}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.container.type<span class="type-signature type enum">enum</span>
{:#nodes-container-type}








To set the type of the container. Applicable if the group has container.




Default Value:
{:.param}






* ej.datavisualization.Diagram.ContainerType.Canvas








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var container = ej.datavisualization.Diagram.ContainerType.Canvas
container.type = "linear; 
var nodes = [{name:"Node1",container : container}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.cornerRadius<span class="type-signature type integer">Integer</span>
{:#nodes-cornerRadius}








Defines the radius of the rounder corner. Applicable if the shape is rectangle




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node={[shape:{type:"rectangle",cornerRadius:2}]};
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.event<span class="type-signature type enum">enum</span>
{:#nodes-event}








Sets the type of BPMN Event See <a href="global.html#BPMNEvents">BPMNEvents</a>




Default Value:
{:.param}






* ej.datavisualization.Diagram.BPMNEvents.Start








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{type: "bpmn", shape: ej.datavisualization.Diagram.BPMNShapes.Event, event: ej.datavisualization.Diagram.BPMNEvents.Start}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.excludeFromLayout<span class="type-signature type boolean">Boolean</span>
{:#nodes-excludeFromLayout}








To set whether the node can be included in layout arrangement




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{visible: true}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.expanded<span class="type-signature type boolean">Boolean</span>
{:#nodes-expanded}








To set whether the node is expanded or collapsed




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{isExpanded: true}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.fillColor<span class="type-signature type string">String</span>
{:#nodes-fillColor}








Sets the color that is used to fill shapes




Default Value:
{:.param}






* "White"








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{fillColor: "white"}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.gateway<span class="type-signature type enum">enum</span>
{:#nodes-gateway}








Sets the type of BPMN Gateway See <a href="global.html#BPMNGateways">BPMNGateways</a>




Default Value:
{:.param}






* ej.datavisualization.Diagram.BPMNGateways.None








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{type: "bpmn", shape: ej.datavisualization.Diagram.BPMNShapes.Gateway, gateway: ej.datavisualization.Diagram.BPMNGateways.None}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.gradient
{:#nodes-gradient}








Smooth transition from one color to another color in node











### nodes.gradient.LinearGradient<span class="type-signature type object">object</span>
{:#nodes-gradient-LinearGradient}








Paints an area with a linear gradient.











### nodes.gradient.LinearGradient.stops<span class="type-signature type array">Array</span>
{:#nodes-gradient-LinearGradient-stops}








The stop region for the gradient




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var gradient = ej.datavisualization.Diagram.LinearGradientDefaults();
gradient.type = "linear;
gradient.x1 = 10;
gradient.x2 = 50;
gradient.y1 = 20;
gradient.y2 = 50;
var stop = ej.datavisualization.Diagram.Stop();
stop.color = "white";
stop.opacity = 0.8;
stop.offset = 0;
gradient.stops.push(stop);
stop = ej.datavisualization.Diagram.Stop();
stop.color = "darkCyan";
stop.offset = 100;
gradient.stops.push(stop);
gradient.stops.push(stop);
var nodes = [{name:"Node1",width: 100,height: 100,gradient : gradient}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.gradient.LinearGradient.x1<span class="type-signature type int">Int</span>
{:#nodes-gradient-LinearGradient-x1}








The starting X-Axis for the region




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var gradient = ej.datavisualization.Diagram.LinearGradientDefaults();
gradient.type = "linear;
gradient.x1 = 10;
gradient.x2 = 50;
gradient.y1 = 0;
gradient.y2 = 50;
var nodes = [{name:"Node1",width: 100,height: 100,gradient : gradient}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.gradient.LinearGradient.x2<span class="type-signature type int">Int</span>
{:#nodes-gradient-LinearGradient-x2}








The ending X-Axis for the region




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var gradient = ej.datavisualization.Diagram.LinearGradientDefaults();
gradient.type = "linear;
gradient.x1 = 10;
gradient.x2 = 50;
gradient.y1 = 20;
gradient.y2 = 50;
var nodes = [{name:"Node1",width: 100,height: 100,gradient : gradient}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.gradient.LinearGradient.y1<span class="type-signature type int">Int</span>
{:#nodes-gradient-LinearGradient-y1}








The starting Y-Axis for the region




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var gradient = ej.datavisualization.Diagram.LinearGradientDefaults();
gradient.type = "linear;
gradient.x1 = 10;
gradient.x2 = 50;
gradient.y1 = 0;
gradient.y2 = 50;
var nodes = [{name:"Node1",width: 100,height: 100,gradient : gradient}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.gradient.LinearGradient.y2<span class="type-signature type int">Int</span>
{:#nodes-gradient-LinearGradient-y2}








The ending Y-Axis for the region




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var gradient = ej.datavisualization.Diagram.LinearGradientDefaults();
gradient.type = "linear;
gradient.x1 = 10;
gradient.x2 = 50;
gradient.y1 = 0;
gradient.y2 = 50;
var nodes = [{name:"Node1",width: 100,height: 100,gradient : gradient}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.gradient.RadialGradient<span class="type-signature type object">object</span>
{:#nodes-gradient-RadialGradient}








Paints an area with a radial gradient. A focal point defines the beginning of the gradient, and a circle defines the end point of the gradient.











### nodes.gradient.RadialGradient.cx<span class="type-signature type int">Int</span>
{:#nodes-gradient-RadialGradient-cx}








The starting X-Axis for the region




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var gradient = ej.datavisualization.Diagram.RadialGradientDefaults();
gradient.type = "linear;
gradient.cx = 20;
gradient.cy = 50;
gradient.fx = 20;
gradient.fy = 50;
var nodes = [{name:"Node1",width: 100,height: 100,gradient : gradient}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.gradient.RadialGradient.cy<span class="type-signature type int">Int</span>
{:#nodes-gradient-RadialGradient-cy}








The ending X-Axis for the region




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var gradient = ej.datavisualization.Diagram.RadialGradientDefaults();
gradient.type = "linear;
gradient.cx = 20;
gradient.cy = 50;
gradient.fx = 20;
gradient.fy = 50;
var nodes = [{name:"Node1",width: 100,height: 100,gradient : gradient}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.gradient.RadialGradient.fx<span class="type-signature type int">Int</span>
{:#nodes-gradient-RadialGradient-fx}








The starting X-Axis for the region




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var gradient = ej.datavisualization.Diagram.RadialGradientDefaults();
gradient.type = "linear;
gradient.cx = 20;
gradient.cy = 50;
gradient.fx = 20;
gradient.fy = 50;
var nodes = [{name:"Node1",width: 100,height: 100,gradient : gradient}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.gradient.RadialGradient.fy<span class="type-signature type int">Int</span>
{:#nodes-gradient-RadialGradient-fy}








The ending Y-Axis for the region




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var gradient = ej.datavisualization.Diagram.RadialGradientDefaults();
gradient.type = "linear;
gradient.cx = 20;
gradient.cy = 50;
gradient.fx = 20;
gradient.fy = 50;
var nodes = [{name:"Node1",width: 100,height: 100,gradient : gradient}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.gradient.RadialGradient.stops<span class="type-signature type array">Array</span>
{:#nodes-gradient-RadialGradient-stops}








The stop region for the gradient




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var gradient = ej.datavisualization.Diagram.RadialGradientDefaults();
gradient.type = "linear;
gradient.x1 = 10;
gradient.x2 = 50;
gradient.y1 = 20;
gradient.y2 = 50;
var stop = ej.datavisualization.Diagram.Stop();
stop.color = "white";
stop.opacity = 0.8;
stop.offset = 0;
gradient.stops.push(stop);
stop = ej.datavisualization.Diagram.Stop();
stop.color = "darkCyan";
stop.offset = 100;
gradient.stops.push(stop);
gradient.stops.push(stop);
var nodes = [{name:"Node1",width: 100,height: 100,gradient : gradient}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.gradient.Stop<span class="type-signature type object">object</span>
{:#nodes-gradient-Stop}








Specifies the stops of the node gradients.











### nodes.gradient.Stop.color<span class="type-signature type string">String</span>
{:#nodes-gradient-Stop-color}








The color of applied gradient




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var gradient = ej.datavisualization.Diagram.LinearGradientDefaults();
gradient.type = "linear;
gradient.x1 = 0;
gradient.x2 = 50;
gradient.y1 = 0;
gradient.y2 = 50;
var stop = ej.datavisualization.Diagram.Stop();
stop.color = "white";
stop.offset = 0;
gradient.stops.push(stop);
stop = ej.datavisualization.Diagram.Stop();
stop.color = "darkCyan";
stop.offset = 100;
gradient.stops.push(stop);
gradient.stops.push(stop);
var nodes = [{name:"Node1",width: 100,height: 100,gradient : gradient}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.gradient.Stop.offset<span class="type-signature type int">Int</span>
{:#nodes-gradient-Stop-offset}








To set desired offset to apply color to the node region




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var gradient = ej.datavisualization.Diagram.LinearGradientDefaults();
gradient.type = "linear;
gradient.x1 = 0;
gradient.x2 = 50;
gradient.y1 = 0;
gradient.y2 = 50;
var stop = ej.datavisualization.Diagram.Stop();
stop.color = "white";
stop.offset = 0;
gradient.stops.push(stop);
stop = ej.datavisualization.Diagram.Stop();
stop.color = "darkCyan";
stop.offset = 100;
gradient.stops.push(stop);
gradient.stops.push(stop);
var nodes = [{name:"Node1",width: 100,height: 100,gradient : gradient}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.gradient.Stop.opacity<span class="type-signature type int">Int</span>
{:#nodes-gradient-Stop-opacity}








Decribes the transparency level for the region




Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var gradient = ej.datavisualization.Diagram.LinearGradientDefaults();
gradient.type = "linear;
gradient.x1 = 0;
gradient.x2 = 50;
gradient.y1 = 0;
gradient.y2 = 50;
var stop = ej.datavisualization.Diagram.Stop();
stop.color = "white";
stop.opacity = 0.8;
stop.offset = 0;
gradient.stops.push(stop);
stop = ej.datavisualization.Diagram.Stop();
stop.color = "darkCyan";
stop.offset = 100;
gradient.stops.push(stop);
gradient.stops.push(stop);
var nodes = [{name:"Node1",width: 100,height: 100,gradient : gradient}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.header<span class="type-signature type obj">obj</span>
{:#nodes-header}








The header of the swimlane. Applicable if the type is group.




Default Value:
{:.param}






* "Null"








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane",  header: {text: "Header", width:50}}});
&lt;/script&gt;</code>
</pre>






### nodes.height<span class="type-signature type int">Int</span>
{:#nodes-height}








To set the height of the node




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{height: 100}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.horizontalAlign<span class="type-signature type horizontalalignment"><a href="global.html#HorizontalAlignment">HorizontalAlignment</a></span>
{:#nodes-horizontalAlign}








To set the horizontal alignment of node. Applicable if the type is group.




Default Value:
{:.param}






* HorizontalAlignment.Left








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt; 
node={name:"node1", ej.datavisualization.Diagram.HorizontalAlignment.Left};
$("#diagramcontent").ejDiagram({nodes:[node]});
&lt;/script&gt;</code>
</pre>






### nodes.inEdges<span class="type-signature type array">Array</span>
{:#nodes-inEdges}








Collection of incoming connectors/edges of the node




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors = [{ name: "connector1", sourceNode: "Node1", targetNode: "Node2"}];
nodes=[{inEdges:connectors}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.isSwimlane<span class="type-signature type boolean">Boolean</span>
{:#nodes-isSwimlane}








Indicates class as swimlane. Applicable if type is swimlane.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt; 
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane",  isSwimlane: true}});
&lt;/script&gt;</code>
</pre>






### nodes.labels<span class="type-signature type array">Array</span>
{:#nodes-labels}








To set the collection of labels to node




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var label = [];
label = { "text": "Node1", "fontColor": "Red"};
nodes=[{labels:label}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.labels.bold<span class="type-signature type boolean">Boolean</span>
{:#nodes-labels-bold}








Enables/disables the bold style of label




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node=[{labels:{"bold": false}}];
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.labels.borderColor<span class="type-signature type string">String</span>
{:#nodes-labels-borderColor}








Sets border color of the text




Default Value:
{:.param}






* "transparent"








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node=[{labels:{borderColor: "transparent"}}];
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.labels.borderWidth<span class="type-signature type number">Number</span>
{:#nodes-labels-borderWidth}








Sets the border width of the label




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node=[{labels:{borderWidth: 4}}];
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.labels.fillColor<span class="type-signature type string">String</span>
{:#nodes-labels-fillColor}








Sets the color that is used to fill text




Default Value:
{:.param}






* "transparent"








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node=[{labels:{fillColor: "green"}}];
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.labels.fontColor<span class="type-signature type string">String</span>
{:#nodes-labels-fontColor}








To set the text color




Default Value:
{:.param}






* "black"








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node=[{labels:{"fontColor": "black"}}];
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.labels.fontFamily<span class="type-signature type string">String</span>
{:#nodes-labels-fontFamily}








To set the font family of the label




Default Value:
{:.param}






* "arial"








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node=[{labels:{"fontFamily": "Arial"}}];
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.labels.fontSize<span class="type-signature type integer">Integer</span>
{:#nodes-labels-fontSize}








To set font size of the label




Default Value:
{:.param}






* 12








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node=[{labels:{"fontSize": 12}}];
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.labels.horizontalAlignment<span class="type-signature type enum">Enum</span>
{:#nodes-labels-horizontalAlignment}








Horizontal alignment of text in an element see<a href="global.html#HorizontalAlignment">HorizontalAlignment</a>




Default Value:
{:.param}






* HorizontalAlignment.Center








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node=[{labels:{horizontalAlignment: ej.datavisualization.Diagram.HorizontalAlignment.Center}}];
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.labels.italic<span class="type-signature type boolean">Boolean</span>
{:#nodes-labels-italic}








Enables/disables the italic font style of label




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node=[{labels:{"italic": false}}];
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.labels.margin<span class="type-signature type object">Object</span>
{:#nodes-labels-margin}








To set the margin of the label




Default Value:
{:.param}






* ej.datavisualization.Diagram.Margin()








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node=[{labels:{"margin": ej.datavisualization.Diagram.Margin()}}];
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.labels.mode<span class="type-signature type enum">Enum</span>
{:#nodes-labels-mode}








To set the label edit mode see<a href="global.html#LabelEditMode">LabelEditMode</a>




Default Value:
{:.param}






* LabelEditMode.Edit








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node=[{labels:{mode: ej.datavisualization.Diagram.LabelEditMode.Edit}}];
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.labels.name<span class="type-signature type string">String</span>
{:#nodes-labels-name}








Name of the label




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node=[{labels:{name:"Label"}}];
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.labels.offset<span class="type-signature type point">Point</span>
{:#nodes-labels-offset}








Ratio with respect to which the label is to be placed




Default Value:
{:.param}






* Point(0.5, 0.5)








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node=[{labels:{offset: ej.datavisualization.Diagram.Point(0.5, 0.5)}}];
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.labels.readOnly<span class="type-signature type boolean">Boolean</span>
{:#nodes-labels-readOnly}








Allows the label to be read only




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node=[{labels:{"readOnly": false}}];
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.labels.rotateAngle<span class="type-signature type number">Number</span>
{:#nodes-labels-rotateAngle}








To set the rotation angle of the label




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node=[{labels:{rotateAngle: 90}}];
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.labels.text<span class="type-signature type string">String</span>
{:#nodes-labels-text}








Sets text for the label




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node=[{labels:{"text": "Label"}}];
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.labels.textAlign<span class="type-signature type enum">Enum</span>
{:#nodes-labels-textAlign}








Alignment of text in an element see <a href="global.html#TextAlign">TextAlign</a>




Default Value:
{:.param}






* TextAlign.Center








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node=[{labels:{textAlign: ej.datavisualization.Diagram.TextAlign.Center}}];
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.labels.textDecoration<span class="type-signature type enum">Enum</span>
{:#nodes-labels-textDecoration}








To set the text decoration for the label see<a href="global.html#TextDecorations">TextDecorations</a>




Default Value:
{:.param}






* TextDecorations.None








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node=[{labels:{textDecoration: ej.datavisualization.Diagram.TextDecorations.Underline}}];
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.labels.verticalAlignment<span class="type-signature type enum">Enum</span>
{:#nodes-labels-verticalAlignment}








Vertical alignment of text in an element see<a href="global.html#VerticalAlignment">VerticalAlignment</a>




Default Value:
{:.param}






* VerticalAlignment.Center








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node=[{labels:{verticalAlignment: ej.datavisualization.Diagram.VerticalAlignment.Center}}];
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.labels.visible<span class="type-signature type boolean">Boolean</span>
{:#nodes-labels-visible}








Enables or disables the visibility of the label




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node=[{labels:{visible: true}}];
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.labels.width<span class="type-signature type interger">Interger</span>
{:#nodes-labels-width}








To set the width of the label




Default Value:
{:.param}






* 50








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node=[{labels:{width: 50}}];
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.labels.wrapping<span class="type-signature type enum">Enum</span>
{:#nodes-labels-wrapping}








To set the wrapping behavior of text see <a href="global.html#TextWrapping">TextWrapping</a>




Default Value:
{:.param}






* TextWrapping.WrapWithOverflow








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node=[{labels:{wrapping: ej.datavisualization.Diagram.TextWrapping.Wrap}}];
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.lanes<span class="type-signature type array">Array</span>
{:#nodes-lanes}








Collection of Lanes in swimlane. Applicable if type is swimlane.




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var lanes = []; 
lanes=[{["Lane1","Lane1"]}];
$("#diagramcontent").ejDiagram( );
var nodes = [ {type: "swimlane",name: "swimlane",lanes: []}
&lt;/script&gt;</code>
</pre>






### nodes.lanes.addInfo<span class="type-signature type object">Object</span>
{:#nodes-lanes-addInfo}








To provide/save extra information about Lane




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagramcontent").ejDiagram({nodes:{type: "lane",name: "lane",{addInfo: addInfo}}});
&lt;/script&gt;</code>
</pre>






### nodes.lanes.children<span class="type-signature type array">Array</span>
{:#nodes-lanes-children}








The children of the lane. Applicable if type is lane.




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", lanes:[{children:[]}]}});
&lt;/script&gt;</code>
</pre>






### nodes.lanes.fillColor<span class="type-signature type string">String</span>
{:#nodes-lanes-fillColor}








The color to be filled inside the lane. Applicable if type is lane.




Default Value:
{:.param}






* "White"








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", lanes:[{fillColor: "white"}]}});
&lt;/script&gt;</code>
</pre>






### nodes.lanes.header<span class="type-signature type obj">obj</span>
{:#nodes-lanes-header}








The header of the lane . Applicable if the type is group.




Default Value:
{:.param}






* "Null"








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", lanes:[{header: {text: "Header", width:50}}]}});
&lt;/script&gt;</code>
</pre>






### nodes.lanes.isLane<span class="type-signature type boolean">Boolean</span>
{:#nodes-lanes-isLane}








Indicates class as lane. Applicable if type is lane.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt; 
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", lanes:[{isLane:true}]}});
&lt;/script&gt;</code>
</pre>






### nodes.lanes.labels<span class="type-signature type string">String</span>
{:#nodes-lanes-labels}








The label shown inside the lane. Applicable if type is lane.




Default Value:
{:.param}






* "White"








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", lanes:[{labels: [{text:"Label"}]}]}});
&lt;/script&gt;</code>
</pre>






### nodes.lanes.name<span class="type-signature type string">String</span>
{:#nodes-lanes-name}








The name of the lane. Applicable if type is lane.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", lanes:[{name:"lane"}]}});
&lt;/script&gt;</code>
</pre>






### nodes.lanes.orientation<span class="type-signature type string">String</span>
{:#nodes-lanes-orientation}








The orientation type of the lane. Applicable if type is lane.




Default Value:
{:.param}






* "vertical"








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", lanes:[{orientation:"horizontal"}]}});
&lt;/script&gt;</code>
</pre>






### nodes.marginBottom<span class="type-signature type int">Int</span>
{:#nodes-marginBottom}








To set bottom margin of the node. Applicable if the type is group.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
node={name:"node1",marginBottom: 1};
$("#diagramcontent").ejDiagram({nodes:[node]});
&lt;/script&gt;</code>
</pre>






### nodes.marginLeft<span class="type-signature type int">Int</span>
{:#nodes-marginLeft}








To set left margin of the node. Applicable if the type is group.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{marginLeft: 1}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.marginRight<span class="type-signature type int">Int</span>
{:#nodes-marginRight}








To set right of for the node. Applicable if the type is group.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
node={name:"node1",marginRight: 1};
$("#diagramcontent").ejDiagram({nodes:[node]});
&lt;/script&gt;</code>
</pre>






### nodes.marginTop<span class="type-signature type int">Int</span>
{:#nodes-marginTop}








To set top margin of the node. Applicable if the type is group.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
node={name:"node1",marginTop: 1};
$("#diagramcontent").ejDiagram({nodes:[node]});
&lt;/script&gt;</code>
</pre>






### nodes.maxHeight<span class="type-signature type int">Int</span>
{:#nodes-maxHeight}








To set maximum height for the node. Applicable if the type is group.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
node={name:"node1",maxHeight: 1};
$("#diagramcontent").ejDiagram({nodes:[node]});
&lt;/script&gt;</code>
</pre>






### nodes.maxWidth<span class="type-signature type int">Int</span>
{:#nodes-maxWidth}








To set maximum width for the node. Applicable if the type is group.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
node={name:"node1",maxWidth: 1};
$("#diagramcontent").ejDiagram({nodes:[node]});
&lt;/script&gt;</code>
</pre>






### nodes.minHeight<span class="type-signature type int">Int</span>
{:#nodes-minHeight}








To set minimum height for the node. Applicable if the type is group.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
node={name:"node1",minHeight: 1};
$("#diagramcontent").ejDiagram({nodes:[node]});
&lt;/script&gt;</code>
</pre>






### nodes.minWidth<span class="type-signature type int">Int</span>
{:#nodes-minWidth}








To set minimum width for the node. Applicable if the type is group.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
node={name:"node1",minWidth: 1};
$("#diagramcontent").ejDiagram({nodes:[node]});
&lt;/script&gt;</code>
</pre>






### nodes.name<span class="type-signature type string">String</span>
{:#nodes-name}








To set the name to the node




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{name:"Node1"}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.offsetX<span class="type-signature type int">Int</span>
{:#nodes-offsetX}








Sets the position of the node on X-Axis




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{offsetX: 100}];
$("#diagramcontent").ejDiagram({nodes:nodes});
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane",offsetX:100}});
&lt;/script&gt;</code>
</pre>






### nodes.offsetY<span class="type-signature type int">Int</span>
{:#nodes-offsetY}








Sets the position of the node on Y-Axis




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{offsetY: 100}];
$("#diagramcontent").ejDiagram({nodes:nodes});          
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane",offsetY:100}});
&lt;/script&gt;</code>
</pre>






### nodes.opacity<span class="type-signature type number">Number</span>
{:#nodes-opacity}








Defines the transparency of the node




Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{opacity: 2}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.orientation<span class="type-signature type string">String</span>
{:#nodes-orientation}








The orientation type of the swimlane. Applicable if type is swimlane.




Default Value:
{:.param}






* "vertical"








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane",  orientation: "vertical"}});
&lt;/script&gt;</code>
</pre>






### nodes.outEdges<span class="type-signature type array">Array</span>
{:#nodes-outEdges}








Collection of outgoing connectors/edges of the node




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var connectors = [{ name: "connector1", sourceNode: "Node1", targetNode: "Node2"}];
nodes=[{outEdges:connectors}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.paddingBottom<span class="type-signature type int">Int</span>
{:#nodes-paddingBottom}








To set bottom padding value to the group. Applicable if the type is group.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{paddingBottom: 1}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.paddingLeft<span class="type-signature type int">Int</span>
{:#nodes-paddingLeft}








To set left padding value to the group. Applicable if the type is group.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{paddingLeft: 1}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.paddingRight<span class="type-signature type int">Int</span>
{:#nodes-paddingRight}








To set Right padding value to the group. Applicable if the type is group.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{paddingRight: 1}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.paddingTop<span class="type-signature type int">Int</span>
{:#nodes-paddingTop}








To set Top padding value to the group. Applicable if the type is group.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{paddingTop: 1}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.parent<span class="type-signature type string">String</span>
{:#nodes-parent}








Sets the parent name of the node




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node = [ {name: "rect",parent:"group1"}];
&lt;/script&gt;</code>
</pre>






### nodes.pathData<span class="type-signature type string">String</span>
{:#nodes-pathData}








Sets the path geometry that defines the shape of the path node




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node={[shape:{type:"path",pathData:"M 269.711,29.3333C 269.711,44.061 257.772,56 243.044,56L 158.058,56C 143.33z"}]};
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.phases<span class="type-signature type array">Array</span>
{:#nodes-phases}








Collection of phases in swimlane node. Applicable if type is swimlane.




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var phases = []; 
phases=[{["phase1","phase2"]}];
$("#diagramcontent").ejDiagram( );
var nodes = [ {type: "swimlane",name: "swimlane",phases: []}
&lt;/script&gt;</code>
</pre>






### nodes.phases.label<span class="type-signature type obj">obj</span>
{:#nodes-phases-label}








Sets the label of the phase. Applicable if type is lane.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", phases:[{label:{text:"label"}}]}});
&lt;/script&gt;</code>
</pre>






### nodes.phases.lineColor<span class="type-signature type string">String</span>
{:#nodes-phases-lineColor}








Sets the line color of the phase. Applicable if type is lane.




Default Value:
{:.param}






* "#606060"








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", phases:[{lineColor: "#606060"}]}});
&lt;/script&gt;</code>
</pre>






### nodes.phases.lineDashArray<span class="type-signature type string">String</span>
{:#nodes-phases-lineDashArray}








Sets the line dash drray of the phase. Applicable if type is lane.




Default Value:
{:.param}






* "3,3"








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", phases:[{lineDashArray: "3,3"}]}});
&lt;/script&gt;</code>
</pre>






### nodes.phases.lineWidth<span class="type-signature type int">Int</span>
{:#nodes-phases-lineWidth}








Sets the line width of the phase. Applicable if type is lane.




Default Value:
{:.param}






* "1"








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", phases:[{lineWidth: 1}]}});
&lt;/script&gt;</code>
</pre>






### nodes.phases.name<span class="type-signature type string">String</span>
{:#nodes-phases-name}








Defines the name of the phase. Applicable if type is lane.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", phases:[{name:"lane"}]}});
&lt;/script&gt;</code>
</pre>






### nodes.phases.offset<span class="type-signature type int">Int</span>
{:#nodes-phases-offset}








Sets the offset of the phase. Applicable if type is lane.




Default Value:
{:.param}






* "0"








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", phases:[{offset: 100}]}});
&lt;/script&gt;</code>
</pre>






### nodes.phases.orientation<span class="type-signature type string">String</span>
{:#nodes-phases-orientation}








Sets the orientation of the phase. Applicable if type is lane.




Default Value:
{:.param}






* "horizontal"








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", phases:[{orientation: "horizontal"}]}});
&lt;/script&gt;</code>
</pre>






### nodes.phases.parent<span class="type-signature type string">String</span>
{:#nodes-phases-parent}








Sets the parent of the phase. Applicable if type is lane.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", phases:[{parent: "parent"}]}});
&lt;/script&gt;</code>
</pre>






### nodes.phases.type<span class="type-signature type string">String</span>
{:#nodes-phases-type}








Sets the type of the phase. Applicable if type is lane.




Default Value:
{:.param}






* "phase"








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", phases:[{type: "phase"}]}});
&lt;/script&gt;</code>
</pre>






### nodes.phaseSize<span class="type-signature type int">Int</span>
{:#nodes-phaseSize}








To set phase size for the swimlane. Applicable if type is swimlane.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt; 
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane",phaseSize:100}});
&lt;/script&gt;</code>
</pre>






### nodes.pivot<span class="type-signature type point">Point</span>
{:#nodes-pivot}








To set the pivot point of the node




Default Value:
{:.param}






* Points(0.5,0.5)








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{pivot: ej.datavisualization.Diagram.Point(0.8, 0.8)}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.points<span class="type-signature type array">Array</span>
{:#nodes-points}








Defines the collection of points to draw polygon node




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node={[shape: { type: "polygon", points:[{ x: 0, y: 12.5 }, { x: 0, y: 50 }, { x: 50, y: 50 }, { x: 50, y: 0 }, { x: 12.5, y: 0 }, { x: 0, y: 12.5 }]}]};
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.ports<span class="type-signature type array">Array</span>
{:#nodes-ports}








To add collection of ports to node




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var port: [{ offset: { x: 0, y: 0.5 }, name: "aport" }]
nodes=[{ports:port}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.ports.borderColor<span class="type-signature type string">String</span>
{:#nodes-ports-borderColor}








Sets the border color of the port




Default Value:
{:.param}






* "#1a1a1a"








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node={ports:[{borderColor:"green"}]};
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.ports.borderWidth<span class="type-signature type number">Number</span>
{:#nodes-ports-borderWidth}








Sets the border width of the port




Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node={ports:[{borderWidth: 1}]};
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.ports.connectorPadding<span class="type-signature type int">Int</span>
{:#nodes-ports-connectorPadding}








To set the distance to be left between the port and connections.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node = [{ports:[{connectorPadding:2}]}];
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.ports.constraints<span class="type-signature type enum">enum</span>
{:#nodes-ports-constraints}








Sets whether connections can be created with the port See <a href="global.html#PortConstraints">PortConstraints</a>




Default Value:
{:.param}






* PortConstraints.Connect








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node={ports:[{constraints: ej.datavisualization.Diagram.PortConstraints.Connect}]};
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.ports.fillColor<span class="type-signature type string">String</span>
{:#nodes-ports-fillColor}








Sets the color that is used to fill port shapes




Default Value:
{:.param}






* "white"








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node={ports:[{fillColor:"green"}]};
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.ports.name;<span class="type-signature type string">String</span>
{:#nodes-ports-name;}








The name of port to be specified




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node={ports:[{ name: "port"}]};
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.ports.offset<span class="type-signature type point">Point</span>
{:#nodes-ports-offset}








Offset value to align the port




Default Value:
{:.param}






* Point(0, 0)








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node={ports:[{{ x: 0, y: 0.5 }}]};
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.ports.pathData<span class="type-signature type string">String</span>
{:#nodes-ports-pathData}








Path data to draw the custom port




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node={ports:[{pathData:""}]};
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.ports.shape<span class="type-signature type enum">enum</span>
{:#nodes-ports-shape}








Sets the shape of the port See <a href="global.html#PortShapes">PortShapes</a>




Default Value:
{:.param}






* PortShapes.Square








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node={ports:[{shape: ej.datavisualization.Diagram.PortShapes.Square}]};
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.ports.size<span class="type-signature type number">Number</span>
{:#nodes-ports-size}








Sets the size of the port




Default Value:
{:.param}






* 8








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node={ports:[{size: 10}]};
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.ports.visibility<span class="type-signature type enum">enum</span>
{:#nodes-ports-visibility}








Enables or disables the visibility of port See <a href="global.html#PortVisibility">PortVisibility</a>




Default Value:
{:.param}






* PortVisibility.Default








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node={ports:[{visibility: ej.datavisualization.Diagram.PortVisibility.Default}]};
$("#diagramcontent").ejDiagram({nodes:port});
&lt;/script&gt; </code>
</pre>






### nodes.rotateAngle<span class="type-signature type number">Number</span>
{:#nodes-rotateAngle}








To set the rotation angle of the node




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{rotateAngle: 120}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.shadow<span class="type-signature type object">Object</span>
{:#nodes-shadow}








To define the shadow behavior of node seeShadow




Default Value:
{:.param}






* Diagram.Shadow()








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[shadow:{distance: 5,angle:45,opacity:0.7}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.shadow.angle<span class="type-signature type integer">Integer</span>
{:#nodes-shadow-angle}








Defines the angle difference to be set between object and shadow




Default Value:
{:.param}






* 45








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node={[shadow:{angle:50}]};
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.shadow.distance<span class="type-signature type integer">Integer</span>
{:#nodes-shadow-distance}








Defines the distance to be left between object and shadow




Default Value:
{:.param}






* 5








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node={[shadow:{distance:7}]};
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.shadow.opacity<span class="type-signature type float">float</span>
{:#nodes-shadow-opacity}








Defines the opacity of the shadow




Default Value:
{:.param}






* 0.7








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node={[shadow:{opacity:0.9}]};
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.shape<span class="type-signature type enum">Enum</span>
{:#nodes-shape}








Sets the shape of the node. It depends upon the type of node. See {Link Shapes}




Default Value:
{:.param}






* "rectangle"








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[shape: "rectangle"}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.source<span class="type-signature type string">String</span>
{:#nodes-source}








Sets the source location of the image node




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node={[shape:{type:"image",source:"Syncfusion.png"}]};
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.subProcess<span class="type-signature type object">object</span>
{:#nodes-subProcess}








Defines the subProcess of BPMN Activity and it is applicable, if the Activity type is "subProcess"




Default Value:
{:.param}






* Diagram.BPMNSubProcess()








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{type: "bpmn", activity: "subProcess", subProcess:{loop: ej.datavisualization.Diagram.BPMNLoops.Standard}}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.subProcess.adhoc<span class="type-signature type boolean">Boolean</span>
{:#nodes-subProcess-adhoc}








To set whether the process is adhoc or not




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{type: "bpmn", activity: "task", subProcess:{adhoc: false}}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.subProcess.boundary<span class="type-signature type enum">enum</span>
{:#nodes-subProcess-boundary}








Sets the boundary of the BPMN process See <a href="global.html#BPMNBoundary">BPMNBoundary</a>




Default Value:
{:.param}






* ej.datavisualization.Diagram.BPMNBoundary.Default








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{type: "bpmn", activity: "task", subProcess:{boundary: ej.datavisualization.Diagram.BPMNBoundary.Default}}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.subProcess.compensation<span class="type-signature type boolean">Boolean</span>
{:#nodes-subProcess-compensation}








To set whether the process is a compensation process or not




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{type: "bpmn", activity: "task", subProcess:{compensation: false}}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.subProcess.loop<span class="type-signature type enum">enum</span>
{:#nodes-subProcess-loop}








Sets the type of loop to a BPMN Process See <a href="global.html#BPMNLoops">BPMNLoops</a>




Default Value:
{:.param}






* ej.datavisualization.Diagram.BPMNLoops.None








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{type: "bpmn", activity: "task", subProcess:{loop: ej.datavisualization.Diagram.BPMNLoops.Standard}}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.task<span class="type-signature type object">object</span>
{:#nodes-task}








Defines the task of BPMN Activity and it is applicable, if Activity type is "task"




Default Value:
{:.param}






* Diagram.BPMNTask()








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{type: "bpmn", activity: "task", task:{loop: ej.datavisualization.Diagram.BPMNLoops.Standard}}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.tasks.call<span class="type-signature type boolean">Boolean</span>
{:#nodes-tasks-call}








To set whether the task is a global task or not




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{type: "bpmn", activity: "task", task:{call: false}}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.tasks.compensation<span class="type-signature type boolean">Boolean</span>
{:#nodes-tasks-compensation}








To set whether the task is a compensation task or not




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{type: "bpmn", activity: "task", task:{compensation: false}}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.tasks.loop<span class="type-signature type enum">enum</span>
{:#nodes-tasks-loop}








Sets the type of loop to a BPMN task See <a href="global.html#BPMNLoops">BPMNLoops</a>




Default Value:
{:.param}






* ej.datavisualization.Diagram.BPMNLoops.None








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{type: "bpmn", activity: "task", task:{loop: ej.datavisualization.Diagram.BPMNLoops.Standard}}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.tasks.type<span class="type-signature type enum">enum</span>
{:#nodes-tasks-type}








Sets the type of the BPMN task See <a href="global.html#BPMNTasks">BPMNTasks</a>




Default Value:
{:.param}






* ej.datavisualization.Diagram.BPMNTasks.None








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{type: "bpmn", activity: "task", task:{type: ej.datavisualization.Diagram.BPMNTasks.Service}}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.templateId<span class="type-signature type string">string</span>
{:#nodes-templateId}








Sets the template id of native/html nodes




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[]; 
node={[shape: { type: "text", templateId: "templateId" }]};
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.textBlock<span class="type-signature type integer">Integer</span>
{:#nodes-textBlock}








Defines the textBlock and it is applicable in case of text node




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
var textBlock = ej.datavisualization.Diagram.TextBlockDefaults;
textBlock.text = "TextNode";
node={[shape: { type: "text", textBlock: textBlock }]};
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.trigger<span class="type-signature type enum">enum</span>
{:#nodes-trigger}








Sets the type of BPMN Event Trigger See <a href="global.html#BPMNTriggers">BPMNTriggers</a>




Default Value:
{:.param}






* ej.datavisualization.Diagram.BPMNTriggers.None








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{type: "bpmn", shape: ej.datavisualization.Diagram.BPMNShapes.Event, trigger: ej.datavisualization.Diagram.BPMNTriggers.None}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.type<span class="type-signature type enum">enum</span>
{:#nodes-type}








The type of node See <a href="global.html#Shapes">Shapes</a>




Default Value:
{:.param}






* ej.datavisualization.Diagram.Shapes.Basic








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var node=[];
node={[shape:{type:"rectangle"}]};
$("#diagramcontent").ejDiagram({nodes:node});
&lt;/script&gt;</code>
</pre>






### nodes.vertical Align<span class="type-signature type verticalalignment"><a href="global.html#VerticalAlignment">VerticalAlignment</a></span>
{:#nodes-vertical}








To set the Vertical alignment of node. Applicable if the type is group.




Default Value:
{:.param}






* VerticalAlignment.Top








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
node={name:"node1",VerticalAlignment: ej.datavisualization.Diagram.VerticalAlignment.Top};
$("#diagramcontent").ejDiagram({nodes:[node]});
&lt;/script&gt;</code>
</pre>






### nodes.visible<span class="type-signature type boolean">Boolean</span>
{:#nodes-visible}








To set the visibility of the node




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{visible: true}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.width<span class="type-signature type int">Int</span>
{:#nodes-width}








To set the width of the node




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{width: 100}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodes.zOrder<span class="type-signature type int">Int</span>
{:#nodes-zOrder}








To set the Zorder of the node




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var nodes = [];
nodes=[{zOrder: 1}];
$("#diagramcontent").ejDiagram({nodes:nodes});
&lt;/script&gt;</code>
</pre>






### nodeTemplate<span class="type-signature type object">object</span>
{:#nodeTemplate}








To customize the node properties before rendering the node.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagram"&gt;&lt;/div&gt;
&lt;script&gt;
function nodeTemplate(diagram, node) {node.labels[0].text = node.Name};
$("#diagram").ejDiagram({ nodeTemplate:nodeTemplate});
&lt;/script&gt;</code>
</pre>






### pageSettings
{:#pageSettings}








To define the page settings of diagram











### pageSettings.multiplePage<span class="type-signature type boolean">Boolean</span>
{:#pageSettings-multiplePage}








To set whether the number of pages can be extended based on the region covered by elements




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//multiplePage of the diagram
$("#diagramContent").ejDiagram({pageSettings: {multiplePage: false}}); </code>
</pre>






### pageSettings.pageBackgroundColor<span class="type-signature type string">String</span>
{:#pageSettings-pageBackgroundColor}








To set the background color of page




Default Value:
{:.param}






* "#ffffff"








Example
{:.example}

<pre class="prettyprint">
<code> 
//pageBackgroundColor of the diagram
$("#diagramContent").ejDiagram({pageSettings: {pageBackgroundColor: "#ffffff"}}); </code>
</pre>






### pageSettings.pageBorderColor<span class="type-signature type string">String</span>
{:#pageSettings-pageBorderColor}








To set the border color of page




Default Value:
{:.param}






* "#565656"








Example
{:.example}

<pre class="prettyprint">
<code> 
//pageBorderColor of the diagram
$("#diagramContent").ejDiagram({pageSettings: {pageBorderColor: "#565656"}}); </code>
</pre>






### pageSettings.pageBorderWidth<span class="type-signature type number">Number</span>
{:#pageSettings-pageBorderWidth}








To set the border width of the page




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
//pageBorderWidth of the diagram
$("#diagramContent").ejDiagram({pageSettings: {pageBorderWidth: 3}}); </code>
</pre>






### pageSettings.pageHeight<span class="type-signature type number">Number</span>
{:#pageSettings-pageHeight}








To set the height of the page




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
//pageHeight of the diagram
$("#diagramContent").ejDiagram({pageSettings: {pageHeight: 4500}}); </code>
</pre>






### pageSettings.pageMargin<span class="type-signature type number">Number</span>
{:#pageSettings-pageMargin}








To set the margin of page




Default Value:
{:.param}






* 24








Example
{:.example}

<pre class="prettyprint">
<code> 
//pageMargin of the diagram
$("#diagramContent").ejDiagram({pageSettings: {pageMargin: 24}}); </code>
</pre>






### pageSettings.pageWidth<span class="type-signature type number">Number</span>
{:#pageSettings-pageWidth}








To set the width of the page




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
//pageWidth
$("#diagramContent").ejDiagram({pageSettings: {pageWidth: 4500}}); </code>
</pre>






### pageSettings.showPageBreak<span class="type-signature type boolean">Boolean</span>
{:#pageSettings-showPageBreak}








Enables or disables the page breaks in diagram




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//showPageBreak of the diagram
$("#diagramContent").ejDiagram({pageSettings: {showPageBreak: false}}); </code>
</pre>






### selectedItems<span class="type-signature type object">object</span>
{:#selectedItems}








The object to define the behavior of the selected items











### selectedItems.constraints<span class="type-signature type enum">enum</span>
{:#selectedItems-constraints}








Sets the visible items of selector see <a href="global.html#SelectorConstraints">SelectorConstraints</a>




Default Value:
{:.param}






* SelectorConstraints.All








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagramContent").ejDiagram({selectedItems:{constraints: ej.datavisualization.Diagram.SelectorConstraints.None} }}); 
&lt;/script&gt;</code>
</pre>






### selectedItems.height<span class="type-signature type number">Number</span>
{:#selectedItems-height}








Sets the height of the selected items




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
$("#diagramContent").ejDiagram({selectedItems: {height: 50}}); </code>
</pre>






### selectedItems.offsetX<span class="type-signature type number">Number</span>
{:#selectedItems-offsetX}








Defines the X co-ordinate of the selected item




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
$("#diagramContent").ejDiagram({selectedItems: {offsetX: 50}}); </code>
</pre>






### selectedItems.offsetY<span class="type-signature type number">Number</span>
{:#selectedItems-offsetY}








Defines the Y co-ordinate of the selected item




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
$("#diagramContent").ejDiagram({selectedItems: {offsetY: 50}}); </code>
</pre>






### selectedItems.rotateAngle<span class="type-signature type number">Number</span>
{:#selectedItems-rotateAngle}








Sets the rotation angle of the selected items.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
$("#diagramContent").ejDiagram({selectedItems: {rotateAngle: 50}}); </code>
</pre>






### selectedItems.userHandles<span class="type-signature type array">array</span>
{:#selectedItems-userHandles}








To add frequently using commands around selector




Default Value:
{:.param}






* []








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var userHandle= [];
function createUserHandles() {
var cloneHandle = ej.datavisualization.Diagram.UserHandle();
userhandle.push(cloneHandles);
}
$("#diagramcontent").ejDiagram({selectedItems:{userHandles:userHandle}});
&lt;/script&gt;</code>
</pre>






### selectedItems.width<span class="type-signature type number">Number</span>
{:#selectedItems-width}








Sets the width of the selected items




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
$("#diagramContent").ejDiagram({selectedItems: {width: 50}}); </code>
</pre>






### showTooltip<span class="type-signature type boolean">Boolean</span>
{:#showTooltip}








Enables or disables tooltip of diagram




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagramcontent").ejDiagram({showTooltip: true});
&lt;/script&gt;</code>
</pre>






### snapSettings<span class="type-signature type object">object</span>
{:#snapSettings}








Specifies the snap settings of the diagram.











### snapSettings.enableSnapToObject<span class="type-signature type boolean">Boolean</span>
{:#snapSettings-enableSnapToObject}








Enables or disables the snap to object




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
var snap = {"enableSnapToObject":true};
//enableSnapToObject: 
$("#diagramContent").ejDiagram({snapSettings: snap}); </code>
</pre>






### snapSettings.horizontalGridLines<span class="type-signature type object">object</span>
{:#snapSettings-horizontalGridLines}








Specifies the settings of horizontal grid lines.











### snapSettings.horizontalGridLines.lineColor<span class="type-signature type string">string</span>
{:#snapSettings-horizontalGridLines-lineColor}








Sets the line color for horizontal gridlines




Default Value:
{:.param}






* "lightgray"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var gridline = { "snapConstraints":"lineColor": "blue" };
//Linecolor of the horizontal gridlines
$("#diagramContent").ejDiagram({snapSettings: { horizontalGridLines: gridline} }); 
&lt;/script&gt;</code>
</pre>






### snapSettings.horizontalGridLines.lineDashArray<span class="type-signature type string">string</span>
{:#snapSettings-horizontalGridLines-lineDashArray}








Specifies the pattern of dashes and gaps used to stroke horizontal grid lines




Default Value:
{:.param}






* "0"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="diagram"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagram").ejDiagram({ snapSettings: { horizontalGridLines: { lineDashArray: "2 2"}}}); 
&lt;/script&gt;</code>
</pre>






### snapSettings.horizontalGridLines.linesInterval<span class="type-signature type array">array</span>
{:#snapSettings-horizontalGridLines-linesInterval}








Specifies pattern of lines and gaps of horizontal gridlines




Default Value:
{:.param}






* [1.25, 18.75, 0.25, 19.75, 0.25, 19.75, 0.25, 19.75, 0.25, 19.75]








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagram"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagram").ejDiagram({ snapSettings: { 
    horizontalGridLines: { linesInterval: [1, 14, 0.25, 15, 0.25, 15, 0.25, 15, 0.25, 15] }
}}); 
&lt;/script&gt;</code>
</pre>






### snapSettings.horizontalGridLines.snapInterval<span class="type-signature type array">array</span>
{:#snapSettings-horizontalGridLines-snapInterval}








Specifies the snap intervals of horizontal grid lines.




Default Value:
{:.param}






* [20]








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="diagram"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagram").ejDiagram({ snapSettings: { horizontalGridLines: { snapInterval: [10] }}}); 
&lt;/script&gt;</code>
</pre>






### snapSettings.snapAngle<span class="type-signature type number">Number</span>
{:#snapSettings-snapAngle}








The Angle by which the object to be snapped




Default Value:
{:.param}






* 5








Example
{:.example}

<pre class="prettyprint">
<code> 
var snap = {"snapAngle":5};
//enableSnapToObject: 
$("#diagramContent").ejDiagram({snapSettings: snap}); </code>
</pre>






### snapSettings.snapObjectDistance<span class="type-signature type number">Number</span>
{:#snapSettings-snapObjectDistance}








Relative distance between the nearer object and selected object




Default Value:
{:.param}






* 5








Example
{:.example}

<pre class="prettyprint">
<code> 
var snap = {"snapObjectDistance":5};
//snapObjectDistance
$("#diagramContent").ejDiagram({snapSettings: snap}); </code>
</pre>






### snapSettings.verticalGridLines<span class="type-signature type object">object</span>
{:#snapSettings-verticalGridLines}








Specifies the settings of vertical grid lines.











### snapSettings.verticalGridLines.lineColor<span class="type-signature type string">string</span>
{:#snapSettings-verticalGridLines-lineColor}








Sets the line color of vertical gridlines




Default Value:
{:.param}






* "lightgray"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var gridline = { "snapConstraints":"lineColor": "blue" };
//Linecolor of the vertical gridlines
$("#diagramContent").ejDiagram({snapSettings: { verticalGridLines: gridline} });
&lt;/script&gt;</code>
</pre>






### snapSettings.verticalGridLines.lineDashArray<span class="type-signature type string">string</span>
{:#snapSettings-verticalGridLines-lineDashArray}








Specifies the pattern of dashes and gaps used to stroke vertical grid lines




Default Value:
{:.param}






* "0"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="diagram"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagram").ejDiagram({ snapSettings: { verticalGridLines: { lineDashArray: "2 2"}}}); 
&lt;/script&gt;</code>
</pre>






### snapSettings.verticalGridLines.linesInterval<span class="type-signature type array">array</span>
{:#snapSettings-verticalGridLines-linesInterval}








Specifies pattern of lines and gaps of vertical gridlines




Default Value:
{:.param}






* [1.25, 18.75, 0.25, 19.75, 0.25, 19.75, 0.25, 19.75, 0.25, 19.75]








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagram"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagram").ejDiagram({ snapSettings: { 
    verticalGridLines: { linesInterval: [1, 14, 0.25, 15, 0.25, 15, 0.25, 15, 0.25, 15] }
}}); 
&lt;/script&gt;</code>
</pre>






### snapSettings.verticalGridLines.snapInterval<span class="type-signature type array">array</span>
{:#snapSettings-verticalGridLines-snapInterval}








Specifies the snap intervals for vertical grid lines.




Default Value:
{:.param}






* [20]








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="diagram"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagram").ejDiagram({ snapSettings: { verticalGridLines: { snapInterval: [10] }}}); 
&lt;/script&gt;</code>
</pre>






### tool<span class="type-signature type enum">enum</span>
{:#tool}








Sets the default behavior of the diagram see<a href="global.html#Tool">Tool</a>




Default Value:
{:.param}






* Tool.All








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagramContent").ejDiagram({tool: ej.datavisualization.Diagram.Tool.Default} }); 
&lt;/script&gt;</code>
</pre>






### tooltipTemplateId<span class="type-signature type string">String</span>
{:#tooltipTemplateId}








To set custom style for tool tip of diagram




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>         
&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script type="text/x-jsrender" id="toolTipId"&gt;
&lt;span &gt;{{:offsetX}}{{:x}}{{:offsetY}}{{:y}}
&lt;/span&gt;
&lt;/script&gt;
&lt;script&gt;
$("#diagramcontent").ejDiagram({ tooltipTemplateId: "toolTipId"});
&lt;/script&gt;</code>
</pre>






### version<span class="type-signature type string">String</span>
{:#version}








Sets the version of the diagram




Default Value:
{:.param}






* "13.1"








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagramcontent").ejDiagram("instance");
&lt;/script&gt;</code>
</pre>






### width<span class="type-signature type string">string</span>
{:#width}








Specifies the width of the diagram.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagram"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagram").ejDiagram({ width:"100%" });
&lt;/script&gt;</code>
</pre>






### zoomFactor<span class="type-signature type number">Number</span>
{:#zoomFactor}








Sets the factor by which we can zoom in or zoom out




Default Value:
{:.param}






* 0.2








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
$("#diagramContent").ejDiagram({zoomFactor: 1}); 
&lt;/script&gt;</code>
</pre>




## Methods








### activateTool<span class="signature">(toolName, singleAction)</span>
{:#activateTool}








To activate the tool specified by toolName

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
<td class="name"><code>toolName</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">name of the tool to be activated</td>
</tr>
<tr>
<td class="name"><code>singleAction</code></td>
<td class="type"><span class="param-type">Boolean</span></td>
<td class="description last">default value set to true tool action to be performed only once</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.activateTool("panTool");
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");                 
diagram.activateTool("orthogonalTool",false);
&lt;/script&gt;</code>
</pre>






### add<span class="signature">(node)</span>
{:#add}








Add the specified node/connector to diagram

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
<td class="name"><code>node</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">pass node/connector to be added</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
var node = [];
node=[{ name: "node", width: 175, height: 60, offsetX: 400, offsetY: 60, type: "Rectangle"];
diagram.add(node);
&lt;/script&gt;</code>
</pre>






### addPhase<span class="signature">(name, options)</span>
{:#addPhase}








Add a phase to the group specified by name

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
<td class="name"><code>name</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">of the group to add the phase</td>
</tr>
<tr>
<td class="name"><code>options</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">to define the phase to be added</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance"); 
diagram.addPhase("swimlane", { name: "CustomPhase", offset: 600, label: { text: "CustomPhase" } });
&lt;/script&gt;</code>
</pre>






### addPorts<span class="signature">(name, ports)</span>
{:#addPorts}








Add the collection of ports to the node specified by name

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
<td class="name"><code>name</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">to identify the object from the model</td>
</tr>
<tr>
<td class="name"><code>ports</code></td>
<td class="type"><span class="param-type">array</span></td>
<td class="description last">collection of ports to be added to the node</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>        
&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram = $("#diagramcontent").ejDiagram("instance");
var port = [{ offset: { x: 0, y: 0.5 }, name: "aport", fillColor: "yellow"}, { offset: { x: 0.5, y: 0.5 }, name: "bport", fillColor: "yellow",  }];
diagram.addPorts("Rect1", port);
&lt;/script&gt;</code>
</pre>






### addSelection<span class="signature">(node)</span>
{:#addSelection}








Select the node specified in the argument

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
<td class="name"><code>node</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">pass target node to be selected</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
var node=diagram.model.nodes[0];
diagram.addSelection(node);
&lt;/script&gt;</code>
</pre>






### align<span class="signature">(direction)</span>
{:#align}








Align selected objects based on reference object and direction

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
<td class="name"><code>direction</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">To specify the driection for alignment ("left","right",top","bottom")</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.align("left"); 
&lt;/script&gt;</code>
</pre>






### bringIntoView<span class="signature">(bounds)</span>
{:#bringIntoView}








To bring the specified portion of the diagram content to the diagram viewport

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
<td class="name"><code>bounds</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">pass bounds value (x,y,height,width)</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.bringIntoView(ej.datavisualization.Diagram.Rectangle(700, 500, 80, 80));
&lt;/script&gt;</code>
</pre>






### bringToCenter<span class="signature">(rect)</span>
{:#bringToCenter}








To bring the specified portion of the diagram content to center of the diagram viewport

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
<td class="name"><code>rect</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">pass bounds value (x,y,height,width)</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.bringToCenter(ej.datavisualization.Diagram.Rectangle(700, 500, 80, 80));
&lt;/script&gt;</code>
</pre>






### bringToFront<span class="signature">()</span>
{:#bringToFront}








Move the selected object over all other intersected objects





Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.bringToFront(); 
&lt;/script&gt;</code>
</pre>






### clear<span class="signature">()</span>
{:#clear}








Remove all the elements from diagram





Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.clear(); 
&lt;/script&gt;</code>
</pre>






### copy<span class="signature">()</span>
{:#copy}








Copy the selected object to internal clipboard





Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.copy(); 
&lt;/script&gt;</code>
</pre>






### cut<span class="signature">()</span>
{:#cut}








Cut the selected object from diagram to diagram internal clipboard





Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.cut(); 
&lt;/script&gt;</code>
</pre>






### deactivateTool<span class="signature">()</span>
{:#deactivateTool}








Deactivate the current activated tool





Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.deactivateTool();
&lt;/script&gt;</code>
</pre>






### exportDiagram<span class="signature">(options)</span>
{:#exportDiagram}








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
<td class="name"><code>options</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">to export the desired region of diagram to the desired formats
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
<td class="name"><code>fileName</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">name of the file to be downloaded</td>
</tr>
<tr>
<td class="name"><code>format</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">format of the exported file/data See <a href="global.html#FileFormats">FileFormats</a></td>
</tr>
<tr>
<td class="name"><code>mode</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">to set whether to export diagram as a file or as raw data See <a href="global.html#ExportModes">ExportModes</a></td>
</tr>
<tr>
<td class="name"><code>region</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">to set the region of the diagram to be exported See <a href="global.html#Region">Region</a></td>
</tr>
<tr>
<td class="name"><code>bounds</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">to set the custom bounds of the diagram to be exported</td>
</tr>
<tr>
<td class="name"><code>margin</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">to set margin to the exported data</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
//To export the positive region of diagram as an image of JPEG format
var diagram=$("#diagramcontent").ejDiagram("instance");
var options = { mode: "download", region: "pageSettings", format: "jpg",
             bounds:{x:0,y:0}, margin:{left:30}};
diagram.exportDiagram(options);
&lt;/script&gt;</code>
</pre>






### fitToPage<span class="signature">(mode, region, margin)</span>
{:#fitToPage}








Fit the diagram content into diagram viewport

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
<td class="name"><code>mode</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">to set the mode of fit to command. See <a href="global.html#FitMode">FitMode</a></td>
</tr>
<tr>
<td class="name"><code>region</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">to set whether the region to be fit will be based on diagram elements or page settings <a href="global.html#Region">Region</a></td>
</tr>
<tr>
<td class="name"><code>margin</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">to set the required margin</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>         
&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.fitToPage(mode,region,margin);
&lt;/script&gt;</code>
</pre>






### group<span class="signature">()</span>
{:#group}








Group the selected nodes and connectors





Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.group(); 
&lt;/script&gt;</code>
</pre>






### layout<span class="signature">()</span>
{:#layout}








Refresh the diagram with the specified layout

<table class="params">
<thead>
<tr>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="type"><span class="param-type">String</span></td>
<td class="description last"></td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.layout();
&lt;/script&gt;</code>
</pre>






### load<span class="signature">(data)</span>
{:#load}








Load the diagram .

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
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last"></td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.load(data);
&lt;/script&gt;</code>
</pre>






### moveForward<span class="signature">()</span>
{:#moveForward}








Increase the Z-index value of selected object by 1





Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.moveForward(); 
&lt;/script&gt;</code>
</pre>






### nudge<span class="signature">(direction, delta)</span>
{:#nudge}








Executes nudge command to move selected node/connector by one pixel/specified pixes

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
<td class="name"><code>direction</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">specifies the driection to move the selected objects ("left","right",top","bottom")</td>
</tr>
<tr>
<td class="name"><code>delta</code></td>
<td class="type"><span class="param-type">Number</span></td>
<td class="description last">specifies the number of pixels by which the selected objects to be moved</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.nudge("direction", 5); 
&lt;/script&gt;</code>
</pre>






### paste<span class="signature">()</span>
{:#paste}








Paste the selected object from internal clipboard to diagram





Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.paste(); 
&lt;/script&gt;</code>
</pre>






### print<span class="signature">()</span>
{:#print}








Print the diagram as image .





Example
{:.example}

<pre class="prettyprint">
<code>  
&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.print();
&lt;/script&gt;</code>
</pre>






### redo<span class="signature">()</span>
{:#redo}








Restore the last action that was performed





Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.redo(); 
&lt;/script&gt;</code>
</pre>






### remove<span class="signature">(node)</span>
{:#remove}








Remove the either given node/connector or the selected element from diagram

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
<td class="name"><code>node</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">pass node/connector to be removed</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.remove(); 
&lt;/script&gt;</code>
</pre>






### sameHeight<span class="signature">()</span>
{:#sameHeight}








Update the height of the objects in the selection list to the height of first object in selection list





Example
{:.example}

<pre class="prettyprint">
<code>        
&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.sameHeight(); 
&lt;/script&gt;</code>
</pre>






### sameSize<span class="signature">()</span>
{:#sameSize}








Update the size of the objects in the selection list to the size of first object in selction list





Example
{:.example}

<pre class="prettyprint">
<code>        
&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.sameSize(); 
&lt;/script&gt;</code>
</pre>






### sameWidth<span class="signature">()</span>
{:#sameWidth}








Update the width of the objects in the selection list to the width of first object in selection list





Example
{:.example}

<pre class="prettyprint">
<code>        
&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.sameWidth(); 
&lt;/script&gt;</code>
</pre>






### save<span class="signature">()</span>
{:#save}








Save the diagram .

<table class="params">
<thead>
<tr>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last"></td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.save();
&lt;/script&gt;</code>
</pre>






### scrollToNode<span class="signature">(node)</span>
{:#scrollToNode}








Bring the node into view

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
<td class="name"><code>node</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">pass node/connector to be brought into view</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
var node = diagram.selectionList[0];
diagram.scrollToNode(node); 
&lt;/script&gt;</code>
</pre>






### selectAll<span class="signature">()</span>
{:#selectAll}








Select all nodes and connector in diagram





Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.selectAll(); 
&lt;/script&gt;</code>
</pre>






### sendBackward<span class="signature">()</span>
{:#sendBackward}








Decrease the Z-index value of selected object by 1





Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.sendBackward(); 
&lt;/script&gt;</code>
</pre>






### sendToBack<span class="signature">()</span>
{:#sendToBack}








Move the selected object behind all other intersected objects





Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.sendToBack(); 
&lt;/script&gt;</code>
</pre>






### spaceAcross<span class="signature">()</span>
{:#spaceAcross}








Update horizontal space between the objects as equal and within selection boundary





Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.spaceAcross(); 
&lt;/script&gt;</code>
</pre>






### spaceDown<span class="signature">()</span>
{:#spaceDown}








Update vertical space between the objects as equal and within the selection boundary





Example
{:.example}

<pre class="prettyprint">
<code>        
&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.spaceDown(); 
&lt;/script&gt;</code>
</pre>






### startLabelEdit<span class="signature">(node, label)</span>
{:#startLabelEdit}








Start the editing of the specified label of the given node

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
<td class="name"><code>node</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">pass the node/connector to which label to be edited</td>
</tr>
<tr>
<td class="name"><code>label</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">pass the label to be edited</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
var node=diagram.selectionList[0];
diagram.startLabelEdit(node,node.labels[0]);
&lt;/script&gt;</code>
</pre>






### undo<span class="signature">()</span>
{:#undo}








Reverse the last action that was performed





Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.undo(); 
&lt;/script&gt;</code>
</pre>






### ungroup<span class="signature">()</span>
{:#ungroup}








Ungroup the selected group





Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.ungroup(); 
&lt;/script&gt;</code>
</pre>






### update<span class="signature">(name, options)</span>
{:#update}








Update Diagram with its specific properties

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
<td class="name"><code>name</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">to identify the diagram from the model</td>
</tr>
<tr>
<td class="name"><code>options</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">to specify which properties of the diagram to be updated</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
var value = ej.datavisualization.Diagram.DiagramConstraints.Default;
diagram.updateDiagram(diagram.name, { constraints: value });      
&lt;/script&gt;</code>
</pre>






### updateConnector<span class="signature">(name, options)</span>
{:#updateConnector}








Update Connector with their its properties

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
<td class="name"><code>name</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">to identify the connector from the model</td>
</tr>
<tr>
<td class="name"><code>options</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">to specify which property of the Connector to be update</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
var value = ej.datavisualization.Diagram.ConnectorConstraints.Default;
diagram.updateConnector(connector.name, { constraints: value });      
&lt;/script&gt;</code>
</pre>






### updateLabel<span class="signature">(nodeName, label, obj)</span>
{:#updateLabel}








Update the given label with its specific properties

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
<td class="name"><code>nodeName</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">pass the name of node/connector</td>
</tr>
<tr>
<td class="name"><code>label</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">pass the label to be modified</td>
</tr>
<tr>
<td class="name"><code>obj</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">pass the new porperties of the label</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
var node=diagram.selectionList[0];
var label = [];
label =[{"name":"node1" "text": "node", "bold": true, "italic": true}]
diagram.updateLabel(node.name,node.labels[0],label);
&lt;/script&gt;</code>
</pre>






### updateNode<span class="signature">(name, options)</span>
{:#updateNode}








Update Node with its specific properties

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
<td class="name"><code>name</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">to identify the Node from the model</td>
</tr>
<tr>
<td class="name"><code>options</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">to specify which property of the Node to be update</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
var value = ej.datavisualization.Diagram.NodeConstraints.Default &amp; ~ej.datavisualization.Diagram.NodeConstraints.Connect;
diagram.updateNode(node.name, { constraints: value });
&lt;/script&gt;</code>
</pre>






### updateSelectedObject<span class="signature">(name)</span>
{:#updateSelectedObject}








Update the specified node as selected object.

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
<td class="name"><code>name</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">to identify the object from the model</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance"); 
diagram.updateSelectedObject(name);    
&lt;/script&gt;</code>
</pre>






### updateSelection<span class="signature">(isDragging)</span>
{:#updateSelection}








Update the selection of target node/connector

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
<td class="name"><code>isDragging</code></td>
<td class="type"><span class="param-type">Boolean</span></td>
<td class="description last">pass true/false whether to drag or not</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.updateSelection(true);
&lt;/script&gt;</code>
</pre>






### updateUserHandles<span class="signature">(node)</span>
{:#updateUserHandles}








Update userhandles with respect to the given node

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
<td class="name"><code>node</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">pass node/connector</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
var node = diagram.selectionList[0];
diagram.updateUSerHandles(node); 
&lt;/script&gt;</code>
</pre>






### updateViewPort<span class="signature">()</span>
{:#updateViewPort}








To update viewport when window resize





Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.updateViewPort();
&lt;/script&gt;</code>
</pre>






### upgrade<span class="signature">(data)</span>
{:#upgrade}








To Upgrade the diagram from old version .

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
<td class="name"><code>data</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last"></td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.upgrade(jsonData);
diagram.load(jsonData);
&lt;/script&gt;</code>
</pre>






### zoomTo<span class="signature">(zoom)</span>
{:#zoomTo}








Used to zoomIn/zoomOut diagram

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
<td class="name"><code>zoom</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">pass zoom commands of the diagram</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var diagram=$("#diagramcontent").ejDiagram("instance");
var zoom =  ej.datavisualization.Diagram.Zoom();
zoom.zoomFactor = .1;
zoom.zoomCommand = ej.datavisualization.Diagram.ZoomCommand.ZoomIn;
diagram.zoomTo(zoom);
&lt;/script&gt;</code>
</pre>




## Events








### autoScrollChange
{:#autoScrollChange}








Triggers When auto scroll is changed

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
<td class="name"><code>argument.delay</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">returns should be inserted or removed</td>
</tr>
<tr>
<td class="name"><code>argument.distanceFromDiagram</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns node which to be added or deleted</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>// autoScrollChange event for diagram
$("#diagramcontent").ejDiagram({
autoScrollChange:function (args)  {}
 });</code>
</pre>






### click
{:#click}








Triggers when click node/connector

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
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">args parameter from diagram
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
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns diagram</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>//  click event for diagram
$("#diagramcontent").ejDiagram({
click:function (args)  {}
        });</code>
</pre>






### connectionChange
{:#connectionChange}








Triggers when the connection is changed

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
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">args parameter from diagram
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
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns connector</td>
</tr>
<tr>
<td class="name"><code>connection</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">parameter returns source or target node that was connected</td>
</tr>
<tr>
<td class="name"><code>port</code></td>
<td class="type"><span class="param-type">port</span></td>
<td class="description last">parameter returns source or target port that was connected</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>// connectionChange event for diagram
$("#diagramcontent").ejDiagram({
connectionChange:function (args)  {}
        }); </code>
</pre>






### connectorCollectionChange
{:#connectorCollectionChange}








Triggers When connector collection is changed

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
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">args parameter from diagram
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
<td class="name"><code>changetype</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">return should be inserted or removed</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns connector which to be added or deleted</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>// connectorCollectionChange event for diagram
$("#diagramcontent").ejDiagram({
connectorCollectionChange:function (args) {}
        });</code>
</pre>






### connectorSourceChange
{:#connectorSourceChange}








Triggers when the connectors' source point is changed

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
<td class="name"><code>argument.point</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns source point</td>
</tr>
<tr>
<td class="name"><code>argument.port</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns source port</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">Boolean</span></td>
<td class="description last">if the event should be cancelled ,otherwise fasle</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>// connectorSourceChange event for diagram
$("#diagramcontent").ejDiagram({
connectorSourceChange:function (args)  {}
       });</code>
</pre>






### connectorTargetChange
{:#connectorTargetChange}








Triggers when the connectors target point is changed

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
<td class="name"><code>argument.point</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns target point</td>
</tr>
<tr>
<td class="name"><code>argument.port</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns target port</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">Boolean</span></td>
<td class="description last">if the event should be cancelled ,otherwise fasle</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>// connectorTargetChange event for diagram
$("#diagramcontent").ejDiagram({
connectorTargetChange:function (args)  {}
      });</code>
</pre>






### contextMenuBeforeOpen
{:#contextMenuBeforeOpen}








Triggers before open the context menu

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
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">args parameter from diagram</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>// contextMenuBeforeOpen event for diagram
$("#diagramcontent").ejDiagram({
contextMenuBeforeOpen:function (args)  {}
         });</code>
</pre>






### contextMenuClick
{:#contextMenuClick}








Triggers when context menu item is clicked

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
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">args parameter from diagram</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>// contextMenuClick event for diagram
$("#diagramcontent").ejDiagram({
contextMenuClick:function (args)  {}
          });</code>
</pre>






### doubleClick
{:#doubleClick}








Triggers when doubleClick node/connector

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
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">args parameter from diagram
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">Boolean</span></td>
<td class="description last">if the event should be cancelled ,otherwise fasle</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns selected object in list</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>//  doubleClick event for diagram
$("#diagramcontent").ejDiagram({
doubleClick:function (args)  {}
        });</code>
</pre>






### drag
{:#drag}








Triggers while dragging the elements in diagram

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
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">args parameter from diagram
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
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns node or connector</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>//  deag event for diagram
$("#diagramcontent").ejDiagram({
drag:function (args)  {}
  });</code>
</pre>






### drop
{:#drop}








Triggers when drag and drop symbols from palette to drawing area

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
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">args parameter from diagram
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
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns node or connector</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>//  drop event for diagram
$("#diagramcontent").ejDiagram({
drop:function (args)  {}
        });</code>
</pre>






### itemClick
{:#itemClick}








Triggers when the diagram/diagram element is clicked

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
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">args.cancel if the event should be cancelled ,otherwise fasle
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
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">return event name</td>
</tr>
<tr>
<td class="name"><code>actualObject</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">node was clicked</td>
</tr>
<tr>
<td class="name"><code>selectedObject</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">actual selected object</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">contains holds the reference of diagram</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>// itemClick event for diagram
$("#diagramcontent").ejDiagram({
itemClick:function (args) {}
        });</code>
</pre>






### mouseEnter
{:#mouseEnter}








Triggers When mouse enter node/connector

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
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">args parameter from diagram
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
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns node or connector</td>
</tr>
<tr>
<td class="name"><code>source</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">the object dragged from this container</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">the object is going to be dropped.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>//  mouseEnter event for diagram
$("#diagramcontent").ejDiagram({
mouseEnter:function (args)  {}
        });</code>
</pre>






### mouseLeave
{:#mouseLeave}








Triggers When mouse leaves node/connector

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
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">args parameter from diagram
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
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns node or connector</td>
</tr>
<tr>
<td class="name"><code>source</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">the object dragged from this container</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">the object is going to be dropped.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>//  mouseLeave event for diagram
$("#diagramcontent").ejDiagram({
mouseLeave:function (args)  {}
               });</code>
</pre>






### mouseOver
{:#mouseOver}








Triggers when mouse hover on node/connector

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
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">args parameter from diagram
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
<td class="name"><code>diagram</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns node or connector</td>
</tr>
<tr>
<td class="name"><code>source</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">the object dragged from this container</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">the object is going to be dropped.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>//  mouseOver event for diagram
$("#diagramcontent").ejDiagram({
mouseOver:function (args)  {}
        });   </code>
</pre>






### nodeCollectionChange
{:#nodeCollectionChange}








Triggers When node collection is changed

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
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">args parameter from diagram
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
<td class="name"><code>changetype</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">returns should be inserted or removed</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns node which to be added or deleted</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>// nodeCollectionChange event for diagram
$("#diagramcontent").ejDiagram({
nodeCollectionChange:function (args)  {}
 });</code>
</pre>






### nodeSizeChange
{:#nodeSizeChange}








Triggers When node size has been changed

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
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">args parameter from diagram
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
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns node that was resized</td>
</tr>
<tr>
<td class="name"><code>offset</code></td>
<td class="type"><span class="param-type">Number</span></td>
<td class="description last">parameter returns size of the node</td>
</tr>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">Boolean</span></td>
<td class="description last">if the event should be cancelled ,otherwise fasle</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>// sizeChange event for diagram
$("#diagramcontent").ejDiagram({
sizeChange:function (args)  {}
         });</code>
</pre>






### rotationChange
{:#rotationChange}








Triggers when the element is rotated

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
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">args parameter from diagram
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
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns node</td>
</tr>
<tr>
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">Boolean</span></td>
<td class="description last">if the event should be cancelled ,otherwise fasle</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>// rotationChange event for diagram
$("#diagramcontent").ejDiagram({
rotationChange:function (args)  {}
        });</code>
</pre>






### selectionChanged
{:#selectionChanged}








Triggers When selection is changed

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
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">args parameter from diagram
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
<td class="name"><code>oldItems</code></td>
<td class="type"><span class="param-type">array</span></td>
<td class="description last">parameter returns collection of nodes and connectors which were currently selected</td>
</tr>
<tr>
<td class="name"><code>newItems</code></td>
<td class="type"><span class="param-type">array</span></td>
<td class="description last">parameter returns collection of nodes and connectors which is to be selected</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>//  selectionChange event for diagram
$("#diagramcontent").ejDiagram({
selectionChange:function (args)  {}
        });</code>
</pre>






### textchanged
{:#textchanged}








Triggers When label editing is ended

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
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">args parameter from diagram
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
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns shape</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">parameter returns value in label edit box</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>// textChanged event for diagram
$("#diagramcontent").ejDiagram({
textChanged:function (args)  {}
        });</code>
</pre>



