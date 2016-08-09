---
layout: post
title: Essential Studio JavaScript Global API reference
description: Essential Studio JavaScript Global API reference
documentation: API
platform: js
---










## Members








### Alignment
{:#enum:alignment}








Enum for alignment. 12






#### Properties

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
<td class="name">
Center</td>
<td class="type">string</td>
<td class="default">center</td>
<td class="description">Sets the lineJoin to center.</td>
</tr>
<tr>
<td class="name">
Near</td>
<td class="type">string</td>
<td class="default">near</td>
<td class="description">Sets the lineJoin to near.</td>
</tr>
<tr>
<td class="name">
Far</td>
<td class="type">string</td>
<td class="default">far</td>
<td class="description">Sets the lineJoin to far.</td>
</tr>
</tbody>
</table>















### ArrowShapes
{:#enum:arrowshapes}








Enum for the ArrowShapes in diagram






#### Properties






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
<td class="name">
None</td>
<td class="type">string</td>
<td class="default">none</td>
<td class="description"></td>
</tr>
<tr>
<td class="name">
CircularArrow</td>
<td class="type">string</td>
<td class="default">circulararrow</td>
<td class="description">Used to specify node Shape as CircularArrow</td>
</tr>
<tr>
<td class="name">
CurvedRightArrow</td>
<td class="type">string</td>
<td class="default">curvedrightarrow</td>
<td class="description">Used to specify node Shape as CurvedRightArrow</td>
</tr>
<tr>
<td class="name">
CurvedUpArrow</td>
<td class="type">string</td>
<td class="default">curveduparrow</td>
<td class="description">Used to specify node Shape as CurvedUpArrow</td>
</tr>
<tr>
<td class="name">
CurvedLeftArrow</td>
<td class="type">string</td>
<td class="default">curvedleftarrow</td>
<td class="description">Used to specify node Shape as CurvedLeftArrow</td>
</tr>
<tr>
<td class="name">
CurvedDownArrow</td>
<td class="type">string</td>
<td class="default">curveddownarrow</td>
<td class="description">Used to specify node Shape as CurvedDownArrow</td>
</tr>
<tr>
<td class="name">
JumpingRightArrow</td>
<td class="type">string</td>
<td class="default">jumpingrightarrow</td>
<td class="description">Used to specify node Shape as JumpingRightArrow</td>
</tr>
<tr>
<td class="name">
JumpingLeftArrow</td>
<td class="type">string</td>
<td class="default">jumpingleftarrow</td>
<td class="description">Used to specify node Shape as JumpingLeftArrow</td>
</tr>
</tbody>
</table>














### BasicShapes
{:#enum:basicshapes}








Enum for the BasicShapes in diagram






#### Properties






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
<td class="name">
Rectangle</td>
<td class="type">string</td>
<td class="default">rectangle</td>
<td class="description">Used to specify node Shape as Rectangle</td>
</tr>
<tr>
<td class="name">
Ellipse</td>
<td class="type">string</td>
<td class="default">ellipse</td>
<td class="description">Used to specify node Shape as Ellipse</td>
</tr>
<tr>
<td class="name">
Path</td>
<td class="type">string</td>
<td class="default">path</td>
<td class="description">Used to specify node Shape as Path</td>
</tr>
<tr>
<td class="name">
Polygon</td>
<td class="type">string</td>
<td class="default">polygon</td>
<td class="description">Used to specify node Shape as Polygon</td>
</tr>
<tr>
<td class="name">
Triangle</td>
<td class="type">string</td>
<td class="default">triangle</td>
<td class="description">Used to specify node Shape as Triangle</td>
</tr>
<tr>
<td class="name">
Plus</td>
<td class="type">string</td>
<td class="default">plus</td>
<td class="description">Used to specify node Shape as Plus</td>
</tr>
<tr>
<td class="name">
Star</td>
<td class="type">string</td>
<td class="default">star</td>
<td class="description">Used to specify node Shape as Star</td>
</tr>
<tr>
<td class="name">
Pentagon</td>
<td class="type">string</td>
<td class="default">pentagon</td>
<td class="description">Used to specify node Shape as Pentagon</td>
</tr>
<tr>
<td class="name">
Heptagon</td>
<td class="type">string</td>
<td class="default">heptagon</td>
<td class="description">Used to specify node Shape as Heptagon</td>
</tr>
<tr>
<td class="name">
Octagon</td>
<td class="type">string</td>
<td class="default">octagon</td>
<td class="description">Used to specify node Shape as Octagon</td>
</tr>
<tr>
<td class="name">
Trapezoid</td>
<td class="type">string</td>
<td class="default">trapezoid</td>
<td class="description">Used to specify node Shape as Trapezoid</td>
</tr>
<tr>
<td class="name">
Decagon</td>
<td class="type">string</td>
<td class="default">decagon</td>
<td class="description">Used to specify node Shape as Decagon</td>
</tr>
<tr>
<td class="name">
RightTriangle</td>
<td class="type">string</td>
<td class="default">righttriangle</td>
<td class="description">Used to specify node Shape as RightTriangle</td>
</tr>
<tr>
<td class="name">
Cylinder</td>
<td class="type">string</td>
<td class="default">cylinder</td>
<td class="description">Used to specify node Shape as Cylinder</td>
</tr>
</tbody>
</table>















### BingMapType
{:#enum:bingmaptype}








Enum for Map Bing map types






#### Properties






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
<td class="name">
Aerial</td>
<td class="type">string</td>
<td class="default">aerial</td>
<td class="description">support for bing map type aerial.</td>
</tr>
<tr>
<td class="name">
AerialWithLabel</td>
<td class="type">string</td>
<td class="default">aerialwithlabel</td>
<td class="description">support for bing map type aerialwithlabel.</td>
</tr>
<tr>
<td class="name">
Road</td>
<td class="type">string</td>
<td class="default">road</td>
<td class="description">support for bing map type road.</td>
</tr>
</tbody>
</table>















### BPMNActivity
{:#enum:bpmnactivity}








Enum for the BPMNActivity in diagram






#### Properties






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
<td class="name">
None</td>
<td class="type">string</td>
<td class="default">none</td>
<td class="description">Used to set BPMN Activity as None</td>
</tr>
<tr>
<td class="name">
Task</td>
<td class="type">string</td>
<td class="default">task</td>
<td class="description">Used to set BPMN Activity as Task</td>
</tr>
<tr>
<td class="name">
SubProcess</td>
<td class="type">string</td>
<td class="default">subprocess</td>
<td class="description">Used to set BPMN Activity as SubProcess</td>
</tr>
</tbody>
</table>















### BPMNBoundary
{:#enum:bpmnboundary}








Enum for the BPMNBoundary in diagram






#### Properties






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
<td class="name">
Default</td>
<td class="type">string</td>
<td class="default">default</td>
<td class="description">Used to set BPMN SubProcess's Boundary as Default</td>
</tr>
<tr>
<td class="name">
Call</td>
<td class="type">string</td>
<td class="default">call</td>
<td class="description">Used to set BPMN SubProcess's Boundary as Call</td>
</tr>
<tr>
<td class="name">
Event</td>
<td class="type">string</td>
<td class="default">event</td>
<td class="description">Used to set BPMN SubProcess's Boundary as Event</td>
</tr>
</tbody>
</table>















### BPMNDirections
{:#enum:bpmndirections}








Enum for the BPMNDirections in diagram






#### Properties






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
<td class="name">
None</td>
<td class="type">string</td>
<td class="default">none</td>
<td class="description">Used to set BPMN Flow Direction as None</td>
</tr>
<tr>
<td class="name">
UniDirectional</td>
<td class="type">string</td>
<td class="default">unidirectional</td>
<td class="description">Used to set BPMN Flow Direction as UniDirectional</td>
</tr>
<tr>
<td class="name">
BiDirectional</td>
<td class="type">string</td>
<td class="default">bidirectional</td>
<td class="description">Used to set BPMN Flow Direction as BiDirectional</td>
</tr>
</tbody>
</table>















### BPMNEvents
{:#enum:bpmnevents}








Enum for the BPMNEvents in diagram






#### Properties






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
<td class="name">
Start</td>
<td class="type">string</td>
<td class="default">start</td>
<td class="description">Used to set BPMN Event as Start</td>
</tr>
<tr>
<td class="name">
Intermediate</td>
<td class="type">string</td>
<td class="default">intermediate</td>
<td class="description">Used to set BPMN Event as Intermediate</td>
</tr>
<tr>
<td class="name">
End</td>
<td class="type">string</td>
<td class="default">end</td>
<td class="description">Used to set BPMN Event as End</td>
</tr>
<tr>
<td class="name">
NonInterruptingStart</td>
<td class="type">string</td>
<td class="default">noninterruptingstart</td>
<td class="description">Used to set BPMN Event as NonInterruptingStart</td>
</tr>
<tr>
<td class="name">
NonInterruptingIntermediate</td>
<td class="type">string</td>
<td class="default">noninterruptingintermediate</td>
<td class="description">Used to set BPMN Event as NonInterruptingIntermediate</td>
</tr>
</tbody>
</table>















### BPMNGateways
{:#enum:bpmngateways}








Enum for the BPMNGateways in diagram






#### Properties






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
<td class="name">
None</td>
<td class="type">string</td>
<td class="default">none</td>
<td class="description">Used to set BPMN Gateway as None</td>
</tr>
<tr>
<td class="name">
Exclusive</td>
<td class="type">string</td>
<td class="default">exclusive</td>
<td class="description">Used to set BPMN Gateway as Exclusive</td>
</tr>
<tr>
<td class="name">
Inclusive</td>
<td class="type">string</td>
<td class="default">inclusive</td>
<td class="description">Used to set BPMN Gateway as Inclusive</td>
</tr>
<tr>
<td class="name">
Parallel</td>
<td class="type">string</td>
<td class="default">parallel</td>
<td class="description">Used to set BPMN Gateway as Parallel</td>
</tr>
<tr>
<td class="name">
Complex</td>
<td class="type">string</td>
<td class="default">complex</td>
<td class="description">Used to set BPMN Gateway as Complex</td>
</tr>
<tr>
<td class="name">
EventBased</td>
<td class="type">string</td>
<td class="default">eventbased</td>
<td class="description">Used to set BPMN Gateway as EventBased</td>
</tr>
</tbody>
</table>















### BPMNLoops
{:#enum:bpmnloops}








Enum for the BPMNLoops in diagram






#### Properties






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
<td class="name">
None</td>
<td class="type">string</td>
<td class="default">none</td>
<td class="description">Used to set BPMN Activity's Loop as None</td>
</tr>
<tr>
<td class="name">
Standard</td>
<td class="type">string</td>
<td class="default">standard</td>
<td class="description">Used to set BPMN Activity's Loop as Standard</td>
</tr>
<tr>
<td class="name">
ParallelMultiInstance</td>
<td class="type">string</td>
<td class="default">parallelmultiinstance</td>
<td class="description">Used to set BPMN Activity's Loop as ParallelMultiInstance</td>
</tr>
<tr>
<td class="name">
SequenceMultiInstance</td>
<td class="type">string</td>
<td class="default">sequencemultiinstance</td>
<td class="description">Used to set BPMN Activity's Loop as SequenceMultiInstance</td>
</tr>
</tbody>
</table>















### BPMNShapes
{:#enum:bpmnshapes}








Enum for the BPMNShapes in diagram






#### Properties






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
<td class="name">
Event</td>
<td class="type">string</td>
<td class="default">event</td>
<td class="description">Used to specify node Shape as Event</td>
</tr>
<tr>
<td class="name">
Gateway</td>
<td class="type">string</td>
<td class="default">gateway</td>
<td class="description">Used to specify node Shape as Gateway</td>
</tr>
<tr>
<td class="name">
SequentialFlow</td>
<td class="type">string</td>
<td class="default">sequentialflow</td>
<td class="description">Used to specify node Shape as SequentialFlow</td>
</tr>
<tr>
<td class="name">
AssociationFlow</td>
<td class="type">string</td>
<td class="default">associationflow</td>
<td class="description">Used to specify node Shape as AssociationFlow</td>
</tr>
<tr>
<td class="name">
MessageFlow</td>
<td class="type">string</td>
<td class="default">messageflow</td>
<td class="description">Used to specify node Shape as MessageFlow</td>
</tr>
<tr>
<td class="name">
Message</td>
<td class="type">string</td>
<td class="default">message</td>
<td class="description">Used to specify node Shape as Message</td>
</tr>
<tr>
<td class="name">
DataObject</td>
<td class="type">string</td>
<td class="default">dataobject</td>
<td class="description">Used to specify node Shape as DataObject</td>
</tr>
<tr>
<td class="name">
DataSource</td>
<td class="type">string</td>
<td class="default">datasource</td>
<td class="description">Used to specify node Shape as DataSource</td>
</tr>
<tr>
<td class="name">
Activity</td>
<td class="type">string</td>
<td class="default">activity</td>
<td class="description">Used to specify node Shape as Activity</td>
</tr>
</tbody>
</table>















### BPMNTasks
{:#enum:bpmntasks}








Enum for the BPMNTasks in diagram






#### Properties






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
<td class="name">
None</td>
<td class="type">string</td>
<td class="default">none</td>
<td class="description">Used to set BPMN Task Type as None</td>
</tr>
<tr>
<td class="name">
Service</td>
<td class="type">string</td>
<td class="default">service</td>
<td class="description">Used to set BPMN Task Type as Service</td>
</tr>
<tr>
<td class="name">
Receive</td>
<td class="type">string</td>
<td class="default">receive</td>
<td class="description">Used to set BPMN Task Type as Receive</td>
</tr>
<tr>
<td class="name">
Send</td>
<td class="type">string</td>
<td class="default">send</td>
<td class="description">Used to set BPMN Task Type as Send</td>
</tr>
<tr>
<td class="name">
InstantiatingReceive</td>
<td class="type">string</td>
<td class="default">instantiatingreceive</td>
<td class="description">Used to set BPMN Task Type as InstantiatingReceive</td>
</tr>
<tr>
<td class="name">
Manual</td>
<td class="type">string</td>
<td class="default">manual</td>
<td class="description">Used to set BPMN Task Type as Manual</td>
</tr>
<tr>
<td class="name">
BusinessRule</td>
<td class="type">string</td>
<td class="default">businessrule</td>
<td class="description">Used to set BPMN Task Type as BusinessRule</td>
</tr>
<tr>
<td class="name">
User</td>
<td class="type">string</td>
<td class="default">user</td>
<td class="description">Used to set BPMN Task Type as User</td>
</tr>
<tr>
<td class="name">
Script</td>
<td class="type">string</td>
<td class="default">script</td>
<td class="description">Used to set BPMN Task Type as Script</td>
</tr>
<tr>
<td class="name">
Parallel</td>
<td class="type">string</td>
<td class="default">parallel</td>
<td class="description">Used to set BPMN Task Type as Parallel</td>
</tr>
</tbody>
</table>















### BPMNTriggers
{:#enum:bpmntriggers}








Enum for the BPMNTriggers in diagram






#### Properties






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
<td class="name">
None</td>
<td class="type">string</td>
<td class="default">none</td>
<td class="description">Used to set Event Trigger as None</td>
</tr>
<tr>
<td class="name">
Message</td>
<td class="type">string</td>
<td class="default">message</td>
<td class="description">Used to set Event Trigger as Message</td>
</tr>
<tr>
<td class="name">
Timer</td>
<td class="type">string</td>
<td class="default">timer</td>
<td class="description">Used to set Event Trigger as Timer</td>
</tr>
<tr>
<td class="name">
Escalation</td>
<td class="type">string</td>
<td class="default">escalation</td>
<td class="description">Used to set Event Trigger as Escalation</td>
</tr>
<tr>
<td class="name">
Link</td>
<td class="type">string</td>
<td class="default">link</td>
<td class="description">Used to set Event Trigger as Link</td>
</tr>
<tr>
<td class="name">
Error</td>
<td class="type">string</td>
<td class="default">error</td>
<td class="description">Used to set Event Trigger as Error</td>
</tr>
<tr>
<td class="name">
Compensation</td>
<td class="type">string</td>
<td class="default">compensation</td>
<td class="description">Used to set Event Trigger as Compensation</td>
</tr>
<tr>
<td class="name">
Signal</td>
<td class="type">string</td>
<td class="default">signal</td>
<td class="description">Used to set Event Trigger as Signal</td>
</tr>
<tr>
<td class="name">
Multiple</td>
<td class="type">string</td>
<td class="default">multiple</td>
<td class="description">Used to set Event Trigger as Multiple</td>
</tr>
<tr>
<td class="name">
Parallel</td>
<td class="type">string</td>
<td class="default">parallel</td>
<td class="description">Used to set Event Trigger as Parallel</td>
</tr>
</tbody>
</table>

### BridgeDirection
{:#enum:bridgedirection}

Enum for the BridgeDirection in diagram

#### Properties

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
<td class="name">Left</td>
<td class="type">string</td>
<td class="default">left</td>
<td class="description">Used to set the direction of line bridges as left</td>
</tr>
<tr>
<td class="name">Right</td>
<td class="type">string</td>
<td class="default">right</td>
<td class="description">Used to set the direction of line bridges as right</td>
</tr>
<tr>
<td class="name">Top</td>
<td class="type">string</td>
<td class="default">top</td>
<td class="description">Used to set the direction of line bridges as top</td>
</tr>
<tr>
<td class="name">Bottom</td>
<td class="type">string</td>
<td class="default">bottom</td>
<td class="description">Used to set the direction of line bridges as bottom</td>
</tr>
</tbody>
</table>














### ButtonStyle
{:#enum:buttonstyle}








Enum for ej.mobile.Menu.IOS7.ButtonStyle






#### Properties






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
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for normal ios7 button style</td>
</tr>
<tr>
<td class="name">
Back</td>
<td class="type">string</td>
<td class="default">back</td>
<td class="description">Enum for back ios7 button style</td>
</tr>
<tr>
<td class="name">
Header</td>
<td class="type">string</td>
<td class="default">header</td>
<td class="description">Enum for header ios7 button style</td>
</tr>
<tr>
<td class="name">
Dialog</td>
<td class="type">string</td>
<td class="default">dialog</td>
<td class="description">Enum for dialog ios7 button style</td>
</tr>
</tbody>
</table>















### CancelButtonColor
{:#enum:cancelbuttoncolor}








Enum for ej.mobile.Menu.IOS7.CancelButtonColor






#### Properties






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
<td class="name">
Blue</td>
<td class="type">string</td>
<td class="default">blue</td>
<td class="description">Enum for blue color button in ios7 mode</td>
</tr>
<tr>
<td class="name">
Gray</td>
<td class="type">string</td>
<td class="default">gray</td>
<td class="description">Enum for gray color button in ios7 mode</td>
</tr>
<tr>
<td class="name">
Black</td>
<td class="type">string</td>
<td class="default">black</td>
<td class="description">Enum for black color button in ios7 mode</td>
</tr>
<tr>
<td class="name">
Green</td>
<td class="type">string</td>
<td class="default">green</td>
<td class="description">Enum for green color button in ios7 mode</td>
</tr>
<tr>
<td class="name">
Red</td>
<td class="type">string</td>
<td class="default">red</td>
<td class="description">Enum for red color button in ios7 mode</td>
</tr>
</tbody>
</table>















### CharacterType
{:#enum:charactertype}








Enum for gauge CharacterType






#### Properties






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
<td class="name">
SevenSegment</td>
<td class="type">string</td>
<td class="default">sevensegment</td>
<td class="description">To set the CharacterType sevensegment.</td>
</tr>
<tr>
<td class="name">
FourteenSegment</td>
<td class="type">string</td>
<td class="default">fourteensegment</td>
<td class="description">To set the CharacterType fourteensegment.</td>
</tr>
<tr>
<td class="name">
SixteenSegment</td>
<td class="type">string</td>
<td class="default">sixteensegment</td>
<td class="description">To set the CharacterType sixteensegment.</td>
</tr>
<tr>
<td class="name">
EightCrossEightDotMatrix</td>
<td class="type">string</td>
<td class="default">eightcrosseightdotmatrix</td>
<td class="description">To set the CharacterType eightcrosseightdotmatrix.</td>
</tr>
<tr>
<td class="name">
EightCrossEightSquareMatrix</td>
<td class="type">string</td>
<td class="default">eightcrosseightsquarematrix</td>
<td class="description">To set the CharacterType eightcrosseightsquarematrix.</td>
</tr>
</tbody>
</table>















### ChartOrientations
{:#enum:chartorientations}








Enum for ChartOrientations in diagram






#### Properties






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
<td class="name">
Horizontal</td>
<td class="type">string</td>
<td class="default">horizontal</td>
<td class="description">Used to set horizontal organizational chart orientation</td>
</tr>
<tr>
<td class="name">
Vertical</td>
<td class="type">string</td>
<td class="default">vertical</td>
<td class="description">Used to set vertical organizational chart orientation</td>
</tr>
</tbody>
</table>















### ChartTypes
{:#enum:charttypes}








Enum for ChartTypes in diagram






#### Properties






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
<td class="name">
Left</td>
<td class="type">string</td>
<td class="default">left</td>
<td class="description">Used to arrange the children at left side of parent</td>
</tr>
<tr>
<td class="name">
Right</td>
<td class="type">string</td>
<td class="default">right</td>
<td class="description">Used to arrange the children at right side of parent</td>
</tr>
<tr>
<td class="name">
Alternate</td>
<td class="type">string</td>
<td class="default">alternate</td>
<td class="description">Used to arrange the children at alternative sides(left,right) of parent</td>
</tr>
<tr>
<td class="name">
Center</td>
<td class="type">string</td>
<td class="default">center</td>
<td class="description">Used to arrange the children with respect to the middle of parent</td>
</tr>
</tbody>
</table>















### CheckState
{:#enum:checkstate}








Enum for CheckboxState






#### Properties






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
<td class="name">
Uncheck</td>
<td class="type">string</td>
<td class="default">uncheck</td>
<td class="description">Enum for Uncheck state checkbox</td>
</tr>
<tr>
<td class="name">
Check</td>
<td class="type">string</td>
<td class="default">check</td>
<td class="description">Enum for Check state checkbox</td>
</tr>
<tr>
<td class="name">
Indeterminate</td>
<td class="type">string</td>
<td class="default">indeterminate</td>
<td class="description">Enum for Indeterminate state checkbox</td>
</tr>
</tbody>
</table>















### Color
{:#enum:color}








Enum for IOS7Color






#### Properties






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
<td class="name">
Gray</td>
<td class="type">string</td>
<td class="default">gray</td>
<td class="description">Enum for gray ios7 button color</td>
</tr>
<tr>
<td class="name">
Black</td>
<td class="type">string</td>
<td class="default">black</td>
<td class="description">Enum for black ios7 button color</td>
</tr>
<tr>
<td class="name">
Blue</td>
<td class="type">string</td>
<td class="default">blue</td>
<td class="description">Enum for black ios7 buttonColor</td>
</tr>
<tr>
<td class="name">
Green</td>
<td class="type">string</td>
<td class="default">green</td>
<td class="description">Enum for green ios7 button color</td>
</tr>
<tr>
<td class="name">
Red</td>
<td class="type">string</td>
<td class="default">red</td>
<td class="description">Enum for red ios7 button color</td>
</tr>
</tbody>
</table>















### ColorPalette
{:#enum:colorpalette}








Enum for Map color palette






#### Properties






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
<td class="name">
Palette1</td>
<td class="type">string</td>
<td class="default">palette1</td>
<td class="description">support for color palette palette1.</td>
</tr>
<tr>
<td class="name">
Palette2</td>
<td class="type">string</td>
<td class="default">palette2</td>
<td class="description">support for color palette palette2.</td>
</tr>
<tr>
<td class="name">
Palette3</td>
<td class="type">string</td>
<td class="default">palette3</td>
<td class="description">support for color palette palette3.</td>
</tr>
<tr>
<td class="name">
CustomPalette</td>
<td class="type">string</td>
<td class="default">custompalette</td>
<td class="description">support for color palette custompalette.</td>
</tr>
</tbody>
</table>















### ConnectorConstraints
{:#enum:connectorconstraints}








Enum for ConnectorConstraints in diagram






#### Properties






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
<td class="name">
None</td>
<td class="type">ConnectorConstraints</td>
<td class="default">LSH</td>
<td class="description">Disable all connector Constraints</td>
</tr>
<tr>
<td class="name">
Select</td>
<td class="type">ConnectorConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables connector to be selected</td>
</tr>
<tr>
<td class="name">
Delete</td>
<td class="type">ConnectorConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables connector to be Deleted</td>
</tr>
<tr>
<td class="name">
Drag</td>
<td class="type">ConnectorConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables connector to be Dragged</td>
</tr>
<tr>
<td class="name">
DragSourceEnd</td>
<td class="type">ConnectorConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables connectors source end to be selected</td>
</tr>
<tr>
<td class="name">
DragTargetEnd</td>
<td class="type">ConnectorConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables connectors target end to be selected</td>
</tr>
<tr>
<td class="name">
DragSegmentThumb</td>
<td class="type">ConnectorConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables control point and end point of every segment in a connector for editing</td>
</tr>
<tr>
<td class="name">
Bridging</td>
<td class="type">ConnectorConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables bridging to the connector</td>
</tr>
<tr>
<td class="name">
DragLabel</td>
<td class="type">ConnectorConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables label of node to be Dragged</td>
</tr>
<tr>
<td class="name">
InheritBridging</td>
<td class="type">ConnectorConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables bridging to the connector</td>
</tr>
<tr>
<td class="name">
Default</td>
<td class="type">ConnectorConstraints</td>
<td class="default">BITOR</td>
<td class="description">Enables all constraints</td>
</tr>
</tbody>
</table>















### ConnectorLineType
{:#enum:connectorlinetype}








Enum for connector line in Chart data label






#### Properties






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
<td class="name">
Line</td>
<td class="type">string</td>
<td class="default">line</td>
<td class="description">Line will be used to connect datalabel and datapoint</td>
</tr>
<tr>
<td class="name">
Bezier</td>
<td class="type">string</td>
<td class="default">bezier</td>
<td class="description">Bezier curve will be used to connect datalabel and datapoint</td>
</tr>
</tbody>
</table>















### ContainerType
{:#enum:containertype}








Enum for various containerType in diagram






#### Properties






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
<td class="name">
Canvas</td>
<td class="type">string</td>
<td class="default">canvas</td>
<td class="description">Sets the container type as Canvas</td>
</tr>
<tr>
<td class="name">
Stack</td>
<td class="type">string</td>
<td class="default">stack</td>
<td class="description">Sets the container type as Stack</td>
</tr>
</tbody>
</table>















### ContentType
{:#enum:contenttype}








Enum for ContentType






#### Properties






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
<td class="name">
Text</td>
<td class="type">string</td>
<td class="default">text</td>
<td class="description">Enum for text content type</td>
</tr>
<tr>
<td class="name">
Image</td>
<td class="type">string</td>
<td class="default">image</td>
<td class="description">Enum for image content type</td>
</tr>
<tr>
<td class="name">
Both</td>
<td class="type">string</td>
<td class="default">both</td>
<td class="description">Enum for displaying both text and image content type</td>
</tr>
</tbody>
</table>















### ContentType
{:#enum:contenttype}








Enum for Android tabContentType






#### Properties






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
<td class="name">
Text</td>
<td class="type">string</td>
<td class="default">text</td>
<td class="description">Enum for text content type</td>
</tr>
<tr>
<td class="name">
Image</td>
<td class="type">string</td>
<td class="default">image</td>
<td class="description">Enum for image content type</td>
</tr>
<tr>
<td class="name">
Both</td>
<td class="type">string</td>
<td class="default">both</td>
<td class="description">Enum for displaying both text and image content type</td>
</tr>
</tbody>
</table>















### CoordinateUnit
{:#enum:coordinateunit}








Enum for coordinate unit in Chart annotation






#### Properties






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
<td class="name">
None</td>
<td class="type">string</td>
<td class="default">none</td>
<td class="description">Set none as coordinate unit. Annotations will be placed at a location based on horizontal and vertical alignments</td>
</tr>
<tr>
<td class="name">
Pixels</td>
<td class="type">string</td>
<td class="default">pixels</td>
<td class="description">Set pixel as coordinate unit.</td>
</tr>
<tr>
<td class="name">
Points</td>
<td class="type">string</td>
<td class="default">Points</td>
<td class="description">Set points as coordinate unit.</td>
</tr>
</tbody>
</table>















### CrosshairType
{:#enum:crosshairtype}








Enum for chart crosshairType.






#### Properties






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
<td class="name">
Crosshair</td>
<td class="type">string</td>
<td class="default">crosshair</td>
<td class="description">set crosshair for chart.</td>
</tr>
<tr>
<td class="name">
TrackBall</td>
<td class="type">string</td>
<td class="default">trackBall</td>
<td class="description">set trackBall for chart.</td>
</tr>
</tbody>
</table>















### CustomLabelPositionType
{:#enum:customlabelpositiontype}








Enum for gauge CustomLabelPositionType






#### Properties






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
<td class="name">
Inner</td>
<td class="type">string</td>
<td class="default">inner</td>
<td class="description">To set the CustomLabelPositionType inner.</td>
</tr>
<tr>
<td class="name">
Outer</td>
<td class="type">string</td>
<td class="default">outer</td>
<td class="description">To set the CustomLabelPositionType outer.</td>
</tr>
</tbody>
</table>















### CustomLabelPositionType
{:#enum:customlabelpositiontype}








Enum for gauge CustomLabelPositionType






#### Properties






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
<td class="name">
Inner</td>
<td class="type">string</td>
<td class="default">inner</td>
<td class="description">To set the CustomLabelPositionType inner.</td>
</tr>
<tr>
<td class="name">
Outer</td>
<td class="type">string</td>
<td class="default">outer</td>
<td class="description">To set the CustomLabelPositionType outer.</td>
</tr>
</tbody>
</table>















### ColumnLayout
{:#enum:columnlayout}
 
Specifies whether the Grid's column layout is Auto or Fixed.
 
<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Auto</td>
<td class="description">Column layout is auto(based on width).</td>
</tr>
<tr>
<td class="name">Fixed</td>
<td class="description">Column layout is fixed(based on width).</td>
</tr>
</tbody>
</table>


### ClipMode
{:#enum:clipmode}
 
Specifies whether the Grid's clip mode is Ellipsis, Clip or EllipsisWithTooltip.

<table class="props">
<thead>
<tr>
<th>Name</th> 
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Ellipsis</td> 
<td class="description">Shows ellipsis for the overflown cell.</td> 
</tr>
<tr>
<td class="name">Clip</td> 
<td class="description">Truncate the text in the cell.</td>
</tr>
<tr>
<td class="name">EllipsisWithTooltip</td> 
<td class="description">Shows ellipsis and tooltip for the overflown cell.</td>
</tr>
</tbody>
</table>




### dataTypes
{:#enum:datatypes}








datatypes to the default model values











### DecoratorShapes
{:#enum:decoratorshapes}








Enum for various decorator shapes in diagram






#### Properties






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
<td class="name">
None</td>
<td class="type">string</td>
<td class="default">none</td>
<td class="description">Used to set decorator shape as none</td>
</tr>
<tr>
<td class="name">
Arrow</td>
<td class="type">string</td>
<td class="default">arrow</td>
<td class="description">Used to set decorator shape as Arrow</td>
</tr>
<tr>
<td class="name">
OpenArrow</td>
<td class="type">string</td>
<td class="default">openarrow</td>
<td class="description">Used to set decorator shape as Open Arrow</td>
</tr>
<tr>
<td class="name">
Circle</td>
<td class="type">string</td>
<td class="default">circle</td>
<td class="description">Used to set decorator shape as Circle</td>
</tr>
<tr>
<td class="name">
Diamond</td>
<td class="type">string</td>
<td class="default">diamond</td>
<td class="description">Used to set decorator shape as Diamond</td>
</tr>
<tr>
<td class="name">
Path</td>
<td class="type">string</td>
<td class="default">path</td>
<td class="description">Used to set decorator shape as path</td>
</tr>
</tbody>
</table>















### DiagramConstraints
{:#enum:diagramconstraints}








Enum for the DiagramConstraints in diagram






#### Properties






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
<td class="name">
None</td>
<td class="type">DiagramConstraints</td>
<td class="default">LSH</td>
<td class="description">Disables all DiagramConstraints</td>
</tr>
<tr>
<tr>
<td class="name">
UserInteraction</td>
<td class="type">DiagramConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables/Disables the interaction at runtime</td>
</tr>
<tr>
<td class="name">
APIUpdate</td>
<td class="type">DiagramConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables/Disables to edit the page programmatically</td>
</tr>
<td class="name">
PageEditable</td>
<td class="type">DiagramConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables/Disables to edit the diagram both through programmatically and through interaction</td>
</tr>
<tr>
<td class="name">
Bridging</td>
<td class="type">DiagramConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables/Disables Bridging</td>
</tr>
<tr>
<td class="name">
Zoomable</td>
<td class="type">DiagramConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables/Disables Zooming</td>
</tr>
<tr>
<td class="name">
PannableX</td>
<td class="type">DiagramConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables/Disables panning on horizontal axis</td>
</tr>
<tr>
<td class="name">
PannableY</td>
<td class="type">DiagramConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables/Disables panning on vertical axis</td>
</tr>
<tr>
<td class="name">
Pannable</td>
<td class="type">DiagramConstraints</td>
<td class="default">BITOR</td>
<td class="description">Enables/Disables Panning</td>
</tr>
<tr>
<td class="name">
Undoable</td>
<td class="type">DiagramConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables/Disables undo actions</td>
</tr>
<tr>
<td class="name">
Resizable</td>
<td class="type">DiagramConstraints</td>
<td class="default">LSH</td>
<td class="description">Automatically adjusts the view port size, when the window is resized</td>
</tr>
<tr>
<td class="name">
Default</td>
<td class="type">DiagramConstraints</td>
<td class="default">BITOR</td>
<td class="description">Enables all Constraints</td>
</tr>
</tbody>
</table>














### Directions
{:#enum:directions}








Enum for gauge Directions






#### Properties






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
<td class="name">
Clockwise</td>
<td class="type">string</td>
<td class="default">clockwise</td>
<td class="description">To set the Directions clockwise.</td>
</tr>
<tr>
<td class="name">
CounterClockwise</td>
<td class="type">string</td>
<td class="default">counterclockwise</td>
<td class="description">To set the Directions counterclockwise.</td>
</tr>
</tbody>
</table>















### Directions
{:#enum:directions}








Enum for gauge Directions






#### Properties






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
<td class="name">
Clockwise</td>
<td class="type">string</td>
<td class="default">clockwise</td>
<td class="description">To set the Directions clockwise.</td>
</tr>
<tr>
<td class="name">
CounterClockwise</td>
<td class="type">string</td>
<td class="default">counterclockwise</td>
<td class="description">To set the Directions counterclockwise.</td>
</tr>
</tbody>
</table>















### DragState
{:#enum:dragstate}








Enum for the Dragstate of the connector in diagram






#### Properties






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
<td class="name">
Starting</td>
<td class="type">string</td>
<td class="default">starting</td>
<td class="description">sets the drag state as starting</td>
</tr>
<tr>
<td class="name">
Dragging</td>
<td class="type">string</td>
<td class="default">dragging</td>
<td class="description">sets the drag state as dragging</td>
</tr>
<tr>
<td class="name">
Completed</td>
<td class="type">string</td>
<td class="default">completed</td>
<td class="description">sets the drag state as completed</td>
</tr>
</tbody>
</table>















### DrawMode
{:#enum:drawmode}








Enum for hilopenclose drawmode.






#### Properties






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
<td class="name">
Both</td>
<td class="type">string</td>
<td class="default">both</td>
<td class="description">Specifies the draw mode as both.</td>
</tr>
<tr>
<td class="name">
Open</td>
<td class="type">string</td>
<td class="default">open</td>
<td class="description">Specifies the draw mode as open.</td>
</tr>
<tr>
<td class="name">
Close</td>
<td class="type">string</td>
<td class="default">close</td>
<td class="description">Specifies the draw mode as close</td>
</tr>
</tbody>
</table>















### DrawType
{:#enum:drawtype}








Enum for chart drawType mode.






#### Properties






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
<td class="name">
Line</td>
<td class="type">string</td>
<td class="default">line</td>
<td class="description">Specifies the drawType as line.</td>
</tr>
<tr>
<td class="name">
Column</td>
<td class="type">string</td>
<td class="default">column</td>
<td class="description">Specifies the drawType as column.</td>
</tr>
<tr>
<td class="name">
Area</td>
<td class="type">string</td>
<td class="default">area</td>
<td class="description">Specifies the drawType as area.</td>
</tr>
</tbody>
</table>















### EdgeLabelPlacement
{:#enum:edgelabelplacement}








Enum for chart edgeLabelPlacement.






#### Properties






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
<td class="name">
None</td>
<td class="type">string</td>
<td class="default">none</td>
<td class="description">Places the edge labels in the same position.</td>
</tr>
<tr>
<td class="name">
Shift</td>
<td class="type">string</td>
<td class="default">shift</td>
<td class="description">Shift the edge labels inside the chart area.</td>
</tr>
<tr>
<td class="name">
Hide</td>
<td class="type">string</td>
<td class="default">hide</td>
<td class="description">Hide the edge labels which exceeds the chart area boundary.</td>
</tr>
</tbody>
</table>















### element
{:#enum:element}








Widget element will be automatically set in this















### ExportType
{:#enum:exporttype}








Enum for the types of exporting in Chart






#### Properties






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
<td class="name">
Image</td>
<td class="type">string</td>
<td class="default">image</td>
<td class="description">Specifies Chart should be exported as an image</td>
</tr>
<tr>
<td class="name">
Excel</td>
<td class="type">string</td>
<td class="default">excel</td>
<td class="description">Specifies Chart should be exported in excel</td>
</tr>
</tbody>
</table>











### ExportModes
{:#enum:exportmodes}








Enum for the ExportModes in diagram






#### Properties






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
<td class="name">
Download</td>
<td class="type">string</td>
<td class="default">download</td>
<td class="description">Downloads the exported diagram</td>
</tr>
<tr>
<td class="name">
Data</td>
<td class="type">string</td>
<td class="default">data</td>
<td class="description">Converts diagram to data of type imageURL/svg</td>
</tr>
</tbody>
</table>















### EditingType
{:#enum:editingtype}
 
Specifies whether the Grid's editing type is String, Boolean, Numeric, Dropdown, DatePicker or DateTimePicker.

<table class="props">
<thead>
<tr>
<th>Name</th> 
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">String</td> 
<td class="description">Specifies editing type as stringedit.</td>
</tr>
<tr>
<td class="name">Boolean</td> 
<td class="description">Specifies editing type as booleanedit.</td>
</tr>
<tr>
<td class="name">Numeric</td> 
<td class="description">Specifies editing type as numericedit.</td>
</tr>
<tr>
<td class="name">Dropdown</td> 
<td class="description">Specifies editing type as dropdownedit.</td>
</tr>
<tr>
<td class="name">DatePicker</td>
<td class="description">Specifies editing type as datepicker.</td>
</tr>
<tr>
<td class="name">DateTimePicker</td> 
<td class="description">Specifies editing type as datetimepicker.</td>
</tr>
</tbody>
</table>
 

### EditMode
{:#enum:editmode}
 
Specifies whether the Grid's edit mode is Normal, Dialog, DialogTemplate, Batch, InlineForm, InlineTemplateForm, ExternalForm or ExternalFormTemplate.
 
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
            <td class="description">Edit mode is normal</td>
        </tr>
        <tr>
            <td class="name">Dialog</td>
            <td class="description">Edit mode is dialog</td>
        </tr>
        <tr>
            <td class="name">DialogTemplate</td>
            <td class="description">Edit mode is dialogtemplate</td>
        </tr>
        <tr>
            <td class="name">Batch</td>
            <td class="description">Edit mode is batch</td>
        </tr>
        <tr>
            <td class="name">InlineForm</td>
            <td class="description">Edit mode is inlineform</td>
        </tr>
        <tr>
            <td class="name">InlineTemplateForm</td>
            <td class="description">Edit mode is inlinetemplateform</td>
        </tr>
        <tr>
            <td class="name">ExternalForm</td>
            <td class="description">Edit mode is externalform</td>
        </tr>
        <tr>
            <td class="name">ExternalFormTemplate</td>
            <td class="description">Edit mode is externalformtemplate</td>
        </tr>
    </tbody>
</table>
 

 ### FileFormats
{:#enum:fileformats}








Enum for the FileFormats in diagram






#### Properties






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
<td class="name">
JPG</td>
<td class="type">string</td>
<td class="default">JPG</td>
<td class="description">Exports diagram to .jpg format</td>
</tr>
<tr>
<td class="name">
PNG</td>
<td class="type">string</td>
<td class="default">PNG</td>
<td class="description">Exports diagram to .png format</td>
</tr>
<tr>
<td class="name">
BMP</td>
<td class="type">string</td>
<td class="default">BMP</td>
<td class="description">Exports diagram to .bmp format</td>
</tr>
<tr>
<td class="name">
SVG</td>
<td class="type">string</td>
<td class="default">SVG</td>
<td class="description">Exports diagram to .svg format</td>
</tr>
</tbody>
</table>















### FilterBarMode
{:#enum:filterbarmode}

Specifies whether the Grid's filterbar mode is Immediate or OnEnter.
 
<table class="props">
<thead>
<tr>
<th>Name</th> 
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Immediate</td> 
<td class="description">Initiate filter operation on typing the filter query</td>
</tr>
<tr>
<td class="name">OnEnter</td> 
<td class="description">Initiate filter operation after Enter key is pressed</td>
</tr>
</tbody>
</table>


### FilterType
{:#enum:filtertype}
 
Specifies whether the Grid's filter type is Menu, Excel or FilterBar.
 
<table class="props">
<thead>
<tr>
<th>Name</th> 
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Menu</td> 
<td class="description">Specifies the filter type as menu.</td>
</tr>
<tr>
<td class="name">Excel</td> 
<td class="description">Specifies the filter type as excel.</td>
</tr>
<tr>
<td class="name">FilterBar</td> 
<td class="description">Specifies the filter type as filterbar.</td>
</tr>
</tbody>
</table>
 

### FitMode
{:#enum:fitmode}








Enum for the FitMode in diagram






#### Properties






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
<td class="name">
Page</td>
<td class="type">string</td>
<td class="default">page</td>
<td class="description">Fits the entire diagram into view</td>
</tr>
<tr>
<td class="name">
Width</td>
<td class="type">string</td>
<td class="default">width</td>
<td class="description">Fits the width of the diagram into the width of view</td>
</tr>
<tr>
<td class="name">
Height</td>
<td class="type">string</td>
<td class="default">height</td>
<td class="description">Fits the height of the diagram into the height of view</td>
</tr>
</tbody>
</table>















### FlowDirection
{:#enum:flowdirection}








Enum for Bullet Graph Flow Direction






#### Properties






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
<td class="name">
Forward</td>
<td class="type">string</td>
<td class="default">forward</td>
<td class="description">To set the flow direction forward.</td>
</tr>
<tr>
<td class="name">
Backward</td>
<td class="type">string</td>
<td class="default">backward</td>
<td class="description">To set the flow direction backward.</td>
</tr>
</tbody>
</table>















### FlowShapes
{:#enum:flowshapes}








Enum for the FlowShapes in diagram






#### Properties






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
<td class="name">
Process</td>
<td class="type">string</td>
<td class="default">process</td>
<td class="description">Used to specify node Shape as Process</td>
</tr>
<tr>
<td class="name">
Decision</td>
<td class="type">string</td>
<td class="default">decision</td>
<td class="description">Used to specify node Shape as Decision</td>
</tr>
<tr>
<td class="name">
Document</td>
<td class="type">string</td>
<td class="default">document</td>
<td class="description">Used to specify node Shape as Document</td>
</tr>
<tr>
<td class="name">
PreDefinedProcess</td>
<td class="type">string</td>
<td class="default">predefinedprocess</td>
<td class="description">Used to specify node Shape as PreDefinedProcess</td>
</tr>
<tr>
<td class="name">
Terminator</td>
<td class="type">string</td>
<td class="default">terminator</td>
<td class="description">Used to specify node Shape as Terminator</td>
</tr>
<tr>
<td class="name">
PaperTap</td>
<td class="type">string</td>
<td class="default">papertap</td>
<td class="description">Used to specify node Shape as PaperTap</td>
</tr>
<tr>
<td class="name">
DirectData</td>
<td class="type">string</td>
<td class="default">directdata</td>
<td class="description">Used to specify node Shape as DirectData</td>
</tr>
<tr>
<td class="name">
SequentialData</td>
<td class="type">string</td>
<td class="default">sequentialdata</td>
<td class="description">Used to specify node Shape as SequentialData</td>
</tr>
<tr>
<td class="name">
Sort</td>
<td class="type">string</td>
<td class="default">sort</td>
<td class="description">Used to specify node Shape as Sort</td>
</tr>
<tr>
<td class="name">
MultiDocument</td>
<td class="type">string</td>
<td class="default">multidocument</td>
<td class="description">Used to specify node Shape as MultiDocument</td>
</tr>
<tr>
<td class="name">
Collate</td>
<td class="type">string</td>
<td class="default">collate</td>
<td class="description">Used to specify node Shape as Collate</td>
</tr>
<tr>
<td class="name">
SummingJunction</td>
<td class="type">string</td>
<td class="default">summingjunction</td>
<td class="description">Used to specify node Shape as SummingJunction</td>
</tr>
<tr>
<td class="name">
Or</td>
<td class="type">string</td>
<td class="default">or</td>
<td class="description">Used to specify node Shape as Or</td>
</tr>
<tr>
<td class="name">
InternalStorage</td>
<td class="type">string</td>
<td class="default">internalstorage</td>
<td class="description">Used to specify node Shape as InternalStorage</td>
</tr>
<tr>
<td class="name">
Extract</td>
<td class="type">string</td>
<td class="default">extract</td>
<td class="description">Used to specify node Shape as Extract</td>
</tr>
<tr>
<td class="name">
ManualOperation</td>
<td class="type">string</td>
<td class="default">manualoperation</td>
<td class="description">Used to specify node Shape as ManualOperation</td>
</tr>
<tr>
<td class="name">
Merge</td>
<td class="type">string</td>
<td class="default">merge</td>
<td class="description">Used to specify node Shape as Merge</td>
</tr>
<tr>
<td class="name">
OffPageReference</td>
<td class="type">string</td>
<td class="default">offpagereference</td>
<td class="description">Used to specify node Shape as OffPageReference</td>
</tr>
<tr>
<td class="name">
SequentialAccessStorage</td>
<td class="type">string</td>
<td class="default">sequentialaccessstorage</td>
<td class="description">Used to specify node Shape as SequentialAccessStorage</td>
</tr>
<tr>
<td class="name">
Annotation1</td>
<td class="type">string</td>
<td class="default">annotation1</td>
<td class="description">Used to specify node Shape as Annotation1</td>
</tr>
<tr>
<td class="name">
Annotation2</td>
<td class="type">string</td>
<td class="default">annotation2</td>
<td class="description">Used to specify node Shape as Annotation2</td>
</tr>
</tbody>
</table>















### FontStyle
{:#enum:fontstyle}








Enum for Font Style






#### Properties






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
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">Normal</td>
<td class="description">To set the fontStyle Normal.</td>
</tr>
<tr>
<td class="name">
Italic</td>
<td class="type">string</td>
<td class="default">Italic</td>
<td class="description">To set the fontStyle Italic.</td>
</tr>
<tr>
<td class="name">
Oblique</td>
<td class="type">string</td>
<td class="default">Oblique</td>
<td class="description">To set the fontStyle Oblique.</td>
</tr>
</tbody>
</table>















### FontStyle
{:#enum:fontstyle}








Enum for gauge FontStyle






#### Properties






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
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">To set the FontStyle normal.</td>
</tr>
<tr>
<td class="name">
Bold</td>
<td class="type">string</td>
<td class="default">bold</td>
<td class="description">To set the FontStyle bold.</td>
</tr>
<tr>
<td class="name">
Italic</td>
<td class="type">string</td>
<td class="default">italic</td>
<td class="description">To set the FontStyle italic.</td>
</tr>
<tr>
<td class="name">
Underline</td>
<td class="type">string</td>
<td class="default">underline</td>
<td class="description">To set the FontStyle underline.</td>
</tr>
<tr>
<td class="name">
Strikeout</td>
<td class="type">string</td>
<td class="default">strikeout</td>
<td class="description">To set the FontStyle strikeout.</td>
</tr>
</tbody>
</table>















### FontStyle
{:#enum:fontstyle}








Enum for gauge FontStyle






#### Properties






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
<td class="name">
Bold</td>
<td class="type">string</td>
<td class="default">bold</td>
<td class="description">To set the FontStyle bold.</td>
</tr>
<tr>
<td class="name">
Italic</td>
<td class="type">string</td>
<td class="default">italic</td>
<td class="description">To set the FontStyle italic.</td>
</tr>
<tr>
<td class="name">
Regular</td>
<td class="type">string</td>
<td class="default">regular</td>
<td class="description">To set the FontStyle regular.</td>
</tr>
<tr>
<td class="name">
Strikeout</td>
<td class="type">string</td>
<td class="default">strikeout</td>
<td class="description">To set the FontStyle strikeout.</td>
</tr>
<tr>
<td class="name">
Underline</td>
<td class="type">string</td>
<td class="default">underline</td>
<td class="description">To set the FontStyle underline.</td>
</tr>
</tbody>
</table>















### FontStyle
{:#enum:fontstyle}








Enum for chart style of font.






#### Properties






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
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Render normal font.</td>
</tr>
<tr>
<td class="name">
Italic</td>
<td class="type">string</td>
<td class="default">italic</td>
<td class="description">Render italic font.</td>
</tr>
</tbody>
</table>















### FontWeight
{:#enum:fontweight}








Enum for Font Weight






#### Properties






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
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">Normal</td>
<td class="description">To set the fontWeight Normal.</td>
</tr>
<tr>
<td class="name">
Bold</td>
<td class="type">string</td>
<td class="default">Bold</td>
<td class="description">To set the fontWeight Bold.</td>
</tr>
<tr>
<td class="name">
Bolder</td>
<td class="type">string</td>
<td class="default">Bolder</td>
<td class="description">To set the fontWeight Bolder.</td>
</tr>
<tr>
<td class="name">
Lighter</td>
<td class="type">string</td>
<td class="default">Lighter</td>
<td class="description">To set the fontWeight Lighter.</td>
</tr>
</tbody>
</table>















### FontWeight
{:#enum:fontweight}








Enum for weight of font.






#### Properties






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
<td class="name">
Regular</td>
<td class="type">string</td>
<td class="default">regular</td>
<td class="description">Render regular font.</td>
</tr>
<tr>
<td class="name">
Bold</td>
<td class="type">string</td>
<td class="default">bold</td>
<td class="description">Render bold font.</td>
</tr>
<tr>
<td class="name">
Lighter</td>
<td class="type">string</td>
<td class="default">lighter</td>
<td class="description">Render lighter font.</td>
</tr>
</tbody>
</table>















### FooterLeftButtonStyle
{:#enum:footerleftbuttonstyle}








Enum for IOS7FooterLeftButtonStyle






#### Properties






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
<td class="name">
Auto</td>
<td class="type">string</td>
<td class="default">auto</td>
<td class="description">Enum for iOS7 auto left button style for Footer</td>
</tr>
<tr>
<td class="name">
Back</td>
<td class="type">string</td>
<td class="default">back</td>
<td class="description">Enum for iOS7 Back left button style for Footer</td>
</tr>
<tr>
<td class="name">
Header</td>
<td class="type">string</td>
<td class="default">header</td>
<td class="description">Enum for iOS7 Footer left button style for Footer</td>
</tr>
<tr>
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for iOS7 Normal left button style for Footer</td>
</tr>
</tbody>
</table>















### FooterLeftButtonStyle
{:#enum:footerleftbuttonstyle}








Enum for AndroidFooterLeftButtonStyle






#### Properties






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
<td class="name">
Auto</td>
<td class="type">string</td>
<td class="default">auto</td>
<td class="description">Enum for Android auto left button style for Footer</td>
</tr>
<tr>
<td class="name">
Back</td>
<td class="type">string</td>
<td class="default">back</td>
<td class="description">Enum for Android Back left button style for Footer</td>
</tr>
<tr>
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for Android Normal left button style for Footer</td>
</tr>
<tr>
<td class="name">
Header</td>
<td class="type">string</td>
<td class="default">header</td>
<td class="description">Enum for Android header left button style for Footer</td>
</tr>
</tbody>
</table>















### FooterLeftButtonStyle
{:#enum:footerleftbuttonstyle}








Enum for WindowsFooterLeftButtonStyle






#### Properties






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
<td class="name">
Auto</td>
<td class="type">string</td>
<td class="default">auto</td>
<td class="description">Enum for Windows auto left button style for Footer</td>
</tr>
<tr>
<td class="name">
Back</td>
<td class="type">string</td>
<td class="default">back</td>
<td class="description">Enum for Windows Back left button style for Footer</td>
</tr>
<tr>
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for Windows Normal left button style for Footer</td>
</tr>
<tr>
<td class="name">
Header</td>
<td class="type">string</td>
<td class="default">header</td>
<td class="description">Enum for Windows header left button style for Footer</td>
</tr>
</tbody>
</table>















### FooterLeftButtonStyle
{:#enum:footerleftbuttonstyle}








Enum for FlatFooterLeftButtonStyle






#### Properties






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
<td class="name">
Auto</td>
<td class="type">string</td>
<td class="default">auto</td>
<td class="description">Enum for Flat auto left button style for Footer</td>
</tr>
<tr>
<td class="name">
Back</td>
<td class="type">string</td>
<td class="default">back</td>
<td class="description">Enum for Flat Back left button style for Footer</td>
</tr>
<tr>
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for Flat Normal left button style for Footer</td>
</tr>
<tr>
<td class="name">
Header</td>
<td class="type">string</td>
<td class="default">header</td>
<td class="description">Enum for Flat Footer left button style for Footer</td>
</tr>
</tbody>
</table>















### FooterLeftButtonStyle
{:#enum:footerleftbuttonstyle}








Enum for HeaderLeftButtonStyle






#### Properties






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
<td class="name">
Back</td>
<td class="type">string</td>
<td class="default">back</td>
<td class="description">Enum for Back left button style for Footer</td>
</tr>
<tr>
<td class="name">
Header</td>
<td class="type">string</td>
<td class="default">header</td>
<td class="description">Enum for Header left button style for Footer</td>
</tr>
<tr>
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for Normal left button style for Footer</td>
</tr>
</tbody>
</table>















### FooterRightButtonStyle
{:#enum:footerrightbuttonstyle}








Enum for IOS7FooterRightButtonStyle






#### Properties






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
<td class="name">
Auto</td>
<td class="type">string</td>
<td class="default">auto</td>
<td class="description">Enum for iOS7 auto right button style for Footer</td>
</tr>
<tr>
<td class="name">
Header</td>
<td class="type">string</td>
<td class="default">header</td>
<td class="description">Enum for Footer right button style for Footer</td>
</tr>
<tr>
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for Normal right button style for Footer</td>
</tr>
</tbody>
</table>















### FooterRightButtonStyle
{:#enum:footerrightbuttonstyle}








Enum for AndroidFooterRightButtonStyle






#### Properties






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
<td class="name">
Auto</td>
<td class="type">string</td>
<td class="default">auto</td>
<td class="description">Enum for Android auto right button style for Footer</td>
</tr>
<tr>
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for Normal right button style for Footer</td>
</tr>
<tr>
<td class="name">
Header</td>
<td class="type">string</td>
<td class="default">header</td>
<td class="description">Enum for Footer right button style for Footer</td>
</tr>
</tbody>
</table>















### FooterRightButtonStyle
{:#enum:footerrightbuttonstyle}








Enum for WindowsFooterRightButtonStyle






#### Properties






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
<td class="name">
Auto</td>
<td class="type">string</td>
<td class="default">auto</td>
<td class="description">Enum for Windows auto right button style for Footer</td>
</tr>
<tr>
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for Normal right button style for Footer</td>
</tr>
<tr>
<td class="name">
Header</td>
<td class="type">string</td>
<td class="default">header</td>
<td class="description">Enum for Footer right button style for Footer</td>
</tr>
</tbody>
</table>















### FooterRightButtonStyle
{:#enum:footerrightbuttonstyle}








Enum for FlatFooterRightButtonStyle






#### Properties






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
<td class="name">
Auto</td>
<td class="type">string</td>
<td class="default">auto</td>
<td class="description">Enum for Flat auto right button style for Footer</td>
</tr>
<tr>
<td class="name">
Header</td>
<td class="type">string</td>
<td class="default">header</td>
<td class="description">Enum for Footer right button style for Footer</td>
</tr>
<tr>
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">/** Enum for Normal right button style for Footer</td>
</tr>
</tbody>
</table>















### FooterRightButtonStyle
{:#enum:footerrightbuttonstyle}








Enum for HeaderRightButtonStyle






#### Properties






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
<td class="name">
Header</td>
<td class="type">string</td>
<td class="default">header</td>
<td class="description">Enum for Header right button style for Footer</td>
</tr>
<tr>
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for Normal right button style for Footer</td>
</tr>
</tbody>
</table>















### Frame
{:#enum:frame}








Enum for gauge Frame






#### Properties






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
<td class="name">
FullCircle</td>
<td class="type">string</td>
<td class="default">fullcircle</td>
<td class="description">To set the CircularGauge Frame as fullcircle.</td>
</tr>
<tr>
<td class="name">
HalfCircle</td>
<td class="type">string</td>
<td class="default">halfcircle</td>
<td class="description">To set the CircularGauge Frame as halfcircle.</td>
</tr>
</tbody>
</table>















### FormPosition
{:#enum:formposition}
 
Specifies whether the position of Grid's edit form is TopRight or BottomLeft.
 
<table class="props">
<tr>
<th>Name</th> 
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">BottomLeft</td> 
<td class="description">Form position is bottomleft.</td>
</tr>
<tr>
<td class="name">TopRight</td> 
<td class="description">Form position is topright.</td>
</tr>
</tbody>
</table>



### FilterOperator
{:#enum:filteroperator}
 
Specifies the filter operator.

<table class="props">
<thead>
<tr>
<th>Name</th> 
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">startsWith</td> 
<td class="description">Specifies the filter operator as startswith.</td>
</tr>
<tr>
<td class="name">endsWith</td> 
<td class="description">Specifies the filter operator as endswith.</td>
</tr>
<td class="name">contains</td> 
<td class="description">Specifies the filter operator as contains.</td>
</tr>
<tr>
<td class="name">equal</td> 
<td class="description">Specifies the filter operator as equal.</td>
</tr>
<tr>
<td class="name">notEqual</td> 
<td class="description">Specifies the filter operator as notequal.</td>
</tr>
<tr>
<td class="name">greaterThan</td> 
<td class="description">Specifies the filter operator as greaterthan.</td>
</tr>
<tr>
<td class="name">greaterThanOrEqual</td> 
<td class="description">Specifies the filter operator as greaterthanorequal.</td>
</tr>
<tr>
<td class="name">lessThan</td> 
<td class="description">Specifies the filter operator as lessthan.</td>
</tr>
<tr>
<td class="name">lessThanOrEqual</td> 
<td class="description">Specifies the filter operator as Lessthanorequal.</td>
</tr>
</tbody>
</table>



### gaugePosition
{:#enum:gaugeposition}








Enum for gauge position






#### Properties






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
<td class="name">
TopLeft</td>
<td class="type">string</td>
<td class="default">topleft</td>
<td class="description">To set the gauge position topleft.</td>
</tr>
<tr>
<td class="name">
TopRight</td>
<td class="type">string</td>
<td class="default">topright</td>
<td class="description">To set the gauge position topright.</td>
</tr>
<tr>
<td class="name">
TopCenter</td>
<td class="type">string</td>
<td class="default">topcenter</td>
<td class="description">To set the gauge position topcenter.</td>
</tr>
<tr>
<td class="name">
MiddleLeft</td>
<td class="type">string</td>
<td class="default">middleleft</td>
<td class="description">To set the gauge position middleleft.</td>
</tr>
<tr>
<td class="name">
MiddleRight</td>
<td class="type">string</td>
<td class="default">middleright</td>
<td class="description">To set the gauge position middleright.</td>
</tr>
<tr>
<td class="name">
Center</td>
<td class="type">string</td>
<td class="default">center</td>
<td class="description">To set the gauge position middlecenter.</td>
</tr>
<tr>
<td class="name">
BottomLeft</td>
<td class="type">string</td>
<td class="default">bottomleft</td>
<td class="description">To set the gauge position bottomleft.</td>
</tr>
<tr>
<td class="name">
BottomRight</td>
<td class="type">string</td>
<td class="default">bottomright</td>
<td class="description">To set the gauge position bottomright.</td>
</tr>
<tr>
<td class="name">
BottomCenter</td>
<td class="type">string</td>
<td class="default">bottomcenter</td>
<td class="description">To set the gauge position bottomcenter.</td>
</tr>
</tbody>
</table>
 

### GridLines
{:#enum:gridlines}
 
Specifies whether the Grid lines is None, Horizontal, Vertical or Both.

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
<td class="description">No grid lines are displayed.</td>
</tr>
<tr>
<td class="name">Horizontal</td> 
<td class="description">Displays the horizontal grid lines only.</td>
</tr>
<tr>
<td class="name">Vertical</td> 
<td class="description">Displays the vertical grid lines only.</td>
</tr>
<tr>
<td class="name">Both</td> 
<td class="description">Displays both the horizontal and vertical grid lines.</td>
</tr>
</tbody>
</table>
 
 
### HeaderLeftButtonStyle
{:#enum:headerleftbuttonstyle}








Enum for IOS7HeaderLeftButtonStyle






#### Properties






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
<td class="name">
Auto</td>
<td class="type">string</td>
<td class="default">auto</td>
<td class="description">Enum for iOS7 Auto left button style for Header</td>
</tr>
<tr>
<td class="name">
Back</td>
<td class="type">string</td>
<td class="default">back</td>
<td class="description">/** Enum for iOS7 Back left button style for Header</td>
</tr>
<tr>
<td class="name">
Header</td>
<td class="type">string</td>
<td class="default">header</td>
<td class="description">Enum for iOS7 Header left button style for Header</td>
</tr>
<tr>
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for iOS7 Normal left button style for Header</td>
</tr>
</tbody>
</table>















### HeaderLeftButtonStyle
{:#enum:headerleftbuttonstyle}








Enum for AndroidHeaderLeftButtonStyle






#### Properties






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
<td class="name">
Auto</td>
<td class="type">string</td>
<td class="default">auto</td>
<td class="description">Enum for Android Auto left button style for Header</td>
</tr>
<tr>
<td class="name">
Back</td>
<td class="type">string</td>
<td class="default">back</td>
<td class="description">Enum for Android Back left button style for Header</td>
</tr>
<tr>
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for Android Normal left button style for Header</td>
</tr>
<tr>
<td class="name">
Header</td>
<td class="type">string</td>
<td class="default">header</td>
<td class="description">Enum for Android Header right button style for Header</td>
</tr>
</tbody>
</table>















### HeaderLeftButtonStyle
{:#enum:headerleftbuttonstyle}








Enum for WindowsHeaderLeftButtonStyle






#### Properties






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
<td class="name">
Auto</td>
<td class="type">string</td>
<td class="default">auto</td>
<td class="description">Enum for Windows Auto left button style for Header</td>
</tr>
<tr>
<td class="name">
Back</td>
<td class="type">string</td>
<td class="default">back</td>
<td class="description">Enum for Windows Back left button style for Header</td>
</tr>
<tr>
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for Windows Normal left button style for Header</td>
</tr>
<tr>
<td class="name">
Header</td>
<td class="type">string</td>
<td class="default">header</td>
<td class="description">Enum for Header left button style for Header</td>
</tr>
</tbody>
</table>















### HeaderLeftButtonStyle
{:#enum:headerleftbuttonstyle}








Enum for FlatHeaderLeftButtonStyle






#### Properties






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
<td class="name">
Auto</td>
<td class="type">string</td>
<td class="default">auto</td>
<td class="description">Enum for Flat Auto left button style for Header</td>
</tr>
<tr>
<td class="name">
Back</td>
<td class="type">string</td>
<td class="default">back</td>
<td class="description">Enum for Flat Back left button style for Header</td>
</tr>
<tr>
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for Flat Normal left button style for Header</td>
</tr>
<tr>
<td class="name">
Header</td>
<td class="type">string</td>
<td class="default">header</td>
<td class="description">Enum for Flat Header left button style for Header</td>
</tr>
</tbody>
</table>















### HeaderLeftButtonStyle
{:#enum:headerleftbuttonstyle}








Enum for HeaderLeftButtonStyle






#### Properties






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
<td class="name">
Back</td>
<td class="type">string</td>
<td class="default">back</td>
<td class="description">Enum for Back left button style for Header</td>
</tr>
<tr>
<td class="name">
Header</td>
<td class="type">string</td>
<td class="default">header</td>
<td class="description">Enum for Header left button style for Header</td>
</tr>
<tr>
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for Normal left button style for Header</td>
</tr>
</tbody>
</table>















### HeaderLeftButtonStyle
{:#enum:headerleftbuttonstyle}








Enum for headerLeftButtonStyle






#### Properties






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
<td class="name">
Back</td>
<td class="type">string</td>
<td class="default">back</td>
<td class="description">Enum for back Button Style</td>
</tr>
<tr>
<td class="name">
Header</td>
<td class="type">string</td>
<td class="default">header</td>
<td class="description">Enum for header Button Style</td>
</tr>
<tr>
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for normal Button Style</td>
</tr>
</tbody>
</table>















### HeaderRightButtonStyle
{:#enum:headerrightbuttonstyle}








Enum for IOS7HeaderRightButtonStyle






#### Properties






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
<td class="name">
Auto</td>
<td class="type">string</td>
<td class="default">auto</td>
<td class="description">Enum for iOS7 Auto right button style for Header</td>
</tr>
<tr>
<td class="name">
Header</td>
<td class="type">string</td>
<td class="default">header</td>
<td class="description">Enum for Header right button style for Header</td>
</tr>
<tr>
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for Normal right button style for Header</td>
</tr>
</tbody>
</table>















### HeaderRightButtonStyle
{:#enum:headerrightbuttonstyle}








Enum for AndroidHeaderRightButtonStyle






#### Properties






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
<td class="name">
Auto</td>
<td class="type">string</td>
<td class="default">auto</td>
<td class="description">Enum for Android Auto right button style for Header</td>
</tr>
<tr>
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for Normal right button style for Header</td>
</tr>
<tr>
<td class="name">
Header</td>
<td class="type">string</td>
<td class="default">header</td>
<td class="description">Enum for Header right button style for Header</td>
</tr>
</tbody>
</table>















### HeaderRightButtonStyle
{:#enum:headerrightbuttonstyle}








Enum for WindowsHeaderRightButtonStyle






#### Properties






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
<td class="name">
Auto</td>
<td class="type">string</td>
<td class="default">auto</td>
<td class="description">Enum for Windows Auto right button style for Header</td>
</tr>
<tr>
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for Normal right button style for Header</td>
</tr>
<tr>
<td class="name">
Header</td>
<td class="type">string</td>
<td class="default">header</td>
<td class="description">Enum for Header right button style for Header</td>
</tr>
</tbody>
</table>















### HeaderRightButtonStyle
{:#enum:headerrightbuttonstyle}








Enum for FlatHeaderRightButtonStyle






#### Properties






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
<td class="name">
Auto</td>
<td class="type">string</td>
<td class="default">auto</td>
<td class="description">Enum for Flat Auto right button style for Header</td>
</tr>
<tr>
<td class="name">
Header</td>
<td class="type">string</td>
<td class="default">header</td>
<td class="description">Enum for Header right button style for Header</td>
</tr>
<tr>
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">/** Enum for Normal right button style for Header</td>
</tr>
</tbody>
</table>















### HeaderRightButtonStyle
{:#enum:headerrightbuttonstyle}








Enum for HeaderRightButtonStyle






#### Properties






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
<td class="name">
Header</td>
<td class="type">string</td>
<td class="default">header</td>
<td class="description">Enum for Header right button style for Header</td>
</tr>
<tr>
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for Normal right button style for Header</td>
</tr>
</tbody>
</table>















### HeaderRightButtonStyle
{:#enum:headerrightbuttonstyle}








Enum for headerRightButtonStyle






#### Properties






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
<td class="name">
Header</td>
<td class="type">string</td>
<td class="default">header</td>
<td class="description">Enum for header Button Style</td>
</tr>
<tr>
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for normal Button Style</td>
</tr>
</tbody>
</table>















### HeightAdjustMode
{:#enum:heightadjustmode}








Enum for accordion height style






#### Properties






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
<td class="name">
Content</td>
<td class="type">string</td>
<td class="default">content</td>
<td class="description">Height fit to the content in the panel</td>
</tr>
<tr>
<td class="name">
Auto</td>
<td class="type">string</td>
<td class="default">auto</td>
<td class="description">Height set to the largest content in the panel</td>
</tr>
<tr>
<td class="name">
Fill</td>
<td class="type">string</td>
<td class="default">fill</td>
<td class="description">Height filled to the content of the panel</td>
</tr>
</tbody>
</table>















### HorizontalAlignment
{:#enum:horizontalalignment}








Enum for Horizontal Alignment of elements in Chart






#### Properties






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
<td class="name">
Left</td>
<td class="type">string</td>
<td class="default">left</td>
<td class="description">Set horizontal alignment as left</td>
</tr>
<tr>
<td class="name">
Middle</td>
<td class="type">string</td>
<td class="default">middle</td>
<td class="description">Set horizontal alignment as middle</td>
</tr>
<tr>
<td class="name">
Right</td>
<td class="type">string</td>
<td class="default">right</td>
<td class="description">Set horizontal alignment as right</td>
</tr>
</tbody>
</table>















### HorizontalAlignment
{:#enum:horizontalalignment}








Enum for Horizontal Alignment of elements in diagram






#### Properties






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
<td class="name">
Left</td>
<td class="type">string</td>
<td class="default">left</td>
<td class="description">Used to align text horizontally on left side of node/connector</td>
</tr>
<tr>
<td class="name">
Center</td>
<td class="type">string</td>
<td class="default">center</td>
<td class="description">Used to align text horizontally on center of node/connector</td>
</tr>
<tr>
<td class="name">
Right</td>
<td class="type">string</td>
<td class="default">right</td>
<td class="description">Used to align text horizontally on right side of node/connector</td>
</tr>
</tbody>
</table>















### HorizontalTextAlignment
{:#enum:horizontaltextalignment}








Enum for Horizontal Alignment of text in Chart






#### Properties






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
<td class="name">
Near</td>
<td class="type">string</td>
<td class="default">near</td>
<td class="description">Sets horizontal alignment of text to near</td>
</tr>
<tr>
<td class="name">
Center</td>
<td class="type">string</td>
<td class="default">center</td>
<td class="description">Sets horizontal alignment of text to center</td>
</tr>
<tr>
<td class="name">
Far</td>
<td class="type">string</td>
<td class="default">far</td>
<td class="description">Sets horizontal alignment of text to far</td>
</tr>
</tbody>
</table>















### HourFormat
{:#enum:hourformat}








Enum for Hour format






#### Properties






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
<td class="name">
TwentyFour</td>
<td class="type">string</td>
<td class="default">twentyfour</td>
<td class="description">Enum for twentyfour hourformat</td>
</tr>
<tr>
<td class="name">
Twelve</td>
<td class="type">string</td>
<td class="default">twelve</td>
<td class="description">Enum for twentyfour hourformat</td>
</tr>
</tbody>
</table>















 
 

### IconName
{:#enum:iconname}








Enum for toolbar icon name






#### Properties






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
<td class="name">
Add</td>
<td class="type">string</td>
<td class="default">Add</td>
<td class="description">Enum for Add toolbar icon</td>
</tr>
<tr>
<td class="name">
Back</td>
<td class="type">string</td>
<td class="default">Back</td>
<td class="description">Enum for Back toolbar icon</td>
</tr>
<tr>
<td class="name">
Bookmark</td>
<td class="type">string</td>
<td class="default">Bookmark</td>
<td class="description">Enum for Bookmark toolbar icon</td>
</tr>
<tr>
<td class="name">
Close</td>
<td class="type">string</td>
<td class="default">Close</td>
<td class="description">Enum for Close toolbar icon</td>
</tr>
<tr>
<td class="name">
Compose</td>
<td class="type">string</td>
<td class="default">Compose</td>
<td class="description">Enum for Compose toolbar icon</td>
</tr>
<tr>
<td class="name">
Copy</td>
<td class="type">string</td>
<td class="default">Copy</td>
<td class="description">Enum for Copy toolbar icon</td>
</tr>
<tr>
<td class="name">
Cut</td>
<td class="type">string</td>
<td class="default">Cut</td>
<td class="description">Enum for Cut toolbar icon</td>
</tr>
<tr>
<td class="name">
Delete</td>
<td class="type">string</td>
<td class="default">Delete</td>
<td class="description">Enum for Delete toolbar icon</td>
</tr>
<tr>
<td class="name">
Done</td>
<td class="type">string</td>
<td class="default">Done</td>
<td class="description">Enum for Done toolbar icon</td>
</tr>
<tr>
<td class="name">
Edit</td>
<td class="type">string</td>
<td class="default">Edit</td>
<td class="description">Enum for Edit toolbar icon</td>
</tr>
<tr>
<td class="name">
Mail</td>
<td class="type">string</td>
<td class="default">Mail</td>
<td class="description">Enum for Mail toolbar icon</td>
</tr>
<tr>
<td class="name">
Next</td>
<td class="type">string</td>
<td class="default">Next</td>
<td class="description">Enum for Next toolbar icon</td>
</tr>
<tr>
<td class="name">
Refresh</td>
<td class="type">string</td>
<td class="default">Refresh</td>
<td class="description">Enum for Refresh toolbar icon</td>
</tr>
<tr>
<td class="name">
Overflow</td>
<td class="type">string</td>
<td class="default">Overflow</td>
<td class="description">Enum for Overflow toolbar icon</td>
</tr>
<tr>
<td class="name">
Paste</td>
<td class="type">string</td>
<td class="default">Paste</td>
<td class="description">Enum for Paste toolbar icon</td>
</tr>
<tr>
<td class="name">
Reply</td>
<td class="type">string</td>
<td class="default">Reply</td>
<td class="description">Enum for Reply toolbar icon</td>
</tr>
<tr>
<td class="name">
Save</td>
<td class="type">string</td>
<td class="default">Save</td>
<td class="description">Enum for Save toolbar icon</td>
</tr>
<tr>
<td class="name">
Search</td>
<td class="type">string</td>
<td class="default">Search</td>
<td class="description">Enum for Search toolbar icon</td>
</tr>
<tr>
<td class="name">
Settings</td>
<td class="type">string</td>
<td class="default">Settings</td>
<td class="description">Enum for Settings toolbar icon</td>
</tr>
<tr>
<td class="name">
Share</td>
<td class="type">string</td>
<td class="default">Share</td>
<td class="description">Enum for Share toolbar icon</td>
</tr>
</tbody>
</table>















### ImagePosition
{:#enum:imageposition}








Enum for ImagePosition






#### Properties






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
<td class="name">
Left</td>
<td class="type">string</td>
<td class="default">left</td>
<td class="description">Enum for image at left position</td>
</tr>
<tr>
<td class="name">
Right</td>
<td class="type">string</td>
<td class="default">right</td>
<td class="description">Enum for image at right position</td>
</tr>
</tbody>
</table>















### ImagePosition
{:#enum:imageposition}








Enum for Tile ImagePosition






#### Properties






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
<td class="name">
Center</td>
<td class="type">string</td>
<td class="default">center</td>
<td class="description">Enum for center position of tile image</td>
</tr>
<tr>
<td class="name">
Top</td>
<td class="type">string</td>
<td class="default">top</td>
<td class="description">Enum for top position of tile image</td>
</tr>
<tr>
<td class="name">
Bottom</td>
<td class="type">string</td>
<td class="default">bottom</td>
<td class="description">Enum for bottom position of tile image</td>
</tr>
<tr>
<td class="name">
Right</td>
<td class="type">string</td>
<td class="default">right</td>
<td class="description">Enum for right position of tile image</td>
</tr>
<tr>
<td class="name">
Left</td>
<td class="type">string</td>
<td class="default">left</td>
<td class="description">Enum for left position of tile image</td>
</tr>
<tr>
<td class="name">
TopLeft</td>
<td class="type">string</td>
<td class="default">topleft</td>
<td class="description">Enum for topleft position of tile image</td>
</tr>
<tr>
<td class="name">
TopRight</td>
<td class="type">string</td>
<td class="default">topright</td>
<td class="description">Enum for topright position of tile image</td>
</tr>
<tr>
<td class="name">
BottomRight</td>
<td class="type">string</td>
<td class="default">bottomright</td>
<td class="description">Enum for bottomright position of tile image</td>
</tr>
<tr>
<td class="name">
BottomLeft</td>
<td class="type">string</td>
<td class="default">bottomleft</td>
<td class="description">Enum for bottomleft position of tile image</td>
</tr>
<tr>
<td class="name">
Fill</td>
<td class="type">string</td>
<td class="default">fill</td>
<td class="description">Enum for fill position of tile image</td>
</tr>
</tbody>
</table>















### IndicatorType
{:#enum:indicatortype}








Enum for gauge IndicatorType






#### Properties






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
<td class="name">
Rectangle</td>
<td class="type">string</td>
<td class="default">rectangle</td>
<td class="description">To set the IndicatorType rectangle.</td>
</tr>
<tr>
<td class="name">
Circle</td>
<td class="type">string</td>
<td class="default">circle</td>
<td class="description">To set the IndicatorType circle.</td>
</tr>
<tr>
<td class="name">
RoundedRectangle</td>
<td class="type">string</td>
<td class="default">roundedrectangle</td>
<td class="description">To set the IndicatorType roundedrectangle.</td>
</tr>
<tr>
<td class="name">
Text</td>
<td class="type">string</td>
<td class="default">text</td>
<td class="description">To set the IndicatorType Text.</td>
</tr>
<tr>
<td class="name">
Image</td>
<td class="type">string</td>
<td class="default">image</td>
<td class="description">To set the IndicatorType Text.</td>
</tr>
</tbody>
</table>















### IndicatorType
{:#enum:indicatortype}








Enum for gauge IndicatorType






#### Properties






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
<td class="name">
Rectangle</td>
<td class="type">string</td>
<td class="default">rectangle</td>
<td class="description">To set the IndicatorType rectangle.</td>
</tr>
<tr>
<td class="name">
Circle</td>
<td class="type">string</td>
<td class="default">circle</td>
<td class="description">To set the IndicatorType circle.</td>
</tr>
<tr>
<td class="name">
RoundedRectangle</td>
<td class="type">string</td>
<td class="default">roundedrectangle</td>
<td class="description">To set the IndicatorType roundedrectangle.</td>
</tr>
<tr>
<td class="name">
Text</td>
<td class="type">string</td>
<td class="default">text</td>
<td class="description">To set the IndicatorType text.</td>
</tr>
</tbody>
</table>















### IndicatorsType
{:#enum:indicatorstype}








Enum for type of indicator in Chart






#### Properties






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
<td class="name">
RSI</td>
<td class="type">string</td>
<td class="default">RSI</td>
<td class="description">Set indicator type as RSI.</td>
</tr>
<tr>
<td class="name">
Momentum</td>
<td class="type">string</td>
<td class="default">Momentum</td>
<td class="description">Set indicator type as Momentum.</td>
</tr>
<tr>
<td class="name">
Bollingerband</td>
<td class="type">string</td>
<td class="default">Bollingerband</td>
<td class="description">Set indicator type as Bollingerband.</td>
</tr>
<tr>
<td class="name">
Accumulationdistribution</td>
<td class="type">string</td>
<td class="default">Accumulationdistribution</td>
<td class="description">Set indicator type as Accumulationdistribution.</td>
</tr>
<tr>
<td class="name">
EMA</td>
<td class="type">string</td>
<td class="default">EMA</td>
<td class="description">Set indicator type as EMA.</td>
</tr>
<tr>
<td class="name">
SMA</td>
<td class="type">string</td>
<td class="default">SMA</td>
<td class="description">Set indicator type as SMA.</td>
</tr>
<tr>
<td class="name">
Stochastic</td>
<td class="type">string</td>
<td class="default">Stochastic</td>
<td class="description">Set indicator type as Stochastic.</td>
</tr>
<tr>
<td class="name">
ATR</td>
<td class="type">string</td>
<td class="default">ATR</td>
<td class="description">Set indicator type as ATR.</td>
</tr>
<tr>
<td class="name">
MACD</td>
<td class="type">string</td>
<td class="default">MACD</td>
<td class="description">Set indicator type as MACD.</td>
</tr>
<tr>
<td class="name">
TMA</td>
<td class="type">string</td>
<td class="default">TMA</td>
<td class="description">Set indicator type as TMA.</td>
</tr>
</tbody>
</table>















### IntervalType
{:#enum:intervaltype}








Enum for chart interval type.






#### Properties






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
<td class="name">
Days</td>
<td class="type">string</td>
<td class="default">days</td>
<td class="description">Sets chart interval type to days.</td>
</tr>
<tr>
<td class="name">
Hours</td>
<td class="type">string</td>
<td class="default">hours</td>
<td class="description">Sets chart interval type to hours.</td>
</tr>
<tr>
<td class="name">
Seconds</td>
<td class="type">string</td>
<td class="default">seconds</td>
<td class="description">Sets chart interval type to seconds.</td>
</tr>
<tr>
<td class="name">
Milliseconds</td>
<td class="type">string</td>
<td class="default">milliseconds</td>
<td class="description">Sets chart interval type to milliseconds.</td>
</tr>
<tr>
<td class="name">
Minutes</td>
<td class="type">string</td>
<td class="default">minutes</td>
<td class="description">Sets chart interval type to minutes.</td>
</tr>
<tr>
<td class="name">
Months</td>
<td class="type">string</td>
<td class="default">months</td>
<td class="description">Sets chart interval type to months.</td>
</tr>
<tr>
<td class="name">
Years</td>
<td class="type">string</td>
<td class="default">years</td>
<td class="description">Sets chart interval type to years.</td>
</tr>
</tbody>
</table>















### ItemsLayoutMode
{:#enum:itemslayoutmode}








Enum for TreeMap items layout mode






#### Properties






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
<td class="name">
Squarified</td>
<td class="type">string</td>
<td class="default">squarified</td>
<td class="description"></td>
</tr>
<tr>
<td class="name">
SliceAndDiceHorizontal</td>
<td class="type">string</td>
<td class="default">sliceanddicehorizontal</td>
<td class="description"></td>
</tr>
<tr>
<td class="name">
SliceAndDiceVertical</td>
<td class="type">string</td>
<td class="default">sliceanddicevertical</td>
<td class="description"></td>
</tr>
<tr>
<td class="name">
SliceAndDiceAuto</td>
<td class="type">string</td>
<td class="default">sliceanddiceauto</td>
<td class="description"></td>
</tr>
</tbody>
</table>











### Keys
{:#enum:keys}

Enum for Keys in diagram.

#### Properties

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th class="last">Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">None</td>
            <td class="description">No key pressed.</td>
        </tr>
        <tr>
            <td class="name">A</td>
            <td class="description">The A key.</td>
        </tr>
        <tr>
            <td class="name">B</td>
            <td class="description">The B key.</td>
        </tr>
        <tr>
            <td class="name">C</td>
            <td class="description">The C key.</td>
        </tr>
        <tr>
            <td class="name">D</td>
            <td class="description">The D Key.</td>
        </tr>
        <tr>
            <td class="name">E</td>
            <td class="description">The E key.</td>
        </tr>
        <tr>
            <td class="name">F</td>
            <td class="description">The F key.</td>
        </tr>
        <tr>
            <td class="name">G</td>
            <td class="description">The G key.</td>
        </tr>
        <tr>
            <td class="name">H</td>
            <td class="description">The H Key.</td>
        </tr>
        <tr>
            <td class="name">I</td>
            <td class="description">The I key.</td>
        </tr>
        <tr>
            <td class="name">J</td>
            <td class="description">The J key.</td>
        </tr>
        <tr>
            <td class="name">K</td>
            <td class="description">The K key.</td>
        </tr>
        <tr>
            <td class="name">L</td>
            <td class="description">The L Key.</td>
        </tr>
        <tr>
            <td class="name">M</td>
            <td class="description">The M key.</td>
        </tr>
        <tr>
            <td class="name">N</td>
            <td class="description">The N key.</td>
        </tr>
        <tr>
            <td class="name">O</td>
            <td class="description">The O key.</td>
        </tr>
        <tr>
            <td class="name">P</td>
            <td class="description">The P Key.</td>
        </tr>
        <tr>
            <td class="name">Q</td>
            <td class="description">The Q key.</td>
        </tr>
        <tr>
            <td class="name">R</td>
            <td class="description">The R key.</td>
        </tr>
        <tr>
            <td class="name">S</td>
            <td class="description">The S key.</td>
        </tr>
        <tr>
            <td class="name">T</td>
            <td class="description">The T Key.</td>
        </tr>
        <tr>
            <td class="name">U</td>
            <td class="description">The U key.</td>
        </tr>
        <tr>
            <td class="name">V</td>
            <td class="description">The V key.</td>
        </tr>
        <tr>
            <td class="name">W</td>
            <td class="description">The W key.</td>
        </tr>
        <tr>
            <td class="name">X</td>
            <td class="description">The X key.</td>
        </tr>
        <tr>
            <td class="name">Y</td>
            <td class="description">The Y key.</td>
        </tr>
        <tr>
            <td class="name">Z</td>
            <td class="description">The Z key.</td>
        </tr>
        <tr>
            <td class="name">Number0</td>
            <td class="description">The 0 key.</td>
        </tr>
        <tr>
            <td class="name">Number1</td>
            <td class="description">The 1 key.</td>
        </tr>
        <tr>
            <td class="name">Number2</td>
            <td class="description">The 2 key.</td>
        </tr>
        <tr>
            <td class="name">Number3</td>
            <td class="description">The 3 key.</td>
        </tr>
        <tr>
            <td class="name">Number4</td>
            <td class="description">The 4 key.</td>
        </tr>
        <tr>
            <td class="name">Number5</td>
            <td class="description">The 5 key.</td>
        </tr>
        <tr>
            <td class="name">Number6</td>
            <td class="description">The 6 key.</td>
        </tr>
        <tr>
            <td class="name">Number7</td>
            <td class="description">The 7 key.</td>
        </tr>
        <tr>
            <td class="name">Number8</td>
            <td class="description">The 8 key.</td>
        </tr>
        <tr>
            <td class="name">Number9</td>
            <td class="description">The 9 key.</td>
        </tr>
        <tr>
            <td class="name">Left</td>
            <td class="description">The LEFT ARROW key.</td>
        </tr>
        <tr>
            <td class="name">Up</td>
            <td class="description">The UP ARROW key.</td>
        </tr>
        <tr>
            <td class="name">Right</td>
            <td class="description">The RIGHT ARROW key.</td>
        </tr>
        <tr>
            <td class="name">Down</td>
            <td class="description">The DOWN ARROW key.</td>
        </tr>
        <tr>
            <td class="name">Escape</td>
            <td class="description">The ESC key.</td>
        </tr>
        <tr>
            <td class="name">Delete</td>
            <td class="description">The DEL key.</td>
        </tr>
        <tr>
            <td class="name">Tab</td>
            <td class="description">The TAB key.</td>
        </tr>
        <tr>
            <td class="name">Enter</td>
            <td class="description">The ENTER key.</td>
        </tr>
    </tbody>
</table>

### KeyModifiers
{:#enum:keymodifiers}

Enum for KeyModifiers in diagram.

#### Properties

<table class="props">
    <thead>
        <tr>
            <th>Name</th>
            <th class="last">Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">None</td>
            <td class="description">No modifiers are pressed.</td>
        </tr>
        <tr>
            <td class="name">Alt</td>
            <td class="description">The ALT key.</td>
        </tr>
        <tr>
            <td class="name">Control</td>
            <td class="description">The CTRL key.</td>
        </tr>
        <tr>
            <td class="name">Shift</td>
            <td class="description">The SHIFT key.</td>
        </tr>
    </tbody>
</table>

### LabelEditMode
{:#enum:labeleditmode}








Enum for LabelEditMode of text in diagram






#### Properties






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
<td class="name">
Edit</td>
<td class="type">string</td>
<td class="default">edit</td>
<td class="description">Used to set label edit mode as edit</td>
</tr>
<tr>
<td class="name">
View</td>
<td class="type">string</td>
<td class="default">view</td>
<td class="description">Used to set label edit mode as view</td>
</tr>
</tbody>
</table>















### LabelIntersectAction
{:#enum:labelintersectaction}








Enum for chart labelIntersectAction.






#### Properties






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
<td class="name">
None</td>
<td class="type">string</td>
<td class="default">none</td>
<td class="description">No action is made on intersection of labels.</td>
</tr>
<tr>
<td class="name">
Rotate90</td>
<td class="type">string</td>
<td class="default">rotate90</td>
<td class="description">Rotate the labels to 90 degree on intersect.</td>
</tr>
<tr>
<td class="name">
Rotate45</td>
<td class="type">string</td>
<td class="default">rotate45</td>
<td class="description">Rotate the labels to 45 degree on intersect.</td>
</tr>
<tr>
<td class="name">
Wrap</td>
<td class="type">string</td>
<td class="default">wrap</td>
<td class="description">Wrap the label to multiple lines on intersect.</td>
</tr>
<tr>
<td class="name">
Trim</td>
<td class="type">string</td>
<td class="default">trim</td>
<td class="description">Trim the text and display whole text on mouse over.</td>
</tr>
<tr>
<td class="name">
Hide</td>
<td class="type">string</td>
<td class="default">hide</td>
<td class="description">Hide the label which intersect.</td>
</tr>
<tr>
<td class="name">
MultipleRows</td>
<td class="type">string</td>
<td class="default">multipleRows</td>
<td class="description">Labels are placed on another row on intersect.</td>
</tr>
</tbody>
</table>















### LabelPlacement
{:#enum:labelplacement}








Enum for Bullet Graph label placement






#### Properties






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
<td class="name">
Inside</td>
<td class="type">string</td>
<td class="default">inside</td>
<td class="description">support for placing labels inside scale.</td>
</tr>
<tr>
<td class="name">
Outside</td>
<td class="type">string</td>
<td class="default">outside</td>
<td class="description">support for placing labels outside scale.</td>
</tr>
</tbody>
</table>















### LabelPlacement
{:#enum:labelplacement}








Enum for gauge LabelPlacement






#### Properties






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
<td class="name">
Near</td>
<td class="type">string</td>
<td class="default">near</td>
<td class="description">To set the LabelPlacement near.</td>
</tr>
<tr>
<td class="name">
Far</td>
<td class="type">string</td>
<td class="default">far</td>
<td class="description">To set the LabelPlacement far.</td>
</tr>
<tr>
<td class="name">
Center</td>
<td class="type">string</td>
<td class="default">center</td>
<td class="description">To set the LabelPlacement center.</td>
</tr>
</tbody>
</table>















### LabelPlacement
{:#enum:labelplacement}








Enum for gauge LabelPlacement






#### Properties






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
<td class="name">
Near</td>
<td class="type">string</td>
<td class="default">near</td>
<td class="description">To set the LabelPlacement near.</td>
</tr>
<tr>
<td class="name">
Far</td>
<td class="type">string</td>
<td class="default">far</td>
<td class="description">To set the LabelPlacement far.</td>
</tr>
<tr>
<td class="name">
Center</td>
<td class="type">string</td>
<td class="default">center</td>
<td class="description">To set the LabelPlacement center.</td>
</tr>
</tbody>
</table>















### LabelPlacement
{:#enum:labelplacement}








Enum for chart labelPlacement.






#### Properties






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
<td class="name">
BetweenTicks</td>
<td class="type">string</td>
<td class="default">betweenTicks</td>
<td class="description">specifies the placement of labels between the ticks.</td>
</tr>
<tr>
<td class="name">
OnTicks</td>
<td class="type">string</td>
<td class="default">onTicks</td>
<td class="description">specifies the placement of labels on the ticks.</td>
</tr>
</tbody>
</table>















### LabelPosition
{:#enum:labelposition}








Enum for Bullet Graph Label Position






#### Properties






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
<td class="name">
Below</td>
<td class="type">string</td>
<td class="default">below</td>
<td class="description">To set the label position below.</td>
</tr>
<tr>
<td class="name">
Above</td>
<td class="type">string</td>
<td class="default">above</td>
<td class="description">To set the label position above.</td>
</tr>
</tbody>
</table>















### LabelPosition
{:#enum:labelposition}








Enum for label position.






#### Properties






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
<td class="name">
Inside</td>
<td class="type">string</td>
<td class="default">inside</td>
<td class="description">Support for changing the labelPosition to inside.</td>
</tr>
<tr>
<td class="name">
Outside</td>
<td class="type">string</td>
<td class="default">outside</td>
<td class="description">Support for changing the labelPosition to outside.</td>
</tr>
</tbody>
</table>















### LabelSize
{:#enum:labelsize}








Enum for Map Label size






#### Properties






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
<td class="name">
Fixed</td>
<td class="type">string</td>
<td class="default">fixed</td>
<td class="description">support for label size fixed.</td>
</tr>
<tr>
<td class="name">
Default</td>
<td class="type">string</td>
<td class="default">default</td>
<td class="description">support for label size default.</td>
</tr>
</tbody>
</table>















### LabelType
{:#enum:labeltype}








Enum for gauge LabelType






#### Properties






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
<td class="name">
Major</td>
<td class="type">string</td>
<td class="default">major</td>
<td class="description">To set the LabelType major.</td>
</tr>
<tr>
<td class="name">
Minor</td>
<td class="type">string</td>
<td class="default">minor</td>
<td class="description">To set the LabelType minor.</td>
</tr>
</tbody>
</table>















### LabelType
{:#enum:labeltype}








Enum for gauge LabelType






#### Properties






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
<td class="name">
Major</td>
<td class="type">string</td>
<td class="default">major</td>
<td class="description">To set the LabelType major.</td>
</tr>
<tr>
<td class="name">
Minor</td>
<td class="type">string</td>
<td class="default">minor</td>
<td class="description">To set the LabelType minor.</td>
</tr>
</tbody>
</table>















### LayerType
{:#enum:layertype}








Enum for Map LayerType






#### Properties






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
<td class="name">
Geometry</td>
<td class="type">string</td>
<td class="default">geometry</td>
<td class="description">support for layer type geometry.</td>
</tr>
<tr>
<td class="name">
OSM</td>
<td class="type">string</td>
<td class="default">osm</td>
<td class="description">support for layer type osm.</td>
</tr>
<tr>
<td class="name">
Bing</td>
<td class="type">string</td>
<td class="default">bing</td>
<td class="description">support for layer type bing.</td>
</tr>
</tbody>
</table>















### LayoutOrientations
{:#enum:layoutorientations}








Enum for LayoutOrientations in diagram






#### Properties






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
<td class="name">
TopToBottom</td>
<td class="type">string</td>
<td class="default">toptobottom</td>
<td class="description">Used to set LayoutOrientation from top to bottom</td>
</tr>
<tr>
<td class="name">
BottomToTop</td>
<td class="type">string</td>
<td class="default">bottomtotop</td>
<td class="description">Used to set LayoutOrientation from bottom to top</td>
</tr>
<tr>
<td class="name">
LeftToRight</td>
<td class="type">string</td>
<td class="default">lefttoright</td>
<td class="description">Used to set LayoutOrientation from left to right</td>
</tr>
<tr>
<td class="name">
RightToLeft</td>
<td class="type">string</td>
<td class="default">righttoleft</td>
<td class="description">Used to set LayoutOrientation from right to left</td>
</tr>
</tbody>
</table>















### LayoutTypes
{:#enum:layouttypes}








Enum for LayoutTypes in diagram






#### Properties






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
<td class="name">
None</td>
<td class="type">string</td>
<td class="default">none</td>
<td class="description">Used not to set any specific layout</td>
</tr>
<tr>
<td class="name">
HierarchicalTree</td>
<td class="type">string</td>
<td class="default">hierarchicaltree</td>
<td class="description">Used to set layout type as hierarchical layout</td>
</tr>
<tr>
<td class="name">
OrganizationalChart</td>
<td class="type">string</td>
<td class="default">organizationalchart</td>
<td class="description">Used to set layout type as organnizational chart</td>
</tr>
</tbody>
</table>















### LegendIcons
{:#enum:legendicons}








Enum for Map legend icons






#### Properties






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
<td class="name">
Rectangle</td>
<td class="type">string</td>
<td class="default">rectangle</td>
<td class="description">support for legend icon rectangle.</td>
</tr>
<tr>
<td class="name">
Circle</td>
<td class="type">string</td>
<td class="default">circle</td>
<td class="description">support for legend icon circle.</td>
</tr>
</tbody>
</table>















### LegendMode
{:#enum:legendmode}








Enum for Map Legend mode






#### Properties






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
<td class="name">
Default</td>
<td class="type">string</td>
<td class="default">default</td>
<td class="description">support for legend mode default.</td>
</tr>
<tr>
<td class="name">
Interactive</td>
<td class="type">string</td>
<td class="default">interactive</td>
<td class="description">support for legend mode interactive.</td>
</tr>
</tbody>
</table>















### LegendType
{:#enum:legendtype}








Enum for Map Legend type






#### Properties






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
<td class="name">
Layers</td>
<td class="type">string</td>
<td class="default">layers</td>
<td class="description">support for Legend type layers.</td>
</tr>
<tr>
<td class="name">
Bubbles</td>
<td class="type">string</td>
<td class="default">bubbles</td>
<td class="description">support for Legend type bubbles.</td>
</tr>
</tbody>
</table>















### LineCap
{:#enum:linecap}








Enum for linecap.






#### Properties






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
<td class="name">
Butt</td>
<td class="type">string</td>
<td class="default">butt</td>
<td class="description">Sets the linecap as butt.</td>
</tr>
<tr>
<td class="name">
Round</td>
<td class="type">string</td>
<td class="default">round</td>
<td class="description">Sets the linecap as round.</td>
</tr>
<tr>
<td class="name">
Square</td>
<td class="type">string</td>
<td class="default">square</td>
<td class="description">Sets the linecap as square.</td>
</tr>
</tbody>
</table>















### LineJoin
{:#enum:linejoin}








Enum for line join.






#### Properties






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
<td class="name">
Round</td>
<td class="type">string</td>
<td class="default">round</td>
<td class="description">Sets the lineJoin to round.</td>
</tr>
<tr>
<td class="name">
Bevel</td>
<td class="type">string</td>
<td class="default">bevel</td>
<td class="description">Sets the lineJoin to bevel.</td>
</tr>
<tr>
<td class="name">
Miter</td>
<td class="type">string</td>
<td class="default">miter</td>
<td class="description">Sets the lineJoin to miter.</td>
</tr>
</tbody>
</table>















### LiveTileType
{:#enum:livetiletype}








Enum for LiveTileType






#### Properties






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
<td class="name">
Flip</td>
<td class="type">string</td>
<td class="default">flip</td>
<td class="description">Enum for flip type of livetile</td>
</tr>
<tr>
<td class="name">
Slide</td>
<td class="type">string</td>
<td class="default">slide</td>
<td class="description">Enum for slide type of livetile</td>
</tr>
<tr>
<td class="name">
Carousel</td>
<td class="type">string</td>
<td class="default">carousel</td>
<td class="description">Enum for carousel type of livetile</td>
</tr>
</tbody>
</table>















### MACDType
{:#enum:macdtype}








Enum for MACDType






#### Properties






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
<td class="name">
Line</td>
<td class="type">string</td>
<td class="default">line</td>
<td class="description">Enum for MACD line</td>
</tr>
<tr>
<td class="name">
Histogram</td>
<td class="type">string</td>
<td class="default">histogram</td>
<td class="description">Enum for MACD Histogram</td>
</tr>
<tr>
<td class="name">
Both</td>
<td class="type">string</td>
<td class="default">both</td>
<td class="description">Enum for both MACD line and histogram</td>
</tr>
</tbody>
</table>















### MarkerType
{:#enum:markertype}








Enum for gauge MarkerType






#### Properties






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
<td class="name">
Rectangle</td>
<td class="type">string</td>
<td class="default">rectangle</td>
<td class="description">To set the MarkerType rectangle.</td>
</tr>
<tr>
<td class="name">
Triangle</td>
<td class="type">string</td>
<td class="default">triangle</td>
<td class="description">To set the MarkerType triangle.</td>
</tr>
<tr>
<td class="name">
Ellipse</td>
<td class="type">string</td>
<td class="default">ellipse</td>
<td class="description">To set the MarkerType ellipse.</td>
</tr>
<tr>
<td class="name">
Diamond</td>
<td class="type">string</td>
<td class="default">diamond</td>
<td class="description">To set the MarkerType diamond.</td>
</tr>
<tr>
<td class="name">
Pentagon</td>
<td class="type">string</td>
<td class="default">pentagon</td>
<td class="description">To set the MarkerType pentagon.</td>
</tr>
<tr>
<td class="name">
Circle</td>
<td class="type">string</td>
<td class="default">circle</td>
<td class="description">To set the MarkerType circle.</td>
</tr>
<tr>
<td class="name">
Slider</td>
<td class="type">string</td>
<td class="default">slider</td>
<td class="description">To set the MarkerType slider.</td>
</tr>
<tr>
<td class="name">
Pointer</td>
<td class="type">string</td>
<td class="default">pointer</td>
<td class="description">To set the MarkerType pointer.</td>
</tr>
<tr>
<td class="name">
Wedge</td>
<td class="type">string</td>
<td class="default">wedge</td>
<td class="description">To set the MarkerType wedge.</td>
</tr>
<tr>
<td class="name">
Trapezoid</td>
<td class="type">string</td>
<td class="default">trapezoid</td>
<td class="description">To set the MarkerType trapezoid.</td>
</tr>
<tr>
<td class="name">
RoundedRectangle</td>
<td class="type">string</td>
<td class="default">roundedrectangle</td>
<td class="description">To set the MarkerType roundedrectangle.</td>
</tr>
<tr>
<td class="name">
Image</td>
<td class="type">string</td>
<td class="default">image</td>
<td class="description">To set the MarkerType image.</td>
</tr>
</tbody>
</table>















### MarkerType
{:#enum:markertype}








Enum for gauge MarkerType






#### Properties






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
<td class="name">
Rectangle</td>
<td class="type">string</td>
<td class="default">rectangle</td>
<td class="description">To set the MarkerType rectangle.</td>
</tr>
<tr>
<td class="name">
Triangle</td>
<td class="type">string</td>
<td class="default">triangle</td>
<td class="description">To set the MarkerType triangle.</td>
</tr>
<tr>
<td class="name">
Ellipse</td>
<td class="type">string</td>
<td class="default">ellipse</td>
<td class="description">To set the MarkerType ellipse.</td>
</tr>
<tr>
<td class="name">
Diamond</td>
<td class="type">string</td>
<td class="default">diamond</td>
<td class="description">To set the MarkerType diamond.</td>
</tr>
<tr>
<td class="name">
Pentagon</td>
<td class="type">string</td>
<td class="default">pentagon</td>
<td class="description">To set the MarkerType pentagon.</td>
</tr>
<tr>
<td class="name">
Circle</td>
<td class="type">string</td>
<td class="default">circle</td>
<td class="description">To set the MarkerType circle.</td>
</tr>
<tr>
<td class="name">
Star</td>
<td class="type">string</td>
<td class="default">star</td>
<td class="description">To set the MarkerType star.</td>
</tr>
<tr>
<td class="name">
Slider</td>
<td class="type">string</td>
<td class="default">slider</td>
<td class="description">To set the MarkerType slider.</td>
</tr>
<tr>
<td class="name">
Pointer</td>
<td class="type">string</td>
<td class="default">pointer</td>
<td class="description">To set the MarkerType pointer.</td>
</tr>
<tr>
<td class="name">
Wedge</td>
<td class="type">string</td>
<td class="default">wedge</td>
<td class="description">To set the MarkerType wedge.</td>
</tr>
<tr>
<td class="name">
Trapezoid</td>
<td class="type">string</td>
<td class="default">trapezoid</td>
<td class="description">To set the MarkerType trapezoid.</td>
</tr>
<tr>
<td class="name">
RoundedRectangle</td>
<td class="type">string</td>
<td class="default">roundedrectangle</td>
<td class="description">To set the MarkerType roundedrectangle.</td>
</tr>
</tbody>
</table>















### Mode
{:#enum:mode}








Enum for highlighting and selection mode in Chart






#### Properties






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
<td class="name">
Series</td>
<td class="type">string</td>
<td class="default">series</td>
<td class="description">Specifies entire series should be highlighted or selected</td>
</tr>
<tr>
<td class="name">
Point</td>
<td class="type">string</td>
<td class="default">point</td>
<td class="description">Specifies data point should be highlighted or selected</td>
</tr>
</tbody>
</table>















### Mode
{:#enum:mode}








Enum for mode






#### Properties






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
<td class="name">
Search</td>
<td class="type">string</td>
<td class="default">search</td>
<td class="description">Enum for Search mode</td>
</tr>
<tr>
<td class="name">
Default</td>
<td class="type">string</td>
<td class="default">default</td>
<td class="description">Enum for Default mode</td>
</tr>
</tbody>
</table>















### Mode
{:#enum:mode}








Enum for mode






#### Properties






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
<td class="name">
Alert</td>
<td class="type">string</td>
<td class="default">alert</td>
<td class="description">Enum for alert mode dialog</td>
</tr>
<tr>
<td class="name">
Confirm</td>
<td class="type">string</td>
<td class="default">confirm</td>
<td class="description">Enum for confirm mode dialog</td>
</tr>
<tr>
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for normal mode dialog</td>
</tr>
<tr>
<td class="name">
FullView</td>
<td class="type">string</td>
<td class="default">fullview</td>
<td class="description">Enum for fullview mode dialog</td>
</tr>
</tbody>
</table>















### model
{:#enum:model}








User defined model will be automatically set in this











### NeedleType
{:#enum:needletype}








Enum for gauge NeedleType






#### Properties






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
<td class="name">
Triangle</td>
<td class="type">string</td>
<td class="default">triangle</td>
<td class="description">To set the NeedleType triangle.</td>
</tr>
<tr>
<td class="name">
Rectangle</td>
<td class="type">string</td>
<td class="default">rectangle</td>
<td class="description">To set the NeedleType rectangle.</td>
</tr>
<tr>
<td class="name">
Trapezoid</td>
<td class="type">string</td>
<td class="default">trapezoid</td>
<td class="description">To set the NeedleType trapezoid.</td>
</tr>
<tr>
<td class="name">
Arrow</td>
<td class="type">string</td>
<td class="default">arrow</td>
<td class="description">To set the NeedleType arrow.</td>
</tr>
<tr>
<td class="name">
Image</td>
<td class="type">string</td>
<td class="default">image</td>
<td class="description">To set the NeedleType image.</td>
</tr>
</tbody>
</table>















### NodeConstraints
{:#enum:nodeconstraints}








Enum for the NodeConstraints in diagram






#### Properties






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
<td class="name">
None</td>
<td class="type">NodeConstraints</td>
<td class="default">LSH</td>
<td class="description">Disable all node Constraints</td>
</tr>
<tr>
<td class="name">
Select</td>
<td class="type">NodeConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables node to be selected</td>
</tr>
<tr>
<td class="name">
Delete</td>
<td class="type">NodeConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables node to be Deleted</td>
</tr>
<tr>
<td class="name">
Drag</td>
<td class="type">NodeConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables node to be Dragged</td>
</tr>
<tr>
<td class="name">
Rotate</td>
<td class="type">NodeConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables node to be Rotated</td>
</tr>
<tr>
<td class="name">
Connect</td>
<td class="type">NodeConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables node to be connected</td>
</tr>
<tr>
<td class="name">
ResizeNorthEast</td>
<td class="type">NodeConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables node to be resize north east</td>
</tr>
<tr>
<td class="name">
ResizeEast</td>
<td class="type">NodeConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables node to be resize east</td>
</tr>
<tr>
<td class="name">
ResizeSouthEast</td>
<td class="type">NodeConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables node to be resize south east</td>
</tr>
<tr>
<td class="name">
ResizeSouth</td>
<td class="type">NodeConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables node to be resize south</td>
</tr>
<tr>
<td class="name">
ResizeSouthWest</td>
<td class="type">NodeConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables node to be resize south west</td>
</tr>
<tr>
<td class="name">
ResizeWest</td>
<td class="type">NodeConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables node to be resize west</td>
</tr>
<tr>
<td class="name">
ResizeNorthWest</td>
<td class="type">NodeConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables node to be resize north west</td>
</tr>
<tr>
<td class="name">
ResizeNorth</td>
<td class="type">NodeConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables node to be resize north</td>
</tr>
<tr>
<td class="name">
Resize</td>
<td class="type">NodeConstraints</td>
<td class="default">BITOR</td>
<td class="description">Enables node to be Resized</td>
</tr>
<tr>
<td class="name">
Shadow</td>
<td class="type">NodeConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables shadow</td>
</tr>
<tr>
<td class="name">
DragLabel</td>
<td class="type">NodeConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables label of node to be Dragged</td>
</tr>
<tr>
<td class="name">
AllowPan</td>
<td class="type">NodeConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables panning should be done while node dragging</td>
</tr>
<tr>
<td class="name">
AspectRatio</td>
<td class="type">NodeConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables Proportional resize for node</td>
</tr>
<tr>
<td class="name">
Default</td>
<td class="type">NodeConstraints</td>
<td class="default">BITOR</td>
<td class="description">Enables all node constraints</td>
</tr>
</tbody>
</table>

### ObjectTypes
{:#enum:objectypes}
Enum for ObjectTypes in diagram

#### Properties

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
<td class="name">
Diagram</td>
<td class="type">string</td>
<td class="default">diagram</td>
<td class="description">Specifies that the type of the object is diagram</td>
</tr>
<tr>
<td class="name">
Palette</td>
<td class="type">string</td>
<td class="default">palette</td>
<td class="description">Specifies that the type of the object is palette</td>
</tr>
<td class="name">
Lane</td>
<td class="type">string</td>
<td class="default">lane</td>
<td class="description">Specifies that the type of the object is lane</td>
</tr>
<tr>
<td class="name">
Group</td>
<td class="type">string</td>
<td class="default">group</td>
<td class="description">Specifies that the type of the object is group</td>
</tr>
</tbody>
</table>














### Orientation
{:#enum:orientation}








Enum for Bullet Graph Orientation






#### Properties






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
<td class="name">
Horizontal</td>
<td class="type">string</td>
<td class="default">horizontal</td>
<td class="description">support for orientation in horizontal direction.</td>
</tr>
<tr>
<td class="name">
Vertical</td>
<td class="type">string</td>
<td class="default">vertical</td>
<td class="description">support for orientation in vertical direction.</td>
</tr>
</tbody>
</table>















### Orientation
{:#enum:orientation}








Enum for chart orientation.






#### Properties






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
<td class="name">
Horizontal</td>
<td class="type">string</td>
<td class="default">horizontal</td>
<td class="description">Sets chart orientation to horizontal.</td>
</tr>
<tr>
<td class="name">
Vertical</td>
<td class="type">string</td>
<td class="default">vertical</td>
<td class="description">Sets chart orientation to vertical.</td>
</tr>
</tbody>
</table>















### Orientation
{:#enum:orientation}








Enum for ProgressbarOrientation






#### Properties






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
<td class="name">
Horizontal</td>
<td class="type">string</td>
<td class="default">horizontal</td>
<td class="description">Enum for horizontal mode progress bar</td>
</tr>
<tr>
<td class="name">
Vertical</td>
<td class="type">string</td>
<td class="default">vertical</td>
<td class="description">Enum for vertical mode progress bar</td>
</tr>
</tbody>
</table>















### Orientation
{:#enum:orientation}








Enum for RatingOrientation






#### Properties






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
<td class="name">
Horizontal</td>
<td class="type">string</td>
<td class="default">horizontal</td>
<td class="description">Enum for horizontal mode rating</td>
</tr>
<tr>
<td class="name">
Vertical</td>
<td class="type">string</td>
<td class="default">vertical</td>
<td class="description">Enum for vertical mode rating</td>
</tr>
</tbody>
</table>















### Orientation
{:#enum:orientation}








Enum for Orientation






#### Properties






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
<td class="name">
Horizontal</td>
<td class="type">string</td>
<td class="default">horizontal</td>
<td class="description">Enum for Horizontal Orientation</td>
</tr>
<tr>
<td class="name">
Vertical</td>
<td class="type">string</td>
<td class="default">vertical</td>
<td class="description">Enum for Vertical Orientation</td>
</tr>
</tbody>
</table>















### Orientation
{:#enum:orientation}








Enum for slider






#### Properties






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
<td class="name">
Horizontal</td>
<td class="type">string</td>
<td class="default">horizontal</td>
<td class="description">Enum for horizontal mode slider</td>
</tr>
<tr>
<td class="name">
Vertical</td>
<td class="type">string</td>
<td class="default">vertical</td>
<td class="description">Enum for vertical mode slider</td>
</tr>
</tbody>
</table>















### OuterCustomLabelPosition
{:#enum:outercustomlabelposition}








Enum for gauge OuterCustomLabelPosition






#### Properties






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
<td class="name">
Left</td>
<td class="type">string</td>
<td class="default">left</td>
<td class="description">To set the OuterCustomLabelPosition left.</td>
</tr>
<tr>
<td class="name">
Right</td>
<td class="type">string</td>
<td class="default">right</td>
<td class="description">To set the OuterCustomLabelPosition right.</td>
</tr>
<tr>
<td class="name">
Top</td>
<td class="type">string</td>
<td class="default">top</td>
<td class="description">To set the OuterCustomLabelPosition top.</td>
</tr>
<tr>
<td class="name">
Bottom</td>
<td class="type">string</td>
<td class="default">bottom</td>
<td class="description">To set the OuterCustomLabelPosition bottom.</td>
</tr>
</tbody>
</table>















### OuterCustomLabelPosition
{:#enum:outercustomlabelposition}








Enum for gauge OuterCustomLabelPosition






#### Properties






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
<td class="name">
Left</td>
<td class="type">string</td>
<td class="default">left</td>
<td class="description">To set the OuterCustomLabelPosition left.</td>
</tr>
<tr>
<td class="name">
Right</td>
<td class="type">string</td>
<td class="default">right</td>
<td class="description">To set the OuterCustomLabelPosition right.</td>
</tr>
<tr>
<td class="name">
Top</td>
<td class="type">string</td>
<td class="default">top</td>
<td class="description">To set the OuterCustomLabelPosition top.</td>
</tr>
<tr>
<td class="name">
Bottom</td>
<td class="type">string</td>
<td class="default">bottom</td>
<td class="description">To set the OuterCustomLabelPosition bottom.</td>
</tr>
</tbody>
</table>















### PageOrientations
{:#enum:pageorientations}








Enum for PageOrientations in diagram






#### Properties






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
<td class="name">
Landscape</td>
<td class="type">string</td>
<td class="default">landscape</td>
<td class="description">Used to set orientation as Landscape</td>
</tr>
<tr>
<td class="name">
Portrait</td>
<td class="type">string</td>
<td class="default">portrait</td>
<td class="description">Used to set orientation as portrait</td>
</tr>
</tbody>
</table>















### PagerDisplay
{:#enum:pagerdisplay}








Enum for Grid Pager Display






#### Properties






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
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for Normal pager display</td>
</tr>
<tr>
<td class="name">
Fixed</td>
<td class="type">string</td>
<td class="default">fixed</td>
<td class="description">Enum for Fixed pager display</td>
</tr>
</tbody>
</table>















### PagerPositionHorizontal
{:#enum:pagerpositionhorizontal}








Enum for PagerPositionHorizontal






#### Properties






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
<td class="name">
Bottom</td>
<td class="type">string</td>
<td class="default">bottom</td>
<td class="description">Enum for Bottom PagerPositionHorizontal</td>
</tr>
<tr>
<td class="name">
Top</td>
<td class="type">string</td>
<td class="default">top</td>
<td class="description">Enum for Top PagerPositionHorizontal</td>
</tr>
</tbody>
</table>















### PagerPositionVertical
{:#enum:pagerpositionvertical}








Enum for PagerPositionVertical






#### Properties






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
<td class="name">
Right</td>
<td class="type">string</td>
<td class="default">right</td>
<td class="description">Enum for Right PagerPositionVertical</td>
</tr>
<tr>
<td class="name">
Left</td>
<td class="type">string</td>
<td class="default">left</td>
<td class="description">Enum for Left PagerPositionVertical</td>
</tr>
</tbody>
</table>















### PagerType
{:#enum:pagertype}








Enum for Grid Pager Type






#### Properties






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
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">used to enable normal pager which contain page navigation buttons</td>
</tr>
<tr>
<td class="name">
Scrollable</td>
<td class="type">string</td>
<td class="default">scrollable</td>
<td class="description">used to enable scrollable pager</td>
</tr>
</tbody>
</table>















### Pattern
{:#enum:pattern}








Enum for highlighting or selecting patterns in Chart 






#### Properties






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
<td class="name">
None</td>
<td class="type">string</td>
<td class="default">none</td>
<td class="description">Sets none as highlighting or selecting pattern</td>
</tr>
<tr>
<td class="name">
Chessboard</td>
<td class="type">string</td>
<td class="default">chessboard</td>
<td class="description">Sets chess board as highlighting or selecting pattern</td>
</tr>
<tr>
<td class="name">
Crosshatch</td>
<td class="type">string</td>
<td class="default">crosshatch</td>
<td class="description">Sets cross hatch as highlighting or selecting pattern</td>
</tr>
<tr>
<td class="name">
Dots</td>
<td class="type">string</td>
<td class="default">dots</td>
<td class="description">Set dots as highlighting or selecting pattern</td>
</tr>
<tr>
<td class="name">
Pacman</td>
<td class="type">string</td>
<td class="default">pacman</td>
<td class="description">Sets pacman as highlighting or selecting pattern</td>
</tr>
<tr>
<td class="name">
DiagonalBackward</td>
<td class="type">string</td>
<td class="default">diagonalbackward</td>
<td class="description">Sets diagonal backward as highlighting or selecting pattern</td>
</tr>
<tr>
<td class="name">
DiagonalForward</td>
<td class="type">string</td>
<td class="default">crosshatch</td>
<td class="description">Sets diagonal forward as highlighting or selecting pattern</td>
</tr>
<tr>
<td class="name">
Grid</td>
<td class="type">string</td>
<td class="default">grid</td>
<td class="description">Set grid as highlighting or selecting pattern</td>
</tr>
<tr>
<td class="name">
Turquoise</td>
<td class="type">string</td>
<td class="default">turquoise</td>
<td class="description">Sets turquoise as highlighting or selecting pattern</td>
</tr>
<tr>
<td class="name">
Star</td>
<td class="type">string</td>
<td class="default">star</td>
<td class="description">Sets star as highlighting or selecting pattern</td>
</tr>
<tr>
<td class="name">
Triangle</td>
<td class="type">string</td>
<td class="default">triangle</td>
<td class="description">Sets triangle as highlighting or selecting pattern</td>
</tr>
<tr>
<td class="name">
Circle</td>
<td class="type">string</td>
<td class="default">circle</td>
<td class="description">Sets circle as highlighting or selecting pattern</td>
</tr>
<tr>
<td class="name">
Tile</td>
<td class="type">string</td>
<td class="default">tile</td>
<td class="description">Sets tile as highlighting or selecting pattern</td>
</tr>
<tr>
<td class="name">
HorizontalDash</td>
<td class="type">string</td>
<td class="default">horizontaldash</td>
<td class="description">Sets horizontal dash as highlighting or selecting pattern</td>
</tr>
<tr>
<td class="name">
VerticalDash</td>
<td class="type">string</td>
<td class="default">verticaldash</td>
<td class="description">Sets vertical dash as highlighting or selecting pattern</td>
</tr>
<tr>
<td class="name">
Rectangle</td>
<td class="type">string</td>
<td class="default">rectangle</td>
<td class="description">Set rectangle as highlighting or selecting pattern</td>
</tr>
<tr>
<td class="name">
Box</td>
<td class="type">string</td>
<td class="default">box</td>
<td class="description">Sets box as highlighting or selecting pattern</td>
</tr>
<tr>
<td class="name">
VerticalStripe</td>
<td class="type">string</td>
<td class="default">tile</td>
<td class="description">Sets vertical stripe as highlighting or selecting pattern</td>
</tr>
<tr>
<td class="name">
HorizontalStripe</td>
<td class="type">string</td>
<td class="default">horizontalstripe</td>
<td class="description">Sets horizontal stripe as highlighting or selecting pattern</td>
</tr>
<tr>
<td class="name">
Bubble</td>
<td class="type">string</td>
<td class="default">bubble</td>
<td class="description">Sets bubble as highlighting or selecting pattern</td>
</tr>
<tr>
<td class="name">
Custom</td>
<td class="type">string</td>
<td class="default">custom</td>
<td class="description">Set custom as highlighting or selecting pattern. The user defined pattern provided in custom patter property will be used</td>
</tr>
</tbody>
</table>















### PointerPlacement
{:#enum:pointerplacement}








Enum for gauge PointerPlacement






#### Properties






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
<td class="name">
Near</td>
<td class="type">string</td>
<td class="default">near</td>
<td class="description">To set the PointerPlacement near.</td>
</tr>
<tr>
<td class="name">
Far</td>
<td class="type">string</td>
<td class="default">far</td>
<td class="description">To set the PointerPlacement far.</td>
</tr>
<tr>
<td class="name">
Center</td>
<td class="type">string</td>
<td class="default">center</td>
<td class="description">To set the PointerPlacement center.</td>
</tr>
</tbody>
</table>















### PointerPlacement
{:#enum:pointerplacement}








Enum for gauge PointerPlacement






#### Properties






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
<td class="name">
Near</td>
<td class="type">string</td>
<td class="default">near</td>
<td class="description">To set the PointerPlacement near.</td>
</tr>
<tr>
<td class="name">
Far</td>
<td class="type">string</td>
<td class="default">far</td>
<td class="description">To set the PointerPlacement far.</td>
</tr>
<tr>
<td class="name">
Center</td>
<td class="type">string</td>
<td class="default">center</td>
<td class="description">To set the PointerPlacement center.</td>
</tr>
</tbody>
</table>















### PointerType
{:#enum:pointertype}








Enum for gauge PointerType






#### Properties






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
<td class="name">
Needle</td>
<td class="type">string</td>
<td class="default">needle</td>
<td class="description">To set the PointerType needle.</td>
</tr>
<tr>
<td class="name">
Marker</td>
<td class="type">string</td>
<td class="default">marker</td>
<td class="description">To set the PointerType marker.</td>
</tr>
</tbody>
</table>















### PortConstraints
{:#enum:portconstraints}








Enum for PortConstraints in diagram






#### Properties






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
<td class="name">
None</td>
<td class="type">PortConstraints</td>
<td class="default">LSH</td>
<td class="description">Disable all constraints</td>
</tr>
<tr>
<td class="name">
Connect</td>
<td class="type">PortConstraints</td>
<td class="default">LSH</td>
<td class="description">Enables connections with connector</td>
</tr>
</tbody>
</table>















### PortShapes
{:#enum:portshapes}








Enum for various port shapes in diagram






#### Properties






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
<td class="name">
X</td>
<td class="type">string</td>
<td class="default">x</td>
<td class="description">Used to set port shape as X</td>
</tr>
<tr>
<td class="name">
Circle</td>
<td class="type">string</td>
<td class="default">circle</td>
<td class="description">Used to set port shape as Circle</td>
</tr>
<tr>
<td class="name">
Square</td>
<td class="type">string</td>
<td class="default">square</td>
<td class="description">Used to set port shape as Square</td>
</tr>
<tr>
<td class="name">
Path</td>
<td class="type">string</td>
<td class="default">path</td>
<td class="description">Used to set port shape as Path</td>
</tr>
</tbody>
</table>















### PortVisibility
{:#enum:portvisibility}








Enum for port visibility in diagram






#### Properties






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
<td class="name">
Visible</td>
<td class="type">PortVisibility</td>
<td class="default">LSH</td>
<td class="description">Set the port visibility as Visible</td>
</tr>
<tr>
<td class="name">
Hidden</td>
<td class="type">PortVisibility</td>
<td class="default">LSH</td>
<td class="description">Set the port visibility as Hidden</td>
</tr>
<tr>
<td class="name">
Hover</td>
<td class="type">PortVisibility</td>
<td class="default">LSH</td>
<td class="description">Port get visible when hover connector on node</td>
</tr>
<tr>
<td class="name">
Connect</td>
<td class="type">PortVisibility</td>
<td class="default">LSH</td>
<td class="description">Port gets visible when connect connector to node</td>
</tr>
<tr>
<td class="name">
Default</td>
<td class="type">PortVisibility</td>
<td class="default">LSH</td>
<td class="description">Specifies the port visibility as default</td>
</tr>
</tbody>
</table>















### Position
{:#enum:position}








Enum for Map Navigation Control and Legend dock position






#### Properties






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
<td class="name">
None</td>
<td class="type">string</td>
<td class="default">none</td>
<td class="description">support for dock position none.</td>
</tr>
<tr>
<td class="name">
TopLeft</td>
<td class="type">string</td>
<td class="default">topleft</td>
<td class="description">support for dock position topleft.</td>
</tr>
<tr>
<td class="name">
TopCenter</td>
<td class="type">string</td>
<td class="default">topcenter</td>
<td class="description">support for dock position topcenter.</td>
</tr>
<tr>
<td class="name">
TopRight</td>
<td class="type">string</td>
<td class="default">topright</td>
<td class="description">support for dock position topright.</td>
</tr>
<tr>
<td class="name">
CenterLeft</td>
<td class="type">string</td>
<td class="default">centerleft</td>
<td class="description">support for dock position centerleft.</td>
</tr>
<tr>
<td class="name">
Center</td>
<td class="type">string</td>
<td class="default">center</td>
<td class="description">support for dock position center.</td>
</tr>
<tr>
<td class="name">
CenterRight</td>
<td class="type">string</td>
<td class="default">centerright</td>
<td class="description">support for dock position centerright.</td>
</tr>
<tr>
<td class="name">
BottomLeft</td>
<td class="type">string</td>
<td class="default">bottomleft</td>
<td class="description">support for dock position bottomleft.</td>
</tr>
<tr>
<td class="name">
BottomCenter</td>
<td class="type">string</td>
<td class="default">bottomcenter</td>
<td class="description">support for dock position bottomcenter.</td>
</tr>
<tr>
<td class="name">
BottomRight</td>
<td class="type">string</td>
<td class="default">bottomright</td>
<td class="description">support for dock position bottomright.</td>
</tr>
</tbody>
</table>















### Position
{:#enum:position}








Enum for position.






#### Properties






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
<td class="name">
Top</td>
<td class="type">string</td>
<td class="default">top</td>
<td class="description">Sets the position to top.</td>
</tr>
<tr>
<td class="name">
Middle</td>
<td class="type">string</td>
<td class="default">middle</td>
<td class="description">Sets the position to middle.</td>
</tr>
<tr>
<td class="name">
Bottom</td>
<td class="type">string</td>
<td class="default">bottom</td>
<td class="description">Sets the position to bottom.</td>
</tr>
</tbody>
</table>















### Position
{:#enum:position}








Enum for Position






#### Properties






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
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for relative position for Footer</td>
</tr>
<tr>
<td class="name">
Fixed</td>
<td class="type">string</td>
<td class="default">fixed</td>
<td class="description">Enum for fixed position for Footer</td>
</tr>
</tbody>
</table>















### Position
{:#enum:position}








Enum for Position






#### Properties






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
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for relative position for Header</td>
</tr>
<tr>
<td class="name">
Fixed</td>
<td class="type">string</td>
<td class="default">fixed</td>
<td class="description">Enum for fixed position for Header</td>
</tr>
</tbody>
</table>















### Position
{:#enum:position}








Enum for Position






#### Properties






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
<td class="name">
RightCenter</td>
<td class="type">string</td>
<td class="default">rightcenter</td>
<td class="description">Enum for RightCenter Position</td>
</tr>
<tr>
<td class="name">
RightTop</td>
<td class="type">string</td>
<td class="default">righttop</td>
<td class="description">Enum for RightTop Position</td>
</tr>
<tr>
<td class="name">
RightBottom</td>
<td class="type">string</td>
<td class="default">rightbottom</td>
<td class="description">Enum for RightBottom Position</td>
</tr>
<tr>
<td class="name">
LeftCenter</td>
<td class="type">string</td>
<td class="default">leftcenter</td>
<td class="description">Enum for LeftCenter Position</td>
</tr>
<tr>
<td class="name">
LeftTop</td>
<td class="type">string</td>
<td class="default">lefttop</td>
<td class="description">Enum for LeftTop Position</td>
</tr>
<tr>
<td class="name">
LeftBottom</td>
<td class="type">string</td>
<td class="default">leftbottom</td>
<td class="description">Enum for LeftBottom Position</td>
</tr>
</tbody>
</table>















### Position
{:#enum:position}








Enum for Position






#### Properties






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
<td class="name">
Fixed</td>
<td class="type">string</td>
<td class="default">fixed</td>
<td class="description">Enum for Fixed position Tab</td>
</tr>
<tr>
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for Normal position Tab</td>
</tr>
</tbody>
</table>















### Position
{:#enum:position}








Enum for toolbar position






#### Properties






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
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for relative position for toolbar</td>
</tr>
<tr>
<td class="name">
Fixed</td>
<td class="type">string</td>
<td class="default">fixed</td>
<td class="description">Enum for fixed position for toolbar</td>
</tr>
</tbody>
</table>















### Precision
{:#enum:precision}








Enum for RatingPrecision






#### Properties






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
<td class="name">
Full</td>
<td class="type">string</td>
<td class="default">full</td>
<td class="description">Enum for full precision rating</td>
</tr>
<tr>
<td class="name">
Exact</td>
<td class="type">string</td>
<td class="default">exact</td>
<td class="description">Enum for exact precision rating</td>
</tr>
<tr>
<td class="name">
Half</td>
<td class="type">string</td>
<td class="default">half</td>
<td class="description">Enum for half precision rating</td>
</tr>
</tbody>
</table>















### PyramidMode
{:#enum:pyramidmode}








Enum for chart pyramid mode.






#### Properties






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
<td class="name">
Linear</td>
<td class="type">string</td>
<td class="default">linear</td>
<td class="description">Specifies the mode of the pyramid as linear.</td>
</tr>
<tr>
<td class="name">
Surface</td>
<td class="type">string</td>
<td class="default">Surface</td>
<td class="description">Specifies the mode of the pyramid as surface.</td>
</tr>
</tbody>
</table>















### PrintMode
{:#enum:printmode}
 
Specifies whether the Grid's printmode is AllPages or CurrentPage.

<table class="props">
<thead>
<tr>
<th>Name</th> 
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">AllPages</td> 
<td class="description">Prints allpages.</td>
</tr>
<tr>
<td class="name">CurrentPage</td> 
<td class="description">Prints currentpage.</td>
</tr>
</tbody>
</table>
 

### RangePadding
{:#enum:rangepadding}








Enum for range padding.






#### Properties






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
<td class="name">
Additional</td>
<td class="type">string</td>
<td class="default">additional</td>
<td class="description">Sets chart range padding as additional.</td>
</tr>
<tr>
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Sets chart range padding as normal.</td>
</tr>
<tr>
<td class="name">
None</td>
<td class="type">string</td>
<td class="default">none</td>
<td class="description">Sets chart range padding as none.</td>
</tr>
<tr>
<td class="name">
Round</td>
<td class="type">string</td>
<td class="default">round</td>
<td class="description">Sets chart range padding as round.</td>
</tr>
<tr>
<td class="name">
Auto</td>
<td class="type">string</td>
<td class="default">auto</td>
<td class="description">Sets chart range padding as auto.</td>
</tr>
</tbody>
</table>















### RangePlacement
{:#enum:rangeplacement}








Enum for gauge RangePlacement






#### Properties






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
<td class="name">
Near</td>
<td class="type">string</td>
<td class="default">near</td>
<td class="description">To set the RangePlacement near.</td>
</tr>
<tr>
<td class="name">
Far</td>
<td class="type">string</td>
<td class="default">far</td>
<td class="description">To set the RangePlacement far.</td>
</tr>
<tr>
<td class="name">
Center</td>
<td class="type">string</td>
<td class="default">center</td>
<td class="description">To set the RangePlacement center.</td>
</tr>
</tbody>
</table>















### RangePlacement
{:#enum:rangeplacement}








Enum for gauge RangePlacement






#### Properties






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
<td class="name">
Near</td>
<td class="type">string</td>
<td class="default">near</td>
<td class="description">To set the RangePlacement near.</td>
</tr>
<tr>
<td class="name">
Far</td>
<td class="type">string</td>
<td class="default">far</td>
<td class="description">To set the RangePlacement far.</td>
</tr>
<tr>
<td class="name">
Center</td>
<td class="type">string</td>
<td class="default">center</td>
<td class="description">To set the RangePlacement center.</td>
</tr>
</tbody>
</table>















### Region
{:#enum:region}








Enum for the Region in diagram






#### Properties






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
<td class="name">
Content</td>
<td class="type">string</td>
<td class="default">content</td>
<td class="description">specifies region that is occupied by diagram elements</td>
</tr>
<tr>
<td class="name">
PageSettings</td>
<td class="type">string</td>
<td class="default">pageSettings</td>
<td class="description">specifies the region based on the page settings</td>
</tr>
</tbody>
</table>















### Region
{:#enum:region}








Enum for placing annotation in Chart






#### Properties






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
<td class="name">
Chart</td>
<td class="type">string</td>
<td class="default">chart</td>
<td class="description">Specifies annotation placement should be based on Chart location</td>
</tr>
<tr>
<td class="name">
Series</td>
<td class="type">string</td>
<td class="default">series</td>
<td class="description">Specifies annotation placement should be based on chart area</td>
</tr>
</tbody>
</table>

### RelativeMode
{:#enum:relativemode}

Enum for the RelativeMode in diagram

#### Properties

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
<td class="name">Object</td>
<td class="type">String</td>
<td class="default">object</td>
<td class="description">Shows tooltip around the node</td>
</tr>
<tr>
<td class="name">Mouse</td>
<td class="type">String</td>
<td class="default">mouse</td>
<td class="description">Shows tooltip at the mouse position</td>
</tr>
</tbody>
</table>















### RenderMode
{:#enum:rendermode}








Enum for RenderMode






#### Properties






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
<td class="name">
Auto</td>
<td class="type">string</td>
<td class="default">auto</td>
<td class="description">Auto RenderMode</td>
</tr>
<tr>
<td class="name">
IOS7</td>
<td class="type">string</td>
<td class="default">ios7</td>
<td class="description">IOS7 RenderMode</td>
</tr>
<tr>
<td class="name">
Android</td>
<td class="type">string</td>
<td class="default">android</td>
<td class="description">Android RenderMode</td>
</tr>
<tr>
<td class="name">
Windows</td>
<td class="type">string</td>
<td class="default">windows</td>
<td class="description">Windows RenderMode</td>
</tr>
</tbody>
</table>















### RowPosition
{:#enum:rowposition}
 
Specifies whether the position of add new row in Grid is Top or Bottom.

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
<td class="description">Specifies position of add new row as top.</td>
</tr>
<tr>
<td class="name">Bottom</td> 
<td class="description">Specifies position of add new row as bottom.</td>
</tr>
</tbody>
</table>


### ScaleType
{:#enum:scaletype}








Enum for gauge ScaleType






#### Properties






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
<td class="name">
Rectangle</td>
<td class="type">string</td>
<td class="default">rectangle</td>
<td class="description">To set the ScaleType rectangle.</td>
</tr>
<tr>
<td class="name">
RoundedRectangle</td>
<td class="type">string</td>
<td class="default">roundedrectangle</td>
<td class="description">To set the ScaleType roundedrectangle.</td>
</tr>
<tr>
<td class="name">
Thermometer</td>
<td class="type">string</td>
<td class="default">thermometer</td>
<td class="description">To set the ScaleType thermometer.</td>
</tr>
</tbody>
</table>








### Boundary Constraints
{:#enum:boundaryConstraints}








Enum for Boundary Constraints in diagram






#### Properties






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
<td class="name">
Infinity</td>
<td class="type">string</td>
<td class="default">infinity</td>
<td class="description">Allows to move the diagram elements in all directions, without any restrictions</td>
</tr>
<tr>
<td class="name">
Diagram</td>
<td class="type">string</td>
<td class="default">diagram</td>
<td class="description">Allows to move the diagram elements beyond the diagram content</td>
</tr>
<tr>
<td class="name">
Page</td>
<td class="type">string</td>
<td class="default">page</td>
<td class="description">Allows to move the diagram elements only the region specified on pageSettings </td>
</tr>
</tbody>
</table>






### ScrollLimit
{:#enum:scrolllimit}








Enum for ScrollLimit in diagram






#### Properties






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
<td class="name">
Infinity</td>
<td class="type">string</td>
<td class="default">infinity</td>
<td class="description">Used to set scrollLimit as Infinity</td>
</tr>
<tr>
<td class="name">
Diagram</td>
<td class="type">string</td>
<td class="default">diagram</td>
<td class="description">Used to set scrollLimit as Diagram</td>
</tr>
<tr>
<td class="name">
Limited</td>
<td class="type">string</td>
<td class="default">limited</td>
<td class="description">Used to set scrollLimit as Limited</td>
</tr>
</tbody>
</table>















### Segments
{:#enum:segments}








Enum for various connector segments in diagram






#### Properties






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
<td class="name">
Straight</td>
<td class="type">string</td>
<td class="default">straight</td>
<td class="description">Used to specify the lines as Straight</td>
</tr>
<tr>
<td class="name">
Orthogonal</td>
<td class="type">string</td>
<td class="default">orthogonal</td>
<td class="description">Used to specify the lines as Orthogonal</td>
</tr>
<tr>
<td class="name">
Bezier</td>
<td class="type">string</td>
<td class="default">bezier</td>
<td class="description">Used to specify the lines as Bezier</td>
</tr>
</tbody>
</table>















### SelectionMode
{:#enum:selectionmode}








Enum for Map selection mode






#### Properties






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
<td class="name">
Default</td>
<td class="type">string</td>
<td class="default">default</td>
<td class="description">support for selection mode default.</td>
</tr>
<tr>
<td class="name">
Multiple</td>
<td class="type">string</td>
<td class="default">multiple</td>
<td class="description">support for selection mode multiple.</td>
</tr>
</tbody>
</table>















### SelectorConstraints
{:#enum:selectorconstraints}








Enum to specify the SelectorConstraints in diagram






#### Properties






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
<td class="name">
None</td>
<td class="type">SelectorConstraints</td>
<td class="default">LSH</td>
<td class="description">Hides the selector</td>
</tr>
<tr>
<td class="name">
Rotator</td>
<td class="type">SelectorConstraints</td>
<td class="default">LSH</td>
<td class="description">Sets the visibility of rotation handle as visible</td>
</tr>
<tr>
<td class="name">
Resizer</td>
<td class="type">SelectorConstraints</td>
<td class="default">LSH</td>
<td class="description">Sets the visibility of resize handles as visible</td>
</tr>
<tr>
<td class="name">
UserHandles</td>
<td class="type">SelectorConstraints</td>
<td class="default">LSH</td>
<td class="description">Sets the visibility of user handles as visible</td>
</tr>
<tr>
<td class="name">
All</td>
<td class="type">SelectorConstraints</td>
<td class="default">BITOR</td>
<td class="description">Sets the visibility of all selection handles as visible</td>
</tr>
</tbody>
</table>















### Shape
{:#enum:shape}








Enum for the shape of indicator symbol






#### Properties






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
<td class="name">
Circle</td>
<td class="type">string</td>
<td class="default">circle</td>
<td class="description">support for drawing circle as indicator symbol.</td>
</tr>
<tr>
<td class="name">
Cross</td>
<td class="type">string</td>
<td class="default">cross</td>
<td class="description">support for drawing cross as indicator symbol.</td>
</tr>
<tr>
<td class="name">
Diamond</td>
<td class="type">string</td>
<td class="default">diamond</td>
<td class="description">support for drawing diamond as indicator symbol.</td>
</tr>
<tr>
<td class="name">
DownArrow</td>
<td class="type">string</td>
<td class="default">downarrow</td>
<td class="description">support for drawing down arrow as indicator symbol.</td>
</tr>
<tr>
<td class="name">
Ellipse</td>
<td class="type">string</td>
<td class="default">ellipse</td>
<td class="description">support for drawing ellipse as indicator symbol.</td>
</tr>
<tr>
<td class="name">
HorizontalLine</td>
<td class="type">string</td>
<td class="default">horizontalLine</td>
<td class="description">support for drawing horizontal line as indicator symbol.</td>
</tr>
<tr>
<td class="name">
Image</td>
<td class="type">string</td>
<td class="default">image</td>
<td class="description">support for drawing image as indicator symbol.</td>
</tr>
<tr>
<td class="name">
InvertedTriangle</td>
<td class="type">string</td>
<td class="default">invertedtriangle</td>
<td class="description">support for drawing inverted triangle as indicator symbol.</td>
</tr>
<tr>
<td class="name">
LeftArrow</td>
<td class="type">string</td>
<td class="default">leftarrow</td>
<td class="description">support for drawing left arrow as indicator symbol.</td>
</tr>
<tr>
<td class="name">
Pentagon</td>
<td class="type">string</td>
<td class="default">pentagon</td>
<td class="description">support for drawing pentagon as indicator symbol.</td>
</tr>
<tr>
<td class="name">
Rectangle</td>
<td class="type">string</td>
<td class="default">Rectangle</td>
<td class="description">support for drawing rectangle as indicator symbol.</td>
</tr>
<tr>
<td class="name">
RightArrow</td>
<td class="type">string</td>
<td class="default">rightarrow</td>
<td class="description">support for drawing right arrow as indicator symbol.</td>
</tr>
<tr>
<td class="name">
Star</td>
<td class="type">string</td>
<td class="default">star</td>
<td class="description">support for drawing star as indicator symbol.</td>
</tr>
<tr>
<td class="name">
Trapezoid</td>
<td class="type">string</td>
<td class="default">trapezoid</td>
<td class="description">support for drawing trapezoid as indicator symbol.</td>
</tr>
<tr>
<td class="name">
Triangle</td>
<td class="type">string</td>
<td class="default">triangle</td>
<td class="description">support for drawing triangle as indicator symbol.</td>
</tr>
<tr>
<td class="name">
UpArrow</td>
<td class="type">string</td>
<td class="default">uparrow</td>
<td class="description">support for drawing up arrow as indicator symbol.</td>
</tr>
<tr>
<td class="name">
VerticalLine</td>
<td class="type">string</td>
<td class="default">verticalline</td>
<td class="description">support for drawing vertical line as indicator symbol.</td>
</tr>
<tr>
<td class="name">
Wedge</td>
<td class="type">string</td>
<td class="default">wedge</td>
<td class="description">support for drawing wedge as indicator symbol.</td>
</tr>
</tbody>
</table>















### Shape
{:#enum:shape}








Enum for chart shape.






#### Properties






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
<td class="name">
None</td>
<td class="type">string</td>
<td class="default">none</td>
<td class="description">Sets the shape to none.</td>
</tr>
<tr>
<td class="name">
LeftArrow</td>
<td class="type">string</td>
<td class="default">leftarrow</td>
<td class="description">Sets the shape to leftarrow.</td>
</tr>
<tr>
<td class="name">
RightArrow</td>
<td class="type">string</td>
<td class="default">rightarrow</td>
<td class="description">Sets the shape to rightarrow.</td>
</tr>
<tr>
<td class="name">
Circle</td>
<td class="type">string</td>
<td class="default">circle</td>
<td class="description">Sets the shape to circle.</td>
</tr>
<tr>
<td class="name">
Cross</td>
<td class="type">string</td>
<td class="default">cross</td>
<td class="description">Sets the shape to cross.</td>
</tr>
<tr>
<td class="name">
HorizLine</td>
<td class="type">string</td>
<td class="default">horizline</td>
<td class="description">Sets the shape to horizline.</td>
</tr>
<tr>
<td class="name">
VertLine</td>
<td class="type">string</td>
<td class="default">vertLine</td>
<td class="description">Sets the shape to vertline.</td>
</tr>
<tr>
<td class="name">
Diamond</td>
<td class="type">string</td>
<td class="default">diamond</td>
<td class="description">Sets the shape to diamond.</td>
</tr>
<tr>
<td class="name">
Rectangle</td>
<td class="type">string</td>
<td class="default">rectangle</td>
<td class="description">Sets the shape to rectangle.</td>
</tr>
<tr>
<td class="name">
Triangle</td>
<td class="type">string</td>
<td class="default">triangle</td>
<td class="description">Sets the shape to triangle.</td>
</tr>
<tr>
<td class="name">
InvertedTriangle</td>
<td class="type">string</td>
<td class="default">invertedtriangle</td>
<td class="description">Sets the shape to invertedtriangle.</td>
</tr>
<tr>
<td class="name">
Hexagon</td>
<td class="type">string</td>
<td class="default">hexagon</td>
<td class="description">Sets the shape to hexagon.</td>
</tr>
<tr>
<td class="name">
Pentagon</td>
<td class="type">string</td>
<td class="default">pentagon</td>
<td class="description">Sets the shape to pentagon.</td>
</tr>
<tr>
<td class="name">
Star</td>
<td class="type">string</td>
<td class="default">star</td>
<td class="description">Sets the shape to star.</td>
</tr>
<tr>
<td class="name">
Ellipse</td>
<td class="type">string</td>
<td class="default">ellipse</td>
<td class="description">Sets the shape to ellipse.</td>
</tr>
<tr>
<td class="name">
Wedge</td>
<td class="type">string</td>
<td class="default">wedge</td>
<td class="description">Sets the shape to wedge.</td>
</tr>
<tr>
<td class="name">
Trapezoid</td>
<td class="type">string</td>
<td class="default">trapezoid</td>
<td class="description">Sets the shape to trapezoid.</td>
</tr>
<tr>
<td class="name">
UpArrow</td>
<td class="type">string</td>
<td class="default">uparrow</td>
<td class="description">Sets the shape to uparrow.</td>
</tr>
<tr>
<td class="name">
DownArrow</td>
<td class="type">string</td>
<td class="default">downarrow</td>
<td class="description">Sets the shape to downarrow.</td>
</tr>
<tr>
<td class="name">
Image</td>
<td class="type">string</td>
<td class="default">image</td>
<td class="description">Sets the shape to image.</td>
</tr>
</tbody>
</table>















### Shape
{:#enum:shape}








Enum for RatingShape






#### Properties






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
<td class="name">
Star</td>
<td class="type">string</td>
<td class="default">star</td>
<td class="description">Enum for star shape rating</td>
</tr>
<tr>
<td class="name">
Circle</td>
<td class="type">string</td>
<td class="default">circle</td>
<td class="description">Enum for circle shape rating</td>
</tr>
<tr>
<td class="name">
Diamond</td>
<td class="type">string</td>
<td class="default">diamond</td>
<td class="description">Enum for diamond shape rating</td>
</tr>
<tr>
<td class="name">
Heart</td>
<td class="type">string</td>
<td class="default">heart</td>
<td class="description">Enum for heart shape rating</td>
</tr>
<tr>
<td class="name">
Pentagon</td>
<td class="type">string</td>
<td class="default">pentagon</td>
<td class="description">Enum for pentagon shape rating</td>
</tr>
<tr>
<td class="name">
Square</td>
<td class="type">string</td>
<td class="default">square</td>
<td class="description">Enum for square shape rating</td>
</tr>
<tr>
<td class="name">
Triangle</td>
<td class="type">string</td>
<td class="default">triangle</td>
<td class="description">Enum for triangle shape rating</td>
</tr>
</tbody>
</table>















### Shapes
{:#enum:shapes}








Enum for various Shapes of node in diagram






#### Properties






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
<td class="name">
Image</td>
<td class="type">string</td>
<td class="default">image</td>
<td class="description">Used to specify node Shape as Image</td>
</tr>
<tr>
<td class="name">
Text</td>
<td class="type">string</td>
<td class="default">text</td>
<td class="description">Used to specify node Shape as Text</td>
</tr>
<tr>
<td class="name">
HTML</td>
<td class="type">string</td>
<td class="default">HTML</td>
<td class="description">Used to specify node Shape as HTML</td>
</tr>
<tr>
<td class="name">
Native</td>
<td class="type">string</td>
<td class="default">native</td>
<td class="description">Used to specify node Shape as Native</td>
</tr>
<tr>
<td class="name">
Basic</td>
<td class="type">string</td>
<td class="default">basic</td>
<td class="description">Used to specify node Shape as Basic</td>
</tr>
<tr>
<td class="name">
Flow</td>
<td class="type">string</td>
<td class="default">flow</td>
<td class="description">Used to specify node Shape as Flow</td>
</tr>
<tr>
<td class="name">
Arrow</td>
<td class="type">string</td>
<td class="default">arrow</td>
<td class="description">Used to specify node Shape as Arrow</td>
</tr>
<tr>
<td class="name">
BPMN</td>
<td class="type">string</td>
<td class="default">BPMN</td>
<td class="description">Used to specify node Shape as BPMN</td>
</tr>
</tbody>
</table>















### ShowOn
{:#enum:showon}








Enum for Menu ShowOn






#### Properties






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
<td class="name">
Tap</td>
<td class="type">string</td>
<td class="default">tap</td>
<td class="description">Enum for show menu on tap</td>
</tr>
<tr>
<td class="name">
TapHold</td>
<td class="type">string</td>
<td class="default">taphold</td>
<td class="description">Enum for show menu on tap hold</td>
</tr>
</tbody>
</table>















### SnapConstraints
{:#enum:snapconstraints}








Enum for SnapConstraints in diagram






#### Properties






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
<td class="name">
None</td>
<td class="type">SnapConstraints</td>
<td class="default">0</td>
<td class="description">Enables node to be snapped to horizontal gridlines</td>
</tr>
<tr>
<td class="name">
SnapToHorizontalLines</td>
<td class="type">SnapConstraints</td>
<td class="default">1</td>
<td class="description">Enables node to be snapped to vertical gridlines</td>
</tr>
<tr>
<td class="name">
SnapToVerticalLines</td>
<td class="type">SnapConstraints</td>
<td class="default">2</td>
<td class="description">Enables node to be snapped to horizontal gridlines</td>
</tr>
<tr>
<td class="name">
SnapToLines</td>
<td class="type">SnapConstraints</td>
<td class="default">BITOR</td>
<td class="description">Enables node to be snapped to gridlines</td>
</tr>
<tr>
<td class="name">
ShowHorizontalLines</td>
<td class="type">SnapConstraints</td>
<td class="default">4</td>
<td class="description">Enable horizontal lines</td>
</tr>
<tr>
<td class="name">
ShowVerticalLines</td>
<td class="type">SnapConstraints</td>
<td class="default">8</td>
<td class="description">Enable vertical lines</td>
</tr>
<tr>
<td class="name">
ShowLines</td>
<td class="type">SnapConstraints</td>
<td class="default">BITOR</td>
<td class="description">Enable both horizontal and vertical lines</td>
</tr>
<tr>
<td class="name">
All</td>
<td class="type">SnapConstraints</td>
<td class="default">BITOR</td>
<td class="description">Enable all the constraints</td>
</tr>
</tbody>
</table>















### SortOrder
{:#enum:sortorder}








Enum for sortorder






#### Properties






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
<td class="name">
Ascending</td>
<td class="type">string</td>
<td class="default">ascending</td>
<td class="description">Enum for Ascending sort order</td>
</tr>
<tr>
<td class="name">
Descending</td>
<td class="type">string</td>
<td class="default">descending</td>
<td class="description">Enum for Descending sort order</td>
</tr>
</tbody>
</table>















### Style
{:#enum:style}








Enum for IOS7style






#### Properties






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
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for normal ios7 button style</td>
</tr>
<tr>
<td class="name">
Back</td>
<td class="type">string</td>
<td class="default">back</td>
<td class="description">Enum for back ios7 button style</td>
</tr>
<tr>
<td class="name">
Header</td>
<td class="type">string</td>
<td class="default">header</td>
<td class="description">Enum for header ios7 button style</td>
</tr>
<tr>
<td class="name">
Dialog</td>
<td class="type">string</td>
<td class="default">dialog</td>
<td class="description">Enum for dialog ios7 button style</td>
</tr>
</tbody>
</table>















### Style
{:#enum:style}








Enum for AndroidStyle






#### Properties






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
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for normal anroid button style</td>
</tr>
<tr>
<td class="name">
Small</td>
<td class="type">string</td>
<td class="default">small</td>
<td class="description">Enum for small android button style</td>
</tr>
<tr>
<td class="name">
Dialog</td>
<td class="type">string</td>
<td class="default">dialog</td>
<td class="description">Enum for dialog android button style</td>
</tr>
</tbody>
</table>















### Style
{:#enum:style}








Enum for windowsstyle






#### Properties






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
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for normal windows button style</td>
</tr>
<tr>
<td class="name">
Back</td>
<td class="type">string</td>
<td class="default">back</td>
<td class="description">Enum for back windows button style</td>
</tr>
</tbody>
</table>















### Style
{:#enum:style}








Enum for FlatStyle






#### Properties






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
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for normal flat button style</td>
</tr>
<tr>
<td class="name">
Back</td>
<td class="type">string</td>
<td class="default">back</td>
<td class="description">Enum for back flat button style</td>
</tr>
<tr>
<td class="name">
Header</td>
<td class="type">string</td>
<td class="default">header</td>
<td class="description">Enum for header flat button style</td>
</tr>
</tbody>
</table>















### SymbologyType
{:#enum:symbologytype}








Enum for Symbol type.






#### Properties






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
<td class="name">
code39</td>
<td class="type">string</td>
<td class="default">code39</td>
<td class="description">Specifies Code 39 Barcode.</td>
</tr>
<tr>
<td class="name">
code39Extended</td>
<td class="type">string</td>
<td class="default">code39extended</td>
<td class="description">Specifies Code 39 Extended Barcode.</td>
</tr>
<tr>
<td class="name">
code11</td>
<td class="type">string</td>
<td class="default">code11</td>
<td class="description">Specifies Code 11 Barcode.</td>
</tr>
<tr>
<td class="name">
codabar</td>
<td class="type">string</td>
<td class="default">codabar</td>
<td class="description">Specifies Codabar Barcode.</td>
</tr>
<tr>
<td class="name">
code32</td>
<td class="type">string</td>
<td class="default">code32</td>
<td class="description">Specifies Code 32 Barcode.</td>
</tr>
<tr>
<td class="name">
code93</td>
<td class="type">string</td>
<td class="default">code93</td>
<td class="description">Specifies Code 93 Barcode.</td>
</tr>
<tr>
<td class="name">
code93Extended</td>
<td class="type">string</td>
<td class="default">code93extended</td>
<td class="description">Specifies Code 93 Extended Barcode.</td>
</tr>
<tr>
<td class="name">
code128A</td>
<td class="type">string</td>
<td class="default">code128a</td>
<td class="description">Specifies Code 128 A Barcode.</td>
</tr>
<tr>
<td class="name">
code128B</td>
<td class="type">string</td>
<td class="default">code128b</td>
<td class="description">Specifies Code 128 B Barcode.</td>
</tr>
<tr>
<td class="name">
code128C</td>
<td class="type">string</td>
<td class="default">code128c</td>
<td class="description">Specifies Code 128 C Barcode.</td>
</tr>
<tr>
<td class="name">
dataMatrix</td>
<td class="type">string</td>
<td class="default">datamatrix</td>
<td class="description">Specifies DataMatrix Barcode.</td>
</tr>
<tr>
<td class="name">
qrBarcode</td>
<td class="type">string</td>
<td class="default">qrbarcode</td>
<td class="description">Specifies QR Barcode.</td>
</tr>
</tbody>
</table>


### SelectionMode
{:#enum:selectionmode}
 
Specifies whether the Grid's selection mode is Row, Cell or Column.
 
<table class="props">
<thead>
<tr>
<th>Name</th> 
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Row</td> 
<td class="description">Selection is row basis.</td>
</tr>
<tr>
<td class="name">Cell</td> 
<td class="description">Selection is cell basis.</td>
</tr>
<tr>
<td class="name">Column</td> 
<td class="description">Selection is column basis.</td>
</tr>
</tbody>
</table>
 

### SelectionType
{:#enum:selectiontype}

Specifies whether the Grid's selection type is Single or Multiple.
 
<table class="props">
<thead>
<tr>
<th>Name</th> 
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Single</td> 
<td class="description">Specifies the selection type as single.</td>
</tr>
<tr>
<td class="name">Multiple</td> 
<td class="description">Specifies the selection type as multiple.</td>
</tr>
</tbody>
</table>


### SummaryType
{:#enum:summarytype}
 
Specifies whether the Grid's summary type to be used.

<table class="props">
<thead>
<tr>
<th>Name</th> 
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Average</td> 
<td class="description">Summary type is average.</td>
</tr>
<tr>
<td class="name">Minimum</td> 
<td class="description">Summary type is minimum.</td>
</tr>
<tr>
<td class="name">Maximum</td> 
<td class="description">Summary type is maximum.</td>
</tr>
<tr>
<td class="name">Count</td> 
<td class="description">Summary type is count.</td>
</tr>
<tr>
<td class="name">Sum</td> 
<td class="description">Summary type is sum.</td>
</tr>
<tr>
<td class="name">Custom</td> 
<td class="description">Summary type is custom.</td>
</tr>
<tr>
<td class="name">TrueCount</td> 
<td class="description">Summary type is truecount.</td>
</tr>
<tr>
<td class="name">FalseCount</td> 
<td class="description">Summary type is falsecount.</td>
</tr>
</tbody>
</table>












### TrendlinesType
{:#enum:trendlinestype}








Enum for type of trendline in Chart.






#### Properties






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
<td class="name">
Linear</td>
<td class="type">string</td>
<td class="default">linear</td>
<td class="description">Sets linear as trendline type.</td>
</tr>
<tr>
<td class="name">
Exponential</td>
<td class="type">string</td>
<td class="default">exponential</td>
<td class="description">Sets exponential as trendline type.</td>
</tr>
<tr>
<td class="name">
Logarithmic</td>
<td class="type">string</td>
<td class="default">logarithmic</td>
<td class="description">Sets logarithmic as trendline type.</td>
</tr>
<tr>
<td class="name">
Power</td>
<td class="type">string</td>
<td class="default">power</td>
<td class="description">Sets power as trendline type.</td>
</tr>
<tr>
<td class="name">
Polynomial</td>
<td class="type">string</td>
<td class="default">polynomial</td>
<td class="description">Sets polynomial as trendline type.</td>
</tr>
</tbody>
</table>















### TextAlign
{:#enum:textalign}








Enum for the Text Alignment in diagram






#### Properties






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
<td class="name">
Left</td>
<td class="type">string</td>
<td class="default">left</td>
<td class="description">Used to align text on left side of node/connector</td>
</tr>
<tr>
<td class="name">
Center</td>
<td class="type">string</td>
<td class="default">center</td>
<td class="description">Used to align text on center of node/connector</td>
</tr>
<tr>
<td class="name">
Right</td>
<td class="type">string</td>
<td class="default">right</td>
<td class="description">Used to align text on Right side of node/connector</td>
</tr>
</tbody>
</table>















### TextAlign
{:#enum:textalign}
 
Specifies whether the text alignment in the cell is Center, Justify, Left or Right.

<table class="props">
<thead>
<tr>
<th>Name</th> 
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Center</td> 
<td class="description">Text is centered.</td>
</tr>
<tr>
<td class="name">Justify</td> 
<td class="description">Text is justified.</td>
</tr>
<tr>
<td class="name">Left</td> 
<td class="description">Text is aligned to the left.</td>
</tr>
<tr>
<td class="name">Right</td> 
<td class="description">Text is aligned to the right.</td>
</tr>
</tbody>
</table>
 

### TextAlign
{:#enum:textalign}








Enum for gauge TextAlign






#### Properties






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
<td class="name">
Left</td>
<td class="type">string</td>
<td class="default">left</td>
<td class="description">To set the TextAlign Left.</td>
</tr>
<tr>
<td class="name">
Right</td>
<td class="type">string</td>
<td class="default">right</td>
<td class="description">To set the TextAlign right.</td>
</tr>
</tbody>
</table>















### TextAlignment
{:#enum:textalignment}








Enum for text alignment.






#### Properties






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
<td class="name">
MiddleTop</td>
<td class="type">string</td>
<td class="default">middletop</td>
<td class="description">Support for changing text alignment to middleTop.</td>
</tr>
<tr>
<td class="name">
MiddleCenter</td>
<td class="type">string</td>
<td class="default">middlecenter</td>
<td class="description">Support for changing text alignment to middleCenter.</td>
</tr>
<tr>
<td class="name">
MiddleBottom</td>
<td class="type">string</td>
<td class="default">middlebottom</td>
<td class="description">Support for changing text alignment to middleBottom.</td>
</tr>
</tbody>
</table>















### TextAlignment
{:#enum:textalignment}








Enum for Tile TextAlignment






#### Properties






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
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for normal alignment of tile text</td>
</tr>
<tr>
<td class="name">
Left</td>
<td class="type">string</td>
<td class="default">left</td>
<td class="description">Enum for left alignment of tile text</td>
</tr>
<tr>
<td class="name">
Right</td>
<td class="type">string</td>
<td class="default">right</td>
<td class="description">Enum for right alignment of tile text</td>
</tr>
<tr>
<td class="name">
Center</td>
<td class="type">string</td>
<td class="default">center</td>
<td class="description">Enum for center alignment of tile text</td>
</tr>
</tbody>
</table>















### TextDecorations
{:#enum:textdecorations}








Enum for TextDecorations in diagram






#### Properties






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
<td class="name">
Underline</td>
<td class="type">string</td>
<td class="default">underline</td>
<td class="description">Used to set text decoration of the label as Underline</td>
</tr>
<tr>
<td class="name">
Overline</td>
<td class="type">string</td>
<td class="default">overline</td>
<td class="description">Used to set text decoration of the label as Overline</td>
</tr>
<tr>
<td class="name">
LineThrough</td>
<td class="type">string</td>
<td class="default">line-through</td>
<td class="description">Used to set text decoration of the label as LineThrough</td>
</tr>
<tr>
<td class="name">
None</td>
<td class="type">string</td>
<td class="default">none</td>
<td class="description">Used to set text decoration of the label as None</td>
</tr>
</tbody>
</table>















### TextPosition
{:#enum:textposition}








Enum for Tile TextPosition






#### Properties






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
<td class="name">
Inner</td>
<td class="type">string</td>
<td class="default">inner</td>
<td class="description">Enum for inner position of tile text</td>
</tr>
<tr>
<td class="name">
Outer</td>
<td class="type">string</td>
<td class="default">outer</td>
<td class="description">Enum for outer position of tile text</td>
</tr>
</tbody>
</table>















### TextWrapping
{:#enum:textwrapping}








Enum for TextWrapping in diagram






#### Properties






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
<td class="name">
NoWrap</td>
<td class="type">string</td>
<td class="default">nowrap</td>
<td class="description">Disables wrapping</td>
</tr>
<tr>
<td class="name">
Wrap</td>
<td class="type">string</td>
<td class="default">wrap</td>
<td class="description">Enables Line-break at normal word break points</td>
</tr>
<tr>
<td class="name">
WrapWithOverflow</td>
<td class="type">string</td>
<td class="default">wrapwithoverflow</td>
<td class="description">Enables Line-break at normal word break points with longer word overflows</td>
</tr>
</tbody>
</table>















### TickLinesPosition
{:#enum:ticklinesposition}








Enum for tick line position in Chart






#### Properties






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
<td class="name">
Inside</td>
<td class="type">string</td>
<td class="default">inside</td>
<td class="description">Tick lines will be placed inside</td>
</tr>
<tr>
<td class="name">
Outside</td>
<td class="type">string</td>
<td class="default">outside</td>
<td class="description">Tick lines will be placed outside</td>
</tr>
</tbody>
</table>















### Theme
{:#enum:theme}








Enum for chart themes.






#### Properties






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
<td class="name">
Azure</td>
<td class="type">string</td>
<td class="default">azure</td>
<td class="description">Render chart in azure theme.</td>
</tr>
<tr>
<td class="name">
FlatLight</td>
<td class="type">string</td>
<td class="default">flatlight</td>
<td class="description">Render chart in flatlight theme.</td>
</tr>
<tr>
<td class="name">
Azuredark</td>
<td class="type">string</td>
<td class="default">azuredark</td>
<td class="description">Render chart in azuredark theme.</td>
</tr>
<tr>
<td class="name">
Lime</td>
<td class="type">string</td>
<td class="default">lime</td>
<td class="description">Render chart in lime theme.</td>
</tr>
<tr>
<td class="name">
LimeDark</td>
<td class="type">string</td>
<td class="default">limedark</td>
<td class="description">Render chart in limedark theme.</td>
</tr>
<tr>
<td class="name">
Saffron</td>
<td class="type">string</td>
<td class="default">saffron</td>
<td class="description">Render chart in saffron theme.</td>
</tr>
<tr>
<td class="name">
SaffronDark</td>
<td class="type">string</td>
<td class="default">saffrondark</td>
<td class="description">Render chart in saffrondark theme.</td>
</tr>
<tr>
<td class="name">
GradientLight</td>
<td class="type">string</td>
<td class="default">gradientlight</td>
<td class="description">Render chart in gradientlight theme.</td>
</tr>
<tr>
<td class="name">
GradientDark</td>
<td class="type">string</td>
<td class="default">gradientdark</td>
<td class="description">Render chart in gradientdark theme.</td>
</tr>
</tbody>
</table>















### Theme
{:#enum:theme}








Enum for Theme






#### Properties






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
<td class="name">
Auto</td>
<td class="type">string</td>
<td class="default">auto</td>
<td class="description">Auto RenderMode</td>
</tr>
<tr>
<td class="name">
Dark</td>
<td class="type">string</td>
<td class="default">dark</td>
<td class="description">Dark RenderMode</td>
</tr>
<tr>
<td class="name">
Light</td>
<td class="type">string</td>
<td class="default">light</td>
<td class="description">Light RenderMode</td>
</tr>
</tbody>
</table>















### Themes
{:#enum:themes}








Enum for Bullet Graph Theme3






#### Properties






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
<td class="name">
flatlight</td>
<td class="type">string</td>
<td class="default">OBJECTLIT</td>
<td class="description">To set the theme flatlight.</td>
</tr>
<tr>
<td class="name">
flatdark</td>
<td class="type">string</td>
<td class="default">OBJECTLIT</td>
<td class="description">To set the theme flatdark.</td>
</tr>
</tbody>
</table>















### Themes
{:#enum:themes}








Enum for gauge Themes






#### Properties






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
<td class="name">
flatlight</td>
<td class="type">string</td>
<td class="default">OBJECTLIT</td>
<td class="description">To set the themes flatlight.</td>
</tr>
<tr>
<td class="name">
flatdark</td>
<td class="type">string</td>
<td class="default">OBJECTLIT</td>
<td class="description">To set the themes flatdark.</td>
</tr>
</tbody>
</table>















### Themes
{:#enum:themes}








Enum for gauge Themes






#### Properties






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
<td class="name">
flatlight</td>
<td class="type">string</td>
<td class="default">OBJECTLIT</td>
<td class="description">To set the themes flatlight.</td>
</tr>
<tr>
<td class="name">
flatdark</td>
<td class="type">string</td>
<td class="default">OBJECTLIT</td>
<td class="description">To set the themes flatdark.</td>
</tr>
</tbody>
</table>















### Themes
{:#enum:themes}








Enum for gauge Themes






#### Properties






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
<td class="name">
flatlight</td>
<td class="type">string</td>
<td class="default">OBJECTLIT</td>
<td class="description">To set the themes flatlight.</td>
</tr>
<tr>
<td class="name">
flatdark</td>
<td class="type">string</td>
<td class="default">OBJECTLIT</td>
<td class="description">To set the themes flatdark.</td>
</tr>
</tbody>
</table>















### ThumbStyle
{:#enum:thumbstyle}








Enum for slider






#### Properties






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
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for normal mode thumb style slider</td>
</tr>
<tr>
<td class="name">
Small</td>
<td class="type">string</td>
<td class="default">small</td>
<td class="description">Enum for small mode thumb style slider</td>
</tr>
</tbody>
</table>















### TickPlacement
{:#enum:tickplacement}








Enum for Bullet Graph tick placement






#### Properties






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
<td class="name">
Inside</td>
<td class="type">string</td>
<td class="default">inside</td>
<td class="description">support for placing ticks inside scale.</td>
</tr>
<tr>
<td class="name">
Outside</td>
<td class="type">string</td>
<td class="default">outside</td>
<td class="description">support for placing ticks outside scale.</td>
</tr>
</tbody>
</table>















### TickPlacement
{:#enum:tickplacement}








Enum for gauge TickPlacement






#### Properties






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
<td class="name">
Near</td>
<td class="type">string</td>
<td class="default">near</td>
<td class="description">To set the TickPlacement near.</td>
</tr>
<tr>
<td class="name">
Far</td>
<td class="type">string</td>
<td class="default">far</td>
<td class="description">To set the TickPlacement far.</td>
</tr>
<tr>
<td class="name">
Center</td>
<td class="type">string</td>
<td class="default">center</td>
<td class="description">To set the TickPlacement center.</td>
</tr>
</tbody>
</table>















### TickPlacement
{:#enum:tickplacement}








Enum for gauge TickPlacement






#### Properties






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
<td class="name">
Near</td>
<td class="type">string</td>
<td class="default">near</td>
<td class="description">To set the TickPlacement near.</td>
</tr>
<tr>
<td class="name">
Far</td>
<td class="type">string</td>
<td class="default">far</td>
<td class="description">To set the TickPlacement far.</td>
</tr>
<tr>
<td class="name">
Center</td>
<td class="type">string</td>
<td class="default">center</td>
<td class="description">To set the TickPlacement center.</td>
</tr>
</tbody>
</table>















### TickPosition
{:#enum:tickposition}








Enum for Bullet Graph Tick Position






#### Properties






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
<td class="name">
Far</td>
<td class="type">string</td>
<td class="default">far</td>
<td class="description">To set the Tick position below quantitative scale.</td>
</tr>
<tr>
<td class="name">
Near</td>
<td class="type">string</td>
<td class="default">near</td>
<td class="description">To set the Tick position above quantitative scale.</td>
</tr>
<tr>
<td class="name">
Center</td>
<td class="type">string</td>
<td class="default">center</td>
<td class="description">To set the Tick position at the center of quantitative scale.</td>
</tr>
</tbody>
</table>















### TickType
{:#enum:ticktype}








Enum for gauge TickType






#### Properties






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
<td class="name">
Major</td>
<td class="type">string</td>
<td class="default">major</td>
<td class="description">To set the TickType major.</td>
</tr>
<tr>
<td class="name">
Minor</td>
<td class="type">string</td>
<td class="default">minor</td>
<td class="description">To set the TickType minor.</td>
</tr>
</tbody>
</table>















### TickType
{:#enum:ticktype}








Enum for gauge TickType






#### Properties






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
<td class="name">
MajorInterval</td>
<td class="type">string</td>
<td class="default">majorinterval</td>
<td class="description">To set the TickType majorinterval.</td>
</tr>
<tr>
<td class="name">
MinorInterval</td>
<td class="type">string</td>
<td class="default">minorinterval</td>
<td class="description">To set the TickType minorinterval.</td>
</tr>
</tbody>
</table>















### TileSize
{:#enum:tilesize}








Enum for Tile Size






#### Properties






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
<td class="name">
Medium</td>
<td class="type">string</td>
<td class="default">medium</td>
<td class="description">Enum for medium size of tile</td>
</tr>
<tr>
<td class="name">
Small</td>
<td class="type">string</td>
<td class="default">small</td>
<td class="description">Enum for small size of tile</td>
</tr>
<tr>
<td class="name">
Large</td>
<td class="type">string</td>
<td class="default">large</td>
<td class="description">Enum for large size of tile</td>
</tr>
<tr>
<td class="name">
Wide</td>
<td class="type">string</td>
<td class="default">wide</td>
<td class="description">Enum for wide size of tile</td>
</tr>
</tbody>
</table>















### Tool
{:#enum:tool}








Enum for the Tool in diagram






#### Properties






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
<td class="name">
None</td>
<td class="type">Tool</td>
<td class="default">LSH</td>
<td class="description">Disables all Tools</td>
</tr>
<tr>
<td class="name">
SingleSelect</td>
<td class="type">Tool</td>
<td class="default">LSH</td>
<td class="description">Enables/Disables SingleSelect tool</td>
</tr>
<tr>
<td class="name">
MultipleSelect</td>
<td class="type">Tool</td>
<td class="default">LSH</td>
<td class="description">Enables/Disables MultiSelect tool</td>
</tr>
<tr>
<td class="name">
ZoomPan</td>
<td class="type">Tool</td>
<td class="default">LSH</td>
<td class="description">Enables/Disables ZoomPan tool</td>
</tr>
<tr>
<td class="name">
DrawOnce</td>
<td class="type">Tool</td>
<td class="default">LSH</td>
<td class="description">Enables/Disables DrawOnce tool</td>
</tr>
<tr>
<td class="name">
ContinuesDraw</td>
<td class="type">Tool</td>
<td class="default">LSH</td>
<td class="description">Enables/Disables ContinuousDraw tool</td>
</tr>
</tbody>
</table>















### Type
{:#enum:type}








Enum for chart series type.






#### Properties






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
<td class="name">
Line</td>
<td class="type">string</td>
<td class="default">line</td>
<td class="description">sets the seriesType of chart to line.</td>
</tr>
<tr>
<td class="name">
Spline</td>
<td class="type">string</td>
<td class="default">spline</td>
<td class="description">sets the seriesType of chart to spline.</td>
</tr>
<tr>
<td class="name">
Column</td>
<td class="type">string</td>
<td class="default">column</td>
<td class="description">sets the seriesType of chart to column.</td>
</tr>
<tr>
<td class="name">
Doughnut</td>
<td class="type">string</td>
<td class="default">doughnut</td>
<td class="description">sets the seriesType of chart to doughnut.</td>
</tr>
<tr>
<td class="name">
Area</td>
<td class="type">string</td>
<td class="default">area</td>
<td class="description">sets the seriesType of chart to area.</td>
</tr>
<tr>
<td class="name">
SplineArea</td>
<td class="type">string</td>
<td class="default">splinearea</td>
<td class="description">sets the seriesType of chart to splinearea.</td>
</tr>
<tr>
<td class="name">
StepLine</td>
<td class="type">string</td>
<td class="default">stepline</td>
<td class="description">sets the seriesType of chart to stepline.</td>
</tr>
<tr>
<td class="name">
StepArea</td>
<td class="type">string</td>
<td class="default">steparea</td>
<td class="description">sets the seriesType of chart to steparea.</td>
</tr>
<tr>
<td class="name">
Pie</td>
<td class="type">string</td>
<td class="default">pie</td>
<td class="description">sets the seriesType of chart to pie.</td>
</tr>
<tr>
<td class="name">
Hilo</td>
<td class="type">string</td>
<td class="default">hilo</td>
<td class="description">sets the seriesType of chart to hilo.</td>
</tr>
<tr>
<td class="name">
HiloOpenClose</td>
<td class="type">string</td>
<td class="default">hiloopenclose</td>
<td class="description">sets the seriesType of chart to hiloopenclose.</td>
</tr>
<tr>
<td class="name">
Candle</td>
<td class="type">string</td>
<td class="default">candle</td>
<td class="description">sets the seriesType of chart to candle.</td>
</tr>
<tr>
<td class="name">
Bubble</td>
<td class="type">string</td>
<td class="default">bubble</td>
<td class="description">sets the seriesType of chart to bubble.</td>
</tr>
<tr>
<td class="name">
Scatter</td>
<td class="type">string</td>
<td class="default">scatter</td>
<td class="description">sets the seriesType of chart to scatter.</td>
</tr>
<tr>
<td class="name">
Bar</td>
<td class="type">string</td>
<td class="default">bar</td>
<td class="description">sets the seriesType of chart to bar.</td>
</tr>
<tr>
<td class="name">
StackingArea</td>
<td class="type">string</td>
<td class="default">stackingarea</td>
<td class="description">sets the seriesType of chart to stackingarea.</td>
</tr>
<tr>
<td class="name">
StackingArea100</td>
<td class="type">string</td>
<td class="default">stackingarea100</td>
<td class="description">sets the seriesType of chart to stackingarea100.</td>
</tr>
<tr>
<td class="name">
RangeColumn</td>
<td class="type">string</td>
<td class="default">rangecolumn</td>
<td class="description">sets the seriesType of chart to rangecolumn.</td>
</tr>
<tr>
<td class="name">
StackingColumn</td>
<td class="type">string</td>
<td class="default">stackingcolumn</td>
<td class="description">sets the seriesType of chart to stackingcolumn.</td>
</tr>
<tr>
<td class="name">
StackingColumn100</td>
<td class="type">string</td>
<td class="default">stackingcolumn100</td>
<td class="description">sets the seriesType of chart to stackingcolumn100.</td>
</tr>
<tr>
<td class="name">
StackingBar</td>
<td class="type">string</td>
<td class="default">stackingbar</td>
<td class="description">sets the seriesType of chart to stackingbar.</td>
</tr>
<tr>
<td class="name">
StackingBar100</td>
<td class="type">string</td>
<td class="default">stackingbar100</td>
<td class="description">sets the seriesType of chart to stackingbar100.</td>
</tr>
<tr>
<td class="name">
Pyramid</td>
<td class="type">string</td>
<td class="default">pyramid</td>
<td class="description">sets the seriesType of chart to pyramid.</td>
</tr>
<tr>
<td class="name">
Funnel</td>
<td class="type">string</td>
<td class="default">funnel</td>
<td class="description">sets the seriesType of chart to funnel.</td>
</tr>
<tr>
<td class="name">
Polar</td>
<td class="type">string</td>
<td class="default">polar</td>
<td class="description">sets the seriesType of chart to polar.</td>
</tr>
<tr>
<td class="name">
Radar</td>
<td class="type">string</td>
<td class="default">radar</td>
<td class="description">sets the seriesType of chart to radar.</td>
</tr>
<tr>
<td class="name">
RangeArea</td>
<td class="type">string</td>
<td class="default">rangearea</td>
<td class="description">sets the seriesType of chart to rangeArea.</td>
</tr>
</tbody>
</table>















### Type
{:#enum:type}








Enum for ej.mobile.Menu.IOS7.Type






#### Properties






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
<td class="name">
Auto</td>
<td class="type">string</td>
<td class="default">auto</td>
<td class="description">Enum for auto type menu in ios7 mode</td>
</tr>
<tr>
<td class="name">
Animate</td>
<td class="type">string</td>
<td class="default">animate</td>
<td class="description">Enum for animate type menu in ios7 mode</td>
</tr>
<tr>
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="default">normal</td>
<td class="description">Enum for normal type menu in ios7 mode</td>
</tr>
</tbody>
</table>















### Type
{:#enum:type}








Enum for ej.mobile.Menu.Android.Type






#### Properties






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
<td class="name">
Contextual</td>
<td class="type">string</td>
<td class="default">contextual</td>
<td class="description">Enum for contextual type menu in android mode</td>
</tr>
<tr>
<td class="name">
Popup</td>
<td class="type">string</td>
<td class="default">popup</td>
<td class="description">Enum for popup type menu in android mode</td>
</tr>
<tr>
<td class="name">
OptionsList</td>
<td class="type">string</td>
<td class="default">optionslist</td>
<td class="description">Enum for optionslist type menu in android mode</td>
</tr>
<tr>
<td class="name">
OptionsMenu</td>
<td class="type">string</td>
<td class="default">optionsmenu</td>
<td class="description">Enum for optionsmenu type menu in android mode</td>
</tr>
</tbody>
</table>















### Type
{:#enum:type}








Enum for ej.mobile.Menu.Windows.Type






#### Properties






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
<td class="name">
Contextual</td>
<td class="type">string</td>
<td class="default">contextual</td>
<td class="description">Enum for contextual type menu in windows mode</td>
</tr>
<tr>
<td class="name">
Popup</td>
<td class="type">string</td>
<td class="default">popup</td>
<td class="description">Enum for popup type menu in windows mode</td>
</tr>
</tbody>
</table>














### ToolBarItems
{:#enum:toolbaritems}
 
Specifies the toolbar items to be used in the Grid. 

<table class="props">
<thead>
<tr>
<th>Name</th> 
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Add</td> 
<td class="description">Toolbar item is add.</td>
</tr>
<tr>
<td class="name">Edit</td> 
<td class="description">Toolbar item is edit.</td>
</tr>
<tr>
<td class="name">Delete</td> 
<td class="description">Toolbar item is delete.</td>
</tr>
<tr>
<td class="name">Update</td> 
<td class="description">Toolbar item is update.</td>
</tr>
<tr>
<td class="name">Cancel</td> 
<td class="description">Toolbar item is cancel.</td>
</tr>
<tr>
<td class="name">Search</td> 
<td class="description">Toolbar item is search.</td>
</tr>
<tr>
<td class="name">ExcelExport</td> 
<td class="description">Toolbar item is excelExport.</td>
</tr>
<tr>
<td class="name">PdfExport</td> 
<td class="description">Toolbar item is pdfExport.</td>
</tr>
<tr>
<td class="name">PrintGrid</td> 
<td class="description">Toolbar item is printGrid.</td>
</tr>
<tr>
<td class="name">WordExport</td> 
<td class="description">Toolbar item is wordExport.</td>
</tr>
</tbody>
</table>


### Unit
{:#enum:unit}









Enum for chart unit.






#### Properties






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
<td class="name">
percentage</td>
<td class="type">string</td>
<td class="default">percentage</td>
<td class="description">Specifies the unit in percentage.</td>
</tr>
<tr>
<td class="name">
pixel</td>
<td class="type">string</td>
<td class="default">pixel</td>
<td class="description">Specifies the unit in pixel.</td>
</tr>
</tbody>
</table>















### UnitTextPlacement
{:#enum:unittextplacement}








Enum for gauge UnitTextPlacement






#### Properties






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
<td class="name">
Back</td>
<td class="type">string</td>
<td class="default">back</td>
<td class="description">To set the UnitTextPlacement back.</td>
</tr>
<tr>
<td class="name">
Front</td>
<td class="type">string</td>
<td class="default">front</td>
<td class="description">To set the UnitTextPlacement front.</td>
</tr>
</tbody>
</table>















### UnitTextPlacement
{:#enum:unittextplacement}








Enum for gauge UnitTextPlacement






#### Properties






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
<td class="name">
Front</td>
<td class="type">string</td>
<td class="default">front</td>
<td class="description">To set the UnitTextPlacement front.</td>
</tr>
<tr>
<td class="name">
Back</td>
<td class="type">string</td>
<td class="default">back</td>
<td class="description">To set the UnitTextPlacement back.</td>
</tr>
</tbody>
</table>















### UserHandlePositions
{:#enum:userhandlepositions}








Enum to specify the userhandle position in diagram






#### Properties






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
<td class="name">
TopLeft</td>
<td class="type">string</td>
<td class="default">topleft</td>
<td class="description">Used to set position as TopLeft</td>
</tr>
<tr>
<td class="name">
TopCenter</td>
<td class="type">string</td>
<td class="default">topcenter</td>
<td class="description">Used to set position as TopCenter</td>
</tr>
<tr>
<td class="name">
TopRight</td>
<td class="type">string</td>
<td class="default">topright</td>
<td class="description">Used to set position as TopRight</td>
</tr>
<tr>
<td class="name">
MiddleLeft</td>
<td class="type">string</td>
<td class="default">middleleft</td>
<td class="description">Used to set position as MiddleLeft</td>
</tr>
<tr>
<td class="name">
MiddleRight</td>
<td class="type">string</td>
<td class="default">middleright</td>
<td class="description">Used to set position as MiddleRight</td>
</tr>
<tr>
<td class="name">
BottomLeft</td>
<td class="type">string</td>
<td class="default">bottomleft</td>
<td class="description">Used to set position as BottomLeft</td>
</tr>
<tr>
<td class="name">
BottomCenter</td>
<td class="type">string</td>
<td class="default">bottomcenter</td>
<td class="description">Used to set position as BottomCenter</td>
</tr>
<tr>
<td class="name">
BottomRight</td>
<td class="type">string</td>
<td class="default">bottomright</td>
<td class="description">Used to set position as BottomRight</td>
</tr>
</tbody>
</table>



### UnboundType
{:#enum:unboundtype}
 
Specifies whether the Grid's unbound type is Edit, Save, Delete or Cancel.
 
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
<td class="description">Unbound type is edit.</td>
</tr>
<tr>
<td class="name">Save</td> 
<td class="description">Unbound type is save.</td>
</tr>
<tr>
<td class="name">Delete</td> 
<td class="description">Unbound type is delete.</td>
</tr>
<tr>
<td class="name">Cancel</td> 
<td class="description">Unbound type is cancel.</td>
</tr>
</tbody>
</table>



### ValueType
{:#enum:valuetype}








Enum for chart valueType.






#### Properties






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
<td class="name">
Double</td>
<td class="type">string</td>
<td class="default">double</td>
<td class="description">set valueType for chart to double.</td>
</tr>
<tr>
<td class="name">
DateTime</td>
<td class="type">string</td>
<td class="default">datetime</td>
<td class="description">set valueType for chart to dateTime.</td>
</tr>
<tr>
<td class="name">
Category</td>
<td class="type">string</td>
<td class="default">category</td>
<td class="description">set valueType for chart to category.</td>
</tr>
<tr>
<td class="name">
Logarithmic</td>
<td class="type">string</td>
<td class="default">logarithmic</td>
<td class="description">set valueType for chart to logarithmic.</td>
</tr>
</tbody>
</table>















### VerticalAlignment
{:#enum:verticalalignment}








Enum for Vertical Alignment of elements in Chart






#### Properties






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
<td class="name">
Top</td>
<td class="type">string</td>
<td class="default">top</td>
<td class="description">Set vertical alignment as top</td>
</tr>
<tr>
<td class="name">
Middle</td>
<td class="type">string</td>
<td class="default">center</td>
<td class="description">Set vertical alignment as middle</td>
</tr>
<tr>
<td class="name">
Bottom</td>
<td class="type">string</td>
<td class="default">bottom</td>
<td class="description">Set vertical alignment as bottom</td>
</tr>
</tbody>
</table>















### VerticalAlignment
{:#enum:verticalalignment}








Enum for Vertical Alignment of elements in diagram






#### Properties






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
<td class="name">
Top</td>
<td class="type">string</td>
<td class="default">top</td>
<td class="description">Used to align text Vertically on left side of node/connector</td>
</tr>
<tr>
<td class="name">
Center</td>
<td class="type">string</td>
<td class="default">center</td>
<td class="description">Used to align text Vertically on center of node/connector</td>
</tr>
<tr>
<td class="name">
Bottom</td>
<td class="type">string</td>
<td class="default">bottom</td>
<td class="description">Used to align text Vertically on bottom of node/connector</td>
</tr>
</tbody>
</table>















### VerticalTextAlignment
{:#enum:verticaltextalignment}








Enum for Vertical Alignment of text in Chart






#### Properties






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
<td class="name">
Near</td>
<td class="type">string</td>
<td class="default">near</td>
<td class="description">Sets vertical alignment of text to near</td>
</tr>
<tr>
<td class="name">
Center</td>
<td class="type">string</td>
<td class="default">center</td>
<td class="description">Sets vertical alignment of text to center</td>
</tr>
<tr>
<td class="name">
Far</td>
<td class="type">string</td>
<td class="default">far</td>
<td class="description">Sets vertical alignment of text to far</td>
</tr>
</tbody>
</table>















### VirtualScrollMode
{:#enum:virtualscrollmode}
 
Specifies whether the Grid's virtual scroll mode is Normal or Continuous.

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
<td class="description">virtual scroll mode is normal.</td>
</tr>
<tr>
<td class="name">Continuous</td> 
<td class="description">virtual scroll mode is continuous.</td>
</tr>
</tbody>
</table>
 

### ZIndex
{:#enum:zindex}








Enum for zIndex.






#### Properties






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
<td class="name">
Over</td>
<td class="type">string</td>
<td class="default">over</td>
<td class="description">Support for changing the zIndex to over.</td>
</tr>
<tr>
<td class="name">
Behind</td>
<td class="type">string</td>
<td class="default">behind</td>
<td class="description">Support for changing the zIndex to behind.</td>
</tr>
</tbody>
</table>


## Methods

### clearShapeSelection
{:#methods:clearshapeselection}

Clear Selected Map Shapes


### refreshMarkers
{:#methods:refreshmarkers}

Generates markers


