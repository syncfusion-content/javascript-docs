---
layout: post
title: -concepts-and-features
description:  concepts and features
platform: js
control: RangeNavigator
documentation: ug
---

##  Concepts and features

### Range Types

**RangeNavigator** control is designed to visualize large number of data and navigate to particular data from the large collection at ease. The data for the **RangeNavigator** is either numeric values or **DateTime** values and the **valueType** property in **RangeNavigator** indicates the type of the data that should be passed for the control. By default the **valueType** of **RangeNavigator** is **DateTime**

* Numeric                   

* DateTime

#### Numeric Type


**RangeNavigator** is also used with numeric data and the **valueType** for this data is “**numeric**”

{% highlight js %}

**[JS]**
$("#rangecontainer").ejRangeNavigator({
      //...
        valueType: "numeric",
      //...	
       });


{% endhighlight %}


The following screenshot displays the **RangeNavigator** with numeric data.



{% include image.html url="\js\RangeNavigator\-concepts-and-features_images\-concepts-and-features_img1.png" Caption="Figure 7: RangeNavigator with numeric data."%}

#### DateTime

By default the **valueType** of the **RangeNavigator** is “**datetime**” and represents the **DateTime** values.

{% highlight js %}

**[JS]**
$("#rangecontainer").ejRangeNavigator({
      //...
        valueType: "datetime",
      //...	
       });


{% endhighlight %}



{% include image.html url="\js\RangeNavigator\-concepts-and-features_images\-concepts-and-features_img2.png" Caption="Figure 8: RangeNavigator with DateTime values"%}

#### DateTime Intervals

The **DateTime** range type contains an **intervalType** property that sets the **DateTime** interval to one of the following:

* Years

* Quarters

* Months

* Weeks

* Days 

* Hours

* By default **intervalType** for higher level labels are **years** and for lower level labels its **quarters.**


{% highlight js %}

**[JS]**
$("#rangecontainer").ejRangeNavigator({
   //...
     labelSettings:
      { 
          higherLevel:
            {
                intervalType: 'years',
            },
        lowerLevel:
           {
               intervalType: ' quarters',
           }
      },    
  //...	
  });


{% endhighlight %}





{% include image.html url="\js\RangeNavigator\-concepts-and-features_images\-concepts-and-features_img3.png" Caption="Figure 9: Date Time property"%}

### Range Padding

**Range Padding** adds padding for range in **RangeNavigator**. It allows you to space the grid lines in the **RangeNavigator**.  By default, this property is set to **none**.

#### Numeric

The **rangePadding** property allows you to customize the automatic range calculation using the default auto range calculation for **RangeNavigator**.

{% highlight js %}

**[JS]**
$("#rangecontainer").ejRangeNavigator({
   //...
        valueType: "numeric",
        rangePadding: 'none ',
   //...	
  });


{% endhighlight %}

##### None:

By default, the **rangePadding** for numerical range is none. The range is calculated from the minimum value to the maximum value of data in the RangeNavigator.

The following screenshot illustrates a **RangeNavigator** with **rangePadding** set to none.



{% include image.html url="\js\RangeNavigator\-concepts-and-features_images\-concepts-and-features_img4.png" Caption="Figure 29: RangeNavigator with rangePadding set to none"%}

##### Additional:

When you set the **rangePadding** for numerical range to **Additional**, range is padded with an interval.

The following screenshot illustrates a **RangeNavigator** with **rangePadding** set to additional.



{% include image.html url="\js\RangeNavigator\-concepts-and-features_images\-concepts-and-features_img5.png" Caption="Figure 10: RangeNavigator with rangePadding set to additional"%}

##### Normal:

In normal **rangePadding**, automatic range calculation differs based on the data. 

The following screenshot illustrates **RangeNavigator** with **rangePadding** set to normal

{% include image.html url="\js\RangeNavigator\-concepts-and-features_images\-concepts-and-features_img6.png" Caption="Figure 11: RangeNavigator with rangePadding set to normal"%}

##### Round:

Round **rangePadding** for a numerical range rounds the range of the control to the nearest possible value that is divisible by the interval.

The following screenshot illustrates a **RangeNavigator** with **rangePadding** set to **Round**.

{% include image.html url="\js\RangeNavigator\-concepts-and-features_images\-concepts-and-features_img7.png" Caption="Figure 12: RangeNavigator with rangePadding set to Round"%}

