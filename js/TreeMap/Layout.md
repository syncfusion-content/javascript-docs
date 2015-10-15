---
layout: post
title: Layout
description: layout
platform: js
control: TreeMap
documentation: ug
---

# Layout

You can decide on the visual representation of nodes belonging to all the treemap levels using the `itemsLayoutMode` property of the TreeMap.

There are four different **TreeMap** layouts such as

* Squarified
* SliceAndDiceAuto
* SliceAndDiceHorizontal
* SliceAndDiceVertical

## Squarified

**Squarified** layout creates rectangles with best aspect ratio.

{% highlight js %}

        jQuery(function ($) {

            $("#treemapContainer").ejTreeMap({
                dataSource: population_data,
                colorValuePath: "Growth",
                weightValuePath: "Population",                
                levels: [
                  { groupPath: "Continent", groupGap: 5 }
                ],
                itemsLayoutMode:"squarified"
            });
        });


{% endhighlight %}



![]("/js/TreeMap/Layout_images/Layout_img1.png")

## SliceAndDiceAuto

**SliceAndDiceAuto** layout creates rectangles with high aspect ratio and displays them sorted both horizontally and vertically.

{% highlight js %}


       jQuery(function ($) {

            $("#treemapContainer").ejTreeMap({
                // ...             
                itemsLayoutMode:"sliceanddiceauto",
                // ...             
            });
        });


{% endhighlight %}



![]("/js/TreeMap/Layout_images/Layout_img2.png")

## SliceAndDiceHorizontal

**SliceAndDiceHorizontal** layout creates rectangles with high aspect ratio and displays them sorted horizontally.

{% highlight js %}

       jQuery(function ($) {

            $("#treemapContainer").ejTreeMap({
                // ...   
                itemsLayoutMode:"sliceanddicehorizontal",
                // ...   
            });
        });



{% endhighlight %}



![]("/js/TreeMap/Layout_images/Layout_img3.png")

## SliceAndDiceVertical

**SliceAndDiceVertical** layout creates rectangles with high aspect ratio and displays them sorted vertical.

{% highlight js %}

        jQuery(function ($) {

            $("#treemapContainer").ejTreeMap({
                // ...   
                itemsLayoutMode:"sliceanddicevertical",
                // ...   
            });
        });



{% endhighlight %}



![]("/js/TreeMap/Layout_images/Layout_img4.png")

