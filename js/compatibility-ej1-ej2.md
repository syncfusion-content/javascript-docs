---
layout: post
title: Compatibility with Syncfusion Essential JS1 and JS2 widgets
description: Learn how to show Compatibility with Syncfusion Essential JS1 and JS2 widgets with Javascript platform.
platform: js
control: Introduction
documentation: ug
---

# Compatibility with Essential JS 2 Components

The Essential JS 1 components can be compatible with the Essential JS 2 components in the same web page. For this we need to follow the below steps,


## Script Compatibility

We should maintain the script reference order (refer Essential JS 1 before Essential JS 2) for this, and we should extend the Essential JS 1 namespace with Essential JS 2.
Please find the below code for script references.

{% highlight html %}

<!-- Essential JS 1 script -->
<script src="http://cdn.syncfusion.com/16.1.0.24/js/web/ej.web.all.min.js"></script>
<!-- Essential JS 2 script -->
<script src="http://cdn.syncfusion.com/ej2/dist/ej2.min.js" type="text/javascript"></script>
<script>
    //Extend ej namespace with Syncfusion
      $.extend(ej, Syncfusion)
</script>

{% endhighlight %}


## Theme Compatibility

We have provided compatibility css files for all the Essential JS 1 web components in all the themes, since we have used same classes for Essential JS 1 and Essential JS 2 components. So, the both classes were overrides with each other. We have provided this support for all the themes which are available in Essential JS 1. 

You can find the compatibility theme files which are ends with the name compatibility in the below mentioned location.

widgets.core - **(installed location)** \Syncfusion\Essential Studio\{RELEASE_VERSION}\ JavaScript\assets\css\web\ej.widgets.core.compatibility.min.css
theme - **(installed location)**\Syncfusion\Essential Studio\{RELEASE_VERSION}\ JavaScript\assets\css\web\default-theme\ej.theme.compatibility.min.css

N>We have illustrated flat azure theme in this document. However, all the themes in Essential JS 1 have compatibility support.


## Compatibility Themes

1.	Bootstrap
2.	Azure and its variants (Flat, Dark, Gradient)
3.	Saffron and its variants
4.	Lime and its variants
5.	High Contrast 01
6.	High Contrast 02
7.	Material
8.	Office 365

You can get the compatibility css in the following way.

*	You can get the compatibility theme files from the below build installed location.

**(installed location) **\Syncfusion\Essential Studio\ {RELEASE_VERSION} \ JavaScript\assets\css\web


## Creating Sample Application for Essential JS 1 Component


### Create Essential JS 1 Button

You can refer the [`Getting Started`](https://help.syncfusion.com/js/button/getting-started#create-button-widget) to create the button component. Now you can modify the sample’s css references as below to refer the compatibility themes.

Please refer the below code snippet.

{% highlight html %}

<!-- Style sheet for default theme (flat Azure) -->
<link href="http://cdn.syncfusion.com/16.1.0.24/js/web/flat-azure/ej.web.all.compatibility.min.css" rel="stylesheet" />

{% endhighlight %}


### Add Essential JS 2 Button

You can refer the [`Getting Started`](http://npmci.syncfusion.com/production/documentation/getting-started/JavaScript-ES5.html?lang=es5) for button creation and made the Essential JS 2 related changes in the same html file.

Please find the below html code.

{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">

<head>
    <title>Essential JS 2 - Essential JS 1</title>
    <!-- Essential JS 1 default theme -->
    <link href=" http://cdn.syncfusion.com/16.1.0.24/js/web/flat-azure/ej.web.all.compatibility.min.css " rel="stylesheet" type="text/css" />
    <!-- Essential JS 2 material theme -->
    <link href="https://cdn.syncfusion.com/ej2/styles/compatibility/material.css" rel="stylesheet" type="text/css" />
    <!-- Essential JS 1 scripts -->
    <script src="https://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js" type="text/javascript"></script>
    <script src="https://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js" type="text/javascript"></script>
    <script src=" https://cdn.syncfusion.com/16.1.0.24/js/web/ej.web.all.min.js" type="text/javascript"></script>
    <!-- Essential JS 2 script -->
    <script src=" https://cdn.syncfusion.com/ej2/dist/ej2.min.js" type="text/javascript"></script>
</head>

<body>
    <div style="margin: 50px;">
        <!-- Add HTML Button element for Essential JS 2 -->
        <button id="btn2">Essential JS 2</button>
    </div>
	<div style="margin: 50px;">
        <!-- Add HTML Button element for Essential JS 1 -->
        <button id="btn1">Essential JS 1</button>
    </div>
</body>

</html>

{% endhighlight %}

Please find the below Javascript code.

{% highlight html %}

<script>
   // Extend ej namespace with Syncfusion
   $.extend(ej, Syncfusion);
   // Initialize Essential JS 1 JavaScript Button component
   $("#btn1").ejButton();
   // Initialize Essential JS 2 JavaScript Button component
   var button = new ej.buttons.Button({});
   button.appendTo('#btn2');
</script>

{% endhighlight %}


### Run the Sample

Now run the html page which contains Essential JS 1 Button and Essential JS 2 Button and the output look like below,

![Compatibility](compatibility_images/compatibility.png)