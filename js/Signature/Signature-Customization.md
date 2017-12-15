---
layout: post
title:  signature customization
description:  signature customization
platform: js
control: Signature
documentation: ug
api: /api/js/ejsignature
---

# Signature Customization

## Background color

Signature widget allows you to set the background Color for the control using the [backgroundColor](https://help.syncfusion.com/api/js/ejsignature#members:backgroundcolor) property. When we set our required background, then the signature’s background color will be changed automatically.

The following code example is used to render the Signature control with background color

Add the following script to render signature with customized background color.

{% highlight js %}

  <script type="text/javascript">
        $(function () {
            $("signature").ejSignature({ backgroundColor:"grey" });
        });
    </script>

{% endhighlight %}

The following screenshot illustrates the Signature with custom defined background color.

![](Signature_Customization_images\backgroundcolor_img1.png)

## Background Image

Signature widget allows you to set the background image for the control using the [backgroundImage](https://help.syncfusion.com/api/js/ejsignature#members:backgroundimage) property. When we set our required background image, then the signature’s canvas will be changed with the given image.

The following code example is used to render the Signature control with customized background image.

Add the following script to render signature with customized value.

{% highlight js %}

   <script type="text/javascript">
        $(function () {
            $("signature").ejSignature({ backgroundImage: "image.jpg" });
        });
    </script>

{% endhighlight %}

The following screenshot illustrates the Signature with custom defined background image.

![](Signature_Customization_images\backgroundimage_img1.png)



## Stroke color

Signature widget allows you to set the stroke color for the signature stroke using the [strokeColor](https://help.syncfusion.com/api/js/ejsignature#members:strokecolor) property. When we set our required color, then the signature’s stroke color will be changed.

The following code example is used to render the Signature control with stroke color.

Add the following script to render signature with customized stroke color.

{% highlight js %}

   <script type="text/javascript">
        $(function () {
            $("signature").ejSignature({ strokeColor: "red" });
        });
    </script>

{% endhighlight %}

The following screenshot illustrates the Signature with custom defined stroke color.

![](Signature_Customization_images\strokecolor_img1.png)

## Stroke Width

Signature widget allows you to set the stroke width for the control using the [strokeWidth](https://help.syncfusion.com/api/js/ejsignature#members:strokewidth) property. When we set our required width, then the signature’s stroke width will be changed.

The following code example is used to render the Signature control with maximum stroke value.

Add the following script to render signature with customized stroke width.

{% highlight js %}

   <script type="text/javascript">
        $(function () {
            $("signature").ejSignature({ strokeWidth: 4 });
        });
    </script>

{% endhighlight %}

The following screenshot illustrates the Signature with custom defined stroke maximum value.

![](Signature_Customization_images\strokewidth_img1.png)