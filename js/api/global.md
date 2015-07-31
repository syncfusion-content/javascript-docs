---
layout: post
title: global
documentation: API
platform: js
metaname: 
metacontent: 
---










## Members








### Alignment<span class="type-signature type string">string</span>
{:#members:alignment}








Enum for alignment. 12






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Center</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">center</td>
<td class="description last">Sets the lineJoin to center.</td>
</tr>
<tr>
<td class="name"><code>Near</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">near</td>
<td class="description last">Sets the lineJoin to near.</td>
</tr>
<tr>
<td class="name"><code>Far</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">far</td>
<td class="description last">Sets the lineJoin to far.</td>
</tr>
</tbody>
</table>















### ArrowShapes<span class="type-signature type arrowshapes"><a href="global.html#ArrowShapes">ArrowShapes</a></span>
{:#members:arrowshapes}








Enum for the ArrowShapes in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>None</code></td>
<td class="type"><span class="param-type"><a href="global.html#ArrowShapes">ArrowShapes</a></span></td>
<td class="default">none</td>
<td class="description last"></td>
</tr>
<tr>
<td class="name"><code>CircularArrow</code></td>
<td class="type"><span class="param-type"><a href="global.html#ArrowShapes">ArrowShapes</a></span></td>
<td class="default">circulararrow</td>
<td class="description last">Used to specify node Shape as CircularArrow</td>
</tr>
<tr>
<td class="name"><code>CurvedRightArrow</code></td>
<td class="type"><span class="param-type"><a href="global.html#ArrowShapes">ArrowShapes</a></span></td>
<td class="default">curvedrightarrow</td>
<td class="description last">Used to specify node Shape as CurvedRightArrow</td>
</tr>
<tr>
<td class="name"><code>CurvedUpArrow</code></td>
<td class="type"><span class="param-type"><a href="global.html#ArrowShapes">ArrowShapes</a></span></td>
<td class="default">curveduparrow</td>
<td class="description last">Used to specify node Shape as CurvedUpArrow</td>
</tr>
<tr>
<td class="name"><code>CurvedLeftArrow</code></td>
<td class="type"><span class="param-type"><a href="global.html#ArrowShapes">ArrowShapes</a></span></td>
<td class="default">curvedleftarrow</td>
<td class="description last">Used to specify node Shape as CurvedLeftArrow</td>
</tr>
<tr>
<td class="name"><code>CurvedDownArrow</code></td>
<td class="type"><span class="param-type"><a href="global.html#ArrowShapes">ArrowShapes</a></span></td>
<td class="default">curveddownarrow</td>
<td class="description last">Used to specify node Shape as CurvedDownArrow</td>
</tr>
<tr>
<td class="name"><code>JumpingRightArrow</code></td>
<td class="type"><span class="param-type"><a href="global.html#ArrowShapes">ArrowShapes</a></span></td>
<td class="default">jumpingrightarrow</td>
<td class="description last">Used to specify node Shape as JumpingRightArrow</td>
</tr>
<tr>
<td class="name"><code>JumpingLeftArrow</code></td>
<td class="type"><span class="param-type"><a href="global.html#ArrowShapes">ArrowShapes</a></span></td>
<td class="default">jumpingleftarrow</td>
<td class="description last">Used to specify node Shape as JumpingLeftArrow</td>
</tr>
</tbody>
</table>















### autoScrollBorder<span class="type-signature type object">object</span>
{:#members:autoscrollborder}








Specifics the auto scroll starting point of diagram control.




Default Value:
{:.param}






* { autoScrollBorder: { left: 15, top: 15, right: 15, bottom: 15 }}








Example
{:.example}

<pre class="prettyprint">
<code>//scrollableArea of the diagram
$("#diagramContent").ejDiagram({pageSettings: {autoScrollBorder: { left: 15, top: 15, right: 15, bottom: 15 }}}); </code>
</pre>






### BasicShapes<span class="type-signature type basicshapes"><a href="global.html#BasicShapes">BasicShapes</a></span>
{:#members:basicshapes}








Enum for the BasicShapes in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Rectangle</code></td>
<td class="type"><span class="param-type"><a href="global.html#BasicShapes">BasicShapes</a></span></td>
<td class="default">rectangle</td>
<td class="description last">Used to specify node Shape as Rectangle</td>
</tr>
<tr>
<td class="name"><code>Ellipse</code></td>
<td class="type"><span class="param-type"><a href="global.html#BasicShapes">BasicShapes</a></span></td>
<td class="default">ellipse</td>
<td class="description last">Used to specify node Shape as Ellipse</td>
</tr>
<tr>
<td class="name"><code>Path</code></td>
<td class="type"><span class="param-type"><a href="global.html#BasicShapes">BasicShapes</a></span></td>
<td class="default">path</td>
<td class="description last">Used to specify node Shape as Path</td>
</tr>
<tr>
<td class="name"><code>Polygon</code></td>
<td class="type"><span class="param-type"><a href="global.html#BasicShapes">BasicShapes</a></span></td>
<td class="default">polygon</td>
<td class="description last">Used to specify node Shape as Polygon</td>
</tr>
<tr>
<td class="name"><code>Triangle</code></td>
<td class="type"><span class="param-type"><a href="global.html#BasicShapes">BasicShapes</a></span></td>
<td class="default">triangle</td>
<td class="description last">Used to specify node Shape as Triangle</td>
</tr>
<tr>
<td class="name"><code>Plus</code></td>
<td class="type"><span class="param-type"><a href="global.html#BasicShapes">BasicShapes</a></span></td>
<td class="default">plus</td>
<td class="description last">Used to specify node Shape as Plus</td>
</tr>
<tr>
<td class="name"><code>Star</code></td>
<td class="type"><span class="param-type"><a href="global.html#BasicShapes">BasicShapes</a></span></td>
<td class="default">star</td>
<td class="description last">Used to specify node Shape as Star</td>
</tr>
<tr>
<td class="name"><code>Pentagon</code></td>
<td class="type"><span class="param-type"><a href="global.html#BasicShapes">BasicShapes</a></span></td>
<td class="default">pentagon</td>
<td class="description last">Used to specify node Shape as Pentagon</td>
</tr>
<tr>
<td class="name"><code>Heptagon</code></td>
<td class="type"><span class="param-type"><a href="global.html#BasicShapes">BasicShapes</a></span></td>
<td class="default">heptagon</td>
<td class="description last">Used to specify node Shape as Heptagon</td>
</tr>
<tr>
<td class="name"><code>Octagon</code></td>
<td class="type"><span class="param-type"><a href="global.html#BasicShapes">BasicShapes</a></span></td>
<td class="default">octagon</td>
<td class="description last">Used to specify node Shape as Octagon</td>
</tr>
<tr>
<td class="name"><code>Trapezoid</code></td>
<td class="type"><span class="param-type"><a href="global.html#BasicShapes">BasicShapes</a></span></td>
<td class="default">trapezoid</td>
<td class="description last">Used to specify node Shape as Trapezoid</td>
</tr>
<tr>
<td class="name"><code>Decagon</code></td>
<td class="type"><span class="param-type"><a href="global.html#BasicShapes">BasicShapes</a></span></td>
<td class="default">decagon</td>
<td class="description last">Used to specify node Shape as Decagon</td>
</tr>
<tr>
<td class="name"><code>RightTriangle</code></td>
<td class="type"><span class="param-type"><a href="global.html#BasicShapes">BasicShapes</a></span></td>
<td class="default">righttriangle</td>
<td class="description last">Used to specify node Shape as RightTriangle</td>
</tr>
<tr>
<td class="name"><code>Cylinder</code></td>
<td class="type"><span class="param-type"><a href="global.html#BasicShapes">BasicShapes</a></span></td>
<td class="default">cylinder</td>
<td class="description last">Used to specify node Shape as Cylinder</td>
</tr>
</tbody>
</table>















### BingMapType<span class="type-signature type string">string</span>
{:#members:bingmaptype}








Enum for Map Bing map types






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Aerial</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">aerial</td>
<td class="description last">support for bing map type aerial.</td>
</tr>
<tr>
<td class="name"><code>AerialWithLabel</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">aerialwithlabel</td>
<td class="description last">support for bing map type aerialwithlabel.</td>
</tr>
<tr>
<td class="name"><code>Road</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">road</td>
<td class="description last">support for bing map type road.</td>
</tr>
</tbody>
</table>















### BPMNActivity<span class="type-signature type bpmnactivity"><a href="global.html#BPMNActivity">BPMNActivity</a></span>
{:#members:bpmnactivity}








Enum for the BPMNActivity in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>None</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNActivity">BPMNActivity</a></span></td>
<td class="default">none</td>
<td class="description last">Used to set BPMN Activity as None</td>
</tr>
<tr>
<td class="name"><code>Task</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNActivity">BPMNActivity</a></span></td>
<td class="default">task</td>
<td class="description last">Used to set BPMN Activity as Task</td>
</tr>
<tr>
<td class="name"><code>SubProcess</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNActivity">BPMNActivity</a></span></td>
<td class="default">subprocess</td>
<td class="description last">Used to set BPMN Activity as SubProcess</td>
</tr>
</tbody>
</table>















### BPMNBoundary<span class="type-signature type bpmnboundary"><a href="global.html#BPMNBoundary">BPMNBoundary</a></span>
{:#members:bpmnboundary}








Enum for the BPMNBoundary in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Default</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNBoundary">BPMNBoundary</a></span></td>
<td class="default">default</td>
<td class="description last">Used to set BPMN SubProcess's Boundary as Default</td>
</tr>
<tr>
<td class="name"><code>Call</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNBoundary">BPMNBoundary</a></span></td>
<td class="default">call</td>
<td class="description last">Used to set BPMN SubProcess's Boundary as Call</td>
</tr>
<tr>
<td class="name"><code>Event</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNBoundary">BPMNBoundary</a></span></td>
<td class="default">event</td>
<td class="description last">Used to set BPMN SubProcess's Boundary as Event</td>
</tr>
</tbody>
</table>















### BPMNDirections<span class="type-signature type bpmndirections"><a href="global.html#BPMNDirections">BPMNDirections</a></span>
{:#members:bpmndirections}








Enum for the BPMNDirections in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>None</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNDirections">BPMNDirections</a></span></td>
<td class="default">none</td>
<td class="description last">Used to set BPMN Flow Direction as None</td>
</tr>
<tr>
<td class="name"><code>UniDirectional</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNDirections">BPMNDirections</a></span></td>
<td class="default">unidirectional</td>
<td class="description last">Used to set BPMN Flow Direction as UniDirectional</td>
</tr>
<tr>
<td class="name"><code>BiDirectional</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNDirections">BPMNDirections</a></span></td>
<td class="default">bidirectional</td>
<td class="description last">Used to set BPMN Flow Direction as BiDirectional</td>
</tr>
</tbody>
</table>















### BPMNEvents<span class="type-signature type bpmnevents"><a href="global.html#BPMNEvents">BPMNEvents</a></span>
{:#members:bpmnevents}








Enum for the BPMNEvents in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Start</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNEvents">BPMNEvents</a></span></td>
<td class="default">start</td>
<td class="description last">Used to set BPMN Event as Start</td>
</tr>
<tr>
<td class="name"><code>Intermediate</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNEvents">BPMNEvents</a></span></td>
<td class="default">intermediate</td>
<td class="description last">Used to set BPMN Event as Intermediate</td>
</tr>
<tr>
<td class="name"><code>End</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNEvents">BPMNEvents</a></span></td>
<td class="default">end</td>
<td class="description last">Used to set BPMN Event as End</td>
</tr>
<tr>
<td class="name"><code>NonInterruptingStart</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNEvents">BPMNEvents</a></span></td>
<td class="default">noninterruptingstart</td>
<td class="description last">Used to set BPMN Event as NonInterruptingStart</td>
</tr>
<tr>
<td class="name"><code>NonInterruptingIntermediate</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNEvents">BPMNEvents</a></span></td>
<td class="default">noninterruptingintermediate</td>
<td class="description last">Used to set BPMN Event as NonInterruptingIntermediate</td>
</tr>
</tbody>
</table>















### BPMNGateways<span class="type-signature type bpmngateways"><a href="global.html#BPMNGateways">BPMNGateways</a></span>
{:#members:bpmngateways}








Enum for the BPMNGateways in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>None</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNGateways">BPMNGateways</a></span></td>
<td class="default">none</td>
<td class="description last">Used to set BPMN Gateway as None</td>
</tr>
<tr>
<td class="name"><code>Exclusive</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNGateways">BPMNGateways</a></span></td>
<td class="default">exclusive</td>
<td class="description last">Used to set BPMN Gateway as Exclusive</td>
</tr>
<tr>
<td class="name"><code>Inclusive</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNGateways">BPMNGateways</a></span></td>
<td class="default">inclusive</td>
<td class="description last">Used to set BPMN Gateway as Inclusive</td>
</tr>
<tr>
<td class="name"><code>Parallel</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNGateways">BPMNGateways</a></span></td>
<td class="default">parallel</td>
<td class="description last">Used to set BPMN Gateway as Parallel</td>
</tr>
<tr>
<td class="name"><code>Complex</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNGateways">BPMNGateways</a></span></td>
<td class="default">complex</td>
<td class="description last">Used to set BPMN Gateway as Complex</td>
</tr>
<tr>
<td class="name"><code>EventBased</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNGateways">BPMNGateways</a></span></td>
<td class="default">eventbased</td>
<td class="description last">Used to set BPMN Gateway as EventBased</td>
</tr>
</tbody>
</table>















### BPMNLoops<span class="type-signature type bpmnloops"><a href="global.html#BPMNLoops">BPMNLoops</a></span>
{:#members:bpmnloops}








Enum for the BPMNLoops in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>None</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNLoops">BPMNLoops</a></span></td>
<td class="default">none</td>
<td class="description last">Used to set BPMN Activity's Loop as None</td>
</tr>
<tr>
<td class="name"><code>Standard</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNLoops">BPMNLoops</a></span></td>
<td class="default">standard</td>
<td class="description last">Used to set BPMN Activity's Loop as Standard</td>
</tr>
<tr>
<td class="name"><code>ParallelMultiInstance</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNLoops">BPMNLoops</a></span></td>
<td class="default">parallelmultiinstance</td>
<td class="description last">Used to set BPMN Activity's Loop as ParallelMultiInstance</td>
</tr>
<tr>
<td class="name"><code>SequenceMultiInstance</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNLoops">BPMNLoops</a></span></td>
<td class="default">sequencemultiinstance</td>
<td class="description last">Used to set BPMN Activity's Loop as SequenceMultiInstance</td>
</tr>
</tbody>
</table>















### BPMNShapes<span class="type-signature type bpmnshapes"><a href="global.html#BPMNShapes">BPMNShapes</a></span>
{:#members:bpmnshapes}








Enum for the BPMNShapes in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Event</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNShapes">BPMNShapes</a></span></td>
<td class="default">event</td>
<td class="description last">Used to specify node Shape as Event</td>
</tr>
<tr>
<td class="name"><code>Gateway</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNShapes">BPMNShapes</a></span></td>
<td class="default">gateway</td>
<td class="description last">Used to specify node Shape as Gateway</td>
</tr>
<tr>
<td class="name"><code>SequentialFlow</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNShapes">BPMNShapes</a></span></td>
<td class="default">sequentialflow</td>
<td class="description last">Used to specify node Shape as SequentialFlow</td>
</tr>
<tr>
<td class="name"><code>AssociationFlow</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNShapes">BPMNShapes</a></span></td>
<td class="default">associationflow</td>
<td class="description last">Used to specify node Shape as AssociationFlow</td>
</tr>
<tr>
<td class="name"><code>MessageFlow</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNShapes">BPMNShapes</a></span></td>
<td class="default">messageflow</td>
<td class="description last">Used to specify node Shape as MessageFlow</td>
</tr>
<tr>
<td class="name"><code>Message</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNShapes">BPMNShapes</a></span></td>
<td class="default">message</td>
<td class="description last">Used to specify node Shape as Message</td>
</tr>
<tr>
<td class="name"><code>DataObject</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNShapes">BPMNShapes</a></span></td>
<td class="default">dataobject</td>
<td class="description last">Used to specify node Shape as DataObject</td>
</tr>
<tr>
<td class="name"><code>DataSource</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNShapes">BPMNShapes</a></span></td>
<td class="default">datasource</td>
<td class="description last">Used to specify node Shape as DataSource</td>
</tr>
<tr>
<td class="name"><code>Activity</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNShapes">BPMNShapes</a></span></td>
<td class="default">activity</td>
<td class="description last">Used to specify node Shape as Activity</td>
</tr>
</tbody>
</table>















### BPMNTasks<span class="type-signature type bpmntasks"><a href="global.html#BPMNTasks">BPMNTasks</a></span>
{:#members:bpmntasks}








Enum for the BPMNTasks in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>None</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNTasks">BPMNTasks</a></span></td>
<td class="default">none</td>
<td class="description last">Used to set BPMN Task Type as None</td>
</tr>
<tr>
<td class="name"><code>Service</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNTasks">BPMNTasks</a></span></td>
<td class="default">service</td>
<td class="description last">Used to set BPMN Task Type as Service</td>
</tr>
<tr>
<td class="name"><code>Receive</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNTasks">BPMNTasks</a></span></td>
<td class="default">receive</td>
<td class="description last">Used to set BPMN Task Type as Receive</td>
</tr>
<tr>
<td class="name"><code>Send</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNTasks">BPMNTasks</a></span></td>
<td class="default">send</td>
<td class="description last">Used to set BPMN Task Type as Send</td>
</tr>
<tr>
<td class="name"><code>InstantiatingReceive</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNTasks">BPMNTasks</a></span></td>
<td class="default">instantiatingreceive</td>
<td class="description last">Used to set BPMN Task Type as InstantiatingReceive</td>
</tr>
<tr>
<td class="name"><code>Manual</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNTasks">BPMNTasks</a></span></td>
<td class="default">manual</td>
<td class="description last">Used to set BPMN Task Type as Manual</td>
</tr>
<tr>
<td class="name"><code>BusinessRule</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNTasks">BPMNTasks</a></span></td>
<td class="default">businessrule</td>
<td class="description last">Used to set BPMN Task Type as BusinessRule</td>
</tr>
<tr>
<td class="name"><code>User</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNTasks">BPMNTasks</a></span></td>
<td class="default">user</td>
<td class="description last">Used to set BPMN Task Type as User</td>
</tr>
<tr>
<td class="name"><code>Script</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNTasks">BPMNTasks</a></span></td>
<td class="default">script</td>
<td class="description last">Used to set BPMN Task Type as Script</td>
</tr>
<tr>
<td class="name"><code>Parallel</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNTasks">BPMNTasks</a></span></td>
<td class="default">parallel</td>
<td class="description last">Used to set BPMN Task Type as Parallel</td>
</tr>
</tbody>
</table>















### BPMNTriggers<span class="type-signature type bpmntriggers"><a href="global.html#BPMNTriggers">BPMNTriggers</a></span>
{:#members:bpmntriggers}








Enum for the BPMNTriggers in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>None</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNTriggers">BPMNTriggers</a></span></td>
<td class="default">none</td>
<td class="description last">Used to set Event Triger as None</td>
</tr>
<tr>
<td class="name"><code>Message</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNTriggers">BPMNTriggers</a></span></td>
<td class="default">message</td>
<td class="description last">Used to set Event Triger as Message</td>
</tr>
<tr>
<td class="name"><code>Timer</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNTriggers">BPMNTriggers</a></span></td>
<td class="default">timer</td>
<td class="description last">Used to set Event Triger as Timer</td>
</tr>
<tr>
<td class="name"><code>Escalation</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNTriggers">BPMNTriggers</a></span></td>
<td class="default">escalation</td>
<td class="description last">Used to set Event Triger as Escalation</td>
</tr>
<tr>
<td class="name"><code>Link</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNTriggers">BPMNTriggers</a></span></td>
<td class="default">link</td>
<td class="description last">Used to set Event Triger as Link</td>
</tr>
<tr>
<td class="name"><code>Error</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNTriggers">BPMNTriggers</a></span></td>
<td class="default">error</td>
<td class="description last">Used to set Event Triger as Error</td>
</tr>
<tr>
<td class="name"><code>Compensation</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNTriggers">BPMNTriggers</a></span></td>
<td class="default">compensation</td>
<td class="description last">Used to set Event Triger as Compensation</td>
</tr>
<tr>
<td class="name"><code>Signal</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNTriggers">BPMNTriggers</a></span></td>
<td class="default">signal</td>
<td class="description last">Used to set Event Triger as Signal</td>
</tr>
<tr>
<td class="name"><code>Multiple</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNTriggers">BPMNTriggers</a></span></td>
<td class="default">multiple</td>
<td class="description last">Used to set Event Triger as Multiple</td>
</tr>
<tr>
<td class="name"><code>Parallel</code></td>
<td class="type"><span class="param-type"><a href="global.html#BPMNTriggers">BPMNTriggers</a></span></td>
<td class="default">parallel</td>
<td class="description last">Used to set Event Triger as Parallel</td>
</tr>
</tbody>
</table>















### ButtonStyle<span class="type-signature type string">string</span>
{:#members:buttonstyle}








Enum for ej.mobile.Menu.IOS7.ButtonStyle






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Enum for normal ios7 button style</td>
</tr>
<tr>
<td class="name"><code>Back</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">back</td>
<td class="description last">Enum for back ios7 button style</td>
</tr>
<tr>
<td class="name"><code>Header</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">header</td>
<td class="description last">Enum for header ios7 button style</td>
</tr>
<tr>
<td class="name"><code>Dialog</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">dialog</td>
<td class="description last">Enum for dialog ios7 button style</td>
</tr>
</tbody>
</table>















### CancelButtonColor<span class="type-signature type string">string</span>
{:#members:cancelbuttoncolor}








Enum for ej.mobile.Menu.IOS7.CancelButtonColor






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Blue</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">blue</td>
<td class="description last">Enum for blue color button in ios7 mode</td>
</tr>
<tr>
<td class="name"><code>Gray</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">gray</td>
<td class="description last">Enum for gray color button in ios7 mode</td>
</tr>
<tr>
<td class="name"><code>Black</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">black</td>
<td class="description last">Enum for black color button in ios7 mode</td>
</tr>
<tr>
<td class="name"><code>Green</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">green</td>
<td class="description last">Enum for green color button in ios7 mode</td>
</tr>
<tr>
<td class="name"><code>Red</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">red</td>
<td class="description last">Enum for red color button in ios7 mode</td>
</tr>
</tbody>
</table>















### CharacterType<span class="type-signature type string">string</span>
{:#members:charactertype}








Enum for gauge CharacterType






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>SevenSegment</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">sevensegment</td>
<td class="description last">To set the CharacterType sevensegment.</td>
</tr>
<tr>
<td class="name"><code>FourteenSegment</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">fourteensegment</td>
<td class="description last">To set the CharacterType fourteensegment.</td>
</tr>
<tr>
<td class="name"><code>SixteenSegment</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">sixteensegment</td>
<td class="description last">To set the CharacterType sixteensegment.</td>
</tr>
<tr>
<td class="name"><code>EightCrossEightDotMatrix</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">eightcrosseightdotmatrix</td>
<td class="description last">To set the CharacterType eightcrosseightdotmatrix.</td>
</tr>
<tr>
<td class="name"><code>EightCrossEightSquareMatrix</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">eightcrosseightsquarematrix</td>
<td class="description last">To set the CharacterType eightcrosseightsquarematrix.</td>
</tr>
</tbody>
</table>















### ChartOrientations<span class="type-signature type string">String</span>
{:#members:chartorientations}








Enum for ChartOrientations in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Horizontal</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="default">horizontal</td>
<td class="description last">Used to set horizontal organizational chart orientation</td>
</tr>
<tr>
<td class="name"><code>Vertical</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="default">vertical</td>
<td class="description last">Used to set vertical organizational chart orientation</td>
</tr>
</tbody>
</table>















### ChartTypes<span class="type-signature type string">String</span>
{:#members:charttypes}








Enum for ChartTypes in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Left</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="default">left</td>
<td class="description last">Used to arrange the children at left side of parent</td>
</tr>
<tr>
<td class="name"><code>Right</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="default">right</td>
<td class="description last">Used to arrange the children at right side of parent</td>
</tr>
<tr>
<td class="name"><code>Alternate</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="default">alternate</td>
<td class="description last">Used to arrange the children at alternative sides(left,right) of parent</td>
</tr>
<tr>
<td class="name"><code>Center</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="default">center</td>
<td class="description last">Used to arrange the children with respect to the middle of parent</td>
</tr>
</tbody>
</table>















### CheckState<span class="type-signature type string">string</span>
{:#members:checkstate}








Enum for CheckboxState






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Uncheck</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">uncheck</td>
<td class="description last">Enum for Uncheck state checkbox</td>
</tr>
<tr>
<td class="name"><code>Check</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">check</td>
<td class="description last">Enum for Check state checkbox</td>
</tr>
<tr>
<td class="name"><code>Indeterminate</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">indeterminate</td>
<td class="description last">Enum for Indeterminate state checkbox</td>
</tr>
</tbody>
</table>















### Color<span class="type-signature type string">string</span>
{:#members:color}








Enum for IOS7Color






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Gray</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">gray</td>
<td class="description last">Enum for gray ios7 button color</td>
</tr>
<tr>
<td class="name"><code>Black</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">black</td>
<td class="description last">Enum for black ios7 button color</td>
</tr>
<tr>
<td class="name"><code>Blue</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">blue</td>
<td class="description last">Enum for black ios7 buttonColor</td>
</tr>
<tr>
<td class="name"><code>Green</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">green</td>
<td class="description last">Enum for green ios7 button color</td>
</tr>
<tr>
<td class="name"><code>Red</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">red</td>
<td class="description last">Enum for red ios7 button color</td>
</tr>
</tbody>
</table>















### ColorPalette<span class="type-signature type string">string</span>
{:#members:colorpalette}








Enum for Map color palette






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Palette1</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">palette1</td>
<td class="description last">support for color palette palette1.</td>
</tr>
<tr>
<td class="name"><code>Palette2</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">palette2</td>
<td class="description last">support for color palette palette2.</td>
</tr>
<tr>
<td class="name"><code>Palette3</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">palette3</td>
<td class="description last">support for color palette palette3.</td>
</tr>
<tr>
<td class="name"><code>CustomPalette</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">custompalette</td>
<td class="description last">support for color palette custompalette.</td>
</tr>
</tbody>
</table>















### ConnectorConstraints<span class="type-signature type connectorconstraints"><a href="global.html#ConnectorConstraints">ConnectorConstraints</a></span>
{:#members:connectorconstraints}








Enum for ConnectorConstraints in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>None</code></td>
<td class="type"><span class="param-type"><a href="global.html#ConnectorConstraints">ConnectorConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Disable all connector Constraints</td>
</tr>
<tr>
<td class="name"><code>Select</code></td>
<td class="type"><span class="param-type"><a href="global.html#ConnectorConstraints">ConnectorConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables connector to be selected</td>
</tr>
<tr>
<td class="name"><code>Delete</code></td>
<td class="type"><span class="param-type"><a href="global.html#ConnectorConstraints">ConnectorConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables connector to be Deleted</td>
</tr>
<tr>
<td class="name"><code>Drag</code></td>
<td class="type"><span class="param-type"><a href="global.html#ConnectorConstraints">ConnectorConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables connector to be Dragged</td>
</tr>
<tr>
<td class="name"><code>DragSourceEnd</code></td>
<td class="type"><span class="param-type"><a href="global.html#ConnectorConstraints">ConnectorConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables connectors source end to be selected</td>
</tr>
<tr>
<td class="name"><code>DragTargetEnd</code></td>
<td class="type"><span class="param-type"><a href="global.html#ConnectorConstraints">ConnectorConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables connectors target end to be selected</td>
</tr>
<tr>
<td class="name"><code>DragSegmentThumb</code></td>
<td class="type"><span class="param-type"><a href="global.html#ConnectorConstraints">ConnectorConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables control point and end point of every segment in a connector for editing</td>
</tr>
<tr>
<td class="name"><code>Bridging</code></td>
<td class="type"><span class="param-type"><a href="global.html#ConnectorConstraints">ConnectorConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables bridging to the connector</td>
</tr>
<tr>
<td class="name"><code>DragLabel</code></td>
<td class="type"><span class="param-type"><a href="global.html#ConnectorConstraints">ConnectorConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables label of node to be Dragged</td>
</tr>
<tr>
<td class="name"><code>InheritBridging</code></td>
<td class="type"><span class="param-type"><a href="global.html#ConnectorConstraints">ConnectorConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables bridging to the connector</td>
</tr>
<tr>
<td class="name"><code>Default</code></td>
<td class="type"><span class="param-type"><a href="global.html#ConnectorConstraints">ConnectorConstraints</a></span></td>
<td class="default">BITOR</td>
<td class="description last">Enables all constraints</td>
</tr>
</tbody>
</table>















### ContainerType<span class="type-signature type string">string</span>
{:#members:containertype}








Enum for various containerType in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Canvas</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">canvas</td>
<td class="description last">Sets the container type as Canvas</td>
</tr>
<tr>
<td class="name"><code>Stack</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">stack</td>
<td class="description last">Sets the container type as Stack</td>
</tr>
</tbody>
</table>















### ContentType<span class="type-signature type string">string</span>
{:#members:contenttype}








Enum for ContentType






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Text</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">text</td>
<td class="description last">Enum for text content type</td>
</tr>
<tr>
<td class="name"><code>Image</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">image</td>
<td class="description last">Enum for image content type</td>
</tr>
<tr>
<td class="name"><code>Both</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">both</td>
<td class="description last">Enum for displaying both text and image content type</td>
</tr>
</tbody>
</table>















### ContentType<span class="type-signature type string">string</span>
{:#members:contenttype}








Enum for Android tabContentType






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Text</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">text</td>
<td class="description last">Enum for text content type</td>
</tr>
<tr>
<td class="name"><code>Image</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">image</td>
<td class="description last">Enum for image content type</td>
</tr>
<tr>
<td class="name"><code>Both</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">both</td>
<td class="description last">Enum for displaying both text and image content type</td>
</tr>
</tbody>
</table>















### CrosshairType<span class="type-signature type string">string</span>
{:#members:crosshairtype}








Enum for chart crosshairType.






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Crosshair</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">crosshair</td>
<td class="description last">set crosshair for chart.</td>
</tr>
<tr>
<td class="name"><code>TrackBall</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">trackBall</td>
<td class="description last">set trackBall for chart.</td>
</tr>
</tbody>
</table>















### CustomLabelPositionType<span class="type-signature type string">string</span>
{:#members:customlabelpositiontype}








Enum for gauge CustomLabelPositionType






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Inner</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">inner</td>
<td class="description last">To set the CustomLabelPositionType inner.</td>
</tr>
<tr>
<td class="name"><code>Outer</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">outer</td>
<td class="description last">To set the CustomLabelPositionType outer.</td>
</tr>
</tbody>
</table>















### CustomLabelPositionType<span class="type-signature type string">string</span>
{:#members:customlabelpositiontype}








Enum for gauge CustomLabelPositionType






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Inner</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">inner</td>
<td class="description last">To set the CustomLabelPositionType inner.</td>
</tr>
<tr>
<td class="name"><code>Outer</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">outer</td>
<td class="description last">To set the CustomLabelPositionType outer.</td>
</tr>
</tbody>
</table>















### dataTypes
{:#members:datatypes}








datatypes to the default model values











### DecoratorShapes<span class="type-signature type string">string</span>
{:#members:decoratorshapes}








Enum for various decorator shapes in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>None</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">none</td>
<td class="description last">Used to set decorator shape as none</td>
</tr>
<tr>
<td class="name"><code>Arrow</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">arrow</td>
<td class="description last">Used to set decorator shape as Arrow</td>
</tr>
<tr>
<td class="name"><code>OpenArrow</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">openarrow</td>
<td class="description last">Used to set decorator shape as Open Arrow</td>
</tr>
<tr>
<td class="name"><code>Circle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">circle</td>
<td class="description last">Used to set decorator shape as Circle</td>
</tr>
<tr>
<td class="name"><code>Diamond</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">diamond</td>
<td class="description last">Used to set decorator shape as Diamond</td>
</tr>
<tr>
<td class="name"><code>Path</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">path</td>
<td class="description last">Used to set decorator shape as path</td>
</tr>
</tbody>
</table>















### DiagramConstraints<span class="type-signature type diagramconstraints"><a href="global.html#DiagramConstraints">DiagramConstraints</a></span>
{:#members:diagramconstraints}








Enum for the DiagramConstraints in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>None</code></td>
<td class="type"><span class="param-type"><a href="global.html#DiagramConstraints">DiagramConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Disables all DiagramConstraints</td>
</tr>
<tr>
<td class="name"><code>PageEditable</code></td>
<td class="type"><span class="param-type"><a href="global.html#DiagramConstraints">DiagramConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables/Disables PageEditing</td>
</tr>
<tr>
<td class="name"><code>Bridging</code></td>
<td class="type"><span class="param-type"><a href="global.html#DiagramConstraints">DiagramConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables/Disables Bridging</td>
</tr>
<tr>
<td class="name"><code>Zoomable</code></td>
<td class="type"><span class="param-type"><a href="global.html#DiagramConstraints">DiagramConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables/Disables Zooming</td>
</tr>
<tr>
<td class="name"><code>PannableX</code></td>
<td class="type"><span class="param-type"><a href="global.html#DiagramConstraints">DiagramConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables/Disables panning on horizontal axis</td>
</tr>
<tr>
<td class="name"><code>PannableY</code></td>
<td class="type"><span class="param-type"><a href="global.html#DiagramConstraints">DiagramConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables/Disables panning on vertical axis</td>
</tr>
<tr>
<td class="name"><code>Pannable</code></td>
<td class="type"><span class="param-type"><a href="global.html#DiagramConstraints">DiagramConstraints</a></span></td>
<td class="default">BITOR</td>
<td class="description last">Enables/Disables Panning</td>
</tr>
<tr>
<td class="name"><code>Undoable</code></td>
<td class="type"><span class="param-type"><a href="global.html#DiagramConstraints">DiagramConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables/Disables undo actions</td>
</tr>
<tr>
<td class="name"><code>Default</code></td>
<td class="type"><span class="param-type"><a href="global.html#DiagramConstraints">DiagramConstraints</a></span></td>
<td class="default">BITOR</td>
<td class="description last">Enables all Constraints</td>
</tr>
</tbody>
</table>















### Directions<span class="type-signature type string">string</span>
{:#members:directions}








Enum for gauge Directions






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Clockwise</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">clockwise</td>
<td class="description last">To set the Directions clockwise.</td>
</tr>
<tr>
<td class="name"><code>CounterClockwise</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">counterclockwise</td>
<td class="description last">To set the Directions counterclockwise.</td>
</tr>
</tbody>
</table>















### Directions<span class="type-signature type string">string</span>
{:#members:directions}








Enum for gauge Directions






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Clockwise</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">clockwise</td>
<td class="description last">To set the Directions clockwise.</td>
</tr>
<tr>
<td class="name"><code>CounterClockwise</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">counterclockwise</td>
<td class="description last">To set the Directions counterclockwise.</td>
</tr>
</tbody>
</table>















### DragState<span class="type-signature type dragstate"><a href="global.html#DragState">DragState</a></span>
{:#members:dragstate}








Enum for the Dragstate of the connector in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Starting</code></td>
<td class="type"><span class="param-type"><a href="global.html#DragState">DragState</a></span></td>
<td class="default">starting</td>
<td class="description last">sets the drag state as starting</td>
</tr>
<tr>
<td class="name"><code>Dragging</code></td>
<td class="type"><span class="param-type"><a href="global.html#DragState">DragState</a></span></td>
<td class="default">dragging</td>
<td class="description last">sets the drag state as dragging</td>
</tr>
<tr>
<td class="name"><code>Completed</code></td>
<td class="type"><span class="param-type"><a href="global.html#DragState">DragState</a></span></td>
<td class="default">completed</td>
<td class="description last">sets the drag state as completed</td>
</tr>
</tbody>
</table>















### DrawMode<span class="type-signature type string">string</span>
{:#members:drawmode}








Enum for hilopenclose drawmode.






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Both</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">both</td>
<td class="description last">Specifies the draw mode as both.</td>
</tr>
<tr>
<td class="name"><code>Open</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">open</td>
<td class="description last">Specifies the draw mode as open.</td>
</tr>
<tr>
<td class="name"><code>Close</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">close</td>
<td class="description last">Specifies the draw mode as close</td>
</tr>
</tbody>
</table>















### DrawType<span class="type-signature type string">string</span>
{:#members:drawtype}








Enum for chart drawType mode.






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Line</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">line</td>
<td class="description last">Specifies the drawType as line.</td>
</tr>
<tr>
<td class="name"><code>Column</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">column</td>
<td class="description last">Specifies the drawType as column.</td>
</tr>
<tr>
<td class="name"><code>Area</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">area</td>
<td class="description last">Specifies the drawType as area.</td>
</tr>
</tbody>
</table>















### EdgeLabelPlacement<span class="type-signature type string">string</span>
{:#members:edgelabelplacement}








Enum for chart edgeLabelPlacement.






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>None</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">none</td>
<td class="description last">Places the edge labels in the same position.</td>
</tr>
<tr>
<td class="name"><code>Shift</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">shift</td>
<td class="description last">Shift the edge labels inside the chart area.</td>
</tr>
<tr>
<td class="name"><code>Hide</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">hide</td>
<td class="description last">Hide the edge labels which exceeds the chart area boundary.</td>
</tr>
</tbody>
</table>















### element
{:#members:element}








Widget element will be automatically set in this











### ExportModes<span class="type-signature type exportmodes"><a href="global.html#ExportModes">ExportModes</a></span>
{:#members:exportmodes}








Enum for the ExportModes in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Download</code></td>
<td class="type"><span class="param-type"><a href="global.html#ExportModes">ExportModes</a></span></td>
<td class="default">download</td>
<td class="description last">Downloads the exported diagram</td>
</tr>
<tr>
<td class="name"><code>Data</code></td>
<td class="type"><span class="param-type"><a href="global.html#ExportModes">ExportModes</a></span></td>
<td class="default">data</td>
<td class="description last">Converts diagram to data of type imageURL/svg</td>
</tr>
</tbody>
</table>















### FileFormats<span class="type-signature type fileformats"><a href="global.html#FileFormats">FileFormats</a></span>
{:#members:fileformats}








Enum for the FileFormats in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>JPG</code></td>
<td class="type"><span class="param-type"><a href="global.html#FileFormats">FileFormats</a></span></td>
<td class="default">jpg</td>
<td class="description last">Exports diagram to .jpg format</td>
</tr>
<tr>
<td class="name"><code>PNG</code></td>
<td class="type"><span class="param-type"><a href="global.html#FileFormats">FileFormats</a></span></td>
<td class="default">png</td>
<td class="description last">Exports diagram to .png format</td>
</tr>
<tr>
<td class="name"><code>BMP</code></td>
<td class="type"><span class="param-type"><a href="global.html#FileFormats">FileFormats</a></span></td>
<td class="default">bmp</td>
<td class="description last">Exports diagram to .bmp format</td>
</tr>
<tr>
<td class="name"><code>SVG</code></td>
<td class="type"><span class="param-type"><a href="global.html#FileFormats">FileFormats</a></span></td>
<td class="default">svg</td>
<td class="description last">Exports diagram to .svg format</td>
</tr>
</tbody>
</table>















### FilterBarMode<span class="type-signature type string">string</span>
{:#members:filterbarmode}








Enum for Grid Filter Bar mode






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Immediate</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">immediate</td>
<td class="description last">Used to display filter results as soon as typing the filter query or after specified time interval</td>
</tr>
<tr>
<td class="name"><code>OnEnter</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">onenter</td>
<td class="description last">Used to display filter results after enter key is pressed</td>
</tr>
</tbody>
</table>















### FilterType<span class="type-signature type string">string</span>
{:#members:filtertype}








Enum for filtertype






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>StartsWith</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">startswith</td>
<td class="description last">Enum for filter type startswith</td>
</tr>
<tr>
<td class="name"><code>Contains</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">contains</td>
<td class="description last">Enum for filter type contains</td>
</tr>
</tbody>
</table>















### FitMode<span class="type-signature type fitmode"><a href="global.html#FitMode">FitMode</a></span>
{:#members:fitmode}








Enum for the FitMode in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Page</code></td>
<td class="type"><span class="param-type"><a href="global.html#FitMode">FitMode</a></span></td>
<td class="default">page</td>
<td class="description last">Fits the entire diagram into view</td>
</tr>
<tr>
<td class="name"><code>Width</code></td>
<td class="type"><span class="param-type"><a href="global.html#FitMode">FitMode</a></span></td>
<td class="default">width</td>
<td class="description last">Fits the width of the diagram into the width of view</td>
</tr>
<tr>
<td class="name"><code>Height</code></td>
<td class="type"><span class="param-type"><a href="global.html#FitMode">FitMode</a></span></td>
<td class="default">height</td>
<td class="description last">Fits the height of the diagram into the height of view</td>
</tr>
</tbody>
</table>















### FlowDirection<span class="type-signature type string">string</span>
{:#members:flowdirection}








Enum for Bullet Graph Flow Direction






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Forward</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">forward</td>
<td class="description last">To set the flow direction forward.</td>
</tr>
<tr>
<td class="name"><code>Backward</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">backward</td>
<td class="description last">To set the flow direction backward.</td>
</tr>
</tbody>
</table>















### FlowShapes<span class="type-signature type flowshapes"><a href="global.html#FlowShapes">FlowShapes</a></span>
{:#members:flowshapes}








Enum for the FlowShapes in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Process</code></td>
<td class="type"><span class="param-type"><a href="global.html#FlowShapes">FlowShapes</a></span></td>
<td class="default">process</td>
<td class="description last">Used to specify node Shape as Process</td>
</tr>
<tr>
<td class="name"><code>Decision</code></td>
<td class="type"><span class="param-type"><a href="global.html#FlowShapes">FlowShapes</a></span></td>
<td class="default">decision</td>
<td class="description last">Used to specify node Shape as Decision</td>
</tr>
<tr>
<td class="name"><code>Document</code></td>
<td class="type"><span class="param-type"><a href="global.html#FlowShapes">FlowShapes</a></span></td>
<td class="default">document</td>
<td class="description last">Used to specify node Shape as Document</td>
</tr>
<tr>
<td class="name"><code>PreDefinedProcess</code></td>
<td class="type"><span class="param-type"><a href="global.html#FlowShapes">FlowShapes</a></span></td>
<td class="default">predefinedprocess</td>
<td class="description last">Used to specify node Shape as PreDefinedProcess</td>
</tr>
<tr>
<td class="name"><code>Terminator</code></td>
<td class="type"><span class="param-type"><a href="global.html#FlowShapes">FlowShapes</a></span></td>
<td class="default">terminator</td>
<td class="description last">Used to specify node Shape as Terminator</td>
</tr>
<tr>
<td class="name"><code>PaperTap</code></td>
<td class="type"><span class="param-type"><a href="global.html#FlowShapes">FlowShapes</a></span></td>
<td class="default">papertap</td>
<td class="description last">Used to specify node Shape as PaperTap</td>
</tr>
<tr>
<td class="name"><code>DirectData</code></td>
<td class="type"><span class="param-type"><a href="global.html#FlowShapes">FlowShapes</a></span></td>
<td class="default">directdata</td>
<td class="description last">Used to specify node Shape as DirectData</td>
</tr>
<tr>
<td class="name"><code>SequentialData</code></td>
<td class="type"><span class="param-type"><a href="global.html#FlowShapes">FlowShapes</a></span></td>
<td class="default">sequentialdata</td>
<td class="description last">Used to specify node Shape as SequentialData</td>
</tr>
<tr>
<td class="name"><code>Sort</code></td>
<td class="type"><span class="param-type"><a href="global.html#FlowShapes">FlowShapes</a></span></td>
<td class="default">sort</td>
<td class="description last">Used to specify node Shape as Sort</td>
</tr>
<tr>
<td class="name"><code>MultiDocument</code></td>
<td class="type"><span class="param-type"><a href="global.html#FlowShapes">FlowShapes</a></span></td>
<td class="default">multidocument</td>
<td class="description last">Used to specify node Shape as MultiDocument</td>
</tr>
<tr>
<td class="name"><code>Collate</code></td>
<td class="type"><span class="param-type"><a href="global.html#FlowShapes">FlowShapes</a></span></td>
<td class="default">collate</td>
<td class="description last">Used to specify node Shape as Collate</td>
</tr>
<tr>
<td class="name"><code>SummingJunction</code></td>
<td class="type"><span class="param-type"><a href="global.html#FlowShapes">FlowShapes</a></span></td>
<td class="default">summingjunction</td>
<td class="description last">Used to specify node Shape as SummingJunction</td>
</tr>
<tr>
<td class="name"><code>Or</code></td>
<td class="type"><span class="param-type"><a href="global.html#FlowShapes">FlowShapes</a></span></td>
<td class="default">or</td>
<td class="description last">Used to specify node Shape as Or</td>
</tr>
<tr>
<td class="name"><code>InternalStorage</code></td>
<td class="type"><span class="param-type"><a href="global.html#FlowShapes">FlowShapes</a></span></td>
<td class="default">internalstorage</td>
<td class="description last">Used to specify node Shape as InternalStorage</td>
</tr>
<tr>
<td class="name"><code>Extract</code></td>
<td class="type"><span class="param-type"><a href="global.html#FlowShapes">FlowShapes</a></span></td>
<td class="default">extract</td>
<td class="description last">Used to specify node Shape as Extract</td>
</tr>
<tr>
<td class="name"><code>ManualOperation</code></td>
<td class="type"><span class="param-type"><a href="global.html#FlowShapes">FlowShapes</a></span></td>
<td class="default">manualoperation</td>
<td class="description last">Used to specify node Shape as ManualOperation</td>
</tr>
<tr>
<td class="name"><code>Merge</code></td>
<td class="type"><span class="param-type"><a href="global.html#FlowShapes">FlowShapes</a></span></td>
<td class="default">merge</td>
<td class="description last">Used to specify node Shape as Merge</td>
</tr>
<tr>
<td class="name"><code>OffPageReference</code></td>
<td class="type"><span class="param-type"><a href="global.html#FlowShapes">FlowShapes</a></span></td>
<td class="default">offpagereference</td>
<td class="description last">Used to specify node Shape as OffPageReference</td>
</tr>
<tr>
<td class="name"><code>SequentialAccessStorage</code></td>
<td class="type"><span class="param-type"><a href="global.html#FlowShapes">FlowShapes</a></span></td>
<td class="default">sequentialaccessstorage</td>
<td class="description last">Used to specify node Shape as SequentialAccessStorage</td>
</tr>
<tr>
<td class="name"><code>Annotation1</code></td>
<td class="type"><span class="param-type"><a href="global.html#FlowShapes">FlowShapes</a></span></td>
<td class="default">annotation1</td>
<td class="description last">Used to specify node Shape as Annotation1</td>
</tr>
<tr>
<td class="name"><code>Annotation2</code></td>
<td class="type"><span class="param-type"><a href="global.html#FlowShapes">FlowShapes</a></span></td>
<td class="default">annotation2</td>
<td class="description last">Used to specify node Shape as Annotation2</td>
</tr>
</tbody>
</table>















### FontStyle<span class="type-signature type string">string</span>
{:#members:fontstyle}








Enum for Font Style






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">Normal</td>
<td class="description last">To set the fontStyle Normal.</td>
</tr>
<tr>
<td class="name"><code>Italic</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">Italic</td>
<td class="description last">To set the fontStyle Italic.</td>
</tr>
<tr>
<td class="name"><code>Oblique</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">Oblique</td>
<td class="description last">To set the fontStyle Oblique.</td>
</tr>
</tbody>
</table>















### FontStyle<span class="type-signature type string">string</span>
{:#members:fontstyle}








Enum for gauge FontStyle






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">To set the FontStyle normal.</td>
</tr>
<tr>
<td class="name"><code>Bold</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">bold</td>
<td class="description last">To set the FontStyle bold.</td>
</tr>
<tr>
<td class="name"><code>Italic</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">italic</td>
<td class="description last">To set the FontStyle italic.</td>
</tr>
<tr>
<td class="name"><code>Underline</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">underline</td>
<td class="description last">To set the FontStyle underline.</td>
</tr>
<tr>
<td class="name"><code>Strikeout</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">strikeout</td>
<td class="description last">To set the FontStyle strikeout.</td>
</tr>
</tbody>
</table>















### FontStyle<span class="type-signature type string">string</span>
{:#members:fontstyle}








Enum for gauge FontStyle






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Bold</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">bold</td>
<td class="description last">To set the FontStyle bold.</td>
</tr>
<tr>
<td class="name"><code>Italic</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">italic</td>
<td class="description last">To set the FontStyle italic.</td>
</tr>
<tr>
<td class="name"><code>Regular</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">regular</td>
<td class="description last">To set the FontStyle regular.</td>
</tr>
<tr>
<td class="name"><code>Strikeout</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">strikeout</td>
<td class="description last">To set the FontStyle strikeout.</td>
</tr>
<tr>
<td class="name"><code>Underline</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">underline</td>
<td class="description last">To set the FontStyle underline.</td>
</tr>
</tbody>
</table>















### FontStyle<span class="type-signature type string">string</span>
{:#members:fontstyle}








Enum for chart style of font.






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Render normal font.</td>
</tr>
<tr>
<td class="name"><code>Italic</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">italic</td>
<td class="description last">Render italic font.</td>
</tr>
</tbody>
</table>















### FontWeight<span class="type-signature type string">string</span>
{:#members:fontweight}








Enum for Font Weight






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">Normal</td>
<td class="description last">To set the fontWeight Normal.</td>
</tr>
<tr>
<td class="name"><code>Bold</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">Bold</td>
<td class="description last">To set the fontWeight Bold.</td>
</tr>
<tr>
<td class="name"><code>Bolder</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">Bolder</td>
<td class="description last">To set the fontWeight Bolder.</td>
</tr>
<tr>
<td class="name"><code>Lighter</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">Lighter</td>
<td class="description last">To set the fontWeight Lighter.</td>
</tr>
</tbody>
</table>















### FontWeight<span class="type-signature type string">string</span>
{:#members:fontweight}








Enum for weight of font.






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Regular</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">regular</td>
<td class="description last">Render regular font.</td>
</tr>
<tr>
<td class="name"><code>Bold</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">bold</td>
<td class="description last">Render bold font.</td>
</tr>
<tr>
<td class="name"><code>Lighter</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">lighter</td>
<td class="description last">Render lighter font.</td>
</tr>
</tbody>
</table>















### FooterLeftButtonStyle<span class="type-signature type string">string</span>
{:#members:footerleftbuttonstyle}








Enum for IOS7FooterLeftButtonStyle






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Auto</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">auto</td>
<td class="description last">Enum for iOS7 auto left button style for Footer</td>
</tr>
<tr>
<td class="name"><code>Back</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">back</td>
<td class="description last">Enum for iOS7 Back left button style for Footer</td>
</tr>
<tr>
<td class="name"><code>Header</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">header</td>
<td class="description last">Enum for iOS7 Footer left button style for Footer</td>
</tr>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Enum for iOS7 Normal left button style for Footer</td>
</tr>
</tbody>
</table>















### FooterLeftButtonStyle<span class="type-signature type string">string</span>
{:#members:footerleftbuttonstyle}








Enum for AndroidFooterLeftButtonStyle






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Auto</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">auto</td>
<td class="description last">Enum for Android auto left button style for Footer</td>
</tr>
<tr>
<td class="name"><code>Back</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">back</td>
<td class="description last">Enum for Android Back left button style for Footer</td>
</tr>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Enum for Android Normal left button style for Footer</td>
</tr>
<tr>
<td class="name"><code>Header</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">header</td>
<td class="description last">Enum for Android header left button style for Footer</td>
</tr>
</tbody>
</table>















### FooterLeftButtonStyle<span class="type-signature type string">string</span>
{:#members:footerleftbuttonstyle}








Enum for WindowsFooterLeftButtonStyle






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Auto</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">auto</td>
<td class="description last">Enum for Windows auto left button style for Footer</td>
</tr>
<tr>
<td class="name"><code>Back</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">back</td>
<td class="description last">Enum for Windows Back left button style for Footer</td>
</tr>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Enum for Windows Normal left button style for Footer</td>
</tr>
<tr>
<td class="name"><code>Header</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">header</td>
<td class="description last">Enum for Windows header left button style for Footer</td>
</tr>
</tbody>
</table>















### FooterLeftButtonStyle<span class="type-signature type string">string</span>
{:#members:footerleftbuttonstyle}








Enum for FlatFooterLeftButtonStyle






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Auto</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">auto</td>
<td class="description last">Enum for Flat auto left button style for Footer</td>
</tr>
<tr>
<td class="name"><code>Back</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">back</td>
<td class="description last">Enum for Flat Back left button style for Footer</td>
</tr>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Enum for Flat Normal left button style for Footer</td>
</tr>
<tr>
<td class="name"><code>Header</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">header</td>
<td class="description last">Enum for Flat Footer left button style for Footer</td>
</tr>
</tbody>
</table>















### FooterLeftButtonStyle<span class="type-signature type string">string</span>
{:#members:footerleftbuttonstyle}








Enum for HeaderLeftButtonStyle






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Back</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">back</td>
<td class="description last">Enum for Back left button style for Footer</td>
</tr>
<tr>
<td class="name"><code>Header</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">header</td>
<td class="description last">Enum for Header left button style for Footer</td>
</tr>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Enum for Normal left button style for Footer</td>
</tr>
</tbody>
</table>















### FooterRightButtonStyle<span class="type-signature type string">string</span>
{:#members:footerrightbuttonstyle}








Enum for IOS7FooterRightButtonStyle






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Auto</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">auto</td>
<td class="description last">Enum for iOS7 auto right button style for Footer</td>
</tr>
<tr>
<td class="name"><code>Header</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">header</td>
<td class="description last">Enum for Footer right button style for Footer</td>
</tr>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Enum for Normal right button style for Footer</td>
</tr>
</tbody>
</table>















### FooterRightButtonStyle<span class="type-signature type string">string</span>
{:#members:footerrightbuttonstyle}








Enum for AndroidFooterRightButtonStyle






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Auto</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">auto</td>
<td class="description last">Enum for Android auto right button style for Footer</td>
</tr>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Enum for Normal right button style for Footer</td>
</tr>
<tr>
<td class="name"><code>Header</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">header</td>
<td class="description last">Enum for Footer right button style for Footer</td>
</tr>
</tbody>
</table>















### FooterRightButtonStyle<span class="type-signature type string">string</span>
{:#members:footerrightbuttonstyle}








Enum for WindowsFooterRightButtonStyle






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Auto</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">auto</td>
<td class="description last">Enum for Windows auto right button style for Footer</td>
</tr>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Enum for Normal right button style for Footer</td>
</tr>
<tr>
<td class="name"><code>Header</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">header</td>
<td class="description last">Enum for Footer right button style for Footer</td>
</tr>
</tbody>
</table>















### FooterRightButtonStyle<span class="type-signature type string">string</span>
{:#members:footerrightbuttonstyle}








Enum for FlatFooterRightButtonStyle






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Auto</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">auto</td>
<td class="description last">Enum for Flat auto right button style for Footer</td>
</tr>
<tr>
<td class="name"><code>Header</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">header</td>
<td class="description last">Enum for Footer right button style for Footer</td>
</tr>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">/** Enum for Normal right button style for Footer</td>
</tr>
</tbody>
</table>















### FooterRightButtonStyle<span class="type-signature type string">string</span>
{:#members:footerrightbuttonstyle}








Enum for HeaderRightButtonStyle






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Header</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">header</td>
<td class="description last">Enum for Header right button style for Footer</td>
</tr>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Enum for Normal right button style for Footer</td>
</tr>
</tbody>
</table>















### Frame<span class="type-signature type string">string</span>
{:#members:frame}








Enum for gauge Frame






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>FullCircle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">fullcircle</td>
<td class="description last">To set the CircularGauge Frame as fullcircle.</td>
</tr>
<tr>
<td class="name"><code>HalfCircle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">halfcircle</td>
<td class="description last">To set the CircularGauge Frame as halfcircle.</td>
</tr>
</tbody>
</table>















### gaugePosition<span class="type-signature type string">string</span>
{:#members:gaugeposition}








Enum for gauge position






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>TopLeft</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">topleft</td>
<td class="description last">To set the gauge position topleft.</td>
</tr>
<tr>
<td class="name"><code>TopRight</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">topright</td>
<td class="description last">To set the gauge position topright.</td>
</tr>
<tr>
<td class="name"><code>TopCenter</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">topcenter</td>
<td class="description last">To set the gauge position topcenter.</td>
</tr>
<tr>
<td class="name"><code>MiddleLeft</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">middleleft</td>
<td class="description last">To set the gauge position middleleft.</td>
</tr>
<tr>
<td class="name"><code>MiddleRight</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">middleright</td>
<td class="description last">To set the gauge position middleright.</td>
</tr>
<tr>
<td class="name"><code>Center</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">center</td>
<td class="description last">To set the gauge position middlecenter.</td>
</tr>
<tr>
<td class="name"><code>BottomLeft</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">bottomleft</td>
<td class="description last">To set the gauge position bottomleft.</td>
</tr>
<tr>
<td class="name"><code>BottomRight</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">bottomright</td>
<td class="description last">To set the gauge position bottomright.</td>
</tr>
<tr>
<td class="name"><code>BottomCenter</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">bottomcenter</td>
<td class="description last">To set the gauge position bottomcenter.</td>
</tr>
</tbody>
</table>















### HeaderLeftButtonStyle<span class="type-signature type string">string</span>
{:#members:headerleftbuttonstyle}








Enum for IOS7HeaderLeftButtonStyle






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Auto</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">auto</td>
<td class="description last">Enum for iOS7 Auto left button style for Header</td>
</tr>
<tr>
<td class="name"><code>Back</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">back</td>
<td class="description last">/** Enum for iOS7 Back left button style for Header</td>
</tr>
<tr>
<td class="name"><code>Header</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">header</td>
<td class="description last">Enum for iOS7 Header left button style for Header</td>
</tr>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Enum for iOS7 Normal left button style for Header</td>
</tr>
</tbody>
</table>















### HeaderLeftButtonStyle<span class="type-signature type string">string</span>
{:#members:headerleftbuttonstyle}








Enum for AndroidHeaderLeftButtonStyle






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Auto</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">auto</td>
<td class="description last">Enum for Android Auto left button style for Header</td>
</tr>
<tr>
<td class="name"><code>Back</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">back</td>
<td class="description last">Enum for Android Back left button style for Header</td>
</tr>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Enum for Android Normal left button style for Header</td>
</tr>
<tr>
<td class="name"><code>Header</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">header</td>
<td class="description last">Enum for Android Header right button style for Header</td>
</tr>
</tbody>
</table>















### HeaderLeftButtonStyle<span class="type-signature type string">string</span>
{:#members:headerleftbuttonstyle}








Enum for WindowsHeaderLeftButtonStyle






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Auto</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">auto</td>
<td class="description last">Enum for Windows Auto left button style for Header</td>
</tr>
<tr>
<td class="name"><code>Back</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">back</td>
<td class="description last">Enum for Windows Back left button style for Header</td>
</tr>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Enum for Windows Normal left button style for Header</td>
</tr>
<tr>
<td class="name"><code>Header</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">header</td>
<td class="description last">Enum for Header left button style for Header</td>
</tr>
</tbody>
</table>















### HeaderLeftButtonStyle<span class="type-signature type string">string</span>
{:#members:headerleftbuttonstyle}








Enum for FlatHeaderLeftButtonStyle






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Auto</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">auto</td>
<td class="description last">Enum for Flat Auto left button style for Header</td>
</tr>
<tr>
<td class="name"><code>Back</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">back</td>
<td class="description last">Enum for Flat Back left button style for Header</td>
</tr>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Enum for Flat Normal left button style for Header</td>
</tr>
<tr>
<td class="name"><code>Header</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">header</td>
<td class="description last">Enum for Flat Header left button style for Header</td>
</tr>
</tbody>
</table>















### HeaderLeftButtonStyle<span class="type-signature type string">string</span>
{:#members:headerleftbuttonstyle}








Enum for HeaderLeftButtonStyle






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Back</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">back</td>
<td class="description last">Enum for Back left button style for Header</td>
</tr>
<tr>
<td class="name"><code>Header</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">header</td>
<td class="description last">Enum for Header left button style for Header</td>
</tr>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Enum for Normal left button style for Header</td>
</tr>
</tbody>
</table>















### HeaderLeftButtonStyle<span class="type-signature type string">String</span>
{:#members:headerleftbuttonstyle}








Enum for headerLeftButtonStyle






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Back</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="default">back</td>
<td class="description last">Enum for back Button Style</td>
</tr>
<tr>
<td class="name"><code>Header</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="default">header</td>
<td class="description last">Enum for header Button Style</td>
</tr>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="default">normal</td>
<td class="description last">Enum for normal Button Style</td>
</tr>
</tbody>
</table>















### HeaderRightButtonStyle<span class="type-signature type string">string</span>
{:#members:headerrightbuttonstyle}








Enum for IOS7HeaderRightButtonStyle






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Auto</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">auto</td>
<td class="description last">Enum for iOS7 Auto right button style for Header</td>
</tr>
<tr>
<td class="name"><code>Header</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">header</td>
<td class="description last">Enum for Header right button style for Header</td>
</tr>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Enum for Normal right button style for Header</td>
</tr>
</tbody>
</table>















### HeaderRightButtonStyle<span class="type-signature type string">string</span>
{:#members:headerrightbuttonstyle}








Enum for AndroidHeaderRightButtonStyle






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Auto</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">auto</td>
<td class="description last">Enum for Android Auto right button style for Header</td>
</tr>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Enum for Normal right button style for Header</td>
</tr>
<tr>
<td class="name"><code>Header</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">header</td>
<td class="description last">Enum for Header right button style for Header</td>
</tr>
</tbody>
</table>















### HeaderRightButtonStyle<span class="type-signature type string">string</span>
{:#members:headerrightbuttonstyle}








Enum for WindowsHeaderRightButtonStyle






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Auto</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">auto</td>
<td class="description last">Enum for Windows Auto right button style for Header</td>
</tr>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Enum for Normal right button style for Header</td>
</tr>
<tr>
<td class="name"><code>Header</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">header</td>
<td class="description last">Enum for Header right button style for Header</td>
</tr>
</tbody>
</table>















### HeaderRightButtonStyle<span class="type-signature type string">string</span>
{:#members:headerrightbuttonstyle}








Enum for FlatHeaderRightButtonStyle






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Auto</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">auto</td>
<td class="description last">Enum for Flat Auto right button style for Header</td>
</tr>
<tr>
<td class="name"><code>Header</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">header</td>
<td class="description last">Enum for Header right button style for Header</td>
</tr>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">/** Enum for Normal right button style for Header</td>
</tr>
</tbody>
</table>















### HeaderRightButtonStyle<span class="type-signature type string">string</span>
{:#members:headerrightbuttonstyle}








Enum for HeaderRightButtonStyle






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Header</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">header</td>
<td class="description last">Enum for Header right button style for Header</td>
</tr>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Enum for Normal right button style for Header</td>
</tr>
</tbody>
</table>















### HeaderRightButtonStyle<span class="type-signature type string">String</span>
{:#members:headerrightbuttonstyle}








Enum for headerRightButtonStyle






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Header</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="default">header</td>
<td class="description last">Enum for header Button Style</td>
</tr>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="default">normal</td>
<td class="description last">Enum for normal Button Style</td>
</tr>
</tbody>
</table>















### HeightAdjustMode<span class="type-signature type string">string</span>
{:#members:heightadjustmode}








Enum for accordion height style






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Content</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">content</td>
<td class="description last">Height fit to the content in the panel</td>
</tr>
<tr>
<td class="name"><code>Auto</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">auto</td>
<td class="description last">Height set to the largest content in the panel</td>
</tr>
<tr>
<td class="name"><code>Fill</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">fill</td>
<td class="description last">Height filled to the content of the panel</td>
</tr>
</tbody>
</table>















### HorizontalAlignment<span class="type-signature type string">string</span>
{:#members:horizontalalignment}








Enum for Horizontal Alignment of elements in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Left</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">left</td>
<td class="description last">Used to align text horizontally on left side of node/connector</td>
</tr>
<tr>
<td class="name"><code>Center</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">center</td>
<td class="description last">Used to align text horizontally on center of node/connector</td>
</tr>
<tr>
<td class="name"><code>Right</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">right</td>
<td class="description last">Used to align text horizontally on right side of node/connector</td>
</tr>
</tbody>
</table>















### HourFormat<span class="type-signature type string">string</span>
{:#members:hourformat}








Enum for Hour format






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>TwentyFour</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">twentyfour</td>
<td class="description last">Enum for twentyfour hourformat</td>
</tr>
<tr>
<td class="name"><code>Twelve</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">twelve</td>
<td class="description last">Enum for twentyfour hourformat</td>
</tr>
</tbody>
</table>















### IconName<span class="type-signature type string">string</span>
{:#members:iconname}








Enum for toolbar icon name






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Add</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">Add</td>
<td class="description last">Enum for Add toolbar icon</td>
</tr>
<tr>
<td class="name"><code>Back</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">Back</td>
<td class="description last">Enum for Back toolbar icon</td>
</tr>
<tr>
<td class="name"><code>Bookmark</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">Bookmark</td>
<td class="description last">Enum for Bookmark toolbar icon</td>
</tr>
<tr>
<td class="name"><code>Close</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">Close</td>
<td class="description last">Enum for Close toolbar icon</td>
</tr>
<tr>
<td class="name"><code>Compose</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">Compose</td>
<td class="description last">Enum for Compose toolbar icon</td>
</tr>
<tr>
<td class="name"><code>Copy</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">Copy</td>
<td class="description last">Enum for Copy toolbar icon</td>
</tr>
<tr>
<td class="name"><code>Cut</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">Cut</td>
<td class="description last">Enum for Cut toolbar icon</td>
</tr>
<tr>
<td class="name"><code>Delete</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">Delete</td>
<td class="description last">Enum for Delete toolbar icon</td>
</tr>
<tr>
<td class="name"><code>Done</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">Done</td>
<td class="description last">Enum for Done toolbar icon</td>
</tr>
<tr>
<td class="name"><code>Edit</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">Edit</td>
<td class="description last">Enum for Edit toolbar icon</td>
</tr>
<tr>
<td class="name"><code>Mail</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">Mail</td>
<td class="description last">Enum for Mail toolbar icon</td>
</tr>
<tr>
<td class="name"><code>Next</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">Next</td>
<td class="description last">Enum for Next toolbar icon</td>
</tr>
<tr>
<td class="name"><code>Refresh</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">Refresh</td>
<td class="description last">Enum for Refresh toolbar icon</td>
</tr>
<tr>
<td class="name"><code>Overflow</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">Overflow</td>
<td class="description last">Enum for Overflow toolbar icon</td>
</tr>
<tr>
<td class="name"><code>Paste</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">Paste</td>
<td class="description last">Enum for Paste toolbar icon</td>
</tr>
<tr>
<td class="name"><code>Reply</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">Reply</td>
<td class="description last">Enum for Reply toolbar icon</td>
</tr>
<tr>
<td class="name"><code>Save</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">Save</td>
<td class="description last">Enum for Save toolbar icon</td>
</tr>
<tr>
<td class="name"><code>Search</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">Search</td>
<td class="description last">Enum for Search toolbar icon</td>
</tr>
<tr>
<td class="name"><code>Settings</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">Settings</td>
<td class="description last">Enum for Settings toolbar icon</td>
</tr>
<tr>
<td class="name"><code>Share</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">Share</td>
<td class="description last">Enum for Share toolbar icon</td>
</tr>
</tbody>
</table>















### ImagePosition<span class="type-signature type string">string</span>
{:#members:imageposition}








Enum for ImagePosition






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Left</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">left</td>
<td class="description last">Enum for image at left position</td>
</tr>
<tr>
<td class="name"><code>Right</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">right</td>
<td class="description last">Enum for image at right position</td>
</tr>
</tbody>
</table>















### ImagePosition<span class="type-signature type string">string</span>
{:#members:imageposition}








Enum for Tile ImagePosition






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Center</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">center</td>
<td class="description last">Enum for center position of tile image</td>
</tr>
<tr>
<td class="name"><code>Top</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">top</td>
<td class="description last">Enum for top position of tile image</td>
</tr>
<tr>
<td class="name"><code>Bottom</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">bottom</td>
<td class="description last">Enum for bottom position of tile image</td>
</tr>
<tr>
<td class="name"><code>Right</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">right</td>
<td class="description last">Enum for right position of tile image</td>
</tr>
<tr>
<td class="name"><code>Left</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">left</td>
<td class="description last">Enum for left position of tile image</td>
</tr>
<tr>
<td class="name"><code>TopLeft</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">topleft</td>
<td class="description last">Enum for topleft position of tile image</td>
</tr>
<tr>
<td class="name"><code>TopRight</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">topright</td>
<td class="description last">Enum for topright position of tile image</td>
</tr>
<tr>
<td class="name"><code>BottomRight</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">bottomright</td>
<td class="description last">Enum for bottomright position of tile image</td>
</tr>
<tr>
<td class="name"><code>BottomLeft</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">bottomleft</td>
<td class="description last">Enum for bottomleft position of tile image</td>
</tr>
<tr>
<td class="name"><code>Fill</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">fill</td>
<td class="description last">Enum for fill position of tile image</td>
</tr>
</tbody>
</table>















### IndicatorType<span class="type-signature type string">string</span>
{:#members:indicatortype}








Enum for gauge IndicatorType






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Rectangle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">rectangle</td>
<td class="description last">To set the IndicatorType rectangle.</td>
</tr>
<tr>
<td class="name"><code>Circle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">circle</td>
<td class="description last">To set the IndicatorType circle.</td>
</tr>
<tr>
<td class="name"><code>RoundedRectangle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">roundedrectangle</td>
<td class="description last">To set the IndicatorType roundedrectangle.</td>
</tr>
<tr>
<td class="name"><code>Text</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">text</td>
<td class="description last">To set the IndicatorType Text.</td>
</tr>
<tr>
<td class="name"><code>Image</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">image</td>
<td class="description last">To set the IndicatorType Text.</td>
</tr>
</tbody>
</table>















### IndicatorType<span class="type-signature type string">string</span>
{:#members:indicatortype}








Enum for gauge IndicatorType






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Rectangle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">rectangle</td>
<td class="description last">To set the IndicatorType rectangle.</td>
</tr>
<tr>
<td class="name"><code>Circle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">circle</td>
<td class="description last">To set the IndicatorType circle.</td>
</tr>
<tr>
<td class="name"><code>RoundedRectangle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">roundedrectangle</td>
<td class="description last">To set the IndicatorType roundedrectangle.</td>
</tr>
<tr>
<td class="name"><code>Text</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">text</td>
<td class="description last">To set the IndicatorType text.</td>
</tr>
</tbody>
</table>















### IntervalType<span class="type-signature type string">string</span>
{:#members:intervaltype}








Enum for chart interval type.






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Days</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">days</td>
<td class="description last">Sets chart interval type to days.</td>
</tr>
<tr>
<td class="name"><code>Hours</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">hours</td>
<td class="description last">Sets chart interval type to hours.</td>
</tr>
<tr>
<td class="name"><code>Seconds</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">seconds</td>
<td class="description last">Sets chart interval type to seconds.</td>
</tr>
<tr>
<td class="name"><code>Milliseconds</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">milliseconds</td>
<td class="description last">Sets chart interval type to milliseconds.</td>
</tr>
<tr>
<td class="name"><code>Minutes</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">minutes</td>
<td class="description last">Sets chart interval type to minutes.</td>
</tr>
<tr>
<td class="name"><code>Months</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">months</td>
<td class="description last">Sets chart interval type to months.</td>
</tr>
<tr>
<td class="name"><code>Years</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">years</td>
<td class="description last">Sets chart interval type to years.</td>
</tr>
</tbody>
</table>















### ItemsLayoutMode<span class="type-signature type string">string</span>
{:#members:itemslayoutmode}








Enum for TreeMap items layout mode






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Squarified</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">squarified</td>
<td class="description last"></td>
</tr>
<tr>
<td class="name"><code>SliceAndDiceHorizontal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">sliceanddicehorizontal</td>
<td class="description last"></td>
</tr>
<tr>
<td class="name"><code>SliceAndDiceVertical</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">sliceanddicevertical</td>
<td class="description last"></td>
</tr>
<tr>
<td class="name"><code>SliceAndDiceAuto</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">sliceanddiceauto</td>
<td class="description last"></td>
</tr>
</tbody>
</table>















### LabelEditMode<span class="type-signature type string">string</span>
{:#members:labeleditmode}








Enum for LabelEditMode of text in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Edit</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">edit</td>
<td class="description last">Used to set label edit mode as edit</td>
</tr>
<tr>
<td class="name"><code>View</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">view</td>
<td class="description last">Used to set label edit mode as view</td>
</tr>
</tbody>
</table>















### LabelIntersectAction<span class="type-signature type string">string</span>
{:#members:labelintersectaction}








Enum for chart labelIntersectAction.






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>None</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">none</td>
<td class="description last">No action is made on intersection of labels.</td>
</tr>
<tr>
<td class="name"><code>Rotate90</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">rotate90</td>
<td class="description last">Rotate the labels to 90 degree on intersect.</td>
</tr>
<tr>
<td class="name"><code>Rotate45</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">rotate45</td>
<td class="description last">Rotate the labels to 45 degree on intersect.</td>
</tr>
<tr>
<td class="name"><code>Wrap</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">wrap</td>
<td class="description last">Wrap the label to multiple lines on intersect.</td>
</tr>
<tr>
<td class="name"><code>Trim</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">trim</td>
<td class="description last">Trim the text and display whole text on mouse over.</td>
</tr>
<tr>
<td class="name"><code>Hide</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">hide</td>
<td class="description last">Hide the label which intersect.</td>
</tr>
<tr>
<td class="name"><code>MultipleRows</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">multipleRows</td>
<td class="description last">Labels are placed on another row on intersect.</td>
</tr>
</tbody>
</table>















### LabelPlacement<span class="type-signature type string">string</span>
{:#members:labelplacement}








Enum for Bullet Graph label placement






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Inside</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">inside</td>
<td class="description last">support for placing labels inside scale.</td>
</tr>
<tr>
<td class="name"><code>Outside</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">outside</td>
<td class="description last">support for placing labels outside scale.</td>
</tr>
</tbody>
</table>















### LabelPlacement<span class="type-signature type string">string</span>
{:#members:labelplacement}








Enum for gauge LabelPlacement






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Near</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">near</td>
<td class="description last">To set the LabelPlacement near.</td>
</tr>
<tr>
<td class="name"><code>Far</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">far</td>
<td class="description last">To set the LabelPlacement far.</td>
</tr>
<tr>
<td class="name"><code>Center</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">center</td>
<td class="description last">To set the LabelPlacement center.</td>
</tr>
</tbody>
</table>















### LabelPlacement<span class="type-signature type string">string</span>
{:#members:labelplacement}








Enum for gauge LabelPlacement






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Near</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">near</td>
<td class="description last">To set the LabelPlacement near.</td>
</tr>
<tr>
<td class="name"><code>Far</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">far</td>
<td class="description last">To set the LabelPlacement far.</td>
</tr>
<tr>
<td class="name"><code>Center</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">center</td>
<td class="description last">To set the LabelPlacement center.</td>
</tr>
</tbody>
</table>















### LabelPlacement<span class="type-signature type string">string</span>
{:#members:labelplacement}








Enum for chart labelPlacement.






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>BetweenTicks</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">betweenTicks</td>
<td class="description last">specifies the placement of labels between the ticks.</td>
</tr>
<tr>
<td class="name"><code>OnTicks</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">onTicks</td>
<td class="description last">specifies the placement of labels on the ticks.</td>
</tr>
</tbody>
</table>















### LabelPosition<span class="type-signature type string">string</span>
{:#members:labelposition}








Enum for Bullet Graph Label Position






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Below</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">below</td>
<td class="description last">To set the label position below.</td>
</tr>
<tr>
<td class="name"><code>Above</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">above</td>
<td class="description last">To set the label position above.</td>
</tr>
</tbody>
</table>















### LabelPosition<span class="type-signature type string">string</span>
{:#members:labelposition}








Enum for label position.






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Inside</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">inside</td>
<td class="description last">Support for changing the labelPosition to inside.</td>
</tr>
<tr>
<td class="name"><code>Outside</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">outside</td>
<td class="description last">Support for changing the labelPosition to outside.</td>
</tr>
</tbody>
</table>















### LabelSize<span class="type-signature type string">string</span>
{:#members:labelsize}








Enum for Map Label size






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Fixed</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">fixed</td>
<td class="description last">support for label size fixed.</td>
</tr>
<tr>
<td class="name"><code>Default</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">default</td>
<td class="description last">support for label size default.</td>
</tr>
</tbody>
</table>















### LabelType<span class="type-signature type string">string</span>
{:#members:labeltype}








Enum for gauge LabelType






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Major</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">major</td>
<td class="description last">To set the LabelType major.</td>
</tr>
<tr>
<td class="name"><code>Minor</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">minor</td>
<td class="description last">To set the LabelType minor.</td>
</tr>
</tbody>
</table>















### LabelType<span class="type-signature type string">string</span>
{:#members:labeltype}








Enum for gauge LabelType






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Major</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">major</td>
<td class="description last">To set the LabelType major.</td>
</tr>
<tr>
<td class="name"><code>Minor</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">minor</td>
<td class="description last">To set the LabelType minor.</td>
</tr>
</tbody>
</table>















### LayerType<span class="type-signature type string">string</span>
{:#members:layertype}








Enum for Map LayerType






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Geometry</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">geometry</td>
<td class="description last">support for layer type geometry.</td>
</tr>
<tr>
<td class="name"><code>OSM</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">osm</td>
<td class="description last">support for layer type osm.</td>
</tr>
<tr>
<td class="name"><code>Bing</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">bing</td>
<td class="description last">support for layer type bing.</td>
</tr>
</tbody>
</table>















### LayoutOrientations<span class="type-signature type string">String</span>
{:#members:layoutorientations}








Enum for LayoutOrientations in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>TopToBottom</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="default">toptobottom</td>
<td class="description last">Used to set LayoutOrientation from top to bottom</td>
</tr>
<tr>
<td class="name"><code>BottomToTop</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="default">bottomtotop</td>
<td class="description last">Used to set LayoutOrientation from bottom to top</td>
</tr>
<tr>
<td class="name"><code>LeftToRight</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="default">lefttoright</td>
<td class="description last">Used to set LayoutOrientation from left to right</td>
</tr>
<tr>
<td class="name"><code>RightToLeft</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="default">righttoleft</td>
<td class="description last">Used to set LayoutOrientation from right to left</td>
</tr>
</tbody>
</table>















### LayoutTypes<span class="type-signature type string">String</span>
{:#members:layouttypes}








Enum for LayoutTypes in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>None</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="default">none</td>
<td class="description last">Used not to set any specific layout</td>
</tr>
<tr>
<td class="name"><code>HierarchicalTree</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="default">hierarchicaltree</td>
<td class="description last">Used to set layout type as hierarchical layout</td>
</tr>
<tr>
<td class="name"><code>OrganizationalChart</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="default">organizationalchart</td>
<td class="description last">Used to set layout type as organnizational chart</td>
</tr>
</tbody>
</table>















### LegendIcons<span class="type-signature type string">string</span>
{:#members:legendicons}








Enum for Map legend icons






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Rectangle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">rectangle</td>
<td class="description last">support for legend icon rectangle.</td>
</tr>
<tr>
<td class="name"><code>Circle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">circle</td>
<td class="description last">support for legend icon circle.</td>
</tr>
</tbody>
</table>















### LegendMode<span class="type-signature type string">string</span>
{:#members:legendmode}








Enum for Map Legend mode






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Default</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">default</td>
<td class="description last">support for legend mode default.</td>
</tr>
<tr>
<td class="name"><code>Interactive</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">interactive</td>
<td class="description last">support for legend mode interactive.</td>
</tr>
</tbody>
</table>















### LegendType<span class="type-signature type string">string</span>
{:#members:legendtype}








Enum for Map Legend type






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Layers</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">layers</td>
<td class="description last">support for Legend type layers.</td>
</tr>
<tr>
<td class="name"><code>Bubbles</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">bubbles</td>
<td class="description last">support for Legend type bubbles.</td>
</tr>
</tbody>
</table>















### LineCap<span class="type-signature type string">string</span>
{:#members:linecap}








Enum for linecap.






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Butt</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">butt</td>
<td class="description last">Sets the linecap as butt.</td>
</tr>
<tr>
<td class="name"><code>Round</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">round</td>
<td class="description last">Sets the linecap as round.</td>
</tr>
<tr>
<td class="name"><code>Square</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">square</td>
<td class="description last">Sets the linecap as square.</td>
</tr>
</tbody>
</table>















### LineJoin<span class="type-signature type string">string</span>
{:#members:linejoin}








Enum for line join.






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Round</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">round</td>
<td class="description last">Sets the lineJoin to round.</td>
</tr>
<tr>
<td class="name"><code>Bevel</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">bevel</td>
<td class="description last">Sets the lineJoin to bevel.</td>
</tr>
<tr>
<td class="name"><code>Miter</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">miter</td>
<td class="description last">Sets the lineJoin to miter.</td>
</tr>
</tbody>
</table>















### LiveTileType<span class="type-signature type string">string</span>
{:#members:livetiletype}








Enum for LiveTileType






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Flip</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">flip</td>
<td class="description last">Enum for flip type of livetile</td>
</tr>
<tr>
<td class="name"><code>Slide</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">slide</td>
<td class="description last">Enum for slide type of livetile</td>
</tr>
<tr>
<td class="name"><code>Carousel</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">carousel</td>
<td class="description last">Enum for carousel type of livetile</td>
</tr>
</tbody>
</table>















### MarkerType<span class="type-signature type string">string</span>
{:#members:markertype}








Enum for gauge MarkerType






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Rectangle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">rectangle</td>
<td class="description last">To set the MarkerType rectangle.</td>
</tr>
<tr>
<td class="name"><code>Triangle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">triangle</td>
<td class="description last">To set the MarkerType triangle.</td>
</tr>
<tr>
<td class="name"><code>Ellipse</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">ellipse</td>
<td class="description last">To set the MarkerType ellipse.</td>
</tr>
<tr>
<td class="name"><code>Diamond</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">diamond</td>
<td class="description last">To set the MarkerType diamond.</td>
</tr>
<tr>
<td class="name"><code>Pentagon</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">pentagon</td>
<td class="description last">To set the MarkerType pentagon.</td>
</tr>
<tr>
<td class="name"><code>Circle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">circle</td>
<td class="description last">To set the MarkerType circle.</td>
</tr>
<tr>
<td class="name"><code>Slider</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">slider</td>
<td class="description last">To set the MarkerType slider.</td>
</tr>
<tr>
<td class="name"><code>Pointer</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">pointer</td>
<td class="description last">To set the MarkerType pointer.</td>
</tr>
<tr>
<td class="name"><code>Wedge</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">wedge</td>
<td class="description last">To set the MarkerType wedge.</td>
</tr>
<tr>
<td class="name"><code>Trapezoid</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">trapezoid</td>
<td class="description last">To set the MarkerType trapezoid.</td>
</tr>
<tr>
<td class="name"><code>RoundedRectangle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">roundedrectangle</td>
<td class="description last">To set the MarkerType roundedrectangle.</td>
</tr>
<tr>
<td class="name"><code>Image</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">image</td>
<td class="description last">To set the MarkerType image.</td>
</tr>
</tbody>
</table>















### MarkerType<span class="type-signature type string">string</span>
{:#members:markertype}








Enum for gauge MarkerType






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Rectangle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">rectangle</td>
<td class="description last">To set the MarkerType rectangle.</td>
</tr>
<tr>
<td class="name"><code>Triangle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">triangle</td>
<td class="description last">To set the MarkerType triangle.</td>
</tr>
<tr>
<td class="name"><code>Ellipse</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">ellipse</td>
<td class="description last">To set the MarkerType ellipse.</td>
</tr>
<tr>
<td class="name"><code>Diamond</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">diamond</td>
<td class="description last">To set the MarkerType diamond.</td>
</tr>
<tr>
<td class="name"><code>Pentagon</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">pentagon</td>
<td class="description last">To set the MarkerType pentagon.</td>
</tr>
<tr>
<td class="name"><code>Circle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">circle</td>
<td class="description last">To set the MarkerType circle.</td>
</tr>
<tr>
<td class="name"><code>Star</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">star</td>
<td class="description last">To set the MarkerType star.</td>
</tr>
<tr>
<td class="name"><code>Slider</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">slider</td>
<td class="description last">To set the MarkerType slider.</td>
</tr>
<tr>
<td class="name"><code>Pointer</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">pointer</td>
<td class="description last">To set the MarkerType pointer.</td>
</tr>
<tr>
<td class="name"><code>Wedge</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">wedge</td>
<td class="description last">To set the MarkerType wedge.</td>
</tr>
<tr>
<td class="name"><code>Trapezoid</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">trapezoid</td>
<td class="description last">To set the MarkerType trapezoid.</td>
</tr>
<tr>
<td class="name"><code>RoundedRectangle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">roundedrectangle</td>
<td class="description last">To set the MarkerType roundedrectangle.</td>
</tr>
</tbody>
</table>















### Mode<span class="type-signature type string">string</span>
{:#members:mode}








Enum for mode






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Search</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">search</td>
<td class="description last">Enum for Search mode</td>
</tr>
<tr>
<td class="name"><code>Default</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">default</td>
<td class="description last">Enum for Default mode</td>
</tr>
</tbody>
</table>















### Mode<span class="type-signature type string">string</span>
{:#members:mode}








Enum for mode






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Alert</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">alert</td>
<td class="description last">Enum for alert mode dialog</td>
</tr>
<tr>
<td class="name"><code>Confirm</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">confirm</td>
<td class="description last">Enum for confirm mode dialog</td>
</tr>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Enum for normal mode dialog</td>
</tr>
<tr>
<td class="name"><code>FullView</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">fullview</td>
<td class="description last">Enum for fullview mode dialog</td>
</tr>
</tbody>
</table>















### model
{:#members:model}








User defined model will be automatically set in this











### NeedleType<span class="type-signature type string">string</span>
{:#members:needletype}








Enum for gauge NeedleType






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Triangle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">triangle</td>
<td class="description last">To set the NeedleType triangle.</td>
</tr>
<tr>
<td class="name"><code>Rectangle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">rectangle</td>
<td class="description last">To set the NeedleType rectangle.</td>
</tr>
<tr>
<td class="name"><code>Trapezoid</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">trapezoid</td>
<td class="description last">To set the NeedleType trapezoid.</td>
</tr>
<tr>
<td class="name"><code>Arrow</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">arrow</td>
<td class="description last">To set the NeedleType arrow.</td>
</tr>
<tr>
<td class="name"><code>Image</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">image</td>
<td class="description last">To set the NeedleType image.</td>
</tr>
</tbody>
</table>















### NodeConstraints<span class="type-signature type nodeconstraints"><a href="global.html#NodeConstraints">NodeConstraints</a></span>
{:#members:nodeconstraints}








Enum for the NodeConstraints in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>None</code></td>
<td class="type"><span class="param-type"><a href="global.html#NodeConstraints">NodeConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Disable all node Constraints</td>
</tr>
<tr>
<td class="name"><code>Select</code></td>
<td class="type"><span class="param-type"><a href="global.html#NodeConstraints">NodeConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables node to be selected</td>
</tr>
<tr>
<td class="name"><code>Delete</code></td>
<td class="type"><span class="param-type"><a href="global.html#NodeConstraints">NodeConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables node to be Deleted</td>
</tr>
<tr>
<td class="name"><code>Drag</code></td>
<td class="type"><span class="param-type"><a href="global.html#NodeConstraints">NodeConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables node to be Dragged</td>
</tr>
<tr>
<td class="name"><code>Rotate</code></td>
<td class="type"><span class="param-type"><a href="global.html#NodeConstraints">NodeConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables node to be Rotated</td>
</tr>
<tr>
<td class="name"><code>Connect</code></td>
<td class="type"><span class="param-type"><a href="global.html#NodeConstraints">NodeConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables node to be connected</td>
</tr>
<tr>
<td class="name"><code>ResizeNorthEast</code></td>
<td class="type"><span class="param-type"><a href="global.html#NodeConstraints">NodeConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables node to be resize north east</td>
</tr>
<tr>
<td class="name"><code>ResizeEast</code></td>
<td class="type"><span class="param-type"><a href="global.html#NodeConstraints">NodeConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables node to be resize east</td>
</tr>
<tr>
<td class="name"><code>ResizeSouthEast</code></td>
<td class="type"><span class="param-type"><a href="global.html#NodeConstraints">NodeConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables node to be resize south east</td>
</tr>
<tr>
<td class="name"><code>ResizeSouth</code></td>
<td class="type"><span class="param-type"><a href="global.html#NodeConstraints">NodeConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables node to be resize south</td>
</tr>
<tr>
<td class="name"><code>ResizeSouthWest</code></td>
<td class="type"><span class="param-type"><a href="global.html#NodeConstraints">NodeConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables node to be resize south west</td>
</tr>
<tr>
<td class="name"><code>ResizeWest</code></td>
<td class="type"><span class="param-type"><a href="global.html#NodeConstraints">NodeConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables node to be resize west</td>
</tr>
<tr>
<td class="name"><code>ResizeNorthWest</code></td>
<td class="type"><span class="param-type"><a href="global.html#NodeConstraints">NodeConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables node to be resize north west</td>
</tr>
<tr>
<td class="name"><code>ResizeNorth</code></td>
<td class="type"><span class="param-type"><a href="global.html#NodeConstraints">NodeConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables node to be resize north</td>
</tr>
<tr>
<td class="name"><code>Resize</code></td>
<td class="type"><span class="param-type"><a href="global.html#NodeConstraints">NodeConstraints</a></span></td>
<td class="default">BITOR</td>
<td class="description last">Enables node to be Resized</td>
</tr>
<tr>
<td class="name"><code>Shadow</code></td>
<td class="type"><span class="param-type"><a href="global.html#NodeConstraints">NodeConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables shadow</td>
</tr>
<tr>
<td class="name"><code>DragLabel</code></td>
<td class="type"><span class="param-type"><a href="global.html#NodeConstraints">NodeConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables label of node to be Dragged</td>
</tr>
<tr>
<td class="name"><code>AllowPan</code></td>
<td class="type"><span class="param-type"><a href="global.html#NodeConstraints">NodeConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables panning should be done while node dragging</td>
</tr>
<tr>
<td class="name"><code>AspectRatio</code></td>
<td class="type"><span class="param-type"><a href="global.html#NodeConstraints">NodeConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables Proportional resize for node</td>
</tr>
<tr>
<td class="name"><code>Default</code></td>
<td class="type"><span class="param-type"><a href="global.html#NodeConstraints">NodeConstraints</a></span></td>
<td class="default">BITOR</td>
<td class="description last">Enables all node constraints</td>
</tr>
</tbody>
</table>















### Orientation<span class="type-signature type string">string</span>
{:#members:orientation}








Enum for Bullet Graph Orientation






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Horizontal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">horizontal</td>
<td class="description last">support for orientation in horizontal direction.</td>
</tr>
<tr>
<td class="name"><code>Vertical</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">vertical</td>
<td class="description last">support for orientation in vertical direction.</td>
</tr>
</tbody>
</table>















### Orientation<span class="type-signature type string">string</span>
{:#members:orientation}








Enum for chart orientation.






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Horizontal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">horizontal</td>
<td class="description last">Sets chart orientation to horizontal.</td>
</tr>
<tr>
<td class="name"><code>Vertical</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">vertical</td>
<td class="description last">Sets chart orientation to vertical.</td>
</tr>
</tbody>
</table>















### Orientation<span class="type-signature type string">string</span>
{:#members:orientation}








Enum for ProgressbarOrientation






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Horizontal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">horizontal</td>
<td class="description last">Enum for horizontal mode progress bar</td>
</tr>
<tr>
<td class="name"><code>Vertical</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">vertical</td>
<td class="description last">Enum for vertical mode progress bar</td>
</tr>
</tbody>
</table>















### Orientation<span class="type-signature type string">string</span>
{:#members:orientation}








Enum for RatingOrientation






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Horizontal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">horizontal</td>
<td class="description last">Enum for horizontal mode rating</td>
</tr>
<tr>
<td class="name"><code>Vertical</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">vertical</td>
<td class="description last">Enum for vertical mode rating</td>
</tr>
</tbody>
</table>















### Orientation<span class="type-signature type string">string</span>
{:#members:orientation}








Enum for Orientation






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Horizontal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">horizontal</td>
<td class="description last">Enum for Horizontal Orientation</td>
</tr>
<tr>
<td class="name"><code>Vertical</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">vertical</td>
<td class="description last">Enum for Vertical Orientation</td>
</tr>
</tbody>
</table>















### Orientation<span class="type-signature type string">string</span>
{:#members:orientation}








Enum for slider






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Horizontal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">horizontal</td>
<td class="description last">Enum for horizontal mode slider</td>
</tr>
<tr>
<td class="name"><code>Vertical</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">vertical</td>
<td class="description last">Enum for vertical mode slider</td>
</tr>
</tbody>
</table>















### OuterCustomLabelPosition<span class="type-signature type string">string</span>
{:#members:outercustomlabelposition}








Enum for gauge OuterCustomLabelPosition






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Left</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">left</td>
<td class="description last">To set the OuterCustomLabelPosition left.</td>
</tr>
<tr>
<td class="name"><code>Right</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">right</td>
<td class="description last">To set the OuterCustomLabelPosition right.</td>
</tr>
<tr>
<td class="name"><code>Top</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">top</td>
<td class="description last">To set the OuterCustomLabelPosition top.</td>
</tr>
<tr>
<td class="name"><code>Bottom</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">bottom</td>
<td class="description last">To set the OuterCustomLabelPosition bottom.</td>
</tr>
</tbody>
</table>















### OuterCustomLabelPosition<span class="type-signature type string">string</span>
{:#members:outercustomlabelposition}








Enum for gauge OuterCustomLabelPosition






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Left</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">left</td>
<td class="description last">To set the OuterCustomLabelPosition left.</td>
</tr>
<tr>
<td class="name"><code>Right</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">right</td>
<td class="description last">To set the OuterCustomLabelPosition right.</td>
</tr>
<tr>
<td class="name"><code>Top</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">top</td>
<td class="description last">To set the OuterCustomLabelPosition top.</td>
</tr>
<tr>
<td class="name"><code>Bottom</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">bottom</td>
<td class="description last">To set the OuterCustomLabelPosition bottom.</td>
</tr>
</tbody>
</table>















### pageOrientation<span class="type-signature type enum">enum</span>
{:#members:pageorientation}








To set the page orientation see<a href="global.html#PageOrientations">PageOrientations</a>




Default Value:
{:.param}






* "portrait"








Example
{:.example}

<pre class="prettyprint">
<code> 
//pageOrientation of the diagram
$("#diagramContent").ejDiagram({pageSettings: {pageOrientation: "portrait"}}); </code>
</pre>






### PageOrientations<span class="type-signature type string">String</span>
{:#members:pageorientations}








Enum for PageOrientations in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Landscape</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="default">landscape</td>
<td class="description last">Used to set orientation as Landscape</td>
</tr>
<tr>
<td class="name"><code>Portrait</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="default">portrait</td>
<td class="description last">Used to set orientation as portrait</td>
</tr>
</tbody>
</table>















### PagerDisplay<span class="type-signature type string">string</span>
{:#members:pagerdisplay}








Enum for Grid Pager Display






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Enum for Normal pager display</td>
</tr>
<tr>
<td class="name"><code>Fixed</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">fixed</td>
<td class="description last">Enum for Fixed pager display</td>
</tr>
</tbody>
</table>















### PagerPositionHorizontal<span class="type-signature type string">string</span>
{:#members:pagerpositionhorizontal}








Enum for PagerPositionHorizontal






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Bottom</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">bottom</td>
<td class="description last">Enum for Bottom PagerPositionHorizontal</td>
</tr>
<tr>
<td class="name"><code>Top</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">top</td>
<td class="description last">Enum for Top PagerPositionHorizontal</td>
</tr>
</tbody>
</table>















### PagerPositionVertical<span class="type-signature type string">string</span>
{:#members:pagerpositionvertical}








Enum for PagerPositionVertical






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Right</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">right</td>
<td class="description last">Enum for Right PagerPositionVertical</td>
</tr>
<tr>
<td class="name"><code>Left</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">left</td>
<td class="description last">Enum for Left PagerPositionVertical</td>
</tr>
</tbody>
</table>















### PagerType<span class="type-signature type string">string</span>
{:#members:pagertype}








Enum for Grid Pager Type






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">used to enable normal pager which contain page navigation buttons</td>
</tr>
<tr>
<td class="name"><code>Scrollable</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">scrollable</td>
<td class="description last">used to enable scrollable pager</td>
</tr>
</tbody>
</table>















### PointerPlacement<span class="type-signature type string">string</span>
{:#members:pointerplacement}








Enum for gauge PointerPlacement






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Near</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">near</td>
<td class="description last">To set the PointerPlacement near.</td>
</tr>
<tr>
<td class="name"><code>Far</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">far</td>
<td class="description last">To set the PointerPlacement far.</td>
</tr>
<tr>
<td class="name"><code>Center</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">center</td>
<td class="description last">To set the PointerPlacement center.</td>
</tr>
</tbody>
</table>















### PointerPlacement<span class="type-signature type string">string</span>
{:#members:pointerplacement}








Enum for gauge PointerPlacement






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Near</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">near</td>
<td class="description last">To set the PointerPlacement near.</td>
</tr>
<tr>
<td class="name"><code>Far</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">far</td>
<td class="description last">To set the PointerPlacement far.</td>
</tr>
<tr>
<td class="name"><code>Center</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">center</td>
<td class="description last">To set the PointerPlacement center.</td>
</tr>
</tbody>
</table>















### PointerType<span class="type-signature type string">string</span>
{:#members:pointertype}








Enum for gauge PointerType






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Needle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">needle</td>
<td class="description last">To set the PointerType needle.</td>
</tr>
<tr>
<td class="name"><code>Marker</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">marker</td>
<td class="description last">To set the PointerType marker.</td>
</tr>
</tbody>
</table>















### PortConstraints<span class="type-signature type portconstraints"><a href="global.html#PortConstraints">PortConstraints</a></span>
{:#members:portconstraints}








Enum for PortConstraints in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>None</code></td>
<td class="type"><span class="param-type"><a href="global.html#PortConstraints">PortConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Disable all constraints</td>
</tr>
<tr>
<td class="name"><code>Connect</code></td>
<td class="type"><span class="param-type"><a href="global.html#PortConstraints">PortConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables connections with connector</td>
</tr>
</tbody>
</table>















### PortShapes<span class="type-signature type string">string</span>
{:#members:portshapes}








Enum for various port shapes in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>X</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">x</td>
<td class="description last">Used to set port shape as X</td>
</tr>
<tr>
<td class="name"><code>Circle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">circle</td>
<td class="description last">Used to set port shape as Circle</td>
</tr>
<tr>
<td class="name"><code>Square</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">square</td>
<td class="description last">Used to set port shape as Square</td>
</tr>
<tr>
<td class="name"><code>Path</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">path</td>
<td class="description last">Used to set port shape as Path</td>
</tr>
</tbody>
</table>















### PortVisibility<span class="type-signature type portvisibility"><a href="global.html#PortVisibility">PortVisibility</a></span>
{:#members:portvisibility}








Enum for port visibility in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Visible</code></td>
<td class="type"><span class="param-type"><a href="global.html#PortVisibility">PortVisibility</a></span></td>
<td class="default">LSH</td>
<td class="description last">Set the port visibility as Visible</td>
</tr>
<tr>
<td class="name"><code>Hidden</code></td>
<td class="type"><span class="param-type"><a href="global.html#PortVisibility">PortVisibility</a></span></td>
<td class="default">LSH</td>
<td class="description last">Set the port visibility as Hidden</td>
</tr>
<tr>
<td class="name"><code>Hover</code></td>
<td class="type"><span class="param-type"><a href="global.html#PortVisibility">PortVisibility</a></span></td>
<td class="default">LSH</td>
<td class="description last">Port get visible when hover connector on node</td>
</tr>
<tr>
<td class="name"><code>Connect</code></td>
<td class="type"><span class="param-type"><a href="global.html#PortVisibility">PortVisibility</a></span></td>
<td class="default">LSH</td>
<td class="description last">Port gets visibile when connect connector to node</td>
</tr>
<tr>
<td class="name"><code>Default</code></td>
<td class="type"><span class="param-type"><a href="global.html#PortVisibility">PortVisibility</a></span></td>
<td class="default">LSH</td>
<td class="description last">Specifies the port visibility as default</td>
</tr>
</tbody>
</table>















### Position<span class="type-signature type string">string</span>
{:#members:position}








Enum for Map Navigation Control and Legend dock position






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>None</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">none</td>
<td class="description last">support for dock position none.</td>
</tr>
<tr>
<td class="name"><code>TopLeft</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">topleft</td>
<td class="description last">support for dock position topleft.</td>
</tr>
<tr>
<td class="name"><code>TopCenter</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">topcenter</td>
<td class="description last">support for dock position topcenter.</td>
</tr>
<tr>
<td class="name"><code>TopRight</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">topright</td>
<td class="description last">support for dock position topright.</td>
</tr>
<tr>
<td class="name"><code>CenterLeft</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">centerleft</td>
<td class="description last">support for dock position centerleft.</td>
</tr>
<tr>
<td class="name"><code>Center</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">center</td>
<td class="description last">support for dock position center.</td>
</tr>
<tr>
<td class="name"><code>CenterRight</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">centerright</td>
<td class="description last">support for dock position centerright.</td>
</tr>
<tr>
<td class="name"><code>BottomLeft</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">bottomleft</td>
<td class="description last">support for dock position bottomleft.</td>
</tr>
<tr>
<td class="name"><code>BottomCenter</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">bottomcenter</td>
<td class="description last">support for dock position bottomcenter.</td>
</tr>
<tr>
<td class="name"><code>BottomRight</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">bottomright</td>
<td class="description last">support for dock position bottomright.</td>
</tr>
</tbody>
</table>















### Position<span class="type-signature type string">string</span>
{:#members:position}








Enum for position.






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Top</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">top</td>
<td class="description last">Sets the position to top.</td>
</tr>
<tr>
<td class="name"><code>Middle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">middle</td>
<td class="description last">Sets the position to middle.</td>
</tr>
<tr>
<td class="name"><code>Bottom</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">bottom</td>
<td class="description last">Sets the position to bottom.</td>
</tr>
</tbody>
</table>















### Position<span class="type-signature type string">string</span>
{:#members:position}








Enum for Position






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Enum for relative position for Footer</td>
</tr>
<tr>
<td class="name"><code>Fixed</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">fixed</td>
<td class="description last">Enum for fixed position for Footer</td>
</tr>
</tbody>
</table>















### Position<span class="type-signature type string">string</span>
{:#members:position}








Enum for Position






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Enum for relative position for Header</td>
</tr>
<tr>
<td class="name"><code>Fixed</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">fixed</td>
<td class="description last">Enum for fixed position for Header</td>
</tr>
</tbody>
</table>















### Position<span class="type-signature type string">string</span>
{:#members:position}








Enum for Position






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>RightCenter</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">rightcenter</td>
<td class="description last">Enum for RightCenter Position</td>
</tr>
<tr>
<td class="name"><code>RightTop</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">righttop</td>
<td class="description last">Enum for RightTop Position</td>
</tr>
<tr>
<td class="name"><code>RightBottom</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">rightbottom</td>
<td class="description last">Enum for RightBottom Position</td>
</tr>
<tr>
<td class="name"><code>LeftCenter</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">leftcenter</td>
<td class="description last">Enum for LeftCenter Position</td>
</tr>
<tr>
<td class="name"><code>LeftTop</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">lefttop</td>
<td class="description last">Enum for LeftTop Position</td>
</tr>
<tr>
<td class="name"><code>LeftBottom</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">leftbottom</td>
<td class="description last">Enum for LeftBottom Position</td>
</tr>
</tbody>
</table>















### Position<span class="type-signature type string">string</span>
{:#members:position}








Enum for Position






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Fixed</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">fixed</td>
<td class="description last">Enum for Fixed position Tab</td>
</tr>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Enum for Normal position Tab</td>
</tr>
</tbody>
</table>















### Position<span class="type-signature type string">string</span>
{:#members:position}








Enum for toolbar position






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Enum for relative position for toolbar</td>
</tr>
<tr>
<td class="name"><code>Fixed</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">fixed</td>
<td class="description last">Enum for fixed position for toolbar</td>
</tr>
</tbody>
</table>















### Precision<span class="type-signature type string">string</span>
{:#members:precision}








Enum for RatingPrecision






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Full</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">full</td>
<td class="description last">Enum for full precision rating</td>
</tr>
<tr>
<td class="name"><code>Exact</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">exact</td>
<td class="description last">Enum for exact precision rating</td>
</tr>
<tr>
<td class="name"><code>Half</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">half</td>
<td class="description last">Enum for half precision rating</td>
</tr>
</tbody>
</table>















### PyramidMode<span class="type-signature type string">string</span>
{:#members:pyramidmode}








Enum for chart pyramid mode.






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Linear</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">linear</td>
<td class="description last">Specifies the mode of the pyramid as linear.</td>
</tr>
<tr>
<td class="name"><code>Surface</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">Surface</td>
<td class="description last">Specifies the mode of the pyramid as surface.</td>
</tr>
</tbody>
</table>















### RangePadding<span class="type-signature type string">string</span>
{:#members:rangepadding}








Enum for range padding.






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Additional</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">additional</td>
<td class="description last">Sets chart range padding as additional.</td>
</tr>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Sets chart range padding as normal.</td>
</tr>
<tr>
<td class="name"><code>None</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">none</td>
<td class="description last">Sets chart range padding as none.</td>
</tr>
<tr>
<td class="name"><code>Round</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">round</td>
<td class="description last">Sets chart range padding as round.</td>
</tr>
<tr>
<td class="name"><code>Auto</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">auto</td>
<td class="description last">Sets chart range padding as auto.</td>
</tr>
</tbody>
</table>















### RangePlacement<span class="type-signature type string">string</span>
{:#members:rangeplacement}








Enum for gauge RangePlacement






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Near</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">near</td>
<td class="description last">To set the RangePlacement near.</td>
</tr>
<tr>
<td class="name"><code>Far</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">far</td>
<td class="description last">To set the RangePlacement far.</td>
</tr>
<tr>
<td class="name"><code>Center</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">center</td>
<td class="description last">To set the RangePlacement center.</td>
</tr>
</tbody>
</table>















### RangePlacement<span class="type-signature type string">string</span>
{:#members:rangeplacement}








Enum for gauge RangePlacement






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Near</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">near</td>
<td class="description last">To set the RangePlacement near.</td>
</tr>
<tr>
<td class="name"><code>Far</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">far</td>
<td class="description last">To set the RangePlacement far.</td>
</tr>
<tr>
<td class="name"><code>Center</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">center</td>
<td class="description last">To set the RangePlacement center.</td>
</tr>
</tbody>
</table>















### Region<span class="type-signature type region"><a href="global.html#Region">Region</a></span>
{:#members:region}








Enum for the Region in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Content</code></td>
<td class="type"><span class="param-type"><a href="global.html#Region">Region</a></span></td>
<td class="default">content</td>
<td class="description last">specifies region that is occupied by diagram elements</td>
</tr>
<tr>
<td class="name"><code>PageSettings</code></td>
<td class="type"><span class="param-type"><a href="global.html#Region">Region</a></span></td>
<td class="default">pageSettings</td>
<td class="description last">specifies the region based on the page settings</td>
</tr>
</tbody>
</table>















### RenderMode<span class="type-signature type string">string</span>
{:#members:rendermode}








Enum for RenderMode






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Auto</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">auto</td>
<td class="description last">Auto RenderMode</td>
</tr>
<tr>
<td class="name"><code>IOS7</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">ios7</td>
<td class="description last">IOS7 RenderMode</td>
</tr>
<tr>
<td class="name"><code>Android</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">android</td>
<td class="description last">Android RenderMode</td>
</tr>
<tr>
<td class="name"><code>Windows</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">windows</td>
<td class="description last">Windows RenderMode</td>
</tr>
</tbody>
</table>















### ScaleType<span class="type-signature type string">string</span>
{:#members:scaletype}








Enum for gauge ScaleType






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Rectangle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">rectangle</td>
<td class="description last">To set the ScaleType rectangle.</td>
</tr>
<tr>
<td class="name"><code>RoundedRectangle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">roundedrectangle</td>
<td class="description last">To set the ScaleType roundedrectangle.</td>
</tr>
<tr>
<td class="name"><code>Thermometer</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">thermometer</td>
<td class="description last">To set the ScaleType thermometer.</td>
</tr>
</tbody>
</table>















### scrollableArea<span class="type-signature type object">object</span>
{:#members:scrollablearea}








To set the scrollable region of diagram




Default Value:
{:.param}






* {scrollableArea: { x: Infinity, y: Infinity, width: Infinity, height: Infinity }}








Example
{:.example}

<pre class="prettyprint">
<code> 
//scrollableArea of the diagram
$("#diagramContent").ejDiagram({pageSettings: {scrollableArea: { x: 0, y: 0, width: 0, height: 0 }}}); </code>
</pre>






### scrollLimit<span class="type-signature type enum">enum</span>
{:#members:scrolllimit}








To define the scrollable limit of diagram see<a href="global.html#ScrollLimit">ScrollLimit</a>




Default Value:
{:.param}






* "infinity"








Example
{:.example}

<pre class="prettyprint">
<code> 
//scrollLimit of the diagram
$("#diagramContent").ejDiagram({pageSettings: {scrollLimit: "infinity"}}); </code>
</pre>






### ScrollLimit<span class="type-signature type string">String</span>
{:#members:scrolllimit}








Enum for ScrollLimit in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Infinity</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="default">infinity</td>
<td class="description last">Used to set scrollLimit as Infinity</td>
</tr>
<tr>
<td class="name"><code>Diagram</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="default">diagram</td>
<td class="description last">Used to set scrollLimit as Diagram</td>
</tr>
<tr>
<td class="name"><code>Limited</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="default">limited</td>
<td class="description last">Used to set scrollLimit as Limited</td>
</tr>
</tbody>
</table>















### Segments<span class="type-signature type string">string</span>
{:#members:segments}








Enum for various connector segments in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Straight</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">straight</td>
<td class="description last">Used to specify the lines as Straight</td>
</tr>
<tr>
<td class="name"><code>Orthogonal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">orthogonal</td>
<td class="description last">Used to specify the lines as Orthogonal</td>
</tr>
<tr>
<td class="name"><code>Bezier</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">bezier</td>
<td class="description last">Used to specify the lines as Bezier</td>
</tr>
</tbody>
</table>















### SelectionMode<span class="type-signature type string">string</span>
{:#members:selectionmode}








Enum for Map selection mode






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Default</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">default</td>
<td class="description last">support for selection mode default.</td>
</tr>
<tr>
<td class="name"><code>Multiple</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">multiple</td>
<td class="description last">support for selection mode multiple.</td>
</tr>
</tbody>
</table>















### SelectorConstraints<span class="type-signature type selectorconstraints"><a href="global.html#SelectorConstraints">SelectorConstraints</a></span>
{:#members:selectorconstraints}








Enum to specify the SelectorConstraints in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>None</code></td>
<td class="type"><span class="param-type"><a href="global.html#SelectorConstraints">SelectorConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Hides the selector</td>
</tr>
<tr>
<td class="name"><code>Rotator</code></td>
<td class="type"><span class="param-type"><a href="global.html#SelectorConstraints">SelectorConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Sets the visibility of rotation handle as visible</td>
</tr>
<tr>
<td class="name"><code>Resizer</code></td>
<td class="type"><span class="param-type"><a href="global.html#SelectorConstraints">SelectorConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Sets the visibility of resize handles as visible</td>
</tr>
<tr>
<td class="name"><code>UserHandles</code></td>
<td class="type"><span class="param-type"><a href="global.html#SelectorConstraints">SelectorConstraints</a></span></td>
<td class="default">LSH</td>
<td class="description last">Sets the visibility of user handles as visible</td>
</tr>
<tr>
<td class="name"><code>All</code></td>
<td class="type"><span class="param-type"><a href="global.html#SelectorConstraints">SelectorConstraints</a></span></td>
<td class="default">BITOR</td>
<td class="description last">Sets the visibility of all selection handles as visible</td>
</tr>
</tbody>
</table>















### Shape<span class="type-signature type string">string</span>
{:#members:shape}








Enum for the shape of indicator symbol






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Circle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">circle</td>
<td class="description last">support for drawing circle as indicator symbol.</td>
</tr>
<tr>
<td class="name"><code>Cross</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">cross</td>
<td class="description last">support for drawing cross as indicator symbol.</td>
</tr>
<tr>
<td class="name"><code>Diamond</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">diamond</td>
<td class="description last">support for drawing diamond as indicator symbol.</td>
</tr>
<tr>
<td class="name"><code>DownArrow</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">downarrow</td>
<td class="description last">support for drawing down arrow as indicator symbol.</td>
</tr>
<tr>
<td class="name"><code>Ellipse</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">ellipse</td>
<td class="description last">support for drawing ellipse as indicator symbol.</td>
</tr>
<tr>
<td class="name"><code>HorizontalLine</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">horizontalLine</td>
<td class="description last">support for drawing horizontal line as indicator symbol.</td>
</tr>
<tr>
<td class="name"><code>Image</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">image</td>
<td class="description last">support for drawing image as indicator symbol.</td>
</tr>
<tr>
<td class="name"><code>InvertedTriangle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">invertedtriangle</td>
<td class="description last">support for drawing inverted triangle as indicator symbol.</td>
</tr>
<tr>
<td class="name"><code>LeftArrow</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">leftarrow</td>
<td class="description last">support for drawing left arrow as indicator symbol.</td>
</tr>
<tr>
<td class="name"><code>Pentagon</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">pentagon</td>
<td class="description last">support for drawing pentagon as indicator symbol.</td>
</tr>
<tr>
<td class="name"><code>Rectangle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">Rectangle</td>
<td class="description last">support for drawing rectangle as indicator symbol.</td>
</tr>
<tr>
<td class="name"><code>RightArrow</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">rightarrow</td>
<td class="description last">support for drawing right arrow as indicator symbol.</td>
</tr>
<tr>
<td class="name"><code>Star</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">star</td>
<td class="description last">support for drawing star as indicator symbol.</td>
</tr>
<tr>
<td class="name"><code>Trapezoid</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">trapezoid</td>
<td class="description last">support for drawing trapezoid as indicator symbol.</td>
</tr>
<tr>
<td class="name"><code>Triangle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">triangle</td>
<td class="description last">support for drawing triangle as indicator symbol.</td>
</tr>
<tr>
<td class="name"><code>UpArrow</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">uparrow</td>
<td class="description last">support for drawing up arrow as indicator symbol.</td>
</tr>
<tr>
<td class="name"><code>VerticalLine</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">verticalline</td>
<td class="description last">support for drawing vertical line as indicator symbol.</td>
</tr>
<tr>
<td class="name"><code>Wedge</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">wedge</td>
<td class="description last">support for drawing wedge as indicator symbol.</td>
</tr>
</tbody>
</table>















### Shape<span class="type-signature type string">string</span>
{:#members:shape}








Enum for chart shape.






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>None</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">none</td>
<td class="description last">Sets the shape to none.</td>
</tr>
<tr>
<td class="name"><code>LeftArrow</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">leftarrow</td>
<td class="description last">Sets the shape to leftarrow.</td>
</tr>
<tr>
<td class="name"><code>RightArrow</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">rightarrow</td>
<td class="description last">Sets the shape to rightarrow.</td>
</tr>
<tr>
<td class="name"><code>Circle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">circle</td>
<td class="description last">Sets the shape to circle.</td>
</tr>
<tr>
<td class="name"><code>Cross</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">cross</td>
<td class="description last">Sets the shape to cross.</td>
</tr>
<tr>
<td class="name"><code>HorizLine</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">horizline</td>
<td class="description last">Sets the shape to horizline.</td>
</tr>
<tr>
<td class="name"><code>VertLine</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">vertLine</td>
<td class="description last">Sets the shape to vertline.</td>
</tr>
<tr>
<td class="name"><code>Diamond</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">diamond</td>
<td class="description last">Sets the shape to diamond.</td>
</tr>
<tr>
<td class="name"><code>Rectangle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">rectangle</td>
<td class="description last">Sets the shape to rectangle.</td>
</tr>
<tr>
<td class="name"><code>Triangle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">triangle</td>
<td class="description last">Sets the shape to triangle.</td>
</tr>
<tr>
<td class="name"><code>InvertedTriangle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">invertedtriangle</td>
<td class="description last">Sets the shape to invertedtriangle.</td>
</tr>
<tr>
<td class="name"><code>Hexagon</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">hexagon</td>
<td class="description last">Sets the shape to hexagon.</td>
</tr>
<tr>
<td class="name"><code>Pentagon</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">pentagon</td>
<td class="description last">Sets the shape to pentagon.</td>
</tr>
<tr>
<td class="name"><code>Star</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">star</td>
<td class="description last">Sets the shape to star.</td>
</tr>
<tr>
<td class="name"><code>Ellipse</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">ellipse</td>
<td class="description last">Sets the shape to ellipse.</td>
</tr>
<tr>
<td class="name"><code>Wedge</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">wedge</td>
<td class="description last">Sets the shape to wedge.</td>
</tr>
<tr>
<td class="name"><code>Trapezoid</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">trapezoid</td>
<td class="description last">Sets the shape to trapezoid.</td>
</tr>
<tr>
<td class="name"><code>UpArrow</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">uparrow</td>
<td class="description last">Sets the shape to uparrow.</td>
</tr>
<tr>
<td class="name"><code>DownArrow</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">downarrow</td>
<td class="description last">Sets the shape to downarrow.</td>
</tr>
<tr>
<td class="name"><code>Image</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">image</td>
<td class="description last">Sets the shape to image.</td>
</tr>
</tbody>
</table>















### Shape<span class="type-signature type string">string</span>
{:#members:shape}








Enum for RatingShape






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Star</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">star</td>
<td class="description last">Enum for star shape rating</td>
</tr>
<tr>
<td class="name"><code>Circle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">circle</td>
<td class="description last">Enum for circle shape rating</td>
</tr>
<tr>
<td class="name"><code>Diamond</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">diamond</td>
<td class="description last">Enum for diamond shape rating</td>
</tr>
<tr>
<td class="name"><code>Heart</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">heart</td>
<td class="description last">Enum for heart shape rating</td>
</tr>
<tr>
<td class="name"><code>Pentagon</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">pentagon</td>
<td class="description last">Enum for pentagon shape rating</td>
</tr>
<tr>
<td class="name"><code>Square</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">square</td>
<td class="description last">Enum for square shape rating</td>
</tr>
<tr>
<td class="name"><code>Triangle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">triangle</td>
<td class="description last">Enum for triangle shape rating</td>
</tr>
</tbody>
</table>















### Shapes<span class="type-signature type string">string</span>
{:#members:shapes}








Enum for various Shapes of node in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Image</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">image</td>
<td class="description last">Used to specify node Shape as Image</td>
</tr>
<tr>
<td class="name"><code>Text</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">text</td>
<td class="description last">Used to specify node Shape as Text</td>
</tr>
<tr>
<td class="name"><code>Html</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">html</td>
<td class="description last">Used to specify node Shape as Html</td>
</tr>
<tr>
<td class="name"><code>Native</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">native</td>
<td class="description last">Used to specify node Shape as Native</td>
</tr>
<tr>
<td class="name"><code>Basic</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">basic</td>
<td class="description last">Used to specify node Shape as Basic</td>
</tr>
<tr>
<td class="name"><code>Flow</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">flow</td>
<td class="description last">Used to specify node Shape as Flow</td>
</tr>
<tr>
<td class="name"><code>Arrow</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">arrow</td>
<td class="description last">Used to specify node Shape as Arrow</td>
</tr>
<tr>
<td class="name"><code>BPMN</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">bpmn</td>
<td class="description last">Used to specify node Shape as BPMN</td>
</tr>
</tbody>
</table>















### ShowOn<span class="type-signature type string">string</span>
{:#members:showon}








Enum for Menu ShowOn






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Tap</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">tap</td>
<td class="description last">Enum for show menu on tap</td>
</tr>
<tr>
<td class="name"><code>TapHold</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">taphold</td>
<td class="description last">Enum for show menu on tap hold</td>
</tr>
</tbody>
</table>















### SnapConstraints<span class="type-signature type enum">enum</span>
{:#members:snapconstraints}








Defines the snapconstraints of diagram seesnapConstraints




Default Value:
{:.param}






* SnapConstraints.ShowLines








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="diagramcontent"&gt;&lt;/div&gt;
&lt;script&gt;
var gridline = { "snapConstraints": ej.datavisualization.Diagram.SnapConstraints.ShowLines};
//snap constraints of gridlines
$("#diagramContent").ejDiagram({snapSettings: gridline} });
&lt;/script&gt;</code>
</pre>






### SnapConstraints<span class="type-signature type snapconstraints"><a href="global.html#SnapConstraints">SnapConstraints</a></span>
{:#members:snapconstraints}








Enum for SnapConstraints in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>None</code></td>
<td class="type"><span class="param-type"><a href="global.html#SnapConstraints">SnapConstraints</a></span></td>
<td class="default">0</td>
<td class="description last">Enables node to be snapped to horizontal gridlines</td>
</tr>
<tr>
<td class="name"><code>SnapToHorizontalLines</code></td>
<td class="type"><span class="param-type"><a href="global.html#SnapConstraints">SnapConstraints</a></span></td>
<td class="default">1</td>
<td class="description last">Enables node to be snapped to vertical gridlines</td>
</tr>
<tr>
<td class="name"><code>SnapToVerticalLines</code></td>
<td class="type"><span class="param-type"><a href="global.html#SnapConstraints">SnapConstraints</a></span></td>
<td class="default">2</td>
<td class="description last">Enables node to be snapped to horizontal gridlines</td>
</tr>
<tr>
<td class="name"><code>SnapToLines</code></td>
<td class="type"><span class="param-type"><a href="global.html#SnapConstraints">SnapConstraints</a></span></td>
<td class="default">BITOR</td>
<td class="description last">Enables node to be snapped to gridlines</td>
</tr>
<tr>
<td class="name"><code>ShowHorizontalLines</code></td>
<td class="type"><span class="param-type"><a href="global.html#SnapConstraints">SnapConstraints</a></span></td>
<td class="default">4</td>
<td class="description last">Enable horizontal lines</td>
</tr>
<tr>
<td class="name"><code>ShowVerticalLines</code></td>
<td class="type"><span class="param-type"><a href="global.html#SnapConstraints">SnapConstraints</a></span></td>
<td class="default">8</td>
<td class="description last">Enable vertical lines</td>
</tr>
<tr>
<td class="name"><code>ShowLines</code></td>
<td class="type"><span class="param-type"><a href="global.html#SnapConstraints">SnapConstraints</a></span></td>
<td class="default">BITOR</td>
<td class="description last">Enable both horizontal and vertical lines</td>
</tr>
<tr>
<td class="name"><code>All</code></td>
<td class="type"><span class="param-type"><a href="global.html#SnapConstraints">SnapConstraints</a></span></td>
<td class="default">BITOR</td>
<td class="description last">Enable all the constraints</td>
</tr>
</tbody>
</table>















### SortOrder<span class="type-signature type string">string</span>
{:#members:sortorder}








Enum for sortorder






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Ascending</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">ascending</td>
<td class="description last">Enum for Ascending sort order</td>
</tr>
<tr>
<td class="name"><code>Descending</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">descending</td>
<td class="description last">Enum for Descending sort order</td>
</tr>
</tbody>
</table>















### Style<span class="type-signature type string">string</span>
{:#members:style}








Enum for IOS7style






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Enum for normal ios7 button style</td>
</tr>
<tr>
<td class="name"><code>Back</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">back</td>
<td class="description last">Enum for back ios7 button style</td>
</tr>
<tr>
<td class="name"><code>Header</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">header</td>
<td class="description last">Enum for header ios7 button style</td>
</tr>
<tr>
<td class="name"><code>Dialog</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">dialog</td>
<td class="description last">Enum for dialog ios7 button style</td>
</tr>
</tbody>
</table>















### Style<span class="type-signature type string">string</span>
{:#members:style}








Enum for AndroidStyle






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Enum for normal anroid button style</td>
</tr>
<tr>
<td class="name"><code>Small</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">small</td>
<td class="description last">Enum for small android button style</td>
</tr>
<tr>
<td class="name"><code>Dialog</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">dialog</td>
<td class="description last">Enum for dialog android button style</td>
</tr>
</tbody>
</table>















### Style<span class="type-signature type string">string</span>
{:#members:style}








Enum for windowsstyle






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Enum for normal windows button style</td>
</tr>
<tr>
<td class="name"><code>Back</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">back</td>
<td class="description last">Enum for back windows button style</td>
</tr>
</tbody>
</table>















### Style<span class="type-signature type string">string</span>
{:#members:style}








Enum for FlatStyle






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Enum for normal flat button style</td>
</tr>
<tr>
<td class="name"><code>Back</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">back</td>
<td class="description last">Enum for back flat button style</td>
</tr>
<tr>
<td class="name"><code>Header</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">header</td>
<td class="description last">Enum for header flat button style</td>
</tr>
</tbody>
</table>















### SymbologyType<span class="type-signature type string">string</span>
{:#members:symbologytype}








Enum for Symbol type.






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>code39</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">code39</td>
<td class="description last">Specifies Code 39 Barcode.</td>
</tr>
<tr>
<td class="name"><code>code39Extended</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">code39extended</td>
<td class="description last">Specifies Code 39 Extended Barcode.</td>
</tr>
<tr>
<td class="name"><code>code11</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">code11</td>
<td class="description last">Specifies Code 11 Barcode.</td>
</tr>
<tr>
<td class="name"><code>codabar</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">codabar</td>
<td class="description last">Specifies Codabar Barcode.</td>
</tr>
<tr>
<td class="name"><code>code32</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">code32</td>
<td class="description last">Specifies Code 32 Barcode.</td>
</tr>
<tr>
<td class="name"><code>code93</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">code93</td>
<td class="description last">Specifies Code 93 Barcode.</td>
</tr>
<tr>
<td class="name"><code>code93Extended</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">code93extended</td>
<td class="description last">Specifies Code 93 Extended Barcode.</td>
</tr>
<tr>
<td class="name"><code>code128A</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">code128a</td>
<td class="description last">Specifies Code 128 A Barcode.</td>
</tr>
<tr>
<td class="name"><code>code128B</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">code128b</td>
<td class="description last">Specifies Code 128 B Barcode.</td>
</tr>
<tr>
<td class="name"><code>code128C</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">code128c</td>
<td class="description last">Specifies Code 128 C Barcode.</td>
</tr>
<tr>
<td class="name"><code>dataMatrix</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">datamatrix</td>
<td class="description last">Specifies DataMatrix Barcode.</td>
</tr>
<tr>
<td class="name"><code>qrBarcode</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">qrbarcode</td>
<td class="description last">Specifies QR Barcode.</td>
</tr>
</tbody>
</table>















### TextAlign<span class="type-signature type string">string</span>
{:#members:textalign}








Enum for the Text Alignment in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Left</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">left</td>
<td class="description last">Used to align text on left side of node/connector</td>
</tr>
<tr>
<td class="name"><code>Center</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">center</td>
<td class="description last">Used to align text on center of node/connector</td>
</tr>
<tr>
<td class="name"><code>Right</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">right</td>
<td class="description last">Used to align text on Right side of node/connector</td>
</tr>
</tbody>
</table>















### TextAlign<span class="type-signature type string">string</span>
{:#members:textalign}








Enum for gauge TextAlign






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Left</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">left</td>
<td class="description last">To set the TextAlign Left.</td>
</tr>
<tr>
<td class="name"><code>Right</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">right</td>
<td class="description last">To set the TextAlign right.</td>
</tr>
</tbody>
</table>















### TextAlignment<span class="type-signature type string">string</span>
{:#members:textalignment}








Enum for text alignment.






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>MiddleTop</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">middletop</td>
<td class="description last">Support for changing text alignment to middleTop.</td>
</tr>
<tr>
<td class="name"><code>MiddleCenter</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">middlecenter</td>
<td class="description last">Support for changing text alignment to middleCenter.</td>
</tr>
<tr>
<td class="name"><code>MiddleBottom</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">middlebottom</td>
<td class="description last">Support for changing text alignment to middleBottom.</td>
</tr>
</tbody>
</table>















### TextAlignment<span class="type-signature type string">string</span>
{:#members:textalignment}








Enum for Tile TextAlignment






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Enum for normal alignment of tile text</td>
</tr>
<tr>
<td class="name"><code>Left</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">left</td>
<td class="description last">Enum for left alignment of tile text</td>
</tr>
<tr>
<td class="name"><code>Right</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">right</td>
<td class="description last">Enum for right alignment of tile text</td>
</tr>
<tr>
<td class="name"><code>Center</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">center</td>
<td class="description last">Enum for center alignment of tile text</td>
</tr>
</tbody>
</table>















### TextDecorations<span class="type-signature type string">string</span>
{:#members:textdecorations}








Enum for TextDecorations in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Underline</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">underline</td>
<td class="description last">Used to set text decoration of the label as Underline</td>
</tr>
<tr>
<td class="name"><code>Overline</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">overline</td>
<td class="description last">Used to set text decoration of the label as Overline</td>
</tr>
<tr>
<td class="name"><code>LineThrough</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">line-through</td>
<td class="description last">Used to set text decoration of the label as LineThrough</td>
</tr>
<tr>
<td class="name"><code>None</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">none</td>
<td class="description last">Used to set text decoration of the label as None</td>
</tr>
</tbody>
</table>















### TextPosition<span class="type-signature type string">string</span>
{:#members:textposition}








Enum for Tile TextPosition






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Inner</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">inner</td>
<td class="description last">Enum for inner position of tile text</td>
</tr>
<tr>
<td class="name"><code>Outer</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">outer</td>
<td class="description last">Enum for outer position of tile text</td>
</tr>
</tbody>
</table>















### TextWrapping<span class="type-signature type string">string</span>
{:#members:textwrapping}








Enum for TextWrapping in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>NoWrap</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">nowrap</td>
<td class="description last">Disables wrapping</td>
</tr>
<tr>
<td class="name"><code>Wrap</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">wrap</td>
<td class="description last">Enables Line-break at normal word break points</td>
</tr>
<tr>
<td class="name"><code>WrapWithOverflow</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">wrapwithoverflow</td>
<td class="description last">Enables Line-break at normal word break points with longer word overflows</td>
</tr>
</tbody>
</table>















### Theme<span class="type-signature type string">string</span>
{:#members:theme}








Enum for chart themes.






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Azure</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">azure</td>
<td class="description last">Render chart in azure theme.</td>
</tr>
<tr>
<td class="name"><code>FlatLight</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">flatlight</td>
<td class="description last">Render chart in flatlight theme.</td>
</tr>
<tr>
<td class="name"><code>Azuredark</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">azuredark</td>
<td class="description last">Render chart in azuredark theme.</td>
</tr>
<tr>
<td class="name"><code>Lime</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">lime</td>
<td class="description last">Render chart in lime theme.</td>
</tr>
<tr>
<td class="name"><code>LimeDark</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">limedark</td>
<td class="description last">Render chart in limedark theme.</td>
</tr>
<tr>
<td class="name"><code>Saffron</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">saffron</td>
<td class="description last">Render chart in saffron theme.</td>
</tr>
<tr>
<td class="name"><code>SaffronDark</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">saffrondark</td>
<td class="description last">Render chart in saffrondark theme.</td>
</tr>
<tr>
<td class="name"><code>GradientLight</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">gradientlight</td>
<td class="description last">Render chart in gradientlight theme.</td>
</tr>
<tr>
<td class="name"><code>GradientDark</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">gradientdark</td>
<td class="description last">Render chart in gradientdark theme.</td>
</tr>
</tbody>
</table>















### Theme<span class="type-signature type string">string</span>
{:#members:theme}








Enum for Theme






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Auto</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">auto</td>
<td class="description last">Auto RenderMode</td>
</tr>
<tr>
<td class="name"><code>Dark</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">dark</td>
<td class="description last">Dark RenderMode</td>
</tr>
<tr>
<td class="name"><code>Light</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">light</td>
<td class="description last">Light RenderMode</td>
</tr>
</tbody>
</table>















### Themes<span class="type-signature type string">string</span>
{:#members:themes}








Enum for Bullet Graph Theme3






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>flatlight</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">OBJECTLIT</td>
<td class="description last">To set the theme flatlight.</td>
</tr>
<tr>
<td class="name"><code>flatdark</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">OBJECTLIT</td>
<td class="description last">To set the theme flatdark.</td>
</tr>
</tbody>
</table>















### Themes<span class="type-signature type string">string</span>
{:#members:themes}








Enum for gauge Themes






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>flatlight</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">OBJECTLIT</td>
<td class="description last">To set the themes flatlight.</td>
</tr>
<tr>
<td class="name"><code>flatdark</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">OBJECTLIT</td>
<td class="description last">To set the themes flatdark.</td>
</tr>
</tbody>
</table>















### Themes<span class="type-signature type string">string</span>
{:#members:themes}








Enum for gauge Themes






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>flatlight</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">OBJECTLIT</td>
<td class="description last">To set the themes flatlight.</td>
</tr>
<tr>
<td class="name"><code>flatdark</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">OBJECTLIT</td>
<td class="description last">To set the themes flatdark.</td>
</tr>
</tbody>
</table>















### Themes<span class="type-signature type string">string</span>
{:#members:themes}








Enum for gauge Themes






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>flatlight</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">OBJECTLIT</td>
<td class="description last">To set the themes flatlight.</td>
</tr>
<tr>
<td class="name"><code>flatdark</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">OBJECTLIT</td>
<td class="description last">To set the themes flatdark.</td>
</tr>
</tbody>
</table>















### ThumbStyle<span class="type-signature type string">string</span>
{:#members:thumbstyle}








Enum for slider






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Enum for normal mode thumb style slider</td>
</tr>
<tr>
<td class="name"><code>Small</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">small</td>
<td class="description last">Enum for small mode thumb style slider</td>
</tr>
</tbody>
</table>















### TickPlacement<span class="type-signature type string">string</span>
{:#members:tickplacement}








Enum for Bullet Graph tick placement






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Inside</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">inside</td>
<td class="description last">support for placing ticks inside scale.</td>
</tr>
<tr>
<td class="name"><code>Outside</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">outside</td>
<td class="description last">support for placing ticks outside scale.</td>
</tr>
</tbody>
</table>















### TickPlacement<span class="type-signature type string">string</span>
{:#members:tickplacement}








Enum for gauge TickPlacement






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Near</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">near</td>
<td class="description last">To set the TickPlacement near.</td>
</tr>
<tr>
<td class="name"><code>Far</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">far</td>
<td class="description last">To set the TickPlacement far.</td>
</tr>
<tr>
<td class="name"><code>Center</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">center</td>
<td class="description last">To set the TickPlacement center.</td>
</tr>
</tbody>
</table>















### TickPlacement<span class="type-signature type string">string</span>
{:#members:tickplacement}








Enum for gauge TickPlacement






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Near</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">near</td>
<td class="description last">To set the TickPlacement near.</td>
</tr>
<tr>
<td class="name"><code>Far</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">far</td>
<td class="description last">To set the TickPlacement far.</td>
</tr>
<tr>
<td class="name"><code>Center</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">center</td>
<td class="description last">To set the TickPlacement center.</td>
</tr>
</tbody>
</table>















### TickPosition<span class="type-signature type string">string</span>
{:#members:tickposition}








Enum for Bullet Graph Tick Position






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Far</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">far</td>
<td class="description last">To set the Tick position below quantitative scale.</td>
</tr>
<tr>
<td class="name"><code>Near</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">near</td>
<td class="description last">To set the Tick position above quantitative scale.</td>
</tr>
<tr>
<td class="name"><code>Center</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">center</td>
<td class="description last">To set the Tick position at the center of quantitative scale.</td>
</tr>
</tbody>
</table>















### TickType<span class="type-signature type string">string</span>
{:#members:ticktype}








Enum for gauge TickType






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Major</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">major</td>
<td class="description last">To set the TickType major.</td>
</tr>
<tr>
<td class="name"><code>Minor</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">minor</td>
<td class="description last">To set the TickType minor.</td>
</tr>
</tbody>
</table>















### TickType<span class="type-signature type string">string</span>
{:#members:ticktype}








Enum for gauge TickType






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>MajorInterval</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">majorinterval</td>
<td class="description last">To set the TickType majorinterval.</td>
</tr>
<tr>
<td class="name"><code>MinorInterval</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">minorinterval</td>
<td class="description last">To set the TickType minorinterval.</td>
</tr>
</tbody>
</table>















### TileSize<span class="type-signature type string">string</span>
{:#members:tilesize}








Enum for Tile Size






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Medium</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">medium</td>
<td class="description last">Enum for medium size of tile</td>
</tr>
<tr>
<td class="name"><code>Small</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">small</td>
<td class="description last">Enum for small size of tile</td>
</tr>
<tr>
<td class="name"><code>Large</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">large</td>
<td class="description last">Enum for large size of tile</td>
</tr>
<tr>
<td class="name"><code>Wide</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">wide</td>
<td class="description last">Enum for wide size of tile</td>
</tr>
</tbody>
</table>















### Tool<span class="type-signature type tool"><a href="global.html#Tool">Tool</a></span>
{:#members:tool}








Enum for the Tool in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>None</code></td>
<td class="type"><span class="param-type"><a href="global.html#Tool">Tool</a></span></td>
<td class="default">LSH</td>
<td class="description last">Disables all Tools</td>
</tr>
<tr>
<td class="name"><code>SingleSelect</code></td>
<td class="type"><span class="param-type"><a href="global.html#Tool">Tool</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables/Disables SingleSelect tool</td>
</tr>
<tr>
<td class="name"><code>MultipleSelect</code></td>
<td class="type"><span class="param-type"><a href="global.html#Tool">Tool</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables/Disables MultiSelect tool</td>
</tr>
<tr>
<td class="name"><code>ZoomPan</code></td>
<td class="type"><span class="param-type"><a href="global.html#Tool">Tool</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables/Disables ZoomPan tool</td>
</tr>
<tr>
<td class="name"><code>DrawOnce</code></td>
<td class="type"><span class="param-type"><a href="global.html#Tool">Tool</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables/Disables DrawOnce tool</td>
</tr>
<tr>
<td class="name"><code>ContinuesDraw</code></td>
<td class="type"><span class="param-type"><a href="global.html#Tool">Tool</a></span></td>
<td class="default">LSH</td>
<td class="description last">Enables/Disables ContinuousDraw tool</td>
</tr>
</tbody>
</table>















### Type<span class="type-signature type string">string</span>
{:#members:type}








Enum for chart series type.






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Line</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">line</td>
<td class="description last">sets the seriesType of chart to line.</td>
</tr>
<tr>
<td class="name"><code>Spline</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">spline</td>
<td class="description last">sets the seriesType of chart to spline.</td>
</tr>
<tr>
<td class="name"><code>Column</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">column</td>
<td class="description last">sets the seriesType of chart to column.</td>
</tr>
<tr>
<td class="name"><code>Doughnut</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">doughnut</td>
<td class="description last">sets the seriesType of chart to doughnut.</td>
</tr>
<tr>
<td class="name"><code>Area</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">area</td>
<td class="description last">sets the seriesType of chart to area.</td>
</tr>
<tr>
<td class="name"><code>SplineArea</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">splinearea</td>
<td class="description last">sets the seriesType of chart to splinearea.</td>
</tr>
<tr>
<td class="name"><code>StepLine</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">stepline</td>
<td class="description last">sets the seriesType of chart to stepline.</td>
</tr>
<tr>
<td class="name"><code>StepArea</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">steparea</td>
<td class="description last">sets the seriesType of chart to steparea.</td>
</tr>
<tr>
<td class="name"><code>Pie</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">pie</td>
<td class="description last">sets the seriesType of chart to pie.</td>
</tr>
<tr>
<td class="name"><code>Hilo</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">hilo</td>
<td class="description last">sets the seriesType of chart to hilo.</td>
</tr>
<tr>
<td class="name"><code>HiloOpenClose</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">hiloopenclose</td>
<td class="description last">sets the seriesType of chart to hiloopenclose.</td>
</tr>
<tr>
<td class="name"><code>Candle</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">candle</td>
<td class="description last">sets the seriesType of chart to candle.</td>
</tr>
<tr>
<td class="name"><code>Bubble</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">bubble</td>
<td class="description last">sets the seriesType of chart to bubble.</td>
</tr>
<tr>
<td class="name"><code>Scatter</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">scatter</td>
<td class="description last">sets the seriesType of chart to scatter.</td>
</tr>
<tr>
<td class="name"><code>Bar</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">bar</td>
<td class="description last">sets the seriesType of chart to bar.</td>
</tr>
<tr>
<td class="name"><code>StackingArea</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">stackingarea</td>
<td class="description last">sets the seriesType of chart to stackingarea.</td>
</tr>
<tr>
<td class="name"><code>StackingArea100</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">stackingarea100</td>
<td class="description last">sets the seriesType of chart to stackingarea100.</td>
</tr>
<tr>
<td class="name"><code>RangeColumn</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">rangecolumn</td>
<td class="description last">sets the seriesType of chart to rangecolumn.</td>
</tr>
<tr>
<td class="name"><code>StackingColumn</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">stackingcolumn</td>
<td class="description last">sets the seriesType of chart to stackingcolumn.</td>
</tr>
<tr>
<td class="name"><code>StackingColumn100</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">stackingcolumn100</td>
<td class="description last">sets the seriesType of chart to stackingcolumn100.</td>
</tr>
<tr>
<td class="name"><code>StackingBar</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">stackingbar</td>
<td class="description last">sets the seriesType of chart to stackingbar.</td>
</tr>
<tr>
<td class="name"><code>StackingBar100</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">stackingbar100</td>
<td class="description last">sets the seriesType of chart to stackingbar100.</td>
</tr>
<tr>
<td class="name"><code>Pyramid</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">pyramid</td>
<td class="description last">sets the seriesType of chart to pyramid.</td>
</tr>
<tr>
<td class="name"><code>Funnel</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">funnel</td>
<td class="description last">sets the seriesType of chart to funnel.</td>
</tr>
<tr>
<td class="name"><code>Polar</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">polar</td>
<td class="description last">sets the seriesType of chart to polar.</td>
</tr>
<tr>
<td class="name"><code>Radar</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">radar</td>
<td class="description last">sets the seriesType of chart to radar.</td>
</tr>
<tr>
<td class="name"><code>RangeArea</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">rangearea</td>
<td class="description last">sets the seriesType of chart to rangeArea.</td>
</tr>
</tbody>
</table>















### Type<span class="type-signature type string">string</span>
{:#members:type}








Enum for ej.mobile.Menu.IOS7.Type






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Auto</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">auto</td>
<td class="description last">Enum for auto type menu in ios7 mode</td>
</tr>
<tr>
<td class="name"><code>Animate</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">animate</td>
<td class="description last">Enum for animate type menu in ios7 mode</td>
</tr>
<tr>
<td class="name"><code>Normal</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">normal</td>
<td class="description last">Enum for normal type menu in ios7 mode</td>
</tr>
</tbody>
</table>















### Type<span class="type-signature type string">string</span>
{:#members:type}








Enum for ej.mobile.Menu.Android.Type






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Contextual</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">contextual</td>
<td class="description last">Enum for contextual type menu in android mode</td>
</tr>
<tr>
<td class="name"><code>Popup</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">popup</td>
<td class="description last">Enum for popup type menu in android mode</td>
</tr>
<tr>
<td class="name"><code>OptionsList</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">optionslist</td>
<td class="description last">Enum for optionslist type menu in android mode</td>
</tr>
<tr>
<td class="name"><code>OptionsMenu</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">optionsmenu</td>
<td class="description last">Enum for optionsmenu type menu in android mode</td>
</tr>
</tbody>
</table>















### Type<span class="type-signature type string">string</span>
{:#members:type}








Enum for ej.mobile.Menu.Windows.Type






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Contextual</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">contextual</td>
<td class="description last">Enum for contextual type menu in windows mode</td>
</tr>
<tr>
<td class="name"><code>Popup</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">popup</td>
<td class="description last">Enum for popup type menu in windows mode</td>
</tr>
</tbody>
</table>















### Unit<span class="type-signature type string">string</span>
{:#members:unit}








Enum for chart unit.






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>percentage</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">percentage</td>
<td class="description last">Specifies the unit in percentage.</td>
</tr>
<tr>
<td class="name"><code>pixel</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">pixel</td>
<td class="description last">Specifies the unit in pixel.</td>
</tr>
</tbody>
</table>















### UnitTextPlacement<span class="type-signature type string">string</span>
{:#members:unittextplacement}








Enum for gauge UnitTextPlacement






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Back</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">back</td>
<td class="description last">To set the UnitTextPlacement back.</td>
</tr>
<tr>
<td class="name"><code>Front</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">front</td>
<td class="description last">To set the UnitTextPlacement front.</td>
</tr>
</tbody>
</table>















### UnitTextPlacement<span class="type-signature type string">string</span>
{:#members:unittextplacement}








Enum for gauge UnitTextPlacement






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Front</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">front</td>
<td class="description last">To set the UnitTextPlacement front.</td>
</tr>
<tr>
<td class="name"><code>Back</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">back</td>
<td class="description last">To set the UnitTextPlacement back.</td>
</tr>
</tbody>
</table>















### UserHandlePositions<span class="type-signature type string">String</span>
{:#members:userhandlepositions}








Enum to specify the userhandle position in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>TopLeft</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="default">topleft</td>
<td class="description last">Used to set position as TopLeft</td>
</tr>
<tr>
<td class="name"><code>TopCenter</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="default">topcenter</td>
<td class="description last">Used to set position as TopCenter</td>
</tr>
<tr>
<td class="name"><code>TopRight</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="default">topright</td>
<td class="description last">Used to set position as TopRight</td>
</tr>
<tr>
<td class="name"><code>MiddleLeft</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="default">middleleft</td>
<td class="description last">Used to set position as MiddleLeft</td>
</tr>
<tr>
<td class="name"><code>MiddleRight</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="default">middleright</td>
<td class="description last">Used to set position as MiddleRight</td>
</tr>
<tr>
<td class="name"><code>BottomLeft</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="default">bottomleft</td>
<td class="description last">Used to set position as BottomLeft</td>
</tr>
<tr>
<td class="name"><code>BottomCenter</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="default">bottomcenter</td>
<td class="description last">Used to set position as BottomCenter</td>
</tr>
<tr>
<td class="name"><code>BottomRight</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="default">bottomright</td>
<td class="description last">Used to set position as BottomRight</td>
</tr>
</tbody>
</table>















### ValueType<span class="type-signature type string">string</span>
{:#members:valuetype}








Enum for chart valueType.






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Double</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">double</td>
<td class="description last">set valueType for chart to double.</td>
</tr>
<tr>
<td class="name"><code>DateTime</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">datetime</td>
<td class="description last">set valueType for chart to dateTime.</td>
</tr>
<tr>
<td class="name"><code>Category</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">category</td>
<td class="description last">set valueType for chart to category.</td>
</tr>
<tr>
<td class="name"><code>Logarithmic</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">logarithmic</td>
<td class="description last">set valueType for chart to logarithmic.</td>
</tr>
</tbody>
</table>















### VerticalAlignment<span class="type-signature type string">string</span>
{:#members:verticalalignment}








Enum for Vertical Alignment of elements in diagram






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Top</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">top</td>
<td class="description last">Used to align text Vertically on left side of node/connector</td>
</tr>
<tr>
<td class="name"><code>Center</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">center</td>
<td class="description last">Used to align text Vertically on center of node/connector</td>
</tr>
<tr>
<td class="name"><code>Bottom</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">bottom</td>
<td class="description last">Used to align text Vertically on bottom of node/connector</td>
</tr>
</tbody>
</table>















### ZIndex<span class="type-signature type string">string</span>
{:#members:zindex}








Enum for zIndex.






#### Properties:
{:#members:properties:}





<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>Over</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">over</td>
<td class="description last">Support for changing the zIndex to over.</td>
</tr>
<tr>
<td class="name"><code>Behind</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="default">behind</td>
<td class="description last">Support for changing the labelPosition to behind.</td>
</tr>
</tbody>
</table>













## Methods








### clearShapeSelection<span class="signature">()</span>
{:#methods:clearshapeselection}








Clear Selected Map Shapes











### refreshMarkers<span class="signature">()</span>
{:#methods:refreshmarkers}








Generates markers










<script type="text/javascript">
prettyPrint();
</script><script src="scripts/linenumber.js" type="text/javascript">
</script><script src="scripts/main.js" type="text/javascript">
</script>