#### DateTime

Using the default range calculation for **RangeNavigator**, the **rangePadding** property allows you to customize the range.

{% highlight js %}

**[JS]**
$("#rangecontainer").ejRangeNavigator({
   //...
        rangePadding: 'none ',
   //...	
  });


{% endhighlight %}

##### None:

By default, the **rangePadding** for **DateTime** range is none. The range is calculated from the minimum value to the maximum value of data in the RangeNavigator

The following screenshot illustrates a **RangeNavigator** with **rangePadding** set to none.

{% include image.html url="\js\RangeNavigator\-concepts-and-features_images\-concepts-and-features_img8.png" Caption="Figure 13: RangeNavigator with rangePadding set to none"%}

##### Round:

Round **rangePadding** for a **DateTime** range rounds the range of the control to the nearest possible value.

The following screenshot illustrates a **RangeNavigator** with **rangePadding** set to Round.

{% include image.html url="\js\RangeNavigator\-concepts-and-features_images\-concepts-and-features_img9.png" Caption="Figure 14: RangeNavigator with rangePadding set to Round"%}

### Customize axis range of navigator

**RangeNavigator** calculates the range automatically based on the values of series data points. However you can explicitly specify the range using the **start**, **end** properties in **rangeSettings** that is not possible when data is provided.

The following code example renders a RangeNavigator with a range from 2010 January 1st to 2013 January 1st.

{% highlight js %}

**[JS]**
$("#rangecontainer").ejRangeNavigator({
   //...
         rangeSettings: {
                    start: "2010/1/1", end: "2012/13/1"
                },  
   //...	
  });


{% endhighlight %}


{% include image.html url="\js\RangeNavigator\-concepts-and-features_images\-concepts-and-features_img10.png" Caption="Figure 15: RangeNavigator"%}

### Populate Data

When you provide data to **RangeNavigator**, it produces limited set of data. You can populate the **RangeNavigator** with data using the **dataSource** and **series** properties.

#### Add series to the RangeNavigator

The **Series** property provides access to a collection of all series that are defined explicitly within a **RangeNavigator** control. Each series is assigned with type and name. It contains collection of data point, each point contains x value and y values. You can add data points to the series through **dataSource** property.



{% highlight js %}

**[JS]**
$("#rangecontainer").ejRangeNavigator({
   //...
    // Adding series
     series: [
                {
                  type: 'line',
                  dataSource: data.Open, xName: "XValue", yName: "YValue",                     
                  opacity: 0.5, fill: '#69D2E7',
                  border: { color: 'transparent', width: 2 }
                },
             ],
    //...	
  });
  var data;
        function GetData() {
            var series1 = [];       
            var value = 100;
            for (var i = 1; i < 360; i++) {
                if (Math.random() > .5) {
                    value += Math.random();                 
                } else {
                    value -= Math.random();           
                }
                var point1 = { XValue: new Date(2010, 0, i), YValue: value };               
                series1.push(point1);             
            }
            data = { Open: series1};
            return data;
        }


{% endhighlight %}


The following screenshot illustrates the **RangeNavigator** that is populated with data using **dataSource** property in series.

{% include image.html url="\js\RangeNavigator\-concepts-and-features_images\-concepts-and-features_img11.png" Caption="Figure 16: RangeNavigator that is populated with data using dataSource property in series"%}

### Behavior Customization

**RangeNavigator** allows you to customize the control using events. You can change the range for selected data of the **RangeNavigator** using events.

#### Deferred update

If you set enableDeferredUpdate****to true, the **rangeChanged** event gets fired after dragging and dropping the slider. By default the enableDeferredUpdate****is true. If enableDeferredUpdate****is false then the **rangeChanged** event gets fired while dragging the slider.


{% highlight js %}

**[JS]**
$("#rangecontainer").ejRangeNavigator(
   //...
        enableDeferredUpdate: true,
   //...	
  });


{% endhighlight %}


![](-concepts-and-features_images\-concepts-and-features_img12.png)

_Figure 17: Deferred update_

#### Handle Events

**loaded:** function

This event is handled when the **RangeNavigator** gets loaded. A parameter **sender** is passed to the handler. Using **sender.model**, you can access the RangeNavigator properties. 

{% highlight js %}

