---
layout: post
title: Layout
description: layout
platform: js
control: TreeMap
documentation: ug
---

# Layout

You can decide on the visual representation of nodes belonging to all the treemap levels using the **itemsLayoutMode** property of the TreeMap.

There are four different **TreeMap** layouts such as

* Squarified Layout

* SliceAndDiceAuto Layout

* SliceAndDiceHorizontal Layout

* SliceAndDiceVertical Layout

**Squarified Layout**

**Squarified****layout** creates rectangles with best aspect ratio.

{% highlight js %}

**[HTML]**
        jQuery(function ($) {

            $("#treemapContainer").ejTreeMap({
                dataSource: population_data,
                colorValuePath: "Growth",
                weightValuePath: "Population",                
                levels: [
                  { groupPath: "Continent", groupGap: 5 }
                ],
                **itemsLayoutMode:"Squarified"**
            });
        });


{% endhighlight %}



{% include image.html url="/js/TreeMap/Concepts-and-Features/Layout_images/Layout_img1.png" Caption="Squarified Layout"%}

**SliceAndDiceAuto Layout**

**SliceAndDiceAuto layout** creates rectangles with high aspect ratio and displays them sorted both horizontally and vertically.

{% highlight js %}


**[HTML]**

       jQuery(function ($) {

            $("#treemapContainer").ejTreeMap({
                // ...             
                **itemsLayoutMode:"SliceAndDiceAuto",**
                // ...             
            });
        });


{% endhighlight %}



{% include image.html url="/js/TreeMap/Concepts-and-Features/Layout_images/Layout_img2.png" Caption="SliceAndDiceAuto Layout"%}

**SliceAndDiceHorizontal Layout**

**SliceAndDiceHorizontal layout** creates rectangles with high aspect ratio and displays them sorted horizontally.

{% highlight js %}

**[HTML]**
       jQuery(function ($) {

            $("#treemapContainer").ejTreeMap({
                // ...   
                **itemsLayoutMode:"SliceAndDiceHorizontal",**
                // ...   
            });
        });



{% endhighlight %}



{% include image.html url="/js/TreeMap/Concepts-and-Features/Layout_images/Layout_img3.png" Caption="SliceAndDiceHorizontal Layout"%}

**SliceAndDiceVertical Layout**

**SliceAndDiceVertical layout** creates rectangles with high aspect ratio and displays them sorted vertical.

{% highlight js %}

**[HTML]**
        jQuery(function ($) {

            $("#treemapContainer").ejTreeMap({
                // ...   
                **itemsLayoutMode:"SliceAndDiceVertical",**
                // ...   
            });
        });



{% endhighlight %}



{% include image.html url="/js/TreeMap/Concepts-and-Features/Layout_images/Layout_img4.png" Caption="SliceAndDiceVertical Layout"%}

