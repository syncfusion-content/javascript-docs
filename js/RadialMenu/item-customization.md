---
layout: post
title: item-customization
description: item customization
platform: js
control: Radial Menu
documentation: ug
---

## Item Customization

You can customize the **Radial Menu** items by using the **ImageUrl** and **Text** properties. The **imageUrl** property specifies the URL of the image for the items. **Data-ej-text** attribute is used to specify the item text. Refer to the following code example.

You can add the page content with text-area by referring to this section.

{% highlight html %}


    <div id="defaultradialmenu">
        <ul>
            <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/copy.png" data-ej-text="Copy"></li>
            <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/paste.png" data-ej-text="Paste"></li>
            <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/redo.png" data-ej-text="Redo"></li>
            <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/undo.png" data-ej-text="Undo"></li>
        </ul>
    </div>
    
{% endhighlight %}

Add the following script in your code.
    
{% highlight javascript %}

        $(function () {
            $('#defaultradialmenu').ejRadialMenu({ width: "250" });
        });

        $("#rteSampleone").select(function (e) {
            $('#defaultradialmenu').ejRadialMenu("show");
        });


{% endhighlight %}



The following screenshot illustrates the output.

![](item-customization_images\item-customization_img1.png)

