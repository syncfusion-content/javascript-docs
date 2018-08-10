---
layout: post
title: Appearance-And-Styling
description: Appearance And Styling
platform: js
control: RangeNavigator
documentation: ug
api: /api/js/ejrangenavigator
---

### Appearance and Styling

**JavaScript RangeNavigator** is enriched with lots of customization options for labels, gridlines and slider to develop high quality graphic rich control.

#### Customize labels

The labels are found along the range, displaying the value of the data it correspond, both on (higher level label) and below (lower level label) the **RangeNavigator**. **RangeNavigator** labels are further customized using higher level label [`style`](../api/ejrangenavigator#members:labelsettings-higherlevel-style) and lower level label [`style`](../api/ejrangenavigator#members:labelsettings-lowerlevel-style) property of [`font`](../api/ejrangenavigator#members:labelsettings-style-font),[`color`](../api/ejrangenavigator#members:labelsettings-style-font-color),[`fontFamily`](../api/ejrangenavigator#members:labelsettings-style-font-family),[`fontStyle`](../api/ejrangenavigator#members:labelsettings-style-font-style),[`fontWeight`](../api/ejrangenavigator#members:labelsettings-style-font-weight),[`opacity`](../api/ejrangenavigator#members:labelsettings-style-font-opacity) and [`size`](../api/ejrangenavigator#members:labelsettings-style-font-size) property in [`labelSettings`](../api/ejrangenavigator#members:labelsettings). 

The higher level labels [`font`](../api/ejrangenavigator#members:labelsettings-higherlevel-style-font), [`color`](../api/ejrangenavigator#members:labelsettings-higherlevel-style-font-color), [`fontFamily`](../api/ejrangenavigator#members:labelsettings-higherlevel-style-font-fontfamily), [`fontStyle`](../api/ejrangenavigator#members:labelsettings-higherlevel-style-font-fontstyle), [`fontWeight`](../api/ejrangenavigator#members:labelsettings-higherlevel-style-font-fontweight), [`opacity`](../api/ejrangenavigator#members:labelsettings-higherlevel-style-font-opacity) and [`size`](../api/ejrangenavigator#members:labelsettings-higherlevel-style-font-size) can be customized using [`higherLevel`](../api/ejrangenavigator#members:labelsettings-higherlevel) property.

The lower level labels [`font`](../api/ejrangenavigator#members:labelsettings-lowerlevel-style-font) [`color`](../api/ejrangenavigator#members:labelsettings-lowerlevel-style-font-color), [`fontFamily`](../api/ejrangenavigator#members:labelsettings-lowerlevel-style-font-fontfamily), [`fontStyle`](../api/ejrangenavigator#members:labelsettings-lowerlevel-style-font-fontstyle), [`fontWeight`](../api/ejrangenavigator#members:labelsettings-lowerlevel-style-font-fontweight), [`opacity`](../api/ejrangenavigator#members:labelsettings-lowerlevel-style-font-opacity) and [`size`](../api/ejrangenavigator#members:labelsettings-lowerlevel-style-font-size) can be customized using [`lowerLevel`](../api/ejrangenavigator#members:labelsettings-lowerlevel) property.

{% highlight javascript %}

        $("#container").ejRangeNavigator({
        // ...             
        labelSettings: {
            // customizing higher level labels.
            higherLevel: {
                style: {
                    font: {
                        color: '#ff0000',
                        style: 'Normal',
                        size: '12px',
                        opacity: 1,
                        weight: 'regular'
                    },
        
                },
            },
            // customizing lower level labels.
            lowerLevel: {
                style: {
                    font: {
                        color: '#ff0000',
                        style: 'Normal',
                        size: '12px',
                        opacity: 1,
                        weight: 'regular'
                    },
                },
            }
        },
        // ...             
        
        });
        });

{% endhighlight %}

![](/js/RangeNavigator/Appearance-And-Styling_images/Appearance-And-Styling_img1.png) 


##### Label Placement

Labels in **RangeNavigator** are placed inside or outside of the control. You can customize both the higher and lower level labels using [`labelPlacement`](../api/ejrangenavigator#members:labelsettings-higherlevel-labelplacement) property in label setting of **labelPlacement**. By default **labelPlacement** is "outside" for the both higher and lower level labels.

The following screen shot illustrates both the lower and higher level labels that are placed outside the control with [`labelPlacement`](../api/ejrangenavigator#members:labelsettings-lowerlevel-labelplacement) specified as outside.

{% highlight javascript %}

        $("#container").ejRangeNavigator({
        // ...             
        labelSettings: {
            higherLevel: {
                labelPlacement: "inside",
            },
            lowerLevel: {
                labelPlacement: "inside"
            }
        },
        // ...             
        
        });
        });

{% endhighlight %}


The following screenshot illustrates a **RangeNavigator** with labels inside the control after specifying the labelPlacement as inside.



![](/js/RangeNavigator/Appearance-And-Styling_images/Appearance-And-Styling_img2.png) 

##### Label intersection

The labels will overlap with each other when they are large in size. You can avoid overlapping using the [`labelIntersectAction`](../api/ejrangenavigator#members:labelsettings-higherlevel-labelintersectaction) property. The default value of the [`labelIntersectAction`](../api/ejrangenavigator#members:labelsettings-higherlevel-labelintersectaction) is **none**; another available value of the this property is **hide**.

{% highlight javascript %}

        $("#container").ejRangeNavigator({
        // ...             
        labelSettings: {
            higherLevel: {
                labelIntersectAction: "hide",
            },
            lowerLevel: {
                labelIntersectAction: "hide"
            }
        },
        // ...             
        
        });
        });

