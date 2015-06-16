---
layout: post
title: Localization-Support
description: localization support
platform: js
control: PercentageTextBox 
documentation: ug
---

# Localization Support

**Localization** is language support based on the culture in **Textboxes**. You can achieve the **Localization** using “**locale”** property in **PercentageTextBox** . 

The **PercentageTextBox** widget provides multi-language support using globalization. You can customize the **PercentageTextBox** with your own language style by using this feature. You can change the localization by using the **locale** property. The default value for **locale** property is **en-US** in **PercentageTextBox** control.

In order to enable [localization](http://help.syncfusion.com/ug/js/default.htm) refer the following scripts: **globalize.cultures.js and globalize.js.** The “**globalize.cultures.js**” includes different language support for **JavaScript** controls and the “**globalize.js**” is a simple **JavaScript** library that allows you to format the value based on the specified culture.

You can refer the following online link reference for **globalize.js**

[http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js](http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js)

You can refer the following online link reference for **globalize.culture.js**

[http://ajax.aspnetcdn.com/ajax/globalize/0.1.1/cultures/globalize.cultures.js](http://ajax.aspnetcdn.com/ajax/globalize/0.1.1/cultures/globalize.cultures.js)

You can get the script file of various cultures from the following path also:

**"&lt;Installed Location&gt;\Syncfusion\Essential Studio\&lt;version&gt;\JavaScript\assets\external\cultures"**

You can dynamically change the language based on their culture.

## Configure Localization

The following example describes the way to use localization for **PercentageTextBox** widget.

{% highlight html %}


<table cellpadding="10">
            <tbody>
                <tr>
                    <td>
                        <label for="percent">Percent</label>
                    </td>
                    <td>
                        <input id="percent" type="text" />
                    </td>
                </tr>
            </tbody>
        </table>

{% endhighlight %}

{% highlight js %}

<script type="text/javascript">
                $("#percent").ejPercentageTextbox({
            value: 21234,
            decimalPlaces: 3,
            locale: "de-DE"
        });    
</script>

{% endhighlight %}

The output for **PercentageTextBox** with localization.



{% include image.html url="/js/PercentageTextBox/Concepts-and-Features/Localization-Support_images/Localization-Support_img1.png" Caption="Figure 24: PercentageTextBox with de-DE locale"%}



{% include image.html url="/js/PercentageTextBox/Concepts-and-Features/Localization-Support_images/Localization-Support_img2.png" Caption="Figure 25: PercentageTextBox with en-US locale				"%}

