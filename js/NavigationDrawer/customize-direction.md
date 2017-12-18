---
layout: post
title: customize-direction
description: customize direction
platform: js
control: Navigation Drawer
documentation: ug
api: /api/js/ejnavigationdrawer
---

## Customize Direction

By using [direction](https://help.syncfusion.com/api/js/ejnavigationdrawer#members:direction) property you can set the drawer to be open from right to left direction or left to right direction. The possible direction values are Right, Left and the default value is Left. Refer to the following code example.

{% highlight html %}

    <div id="main" style="height:700px;">
        <div id="navigationPane">
            <ul>
                <li>Settings</li>
                <li>Read</li>
                <li>Help</li>
                <li>About</li>
            </ul>
        </div>
    </div>

{% endhighlight %}

Add the following code in the **script** tag.

{% highlight javascript %}
    
        $("#navigationPane").ejNavigationDrawer({ direction: "right", position: "fixed", enableListView: true, listViewSettings: { width: 300 } });

{% endhighlight %}


The following screenshot displays the output by swiping from right to left at the right side end of the screen.

![](customize-direction_images\customize-direction_img1.png)

