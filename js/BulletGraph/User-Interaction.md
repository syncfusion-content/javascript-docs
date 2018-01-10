---
layout: post
title: User-Interaction
description: user interaction
platform: js
control: BulletGraph	
documentation: ug
api: /api/js/ejbulletgraph
---

# User Interaction

## Animation

**Bullet Graph** supports animation that makes the performance measure bar to animate when rendering the **Bullet Graph**. **Animation** is enabled or disabled using [`enable animation`](../api/ejbulletgraph#members:enableanimation) property. By default, **Animation** is enabled in **Bullet Graph**.

{% highlight javascript %}



$("#BulletGraph1").ejBulletGraph({
                    enableAnimation: true,
                    value: 8,
                    comparativeMeasureValue: 5,                    
                });


{% endhighlight %}

## Responsiveness during browser resize

**Bullet Graph** is made responsive when resizing the browser by using [`isResponsive`](../api/ejbulletgraph#members:isresponsive) property. By default the value of this property is **true** in **Bullet Graph**.

{% highlight javascript %}



$("#BulletGraph1").ejBulletGraph({
                    isResponsive: true,
                    value: 8,
                    comparativeMeasureValue: 5,                    
                });


{% endhighlight %}

Responsiveness of the bullet graph is controlled by using [`enableResize`](../api/ejbulletgraph#members:enableresizing) property.

{% highlight javascript %}

<div id="BulletGraph1"></div> 
 
<script>
        $("#BulletGraph1").ejBulletGraph({ enableResizing: true });   
</script>

{% endhighlight %}



## Applying same color to all ticks and labels in a range

Background color for qualitative range is applied to major ticks and minor ticks of the **Bullet Graph** using [`applyRangeStrokeToTicks`](../api/ejbulletgraph#members:applyrangestroketoticks) property. The range colors are applied to labels using [`applyRangeStrokeToLabels`](../api/ejbulletgraph#members:applyrangestroketolabels) property. By default same colors are not applied to a qualitative range and its corresponding ticks or labels.

{% highlight javascript %}



$("#BulletGraph1").ejBulletGraph({
                    applyRangeStrokeToTicks: true,
                    applyRangeStrokeToLabels: true,

                    qualitativeRanges: [
                        { rangeEnd: 3.5, rangeStroke: 'darkred', rangeOpacity: 0.5 },
                        { rangeEnd: 5.0, rangeStroke: 'red', rangeOpacity: 1 },
                        { rangeEnd: 7.5, rangeStroke: 'blue', rangeOpacity: 0.7 },
                        { rangeEnd: 9.0, rangeStroke: 'lightgreen', rangeOpacity: 1 },
                        { rangeEnd: 10.0, rangeStroke: 'green', rangeOpacity: 1 }
                    ],
                    value: 8,
                    comparativeMeasureValue: 5,                    
                });


{% endhighlight %}

![](/js/BulletGraph/User-Interaction_images/User-Interaction_img1.png) 

## Tooltip

By default **Bullet Graph** displays **Tooltip** when mouse is hovered over feature measure bar. **Tooltip** is enabled or disabled using [`visible`](../api/ejbulletgraph#members:tooltipsettings-visible) property in [`tooltipSettings`](../api/ejbulletgraph#members:tooltipsettings).

![](/js/BulletGraph/User-Interaction_images/User-Interaction_img2.png) 

Bullet Graph supports Tooltip template instead of default Tooltip to customize the appearance and contents of Tooltip. The Tooltip template should be a &lt;div&gt; element with display set to ‘none’, so it is displayed only when mouse is placed on feature measure bar. The id value of the &lt;div&gt; element should be provided as value to the [`template`](../api/ejbulletgraph#members:tooltipsettings-template) property in tooltipSettings of Bullet Graph to display the customized &lt;div&gt; element as Tooltip instead of default Tooltip. The values displayed in default Tooltip such as current value, target value and category are accessed in template &lt;div&gt; element by using {{currentValue}}, {{targetValue}} and {{category}} respectively.


{% highlight html %}

<div id="BulletGraphTooltip" style="display:none; width:125px; padding-top: 10px; padding-bottom:10px; color: blue"> 
    <div align="center" style="color:blue; font-weight:bold"> Sales </div> 
    <table style="color:green"> <tr> <td> Current </td> <td> : </td> </tr> <tr> <td> Target </td> <td> : </td> </tr> </table> 
</div>

{% endhighlight %}

{% highlight javascript %}

    $("#BulletGraph1").ejBulletGraph({
         value: 8,
         comparativeMeasureValue: 6,
         height: 150,
         tooltipSettings: { template: 'BulletGraphTooltip' } 
    });

{% endhighlight %}

### captionTemplate

Specifies template for caption tooltip by using the property [`captionTooltip`](../api/ejbulletgraph#members:tooltipsettings-captiontemplate)

{% highlight javascript %}

<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
tooltipSettings :{captionTemplate: "BulletGraphTooltip"}
});
</script>

{% endhighlight %}

### enableCaptionTooltip 

Toggles the visibility of caption tooltip by using the property [`enableCaptionTooltip`](../api/ejbulletgraph#members:tooltipsettings-enablecaptiontooltip)

{% highlight javascript %}

<div id="bulletGraph1"></div> 
<script>
$("#bulletGraph1").ejBulletGraph({
tooltipSettings :{enableCaptionTooltip: true}
});
</script>

{% endhighlight %}

The following screenshot displays **Bullet Graph** with a customized **Tooltip** including a header and contents such as current value and target value in different colors.

![](/js/BulletGraph/User-Interaction_images/User-Interaction_img3.png) 

## Localization

**BulletGraph** supports localization for its axis labels and tooltip. To render the gauge with specific culture you have to refer the corresponding globalize culture script and need to specify the culture name in [`locale`](../api/ejbulletgraph#members:locale) property of gauge.

**Enable Group Separator** is used to Convert the date object to string while using the locale settings, you can set [`enableGroupSeparator`](../api/ejbulletgraph#members:enablegroupseparator) property as **true**.

{% highlight javascript %}

<div id="BulletGraph1"></div> 
 
<script>
        $("#BulletGraph1").ejBulletGraph({ 
            locale : "en-US" ,
            enableGroupSeparator: true
            }); 
</script>

{% endhighlight %}


