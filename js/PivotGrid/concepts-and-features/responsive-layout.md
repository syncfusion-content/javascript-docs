---
layout: post
title: responsive-layout
description: responsive layout
platform: js
control: PivotGrid
documentation: ug
---

# Responsive Layout

Responsive layout is aimed at crafting sites to provide an optimal viewing experience - easy reading. It also provides navigation with a minimum of resizing, panning, and scrolling across a wide range of devices from tablet to desktop. To get responsive layout for PivotGrid, enable IsResponsive API to true. By using this feature, you can achieve an effective view of the PivotGrid control in all devices including desktops, tablets, mobiles, etc. 

{% highlight js %}

**[JS]**
<script type="text/javascript">
$(function () {
       $("#PivotGrid1").ejPivotGrid({
             url: "../wcf/OLAPService.svc", **isResponsive: true**
       });
});
</script>


{% endhighlight %}



{% include image.html url="\js\PivotGrid\concepts-and-features\responsive-layout_images\responsive-layout_img1.png" Caption="Normal View"%}

{% include image.html url="\js\PivotGrid\concepts-and-features\responsive-layout_images\responsive-layout_img2.png" Caption="Responsive View"%}

