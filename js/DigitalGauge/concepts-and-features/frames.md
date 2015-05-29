---
layout: post
title: frames
description: frames
platform: js
control: Digital Gauge
documentation: ug
---

# Frames

## Inner and Outer Width Customization

**Frames** are space that enclose the **Digital Gauge**. The inner width of the **Frame** is the distance between the canvas element and the frame. The outer width is the distance from the frame. The code example to set frame’s **innerWidth** and **outerWidth** is as follow.

{% highlight js %}

**[JavaScript]**
<div id="DigitalGauge1"></div>
<script type="text/javascript">
$(function () {
// For Digital Gauge rendering
$("#DigitalGauge1").ejDigitalGauge({
// For setting text
value**:** "WELCOME",
frame: {
// For setting inner width
innerWidth: 6,
// For setting outer width
outerWidth: 10,
},
})
});
</script>


{% endhighlight %}



Execute the above code examples to render the **Digital****Gauge** as follows.



{% include image.html url="\js\DigitalGauge\concepts-and-features\frames_images\frames_img1.png" Caption="Figure 27: Digital Gauge control with frame inner and outer width"%}



## Setting Background Image

For a better appearance, you can set the **background****image** for the **Digital Gauge** using the property **backgroundImageUrl.** 



{% highlight js %}

**[JavaScript]**
<div id="DigitalGauge1"></div>
<script type="text/javascript">
$(function () {
// For Digital Gauge rendering
$("#DigitalGauge1").ejDigitalGauge({
// For setting text
value**:** "RADAR",
frame: {
// For setting backgroung image
backgroundImageUrl: "board3.jpg",
},
items:[{
position:{
x:80,
y:10
}
}]

})
});
</script>


{% endhighlight %}



Execute the above code examples to render the **Digital****Gauge** as follows.





{% include image.html url="\js\DigitalGauge\concepts-and-features\frames_images\frames_img2.png" Caption="Figure 28: Digital Gauge control with frame background image"%}



