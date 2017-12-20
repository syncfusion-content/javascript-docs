---
layout: post
title: Dimensions
description: dimensions
platform: js
control: ListView
documentation: ug
api: /api/js/ejlistview
---

# Dimensions

To customize the **ListView** dimensions, [Width](https://help.syncfusion.com/api/js/ejlistview#members:width) and [Height](https://help.syncfusion.com/api/js/ejlistview#members:height) properties are used.

Refer to the following code examples.



{% highlight html %}


    <div id="defaultListView">
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
    
{% endhighlight %}

Add the following script in your code.
    
{% highlight javascript %}

        $(function () {
            $("#defaultListView").ejListView({ width: 300, height: 600 });
        });

{% endhighlight %}



Run the code to get the following output

![](/js/ListView/Dimensions_images/Dimensions_img1.png) 

