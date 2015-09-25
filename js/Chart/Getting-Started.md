---
layout: post
title: Getting-Started
description: getting started
platform: js
control: Chart
documentation: ug
---

# Getting Started

This section walks you through the steps required to populate the Chart with data, add data labels, tooltips and title to the Chart. This section covers only the minimal features that you need to know to get started with the Chart.

## Adding script reference

Create an **HTML** page and add the scripts references in the order mentioned in the following code snippet.

{% highlight html %}


<!DOCTYPE html>
<html>
<head>
    <!--  jquery script  -->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <!--  jquery localization dependency  -->
    <script src="http://ajax.aspnetcdn.com/ajax/globalize/0.1.1/globalize.min.js"></script>
    <!-- Essential JS UI widget -->
    <script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js"></script>
</head>
<body>
</body>
</html>



{% endhighlight %}

In the above code, ej.web.all.min.js script reference has been added for demonstration purpose. It is not recommended to use this for deployment purpose, as its file size is larger since it contains all the widgets. Instead, you can use [CSG](http://csg.syncfusion.com/) utility to generate a custom script file with the required widgets for deployment purpose.

## Initialize chart

Add a *div* container to render the chart.

{% highlight html %}

<!DOCTYPE html>
<html>
<body>
      <div id=”chartcontainer” style="width: 820px; height: 500px;"></div>
</body>
</html>


{% endhighlight %}

Next, initialize chart using ejChart method. By default, chart will be rendered to the size of its container. You can also customize chart dimension either by setting width and height for the container element as in the above code or using size option of Chart. Refer [Chart Dimensions](chart-dimensions.html) to know more about setting size for chart.

{% highlight html %}

<!DOCTYPE html>
<html>
<body>
      <script type="text/javascript" language="javascript ">

            $(function () {
                $("#chartcontainer").ejChart();
            });
      </script>
</body>
</html>


{% endhighlight %}

Now, the Chart will be rendered with some auto-generated random values and with default Column chart type.

{% include image.html url="/js/Chart/Getting-Started_images/Getting-Started_img1.png" Caption="Chart"%}

## Populate chart with data

Now, let’s see how to plot JSON data to the Chart. First, let us prepare a sample JSON data with each object containing following fields – month and sales.

{% highlight js %}


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

Add a series object to the chart using *series* option and set the chart type as *line* using *type* option. 

{% highlight js %}


     $("#chartcontainer").ejChart({
            // ...      
            series: [{
		           // ...
		           // set series type
			       type: 'line'
	         }],
           // ...
    });


{% endhighlight %}

You can also add multiple series objects based on your requirement. Refer [Chart Types](Chart-Types.html) and [Chart Series](Chart-Series.html) sections to know more about chart types, how to add multiple series and customize series appearance.

Next, map the month and sales values in the data source to the line series by setting *xName* and *yName* with the field names respectively, and then set the actual data using *dataSource* option. Refer [Data Binding](working-with-data.html) section to know more about binding local and remote data to the chart.

{% highlight js %}


     $("#chartcontainer").ejChart({
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

{% include image.html url="/js/Chart/Getting-Started_images/Getting-Started_img2.png" Caption="Chart"%}

Since the data is related to sales, let us format the vertical axis labels by adding ‘$’ as a prefix and ‘K’ as a suffix to each label. This can be achieved by setting “${value}K” to the *labelFormat* option in axis. Here, {value} acts as a placeholder for each axis label, “$” and “K” are the actual prefix and suffix added to each axis label. 

The following code example illustrates this,

{% highlight js %}


     $("#chartcontainer").ejChart({
            // ... 
	        primaryYAxis:{
                //Customize the axis label format.
                labelFormat: '${value}K'
            },
	    // ...
    });


{% endhighlight %}

{% include image.html url="/js/Chart/Getting-Started_images/Getting-Started_img3.png" Caption="Chart"%}

Refer [Axis](Axis.html) section to know more about axis types, adding multiple axes and other customization options.

## Add Data Labels

You can add data labels to improve the readability of the chart. This can be achieved by enabling *visible* option in **dataLabel** option. Now, the data labels will be rendered at the top of all the data points.

The following code example illustrates this,



{% highlight js %}


     $("#chartcontainer").ejChart({
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

{% include image.html url="/js/Chart/Getting-Started_images/Getting-Started_img4.png" Caption="Chart"%}

There are situations where the default label content is not sufficient to the user. In this case, you can use *template* option to format the label content with some additional information.

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

Above HTML template will be used as a template for each data label. Here, “point.x” and “point.y” are the placeholder text used to display the corresponding data point’s x & y value.

The following code example shows how to set the id of the above template to *‘template’* option,

{% highlight js %}


     $("#chartcontainer").ejChart({
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

{% include image.html url="/js/Chart/Getting-Started_images/Getting-Started_img5.png" Caption="Chart"%}

Refer [Data Markers](Data-Markers.html) section to know more about the options available to customize it.

## Enable Legend

You can enable or disable legend using *visible* option in **legend**. By default, it is enabled in chart.

{% highlight js %}


     $("#chartcontainer").ejChart({
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

{% include image.html url="/js/Chart/Getting-Started_images/Getting-Started_img6.png" Caption="Chart"%}

Refer [Legend](Legend.html) section to know more about how to position legend and customize its appearance.

## Enable Tooltip

Tooltip is useful at situations when you cannot display information to the user using [Data Labels](data-markers.html#adding-labels) due to space constraints. You can enable tooltip by enabling *visible* option of **tooltip** in the specific series.

The following code illustrates this,

{% highlight js %}


     $("#chartcontainer").ejChart({
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

{% include image.html url="/js/Chart/Getting-Started_images/Getting-Started_img7.png" Caption="Chart"%}

Refer [Tooltip](user-interactions.html) section to know more about formatting tooltip contents and customizing its appearance.

## Add Chart Title

You need to add a title to the chart to provide quick information to the user about the data being plotted in chart. You can add it using *text* option of **title**.

{% highlight js %}


     $("#chartcontainer").ejChart({
            // ...      
            title: {
	           //Add chart title
               text: 'Sales Analysis'			
	        },
           // ....
    });


{% endhighlight %}

{% include image.html url="/js/Chart/Getting-Started_images/Getting-Started_img8.png" Caption="Chart"%}

Refer [Chart Title](chart-title.html) section to know more about aligning title, customizing its appearance and adding subtitle to the chart.
