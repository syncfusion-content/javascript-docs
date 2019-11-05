---
layout: post
title: Undo-Redo | Diagram | Javascript | Syncfusion
description: This section explains how to revert/restore the changes using Undo and Redo commands in the ejDiagram control.
platform: js
control: Diagram
documentation: ug
api: /api/js/ejdiagram
---

# History Manager

Diagram tracks the history of actions that are performed after loading the time and provides support to reverse and restore those changes.

## Undo and Redo

Diagram provides built-in support to track the changes that are made through interaction and through public APIs. The changes can be reverted or restored either through short cut keys or through commands.

### Undo redo through short cut keys

Undo redo commands can be executed through short cut keys. Short cut key for undo is ctrl+z and short cut key for redo is ctrl+y.

For more information, refer to [Keyboard Interactions](/js/Diagram/Interaction#keyboard "Keyboard Interactions").

### Undo redo through public APIs

The client side methods [undo](/api/js/ejdiagram#methods:undo "undo") and [redo](/api/js/ejdiagram#methods:redo "redo") help you to revert/restore the changes. The following code example illustrates how to undo/redo the changes through script.

{% highlight javascript %}

var diagram = $("#Diagram").ejDiagram("instance");

// Reverts the last action performed
diagram.undo();

// Restores the last undone action
diagram.redo();

{% endhighlight %}

When a change in diagram is reverted or restored(undo/redo), the [historyChange](/api/js/ejdiagram#events:historychange "historyChange") event gets triggered.

## Track custom changes

Diagram provides options to track the changes that are made to custom properties. For example, in case of an employee relationship Diagram, you may need to track the changes in the employee information. The [historyManager](/api/js/ejdiagram#members:historymanager "historyManager") of the Diagram model enables you to track such changes.
The following example illustrates how to track such custom property changes.

* Before changing the employee information, save the existing information to history manager by using the client side method [push](/api/js/ejdiagram#members:historymanager-push "push") of `historyManager`.
* You can use historyManager [canPop](/api/js/ejdiagram#members:historymanager-canpop "canPop") method which takes a history entry as argument and returns whether the specific entry can be popped or not.
* The [pop](/api/js/ejdiagram#members:historymanager-pop "pop") method is used to remove the history of a recent change made in diagram.

The following code example illustrates how to save the existing property values and pop it. 

{% highlight javascript %}

var diagram = $("#diagram").ejDiagram("instance");

//Creates a custom entry and adds that to history manager
var entry = { object: node, prevState: node.empInfo };
diagram.model.historyManager.push(entry);

//Updates the new information
var newValue = { role: "New role" };
node.empInfo = newValue;

//Pop if the change doesn't need to be tracked
if(diagram.model.historyManager.canPop(entry))
	diagram.model.historyManager.pop();

{% endhighlight %}

* Change the employee information

{% highlight javascript %}

//Updates the new information
var newValue = { role: "New role" };
node.empInfo = newValue;

{% endhighlight %}

* Define the methods to handle the custom changes. These methods are called when you try to revert/restore the custom changes.

You need to define the methods to handle the custom changes and you need to assign that to [undo](/api/js/ejdiagram#members:historymanager-undo "undo") and [redo](/api/js/ejdiagram#members:historymanager-redo "redo") properties of `historyManager`.
The following code example illustrates how to define methods to handle the custom changes.

{% highlight javascript %}

$("#diagram").ejDiagram({
	historyManager: {
		//Called to revert a custom action
		undo: customUndoRedo,
		//Called to restore the reverted custom action
		redo: customUndoRedo
	}
});

//Method to handle the custom action
function customUndoRedo(args) {
	var diagram = $("#diagram").ejDiagram("instance");
	var node = args.object;
	var currentState = node.empInfo;

	//Resets the state
	node.empInfo = args.prevState;

	//Saves the previous state
	args.prevState = currentState;
}

{% endhighlight %}

## Group multiple changes 

History manager allows to revert or restore multiple changes through a single undo/redo command. For example, you may need to revert/restore the fill color change of multiple elements at a time.

The client side method [startGroupAction](/api/js/ejdiagram#members:historymanager-startgroupaction "startGroupAction") is used to notify the Diagram to start grouping the changes. The client side method [closeGroupAction](/api/js/ejdiagram#members:historymanager-closegroupaction "closeGroupAction") is used to notify to stop grouping the changes. The following code illustrates how to undo/redo fillColor change of multiple elements at a time.

{% highlight javascript %}

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

{% endhighlight %}

## Track Undo/Redo actions

The historyManager [undoStack](/api/js/ejdiagram#members:historymanager-undostack "undoStack") property is used to get the collection of undo actions which needs to be performed in the diagram.
The historyManager [redoStack](/api/js/ejdiagram#members:historymanager-redostack "redoStack") property is used to get the collection of redo actions which needs to be performed in the diagram.
The historyManager [stackLimit](/api/js/ejdiagram#members:historymanager-stacklimit "stackLimit") property limits the number of actions to be stored on the historyManager.
The undoStack/redoStack is an read only property.

{% highlight javascript %}
 
$("#diagram").ejDiagram({
    //define historyChange event
	historyChange: function (args) {
		//get the collection of undoStack objects
		var undoStack = args.model.historyManager.undoStack;
		//get the collection of redoStack objects
		var redoStack = args.model.historyManager.redoStack;
	},
	//define historyManager stack limit property which limits the number of actions to be stored on the historyManager.
	historyManager: { stackLimit: 5 }
});
//We can get the undoStack/redoStack objects by taking instance of diagram. 
var diagram = $("#diagram").ejDiagram("instance");
var undoStack = diagram.model.historyManager.undoStack;
var redoStack = diagram.model.historyManager.redoStack;
		
{% endhighlight %}

## clear History

The clearHistory method used to Clears the actions which is recorded to perform undo/redo operation in the diagram. Please refer to the below link which shows how to use clearHistory method in diagram.

[clearHistory](/api/js/ejdiagram#methods:clearhistory "clearHistory")

