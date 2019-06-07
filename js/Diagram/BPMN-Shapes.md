---
layout: post
title: BPMN-Shapes | Diagram | Javascript | Syncfusion
description: This section explains about how to graphically notate the internal business procedure in ejDiagram control? 
platform: js
control: Diagram
documentation: ug
api: /api/js/ejdiagram
---

### BPMN Shapes

BPMN shapes are used to represent the internal business procedure in a graphical notation and enables you to communicate the procedures in a standard manner. To create a BPMN shape, the [type](/api/js/ejdiagram#members:nodes-type "type") of the node should be set as "bpmn" and its [shape](/api/js/ejdiagram#members:nodes-shape "shape") should be set as any one of the built-in shape. [BPMN Shapes](/api/js/global#bpmnshapes "BPMN Shapes"). The following code example illustrates how to create a simple business process. 

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

![BPMN Shapes](Shapes_images/Shapes_img5.png)

N> The default value for the property `shape` is "event".

The list of BPMN shapes are as follows.

| Shape | Image |
|---|---|
| Event | ![BPMN Event Shape](Shapes_images/Shapes_img6.png) |
| Gateway | ![BPMN Gateway Shape](Shapes_images/Shapes_img7.png) |
| Task | ![BPMN Task Shape](Shapes_images/Shapes_img8.png) |
| Message | ![BPMN Message Shape](Shapes_images/Shapes_img9.png) |
| DataSource | ![BPMN DataSource Shape](Shapes_images/Shapes_img10.png) |
| DataObject | ![BPMN DataObject Shape](Shapes_images/Shapes_img11.png) |
| Group | ![BPMN Group Shape](Shapes_images/Shapes_img12.png) |

The BPMN shapes and its types are explained as follows.

### Event 

An event is notated with a circle and it represents an event in a business process. The type of events are as follows.

* Start
* End
* Intermediate

The [event](/api/js/ejdiagram#members:nodes-event "event")  property of the node allows you to define the type of the event. The default value of the `event` is "start". The following code example illustrates how to create a BPMN Event.

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

![BPMN Event End Shapes](Shapes_images/Shapes_img13.png)

Event triggers are notated as icons inside the circle and they represent the specific details of the process. The [trigger](/api/js/ejdiagram#members:nodes-trigger "trigger") property of node allows you to set the type of trigger and by default, it is set as "none". The following table illustrates the type of event triggers.

| Triggers | Start | Non-Interrupting Start | Intermediate | Non-Interrupting Intermediate | Throwing Intermediate | End |
| --- | --- | --- | --- | --- | --- | --- |
| None | ![Start](Shapes_images/Shapes_img63.png) | ![Non-Interrupting Start](Shapes_images/Shapes_img64.png) | ![Intermediate](Shapes_images/Shapes_img65.png) | ![Throwing Intermediate](Shapes_images/Shapes_img66.png) |   | ![End](Shapes_images/Shapes_img67.png) |
| Message | ![Start Message](Shapes_images/Shapes_img68.png) | ![Non-Interrupting Start Message](Shapes_images/Shapes_img69.png) | ![Intermediate Message shape](Shapes_images/Shapes_img70.png) | ![Non-Interrupting message shape](Shapes_images/Shapes_img71.png) | ![Throwing Intermediate message shape](Shapes_images/Shapes_img72.png) | ![End Message shape](Shapes_images/Shapes_img73.png) |
| Timer | ![Start timer shape](Shapes_images/Shapes_img74.png) | ![Non-Interrupting Start timer shape](Shapes_images/Shapes_img75.png) | ![Intermediate timer shape](Shapes_images/Shapes_img76.png) | ![Non-Interrupting Intermediate timer shape](Shapes_images/Shapes_img77.png) |   |   |
| Conditional | ![Conditional Start shape](Shapes_images/Shapes_img78.png) | ![Conditional Non-Interrupting Start](Shapes_images/Shapes_img79.png) | ![Conditional Intermediate](Shapes_images/Shapes_img80.png) | ![Conditional Non-Interrupting Intermediate](Shapes_images/Shapes_img81.png) |   |   |
| Link |   |   | ![Link Intermediate shape](Shapes_images/Shapes_img82.png) |   | ![Link Throwing Intermediate](Shapes_images/Shapes_img83.png) |   |
| Signal | ![Start Signal shape](Shapes_images/Shapes_img84.png) | ![Non-Interrupting Start Signal shape](Shapes_images/Shapes_img85.png) | ![Intermediate Signal shape](Shapes_images/Shapes_img86.png) | ![Non-Interrupting Intermediate Signal shape](Shapes_images/Shapes_img87.png) | ![Throwing Intermediate Signal shape](Shapes_images/Shapes_img88.png) | ![End Signal shape](Shapes_images/Shapes_img89.png) |
| Error | ![Start Error shape](Shapes_images/Shapes_img90.png) |   | ![Intermediate Error shape](Shapes_images/Shapes_img91.png) |   |   | ![End Error shape](Shapes_images/Shapes_img92.png) |
| Escalation | ![Start Escalation shape](Shapes_images/Shapes_img93.png) | ![Non-Interrupting Start Escalation shape](Shapes_images/Shapes_img94.png) | ![Intermediate Escalation shape](Shapes_images/Shapes_img95.png) | ![Non-Interrupting Intermediate Escalation shape](Shapes_images/Shapes_img96.png) | ![Throwing Intermediate Escalation shape](Shapes_images/Shapes_img97.png) | ![End Escalation shape](Shapes_images/Shapes_img98.png) |
| Termination |   |   |   |   |   | ![End Termination shape](Shapes_images/Shapes_img99.png) |
| Compensation | ![Start Compensation shape](Shapes_images/Shapes_img100.png) |   | ![Intermediate Compensation shape](Shapes_images/Shapes_img101.png) |   | ![Throwing Intermediate Compensation shape](Shapes_images/Shapes_img102.png) | ![End Compensation shape](Shapes_images/Shapes_img103.png) |
| Cancel |   |   | ![Intermediate Cancel shape](Shapes_images/Shapes_img104.png) |   |   | ![End Cancel shape](Shapes_images/Shapes_img105.png) |
| Multiple | ![Start Multiple shape](Shapes_images/Shapes_img106.png) | ![Non-Interrupting Start Multiple shape](Shapes_images/Shapes_img107.png) | ![Intermediate Multiple shape](Shapes_images/Shapes_img108.png) | ![Non-Interrupting Intermediate Multiple shape](Shapes_images/Shapes_img109.png) | ![Throwing Intermediate Multiple shape](Shapes_images/Shapes_img110.png) | ![End Multiple shape](Shapes_images/Shapes_img111.png) |
| Parallel | ![Start Parallel shape](Shapes_images/Shapes_img112.png) | ![Non-Interrupting Start Parallel shape](Shapes_images/Shapes_img113.png) | ![Intermediate Parallel shape](Shapes_images/Shapes_img114.png) | ![Non-Interrupting Intermediate Parallel shape](Shapes_images/Shapes_img115.png) |   |   |

### Gateway

Gateway is used to control the flow of a process. It is represented as a diamond shape. To create a gateway, the [shape](/api/js/ejdiagram#members:nodes-shape "shape") property of node should be set as "gateway" and the [gateway](/api/js/ejdiagram#members:nodes-gateway "gateway") property can be set with any of the appropriate [Gateways](/api/js/global#bpmngateways "Gateways"). The following code example illustrates how to create a BPMN Gateway.

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

![Gateway](Shapes_images/Shapes_img25.png)

N> By default, the `gateway` will be set as "none".

There are several types of gateways as tabulated

| Gateways | Image |
|---|---|
| Exclusive | ![Exclusive shape](Shapes_images/Shapes_img26.png) |
| Parallel | ![Parallel shape](Shapes_images/Shapes_img27.png) |
| Inclusive | ![Inclusive shape](Shapes_images/Shapes_img28.png) |
| Complex | ![Complex shape](Shapes_images/Shapes_img29.png) |
| EventBased | ![EventBased shape](Shapes_images/Shapes_img30.png) |
| ExclusiveEventBased | ![ExclusiveEventBased shape](Shapes_images/Shapes_img31.png) |
| ParallelEventBased | ![ParallelEventBased shape](Shapes_images/Shapes_img32.png) |

### Activity

The activity is the task that is performed in a business process. It is represented by a rounded rectangle.

There are two types of activities .They are listed as follows.

* Task – Occurs within a process and it is not broken down to finer level of detail.
* Subprocess – Occurs within a process and it is broken down to finer level of detail.

To create a BPMN activity, you need to set the [shape](/api/js/ejdiagram#members:nodes-shape "shape") as "activity". You also need to set the type of the [BPMN Activity](/api/js/global#bpmnactivity "BPMN Activity") by using the [activity](/api/js/ejdiagram#members:nodes-activity "activity") property of node. By default, the type of the `activity` is set as "task". The following code example illustrates how to create an activity.

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

![Activity shape](Shapes_images/Shapes_img33.png)

The different activities of BPMN process are listed as follows.

#### Tasks

The [task](/api/js/ejdiagram#members:nodes-task "task") property of node allows you to define the [type](/api/js/ejdiagram#members:nodes-tasks-type "type") of task such as sending, receiving, user based task etc… By default, the `type` property of task is set as "none". The following code illustrates how to create different types of BPMN tasks. 
The [events](/api/js/ejdiagram#members:nodes-tasks-events "events") property of tasks allows to represent these results as an event attached to the task.

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

![Tasks shape](Shapes_images/Shapes_img34.png)

The various types of BPMN tasks are tabulated as follows.

| Task Type | Image |
|---|---|
| Service | ![Service shape](Shapes_images/Shapes_img35.png) |
| Send | ![Send shape](Shapes_images/Shapes_img34.png) |
| Receive | ![Receive shape](Shapes_images/Shapes_img37.png) |
| Instantiating Receive | ![Instantiating Receive shape](Shapes_images/Shapes_img38.png) |
| Manual | ![Manual shape](Shapes_images/Shapes_img39.png) |
| Business Rule | ![Business Rule shape](Shapes_images/Shapes_img40.png) |
| User | ![User shape](Shapes_images/Shapes_img41.png) |
| Script | ![Script shape](Shapes_images/Shapes_img42.png) |

#### Subprocess

A [sub-process](/api/js/ejdiagram#members:nodes-subprocess "sub-process") is a group of tasks which is used to hide or reveal details of additional levels which can be done using [collapsed](/api/js/ejdiagram#members:nodes-subprocess-collapsed "collapsed") property .

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

![Subprocess shape](Shapes_images/Shapes_img116.png)

The different types of subprocess are as follows. 

* Event Subprocess
* Transaction 

##### Event Subprocess

A Sub-process is defined as an Event Sub-process when it is triggered by an event. An event-subprocess is placed within another subprocess which is not part of the normal flow of its parent process . You can set event to a sub-process with the [event](/api/js/ejdiagram#members:nodes-subprocess-event "event") and [trigger](/api/js/ejdiagram#members:nodes-subprocess-trigger "trigger") property of subprocess. The [type](/api/js/ejdiagram#members:nodes-subprocess-type "type") property of sub-process allows you to define type of sub-process whether it should be event sub-process or transaction sub-process.

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

![Event Subprocess shape](Shapes_images/Shapes_img117.png)

##### Transaction Subprocess

* An transaction is a set of activities that logically belong together, in which all contained activities must complete their parts of the transaction; otherwise the process is undone. The execution result of a transaction is one of Successful Completion, Unsuccessful Completion (Cancel), and Hazard (Exception). The [events](/api/js/ejdiagram#members:nodes-subprocess-events "events") property of subprocess allows to represent these results as an event attached to the subprocess. 

* The [event](/api/js/ejdiagram#members:nodes-subprocess-events-event "event") object allows you define the type of event by which the sub-process will be triggered. Also you can define [name](/api/js/ejdiagram#members:nodes-subprocess-events-name "name") of the event to identify the event at runtime.

* The event's [offset](/api/js/ejdiagram#members:nodes-subprocess-events-offset "offset") property is used to set the fraction/ratio(relative to parent) that defines the position of the event shape.

* The [trigger](/api/js/ejdiagram#members:nodes-subprocess-events-trigger "trigger") property defines the type of the event trigger.

* You can also use define ports and labels to sub-process events by using event's [ports](/api/js/ejdiagram#members:nodes-subprocess-events-ports "ports") and [labels](/api/js/ejdiagram#members:nodes-subprocess-events-labels "labels") properties.

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
		//Creates transaction subprocess
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

![Transaction Subprocess shape](Shapes_images/Shapes_img118.png)

#### Processes 

[processes](/api/js/ejdiagram#members:nodes-subprocess-processes "processes") is a array collection that defines the children values for BPMN subprocess.

{% highlight javascript %}
<div id="diagram"></div>
<script type="text/javascript">
var nodes = [{
        name: "group", offsetX: 500, offsetY: 300, width: 300, height: 200,
        type: "bpmn", shape: ej.datavisualization.Diagram.BPMNShapes.Group,
        children: [{
            name: "node", marginLeft: 15, marginTop: 15, width: 250, height: 150,
            type: "bpmn", shape: ej.datavisualization.Diagram.BPMNShapes.Activity, activity: ej.datavisualization.Diagram.BPMNActivity.SubProcess,
            subProcess: {
                collapsed: false,
                Processes: [{
                    name: "subnode01", marginLeft: 20, marginTop: 50, width: 30, height: 30,
                    type: "bpmn", shape: ej.datavisualization.Diagram.BPMNShapes.Event
                },
                    {
                        name: "subnode02", marginLeft: 90, marginTop: 25, width: 100, height: 80,
                        type: "bpmn", shape: ej.datavisualization.Diagram.BPMNShapes.Activity, activity: ej.datavisualization.Diagram.BPMNActivity.Task, task: { type: "user" }, annotation: { text: "Review Customer Rating", length: 125, angle: 24, width: 100, height: 30 }
                    }]
            }
        }]
    }];
var connectors = [{
        name: "connector1", sourceNode: "subnode01", targetNode: "subnode02"
    }];

$("#diagram").ejDiagram({
        connectors: connectors,
        nodes: nodes});
</script>
{% endhighlight %}

![BPMN Processes diagram](Shapes_images/Shapes_img151.png)

#### Loop

Loop is a task that is internally being looped. The [loop](/api/js/ejdiagram#members:nodes-tasks-loop "loop") property of task allows you to define the type of loop. The default value for `loop` is "none". 
You can define the [loop](/api/js/ejdiagram#members:nodes-subprocess-loop "loop") property in subprocess BPMN shape as shown in the below code.

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

![BPMN Loop diagram](Shapes_images/Shapes_img43.png)

The following table contains various types of BPMN loops.

| Loops | Task | SubProcess |
|---|---|---|
| Standard | ![Standard task shape](Shapes_images/Shapes_img44.png) | ![Standard SubProcess shape](Shapes_images/Shapes_img45.png) |
| SequenceMultiInstance | ![SequenceMultiInstance task shape](Shapes_images/Shapes_img46.png) | ![SequenceMultiInstance SubProcess shape](Shapes_images/Shapes_img47.png) |
| ParallelMultiInstance | ![ParallelMultiInstance Task shape](Shapes_images/Shapes_img48.png) | ![ParallelMultiInstance SubProcess shape](Shapes_images/Shapes_img49.png) |

#### Compensation

Compensation is triggered when operation is partially failed and you can enable it with the [compensation](/api/js/ejdiagram#members:nodes-tasks-compensation "compensation") property of task and [compensation](/api/js/ejdiagram#members:nodes-subprocess-compensation "compensation") property of subprocess.

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

![Compensation diagram](Shapes_images/Shapes_img50.png)

#### Call

A call activity is a global sub-process that is reused at various points of the business flow and you can set it with the [call](/api/js/ejdiagram#members:nodes-tasks-call "call") property of task.

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

![Call shape](Shapes_images/Shapes_img51.png)

#### Ad-Hoc

An ad hoc subprocess is a group of tasks that are executed in any order or skipped in order to fulfill the end condition and you can set it with the [adhoc](/api/js/ejdiagram#members:nodes-subprocess-adhoc "adhoc") property of subprocess. 

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

![Boundary shape](Shapes_images/Shapes_img52.png)

#### Boundary

Boundary represents the type of task that is being processed. The [boundary](/api/js/ejdiagram#members:nodes-subprocess-boundary "boundary") property of sub process allows you to define the type of boundary. By default, it is set as "default".

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
| Call | ![Boundary call shape](Shapes_images/Shapes_img53.png) |
| Event | ![Boundary event shape](Shapes_images/Shapes_img54.png) |
| Default | ![Boundary default shape](Shapes_images/Shapes_img55.png) |

### Data

A data object represents information flowing through the process, such as data placed into the process, data resulting from the process, data that needs to be collected, or data that must be stored. To define a [data](/api/js/ejdiagram#members:nodes-data "data") object, set the [shape](/api/js/ejdiagram#members:nodes-shape "shape")  as "dataobject" and [type](/api/js/ejdiagram#members:nodes-data-type "type") property defines whether data is an input or a output. You can create multiple instances of data object with the [collection](/api/js/ejdiagram#members:nodes-data-collection "collection") property of data.

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
			type: ej.datavisualization.Diagram.BPMNDataObjects.Input,
			collection: true
		}
	}]
});

{% endhighlight %}

![Data shape](Shapes_images/Shapes_img56.png)

The following table contains various representation of BPMN Data Object.

| Boundary | Image |
|---|---|
| Collection Data Object | ![Boundary data object shape](Shapes_images/Shapes_img119.png) |
| Data Input | ![Boundary data input shape](Shapes_images/Shapes_img120.png) |
| Data Ouptput | ![Boundary data output shape](Shapes_images/Shapes_img121.png) |

### Datasource

DataSource is used to store or access data associated with a business process. To create a data source, set the [shape](/api/js/ejdiagram#members:nodes-shape "shape") as "datasource". The following code example illustrate how to create data source.

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

![Datasource shape](Shapes_images/Shapes_img57.png)

### Artifact

Artifact is used to show additional information about a Process in order to make it easier to understand. There are 2 types of artifacts in BPMN.

* Text Annotation
* Group

#### Text Annotation

* A BPMN object can be associated with a text annotation which does not affect the flow but gives details about objects within a flow. The [annotation](/api/js/ejdiagram#members:nodes-annotation "annotation") property of the node is used to connect an annotation element to the BPNN node.

* The annotation [angle](/api/js/ejdiagram#members:nodes-annotation-angle "angle") property is used to set the angle between the BPMN shape and the annotation.

* The annotation [direction](/api/js/ejdiagram#members:nodes-annotation-direction "direction") property is used to set direction of the text annotation.

* To set the size for text annotation, use [width](/api/js/ejdiagram#members:nodes-annotation-width "width") and [height](/api/js/ejdiagram#members:nodes-annotation-height "height") properties.

* The annotation [length](/api/js/ejdiagram#members:nodes-annotation-length "length") property is used to set the distance between the BPMN shape and the annotation.

* The annotation [text](/api/js/ejdiagram#members:nodes-annotation-text "text") property defines the additional information about the flow object in a BPMN Process.

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

![Text Annotation shape](Shapes_images/Shapes_img122.png)

#### Group

A group is used to frame a part of the diagram, shows that elements included in it are logically belong together and don't have any other semantics other than organizing elements. To create a Group, the [shape](/api/js/ejdiagram#members:nodes-shape "shape") property of node should be set as "group". The following code example illustrates how to create a BPMN Group.

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

![Group shpae](Shapes_images/Shapes_img123.png)

#### BPMN Flows

BPMN Flows are lines that connects BPMN flow objects.

### Association

BPMN Association flow is used to link flow objects with its corresponding text or artifact. An association is represented as a dotted graphical line with opened arrow. The type of association are as follows.

* Directional
* BiDirectional
* Default

The [association](/api/js/ejdiagram#members:connectors-shape-flow-association "association") property allows you to define the type of association.The following code example illustrates how to create an association.

{% highlight javascript %}

 $("#diagram").ejDiagram({
	width: "100%",
	height: "100%",
	pageSettings: {
		scrollLimit: "diagram"
	},
    connectors: [{
        name: "connect1", 
        sourcePoint:{
               x:100,
               y:200
             }, 
         targetPoint: 
            {
               x:300
               ,y:200
             }, 
          segments: [{ 
                type: "straight" 
              }], 
           shape: {
                  type: "bpmn",
				  //Sets the type of the flow as association
                  flow: "association",
				  //Sets the type of association
                  association: "bidirectional"
              }
	}]
});	

{% endhighlight %}

![Association shape](Shapes_images/Shapes_img134.png)

The following table demonstrates the visual representation of assosiation flows.

| Association | Image |
|---|---|
| Default | ![Association Default shape](Shapes_images/Shapes_img133.png) |
| Directional | ![Association Directional shape](Shapes_images/Shapes_img134.png) |
| BiDirectional | ![Association BiDirectional shape](Shapes_images/Shapes_img132.png) |

N> The default value for the property `association` is "default".

### Sequence

A Sequence flow shows the order in which the activities are performed in a BPMN Process and is represented with a solid graphical line.The type of sequence are as follows.

* Normal
* Conditional
* Default

The [sequence](/api/js/ejdiagram#members:connectors-shape-sequence "sequence") property allows you to define the type of sequence.The following code example illustrates how to create a sequence flow.

{% highlight javascript %}

 $("#diagram").ejDiagram({
	width: "100%",
	height: "100%",
	pageSettings: {
		scrollLimit: "diagram"
	},
    connectors: [{
        name: "connect1", 
        sourcePoint:{
               x:100,
               y:200
             }, 
         targetPoint: 
            {
               x:300
               ,y:200
             }, 
          segments: [{ 
                type: "straight" 
              }], 
           shape: {
                  type: "bpmn",
                  flow: "sequence",
				  //Sets the type of sequence flow
                  sequence: "conditional"
              }
	}]
});	

{% endhighlight %}

![Sequence shape](Shapes_images/Shapes_img135.png)

The following table contains various representation of sequence flows.

| Sequence | Image |
|---|---|
| Default | ![Default Sequence shape](Shapes_images/Shapes_img136.png) |
| Conditional | ![Conditional Sequence shape](Shapes_images/Shapes_img135.png) |
| Normal | ![Normal Sequence shape](Shapes_images/Shapes_img137.png) |

N> The default value for the property `sequence` is "normal".

### Message

A Message flow shows the flow of messages between two Participents.A message flow is represented by dashed line.The type of message are as follows.

* InitiatingMessage
* NonInitiatingMessage
* Default

The [message](/api/js/ejdiagram#members:connectors-shape-message "message") property allows you to define the type of message.The following code example illustrates how to define a message flow.

{% highlight javascript %}

 $("#diagram").ejDiagram({
	width: "100%",
	height: "100%",
	pageSettings: {
		scrollLimit: "diagram"
	},
    connectors: [{
        name: "connect1", 
        sourcePoint:{
               x:100,
               y:200
             }, 
         targetPoint: 
            {
               x:300
               ,y:200
             }, 
          segments: [{ 
                type: "straight" 
              }], 
           shape: {
                  type: "bpmn",
                  flow: "message",
				  //Sets the type of message flow
                  message: "initiatingmessage"
              }
	}]
});	

{% endhighlight %}

![Message shape](Shapes_images/Shapes_img138.png)

The following table contains various representation of message flows.

| Message | Image |
|---|---|
| Default | ![Default Message shape](Shapes_images/Shapes_img139.png) |
| InitiatingMessage | ![InitiatingMessage Message shape](Shapes_images/Shapes_img138.png) |
| NonInitiatingMessage | ![NonInitiatingMessage Message shape](Shapes_images/Shapes_img140.png) |

N> The default value for the property `message` is "default".