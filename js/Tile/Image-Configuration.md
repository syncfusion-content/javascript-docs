---
layout: post
title: Image-Configuration
description: image configuration
platform: js
control: Tile
documentation: ug
api: /api/js/ejtile
---

# Image Configuration

The [data-ej-imagePosition](https://help.syncfusion.com/api/js/ejtile#members:imageposition) attribute is used to adjust the position of **Tile** image at the **center** on initialization. The possible values for the “**data-ej-imagePosition”** are as follows

1. center
2. top
3. bottom
4. right
5. left
6. topleft
7. bottomright
8. bottomleft 
9. fill



The [data-ej-imageUrl](https://help.syncfusion.com/api/js/ejtile#members:imageurl) attribute is used to set the background image for **Tile**, where the image is given in the path specified by “**data-ej-imageUrl”** attribute.

Refer to the following code examples.

{% highlight html %}

    <div id="tile"></div>
    
{% endhighlight %}
 
Add the following code inside the **script** tag.
 
{% highlight javascript %}

    $("#tile").ejTile({ tileSize: "wide", imagePosition: "center", imageUrl: "http://js.syncfusion.com/UG/web/Content/tile/Weather_2.png", text: "weather" });

{% endhighlight %}



![](/js/Tile/Image-Configuration_images/Image-Configuration_img1.png)

You can give images for each tile through **css** classes by using [data-ej-imageClass](https://help.syncfusion.com/api/js/ejtile#members:imageclass) attribute. You can define your desired styles in the specified class.

Refer to the following code examples.

{% highlight html %}

    <div id="tile"></div>
    
{% endhighlight %}

{% highlight css %}
    <style>
        .pictures {
            background: url("http://js.syncfusion.com/UG/web/Content/tile/pictures.png");
            background-size: 30px 30px;
        }
    </style>

{% endhighlight %}

Add the following code inside the **script** tag.

{% highlight javascript %}

    $("#tile").ejTile({ tileSize: "medium", imagePosition: "center", imageClass: "pictures", text: "Pictures" });

{% endhighlight %}

![](/js/Tile/Image-Configuration_images/Image-Configuration_img2.png)

