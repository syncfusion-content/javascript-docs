---
layout: post
title: Appearance
description: appearance
platform: js
control: PivotChart
documentation: ug
---

#Appearance

##Built-in Themes

Following are the built-in themes available in the PivotChart.

* flatlight
* flatdark
* gradientlight
* gradientdark
* azure
* azuredark
* lime
* limedark
* saffron
* saffrondark
* gradient-azure
* gradient-azuredark
* gradient-lime
* gradient-limedark
* gradient-saffron
* gradient-saffrondark

By using the [`theme`](/js/api/ejchart#members:theme) property, you can set the desired theme in PivotChart. By default, **“Flat Light”** theme is applied to PivotChart.

{% highlight javascript %}

    $(function()
    {
        $("#PivotChart1").ejPivotChart(
        {
            //....
            //Applying gradient theme
            theme: "gradientlight",
            //....
        });
    });
{% endhighlight %}

![](Appearance_images/BuiltInThemes.png)

##PivotChart - Area Customization

###Border Customization
To customize the PivotChart border, use [`border`](/js/api/ejchart#members:border) property in PivotChart.

{% highlight javascript %}

    $(function()
    {
        $("#PivotChart1").ejPivotChart(
        {
            //....
            //Customize the Chart border and opacity
            border:
            {
                color: "#FF0000",
                width: 5,
                opacity: 0.35
            },
            //....
        });
    });
{% endhighlight %}

![](Appearance_images/BorderCustomization.png)

###Margin Customization
The PivotChart control [`margin`](/js/api/ejchart#members:margin) property is used to add the margin to the Chart area at left, right, top and bottom position.

{% highlight javascript %}

    $(function()
    {
        $("#PivotChart1").ejPivotChart(
        {
            //....
            //Change Chart margin to left, right, top and bottom.
            margin:
            {
                left: 40,
                right: 40,
                top: 40,
                bottom: 40
            },
            //....
        });
    });
{% endhighlight %}

![](Appearance_images/MarginCustomization.png)

###Background Customization
The PivotChart control background can be customized by using the [`background`](/js/api/ejchart#members:chartarea-background) property in the Chart area.

{% highlight javascript %}

    $(function()
    {
        $("#PivotChart1").ejPivotChart(
        {
            //....
            chartArea:
            {
                //Setting background for Chart area
                background: "skyblue"
            },
            //....
        });
    });
{% endhighlight %}

![](Appearance_images/BackgroundCustomization.png)

###Grid Bands Customization
By using the [`alternateGridBand`](/js/api/ejchart#members:primaryxaxis-alternategridband) property of the axis, you can provide different color for grid rows and columns formed by the grid lines in the Chart area. The properties [`odd`](/js/api/ejchart#members:primaryyaxis-alternategridband-odd) and [`even`](/js/api/ejchart#members:primaryyaxis-alternategridband-even) are used to customize the grid bands at odd and even positions respectively.

{% highlight javascript %}

    $(function()
    {
        $("#PivotChart1").ejPivotChart(
        {
            //....
            primaryYAxis:
            {
                //....
                //Customizing horizontal grid bands at even position
                alternateGridBand:
                {
                    even:
                    {
                        fill: "#A7A9AB",
                        opacity: 0.1,
                    }
                },
                //....
            },
            //....
        });
    });
{% endhighlight %}

![](Appearance_images/GridBandsCustomization.png)

###Animation
You can enable animation by using the [`enableAnimation`](/js/api/ejchart#members:commonseriesoptions-enableanimation) property under [`commonSeriesOptions`](/js/api/ejchart#members:commonseriesoptions) of the PivotChart control. This animates the Chart series on two occasions - when the Chart is loaded for the first time and when you change the series type by using the “type” property.

{% highlight javascript %}

    $(function()
    {
        $("#PivotChart1").ejPivotChart(
        {
            ....
            commonSeriesOptions:
            {
                //Enabling animation in series
                enableAnimation: true,
                //....
            },
            //....
        });
    });
{% endhighlight %}
