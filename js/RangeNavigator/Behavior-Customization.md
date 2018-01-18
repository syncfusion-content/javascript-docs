---
layout: post
title: Behavior-Customization
description: Behavior Customization
platform: js
control: RangeNavigator
documentation: ug
api: /api/js/ejrangenavigator
---

## Behavior Customization

**RangeNavigator** allows you to customize the control using events. You can change the range for selected data of the **RangeNavigator** using events.

#### Deferred update

If you set [`enableDeferredUpdate`](../api/ejrangenavigator#members:enabledeferredupdate)to true, the [`rangeChanged`](../api/ejrangenavigator#events:rangechanged) event gets fired after dragging and dropping the slider. By default the [`enableDeferredUpdate`](../api/ejrangenavigator#members:enabledeferredupdate)is true. If [`enableDeferredUpdate`](../api/ejrangenavigator#members:enabledeferredupdate)is false then the [`rangeChanged`](../api/ejrangenavigator#events:rangechanged) event gets fired while dragging the slider.


{% highlight javascript %}


$("#container").ejRangeNavigator(
   //...
        enableDeferredUpdate: true,
   //...	
  });


{% endhighlight %}


![](/js/RangeNavigator/Behavior-Customization_images/Behavior-Customization_img1.png)

## Methods 

#### Use of destroy method 

[`_destroy`](../api/ejrangenavigator#methods:_destroy) method is used to destroy the **RangeNavigator** widget. 

{% highlight html %}
<div id="container"></div>
<script type="text/javascript" language="javascript">
    // Destroy range navigator
    var obj = $("#container").data("ejRangeNavigator");
    obj.destroy(); // destroy the range navigator
</script>

{% endhighlight %}

## Handle Events

#### load

[`load`](../api/ejrangenavigator#events:load) event is fired when **RangeNavigator** is loading. A parameter **sender** is passed to the handler. Using **sender.model**, you can access the RangeNavigator properties. 

{% highlight javascript %}


    $("#container").ejRangeNavigator({
    // ...             
    load: function(sender) {
        sender.model.allowSnapping = true;
    },
    //...
    });
    });


{% endhighlight %}

#### loaded

[`loaded`](../api/ejrangenavigator#events:loaded) event is handled when the **RangeNavigator** gets loaded. A parameter **sender** is passed to the handler. Using **sender.model**, you can access the RangeNavigator properties. 

{% highlight javascript %}


    $("#container").ejRangeNavigator({
    // ...             
    loaded: function(sender) {
        sender.model.isResponsive = false;
    },
    //...
    });
    });


{% endhighlight %}

#### rangeChanged

[`rangeChanged`](../api/ejrangenavigator#events:rangechanged)event gets fired whenever the selected range changes in **RangeNavigator**. A parameter **sender** is passed to the handler. Using sender.selectedRangeSettings, you can access the start and end value of range for the selected region. The [`selectedData`](../api/ejrangenavigator#members:selecteddata) can be obtained when this event is triggered from client side.

{% highlight javascript %}


    $("#container").ejRangeNavigator({
    // ...             
    rangeChanged: function(sender) {
        console.log(sender.selectedRangeSettings.start);
    },
    // ...             
    });
    });


{% endhighlight %}

#### selectedRangeStart

[`selectedRangeStart`](../api/ejrangenavigator#events:selectedrangestart) event is fired when starting to change the slider position in **RangeNavigator**. A parameter **sender** is passed to the handler. Using sender.selectedRangeSettings, you can access the start value of range for the selected region. 

{% highlight javascript %}


    $("#container").ejRangeNavigator({
    // ...             
    selectedRangeStart: function(sender) {
        console.log(sender.selectedRangeSettings.start);
    },
    // ...             
    });
    });


{% endhighlight %}

#### selectedRangeEnd

