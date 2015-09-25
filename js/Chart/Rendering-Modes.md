---
layout: post
title: Rendering-Modes
description: rendering modes                    
platform: js
control: Chart
documentation: ug
---

# Rendering Modes

Chart uses following three rendering technologies

   * VML
   * SVG
   * HTML5 Canvas

## VML

VML is used to render chart in IE lower versions such as IE7 and IE8. VML is used by default in these two browsers, as SVG and Canvas are not supported in these browsers.

**Limitations:**

* Label rotation is not supported.
* Animation is not supported.
* Patterns are not supported.
* Zooming and panning features are not supported.

## SVG

SVG is used to render Chart by default for all browsers other than IE7 and IE8.

## Canvas

You can switch between SVG and Canvas rendering using **enableCanvasRendering** option. We recommend using canvas mode rendering in the following scenarios,

* Plotting large number of data points.
* Performing high frequency live updates.
 
The following code example shows how to enable HTML5 Canvas rendering in chart.


{% highlight js %}


       $("#chartcontainer").ejChart({
                    
             //Rendering chart in canvas mode
             enableCanvasRendering: true
             
             // ...
        });


{% endhighlight %}

{% include image.html url="/js/Chart/Rendering-Modes_images/Rendering-Modes_img1.png" Caption="Canvas Chart"%}

**Limitations:**
  
* Animation is not supported.
* 3D charts are not supported.


