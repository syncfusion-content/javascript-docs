---
layout: post
title: bullet-graph-caption
description: bullet graph caption
platform: js
control: BulletGraph	
documentation: ug
---

# Bullet Graph Caption

**Bullet Graph** supports title and **subtitle** to convey what is represented in **Bullet Graph**. They are customized using **captionSettings** property.

## Title

**Title** is set to **Bullet Graph** using **text** property in **captionSettings**. Caption settings also include properties like location, font, and textAngle for customizing the caption of **Bullet Graph**.

{% highlight js %}

**[JavaScript]**

$("#BulletGraph1").ejBulletGraph({
                    quantitativeScaleSettings: {
                        location: { x: 100, y: 200 },                   
                        minimum: 0,
                        maximum: 5,
                        interval: 0.5,
                        featureMeasures: [{ value: 4, comparativeMeasureValue: 3.5, category: "" }]
                    },
                    height: 700, width: 600,
                    captionSettings: {
                        text: "Revenue YTD",
                        textAngle: 0,
                        location: {
                            x: 10, y: 220
                        },
                        font: {
                            color: 'gray',
                            fontFamily: 'Segoe UI',
                            fontStyle: 'bold',
                            size: '14px',
                            fontWeight: 'regular',
                            opacity: 1
                        }                        
                    }
                });



{% endhighlight %}



The following screenshot displays a **Bullet Graph** with customized caption using the above code.

{% include image.html url="\js\BulletGraph\concepts-and-features\bullet-graph-caption_images\bullet-graph-caption_img1.png" Caption="Bullet Graph with title"%}

## Subtitle

**Subtitle** is added to **Bullet Braph** using **text** property of **subtitle** in **captionSettings**. **Subtitle** also provides properties like location, textAngle and font to customize subtitle similar to caption.

{% highlight js %}

**[JavaScript]**

$("#BulletGraph1").ejBulletGraph({
                    height: 700, width: 600,
                    captionSettings: {
                        subTitle: {
                            text: "Subtitle",
                            location: { x: 20, y: 225 },
                            font: {
                                    color: 'black',
                                    fontFamily: 'segoe ui',
                                    fontStyle: 'italic',
                                    size: '16px',
                                    fontWeight: 'regular',
                                    opacity: 1
                                }
                        }, 
                    }
                });


{% endhighlight %}



The following screenshot displays **Bullet Graph** with a subtitle

{% include image.html url="\js\BulletGraph\concepts-and-features\bullet-graph-caption_images\bullet-graph-caption_img2.png" Caption="Bullet Graph with subtitle"%}

## Indicator

You can add **Indicator** to bullet graph by enabling **visible** and setting **text** properties of **indicator** in **captionSettings**. Indicator is used to represent whether target is achieved or not with text and symbol by comparing current and target values in bullet graph. 

Indicator displays a symbol along with text which is different from caption and subtitle. Images like logos can be used in indicator instead of symbols. Indicator has properties such as **symbol**, **text**, **textSpacing**, **textAngle**, **location** and **font**.

{% highlight js %}

**[JS]**

$("#BulletGraph1").ejBulletGraph({
                    captionSettings: {
                        indicator: {
                            visible: true,
                            textAngle: 0,
                            location: { x: 15, y: 240 },
                            text: "+ $0.5 K",
                            textSpacing: 5,
                            symbol: {
                                color: 'green',
                                shape: 'triangle',
                                imageURL: "Column.png",
                                size: {
                                    width: 10,
                                    height: 10
                                },
                                border: {
                                    width: 1,
                                    color: 'green'
                                }
                            },
                            font: {
                                color: 'green',
                                fontFamily: 'Segoe UI',
                                fontStyle: 'Normal ',
                                size: '12px',
                                fontWeight: 'regular',
                                opacity: 1
                            },
                        }
                    }
                });


{% endhighlight %}



The following screenshot displays a bullet graph with indicator.

{% include image.html url="\js\BulletGraph\concepts-and-features\bullet-graph-caption_images\bullet-graph-caption_img3.png" Caption="Bullet Graph with indicator"%}

## Trim

The title, subtitle and indicator text can be overlapped to the scale group. You can avoid the overlapped text by using the enableTrim property of the captionSettings. The default value of the enableTrim is true. 

{% highlight js %}

**[JS]**

$("#BulletGraph1").ejBulletGraph({
      captionSettings: {
          text: 'Bullet Graph Title',
          enableTrim : true,
      }
});



{% endhighlight %}



The following screenshot displays the BulletGraph with Trim.

