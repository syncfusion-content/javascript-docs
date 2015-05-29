---
layout: post
title: exporting-the-digital-gauge
description: exporting the digital gauge
platform: js
control: Digital Gauge
documentation: ug
---

# Exporting the Digital Gauge

**Digital Gauge** has an exporting feature where **Gauge** control is converted into image format and then exported to client-side. The method API **exportImage** exports the **Digital Gauge**. It has two arguments such as **file****name** and **file format**. For exporting, you can refer the following code example.



{% highlight js %}

**[JavaScript]**
<div id="DigitalGauge1"></div>
<button id="btnSubmit">Export</button>
<div id=" fileName "> FileName </div>
<div id=" fileFormat "> FileFormat </div>
<select id="fileFormat">
<option value="JPEG">JPEG</option>
<option value="PNG">PNG</option>
</select>
<script type="text/javascript">
$(function () {
$("#btnSubmit").ejButton({ width: "50px", text: "Export", click: "buttonclickevent", });
$("#fileFormat").ejDropDownList({ selectedItemIndex: 0,width:"115px" });
$("# DigitalGauge1").ejDigitalgauge({value: "Syncfusion"});
});
$("# DigitalGauge1").ejDigitalGauge("exportImage", "Digital", "JPEG");
function buttonclickevent() {
var FileName = $("#fileName").val();
var FileFormat = $("#fileFormat").ejDropDownList("option", "value");
var flag = $("#DigitalGauge1").ejDigitalGauge("exportImage", FileName, FileFormat);
if (!flag)
alert("Sorry for the inconvenience. Export is currently not supported in Internet Explorer 9 and below version");
}
</script>



{% endhighlight %}



Execute the above code examples to render the **Digital****Gauge** as follows.



























{% include image.html url="\js\DigitalGauge\concepts-and-features\exporting-the-digital-gauge_images\exporting-the-digital-gauge_img1.png" Caption="Figure 37: Digital Gauge control with Export functionality"%}

