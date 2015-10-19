---
layout: post
title: width
description: width
platform: js
control: Radial Menu
documentation: ug
---

## Width

You can customize the **Radial Menu** width or radius by using the **width** property. By default, the **Radial Menu** width is set as 300px. Refer to the following code example.

You can add the page content with text-area by referring to this section.

{% highlight html %}


    <div id="defaultradialmenu">
        <ul>
            <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/font.png" data-ej-text="Bold"></li>
            <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/f1.png" data-ej-text="Italic"></li>
            <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/align.png" data-ej-text="Align"></li>
            <li data-ej-imageurl="http://js.syncfusion.com/UG/web/Content/radial/sort.png" data-ej-text="Sort"></li>
        </ul>
    </div>
    
{% endhighlight %}

Add the following script in your code.
    
{% highlight js %}

        $(function () {
            $('#defaultradialmenu').ejRadialMenu({ width: "250"});
        });
        
        $("#rteSampleone").select(function (e) {
            $('#defaultradialmenu').ejRadialMenu("show");
        });

{% endhighlight %}



The following screenshot illustrates the output while selecting the text in the page.

![](width_images\width_img1.png)

Selecting text in the page
{:.caption}



The following screenshot illustrates the **Radial Menu** while clicking on the settings icon.

![](width_images\width_img2.png)

