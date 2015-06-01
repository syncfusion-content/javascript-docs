---
layout: post
title: Model
description: model
platform: js
control: Diagram
documentation: ug
---

# Model

The **Diagram** model represents data for rendering the Diagram and manipulating the Diagram elements.

The following code illustrates how to create a **Diagram** with some model properties.

{% highlight js %}

**[JS]** 

//create diagram
$("#Diagram").ejDiagram({
  //set diagram model properties
  width: "100%",
  height: "100%",
  pageSettings: { pageWidth: 2000, pageHeight: 2000 }
});


{% endhighlight %}



{% include image.html url="/js/Diagram/Concepts-and-Features/Model_images/Model_img1.png" Caption="Model"%}

## Events

_Events_

<table>
<tr>
<td>
<b>Events</b></td><td>
<b>Argument</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
nodeCollectionChange</td><td>
{cancel, changeType, element, model, type}cancel: booleanchangeType-string(“insert”/”remove”) element- object(Node to be added or removed) model- object(diagram’s model)type-string(event name: “nodeCollectionChange”) </td><td>
This event is raised when you add/delete node during runtime.</td></tr>
<tr>
<td>
connectorCollectionChange</td><td>
{cancel, changeType, element, model, type }cancel: booleanchangeType- string(“insert”/”remove”) element- object(Connector to be added or removed)model- object(diagram’s model)type- string(event name: “connectorCollectionChange”)</td><td>
This event is raised when you add/delete connector during run time.</td></tr>
</table>


