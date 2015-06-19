---
layout: post
title: Undo-and-Redo
description: undo and redo
platform: js
control: Diagram
documentation: ug
---

# Undo and Redo

The **Undo command** reverses the last editing action performed on Diagram. For example, some of the basic operations performed on Diagram objects such as translation, rotation, resizing, grouping, ungrouping, changing z-order, addition, deletion and so on, can be reversed. The **Redo command** restores the last editing action if no other actions have occurred since the last undo. Diagram provides public API **undo()/redo()** to execute the undo/redo commands and the following code illustrate this.

{% highlight js %}

//undo
var diagram = $("#Diagram").ejDiagram("instance");
diagram.undo();

//redo
diagram.redo();

{% endhighlight %}
