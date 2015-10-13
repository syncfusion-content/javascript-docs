---
layout: post
title: Undo-and-Redo
description: undo and redo
platform: js
control: Diagram
documentation: ug
---

# History Manager

Diagram tracks the history of actions that are performed after loading time and provides support to reverse and restore those changes. 

## Undo and Redo

Diagram provides inbuilt support to track the changes that are made through interaction and through public APIs. The changes can be reverted or restored either through short cut keys or through commands.

### Undo redo through short cut keys

Undo redo commands can be executed through short cut keys. Short cut key for undo is ctrl+z and short cut key for redo is ctrl+y.

For more information, refer [Keyboard Interactions](/js/Diagram/Interaction "Keyboard").

### Undo redo through public APIs

The client side methods `undo` and `redo` helps you to revert/restore the changes. The following snippet illustrates how to undo/redo the changes through script.

{% highlight js %}

    var diagram = $("#Diagram").ejDiagram("instance");
    
    // Revert the last action performed    
    diagram.undo();
    
    // Restore the last undone action     
    diagram.redo();  

{% endhighlight %} 


## Track custom changes

Diagram provides options to track the changes that are made to custom properties. For example, in case of an employee relationship diagram, you may need to track the changes in the employee information. The `historyManager` of diagram model enables you to track such changes.      
Following example illustrates how to track such custom property changes.

* Before changing the employee information, save the existing information to history manager using the client side method `push` of `historyManager`.

 Following code snippet illustrates how to save the existing property values. 

{% highlight js %}

    var diagram = $("#diagram").ejDiagram("instance");
    
    //create a custom entry and add that to history manager 
    var entry = { object: node, prevState: node.empInfo };    
    diagram.model.historyManager.push(entry);

    //update the new information    
    var newValue = { role: "New role" };
    node.empInfo = newValue;

{% endhighlight %} 

* Change the employee information

{% highlight js %}

    //update the new information    
    var newValue = { role: "New role" };
    node.empInfo = newValue;

{% endhighlight %} 

* Define the methods to handle the custom changes. These methods will be called when you try to revert/restore the custom changes.

You need to define the methods to handle the custom changes and you need to assign that to `undo` and `redo` properties of `historyManager`.
Following code snippet illustrates how to define methods to handle the custom changes.

{% highlight js %}

    $("#diagram").ejDiagram({
        historyManager: {
            //will be called to revert a custom action
            undo: customUndoRedo,
            //will be called to restore the reverted custom action
            redo: customUndoRedo
        }
    });

    //Method to handle the custom action 
    function customUndoRedo(args) {
        var diagram = $("#diagram").ejDiagram("instance");
        var node = args.object;
        var currentState = node.empInfo;

        //Reset the state
        node.empInfo = args.prevState;

        //save previous state
        args.prevState = currentState;
    }
    
{% endhighlight %} 

## Group multiple changes 

History manager allows to revert or restore multiple changes through a single undo/redo command. For example, you may need to revert/restore the fill color change of multiple elements at a time.

The client side method `startGroupAction` is used to notify the diagram to start grouping the changes. The client side method `closeGroupAction` is used to notify to stop grouping the changes. Following code illustrates how to undo/redo fillColor change of multiple elements at a time.

{% highlight js %}

    var group = diagram.model.selectedItems

    // Start to group the changes
    diagram.model.historyManager.startGroupAction();

    //Make the changes
    for (var i = 0; i < group.children.length; i++) {
        var option = {};
        var item = group.children[i];
        // update the fillColor for all the child elements.
        option.fillColor = args.style.backgroundColor;
        diagram.updateNode(item.name, option);
    }

    //End grouping the changes
    diagram.model.historyManager.closeGroupAction();

{% endhighlight %} 