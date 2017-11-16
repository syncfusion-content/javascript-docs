---
layout: post
title: Tooltip
description: Tooltip
platform: js
control: RangeNavigator
documentation: ug
api: /api/js/ejrangenavigator
---


### Tooltip

**RangeNavigator** provides **Tooltip** support for sliders. Sliders are used to select data at particular range in the **RangeNavigator** control. **Tooltips** for sliders display the selected start and end **DateTime** values.

#### Customization

**RangeNavigator** provides support for you to customize the text display in the tooltip and background using [`tooltipSettings`](../api/ejrangenavigator#members:tooltipsettings) property. You can change font family, font color, font style, font weight. By default “**Segoe UI**” font family is set to tooltip text.

* Tooltip visibility can be enabled or disabled using [`visible`](../api/ejrangenavigator#members:tooltipsettings-visible) property.
* You can change background color of tooltip using [`backgroundColor`](../api/ejrangenavigator#members:tooltipsettings-backgroundcolor) property.
* You can customize the [`color`](../api/ejrangenavigator#members:tooltipsettings-font-color), [`family`](../api/ejrangenavigator#members:tooltipsettings-font-family), [`fontStyle`](../api/ejrangenavigator#members:tooltipsettings-font-fontstyle), [`opacity`](../api/ejrangenavigator#members:tooltipsettings-font-opacity), [`size`](../api/ejrangenavigator#members:tooltipsettings-font-size) and [`weight`](../api/ejrangenavigator#members:tooltipsettings-font-weight) of tooltip text in [`font`](../api/ejrangenavigator#members:tooltipsettings-font) property.

{% highlight javascript %}


$("#container").ejRangeNavigator(
               {   
                   // ...              
                tooltipSettings: {
                    visible: true,  
                    backgroundColor: "black",
                           //  To customize the tooltip text

                        font: {
                            color: 'red',
                            family: 'Segoe UI',
                            style: 'Normal',
                            size: '12px',
                            opacity: 1,
                            weight: 'regular'
                        }

                },
                   // ...             
               });


{% endhighlight %}



![](/js/RangeNavigator/Tooltip_images/Tooltip_img1.png) 

#### Label Format

By default, the **tooltip** texts are automatically determined based on the data points.  To make it readable and understandable you can format the **tooltip** text. For **DateTime** data, all globalized format are supported. By default the [`labelFormat`](../api/ejrangenavigator#members:tooltipsettings-labelformat) is "MM/dd/yyyy".

Some of the [`labelFormat`](../api/ejrangenavigator#members:tooltipsettings-labelformat) for **DateTime** data area as follows:

* 'MMM, yyyy'
* 'dd, MMM'
* 'dd/MM/yyyy'
* 'dd, hh:mm'
* 'hh:mm:ss'
* 'hh:mm:ss:tt'


{% highlight javascript %}


$("#container").ejRangeNavigator({
               {   
                   // ...              
                 tooltipSettings: {
                    labelFormat:'MMM, yyyy',
                },              
                   // ...             
               });


{% endhighlight %}


![](/js/RangeNavigator/Tooltip_images/Tooltip_img2.png) 

#### Tooltip display mode

By default the **tooltip** for RangeNavigator gets displayed. You can change this behavior using the [`tooltipDisplayMode`](../api/ejrangenavigator#members:tooltipsettings-tooltipdisplaymode) property in the tooltip and it takes the following values.



<table>
<tr>
<td>
<b>Value</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
always</td><td>
Tooltip get displayed for RangeNavigator always.</td></tr>
<tr>
<td>
onDemand</td><td>
Tooltip get displayed only when we move the slider.</td></tr>
</table>


{% highlight javascript %}


$("#container").ejRangeNavigator({
               {   
                   // ...              
                 tooltipSettings: {
                         tooltipDisplayMode: "onDemand",                    
                },              
                   // ...             
               });


{% endhighlight %}



![](/js/RangeNavigator/Tooltip_images/Tooltip_img3.png) 
