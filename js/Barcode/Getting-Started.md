---
layout: post
title: Getting-Started
description: getting started
platform: js
control: Barcode
documentation: ug
---

# Getting Started

This section explains you briefly on how to create a barcode in your application with JavaScript.

## Create your first Barcode in JavaScript

You can easily configure the barcode to any DOM element such as div or span. It takes text and symbol as input and renders the encoded text as barcode.

###Add a QR Code to JavaScript application

Create an HTML file using the following code example for `ejBarcode` creation.

{% highlight html %}

<!DOCTYPE html>
<html>
   <head>
      <title>Getting Started Essential JS</title>
      <!-- Style sheet for default theme (flat azure)-->
      <link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.widgets.all.min.css" rel="stylesheet" />
      <!--scripts-->
      <script src="http://code.jquery.com/jquery-1.10.1.min.js"></script>
      <script src="http://cdn.syncfusion.com/13.1.0.21/js/ej.widgets.all.min.js"></script>
      <!--Add custom scripts here -->
   </head>
   <body>
      <!-- Add Barcode element here. -->
   </body>
</html>
{% endhighlight %}

Add element for barcode rendering.

{% highlight html %}
<div id="barcode"></div>
{% endhighlight %}

Add the following script in the HTML file to initialize `ejBarcode` and to render the QR Code.

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

The above code gives the output displayed in following screenshot.
{% include image.html url="/js/Barcode/Getting-Started_images/Getting-Started_img2.png" Caption=""%}

###Add a Code39 Barcode to JavaScript application

Create an HTML file using the following code example for creating a Code39 barcode.

{% highlight html %}

<!DOCTYPE html>
<html>
   <head>
      <title>Getting Started Essential JS</title>
      <!-- Style sheet for default theme (flat azure)-->
      <link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.widgets.all.min.css" rel="stylesheet" />
      <!--scripts-->
      <script src="http://code.jquery.com/jquery-1.10.1.min.js"></script>
      <script src="http://cdn.syncfusion.com/13.1.0.21/js/ej.widgets.all.min.js"></script>
      <!--Add custom scripts here -->
   </head>
   <body>
      <!-- Add Barcode element here. -->
   </body>
</html>
{% endhighlight %}

Add element for barcode rendering.

{% highlight html %}
<div id="barcode"></div>
{% endhighlight %}

Add the following script in the HTML file to initialize `ejBarcode` and to render the Code39 barcode.

{% highlight js %}
$("#barcode").ejBarcode({
   text: "SYNCFUSION",
   symbologyType: "code39",
   displayText: true,
   quietZone: {
      all: 30
   }
});
{% endhighlight %}

The above code gives the output displayed in following screenshot.
{% include image.html url="/js/Barcode/Getting-Started_images/Getting-Started_img3.png" Caption=""%}

###Customizing the Barcode appearance

##Customizing the Barcode color

A page or printed media with barcode often appears colorful in the background and surrounding region with other contents. In such cases the barcode can also be customized to suit the needs. You can achieve this by changing the [darkBarColor](/js/api/ejBarcode#darkbarcolorspan-classtype-signature-type-objectobjectspan) property.

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

{% include image.html url="/js/Barcode/Customizing-the-appearance_images/Customizing-the-appearance_img2.png" Caption=""%}

##Customizing the Barcode height
The height of the barcode can be changed using the [barHeight](/js/api/ejBarcode#barheightspan-classtype-signature-type-numbernumberspan) property. The equivalent property to change the block size for two dimensional barcode is [xDimension](/js/api/ejBarcode#xdimensionspan-classtype-signature-type-numbernumberspan).

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

{% include image.html url="/js/Barcode/Customizing-the-appearance_images/Customizing-the-appearance_img3.png" Caption=""%}