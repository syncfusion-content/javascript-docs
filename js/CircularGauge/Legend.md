---
layout: post
title: Legend
description: legend for ranges in the Circular Gauge 
platform: js
control: Circular Gauge
documentation: ug
api: /api/js/ejcirculargauge
---

# Legend

The [`legend`](../api/ejcirculargauge#members:legend) contains the list of the ranges that appear in the circular gauge  

## Legend Visibility

By default, the legend will not be displayed in the circular gauge. You can enable or disable it by using the [`visible`](../api/ejcirculargauge#members:legend-visible) property of the legend.

{% highlight javascript %}

$("#CircularGauge1").ejCircularGauge({
  legend:{ 
     visible : true,
       },
            });



{% endhighlight %}

![](/js/CircularGauge/Legend_images/Legend_img1.png)


[Click](http://js.syncfusion.com/demos/web/#!/flatlight/radialgauge/legend) here to view the online demo sample for  legend in the circular Gauge.

### Legend Text

The text displayed in the legend can be customized by using the [`legendText`](../api/ejcirculargauge#members:scales-ranges-legendtext) property present in the ranges of the circular gauge. When the legendText is not specified in the ranges, then the legend item for that particular range will not displayed. By default the legendText value is **null** . 

{% highlight javascript %}

$("#CircularGauge1").ejCircularGauge({
            // ...             
              ranges: [{
                 legendText:"Light air",			
            }]
            //...

            // ...             
        });


{% endhighlight %}

## Position and Align the Legend

By using the [`position`](../api/ejcirculargauge#members:legend-position) property, you can position the legend at *left*, *right*, *top* or *bottom* of the CircularGauge. The legend is positioned at the **bottom** of the circular gauge, by default.

{% highlight javascript %}

$("#CircularGauge1").ejCircularGauge({
            // ...             
            legend: {
                // ...  
                //Place the legend at top of the circular gauge
                position: 'top',

            }
            // ...             
        });


{% endhighlight %}

![](/js/CircularGauge/Legend_images/Legend_img2.png)

### Legend Alignment

You can align the legend to the *center*, *far* or *near* based on its position by using the [`alignment`](../api/ejcirculargauge#members:legend-alignment) property.

{% highlight javascript %}


  $("#CircularGauge1").ejCircularGauge({
            // ...             
            legend: {
                //...
                //The below two settings will place the legend at the top-right corner of the circular gauge.
                alignment: 'far',
                position: 'top', 
            }
            // ...             
        });


{% endhighlight %}

![](/js/CircularGauge/Legend_images/Legend_img3.png)

## Customization

### Legend Fill and Opacity

You can change the opacity and fill color of legend text using [`opacity`](../api/ejcirculargauge#members:legend-opacity) and [`fill`](../api/ejcirculargauge#members:legend-fill) property of legend. 

{% highlight javascript %}

        $("#CircularGauge1").ejCircularGauge({
            // ...             
            legend: {
                //...
                //fill color of legend
                 fill: 'red',
                //opacity of legend
                 opacity: 0.8
            }
            // ...             
        });

{% endhighlight %}

### Legend shape

To change the legend item shape, you have to specify the desired shape in the [`shape`](../api/ejcirculargauge#members:legend-shape) property of the legend. By default, the shape of the legend is **circle**.It also supports rectangle,diamond,triangle,slider,line,pentagon,trapezoid and wedge shapes.

{% highlight javascript %}


        $("#CircularGauge1").ejCircularGauge({
            // ...             
            legend: {
                //...
                //Change legend shape
                 shape: 'slider',
            }
            // ...             
        });


{% endhighlight %}

![](/js/CircularGauge/Legend_images/Legend_img4.png)


### Legend Item Size and Border

You can change the size of the legend items by using the [`width`](../api/ejcirculargauge#members:legend-itemstyle-width) and [`height`](../api/ejcirculargauge#members:legend-itemstyle-height) properties in the [`itemStyle`](../api/ejcirculargauge#members:legend-itemstyle). To change the legend item border, use [`border`](../api/ejcirculargauge#members:legend-itemstyle-border) property of the legend itemStyle. The color and width of legend item border can be customized using border [`color`](../api/ejcirculargauge#members:legend-itemstyle-border-color) and [`width`](../api/ejcirculargauge#members:legend-itemstyle-border-width) property.

{% highlight javascript %}


        $("#CircularGauge1").ejCircularGauge({
            // ...             
            legend: {
                //...
                //Change legend items border, height and width
                itemStyle: {width: 13, height: 13, border: { color: "#FF0000", width: 2 } },
            }
            // ...             
        });


{% endhighlight %}

![](/js/CircularGauge/Legend_images/Legend_img5.png)

### Legend size

You can change the default legend size by using the [`size`](../api/ejcirculargauge#members:legend-size) property of the legend. The height and width of legend size can customized using [`height`](../api/ejcirculargauge#members:legend-size-height) and [`width`](../api/ejcirculargauge#members:legend-size-width) property. The color and width of legend border can be customized using [`border color`](../api/ejcirculargauge#members:legend-border-color) and [`width`](../api/ejcirculargauge#members:legend-border-width) property.

{% highlight javascript %}


        $("#CircularGauge1").ejCircularGauge({   
            // ...
            legend: { 
                 //...
                 //Change legend size
                 size:{width: '350', height: '100'}
            }
            // ...             
        });


{% endhighlight %}

![](/js/CircularGauge/Legend_images/Legend_img6.png)


### Legend Item Padding

You can control the spacing between the legend items by using the [`itemPadding`](../api/ejcirculargauge#members:legend-itempadding) option of the legend.  The default value is 20. 

{% highlight javascript %}


        $("#CircularGauge1").ejCircularGauge({
            // ...             
            legend: {
                //...
                //Add space between each legend item
                itemPadding: 30,
            }
            // ...             
        });


{% endhighlight %}

![](/js/CircularGauge/Legend_images/Legend_img7.png)

### Legend border

You can customize the legend border by using the [`border`](../api/ejcirculargauge#members:legend-border) option in the legend. The legend border can be customized using border [`color`](../api/ejcirculargauge#members:legend-border-color) and [`width`](../api/ejcirculargauge#members:legend-border-width) property. 

{% highlight javascript %}


        $("#CircularGauge1").ejCircularGauge({
            // ...             
            legend: {
                //...
                //Set border color and width to legend
                border: {color: "#FFC342", width: 2},
            }
            // ...             
        });


{% endhighlight %}

![](/js/CircularGauge/Legend_images/Legend_img8.png)

### Font of the legend text

The [`font`](../api/ejcirculargauge#members:legend-font) of the legend item text can be customized by using properties such as [`fontFamily`](../api/ejcirculargauge#members:legend-font-fontfamily), [`fontStyle`](../api/ejcirculargauge#members:legend-font-fontstyle), [`fontWeight`](../api/ejcirculargauge#members:legend-font-fontweight) , [`color`](../api/ejcirculargauge#members:legend-font-color) and [`size`](../api/ejcirculargauge#members:legend-font-size) of legend font.


{% highlight javascript %}


        $("#CircularGauge1").ejCircularGauge({
            // ...             
            legend: {
                //...
                //Customize the legend item text
                font: { fontFamily: 'Segoe UI', fontStyle: 'Normal', fontWeight: 'Bold', size: '15px' },
                         
             },
            // ...             
        });


{% endhighlight %}

![](/js/CircularGauge/Legend_images/Legend_img9.png)

## Events

### Legend Item Render

[`LegendItemRender`](../api/ejcirculargauge#events:legenditemrender) event triggers before rendering the legend items. This event is triggered for each legend item in Circular gauge. You can use this event to customize legend item shape or add custom text to legend item dynamically

{% highlight javascript %}

$("#CircularGauge1").ejCircularGauge({

           
            //Subscribe the legendItemRender event
            legendItemRender: "onLegendRender",

            //...
        });

        function onLegendRender(sender) {
            //Get legend item details before rendering
            var legendItem = sender.data;

        }

{% endhighlight %}

### Legend Item Click

You can get the legend item details such as *RangeIndex, bounds and shape* by subscribing the [`legendItemClick`](../api/ejcirculargauge#events:legenditemclick) event of the circular gauge. When the legend item is clicked, it triggers the event and returns the legend information 

{% highlight javascript %}

$("#CircularGauge1").ejCircularGauge({
           
            //Subscribe the legend item click event
            legendItemClick: "onLegendClicked",

            //...
        });

        function onLegendClicked(sender) {
            //Get legend item details on legend item click.
            var legendItem = sender.data;
        }


{% endhighlight %}

You can select a specific range while clicking on the corresponding legend item through disabling the [`toggleVisibility`](../api/ejcirculargauge#members:legend-togglevisibility) option of the legend. The default value of toggleVisibility option is **true**. 

{% highlight javascript %}

 $("#CircularGauge1").ejCircularGauge({   
            // ...
            legend: { 
                  //Disable ranges collapsing on legend item clicked
                   toggleVisibility: false,
            }
            // ...             
        });
             
{% endhighlight %}

