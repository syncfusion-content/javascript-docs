---
layout: post
title: Duration-Round-Off
description: Rounding off duration
platform: js
control: Gantt
documentation: ug
---

## Round-off start date, end date and duration value on taskbar editing
In Gantt start date, end date and duration values can be round-off as per current [`scheduleHeaderSettings.scheduleHeaderType`](/api/js/ejgantt#members:scheduleheadersettings-scheduleheadertype "scheduleHeaderSettings.scheduleHeaderType") value on taskbar resizing and dragging actions. This can be achieved by setting `roundOffDuration` argument value as `true` in [`taskbarEditing`](/api/js/ejgantt#events:taskbarediting) event.

The below code example explains how to achieve this requirement. 

{% highlight javascript %}

   $("#gantt").ejGantt({
         taskbarEditing : function (args) {
                args.roundOffDuration = true;
         }
   })

{% endhighlight %}

![](Duration-Round-Off_images/OnResizing_img1.png)

Before resizing

{:.caption}

![](Duration-Round-Off_images/AfterResizing_img2.png)

After resizing

{:.caption} 