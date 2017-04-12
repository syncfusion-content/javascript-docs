---
layout: post
title: Drag and drop list elements
description: Drag and drop list elements
platform: js
control: Draggable, Droppable
documentation: ug
keywords: Draggable,Drop,draganddrop
---

# Drag and Drop List elements:

You can drag an element from list view and drop this into another element. The below code illustrates how to drag element from list view 

{% highlight html %}

	    <div class="contents"><h4>Drag  elements</h4>
    	     <div id="defaultlistbox">
                  <ul id="draggable">
	                  <li data-ej-text="Hot Singles" class="drag"></li>
                      <li data-ej-text="Rising Artists" class="drag"></li>
                      <li data-ej-text="Live Music" class="drag"></li>
                      <li data-ej-text="Best of 2013 So Far" class="drag"></li>
	                  <li data-ej-text="Songs" class="drag"></li>
                </ul>
             </div>
          </div>
	<div class="contents" style="margin-left:200px"><h4>Drop elements</h4>
		<div id="listitem"></div>
	 </div>
    
    
{% endhighlight %}

{% highlight css %}

	 <style>
	      #listitem
        	{   
            width: 150px;
            height: 200px;
            border:1px solid #c8c8c8;
           }
	     .contents {
             display: inline-block;
             padding:5px;
             position:absolute;
            }
	</style>
{% endhighlight %}

{% highlight javascript %}
	
     $(function () {
          $("#defaultlistbox").ejListView();
	      $(".drag").ejDraggable({helper: function (event) {
                    return $(event.element); // Object of the Draggable element.	
                }
            });
			
	      $("#listitem").ejDroppable({
              drop: function (event, ui) {
                event.dropTarget.append(event.dragElement);
                event.dropTarget.ejListView();
                $("#listitem").find("li").attr("style","position:relative;left:0px;top:0px;list-style-type:none");
                $("#listitem").find("li").removeClass("e-state-active").addClass("e-state-default");
                }
            });
        });

{% endhighlight %}

Before Drag:

![](dragList_images/listdrag.png)

After Drag:

![](dragList_images/Afterdrag.png)