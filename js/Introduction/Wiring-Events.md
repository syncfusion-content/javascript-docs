---
layout: post
title: Wiring-Events
description: wiring events
platform: js
control: Introduction
documentation: ug
---

## Wiring Events

Whenever the control undergoes some changes or action, it should be notified to the users properly. To notify such actions, the appropriate events are needed to be bind to the control. Events are wired the same way as jQuery events are bound, either **during or after control initialization**.

#### During Initialization

{% highlight text %}


1. $(“jquery-selector”).<ej-plugin-name>({ eventName : <eventhandler> });
**Example**:  $("#myDate").ejDatePicker({ **select**: **function () { // event handler }**  });



{% endhighlight %}



#### After initialization

{% highlight text %}


1. $(“jquery-selector”).<ej-plugin-name>(“model.eventName”, <eventhandler>);
**Example**:  $("#myDate").ejDatePicker("model.destroy" , function () {
            // event handler
         });


2. $(“jquery-selector”).on(“ej-plugin-nameeventName”, <eventhandler>);
**Example**:  $("#myDate").on("ejDatePickerdestroy", function () {
            // event handler
         }); 



{% endhighlight %}



