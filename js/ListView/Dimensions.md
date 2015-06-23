---
layout: post
title: Dimensions
description: dimensions
platform: js
control: ListView
documentation: ug
---

# Dimensions

To customize the **ListView** dimensions, **Width** and **Height** properties are used.

Refer to the following code examples.



{% highlight html %}


    <div id="defaultlistbox">
        <ul>
            <li data-ej-text="Artwork"></li>
            <li data-ej-text="Abstract"></li>
            <li data-ej-text="2 Acrylic Mediums"></li>
            <li data-ej-text="Creative Acrylic"></li>
            <li data-ej-text="Canvas Art"></li>
            <li data-ej-text="Black white"></li>
            <li data-ej-text="Children"></li>
            <li data-ej-text="Preschool Crafts"></li>
            <li data-ej-text="School-age Crafts"></li>
        </ul>
    </div>
    <script type="text/javascript">
        $(function () {
            $("#defaultlistbox").ejListView({ width: 300, height: 600 });
        });
    </script>




{% endhighlight %}



**Screenshot:**

{% include image.html url="/js/ListView/Dimensions_images/Dimensions_img1.png" %}

