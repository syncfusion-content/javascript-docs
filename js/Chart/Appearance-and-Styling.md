---
layout: post
title: Appearance-and-Styling
description: appearance and styling
platform: js
control: Chart
documentation: ug
---

# Appearance and Styling

**Chart JS** is enriched with lots of customization options to develop high quality graphic rich Charts.

## Tooltip Template

You can customize a **tooltip** with required template by adding a **“div”** element with an **“id”** to the web page and assigning the **“id”** to the property **“template”** under **“tooltip”** as illustrated in the following code example.

{% highlight html %}

    <div id="Tooltip" style="display: none;">
        <div id="icon">
            <div id="grain"></div>
        </div>
        <div id="value">
            <div>
                <div id="efpercentage">#point.x#</div>
                <div id="ef">#point.y#</div>
            </div>
        </div>
    </div>

    <style class="cssStyles">
        .tooltipDiv {
            background-color: #C1272D !important;
            color: white;
            width: 100px;
        }

        #Tooltip > div:first-child {
            float: left;
        }

        #Tooltip #value {
            float: right;
            height: 50px;
            width: 50px;
            background-color: #C1272D;
        }

            #Tooltip #value > div {
                margin: 3px 5px 5px 5px;
            }

        #Tooltip #efpercentage {
            font-size: 12px;
            font-family: segoe ui;
            color: #E7C554;
            font-weight: bold;
        }

        #Tooltip #ef {
            font-size: 20px;
            font-family: segoe ui;
            font-weight: bold;
        }

        #grain {
            background-image: url("../images/chart/grain.png");
            height: 50px;
            width: 50px;
            background-repeat: no-repeat;
        }
    </style>
    <script type="text/javascript" language="javascript "> 


        $(function () {
            $("#container").ejChart({
                series: [{
                    points: [
                    { x: 2002, y: 1.61 }, { x: 2003, y: 2.34 }, { x: 2004, y: 2.16 }, { x: 2005, y: 2.10 }, 
                    { x: 2006, y: 1.81 }, { x: 2007, y: 2.05 }, { x: 2008, y: 2.50 },
                    { x: 2009, y: 2.22 }, { x: 2010, y: 2.21 }, { x: 2011, y: 2.00 }, { x: 2012, y: 2.27 }],
                    name: 'India',
                    tooltip:
                    {
                        visible: true,
                        template: 'Tooltip'
                    }
                }]
            });
        });

    </script>         


{% endhighlight %}



{% include image.html url="/js/Chart/Appearance-and-Styling_images/Appearance-and-Styling_img1.png" %}

## Label Template

You customize a **data label** with required template by adding a **“div”** element with an **“id”** to the web page and assigning the **“id”** to the property **“template”** under **“dataLabel”** as illustrated in the following code example.

{% highlight html %}

    <div id="template">

        <div id="left">
            <img src="../images/chart/icon_investments.png" />
        </div>
        <div id="right">
            <div id="Div2">#point.y#%</div>
        </div>
    </div>

    <style>
        #point {
            font-family: segoe ui;
            font-size: 16px;
            color: black;
        }

        #left, #right {
            float: left;
        }

        img {
            height: 25px;
            width: 30px;
        }

        #left {
            background-color: #8CC640;
        }

        #right {
            background-color: #C3C3C3;
            height: 30px;
            border-style: solid;
            border-color: #8CC640;
            border-width: 1px;
        }

        #template {
            display: none;
        }
    </style>

    <script type="text/javascript" language="javascript">
        $(function () {
            $("#container").ejChart(
                {
                    series: [{
                        points: [
                            { x: 2005, y: 28.1 }, { x: 2006, y: 29.2 },
                            { x: 2007, y: 33.9 }, { x: 2008, y: 36 },
                            { x: 2009, y: 32.4 }, { x: 2010, y: 32 },
                            { x: 2011, y: 32.8 }],
                        name: 'India',
                        marker: {
                            dataLabel: {
                                visible: true,
                                template: 'template'
                            }
                        },
                        fill: '#8CC640'
                    },
                    //....                        
                    ]
                });
        });
    </script>


{% endhighlight %}



