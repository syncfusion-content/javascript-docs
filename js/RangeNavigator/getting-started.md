---
layout: post
title: getting-started
description: getting started
platform: js
control: RangeNavigator
documentation: ug
---

# Getting Started

This section explains briefly about how to create a **RangeNavigator** in your application with **JavaScript**.

## Create your first RangeNavigator in JavaScript

This section encompasses on how to configure the **ejRangeNavigator** and update the **chart** control for **RangeNavigator’s** selected range. It also helps you to learn how to pass the required data to **RangeNavigator** and customize the scale and selected range for your requirements. In this example, you will look at the steps to configure a RangeNavigator to analyze sales of a product for a particular quarter in a year.



{% include image.html url="\js\RangeNavigator\getting-started_images\getting-started_img1.png" Caption="Figure 1: RangeNavigator to analyze sales of a product"%}

**Configure ejRangeNavigator**

Getting started with your **ejRangeNavigator** is simple. You can initialize the **ejRangeNavigator** by setting its range values.

You can create an **HTML** file as shown in the following code example.

{% highlight js %}

**[HTML]**
<!DOCTYPE html>
<html>
<head>
<script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js" type="text/javascript"></script>
<script src="http://ajax.aspnetcdn.com/ajax/globalize/0.1.1/globalize.min.js"></script>
<script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js" type="text/javascript"></script>
</head>
<body></body>
</html>


{% endhighlight %}



1. Create a &lt;div&gt; tag with an id.



{% highlight js %}

<body>
<div id="rangecontainer"  ></div>
</body>


{% endhighlight %}



2. Add a script tag inside the &lt;Body&gt; tag and add the following code example.  

The following code example renders a **RangeNavigator** with a range from 2010, January 1st to December 31st.

{% highlight js %}

**[JavaScript]**
<script type="”text/javascript"” language="”javascript"”>
        $(function () {
            $("“#rangecontainer"”).ejRangeNavigator({
                rangeSettings: {
                    start: "“2010/1/1"”, end: "“2010/12/31"”
                },
            });
        });
    </script>


{% endhighlight %}



The following screen shot displays the **RangeNavigator** with a range from 2010, January 1st to December 31st.



{% include image.html url="\js\RangeNavigator\getting-started_images\getting-started_img2.png" Caption="Figure 2: RangeNavigator with range from 2010, January 1st to December 31st."%}

**Add series**

To add series to **ejRangeNavigator,** you need to set **dataSource** property of **ejRangeNavigator** as shown in the following code example. 

You can create data source for **RangeNavigator** as follows.

{% highlight js %}

**[JavaScript]**
window.chartData = [{ "“xDate"”: new Date(2011, 0, 1), "“yValue"”: 10 },
                    { "“xDate"”: new Date(2011, 2, 1), "“yValue"”: 5 },
                    { "“xDate"”: new Date(2011, 4, 1), "“yValue"”: 15 },
                    { "“xDate"”: new Date(2011, 6, 1), "“yValue"”: 25 },
                    { "“xDate"”: new Date(2011, 8, 1), "“yValue"”: 10 },
                    { "“xDate"”: new Date(2011, 10, 1), "“yValue"”: 5 },
                    { "“xDate"”: new Date(2011, 12, 1), "“yValue"”: 15 }
];



{% endhighlight %}


Now, add the **dataSource** to the **RangeNavigator** and provide the field name to get the values from the **dataSource** in **xName** and **yName** options.

{% highlight js %}

$(function () {
            $("“#rangecontainer"”).ejRangeNavigator({
              dataSource: window.chartData, xName: "“xDate"”, yName: "“yValue"”      
            });
        });


{% endhighlight %}


The following screenshot displays a RangeNavigator with the default **“Line”** series type.



{% include image.html url="\js\RangeNavigator\getting-started_images\getting-started_img3.png" Caption="Figure 3: RangeNavigator with the default “Line” series type"%}

**Enable tooltip**

