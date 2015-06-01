---
layout: post
title: Tooltip
description: tooltip
platform: js
control: Circular Gauge
documentation: ug
---

# Tooltip

**Tooltip** feature has been added to the **Circular Gauge**. **Circular Gauge** has several elements such as pointers, label, customLabel, scales, etc. There is a need for **Tooltip** feature in the **Circular Gauge** control because whenever the text hides or overrides with other gauge elements, it may not be fully visible. For resolving those problems **Tooltip** feature has been implemented in the **Circular Gauge** control.

## Default Tooltip

**Tooltip** has three attributes in it. The first two attributes such as **showLabelTooltip** and **showCustomLabelTooltip** are for enabling the **Tooltip** for label as well as custom label in default appearance. 

**ShowLabelTooltip** is to enable the **Tooltip** for labels and **showCustomLabelTooltip** is for enabling the **Tooltip** option for customLabels.

{% highlight js %}

**[JavaScript]**
<div id="tooltipGauge"></div>
<script type=”text/javascript”>
$(function () {
$(“#tooltipGauge”).ejCircularGauge({

//Defines the tooltip object.
tooltip: {

//Enables the label tooltip.
showLabelTooltip: true,

//Enables the custom label tooltip.
showCustomLabelTooltip: true,
},

//Customizes the scale options.
scales: [{
showLabels: true,
radius: 130,

//Customizes the custom label options.
customLabels: [{
value: "095345",
font: {
size: "18px",
fontFamily: "Arial",
fontStyle: "bold"
},

position: { x: 180, y: 220 }
}],

//Customizes the pointers options.
pointers: [{
value: 60,
length: 95,
}]
}]
});
});
</script>


{% endhighlight %}



Execute the above code to render the following output.

{% include image.html url="/js/CircularGauge/Concepts-and-Features/Tooltip_images/Tooltip_img1.png" Caption="Gauge with Default ToolTip"%}

## Tooltip Template

In **Tooltip** option, you can customize the Tooltip window by adding the tooltip template on that page with the help of API **TemplateID**. Refer to the following code example to know more about Tooltip template.

{% highlight js %}

**[JavaScript]**

<div id=”Tooltip” style=”height: 60px; display: none;”>
<div id=”icon”>
<div id=”eficon”></div>
</div>
<div id=”value”>
<div>
<label id=”efpercentage”>&nbsp;#label#</label>
</div>
</div>
</div>
<div id="tooltipGauge"></div>

<script type=”text/javascript”>
$(function () {
$(“#tooltipGauge”).ejCircularGauge({

//Defines the tooltip object.
tooltip: {

// Enables the label tooltip.
showLabelTooltip: true,

// Enables the custom label tooltip.
showCustomLabelTooltip: true,

// Adds tooltip template.
templateID: “Tooltip”
},

// Customizes the scale options.
scales: [{
showLabels: true,
radius: 130,

// Customizes the custom label options.
customLabels: [{
value: “0 9 5 3 4 5”,
font: {
size: "18px",
fontFamily: "Arial",
fontStyle: "bold"
},

position: { x: 180, y: 220 }
}],

// Customizes the pointers options.
pointers: [{
value: 60,
length: 95,
}]
}]
});
});
</script>
<style type=”text/css”>

// Adds the necessary styles here.

</style>


{% endhighlight %}


Execute the above code to render the following output.

{% include image.html url="/js/CircularGauge/Concepts-and-Features/Tooltip_images/Tooltip_img2.png" Caption="Circular gauge with tooltip template"%}

