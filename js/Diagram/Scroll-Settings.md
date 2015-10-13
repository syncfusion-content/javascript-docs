---
layout: post
title: Scroll-Settings
description: Scroll settings
platform: js
control: Diagram
documentation: ug
---

# Scroll Settings
The diagram can be scrolled using the vertical and horizontal scrollbars. In addition to the scrollbars, you can use mouse wheel to scroll the diagram. 
Diagram's `scrollSettings` enables you to read the current scroll status, view port size, current zoom and zoom factor. It also allows you to scroll the diagram programmatically. 

## Get current scroll status

Scroll settings allows you to read the scroll status, view port size and current zoom factor with a set of propeties. To explore those properties, see [Scroll Settings](/js/api/ejDiagram "members:scrollSettings")

## Define scroll status
Diagram allows you to pan the diagram before loading, so that any desired region of a large diagram will be bring into view. You can programmatically pan the diagram with the `horizontalOffset` and `verticalOffset` properties of scroll settings. The following code illustrates how to set pan the diagram programmatically.

{% highlight js %}

    $("#diagram").ejDiagram({
        height: "400px",
        width: "400px",
        //Set horizontal and vertical scroll offsets
        scrollSettings: {
            horizontalOffset: 100,
            verticalOffset: 50,
            zoomFactor: 0.2
        },

        //Set page settings
        pageSettings: {
            pageWidth: 500,
            pageHeight: 500
        }
    });

{% endhighlight %}

In the example given below, the vertical scroll bar is scrolled down by 50px and horizontal scroll bar is scrolled to right by 100px. 

{% include image.html url="/js/Diagram/Scroll-Settings/Scroll-Settings_img1.png" %}

## Update scroll status

You can programmatically change the scroll offsets at runtime using the client side method `update`. The following code illustrates how to change the scroll offsets and zoom factor at runtime.

{% highlight js %}

            var diagram = $("#diagram").ejDiagram("instance");
            var scrollSettings = {
                //Set scroll status
                horizontalOffset: 200,
                verticalOffset: 200,
                
                //Set zoomFactor
                zoomFactor: 0.5
            }

            //update scroll settings
            diagram.update({ scrollSettings: scrollSettings });
            
{% endhighlight %}

## AutoScroll 

Autoscroll feature automatically scrolls the diagram whenever the node or connector is moved beyond the boundary of the diagram. So that, it is always visible during dragging, resizing and multiple selection operations. Autoscroll is automatically triggered when any one of the following is done towards edges of the diagram.

  * Node dragging , resizing 

  * Connection editing

  * Rubber band selection

  * Label dragging

## Autoscroll border

The auto scroll border is used to specify the maximum distance between the object and diagram edge to trigger auto scroll. The default value is set as 15 for all sides (left, right, top and bottom) and it can be changed using the `autoScrollBorder` property of page settings. The following code example illustrates how to set autoscroll border. 

{% highlight js %}

      $("#Diagram").ejDiagram({      
            pageSettings: {            
                  // Specifies autoscroll border            
                  autoScrollBorder: { left: 150, top: 15, right: 15, bottom: 15 }
            }      
      });

{% endhighlight %}

## Scroll limit

The scroll limit allows you to define the scrollable region of diagram. It includes the following options.

* Allows to scroll in all directions, without any restrictions

* Allows to scroll within the diagram content.

* Allows to scroll within the specified scrollable area.

`scrollLimit` property of scroll settings helps to limit the scrolling. For the accepted values of the scrollLimit, refer [Scroll Limit](/js/api/ejDiagram "Scroll-Limit").

The following code example illustrates how to specify the scroll limit.

{% highlight js %}

      $("#diagram").ejDiagram({      
            pageSettings: {             
            //Set the scroll limit            
            scrollLimit: "infinity"            
            }      
      });

{% endhighlight %}

## Scrollable Area

You can restrict scrolling beyond any particular rectangular area using the `scrollableArea` property of scroll settings. To restrict scrolling beyind any custom region, you have to set the `scrollLimit` as "limited". The following code example illustrates how to customize scrollable area.

{% highlight js %}
   
      $("#diagram").ejDiagram({      
            pageSettings: {            
                  //Set scroll limit as limited            
                  scrollLimit: "limited",            
                  //Set the limited scrollable area            
                  scrollableArea: {            
                        x: 0,            
                        y: 0,            
                        width: 500,            
                        height: 500            
                  }            
            }      
      });
{% endhighlight %}
