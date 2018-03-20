---
layout: post
title: Sunburst Zooming
description: Learn how to Zoom the SunburstChart for better data visualization
platform: js
control: SunburstChart
documentation: ug
api: /api/js/ejsunburstchart
---

# Zooming

Sunburst chart provides zooming (drill down) experience with animation for both mouse and touch enabled devices. It allows you to virtualizing the large sets of data into minimum data view.The zooming is achieved by using the property of [`zoomSettings`](../api/ejsunburstchart#members:zoomsettings)

The following code shows how to initialize the zooming.

{% highlight js %}

$("#chart"). ejSunburstChart ({

zoomSettings: { enable: true },	
   });

{% endhighlight %}

![](/js/SunburstChart/Zooming_images/Zooming_img1.gif)

## Zooming toolbar
By default, zooming toolbar will be enabled while zooming the segment.It contains both back and reset option.
You can align the zooming toolbar position by using [`toolbarHorizontalAlignment`](../api/ejsunburstchart#members:zoomsettings-toolbarhorizontalalignment) and [`toolbarVerticalAlignment`](../api/ejsunburstchart#members:zoomsettings-toolbarverticalalignment) property.


{% highlight js %}

$("#chart"). ejSunburstChart ({
zoomSettings: {enable: true,toolbarHorizontalAlignment: "left"},	
   });

{% endhighlight %}

![](/js/SunburstChart/Zooming_images/Zooming_img2.png)

[Click](http://js.syncfusion.com/demos/web/#!/bootstrap/sunburst/zooming) here to view the online demo sample of Zooming in  the Sunburst Chart
