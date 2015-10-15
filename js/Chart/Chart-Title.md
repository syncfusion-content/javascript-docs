---
layout: post
title: Chart-Title
description: chart title
platform: js
control: Chart
documentation: ug
---

# Chart Title & Subtitle

## Title

By using the title option, you can add the [text](../api/ejchart.html#members:title-text) as well as customize its [font](../api/ejchart.html#members:title-font).

{% highlight js %}


    $("#chartcontainer").ejChart({
    
          // ...  
          title: {
                //Adding text to chart title   
                text: 'Efficiency of oil-fired power production ',
                 //Customizing Chart title font
                 font:{
                         opacity: 1,
                          fontFamily: "Arial",
                          fontStyle: 'italic',
                          fontWeight: 'bold',
                          color: "#E27F2D",
                          size: '23px'
                 },
            },
        // ...
        
    });


{% endhighlight %}

{% include image.html url="/js/Chart/Chart-Title_images/Chart-Title_img1.png" Caption="Chart with title"%}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/chartcustomization/subtitle) here to view the Chart Title online demo sample.


### Title Alignment

You can change the title alignment to *center*, *far* and *near* by using the [textAlignment](../api/ejchart.html#members:title-textalignment) property of the chart title. 

{% highlight js %}


    $("#chartcontainer").ejChart({
           
          //  ...
          
           title: {
                //Change title text alignment
                textAlignment: "near",
                //...
            }          

            //  ...   
      });


{% endhighlight %} 

{% include image.html url="/js/Chart/Chart-Title_images/Chart-Title_img2.png" Caption="Title text alignment"%}


## Add Subtitle to the chart

By using the subTitle option, you can add the [subTitle](../api/ejchart.html#members:title-subtitle) to the chart title and customize its [font](../api/ejchart.html#members:title-subtitle-font). 

{% highlight js %}


    $("#chartcontainer").ejChart({
    
           //  ...  
           title: {
              // ...
              subTitle: {
                  //Add subtitle to chart title
                  text: "( in a week )",
                  //Customizing Chart title font
                  font:{
                       opacity: 1,
                       fontFamily: "Arial",
                       fontStyle: 'italic',
                       fontWeight: 'bold',
                       color: "#E27F2D",
                       size: '12px'
                    },
                }
            }            
            //  ...   
      });


{% endhighlight %}

{% include image.html url="/js/Chart/Chart-Title_images/Chart-Title_img3.png" Caption="Title and SubTitle"%}


### Subtitle Alignment

You can change the subtitle alignment to *center*, *far* and *near* by using the [textAlignment](../api/ejchart.html#members:title-subtitle-textalignment) property of the subTitle.

{% highlight js %}


    $("#chartcontainer").ejChart({
    
        //  ...  
        title: {                
             // ...
             subTitle:{
                 //Change subtitle to text aligment
                 textAlignment: "center",		
                 // ...
               }
         }
            
            //  ...   
      });


{% endhighlight %}

{% include image.html url="/js/Chart/Chart-Title_images/Chart-Title_img4.png" Caption="Subtitle text alignment"%}

