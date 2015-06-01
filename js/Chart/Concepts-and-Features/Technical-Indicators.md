---
layout: post
title: Technical-Indicators
description: technical indicators
platform: js
control: Chart
documentation: ug
---

# Technical Indicators

Technical indicators are the base of technical analysis, used to determine the future of financial, stock or economic trends. Indicators serve three broad functions: to alert, to confirm and to predict actions. Future price levels can be predicted easily with the help of given data and it also supports you to enter or exit a trade and enables to make a profit.

The following are the Technical indicators supported by **ejChart**.

## Accumulation Distribution Indicator

Accumulation distribution indicator is one of the technical indicator supported by **ejChart**. The indicator rendered is called signal line. **ejChart** also provides options to customize the width and color of the signal line.

{% highlight js %}

**[JS]**
$("#chartcontainer").ejChart(
               {   
                   // ...             
                axes:[     // axis for indicator
                {
                   name: 'indicator',
                   opposedPosition: true
                }],      
             // ... 
series: [
                {  name: 'candle', 
type: 'hiloopenclose',
drawMode: 'both',
                  dataSource: window.chartData,
                  high:"High",
                  low: "Low",
                  close: "Close",
                  open: "Open",
                  volume:"Volume",
                  xName: "xDate",

                }],  
             // ... 

                 indicators:[
                  {
                     type: 'accumulationdistribution', 
                     seriesName: 'indicator',
                     yAxisName:'indicator'
                  }],
              // ...   
               });


{% endhighlight %}



The following screenshot displays Accumulation Distribution indicator.



{% include image.html url="/js/Chart/Concepts-and-Features/Technical-Indicators_images/Technical-Indicators_img1.png" Caption="Accumulation Distribution indicator"%}

## Average True Range Indicator

Average true range Indicator is one of the technical indicator supported by **ejChart**. The indicator rendered is called as signal line. You can also customize the width and color of the signal line.

{% highlight js %}

**[JS]**
$("#chartcontainer").ejChart(
               {   
                   // ...             
                axes:[     // axis for indicator
                {
                   name: 'indicator',
                   opposedPosition: true
                 }],      
             // ...   
                 indicators:[
                  {
                     type: 'atr', seriesName: 'indicator',period:14,
                     yAxisName:'indicator'
                  }],
              // ...   
               });


{% endhighlight %}


The following screenshot displays the Average true range indicator.

{% include image.html url="/js/Chart/Concepts-and-Features/Technical-Indicators_images/Technical-Indicators_img2.png" Caption="Average true range indicator"%}

## Bollinger Band Indicator

Bollinger Band Indicator is one of the technical indicator supported by **ejChart**. It contains three lines namely upper band, lower band and signal line. Upper band, lower band are calculated based on the standard deviations value. Signal band is calculated based on the simple moving average. You can also customize the width and color of the upper band, lower band and signal line. The default value of period is 14.The default value of standardDeviations is 2.

{% highlight js %}

**[JS]**
$("#chartcontainer").ejChart(
               {   
              // ...             
                axes:[     // axis for indicator
                {
                   name: 'indicator',
                   opposedPosition: true
                 }],      
             // ...   
                indicators:[
                  {
                      type: 'bollingerband', 
                      seriesName: 'indicator',            						period:5,
standardDeviations:2,
                      yAxisName:'indicator'
                  }],
              // ...   
               });


{% endhighlight %}



The following screenshot displays the Bollinger Band indicator.

{% include image.html url="/js/Chart/Concepts-and-Features/Technical-Indicators_images/Technical-Indicators_img3.png" Caption="Bollinger Band indicator"%}

## Exponential Moving Average Indicator

Exponential Moving Average Indicator is one of the technical indicator supported by ejChart. The indicator renders a line called signal line. You can also customize properties such as width, color etc., of the signal line.

{% highlight js %}

**[JS]**
$("#chartcontainer").ejChart(
              {   
                axes:[{
                   name: 'indicator',
                   opposedPosition: true
                     }],      
                indicators:[{
                        type: 'ema',
                        seriesName: 'indicator',
                        period:14,
                        yAxisName:'indicator'
                            }],
               });


{% endhighlight %}



The following screenshot displays the Exponential Moving Average Indicator

{% include image.html url="/js/Chart/Concepts-and-Features/Technical-Indicators_images/Technical-Indicators_img4.png" Caption="Exponential Moving Average Indicator"%}

## Momentum Technical Indicator

Momentum is one of the technical indicator supported by **ejChart**. The indicator renders two lines namely upper band and signal line. Upper band always render at value 100 and signal band is calculated based on the momentum formula. **ejChart** also provide options to customize the width and color of the upper band and signal line. You can also change the value for period. The default value of period is 14.

{% highlight js %}

**[JS]**
$("#chartcontainer").ejChart(
               {   
                   // ...             
                axes:[     // axis for indicator
                {
                   name: 'indicator',
                   opposedPosition: true
                 }],      
             // ...   
                 indicators:[
                  {
                     type: 'momentum', seriesName: 'indicator',period:3,
                     yAxisName:'indicator'
                  }],
              // ...   
               });


{% endhighlight %}



The following screenshot displays the momentum technical indicator.

{% include image.html url="/js/Chart/Concepts-and-Features/Technical-Indicators_images/Technical-Indicators_img5.png" Caption="Momentum technical indicator"%}

