---
layout: post
title: Two-Dimensional-Barcodes
description: two dimensional barcodes
platform: js
control: Barcode
documentation: ug
api: /api/js/ejbarcode
---

# Two Dimensional Barcodes

## QR Code

A **QR Code** is a two-dimensional barcode that consists of a grid of dark and light dots or blocks that form a square. The data encoded in the barcode can be numeric, alphanumeric, or Shift Japanese Industrial Standards (JIS8) characters. The QR Code uses version from 1 to 40. Version 1 measures 21 modules x 21 modules, Version 2 measures 25 modules x 25 modules, and so on. The number of modules increases in steps of 4 modules per side up to Version 40 that measures 177 modules x 177 modules. Each version has its own capacity. By default, the barcode control automatically set the version according to the length of the input text. The QR Barcodes are designed for industrial uses and also commonly used in consumer advertising.

Here is the code snippet to create a QR Code:

{% highlight javascript %}
$("#barcode").ej.Barcode({
   text: "B5330E8278BC4C797C49DD3ED5AD9715",
   symbologyType: "qrbarcode",
   xDimension: 8
});
{% endhighlight %}

## DataMatrix

**DataMatrix Barcode** is a two dimensional barcode that consists of a grid of dark and light dots or blocks forming square or rectangular symbol. The data encoded in the barcode can either be numbers or alphanumeric. They are widely used in printed media such as labels and letters. You can read it easily with the help of a barcode reader and mobile phones.