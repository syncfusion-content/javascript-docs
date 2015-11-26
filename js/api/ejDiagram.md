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


{% highlight html %}
 
<div id="diagram"></div>
<script>
//Create Diagram
    $("#diagram").ejDiagram();
</script>{% endhighlight %}







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
{:#members:backgroundcolor}








Color to be set as the background of the elements




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({ backgroundColor: "red"});
</script>{% endhighlight %}







### backgroundImage<span class="type-signature type string">String</span>
{:#members:backgroundimage}








Image to be set as the background of the elements




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({ backgroundImage: "Syncfusion.png"});
</script>{% endhighlight %}







### bridgeDirection<span class="type-signature type string">String</span>
{:#members:bridgedirection}








Sets the bridge direction of connectors




Default Value:
{:.param}






* "top"








Example
{:.example}


{% highlight html %}
 
<div id="diagramcontent"></div>
<script>
$("#diagramContent").ejDiagram({bridgeDirection: "top"} }); 
</script>{% endhighlight %}







### connectors<span class="type-signature type array">array</span>
{:#members:connectors}








Array of connector objects where each object has definition/properties of connector.




Default Value:
{:.param}






* []








Example
{:.example}


{% highlight html %}
<div id="diagram"></div>
<script>
var connectors = [{ name: "connector" sourceNode: "node1", targetNode: "node2"}];
$("#diagram").ejDiagram({ connectors:connectors });
</script>{% endhighlight %}







### connectors.addInfo<span class="type-signature type object">Object</span>
{:#members:connectors-addinfo}








To provide/save extra information about Connector




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connectors = [];
var addInfo = {Name1:"Connector1",Connector2:"Connector3"}
connectors=[{addInfo: addInfo}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.bridgeSpace<span class="type-signature type integer">Integer</span>
{:#members:connectors-bridgespace}








Defines width of the line bridges




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connectors=[];
connectors=[{bridgeSpace:15}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.constraints<span class="type-signature type enum">enum</span>
{:#members:connectors-constraints}








Enables or disables the behaviors of connector see<a href="global.html#ConnectorConstraints">ConnectorConstraints</a>




Default Value:
{:.param}






* ConnectorConstraints.Default








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connectors = [];
connectors=[{constraints: ej.datavisualization.Diagram.ConnectorConstraints.Select}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.cornerRadius<span class="type-signature type integer">Integer</span>
{:#members:connectors-cornerradius}








Defines the radius of the rounded corner




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connectors=[];
connectors=[{cornerRadius:2}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.horizontalAlign<span class="type-signature type horizontalalignment"><a href="global.html#HorizontalAlignment">HorizontalAlignment</a></span>
{:#members:connectors-horizontalalign}








To set the horizontal alignment of connector.Applicable if the parent is group.




Default Value:
{:.param}






* HorizontalAlignment.Left








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connectors = [];
connectors=[{HorizontalAlignment: ej.datavisualization.Diagram.HorizontalAlignment.Left}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.labels<span class="type-signature type array">Array</span>
{:#members:connectors-labels}








Sets the collection of labels of connector




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
Refer nodes label for label properties details 
<div id="diagramcontent"></div>
<script>
var label = [];
label = [{ "text": "Connector1", "fontColor": "Red"}];
$("#diagramcontent").ejDiagram({label:label});
</script>{% endhighlight %}







### connectors.lineColor<span class="type-signature type string">String</span>
{:#members:connectors-linecolor}








Sets the stroke color of the connector




Default Value:
{:.param}






* black








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connectors = [];
connectors=[{lineColor:"blue"}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.lineDashArray<span class="type-signature type string">String</span>
{:#members:connectors-linedasharray}








Sets the pattern of dashes and gaps used to stroke the path of connector




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connectors = [];
connectors=[{lineDashArray:"4 4"}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.lineHitPadding<span class="type-signature type int">Int</span>
{:#members:connectors-linehitpadding}








Defines padding set to line to ease interaction




Default Value:
{:.param}






* 10








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connectors= [];
connectors=[{lineHitPadding: 30}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.lineWidth<span class="type-signature type int">Int</span>
{:#members:connectors-linewidth}








Sets the width of the line




Default Value:
{:.param}






* 1








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connectors = [];
connectors=[{lineWidth:4}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.marginBottom<span class="type-signature type int">Int</span>
{:#members:connectors-marginbottom}








To set margin bottom for the connector.Applicable if the parent is group.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connectors = [];
connectors=[{marginBottom: 1}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.marginLeft<span class="type-signature type int">Int</span>
{:#members:connectors-marginleft}








To set left margin for the connector.Applicable if the parent is group.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connectors = [];
connectors=[{name:"connector",marginLeft: 1}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.marginRight<span class="type-signature type int">Int</span>
{:#members:connectors-marginright}








To set right margin for the connector.Applicable if the parent is group.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connectors = [];
connectors=[{marginRight: 1}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.marginTop<span class="type-signature type int">Int</span>
{:#members:connectors-margintop}








To set top margin for the connector.Applicable if the parent is group.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connectors = [];
connectors=[{marginTop: 1}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.name<span class="type-signature type string">String</span>
{:#members:connectors-name}








Sets the name of the connector




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connectors = [];
connectors=[{name:"Connector1"}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.opacity<span class="type-signature type int">Int</span>
{:#members:connectors-opacity}








Defines the transparency of the connector




Default Value:
{:.param}






* 1








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connectors = [];
connectors=[{opacity:0.6}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.parent<span class="type-signature type string">String</span>
{:#members:connectors-parent}








Sets the parent name of the connector




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connector = [ {name: "rect",parent:"group1"}];
</script>{% endhighlight %}







### connectors.segments<span class="type-signature type array">Array</span>
{:#members:connectors-segments}








Describes the collection of segments




Default Value:
{:.param}






* [ Segment ]








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connectors = [];
var point= {x:20,y:20};
connectors=[{segments: [{type:"straight",point:point}]}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.segments.direction<span class="type-signature type string">String</span>
{:#members:connectors-segments-direction}








Describes the direction of orthogonal segment




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connectors = [];
connectors=[{segments: [{type:"orthogonal",direction:"left"}]}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.segments.length<span class="type-signature type number">Number</span>
{:#members:connectors-segments-length}








Describes the length of orthogonal segment




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connectors = [];
connectors=[{segments: [{type:"orthogonal",length:20}]}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.segments.point<span class="type-signature type point">Point</span>
{:#members:connectors-segments-point}








Describes the end point of segment




Default Value:
{:.param}






* Diagram.Point()








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var segments = [{ type: "straight",point:{x:10,y:30}}];
connectors = [{ name: "connector1", segments: segments, sourcePoint: { x: 450, y: 150 }, targetPoint: { x: 210, y: 40 }}];
$("#diagramcontent").ejDiagram({segments:segments});
</script>{% endhighlight %}







### connectors.segments.point1<span class="type-signature type point">Point</span>
{:#members:connectors-segments-point1}








Describes the first control point of bezier segment




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connectors = [];
var point1={x:10,y:10}];
connectors=[{segments: [{type:"bezier", point1:point1}]}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.segments.point2<span class="type-signature type point">Point</span>
{:#members:connectors-segments-point2}








Describes the second control point of bezier segment




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connectors = [];
var point2= {x:10,y:10};
connectors=[{segments: [{type:"bezier",point2:point2}]}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.segments.type<span class="type-signature type enum">enum</span>
{:#members:connectors-segments-type}








Type of the segments See <a href="global.html#Segments">Segments</a>




Default Value:
{:.param}






* ej.datavisualization.Diagram.Segments.Straight








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var link=[];
link=[{segments:[{type:"straight"}]}];
$("#diagramcontent").ejDiagram({connectors:link});
</script>{% endhighlight %}







### connectors.segments.vector1<span class="type-signature type point">Point</span>
{:#members:connectors-segments-vector1}








Describes the length and angle between the first control point and start point of segment




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connectors = [];
var vector1= {x:20,y:20};
connectors=[{segments: [{type:"bezier",vector1:vector1}]}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.segments.vector2<span class="type-signature type point">Point</span>
{:#members:connectors-segments-vector2}








Describes the length and angle between the second control point and end point of segment




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connectors = [];
var vector2= {x:20,y:20};
connectors=[{segments: [{type:"bezier",vector2:vector2}]}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.sourceDecorator<span class="type-signature type string">String</span>
{:#members:connectors-sourcedecorator}








To set sourceDecorator for connector




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connectors = [];
var targetDecorator = { shape: "arrow", borderColor: "#606060", width: "10", height: "10" };
connectors=[{targetDecorator:targetDecorator}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.sourceDecorator.borderColor<span class="type-signature type string">String</span>
{:#members:connectors-sourcedecorator-bordercolor}








Sets the border color of the decorator




Default Value:
{:.param}






* "black"








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var link=[];
link={[targetDecorator:{borderColor: "green"}]};
$("#diagramcontent").ejDiagram({connectors:link});
</script>{% endhighlight %}







### connectors.sourceDecorator.borderColor<span class="type-signature type string">String</span>
{:#members:connectors-sourcedecorator-bordercolor}








Sets the border color of the decorator




Default Value:
{:.param}






* "black"








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var link=[];
link={[targetDecorator:{borderColor: "green"}]};
$("#diagramcontent").ejDiagram({connectors:link});
</script>{% endhighlight %}







### connectors.sourceDecorator.borderWidth<span class="type-signature type number">Number</span>
{:#members:connectors-sourcedecorator-borderwidth}








Sets the border width of the decorator




Default Value:
{:.param}






* 1








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var link=[];
link={[targetDecorator:{borderWidth: 1}]};
$("#diagramcontent").ejDiagram({connectors:link});
</script>{% endhighlight %}







### connectors.sourceDecorator.fillColor<span class="type-signature type string">String</span>
{:#members:connectors-sourcedecorator-fillcolor}








Sets the color with which the decorator is to be filled




Default Value:
{:.param}






* "black"








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var link=[];
link={[targetDecorator:{fillColor: "green"}]};
$("#diagramcontent").ejDiagram({connectors:link});
</script>{% endhighlight %}







### connectors.sourceDecorator.fillColor<span class="type-signature type string">String</span>
{:#members:connectors-sourcedecorator-fillcolor}








Sets the color with which the decorator is to be filled




Default Value:
{:.param}






* "black"








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var link=[];
link={[targetDecorator:{fillColor: "green"}]};
$("#diagramcontent").ejDiagram({connectors:link});
</script>{% endhighlight %}







### connectors.sourceDecorator.height<span class="type-signature type number">Number</span>
{:#members:connectors-sourcedecorator-height}








To set the height of the connection decorator




Default Value:
{:.param}






* 8








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var link=[];
link={[targetDecorator:{height:10}]};
$("#diagramcontent").ejDiagram({connectors:link});
</script>{% endhighlight %}







### connectors.sourceDecorator.height<span class="type-signature type number">Number</span>
{:#members:connectors-sourcedecorator-height}








To set the height of the connection decorator




Default Value:
{:.param}






* 8








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var link=[];
link={[targetDecorator:{height:10}]};
$("#diagramcontent").ejDiagram({connectors:link});
</script>{% endhighlight %}







### connectors.sourceDecorator.pathData<span class="type-signature type string">String</span>
{:#members:connectors-sourcedecorator-pathdata}








Path data to draw decorator with custom shape




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var link=[];
link={[targetDecorator:{pathData: "M 269.711,29.3333C 269.711,44.061 257.772,56 243.044,56z"}]};
$("#diagramcontent").ejDiagram({connectors:link});
</script>{% endhighlight %}







### connectors.sourceDecorator.pathData<span class="type-signature type string">String</span>
{:#members:connectors-sourcedecorator-pathdata}








Path data to decorator with custom shape




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var link=[];
link={[targetDecorator:{pathData: "M 269.711,29.3333C 269.711,44.061 257.772,56 243.044,56z"}]};
$("#diagramcontent").ejDiagram({connectors:link});
</script>{% endhighlight %}







### connectors.sourceDecorator.shape<span class="type-signature type enum">enum</span>
{:#members:connectors-sourcedecorator-shape}








To set the decorator shape of the connector See <a href="global.html#DecoratorShapes">DecoratorShapes</a>




Default Value:
{:.param}






* ej.datavisualization.Diagram.DecoratorShapes.Arrow








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var link=[];
link={[targetDecorator:{shape:"arrow"}]};
$("#diagramcontent").ejDiagram({connectors:link});
</script>{% endhighlight %}







### connectors.sourceDecorator.shape<span class="type-signature type enum">enum</span>
{:#members:connectors-sourcedecorator-shape}








Sets the decorator shape See <a href="global.html#DecoratorShapes">DecoratorShapes</a>




Default Value:
{:.param}






* ej.datavisualization.Diagram.DecoratorShapes.Arrow








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var link=[];
link={[targetDecorator:{shape:"arrow"}]};
$("#diagramcontent").ejDiagram({connectors:link});
</script>{% endhighlight %}







### connectors.sourceDecorator.width<span class="type-signature type number">Number</span>
{:#members:connectors-sourcedecorator-width}








To set the width of the connection decorator




Default Value:
{:.param}






* 8








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var link=[];
link={[targetDecorator:{width:10}]};
$("#diagramcontent").ejDiagram({connectors:link});
</script>{% endhighlight %}







### connectors.sourceDecorator.width<span class="type-signature type number">Number</span>
{:#members:connectors-sourcedecorator-width}








To set width of the connection decorator




Default Value:
{:.param}






* 8








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var link=[];
link={[targetDecorator:{width:10}]};
$("#diagramcontent").ejDiagram({connectors:link});
</script>{% endhighlight %}







### connectors.sourceNode<span class="type-signature type object">Object</span>
{:#members:connectors-sourcenode}








Sets the sourceNode of the connector




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
var connectors = [];
nodes = {name: "openBrowses", width: 175, height: 60};
connectors=[{sourceNode: "openBrowses"}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.sourcePadding<span class="type-signature type integer">Integer</span>
{:#members:connectors-sourcepadding}








Defines the space between node and connector's source point




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connectors=[];
connectors=[{sourcePadding:5}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.sourcePoint<span class="type-signature type point">Point</span>
{:#members:connectors-sourcepoint}








Describes the sourcePoint of connector




Default Value:
{:.param}






* Point








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connectors = [];
var sourcePoint= {x:20,y:20};
connectors=[{ name: "connector1",sourcePoint: { x: 450, y: 150 }}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.sourcePort<span class="type-signature type object">Object</span>
{:#members:connectors-sourceport}








Sets the sourcePort of the connector




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
var ports = [];
var connectors = [];
nodes = {name: "openBrowses", width: 175, height: 60};
ports = { offset: { x: 0, y: 0.5 }, name: "bport" };
connectors=[{sourcePort: "bport"}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.targetDecorator<span class="type-signature type string">String</span>
{:#members:connectors-targetdecorator}








To set targetDecorator for connector




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connectors = [];
var targetDecorator = { shape: "arrow", borderColor: "#606060", width: "10", height: "10" };
connectors=[{targetDecorator:targetDecorator}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.targetDecorator.borderColor<span class="type-signature type string">String</span>
{:#members:connectors-targetdecorator-bordercolor}








Sets the border color of the decorator




Default Value:
{:.param}






* "black"








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var link=[];
link={[targetDecorator:{borderColor: "green"}]};
$("#diagramcontent").ejDiagram({connectors:link});
</script>{% endhighlight %}







### connectors.targetDecorator.fillColor<span class="type-signature type string">String</span>
{:#members:connectors-targetdecorator-fillcolor}








Sets the color with which the decorator is to be filled




Default Value:
{:.param}






* "black"








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var link=[];
link={[targetDecorator:{fillColor: "green"}]};
$("#diagramcontent").ejDiagram({connectors:link});
</script>{% endhighlight %}







### connectors.targetDecorator.height<span class="type-signature type number">Number</span>
{:#members:connectors-targetdecorator-height}








To set the height of the decorator




Default Value:
{:.param}






* 8








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var link=[];
link={[targetDecorator:{height:10}]};
$("#diagramcontent").ejDiagram({connectors:link});
</script>{% endhighlight %}







### connectors.targetDecorator.pathData<span class="type-signature type string">String</span>
{:#members:connectors-targetdecorator-pathdata}








Path data to draw decorator with custom shape




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var link=[];
link={[targetDecorator:{pathData: "M 269.711,29.3333C 269.711,44.061 257.772,56 243.044,56z"}]};
$("#diagramcontent").ejDiagram({connectors:link});
</script>{% endhighlight %}







### connectors.targetDecorator.shape<span class="type-signature type enum">enum</span>
{:#members:connectors-targetdecorator-shape}








To set the shape of the decorator in connector See <a href="global.html#DecoratorShapes">DecoratorShapes</a>




Default Value:
{:.param}






* ej.datavisualization.Diagram.DecoratorShapes.Arrow








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var link=[];
link={[targetDecorator:{shape:"arrow"}]};
$("#diagramcontent").ejDiagram({connectors:link});
</script>{% endhighlight %}







### connectors.targetDecorator.width<span class="type-signature type number">Number</span>
{:#members:connectors-targetdecorator-width}








To set the width of the decorator




Default Value:
{:.param}






* 8








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var link=[];
link={[targetDecorator:{width:10}]};
$("#diagramcontent").ejDiagram({connectors:link});
</script>{% endhighlight %}







### connectors.targetNode<span class="type-signature type object">Object</span>
{:#members:connectors-targetnode}








Sets the target node of the connector




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes =[];
var connectors = [];
nodes = {name: "openBrowses", width: 175, height: 60};
connectors=[{targetNode: "openBrowses"}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.targetPadding<span class="type-signature type integer">Integer</span>
{:#members:connectors-targetpadding}








Defines the space between node and connector's target point




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connectors=[];
connectors=[{targetPadding:5}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.targetPoint<span class="type-signature type point">Point</span>
{:#members:connectors-targetpoint}








Describes the targetPoint of connector




Default Value:
{:.param}






* Point








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connectors = [];
var targetPoint= {x:20,y:20};
connectors=[{ name: "connector1",targetPoint: { x: 450, y: 150 }}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.targetPort<span class="type-signature type object">Object</span>
{:#members:connectors-targetport}








Sets the targetPort of the connector




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
var ports = [];
var connectors = [];
nodes = {name: "openBrowses", width: 175, height: 60};
ports = { offset: { x: 0, y: 0.5 }, name: "aport" };
connectors=[{targetPort: "aport"}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.verticalAlign<span class="type-signature type verticalalignment"><a href="global.html#VerticalAlignment">VerticalAlignment</a></span>
{:#members:connectors-verticalalign}








To set the vertical alignment of connector.Applicable if the parent is group.




Default Value:
{:.param}






* VerticalAlignment.Top








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connectors = [];
connectors=[{VerticalAlignment: ej.datavisualization.Diagram.VerticalAlignment.Top}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.visible<span class="type-signature type boolean">Boolean</span>
{:#members:connectors-visible}








Enables or disables the visibility of connector




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connectors = [];
connectors=[{visible: true}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectors.zOrder<span class="type-signature type int">Int</span>
{:#members:connectors-zorder}








Sets the Zorder of the connector




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connectors= [];
connectors=[{connectors: 1}];
$("#diagramcontent").ejDiagram({connectors:connectors});
</script>{% endhighlight %}







### connectorTemplate<span class="type-signature type object">object</span>
{:#members:connectortemplate}








To customize the connector properties before rendering the connector.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="diagram"></div>
<script>
function connectorTemplate(diagram, connector, data) {connector.labels[0].text = data.Name};
$("#diagram").ejDiagram({ connectorTemplate:connectorTemplate});
</script>{% endhighlight %}







### constraints<span class="type-signature type enum">enum</span>
{:#members:constraints}








Sets the default behavior of the diagram see <a href="global.html#DiagramConstraints">DiagramConstraints</a>




Default Value:
{:.param}






* constraints.All








Example
{:.example}


{% highlight html %}
 
<div id="diagramcontent"></div>
<script>
$("#diagramContent").ejDiagram({constraints: ej.datavisualization.Diagram.DiagramConstraints.Default} }); 
</script>{% endhighlight %}







### contextMenu
{:#members:contextmenu}








Object to customize context menu behavior of diagram











### contextMenu.items<span class="type-signature type object">Object</span>
{:#members:contextmenu-items}








To define the collection of context menu items




Default Value:
{:.param}






* []








Example
{:.example}


{% highlight html %}
 
<div id="diagramcontent"></div>
<script>
//Collection of  items
var menucollection = [{ "name": "hyperLink", "text": "Hyperlink", "image": "", "style": "" }];
var contextMenu = { items: menucollection};
$("#diagramContent").ejDiagram({contextMenu: contextMenu}); 
</script>{% endhighlight %}







### contextMenu.showCustomMenuItemsOnly<span class="type-signature type boolean">Boolean</span>
{:#members:contextmenu-showcustommenuitemsonly}








To set whether to display the default context menu items or not




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({showCustomMenuItemsOnly: true});
</script>{% endhighlight %}







### dataSourceSettings
{:#members:datasourcesettings}








Object to set dataSource to diagram











### dataSourceSettings.dataSource<span class="type-signature type object">object</span>
{:#members:datasourcesettings-datasource}








Describes data source either as a collection of objects or an instance of ej.DataManager




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="diagram"></div>
<script>
$("#diagram").ejDiagram({ dataSourceSettings: {dataSource: localData}});
</script>{% endhighlight %}







### dataSourceSettings.id<span class="type-signature type string">String</span>
{:#members:datasourcesettings-id}








Describes the unique id of data source items.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="diagram"></div>
<script>
$("#diagram").ejDiagram({ dataSourceSettings: {id: "CategoryID"}});
</script>{% endhighlight %}







### dataSourceSettings.parent<span class="type-signature type string">String</span>
{:#members:datasourcesettings-parent}








Describes the parent id of data source items.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="diagram"></div>
<script>
$("#diagram").ejDiagram({ dataSourceSettings: { parent: "reportingPerson"}});
</script>{% endhighlight %}







### dataSourceSettings.query<span class="type-signature type object">object</span>
{:#members:datasourcesettings-query}








Describes query to retrieve a set of data from the specified datasource.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="diagram"></div>
<script>
query: ej.Query().from("Categories").select("CategoryID,CategoryName").take(3);
</script>{% endhighlight %}







### dataSourceSettings.root<span class="type-signature type string">String</span>
{:#members:datasourcesettings-root}








Describes the root node.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="diagram"></div>
<script>
$("#diagram").ejDiagram({ dataSourceSettings: { root: "1"}});
</script>{% endhighlight %}







### dataSourceSettings.tablename<span class="type-signature type string">String</span>
{:#members:datasourcesettings-tablename}








Describes the name of the table on which the specified query to be executed




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="diagram"></div>
<script>
$("#diagram").ejDiagram({ dataSourceSettings:{tableName: "Categories"}});
</script>{% endhighlight %}







### defaultSettings<span class="type-signature type object">object</span>
{:#members:defaultsettings}








To set the default values to nodes and connector properties




Default Value:
{:.param}






* {}








Example
{:.example}


{% highlight html %}
<div id="diagram"></div>
<script>
$("#diagram").ejDiagram({ defaultSettings: { node:  {width: 110, height: 40, fillColor:"skyblue"}}});
</script>{% endhighlight %}







### defaultSettings.connector<span class="type-signature type object">object</span>
{:#members:defaultsettings-connector}








To set the default values to connector properties




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="diagram"></div>
<script>
$("#diagram").ejDiagram({ defaultSettings:{ connector:{ lineColor: "gray", lineWidth: 2 }}});
</script>{% endhighlight %}







### defaultSettings.node<span class="type-signature type object">object</span>
{:#members:defaultsettings-node}








To set the default values to node properties




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="diagram"></div>
<script>
$("#diagram").ejDiagram({ defaultSettings:{node: { fillColor: "#83A93F", borderColor: "#000000" }}});
</script>{% endhighlight %}







### drawingTools<span class="type-signature type object">Object</span>
{:#members:drawingtools}








Describes the interactive features to be performed




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({ drawingTools: {textTool: ej.datavisualization.Diagram.TextTool()}});
</script>{% endhighlight %}







### drawType<span class="type-signature type object">Object</span>
{:#members:drawtype}








Sets the type of Json object to be drawn through drawing tool




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({drawType:{type:"node"}});
</script>{% endhighlight %}







### enableAutoScroll<span class="type-signature type boolean">Boolean</span>
{:#members:enableautoscroll}








Enables or disables Auto scroll in diagram




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({enableAutoScroll: true});
</script>{% endhighlight %}







### enableContextMenu<span class="type-signature type boolean">Boolean</span>
{:#members:enablecontextmenu}








Enables or disables diagram context menu




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({enableContextMenu: true});
</script>{% endhighlight %}







### height<span class="type-signature type string">string</span>
{:#members:height}








Specifies the height of the diagram.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="diagram"></div>
<script>
$("#diagram").ejDiagram({ height:"100%" });
</script>{% endhighlight %}







### layout
{:#members:layout}








To arrange the diagram elements on page











### layout. fixedNode<span class="type-signature type string">String</span>
{:#members:layout-}








Sets the fixed node with respect to which the layout will be aligned




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
//fixedNode of the layout
$("#diagramContent").ejDiagram({layout: { fixedNode: "nodename"}}); {% endhighlight %}







### layout. getLayoutInfo<span class="type-signature type object">object</span>
{:#members:layout-}








To customize the orientation of trees/sub trees For orientations see <a href="global.html#ChartOrientations">ChartOrientations</a> For chart types see <a href="global.html#ChartTypes">ChartTypes</a>




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="diagram"></div>
<script>
function getLayoutInfo(diagram, node, options) { options.orientation = "vertical"; options.type = "left"; offset = 10;};
$("#diagram").ejDiagram({layout: { getLayoutInfo:getLayoutInfo } });
</script>{% endhighlight %}







### layout. marginY<span class="type-signature type number">Number</span>
{:#members:layout-}








Sets the margin value to be vertically left between layout and diagram




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
// marginY of the layout
$("#diagramContent").ejDiagram({layout: { marginY: 0}}); {% endhighlight %}







### layout.horizontalSpacing<span class="type-signature type number">Number</span>
{:#members:layout-horizontalspacing}








Sets the space to be horizontally left between nodes




Default Value:
{:.param}






* 30








Example
{:.example}


{% highlight html %}
 
//horizontalSpacing of the layout
$("#diagramContent").ejDiagram({layout: {horizontalSpacing: 30}}); {% endhighlight %}







### layout.marginX<span class="type-signature type number">Number</span>
{:#members:layout-marginx}








Sets the margin value to be horizontally left between layout and diagram




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
//marginX of the layout
$("#diagramContent").ejDiagram({layout: {marginX: 0}}); {% endhighlight %}







### layout.orientation<span class="type-signature type string">String</span>
{:#members:layout-orientation}








Sets the orientation/direction to arrange the diagram elements see <a href="global.html#LayoutOrientations">LayoutOrientations</a>




Default Value:
{:.param}






* "topToBottom"








Example
{:.example}


{% highlight html %}
 
//orientation of the layout
$("#diagramContent").ejDiagram({layout: {orientation: "topToBottom"}}); {% endhighlight %}







### layout.type<span class="type-signature type string">String</span>
{:#members:layout-type}








Sets the type of the layout based on which the elements will be arranged




Default Value:
{:.param}






* "none"








Example
{:.example}


{% highlight html %}
 
//type of the layout
$("#diagramContent").ejDiagram({layout: {type: "none"}}); {% endhighlight %}







### layout.verticalSpacing<span class="type-signature type number">Number</span>
{:#members:layout-verticalspacing}








Sets the space to be vertically left between nodes




Default Value:
{:.param}






* 30








Example
{:.example}


{% highlight html %}
 
//verticalSpacing of the layout
$("#diagramContent").ejDiagram({layout: {verticalSpacing: 30}}); {% endhighlight %}







### locale<span class="type-signature type string">String</span>
{:#members:locale}








To define the current culture of diagram




Default Value:
{:.param}






* "en-US"








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({locale: "en-US"});
</script>{% endhighlight %}







### nodes<span class="type-signature type array">array</span>
{:#members:nodes}








Array of node objects where each object has definition/properties of node.




Default Value:
{:.param}






* []








Example
{:.example}


{% highlight html %}
<div id="diagram"></div>
<script>
var nodes = [{ name: "node", width: 175, height: 60}];
$("#diagram").ejDiagram({ nodes:nodes });
</script>{% endhighlight %}







### nodes.activity<span class="type-signature type enum">enum</span>
{:#members:nodes-activity}








Sets the type of BPMN Activity See <a href="global.html#BPMNActivity">BPMNActivity</a>




Default Value:
{:.param}






* ej.datavisualization.Diagram.BPMNActivity.Task








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{type: "bpmn", shape: ej.datavisualization.Diagram.BPMNShapes.Activity, activity: ej.datavisualization.Diagram.BPMNActivity.SubProcess}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.addInfo<span class="type-signature type object">Object</span>
{:#members:nodes-addinfo}








To provide/save extra information about Node




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
var addInfo = {Name1:"Node1",Name2:"Name2"}
nodes=[{addInfo: addInfo}];
$("#diagramcontent").ejDiagram({nodes:nodes});
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane",{addInfo: addInfo}}});
</script>{% endhighlight %}







### nodes.allowDrop<span class="type-signature type boolean">Boolean</span>
{:#members:nodes-allowdrop}








To indicate whether this element can be used as the target of a drop operation. Applicable if the type is group.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{name:"GroupNode",allowDrop:true}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.borderColor<span class="type-signature type string">String</span>
{:#members:nodes-bordercolor}








Sets the border color of node




Default Value:
{:.param}






* "black"








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{borderColor: "black"}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.borderDashArray<span class="type-signature type string">String</span>
{:#members:nodes-borderdasharray}








The pattern of dashes and gaps to stroke the border




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{borderDashArray: "2 2"}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.borderWidth<span class="type-signature type number">Number</span>
{:#members:nodes-borderwidth}








Sets the border width of the node




Default Value:
{:.param}






* 1








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{borderWidth: 3}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.canUngroup<span class="type-signature type boolean">Boolean</span>
{:#members:nodes-canungroup}








To set whether the group can be ungrouped or not




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
var children = ["Node1","Node2"];
nodes=[{name:"GroupNode",children:children,canUngroup:false}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.children<span class="type-signature type array">Array</span>
{:#members:nodes-children}








Collection of children of the group node




Default Value:
{:.param}






* []








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
var children = ["Node1","Node2"];
nodes=[{name:"GroupNode",children:children}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.collection<span class="type-signature type boolean">Boolean</span>
{:#members:nodes-collection}








To set whether the BPMN dataobject is a collection or not




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{type: "bpmn", shape:"dataObject", collection: false}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.connectorPadding<span class="type-signature type int">Int</span>
{:#members:nodes-connectorpadding}








To set the distance to be left between the node and connections.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
node={name:"node1",connectorPadding: 2};
$("#diagramcontent").ejDiagram({nodes:[node]});
</script>{% endhighlight %}







### nodes.constraints<span class="type-signature type enum">enum</span>
{:#members:nodes-constraints}








To enable or disable the default behaviors of the node see<a href="global.html#NodeConstraints">NodeConstraints</a>




Default Value:
{:.param}






* NodeConstraints.Default








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{Constraints: ej.datavisualization.Diagram.NodeConstraints.Select}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.constraints<span class="type-signature type enum">enum</span>
{:#members:nodes-constraints}








To set the constraints for the swimlane see <a href="global.html#NodeConstraints">NodeConstraints</a> ej.datavisualization.Diagram.NodeConstraints.Default &amp; ~(ej.datavisualization.Diagram.NodeConstraints.ResizeNorth | ej.datavisualization.Diagram.NodeConstraints.ResizeWest | ej.datavisualization.Diagram.NodeConstraints.ResizeNorthWest | ej.datavisualization.Diagram.NodeConstraints.ResizeNorthEast | ej.datavisualization.Diagram.NodeConstraints.ResizeSouthWest)





Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes = [ {type: "swimlane",name: "swimlane",constraints: ej.datavisualization.Diagram.NodeConstraints.Connect}
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.container<span class="type-signature type obj">obj</span>
{:#members:nodes-container}








To indicate whether this element can be used as a container.Applicable only if the object as Group.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{name:"GroupNode",container:{}}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.container.orientation<span class="type-signature type string">string</span>
{:#members:nodes-container-orientation}








To set the container orientation. Applicable if the group has container.




Default Value:
{:.param}






* "vertical"








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var container = ej.datavisualization.Diagram.ContainerType.Canvas
container.orientation = "vertical"; 
var nodes = [{name:"Node1",container : container}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.container.type<span class="type-signature type enum">enum</span>
{:#members:nodes-container-type}








To set the type of the container. Applicable if the group has container.




Default Value:
{:.param}






* ej.datavisualization.Diagram.ContainerType.Canvas








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var container = ej.datavisualization.Diagram.ContainerType.Canvas
container.type = "linear; 
var nodes = [{name:"Node1",container : container}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.cornerRadius<span class="type-signature type integer">Integer</span>
{:#members:nodes-cornerradius}








Defines the radius of the rounder corner. Applicable if the shape is rectangle




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node={[shape:{type:"rectangle",cornerRadius:2}]};
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.event<span class="type-signature type enum">enum</span>
{:#members:nodes-event}








Sets the type of BPMN Event See <a href="global.html#BPMNEvents">BPMNEvents</a>




Default Value:
{:.param}






* ej.datavisualization.Diagram.BPMNEvents.Start








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{type: "bpmn", shape: ej.datavisualization.Diagram.BPMNShapes.Event, event: ej.datavisualization.Diagram.BPMNEvents.Start}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.excludeFromLayout<span class="type-signature type boolean">Boolean</span>
{:#members:nodes-excludefromlayout}








To set whether the node can be included in layout arrangement




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{visible: true}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.expanded<span class="type-signature type boolean">Boolean</span>
{:#members:nodes-expanded}








To set whether the node is expanded or collapsed




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{isExpanded: true}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.fillColor<span class="type-signature type string">String</span>
{:#members:nodes-fillcolor}








Sets the color that is used to fill shapes




Default Value:
{:.param}






* "White"








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{fillColor: "white"}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.gateway<span class="type-signature type enum">enum</span>
{:#members:nodes-gateway}








Sets the type of BPMN Gateway See <a href="global.html#BPMNGateways">BPMNGateways</a>




Default Value:
{:.param}






* ej.datavisualization.Diagram.BPMNGateways.None








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{type: "bpmn", shape: ej.datavisualization.Diagram.BPMNShapes.Gateway, gateway: ej.datavisualization.Diagram.BPMNGateways.None}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.gradient
{:#members:nodes-gradient}








Smooth transition from one color to another color in node











### nodes.gradient.LinearGradient<span class="type-signature type object">object</span>
{:#members:nodes-gradient-lineargradient}








Paints an area with a linear gradient.











### nodes.gradient.LinearGradient.stops<span class="type-signature type array">Array</span>
{:#members:nodes-gradient-lineargradient-stops}








The stop region for the gradient




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
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
</script>{% endhighlight %}







### nodes.gradient.LinearGradient.x1<span class="type-signature type int">Int</span>
{:#members:nodes-gradient-lineargradient-x1}








The starting X-Axis for the region




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var gradient = ej.datavisualization.Diagram.LinearGradientDefaults();
gradient.type = "linear;
gradient.x1 = 10;
gradient.x2 = 50;
gradient.y1 = 0;
gradient.y2 = 50;
var nodes = [{name:"Node1",width: 100,height: 100,gradient : gradient}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.gradient.LinearGradient.x2<span class="type-signature type int">Int</span>
{:#members:nodes-gradient-lineargradient-x2}








The ending X-Axis for the region




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var gradient = ej.datavisualization.Diagram.LinearGradientDefaults();
gradient.type = "linear;
gradient.x1 = 10;
gradient.x2 = 50;
gradient.y1 = 20;
gradient.y2 = 50;
var nodes = [{name:"Node1",width: 100,height: 100,gradient : gradient}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.gradient.LinearGradient.y1<span class="type-signature type int">Int</span>
{:#members:nodes-gradient-lineargradient-y1}








The starting Y-Axis for the region




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var gradient = ej.datavisualization.Diagram.LinearGradientDefaults();
gradient.type = "linear;
gradient.x1 = 10;
gradient.x2 = 50;
gradient.y1 = 0;
gradient.y2 = 50;
var nodes = [{name:"Node1",width: 100,height: 100,gradient : gradient}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.gradient.LinearGradient.y2<span class="type-signature type int">Int</span>
{:#members:nodes-gradient-lineargradient-y2}








The ending Y-Axis for the region




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var gradient = ej.datavisualization.Diagram.LinearGradientDefaults();
gradient.type = "linear;
gradient.x1 = 10;
gradient.x2 = 50;
gradient.y1 = 0;
gradient.y2 = 50;
var nodes = [{name:"Node1",width: 100,height: 100,gradient : gradient}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.gradient.RadialGradient<span class="type-signature type object">object</span>
{:#members:nodes-gradient-radialgradient}








Paints an area with a radial gradient. A focal point defines the beginning of the gradient, and a circle defines the end point of the gradient.











### nodes.gradient.RadialGradient.cx<span class="type-signature type int">Int</span>
{:#members:nodes-gradient-radialgradient-cx}








The starting X-Axis for the region




Default Value:
{:.param}






* 0








Example
{:.example}


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
</script>{% endhighlight %}







### nodes.gradient.RadialGradient.cy<span class="type-signature type int">Int</span>
{:#members:nodes-gradient-radialgradient-cy}








The ending X-Axis for the region




Default Value:
{:.param}






* 0








Example
{:.example}


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
</script>{% endhighlight %}







### nodes.gradient.RadialGradient.fx<span class="type-signature type int">Int</span>
{:#members:nodes-gradient-radialgradient-fx}








The starting X-Axis for the region




Default Value:
{:.param}






* 0








Example
{:.example}


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
</script>{% endhighlight %}







### nodes.gradient.RadialGradient.fy<span class="type-signature type int">Int</span>
{:#members:nodes-gradient-radialgradient-fy}








The ending Y-Axis for the region




Default Value:
{:.param}






* 0








Example
{:.example}


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
</script>{% endhighlight %}







### nodes.gradient.RadialGradient.stops<span class="type-signature type array">Array</span>
{:#members:nodes-gradient-radialgradient-stops}








The stop region for the gradient




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
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
</script>{% endhighlight %}







### nodes.gradient.Stop<span class="type-signature type object">object</span>
{:#members:nodes-gradient-stop}








Specifies the stops of the node gradients.











### nodes.gradient.Stop.color<span class="type-signature type string">String</span>
{:#members:nodes-gradient-stop-color}








The color of applied gradient




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
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
</script>{% endhighlight %}







### nodes.gradient.Stop.offset<span class="type-signature type int">Int</span>
{:#members:nodes-gradient-stop-offset}








To set desired offset to apply color to the node region




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
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
</script>{% endhighlight %}







### nodes.gradient.Stop.opacity<span class="type-signature type int">Int</span>
{:#members:nodes-gradient-stop-opacity}








Decribes the transparency level for the region




Default Value:
{:.param}






* 1








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
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
</script>{% endhighlight %}







### nodes.header<span class="type-signature type obj">obj</span>
{:#members:nodes-header}








The header of the swimlane. Applicable if the type is group.




Default Value:
{:.param}






* "Null"








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane",  header: {text: "Header", width:50}}});
</script>{% endhighlight %}







### nodes.height<span class="type-signature type int">Int</span>
{:#members:nodes-height}








To set the height of the node




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{height: 100}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.horizontalAlign<span class="type-signature type horizontalalignment"><a href="global.html#HorizontalAlignment">HorizontalAlignment</a></span>
{:#members:nodes-horizontalalign}








To set the horizontal alignment of node. Applicable if the type is group.




Default Value:
{:.param}






* HorizontalAlignment.Left








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script> 
node={name:"node1", ej.datavisualization.Diagram.HorizontalAlignment.Left};
$("#diagramcontent").ejDiagram({nodes:[node]});
</script>{% endhighlight %}







### nodes.inEdges<span class="type-signature type array">Array</span>
{:#members:nodes-inedges}








Collection of incoming connectors/edges of the node




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connectors = [{ name: "connector1", sourceNode: "Node1", targetNode: "Node2"}];
nodes=[{inEdges:connectors}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.isSwimlane<span class="type-signature type boolean">Boolean</span>
{:#members:nodes-isswimlane}








Indicates class as swimlane. Applicable if type is swimlane.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script> 
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane",  isSwimlane: true}});
</script>{% endhighlight %}







### nodes.labels<span class="type-signature type array">Array</span>
{:#members:nodes-labels}








To set the collection of labels to node




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var label = [];
label = { "text": "Node1", "fontColor": "Red"};
nodes=[{labels:label}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.labels.bold<span class="type-signature type boolean">Boolean</span>
{:#members:nodes-labels-bold}








Enables/disables the bold style of label




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node=[{labels:{"bold": false}}];
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.labels.borderColor<span class="type-signature type string">String</span>
{:#members:nodes-labels-bordercolor}








Sets border color of the text




Default Value:
{:.param}






* "transparent"








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node=[{labels:{borderColor: "transparent"}}];
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.labels.borderWidth<span class="type-signature type number">Number</span>
{:#members:nodes-labels-borderwidth}








Sets the border width of the label




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node=[{labels:{borderWidth: 4}}];
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.labels.fillColor<span class="type-signature type string">String</span>
{:#members:nodes-labels-fillcolor}








Sets the color that is used to fill text




Default Value:
{:.param}






* "transparent"








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node=[{labels:{fillColor: "green"}}];
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.labels.fontColor<span class="type-signature type string">String</span>
{:#members:nodes-labels-fontcolor}








To set the text color




Default Value:
{:.param}






* "black"








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node=[{labels:{"fontColor": "black"}}];
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.labels.fontFamily<span class="type-signature type string">String</span>
{:#members:nodes-labels-fontfamily}








To set the font family of the label




Default Value:
{:.param}






* "arial"








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node=[{labels:{"fontFamily": "Arial"}}];
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.labels.fontSize<span class="type-signature type integer">Integer</span>
{:#members:nodes-labels-fontsize}








To set font size of the label




Default Value:
{:.param}






* 12








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node=[{labels:{"fontSize": 12}}];
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.labels.horizontalAlignment<span class="type-signature type enum">Enum</span>
{:#members:nodes-labels-horizontalalignment}








Horizontal alignment of text in an element see<a href="global.html#HorizontalAlignment">HorizontalAlignment</a>




Default Value:
{:.param}






* HorizontalAlignment.Center








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node=[{labels:{horizontalAlignment: ej.datavisualization.Diagram.HorizontalAlignment.Center}}];
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.labels.italic<span class="type-signature type boolean">Boolean</span>
{:#members:nodes-labels-italic}








Enables/disables the italic font style of label




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node=[{labels:{"italic": false}}];
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.labels.margin<span class="type-signature type object">Object</span>
{:#members:nodes-labels-margin}








To set the margin of the label




Default Value:
{:.param}






* ej.datavisualization.Diagram.Margin()








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node=[{labels:{"margin": ej.datavisualization.Diagram.Margin()}}];
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.labels.mode<span class="type-signature type enum">Enum</span>
{:#members:nodes-labels-mode}








To set the label edit mode see<a href="global.html#LabelEditMode">LabelEditMode</a>




Default Value:
{:.param}






* LabelEditMode.Edit








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node=[{labels:{mode: ej.datavisualization.Diagram.LabelEditMode.Edit}}];
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.labels.name<span class="type-signature type string">String</span>
{:#members:nodes-labels-name}








Name of the label




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node=[{labels:{name:"Label"}}];
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.labels.offset<span class="type-signature type point">Point</span>
{:#members:nodes-labels-offset}








Ratio with respect to which the label is to be placed




Default Value:
{:.param}






* Point(0.5, 0.5)








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node=[{labels:{offset: ej.datavisualization.Diagram.Point(0.5, 0.5)}}];
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.labels.readOnly<span class="type-signature type boolean">Boolean</span>
{:#members:nodes-labels-readonly}








Allows the label to be read only




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node=[{labels:{"readOnly": false}}];
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.labels.rotateAngle<span class="type-signature type number">Number</span>
{:#members:nodes-labels-rotateangle}








To set the rotation angle of the label




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node=[{labels:{rotateAngle: 90}}];
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.labels.text<span class="type-signature type string">String</span>
{:#members:nodes-labels-text}








Sets text for the label




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node=[{labels:{"text": "Label"}}];
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.labels.textAlign<span class="type-signature type enum">Enum</span>
{:#members:nodes-labels-textalign}








Alignment of text in an element see <a href="global.html#TextAlign">TextAlign</a>




Default Value:
{:.param}






* TextAlign.Center








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node=[{labels:{textAlign: ej.datavisualization.Diagram.TextAlign.Center}}];
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.labels.textDecoration<span class="type-signature type enum">Enum</span>
{:#members:nodes-labels-textdecoration}








To set the text decoration for the label see<a href="global.html#TextDecorations">TextDecorations</a>




Default Value:
{:.param}






* TextDecorations.None








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node=[{labels:{textDecoration: ej.datavisualization.Diagram.TextDecorations.Underline}}];
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.labels.verticalAlignment<span class="type-signature type enum">Enum</span>
{:#members:nodes-labels-verticalalignment}








Vertical alignment of text in an element see<a href="global.html#VerticalAlignment">VerticalAlignment</a>




Default Value:
{:.param}






* VerticalAlignment.Center








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node=[{labels:{verticalAlignment: ej.datavisualization.Diagram.VerticalAlignment.Center}}];
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.labels.visible<span class="type-signature type boolean">Boolean</span>
{:#members:nodes-labels-visible}








Enables or disables the visibility of the label




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node=[{labels:{visible: true}}];
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.labels.width<span class="type-signature type interger">Interger</span>
{:#members:nodes-labels-width}








To set the width of the label




Default Value:
{:.param}






* 50








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node=[{labels:{width: 50}}];
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.labels.wrapping<span class="type-signature type enum">Enum</span>
{:#members:nodes-labels-wrapping}








To set the wrapping behavior of text see <a href="global.html#TextWrapping">TextWrapping</a>




Default Value:
{:.param}






* TextWrapping.WrapWithOverflow








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node=[{labels:{wrapping: ej.datavisualization.Diagram.TextWrapping.Wrap}}];
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.lanes<span class="type-signature type array">Array</span>
{:#members:nodes-lanes}








Collection of Lanes in swimlane. Applicable if type is swimlane.




Default Value:
{:.param}






* []








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var lanes = []; 
lanes=[{["Lane1","Lane1"]}];
$("#diagramcontent").ejDiagram( );
var nodes = [ {type: "swimlane",name: "swimlane",lanes: []}
</script>{% endhighlight %}







### nodes.lanes.addInfo<span class="type-signature type object">Object</span>
{:#members:nodes-lanes-addinfo}








To provide/save extra information about Lane




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({nodes:{type: "lane",name: "lane",{addInfo: addInfo}}});
</script>{% endhighlight %}







### nodes.lanes.children<span class="type-signature type array">Array</span>
{:#members:nodes-lanes-children}








The children of the lane. Applicable if type is lane.




Default Value:
{:.param}






* []








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", lanes:[{children:[]}]}});
</script>{% endhighlight %}







### nodes.lanes.fillColor<span class="type-signature type string">String</span>
{:#members:nodes-lanes-fillcolor}








The color to be filled inside the lane. Applicable if type is lane.




Default Value:
{:.param}






* "White"








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", lanes:[{fillColor: "white"}]}});
</script>{% endhighlight %}







### nodes.lanes.header<span class="type-signature type obj">obj</span>
{:#members:nodes-lanes-header}








The header of the lane . Applicable if the type is group.




Default Value:
{:.param}






* "Null"








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", lanes:[{header: {text: "Header", width:50}}]}});
</script>{% endhighlight %}







### nodes.lanes.isLane<span class="type-signature type boolean">Boolean</span>
{:#members:nodes-lanes-islane}








Indicates class as lane. Applicable if type is lane.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script> 
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", lanes:[{isLane:true}]}});
</script>{% endhighlight %}







### nodes.lanes.labels<span class="type-signature type string">String</span>
{:#members:nodes-lanes-labels}








The label shown inside the lane. Applicable if type is lane.




Default Value:
{:.param}






* "White"








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", lanes:[{labels: [{text:"Label"}]}]}});
</script>{% endhighlight %}







### nodes.lanes.name<span class="type-signature type string">String</span>
{:#members:nodes-lanes-name}








The name of the lane. Applicable if type is lane.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", lanes:[{name:"lane"}]}});
</script>{% endhighlight %}







### nodes.lanes.orientation<span class="type-signature type string">String</span>
{:#members:nodes-lanes-orientation}








The orientation type of the lane. Applicable if type is lane.




Default Value:
{:.param}






* "vertical"








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", lanes:[{orientation:"horizontal"}]}});
</script>{% endhighlight %}







### nodes.marginBottom<span class="type-signature type int">Int</span>
{:#members:nodes-marginbottom}








To set bottom margin of the node. Applicable if the type is group.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
node={name:"node1",marginBottom: 1};
$("#diagramcontent").ejDiagram({nodes:[node]});
</script>{% endhighlight %}







### nodes.marginLeft<span class="type-signature type int">Int</span>
{:#members:nodes-marginleft}








To set left margin of the node. Applicable if the type is group.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{marginLeft: 1}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.marginRight<span class="type-signature type int">Int</span>
{:#members:nodes-marginright}








To set right of for the node. Applicable if the type is group.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
node={name:"node1",marginRight: 1};
$("#diagramcontent").ejDiagram({nodes:[node]});
</script>{% endhighlight %}







### nodes.marginTop<span class="type-signature type int">Int</span>
{:#members:nodes-margintop}








To set top margin of the node. Applicable if the type is group.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
node={name:"node1",marginTop: 1};
$("#diagramcontent").ejDiagram({nodes:[node]});
</script>{% endhighlight %}







### nodes.maxHeight<span class="type-signature type int">Int</span>
{:#members:nodes-maxheight}








To set maximum height for the node. Applicable if the type is group.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
node={name:"node1",maxHeight: 1};
$("#diagramcontent").ejDiagram({nodes:[node]});
</script>{% endhighlight %}







### nodes.maxWidth<span class="type-signature type int">Int</span>
{:#members:nodes-maxwidth}








To set maximum width for the node. Applicable if the type is group.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
node={name:"node1",maxWidth: 1};
$("#diagramcontent").ejDiagram({nodes:[node]});
</script>{% endhighlight %}







### nodes.minHeight<span class="type-signature type int">Int</span>
{:#members:nodes-minheight}








To set minimum height for the node. Applicable if the type is group.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
node={name:"node1",minHeight: 1};
$("#diagramcontent").ejDiagram({nodes:[node]});
</script>{% endhighlight %}







### nodes.minWidth<span class="type-signature type int">Int</span>
{:#members:nodes-minwidth}








To set minimum width for the node. Applicable if the type is group.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
node={name:"node1",minWidth: 1};
$("#diagramcontent").ejDiagram({nodes:[node]});
</script>{% endhighlight %}







### nodes.name<span class="type-signature type string">String</span>
{:#members:nodes-name}








To set the name to the node




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{name:"Node1"}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.offsetX<span class="type-signature type int">Int</span>
{:#members:nodes-offsetx}








Sets the position of the node on X-Axis




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{offsetX: 100}];
$("#diagramcontent").ejDiagram({nodes:nodes});
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane",offsetX:100}});
</script>{% endhighlight %}







### nodes.offsetY<span class="type-signature type int">Int</span>
{:#members:nodes-offsety}








Sets the position of the node on Y-Axis




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{offsetY: 100}];
$("#diagramcontent").ejDiagram({nodes:nodes});          
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane",offsetY:100}});
</script>{% endhighlight %}







### nodes.opacity<span class="type-signature type number">Number</span>
{:#members:nodes-opacity}








Defines the transparency of the node




Default Value:
{:.param}






* 1








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{opacity: 2}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.orientation<span class="type-signature type string">String</span>
{:#members:nodes-orientation}








The orientation type of the swimlane. Applicable if type is swimlane.




Default Value:
{:.param}






* "vertical"








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane",  orientation: "vertical"}});
</script>{% endhighlight %}







### nodes.outEdges<span class="type-signature type array">Array</span>
{:#members:nodes-outedges}








Collection of outgoing connectors/edges of the node




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var connectors = [{ name: "connector1", sourceNode: "Node1", targetNode: "Node2"}];
nodes=[{outEdges:connectors}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.paddingBottom<span class="type-signature type int">Int</span>
{:#members:nodes-paddingbottom}








To set bottom padding value to the group. Applicable if the type is group.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{paddingBottom: 1}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.paddingLeft<span class="type-signature type int">Int</span>
{:#members:nodes-paddingleft}








To set left padding value to the group. Applicable if the type is group.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{paddingLeft: 1}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.paddingRight<span class="type-signature type int">Int</span>
{:#members:nodes-paddingright}








To set Right padding value to the group. Applicable if the type is group.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{paddingRight: 1}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.paddingTop<span class="type-signature type int">Int</span>
{:#members:nodes-paddingtop}








To set Top padding value to the group. Applicable if the type is group.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{paddingTop: 1}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.parent<span class="type-signature type string">String</span>
{:#members:nodes-parent}








Sets the parent name of the node




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node = [ {name: "rect",parent:"group1"}];
</script>{% endhighlight %}







### nodes.pathData<span class="type-signature type string">String</span>
{:#members:nodes-pathdata}








Sets the path geometry that defines the shape of the path node




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node={[shape:{type:"path",pathData:"M 269.711,29.3333C 269.711,44.061 257.772,56 243.044,56L 158.058,56C 143.33z"}]};
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.phases<span class="type-signature type array">Array</span>
{:#members:nodes-phases}








Collection of phases in swimlane node. Applicable if type is swimlane.




Default Value:
{:.param}






* []








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var phases = []; 
phases=[{["phase1","phase2"]}];
$("#diagramcontent").ejDiagram( );
var nodes = [ {type: "swimlane",name: "swimlane",phases: []}
</script>{% endhighlight %}







### nodes.phases.label<span class="type-signature type obj">obj</span>
{:#members:nodes-phases-label}








Sets the label of the phase. Applicable if type is lane.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", phases:[{label:{text:"label"}}]}});
</script>{% endhighlight %}







### nodes.phases.lineColor<span class="type-signature type string">String</span>
{:#members:nodes-phases-linecolor}








Sets the line color of the phase. Applicable if type is lane.




Default Value:
{:.param}






* "#606060"








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", phases:[{lineColor: "#606060"}]}});
</script>{% endhighlight %}







### nodes.phases.lineDashArray<span class="type-signature type string">String</span>
{:#members:nodes-phases-linedasharray}








Sets the line dash drray of the phase. Applicable if type is lane.




Default Value:
{:.param}






* "3,3"








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", phases:[{lineDashArray: "3,3"}]}});
</script>{% endhighlight %}







### nodes.phases.lineWidth<span class="type-signature type int">Int</span>
{:#members:nodes-phases-linewidth}








Sets the line width of the phase. Applicable if type is lane.




Default Value:
{:.param}






* "1"








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", phases:[{lineWidth: 1}]}});
</script>{% endhighlight %}







### nodes.phases.name<span class="type-signature type string">String</span>
{:#members:nodes-phases-name}








Defines the name of the phase. Applicable if type is lane.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", phases:[{name:"lane"}]}});
</script>{% endhighlight %}







### nodes.phases.offset<span class="type-signature type int">Int</span>
{:#members:nodes-phases-offset}








Sets the offset of the phase. Applicable if type is lane.




Default Value:
{:.param}






* "0"








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", phases:[{offset: 100}]}});
</script>{% endhighlight %}







### nodes.phases.orientation<span class="type-signature type string">String</span>
{:#members:nodes-phases-orientation}








Sets the orientation of the phase. Applicable if type is lane.




Default Value:
{:.param}






* "horizontal"








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", phases:[{orientation: "horizontal"}]}});
</script>{% endhighlight %}







### nodes.phases.parent<span class="type-signature type string">String</span>
{:#members:nodes-phases-parent}








Sets the parent of the phase. Applicable if type is lane.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", phases:[{parent: "parent"}]}});
</script>{% endhighlight %}







### nodes.phases.type<span class="type-signature type string">String</span>
{:#members:nodes-phases-type}








Sets the type of the phase. Applicable if type is lane.




Default Value:
{:.param}






* "phase"








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane", phases:[{type: "phase"}]}});
</script>{% endhighlight %}







### nodes.phaseSize<span class="type-signature type int">Int</span>
{:#members:nodes-phasesize}








To set phase size for the swimlane. Applicable if type is swimlane.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script> 
$("#diagramcontent").ejDiagram({nodes:{type: "swimlane",name: "swimlane",phaseSize:100}});
</script>{% endhighlight %}







### nodes.pivot<span class="type-signature type point">Point</span>
{:#members:nodes-pivot}








To set the pivot point of the node




Default Value:
{:.param}






* Points(0.5,0.5)








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{pivot: ej.datavisualization.Diagram.Point(0.8, 0.8)}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.points<span class="type-signature type array">Array</span>
{:#members:nodes-points}








Defines the collection of points to draw polygon node




Default Value:
{:.param}






* []








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node={[shape: { type: "polygon", points:[{ x: 0, y: 12.5 }, { x: 0, y: 50 }, { x: 50, y: 50 }, { x: 50, y: 0 }, { x: 12.5, y: 0 }, { x: 0, y: 12.5 }]}]};
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.ports<span class="type-signature type array">Array</span>
{:#members:nodes-ports}








To add collection of ports to node




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var port: [{ offset: { x: 0, y: 0.5 }, name: "aport" }]
nodes=[{ports:port}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.ports.borderColor<span class="type-signature type string">String</span>
{:#members:nodes-ports-bordercolor}








Sets the border color of the port




Default Value:
{:.param}






* "#1a1a1a"








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node={ports:[{borderColor:"green"}]};
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.ports.borderWidth<span class="type-signature type number">Number</span>
{:#members:nodes-ports-borderwidth}








Sets the border width of the port




Default Value:
{:.param}






* 1








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node={ports:[{borderWidth: 1}]};
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.ports.connectorPadding<span class="type-signature type int">Int</span>
{:#members:nodes-ports-connectorpadding}








To set the distance to be left between the port and connections.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node = [{ports:[{connectorPadding:2}]}];
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.ports.constraints<span class="type-signature type enum">enum</span>
{:#members:nodes-ports-constraints}








Sets whether connections can be created with the port See <a href="global.html#PortConstraints">PortConstraints</a>




Default Value:
{:.param}






* PortConstraints.Connect








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node={ports:[{constraints: ej.datavisualization.Diagram.PortConstraints.Connect}]};
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.ports.fillColor<span class="type-signature type string">String</span>
{:#members:nodes-ports-fillcolor}








Sets the color that is used to fill port shapes




Default Value:
{:.param}






* "white"








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node={ports:[{fillColor:"green"}]};
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.ports.name;<span class="type-signature type string">String</span>
{:#members:nodes-ports-name;}








The name of port to be specified




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node={ports:[{ name: "port"}]};
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.ports.offset<span class="type-signature type point">Point</span>
{:#members:nodes-ports-offset}








Offset value to align the port




Default Value:
{:.param}






* Point(0, 0)








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node={ports:[{{ x: 0, y: 0.5 }}]};
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.ports.pathData<span class="type-signature type string">String</span>
{:#members:nodes-ports-pathdata}








Path data to draw the custom port




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node={ports:[{pathData:""}]};
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.ports.shape<span class="type-signature type enum">enum</span>
{:#members:nodes-ports-shape}








Sets the shape of the port See <a href="global.html#PortShapes">PortShapes</a>




Default Value:
{:.param}






* PortShapes.Square








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node={ports:[{shape: ej.datavisualization.Diagram.PortShapes.Square}]};
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.ports.size<span class="type-signature type number">Number</span>
{:#members:nodes-ports-size}








Sets the size of the port




Default Value:
{:.param}






* 8








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node={ports:[{size: 10}]};
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.ports.visibility<span class="type-signature type enum">enum</span>
{:#members:nodes-ports-visibility}








Enables or disables the visibility of port See <a href="global.html#PortVisibility">PortVisibility</a>




Default Value:
{:.param}






* PortVisibility.Default








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node={ports:[{visibility: ej.datavisualization.Diagram.PortVisibility.Default}]};
$("#diagramcontent").ejDiagram({nodes:port});
</script> {% endhighlight %}







### nodes.rotateAngle<span class="type-signature type number">Number</span>
{:#members:nodes-rotateangle}








To set the rotation angle of the node




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{rotateAngle: 120}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.shadow<span class="type-signature type object">Object</span>
{:#members:nodes-shadow}








To define the shadow behavior of node seeShadow




Default Value:
{:.param}






* Diagram.Shadow()








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[shadow:{distance: 5,angle:45,opacity:0.7}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.shadow.angle<span class="type-signature type integer">Integer</span>
{:#members:nodes-shadow-angle}








Defines the angle difference to be set between object and shadow




Default Value:
{:.param}






* 45








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node={[shadow:{angle:50}]};
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.shadow.distance<span class="type-signature type integer">Integer</span>
{:#members:nodes-shadow-distance}








Defines the distance to be left between object and shadow




Default Value:
{:.param}






* 5








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node={[shadow:{distance:7}]};
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.shadow.opacity<span class="type-signature type float">float</span>
{:#members:nodes-shadow-opacity}








Defines the opacity of the shadow




Default Value:
{:.param}






* 0.7








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node={[shadow:{opacity:0.9}]};
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.shape<span class="type-signature type enum">Enum</span>
{:#members:nodes-shape}








Sets the shape of the node. It depends upon the type of node. See {Link Shapes}




Default Value:
{:.param}






* "rectangle"








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[shape: "rectangle"}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.source<span class="type-signature type string">String</span>
{:#members:nodes-source}








Sets the source location of the image node




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node={[shape:{type:"image",source:"Syncfusion.png"}]};
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.subProcess<span class="type-signature type object">object</span>
{:#members:nodes-subprocess}








Defines the subProcess of BPMN Activity and it is applicable, if the Activity type is "subProcess"




Default Value:
{:.param}






* Diagram.BPMNSubProcess()








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{type: "bpmn", activity: "subProcess", subProcess:{loop: ej.datavisualization.Diagram.BPMNLoops.Standard}}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.subProcess.adhoc<span class="type-signature type boolean">Boolean</span>
{:#members:nodes-subprocess-adhoc}








To set whether the process is adhoc or not




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{type: "bpmn", activity: "task", subProcess:{adhoc: false}}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.subProcess.boundary<span class="type-signature type enum">enum</span>
{:#members:nodes-subprocess-boundary}








Sets the boundary of the BPMN process See <a href="global.html#BPMNBoundary">BPMNBoundary</a>




Default Value:
{:.param}






* ej.datavisualization.Diagram.BPMNBoundary.Default








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{type: "bpmn", activity: "task", subProcess:{boundary: ej.datavisualization.Diagram.BPMNBoundary.Default}}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.subProcess.compensation<span class="type-signature type boolean">Boolean</span>
{:#members:nodes-subprocess-compensation}








To set whether the process is a compensation process or not




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{type: "bpmn", activity: "task", subProcess:{compensation: false}}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.subProcess.loop<span class="type-signature type enum">enum</span>
{:#members:nodes-subprocess-loop}








Sets the type of loop to a BPMN Process See <a href="global.html#BPMNLoops">BPMNLoops</a>




Default Value:
{:.param}






* ej.datavisualization.Diagram.BPMNLoops.None








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{type: "bpmn", activity: "task", subProcess:{loop: ej.datavisualization.Diagram.BPMNLoops.Standard}}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.task<span class="type-signature type object">object</span>
{:#members:nodes-task}








Defines the task of BPMN Activity and it is applicable, if Activity type is "task"




Default Value:
{:.param}






* Diagram.BPMNTask()








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{type: "bpmn", activity: "task", task:{loop: ej.datavisualization.Diagram.BPMNLoops.Standard}}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.tasks.call<span class="type-signature type boolean">Boolean</span>
{:#members:nodes-tasks-call}








To set whether the task is a global task or not




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{type: "bpmn", activity: "task", task:{call: false}}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.tasks.compensation<span class="type-signature type boolean">Boolean</span>
{:#members:nodes-tasks-compensation}








To set whether the task is a compensation task or not




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{type: "bpmn", activity: "task", task:{compensation: false}}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.tasks.loop<span class="type-signature type enum">enum</span>
{:#members:nodes-tasks-loop}








Sets the type of loop to a BPMN task See <a href="global.html#BPMNLoops">BPMNLoops</a>




Default Value:
{:.param}






* ej.datavisualization.Diagram.BPMNLoops.None








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{type: "bpmn", activity: "task", task:{loop: ej.datavisualization.Diagram.BPMNLoops.Standard}}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.tasks.type<span class="type-signature type enum">enum</span>
{:#members:nodes-tasks-type}








Sets the type of the BPMN task See <a href="global.html#BPMNTasks">BPMNTasks</a>




Default Value:
{:.param}






* ej.datavisualization.Diagram.BPMNTasks.None








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{type: "bpmn", activity: "task", task:{type: ej.datavisualization.Diagram.BPMNTasks.Service}}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.templateId<span class="type-signature type string">string</span>
{:#members:nodes-templateid}








Sets the template id of native/html nodes




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[]; 
node={[shape: { type: "text", templateId: "templateId" }]};
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.textBlock<span class="type-signature type integer">Integer</span>
{:#members:nodes-textblock}








Defines the textBlock and it is applicable in case of text node




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
var textBlock = ej.datavisualization.Diagram.TextBlockDefaults;
textBlock.text = "TextNode";
node={[shape: { type: "text", textBlock: textBlock }]};
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.trigger<span class="type-signature type enum">enum</span>
{:#members:nodes-trigger}








Sets the type of BPMN Event Trigger See <a href="global.html#BPMNTriggers">BPMNTriggers</a>




Default Value:
{:.param}






* ej.datavisualization.Diagram.BPMNTriggers.None








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{type: "bpmn", shape: ej.datavisualization.Diagram.BPMNShapes.Event, trigger: ej.datavisualization.Diagram.BPMNTriggers.None}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.type<span class="type-signature type enum">enum</span>
{:#members:nodes-type}








The type of node See <a href="global.html#Shapes">Shapes</a>




Default Value:
{:.param}






* ej.datavisualization.Diagram.Shapes.Basic








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var node=[];
node={[shape:{type:"rectangle"}]};
$("#diagramcontent").ejDiagram({nodes:node});
</script>{% endhighlight %}







### nodes.vertical Align<span class="type-signature type verticalalignment"><a href="global.html#VerticalAlignment">VerticalAlignment</a></span>
{:#members:nodes-vertical}








To set the Vertical alignment of node. Applicable if the type is group.




Default Value:
{:.param}






* VerticalAlignment.Top








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
node={name:"node1",VerticalAlignment: ej.datavisualization.Diagram.VerticalAlignment.Top};
$("#diagramcontent").ejDiagram({nodes:[node]});
</script>{% endhighlight %}







### nodes.visible<span class="type-signature type boolean">Boolean</span>
{:#members:nodes-visible}








To set the visibility of the node




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{visible: true}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.width<span class="type-signature type int">Int</span>
{:#members:nodes-width}








To set the width of the node




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{width: 100}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodes.zOrder<span class="type-signature type int">Int</span>
{:#members:nodes-zorder}








To set the Zorder of the node




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var nodes = [];
nodes=[{zOrder: 1}];
$("#diagramcontent").ejDiagram({nodes:nodes});
</script>{% endhighlight %}







### nodeTemplate<span class="type-signature type object">object</span>
{:#members:nodetemplate}








To customize the node properties before rendering the node.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="diagram"></div>
<script>
function nodeTemplate(diagram, node) {node.labels[0].text = node.Name};
$("#diagram").ejDiagram({ nodeTemplate:nodeTemplate});
</script>{% endhighlight %}







### pageSettings
{:#members:pagesettings}








To define the page settings of diagram











### pageSettings.multiplePage<span class="type-signature type boolean">Boolean</span>
{:#members:pagesettings-multiplepage}








To set whether the number of pages can be extended based on the region covered by elements




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
//multiplePage of the diagram
$("#diagramContent").ejDiagram({pageSettings: {multiplePage: false}}); {% endhighlight %}







### pageSettings.pageBackgroundColor<span class="type-signature type string">String</span>
{:#members:pagesettings-pagebackgroundcolor}








To set the background color of page




Default Value:
{:.param}






* "#ffffff"








Example
{:.example}


{% highlight html %}
 
//pageBackgroundColor of the diagram
$("#diagramContent").ejDiagram({pageSettings: {pageBackgroundColor: "#ffffff"}}); {% endhighlight %}







### pageSettings.pageBorderColor<span class="type-signature type string">String</span>
{:#members:pagesettings-pagebordercolor}








To set the border color of page




Default Value:
{:.param}






* "#565656"








Example
{:.example}


{% highlight html %}
 
//pageBorderColor of the diagram
$("#diagramContent").ejDiagram({pageSettings: {pageBorderColor: "#565656"}}); {% endhighlight %}







### pageSettings.pageBorderWidth<span class="type-signature type number">Number</span>
{:#members:pagesettings-pageborderwidth}








To set the border width of the page




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
//pageBorderWidth of the diagram
$("#diagramContent").ejDiagram({pageSettings: {pageBorderWidth: 3}}); {% endhighlight %}







### pageSettings.pageHeight<span class="type-signature type number">Number</span>
{:#members:pagesettings-pageheight}








To set the height of the page




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
//pageHeight of the diagram
$("#diagramContent").ejDiagram({pageSettings: {pageHeight: 4500}}); {% endhighlight %}







### pageSettings.pageMargin<span class="type-signature type number">Number</span>
{:#members:pagesettings-pagemargin}








To set the margin of page




Default Value:
{:.param}






* 24








Example
{:.example}


{% highlight html %}
 
//pageMargin of the diagram
$("#diagramContent").ejDiagram({pageSettings: {pageMargin: 24}}); {% endhighlight %}







### pageSettings.pageWidth<span class="type-signature type number">Number</span>
{:#members:pagesettings-pagewidth}








To set the width of the page




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
//pageWidth
$("#diagramContent").ejDiagram({pageSettings: {pageWidth: 4500}}); {% endhighlight %}







### pageSettings.showPageBreak<span class="type-signature type boolean">Boolean</span>
{:#members:pagesettings-showpagebreak}








Enables or disables the page breaks in diagram




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
//showPageBreak of the diagram
$("#diagramContent").ejDiagram({pageSettings: {showPageBreak: false}}); {% endhighlight %}







### selectedItems<span class="type-signature type object">object</span>
{:#members:selecteditems}








The object to define the behavior of the selected items











### selectedItems.constraints<span class="type-signature type enum">enum</span>
{:#members:selecteditems-constraints}








Sets the visible items of selector see <a href="global.html#SelectorConstraints">SelectorConstraints</a>




Default Value:
{:.param}






* SelectorConstraints.All








Example
{:.example}


{% highlight html %}
 
<div id="diagramcontent"></div>
<script>
$("#diagramContent").ejDiagram({selectedItems:{constraints: ej.datavisualization.Diagram.SelectorConstraints.None} }}); 
</script>{% endhighlight %}







### selectedItems.height<span class="type-signature type number">Number</span>
{:#members:selecteditems-height}








Sets the height of the selected items




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
$("#diagramContent").ejDiagram({selectedItems: {height: 50}}); {% endhighlight %}







### selectedItems.offsetX<span class="type-signature type number">Number</span>
{:#members:selecteditems-offsetx}








Defines the X co-ordinate of the selected item




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
$("#diagramContent").ejDiagram({selectedItems: {offsetX: 50}}); {% endhighlight %}







### selectedItems.offsetY<span class="type-signature type number">Number</span>
{:#members:selecteditems-offsety}








Defines the Y co-ordinate of the selected item




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
$("#diagramContent").ejDiagram({selectedItems: {offsetY: 50}}); {% endhighlight %}







### selectedItems.rotateAngle<span class="type-signature type number">Number</span>
{:#members:selecteditems-rotateangle}








Sets the rotation angle of the selected items.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
$("#diagramContent").ejDiagram({selectedItems: {rotateAngle: 50}}); {% endhighlight %}







### selectedItems.userHandles<span class="type-signature type array">array</span>
{:#members:selecteditems-userhandles}








To add frequently using commands around selector




Default Value:
{:.param}






* []








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var userHandle= [];
function createUserHandles() {
var cloneHandle = ej.datavisualization.Diagram.UserHandle();
userhandle.push(cloneHandles);
}
$("#diagramcontent").ejDiagram({selectedItems:{userHandles:userHandle}});
</script>{% endhighlight %}







### selectedItems.width<span class="type-signature type number">Number</span>
{:#members:selecteditems-width}








Sets the width of the selected items




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
$("#diagramContent").ejDiagram({selectedItems: {width: 50}}); {% endhighlight %}







### showTooltip<span class="type-signature type boolean">Boolean</span>
{:#members:showtooltip}








Enables or disables tooltip of diagram




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram({showTooltip: true});
</script>{% endhighlight %}







### snapSettings<span class="type-signature type object">object</span>
{:#members:snapsettings}








Specifies the snap settings of the diagram.











### snapSettings.enableSnapToObject<span class="type-signature type boolean">Boolean</span>
{:#members:snapsettings-enablesnaptoobject}








Enables or disables the snap to object




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
var snap = {"enableSnapToObject":true};
//enableSnapToObject: 
$("#diagramContent").ejDiagram({snapSettings: snap}); {% endhighlight %}







### snapSettings.horizontalGridLines<span class="type-signature type object">object</span>
{:#members:snapsettings-horizontalgridlines}








Specifies the settings of horizontal grid lines.











### snapSettings.horizontalGridLines.lineColor<span class="type-signature type string">string</span>
{:#members:snapsettings-horizontalgridlines-linecolor}








Sets the line color for horizontal gridlines




Default Value:
{:.param}






* "lightgray"








Example
{:.example}


{% highlight html %}
 
<div id="diagramcontent"></div>
<script>
var gridline = { "snapConstraints":"lineColor": "blue" };
//Linecolor of the horizontal gridlines
$("#diagramContent").ejDiagram({snapSettings: { horizontalGridLines: gridline} }); 
</script>{% endhighlight %}







### snapSettings.horizontalGridLines.lineDashArray<span class="type-signature type string">string</span>
{:#members:snapsettings-horizontalgridlines-linedasharray}








Specifies the pattern of dashes and gaps used to stroke horizontal grid lines




Default Value:
{:.param}






* "0"








Example
{:.example}


{% highlight html %}
 
<div id="diagram"></div>
<script>
$("#diagram").ejDiagram({ snapSettings: { horizontalGridLines: { lineDashArray: "2 2"}}}); 
</script>{% endhighlight %}







### snapSettings.horizontalGridLines.linesInterval<span class="type-signature type array">array</span>
{:#members:snapsettings-horizontalgridlines-linesinterval}








Specifies pattern of lines and gaps of horizontal gridlines




Default Value:
{:.param}






* [1.25, 18.75, 0.25, 19.75, 0.25, 19.75, 0.25, 19.75, 0.25, 19.75]








Example
{:.example}


{% highlight html %}
<div id="diagram"></div>
<script>
$("#diagram").ejDiagram({ snapSettings: { 
    horizontalGridLines: { linesInterval: [1, 14, 0.25, 15, 0.25, 15, 0.25, 15, 0.25, 15] }
}}); 
</script>{% endhighlight %}







### snapSettings.horizontalGridLines.snapInterval<span class="type-signature type array">array</span>
{:#members:snapsettings-horizontalgridlines-snapinterval}








Specifies the snap intervals of horizontal grid lines.




Default Value:
{:.param}






* [20]








Example
{:.example}


{% highlight html %}
 
<div id="diagram"></div>
<script>
$("#diagram").ejDiagram({ snapSettings: { horizontalGridLines: { snapInterval: [10] }}}); 
</script>{% endhighlight %}







### snapSettings.snapAngle<span class="type-signature type number">Number</span>
{:#members:snapsettings-snapangle}








The Angle by which the object to be snapped




Default Value:
{:.param}






* 5








Example
{:.example}


{% highlight html %}
 
var snap = {"snapAngle":5};
//enableSnapToObject: 
$("#diagramContent").ejDiagram({snapSettings: snap}); {% endhighlight %}







### snapSettings.snapObjectDistance<span class="type-signature type number">Number</span>
{:#members:snapsettings-snapobjectdistance}








Relative distance between the nearer object and selected object




Default Value:
{:.param}






* 5








Example
{:.example}


{% highlight html %}
 
var snap = {"snapObjectDistance":5};
//snapObjectDistance
$("#diagramContent").ejDiagram({snapSettings: snap}); {% endhighlight %}







### snapSettings.verticalGridLines<span class="type-signature type object">object</span>
{:#members:snapsettings-verticalgridlines}








Specifies the settings of vertical grid lines.











### snapSettings.verticalGridLines.lineColor<span class="type-signature type string">string</span>
{:#members:snapsettings-verticalgridlines-linecolor}








Sets the line color of vertical gridlines




Default Value:
{:.param}






* "lightgray"








Example
{:.example}


{% highlight html %}
 
<div id="diagramcontent"></div>
<script>
var gridline = { "snapConstraints":"lineColor": "blue" };
//Linecolor of the vertical gridlines
$("#diagramContent").ejDiagram({snapSettings: { verticalGridLines: gridline} });
</script>{% endhighlight %}







### snapSettings.verticalGridLines.lineDashArray<span class="type-signature type string">string</span>
{:#members:snapsettings-verticalgridlines-linedasharray}








Specifies the pattern of dashes and gaps used to stroke vertical grid lines




Default Value:
{:.param}






* "0"








Example
{:.example}


{% highlight html %}
 
<div id="diagram"></div>
<script>
$("#diagram").ejDiagram({ snapSettings: { verticalGridLines: { lineDashArray: "2 2"}}}); 
</script>{% endhighlight %}







### snapSettings.verticalGridLines.linesInterval<span class="type-signature type array">array</span>
{:#members:snapsettings-verticalgridlines-linesinterval}








Specifies pattern of lines and gaps of vertical gridlines




Default Value:
{:.param}






* [1.25, 18.75, 0.25, 19.75, 0.25, 19.75, 0.25, 19.75, 0.25, 19.75]








Example
{:.example}


{% highlight html %}
<div id="diagram"></div>
<script>
$("#diagram").ejDiagram({ snapSettings: { 
    verticalGridLines: { linesInterval: [1, 14, 0.25, 15, 0.25, 15, 0.25, 15, 0.25, 15] }
}}); 
</script>{% endhighlight %}







### snapSettings.verticalGridLines.snapInterval<span class="type-signature type array">array</span>
{:#members:snapsettings-verticalgridlines-snapinterval}








Specifies the snap intervals for vertical grid lines.




Default Value:
{:.param}






* [20]








Example
{:.example}


{% highlight html %}
 
<div id="diagram"></div>
<script>
$("#diagram").ejDiagram({ snapSettings: { verticalGridLines: { snapInterval: [10] }}}); 
</script>{% endhighlight %}







### tool<span class="type-signature type enum">enum</span>
{:#members:tool}








Sets the default behavior of the diagram see<a href="global.html#Tool">Tool</a>




Default Value:
{:.param}






* Tool.All








Example
{:.example}


{% highlight html %}
 
<div id="diagramcontent"></div>
<script>
$("#diagramContent").ejDiagram({tool: ej.datavisualization.Diagram.Tool.Default} }); 
</script>{% endhighlight %}







### tooltipTemplateId<span class="type-signature type string">String</span>
{:#members:tooltiptemplateid}








To set custom style for tool tip of diagram




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
         
<div id="diagramcontent"></div>
<script type="text/x-jsrender" id="toolTipId">
<span >{{:offsetX}}{{:x}}{{:offsetY}}{{:y}}
</span>
</script>
<script>
$("#diagramcontent").ejDiagram({ tooltipTemplateId: "toolTipId"});
</script>{% endhighlight %}







### version<span class="type-signature type string">String</span>
{:#members:version}








Sets the version of the diagram




Default Value:
{:.param}






* "13.1"








Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
$("#diagramcontent").ejDiagram("instance");
</script>{% endhighlight %}







### width<span class="type-signature type string">string</span>
{:#members:width}








Specifies the width of the diagram.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="diagram"></div>
<script>
$("#diagram").ejDiagram({ width:"100%" });
</script>{% endhighlight %}







### zoomFactor<span class="type-signature type number">Number</span>
{:#members:zoomfactor}








Sets the factor by which we can zoom in or zoom out




Default Value:
{:.param}






* 0.2








Example
{:.example}


{% highlight html %}
 
<div id="diagramcontent"></div>
<script>
$("#diagramContent").ejDiagram({zoomFactor: 1}); 
</script>{% endhighlight %}





## Methods


### add<span class="signature">(node)</span>
{:#methods:add}








Add nodes and connectors to diagram at runtime

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
<td class="name">{% highlight html %}
node{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">JSON to add a node/connector</td>
</tr>
</tbody>
</table>




Example
{:.example}


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


### addLabel<span class="signature">(nodeName, label)</span>
{:#methods:addLabel}

Add a label to a node at runtime

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
<td class="name">{% highlight html %}
name{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">of the node to add a label</td>
</tr>
<tr>
<td class="name">{% highlight html %}
label{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">to be added to the node specified by name</td>
</tr>
</tbody>
</table>

Example
{:.example}
{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
var node=diagram.selectionList[0];
diagram.addLabel(node.name, {fontColor:"red", text:"newLabel"});
</script>

{% endhighlight %}



### addPhase<span class="signature">(name, options)</span>
{:#methods:addphase}

Add a phase to a swimlane at runtime

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
<td class="name">{% highlight html %}
name{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">of the swimlane to add the phase</td>
</tr>
<tr>
<td class="name">{% highlight html %}
options{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">to define the phase to be added</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance"); 
diagram.addPhase("swimlane", { name: "CustomPhase", offset: 600, label: { text: "CustomPhase" } });
</script>
{% endhighlight %}







### addPorts<span class="signature">(name, ports)</span>
{:#methods:addports}








Add a collection of ports to the node specified by name

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
<td class="name">{% highlight html %}
name{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">to identify the node from the model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
ports{% endhighlight %}</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description last">collection of ports to be added to the specified node</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
        
<div id="diagramcontent"></div>
<script>
var diagram = $("#diagramcontent").ejDiagram("instance");
var port = [{ offset: { x: 0, y: 0.5 }, name: "aport", fillColor: "yellow"}, { offset: { x: 0.5, y: 0.5 }, name: "bport", fillColor: "yellow",  }];
diagram.addPorts("Rect1", port);
</script>

{% endhighlight %}







### addSelection<span class="signature">(node)</span>
{:#methods:addselection}


Add the specified node to selection list

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
<td class="name">{% highlight html %}
node{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">pass the node to be selected</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
var node=diagram.model.nodes[0];
diagram.addSelection(node);
</script>

{% endhighlight %}







### align<span class="signature">(direction)</span>
{:#methods:align}








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
<td class="name">{% highlight html %}
direction{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">To specify the direction towards which the selected objects are to be aligned("left","right",top","bottom")</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.align("left"); 
</script>{% endhighlight %}







### bringIntoView<span class="signature">(bounds)</span>
{:#methods:bringintoview}








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
<td class="name">{% highlight html %}
bounds{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">rectangular region that is to be brought into diagram viewport</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.bringIntoView(ej.datavisualization.Diagram.Rectangle(700, 500, 80, 80));
</script>{% endhighlight %}







### bringToCenter<span class="signature">(rect)</span>
{:#methods:bringtocenter}








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
<td class="name">{% highlight html %}
rect{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">rectangular region that is to be brought to the center of diagram viewport</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.bringToCenter(ej.datavisualization.Diagram.Rectangle(700, 500, 80, 80));
</script>{% endhighlight %}







### bringToFront<span class="signature">()</span>
{:#methods:bringtofront}








Visually move the selected object over all other intersected objects





Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.bringToFront(); 
</script>{% endhighlight %}







### clear<span class="signature">()</span>
{:#methods:clear}








Remove all the elements from diagram





Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.clear(); 
</script>{% endhighlight %}




### clearSelection<span class="signature">()</span>
{:#methods:clearSelection}

Remove the current selection in diagram

Example
{:.example}

{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.clearSelection(); 
</script>




{% endhighlight %}



### copy<span class="signature">()</span>
{:#methods:copy}








Copy the selected object to internal clipboard and get the copied object





Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
//Save the copied object
var obj = diagram.copy(); 
</script>
{% endhighlight %}







### cut<span class="signature">()</span>
{:#methods:cut}








Cut the selected object from diagram to diagram internal clipboard





Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.cut(); 
</script>

{% endhighlight %}



### exportDiagram<span class="signature">(options)</span>
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
<td class="name">{% highlight html %}
options{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
fileName{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">name of the file to be downloaded</td>
</tr>
<tr>
<td class="name">{% highlight html %}
format{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">format of the exported file/data See <a href="global.html#fileformats">FileFormats</a></td>
</tr>
<tr>
<td class="name">{% highlight html %}
mode{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">to set whether to export diagram as a file or as raw data See <a href="global.html#exportmodes">ExportModes</a></td>
</tr>
<tr>
<td class="name">{% highlight html %}
region{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">to set the region of the diagram to be exported See <a href="global.html#region">Region</a></td>
</tr>
<tr>
<td class="name">{% highlight html %}
bounds{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">to set the custom bounds that is to be exported</td>
</tr>
<tr>
<td class="name">{% highlight html %}
margin{% endhighlight %}</td>
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



### findNode<span class="signature">(nodeName)</span>

{:#methods:findNode}

Find a node/connector by its name

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
<td class="name">{% highlight html %}
name{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">name of the node/connector that is to be found</td>
</tr>
</tbody>
</table>

Example
{:.example}

{% highlight html %}

<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
var node = diagram.findNode("nodeName");
</script>





{% endhighlight %}



### fitToPage<span class="signature">(mode, region, margin)</span>
{:#methods:fittopage}




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
<td class="name">{% highlight html %}
mode{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">to set the mode of fit to command. See <a href="global.html#fitmode">FitMode</a></td>
</tr>
<tr>
<td class="name">{% highlight html %}
region{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">to set whether the region to be fit will be based on diagram elements or page settings <a href="global.html#region">Region</a></td>
</tr>
<tr>
<td class="name">{% highlight html %}
margin{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">to set the required margin</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
         
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.fitToPage(mode,region,margin);
</script>{% endhighlight %}







### group<span class="signature">()</span>
{:#methods:group}



Group the selected nodes and connectors





Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.group(); 
</script>

{% endhighlight %}



### insertLabel<span class="signature">(name, label, index)</span>
{:#methods:insertLabel}

Insert a label into a node's label collection at runtime

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
<td class="name">{% highlight html %}
name{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">of the node to add a label</td>
</tr>
<tr>
<td class="name">{% highlight html %}
label{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">to be added to the node specified by name</td>
</tr>
<tr>
<td class="name">{% highlight html %}
index{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last"> to insert the label into the node</td>
</tr>
</tbody>
</table>

Example
{:.example}
{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
var node=diagram.selectionList[0];
diagram.insertLabel(node.name, {fontColor:"red", text:"newLabel"},0);
</script>




{% endhighlight %}



### layout<span class="signature">()</span>
{:#methods:layout}





Refresh the diagram with the specified layout



Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.layout();
</script>{% endhighlight %}







### load<span class="signature">(data)</span>
{:#methods:load}



Load the diagram 

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
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">JSON data that is to be loaded as diagram</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.load(data);
</script>{% endhighlight %}







### moveForward<span class="signature">()</span>
{:#methods:moveforward}








Visually move the selected object over its closest intersected object





Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.moveForward(); 
</script>{% endhighlight %}







### nudge<span class="signature">(direction, delta)</span>
{:#methods:nudge}








Move the selected objects by either one pixel or by the pixels specified through argument

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
<td class="name">{% highlight html %}
direction{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">specifies the driection to move the selected objects ("left","right",top","bottom")</td>
</tr>
<tr>
<td class="name">{% highlight html %}
delta{% endhighlight %}</td>
<td class="type"><span class="param-type">Number</span></td>
<td class="description last">specifies the number of pixels by which the selected objects to be moved</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.nudge("direction", 5); 
</script>{% endhighlight %}







### paste<span class="signature">(object, rename)</span>
{:#methods:paste}








Paste the selected object from internal clipboard to diagram

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
<td class="name">{% highlight html %}
object{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">object to be pasted</td>
</tr>
<tr>
<td class="name">{% highlight html %}
rename{% endhighlight %}</td>
<td class="type"><span class="param-type">Boolean</span></td>
<td class="description last">to define whether the specified object is to be renamed or not</td>
</tr>
</tbody>
</table>



Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
//Paste the object from internal clipboard to diagram
diagram.paste(); 

//Add the specific object to diagram
diagram.paste(obj);
</script>

{% endhighlight %}







### print<span class="signature">()</span>
{:#methods:print}








Print the diagram as image





Example
{:.example}


{% highlight html %}
  
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.print();
</script>

{% endhighlight %}







### redo<span class="signature">()</span>
{:#methods:redo}








Restore the last action that was reverted





Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.redo(); 
</script>

{% endhighlight %}



### refresh<span class="signature">()</span>
{:#methods:refresh}

Refresh diagram at runtime

Example
{:.example}

{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.refresh(); 
</script>





{% endhighlight %}



### remove<span class="signature">(node)</span>
{:#methods:remove}



Remove either the given node/connector or the selected element from diagram

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
<td class="name">{% highlight html %}
node{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last"> node/connector to be removed</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.remove(); 
</script>

{% endhighlight %}




### removeSelection<span class="signature">(node)</span>
{:#methods:removeSelection}

Remove a particular object from selection list

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
<td class="name">{% highlight html %}
node{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last"> node/connector to be removed from selection list</td>
</tr>
</tbody>
</table>

Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
var node=diagram.selectionList[0];
diagram.removeSelection(node);
</script>




{% endhighlight %}



### sameHeight<span class="signature">()</span>
{:#methods:sameheight}



Scale the selected objects to the height of the first selected object





Example
{:.example}


{% highlight html %}
        
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.sameHeight(); 
</script>{% endhighlight %}







### sameSize<span class="signature">()</span>
{:#methods:samesize}








Scale the selected objects to the size of the first selected object





Example
{:.example}


{% highlight html %}
        
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.sameSize(); 
</script>{% endhighlight %}







### sameWidth<span class="signature">()</span>
{:#methods:samewidth}








Scale the selected objects to the width of the first selected object





Example
{:.example}


{% highlight html %}
        
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.sameWidth(); 
</script>{% endhighlight %}







### save<span class="signature">()</span>
{:#methods:save}








Save the diagram as serialized JSON

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


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
var savedDiagram = diagram.save();
</script>{% endhighlight %}







### scrollToNode<span class="signature">(node)</span>
{:#methods:scrolltonode}




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
<td class="name">{% highlight html %}
node{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">the node/connector to be brought into view</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
var node = diagram.selectionList[0];
diagram.scrollToNode(node); 
</script>{% endhighlight %}







### selectAll<span class="signature">()</span>
{:#methods:selectall}








Select all nodes and connector in diagram





Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.selectAll(); 
</script>{% endhighlight %}







### sendBackward<span class="signature">()</span>
{:#methods:sendbackward}








Visually move the selected object behind its closest intersected object





Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.sendBackward(); 
</script>{% endhighlight %}







### sendToBack<span class="signature">()</span>
{:#methods:sendtoback}








Visually move the selected object behind all other intersected objects





Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.sendToBack(); 
</script>{% endhighlight %}







### spaceAcross<span class="signature">()</span>
{:#methods:spaceacross}








Update horizontal space between the selected objects as equal and within the selection boundary





Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.spaceAcross(); 
</script>{% endhighlight %}







### spaceDown<span class="signature">()</span>
{:#methods:spacedown}








Update vertical space between the selected objects as equal and within the selection boundary





Example
{:.example}


{% highlight html %}
        
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.spaceDown(); 
</script>{% endhighlight %}







### startLabelEdit<span class="signature">(node, label)</span>
{:#methods:startlabeledit}








Start the editing of the specified label

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
<td class="name">{% highlight html %}
node{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">node/connector that contains the label to be edited</td>
</tr>
<tr>
<td class="name">{% highlight html %}
label{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">the label to be edited</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
var node=diagram.selectionList[0];
diagram.startLabelEdit(node,node.labels[0]);
</script>{% endhighlight %}







### undo<span class="signature">()</span>
{:#methods:undo}








Reverse the last action that was performed





Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.undo(); 
</script>{% endhighlight %}







### ungroup<span class="signature">()</span>
{:#methods:ungroup}








Ungroup the selected group





Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.ungroup(); 
</script>{% endhighlight %}







### update<span class="signature">(name, options)</span>
{:#methods:update}








Update diagram at runtime

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
<td class="name">{% highlight html %}
options{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">to specify the properties of diagram to be updated</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
var tool = ej.datavisualization.Diagram.Tool.ZoomPan;
//update the tool
diagram.update({ tool: tool });

{% endhighlight %}







### updateConnector<span class="signature">(name, options)</span>
{:#methods:updateconnector}








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
<td class="name">{% highlight html %}
name{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">to identify the connector from the model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
options{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">to specify the connector properties that have to be updated</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.updateConnector("connector1", { lineColor: "red", lineWidth: 3 });   
</script>{% endhighlight %}







### updateLabel<span class="signature">(nodeName, label, obj)</span>
{:#methods:updatelabel}








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
<td class="name">{% highlight html %}
nodeName{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">the name of node/connector which contains the label to be updated</td>
</tr>
<tr>
<td class="name">{% highlight html %}
label{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">the label to be modified</td>
</tr>
<tr>
<td class="name">{% highlight html %}
obj{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">the new porperties of the label</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
var node=diagram.selectionList[0];
var label = [];
label =[{"name":"node1" "text": "node", "bold": true, "italic": true}]
diagram.updateLabel(node.name,node.labels[0],label);
</script>{% endhighlight %}







### updateNode<span class="signature">(name, options)</span>
{:#methods:updatenode}








Update Node with its modified properties at runtime

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
<td class="name">{% highlight html %}
name{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">to identify the Node from the model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
options{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">to specify the properties of node that have to be updated</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.updateNode("node1", { fillColor: "red", borderWidth: "3" });
</script>
{% endhighlight %}



### updatePort<span class="signature">(nodeName, port, options)</span>
{:#methods:updatePort}

Update a port with its modified properties at runtime

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
<td class="name">{% highlight html %}
nodeName{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">the name of node which contains the port to be updated</td>
</tr>
<tr>
<td class="name">{% highlight html %}
label{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">the port to be updated</td>
</tr>
<tr>
<td class="name">{% highlight html %}
obj{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">the new porperties of the port</td>
</tr>
</tbody>
</table>

Example
{:.example}
{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
var node=diagram.selectionList[0];
var port ={fillColor:"red", visibility:ej.datavisualization.Diagram.PortVisibility.Visible}
diagram.updatePort(node.name,node.ports[0], port);
</script>





{% endhighlight %}



### updateSelectedObject<span class="signature">(name)</span>
{:#methods:updateselectedobject}








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
<td class="name">{% highlight html %}
name{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">to identify the object from the model</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance"); 
diagram.updateSelectedObject(name);    
</script>{% endhighlight %}







### updateSelection<span class="signature">(isDragging)</span>
{:#methods:updateselection}








Update the selection at runtime

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
<td class="name">{% highlight html %}
isDragging{% endhighlight %}</td>
<td class="type"><span class="param-type">Boolean</span></td>
<td class="description last">pass true/false whether the selected object is draggable or not</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.updateSelection(true);
</script>{% endhighlight %}







### updateUserHandles<span class="signature">(node)</span>
{:#methods:updateuserhandles}








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
<td class="name">{% highlight html %}
node{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">node/connector with respect to which, the user handles have to be updated</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
var node = diagram.selectionList[0];
diagram.updateUSerHandles(node); 
</script>{% endhighlight %}







### updateViewPort<span class="signature">()</span>
{:#methods:updateviewport}







Update the viewport at runtime





Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.updateViewPort();
</script>{% endhighlight %}







### upgrade<span class="signature">(data)</span>
{:#methods:upgrade}








Upgrade the diagram from old version

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
<td class="name">{% highlight html %}
data{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last"></td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
diagram.upgrade(jsonData);
diagram.load(jsonData);
</script>{% endhighlight %}







### zoomTo<span class="signature">(zoom)</span>
{:#methods:zoomto}








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
<td class="name">{% highlight html %}
zoom{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">options to zoom the diagram(zoom factor, zoomin/zoomout)</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



Example
{:.example}


{% highlight html %}
<div id="diagramcontent"></div>
<script>
var diagram=$("#diagramcontent").ejDiagram("instance");
var zoom =  ej.datavisualization.Diagram.Zoom();
zoom.zoomFactor = .1;
zoom.zoomCommand = ej.datavisualization.Diagram.ZoomCommand.ZoomIn;
diagram.zoomTo(zoom);
</script>{% endhighlight %}




## Events








### autoScrollChange
{:#events:autoscrollchange}








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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
delay{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">returns should be inserted or removed</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



Example
{:.example}


{% highlight html %}
// autoScrollChange event for diagram
$("#diagramcontent").ejDiagram({
autoScrollChange:function (args)  {}
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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns diagram/ diargram element that is clicked</td>
</tr>
<tr>
<td class="name">{% highlight html %}
count{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns the count of how many times the mouse button is pressed</td>
</tr>
<tr>
<td class="name">{% highlight html %}
event{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns the actual click arguments that explains which button is clicked</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



Example
{:.example}


{% highlight html %}
//  click event for diagram
$("#diagramcontent").ejDiagram({
click:function (args)  {}
        });{% endhighlight %}







### connectionChange
{:#events:connectionchange}








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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns the connection that is changed between nodes, ports or points</td>
</tr>
<tr>
<td class="name">{% highlight html %}
connection{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">parameter returns the changed source or target node of the connector</td>
</tr>
<tr>
<td class="name">{% highlight html %}
port{% endhighlight %}</td>
<td class="type"><span class="param-type">port</span></td>
<td class="description last">parameter returns the changed source or target port of the connector</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



Example
{:.example}


{% highlight html %}
// connectionChange event for diagram
$("#diagramcontent").ejDiagram({
connectionChange:function (args)  {}
        }); {% endhighlight %}







### connectorCollectionChange
{:#events:connectorcollectionchange}








Triggers when the connector collection is changed

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
changetype{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">return should be inserted or removed</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
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


{% highlight html %}
// connectorCollectionChange event for diagram
$("#diagramcontent").ejDiagram({
connectorCollectionChange:function (args) {}
        });{% endhighlight %}







### connectorSourceChange
{:#events:connectorsourcechange}








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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the connector, the source point of which is being dragged</td>
</tr>
<tr>
<td class="name">{% highlight html %}
point{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the source point of the element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
port{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">returns the source port of the element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
dragState{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">returns the state of connection end point dragging(starting, dragging, completed)</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



Example
{:.example}


{% highlight html %}
// connectorSourceChange event for diagram
$("#diagramcontent").ejDiagram({
connectorSourceChange:function (args)  {}
       });{% endhighlight %}







### connectorTargetChange
{:#events:connectortargetchange}








Triggers when the connectors' target point is changed

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns the connector, the target point of which is being dragging</td>
</tr>
<tr>
<td class="name">{% highlight html %}
point{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the target point of the element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
port{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">returns the target port of the element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
dragState{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">returns the state of connection end point dragging(starting, dragging, completed)</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



Example
{:.example}


{% highlight html %}
// connectorTargetChange event for diagram
$("#diagramcontent").ejDiagram({
connectorTargetChange:function (args)  {}
      });{% endhighlight %}







### contextMenuBeforeOpen
{:#events:contextmenubeforeopen}








Triggers before opening the context menu

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
diagram{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns the diagram object</td>
</tr>
<tr>
<td class="name">{% highlight html %}
contextmenu{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns the actual arguments from context menu</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



Example
{:.example}


{% highlight html %}
// contextMenuBeforeOpen event for diagram
$("#diagramcontent").ejDiagram({
contextMenuBeforeOpen:function (args)  {}
         });{% endhighlight %}







### contextMenuClick
{:#events:contextmenuclick}








Triggers when a context menu item is clicked

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
id{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">parameter returns the id of the selected context menu item</td>
</tr>
<tr>
<td class="name">{% highlight html %}
text{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">parameter returns the text of the selected context menu item</td>
</tr>
<tr>
<td class="name">{% highlight html %}
parentId{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">parameter returns the parent id of the selected context menu item</td>
</tr>
<tr>
<td class="name">{% highlight html %}
parentText{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">parameter returns the parent text of the selected context menu item</td>
</tr>
<tr>
<td class="name">{% highlight html %}
target{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns the object that was clicked</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



Example
{:.example}


{% highlight html %}
// contextMenuClick event for diagram
$("#diagramcontent").ejDiagram({
contextMenuClick:function (args)  {}
          });{% endhighlight %}







### doubleClick
{:#events:doubleclick}








Triggers when a node, connector or diagram model is clicked twice

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
actualObject{% endhighlight %}</td>
<td class="type"><span class="param-type">Boolean</span></td>
<td class="description last">parameter returns the object that is actually clicked</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns the selected obejct</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
//  doubleClick event for diagram
$("#diagramcontent").ejDiagram({
doubleClick:function (args)  {}
        });{% endhighlight %}







### drag
{:#events:drag}








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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns node or connector that is being dragged</td>
</tr>
<tr>
<td class="name">{% highlight html %}
oldValue{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns the previous position of the node/connector</td>
</tr>
<tr>
<td class="name">{% highlight html %}
newValue{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns the new position of the node/connector</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">Boolean</span></td>
<td class="description last">parameter returns whether or not to cancel the drag event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
//  deag event for diagram
$("#diagramcontent").ejDiagram({
drag:function (args)  {}
  });{% endhighlight %}



### dragEnter
{:#events:dragEnter}








Triggers when a symbol is dragged into diagram from symbol palette

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns node or connector that is dragged into diagram</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">Boolean</span></td>
<td class="description last">parameter returns whether to add or remove the symbol from diagram</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
//  drag enter event for diagram
$("#diagramcontent").ejDiagram({
dragEnter:function (args)  {}
        });{% endhighlight %}



### dragOver
{:#events:dragOver}








Triggers when a symbol is dragged over diagram

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns node or connector that is dragged over diagram</td>
</tr>
<tr>
<td class="name">{% highlight html %}
allowDrop{% endhighlight %}</td>
<td class="type"><span class="param-type">Boolean</span></td>
<td class="description last">parameter defines whether the symbol can be dropped at the current mouse position</td>
</tr>
<tr>
<td class="name">{% highlight html %}
target{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns the node/connector over which the symbol is dragged</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
//  drag over event for diagram
$("#diagramcontent").ejDiagram({
dragOver:function (args)  {}
        });{% endhighlight %}





### drop
{:#events:drop}








Triggers when a symbol is dragged and dropped from symbol palette to drawing area

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns node or connector that is being dropped</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">Boolean</span></td>
<td class="description last">parameter returns whether or not to cancel the drop event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
source{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns the object from where the element is dragged</td>
</tr>
<tr>
<td class="name">{% highlight html %}
target{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns the object over which the objecct will be dropped</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
//  drop event for diagram
$("#diagramcontent").ejDiagram({
drop:function (args)  {}
        });{% endhighlight %}


### groupChange
{:#events:groupChange}

Triggers when a child is added to or removed from a group

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns the object that is added to/removed from a group</td>
</tr>
<tr>
<td class="name">{% highlight html %}
oldParent{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns the old parent group(if any) of the object</td>
</tr>
<tr>
<td class="name">{% highlight html %}
newParent{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns the new parent group(if any) of the object</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cause{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">parameter returns the cause of group change("group", unGroup")</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

Example
{:.example}
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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">return event name</td>
</tr>
<tr>
<td class="name">{% highlight html %}
actualObject{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns the object that was actually clicked</td>
</tr>
<tr>
<td class="name">{% highlight html %}
selectedObject{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns the object that is selected</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
// itemClick event for diagram
$("#diagramcontent").ejDiagram({
itemClick:function (args) {}
        });{% endhighlight %}







### mouseEnter
{:#events:mouseenter}








Triggers when mouse enters a node/connector

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns the target node or connector</td>
</tr>
<tr>
<td class="name">{% highlight html %}
source{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">the object dragged from this container</td>
</tr>
<tr>
<td class="name">{% highlight html %}
target{% endhighlight %}</td>
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


{% highlight html %}
//  mouseEnter event for diagram
$("#diagramcontent").ejDiagram({
mouseEnter:function (args)  {}
        });{% endhighlight %}







### mouseLeave
{:#events:mouseleave}








Triggers when mouse leaves node/connector

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns the target node or connector</td>
</tr>
<tr>
<td class="name">{% highlight html %}
source{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">the object dragged from this container</td>
</tr>
<tr>
<td class="name">{% highlight html %}
target{% endhighlight %}</td>
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


{% highlight html %}
//  mouseLeave event for diagram
$("#diagramcontent").ejDiagram({
mouseLeave:function (args)  {}
               });{% endhighlight %}







### mouseOver
{:#events:mouseover}








Triggers when mouse hovers over a node/connector

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns the target node or connector</td>
</tr>
<tr>
<td class="name">{% highlight html %}
source{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns the object from where the element is dragged</td>
</tr>
<tr>
<td class="name">{% highlight html %}
target{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">the object over which the element is being dragged.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
//  mouseOver event for diagram
$("#diagramcontent").ejDiagram({
mouseOver:function (args)  {}
        });   {% endhighlight %}







### nodeCollectionChange
{:#events:nodecollectionchange}








Triggers when node collection is changed

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
changetype{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">returns should be inserted or removed</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
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


{% highlight html %}
// nodeCollectionChange event for diagram
$("#diagramcontent").ejDiagram({
nodeCollectionChange:function (args)  {}
 });{% endhighlight %}







### nodeSizeChange
{:#events:nodesizechange}








Triggers when a node is resized

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns node that was resized</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">Boolean</span></td>
<td class="description last">parameter to cancel the size change</td>
</tr>
<tr>
<td class="name">{% highlight html %}
newValue{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns the new width, height, offsetX and offsetY values of the element that is being resized</td>
</tr>
<tr>
<td class="name">{% highlight html %}
oldValue{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns the previous width,height,offsetX and offsetY values of the element that is being resized</td>
</tr>
<tr>
<td class="name">{% highlight html %}
resizeState{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">parameter returns the state of resizing(starting,resizing,completed)</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
// sizeChange event for diagram
$("#diagramcontent").ejDiagram({
sizeChange:function (args)  {}
         });{% endhighlight %}


### propertyChange
{:#events:propertyChange}








Triggers when the node properties(x, y,width and height alone) are changed using nudge commands or updateNode API.

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns the selected element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
newValue{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns the new value of the node property that is being changed</td>
</tr>
<tr>
<td class="name">{% highlight html %}
oldValue{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns the old value of the property that is being changed</td>
</tr>
<tr>
<td class="name">{% highlight html %}
propertyName{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">parameter returns the name of the property that is changed </td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
// propertyChange event for diagram
$("#diagramcontent").ejDiagram({
propertyChange:function (args)  {}
         });{% endhighlight %}




### rotationChange
{:#events:rotationchange}








Triggers when the diagram elements are rotated

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns the node that is rotated</td>
</tr>
<tr>
<td class="name">{% highlight html %}
oldValue{% endhighlight %}</td>
<td class="type"><span class="param-type">Boolean</span></td>
<td class="description last">parameter returns the previous rotation angle</td>
</tr>
<tr>
<td class="name">{% highlight html %}
newValue{% endhighlight %}</td>
<td class="type"><span class="param-type">Boolean</span></td>
<td class="description last">parameter returns the new rotation angle</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">Boolean</span></td>
<td class="description last">parameter to specify whether or not to cancel the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
// rotationChange event for diagram
$("#diagramcontent").ejDiagram({
rotationChange:function (args)  {}
        });{% endhighlight %}




### scrollChange
{:#events:scrollChange}








Triggers when the diagram is zoomed or panned

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
newValues{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Parameter returns the new zoom value, horizontal and vertical scroll offsets.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
oldValues{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns the previous zoom value, horizontal and vertical scroll offsets.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
//  ScrollChange  event
$("#diagramcontent").ejDiagram({
scrollChange :function (args)  {
} });
{% endhighlight %}



### segmentChange
{:#events:segmentChange}

Triggers when a connector segment is edited

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Parameter returns the connector that is being edited</td>
</tr>
<tr>
<td class="name">{% highlight html %}
dragState{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">parameter returns the state of editing (starting, dragging, completed)</td>
</tr>
<tr>
<td class="name">{% highlight html %}
point{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns the current mouse position</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

Example
{:.example}
{% highlight html %}
// segment changed event for diagram
$("#diagramcontent").ejDiagram({
segmentChange:function (args) {}
});




{% endhighlight %}



### selectionChanged
{:#events:selectionchanged}








Triggers when the selection is changed in diagram

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
oldItems{% endhighlight %}</td>
<td class="type"><span class="param-type">Array</span></td>
<td class="description last">parameter returns the collection of nodes and connectors that have to be removed from selection list</td>
</tr>
<tr>
<td class="name">{% highlight html %}
newItems{% endhighlight %}</td>
<td class="type"><span class="param-type">Array</span></td>
<td class="description last">parameter returns the collection of nodes and connectors that have to be added to selection list</td>
</tr>
<tr>
<td class="name">{% highlight html %}
selectedItems{% endhighlight %}</td>
<td class="type"><span class="param-type">Array</span></td>
<td class="description last">parameter returns the collection of nodes and connectors that will be selected after selection change</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">Boolean</span></td>
<td class="description last">parameter to specify whether or not to cancel the selection change event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
//  selectionChange event for diagram
$("#diagramcontent").ejDiagram({
selectionChange:function (args)  {}
        });{% endhighlight %}







### textchanged
{:#events:textchanged}








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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameter returns the node that contains the text being edited</td>
</tr>
<tr>
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">parameter returns the new text</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
// textChanged event for diagram
$("#diagramcontent").ejDiagram({
textChanged:function (args)  {}
        });
{% endhighlight %}




