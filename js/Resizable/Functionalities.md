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

We can set the required distance the mouse should travel in order to initiate resize using [distance](https://help.syncfusion.com/api/js/ejresizable#members:distance) property.

{% highlight html %}

   <div id="Container">
        <!-- Resizable element-->
        <div id="resizeElement" class="Resize">
            <span class="ResizeText">Resize</span>
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


        .ResizeText {
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

We can set the offset for resize helper with respect to the mouse cursor using [cursorAt](https://help.syncfusion.com/api/js/ejresizable#members:cursorat) property.

{% highlight html %}

    <div id="Container">
        <!-- Resizable element-->
        <div id="resizeElement" class="Resize">
            <span class="ResizeText">Resize</span>
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


        .ResizeText {
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

We have some properties [minHeight](https://help.syncfusion.com/api/js/ejresizable#members:minheight), [minWidth](https://help.syncfusion.com/api/js/ejresizable#members:minwidth), [maxHeight](https://help.syncfusion.com/api/js/ejresizable#members:maxheight) and [maxWidth](https://help.syncfusion.com/api/js/ejresizable#members:maxwidth) which can be used to restrict the height and width below or above which the element cannot be resized.


{% highlight html %}

     <div id="Container">
        <!-- Resizable element-->
        <div id="resizeElement" class="Resize">
            <span class="ResizeText">Resize</span>
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


        .ResizeText {
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
             scope:"Container",
              minHeight: 80,
              minWidth: 90,
              maxHeight: 130,
              maxWidth: 150,
              resizeStop:function(event)
              {
                  if ((event.element.height() == 130)||(event.element.width() == 150)||(event.element.height() == 80)||(event.element.width() == 90))
                      $(".ResizeText")[0].innerText = "Resize Restricted.Out of scope!";
                  
              }
          });

      });

{% endhighlight %}

Before Resize:

![](Functionalities_images/Resize.png)

When resize done out of these limits:

![](Functionalities_images/Exceed.png)