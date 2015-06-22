---
layout: post
title: State-Persistence
description: state persistence 
platform: js
control: DatePicker
documentation: ug
---

# State Persistence 

It **Enables** or **Disables** the **state maintenance** of **DatePicker.** **DatePicker** widget can store the model value in the browser cookies and on every time after initial rendering, the control gets the model from the cookie only. Using **enablePersistence** property, you can store the model value in cookies. So when any changes are made dynamically then those values are updated in cookie. On refreshing the page, the past state of the **DatePicker** widget is rendered from cookies. By default “**enablePersistence**” property is set as ‘**false**’ in **DatePicker**.

The following steps explain you how to enable the **state maintenance** for **DatePicker** widget.

In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget

 {% highlight html %}
 
      <input id="datepicker" type="text" />
      
  {% endhighlight %}
  
  {% highlight js %}

        // Add the code to enable the state maintenance for DatePicker widget
        $(function () {
            // declaration
            $("#datepicker").ejDatePicker({
                enablePersistence: true
            });
        });


  {% endhighlight %}


