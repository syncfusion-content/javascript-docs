---
layout: post
title: Technical-Indicators
description: technical indicators
platform: js
control: Chart
documentation: ug
---

# Technical Indicators

EjChart control supports 10 types of technical indicators. 

## Binding data to render indicator

You can bind series **dataSource** to indicator by setting the specific series name to indicator using **"indicators.seriesName"** property.

{% highlight js %}

        $("#chartcontainer").ejChart({
              //  ...
              //Initializing Series
              series:[{
                  dataSource: chartData,
                  xName: "xDate",
                  high: "High",
                  low: "Low",
                  open: "Open",
                  close: "Close", 
                  //Set name to series
                  name: 'Hilo',
                  //  ...
            }],

            //Initializing Indicators    
            indicators: [{
                //Set Hilo series dataSource to indicator using seriesName
                seriesName: "Hilo",
                //  ...
	     }],
            //  ...
     });

{% endhighlight %}


Also you can add data to indicator directly use **dataSource** option of indicator.  

{% highlight js %}


        $("#chartcontainer").ejChart({
            //  ...
            //Initializing Indicators    
            indicators: [{
                   //Add dataSource to indicator directly
                    dataSource: chartData,
                    xName: "xDate",
                    high: "High",
                    low: "Low",
                    open: "Open",
                    close: "Close",                
                    //  ...
	       }],
            //  ...
     });

{% endhighlight %}

	
## Indicator Types

### Accumulation Distribution

To create an Accumulation Distribution indicator, set the **indicators.type** as **"accumulationdistribution"**. Accumulation Distribution require **‘volume’** field additionally with **dataSource** to calculate the signal line.

{% highlight js %}


        $("#chartcontainer").ejChart({
             // Initializing Series
              series:[{
                       name: "Hilo",
                       dataSource: chartData,
                       xName: "xDate",
                       high: "High",
                       low: "Low",
                       open: "Open",
                       close: "Close",
                       //Add additional volume field to data source for accumulation distribution
                       volume: "Volume",
                       //  ...
                   }],
               //Initializing Indicators    
               indicators: [{
                     seriesName: "Hilo",
                     //Set indicator type
                     type: "accumulationdistribution", 
                     //  ...
	        }],
            // ...   
        });


{% endhighlight %}

![]("/js/Chart/Technical-Indicators_images/Technical-Indicators_img1.png" Caption="Accumulation Distribution Indicator")

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/technicalindicators/accumulationdistribution) here to view the Accumulation Distribution indicator online demo sample.


### Average True Range (ATR)

You can create an ATR indicator by setting the **indicators.type** as **"atr"** in the **indicators**. 

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...
            //Initializing Indicators    
            indicators: [{
                 //Set indicator type
                 type: "atr", 
                 //  ...
	      }],
            // ...   
        });


{% endhighlight %}

![]("/js/Chart/Technical-Indicators_images/Technical-Indicators_img2.png" Caption="Average true range Indicator")

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/technicalindicators/atr) here to view the ATR indicator online demo sample.


### Bollinger Band 

Bollinger Band indicator is created by setting the **indicators.type** as **"bollingerband"**. It contains three lines, namely upper band, lower band and signal line. Bollinger Band default value of period is 14 and standardDeviations is 2.

{% highlight js %}


        $("#chartcontainer").ejChart({
             // ...             
             //Initializing Indicators    
              indicators: [{
                   //Set indicator type
                   type: " bollingerband", 
                   //  ...
	         }],
            // ...   
        });


{% endhighlight %}

![]("/js/Chart/Technical-Indicators_images/Technical-Indicators_img3.png" Caption="Bollinger Band Indicator")

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/technicalindicators/bollingerband) here to view the Bollinger Band indicator online demo sample.


### Exponential Moving Average (EMA)

To render an EMA indicator, you have to set the **indicators.type** as **"ema"**.  

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
             //Initializing Indicators    
              indicators: [{
                   //Set indicator type
                   type: "ema", 
                   //  ...
	         }],
            // ...   
        });


{% endhighlight %}

![]("/js/Chart/Technical-Indicators_images/Technical-Indicators_img4.png" Caption="Exponential Moving Average Indicator")

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/technicalindicators/ema) here to view the EMA indicator online demo sample.


### Momentum 

Momentum Technical indicator is created by setting the **indicators.type** as **"momentum"**. The momentum indicator renders two lines, namely upper band and signal line. Upper band always rendered at the value 100 and the signal line is calculated based on the momentum of data.

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
             //Initializing Indicators    
              indicators: [{
                   //Set indicator type
                   type: "momentum", 
                   //  ...
	         }],
            // ... 
        });


