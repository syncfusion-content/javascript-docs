---
layout: post
title: Chart Striplines
description: Learn how to add horizontal or vertical lines in Chart.                                                  
platform: js
control: Chart
documentation: ug
api : /api/js/ejchart
---

# Striplines

EjChart supports horizontal and vertical striplines. 

## Horizontal Stripline

You can create horizontal stripline by adding the [`stripline`](../api/ejchart#members:primaryyaxis-stripline) in the **vertical axis** and set [`visible`](../api/ejchart#members:primaryxaxis-stripline-visible) option to **true**. Striplines are rendered in the specified **start** to **end** range and you can add more than one stripline for an axis.


{% highlight javascript %}

     $("#container").ejChart({
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

![](/js/Chart/Striplines_images/Striplines_img1.png)


[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/chartaxes/striplines) here to view the Striplines online demo sample.


## Vertical Stripline

You can create vertical stripline by adding the [`stripline`](../api/ejchart#members:primaryxaxis-stripline) in the **horizontal axis** and set [`visible`](../api/ejchart#members:primaryyaxis-stripline-visible) option to **true**.  


{% highlight javascript %}

     $("#container").ejChart({
          // ...

          //Initializing Primary X Axis
           primaryXAxis: {
               // ...
                stripLine: [
                     //Create vertical Stripline using horizontal Axis
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

![](/js/Chart/Striplines_images/Striplines_img2.png)


## Customize the Text

To customize the stripLine text, use the [`text`](../api/ejchart#members:primaryyaxis-stripline-text) and [`font`](../api/ejchart#members:primaryyaxis-stripline-font) options. 

{% highlight javascript %}

     $("#container").ejChart({
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

![](/js/Chart/Striplines_images/Striplines_img3.png)
	

**Text Alignment**

Stripline text can be aligned by using the [`textAlignment`](../api/ejchart#members:primaryyaxis-stripline-textalignment) property.  

{% highlight javascript %}

     $("#container").ejChart({
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

![](/js/Chart/Striplines_images/Striplines_img4.png)


## Customize the Stripline

To customize the stripLine styles, use the [`color`](../api/ejchart#members:primaryyaxis-stripline-color), [`opacity`](../api/ejchart#members:primaryyaxis-stripline-opacity), [`borderWidth`](../api/ejchart#members:primaryyaxis-stripline-borderwidth) and [`borderColor`](../api/ejchart#members:primaryyaxis-stripline-bordercolor) properties. 

{% highlight javascript %}

     $("#container").ejChart({
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

![](/js/Chart/Striplines_images/Striplines_img5.png)


## Change the Z-order of the stripline

Stripline [`zIndex`](../api/ejchart#members:primaryyaxis-stripline-zindex) property is used to display the stripLine either behind or over the series.  

{% highlight javascript %}

     $("#container").ejChart({
          // ...

        //Initializing Primary Y Axis
        primaryYAxis: {
               // ...
                stripLine: [{
                        //Change stripLine zIndex
                        zIndex: 'over',
                        // ...
                       }],
           },
        // ...
      });


{% endhighlight %}

![](/js/Chart/Striplines_images/Striplines_img6.png)
