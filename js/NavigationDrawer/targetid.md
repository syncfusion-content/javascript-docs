---
layout: post
title: targetid
description: targetid
platform: js
control: Navigation Drawer
documentation: ug
---

## TargetId

This property is used to define the target Id for **Navigation Drawer**. The drawer opens while you click on the specified target element.

{% highlight html %}

<button id="drawerTarget" style="top:200px;left:600px;position:absolute"></button>

<div id="navpane">
        <ul>
            <li>Settings</li>
            <li>Read</li>
            <li>Help</li>
            <li>About</li>
        </ul>
</div>
{% endhighlight %}
{% highlight js %}
    
        $("#navpane").ejNavigationDrawer({ position: "fixed", targetId: "drawerTarget", enableListView: true, listViewSettings: { width: 300 }});
        $("#drawerTarget").ejButton({text:"Open Drawer"});
 
{% endhighlight %}





The following screenshots illustrates the output.

{% include image.html url="targetid_images\targetid_img1.png" Caption="Before target click"%}



{% include image.html url="targetid_images\targetid_img2.png" Caption="After target click"%}

