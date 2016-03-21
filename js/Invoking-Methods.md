---
layout: post
title: Invoking methods of Syncfusion Essential JS widgets
description: How to invoke the methods of Syncfusion Essential JS widgets. 
platform: js
control: Introduction
documentation: ug
---

# Invoking Methods

The methods can be invoked the same way as the properties are accessed. The following syntaxes defines the ways to invoke the public methods of the widgets.

{% highlight javascript %}

// First way
var obj = $("jquery-selector").data("ej-plugin-name"); // [RECOMMENDED METHOD]
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


