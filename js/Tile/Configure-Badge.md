---
layout: post
title: Configure-Badge
description: configure badge
platform: js
control: Tile
documentation: ug
api: /api/js/ejtile
---

# Configure Badge

The [badge](https://help.syncfusion.com/api/js/ejtile#members:badge) property handles badge specific functionalities like enable or disable the badge and setting badge value for **Tile**.

The [data-ej-badge-enabled](https://help.syncfusion.com/api/js/ejtile#members:badge-enabled) attribute enables or disables the badge for a **Tile**. The **Tile** renders with hidden badge when it is set to **false**.

The [data-ej-badge-value](https://help.syncfusion.com/api/js/ejtile#members:badge-value) attribute is used to set the badge value to a **Tile**. By default, the **Value** is set to **1** on initialization. The **"data-ej-badge-text"** attribute is used to set the text instead of number for **Tile** badge. 

The [data-ej-badge-maxValue](https://help.syncfusion.com/api/js/ejtile#members:badge-maxvalue) attribute is used to set the maximum badge value to a **Tile**. When you set the badge value greater than **"data-ej-badge-maxValue”**, it shows maximum value in badge with **plus** symbol. 

The [data-ej-badge-minValue](https://help.syncfusion.com/api/js/ejtile#members:badge-minvalue) attribute is used to set the minimum badge value to a **Tile**. When you set the badge value less than **"data-ej-badge-minValue”**, it shows minimum value in badge.

Refer to the following code examples.

{% highlight html %}

    <div id="tile"></div>
    
{% endhighlight %}

Add the following code inside the **script** tag.

{% highlight javascript %}

        $("#tile").ejTile({
            tileSize: "medium", imagePosition: "center",
            badge: { enabled: true, minValue: 10, maxValue: 80, value: 88 },
            text: "Messages", imageUrl: "http://js.syncfusion.com/UG/Web/Content/tile/messages.png"
        });

{% endhighlight %}



![](/js/Tile/Configure-Badge_images/Configure-Badge_img1.png)

