---
layout: post
title: Getting started with Javascript Draggable and Droppable | Syncfusion
description: Learn here about getting started with Syncfusion Essential Studio JavaScript Draggable and Droppable control, its elements, and more.
platform: js
control: Draggable,Droppable
documentation: ug
keywords: Draggable,Drop,draganddrop
api: /api/js/ejdraggable

---

# Getting Started with Javascript Draggable and Droppable

The external script dependencies of the Drag and Drop are,

* [jQuery 1.7.1](http://jquery.com/) and later versions.

And the internal script dependencies of the Drag and Drop are:

<table>
	<tr>
		<th>File </th>
		<th>Description / Usage </th>
	</tr>
	<tr>
		<td>ej.core.min.js</td>
		<td>Must be referred always before using all the JS controls.</td>
	</tr>
	<tr>
		<td>ej.draggable.min.js</td>
		<td>Main file for Drag and Drop</td>
	</tr>
</table>

For getting started you can use the ‘ej.web.all.min.js’ file, which encapsulates all the 'ej' controls and frameworks in one single file.<br/> 

For themes, you can use the ‘ej.web.all.min.css’ CDN link from the snippet given. To add the themes in your application, please refer [this link](https://help.syncfusion.com/js/theming-in-essential-javascript-components#adding-specific-theme-to-your-application).


## Configure the sample

Create a new HTML file and add [CDN](https://help.syncfusion.com/js/cdn) links to the [JavaScript](https://help.syncfusion.com/js/dependencies) and [CSS](https://help.syncfusion.com/js/theming-in-essential-javascript-components) dependencies to your project.

{% highlight html %}

    <!DOCTYPE html>

    <html>

    <head>

        <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />

        <!-- style sheet for default theme(flat azure) -->

        <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css"
              rel="stylesheet" />

        <!--scripts-->

        <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.11.3.min.js"></script>

        <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>

    </head>

    <body>

        <!--Place div element to perform Drag and Drop-->

        <script>

            // Place your script code here to initialize DropDownList

        </script>

    </body>

    </html>

{% endhighlight %}

N>  In production, we highly recommend you to use our [custom script generator](https://help.syncfusion.com/js/custom-script-generator#) to create custom script file with required controls and its dependencies only. Also to reduce the file size further please use [GZip compression](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer?hl=en#text-compression-with-gzip) in your server. 

## Initialize Drag And Drop

You can make any Html elements to be draggable or droppable by using ejDraggable and ejDroppable.This section explains how to perform drag using [drag](https://help.syncfusion.com/api/js/ejdraggable#events:drag) event and drop using [drop](https://help.syncfusion.com/api/js/ejdroppable#events:drop) by using html elements

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
    <style>
         #leftContainer {
            width: 100px;
            height: 100px;
            padding: 30px;
            float: left;
        }

        #rightContainer {
            width: 100px;
            height: 100px;
            padding: 30px;
            float: left;
        }

        .drag {
            width: 60px;
            height: 40px;
            float: left;
            font-size: 14px;
            line-height: 37px;
            color: white;
            text-align: center;
            z-index: 100002;
            background-color: #666;
        }

        .drop {
            width: 80px;
            height: 80px;
            float: left;
            position: relative;
            padding: 8px;
            background-color: #eee;
        }

        .dragText, .dropText {
            font-size: 12px;
            line-height: 40px;
            display: inline-block;
        }

        .dragText {
            color: white;
        }

        .dropText {
            margin: 12px;
        }

        body {
            font-family: -webkit-pictograph;
        }
    </style>
		
{% endhighlight %}
	
{% highlight javascript %}	
	
           jQuery(function ($){
            $("#dragElement").ejDraggable({
                helper: function (event) {
                    return $(event.element); // Object of the Draggable element.
                },
                drag:function(event)
				{
                event.target.textContent="Dragging";
				}
            });

            $("#dropContainer").ejDroppable({
                // Drop event for change the container text while dropping element.
                drop: function (event, ui) {
                    event.dropTarget.text("Dropped..!");
                }
            });
         });	
			
{% endhighlight %}

Output of the above code will be as shown below:

Before Dragging:

![Getting_Started_Image1](Getting-Started_images/Getting-Started-img1.png)

During Drag:

![Getting_Started_Image2](Getting-Started_images/Getting-Started-img2.png)

After Dragging:

![Getting_Started_Image13](Getting-Started_images/Getting-Started-img3.png)

## Helper

Helper will return the object of corresponding draggable element. You can drag the element by using [helper](https://help.syncfusion.com/api/js/ejdraggable#events:helper) event. 

{% highlight javascript %}	

      $("#draggable-item").ejDraggable({
	      helper:function (event) {
	           return $(event.element);
                   },
	      clone:true
	     });


{% endhighlight %}

## Set Boundaries 

You can restrict the movement of draggable element within a specified area using [dragArea](https://help.syncfusion.com/api/js/ejdraggable#members:dragarea) property. 

The below code explains how to make the movement constrained to the container boundaries. 
	
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
        cursor:default;
      }
    </style>

{% endhighlight %}
	
{% highlight javascript %}	
	
    $(function () {
	   $("#draggable-item").ejDraggable({
	   dragArea:"#draggable-container",
	   helper:function (event) {
	         return $(event.element);
            }
			});
    }); 

{% endhighlight %}

The drag element cannot be moved outside this boundary.

![Getting_Started_Image](Getting-Started_images/Container.png)
