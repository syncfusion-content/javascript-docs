---
layout: post
title: parseandCompute
description: parseandcompute
platform: js
control: Calculate
documentation: ug
---

# Computing Formulas

When you require an algebraic expression that contains constants and function library methods, the most effective way of using **ej.calculate** is to invoke its **parseAndCompute** method. Using **CalcEngine** makes this very simple. For example, in application, add the textbox and button with **CalcEngine** objects. Now, you can type a formula in the text box and click the button to get the computed value. The following code example illustrates this.

{% highlight js %}


var value = calcObj.parseAndComputeFormula($("#formulaTxt").val());
document.getElementById("result").innerHTML = value;



{% endhighlight %}



Refer to the following screenshot that shows the computed formula value by using **parseandCompute** method.

{% include image.html url="/js/Calculate/parseandCompute_images/parseandCompute_img1.png" Caption=""%}

