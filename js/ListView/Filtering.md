---
layout: post
title: Filtering
description: filtering
platform: js
control: ListView
documentation: ug
api: /api/js/ejlistview
---

# Filtering

**Filtering** is one of the key features of **ListView** control. The **Filtering** option is added into the **ListView** control when the [enableFiltering](https://help.syncfusion.com/api/js/ejlistview#members:enablefiltering) property is set to **“true”**. This enables a simple interface to filter items from a large collection of **ListView** items.

Refer the following code examples.



{% highlight html %}



    <div id="defaultListView">
        <ul>
            <li data-ej-text="Artwork"></li>
            <li data-ej-text="Abstract"></li>
            <li data-ej-text="2 Acrylic Mediums"></li>
            <li data-ej-text="Creative Acrylic"></li>
            <li data-ej-text="Modern Painting"></li>
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
            $("#defaultListView").ejListView({ width: 300, enableFiltering: true });
        });


{% endhighlight %}



**Screenshot:**

![](/js/ListView/Filtering_images/Filtering_img1.png)

Before Filtering
{:.caption}



![](/js/ListView/Filtering_images/Filtering_img2.png)

After Filtering
{:.caption}

