---
layout: post
title: exporting
description: exporting
platform: js
control: Chart
documentation: ug
---

# Exporting

The **EJChart** supports client-side exporting using **canvg** script. **canvg** is a **SVG** parser and renderer. It takes a **URL** to a **SVG** file or the text of an SVG file, parses it to canvas, and renders the canvas image. 

**Code**

{% highlight js %}

<img src="../images/chart/export.png" onclick="onExport()" title="Export Chart" style="float: right" />
<div id="container"></div>
<canvas id="canvas2" style="display:none"></canvas>

**[JS]**

$("#chartcontainer").ejChart(
               {   
           });
        });
function onExport() {
            var canvas = document.getElementById('canvas2');
            svg = $("#container").html();
            canvg(canvas, svg);
            var image = canvas.toDataURL("image/png")
                              .replace("image/png","image/octet-stream");
            var downloadLink = document.createElement("a");
            downloadLink.href = image;
            downloadLink.download = "Chart.png";
            document.body.appendChild(downloadLink);
            downloadLink.click();
            document.body.removeChild(downloadLink);
            $('#canvas2').hide();
        }



{% endhighlight %}



