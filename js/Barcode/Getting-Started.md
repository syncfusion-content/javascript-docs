---
layout: post
title: Getting-Started
description: getting started
platform: js
control: Barcode
documentation: ug
---

# Getting Started

This section explains you briefly on how to create a **Barcode** in your application with **JavaScript**.

**Control** **Structure**

{% include image.html url="/js/Barcode/Getting-Started_images/Getting-Started_img1.png" Caption="Figure 1: Control structure"%}

## Create your first Barcode in JavaScript

You can easily configure the **Barcode** to any **DOM** element such as div or span. It takes text and symbol as input and renders the encoded text as **Barcode**.

**Add Barcode to JavaScript application**

* Create an **HTML** file using the following code example for **ejBarcode** creation.

{% highlight html %}

<!DOCTYPE html>
<html>
<head>
<title>Getting Started Essential JS</title>
<!-- Style sheet for default theme (flat azure)-->
<link href ="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.widgets.all.min.css" rel ="stylesheet" />
<!--scripts-->
<script src ="http://code.jquery.com/jquery-1.10.1.min.js"></script>
<script src ="http://cdn.syncfusion.com/13.1.0.21/js/ej.widgets.all.min.js"></script>
</head>
<body>
//add barcode element here
</body>
</html>


{% endhighlight %}





* Add element for **Barcode** rendering.



{% highlight html %}

<div id="barcode"></div>


{% endhighlight %}



* Initialize **ejBarcode** in script.

{% highlight js %}

$(function (){
// document ready
// simple control creation
$("#barcode").ejBarcode({ text:"http://www.syncfusion.com", symbologyType: "qrbarcode"});
});


{% endhighlight %}



