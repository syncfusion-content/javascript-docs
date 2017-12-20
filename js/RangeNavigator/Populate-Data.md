---
layout: post
title: Populate-Data
description: Populate Data
platform: js
control: RangeNavigator
documentation: ug
api: /api/js/ejrangenavigator
---

### Populate Data

When you provide data to **RangeNavigator**, it produces limited set of data. You can populate the **RangeNavigator** with data using the [`dataSource`](../api/ejrangenavigator#members:datasource) and [`series`](../api/ejrangenavigator#members:series) properties.

#### Add series to the RangeNavigator

The [`series`](../api/ejrangenavigator#members:series) property provides access to a collection of all series that are defined explicitly within a **RangeNavigator** control. Each series is assigned with [`type`](../api/ejrangenavigator#members:type) and name. It contains collection of data point, each point contains x value and y values. You can add data points to the series through [`dataSource`](../api/ejrangenavigator#members:datasource) property by providing field name to get the values from the dataSource in [`xName`](../api/ejrangenavigator#members:xname) and [`yName`](../api/ejrangenavigator#members:yname) options.

Animation can be enabled by setting [`enableAnimation`](../api/ejrangenavigator#members:enableAnimation) property as true and the series color can be customized by using [`fill`](../api/ejrangenavigator#members:fill) property in series. 

{% highlight javascript %}


$("#container").ejRangeNavigator({
   //...
    // Adding series
     series: [
                {
                  type: 'line',
                  dataSource: data.Open, xName: "XValue", yName: "YValue",                     
                  opacity: 0.5, fill: '#69D2E7',
                  enableAnimation: true,
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

![](/js/RangeNavigator/Populate-Data_images/Populate-Data_img1.png) 
