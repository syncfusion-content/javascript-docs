---
layout: post
title: Getting Started with Syncfusion Essential JS Barcode widget
description: How to create one dimensional, two dimensional barcode and customizing the appearance of it. 
platform: js
control: Barcode
documentation: ug
---

# Getting Started

This section explains you briefly on how to create a barcode in your application with JavaScript.

You can easily configure the barcode to any DOM element such as `div` or `span`. It takes `text` and `symbol` as input and renders the encoded text as barcode.

## Adding a QR Code to JavaScript application

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

{% highlight js %}
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

{% include image.html url="/js/Barcode/Getting-Started_images/Getting-Started_img2.png" Caption=""%}

## Adding a Code39 Barcode to JavaScript application

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

{% highlight js %}
$("#barcode").ejBarcode({
   text: "SYNCFUSION",
   symbologyType: "code39"
});
{% endhighlight %}


{% include image.html url="/js/Barcode/Getting-Started_images/Getting-Started_img3.png" Caption=""%}

## Customizing the Barcode appearance
The height of the barcode can be changed using the [barHeight](/js/api/ejBarcode#barheightspan-classtype-signature-type-numbernumberspan) property. The equivalent property to change the block size for two dimensional barcode is [xDimension](/js/api/ejBarcode#xdimensionspan-classtype-signature-type-numbernumberspan). You can also customize the barcode color by changing the [darkBarColor](/js/api/ejBarcode#darkbarcolorspan-classtype-signature-type-objectobjectspan) and [lightBarColor](http://helpjs.syncfusion.com/js/api/ejbarcode#lightbarcolorspan-classtype-signature-type-objectobjectspan) properties.

>   **Note:** This color customization is possible only for one dimensional barcodes and it is not supported for two dimensional barcodes.


