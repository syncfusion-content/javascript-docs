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
         <div class="orange"></div>
         <div class="purple"></div>
         <div class="orange"></div>
         <div class="purple"></div>
      </div>
     <div id="container" style="background-color:antiquewhite; height:100px;width:375px;">
     <div id="draggable"><span>Drag Me..</span></div>
    <style>
      #draggable {
         width: 50px;
         height: 50px;
         border: 2px solid green;
         margin: 5px;
         display: inline-block;
         background-color: orange;
        }
    .orange, .purple {
       width: 70px;
       height: 80px;
       margin: 10px;
     }
    .orange { background-color: orange; }
    .purple { background-color: purple; }
    #area {
      width: 375px;
      height: 340px;
      background-color: antiquewhite;
    }
   #droptarget {
      width: 100px;
      height: 100px;
      border: 2px solid green;
      margin: 0 96px;
      display: inline-block;
      vertical-align: middle;
     }

{% endhighlight %}

{% highlight javascript %}

    $("#draggable").ejDraggable({
            helper: function(event) {
	        return $(event.element);
	         // Object of the Draggable element.
           },
	     scope: "orange"
        });
    $(".orange").ejDroppable({
        scope: "orange",
         drop: function (event, ui) {
            event.dropTarget.text("Dropped..!");
         }
     });
    $(".purple").ejDroppable();  
{% endhighlight %}

Before Drag:

![](Grouping_images/scope.png)

After Drag:

![](Grouping_images/scope1.png)