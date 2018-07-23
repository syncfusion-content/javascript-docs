---
layout: post
title: Getting Started for Essential JavaScript Chart
description: How to create a chart, add series, enable tooltip and other features in Chart.
platform: js
control: Chart
documentation: ug
api : /api/js/ejchart
---

# Getting Started

This section explains you the steps required to populate the Chart with data, add data labels, tooltips and title to the Chart. This section covers only the minimal features that you need to know to get started with the Chart.

## Adding script reference

Create an **HTML** page and add the scripts references in the order mentioned in the following code example.

{% highlight html %}


<!DOCTYPE html>
<html>
<head>
    <!--  jquery script  -->
    <script src="https://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <!-- Essential JS UI widget -->
    <script src="https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
</head>
<body>
</body>
</html>



{% endhighlight %}

N> If you are using the Essential Studio below 13.4.0.53 version, then you need to refer **jQuery.globalize.js** script file along with the above references to render the Chart control.

In the above code, ej.web.all.min.js script reference has been added for demonstration purpose. It is not recommended to use this for deployment purpose, as its file size is larger since it contains all the widgets. Instead, you can use [`CSG`](http://csg.syncfusion.com/) utility to generate a custom script file with the required widgets for deployment purpose.

## Initialize chart

Add a *div* container to render the chart.

{% highlight html %}

<!DOCTYPE html>
<html>
<body>
      <div id="container" style="width: 820px; height: 500px;"></div>
</body>
</html>


{% endhighlight %}

Initialize the chart by using the ejChart method. The chart is rendered to the size of its container, by default. You can also customize the chart dimension either by setting the width and height of the container element as in the above code example or by using the [`size`](../api/ejchart.html#members:size) option of the Chart. Refer to the [`Chart Dimensions`](chart-dimensions.html) to know more about setting the [`size`]() of the chart.

{% highlight html %}

<!DOCTYPE html>
<html>
<body>
      <script type="text/javascript" language="javascript ">

            $(function () {
                $("#container").ejChart();
            });
      </script>
</body>
</html>


{% endhighlight %}

Now, the Chart is rendered with some auto-generated random values and with default Column chart type.

![](/js/Chart/Getting-Started_images/Getting-Started_img1.png)


## Populate chart with data

Now, this section explains how to plot JSON data to the Chart. First, let us prepare a sample JSON data with each object containing following fields – month and sales.

{% highlight javascript %}


  var chartData = [
      { month: 'Jan', sales: 35 },
      { month: 'Feb', sales: 28 },
      { month: 'Mar', sales: 34 },
      { month: 'Apr', sales: 32 },
      { month: 'May', sales: 40 },
      { month: 'Jun', sales: 32 },
      { month: 'Jul', sales: 35 },
      { month: 'Aug', sales: 55 },
      { month: 'Sep', sales: 38 },
      { month: 'Oct', sales: 30 },
      { month: 'Nov', sales: 25 },
      { month: 'Dec', sales: 32 }];


{% endhighlight %}

Add a series object to the chart by using the [`series`](../api/ejchart.html#members:series) option and set the chart type as *line* by using the [`type`](../api/ejchart#members:series-type) option. 

{% highlight javascript %}


     $("#container").ejChart({
            // ...      
            series: [{
		           // ...
		           // set series type
			       type: 'line'
	         }],
           // ...
    });


{% endhighlight %}

You can also add multiple series objects based on your requirement. Refer to the [`Chart Types`](Chart-Types.html) and [`Chart Series`](Chart-Series.html) sections to know more about chart types, how to add multiple series and customize series appearance.

Now, map the month and sales values in the data source to the line series by setting the [`xName`](../api/ejchart.html#members:series-xname) and [`yName`](../api/ejchart#members:series-yname) with the field names respectively and then set the actual data by using the *dataSource* option. Refer to the [`Data Binding`](working-with-data.html) section to know more about binding the local and remote data to the chart.

{% highlight javascript %}


     $("#container").ejChart({
            // ...      
            series: [{
		           // ...
		           //Set datasource, xName and yName 
                   dataSource: chartData, 
                   xName: "month", 
                   yName: "sales"
	         }],
           // ...
    });


{% endhighlight %}

![](/js/Chart/Getting-Started_images/Getting-Started_img2.png)


Since the data is related to sales, format the vertical axis labels by adding ‘$’ as a prefix and ‘K’ as a suffix to each label. This can be achieved by setting the "${value}K" to the [`labelFormat`](../api/ejchart#members:primaryxaxis-labelformat) option of the axis. Here, {value} acts as a placeholder for each axis label, "$" and "K" are the actual prefix and suffix added to each axis label. 

The following code example illustrates this,

{% highlight javascript %}


     $("#container").ejChart({
            // ... 
	        primaryYAxis:{
                //Customize the axis label format.
                labelFormat: '${value}K'
            },
	    // ...
    });


{% endhighlight %}

![](/js/Chart/Getting-Started_images/Getting-Started_img3.png)


Refer to the [`Axis`](Axis.html) section to know more about axis types, adding multiple axes and other customization options.

## Add Data Labels

You can add data labels to improve the readability of the chart. This can be achieved by enabling the [`visible`](../api/ejchart#members:series-marker-datalabel-visible) option in the [`dataLabel`](../api/ejchart#members:series-marker-datalabel    ) option. Now, the data labels are rendered at the top of all the data points.

The following code example illustrates this,



{% highlight javascript %}


     $("#container").ejChart({
            // ...      
            series: [{
		           // ....
		           marker: {
                         dataLabel: {
                                //Enable data label in the chart 
                                visible: true
                   } }
	         }],
           // ...
    });


{% endhighlight %}

![](/js/Chart/Getting-Started_images/Getting-Started_img4.png)


There are situations where the default label content is not sufficient to the user. In this case, you can use the [`template`](../api/ejchart#members:series-marker-datalabel-template) option to format the label content with some additional information.

 {% highlight html %}

<!DOCTYPE html>
<html>
<body>
      <div id="dataLabelTemplate" style="display:none; padding:3px;background-color:#B9C5C9; opacity:0.8;">
         <div id="point">#point.x#:$#point.y#K</div>
      </div>
</body>
</html>


{% endhighlight %}

The above HTML template is used as a template for each data label. Here, "point.x" and "point.y" are the placeholder text used to display the corresponding data point’s x & y value.

The following code example shows how to set the id of the above template to [`template`](../api/ejchart#members:series-marker-datalabel-template) option,

{% highlight javascript %}


     $("#container").ejChart({
            // ...      
            series: [{
		         // ...
		         marker: {
                     dataLabel: {
                         visible: true,
                         //Set the id of HTML template to the chart series
                         template: "dataLabelTemplate"
                         }
                       }	
                   }],
           // ...
    });


{% endhighlight %}

![](/js/Chart/Getting-Started_images/Getting-Started_img5.png)


Refer to the [`Data Markers`](Data-Markers.html) section to know more about the options available to customize it.

## Enable Legend

You can enable or disable the legend by using the [`visible`](../api/ejchart#members:legend-visible) option in the [`legend`](../api/ejchart#members:legend). It is enabled in the chart, by default.

{% highlight javascript %}


     $("#container").ejChart({
            // ...      
            //Initializing Series	
            series: [{
                // ...
                //Add series name to display on the legend item
                name: "Sales"
            }],

           legend: {
                //Enable chart legend
                visible: true
           },
           // ...
    });


{% endhighlight %}

![](/js/Chart/Getting-Started_images/Getting-Started_img6.png)


Refer to the [`Legend`](Legend.html) section to know more about how to position legend and customize its appearance.

## Enable Tooltip

The Tooltip is useful when you cannot display information by using the [`Data Labels`](data-markers.html#adding-labels) due to the space constraints. You can enable tooltip by using the [`visible`](../api/ejchart#members:series-tooltip-visible) option of the [`tooltip`](../api/ejchart#members:series-tooltip) in the specific series.

The following code example illustrates this,

{% highlight javascript %}


     $("#container").ejChart({
            // ...      
            //Initializing Series	
            series: [{
                   // ...
                   //Enable tooltip in chart area
                   tooltip: {visible: true}
            }],
           // ...
    });


{% endhighlight %}

![](/js/Chart/Getting-Started_images/Getting-Started_img7.png)


Refer to the [`Tooltip`](user-interactions.html) section to know more about formatting tooltip contents and customizing its appearance.

## Add Chart Title

You need to add a title to the chart to provide quick information to the user about the data being plotted in the chart. You can add it by using the [`text`](../api/ejchart#members:title-text) option of the [`title`](../api/ejchart#members:title).

{% highlight javascript %}


     $("#container").ejChart({
            // ...      
            title: {
	           //Add chart title
               text: 'Sales Analysis'			
	        },
           // ....
    });


{% endhighlight %}

![](/js/Chart/Getting-Started_images/Getting-Started_img8.png)


Refer to the [`Chart Title`](chart-title.html) section to know more about aligning title, customizing its appearance and adding subtitle to the chart.
