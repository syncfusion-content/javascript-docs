---
layout: post
title: Wiring events of Syncfusion Essential JS widgets
description: How to wire the events of syncfusion essential js widgets
platform: js
control: Introduction
documentation: ug
---

# Wiring Events

Essential JS widgets events can be wired the same way as jQuery events are bound, either during or after control initialization.

## During Initialization

{% highlight js %}

$("jquery-selector").ej-plugin-name({ eventName : "eventhandler" });
//Example
$("#myDate").ejDatePicker({ select: function () { 
          // event handler 
   }  
});
   
{% endhighlight %}

## After initialization

{% highlight js %}

// First way
$("jquery-selector").ej-plugin-name("model.eventName", "eventhandler");
//Example
$("#myDate").ejDatePicker("model.destroy" , function () {
      // event handler
});

// Second way
$("jquery-selector").on("ej-plugin-nameEventName", "eventhandler");
//Example
$("#myDate").on("ejDatePickerdestroy", function () {
      // event handler
}); 

{% endhighlight %}


