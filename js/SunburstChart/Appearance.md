---
layout: post
title: Appearance
description: What are the different ways to customize the SunburstChart 
platform: js
control: SunburstChart
documentation: ug
api: /api/js/ejsunburstchart
---

# Appearance
The appearance of the Sunburst Chart can be customized as shown below 

## Palette
The Sunburst Chart displays different segments in different colors by default. You can customize the color of each segment by providing a custom color palette of your choice by using the [`palette`](../api/ejsunburstchart#members:palette) property.

{% highlight js %}

$("#chart"). ejSunburstChart ({
palette: ["#002e4d", "#005c99", "#008ae6", "#33adff", "#80ccff"],	
   });

{% endhighlight %}

The Sunburst Chart rendered with palette colors

![](/js/SunburstChart/Appearance_images/Appearance_img1.png)

 
## Built- in Themes
The Sunburst Chart supports different themes. 
*	flatlight
*	flatdark
*	gradientlight
*	gradientdark
*	azure
*	azuredark
*	lime
*	limedark
*	saffron
*	saffrondark
*	gradient-azure
*	gradient-azuredark
*	gradient-lime
*	gradient-limedark
*	gradient-saffron
*	gradient-saffrondark

You can set your desired theme by using the [`theme`](../api/ejsunburstchart#members:theme) property. **Flat light** is the default theme used in the Sunburst Chart.

{% highlight js %}

$("#chart"). ejSunburstChart ({

theme: "flatdark",	
   
   });

{% endhighlight %}

![](/js/SunburstChart/Appearance_images/Appearance_img2.png)

## Background color

It specifies the [`background`](../api/ejsunburstchart#members:background) color of the plot area.

{% highlight js %}

$("#chart"). ejSunburstChart ({

background: "grey",	
   
   });

{% endhighlight %}

### Responsiveness during browser resize

Sunburst chart is made responsive when resizing the browser by using [`isResponsive`](../api/ejsunburstchart#members:isresponsive) property.

{% highlight js %}

$("#chart"). ejSunburstChart ({

   isResponsive:true,
   
   });

{% endhighlight %}