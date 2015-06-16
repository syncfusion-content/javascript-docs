---
layout: post
title: Tooltip
description: Tooltip
platform: js
control: RangeNavigator
documentation: ug
---


### Tooltip

**RangeNavigator** provides **Tooltip** support for sliders. Sliders are used to select data at particular range in the **RangeNavigator** control. **Tooltips** for sliders display the selected start and end **DateTime** values.

#### Customization

**RangeNavigator** provides support for you to customize the text display in the tooltip and background using **tooltipSettings** property. You can change font family, font color, font style, font weight. By default “**Segoe UI**” font family is set to tooltip text.


{% highlight js %}


$("#rangecontainer").ejRangeNavigator(
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



{% include image.html url="/js/RangeNavigator/Concepts-and-features_images/Concepts-and-features_img19.png" Caption="Figure 24: Tool Tip"%}

#### Label Format

By default, the **tooltip** texts are automatically determined based on the data points.  To make it readable and understandable you can format the **tooltip** text. For **DateTime** data, all globalized format are supported. By default the **labelFormat** is "MM/dd/yyyy".

Some of the **labelFormat** for **DateTime** data area as follows:

* 'MMM, yyyy'

* 'dd, MMM'

* 'dd/MM/yyyy'

* 'dd, hh:mm'

* 'hh:mm:ss'

* 'hh:mm:ss:tt'


{% highlight js %}


$("#rangecontainer").ejRangeNavigator({
               {   
                   // ...              
                 tooltipSettings: {
                    labelFormat:'MMM, yyyy',
                },              
                   // ...             
               });


{% endhighlight %}


{% include image.html url="/js/RangeNavigator/Concepts-and-features_images/Concepts-and-features_img20.png" Caption="Figure 25: labelFormat"%}

#### Tooltip display mode

By default the **tooltip** for RangeNavigator gets displayed. You can change this behavior using the **tooltipDisplayMode** property in the tooltip and it takes the following values.

_Table_ _1__: Tooltip values_

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
ondemand</td><td>
Tooltip get displayed only when we move the slider.</td></tr>
</table>


{% highlight js %}


$("#rangecontainer").ejRangeNavigator({
               {   
                   // ...              
                 tooltipSettings: {
                         tooltipDisplayMode: "ondemand",                    
                },              
                   // ...             
               });


{% endhighlight %}



{% include image.html url="/js/RangeNavigator/Concepts-and-features_images/Concepts-and-features_img21.png" Caption="Figure 26: Tool Tip display mode"%}
