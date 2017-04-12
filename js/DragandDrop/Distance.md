---
layout: post
title: Setting distance for mouse move 
description: Setting distance for mouse moveS
platform: js
control: Draggable,Droppable
documentation: ug
keywords: Draggable,Drop,draganddrop
---

# Set distance for mouse move

You can set the required distance the mouse should travel in order to initiate a drag using [distance](https://help.syncfusion.com/api/js/ejdraggable#members:distance) property.

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
	       distance:5,
	        helper: function (event) {
	           return $(event.element);
               }
			});
         }); 

{% endhighlight %}