[`selectedRangeEnd`](../api/ejrangenavigator#events:selectedrangeend) event is fired when selection ends in **RangeNavigator**. A parameter **sender** is passed to the handler. Using sender.selectedRangeSettings, you can access the end value of range for the selected region. 

{% highlight javascript %}


    $("#container").ejRangeNavigator({
    // ...             
    selectedRangeEnd: function(sender) {
        console.log(sender.selectedRangeSettings.end);
    },
    // ...             
    });
    });


{% endhighlight %}

#### scrollStart

[`scrollStart`](../api/ejrangenavigator#events:scrollstart) event is fired when starting to change the scrollbar position of **RangeNavigator**. A parameter **sender** is passed to the handler. Using sender.data startRange and sender.data endRange, you can access the scrollbar position starting and ending range value on changed scrollbar. 

{% highlight javascript %}


    $("#container").ejRangeNavigator({
    // ...             
    scrollStart: function(sender) { },
    // ...             
    });
    });


{% endhighlight %}

#### scrollEnd

[`scrollEnd`](../api/ejrangenavigator#events:scrollend) event is fired while ending the change in scrollbar position of **RangeNavigator**. A parameter **sender** is passed to the handler. Using data oldRange and data newRange, you can access the scrollbar position old and new range values on changing scrollbar. 

{% highlight javascript %}


    $("#container").ejRangeNavigator({
    // ...             
    scrollEnd: function(sender) { },
    // ...             
    });
    });

{% endhighlight %}

#### scrollChanged

[`scrollChanged`](../api/ejrangenavigator#events:scrollchanged) event is fired when changing the scrollbar position of **RangeNavigator**. A parameter **sender** is passed to the handler. Using data oldRange and data newRange, you can access the old and new range values of changed scrollbar position. 

{% highlight javascript %}


    $("#container").ejRangeNavigator({
    // ...             
    scrollChanged: function(sender) { },
    // ...             
    });
    });

{% endhighlight %}

### Click

