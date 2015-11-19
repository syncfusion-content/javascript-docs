---
layout: post
title: Globalization and Localization
description: Globalize formatting and Localize strings in DatePicker  
platform: js
control: DatePicker
documentation: ug
---
# Globalization

DatePicker has been provided with inbuilt localization support, so that it will be able adapt based on culture specific locale defined for it. DatePicker supports this localization with help of [jQuery.globalize.js](http://ajax.aspnetcdn.com/ajax/globalize/0.1.1/globalize.min.js) library. So you have to refer this library and the culture specific file in page in order to localize (mandatory). 

More than 350 culture specific files are available to localize the date. To know more about **‘jQuery.globalize.js’** plugin, please refer the below link [https://github.com/jquery/globalize](https://github.com/jquery/globalize#). 

N> All the culture-specific script files are available within the below specified location, once you have installed Essential Studio in your machine, therefore it is not necessary to download these files explicitly.

<table>
<tr>
<td>
(installed location)\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\assets\external\cultures\minified<br/><br/>For example, If you have installed the Essential Studio package within C:\Program Files (x86), then navigate to the below location, <br/><br/>C:\Program Files (x86)\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\assets\external\cultures\minified</td></tr>
</table>
To translate our control content from default English to any of the culture, say For example - German language, then you need to refer the globalize.culture.de-DE.min.js file in your application, after the reference of **jquery.globalize.min.js** file.

The **‘en-US’** locale is currently being used as default culture in DatePicker. You can set any other culture to DatePicker by using [locale](http://help.syncfusion.com/js/api/ejdatepicker#members:locale) property. Below code example shows German cultured DatePicker.

Refer the below German culture file in head section of html page after the reference of **‘jQuery.globalize.js’** file.

 {% highlight js %}
   
           <script src="http://cdn.syncfusion.com/js/assets/external/cultures/globalize.culture.de-DE.min.js"></script>
                
 {% endhighlight %}

Set German culture to DatePicker at initialization.

{% highlight js %}

        $(function () {

            // create DatePicker from input with current date value

            $("#datePicker").ejDatePicker({

                value: new Date(), // sets the current date

                locale: "de-DE" // sets German culture

            });

        });

{% endhighlight %}

## Watermark and Today Button Text

By default DatePicker input has **“select date”** as watermark text, you can also change this value by using [watermarkText](http://help.syncfusion.com/js/api/ejdatepicker#members:watermarktext) property. Also there’s a today button in DatePicker calendar which allows you to quick select the current date and its value can be changed by using **‘buttonText’** property.

{% highlight js %}

        $(function () {

            // creates DatePicker from input

            $("#datePicker").ejDatePicker({

                watermarkText: "enter date value",// sets watermart text in input

                buttonText: "current date" // sets button text in DatePicker calendar

            });

        });

{% endhighlight %}

Based on culture specific, only date gets localized but by changing the watermark and button text, you can completely localize the DatePicker UI too.

Refer below code example to update those value based some culture say for example English and German.

{% highlight js %}

        //create instance for datePicker.

        // only after control creation we can get dateObj otherwise it throws exception.

        var dateObj = $("#datePicker").ejDatePicker('instance');

        //condition to check English culture and change watermark and button text using dateObj.

        if (Globalize.cultureSelector == "en-US") {

            dateObj.option({ buttonText: "Today", watermarkText: "select date" })

        }

        //condition to check German culture and change watermark and button text using dateObj.

        if (Globalize.cultureSelector == "de-DE") {

            dateObj.option({ buttonText: "heute", watermarkText: "Datum auswählen" })

        }

{% endhighlight %}

