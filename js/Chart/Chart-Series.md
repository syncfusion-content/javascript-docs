---
layout: post
title: Chart-Series
description: chart series
platform: js
control: Chart
documentation: ug
---

# Chart Series

## Multiple Series

In EjChart, you can add multiple series object in the **series** options. By default, the series are rendered in the order it is added to the **series** option. You can change this order by using the **zOrder** option.  

{% highlight js %}


    $("#chartcontainer").ejChart({
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

![]("/js/Chart/Chart-Series_images/Chart-Series_img1.png" Caption="Chart with multiple series")

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/column) here to view the multiple series online demo sample.


### Customizing all series together

By using the **commonSeriesOptions**, you can customize the series options for all the series commonly instead of setting the options directly on each series object. 

N> The inline properties of the series has the first priority and override the commonSeriesOptions.

The following code example explains on how to enable marker, tooltip and animation for the chart series by using the commonSeriesOptions.

{% highlight js %}


    $("#chartcontainer").ejChart({
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

![]("/js/Chart/Chart-Series_images/Chart-Series_img2.png" Caption="Chart with CommonSeriesOptions")


## Combination Series

EjChart allows you to render the combination of different series in the chart. 

{% highlight js %}


    $("#chartcontainer").ejChart({
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

![]("/js/Chart/Chart-Series_images/Chart-Series_img3.png" Caption="Chart with CombinationSeries")

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/combination) here to view the combination series online demo sample.

### Limitation of combination chart

* *Bar*, *StackingBar*, and *StackingBar100* cannot be combined with the other Cartesian type series.

* Cartesian type series cannot be combined with the accumulation series (*pie, doughnut, funnel, and pyramid*).

* *Polar* and *Radar* series cannot be combined with the accumulation and Cartesian type series.

When the combination of Cartesian and accumulation series types are added to the series option, the series that are similar to the first series are rendered and other series are ignored. The following code example illustrates this,  


{% highlight js %}


    $("#chartcontainer").ejChart({
          //  ...
          
          //Adding Multiple Series
          series: [{    // Add line series
                 points: [{ x: "Jan", y: 45 },
                    // ...
                 ],
                 type: 'line',
                 // ...
               },
               {       // Add pie series
                points: [{ x: "Jan", y: 70 },
                  // ...
                ],                
              type: 'pie'
                // ...
            }],

            //  ...   
      });


{% endhighlight %}

![]("/js/Chart/Chart-Series_images/Chart-Series_img4.png" Caption="Chart with line series")
