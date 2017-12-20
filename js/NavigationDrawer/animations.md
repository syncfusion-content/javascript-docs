---
layout: post
title: animations
description: animations
platform: js
control: Navigation Drawer
documentation: ug
api: /api/js/ejnavigationdrawer
---

## Animations

You can set the transition type of the **Navigation Drawer** by using [type](https://help.syncfusion.com/api/js/ejnavigationdrawer#members:type) property. The possible transition types are **slide** and **overlay**.

* **Slide** - both navigation panel and content page slides towards left/right direction to view the navigation panel items.
* **Overlay** - Only the navigation panel slides over the content page to view the navigation panel items. That is, part of the content page is hidden under navigation panel.

N> ![C:\Users\ApoorvahR\Desktop\Note.png](animations_images\animations_img1.png)_ Transition slide type works only with fixed position._

The default value is Overlay.

{% highlight html %}

    <div id="main" style="height:1000px;">
        <div id="navigationPane">
            <ul>
                <li>Settings</li>
                <li>Read</li>
                <li>Help</li>
                <li>About</li>
            </ul>
        </div>
        <button id="drawerTarget" style="top:200px;left:600px;position:absolute"></button>
    </div>
 {% endhighlight %}
 
 Add the following code in the **script** tag.
 
 {% highlight javascript %}
 
        $("#navigationPane").ejNavigationDrawer({ type: "slide", position: "fixed", targetId: "drawerTarget", enableListView: true, listViewSettings: { width: 300 }});
        $("#drawerTarget").ejButton({ text: "OpenDrawer" });
  
{% endhighlight %}


The following screenshot illustrates the output.

![](animations_images\animations_img2.png)

Before target click
{:.caption}

![](animations_images\animations_img3.png)

After target click
{:.caption}

