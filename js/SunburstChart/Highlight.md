---
layout: post
title: Highlight
description: What are the different modes of highlight present in the Sunburst Chart
platform: js
control: Sunburst Chart
documentation: ug
api: /api/js/ejsunburstchart
---

# Highlight 
EjSunburstChart provides highlighting support for the points on mouse hover. To [`enable`](../api/ejsunburstchart#members:highlightSettings-enable) the highlighting , set the [`enable`](../api/ejsunburstchart#members:highlightsettings-enable) property to true in the [`highlightSettings`](../api/ejsunburstchart#members:highlightsettings). 

{% highlight js %}

$("#chart").ejSunburstChart({

          //..         
          highlightSettings: { enable: true },         
         //..

});
{% endhighlight %}

![](/js/SunburstChart/Highlight_images/Highlight_img1.png)

 
## Highlight Display mode

 You can customize the highlighted segment appearance by using [`color`](../api/ejsunburstchart#members:highlightsettings-color) or [`opacity`](../api/ejsunburstchart#members:highlightsettings-opacity). You can choose between color or opacity using the [`type`](../api/ejsunburstchart#members:highlightsettings-type) property in the highlight Settings.

*	HighlightByColor – To display the highlighted segment appearance using color.
*	HighlightByOpacity – To display the highlighted segment appearance using opacity.

{% highlight js %}

$("#chart").ejSunburstChart({

          //..         
          highlightSettings: { enable: true, type:"color",color:"red" },         
         //..

 });

 {% endhighlight %}

![](/js/SunburstChart/Highlight_images/Highlight_img2.png)

## Highlight Mode

Sunburst chart provides multiple options to represent the highlighted categories. You can highlight the segment categories by using the [`mode`](../api/ejsunburstchart#members:highlightsettings-mode) property in highlightSettings

*	Child – To highlight the child of selected parent.
*	All – To highlight the entire categories in group.
*	Parent – To highlight the parent of selected child.
*	Single - To highlight single item in the category.

### Child

The following code shows how to set the highlight type as child 

{% highlight js %}

$("#chart").ejSunburstChart({

          //..         
          highlightSettings: { enable: true,mode:"child"},         
//..

});
{% endhighlight %}

![](/js/SunburstChart/Highlight_images/Highlight_img3.png)
 
### Parent

The parent mode can be enabled by using the below code 

{% highlight js %}

$("#chart").ejSunburstChart({

          //..         
          highlightSettings: { enable: true,mode:"parent"},         
          //..

});
{% endhighlight %}

![](/js/SunburstChart/Highlight_images/Highlight_img4.png)
 
### Point

To highlight the particular segment, the point mode of the highlight settings is used.

{% highlight js %}

$("#chart").ejSunburstChart({

          //..         
          highlightSettings: { enable: true,mode:"point"},         
         //..

});
 {% endhighlight %}

![](/js/SunburstChart/Highlight_images/Highlight_img5.png)
 
### All

The following code snippet is used for the all mode of highlight settings

{% highlight js %}
$("#chart").ejSunburstChart({

          //..         
          highlightSettings: { enable: true,mode:"all"},         
         //..

});

{% endhighlight %}

![](/js/SunburstChart/Highlight_images/Highlight_img6.png)

[Click](http://js.syncfusion.com/demos/web/#!/bootstrap/sunburst/selection) here to view the online demo sample of Highlight  in  the Sunburst Chart
