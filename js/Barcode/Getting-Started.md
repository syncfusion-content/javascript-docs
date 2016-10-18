---
layout: post
title: Getting Started with Syncfusion Essential JS Barcode widget
description: How to create one dimensional, two dimensional barcode and customizing the appearance of it. 
platform: js
control: Barcode
documentation: ug
---

# Getting Started

This section explains you briefly on how to create one dimensional and two dimensional barcodes and customizing its appearance in your JavaScript application.

You can easily configure the barcode to any DOM element such as `div` or `span`. It takes [`text`](/api/js/ejbarcode#textspan-classtype-signature-type-stringstringspan) and [`symbologyType`](/api/js/ejbarcode#symbologytypespan-classtype-signature-type-enumenumspan) as input and renders the encoded text as barcode.

## Adding a QR Code

Create an HTML file using the following code example for `ejBarcode` creation.

{% highlight html %}

<!DOCTYPE html>
<html>
   <head>
      <title>Getting Started Essential JS</title>
      <!-- Style sheet for default theme (flat azure)-->
      <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.widgets.all.min.css" rel="stylesheet" />
      <!--scripts-->
      <script src="http://code.jquery.com/jquery-1.10.1.min.js"></script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/ej.widgets.all.min.js"></script>
      <!--Add custom scripts here -->
   </head>
   <body>
      <!-- Add Barcode element here. -->
   </body>
</html>
{% endhighlight %}

Add `div` container for barcode rendering.

{% highlight html %}
<div id="barcode"></div>
{% endhighlight %}

Set the `symbologyType` and provide input URL to the `text` property to render the QR Code.

{% highlight javascript %}
<script type="text/javascript">
   $(function() {
      // document ready
      // simple control creation
      $("#barcode").ejBarcode({
         text: "http://www.syncfusion.com",
         symbologyType: "qrbarcode"
      });
   });
</script>
{% endhighlight %}

![](/js/Barcode/Getting-Started_images/Getting-Started_img2.png)

## Adding a Code39 Barcode

Create an HTML file using the following code example for creating a Code39 barcode.

{% highlight html %}

<!DOCTYPE html>
<html>
   <head>
      <title>Getting Started Essential JS</title>
      <!-- Style sheet for default theme (flat azure)-->
      <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.widgets.all.min.css" rel="stylesheet" />
      <!--scripts-->
      <script src="http://code.jquery.com/jquery-1.10.1.min.js"></script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/ej.widgets.all.min.js"></script>
      <!--Add custom scripts here -->
   </head>
   <body>
      <!-- Add Barcode element here. -->
   </body>
</html>
{% endhighlight %}

Add `div` container for barcode rendering.

{% highlight html %}
<div id="barcode"></div>
{% endhighlight %}

Set the `symbologyType` and provide input to the `text` property to render the Code39 barcode.

{% highlight javascript %}
$("#barcode").ejBarcode({
   text: "SYNCFUSION",
   symbologyType: "code39"
});
{% endhighlight %}


![](/js/Barcode/Getting-Started_images/Getting-Started_img3.png)

## Customizing the Barcode appearance
The height of the barcode can be changed using the [barHeight](/api/js/ejBarcode#barheightspan-classtype-signature-type-numbernumberspan) property. The equivalent property to change the block size for two dimensional barcode is [xDimension](/api/js/ejBarcode#xdimensionspan-classtype-signature-type-numbernumberspan). You can also customize the barcode color by changing the [darkBarColor](/api/js/ejBarcode#darkbarcolorspan-classtype-signature-type-objectobjectspan) and [lightBarColor](/api/js/ejbarcode#lightbarcolorspan-classtype-signature-type-objectobjectspan) properties.

N>    This color customization is possible only for one dimensional barcodes and it is not supported for two dimensional barcodes.