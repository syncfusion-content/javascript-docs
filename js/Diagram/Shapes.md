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
* HTML Node
* Native Node
* Basic Shapes
* Flow Shapes
* BPMN Shapes

## Text

Texts can be added to the Diagram as text nodes. For text nodes, the `type` should be set as "text". In addition, you need to define the `textBlock` object that is used to define the `text` to be added and to customize the appearance of that text. The following code illustrates how to create a text node.

{% highlight javascript %}

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
Diagram allows to add images as image nodes. For image nodes, the `type` should be set as "image". In addition, the `source` property of node enables you to set the image source. 

The following code illustrates how an **Image** node is created.

{% highlight javascript %}

var diagram = ej.datavisualization.Diagram;
//Creates an Image node
var nodes = [{
	name: "imageNode", offsetX: 100, offsetY: 100,
	width: 50, height: 50,
	
	//Sets type of the node as Image
	type: diagram.Shapes.Image,
	
	//Sets url of the image
	source: "sample/syncfusion.png"
}];

{% endhighlight %}

![](/js/Diagram/Shapes_images/Shapes_img60.png)

N> Deploy your HTML file in the web Application and export the diagram (image node) or else the image node will not be exported in the chrome and Firefox due to security issues. Please refer to the link below.

Link: http://asked.online/draw-images-on-canvas-locally-using-chrome/2546077/

Link1: http://stackoverflow.com/questions/4761711/local-image-in-canvas-in-chrome

### Image Alignment

You can stretch and align the image content anywhere but within the node boundary.

The `contentAlignment` property of node allows to align an image within the node boundary. The `scale` property of node allows to stretch the image as you desired (either to maintain proportion or to stretch). By default, the `scale` property of node is set as "meet".
The following code illustrates how to scale or stretch the content of the image node.

{% highlight javascript %}

// Defines JSON to create node with image
var nodes = [{
	name: "imageNode", 
	width: 100, 
	height: 60, 
	offsetX: 40, 
	offsetY: 40,
	type: ej.datavisualization.Diagram.Shapes.Image,
	source: "sample/emlpoyee.png"
	borderWidth:3,
	borderColor:"white",
}];
//Initializes Diagram
$("#diagram").ejDiagram({
	width: "100%", 
	height: "100%",
	//Initializes nodes collection
	nodes: nodes,
});

{% endhighlight %}

The following tables illustrates all the possible scale options for the image node

| Values| Image |
|---|---|
| None | ![](/js/Diagram/Shapes_images/Shapes_img128.png) |
| Meet | ![](/js/Diagram/Shapes_images/Shapes_img129.png) |
| Slice | ![](/js/Diagram/Shapes_images/Shapes_img130.png) |
| Stretch | ![](/js/Diagram/Shapes_images/Shapes_img131.png) |


## HTML

**Html** elements can be embedded in the Diagram through **Html** type node. To create a HTML node, you need to set the `type` of node as "html". In addition, you need to set the id of HTML template to the `templateId` property of node. The following code illustrates how an **Html** node is created.

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

{% highlight javascript %}

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

**Diagram** provides support to embed **SVG** element into a node. To create a native node, the `type` node should be set as "native". Also, you need to define the id of the SVG template by using the `templateId` property of node. The following code illustrates how a **Native node** is created.

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

{% highlight javascript %}

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

### SVG content alignment

You can stretch and align the svg content anywhere but within the node boundary.

The `contentAlignment` property of node allows to align the svg content within the node boundaries. The `scale` property of node allows to stretch the svg content as you desired(either to maintain proportion or to stretch).By default, the `scale` property of node is set as "meet".
The following code illustrates how to scale or stretch the content of the node.

{% highlight html %}

<!--dependency scripts-->
<script src="http://borismoore.github.io/jsrender/jsrender.min.js"></script>
<!--define html element-->
<script id="svgTemplate" type="text/x-jsrender">
	<g>	
		<ellipse  ry="35" rx="37" id="svg_1" cy="139" cx="215.5"  />
	</g>
</script>

{% endhighlight %}

{% highlight javascript %}

