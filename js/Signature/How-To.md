---
layout: post
title:  how to
description:  how to
platform: js
control: Signature
documentation: ug
---

##  How To

### Save signature image with user defined format

By default, the downloaded image from the signature canvas will be in **png** format. We can define our own format to download the image with **saveImageFormat** property. And we can also save the image along with the background by using the **saveWithBackground** property.

The following code example is used to download drawn image on the Signature control.

{% highlight html %}

<div id="signature"></div>

<input id="save" type="button" value="save" />

{% endhighlight %}

Add the following script to define the download format for the canvas

{% highlight js %}

<script type="text/javascript">
        $(function () {
            $("signature").ejSignature({
                height: "500px",
                saveWithBackground: true,
                strokeWidth: 3,
                saveImageFormat :"jpg",
                backgroundImage: "../content/images/progressbar/water.png",

            });
            $("#signsave").ejButton({
                size: "normal", width: "70px",
                showRoundedCorner: true,
                click: onsave
            });  
        });

      function onsave(args) {
            var sig = $("#signature").ejSignature("instance");
            sig.save("MySignature");
        }

    </script>

{% endhighlight %}

The following screenshot illustrates the Signature with saving (downloading) the drawn image.

![](How_To_images\savesignatureimagewithuserdefinedformat_img1.png)


###  Make signature as responsive

When the signature control is resized or even the window is resized the strokes drawn in the signature will be disappeared. To make the strokes visible even after resizing the window, we must set the **i****sResponsive**property as true.

The following code example is used to render the Signature control with responsive support.

{% highlight js %}

   <script type="text/javascript">
        $("signature").ejSignature({
            isResponsive: true
        });
    </script>   

{% endhighlight %}

The following screenshot illustrates the Signature with responsiveness.

Before Responsiveness:

![](How_To_images\makesignatureasresponsive_img1.png)


After giving the Responsiveness:

![](How_To_images\makesignatureasresponsive_img2.png)




