---
layout: post
title: Appearance
description: appearance
platform: js
control: PivotChart
documentation: ug
api: /api/js/ejpivotchart
---

# Appearance

## Built-in Themes

Following are the built-in themes available in the PivotChart.

* flatlight
* gradientlight
* gradientdark
* azure
* azuredark
* lime
* limedark
* saffron
* saffrondark
* gradientlight
* gradientdark
* highcontrast01
* highcontrast02
* material
* office365
* bootstrap


By using the [`theme`](/api/js/ejchart#members:theme) property, you can set the desired theme in PivotChart. By default, **“Flat Light”** theme is applied to PivotChart.

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

## PivotChart - Area Customization

### Border Customization
To customize the PivotChart border, use [`border`](/api/js/ejchart#members:border) property in PivotChart.

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

### Margin Customization
The PivotChart control [`margin`](/api/js/ejchart#members:margin) property is used to add the margin to the Chart area at left, right, top and bottom position.

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

### Background Customization
The PivotChart control background can be customized by using the [`background`](/api/js/ejchart#members:chartarea-background) property in the Chart area.

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

### Grid Bands Customization
By using the [`alternateGridBand`](/api/js/ejchart#members:primaryxaxis-alternategridband) property of the axis, you can provide different color for grid rows and columns formed by the grid lines in the Chart area. The properties [`odd`](/api/js/ejchart#members:primaryyaxis-alternategridband-odd) and [`even`](/api/js/ejchart#members:primaryyaxis-alternategridband-even) are used to customize the grid bands at odd and even positions respectively.

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

### Animation
You can enable animation by using the [`enableAnimation`](/api/js/ejchart#members:commonseriesoptions-enableanimation) property under [`commonSeriesOptions`](/api/js/ejchart#members:commonseriesoptions) of the PivotChart control. This animates the Chart series on two occasions - when the Chart is loaded for the first time and when you change the series type by using the “type” property.

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
