---
layout: post
title: Customizing-the-appearance
description: customizing the appearance
platform: js
control: Barcode
documentation: ug
api: /api/js/ejbarcode
---

# Customizing the appearance

##Customizing the Barcode color

A page or printed media with barcode often appears colorful in the background and surrounding region with other contents. In such cases the barcode can also be customized to suit the needs. You can achieve this by changing the [darkBarColor](/api/js/ejBarcode#darkbarcolorspan-classtype-signature-type-objectobjectspan) property.

N>    This color customization is possible only for one dimensional barcodes and it is not supported for two dimensional barcodes.

{% highlight javascript %}
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

![](/js/Barcode/Customizing-the-appearance_images/Customizing-the-appearance_img2.png)

##Customizing the Barcode height
The height of the barcode can be changed using the [barHeight](/api/js/ejBarcode#barheightspan-classtype-signature-type-numbernumberspan) property. The equivalent property to change the block size for two dimensional barcode is [xDimension](/api/js/ejBarcode#xdimensionspan-classtype-signature-type-numbernumberspan).

{% highlight javascript %}
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

![](/js/Barcode/Customizing-the-appearance_images/Customizing-the-appearance_img3.png)