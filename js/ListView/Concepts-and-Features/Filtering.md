---
layout: post
title: Filtering
description: filtering
platform: js
control: ListView
documentation: ug
---

# Filtering

**Filtering** is one of the key features of **ListView** control. The **Filtering** option is added into the **ListView** control when the **data-ej-enablefiltering** attribute is set to **“True”**. This enables a simple interface to filter items from a large collection of **ListView** items.

Refer the following code examples.



{% highlight javascript %}


    <div id="defaultlistbox" >
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
    <script type="text/javascript">
        $(function () {
            $("#defaultlistbox").ejListView({ width:300, enableFiltering:true });
        });
    </script>



{% endhighlight %}



**Screenshot:**

{% include image.html url="/js/ListView/Concepts-and-Features/Filtering_images/Filtering_img1.png" Caption="Enable Filtering"%}



{% include image.html url="/js/ListView/Concepts-and-Features/Filtering_images/Filtering_img2.png" Caption="Enable Filtering"%}

