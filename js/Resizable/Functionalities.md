---
layout: post
title: Getting started with Resizable widget for Syncfusion Essential JS
description: To get start with Resizable by adding references.
platform: js
control: Resizable
documentation: ug
keywords: Resizable,Resize
api: /api/js/ejresizable
---

# Functionalities


## Delay Resize

You can set the required distance the mouse should travel in order to initiate resize using [distance](https://help.syncfusion.com/api/js/ejresizable#members:distance) property.

{% highlight html %}

   <div id="Container">
        <!-- Resizable element-->
        <div id="resizeElement" class="Resize">
            <span class="Resizetext">Resize</span>
        </div>

    </div>
    <style>
        #Container {
            width: 100px;
            height: 100px;
            padding: 30px;
            float: left;
        }


        .Resize {
            width: 120px;
            height: 100px;
            float: left;
            font-size: 14px;
            line-height: 37px;
            color: white;
            text-align: center;
            z-index: 100002;
            background-color: #666;
            cursor: nw-resize;
        }


        .Resizetext {
            font-size: 15px;
            line-height: 80px;
            display: inline-block;
            color: white;
        }

        body {
            font-family: -webkit-pictograph;
        }
    </style>


 
{% endhighlight %}

{% highlight javascript %}

   jQuery(function ($) {
          $("#resizeElement").ejResizable({
              helper: function (event) {
                  return $(event.element); // Object of the Resizable element.
              },
              distance:20
          });



      });


{% endhighlight %}

## Cursor Distance

You can set the offset for resize helper with respect to the mouse cursor using [cursorAt](https://help.syncfusion.com/api/js/ejresizable#members:cursorat) property.

{% highlight html %}

    <div id="Container">
        <!-- Resizable element-->
        <div id="resizeElement" class="Resize">
            <span class="Resizetext">Resize</span>
        </div>

    </div>
    <style>
        #Container {
            width: 100px;
            height: 100px;
            padding: 30px;
            float: left;
        }


        .Resize {
            width: 120px;
            height: 100px;
            float: left;
            font-size: 14px;
            line-height: 37px;
            color: white;
            text-align: center;
            z-index: 100002;
            background-color: #666;
            cursor: nw-resize;
        }


        .Resizetext {
            font-size: 15px;
            line-height: 80px;
            display: inline-block;
            color: white;
        }

        body {
            font-family: -webkit-pictograph;
        }
    </style>

{% endhighlight %}

{% highlight javascript %}

         jQuery(function ($) {
          $("#resizeElement").ejResizable({
              helper: function (event) {
                  return $(event.element); // Object of the Resizable element.
              },
             cursorAt:{ top: 3, left: -2 }
          });
      });

{% endhighlight %}

## Restrict Resize Height and Width:

[minHeight](https://help.syncfusion.com/api/js/ejresizable#members:minheight), [minWidth](https://help.syncfusion.com/api/js/ejresizable#members:minwidth), [maxHeight](https://help.syncfusion.com/api/js/ejresizable#members:maxheight) and [maxWidth](https://help.syncfusion.com/api/js/ejresizable#members:maxwidth) can be used to restrict the height and width below or above which the element cannot be resized.


{% highlight html %}

     <div id="Container">
        <!-- Resizable element-->
        <div id="resizeElement" class="Resize">
            <span class="Resizetext">Resize</span>
        </div>

    </div>
    <style>
        #Container {
            width: 100px;
            height: 100px;
            padding: 30px;
            float: left;
        }


        .Resize {
            width: 120px;
            height: 100px;
            float: left;
            font-size: 14px;
            color: white;
            text-align: center;
            z-index: 100002;
            background-color: #666;
            cursor: nw-resize;
        }


        .Resizetext {
            font-size: 15px;
            margin-top:30px;
            display: inline-block;
            color: white;
        }

        body {
            font-family: -webkit-pictograph;
        }
    </style>

{% endhighlight %}

{% highlight javascript %}

           jQuery(function ($) {
          $("#resizeElement").ejResizable({
              helper: function (event) {
                  return $(event.element); // Object of the Resizable element.
              },
              minHeight: 80,
              minWidth: 90,
              maxHeight: 130,
              maxWidth: 150,
              resizeStop:function(event)
              {
                  if (event.element.height() == 130)
                      $(".Resizetext")[0].innerText = "Cannot exceed maxHeight";
                  if (event.element.width() == 150)
                      $(".Resizetext")[0].innerText = "Cannot exceed maxWidth"
                  if(event.element.height() == 80)
                      $(".Resizetext")[0].innerText = "Below minHeight";
                  if (event.element.width() == 90)
                      $(".Resizetext")[0].innerText = "Below minWidth";
              }
          });

      });

{% endhighlight %}

Before Resize:

![](Functionalities_images/Resize.png)

When resize beyond maxWidth:

![](Functionalities_images/maxWidth.png)

When resize beyond maxHeight:

![](Functionalities_images/maxHeight.png)

When resize below minWidth:

![](Functionalities_images/minWidth.png)

When resize below minHeight:

![](Functionalities_images/minHeight.png)