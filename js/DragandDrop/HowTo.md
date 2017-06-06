--
layout: post
title: Getting started with Draggable and Droppable widget for Syncfusion Essential JS
description: To get start with Drag and Drop by adding references.
platform: js
control: Draggable,Droppable
documentation: ug
keywords: Draggable,Drop,draganddrop
---


# How To

## Set cusrsor at (0,0)

You can set the offset as (0, 0) for dragging helper with respect to the mouse cursor using [cursorAt](https://help.syncfusion.com/api/js/ejdraggable#members:cursorat) property.

{% highlight html %}

   <div id="leftContainer">
        <!-- draggable element-->
        <div id="dragElement" class="drag">
            <span>Drag Me</span>
        </div>
    </div>

    <div id="rightContainer">
        <!-- droppable target element-->
        <div id="dropContainer" class="drop">
            <span>Drop Here</span>
        </div>
    </div>

     
{% endhighlight %}

{% highlight javascript %}

         jQuery(function ($){
            $("#dragElement").ejDraggable({
                helper: function (event) {
                    return $(event.element); // Object of the Draggable element.
                },
	            cursorAt:{ top: 0, left: 0 },
			
            });

            $("#dropContainer").ejDroppable({
                // Drop event for change the container text while dropping element.
                drop: function (event, ui) {
                    event.dropTarget.text("Element Dropped..!");
                }
				
            });
        });

 
{% endhighlight %}

## Make an element draggable on tapHold in mobile devices

Inorder to drag an element during tapHold in mobile devices set the dragOnTaphold to true 

{% highlight javascript %}

         jQuery(function ($){
            $("#dragElement").ejDraggable({
                helper: function (event) {
                    return $(event.element); // Object of the Draggable element.
                },
	            dragOnTaphold:true
			
            });

        });
