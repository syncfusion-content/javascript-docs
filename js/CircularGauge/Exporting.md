---
layout: post
title: Exporting
description: exporting
platform: js
control: Circular Gauge
documentation: ug
api: /api/js/ejcirculargauge
---

# Exporting

**Circular Gauge** has an exporting feature that converts **Gauge** control into image format and then export in client side. The method API **exportImage** is used to export the **Circular Gauge**. It has two arguments such as **file name** and **file format** to specify the file name and file formats. For exporting refer the following code example.

{% highlight html %}

<input type="submit" value="Export Image" id="btnExportImage">
    <div id=" circulargauge "></div>
    <div id="txtFileName">FileName </div>
    <div id="ddlFileType">FileFormat </div>
</input>
<select id="Select1">
    <option value="JPEG">JPEG</option>
    <option value="PNG">PNG</option>
</select>

{% endhighlight %}

{% highlight javascript %}

$(function () {
        $("#circulargauge").ejCircularGauge();
        $("#btnExportImage").ejButton({ width: "100px", click: "buttonclickevent", });
    });
    function buttonclickevent() {
        var FileName = $("#txtFileName").val();
        var FileFormat = $("#ddlFileType").val();
        $("#circulargauge").ejCircularGauge("exportImage", FileName, FileFormat);
    }

{% endhighlight %}


Execute the above code to render the following output.

![](/js/CircularGauge/Exporting_images/Exporting_img1.png)

