---
layout: post
title:  getting started
description:  getting started
platform: js
control: Signature
documentation: ug
api: /api/js/ejsignature
---

# Getting Started

The Essential JavaScript Signature simplifies creation of a signature capture in a browser, allowing a user to draw a signature using mouse or touch.

This section explains briefly about how to create a **Signature** control in your application with JavaScript by the following step-by-step instructions. The following screenshot demonstrates the functionality of Signature widget.

![](Getting_Started_images\gettingstarted_img1.png)

## Create Signature Control

Create an HTML file and add the following template in the HTML file.

{% highlight html %}

<!doctype html>

<html>
<head>
    <title>Essential Studio for JavaScript : Signature Default Functionalities</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
    <link href="http://cdn.syncfusion.com/**{{**site.releaseversion**}}**/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-3.1.1.min.js"></script>
    <script src="http://cdn.syncfusion.com/**{{**site.releaseversion**}}**/js/web/ej.web.all.min.js"></script>
    <!--Add custom scripts here -->
</head>
<body>

</body>
</html>

{% endhighlight %}

Add div element to create Signature.

{% highlight html %}

<div class="content-container-fluid">
    <div class="row">
        <div class="cols-sample-area">
            <! ----------------signature Control---------------->
            <div id="signature">
            </div>
        </div>
    </div>
</div>

{% endhighlight %}

Add the following script to create the signature.

{% highlight js %}

<script type="text/javascript">
        $(function () {
            $("signature").ejSignature({});
        });

    </script>

{% endhighlight %}

The following screenshot is the output for the above code.

![](Getting_Started_images\createsignaturecontrol_img1.png)

## Adjusting Signature Size

You can customize the width and height of the Signature by [width](https://help.syncfusion.com/api/js/ejsignature#members:width) and [height](https://help.syncfusion.com/api/js/ejsignature#members:height) properties. These properties completely depend on signature canvas. The width and height are adjusted within the signature canvas.

The following code example is used to render the Signature control with customized width and height.

Add the following HTML to render signature with customized width and height.

{% highlight html %}

<div>
    <div id="signature" class="signature" />
</div>

{% endhighlight %}

Add the following script to render signature with customized width and height.

{% highlight js %}

  <script type="text/javascript">
        $(function () {
            $("signature").ejSignature({ width: "200px", height: "300px" });
        });
    </script>


{% endhighlight %}


The following screenshot illustrates signature with customized width and height.


![](Getting_Started_images\adjustingsignaturesize_img1.png)







