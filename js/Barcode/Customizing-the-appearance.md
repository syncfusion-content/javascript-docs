---
layout: post
title: Customizing-the-appearance
description: customizing the appearance
platform: js
control: Barcode
documentation: ug
---

# Customizing the appearance

A page or printed media with **Barcode** often appears colorful in the background and surrounding region with other contents. In such cases the **Barcode** can also be customized to suit the needs. You can achieve this by changing the **darkBarColor** property.

>   **Note:** This color customization is possible only for one dimensional barcodes and it is not supported for two dimensional barcodes.

{% highlight js %}
$("#barcode").ejBarcode({
   text: "B5330E8278BC4C797C49DD3ED5AD9715",
   symbologyType: "code39",
   displayText: true,
   darkBarColor: "blue",
   quietZone: {
      all: 30
   }
});
{% endhighlight %}

Execute the above code to render the following output.

{% include image.html url="/js/Barcode/Customizing-the-appearance_images/Customizing-the-appearance_img2.png" Caption="Customized Barcode"%}

The height of the barcode can be changed using the **BarHeight** property. The equivalent property to change the block size for two dimensional barcode is **XDimension**.

{% highlight js %}
$("#barcode").ejBarcode({
   text: "B5330E8278BC4C797C49DD3ED5AD9715",
   symbologyType: "code39",
   displayText: true,
   darkBarColor: "#990099",
   barHeight: 45,
   quietZone: {
      all: 30
   }
});
{% endhighlight %}

Execute the above code to render the following output.

{% include image.html url="/js/Barcode/Customizing-the-appearance_images/Customizing-the-appearance_img3.png" Caption="Barcode with customized height"%}