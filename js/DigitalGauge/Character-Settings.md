---
layout: post
title: Character-Settings
description: character settings
platform: js
control: Digital Gauge
documentation: ug
api : /api/js/ejdigitalgauge
---

# Character Settings

## Appearance

The opacity of the character is adjustable with the help of **opacity** property. The space between two characters are adjusted with **spacing** property as like in the segment settings.

{% highlight html %}

<div id="DigitalGauge1"></div>

{% endhighlight %}

{% highlight javascript %}
  $(function () {
        // For Digital Gauge rendering
        $("#DigitalGauge1").ejDigitalGauge({
            width: 800,
            items: [{
                // For setting text
                value: " Syncfusion ",
                characterSettings: {
                    // For setting character opacity
                    opacity: 0.3,
                    // For setting character spacing
                    spacing: 3
                }
            }]
        })
    });

{% endhighlight %}

Execute the above code examples to render the **Digital****Gauge** as follows.

![](/js/DigitalGauge/Character-Settings_images/Character-Settings_img1.png)

## Count and Type

The number of text to be displayed can be limited by the attribute called **count**. In **Digital Gauge** five different types of characters are supported. They are as follows, 

  * EightCrossEightDotMatrix

  * SevenSegment

  * FourteenSegment

  * SixteenSegment 

  * EightCrossEightSquareMatrix.


{% highlight html %}

<div id="DigitalGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

  $(function () {
        // For Digital Gauge rendering
        $("#DigitalGauge1").ejDigitalGauge({
            width: 800,
            items: [{
                // For setting text
                value: "1234567890",
                segemntSettings: {
                    // For setting segment length
                    length: 8,
                    // For setting segment width
                    width: 1
                },
                characterSettings: {
                    // For setting character count
                    count: 10,
                    // For setting segment spacing
                    spacing: 10,

                    // For setting character type
                    type: "sevensegment",
                }
            }]
        })
    });


{% endhighlight %}

Execute the above code examples to render the **Digital****Gauge** as follows.

![](/js/DigitalGauge/Character-Settings_images/Character-Settings_img2.png)

## Text Positioning

The text in the **Digital****Gauge** is positioned with position object. This object contains two attributes such as **x** and **y.** The **x** variable positions the text in the horizontal axis and the **y** variable positions the text in the vertical axis.

{% highlight html %}

<div id="DigitalGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

  $(function () {
        // For Digital Gauge rendering
        $("#DigitalGauge1").ejDigitalGauge({
            width: 800,
            height:300,
            frame: {
                backgroundImageUrl: "Board1.jpg"
            },
            items:[{
                // For setting text
                value: "YELLOW",
                // For setting segment color
                segmentSettings: { color: "Yellow" },
                position:{
                    // For setting segment x location
                    x:80,
                    // For setting segment y location
                    y:10
                }
            }]
        });
    });


{% endhighlight %}

Execute the above code examples to render the **Digital****Gauge** as follows.


![](/js/DigitalGauge/Character-Settings_images/Character-Settings_img3.png)

## Shadow Effects

The text in the **Digital Gauge** is positioned with position object. This object contains two attributes such as **x** and **y.** The **x** variable positions the text in the horizontal axis and **y** variable positions the text in the vertical axis.

{% highlight html %}

<div id="DigitalGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

 $(function () {
        // For Digital Gauge rendering
        $("#DigitalGauge1").ejDigitalGauge({
            width: 800,
            items: [{
                //For setting Text
                value: "WELCOME",
                //For setting segment length and width
                segmentSettings: {
                    length: 3,
                    width: 3
                },
                //For setting shadow color
                shadowColor: "yellow",
                //For setting shadow Blur
                shadowBlur: 20,
                //For setting horizontal offset
                shadowOffsetX: 15,
                //For setting vertical offset
                shadowOffsetY: 15,
            }]
        });
    });

{% endhighlight %}

Execute the above code examples to render the **Digital****Gauge** as follows.

![](/js/DigitalGauge/Character-Settings_images/Character-Settings_img4.png)

