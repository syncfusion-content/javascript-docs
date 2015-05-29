---
layout: post
title: responsive-layout
description: responsive layout
platform: js
control: OLAP Client
documentation: ug
---

# Responsive Layout

**Responsive layout** is aimed at crafting sites to provide an optimal viewing experience - easy reading. It also provides navigation with a minimum of resizing, panning, and scrolling across a wide range of devices from tablet to desktop. To get responsive layout for **OLAP Client,** enable **IsResponsive** API to true. By using this feature, you can achieve an effective view of the **OLAP Client** control in all devices including desktops, tablets, mobiles, etc. 

{% highlight js %}

**[JS]**
<script type="text/javascript">
$(function () {
       $("#OlapClient1").ejOlapClient({ url: "../wcf/OlapClientService.svc", **isResponsive: true,** chartLoad: "setChartProperties" });
});
function setChartProperties(args) {
       this.model.load = "loadTheme";
};
</script>


{% endhighlight %}

![](responsive-layout_images\responsive-layout_img1.png)

{% include image.html url="\js\OlapClient\concepts-and-features\responsive-layout_images\responsive-layout_img2.png" Caption="Figure: Normal View"%}

{% include image.html url="\js\OlapClient\concepts-and-features\responsive-layout_images\responsive-layout_img3.png" Caption="Figure: Responsive View"%}



{% include image.html url="\js\OlapClient\concepts-and-features\responsive-layout_images\responsive-layout_img4.png" Caption="Figure: Responsive View"%}



