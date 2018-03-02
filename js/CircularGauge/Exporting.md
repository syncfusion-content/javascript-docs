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

**Circular Gauge** has an exporting feature that converts **Gauge** control into image format and then export in client side. The method API [`exportImage`](../api/ejcirculargauge#methods:exportimage) is used to export the **Circular Gauge**. It has two arguments such as **file name** and **file format** to specify the file name and file formats. For exporting refer the following code example.

{% highlight html %}

<input type="submit" value="Export Image" id="btnExportImage">
    <div id=" circulargauge "></div>
    <div id="txtFileName">FileName </div>
    <div id="ddFileType">FileFormat </div>
</input>
<select id="Select1">
    <option value="JPEG">JPEG</option>
    <option value="PNG">PNG</option>
</select>

{% endhighlight %}

{% highlight javascript %}

$(function () {
        $("#circulargauge").ejCircularGauge();
        $("#btnExportImage").ejButton({ width: "100px", click: "buttonClickEvent", });
    });
    function buttonClickEvent() {
        var FileName = $("#txtFileName").val();
        var FileFormat = $("#ddFileType").val();
        $("#circulargauge").ejCircularGauge("exportImage", FileName, FileFormat);
    }

{% endhighlight %}


Execute the above code to render the following output.

![](/js/CircularGauge/Exporting_images/Exporting_img1.png)

### Export Properties

Each [`export`](../api/ejcirculargauge#members:exportsettings) object contains the following list of properties.

[`type`](../api/ejcirculargauge#members:exportsettings-type) - Specifies the format of the file to export

[`fileName`](../api/ejcirculargauge#members:exportsettings-filename) - Specifies the downloading filename 

[`action`](../api/ejcirculargauge#members:exportsettings-action) - Specifies the name of the action URL 

[`mode`](../api/ejcirculargauge#members:exportsettings-mode) - Specifies the mode of exporting

