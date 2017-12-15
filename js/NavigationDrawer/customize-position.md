---
layout: post
title: customize-position
description: customize position
platform: js
control: Navigation Drawer
documentation: ug
api: /api/js/ejnavigationdrawer
---

## Customize Position

[Position](https://help.syncfusion.com/api/js/ejnavigationdrawer#members:position) property is used to specify the position whether it is in fixed or relative to the page. When you set a normal value to **position** property, it appears within the container. Otherwise, it appears in the whole body .The possible position values are fixed and normal. The Default value is normal.

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

        $("#navigationPane").ejNavigationDrawer({ position: "fixed", enableListView: true, listViewSettings: { width: 300 } });

{% endhighlight %}


The following screenshot illustrates the output by swiping from left to right at the left end of the screen.

![](customize-position_images\customize-position_img1.png)

