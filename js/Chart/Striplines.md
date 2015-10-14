---
layout: post
title: Striplines
description: striplines                                                   
platform: js
control: Chart
documentation: ug
---

# Striplines

EjChart supports horizontal and vertical striplines. 

## Horizontal Stripline

You can create horizontal stripline by adding [stripline](../api/ejchart#members:primaryyaxis-stripline) in the **vertical axis** and set [visible](../api/ejchart#members:primaryxaxis-stripline-visible) option as **true**. Striplines will be rendering in the specified **start** to **end** range and you can add more than one stripline for an axis.


{% highlight js %}

     $("#chartcontainer").ejChart({
          // ...

          //Initializing Primary Y Axis
          primaryYAxis: {
               // ...
                stripLine: [
                     //Create horizontal Stripline using vertical Axis
                     {
                       //Enable Stripline
                       visible: true,
                       start: 30,
                       end: 40,
                      },
                      // ...
                   ],
               },
           // ...
      });


{% endhighlight %}

{% include image.html url="/js/Chart/Striplines_images/Striplines_img1.png" Caption="Horizontal Striplines"%}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/chartaxes/striplines) here to view the Striplines online demo sample.


## Vertical Stripline

You can create vertical stripline by adding [stripline](../api/ejchart#members:primaryxaxis-stripline) in the **horizontal axis** and set [visible](../api/ejchart#members:primaryyaxis-stripline-visible) option as **true**.  


{% highlight js %}

     $("#chartcontainer").ejChart({
          // ...

          //Initializing Primary X Axis
           primaryXAxis: {
               // ...
                stripLine: [
                     //Create horizontal Stripline using horizontal Axis
                       {
                         //Enable Stripline
                         visible: true,
                         start: 3,
                         end: 7,
                       },
                     // ...
                     ],
                },

             // ...
      });


{% endhighlight %}

{% include image.html url="/js/Chart/Striplines_images/Striplines_img2.png" Caption="Vertical Striplines"%}


## Customizing Text

For customizing the stripLine text, use [text](../api/ejchart#members:primaryyaxis-stripline-text) and [font](../api/ejchart#members:primaryyaxis-stripline-font) options. 

{% highlight js %}

     $("#chartcontainer").ejChart({
          // ...

          //Initializing Primary Y Axis
          primaryYAxis: {
               // ...
                stripLine: [{
                  //Customize the stripLine text and font styles
                   text: 'High Temperature',
                   font: { size: '18px', color: 'white' }      
                   // ...                         
               }],
           },
        // ...
      });


{% endhighlight %}

{% include image.html url="/js/Chart/Striplines_images/Striplines_img3.png" Caption="Customize stripline text"%}	

**Text Alignment**

Stripline text can be aligned using [textAlignment](../api/ejchart#members:primaryyaxis-stripline-textalignment) property.  

{% highlight js %}

     $("#chartcontainer").ejChart({
          // ...

          //Initializing Primary Y Axis
          primaryYAxis: {
               // ...
                stripLine: [{
                    //Set stripLine text alignment to top position
                    textAlignment: 'middletop',        
                   // ...                         
               }],
           },
        // ...
      });


{% endhighlight %}

{% include image.html url="/js/Chart/Striplines_images/Striplines_img4.png" Caption="Stripline text alignment"%}


## Customizing Stripline

For customizing the stripLine styles, use [color](../api/ejchart#members:primaryyaxis-stripline-color), [opacity](../api/ejchart#members:primaryyaxis-stripline-opacity), [borderWidth](../api/ejchart#members:primaryyaxis-stripline-borderwidth) and [borderColor](../api/ejchart#members:primaryyaxis-stripline-bordercolor) properties. 

{% highlight js %}

     $("#chartcontainer").ejChart({
          // ...

        //Initializing Primary Y Axis
        primaryYAxis: {
               // ...
                stripLine: [{
                         //Customize the StripLine rectangle
                         color: '#33CCFF',
                         borderWidth: 2,
                         opacity: 0.5,
                         borderColor: 'red',  
                         // ...
                       }],
           },
        // ...
      });


{% endhighlight %}

{% include image.html url="/js/Chart/Striplines_images/Striplines_img5.png" Caption="Customize stripline rectangle"%}


## Changing the zorder of stripline

Stripline [zIndex](../api/ejchart#members:primaryyaxis-stripline-zindex) property is used to display the stripLine either behind or over of the series.  

{% highlight js %}

     $("#chartcontainer").ejChart({
          // ...

        //Initializing Primary Y Axis
        primaryYAxis: {
               // ...
                stripLine: [{
                        //Change stripLine zIndex
                        zindex: 'over',
                        // ...
                       }],
           },
        // ...
      });


{% endhighlight %}

{% include image.html url="/js/Chart/Striplines_images/Striplines_img6.png" Caption="Stripline zIndex"%} 