**[JS]**
$("#rangecontainer").ejRangeNavigator(
               {   
                   // ...             
                        loaded: function (sender) {
                     sender.model. enableAutoResizing = false;
                    },
         //...
                    });
        });         


{% endhighlight %}


**rangeChanged**: function

This event gets fired whenever the selected range changes in **RangeNavigator**. A parameter **sender** is passed to the handler. Using sender.selectedRangeSettings, you can access the start and end value of range for the selected region. 

{% highlight js %}

**[JS]**
$("#rangecontainer").ejRangeNavigator(
               {   
                   // ...             
                        rangeChanged: function (sender) {
                    console.log(sender.selectedRangeSettings.start);
                    },
                   // ...             
                    });
        });


{% endhighlight %}

#### Use of ZoomCoordinates

**RangeNavigator** is used along with the controls like chart and grid to view the selected data. To update chart/grid, whenever the selected range changes in **RangeNavigator**, you can use **rangeChanged** event of **RangeNavigator** and then update the chart/grid with the selected data in this event. 

You can easily update the data for chart by assigning the **zoomFactor** and **zoomPosition** of the **RangeNavigator** to the chart axis.

{% highlight js %}

**[JS]**
$("#rangecontainer").ejRangeNavigator(
               {   
                   // ...             
                          rangeChanged: onchartloaded
                   // ...             
                    });
        });
       // setting zoom factor and position for chart axis in rangeChanged event.
  function onchartloaded(sender) {
         var chartobj = $("#container").data("ejChart");
         if (chartobj != null) {
           chartobj.model.axes[0].zoomPosition = sender. zoomPosition;                                                               
           chartobj.model.axes[0].zoomFactor = sender. zoomFactor;
            }
            $("#container").ejChart("redraw");
     }


{% endhighlight %}



{% include image.html url="\js\RangeNavigator\-concepts-and-features_images\-concepts-and-features_img13.png" Caption="Figure 18: Use of ZoomCoordinates"%}

#### Thumb Template

You can customize Thumb template by using **leftThumbTemplate** and **rightThumbTemplate** property. You can add the required template as a “div” element with an “id” to the web page and assign the id or assign the html string to this property under **navigatorStyleSettings**.

{% highlight js %}

 **[JS]**
<script type="text/x-jsrender" id="left" >
           <svg height="24" width="32" style="fill:#DD4A4A;stroke:black;">
                <path d="M2 2 L2 22 L22 22 L32 12 L22 2 Z" />
           </svg>
</script>
<script type="text/x-jsrender" id="right">
           <svg height="24" width="32" style="fill:#DD4A4A;stroke:black; ">
               <path d="M2 12 L12 22 L32 22 L32 2 L12 2 Z" />
           </svg>
</script>
<script type="text/javascript" language="javascript">
           $(function () {
                $("#scrollcontent").ejRangeNavigator({
               // ...             
                    navigatorStyleSettings: {
                          leftThumbTemplate: 'left',
                          rightThumbTemplate: 'right',
                    },
               // ...   
             });
          });
</script>


{% endhighlight %}



The following screenshot displays the **RangeNavigator** using thumb template.

{% include image.html url="\js\RangeNavigator\-concepts-and-features_images\-concepts-and-features_img14.png" Caption="Figure 19: Thumb template"%}

### Appearance and Styling

**JavaScript RangeNavigator** is enriched with lots of customization options for labels, gridlines and slider to develop high quality graphic rich control.

#### Customize labels

The labels are found along the range, displaying the value of the data it correspond, both on (higher level label) and below (lower level label) the **RangeNavigator**. **RangeNavigator** labels are further customized using “**font**” property in label Settings. 

{% highlight js %}

**[JS]**
$("#rangecontainer").ejRangeNavigator(
               {   
                   // ...             
               labelSettings:
        {
           // customizing higher level labels.
            higherLevel:
               {                    
                   style:
                     {
                         font:
                          {
                              color: '#ff0000',
                              style: 'Normal',
                              size: '12px',
                              opacity: 1,
                              weight: 'regular'
                          },

                     },                 
               },
                    // customizing lower level labels.
            lowerLevel:
               {   
                   style:
                     {
                         font:
                           {
                               color: '#ff0000',
                               style: 'Normal',
                               size: '12px',
                               opacity: 1,
                               weight: 'regular'
                           },  
                     },   
               }
        },   
                // ...             

                    });
        });


