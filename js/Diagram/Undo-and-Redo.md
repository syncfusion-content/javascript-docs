---
layout: post
title: Undo-and-Redo
description: undo and redo
platform: js
control: Diagram
documentation: ug
---

# Undo and Redo

The **Undo command** reverses the last editing action performed on Diagram. For example, some of the basic operations performed on Diagram objects such as translation, rotation, resizing, grouping, ungrouping, changing z-order, addition, deletion and so on, can be reversed. The Redo command restores the last editing action if no other actions have occurred since the last undo.

Diagram provides public API undo()/redo() to execute the undo/redo commands and the following code illustrate this.

{% highlight js %}

//undo
var diagram = $("#Diagram").ejDiagram("instance");
diagram.undo();

//redo
diagram.redo();

{% endhighlight %}

## History Manager

Diagram provides inbuilt support to revert and restore the actions performed through interactions. If any other custom actions (changes through APIs) have to be tracked, it can be achieved using HistoryManager. History manager allows to push custom history entries and to handle them when undo/redo is executed.

Following example illustrates how to revert the font color change of a text node.

1\. Before changing the font color, push the current state to history manager.

{% highlight js %}

//Saving the current state
var entry = { object: node.name, previousState: { fontColor: node.textBlock.fontColor } };

//Add the state to history manager
diagram.model.historyManager.push(entry);

//Font color change
diagram.updateLabel(node.name, node.textBlock, { fontColor: "red" });

{% endhighlight %}

2\. Define the methods to handle the custom changes

{% highlight js %}

$("#diagram").ejDiagram({
    historyManager: {
        //will be called to revert a custom action
        undo: customUndoRedo,
        
        //will be called to restore a reverted custom action
        redo: customUndoRedo
    }
});

{% endhighlight %}