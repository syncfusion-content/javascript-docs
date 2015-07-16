---
layout: post
title: Drill-Operation
description: drill operation
platform: js
control: OlapChart
documentation: ug
---

#Drill Operation

This is a basic feature of OlapChart through which the amount of information can be limited (for a better view). It allows you to drill down to access the detailed level of data or drill up to see the summarized data by using the context menu present in the OlapChart.
 
Drill up (also called roll up) navigates from more detailed data to less detailed data i.e. by climbing up a concept hierarchy for a dimension.
 
Drill down (also called roll down) is the reverse of drill up. It navigates from less detailed data to more detailed data. i.e. by climbing down a concept hierarchy for a dimension.

{% include image.html url="/js/OlapChart/Drill-Operation_images/Drill_img1.png" Caption="Drill-down operation in OLAP Chart"%}

{% include image.html url="/js/OlapChart/Drill-Operation_images/Drill_img2.png" Caption="Drill-up Operation in OLAP Chart"%}

DrillSuccess event will get triggered when we right click on the OlapChart and select any option available from the context menu to perform drill up or drill down operation.

{% highlight js %}

$(function()
{
    $("#OlapChart").ejOlapChart(
    {
        url: "../wcf/OlapChartService.svc",
        drillSuccess: "drillSuccess"
    });
});

function drillSuccess(args)
{
    alert("Drill Success");
}

{% endhighlight %}



