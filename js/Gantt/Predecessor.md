---
layout: post
title: Predecessor
description: Predecessor
platform: js
control: Gantt
documentation: ug
api: /api/js/ejgantt
---

# Predecessor

## Predecessor offset with duration units

In Gantt, predecessor offset can be defined with the following duration units, 

* Day
* Hour
* Minute

We can define offset with various offset duration units for predecessors by using below code example

{% highlight javascript %}

var data = [
    //...
    Predecessor: "3FS+2d" { 
        //...
        Predecessor: "3FS+16h"
    },
    { 
        //...
        Predecessor: "3FS+960m"
    }
];
$("#GanttContainer").ejGantt({
    //...
    predecessorMapping: "Predecessor",
});

{% endhighlight %}

The following screen shot depicts the duration unit support in the predecessor offset.

![](/js/Gantt/Predecessor_images/Predecessor_img1.png)


