---
layout: post
title: Behavior-Customization
description: behavior customization
platform: js
control: Chart
documentation: ug
---

# Behavior Customization

Essential JavaScript Chart allows you to customize the Chart through events. For example, you can add custom marker for highest and lowest data point using the events.

## Select a point

You can acquire the information related to a particular data point of series by moving mouse over the point or by clicking the point using **pointRegionMouseMove** or **pointRegionClick** event.  **pointRegionMouseMove** event gets triggered when you move the mouse over the point and the **pointRegionClick** event gets triggered when you click the point. The following code example illustrates that x and y values of a point gets displayed when you move the mouse over the point or click the point.

{% highlight js %}

        $("#chartcontainer").ejChart({   
            // ...             
            commonSeriesOptions: {type:'column'},
            pointRegionMouseMove: "pointDetails",
            pointRegionClick: " pointDetails ",
            size: {width:800, height:600}
        });
        function pointDetails(sender) {
            series = sender.model.series[sender.data.region.SeriesIndex];
            var X = series.points[sender.data.region.Region.PointIndex].x;
            var Y = series.points[sender.data.region.Region.PointIndex].y;
            alert("X:" + X + "  Y:" + Y);
        }        


{% endhighlight %}



{% include image.html url="/js/Chart/Behaviour-Customization_images/Behaviour-Customization_img1.png" %}

## Handle Events

### Chart Events

**load**: function

This event is handled when the Chart gets loaded; a parameter **sender** is passed to the handler. Using **sender.model**, you can access the **Chart** properties except series that were passed to the **ejchart**. 

{% highlight js %}

        $("#chartcontainer").ejChart({   
            // ...             
            load: function (sender) {
                sender.model.canResize = false;
            },
        });         


{% endhighlight %}



**preRender**: function

This event is handled before the Chart gets rendered; a parameter **sender** is passed to the handler. Using **sender.model**, you can access the Chart properties that were passed to the **ejChart**. 

{% highlight js %}

        $("#chartcontainer").ejChart({
            // ...             
            preRender: function (sender) {
                console.log(sender.model.series.length);
            },
        });         


{% endhighlight %}



**titleRendering**: function

This event is handled before the Chart title gets rendered; a parameter **sender** is passed to the handler. Using **sender.data.title**, you can change the title of the Chart after the Chart is loaded.

{% highlight js %}


        $("#chartcontainer").ejChart({   
            // ...             
            titleRendering: function (sender) {
                sender.data.title = "Olympic";
            },
        });         


{% endhighlight %}



**ChartAxis Events**

**axesLabelsInitialize: function**

This event is handled before the Chart axis gets rendered; a parameter sender is passed to the handler. Using sender.data.axes, you can change the axis related properties after the Chart is loaded.

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
            axesLabelsInitialize: function (sender) {
                sender.data.axes[0].orientation = "horizontal";
            },
        });         


{% endhighlight %}



**axesRangeCalculate**: function

This event is handled after the Chart axis range gets calculated; a parameter sender is passed to the handler. Using sender.data.range, you can change the range calculated for the Chart axis.

{% highlight js %}


        $("#chartcontainer").ejChart({   
            // ...             
            axesRangeCalculate: function (sender) {
                sender.data.range.min = 2;
            },       
        });


{% endhighlight %}

**axesTitleRendering**: function

This event is handled before the Chart axis title gets rendered; a parameter sender is passed to the handler. Using sender.data.Title, you can change the axis title after the Chart is loaded.

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
            axesTitleRendering: function (sender) {
                sender.data.title = "Countries";
            },
        });         


{% endhighlight %}



**axesLabelRendering**: function

This event is handled before the Chart axis label gets rendered; a parameter sender is passed to the handler. Using sender.data.label.Text, you can change the axis labels after the Chart is loaded.

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
            axesLabelRendering: function (sender) {
                sender.data.label.Text = "Label1";
            },
        });         


{% endhighlight %}



### Series Events

**seriesRendering**: function

This event is handled before the Chart series gets rendered; a parameter sender is passed to the handler. Using sender.data.series, you can get access to the series properties.

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
            seriesRendering: function (sender) {
                sender.data.series.name = "horizontal";
            },
        });         


{% endhighlight %}



**symbolRendering**: function

This event is handled before the marker of each series point gets rendered; a parameter sender is passed to the handler. Using sender.data you can get access style and location of the symbol.

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
            symbolRendering: function (sender) {
                console.log(sender.data.style.PointIndex);
            },
        });         


{% endhighlight %}



**displayTextRendering**: function

This event is handled before the dataLabel of each series points gets rendered; a parameter sender is passed to the handler. Using sender.data.text you can change the dataLabel of each point in the series.

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
            displayTextRendering: function (sender) {
                sender.data.text = "34";
            },
        });         


{% endhighlight %}



**animationComplete**: function

This event is handled after the series animation is completed; a parameter sender is passed to the handler.  

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
            animationComplete: function (sender) {
                console.log(sender.data.series.name);
            },
        });         


{% endhighlight %}



### Legend Events

**legendItemRendering**: function

This event is handled before the legend of each series points gets rendered; a parameter sender is passed to the handler. Using sender.data.legendItem.Text you can change the text of each legend text.

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
            legendItemRendering: function (sender) {
                sender.data.legendItem.Text = "Series1"
            },
        });         


{% endhighlight %}



**legendItemClick**: function

This event is handled when you click the legend item; a parameter sender is passed to the handler.  

{% highlight js %}


        $("#chartcontainer").ejChart({   
            // ...             
            legendItemClick: function (sender) {
                console.log("Legend Item Click")
            },
        });         


{% endhighlight %}



**legendItemMouseMove**: function

This event is handled when you move the mouse over the legend item; a parameter sender is passed to the handler. Using sender.data.legendItem.Text you can change the text of each legend text.

{% highlight js %}


        $("#chartcontainer").ejChart({   
            // ...             
            legendItemMouseMove: function (sender) {
                console.log("Legend Item Click")
            },
        });         


{% endhighlight %}



**lengendBoundsCalculate**: function

This event is handled after the bounds for legend is calculated.  A parameter sender is passed to the handler.  Using sender.data.legendBound, you can access the bounds of the Chart legend.

{% highlight js %}


        $("#chartcontainer").ejChart({   
            // ...             
            legendBoundsCalculate: function (sender) {
                sender.data.legendBound.Height = 34;
            },
        });     


{% endhighlight %}



### Tooltip Events

**toolTipInitialize**: function

This event is handled before the tooltip gets rendered.  A parameter sender is passed to the handler.  Using sender.data.currentText, you can change the tooltip text.

{% highlight js %}


        $("#chartcontainer").ejChart({   
            // ...             
            toolTipInitialize: function (sender) {
                sender.data.currentText="tooltip"
            },
        });         


{% endhighlight %}



**trackAxisToolTip**: function

This event is handled before the tooltip for axis gets rendered when crosshair is enabled.  A parameter sender is passed to the handler.  Using sender.data.currentTrackText, you can change the tooltip text.

{% highlight js %}


        $("#chartcontainer").ejChart({   
            // ...             
            trackAxisToolTip: function (sender) {                                
                sender.data.currentTrackText="tooltip"
            },
        });         


{% endhighlight %}



**trackToolTip**: function

This event is handled before the tooltip for trackball get rendered when trackball is enabled.  A parameter sender is passed to the handler.  Using sender.data.currentText, you can change the tooltip text.

{% highlight js %}


        $("#chartcontainer").ejChart({   
            // ...             
            trackToolTip: function (sender) {
                sender.data.currentText = "tooltip"
            },
        });         


{% endhighlight %}



