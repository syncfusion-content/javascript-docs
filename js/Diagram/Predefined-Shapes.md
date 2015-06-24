---
layout: post
title: Predefined-Shapes
description: predefined shapes
platform: js
control: Diagram
documentation: ug
---

# Predefined Shapes

Diagram has several in built shapes. The inbuilt shapes are categorized as follows.

1. Basic Shapes
2. Flow Shapes
3. BPMN shapes

## Basic Shape

The Basic shapes are common shapes used to represent geometrical information visually. The following code example illustrates how to create a basic shape.

{% highlight js %}
var diagram = ej.datavisualization.Diagram;
//Create a basic shape
var node = {
   type: "basic",
   shape: Diagram.BasicShapes.Plus
};
{% endhighlight %}

The list of basic shapes are as follows.

{% include image.html url="/js/Diagram/Predefined-Shapes_images/Predefined-Shapes_img1.png" %}

## Flow Shape

The flow shapes are used to represent the process flow. It is used for analyzing, designing, managing or for documentation process. The following code example illustrates how to create a flow shape. 

{% highlight js %}
var diagram = ej.datavisualization.Diagram;
//Create a flow shape
var node = {
   type: "flow",
   shape: diagram.FlowShapes.Document
};
{% endhighlight %}

The list of flow shapes are as follows.

{% include image.html url="/js/Diagram/Predefined-Shapes_images/Predefined-Shapes_img2.png" %}

## BPMN Shape

BPMN shapes are used to represent internal business procedure in graphical notation and enables you to communicate the procedures in a standard manner. The BPMN shapes are categorized as follow.

1. Event
2. Gateway
3. Activity
4. Message
5. DataSource
6. DataObject

The shapes are listed as follows.

{% include image.html url="/js/Diagram/Predefined-Shapes_images/Predefined-Shapes_img3.png" %}

The BPMN shapes and its types are explained as follows.

### Event 

An event is represented with a circle and it denote something that happens. Icons within the circle denote the type of event. For example, an envelope representing a message, or a clock representing time. The following code example illustrate how to create an event in BPMN shape.

{% highlight js %}
var diagram = ej.datavisualization.Diagram;
//Create an event shape in BPMN 
var node = {
   type: "bpmn",
   shape: diagram.BPMNShapes.Event,
   event: diagram.BPMNEvents.Start,
   trigger: diagram.BPMNTriggers.None
};
{% endhighlight %}

<table>
<tr>
<th>
Event</th><th>
Type</th><th>
Trigger Result</th></tr>
<tr>
<td rowspan = "2">
Start Event</td><td>
Interrupting </td><td rowspan = "5">
None<br/>Message<br/>Timer<br/>Escalation<br/>Link<br/>Error<br/>Compensation<br/>Signal<br/>Multiple<br/>Parallel</td></tr>
<tr>
<td>
Non-Interrupting</td></tr>
<tr>
<td rowspan = "2">
Intermediate Event</td><td>
Interrupting </td></tr>
<tr>
<td>
Non-Interrupting</td></tr>
<tr>
<td>
End Event</td><td>
-----</td></tr>
</table>

**Representation of different BPMN events**
<table>
<tr>
<th>
Event</th><th>
Image</th></tr>
<tr>
<td>
Start –Interrupting</td><td>
<img src="/js/Diagram/Predefined-Shapes_images/Predefined-Shapes_img4.png" alt="" width="69pt" height="62pt"/></td></tr>
<tr>
<td>
Start Non Interrupting</td><td>
<img src="/js/Diagram/Predefined-Shapes_images/Predefined-Shapes_img5.png" alt="" width="68pt" height="63pt"/></td></tr>
<tr>
<td>
Intermediate Interrupting</td><td>
<img src="/js/Diagram/Predefined-Shapes_images/Predefined-Shapes_img6.png" alt="" width="66pt" height="62pt"/></td></tr>
<tr>
<td>
Intermediate Non-Interrupting</td><td>
<img src="/js/Diagram/Predefined-Shapes_images/Predefined-Shapes_img7.png" alt="" width="63pt" height="62pt"/></td></tr>
<tr>
<td>
End</td><td>
<img src="/js/Diagram/Predefined-Shapes_images/Predefined-Shapes_img8.png" alt="" width="63pt" height="62pt"/></td></tr>
</table>

**Representation of event trigger states**
<table>
<tr>
<th>
Trigger Result</th><th>
Image</th></tr>
<tr>
<td>
Message</td><td>
<img src="/js/Diagram/Predefined-Shapes_images/Predefined-Shapes_img9.png" alt="" width="44pt" height="44pt"/></td></tr>
<tr>
<td>
Timer</td><td>
<img src="/js/Diagram/Predefined-Shapes_images/Predefined-Shapes_img10.png" alt="" width="55pt" height="52pt"/></td></tr>
<tr>
<td>
Escalation</td><td>
<img src="/js/Diagram/Predefined-Shapes_images/Predefined-Shapes_img11.png" alt="" width="57pt" height="56pt"/></td></tr>
<tr>
<td>
Link </td><td>
<img src="/js/Diagram/Predefined-Shapes_images/Predefined-Shapes_img12.png" alt="" width="56pt" height="50pt"/></td></tr>
<tr>
<td>
Error</td><td>
<img src="/js/Diagram/Predefined-Shapes_images/Predefined-Shapes_img13.png" alt="" width="64pt" height="53pt"/></td></tr>
<tr>
<td>
Compensation</td><td>
<img src="/js/Diagram/Predefined-Shapes_images/Predefined-Shapes_img14.png" alt="" width="58pt" height="50pt"/></td></tr>
<tr>
<td>
Signal</td><td>
<img src="/js/Diagram/Predefined-Shapes_images/Predefined-Shapes_img15.png" alt="" width="52pt" height="56pt"/></td></tr>
<tr>
<td>
Multiple</td><td>
<img src="/js/Diagram/Predefined-Shapes_images/Predefined-Shapes_img16.png" alt="" width="55pt" height="57pt"/></td></tr>
<tr>
<td>
Parallel</td><td>
<img src="/js/Diagram/Predefined-Shapes_images/Predefined-Shapes_img17.png" alt="" width="58pt" height="54pt"/></td></tr>
</table>

