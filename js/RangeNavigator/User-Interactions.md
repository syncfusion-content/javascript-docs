---
layout: post
title: UserInteraction
description: How to enable and cutomize the scrollbar, selection and highlighting in Essential JavaScript RangeNavigator.
platform: js
control: RangeNavigator
documentation: ug
api: /api/js/ejrangenavigator
---

# User Interactions

## Highlight

EjRangeNavigator provides highlighting supports to the intervals on mouse hover. To enable the highlighting option, set the [`enable`](../api/ejrangenavigator#members:navigatorstylesettings-highlightsettings-enable) property to true in the [`highlightSettings`](../api/ejrangenavigator#members:navigatorstylesettings-highlightsettings) of [`navigatorStyleSettings`](../api/ejrangenavigator#members:navigatorstylesettings).

{% highlight javascript %}

    $("#container").ejRangeNavigator({   
     
         //...   
         navigatorStyleSettings:{
                //...        
              highlightSettings:{
                   // enable the highlight settings
                   enable: true                                
              }    
              //...
          }
          // ...             
     });

{% endhighlight %}


![](/js/RangeNavigator/User-Interactions_images/User-Interactions_img1.png) 


[Click](http://js.syncfusion.com/demos/web/#!/azure/rangenavigator/highlight) here to view the highlight and selections online demo sample.

### Customize the highlight style

To customize the highlighted intervals, use [`color`](../api/js/ejrangenavigator#members:navigatorstylesettings-highlightsettings-color), [`border`](../api/js/ejrangenavigator#members:navigatorstylesettings-highlightsettings-border) and [`opacity`](../api/js/ejrangenavigator#members:navigatorstylesettings-highlightsettings-opacity) options in the [`highlightSettings`](../api/ejrangenavigator#members:navigatorstylesettings-highlightsettings).

To customize border of highlighted interval, use [`color`](../api/js/ejrangenavigator#members:navigatorstylesettings-highlightsettings-border-color) and [`width`](../api/js/ejrangenavigator#members:navigatorstylesettings-highlightsettings-border-width) options in border.

{% highlight javascript %}

    $("#container").ejRangeNavigator({   
     
         //...   
         navigatorStyleSettings:{
                //...        
                highlightSettings:{
                    // enable the highlight settings
                    enable: true,         
                    // customizing style
                    color: '#006fa0',  
                    opacity: 0.8,     
                    border:{
                        color: 'red' , width: 2
                      }        
              }
              //...
         }
         // ...             
     });


{% endhighlight %}

![](/js/RangeNavigator/User-Interactions_images/User-Interactions_img2.png)


## Selection

EjRangeNavigator provides selection supports to the intervals by, clicking and dragging the highlighted intervals. To enable the selection option, set the [`enable`](../api/ejrangenavigator#members:navigatorstylesettings-selectionsettings-enable) property to true in the [`selectionSettings`](../api/ejrangenavigator#members:navigatorstylesettings-selectionsettings).

{% highlight javascript %}

    $("#container").ejRangeNavigator({   
     
         //...   
         navigatorStyleSettings:{
                //...        
              selectionSettings:{
                   // enable the selection settings
                   enable: true                                
              }    
              //...
          }
          // ...             
     });

{% endhighlight %}


![](/js/RangeNavigator/User-Interactions_images/User-Interactions_img3.png) 


[Click](http://js.syncfusion.com/demos/web/#!/azure/rangenavigator/highlight) here to view the highlight and selections online demo sample.

### Customize the selection style

To customize the selected intervals, use [`color`](../api/js/ejrangenavigator#members:navigatorstylesettings-selectionsettings-color), [`border`](../api/js/ejrangenavigator#members:navigatorstylesettings-selectionsettings-border) and [`opacity`](../api/js/ejrangenavigator#members:navigatorstylesettings-selectionsettings-opacity) options in the selectionSettings.

To customize border of selected interval, use [`color`](../api/js/ejrangenavigator#members:navigatorstylesettings-selectionsettings-border-color) and [`width`](../api/js/ejrangenavigator#members:navigatorstylesettings-selectionsettings-border-width) options in border.

{% highlight javascript %}

    $("#container").ejRangeNavigator({   
     
         //...   
         navigatorStyleSettings:{
                //...        
                selectionSettings: {
                    // enable the selection settings
                    enable: true,         
                    // customizing style
                    color: '#27e8e5',  
                    opacity: 0.4,     
                    border:{
                         color: 'red' , width: 2
                       }
                  //...
              }
         // ...             
     });


{% endhighlight %}

![](/js/RangeNavigator/User-Interactions_images/User-Interactions_img4.png)


## Scrollbar

* To render the Scrollbar in RangeNavigator, you need to enable [`enableScrollbar`](../api/ejrangenavigator#members:enablescrollbar) option.
 
* [`scrollRangeSettings`](../api/ejrangenavigator#members:scrollrangesettings) of  rangenavigator [`start`](../api/ejrangenavigator#members:scrollrangesettings-start) and [`end`](../api/ejrangenavigator#members:scrollrangesettings-end) value is used to set the minimum and maximum datasource value to be added in the rangenavigator.
 
* Based on the scrollRangeSettings *start, end* value and dataSource *start, end* value scrollbar will be adjust.

* When you change the scrollbar position, [`scrollEnd`](../api/ejrangenavigator#events:scrollend) event returns the current position of start and end range value.

{% highlight javascript %}

    $("#scroll").ejRangeNavigator({
          
         //...
         //Enable scrollbar option in the rangenavigator
          enableScrollbar: true,
         //Maximum data to be displayed in the rangenavigator control
         scrollRangeSettings: {
               start: new Date(2010, 0, 1),
               end: new Date(2011, 10, 31)
           },
           
         //Subscribe the event on scrollbar position changed           
         scrollEnd: "onScrollbarChange"
         
         //...
     });

      function onScrollbarChange(sender) {
            var start  = sender.data.newRange.start;
            var end  = sender.data.newRange.end;
      }

{% endhighlight %}

![](/js/RangeNavigator/User-Interactions_images/User-Interactions_img5.png)

[Click](http://js.syncfusion.com/demos/web/#!/azure/rangenavigator/scrollbar) here to view scrollbar online demo sample.