{% include image.html url="/js/Chart/Appearance-and-Styling_images/Appearance-and-Styling_img2.png" %}

## Label Formatting

### Numerical Axis

By default, the label texts are automatically determined based on the axis data points and the generated intervals. You can make the Chart readable and understandable by formatting axes labels. For example, add "$" prefix when values are given in dollars and add "°F" postfix when values are given in Fahrenheit degrees. To achieve this “**labelFormat**” property in axis is used.

{% highlight js %}

        $("#chartcontainer").ejChart({
            // ...              
            primaryYAxis:
                 {
                     labelFormat: "{value}%",
                 }
            // ...             
        });


{% endhighlight %}



### Date time Axis

For **datetime** axis, all globalized date time formats are supported. By default, based on the interval type the **labelFormat** is calculated. When the **intervalType** is **“year”** then the **labelFormat** is **'MMM, yyyy'**.

Some of the **labelFormat** for **datetime** axis:

* 'MMM, yyyy'

* 'dd, MMM'

* 'dd/MM/yyyy'

* 'dd, hh:mm'

* 'hh:mm:ss'

* 'hh:mm:ss:tt'



{% highlight js %}

        $("#chartcontainer").ejChart({
            // ...              
            primaryXAxis:
            {
                labelFormat: 'MMM-yyyy',
                valueType: 'datetime'

            },
            // ...             
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Appearance-and-Styling_images/Appearance-and-Styling_img3.png" %}

## Title and Subtitle

**EJ Chart** provides **Title and Subtitle** support that is used to give additional information about the chart data. It also has various options to customize the font alignment of the **Title and Subtitle**. 

{% highlight js %}

       $("#chartcontainer").ejChart({
            title: {
                text: "Chart Title",
                subTitle: { text: "Subtitle" }
            }
        });


{% endhighlight %}



The following screenshot shows the **Title and Subtitle** in **Chart** control.

{% include image.html url="/js/Chart/Appearance-and-Styling_images/Appearance-and-Styling_img4.png" %}

## Chart Background and Foreground

You can customize the background for different portion of Chart.

### To Chart

Using the **background** property you can customize the background color of the Chart.

**Code**

{% highlight js %}

        $("#chartcontainer").ejChart({
            background: '#1E90FF',
            // ...             
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Appearance-and-Styling_images/Appearance-and-Styling_img5.png" %}

### To Chart Area

Using **background** property in **ChartArea** you can customize the background color of the **Chart** area.

**Code**

{% highlight js %}

        $("#chartcontainer").ejChart({
            // ...              
            chartArea: { background: '#cc3333' },
            // ...             
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Appearance-and-Styling_images/Appearance-and-Styling_img6.png" %}

### BackGround Image

JS Chart allows you to add background image for your Chart using backGroundImageUrl property.

{% highlight js %}

        $("#chartcontainer").ejChart({
            // ...              
            backGroundImageUrl: '../images/chart/wheat.png',
            // ...             
        });

{% endhighlight %}



{% include image.html url="/js/Chart/Appearance-and-Styling_images/Appearance-and-Styling_img7.png" %}

## Theme

Chart has built-in theme support. The theme configures the colors of following Chart element.

1. Fonts

2. Axis lines

3. Series color

4. Legend

5. Tooltip

6. Background



**Code**

{% highlight js %}

        $("#chartcontainer").ejChart({
            // ...              
            theme: 'gradientlight',
            // ...             
        });

{% endhighlight %}

Following predefined themes are available in **JS Chart**.

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

11. gradient-azure

12. gradient-azuredark

13. gradient-lime

14. gradient-limedark

15. gradient-saffron

16. gradient-saffrondark



{% include image.html url="/js/Chart/Appearance-and-Styling_images/Appearance-and-Styling_img8.png" %}

## Custom Color palette 

Apart from the themes, to define custom set of color you can use “**palette**” property. **Palette** customizes the color of series in the **Chart**. 

{% highlight js %}

        $("#chartcontainer").ejChart({
            // ...              
            palette: ["#69D2E7", "#E27F2D", "#6A4B82"],
            // ...             
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Appearance-and-Styling_images/Appearance-and-Styling_img9.png" %}

