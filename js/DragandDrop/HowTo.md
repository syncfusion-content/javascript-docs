---
layout: post
title: How To- Draggable and Droppable widget for Syncfusion Essential JS
description: How To section in Drag and Drop by adding references.
platform: js
control: Draggable,Droppable
documentation: ug
keywords: Draggable,Drop,draganddrop
api: /api/js/ejdraggable

---

# How To


## Move Between Lists

You can drag an element from list view and drop this into another element. The below code illustrates how to drag element from list view 

{% highlight html %}

	   <div class="content-container-fluid listview-sample">
        <div class="row">
            <div class="cols-sample-area">
                <div class="frame" style="height: 300px;">
                    <div class="contents">
                        <h4>Drag elements</h4>
                        <div id="defaultListBox">
                            <ul id="draggable">
                                <li data-ej-text="Hot Singles" class="drag"></li>
                                <li data-ej-text="Rising Artists" class="drag"></li>
                                <li data-ej-text="Live Music" class="drag"></li>
                                <li data-ej-text="Best of 2013 So Far" class="drag"></li>
                                <li data-ej-text="Songs" class="drag"></li>
                            </ul>
                        </div>
                    </div>
                    <div class="contents" style="margin-left:200px">
                        <h4>Drop elements</h4>
                        <div id="listItem"></div>
                    </div>

                </div>
            </div>
        </div>
    </div>
    
    
{% endhighlight %}

{% highlight css %}

	 <style>
	  #listItem {
            width: 150px;
            height: 205px;
            border: 1px solid #c8c8c8;
            
           }
        
      .contents {
            display: inline-block;
            padding: 5px;
            position: absolute;
          }
     .clone
		{
         padding: 5px 5px 5px 0.857em;
         list-style: none;
		 opacity: 1; 
		}
	</style>
{% endhighlight %}

{% highlight javascript %}
	
       $(function () {
            var cloneElement;
            $("#defaultListBox").ejListView();
            $(".drag").ejDraggable({
                helper: function (event) {
                    proxy = $(event.element).closest('.e-lv.e-js').data('ejListView');
                    cloneElement = $(event.element);
                    cloneElement.addClass("clone");
                    return _clonedElement.appendTo($("body"));

                },

            });

            $("#listItem").ejDroppable({
                drop: function (event, ui) {
                    if (event.target.id == "listItem") {
                        event.dropTarget.append(event.dragElement);
                        event.dropTarget.ejListView();
                    }
                    else
                        ui.draggable[0].remove();
                    $("#listItem").find("li").attr("style", "position:relative;left:0px;top:0px;list-style-type:none");
                    $("#listItem").find("li").removeClass("e-state-active").addClass("e-state-default");
                    if ($('.e-list-container').find('ul li').length == 0) $('.e-list-container').css('border-top', '0px')
                }
            });


        });


        });

{% endhighlight %}

Before Drag:

![](HowTo_images/listdrag.png)

After Drag:

![](HowTo_images/Afterdrag.png)

## Get Drag Element

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

## Order of Events 

The events will be triggered in the following order during Drag and Drop

* [DragStart](https://help.syncfusion.com/api/js/ejdraggable#events:dragstart) -Fires when Draggable action starts.

* **Drag** - Fires when the element is being dragged.

* [DragStop](https://help.syncfusion.com/api/js/ejdraggable#events:dragstop) -Fires when the Draggable action stops.

* **Over** -Fires when the element is Dragged over the Droppable element

* **Drop** -Fires when the element is dropped.

* **Out**- Fires when Drag element is moved out of Droppable target

{% highlight html %}

    <div id="leftContainer">
        <!-- draggable element-->
        <div id="dragElement" class="drag">
            <span class="dragText">Drag</span>
        </div>
		
    </div>

    <div id="rightContainer">
        <!-- droppable target element-->
        <div id="dropContainer" class="drop">
            <span class="dropText">Drop Here</span>
        </div>
    </div>

{% endhighlight %}

{% highlight css %}   

    <style>
        #leftContainer {
            width: 150px;
            height: 150px;
            padding: 30px;
            float: left;
        }

        #rightContainer {
            width: 150px;
            height: 150px;
            padding: 30px;
            float: left;
        }

         .drag 
         {
            width: 70px;
            height: 70px;
            float: left;
            font-size: 17px;
            padding: 8px;
            z-index: 100002;
            background-color: darkgrey;
         }
        .drop
        {
            width: 150px;
            height: 150px;
            float: left;
            position: relative;
            padding: 8px;
            background-color: lightgrey;
        }

		
	   .dragText,.dropText
		 {
		  font-size:17px;
		  margin:20px;
		  display:inline-block;
		 }
		 body { font-family: -webkit-pictograph;}
    </style>

{% endhighlight %}

{% highlight javascript %}

     jQuery(function ($) {
            $("#dragElement").ejDraggable({
                helper: function (event) {
                    return $(event.element); // Object of the Draggable element.
                },
                dragStart: function (event) {
                    console.log("DragStart event is fired");
                },
                drag: function (event) {
                    console.log("Drag event is fired");
                },
                dragStop: function (event) {
                    console.log("DragStop event is fired");
                }
            });


            $("#dropContainer").ejDroppable({
                drop: function (event, ui) {
                    event.dropTarget.text("");
                    event.dragElement.text("Dropped..!");
                    console.log("Drop event is fired");

                },
                out: function (event) {
                    console.log("Out event is fired");
                },
                over: function (event) {
                    console.log("Over event is fired");
                }

            });
        });

{% endhighlight %}

The output of above code will be as shown below:

![](HowTo_images/events.png)