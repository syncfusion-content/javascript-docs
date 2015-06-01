---
layout: post
title: Configure-Badge
description: configure badge
platform: js
control: Tile
documentation: ug
---

# Configure Badge

The -**badge** property handles badge specific functionalities like enable or disable the badge and setting badge value for **Tile**.

The****“**data-ej-badge-enabled”** attribute enables or disables the badge for a **Tile**. The **Tile** renders with hidden badge when it is set to **false**.

The “**data-ej-badge-value”** attribute is used to set the badge value to a **Tile**. By default, the **Value** is set to **1** on initialization. The “**data-ej-badge-text”** attribute is****used****to****set the text instead of number for **Tile** badge. The “**data-ej-badge-maxvalue”** attribute****is****used****to set the maximum badge value to a **Tile**. When you set the badge value greater than “**data-ej-badge-maxvalue”**, it shows maximum value in badge with **plus** symbol. The “**data-ej-badge-minvalue”** attribute is used to set the minimum badge value to a **Tile**. When you set the badge value less than “**data-ej-badge-minvalue”**, it shows minimum value in badge.

Refer to the following code examples.

{% highlight javascript %}

    <div id="tile"></div>
    <script>
        $("#tile").ejTile({
            tileSize: "medium", imagePosition: "center",
            badge: { enabled: true, minVlaue: 10, maxValue: 80, value: 88 },
            text: "Messages", imageUrl: "http://js.syncfusion.com/UG/Web/Content/tile/messages.png"
        })
    </script> 


{% endhighlight %}



{% include image.html url="/js/Tile/Concepts-and-features/Configure-Badge_images/Configure-Badge_img1.png" Caption="Tile - Badge"%}

