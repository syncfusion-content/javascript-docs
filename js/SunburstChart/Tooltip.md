---
layout: post
title: Tooltip
description: Learn how to add Tooltip to Sunburstchart .
platform: ts
control: Sunburst Chart
documentation: ug
api: /api/js/ejsunburstchart
---

## Tooltip  

[`ToolTip`](../api/ejsunburstchart#members:tooltip) allows you to display any information over a sunburst segment. It appears when mouse hovered over or touch any chart segment. By default, it displays the corresponding segment category name and its value

{% highlight js %}

$("#chart").ejSunburstChart ({
    //...
	tooltip: {visible: true},
    //.. 

   });


{% endhighlight %}

![](/js/SunburstChart/Tooltip_images/Tooltip_img1.png)

## Tooltip Template   

HTML elements can be displayed in the tooltip by using the [`template`](../api/ejsunburstchart#members:tooltip-template) property of the tooltip. The template property takes the value of the id attribute of the HTML element. You can use the **#point.x#** and **#point.y#** as place holders in the HTML element to display the x and y values of the corresponding point.

{% highlight js %}

<div id="Tooltip" style="display: none;">
        <div id="value" style="background-color:red;padding-top:3px;padding-right:3px">
            <div>
                <label id="efpercentage" style="color:white">
                    &nbsp;&nbsp;Category:&nbsp;#point.x#
                   <br />&nbsp;&nbsp;Value:#point.y#
                </label>
            </div>
        </div>
    </div>

$("#chart").ejSunburstChart ({
	tooltip: { visible: true,
    template:"Tooltip"},
   });


{% endhighlight %}

![](/js/SunburstChart/Tooltip_images/Tooltip_img2.png)
