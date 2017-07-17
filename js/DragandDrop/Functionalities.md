---
layout: post
title: Functionalities of Drag and Drop
description: Functionalities of Drag and Drop
platform: js
control: Draggable, Droppable
documentation: ug
keywords: Draggable, Draggable, draganddrop , functionalities
api: /api/js/ejdraggable
---

# Functionalities


## Delay Drag

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

## Cursor Distance

You can set the offset for dragging helper with respect to the mouse cursor using [cursorAt](https://help.syncfusion.com/api/js/ejdraggable#members:cursorat) property.

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

## Drag On Tap Hold 

In order to drag an element during tapHold in mobile devices set the dragOnTaphold to true 

{% highlight javascript %}

         jQuery(function ($){
            $("#dragElement").ejDraggable({
                helper: function (event) {
                    return $(event.element); // Object of the Draggable element.
                },
	            dragOnTaphold:true
			
            });

        });

{% endhighlight %}

## Restrict Drop

You can group draggable and droppable elements using [scope](https://help.syncfusion.com/api/js/ejdraggable#members:scope) property. You can define a scope value for both drag and drop elements and the elements will be dragged and dropped based on that.The draggable element with a different scope value will not be accepted by the droppable element

The below code illustrates how to use scope for grouping elements

{% highlight html %}

     <div id="area">
        <div class="scope1"><span class="text1">Same scope</span></div>
        <div class="scope2"><span class="text2">Different scope</span></div>
        <div id="draggable"><span class="text3">Drag</span></div>
    </div>
    <style>
        #draggable {
            width: 55px;
            height: 26px;
            float: right;
            line-height: 27px;
            font-size: 11px;
            color: white;
            display: inline-block;
            background-color: #666;
        }

        .scope1, .scope2 {
            font-size: 11px;
            width: 70px;
            height: 80px;
            margin: 10px;
        }

        .scope1 {
            background-color: #eee;
            margin-top: 10px;
        }

        .scope2 {
            background-color: lightgray;
        }

        #area {
            width: 200px;
            height: 240px;
            border: grey 1px solid;
        }

        .text1 {
            margin-top: 22px;
            padding: 6px;
        }

        .text2 {
            margin-left: 2px;
            margin-top: 10px;
            padding: 11px;
        }

        .text1, .text2 {
            font-size: 12px;
            text-align: center;
            display: inline-block;
        }

        .text3 {
            font-size: 11px;
            color: white;
            line-height: 26px;
            margin-left: 16px;
            display: inline-block;
        }

        body {
            font-family: -webkit-pictograph;
        }
    
		  
	</style>
{% endhighlight %}

{% highlight javascript %}

      $("#draggable").ejDraggable({
        helper: function (event) {
            return $(event.element);
        },
        drag: function (event) {
            event.target.textContent = "Dragging";
            $(".text3").css("margin-left", "7px");
            $("#draggable").css("background", "grey");
        },
        scope: "scope1"
    });

    $(".scope1").ejDroppable({
        scope: "scope1",
        over: function (event, ui) {
            $(".text1")[0].innerText = "You can drop here"
        },
        drop: function (event, ui) {
            event.dropTarget.text("");
            $(".text3")[0].innerText = "Dropped!"
            $("#draggable").css("color", "white");
            $("#draggable").css("background", "#666");
        }
    });

    $(".scope2").ejDroppable({
        over: function (event, ui) {
            $(".text2")[0].innerText = "You can't drop here"
        }
    });		  
{% endhighlight %}

Before Drag:

![](Functionalities_images/scope.png)

During Drag:

![](Functionalities_images/scope1.png)

When Drag element is over the non-scope element

![](Functionalities_images/scope2.png)

When Drag element is over the scope element

![](Functionalities_images/scope3.png)

After Drop:

![](Functionalities_images/scope4.png)