### Gateway

Gateway is used to control the flow of a process. It is represented as a diamond shape. There are several types in Gateway. They are listed as follows.

1. None
2. Exclusive
3. Parallel
4. Inclusive
5. Complex
6. Event Based

The following code example illustrates how to create a gateway in BPMN shape.

{% highlight js %}
var diagram = ej.datavisualization.Diagram;
//Create a gateway shape in BPMN 
var node = {
   type: "bpmn",
   shape: diagram.BPMNShapes.Gateway
};
{% endhighlight %}

**Types of Gateway**
<table>
<tr>
<th>
Gateway Type</th><th>
Image</th></tr>
<tr>
<td>
Exclusive Gateway</td><td>
<img src="/js/Diagram/Predefined-Shapes_images/Predefined-Shapes_img18.png" alt="" width="77pt" height="74pt"/></td></tr>
<tr>
<td>
Parallel Gateway</td><td>
<img src="/js/Diagram/Predefined-Shapes_images/Predefined-Shapes_img19.png" alt="" width="70pt" height="68pt"/></td></tr>
<tr>
<td>
Inclusive Gateway</td><td>
<img src="/js/Diagram/Predefined-Shapes_images/Predefined-Shapes_img20.png" alt="" width="68pt" height="71pt"/></td></tr>
<tr>
<td>
Complex Gateway</td><td>
<img src="/js/Diagram/Predefined-Shapes_images/Predefined-Shapes_img21.png" alt="" width="67pt" height="70pt"/></td></tr>
<tr>
<td>
Event Based</td><td>
<img src="/js/Diagram/Predefined-Shapes_images/Predefined-Shapes_img22.png" alt="" width="68pt" height="68pt"/></td></tr>
</table>

### Activity

The activity is the task that is performed in a process. It is represented by rounded rectangle.

There are two types in activity. They are listed as follows.

1. Task: Occurs within a process and it is not broken down to finer level of detail.
2. Subprocess: Occurs within a process broken down to finer level of detail.

<table>
<tr>
<th>
Activity</th><th>
Loop</th><th>
Tasks</th><th>
Compensation</th><th>
Call</th><th>
Ad-Hoc</th><th>
Boundary</th></tr>
<tr>
<td>
<b>Task</b></td><td>
<b>&#10003;</b></td><td>
<b>&#10003;</b></td><td> 
<b>&#10003;</b></td><td>
<b>&#10003;</b></td><td>
<b>&#10005;</b></td><td>
<b>&#10005;</b></td></tr>
<tr>
<td>
<b>SubProcess</b></td><td>
<b>&#10003;</b></td><td>
<b>&#10005;</b></td><td>
<b>&#10003;</b></td><td>
<b>&#10005;</b></td><td>
<b>&#10003;</b></td><td>
<b>&#10003;</b></td></tr>
</table>

The following code example illustrate how to create activity in BPMN shape.

{% highlight js %}
var diagram = ej.datavisualization.Diagram;
//Create an activity shape in BPMN
var node = {
   type: "bpmn",
   shape: diagram.BPMNShapes.Activity,
   activity: diagram.BPMNActivity.Task
};
{% endhighlight %}

The different activities in the BPMN shape are listed as follows.

* Loop: The task that is internally being looped
{% include image.html url="/js/Diagram/Predefined-Shapes_images/Predefined-Shapes_img23.png" %}
* Tasks: The task for sending, receiving, user based task etc…
{% include image.html url="/js/Diagram/Predefined-Shapes_images/Predefined-Shapes_img24.png" %}
* Compensation: Compensation triggered when operation is partially failed.
{% include image.html url="/js/Diagram/Predefined-Shapes_images/Predefined-Shapes_img25.png" %}
* Call
{% include image.html url="/js/Diagram/Predefined-Shapes_images/Predefined-Shapes_img26.png" %}
* Ad-Hoc
{% include image.html url="/js/Diagram/Predefined-Shapes_images/Predefined-Shapes_img27.png" %}
* Boundary: Boundary represents the type of task that is being processed
{% include image.html url="/js/Diagram/Predefined-Shapes_images/Predefined-Shapes_img28.png" %}

### Data

Data object is used to represent “how data is produced by activities in process”. DataSource is used to read and write data.

### DataObject & Datasource

The following code example illustrate how to create connecting objects in BPMN shape.

{% highlight js %}
var node = [];
var diagram = ej.datavisualization.Diagram;
//Create a DataObject shape in BPMN
node = {
   type: "bpmn",
   shape: diagram.BPMNShapes.DataObject
};
//Create a DataSource shape in BPMN
node = {
   type: "bpmn",
   shape: diagram.BPMNShapes.DataObject
};
{% endhighlight %}

{% include image.html url="/js/Diagram/Predefined-Shapes_images/Predefined-Shapes_img29.png" %}
