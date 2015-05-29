---
layout: post
title: localization-support
description: localization support
platform: js
control: CurrencyTextBox Editors 
documentation: ug
---

# Localization Support

**Localization** is language support based on the culture in **CurrencyTextBox Textboxes**. You can achieve the **Localization** using “**locale”** property in **CurrencyTextBox Textboxes**. 

The **CurrencyTextBox Textbox** widget provides multi-language support using globalization. You can customize the **CurrencyTextBox Textbox** with your own language style by using this feature. You can change the localization by using the **locale** property. The default value for **locale** property is **en-US** in **CurrencyTextBox Textbox** controls.

In order to enable [localization](http://help.syncfusion.com/ug/js/default.htm) refer the following scripts: **globalize.cultures.js and globalize.js.** The “**globalize.cultures.js**” includes different language support for **JavaScript** controls and the “**globalize.js**” is a simple **JavaScript** library that allows you to format the value based on the specified culture.

You can refer the following online link reference for **globalize.js**

[http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js](http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js)

You can refer the following online link reference for **globalize.culture.js**

[http://ajax.aspnetcdn.com/ajax/globalize/0.1.1/cultures/globalize.cultures.js](http://ajax.aspnetcdn.com/ajax/globalize/0.1.1/cultures/globalize.cultures.js)

You can get the script file of various cultures from the following path also:

**"&lt;Installed Location&gt;\Syncfusion\Essential Studio\&lt;version&gt;\JavaScript\assets\external\cultures"**

You can dynamically change the language based on their culture.

## Configure Localization

The following example describes the way to use localization for **CurrencyTextBox Textbox** widgets.

{% highlight html %}

**[HTML]**

<table cellpadding="10">
            <tbody>
                <tr>
                    <td>
                        <label for="numeric">Numeric</label>
                    </td>
                    <td>
                        <input id="numeric" type="text" />
                    </td>
                </tr>
                <tr>
                    <td>
                        <label for="percent">Percent</label>
                    </td>
                    <td>
                        <input id="percent" type="text" />
                    </td>
                </tr>
                <tr>
                    <td>
                        <label for="currency">Currency</label>
                    </td>
                    <td>
                        <input id="currency" type="text" />

                    </td>
                </tr>
            </tbody>
        </table>
        <script type="text/javascript">
        /* Numeric Textbox */
        $("#numeric").ejNumericTextbox({
            value: 12345,
            decimalPlaces: 2,
**locale: "de-DE"**
        });
        /* Percent Textbox */
        $("#percent").ejPercentageTextbox({
            value: 21234,
            decimalPlaces: 3,
**locale: "de-DE"**

        });
        /* Currency Textbox */
        $("#currency").ejCurrencyTextbox({
            value: 33,
            decimalPlaces: 2,
**locale: "de-DE"**
        });
    </script>


{% endhighlight %}





**[_cshtml]**

@* **Add the following code in your view page to render Textbox controls.***@

@Html.EJ().NumericTextbox("numeric").Value("12345").**Locale**("**de-DE**")

@Html.EJ().PercentageTextbox("percentage").Value("21234").**Locale**("**de-DE**")

@Html.EJ().CurrencyTextbox("currency").Value("33").**Locale**("**de-DE**")



**[_aspx]**

&lt;%-- Add the following code in your aspx page to render Textbox controls.--%&gt;

&lt;ej:NumericTextBox ID="numeric" Value="12345" Locale="de-DE" runat="server"&gt;&lt;/ej:NumericTextBox&gt;

&lt;ej:PercentageTextBox ID="percentage" Value="21234" Locale="de-DE" runat="server"&gt;&lt;/ej:PercentageTextBox&gt;

&lt;ej:CurrencyTextBox ID="currency" Value="33" Locale="de-DE"  runat="server"&gt;&lt;/ej:CurrencyTextBox&gt;



The output for **CurrencyTextBox Textboxes** with localization.



{% include image.html url="\js\Currency\concepts-and-features\localization-support_images\localization-support_img1.png" Caption="Figure 322440: CurrencyTextBox Textbox with de-DE locale"%}{% include image.html url="\js\Currency\concepts-and-features\localization-support_images\localization-support_img2.png" Caption="Figure 322440: CurrencyTextBox Textbox with de-DE locale"%}



{% include image.html url="\js\Currency\concepts-and-features\localization-support_images\localization-support_img3.png" Caption="Figure 413325: CurrencyTextBox Textbox with en-US locale				"%}{% include image.html url="\js\Currency\concepts-and-features\localization-support_images\localization-support_img4.png" Caption="Figure 413325: CurrencyTextBox Textbox with en-US locale				"%}

