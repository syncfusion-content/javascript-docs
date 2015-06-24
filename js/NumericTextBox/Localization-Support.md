---
layout: post
title: Localization-Support
description: localization support
platform: js
control: NumericTextbox
documentation: ug
---

# Localization Support

**Localization** is language support based on the culture in **NumericTextBox** . You can achieve the **Localization** using “**locale”** property in **NumericTextBox** . 

The widget provides multi-language support using globalization. You can customize the NumericTextBox with your own language style by using this feature. You can change the localization by using the **locale** property. The default value for **locale** property is **en-US** in NumericTextBox control.

In order to enable [localization](http://help.syncfusion.com/ug/js/default.htm) refer the following scripts: **globalize.cultures.js and globalize.js.** The “**globalize.cultures.js**” includes different language support for **JavaScript** controls and the “**globalize.js**” is a simple **JavaScript** library that allows you to format the value based on the specified culture.

You can refer the following online link reference for **globalize.js**

[http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js](http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js)

You can refer the following online link reference for **globalize.culture.js**

[http://ajax.aspnetcdn.com/ajax/globalize/0.1.1/cultures/globalize.cultures.js](http://ajax.aspnetcdn.com/ajax/globalize/0.1.1/cultures/globalize.cultures.js)

You can get the script file of various cultures from the following path also:

**"&lt;Installed Location&gt;\Syncfusion\Essential Studio\&lt;version&gt;\JavaScript\assets\external\cultures"**

You can dynamically change the language based on their culture.

**Configure Localization**

The following example describes the way to use localization for NumericTextBox widget.

{% highlight html %}

<input id="numeric" type="text" />
        
{% endhighlight %}

{% highlight js %}

        /* Numeric Textbox */
        $("#numeric").ejNumericTextbox({
            value: 12345,
            decimalPlaces: 2,
            locale: "de-DE"
        });

{% endhighlight %}







The output for **NumericTextBox** with localization.



{% include image.html url="/js/NumericTextBox/Localization-Support_images/Localization-Support_img1.png" Caption="NumericTextBox with de-DE locale"%}



{% include image.html url="/js/NumericTextBox/Localization-Support_images/Localization-Support_img2.png" Caption="NumericTextBox with en-US locale				"%}

