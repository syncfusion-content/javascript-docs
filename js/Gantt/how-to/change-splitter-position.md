---
layout: post
title: change-splitter-position
description: change splitter position
platform: js
control: Gantt
documentation: ug
---

## Change Splitter position

In **Gantt** control, **Splitter** separates the **Treegrid** section from the **Chart** section. 

![C:\Users\labuser\Desktop\splitter.png](change-splitter-position_images\change-splitter-position_img1.png)

It is possible to change the position of the **Splitter** while loading the **Gantt** by using the **splitterPosition** property, thereby varying the width of the **Treegrid** and **Chart** sections in the control.  **SplitterPosition** property denotes the percentage of the **Treegrid** section’s width to be rendered and this property supports both pixels and percentage values.

The following code example explains how to define the **splitterPosition** property in the **Gantt**.

{% highlight js %}


$("#gantt").ejGantt(
{   

    // ...     

      splitterPosition:"50%",

    //also you can define with pixel value as 
    //‘ splitterPosition:”650” ’ (or) ‘ splitterPosition:“650px” ’


 });



{% endhighlight %}







{% include image.html url="\js\Gantt\how-to\change-splitter-position_images\change-splitter-position_img2.png" Caption="Figure 59: Gantt with 30 % splitter position"%}





{% include image.html url="\js\Gantt\how-to\change-splitter-position_images\change-splitter-position_img3.png" Caption="Figure 60: Gantt with 50% splitter position"%}

{% include image.html url="\js\Gantt\how-to\change-splitter-position_images\change-splitter-position_img4.png" Caption="Figure 61: Gantt with 600px splitter position"%}

