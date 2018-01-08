---
layout: post
title: Configure-Collapsible-and-Expandable-properties
description: configure collapsible and expandable properties
platform: js
control: Splitter
documentation: ug
api: /api/js/ejsplitter
---

# Configure Collapsible and Expandable properties

The **Splitter** provides you the [option](https://help.syncfusion.com/api/js/ejsplitter#members:properties) to enable or disable the pane collapse functionality. You can click the icon in **Split bar** to collapse or expand the corresponding pane element in **Splitter**. Setting the **collapsible** property to “**false**” disables the pane collapse functionality in the **Splitter** widget.

## Enabling Collapsible

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

{% highlight javascript %}
  
    $("#splitter").ejSplitter({
       height: 280, width: 600,
       properties: [{collapsible: true}]
    });  

{% endhighlight %}

The output for **Splitter** when **collapsible** is set to “**true**” is as follows.

![](/js/Splitter/Enabling-Collapsible_images/Enabling-Collapsible_img1.png) 

The output for Splitter when **collapsible** is “**false**”.

![](/js/Splitter/Enabling-Collapsible_images/Enabling-Collapsible_img2.png) 

## Disable Expandable

The following steps explain the implementation of the **expandable** option in **Splitter**.

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

{% highlight javascript %}
  
    $("#splitter").ejSplitter({
       height: 280, width: 600,
       properties: [{expandable:false},{collapsible: false}]
    });  

{% endhighlight %}

The output for Splitter when **expandable** is “**false**”.

![](/js/Splitter/Enabling-Collapsible_images/Enabling-Collapsible_img3.png) 