{% include image.html url="\js\BulletGraph\concepts-and-features\bullet-graph-caption_images\bullet-graph-caption_img4.png" Caption="Bulletgrpah with trim"%}

## Text Placement

All the caption group elements (caption, subtitle, and indicator) in the **Bullet Graph** support text positioning by using the property **textPosition** available in all caption group elements. The properties, **textAlignment** and **textAnchor** are used to customize text placement further.

**Text Position**

The property, textPosition, is used to position the text at the top, bottom, left, and right side of the quantitative scale. The default value of this property is float. By default, text can be placed at any desired location by using the location property.

{% highlight js %}

**[JS]**

            $("#BulletGraph1").ejBulletGraph({
                value: 8,
                comparativeMeasureValue: 5,
                quantitativeScaleSettings: { location: { x: 120,  y:40 }},
                height: 150,
                width: 650,
                captionSettings: {
                    text: 'Bullet Graph Title',
                    textPosition: 'top',
                    font:{
                        size: '20px',
                        fontWeight: 'bold',

                    }
                }
            });


{% endhighlight %}



The following screenshot displays the Bullet Graph with the title positioned above.

{% include image.html url="\js\BulletGraph\concepts-and-features\bullet-graph-caption_images\bullet-graph-caption_img5.png" Caption="Bullet Graph with title automatically positioned above the scale"%}

### Text Alignment

Alignment of text at different positions with respect to scale can be customized by using the **textAlignment** property. Text can be aligned in the **near**, **center,** and **far** locations of the scale. Text alignment depends upon **textPosition** property and is not applicable when the value of the **textPosition** property is **float**. The default value of the **textAlignment** property is **near**.

{% highlight js %}

**[JS]**

            $("#BulletGraph1").ejBulletGraph({
                value: 8,
                comparativeMeasureValue: 5,
                quantitativeScaleSettings: { location: { x: 120,  y:40 }},
                height: 150,
                width: 650,
                captionSettings: {
                    text: 'Revenue',
                    textPosition: 'left',
                    textAnchor: 'middle',
                    font:{
                        size: '16px',
                        fontWeight: 'bold',

                    },
                    subTitle: {
                        text: '$ in thousands',
                        textPosition: 'left',
                        textAlignment: 'center',
                        font: {
                            size: '12px',
                            fontWeight: 'bold',

                        }
                    }
                }
            });


{% endhighlight %}



The following screenshot displays the Bullet Graph with the title and subtitle at different alignments.

{% include image.html url="\js\BulletGraph\concepts-and-features\bullet-graph-caption_images\bullet-graph-caption_img6.png" Caption="Bullet graph with the title aligned at near and sub title aligned at center positions"%}

### Text Anchor

Text elements aligned at the same position are anchored by using the textAnchor property. These can be anchored at the start, middle, and end. The default value of this property is start and applicable only when two or more text elements are aligned at the same position. 

{% highlight js %}

**[JS]**

            $("#BulletGraph1").ejBulletGraph({
                value: 8,
                comparativeMeasureValue: 5,
                quantitativeScaleSettings: { location: { x: 120,  y:40 }},
                height: 150,
                width: 650,
                captionSettings: {
                    text: 'Revenue',
                    textPosition: 'left',
                    textAnchor: 'middle',
                    font:{
                        size: '16px',
                        fontWeight: 'bold',

                    },
                    subTitle: {
                        text: '$ in thousands',
                        textPosition: 'left',
                        textAlignment: 'center',
                        font: {
                            size: '12px',
                            fontWeight: 'bold',

                        }
                    }
                }
            });


{% endhighlight %}



{% include image.html url="\js\BulletGraph\concepts-and-features\bullet-graph-caption_images\bullet-graph-caption_img7.png" Caption="Bullet Graph with title text anchored at the center with respect to subtitle text"%}

### Padding

The space required between text and quantitative scale is customized by using the padding property. The default value of this property is 5 and not applicable when the value of the textPosition property is float.

{% highlight js %}

**[JS]**

$("#BulletGraph1").ejBulletGraph({
                value: 8,
                comparativeMeasureValue: 5,
                quantitativeScaleSettings: { location: { x: 120,  y:40 }},
                height: 150,
                width: 650,
                captionSettings: {
                    text: 'Profit in %',
                    textPosition: 'left',
                    textAlignment: 'center',
                    padding: 10,
                    font:{
                        size: '16px',
                        fontWeight: 'bold',

                    }
                }
            });


{% endhighlight %}



{% include image.html url="\js\BulletGraph\concepts-and-features\bullet-graph-caption_images\bullet-graph-caption_img8.png" Caption="Bullet graph with 10 pixel padding between the title text and quantitative scale"%}