{% endhighlight %}

![]("/js/Chart/Technical-Indicators_images/Technical-Indicators_img5.png" Caption="Momentum Indicator")

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/technicalindicators/momentum) here to view the Momentum indicator online demo sample.


### Moving Average Convergence Divergence (MACD)

To render an MACD indicator, you have to set the **indicators.type** as **"macd"**.  MACD indicator contains Macd line, Signal line and Histogram column. Histogram is used to differentiate MACD and signal line.

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
             //Initializing Indicators    
              indicators: [{
                   //Set indicator type
                   type: "macd", 
                   //  ...
	         }],
            // ...  
        });


{% endhighlight %}

![]("/js/Chart/Technical-Indicators_images/Technical-Indicators_img6.png" Caption="MACD Indicator")

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/technicalindicators/macd) here to view the MACD indicator online demo sample.


#### macdType

Using **macdType** enumeration property, you can change the MACD rendering as *line*, *histogram* or *both*. 

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
             //Initializing Indicators    
              indicators: [{
                   type: "macd", 
                   //Set macd draw type
                   macdType: "histogram", 
                   //  ...
	         }],
            // ...  
        });


{% endhighlight %}

![]("/js/Chart/Technical-Indicators_images/Technical-Indicators_img7.png" Caption="MACD Histogram")

### Relative Strength Index (RSI)

For rendering the RSI indicator, set the **indicators.type** as **"rsi"**. It contains three lines, namely upper band, lower band and signal line. Upper and lower band always render at value 70 and 30 respectively and signal line is calculated based on the **RSI** formula.

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
             //Initializing Indicators    
              indicators: [{
                   //Set indicator type
                   type: "rsi",
                   //  ...
	         }],
            // ...
        });


{% endhighlight %}


![]("/js/Chart/Technical-Indicators_images/Technical-Indicators_img8.png" Caption="RSI Indicator")

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/technicalindicators/rsi) here to view the RSI indicator online demo sample.


### Simple Moving Average (SMA)

To render the SMA indicator, you should specify the **indicators.type** as **"sma"**.  

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
             //Initializing Indicators    
              indicators: [{
                   //Set indicator type
                   type: "sma",
                   //  ...
	         }],
            // ...
        });


{% endhighlight %}

![]("/js/Chart/Technical-Indicators_images/Technical-Indicators_img9.png" Caption="Simple Moving Average Indicator")

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/technicalindicators/sma) here to view the SMA indicator online demo sample.


### Stochastic 

For Stochastic indicator, you need to set the **indicators.type** as **"stochastic"**. The Stochastic indicator renders four lines, namely upper line, lower line, stochastic line and the signal line. Upper line always rendered at value 80 and the lower line is rendered at value 20. Stochastic and Signal Lines are calculated based on stochastic formula.

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...            
             //Initializing Indicators    
              indicators: [{
                   //Set indicator type
                   type: "stochastic",
                   //  ...
	         }],
            // ...  
        });


{% endhighlight %}

![]("/js/Chart/Technical-Indicators_images/Technical-Indicators_img10.png" Caption="Stochastic Indicator")

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/technicalindicators/stochastic) here to view the stochastic indicator online demo sample.


### Triangular Moving Average (TMA)

To render the TMA indicator, you should specify the **indicators.type** as **"tma"**. 

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
             //Initializing Indicators    
              indicators: [{
                   //Set indicator type
                   type: "tma",
                   //  ...
	         }],
            // ...  
        });


{% endhighlight %}

![]("/js/Chart/Technical-Indicators_images/Technical-Indicators_img11.png" Caption="Triangular Moving Average Indicator")

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/technicalindicators/tma) here to view the TMA indicator online demo sample.


## Enable Tooltip 

To display the indicator tooltip, use **visible** option of **indicators.tooltip**. Also you can change and customize the tooltip color, border, format and font properties similar to the series tooltip.

{% highlight js %}


        $("#chartcontainer").ejChart({
            // ...             
             //Initializing Indicators    
              indicators: [{
                   //  ...
                   tooltip: {
                        //Enable tooltip for indicator
                        visible: true
                      },
	         }],
            // ...  
        });


{% endhighlight %}

![]("/js/Chart/Technical-Indicators_images/Technical-Indicators_img12.png" Caption="Indicator Tooltip")


