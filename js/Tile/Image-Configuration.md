---
layout: post
title: Image-Configuration
description: image configuration
platform: js
control: Tile
documentation: ug
---

# Image Configuration

The **“data-ej-imageposition”** attribute is used to adjust the position of **Tile** image at the **center** on initialization. The possible values for the “**data-ej-imageposition”** are as follows

1. center
2. top
3. bottom
4. right
5. left
6. topleft
7. bottomright
8. bottomleft 
9. fill



The **"data-ej-imageurl”** attribute is used to set the background image for **Tile**, where the image is given in the path specified by “**data-ej-imageurl”** attribute.

Refer to the following code examples.

{% highlight html %}

    <div id="tile"></div>
    
{% endhighlight %}
{% highlight js %}

    $("#tile").ejTile({ tileSize: "wide", imagePosition: "center", imageUrl: "http://js.syncfusion.com/UG/web/Content/tile/Weather_2.png", text: "weather" });

{% endhighlight %}



{% include image.html url="/js/Tile/Image-Configuration_images/Image-Configuration_img1.png" Caption="Tile - Image URL and Image Position"%}

You can give images for each tile through **css** classes by using **"data-ej-imageclass”** attribute. You can define your desired styles in the specified class.

Refer to the following code examples.

{% highlight javascript %}

    <div id="tile"></div>
<script>
    $("#tile").ejTile({ tileSize: "medium", imagePosition: "center", **imageClass: "pictures"**, text: "Pictures" })
</script>
    <style>
        .pictures {
            background: url("http://js.syncfusion.com/UG/web/Content/tile/pictures.png");
            background-size: 30px 30px;
        }
    </style>


{% endhighlight %}



{% include image.html url="/js/Tile/Image-Configuration_images/Image-Configuration_img2.png" Caption="Tile – Image Class"%}

