---
layout: post
title: LiveTile-Configuration
description: livetile configuration
platform: js
control: Tile
documentation: ug
api: /api/js/ejtile
---

# LiveTile Configuration

**Live Tiles** are used to display the current or up to date information like scores, stocks, weather, etc. You can enable [LiveTile](https://help.syncfusion.com/api/js/ejtile#members:livetile) using “**data-ej-livetile-enabled”** attribute by setting it to **true**. The **"data-ej-livetile-type”** attribute allows you to specify the type of animation while updating the information in **Tile**. There are three types of **Tile** animation supported: Flip, Slide and Carousel.

The **“data-ej-livetile-imageUrl”** attribute sets background image for **Live Tile**. This property accepts array values so you can specify the image **url’s** for all the **Tiles** that are used in single **Live Tile**. 

You can specify time interval for each **Tile** update/animation using **"data-ej-livetile-updateInterval”** attribute. Time interval is given in milliseconds. The default value is 2000.

Refer to the following code examples.

{% highlight html %}

    <div id="tile"></div>

{% endhighlight %}

Add the following code inside the **script** tag.

{% highlight javascript %}    
   
        $("#tile").ejTile({
            tileSize: "medium", imagePosition: "fill",
            liveTile: {
                updateInterval: 2500, type: "flip", enabled: true,
                imageUrl: ['http://js.syncfusion.com/UG/Web/Content/tile/people_1.png', 'http://js.syncfusion.com/UG/Web/Content/tile/people_2.png']
            },
            text: "Peoples"
        });
 
{% endhighlight %}



In **"data-ej-livetile-imageTemplateId”** attribute, you can give **Live Tile** images outside the **Tile** rendering. To achieve this, you are required to give image content inside the element where the path is specified by **templateId**. You can update the “**imageTemplateId”** dynamically through **updateTemplateID** public method**.**

Refer to the following code examples. 



{% highlight html %}


    <div id="tile"></div>
    <div id="temp1" style="background-image:
            url('http://js.syncfusion.com/UG/Web/Content/tile/people_1.png'); width: 100%; height: 100%;">
    </div>
    <div id="temp2" style="background-image:
            url('http://js.syncfusion.com/UG/Web/Content/tile/people_2.png'); width: 100%; height: 100%;">
    </div>
 
{% endhighlight %}  

Add the following code inside the **script** tag.

{% highlight javascript %}
    
        $("#tile").ejTile({
            tileSize: "medium", imagePosition: "fill",
            liveTile: {
                updateInterval: 2500, type: "flip", enabled: true,
                imageTemplateId: ["temp1", "temp2"]
            },
            text: "Peoples"
        });

{% endhighlight %}



You can specify the array of images for **Live Tile** through **CSS** classes by using “**data-ej-livetile-imageClass”** attribute and you can define the desired styles in the specified class.

Refer to the following code examples.



{% highlight html %}

    <div id="tile"></div>
    
{% endhighlight %}
    
{% highlight css %}
    
    <style>
        .people1 {
            background-image: url('http://js.syncfusion.com/UG/Web/Content/tile/people_1.png');
            width: 100%;
            height: 100%;
        }
        .people2 {
            background-image: url('http://js.syncfusion.com/UG/Web/Content/tile/people_2.png');
            width: 100%;
            height: 100%;
        }
    </style>
    
 {% endhighlight %}

Add the following code inside the **script** tag.
    
{% highlight javascript %}
        
        $("#tile").ejTile({
            tileSize: "medium", imagePosition: "fill",
            liveTile: {
                updateInterval: 2500, type: "flip", enabled: true,
                imageClass: ["people1", "people2"]
            },
            text: "Peoples"
        });

{% endhighlight %}