[`click`](../api/ejrangenavigator#events:click) event is handled when the **RangeNavigator** gets clicked. A parameter **sender** is passed to the handler. Using **sender.model**, you can access the RangeNavigator properties. 


{% highlight js %}
 
//Click event for range navigator

$("#container").ejRangeNavigator({

    click: function (args) {
              //Do something
    }
   
});

{% endhighlight %}


### doubleClick

[`doubleClick`](../api/ejrangenavigator#events:doubleclick) event is handled when the **RangeNavigator** gets clicked. A parameter **sender** is passed to the handler. Using **sender.model**, you can access the RangeNavigator properties. 


{% highlight js %}
 
//DoubleClick event for range navigator.

$("#container").ejRangeNavigator({

    doubleClick: function (args) {
              //Do something
    }
   
});

{% endhighlight %}



### rightClick

[`rightClick`](../api/ejrangenavigator#events:rightclick) event is handled when the **RangeNavigator** gets clicked. A parameter **sender** is passed to the handler. Using **sender.model**, you can access the RangeNavigator properties. 


{% highlight js %}
 
//RightClick event for range navigator

$("#container").ejRangeNavigator({
    rightClick: function (args) {
              //Do something
    }
   
});

{% endhighlight %}



## Use of ZoomCoordinates

**RangeNavigator** is used along with the controls like chart and grid to view the selected data. To update chart/grid, whenever the selected range changes in **RangeNavigator**, you can use [`rangeChanged`](../api/ejrangenavigator#events:rangechanged) event of **RangeNavigator** and then update the chart/grid with the selected data in this event. 

You can easily update the data for chart by assigning the [`zoomFactor`](../api/ejrangenavigator#members:zoomsettings-zoomfactor) and [`zoomPosition`](../api/ejrangenavigator#members:zoomsettings-zoomposition) of the **RangeNavigator** to the chart axis.

{% highlight javascript %}


    $("#container").ejRangeNavigator({
    // ...             
    rangeChanged: onChartLoaded
        // ...             
    });
    });
    // setting zoom factor and position for chart axis in rangeChanged event.
    function onChartLoaded(sender) {
        var chartObj = $("#container").data("ejChart");
        if (chartObj != null) {
            chartObj.model.axes[0].zoomPosition = sender.zoomPosition;
            chartObj.model.axes[0].zoomFactor = sender.zoomFactor;
        }
        $("#container").ejChart("redraw");
    }


{% endhighlight %}



![](/js/RangeNavigator/Behavior-Customization_images/Behavior-Customization_img2.png) 

## Thumb Template

You can customize Thumb template by using [`leftThumbTemplate`](../api/ejrangenavigator#members:navigatorstylesettings-leftthumbtemplate) and [`rightThumbTemplate`](../api/ejrangenavigator#members:navigatorstylesettings-rightthumbtemplate) property. You can add the required template as a "div" element with an "id" to the web page and assign the id or assign the HTML string to this property under [`navigatorStyleSettings`](../api/ejrangenavigator#members:navigatorstylesettings).

{% highlight html %}

 
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
                $("#scroll").ejRangeNavigator({
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

![](/js/RangeNavigator/Behavior-Customization_images/Behavior-Customization_img3.png) 

## Value Axis Settings

You can customize the line, [`font`](../api/ejrangenavigator#members:valueaxissettings-font) [`size`](../api/ejrangenavigator#members:valueaxissettings-font-size), gridline, tickline, range, [`rangePadding`](../api/ejrangenavigator#members:valueaxissettings-rangepadding) and visibility of **RangeNavigator** axis.

To enable the visibility of axis line, you need to set [`visible`](../api/ejrangenavigator#members:valueaxissettings-axisline-visible) property of [`axisLine`](../api/ejrangenavigator#members:valueaxissettings-axisline) in [`valueAxisSettings`](../api/ejrangenavigator#members:valueaxissettings). 

You can customize the axis range by specifying [`min`](../api/ejrangenavigator#members:valueaxissettings-range-min), [`max`](../api/ejrangenavigator#members:valueaxissettings-range-max) and [`interval`](../api/ejrangenavigator#members:valueaxissettings-range-interval) for [`range`](../api/ejrangenavigator#members:valueaxissettings-range) property.

The [`majorGridLines`](../api/ejrangenavigator#members:valueaxissettings-majorgridlines) can be enabled by specifying [`visible`](../api/ejrangenavigator#members:valueaxissettings-majorgridlines-visible) property. The [`size`](../api/ejrangenavigator#members:valueaxissettings-majorticklines-size), [`width`](../api/ejrangenavigator#members:valueaxissettings-majorticklines-width) and [`visible`](../api/ejrangenavigator#members:valueaxissettings-majorticklines-visible) property of [`majorTickLines`](../api/ejrangenavigator#members:valueaxissettings-majorticklines) is used to customize the axis tick lines.

The visibility of valueAxisSettings is enabled by setting [`visible`](../api/ejrangenavigator#members:valueaxissettings-visible) property as true. 

{% highlight javascript %}

$("#container").ejRangeNavigator({
               {   
                   // ...              
                valueAxisSettings:
                        {
                            axisLine: {visible: true},
                            font: {size: '12px'},
                            majorGridLines: {visible: true},
                            majorTickLines: {size: 3, visible:false, width:3},
                            range:{ min :0 , max :100, interval :10},
                            rangePadding: "normal",
                            visible: true
                        }
                   // ...             
               });

{% endhighlight %}

## Selected Range Settings

The start and end range values of selected range can be customized using [`start`](../api/ejrangenavigator#members:selectedrangesettings-start) and [`end`](../api/ejrangenavigator#members:selectedrangesettings-end) property of [`selectedRangeSettings`](../api/ejrangenavigator#members:selectedrangesettings).

{% highlight javascript %}

$("#container").ejRangeNavigator({
               {   
                   // ...              
                selectedRangeSettings:
                        {
                            start:"01/05/1992",
                            end:"01/05/1993"
                        },
                   // ...             
               });

{% endhighlight %}


