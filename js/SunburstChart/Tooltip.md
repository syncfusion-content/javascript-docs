---
layout: post
title: Tooltip
description: Learn how to add Tooltip to Sunburstchart .
platform: js
control: Sunburst Chart
documentation: ug
api: /api/js/ejsunburstchart
---

## Tooltip  

[`ToolTip`](../api/ejsunburstchart#members:tooltip) allows you to display any information over a sunburst segment. It appears when mouse hovered over or touch any chart segment. By default, it displays the corresponding segment category name and its value
you can set the [`visible`](../api/ejsunburstchart#members:tooltip-visible) property as true or false.

{% highlight js %}

$("#chart").ejSunburstChart ({
    //...
	tooltip: {visible: true},
    //.. 

   });


{% endhighlight %}

![](/js/SunburstChart/Tooltip_images/Tooltip_img1.png)

## Tooltip Template   

HTML elements can be displayed in the tooltip by using the [`template`](../api/ejsunburstchart#members:tooltip-template) property of the tooltip. The template property takes the value of the id attribute of the HTML element. You can use this [`format`](../api/ejsunburstchart#members:tooltip-format) **#point.x#** and **#point.y#** as place holders in the HTML element to display the x and y values of the corresponding point.

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


## Customize the appearance of tooltip

* The [`fill`](../api/ejsunburstchart#members:tooltip-fill) and [`border`](../api/ejsunburstchart#members:tooltip-border) options are used to customize the background color and border of the tooltip respectively. 

* You can change this default border of the tooltip by using the [`width`](../api/ejsunburstchart#members:tooltip-border-width) and [`color`](../api/ejsunburstchart#members:tooltip-border-color) options.

* The opacity of the tooltip are customized by using the [`opacity`](../api/ejsunburstchart#members:tooltip-opacity) properties.The [`font`](../api/ejsunburstchart#members:tooltip-font) option in the tooltip is used to customize the font of the tooltip text.

* Using font property, you can customize [`font color`](../api/ejsunburstchart#members:tooltip-font-color), [`font family`](../api/ejsunburstchart#members:tooltip-font-fontfamily), [`font style`](../api/ejsunburstchart#members:tooltip-font-fontstyle), [`font weight`](../api/ejsunburstchart#members:tooltip-font-fontweight), [`opacity`](../api/ejsunburstchart#members:tooltip-font-opacity), [`size`](../api/ejsunburstchart#members:tooltip-font-size) options.

{% highlight js %}

$("#container").ejSunburstChart({
            // ...
          
                 tooltip: {
                       //Change tooltip color and border
                       fill: '#FF9933',
                       border: { width: 1, color: "#993300" },
                       font: {color:"black",fontWeight:"bold",size:"15px"}	
                       // ...
                 } 
            
            // ...
        });

{% endhighlight %}