---
layout: post
title: Responsive-Layout
description: responsive layout
platform: js
control: OlapClient
documentation: ug
---

# Responsive Layout

**Responsive layout** is aimed at crafting sites to provide an optimal viewing experience - easy reading. It also provides navigation with a minimum of resizing, panning, and scrolling across a wide range of devices from tablet to desktop. To get responsive layout for **OlapClient,** enable **IsResponsive** API to true. By using this feature, you can achieve an effective view of the **OlapClient** control in all devices including desktops, tablets, mobiles, etc.

{% highlight js %}

$(function() {
    $("#OlapClient1").ejOlapClient({
        url: "../wcf/OlapClientService.svc",
        isResponsive: true,
        chartLoad: "setChartProperties"
    });
});

function setChartProperties(args) {
    this.model.load = "loadTheme";
};

{% endhighlight %}

{% include image.html url="/js/OlapClient/Responsive-Layout_images/Responsive-Layout_img2.png" Caption="Normal View"%}

{% include image.html url="/js/OlapClient/Responsive-Layout_images/Responsive-Layout_img3.png" Caption="Responsive View"%}