// Defines JSON to create node with SVG element
var nodes = [{
	name: "NativeNode", 
	width: 100, 
	height: 60, 
	offsetX: 40, 
	offsetY: 40,
	fillColor:"darkcyan",
	borderWidth:3,
	borderColor:"black",

	//Sets type as Native
	type: ej.datavisualization.Diagram.Shapes.Native,

	//Sets id of SVG element
	templateId: "svgTemplate",
}];
//Initializes Diagram
$("#diagram").ejDiagram({
	width: "100%", 
	height: "100%",
	//Initializes nodes collection
	nodes: nodes,
});

{% endhighlight %}

The following tables illustrates all the possible scale options for the node

| Values| Image |
|---|---|
| None | ![](/js/Diagram/Shapes_images/Shapes_img124.png) |
| Meet | ![](/js/Diagram/Shapes_images/Shapes_img125.png) |
| Slice | ![](/js/Diagram/Shapes_images/Shapes_img126.png) |
| Stretch | ![](/js/Diagram/Shapes_images/Shapes_img127.png) |

## Basic Shapes

The Basic shapes are common shapes that are used to represent the geometrical information visually. To create basic shapes, the `type` of the node should be set as "basic". Its `shape` property can be set with any one of the built-in shape. [Basic Shapes](/js/api/global#basicshapes "Basic Shapes"). 
The following code example illustrates how to create a basic shape. 

{% highlight javascript %}

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

Path node is a commonly used basic shape that allows visually to represent the geometrical information. To create a path node, You need to specify the `type` as "basic" and the `shape` as "path". The `pathData` property of node allows you to define the path to be drawn. The following code illustrates how a Path node is created.

{% highlight javascript %}

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

The flow shapes are used to represent the process flow. It is used for analyzing, designing, and managing for documentation process. To create a flow shape, you need to specify the `type` as "flow". Its `shape` property can be set with any one of the built-in shape. [Flow Shapes](/js/api/global#flowshapes "Flow Shapes") and by default, it is considered as "process". The following code example illustrates how to create a flow shape. 

{% highlight javascript %}

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

BPMN shapes are used to represent the internal business procedure in a graphical notation and enables you to communicate the procedures in a standard manner. To create a BPMN shape, the `type` of the node should be set as "bpmn" and its `shape` should be set as any one of the built-in shape. [BPMN Shapes](/js/api/global#bpmnshapes "BPMN Shapes"). The following code example illustrates how to create a simple business process. 

{% highlight javascript %}

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
| Group | ![](/js/Diagram/Shapes_images/Shapes_img12.png) |

The BPMN shapes and its types are explained as follows.

### Event 

An event is notated with a circle and it represents an event in a business process. The type of events are as follows.

* Start
* End
* Intermediate

The `event` property of the node allows you to define the type of the event. The default value of the `event` is "start". The following code example illustrates how to create a BPMN Event.

{% highlight javascript %}

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

![](/js/Diagram/Shapes_images/Shapes_img13.png)

Event triggers are notated as icons inside the circle and they represent the specific details of the process. The `triggers` property of node allows you to set the type of trigger and by default, it is set as "none". The following table illustrates the type of event triggers.

| Triggers | Start | Non-Interrupting Start | Intermediate | Non-Interrupting Intermediate | Throwing Intermediate | End |
| --- | --- | --- | --- | --- | --- | --- |
| None | ![](/js/Diagram/Shapes_images/Shapes_img63.png) | ![](/js/Diagram/Shapes_images/Shapes_img64.png) | ![](/js/Diagram/Shapes_images/Shapes_img65.png) | ![](/js/Diagram/Shapes_images/Shapes_img66.png) |   | ![](/js/Diagram/Shapes_images/Shapes_img67.png) |
| Message | ![](/js/Diagram/Shapes_images/Shapes_img68.png) | ![](/js/Diagram/Shapes_images/Shapes_img69.png) | ![](/js/Diagram/Shapes_images/Shapes_img70.png) | ![](/js/Diagram/Shapes_images/Shapes_img71.png) | ![](/js/Diagram/Shapes_images/Shapes_img72.png) | ![](/js/Diagram/Shapes_images/Shapes_img73.png) |
| Timer | ![](/js/Diagram/Shapes_images/Shapes_img74.png) | ![](/js/Diagram/Shapes_images/Shapes_img75.png) | ![](/js/Diagram/Shapes_images/Shapes_img76.png) | ![](/js/Diagram/Shapes_images/Shapes_img77.png) |   |   |
| Conditional | ![](/js/Diagram/Shapes_images/Shapes_img78.png) | ![](/js/Diagram/Shapes_images/Shapes_img79.png) | ![](/js/Diagram/Shapes_images/Shapes_img80.png) | ![](/js/Diagram/Shapes_images/Shapes_img81.png) |   |   |
| Link |   |   | ![](/js/Diagram/Shapes_images/Shapes_img82.png) |   | ![](/js/Diagram/Shapes_images/Shapes_img83.png) |   |
| Signal | ![](/js/Diagram/Shapes_images/Shapes_img84.png) | ![](/js/Diagram/Shapes_images/Shapes_img85.png) | ![](/js/Diagram/Shapes_images/Shapes_img86.png) | ![](/js/Diagram/Shapes_images/Shapes_img87.png) | ![](/js/Diagram/Shapes_images/Shapes_img88.png) | ![](/js/Diagram/Shapes_images/Shapes_img89.png) |
| Error | ![](/js/Diagram/Shapes_images/Shapes_img90.png) |   | ![](/js/Diagram/Shapes_images/Shapes_img91.png) |   |   | ![](/js/Diagram/Shapes_images/Shapes_img92.png) |
| Escalation | ![](/js/Diagram/Shapes_images/Shapes_img93.png) | ![](/js/Diagram/Shapes_images/Shapes_img94.png) | ![](/js/Diagram/Shapes_images/Shapes_img95.png) | ![](/js/Diagram/Shapes_images/Shapes_img96.png) | ![](/js/Diagram/Shapes_images/Shapes_img97.png) | ![](/js/Diagram/Shapes_images/Shapes_img98.png) |
| Termination |   |   |   |   |   | ![](/js/Diagram/Shapes_images/Shapes_img99.png) |
| Compensation | ![](/js/Diagram/Shapes_images/Shapes_img100.png) |   | ![](/js/Diagram/Shapes_images/Shapes_img101.png) |   | ![](/js/Diagram/Shapes_images/Shapes_img102.png) | ![](/js/Diagram/Shapes_images/Shapes_img103.png) |
| Cancel |   |   | ![](/js/Diagram/Shapes_images/Shapes_img104.png) |   |   | ![](/js/Diagram/Shapes_images/Shapes_img105.png) |
| Multiple | ![](/js/Diagram/Shapes_images/Shapes_img106.png) | ![](/js/Diagram/Shapes_images/Shapes_img107.png) | ![](/js/Diagram/Shapes_images/Shapes_img108.png) | ![](/js/Diagram/Shapes_images/Shapes_img109.png) | ![](/js/Diagram/Shapes_images/Shapes_img110.png) | ![](/js/Diagram/Shapes_images/Shapes_img111.png) |
| Parallel | ![](/js/Diagram/Shapes_images/Shapes_img112.png) | ![](/js/Diagram/Shapes_images/Shapes_img113.png) | ![](/js/Diagram/Shapes_images/Shapes_img114.png) | ![](/js/Diagram/Shapes_images/Shapes_img115.png) |   |   |

### Gateway

Gateway is used to control the flow of a process. It is represented as a diamond shape. To create a gateway, the `shape` property of node should be set as "gateway" and the `gateway` property can be set with any of the appropriate [Gateways](/js/api/global#bpmngateways "Gateways"). The following code example illustrates how to create a BPMN Gateway.

{% highlight javascript %}

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

![](/js/Diagram/Shapes_images/Shapes_img25.png)

N> By default, the `gateway` will be set as "none".

There are several types of gateways as tabulated

| Gateways | Image |
|---|---|
| Complex | ![](/js/Diagram/Shapes_images/Shapes_img26.png) |
| EventBased | ![](/js/Diagram/Shapes_images/Shapes_img27.png) |
| Exclusive | ![](/js/Diagram/Shapes_images/Shapes_img28.png) |
| Inclusive | ![](/js/Diagram/Shapes_images/Shapes_img29.png) |
| Parallel | ![](/js/Diagram/Shapes_images/Shapes_img30.png) |
| ExclusiveEventBased | ![](/js/Diagram/Shapes_images/Shapes_img31.png) |
| ParallelEventBased | ![](/js/Diagram/Shapes_images/Shapes_img32.png) |

### Activity

The activity is the task that is performed in a business process. It is represented by a rounded rectangle.

There are two types of activities .They are listed as follows.

* Task – Occurs within a process and it is not broken down to finer level of detail.
* Subprocess – Occurs within a process and it is broken down to finer level of detail.

To create a BPMN activity, you need to set the `shape` as "activity". You also need to set the type of the [BPMN Activity](/js/api/global#bpmnactivity "BPMN Activity") by using the `activity` property of node. By default, the type of the `activity` is set as "task". The following code example illustrates how to create an activity.

{% highlight javascript %}

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

{% highlight javascript %}

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

#### Subprocess

A sub-process is a group of tasks which is used to hide or reveal details of additional levels which can be done using `collapsed` property .

 {% highlight javascript %}

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
		//Sets the type of bpmn shape
		shape: ej.datavisualization.Diagram.BPMNShapes.Activity,
		//Sets the type of BPMN Activity
		activity: ej.datavisualization.Diagram.BPMNActivity.SubProcess,
		//Sets the state of BPMN Subprocess
		subProcess: {
			collapsed: true,
		}
	}]
});

{% endhighlight %}

![](/js/Diagram/Shapes_images/Shapes_img116.png)

The different types of subprocess are as follows.

* Event Subprocess
* Transaction 

##### Event Subprocess

A Sub-process is defined as an Event Sub-process when it is triggered by an event. An event-subprocess is placed within another subprocess which is not part of the normal flow of its parent process . You can set event to a sub-process with the `event` and `trigger` property of subprocess. 

 {% highlight javascript %}

$("#diagram").ejDiagram({
	width: "100%",
	height: "100%",
	pageSettings: {
		scrollLimit: "diagram"
	},
	nodes: [{
		name: "eventSubProcess",
		width: 100,
		height: 100,
		offsetX: 100,
		offsetY: 100,
		borderWidth: 2,
		borderColor: "black",
		type: ej.datavisualization.Diagram.Shapes.BPMN,
		shape: ej.datavisualization.Diagram.BPMNShapes.Activity,
		activity: ej.datavisualization.Diagram.BPMNActivity.SubProcess,
		//Creates event subprocess
		subProcess: {
			type: ej.datavisualization.Diagram.BPMNSubProcessTypes.Event,
			event: ej.datavisualization.Diagram.BPMNEvents.Start,
			trigger: ej.datavisualization.Diagram.BPMNTriggers.Message
		}
	}]
});

{% endhighlight %}

![](/js/Diagram/Shapes_images/Shapes_img117.png)

##### Transaction Subprocess

An transaction is a set of activities that logically belong together, in which all contained activities must complete their parts of the transaction; otherwise the process is undone. The execution result of a transaction is one of Successful Completion, Unsuccessful Completion (Cancel), and Hazard (Exception). The `events` property of subprocess allows to represent these results as an event attached to the subprocess. 

 {% highlight javascript %}

$("#diagram").ejDiagram({
	width: "100%",
	height: "100%",
	pageSettings: {
		scrollLimit: "diagram"
	},
	nodes: [{
		name: "transactionSubProcess",
		width: 130,
		height: 100,
		offsetX: 100,
		offsetY: 100,
		borderWidth: 2,
		borderColor: "black",
		type: ej.datavisualization.Diagram.Shapes.BPMN,
		shape: ej.datavisualization.Diagram.BPMNShapes.Activity,
		activity: ej.datavisualization.Diagram.BPMNActivity.SubProcess,
		//Creates tranaction subprocess
		subProcess: {
			type: ej.datavisualization.Diagram.BPMNSubProcessTypes.Transaction,
			// Defines a collection of events to be attached 
			events: [
				//Defines type of the event and the position relative to the subprocess. 
				{ event: "intermediate", trigger: "cancel", offset: { x: 0.25, y: 1 } },
				{ event: "intermediate", trigger: "error", offset: { x: 0.75, y: 1 } }
			]
		}
	}]
});

{% endhighlight %}

![](/js/Diagram/Shapes_images/Shapes_img118.png)

#### Loop

Loop is a task that is internally being looped. The `loop` property of task allows you to define the type of loop. The default value for `loop` is "none". 

{% highlight javascript %}

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

{% highlight javascript %}

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

{% highlight javascript %}

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

{% highlight javascript %}

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

{% highlight javascript %}

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

A data object represents information flowing through the process, such as data placed into the process, data resulting from the process, data that needs to be collected, or data that must be stored. To define a data object, set the `shape` as "dataobject" and `type` property defines wheather data is an input or a output. You can create multiple instances of data object with the `collection` property of data.

{% highlight javascript %}

$("#diagram").ejDiagram({
	width: "100%",
	height: "100%",
	pageSettings: {
		scrollLimit: "diagram"
	},
	nodes: [{
		name: "dataObject",
		width: 75,
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
		data: {
			type: type: ej.datavisualization.Diagram.BPMNDataObjects.Input
			collection: true
		}
	}]
});

{% endhighlight %}

![](/js/Diagram/Shapes_images/Shapes_img56.png)

The following table contains various representation of BPMN Data Object.

| Boundary | Image |
|---|---|
| Collection Data Object | ![](/js/Diagram/Shapes_images/Shapes_img119.png) |
| Data Input | ![](/js/Diagram/Shapes_images/Shapes_img120.png) |
| Data Ouptput | ![](/js/Diagram/Shapes_images/Shapes_img121.png) |

### Datasource

DataSource is used to store or access data associated with a business process. To create a data source, set the `shape` as "datasource". The following code example illustrate how to create data source.

{% highlight javascript %}

$("#diagram").ejDiagram({
	width: "100%",
	height: "100%",
	pageSettings: {
		scrollLimit: "diagram"
	},
	nodes: [{
		name: "dataSource",
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

### Artifact

Artifact is used to show additional information about a Process in order to make it easier to understand. There are 2 types of artifacts in BPMN.

* Text Annotation
* Group

#### Text Annoatation

A BPMN object can be associated with a text annotation which does not affect the flow but gives details about objects within a flow. The `annotation` property of the node is used to connect an annotation element to the BPNN node.

 {% highlight javascript %}

$("#diagram").ejDiagram({
	width: "100%",
	height: "100%",
	pageSettings: {
		scrollLimit: "diagram"
	},
	nodes: [{
		name: "data",
		width: 75,
		height: 100,
		offsetX: 100,
		offsetY: 100,
		borderWidth: 2,
		borderColor: "black",
		//Sets type of the shape
		type: ej.datavisualization.Diagram.Shapes.BPMN,
		//Sets the type of bpmn shape
		shape: ej.datavisualization.Diagram.BPMNShapes.DataObject,
		//Sets collection as true when Dataobject is not a Single instance
		data: { collection: true },
		annotation: {
			//Sets the text to annotate the bpmn shape
			text: "Data Collection",
			//Sets the angle between the bpmn shape and the annotation
			angle: 45,
			//Sets the dimensions of the text
			width: 100, height: 40,
			//Sets the distance between the bpmn shape and the annotation 
			length: 150
		} 
	}]
});

{% endhighlight %}

![](/js/Diagram/Shapes_images/Shapes_img122.png)

#### Group

A group is used to frame a part of the diagram, shows that elements included in it are logically belong together and don't have any other semantics other than organizing elements. To create a Group, the `shape` property of node should be set as "group". The following code example illustrates how to create a BPMN Group.

 {% highlight javascript %}

$("#diagram").ejDiagram({
	width: "100%",
	height: "100%",
	pageSettings: {
		scrollLimit: "diagram"
	},
	nodes: [{
		name: "group",
		width: 100,
		height: 100,
		offsetX: 100,
		offsetY: 100,
		borderWidth: 2,
		borderColor: "black",
		//Sets type of the shape
		type: ej.datavisualization.Diagram.Shapes.BPMN,
		//Sets the type of bpmn shape
		shape: ej.datavisualization.Diagram.BPMNShapes.Group, 
	}]
});

{% endhighlight %}

![](/js/Diagram/Shapes_images/Shapes_img123.png)