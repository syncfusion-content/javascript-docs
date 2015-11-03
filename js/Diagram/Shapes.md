---
layout: post
title: Pick the type of node among the predefined nodes and shapes
description: How to choose the type of the node with respect to the requirement? 
platform: js
control: Diagram
documentation: ug
---

# Shapes

Diagram provides support to add different kind of nodes. They are as follows.

* Text Node
* Image Node
* Html Node
* Native Node
* Basic Shapes
* Flow Shapes
* BPMN Shapes

## Text

Texts can be added to the Diagram as text nodes. For text nodes, the `type` should be set as "text". In addition, you need to define the `textBlock` object that is used to define the `text` to be added and to customize the appearance of that text. The following code illustrates how to create a text node.

{% highlight js %}

var diagram = ej.datavisualization.Diagram;
//Creates a html node
var nodes = [{
	name: "textNode",
	offsetX: 100,
	offsetY: 100,
	width: 100,
	height: 50,
	//Sets type of the node
	type: diagram.Shapes.Text,
	//Customizes the appearances such as text, font, fill, and stroke.
	textBlock: {
		text: "Text Node",
		fontColor: "black",
		textAlign: diagram.TextAlign.Center
	}
}];

{% endhighlight %}

![](/js/Diagram/Shapes_images/Shapes_img59.png)

## Image
Diagram allows to add images as image nodes. For image nodes, the `type` should be set as "image". In addition, the `source` property of node enables you to set the image source. The following code illustrates how an **Image** node is created.

{% highlight js %}

var diagram = ej.datavisualization.Diagram;
//Creates an Image node
var nodes = [
	{
		name: "imageNode", offsetX: 100, offsetY: 100,
		width: 50, height: 50,
		
		//Sets type of the node as Image
		type: diagram.Shapes.Image,
		
		//Sets url of the image
		source: "sample/syncfusion.png"
	}
];

{% endhighlight %}

![](/js/Diagram/Shapes_images/Shapes_img60.png)

## HTML

**Html** elements can be embedded in the Diagram through **Html** type node. To create a html node, you need to set the `type` of node as "html". In addition, you need to set the id of html template to the `templateId` property of node. The following code illustrates how an **Html** node is created.

{% highlight html %}

