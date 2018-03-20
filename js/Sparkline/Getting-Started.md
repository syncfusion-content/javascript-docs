---
layout: post
title: Getting Started for Essential JavaScript Sparkline
description: How to create a sparkline.
platform: js
control: Sparkline
documentation: ug
api: /api/js/ejsparkline
---

# Getting Started

This section explains you the steps required to populate the Sparkline with data. This section covers only the minimal features that you need to know to get started with the Sparkline.

## Adding script reference

Create an **HTML** page and add the scripts references in the order mentioned in the following code example.

{% highlight html %}

<!DOCTYPE html>
<html>
<head>
<!--  jquery script  -->
<script src="http://cdn.syncfusion.com/js/assets/external/jquery-2.1.4.min.js"></script>
<!-- Essential JS UI widget -->
<script src="http://cdn.syncfusion.com/14.2.0.26/js/web/ej.web.all.min.js"></script>
</head>
<body>
</body>
</html>

{% endhighlight %}

In the above code, ej.web.all.min.js script reference has been added for demonstration purpose. It is not recommended to use this for deployment purpose, as its file size is larger since it contains all the widgets. Instead, you can use ['CSG'](http://csg.syncfusion.com/) utility to generate a custom script file with the required widgets for deployment purpose.

## Initialize Sparkline

Add a **div** container to render the Sparkline.

{% highlight html %}

<!DOCTYPE html>
<html>
<body>
    <div id="sparklineContainer"></div>
</body>
</html>

{% endhighlight %}

Initialize the Sparkline by using the ejSparkline method. The Sparkline is rendered to the container with default size. You can also customize the Sparkline dimension by setting the width and height.

{% highlight html %}

<!DOCTYPE html>
<html>
<body>
<div id="sparklineContainer"></div>
    <script type="text/javascript" language="javascript ">

        $(function () {
            $("#sparklineContainer").ejSparkline();
        });
    </script>
</body>
</html>

{% endhighlight %}

Now, the Sparkline is rendered with some auto-generated random values and with default Line type. 

![](/js/Sparkline/Getting-Started_images/Getting-Started_img1.png)