---
layout: post
title: Model
description: model
platform: js
control: Diagram
documentation: ug
---

# Model

The Diagram model represents the data to render the Diagram and to manipulate the Diagram elements. The following code illustrates how to define Diagram model.

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

{% include image.html url="/js/Diagram/Model_images/Model_img1.png" %}

To explore more model properties, refer [Model Properties](/js/api/ejdiagram "members").