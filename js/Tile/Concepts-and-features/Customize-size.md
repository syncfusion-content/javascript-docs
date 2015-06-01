---
layout: post
title: Customize-size
description: customize size
platform: js
control: Tile
documentation: ug
---

# Customize size

You can customize the size of the **Tile** by using **“data-ej-tileSize”** attribute. The following built-in tile sizes are supported.

1. medium

2. small

3. large

4. wide



The default **TileSize** value is set to s**mall.**

Refer to the following code examples.

{% highlight javascript %}


    <div id="tile"></div>
    <script>
        $("#tile").ejTile({
            tileSize: "medium", imagePosition: "center",
            imageUrl: "http://js.syncfusion.com/UG/Web/Content/tile/pictures.png",
            text: "Pictures"
        })
    </script>	


{% endhighlight %}



{% include image.html url="/js/Tile/Concepts-and-features/Customize-size_images/Customize-size_img1.png" Caption="Tile - Tile Size"%}

