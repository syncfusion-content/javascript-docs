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

//Creates diagram
$("#Diagram").ejDiagram({
   //Sets Diagram model properties
   width: "100%",
   height: "100%",
   pageSettings: {
      pageWidth: 2000,
      pageHeight: 2000
   }
});
{% endhighlight %}

![]("/js/Diagram/Model_images/Model_img1.png")

To explore more model properties, refer to [Model Properties](/js/api/ejdiagram "members").