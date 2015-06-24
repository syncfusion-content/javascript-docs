---
layout: post
title: State-Persistence
description: state persistence
platform: js
control: AutoComplete
documentation: ug
---

# State Persistence

**AutoComplete** widget can store the model value in the browser’s cookies. Every time after initial rendering, the control gets the model from the cookie only. Using **enablePersistence** property you can store the model value in cookies. So when any changes are made dynamically, the values are updated in the cookie. On refreshing the page, the previous state of the AutoComplete control is maintained in the cookie and the control is rendered from it.

## Configure state persistence of AutoComplete	

The following steps explain you how to enable state maintenance for AutoComplete.

In the **HTML** page, add an **&lt;input&gt;** element to configure AutoComplete widget.

{% highlight html %}

<input type="text" id="autocomplete" />


{% endhighlight %}


 Set **enablePersistence** to '**True**’ for AutoComplete control as follows.

{% highlight js %}

    $('#autocomplete').ejAutocomplete({
        width: 205,
        dataSource: carList,
        enablePersistence: true
    });

{% endhighlight %}


The following image is the output for **AutoComplete** when **enablePersistence** is set to ‘**True**’.

{% include image.html url="/js/Autocomplete/State-Persistence_images/State-Persistence_img1.png"%}

