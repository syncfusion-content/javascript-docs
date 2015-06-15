---
layout: post
title: Chart-Dimensions
description: chart dimensions
platform: js
control: Chart
documentation: ug
---

# Chart Dimensions

In this section you can learn how to change the **Chart****dimensions**. You can change the **Chart** height and width in terms of pixels and percentage with the **size** property. When size is specified, the Chart remains to that specific size irrespective of the size of the container. You can always resize the **Chart** when the browser or **Chart** container is resized by setting **canResize** property to **true**, where the **Chart** adapts to the changes in size of the container. By default, **Chart** height will be 450px and **Chart** width takes the container width as default value.

## Setting dimension in pixel values:

You can specify the width and height in pixels to change the dimension of the Chart. 

**Setting size**

{% highlight js %}


****$("#chartcontainer").ejChart({
            size: { width: "800", height: "600" },
            canResize: true,
        });


{% endhighlight %}



In the above code, the width is set as 800px and height as 600px that displays the following Chart with the dimension 800*600.

{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Dimensions_images/Chart-Dimensions_img1.png" Caption="Chart with the dimension 800*600"%}

## Setting dimension in percentage values:

You can also set the width and height of the **Chart** in percentage. The Chart gets its dimension with respect to its container size.

**Setting size in percentage**

{% highlight js %}


    <div id="chartContainer" style="width: 700px; height: 500px; border-color: #ff0000; border-style: solid;">
    </div>


        $("#chartcontainer").ejChart({
            size: { width: "80%", height: "90%" },
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Concepts-and-Features/Chart-Dimensions_images/Chart-Dimensions_img2.png" Caption="Chart with dimension"%}

