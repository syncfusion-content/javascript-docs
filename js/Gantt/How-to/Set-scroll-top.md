---
layout: post
title: Set-Scroll-Top
description: Set the vertical scroll position
platform: js
control: Gantt
documentation: ug
---

# Set the vertical scroll position
In Gantt it is possible to set the vertical scroller position dynamically in button click using [`setScrollTop`](/api/js/ejgantt#methods:setscrolltop) public method.

The following code example explains how to set the scroll position at button click.

{% highlight javascript %}

<button onclick="setScrollTop()">Change scroll position</button>
<div id="gantt" style="height:450px;width:700px"></div>
<script type="text/javascript">
    $("#gantt").ejGantt({});

    function setScrollTop() {
        var ganttObj = $("#gantt").data("ejGantt");
        ganttObj.setScrollTop(50);
    }
</script>

{% endhighlight %}

![](/js/Gantt/How-to/Set-Scroll-Top_images/image-1.png)
