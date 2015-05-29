---
layout: post
title: exporting
description: exporting
platform: js
control: Linear Gauge
documentation: ug
---

# Exporting

**Linear Gauge** has an exporting feature that converts **Gauge** control into image format and then export in client side. The method API **exportImage** is used to export the **LinearGauge**. It has two arguments such as **file name** and **file format** to specify the file name and file formats. For exporting refer the following code example.



{% highlight js %}

**[JavaScript]**
<div id="LinearGauge1"></div>
<button id="btnSubmit">Export</button>
<div id=" fileName "> FileName </div>
<div id=" fileFormat "> FileFormat </div>
<select id="fileFormat">
<option value="JPEG">JPEG</option>
<option value="PNG">PNG</option>
</select>
<script type="text/javascript">
$(function () {
// declaration
$("#btnSubmit").ejButton({ width: "50px", click: "buttonclickevent", });
$("#fileFormat").ejDropDownList({selectedItemIndex:0,width:"115"});
//For rendering linear gauge
$("#LinearGauge1").ejLinearGauge({
labelColor: "#8c8c8c", width: 450, load: "loadGaugeTheme",

//Adding scale collection
scales: [{
width: 4, border: { color: "transparent", width: 0 }, showBarPointers: false, showRanges: true, length: 310,
position: { x: 52, y: 50 }, markerPointers: [{
value: 50, length: 10, width: 10, backgroundColor: "#4D4D4D", border: { color: "#4D4D4D" }
}],

//Adding label collection
labels: [{ font: { size: "11px", fontFamily: "Segoe UI", fontStyle: "bold" }, distanceFromScale: { x: -13 } }],

//Adding tick collection
ticks: [{ type: "majorinterval", width: 1, color: "#8c8c8c" }],

//Adding range collection
ranges: [{
endValue: 60,
startValue: 0,
backgroundColor: "#F6B53F",
border: { color: "#F6B53F" }, startWidth: 4, endWidth: 4
}, {
endValue: 100,
startValue: 60,
backgroundColor: "#E94649",
border: { color: "#E94649" }, startWidth: 4, endWidth: 4
}]
}]
});
});


function buttonclickevent() {
var FileName = $("#fileName").val();
var FileFormat = $("#fileFormat").ejDropDownList("option", "value");
$("#LinearGauge1").ejLinearGauge("exportImage", FileName, FileFormat);
}
$("#sampleProperties").ejPropertiesPanel();
</script>


{% endhighlight %}



Execute the above code to render the following output.

{% include image.html url="\js\LinearGauge\concepts-and-features\exporting_images\exporting_img1.png" Caption="LinearGauge control with Export Functionality"%}

