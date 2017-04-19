---
layout: post
title: Datalabel Customization
description: Learn how to customize datalabels in Sunburst Chart.
platform: ts
control: SunburstChart
documentation: ug
api: /api/js/ejsunburstchart
---

# Data Labels 

Sunburst data labels are used to display the data related to the segment. It helps to provide the information about the data points to the users.
You can enable or disable the data labels by setting the [`visible`](../api/ejsunburstchart#members:datalabelSettings-visible) property of the [`dataLabelSettings`](../api/ejsunburstchart#members:datalabelSettings) to true as shown in the below code

{% highlight js %}

$("#chart"). ejSunburstChart ({

	 dataLabelSettings:{visible:true},
   });
 {% endhighlight %}

![](/js/SunburstChart/DataLabel_images/DataLabel_img1.png)

## Label Overflow mode

When you represent huge data with data labels, they may intersect each other. You can avoid this using the [`labelOverflowMode`](../api/ejsunburstchart#members:datalabelSettings-labelOverflowMode) property.

The following properties are used to avoid the overlapping.
*	Trim – To trim the large data labels.
*	Hide – To hide the overlapped data labels.
The following code shows how to set Hide and Trim mode.

{% highlight js %}

$("#chart"). ejSunburstChart ({

	dataLabelSettings: {visible: true,labelOverflowMode:"hide"},
   });

 {% endhighlight %}

![](/js/SunburstChart/DataLabel_images/DataLabel_img2.png) 

{% highlight js %}


$("#chart"). ejSunburstChart ({

	dataLabelSettings: {visible: true,labelOverflowMode:"trim"},
   });

 {% endhighlight %}

![](/js/SunburstChart/DataLabel_images/DataLabel_img3.png)

## Label Rotation Mode
You can rotate the data label by using [`labelRotationMode`](../api/ejsunburstchart#members:datalabelSettings-labelRotationMode) property. By default, the labelRotationMode is set as **angle**. 

The following code shows how to set labelRotationMode as normal and angle.

{% highlight js %}
$("#chart"). ejSunburstChart ({

	dataLabelSettings: {visible: true,labelRotationMode:"normal"},
   });

 {% endhighlight %}

![](/js/SunburstChart/DataLabel_images/DataLabel_img4.png)

{% highlight js %}
$("#chart"). ejSunburstChart ({

	dataLabelSettings: {visible: true,labelRotationMode:"angle"},
   });

{% endhighlight %}

![](/js/SunburstChart/DataLabel_images/DataLabel_img5.png)
 
## Customizing the data labels
You can customize the appearance of the data point using the [`font`](../api/ejsunburstchart#members:datalabelSettings-font) property.


{% highlight js %}
$("#chart"). ejSunburstChart ({
	dataLabelSettings: {visible: true, font: {color:"black",fontWeight:"bold",size:"15px"}},
   });

{% endhighlight %}

![](/js/SunburstChart/DataLabel_images/DataLabel_img6.png)

