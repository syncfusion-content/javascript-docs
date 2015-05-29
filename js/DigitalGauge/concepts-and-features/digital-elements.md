---
layout: post
title: digital-elements
description: digital elements
platform: js
control: Digital Gauge
documentation: ug
---

# Digital Elements

**Text Customization**

* The attribute **value** refers the text displayed in the **Digital Gauge**. This text is applicable only for that item instead of all items. Text color is changed by using the property **textColor.**

* It is possible to align the text inside the **Digital Gauge** control by using the property **textAlign**. Two possible values for text align are as follows

1. left

2. right

{% highlight js %}

**[JavaScript]**
<div id="DigitalGauge1"></div>
<script type="text/javascript">
$(function () {
// For Digital Gauge rendering
$("#DigitalGauge1").ejDigitalGauge({
items:[{
// For setting alingment
textAlign: "right",
// For setting text
value**:** "STOP",
}]
})
});
</script>


{% endhighlight %}



Execute the above code examples to render the **Digital****Gauge** as follows.



{% include image.html url="\js\DigitalGauge\concepts-and-features\digital-elements_images\digital-elements_img1.png" Caption="Figure 29: Digital Gauge control with text customization"%}