## Moving Average Convergence Divergence Indicator

**MACD** is one of the technical indicator supported by **ejChart**. It contains three lines namely Macd line, Signal line and Histogram column series that is used to differentiate macd and signal line. And also enumeration property: **macdType,****line**, **histogram** and **both**. By default, line series contain macd and signal line. Enumeration type **both** contain line and histogram series. Macd and signal line is calculated based on the **shortPeriod,****longPeriod** and **trigger** value with indicator formula and histogram displays the difference between them. **ejChart** also provides options to customize the width and color of the macd and signal line and histogram with tooltip and animation options. The value for short, long period and trigger value can also be changed.

{% highlight js %}

**[JS]**
$("#chartcontainer").ejChart(
               {   
                   // ...             
                axes:[     // axis for indicator
                {
                   name: "yAxis1",
                   opposedPosition: true
                 }],      
                // ...   
            indicators: [{
                type: "macd", seriesName: "Hilo", yAxisName: "yaxis", 
                longPeriod: 26, shortPeriod: 12, trigger: 9,
                histogram: { fill: "red", opacity: 0.7, border: { color: 
                "red", width: 1 } },
                macdType: "both", tooltip: { visible: true }
             }],              
          // ...   
   });


{% endhighlight %}



The following screenshot displays the MACD technical indicator

{% include image.html url="/js/Chart/Concepts-and-Features/Technical-Indicators_images/Technical-Indicators_img6.png" Caption="MACD Indicator"%}

## Relative Strength Index Indicator

**RSI** is one of the technical indicator supported by **ejChart**. It contains three lines namely upper band, lower band and signal line. Upper and lower band always render at value 70 and 30 respectively and signal band is calculated based on the **RSI** formula. You can also****customize the width and color of the upper band, lower band and signal line with tooltip and animation options. 

{% highlight js %}

**[JS]**
$("#chartcontainer").ejChart(
               {   
                   // ...             
                axes:[     // axis for indicator
                {
                   name: "yAxis1",
                   opposedPosition: true
                 }],      
                // ...   
            indicators: [{
                type: "rsi", seriesName: "Hilo", 
                yAxisName: "yAxis1", fill: "darkblue", width: 1,
upperLine: {fill: "green", width: 1},
lowerLine: {fill: "red", width: 1},
tooltip: {visible: true}
           }],              
          // ...   
   });


{% endhighlight %}



The following screenshot displays the **RSI** technical indicator

{% include image.html url="/js/Chart/Concepts-and-Features/Technical-Indicators_images/Technical-Indicators_img7.png" Caption="RSI technical indicator"%}

## Simple Moving Average Indicator

Simple Moving Average Indicator is one of the technical indicators supported by ejChart. The indicator rendered is called as signal line. Signal line is calculated based on the simple moving average. You can also customize the Period, width and color of the signal line. The default value of period is 14.

{% highlight js %}

**[JS]**
$("#chartcontainer").ejChart(
         {   
             // ... 

                axes:[      
                      {
                       name: 'indicator',
                       opposedPosition: true
                      }
                     ], 

             // ...   

                indicators:[
                      {
                       type: 'sma',
                       seriesName: 'indicator',
                       period:14,
                       yAxisName:'indicator'
                       }
                      ],

              // ...   
          }
);


{% endhighlight %}



The following screenshot displays the Simple Moving Average Indicator.

{% include image.html url="/js/Chart/Concepts-and-Features/Technical-Indicators_images/Technical-Indicators_img8.png" Caption="Simple Moving Average Indicator"%}

## Stochastic Technical Indicator

Stochastic technical indicator is one of the most common indicators used in technical analysis. The indicators render four lines namely upper line, lower line, stochastic line and signal line. Upper line always render at value 80 and lower line is render at value 20. Stochastic and Signal Lines are calculated based on stochastic formulas. You can also customize the width and color of the all lines. 

{% include image.html url="/js/Chart/Concepts-and-Features/Technical-Indicators_images/Technical-Indicators_img9.png" Caption="Stochastic technical indicator"%}

{% highlight js %}

**[JS]**
$("#chartcontainer").ejChart(
               {   
                   // ...             
                axes:[     // axis for indicator
                {
                   name: 'indicator',
                   opposedPosition: true
                }],      
             // ...   
                 indicators:[
                 {
                     type: 'stochastic', 
                     seriesName:'indicator',
                     period:14,
                     kPeriod:3,
                     dPeriod:3,
                     yAxisName:'indicator'   
                  }],
              // ...   
               });


{% endhighlight %}

## Triangular Moving Average Indicator

Triangular Moving Average Indicator is one of the technical indicator supported by **ejChart**. The indicator rendered is called as signal line. You can also customize the width and color of the signal line.

{% highlight js %}

**[JS]**
$("#chartcontainer").ejChart(
               {   
              // ...             
                axes:[     // axis for indicator
                {
                   name: 'indicator',
                   opposedPosition: true
                 }],      
             // ...   
                indicators:[
                  {
                      type: 'tma', 
                      seriesName: 'indicator',            						period:14,                       						yAxisName:'indicator'
                  }],
              // ...   
               });


{% endhighlight %}



The following screenshot displays the Triangular Moving Average indicator.

{% include image.html url="/js/Chart/Concepts-and-Features/Technical-Indicators_images/Technical-Indicators_img10.png" Caption="Triangular Moving Average indicator"%}



