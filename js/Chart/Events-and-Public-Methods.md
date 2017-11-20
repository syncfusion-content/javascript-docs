---
layout: post
title: Events and Public Methods 
description: How to use the events and public methods in Chart
platform: js
control: Chart
documentation: ug
api : /api/js/ejchart
---

# Methods and Events

## Public Methods

### Redraw the chart

The [`redraw`](../api/ejchart#methods:redraw) method is used for redrawing the entire chart. You can call this method whenever you update, add or remove points from the data source or whenever you want to refresh the UI.

{% highlight javascript %}

   // Redraw Chart
var chartObj = $("#container").data("ejChart");
chartObj.redraw();

 //other way of using redraw method
$("#container").ejChart("redraw");


{% endhighlight %}

### Animating the chart

The [`animate`](../api/ejchart#methods:animate) method animates the series and/or indicators in Chart. When parameter is not passed to this method, then all the series and indicators present in Chart are animated.

{% highlight javascript %}

var chartObj  = $("#container").data("ejChart");
//animating series array
chartObj.animate(chartObj.model.series);

{% endhighlight %}

## Events

### Annotation Click

The [`annotationClick`](../api/ejchart#events:annotationclick) event is triggered while clicking the annotation

{% highlight javascript %}

//annotationClick event for chart

$("#container").ejChart({

    annotationClick: function (args) {
              //Do something
    }
   
});

{% endhighlight %}


### Animation Complete

The [`animationComplete`](../api/ejchart#events:animationcomplete) event is triggered after the series animation is completed.
This event will be triggered for each series when the animation is enabled.

{% highlight javascript %}

//animationComplete event for chart

$("#container").ejChart({

     animationComplete: function (argument) {
     //Do something
 }
});

{% endhighlight %}


### Axis Label Click

The [`axisLabelClick`](../api/ejchart#events:axislabelclick) event is triggered while clicking the axis labels.

{% highlight javascript %}

//axisLabelClick event for chart

$("#container").ejChart({

    axisLabelClick: function (args) {
              //Do something
    }
   
});
{% endhighlight %}


### Axes Label Rendering

The [`axesLabelRendering`](../api/ejchart#events:axeslabelrendering) event is triggered before rendering the labels. This event is triggered for each label in axis. You can use this event to add custom text to axis labels.

{% highlight javascript %}

//axesLabelRendering event for chart

$("#container").ejChart({

    axesLabelRendering: function (args) {
            //Do something
    }
   
});

{% endhighlight %}



### Axis Label Mouse Move

The [`axisLabelMouseMove`](../api/ejchart#events:axislabelmousemove) event is triggered on moving mouse over the axis label.

{% highlight javascript %}

//axisLabelMouseMove event for chart

$("#container").ejChart({

    axisLabelMouseMove: function (args) {
              //Do something
    }
   
});

{% endhighlight %}


### Axes Labels Initialize

The [`axesLabelsInitialize`](../api/ejchart#events:axeslabelsinitialize) event is triggered  during the initialization of axis labels.

{% highlight javascript %}

//axesLabelsInitialize event for chart

$("#container").ejChart({

    axesLabelsInitialize: function (args) {
            //Do something
    }
    
});

{% endhighlight %}


### Axes Range Calculate

The [`axesRangeCalculate`](../api/ejchart#events:axesrangecalculate) event is triggered during axes range calculation. 
This event is triggered for each axis present in Chart. You can use this event to customize axis range as required.

{% highlight javascript %}

//axesRangeCalculate event for chart

$("#container").ejChart({

      axesRangeCalculate: function (args) {
              //Do something
      }
      
});

{% endhighlight %}

### Axes Title Rendering

The [`axesTitleRendering`](../api/ejchart#events:axestitlerendering) event is triggered  before rendering the axis title. This event is triggered for each axis with title. You can use this event to add custom text to axis title.

{% highlight javascript %}

//axesTitleRendering event for chart

$("#container").ejChart({

     axesTitleRendering: function (args) {
             //Do something
     }
     
});

{% endhighlight %}

### After Resize

The [`afterResize`](../api/ejchart#events:afterresize) event is triggered after the chart is resized

{% highlight javascript %}

//afterResize event for chart

$("#container").ejChart({

    afterResize: function (args) {
              //Do something
    }
   
});

{% endhighlight %}

### Before Resize

The [`beforeResize`](../api/ejchart#events:beforeresize) event is triggered while the chart is changing.

{% highlight javascript %}

//beforeResize event for chart

$("#container").ejChart({

    beforeResize: function (args) {
              //Do something
    }
   
});

{% endhighlight %}

### Chart Click

The [`chartClick`](../api/ejchart#events:chartclick) event is triggered while clicking the chart 

{% highlight javascript %}

//chartClick event for chart

$("#container").ejChart({

    chartClick: function (args) {
              //Do something
    }
   
});

{% endhighlight %}

### Chart Double Click

The [`chartDoubleClick`](../api/ejchart#events:chartdoubleclick) event is triggered on double clicking the chart.

{% highlight javascript %}

//chartDoubleClick event for chart

$("#container").ejChart({

    chartDoubleClick: function (args) {
              //Do something
    }
   
});

{% endhighlight %}

### Chart Mouse Move

The [`chartMouseMove`](../api/ejchart#events:chartmousemove) event is triggered while moving the mouse over the chart.

{% highlight javascript %}

//chartMouseMove event for chart

$("#container").ejChart({

    chartMouseMove: function (args) {
              //Do something
    }
   
});

{% endhighlight %}

### Chart Mouse Leave

The [`chartMouseLeave`](../api/ejchart#events:chartmouseleave) event is triggered when the mouse pointer leaves the chart.

{% highlight javascript %}

//chartMouseLeave event for chart

$("#container").ejChart({

    chartMouseLeave: function (args) {
              //Do something
    }
   
});

{% endhighlight %}

### Chart Area Bounds Calculate

The [`chartAreaBoundsCalculate`](../api/ejchart#events:chartareaboundscalculate) event is triggered during the calculation of chart area bounds. You can use this event to customize the bounds of chart area.

{% highlight javascript %}

//chartAreaBoundsCalculate event for chart

$("#container").ejChart({

    chartAreaBoundsCalculate: function (args) {
            //Do something
    }
    
});

{% endhighlight %}

### Create

The [`create`](../api/ejchart#events:create) event is triggered after the chart is created.

{% highlight javascript %}

//Create event for chart

$("#container").ejChart({

     create: function (args) {
             //Do something
     }
     
});

{% endhighlight %}

### Drag Start

The [`dragStart`](../api/ejchart#events:dragstart) event is triggered when the dragging is started.

{% highlight javascript %}

//Drag Start event for chart

$("#container").ejChart({

    dragStart: function (args) {
              //Do something
    }
   
});

{% endhighlight %}


### Dragging

The [`dragging`](../api/ejchart#events:dragging) event is triggered while dragging.

{% highlight javascript %}

//Dragging event for chart

$("#container").ejChart({

    dragging: function (args) {
              //Do something
    }
   
});

{% endhighlight %}


### Drag End

The [`dragEnd`](../api/ejchart#events:dragend) event is triggered when the dragging is completed.

{% highlight javascript %}

//DragEnd event for chart

$("#container").ejChart({

    dragEnd: function (args) {
              //Do something
    }
   
});

{% endhighlight %}


### Destroy

The [`destroy`](../api/ejchart#events:destroy) event is triggered when chart is destroyed completely.

{% highlight javascript %}

//Destroy event for chart

$("#container").ejChart({

     destroy: function (args) {
             //Do something
     }
     
});

{% endhighlight %}


### Display Text Rendering

The [`displayTextRendering`](../api/ejchart#events:displaytextrendering) event is triggered  before rendering the data labels. 
This event is triggered for each data label in the series. You can use this event to add custom text in data labels.


{% highlight javascript %}

//displayTextRendering event for chart

$("#container").ejChart({

    displayTextRendering: function (args) {
             //Do something
    }
	
});

{% endhighlight %}


### Error Bar Rendering

The [`errorBarRendering`](../api/ejchart#events:errorbarrendering) event is triggered when the error bar is rendering.

{% highlight javascript %}

//errorBarRendering event for chart

$("#container").ejChart({

    errorBarRendering: function (args) {
              //Do something
    }
   
});

{% endhighlight %}


### Legend Bounds Calculate

The [`legendBoundsCalculate`](../api/ejchart#events:legendboundscalculate) event is triggered during the calculation of legend bounds. 
You can use this event to customize the bounds of legend.

{% highlight javascript %}

//legendBoundsCalculate event for chart

$("#container").ejChart({

     legendBoundsCalculate: function (args) {
              //Do something
     }
     
});

{% endhighlight %}


### Legend Item Click

The [`legendItemClick`](../api/ejchart#events:legenditemclick) event is triggered on clicking the legend item.

{% highlight javascript %}

//legendItemClick event for chart

$("#container").ejChart({

     legendItemClick: function (args) {
              //Do something
     }
     
});

{% endhighlight %}


### Legend Item Mouse Move

The [`legendItemMouseMove`](../api/ejchart#events:legenditemmousemove) event is triggered when moving mouse over legend item. You can use this event for hit testing on legend items.

{% highlight javascript %}

//legendItemMouseMove event for chart

$("#container").ejChart({

    legendItemMouseMove: function (args) {
             //Do something
    }
    
});

{% endhighlight %}


### Legend Item Rendering

The [`legendItemRendering`](../api/ejchart#events:legenditemrendering) event is triggered before rendering the legend item. This event is fired for each legend item in Chart. 
You can use this event to customize legend item shape or add custom text to legend item.

{% highlight javascript %}

//legendItemRendering event for chart

$("#container").ejChart({

    legendItemRendering: function (args) {
            //Do something
    }
    
});

{% endhighlight %}


### Load

The [`load`](../api/ejchart#events:load) event is triggered before loading the chart.

{% highlight javascript %}

//load event for chart

$("#container").ejChart({

    load: function (args) {
             //Do something
    }
    
});

{% endhighlight %}


### Multi Level Label Click

The [`multiLevelLabelClick`](../api/ejchart#events:multilevellabelclick) event is triggered  on the clicking the Multi level labels of the chart .

{% highlight javascript %}

//MultilevelLabelsClick event for chart

$("#container").ejChart({

    multiLevelLabelClick: function (args) {
              //Do something
    }
   
});

{% endhighlight %}


### Multi Level Label Rendering


The [`multiLevelLabelRendering`](../api/ejchart#events:multilevellabelrendering) event is triggered when multi level labels are rendering.

{% highlight javascript %}

//multi level labels rendering event for chart

$("#container").ejChart({

  multiLevelLabelRendering: function (args) {
              //Do something
    }
   
});

{% endhighlight %}


### Point Region Click


The [`pointRegionClick`](../api/ejchart#events:pointregionclick) event is triggered  on clicking a point in chart. You can use this event to handle clicks made on points.

{% highlight javascript %}

//pointRegionClick event for chart

$("#container").ejChart({

    pointRegionClick: function (args) {
             //Do something
    }
    
});

{% endhighlight %}


### Point Region Mouse Move


The [`pointRegionMouseMove`](../api/ejchart#events:pointregionmousemove) event is triggered when  mouse is moved over a point.

{% highlight javascript %}

//pointRegionMouseMove event for chart

$("#container").ejChart({

    pointRegionMouseMove: function (args) {
                  //Do something
    }
   
});

{% endhighlight %}


### Pre Render


The [`preRender`](../api/ejchart#events:prerender) event is triggered before rendering the chart.

{% highlight javascript %}

//preRender event for chart

$("#container").ejChart({

    preRender: function (args) {
              //Do something
    }
   
});

{% endhighlight %}

### Range Selected


The [`rangeSelected`](../api/ejchart#events:rangeselected) event is triggered after the data is selected in the chart

{% highlight javascript %}

//rangeSelected event for chart

$("#container").ejChart({

    rangeSelected: function (args) {
             //Do something
    }
    
});

{% endhighlight %}

### Series Region Click


The [`seriesRegionClick`](../api/ejchart#events:seriesregionclick) event is triggered after selecting a series. This event is triggered after selecting a series only if selection mode is enabled in the series.

{% highlight javascript %}

//series Region click event for chart

$("#container").ejChart({

    seriesRegionClick: function (args) {
              //Do something
    }
    
});

{% endhighlight %}

### Series Rendering


The [`seriesRendering`](../api/ejchart#events:seriesrendering) event is triggered before rendering a series. This event is fired for each series in Chart.

{% highlight javascript %}

//seriesRendering event for chart

$("#container").ejChart({

    seriesRendering: function (args) {
              //Do something
    }
    
});

{% endhighlight %}


### Symbol Rendering


The [`symbolRendering`](../api/ejchart#events:symbolrendering) event is triggered before rendering the marker symbols. This event is triggered for each marker in Chart.

{% highlight javascript %}

//symbolRendering event for chart

$("#container").ejChart({
 
    symbolRendering: function (args) {
              //Do something
    }
    
});

{% endhighlight %}


### Trendline Rendering


The [`trendlineRendering`](../api/ejchart#events:trendlinerendering) event is triggered when trendlines are rendering.

{% highlight javascript %}

//trendline rendering event for chart

$("#container").ejChart({

  trendlineRendering: function (args) {
              //Do something
    }
   
});

{% endhighlight %}


### Title Rendering


The [`titleRendering`](../api/ejchart#events:titlerendering) event is triggered before rendering the Chart title. You can use this event to add custom text in Chart title.

{% highlight javascript %}

//titleRendering event for chart

$("#container").ejChart({

    titleRendering: function (args) {
              //Do something
    }
    
});

{% endhighlight %}

### Sub Title Rendering


The [`subtitleRendering`](../api/ejchart#events:subtitlerendering) event is triggered before rendering the Chart  Sub title. 

{% highlight javascript %}

//SubtitleRendering event for chart

$("#container").ejChart({

    subTitleRendering: function (args) {
              //Do something
    }
    
});

{% endhighlight %}


### Tooltip Initialize


The [`tooltipInitialize`](../api/ejchart#events:tooltipinitialize) event is triggered before rendering the tooltip. This event is fired when tooltip is enabled and mouse is hovered on a Chart point. You can use this event to customize tooltip before rendering.

{% highlight javascript %}

//toolTipInitialize event for chart
 
$("#container").ejChart({

    toolTipInitialize: function (args) {
              //Do something
    }
    
});

{% endhighlight %}


### Track Axis Tooltip


The [`trackAxisTooltip`](../api/ejchart#events:trackaxistooltip) event is triggered  before rendering crosshair tooltip in axis. This event is fired for each axis with crosshair label enabled. You can use this event to customize crosshair label before rendering

{% highlight javascript %}

//trackAxisToolTip event for chart

$("#container").ejChart({

    trackAxisToolTip: function (args) {
              //Do something
    }
    
});

{% endhighlight %}



### Track tooltip


The [`trackTooltip`](../api/ejchart#events:tracktooltip) event is triggered before rendering trackball tooltip. This event is fired for each series in Chart because trackball tooltip is displayed for all the series. You can use this event to customize the text displayed in trackball tooltip.

{% highlight javascript %}

//trackToolTip event for chart

$("#container").ejChart({

    trackToolTip: function (args) {
              //Do something
    }
   
});

{% endhighlight %}

### Scroll Start


The [`scrollStart`](../api/ejchart#events:scrollstart) event is triggered when scroll starts.

{% highlight javascript %}

//scroll start event for chart

$("#container").ejChart({

   scrollStart: function (args) {}

});

{% endhighlight %}

### Scroll End


The [`scrollEnd`](../api/ejchart#events:scrollend) event is triggered after scrolling is completed.

{% highlight javascript %}


//Scroll End event for chart
$("#container").ejChart({

   scrollEnd: function (args) {}

});


{% endhighlight %}

### Scroll Changed 


The [`scrollChanged`](../api/ejchart#events:scrollchanged) event is triggered after the scrollbar position is changed.

{% highlight javascript %}

//scrollbarChanged event for chart

$("#container").ejChart({

   scrollChanged: function (args) {}
});

{% endhighlight %}

### Zoomed


The [`zoomed`](../api/ejchart#events:zoomed) event is triggered after zooming the chart while using the rectangle zooming.

{% highlight javascript %}

//zoomed event for chart

$("#container").ejChart({

    zoomed: function (args) {
            //Do something
    }
   
});

{% endhighlight %}


