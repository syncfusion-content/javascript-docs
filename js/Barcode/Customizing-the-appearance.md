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

## Customizing the Barcode color

A page or printed media with barcode often appears colorful in the background and surrounding region with other contents. In such cases the barcode can also be customized to suit the needs. You can achieve this by changing the [darkBarColor](/api/js/ejbarcode#members:darkbarcolor), [lightBarColor](/api/js/ejbarcode#members:lightbarcolor) and [textColor](/api/js/ejbarcode#members:textcolor) properties.

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

## Customizing the Barcode dimension
The height of the barcode can be changed using the [barHeight](/api/js/ejbarcode#members:barheight) property. The equivalent property to change the block size for two dimensional barcode is [xDimension](/api/js/ejbarcode#members:xdimension).

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

Advance size customization of the particular elements in the barcode can be done using [barcodeToTextGapHeight](/api/js/ejbarcode#members:barcodetotextgapheight), [narrowBarWidth](/api/js/ejbarcode#members:narrowbarwidth), [quietZone](/api/js/ejbarcode#members:quietzone), [quietZone-all](/api/js/ejbarcode#members:quietzone-all), [quietZone-bottom](/api/js/ejbarcode#members:quietzone-bottom), [quietZone-left](/api/js/ejbarcode#members:quietzone-left), [quietZone-right](/api/js/ejbarcode#members:quietzone-right), [quietZone-top](/api/js/ejbarcode#members:quietzone-top) and [wideBarWidth](/api/js/ejbarcode#members:widebarwidth) properties.

{% highlight javascript %}
$("#barcode").ejBarcode({
   text: "B5330E8278BC4C797C49DD3ED5AD9715",
   symbologyType: "code39",
   barcodeToTextGapHeight: 50,
   narrowBarWidth: 5,
   darkBarColor: "#990099",
   barHeight: 45,
   wideBarWidth: 5,
   quietZone: {
      all: 30
   }
});
{% endhighlight %}

## Customizing the text
In one dimensional barcodes, an additional character is added as start and stop delimiters using [encodeStartStopSymbol](/api/js/ejbarcode#members:encodestartstopsymbol). These symbols are optional and the unique of the symbol allows the reader to determine the direction of the barcode being scanned.

{% highlight javascript %} 
 $("#barcode").ejBarcode({
    text: "SYNCFUSION",
    symbologyType: "code39",
    encodeStartStopSymbol: false
 });
{% endhighlight %}

To hide the text in the barcode use the property [displayText](/api/js/ejbarcode#members:displaytext).

{% highlight javascript %}
 $("#barcode").ejBarcode({
     text: "SYNCFUSION",
     symbologyType: "code39",
     displayText: false
 });
{% endhighlight %}

## Visibility of barcode
To check if the barcode control is enabled use the property [enabled](/api/js/ejbarcode#members:enabled) and the event [load](/api/js/ejbarcode#events:load) will be triggered once the barcode is loaded.

To disable the barcode use the method [disable()](/api/js/ejbarcode#methods:disable).
{% highlight javascript %}
// disable the barcode
$("#barcode").ejBarcode("disable");
{% endhighlight %}

To enable the barcode use the method [enable()](/api/js/ejbarcode#methods:enable).
{% highlight javascript %}
// enable the barcode
$("#barcode").ejBarcode("enable");
{% endhighlight %}

