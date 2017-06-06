---
layout: post
title: Grouping Drag and Drop elements
description: Grouping Drag and Drop elements
platform: js
control: Draggable, Droppable
documentation: ug
keywords: Draggable, Draggable, draganddrop
---
# Grouping Drag and Drop Elements

You can group draggable and droppable elements using [scope](https://help.syncfusion.com/api/js/ejdraggable#members:scope) property. You can define a scope value for both drag and drop elements and the elements will be dragged and dropped based on that.The draggable element with a different scope value will not be accepted by the droppable element

The below code illustrates how to use scope for grouping elements

{% highlight html %}

    <div id="area">
        <div class="scope1"><span class="text1">Same scope</span></div>
        <div class="scope2"><span class="text2">Different scope</span></div>
        <div id="draggable"><span>Drag Me..</span></div>
    </div>
    <style>
        #draggable
	   {
         width: 60px;
         height: 50px;
         border: 1px solid black;
         margin: 5px;
         display: inline-block;
         background-color: #179bd7;
        }
        .scope1, .scope2 
	    {
            width: 90px;
            height: 90px;
            margin: 10px;
   
         }
        .scope1 { background-color: #179bd7; }
        .scope2 { background-color: #74c3e7; }
         #area 
		 {
            width: 300px;
            height: 480px;
            border: grey 1px solid;
	     }
        #droptarget
	    {
          width: 100px;
          height: 100px;
          border: 2px solid;
          margin: 0 96px;
          display: inline-block;
          vertical-align: middle;
        }
       .text1,.text2
	   {
            font-size: 15px;
            margin: 5px;
       }
  
</style>

{% endhighlight %}

{% highlight javascript %}

     $("#draggable").ejDraggable({
           helper: function(event) {
	            return $(event.element);
              },
	         drag:function(event)
	        {
	         event.target.textContent="Dragging";
	         },
	     scope: "scope1"
        });

      $(".scope1").ejDroppable({
              scope: "scope1",
	         over:function(event,ui)
	             {
	                  event.target.textContent="You can Drop here";
	             },
             drop: function (event, ui) {
              event.dropTarget.text("Same scope");
		      event.dragElement.text("Greatjob..");
            }
       });

          $(".scope2").ejDroppable();
		  
{% endhighlight %}

Before Drag:

![](Grouping_images/scope.png)

During Drag:

![](Grouping_images/scope1.png)


When Drag element is over the drop element

![](Grouping_images/scope2.png)

After Drop:

![](Grouping_images/scope3.png)