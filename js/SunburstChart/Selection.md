---
layout: post
title: Selection
description: What are the different modes of selection present in the Sunburst Chart
platform: js
control: SunburstChart
documentation: ug
api: /api/js/ejsunburstchart
---

# Selection 
EjSunburstChart provides selection support for the points on mouse click. To [`enable`](../api/ejsunburstchart#members:selectionsettings-enable) the selection , set the [`enable`](../api/ejsunburstchart#members:selectionsettings-enable) property to true in the [`selectionSettings`](../api/ejsunburstchart#members:selectionsettings). 

{% highlight js %}

$("#chart").ejSunburstChart({

          //..         
          selectionSettings: { enable: true },         
         //..

});
{% endhighlight %}

![](/js/SunburstChart/Selection_images/Selection_img1.png)

 
## Selection Display mode

 You can customize the selected  segment appearance by using [`color`](../api/ejsunburstchart#members:selectionsettings-color) or [`opacity`](../api/ejsunburstchart#members:selectionsettings-opacity). You can choose between color or opacity using the [`type`](../api/ejsunburstchart#members:selectionsettings-type) property in the selection Settings.

*	selectionByColor – To display the selected segment appearance using color.
*	selectionByOpacity – To display the selected segment appearance using opacity.

{% highlight js %}

$("#chart").ejSunburstChart({

          //..         
          selectionSettings: { enable: true, type:"color",color:"red" },         
          //..

});

 {% endhighlight %}

![](/js/SunburstChart/Selection_images/Selection_img2.png)

## Selection Mode

Sunburst chart provides multiple options to represent the selected categories. You can select the segment categories by using the [`mode`](../api/ejsunburstchart#members:selectionsettings-mode) property in selectionSettings
*	Child – To selection the child of selected parent.
*	All – To selection the entire categories in group.
*	Parent – To selection the parent of selected child.
*	Single - To selection single item in the category.

### Child

The following code shows how to set the selection type as child 

{% highlight js %}

$("#chart").ejSunburstChart({

          //..         
          selectionSettings: { enable: true,mode:"child"},         
          //..

});
{% endhighlight %}

![](/js/SunburstChart/Selection_images/Selection_img3.png)
 
### Parent

The parent mode can be enabled by using the below code 

{% highlight js %}

$("#chart").ejSunburstChart({

          //..         
          selectionSettings: { enable: true,mode:"parent"},         
         //..

});
{% endhighlight %}

![](/js/SunburstChart/Selection_images/Selection_img4.png)
 
### Point

To selection the particular segment, the point mode of the selection settings is used.

{% highlight js %}

$("#chart").ejSunburstChart({

          //..         
          selectionSettings: { enable: true,mode:"point"},         
         //..

});
 {% endhighlight %}

![](/js/SunburstChart/Selection_images/Selection_img5.png)
 
### All

The following code snippet is used for the all mode of selection settings

{% highlight js %}
$("#chart").ejSunburstChart({

          //..         
          selectionSettings: { enable: true,mode:"all"},         
          //..

});

{% endhighlight %}

![](/js/SunburstChart/Selection_images/Selection_img6.png)

[Click](http://js.syncfusion.com/demos/web/#!/bootstrap/sunburst/selection) here to view the online demo sample of Selection  in  the Sunburst Chart
