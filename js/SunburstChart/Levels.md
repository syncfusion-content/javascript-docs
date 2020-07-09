---
layout: post
title: Levels in JavaScript SunburstChart widget | Syncfusion
description: You can learn here about levels support in Syncfusion JavaScript SunburstChart control and more details.
platform: js
control: SunburstChart
documentation: ug
api: /api/js/ejsunburstchart
---

# Levels for Sunburst Chart

Sunburst chart is used to display hierarchical data. You can add more than one hierarchical data by using the [`levels`](../api/ejsunburstchart#members:levels) property of Sunburst chart. Each level of the hierarchy is represented by circle.
The following code snippet illustrates 

{% highlight js %}

        $("#chart").ejSunburstChart({
            levels: [
			{
                //... to represent the hierarchical data in different levels 
                   }
            ],
        });

{% endhighlight %}

## GroupMemberPath

It is the string property that is used to map the [`group`](../api/ejsunburstchart#members:levels-groupmemberpath) category value in the dataSource .
You can define the levels as shown in the below code example

{% highlight js %}

        $("#chart").ejSunburstChart({
            levels: [
			{ groupMemberPath: "Level 1" },
            { groupMemberPath: "Level 2" },
            { groupMemberPath: "Level 3" },
            ],
        });

{% endhighlight %}

The following screenshot illustrates the Sunburst Chart with different levels



![GroupMemberPath using SunburstChart in JavaScript](Levels_images/Levels_img1.png)
