---
layout: post
title: Model
description: model
platform: js
control: Diagram
documentation: ug
---

# Model

The **Diagram** model represents data for rendering the Diagram and manipulating the Diagram elements. The following code illustrates how to create a **Diagram** with some model properties.

{% highlight js %}

//create diagram
$("#Diagram").ejDiagram({
   //set diagram model properties
   width: "100%",
   height: "100%",
   pageSettings: {
      pageWidth: 2000,
      pageHeight: 2000
   }
});
{% endhighlight %}

{% include image.html url="/js/Diagram/Model_images/Model_img1.png" Caption="Model"%}
