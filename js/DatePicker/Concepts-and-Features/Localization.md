---
layout: post
title: Localization
description: localization
platform: js
control: DatePicker
documentation: ug
---

# Localization

**Localization** is language support based on the culture in **DatePicker**. You can achieve the **Localization** using “**locale”** property in **DatePicker**.

In order to enable [localization](http://help.syncfusion.com/ug/js/default.htm) refer the following scripts: **globalize.cultures.js** **and globalize.js.** The “**globalize.cultures.js**” includes different language support for **JavaScript** controls and the “**g****lobalize.js**” is a simple **JavaScript** library that allows you to format and dates based on the specified culture.

You can refer the following online link reference for **globalize.js**

[http://ajax.aspnetcdn.com/ajax/globalize/0.1.1/globalize.min.js](http://ajax.aspnetcdn.com/ajax/globalize/0.1.1/globalize.min.js)

You can refer the following online link reference for **globalize.culture.js**

[http://ajax.aspnetcdn.com/ajax/globalize/0.1.1/cultures/globalize.cultures.js](http://ajax.aspnetcdn.com/ajax/globalize/0.1.1/cultures/globalize.cultures.js)

You can dynamically change the language based on their culture.

The following steps explain you how to get the **Localization**.

* In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget

<table>
<tr>
<td>
<b>[HTML]</b>&lt;input id="datepicker" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Add the code to render the <b>Localization</b>&lt;script type="text/javascript"&gt;        $(function () {            $("#datepicker").ejDatePicker({<b>                locale: "fr-FR",</b>                buttonText: "aujourd'hui"            });        });    &lt;/script&gt;</td></tr>
</table>




*  The following screenshot displays the output for the above code.



{% include image.html url="/js/DatePicker/Concepts-and-Features/Localization_images/Localization_img1.png" Caption="Figure 14: Localization Support in DatePicker"%}

