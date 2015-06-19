---
layout: post
title: Overview-Control
description: overview control
platform: js
control: Diagram
documentation: ug
---

# Overview Control

**Overview** control allows you to see a preview or an overall view, of the entire content of a diagram. This helps you to look at the overall picture of large diagram and also to navigate, pan or zoom, on a particular position of the page.

When you work on a very large diagram, you may not know the part you are actually working on, or navigation from one part to another, might be difficult. One solution for navigation is to zoom out of the entire diagram and find where you are. Then you can zoom in on to a particular area where you want to be. This solution is not suitable when you need some frequent navigation.

**Overview** control solves these problems by showing you a preview, that is, an overall view of the entire diagram. A rectangle indicates viewport of the diagram. Navigation becomes easy by dragging this rectangle. The following code illustrates how to create **overview** control.

{% highlight html %}

//Initialize overview
<div id="Overview"></div>
//Initialize diagram
<div id="diagram"></div>

{% endhighlight %}

{% highlight js %}

$("#diagram").ejDiagram({
        width: "1020px",
        height: "600px"
});

$("#overview").ejOverview({
       sourceID: "diagram", 
       width: "100%", 
       height: "100%" 
});

{% endhighlight %}

{% include image.html url="/js/Diagram/Overview-Control_images/Overview-Control_img1.png" Caption="Overview"%}
