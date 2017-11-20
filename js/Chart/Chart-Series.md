---
layout: post
title: Multiple chart series
description: Learn how to render different types of series in chart.
platform: js
control: Chart
documentation: ug
api : /api/js/ejchart
---

# Chart Series

## Multiple Series

In EjChart, you can add multiple series object in the [`series`](../api/ejchart#members:series) options. The series are rendered in the order it is added to the [`series`](../api/ejchart.html#members:series) option, by default. You can change this order by using the [`zOrder`](../api/ejchart#members:series-zOrder) option.  

{% highlight javascript %}


    $("#container").ejChart({
          // ...  
          //Adding Multiple Series
          series: [{   // Add first series
              points: [{ x: "USA", y: 50 },
                       // ...
                  ],
                type: 'column',
                // ...
             },
            {       // Add second series
              points: [{ x: "USA", y: 70 },
                       // ...
                   ],                
                 type: 'column'
                 // ...
             },
            {      // Add third series
              points: [{ x: "USA", y: 45 },
                       // ...
                  ],                
                type: 'column'
                // ...
            }],
            
        // ...
    });


{% endhighlight %}

![](/js/Chart/Chart-Series_images/Chart-Series_img1.png)


[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/column) here to view the multiple series online demo sample.


### Customizing all series together

By using the [`commonSeriesOptions`](../api/ejchart#members:commonseriesoptions), you can customize the series options for all the series commonly, instead of setting the options directly on each series object. 

N> The inline properties of the series has the first priority and override the commonSeriesOptions.

The following code example explains on how to enable marker, tooltip and animation for the chart series by using the commonSeriesOptions.

{% highlight javascript %}


    $("#container").ejChart({
          //  ...
          
           //Initializing Common Properties for all the series
            commonSeriesOptions: {
                type: 'line',
                enableAnimation: true,
                tooltip: {
                    visible: true,
                    template: 'Tooltip'
                },
                marker: {
                    shape: 'circle',
                    size:
                    {
                        height: 10, width: 10
                    },
                    visible: true
                },
                border: { width: 2 }
            },
            
            series: [{
                    // ...         
                },{                
                    //  ...         
              }],
              
            //  ...
      });


{% endhighlight %} 

![](/js/Chart/Chart-Series_images/Chart-Series_img2.png)


## Combination Series

EjChart allows you to render the combination of different series in the chart. 

{% highlight javascript %}


    $("#container").ejChart({
          //  ...
          
           series: [{
                //Set chart type to series1
                 type: 'column',         
               // ...         
            },{
                //Set chart type to series2
                 type: 'line',         
               //  ...         
            }],
              
            //  ...   
      });


{% endhighlight %}

![](/js/Chart/Chart-Series_images/Chart-Series_img3.png)


[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/combination) here to view the combination series online demo sample.

### Limitation of combination chart

* [`Bar`](chart-types#bar-chart), [`StackingBar`](chart-types#stacked-bar-chart), and [`StackingBar100`](chart-types#stacked-bar-chart-1) cannot be combined with the other Cartesian type series.

* Cartesian type series cannot be combined with the accumulation series ([`pie`](chart-types#pie-chart), [`doughnut`](chart-types#doughnut-chart), [`funnel`](chart-types#funnel-chart), and [`pyramid`](chart-types#pyramid-chart)).

* [`Polar`](chart-types#polar) and [`Radar`](chart-types#radar-chart) series cannot be combined with the accumulation and Cartesian type series.

When the combination of Cartesian and accumulation series types are added to the series option, the series that are similar to the first series are rendered and other series are ignored. The following code example illustrates this,  


{% highlight javascript %}


    $("#container").ejChart({
          //  ...
          
          //Adding Multiple Series
          series: [{    // Add line series
                 points: [{ x: "Jan", y: 45 },
                    // ...
                 ],
                 type: 'line',
                 // ...
               },
               {       // Add [Pie](chart-types#pie-chart) series
                points: [{ x: "Jan", y: 70 },
                  // ...
                ],                
              type: 'pie'
                // ...
            }],

            //  ...   
      });


{% endhighlight %}

![](/js/Chart/Chart-Series_images/Chart-Series_img4.png)

## Init Series render

The [`initSeriesRender`](../api/ejchart#members:initseriesrender) property controls whether the series has to be rendered at initial loading of chart.
This property will be useful in scenarios where chart is placed at the bottom of the web page and we need to render the series only when the chart is visible while scrolling to the top.

{% highlight javascript %}


    $("#container").ejChart({

     initSeriesRender : false
                  
});


{% endhighlight %}

