---
layout: post
title: Accordion-Panel-enabler
description: accordion panel enabler
platform: js
control: Accordion 
documentation: ug
api: /api/js/ejaccordion
---

# Accordion Panel enabler

## Enable/Disable widget

**You can enable or disable the Accordion** widget on initial rendering using the [enabled](https://help.syncfusion.com/api/js/ejaccordion#members:enabled) property. By default **enabled** property is set to true and the **Accordion** panels are active always. 

 The following steps explain you on how to disable the **Accordion** widget

In an HTML page, define a &lt;div&gt; element that is a container for  Accordion widget and add the contents correspondingly

{% highlight html %}
  
<div id="accordion" style="width: 500px">
    <h3>
        <a href="#">Orubase</a>
    </h3>
    <div>
        <!-- add accordion contents here to load contents under this header -->
        Orubase is the only mobile application development Framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible time frame.
    </div>
    <h3>
        <a href="#">WinRTXAML</a>
    </h3>
    <div>
        <!-- add accordion contents here to load contents under this header -->
        Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, pdf viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
    </div>
    <h3>
        <a href="#">Metro Studio</a>
    </h3>
    <div>
        <!-- add accordion contents here to load contents under this header -->
        Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
    </div>
</div>

{% endhighlight %}

{% highlight javascript %}

    // To disable the control set enabled property value as false
    $("#accordion").ejAccordion({
       enabled: false
    });

{% endhighlight %}


Output for disabled Accordion control is as follows.


![](/js/Accordion/Accordion-Panel-enabler_images/Accordion-Panel-enabler_img1.png) 

## Enable panel items

You can enable the **Accordion** widget items on initial loading using [enabledItems](https://help.syncfusion.com/api/js/ejaccordion#members:enableditems) property. This property takes array of indices whose panel needs to be enabled in **Accordion** widget. 

The [disabledItems](https://help.syncfusion.com/api/js/ejaccordion#members:disableditems) property disables the **Accordion** items based on the index. This takes array of indices whose panel is to be disabled. 

### Enabling accordion panel items

The following steps explains you on how to enable the panel items in **Accordion** widget

In an HTML page, define a &lt;div&gt; element that is a container for  Accordion widget and add the contents correspondingly

{% highlight html %}
   
<div id="accordion" style="width: 500px">
    <h3>
        <a href="#">Orubase</a>
    </h3>
    <div>
        <!-- add accordion contents here to load contents under this header -->
        Orubase is the only mobile application development Framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible time frame.
    </div>
    <h3>
        <a href="#">WinRTXAML</a>
    </h3>
    <div>
        <!-- add accordion contents here to load contents under this header -->
        Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, pdf viewer, gauges, barcode, editors, and much more. It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
    </div>
    <h3>
        <a href="#">Metro Studio</a>
    </h3>
    <div>
        <!-- add accordion contents here to load contents under this header -->
        Syncfusion Metro Studio is a collection of over 2500 Metro-style icon templates that can be easily customized to create thousands of unique Metro icons.
    </div>
</div>

{% endhighlight %}


{% highlight javascript %}

    $("#accordion").ejAccordion({
        enabledItems: [1, 2],
        disabledItems: [0],
        selectedItemIndex: 1,
        enableMultipleOpen: true
    });

{% endhighlight %}

Output for Accordion control with some enabled and disabled items, where first panel is disabled and it can’t be expanded or collapsed is as follows.



![](/js/Accordion/Accordion-Panel-enabler_images/Accordion-Panel-enabler_img2.png) 

