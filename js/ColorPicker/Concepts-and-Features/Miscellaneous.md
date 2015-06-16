---
layout: post
title: Miscellaneous
description: miscellaneous
platform: js
control: ColorPicker
documentation: ug
---

# Miscellaneous

## getValue

The **getValue**() method in **ColorPicker** returns the hexadecimal value.

* In the **HTML** page, add a **&lt;input&gt;** element to render **ColorPicker** widget

{% highlight html %}


    <input type="text" id="colorPicker" />    

{% endhighlight %}

{% highlight js %}

 
 <script>
   var ColorObj;
   jQuery(function ($) {
      ColorObj = $("#colorPicker").ejColorPicker({ value: "#278787" }).data('ejColorPicker');
      ColorObj.getValue();
    });
 </script>

{% endhighlight %}


## setValue

The **setValue**() method in **ColorPicker** is used to set the color value. The given value is in hexadecimal form.

* In the **HTML** page, add a **&lt;input&gt;** element to render **ColorPicker** widget

{% highlight html %}


    <input type="text" id="colorPicker" />    

{% endhighlight %}

{% highlight js %}
 
 <script>
   var ColorObj;
   jQuery(function ($) {
      ColorObj = $("#colorPicker").ejColorPicker().data('ejColorPicker');
      ColorObj.setValue("#278787");
    });
 </script>

{% endhighlight %}


## getColor

The **getColor**() method in **ColorPicker** control returns the color value in r,g,b,a form.

* In the **HTML** page, add a **&lt;input&gt;** element to render **ColorPicker** widget

{% highlight html %}


    <input type="text" id="colorPicker" />    

{% endhighlight %}

{% highlight js %}

 
 <script>
   var ColorObj;
   jQuery(function ($) {
      ColorObj = $("#colorPicker").ejColorPicker({value: "#278787" }).data('ejColorPicker');
      ColorObj.getColor();
    });
 </script>

{% endhighlight %}



