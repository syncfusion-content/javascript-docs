---
layout: post
title: Quantitative-Scale
description: quantitative scale
platform: js
control: BulletGraph	
documentation: ug
api: /api/js/ejbulletgraph
---

# Quantitative Scale

The **Quantitative Scale** appearance is customized using [`quantitativeScaleSettings`](../api/ejbulletgraph#members:quantitativescalesettings) property. It has properties to [`customize labels`](../api/ejbulletgraph#members:quantitativescalesettings-labelsettings), [`major ticks`](../api/ejbulletgraph#members:quantitativescalesettings-majorticksettings), [`minor ticks`](../api/ejbulletgraph#members:quantitativescalesettings-minorticksettings), [`comparative measure`](../api/ejbulletgraph#members:quantitativescalesettings-comparativemeasuresettings) and performance measure of the bullet graph

## Range for Quantitative Scale

**Quantitative Scale** range is set using the properties [`minimum`](../api/ejbulletgraph#members:quantitativescalesettings-minimum), [`maximum`](../api/ejbulletgraph#members:quantitativescalesettings-maximum) and [`interval`](../api/ejbulletgraph#members:quantitativescalesettings-interval) of **quantitativeScaleSettings** property. **Minimum** specifies the start range of the scale, **maximum** specifies the end range of scale and **interval** specifies the number of intervals between start and end range. Default values of **minimum**, **maximum** and **interval** are 0, 10 and 1 respectively. The number of minor ticks (ticks between intervals) are specified using [`minorTicksPerInterval`](../api/ejbulletgraph#members:quantitativescalesettings-minorticksperinterval) property.

{% highlight javascript %}



$("#BulletGraph1").ejBulletGraph({
                    quantitativeScaleSettings: {                      
                        minimum: 0,
                        maximum: 10,
                        interval: 1,
                        minorTicksPerInterval: 4
                    },
                });


{% endhighlight %}



The following screenshot displays a **Bullet Graph** with start range 0, end range 10 and interval 1 with 4 minor ticks per interval

![](/js/BulletGraph/Quantitative-Scale_images/Quantitative-Scale_img1.png) 

## Quantitative scale location

Bullet Graph does not position Quantitative scale automatically based on its size or space required for caption text, etc. By default Quantitative scale is positioned at 10 pixels from left and 10 pixels from top. Quantitative scale location is customized as per the requirement using the [`location`](../api/ejbulletgraph#members:quantitativescalesettings-location) property available in quantitativeScaleSettings. Using the this property you can set [`X`](../api/ejbulletgraph#members:quantitativescalesettings-location-x) and [`Y`](../api/ejbulletgraph#members:quantitativescalesettings-location-y) location of the quantitative scale.

{% highlight javascript %}



$("#BulletGraph1").ejBulletGraph({
                    quantitativeScaleSettings: {                      
                        location: { x: 20, y: 20 }
                    },
                });


{% endhighlight %}

The following screenshot displays **Bullet Graph** with Quantitative scale at 20 pixels from left and 20 pixels from top

![](/js/BulletGraph/Quantitative-Scale_images/Quantitative-Scale_img2.png) 

## Major ticks

Color, size and width of **Major tick** lines are customized using [`major tick settings`](../api/ejbulletgraph#members:quantitativescalesettings:majorticksettings) property in **quantitativeScaleSettings**. Default value of [`size`](../api/ejbulletgraph#members:quantitativescalesettings-majorticksettings-size) and [`width`](../api/ejbulletgraph#members:quantitativescalesettings-majorticksettings-width) properties are 13 and 2 respectively. **Ticks** are drawn in black color by default. The property **size** represents the height of **tick** lines and **width** represents the width of **tick** lines and **ticks** color are customized using [`stroke`](../api/ejbulletgraph#members:quantitativescalesettings-majorticksettings-stroke) property.

{% highlight javascript %}



$("#BulletGraph1").ejBulletGraph({
                    quantitativeScaleSettings: {                      
                        majorTickSettings: {
                            size: 15,
                            width: 3,
                            stroke: 'gray'
                        }
                    },
                });


{% endhighlight %}



The following screenshot displays **Major ticks** in **gray** color with a width of 3 pixels and height 15 pixels.

![](/js/BulletGraph/Quantitative-Scale_images/Quantitative-Scale_img3.png) 

## Minor ticks

[`Minor ticks`](../api/ejbulletgraph#members:quantitativescalesettings-minorticksettings) can also be customized similar to major ticks. The properties [`stroke`](../api/ejbulletgraph#members:quantitativescalesettings-minorticksettings-stroke), [`width`](../api/ejbulletgraph#members:quantitativescalesettings-minorticksettings-width) and [`size`](../api/ejbulletgraph#members:quantitativescalesettings-minorticksettings-size) of minorTickSettings are used to customize Minor ticks in quantitative scale. Stroke specifies the color of ticks, width specifies the width of ticks and size specifies the height of the ticks.

{% highlight javascript %}



$("#BulletGraph1").ejBulletGraph({
                    quantitativeScaleSettings: {                      
                        minorTickSettings: {
                            size: 7,
                            width: 3,
                            stroke: 'gray'
                        }
                    },
                });


{% endhighlight %}



The following screenshot displays **Bullet Graph** with customized **Minor ticks** in quantitative scale

![](/js/BulletGraph/Quantitative-Scale_images/Quantitative-Scale_img4.png) 

## Tick position

**Ticks** are positioned below, above or inside the quantitative scale. By default **ticks** are positioned below the quantitative scale. The [`tickPosition`](../api/ejbulletgraph#members:quantitativescalesettings-tickposition) property is used to customize the position of ticks in quantitative scale. **Ticks** can be placed inside the quantitative scale by setting **tickPosition** to **cross**.

{% highlight javascript %}



$("#BulletGraph1").ejBulletGraph({
                    quantitativeScaleSettings: {                      
                        tickPosition: 'above'
                    },
                });


{% endhighlight %}



The following screenshot displays **Bullet Graph** with ticks positioned above quantitative scale

![](/js/BulletGraph/Quantitative-Scale_images/Quantitative-Scale_img5.png) 

## Tick Placement

**Quantitative****scale****ticks** can be placed either inside or outside the scale using [`tick placement`](../api/ejbulletgraph#members:quantitativescalesettings-tickplacement) property. By default ticks are placed outside the scale.



{% highlight javascript %}



$("#BulletGraph1").ejBulletGraph({
                value: 8,
                comparativeMeasureValue: 5,                
                qualitativeRangeSize: 50,
                quantitativeScaleSettings: {
                    location: { x: 108, y: 10 },
                    tickPlacement: 'inside',
                    labelSettings: { offset: 5, size: 10, labelPrefix: '$',                                                                              labelSuffix: ' K' },
                },
                captionSettings: {
                    textAngle: 0, location: { x: 17, y: 28 }, text: "Revenue YTD",
                    subTitle: {
                        textAngle: 0,
                        text: "$ in Thousands", location: { x: 10, y: 42 }
                        }
                    }
                });


{% endhighlight %}



The following screenshot displays **Bullet Graph** ticks inside **Quantitative Scale**

![](/js/BulletGraph/Quantitative-Scale_images/Quantitative-Scale_img6.png) 

## Quantitative scale labels

**Quantitative****scale****labels** are customized with prefix, suffix, font, color and size using **labelSettings** property. Following customization options are available in **labelSettings**.

* You can place the label inside or outside of the bullet graph using [`label placement`](../api/ejbulletgraph#members:quantitativescalesettings-labelsettings-labelplacement) property.

* Prefix and suffix to the label is added with [`label prefix`](../api/ejbulletgraph#members:quantitativescalesettings-labelsettings-labelprefix) and [`label suffix`](../api/ejbulletgraph#members:quantitativescalesettings-labelsettings-labelsuffix) property.

* You can specify the horizontal or vertical padding of the labels using [`offset`](../api/ejbulletgraph#members:quantitativescalesettings-labelsettings-offset) property.

* You can position the label either above or below the bulletgraph by using [`position`](../api/ejbulletgraph#members:quantitativescalesettings-labelsettings-position) property.

* To specify the size of the label text, you can use [`size`](../api/ejbulletgraph#members:quantitativescalesettings-labelsettings-size) property.

* You can customize the color the labels using [`stroke`](../api/ejbulletgraph#members:quantitativescalesettings-labelsettings-stroke) property.

* Using [`font`](../api/ejbulletgraph#members:quantitativescalesettings-labelsettings-font) option in the label settings, you can customize the [`font family`](../api/ejbulletgraph#members:quantitativescalesettings-labelsettings-font-fontfamily), [`font style`](../api/ejbulletgraph#members:quantitativescalesettings-labelsettings-font-fontstyle), [`font weight`](../api/ejbulletgraph#members:quantitativescalesettings-labelsettings-font-fontweight) and [`opacity`](../api/ejbulletgraph#members:quantitativescalesettings-labelsettings-font-opacity) of the label text.

{% highlight javascript %}



$("#BulletGraph1").ejBulletGraph({
                    quantitativeScaleSettings: {                      
                        labelSettings: {
                            stroke: 'blue',
                            labelPrefix: '$',
                            labelSuffix: 'K',

                            font: {
                                fontFamily: 'Segoe UI',
                                fontStyle: 'bold',
                                fontWeight: 'regular',
                                opacity: 0.8
                            },
                            size: 12,
                            offset: 15
                        }
                    },
                });


{% endhighlight %}



The following screenshot displays **Bullet Graph** labels in blue color

![](/js/BulletGraph/Quantitative-Scale_images/Quantitative-Scale_img7.png) 

## Label Placement

**Quantitative****scale****labels** can be placed either inside or outside the scale using “**labelPlacement**” property. By default labels are placed 15 pixels outside the scale.

{% highlight javascript %}



$("#BulletGraph1").ejBulletGraph({
                value: 8,
                comparativeMeasureValue: 5,                                
                qualitativeRangeSize: 50,
                quantitativeScaleSettings: {
                    location: { x: 108, y: 10 },
                    labelSettings: {
                        offset: 5, size: 10, labelPrefix: '$', labelSuffix:            ' K', font: { fontWeight: 'bold' },
                        labelPlacement: 'inside'
                    },
                },
                captionSettings: {
                    textAngle: 0, location: { x: 17, y: 28 }, text: "Revenue YTD",
                    subTitle: {
                        textAngle: 0,
                        text: "$ in Thousands", location: { x: 10, y: 42 }
                    }
                }                
           });


{% endhighlight %}



The following screenshot displays **Bullet Graph** labels inside **Quantitative Scale.**

![](/js/BulletGraph/Quantitative-Scale_images/Quantitative-Scale_img8.png) 

## Performance measure bar

Performance measure bar is customized using [`featuredMeasureSettings`](../api/ejbulletgraph#members:quantitativescalesettings-featuredmeasuresettings) in quantitativeScaleSettings property. Color of the bar is customized using [`stroke`](../api/ejbulletgraph#members:quantitativescalesettings-featuredmeasuresettings-stroke) property and [`width`](../api/ejbulletgraph#members:quantitativescalesettings-featuredmeasuresettings-width) using width property. By default bar is drawn in black color with 6 pixels of width.

{% highlight javascript %}



$("#BulletGraph1").ejBulletGraph({
                    value: 5,
                    quantitativeScaleSettings: {                      
                        featuredMeasureSettings: {
                            stroke: 'blue',
                            width: 4
                        },
                    },
                });


{% endhighlight %}



The following screenshot displays **Bullet Graph** with customized **Performance measure bar**.

![](/js/BulletGraph/Quantitative-Scale_images/Quantitative-Scale_img9.png) 

## Comparative measure symbol

Comparative symbol color and width are customized using [`comparativeMeasureSettings`](../api/ejbulletgraph#members:quantitativescalesettings-comparativemeasuresettings) through quantitativeScaleSettings property. Color of the symbol is customized using [`stroke`](../api/ejbulletgraph#members:quantitativescalesettings-comparativemeasuresettings-stroke) property and width using [`width`](../api/ejbulletgraph#members:quantitativescalesettings-comparativemeasuresettings-width) property. By default Comparative measure symbol is displayed in black color with a width of 5 pixels.

{% highlight javascript %}



$("#BulletGraph1").ejBulletGraph({
                    comparativeMeasureValue: 5,
                    quantitativeScaleSettings: {                      
                        comparativeMeasureSettings: {
                            stroke: 'blue',
                            width: 5
                        },
                    },
                });


{% endhighlight %}



The following screenshot displays **Bullet Graph** with customized **Comparative measure value**.

![](/js/BulletGraph/Quantitative-Scale_images/Quantitative-Scale_img10.png) 

## Multiple performance measures comparison

**Bullet Graph** supports comparing more than one performance at a time, given that all the comparisons are related using [`featureMeasure`](../api/ejbulletgraph#members:quantitativescalesettings-featuremeasures) in **quantitativeScaleSettings** property. In feature measures, you can specify [`category`](../api/ejbulletgraph#members:quantitativescalesettings-featuremeasures-category), [`comparative measure value`](../api/ejbulletgraph#members:quantitativescalesettings-featuremeasures-comparativemeasurevalue) and [`value`](../api/ejbulletgraph#members:quantitativescalesettings-featuremeasures-value) properties that are used to comparing performance.

{% highlight javascript %}



$("#BulletGraph1").ejBulletGraph({
                    qualitativeRangeSize: 60,
                    height: 120,
                    quantitativeScaleSettings: {
                        featureMeasures: [
                            { value: 6, comparativeMeasureValue: 3, category: 2010 },
                            { value: 9, comparativeMeasureValue: 6, category: 2011 },
                            { value: 5, comparativeMeasureValue: 5, category: 2012 },
                        ]
                    }
                });


{% endhighlight %}



The following screenshot displays **Bullet Graph** that compares 3 related performance measures.

![](/js/BulletGraph/Quantitative-Scale_images/Quantitative-Scale_img11.png) 

