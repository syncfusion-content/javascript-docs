---
layout: post
title: Enabling-Collapsible
description: enabling collapsible
platform: js
control: Splitter
documentation: ug
---

# Enabling Collapsible

The **Splitter** provides you the option to enable or disable the pane collapse functionality. You can click the icon in **Splitbar** to collapse or expand the corresponding pane element in **Splitter**. Setting the **collapsible** property to “**false**” disables the pane collapse functionality in the **Splitter** widget.

## Configure Collapsible

The following steps explain the implementation of the **collapsible** option in **Splitter**.

In the **HTML** page set the **&lt;div&gt;** element to render **Splitter** control.  

{% highlight html %}

<div id="splitter">
    <div>
        <div style="padding: 0px 15px;">
            <h3 class="h3">Tools </h3>
            Essential Tools is an collection of user interface components used to create interactive
                            JavaScript applications.
        </div>
    </div>
    <div>
        <div style="padding: 0px 15px;">
            <h3 class="h3">Grid </h3>
            Essential JavaScript Grid offers full featured a Grid control with extensive support for
                            Grouping and the display of hierarchical data.
        </div>
    </div>
</div>
        
{% endhighlight %}

{% highlight js %}
  
    $("#splitter").ejSplitter({
       height: 280, width: 600,
       properties: [{collapsible: true}]
    });  

{% endhighlight %}

The output for **Splitter** when **collapsible** is set to “**True**” is as follows.

{% include image.html url="/js/Splitter/Enabling-Collapsible_images/Enabling-Collapsible_img1.png" %}

The output for Splitter when **collapsible** is “**false**”.

{% include image.html url="/js/Splitter/Enabling-Collapsible_images/Enabling-Collapsible_img2.png" %}