{% endhighlight %}

![](-concepts-and-features_images\-concepts-and-features_img15.png)



_Figure_ _2__0__: Customize labels_

##### Label Placement:

Labels in **RangeNavigator** are placed inside or outside of the control. You can customize both the higher and lower level labels using **labelPlacement** property in label setting of **RangeNavigator**. By default **labelPlacement** is “outside” for the both higher and lower level labels.

The following screen shot illustrates both the lower and higher level labels that are placed outside the control with **labelPlacement** specified as outside.

{% highlight js %}

**[JS]**
$("#rangecontainer").ejRangeNavigator(
               {   
                   // ...             
          labelSettings: {
                    higherLevel:
                       {
                           labelPlacement: "inside",
                       },
                    lowerLevel:
                         {
                           labelPlacement: "inside"
                         }
                },             
                 // ...             

                    });
        });



{% endhighlight %}


The following screenshot illustrates a **RangeNavigator** with labels inside the control after specifying the **labelPlacement** as inside.



{% include image.html url="\js\RangeNavigator\-concepts-and-features_images\-concepts-and-features_img16.png" Caption="Figure 21: RangeNavigator with labels inside the control"%}

#### Customize RangeNavigator

RangeNavigator is customized using **navigatorStyleSettings** properties. You can customize the selected and unselected region color using **selectedRegionColor**, **unselectedRegionColor** in **navigatorStyleSettings** and the thumb of the slider using **thumbColor, thumbRadius** and **thumbStorke** in **navigatorStyleSettings.  majorGridLineStyle** and **minorGridLineStyle**  are used to customize the grid line color and visibility.

{% highlight js %}

**[JS]**
$("#rangecontainer").ejRangeNavigator(
               {   
                   // ...    
                   //  To customize the navigator element     
                  navigatorStyleSettings: {

             unselectedRegionColor: "white",
             selectedRegionColor: "#5EABDE",
             thumbColor: "white",
             thumbRadius: 10,
             thumbStroke: "#303030",
             background: "transparent",
             border: { color: "black", width: 3 },
             majorGridLineStyle: { color: "transparent" },
             minorGridLineStyle: { color: "transparent" }
         },
               //  To customize the labels
   labelSettings: {

         higherLevel: {
                        style: {
                                font: { color: 'black', size: '13px', opacity: 1}, 
                                horizontalAlignment: "left"
                        },
                        intervalType: 'years',
                        labelPlacement: "inside"
                    },
         lowerLevel: {
                      style: { 
                             font: { color: 'black', size: '12px', opacity: 1  },  
                             horizontalAlignment: "center"
                          },
                        intervalType: 'quarters',
                        labelPlacement: "inside"
                    }
                },

                // ...             

                    });
        });



{% endhighlight %}



{% include image.html url="\js\RangeNavigator\-concepts-and-features_images\-concepts-and-features_img17.png" Caption="Figure 22: Customize RangeNavigator"%}

#### Themes

**RangeNavigator** theme is a set of pre-defined options that are applied to the control before each **RangeNavigator** is instantiated. Following predefined themes are available in JavaScript **RangeNavigator**.

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

11. gradientazure

12. gradientazuredark

13. gradientlime

14. gradientlimedark

15. gradientsaffron

16. gradientsaffrondark


{% highlight js %}

**[JS]**
$("#rangecontainer").ejRangeNavigator(
               {   
                   // ...              
                      theme: 'azuredark',
                   // ...             
               });


{% endhighlight %}



{% include image.html url="\js\RangeNavigator\-concepts-and-features_images\-concepts-and-features_img18.png" Caption="Figure 23: Themes"%}

### Tooltip

**RangeNavigator** provides **Tooltip** support for sliders. Sliders are used to select data at particular range in the **RangeNavigator** control. **Tooltips** for sliders display the selected start and end **DateTime** values.

#### Customization

**RangeNavigator** provides support for you to customize the text display in the tooltip and background using **tooltipSettings** property. You can change font family, font color, font style, font weight. By default “**Segoe UI**” font family is set to tooltip text.


{% highlight js %}

