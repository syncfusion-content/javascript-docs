---
layout: post
title: Data Label in JavaScript SunburstChart widget | Syncfusion
description: You can learn here about data label support in Syncfusion JavaScript SunburstChart control and more details.
platform: js
control: SunburstChart
documentation: ug
api: /api/js/ejsunburstchart
---

# Data Label in JavaScript SunburstChart

Sunburst data labels are used to display the data related to the segment. It helps to provide the information about the data points to the users.
You can enable or disable the data labels by setting the [`visible`](../api/ejsunburstchart#members:datalabelSettings-visible) property of the [`dataLabelSettings`](../api/ejsunburstchart#members:datalabelSettings) to true as shown in the below code

{% highlight js %}

$("#chart"). ejSunburstChart ({

	 dataLabelSettings:{visible:true},
   });
 {% endhighlight %}

![Visual representation of DataLabel SunburstChart using JavaScript](DataLabel_images/DataLabel_img1.png)

## Label Overflow mode

When you represent huge data with data labels, they may intersect each other. You can avoid this using the [`labelOverflowMode`](../api/ejsunburstchart#members:datalabelsettings-labeloverflowmode) property.

The following properties are used to avoid the overlapping.
*	Trim – To trim the large data labels.
*	Hide – To hide the overlapped data labels.
The following code shows how to set Hide and Trim mode.

{% highlight js %}

$("#chart"). ejSunburstChart ({

	dataLabelSettings: {visible: true,labelOverflowMode:"hide"},
   });

 {% endhighlight %}

![Label Overflow mode - Hide using SunburstChart in JavaScript](DataLabel_images/DataLabel_img2.png) 

{% highlight js %}


$("#chart"). ejSunburstChart ({

	dataLabelSettings: {visible: true,labelOverflowMode:"trim"},
   });

 {% endhighlight %}

![Label Overflow mode - Trim using SunburstChart in JavaScript](DataLabel_images/DataLabel_img3.png)

## Label Rotation Mode
You can rotate the data label by using [`labelRotationMode`](../api/ejsunburstchart#members:datalabelsettings-labelrotationmode) property. By default, the labelRotationMode is set as **angle**. 

The following code shows how to set labelRotationMode as normal and angle.

{% highlight js %}
$("#chart"). ejSunburstChart ({

	dataLabelSettings: {visible: true,labelRotationMode:"normal"},
   });

 {% endhighlight %}

![Label Rotation Mode - Normal using SunburstChart in JavaScript](DataLabel_images/DataLabel_img4.png)

{% highlight js %}
$("#chart"). ejSunburstChart ({

	dataLabelSettings: {visible: true,labelRotationMode:"angle"},
   });

{% endhighlight %}

![Label Rotation Mode - Angle using SunburstChart in JavaScript](DataLabel_images/DataLabel_img5.png)
 
## Customizing the data labels

You can customize the appearance of the data point using the [`font`](../api/ejsunburstchart#members:datalabelsettings-font) property.

Using font property, you can customize [`font color`](../api/ejsunburstchart#members:datalabelsettings-font-color), [`font family`](../api/ejsunburstchart#members:datalabelsettings-font-fontfamily), [`font style`](../api/ejsunburstchart#members:datalabelsettings-font-fontstyle), [`font weight`](../api/ejsunburstchart#members:datalabelsettings-font-fontweight), [`opacity`](../api/ejsunburstchart#members:datalabelsettings-font-opacity), [`size`](../api/ejsunburstchart#members:datalabelsettings-font-size) options.

The color for the datalabel text is set by using the [`fill`](../api/ejsunburstchart#members:datalabelsettings-fill) property.

{% highlight js %}
$("#chart"). ejSunburstChart ({
	dataLabelSettings: {visible: true, font: {color:"black",fontWeight:"bold",size:"15px"}},
   });

{% endhighlight %}

![Customizing the data labels using SunburstChart in JavaScript](DataLabel_images/DataLabel_img6.png)

## Data Label Template

Label content can be formatted by using the [`template`](../api/ejsunburstchart#members:datalabelsettings-template) option.

{% highlight js %}

<div id="item">
     <div id="left">
	<img src="../images/chart/icon_investments.png"/>
     </div>
     <div id="right">
          <div id="point">#point.y#%</div>
     </div>
</div> 

$("#chart").ejSunburstChart({
    dataLabelSettings :{ template: "item" }               
});

{% endhighlight %}

