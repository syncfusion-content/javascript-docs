---
layout: post
title: Invoking-Methods
description: invoking methods
platform: js
control: Introduction
documentation: ug
---

## Invoking Methods

The functions can be invoked the same way the properties are accessed. The following syntaxes defines the ways to invoke the public methods of the widgets.


{% highlight js %}


   // First way
   var obj = $("jquery-selector").data("ej-plugin-name"); // [Recommended method]
   obj.methodName(param1, param2, param3, ...)
   //Example
   var gaugeObject = $("#gauge").data("ejCircularGauge");
   gaugeObject.setPointerValue(0, 0, 50);


   // Second way
   $("jquery-selector").ej-plugin-name("functionName");
   //Example
   $("#myDate").ejDatePicker("getValue" );


   // Third way
   $("jquery-selector").ej-plugin-name("functionName", "param1", "param2", …);
   //Example
   $("#gauge").ejCircularGauge("setPointerValue", "0", "0", "30");


{% endhighlight %}





