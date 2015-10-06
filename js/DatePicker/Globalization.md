---
layout: post
title: Localization
description: localization
platform: js
control: DatePicker
documentation: ug
---

# Globalization

**Globalization** is language support based on the culture in **DatePicker**. You can achieve the **Globalization** using “**locale”** property in **DatePicker**.

In order to enable [Globalization](/js/localization) refer the following scripts: **globalize.cultures.js** **and globalize.js.** The “**globalize.cultures.js**” includes different language support for **JavaScript** controls and the “**globalize.js**” is a simple **JavaScript** library that allows you to format and dates based on the specified culture.

You can refer the following online link reference for **globalize.js**

[http://ajax.aspnetcdn.com/ajax/globalize/0.1.1/globalize.min.js](http://ajax.aspnetcdn.com/ajax/globalize/0.1.1/globalize.min.js)

You can refer the following online link reference for **globalize.culture.js**

[http://ajax.aspnetcdn.com/ajax/globalize/0.1.1/cultures/globalize.cultures.js](http://ajax.aspnetcdn.com/ajax/globalize/0.1.1/cultures/globalize.cultures.js)

You can dynamically change the language based on their culture.

The following steps explain you how to get the **Globalization**.

In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget


{% highlight html %}

<input id="datepicker" type="text" />
      
{% endhighlight %}
  
{% highlight js %}

    // Add the code to render the Globalization  
    $(function() {
       $("#datepicker").ejDatePicker({
          locale: "fr-FR",
          buttonText: "aujourd'hui"
       });
    });

{% endhighlight %}



The following screenshot displays the output for the above code.



{% include image.html url="/js/DatePicker/Globalization_images/Globalization_img1.png"%}