You can customize **Tooltip** for RangeNavigator using **tooltip** option. You can use **tooltipDisplayMode** option in **tooltip**,****to display the tooltip “always” or “ondemand” (displays tooltip only while dragging the sliders). You can also specify label format for tooltip using **labelFormat**.

The following code sample shows how to enable a Tooltip.

{% highlight js %}

**[JS]**
       $(function () {
          $("“#rangecontainer"”).ejRangeNavigator({
            //...…
tooltipSettings: {
visible: true, labelFormat“: "MMM/yy”yy", tooltipDisplayMode“: "alwa”ys",
          },
          //...         
         });
       });



{% endhighlight %}

The following screenshot displays the label format **Tooltip** in RangeNavigator:

{% include image.html url="\js\RangeNavigator\getting-started_images\getting-started_img4.png" Caption="Figure 4: label format Tooltip in RangeNavigator"%}

**Update Chart**

You****can use **ejRangeNavigator** with controls such as **chart** and **grid** to view the range of data selected in **ejRangeNavigator**. 

In order to update **chart**, whenever the selected range changes in **ejRangeNavigator**, you need to use **rangeChanged** event of **ejRangeNavigator** and then update the **chart** with the selected data in this event. 

You can create a chart with line series using the following code sample.

1. Create a &lt;div&gt; tag with an id.



{% highlight js %}

<body>
<div id=" chartContent "></div>
    </body>


{% endhighlight %}



2. Add a script tag inside the body tag and add the following code sample. 



{% highlight js %}

  <body>
<script type="text/javascript" language="javascript ">
$(function () {
      $("#chartContent").ejChart(
      {
         title:{ text:"Sales Analysis"},
         legend: { visible: true, position: 'top' },
primaryYAxis: {
                    title: { text: "Sales(Million)" }
                },
        series: [
        {   
        name: 'Product A', type: 'line',
        dataSource: window.chartData, xName: "xDate", yName: "yValue" 
         }                           
          ],
       });
   });
</script>
</body>



{% endhighlight %}


You can update the chart with the selected data using the **rangeChanged** event of **ejRangeNavigator**.

{% highlight js %}

$("#rangecontainer").ejRangeNavigator({
//...
dataSource: window.chartData, xName: "xDate", yName: "yValue" ,
rangeChanged: "onrangechanged",
//...
});
function onrangechanged(sender) {
    var chartobj = $("#chartContent").data("ejChart");
    if (chartobj != null) {
           chartobj.model.series[0].dataSource = sender.selectedData;
           $("#chartContent").ejChart("redraw");
       }
   }


{% endhighlight %}


The following screenshot displays how a RangeNavigator is updated when a selected range is changed.



{% include image.html url="\js\RangeNavigator\getting-started_images\getting-started_img5.png" Caption="Figure 5: RangeNavigator is updated when a selected range is changed."%}

**Set value type**

**ejRangeNavigator** can also be used with numerical values. You can specify the data type using **valueType** option. 

You can create a **dataSource** for Chart Series with integer Values using the following code sample.

{% highlight js %}

**[JavaScript]**
window.chartData = [
{ "xDate": 0, "yValue": 10 },
{ "xDate": 50, "yValue": 5 },
{ "xDate": 100, "yValue": 15 },
{ "xDate": 150, "yValue": 25 },
{ "xDate": 200, "yValue": 10 },
{ "xDate": 250, "yValue": 5 },
{ "xDate": 300, "yValue": 15 },
];


{% endhighlight %}

Now, you can set the **dataSource** for Chart Series and **valueType** property to “numeric” as given in the following code example.

{% highlight js %}

$(function () {
          $("#rangecontainer").ejRangeNavigator({
            series: [
            {
              type: 'line',
              dataSource: window.chartData, xName: "xDate", yName: "yValue" 
            }
            ],
            valueType:"numeric",
          });
       });



{% endhighlight %}


The following screenshot displays a RangeNavigator with numerical values:



{% include image.html url="\js\RangeNavigator\getting-started_images\getting-started_img6.png" Caption="Figure 6: RangeNavigator with numerical values"%}

