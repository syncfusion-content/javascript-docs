---
layout: post
title: Getting-Started
description: getting started 
platform: js
control: Split Button
documentation: ug
---

# Getting Started 

This section explains briefly about how to create a **Split Button** in your application with **JavaScript**.

## Create your first Split Button in JavaScript

The **HTML** button element and the **&lt;UL&gt;, &lt;LI&gt;** are easily configured as **Essential JavaScript Split Button** control.  The basic rendering of **Essential JavaScript Split****Button** is achieved by using default functionality. Initially the **targetID** is a mandatory one, without this field it does not act as normal button on two sides.

**Control structure**

{% include image.html url="/js/SplitButton/Getting-Started_images/Getting-Started_img1.png" Caption="Essential JavaScript Split Button"%}

**Split Button Creation**

1. Create an **HTML** file and add the following template to **HTML** file for **Split Button** creation.

{% highlight html %}


<!doctype html>
<html>
<head>
<title>Getting Started Essential JS</title> 
      <!-- Style sheet for default theme (flat azure) -->
<linkhref="[http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css](http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css)"rel="stylesheet"/>

    <!--Scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>

<scriptsrc="[http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js](http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js)"></script>
    <!--Add custom scripts here -->
</head>
<body><!--add button element here--></body>
</html>


{% endhighlight %}



2. Adding button element and **&lt;UL&gt;, &lt;LI&gt;** element for **Split****Button** rendering.

{% highlight html %}

<button id="sbutton">Save</button>
<ul id="target">
    <li><a href="#">Open..</a></li>
    <li><a href="#">Save</a></li>
    <li><a href="#">Delete</a></li>
</ul>


{% endhighlight %}



3. Initialization of **ejSplitButton** in script

{% highlight js %}

<script>
        $(function () {
            // simple control creation
            $("#sbutton").ejSplitButton({
                width: "120px",
                height: "50px",
                showRoundedCorner: true,
                targetID: "target"
            });
        });
    </script>


{% endhighlight %}



4. Output of above steps

{% include image.html url="/js/SplitButton/Getting-Started_images/Getting-Started_img2.png" Caption="Split Button"%}

