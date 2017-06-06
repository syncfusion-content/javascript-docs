---
layout: post
title: Getting Draggable element
description: Getting Draggable element
platform: js
control: Draggable,Droppable
documentation: ug
keywords: Draggable,Drop,draganddrop
---

# Get corresponding dragged element

You can get the dragged element from the args of [drag](https://help.syncfusion.com/api/js/ejdraggable#events:drag) event. The below code explains how to get the draggable element using drag event.

{% highlight html %}

    <div id="draggable-container">
      <div id="draggable-item">Drag</div>
    </div>
    <style>
      #draggable-container {
        margin: 10px auto;
        width: 200px;
        height: 200px;
        background: #eee;
        padding: 10px;
        border: 1px solid black;
        }

     #draggable-item {
        width: 30px;
        height: 20px;
        padding: 10px;
        border: 1px solid black;
        margin: 5px;
        background: #666;
        color: white;
        }
    </style>
     
{% endhighlight %}

{% highlight javascript %}
	$(function () {
	   $("#draggable-item").ejDraggable({
	      dragArea:"#draggable-container",
	      helper:function (event) {
	         return $(event.element);
            },
	     drag:function(args)
	      {
	       console.log(args.element);
	      }
	   });
    }); 


{% endhighlight %}

The output of above code will be as shown below:

![](draggableelement_images/dragelement.png)