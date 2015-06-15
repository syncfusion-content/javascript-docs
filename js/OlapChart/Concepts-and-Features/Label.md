---
layout: post
title: Label
description: label
platform: js
control: OLAP Chart
documentation: ug
---

### Label

**Label** represents the text on the axis data points in the Chart. Each axis data point are represented by separate label text information in order to provide precise information about each points. **Label** text is displayed in a customizable format.

**Label font and color customization** 

Font style and color of the label text is customized with the help of **font** and **color** properties within its respective axis.

{% highlight js %}

[JS]
$("#OlapChart1").ejOlapChart({
        url: "../wcf/OlapChartService.svc",
        primaryXAxis: { font: { fontFamily: "Algerian", fontWeight: "lighter", fontStyle: "Italic", size: "14px", color: "red" } },
        primaryYAxis: {font: { fontFamily: "Algerian", fontWeight: "lighter", fontStyle: "Italic", size: "14px", color: "red" },
        },
 });


{% endhighlight %}

{% include image.html url="/js/OlapChart/Concepts-and-Features/Label_images/Label_img1.png" Caption="Label Text Customization "%}

<br/>

**Rotating Axis Labels**

You can rotate the labels to desired angle. The axis labels are rendered in the degree specified in the **label rotation** property.

{% highlight js %}

[JS]
$("#OlapChart1").ejOlapChart({ url: "../wcf/OlapChartService.svc", 
primaryXAxis: { labelRotation: 45 }
});


{% endhighlight %}


{% include image.html url="/js/OlapChart/Concepts-and-Features/Label_images/Label_img2.png" Caption="Label Rotation"%}

