---
layout: post
title:  how to | Signature | Syncfusion
description: This section provides details about all events and their arguments in Syncfusion JavaScript Signature control. 
platform: js
control: Signature
documentation: ug
api: /api/js/ejsignature
---

# Events in JavaScript Signature

## Save signature image with user defined format

By default, the downloaded image from the signature canvas will be in **png** format. We can define our own format to download the image with [saveImageFormat](https://help.syncfusion.com/api/js/ejsignature#members:saveimageformat) property. And we can also save the image along with the background by using the [saveWithBackground](https://help.syncfusion.com/api/js/ejsignature#members:savewithbackground) property.

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
            $("#signSave").ejButton({
                size: "normal", width: "70px",
                showRoundedCorner: true,
                click: onSave
            });  
        });

      function onSave(args) {
            var signature = $("#signature").ejSignature("instance");
            signature.save("MySignature");
        }

    </script>

{% endhighlight %}

The following screenshot illustrates the Signature with saving (downloading) the drawn image.

![save](How_To_images\savesignatureimagewithuserdefinedformat_img1.png)

## To clear the Signature

To clear the signature, you can simply use the [clear()](https://help.syncfusion.com/api/js/ejsignature#methods:clear) method. This method will clear all the drawn strokes in the signature canvas and leaves it empty.

{% highlight js %}

<script type="text/javascript">
        $(function () {
            $("signature").ejSignature({
                height: "500px",
                strokeWidth: 3

            });
            $("#signatureClear").ejButton({
                size: "normal", width: "70px",
                showRoundedCorner: true,
                click: "onClear"
            });  
        });

      function onClear(args) {
            var signature = $("#signature").ejSignature("instance");
            signature.clear();
        }

    </script>
    
{% endhighlight %}

## Make signature as responsive

When the signature control is resized or even the window is resized the strokes drawn in the signature will be disappeared. To make the strokes visible even after resizing the window, we must set the [isResponsive](https://help.syncfusion.com/api/js/ejsignature#members:isresponsive) property as true.

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

![responsive](How_To_images\makesignatureasresponsive_img1.png)


After giving the Responsiveness:

![responsive](How_To_images\makesignatureasresponsive_img2.png)


## To check whether any input to the signature control since render

We can detect whether not there has been any input to the signature control since render. To detect we can use the storeSnap public variable, which is an array that stores all the canvas inputs. At initial rendering this array is empty and we can use this variable to check for the drawn strokes.


{% highlight js %}

   <script type="text/javascript">
      var signature = $("#signature").ejSignature("instance");

            if (ej.isNullOrUndefined(signature.storeSnap)) {
               
                //Something

            }
    </script>   

{% endhighlight %}

## Pre-load signature image

To pre-load signature image , use canvas to get the clear pixel of image and display this through Signature instance. 
  
Refer to the following code

{% highlight js %}

     <script>
        $(function () {
            // declaration
            $("#signature").ejSignature({ height: "400px", isResponsive: true, strokeWidth: 3, width: "300px" });
            var obj = $("#signature").ejSignature("instance");  // Create object for signature control
            canvas = obj._canvas[0];
            context = canvas.getContext("2d");
            var img = new Image;
            img.src = "sample.png"; //specify image source
            context.clearRect(0, 0, canvas.width, canvas.height);  // Clear specified pixel

            img.onload = function () {
                context.drawImage(img, 0, 0);
            }
            obj.refresh();
        });
    </script>

{% endhighlight %}
 