**[JS]**
$("#rangecontainer").ejRangeNavigator(
               {   
                   // ...              
                tooltipSettings: {
                    visible: true,  
                    backgroundColor: "black",
                           //  To customize the tooltip text

                        font: {
                            color: 'red',
                            family: 'Segoe UI',
                            style: 'Normal',
                            size: '12px',
                            opacity: 1,
                            weight: 'regular'
                        }

                },
                   // ...             
               });


{% endhighlight %}



{% include image.html url="\js\RangeNavigator\-concepts-and-features_images\-concepts-and-features_img19.png" Caption="Figure 24: Tool Tip"%}

#### Label Format

By default, the **tooltip** texts are automatically determined based on the data points.  To make it readable and understandable you can format the **tooltip** text. For **DateTime** data, all globalized format are supported. By default the **labelFormat** is "MM/dd/yyyy".

Some of the **labelFormat** for **DateTime** data area as follows:

* 'MMM, yyyy'

* 'dd, MMM'

* 'dd/MM/yyyy'

* 'dd, hh:mm'

* 'hh:mm:ss'

* 'hh:mm:ss:tt'


{% highlight js %}

**[JS]**
$("#rangecontainer").ejRangeNavigator({
               {   
                   // ...              
                 tooltipSettings: {
                    labelFormat:'MMM, yyyy',
                },              
                   // ...             
               });


{% endhighlight %}


{% include image.html url="\js\RangeNavigator\-concepts-and-features_images\-concepts-and-features_img20.png" Caption="Figure 25: labelFormat"%}

#### Tooltip display mode

By default the **tooltip** for RangeNavigator gets displayed. You can change this behavior using the **tooltipDisplayMode** property in the tooltip and it takes the following values.

_Table_ _1__: Tooltip values_

<table>
<tr>
<td>
<b>Value</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
always</td><td>
Tooltip get displayed for RangeNavigator always.</td></tr>
<tr>
<td>
ondemand</td><td>
Tooltip get displayed only when we move the slider.</td></tr>
</table>


{% highlight js %}

**[JS]**
$("#rangecontainer").ejRangeNavigator({
               {   
                   // ...              
                 tooltipSettings: {
                         tooltipDisplayMode: "ondemand",                    
                },              
                   // ...             
               });


{% endhighlight %}



{% include image.html url="\js\RangeNavigator\-concepts-and-features_images\-concepts-and-features_img21.png" Caption="Figure 26: Tool Tip display mode"%}

### Globalization & Localization

**RangeNavigator** supports Localization and Globalization to customize the labels based on a culture specific to a country. The culture defines specific information for the number formats, week and month names, date and time formats etc. 

#### Localization

**Localization** is the process of customizing the user interface based on a culture specific to a particular country or region in order to display regional data.  The culture is represented by a unique string, for example, ―en-US‖ for U.S. English and ―fr-FR‖ for French (common), this is achieved by creating a javascript file “**rangeNavigatorSource.fr-FR.js**” and setting the equivalent word as illustrated in the following code sample.



{% highlight js %}

ej.datavisualization.RangeNavigator.locale["fr-FR"] = {

    intervals: {
        //string to display the intervals on RangeNavigator
        quarter: {longQuarters: "Trimestre", shortQuarters: "T"},
        week: { longWeeks: "Semaine", shortWeeks: "S" }
    }
}


{% endhighlight %}

**Localization** is the key feature that provides solutions globally with the help of localized control. 

{% highlight js %}

**[JS]**
$("#rangecontainer").ejRangeNavigator({
               {   
                   // ...              
                   locale: 'fr-FR',
                   // ...             
               });


{% endhighlight %}



{% include image.html url="\js\RangeNavigator\-concepts-and-features_images\-concepts-and-features_img22.png" Caption="Figure 27: Locialization"%}

#### RTL

**Right-to-Left** or **RTL** describes the ability of application to handle and responds you to communicate with a right-to-left language, like Arabic or Japanese. **enableRTL** property is used to change the rendering format  to **"Right to Left"**, by default it renders from **"Left to Right"** in **RangeNavigator**.

{% highlight js %}

**[JS]**
$("#rangecontainer").ejRangeNavigator({
               {   
                   // ...              
                   enableRTL:true,
                  // ...             
               });


{% endhighlight %}



{% include image.html url="\js\RangeNavigator\-concepts-and-features_images\-concepts-and-features_img23.png" Caption="Figure 28: RTL"%}



