---
layout: post
title: Custom-Action-Support
description: custom action support
platform: js
control: Dialog
documentation: ug
---

# Custom Action Support

The **Dialog** provides custom action buttons such as close, collapsible, maximize, minimize and pin. You can set the action buttons as per your requirement in the **Dialog**.

## Configure Custom Action

The following steps explains you the implementation of custom action. 

1. In the **HTML** page set a **&lt;div&gt;** element with dialog content for rendering the **Dialog** control. 

{% highlight html %}

     <div id="customAction" title="Audi-R8">
        <img src="Content/images/r8-coupe.png" />
        The Audi R8 was initially equipped with a 4.2 litre V8 engine. Specifically, it is an all-aluminum alloy 32-valve (four valves per cylinder) petrol engine, utilising Fuel Stratified Injection (FSI), and has a displacement of 4,163 cubic centimetres (254.0 cu in).
    </div>

{% endhighlight %}

{% highlight js %}

<script type="text/javascript">
// Set the actionButtons property in the Dialog function. The default value of actionButtons is [“close”]
    $("#customAction").ejDialog({
        width: 300,
        actionButtons: ["close", "collapsible", "maximize", "minimize", "pin"]                               
    });
</script>

{% endhighlight %}

2. The output of **actionButtons** in **Dialog** widget is as follows.

{% include image.html url="/js/Dialog/Concepts-and-Features/Custom-Action-Support_images/Custom-Action-Support_img1.png" Caption="Dialog with “actionButtons                                                   "%}