{% endhighlight %}


#### Customize RangeNavigator

##### Customize NavigatorStyleSettings
RangeNavigator is customized using [`navigatorStyleSettings`](../api/ejrangenavigator#members:navigatorstylesettings) properties. You can customize the selected and unselected region color, opacity using [`selectedRegionColor`](../api/ejrangenavigator#members:navigatorstylesettings-selectedregioncolor) and [`unselectedRegionColor`](../api/ejrangenavigator#members:navigatorstylesettings-unselectedregioncolor), [`selectedRegionOpacity`](../api/ejrangenavigator#members:navigatorstylesettings-selectedregionopacity) and [`unselectedRegionOpacity `](../api/ejrangenavigator#members:navigatorstylesettings-unselectedregionopacity) in **NavigatorStyleSettings** and the thumb of the slider using [`thumbColor`](../api/ejrangenavigator#members:navigatorstylesettings-thumbcolor), [`thumbRadius`](../api/ejrangenavigator#members:navigatorstylesettings-thumbradius) and [`thumbStroke`](../api/ejrangenavigator#members:navigatorstylesettings-thumbstroke) in **NavigatorStyleSettings**.  [`majorGridLineStyle`](../api/ejrangenavigator#members:navigatorstylesettings-majorgridlinestyle) and [`minorGridLineStyle`](../api/ejrangenavigator#members:navigatorstylesettings-minorgridlinestyle) are used to customize the major grid line [`color`](../api/ejrangenavigator#members:navigatorstylesettings-majorgridlinestyle-color), [`visible`](../api/ejrangenavigator#members:navigatorstylesettings-majorgridlinestyle-visible) property and minor gridline [`color`](../api/ejrangenavigator#members:navigatorstylesettings-minorgridlinestyle-color) and [`visible`](../api/ejrangenavigator#members:navigatorstylesettings-minorgridlinestyle-visible).

You can customize the [`background`](../api/ejrangenavigator#members:navigatorstylesettings-background), [`opacity`](../api/ejrangenavigator#members:navigatorstylesettings-opacity) and [`border`](../api/ejrangenavigator#members:navigatorstylesettings-border) [`color`](../api/ejrangenavigator#members:navigatorstylesettings-border-color), [`dashArray`](../api/ejrangenavigator#members:navigatorstylesettings-border-dasharray) and [`width`](../api/ejrangenavigator#members:navigatorstylesettings-border-width) of navigatorStyleSettings.

##### Customize Labels
The visibility of labels are enabled by setting [`visible`](../api/ejrangenavigator#members:labelsettings-higherlevel-visible) in higher level and [`visible`](../api/ejrangenavigator#members:labelsettings-lowerlevel-visible) in lower level. The labels can be [`aligned`](../api/ejrangenavigator#members:labelsettings-style-horizontalalignment) by specifying [`horizontalAlignment`](../api/ejrangenavigator#members:labelsettings-higherlevel-style-horizontalalignment) of higher level style and [`horizontalAlignment`](../api/ejrangenavigator#members:labelsettings-lowerlevel-style-horizontalalignment) of lower level [`style`](../api/ejrangenavigator#members:labelsettings-style). 

You can customize the [`border`](../api/ejrangenavigator#members:labelsettings-higherlevel-border) [`color`](../api/ejrangenavigator#members:labelsettings-higherlevel-border-color) and [`width`](../api/ejrangenavigator#members:labelsettings-higherlevel-border-width), [`fill`](../api/ejrangenavigator#members:labelsettings-higherlevel-fill), [`gridLineStyle`](../api/ejrangenavigator#members:labelsettings-higherlevel-gridlinestyle) [`color`](../api/ejrangenavigator#members:labelsettings-higherlevel-gridlinestyle-color), [`dashArray`](../api/ejrangenavigator#members:labelsettings-higherlevel-gridlinestyle-dasharray) and [`width`](../api/ejrangenavigator#members:labelsettings-higherlevel-gridlinestyle-width), [`position`](../api/ejrangenavigator#members:labelsettings-higherlevel-position) property of higher level labels in labelSettings. 

You can also customize the [`border`](../api/ejrangenavigator#members:labelsettings-lowerlevel-border) [`color`](../api/ejrangenavigator#members:labelsettings-lowerlevel-border-color) and [`width`](../api/ejrangenavigator#members:labelsettings-lowerlevel-border-width), [`fill`](../api/ejrangenavigator#members:labelsettings-lowerlevel-fill), [`gridLineStyle`](../api/ejrangenavigator#members:labelsettings-lowerlevel-gridlinestyle) [`color`](../api/ejrangenavigator#members:labelsettings-lowerlevel-gridlinestyle-color), [`dashArray`](../api/ejrangenavigator#members:labelsettings-lowerlevel-gridlinestyle-dasharray) and [`width`](../api/ejrangenavigator#members:labelsettings-lowerlevel-gridlinestyle-width), [`position`](../api/ejrangenavigator#members:labelsettings-lowerlevel-position) property for lower level labels of labelSettings. 

{% highlight javascript %}

        $("#container").ejRangeNavigator({
        // ...    
        //  To customize the navigator element     
        navigatorStyleSettings: {
        
            unselectedRegionColor: "white",
            selectedRegionColor: "#5EABDE",
            thumbColor: "white",
            thumbRadius: 10,
            thumbStroke: "#303030",
            background: "transparent",
            opacity : 0.3,
            border: {
                color: "black",
                width: 3
            },
            majorGridLineStyle: {
                color: "transparent"
            },
            minorGridLineStyle: {
                color: "transparent"
            }
        },
        //  To customize the labels
        labelSettings: {
        
            higherLevel: {
                visible: true,
                border :{color:"#ff0000", width: 1},
                gridLineStyle :{color:"#ff0000", dashArray:"20 10 5", width: 1},
                style: {
                    font: {
                        color: 'black',
                        size: '13px',
                        opacity: 1
                    },
                    horizontalAlignment: "left"
                },
                intervalType: 'years',
                labelPlacement: "inside"
            },
            lowerLevel: {
                visible: true,
                border :{color:"#ff0000", width: 1},
                gridLineStyle :{color:"#ff0000", dashArray:"20 10 5", width: 1},
                style: {
                    font: {
                        color: 'black',
                        size: '12px',
                        opacity: 1
                    },
                    horizontalAlignment: "center"
                },
                intervalType: 'quarters',
                labelPlacement: "inside"
            }
        },
        
        // ...             
        
        });
        });


{% endhighlight %}



![](/js/RangeNavigator/Appearance-And-Styling_images/Appearance-And-Styling_img3.png) 

#### Themes

**RangeNavigator** [`theme`](../api/ejrangenavigator#members:theme) is a set of pre-defined options that are applied to the control before each **RangeNavigator** is instantiated. Following predefined themes are available in JavaScript **RangeNavigator**.

1. flatlight
2. flatdark
3. gradientlight 
4. gradientdark 
5. azure                      
6. azuredark               
7. lime 
8. limedark
9. saffron
10. saffrondark
11. gradientazure
12. gradientazuredark
13. gradientlime
14. gradientlimedark
15. gradientsaffron
16. gradientsaffrondark

{% highlight javascript %}


               $("#container").ejRangeNavigator(
               {   
                   // ...              
                      theme: 'azuredark',
                   // ...             
               });


{% endhighlight %}



![](/js/RangeNavigator/Appearance-And-Styling_images/Appearance-And-Styling_img4.png) 