<!--dependency scripts-->
<script src="http://borismoore.github.io/jsrender/jsrender.min.js"></script>
<!—define html element-->
<script id="htmlTemplate" type="text/x-jsrender">
	<div style="margin-left: 32px; margin-top: 18px">
		<input type="button" value="{{"{{"}}:value{{}}}}" />
	</div>
</script>

{% endhighlight %}

{% highlight js %}

// Defines JSON to create node with HTML element
var nodes = [{
	name: "htmlNode", offsetX: 100, offsetY: 100,
	width: 120, height: 60,
	
	//Sets type as Html
	type: ej.datavisualization.Diagram.Shapes.Html,
	
	//Sets id of html template
	templateId: "htmlTemplate",
	value: "Button"
}];

{% endhighlight %}

![](/js/Diagram/Shapes_images/Shapes_img61.png)

N> HTML node cannot be exported to image format, like JPEG, PNG, and BMP. It is by design that while exporting, Diagram is drawn in a canvas. Further, this canvas is exported into image formats. Currently, drawing in a canvas equivalent from all possible HTML is not feasible. Hence, this limitation. 

## Native

**Diagram** provides support to embed **SVG** element into a node. To create a native node, the `type` node should be set as "native". Also, you need to define the id of the svg template by using the `templateId` property of node. The following code illustrates how a **Native node** is created.

{% highlight html %}

<!--dependency scripts-->
<script src="http://borismoore.github.io/jsrender/jsrender.min.js"></script>
<!--define html element-->
<script id="svgTemplate" type="text/x-jsrender">
	<g>	
		<path d="M 58.813 0 H 3.182 L 30.998 24.141 L 58.813 0 Z M 32.644 34.425 C 32.133 34.87 31.567 35.095 31 35.095 S 29.867 34.87 29.353 34.425 L 1 9.826V 60 H 61 V 9.826 L 32.644 34.425Z"></path>
	</g>
</script>

{% endhighlight %}

{% highlight js %}

// Defines JSON to create node with HTML element
var nodes = [{
	name: "NativeNode", offsetX: 100, offsetY: 100,

	//Sets type as Native
	type: ej.datavisualization.Diagram.Shapes.Native,

	//Sets id of SVG element
	templateId: "svgTemplate",
	labels: [{text: "Mail"}]
}];

{% endhighlight %}

![](/js/Diagram/Shapes_images/Shapes_img62.png)

N> Like HTML node, Native node also cannot be exported to image format. Fill color of native node can be overridden by the inline style or fill of the SVG element specified in the template. 

## Basic Shapes

The Basic shapes are common shapes that are used to represent the geometrical information visually. To create basic shapes, the `type` of the node should be set as "basic". Its `shape` property can be set with any one of the inbuilts [basic shapes](/js/api/global "BasicShapes"). 
The following code example illustrates how to create a basic shape. 

{% highlight js %}

$("#diagram").ejDiagram({
	width: "100%",
	height: "100%",
	pageSettings: {
		scrollLimit: "diagram"
	},
	nodes: [{
		name: "node",
		width: 100,
		height: 70,
		offsetX: 100,
		offsetY: 100,
		borderWidth: 2,
		borderColor: "black",

		//Specifies the radius of rounded corner
		cornerRadius:10,

		//Sets the type of shape
		type: ej.datavisualization.Diagram.Shapes.Basic,

		//Sets the type of basic shape
		shape: ej.datavisualization.Diagram.BasicShapes.Rectangle
	}],
});

{% endhighlight %}

![](/js/Diagram/Shapes_images/Shapes_img1.png)

N> By default, the `type` property of node is set as "basic".

N> When the `shape` is not set for a basic shape, it is considered a "rectangle".

## Path

Path node is a commonly used basic shape that allows visually to represent the geometrical information. To create a path node, You need to specify the `type` as "basic" and the `shape` as "path. The `pathData` property of node allows you to define the path to be drawn. The following code illustrates how a Path node is created.

{% highlight js %}

// Defines JSON to create path node

var nodes = [{
	name: "pathNode", offsetX: 100, offsetY: 100,
	width: 120, height: 60,
	//By default, the type is considered as "basic"

	//Sets shape as Path
	shape: Diagram.BasicShapes.Path,

	//Defines svg pathdata
	pathData: "M35.2441,25 L22.7161,49.9937 L22.7161,0.00657536 L35.2441,25 z M22.7167,25 L-0.00131226,25 M35.2441,49.6337 L35.2441,0.368951 M35.2441,25 L49.9981,25"
}];

{% endhighlight %}

![](/js/Diagram/Shapes_images/Shapes_img58.png)

The list of basic shapes are as follows.

![](/js/Diagram/Shapes_images/Shapes_img2.png)

## Flow Shapes

The flow shapes are used to represent the process flow. It is used for analyzing, designing, and managing for documentation process. To create a flow shape, you need to specify the `type` as "flow". Its `shape` property can be set with any one of the inbuilts [flow shapes](/js/api/global "FlowShapes") and by default, it is considered as "process". The following code example illustrates how to create a flow shape. 

{% highlight js %}

$("#diagram").ejDiagram({
	width: "100%",
	height: "100%",
	pageSettings: {
		scrollLimit: "diagram"
	},
	nodes: [{
		name: "node",
		width: 100,
		height: 100,
		offsetX: 100,
		offsetY: 100,
		borderWidth: 2,
		borderColor: "black",
		//Sets the type of shape
		type: ej.datavisualization.Diagram.Shapes.Flow,
		//Sets the type of flow shape
		shape: ej.datavisualization.Diagram.FlowShapes.Document
	}],
});

{% endhighlight %}

![](/js/Diagram/Shapes_images/Shapes_img3.png)

The list of flow shapes are as follows.

![](/js/Diagram/Shapes_images/Shapes_img4.png)

## BPMN Shapes

BPMN shapes are used to represent the internal business procedure in a graphical notation and enables you to communicate the procedures in a standard manner. To create a bpmn shape, the `type` of the node should be set as "bpmn" and its `shape` should be set as any one of the inbuilts [BPMN Shapes](/js/api/global "BPMNShapes"). The following code example illustrates how to create a simple business process. 

{% highlight js %}

$("#diagram").ejDiagram({
	width: "100%",
	height: "100%",
	pageSettings: {
		scrollLimit: "diagram"
	},
	nodes: [{
		name: "node",
		width: 100,
		height: 100,
		offsetX: 100,
		offsetY: 100,
		borderWidth: 2,
		borderColor: "black",
		labels: [{
			text: "End Event"
		}],
		//Sets the type of shape as BPMN
		type: ej.datavisualization.Diagram.Shapes.BPMN,
		//Sets the type of bpmn shape
		shape: ej.datavisualization.Diagram.BPMNShapes.Event,
		//Sets type of the Event
		event: ej.datavisualization.Diagram.BPMNEvents.End
	}],
});

{% endhighlight %}

![](/js/Diagram/Shapes_images/Shapes_img5.png)

N> The default value for the property `shape` is "event".

The list of BPMN shapes are as follows.

| Shape | Image |
|---|---|
| Event | ![](/js/Diagram/Shapes_images/Shapes_img6.png) |
| Gateway | ![](/js/Diagram/Shapes_images/Shapes_img7.png) |
| Task | ![](/js/Diagram/Shapes_images/Shapes_img8.png) |
| Message | ![](/js/Diagram/Shapes_images/Shapes_img9.png) |
| DataSource | ![](/js/Diagram/Shapes_images/Shapes_img10.png) |
| DataObject | ![](/js/Diagram/Shapes_images/Shapes_img11.png) |

The BPMN shapes and its types are explained as follows.

### Event 

An event is notated with a circle and it represents an event in a business process. The type of events are as follows.

* Start
* End
* Intermediate

The `event` property of the node allows you to define the type of the event. The default value of the `event` is "start". The following code example illustrates how to create a BPMN Event.

{% highlight js %}

$("#diagram").ejDiagram({
	width: "100%",
	height: "100%",
	pageSettings: {
		scrollLimit: "diagram"
	},
	nodes: [{
		name: "node",
		width: 100,
		height: 100,
		offsetX: 100,
		offsetY: 100,
		borderWidth: 2,
		borderColor: "black",
		//Sets the type as BPMN
		type: ej.datavisualization.Diagram.Shapes.BPMN,
		//Sets the shape as BPMN Event
		shape: ej.datavisualization.Diagram.BPMNShapes.Event,
		//Sets type of the Event
		event: ej.datavisualization.Diagram.BPMNEvents.End,
		//Sets sub-type of the Event
		trigger: ej.datavisualization.Diagram.BPMNTriggers.None
	}],
});

{% endhighlight %}

![](/js/Diagram/Shapes_images/Shapes_img12.png)

| Event | Image |
|---|---|
| Start | ![](/js/Diagram/Shapes_images/Shapes_img13.png) |
| NonInterruptingStart | ![](/js/Diagram/Shapes_images/Shapes_img14.png) |
| Intermediate | ![](/js/Diagram/Shapes_images/Shapes_img15.png) |
| NonInterruptingIntermediate | ![](/js/Diagram/Shapes_images/Shapes_img16.png) |
| End | ![](/js/Diagram/Shapes_images/Shapes_img17.png) |

Event triggers are notated as icons inside the circle and they represent the specific details of the process. The `triggers` property of node allows you to set the type of trigger and by default, it is set as "none". The following table illustrates the type of event triggers.

| Triggers | Image |
|---|---|
| Message | ![](/js/Diagram/Shapes_images/Shapes_img18.png) |
| Compensation | ![](/js/Diagram/Shapes_images/Shapes_img19.png) |
| Error | ![](/js/Diagram/Shapes_images/Shapes_img20.png) |
| Escalation | ![](/js/Diagram/Shapes_images/Shapes_img21.png) |
| Link | ![](/js/Diagram/Shapes_images/Shapes_img22.png) |
| Multiple | ![](/js/Diagram/Shapes_images/Shapes_img23.png) |
| Parallel | ![](/js/Diagram/Shapes_images/Shapes_img24.png) |
| Signal | ![](/js/Diagram/Shapes_images/Shapes_img25.png) |
| Timer | ![](/js/Diagram/Shapes_images/Shapes_img26.png) |

### Gateway

Gateway is used to control the flow of a process. It is represented as a diamond shape. To create a gateway, the `shape` property of node should be set as "gateway" and the `gateway` property can be set with any of the appropriate [Gateways](/js/api/global "BPMNGateways"). The following code example illustrates how to create a BPMN Gateway.

{% highlight js %}

$("#diagram").ejDiagram({
	width: "100%",
	height: "100%",
	pageSettings: {
		scrollLimit: "diagram"
	},
	nodes: [{
		name: "node",
		width: 100,
		height: 100,
		offsetX: 100,
		offsetY: 100,
		borderWidth: 2,
		borderColor: "black",
		type: ej.datavisualization.Diagram.Shapes.BPMN,
		//Sets the shape as Gateway
		shape: ej.datavisualization.Diagram.BPMNShapes.Gateway,
		//Sets the type of BPMN Gateway
		gateway: ej.datavisualization.Diagram.BPMNGateways.None,
	}],
});

{% endhighlight %}

![](/js/Diagram/Shapes_images/Shapes_img27.png)

N> By default, the `gateway` will be set as "none".

There are several types of gateways as tabulated

| Gateways | Image |
|---|---|
| Complex | ![](/js/Diagram/Shapes_images/Shapes_img28.png) |
| EventBased | ![](/js/Diagram/Shapes_images/Shapes_img29.png) |
| Exclusive | ![](/js/Diagram/Shapes_images/Shapes_img30.png) |
| Inclusive | ![](/js/Diagram/Shapes_images/Shapes_img31.png) |
| Parallel | ![](/js/Diagram/Shapes_images/Shapes_img32.png) |

### Activity

The activity is the task that is performed in a business process. It is represented by a rounded rectangle.

There are two types of activities .They are listed as follows.

* Task – Occurs within a process and it is not broken down to finer level of detail.
* Subprocess – Occurs within a process and it is broken down to finer level of detail.

To create a BPMN activity, you need to set the `shape` as "activity". You also need to set the type of the [activity](/js/api/global "BPMNActivity") by using the `activity` property of node. By default, the type of the `activity` is set as "task". The following code example illustrates how to create an activity.

{% highlight js %}

$("#diagram").ejDiagram({
	width: "100%",
	height: "100%",
	pageSettings: {
		scrollLimit: "diagram"
	},
	nodes: [{
		name: "node",
		width: 100,
		height: 100,
		offsetX: 100,
		offsetY: 100,
		borderWidth: 2,
		borderColor: "black",
		type: ej.datavisualization.Diagram.Shapes.BPMN,
		//Sets the bpmn shape as activity
		shape: ej.datavisualization.Diagram.BPMNShapes.Activity,
		//Sets the type of BPMN Activity
		activity: ej.datavisualization.Diagram.BPMNActivity.Task,
	}],
});

{% endhighlight %}

![](/js/Diagram/Shapes_images/Shapes_img33.png)

The different activities of BPMN process are listed as follows.

#### Tasks

The `task` property of node allows you to define the `type` of task such as sending, receiving, user based task etc… By default, the `type` property of task is set as "none". The following code illustrates how to create different types of BPMN tasks. 

{% highlight js %}

$("#diagram").ejDiagram({
	width: "100%",
	height: "100%",
	pageSettings: {
		scrollLimit: "diagram"
	},
	nodes: [{
		name: "task",
		width: 100,
		height: 100,
		offsetX: 100,
		offsetY: 100,
		borderWidth: 2,
		borderColor: "black",
		type: ej.datavisualization.Diagram.Shapes.BPMN,
		//Sets the type of bpmn shape
		shape: ej.datavisualization.Diagram.BPMNShapes.Activity,
		//Sets the type of BPMN Activity
		activity: ej.datavisualization.Diagram.BPMNActivity.Task,
		//Sets the type of BPMN Task Activity
		task: {
			type: ej.datavisualization.Diagram.BPMNTasks.Send
		}
	}]
});

{% endhighlight %}

![](/js/Diagram/Shapes_images/Shapes_img34.png)

The various types of BPMN tasks are tabulated as follows.

| Task Type | Image |
|---|---|
| Service | ![](/js/Diagram/Shapes_images/Shapes_img35.png) |
| Send | ![](/js/Diagram/Shapes_images/Shapes_img36.png) |
| Receive | ![](/js/Diagram/Shapes_images/Shapes_img37.png) |
| Instantiating Receive | ![](/js/Diagram/Shapes_images/Shapes_img38.png) |
| Manual | ![](/js/Diagram/Shapes_images/Shapes_img39.png) |
| Business Rule | ![](/js/Diagram/Shapes_images/Shapes_img40.png) |
| User | ![](/js/Diagram/Shapes_images/Shapes_img41.png) |
| Script | ![](/js/Diagram/Shapes_images/Shapes_img42.png) |

#### Loop

Loop is a task that is internally being looped. The `loop` property of task allows you to define the type of loop. The default value for `loop` is "none". 

{% highlight js %}

var diagram = $("#diagram").ejDiagram("instance");

var node = {
	name: "task",
	width: 100,
	height: 100,
	offsetX: 100,
	offsetY: 100,
	borderWidth: 2,
	borderColor: "black",
	type: ej.datavisualization.Diagram.Shapes.BPMN,
	//Sets the type of BPMN shape
	shape: ej.datavisualization.Diagram.BPMNShapes.Activity,
	//Sets the type of BPMN Activity
	activity: ej.datavisualization.Diagram.BPMNActivity.Task,
	//Sets the type of bpmn loops.
	task: {
		loop: ej.datavisualization.Diagram.BPMNLoops.Standard
	}
};
diagram.add(node);

node = {
	name: "subprocess",
	width: 100,
	height: 100,
	offsetX: 300,
	offsetY: 100,
	borderWidth: 2,
	borderColor: "black",
	type: ej.datavisualization.Diagram.Shapes.BPMN,
	shape: ej.datavisualization.Diagram.BPMNShapes.Activity,
	//Sets the type of BPMN activity
	activity: ej.datavisualization.Diagram.BPMNActivity.SubProcess,
	//Sets the type of bpmn loops.
	subProcess: {
		loop: ej.datavisualization.Diagram.BPMNLoops.Standard
	}
};
diagram.add(node);

{% endhighlight %}

![](/js/Diagram/Shapes_images/Shapes_img43.png)

The following table contains various types of BPMN loops.

| Loops | Task | SubProcess |
|---|---|---|
| Standard | ![](/js/Diagram/Shapes_images/Shapes_img44.png) | ![](/js/Diagram/Shapes_images/Shapes_img45.png) |
| SequenceMultiInstance | ![](/js/Diagram/Shapes_images/Shapes_img46.png) | ![](/js/Diagram/Shapes_images/Shapes_img47.png) |
| ParallelMultiInstance | ![](/js/Diagram/Shapes_images/Shapes_img48.png) | ![](/js/Diagram/Shapes_images/Shapes_img49.png) |

#### Compensation

Compensation is triggered when operation is partially failed and you can enable it with the `compensation` property of task.

{% highlight js %}

var nodes = [];

nodes.push({
	name: "task",
	width: 100,
	height: 100,
	offsetX: 100,
	offsetY: 100,
	borderWidth: 2,
	borderColor: "black",
	type: ej.datavisualization.Diagram.Shapes.BPMN,
	shape: ej.datavisualization.Diagram.BPMNShapes.Activity
	//Sets the type of BPMN Activity
	activity: ej.datavisualization.Diagram.BPMNActivity.Task,
	//Creates compensation task
	task: {
		compensation: true
	}
});

nodes.push({
	name: "subprocess",
	width: 100,
	height: 100,
	offsetX: 300,
	offsetY: 100,
	borderWidth: 2,
	borderColor: "black",
	type: ej.datavisualization.Diagram.Shapes.BPMN,
	shape: ej.datavisualization.Diagram.BPMNShapes.Activity,
	//Sets the type of BPMN Activity
	activity: ej.datavisualization.Diagram.BPMNActivity.SubProcess,
	//Creates compensation subprocess 
	subProcess: {
		compensation: true
	}
});

$("#diagram").ejDiagram({
	width: "100%",
	height: "100%",
	pageSettings: {
		scrollLimit: "diagram"
	},
	nodes: nodes
});

{% endhighlight %}

![](/js/Diagram/Shapes_images/Shapes_img50.png)

#### Call

A call activity is a global sub-process that is reused at various points of the business flow and you can set it with the `call` property of task.

{% highlight js %}

$("#diagram").ejDiagram({
	width: "100%",
	height: "100%",
	pageSettings: {
		scrollLimit: "diagram"
	},
	nodes: [{
		name: "task",
		width: 100,
		height: 100,
		offsetX: 100,
		offsetY: 100,
		borderWidth: 2,
		borderColor: "black",
		type: ej.datavisualization.Diagram.Shapes.BPMN,
		shape: ej.datavisualization.Diagram.BPMNShapes.Activity,
		//Sets the type of BPMN Activity
		activity: ej.datavisualization.Diagram.BPMNActivity.Task,
		//Creates a call task
		task: {
			call: true
		}
	}]
});

{% endhighlight %}

![](/js/Diagram/Shapes_images/Shapes_img51.png)

#### Ad-Hoc

An ad hoc subprocess is a group of tasks that are executed in any order or skipped in order to fulfill the end condition and you can set it with the `adhoc` property of subprocess. 

{% highlight js %}

$("#diagram").ejDiagram({
	width: "100%",
	height: "100%",
	pageSettings: {
		scrollLimit: "diagram"
	},
	nodes: [{
		name: "task",
		width: 100,
		height: 100,
		offsetX: 100,
		offsetY: 100,
		borderWidth: 2,
		borderColor: "black",
		type: ej.datavisualization.Diagram.Shapes.BPMN,
		shape: ej.datavisualization.Diagram.BPMNShapes.Activity,
		activity: ej.datavisualization.Diagram.BPMNActivity.SubProcess,
		//Creates ad hoc subprocess
		subProcess: {
			adhoc: true
		}
	}]
});

{% endhighlight %}

![](/js/Diagram/Shapes_images/Shapes_img52.png)

#### Boundary

Boundary represents the type of task that is being processed. The `boundary` property of sub process allows you to define the type of boundary. By default, it is set as "default".

{% highlight js %}

$("#diagram").ejDiagram({
	width: "100%",
	height: "100%",
	pageSettings: {
		scrollLimit: "diagram"
	},
	nodes: [{
		name: "task",
		width: 100,
		height: 100,
		offsetX: 100,
		offsetY: 100,
		borderWidth: 2,
		borderColor: "black",
		type: ej.datavisualization.Diagram.Shapes.BPMN,
		shape: ej.datavisualization.Diagram.BPMNShapes.Activity,
		activity: ej.datavisualization.Diagram.BPMNActivity.SubProcess,
		//Adds boundary to a subprocess 
		subProcess: {
			boundary: ej.datavisualization.Diagram.BPMNBoundary.Call
		}
	}]
});

{% endhighlight %}

The following table contains various types of BPMN boundaries.

| Boundary | Image |
|---|---|
| Call | ![](/js/Diagram/Shapes_images/Shapes_img53.png) |
| Event | ![](/js/Diagram/Shapes_images/Shapes_img54.png) |
| Default | ![](/js/Diagram/Shapes_images/Shapes_img55.png) |

### Data

A data object represents information flowing through the process, such as data placed into the process, data resulting from the process, data that needs to be collected, or data that must be stored. To define a data object, set the `shape` as "dataobject". You can create multiple instances of data object with the `collection` property of node.

{% highlight js %}

$("#diagram").ejDiagram({
	width: "100%",
	height: "100%",
	pageSettings: {
		scrollLimit: "diagram"
	},
	nodes: [{
		name: "task",
		width: 100,
		height: 100,
		offsetX: 100,
		offsetY: 100,
		borderWidth: 2,
		borderColor: "black",
		//Sets the type of the shape
		type: ej.datavisualization.Diagram.Shapes.BPMN,
		//Sets the type of BPMN Shape
		shape: ej.datavisualization.Diagram.BPMNShapes.DataObject,
		//Sets collection as true when Dataobject is not a Single instance
		collection: true
	}]
});

{% endhighlight %}

![](/js/Diagram/Shapes_images/Shapes_img56.png)

### Datasource

DataSource is used to store or access data associated with a business process. To create a data source, set the `shape` as "datasource". The following code example illustrate how to create data source.

{% highlight js %}

$("#diagram").ejDiagram({
	width: "100%",
	height: "100%",
	pageSettings: {
		scrollLimit: "diagram"
	},
	nodes: [{
		name: "task",
		width: 100,
		height: 100,
		offsetX: 100,
		offsetY: 100,
		borderWidth: 2,
		borderColor: "black",
		//Sets type of the shape
		type: ej.datavisualization.Diagram.Shapes.BPMN,
		//Sets the type of bpmn shape
		shape: ej.datavisualization.Diagram.BPMNShapes.DataSource,
	}]
});

{% endhighlight %}

![](/js/Diagram/Shapes_images/Shapes_img57.png)
